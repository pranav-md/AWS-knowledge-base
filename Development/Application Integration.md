
## Amazon SNS (Simple Notification Service)
- Message publishing and processing service (PubSub)
- Allows fanout to millions of consumers (Email, HTTP, endpoint, SQS, Texting).
- Fully managed and durable with automatic scaling.
- Consists of topics and subscriptions.
Features:
- Application to person OR Application to Application messaging.
- Standard and FIFO topics.
- Message durability .
- Message archiving, replay, and analytics
- Message attributes - Metadata of the messages.
- Message filter policies for each subscribers.
- Message security by protecting contents in message.


                      +----------------------+
                      |    Order Placement   |
                      |       (Customer)     |
                      +-----------+----------+
                                  |
                                  v
                           +---------------+
                           | Order Service |
                           | (Publisher)   | Publishes "order placed"
                           +-------+-------+
                                  |
                                  v
                       +------------------------+
                       | SNS Topic: OrderEvents |
                       +------------------------+
                            | There are 3 subscribers for the Topic "OrderEvents"
       +---------------+----------------------+
       |               |                      |
       v               v                      v
 +-------------+            +------------+              +-------------+
 | SQS Queue  |            | SQS Queue   |              | Lambda       |
 | for                |            | for Payment  |              | Function for |
 | Restaurant   |            | Service           |              | Notification |
 | Service         |            +------------+              +-------------+
 +-------------+                         |                                        |
                        v                                       v
                       +-------------------+       +------------------+
                       | Restaurant System |       | Email/SMS Service |
                       +-------------------+       +------------------+
                       (App to App)                   (App to Person)
### Scenario: Application to Person 
Zomato promotion topic to customer category 1,2,3.
### Scenario: Application to Application
Zomato Customer order service, publish message to "Customer Order Topic" which calls applications such as AWS Lambda, NodeJS App etc.

### Pricing
No upfront costs, pay based on number of the messages published, notifications delivered.

## Amazon SQS (Simple Queue Service)



## Amazon SWF (Simple Workflow Service)



## AWS Step Functions



## Amazon EventBridge



## Send Fanout Event Notifications with Amazon Simple Queue Service (SQS) and Amazon Simple Notification Service (SNS)
