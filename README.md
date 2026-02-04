# EC2 State Change Notification using AWS

## Overview
This project detects when an Amazon EC2 instance is stopped or terminated and sends an email notification automatically using AWS services.

## Problem Statement
Manually checking EC2 instance status is not efficient. This project provides an automatic alert system whenever an EC2 instance changes its state.

## AWS Services Used
- Amazon EC2
- Amazon EventBridge (CloudWatch Events)
- Amazon SNS
- IAM

## Architecture
EC2 → EventBridge → SNS → Email Notification

## How It Works
1. An EC2 instance changes its state to STOPPED or TERMINATED.
2. Amazon EventBridge captures the state change event.
3. EventBridge triggers an SNS topic.
4. SNS sends an email notification to the subscribed user.

## Implementation Steps
1. Create an SNS topic and add an email subscription.
2. Confirm the email subscription.
3. Create an EventBridge rule for EC2 state change events.
4. Configure SNS as the target for the rule.
5. Test by stopping or terminating the EC2 instance.

## Testing
-> Stopped EC2 instance → Email notification received.
-> Terminated EC2 instance → Email notification received.

## Cost
This project uses AWS Free Tier services and does not incur significant cost.

## Notes
-> SNS email subscription must be confirmed.
-> All AWS services must be in the same region.
-> No web application or log analysis is required.

## Conclusion
This project demonstrates an event-driven AWS architecture for monitoring EC2 instance state changes and sending notifications.

## Screenshots
- SNS Topic configuration
- SNS email subscription (Confirmed)
- EventBridge rule for EC2 state change
- Email notification received after stopping EC2

