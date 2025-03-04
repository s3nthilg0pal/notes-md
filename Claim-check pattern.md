# Claim-check pattern

as applications grow in complexity, they often need to handle larger messages containing images, documents, sensitive information or complex data structures. This is where traditional messaging patterns face challenges – message size limits, increased latency, and higher costs can impact system performance.


# Architecture
![enter image description here](https://arinco.com.au/wp-content/uploads/2025/02/ClaimCheckPattern-1024x404.jpg)


## Solution

By using the claim-check pattern, large messages no longer must be sent to messaging systems. Instead, the content/payload of the message can be sent to an external data store such as Azure Storage Accounts. A claim-check token is created which has references to the payload in the data store. This token is then sent to the receiving application (the subscriber) which can be used to retrieve the payload from the data store.

## Variations

#### In-process deletion
![enter image description here](https://arinco.com.au/wp-content/uploads/2025/02/image-5-1024x404.png)
#### External service
![enter image description here](https://arinco.com.au/wp-content/uploads/2025/02/image-4.png)

### References

 - https://arinco.com.au/blog/optimising-message-processing-azure/
