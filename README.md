# Delayed Message Service

This is a simple Delayed Message Service implemented in Java, using DynamoDB as the persistence layer. The service allows you to schedule delayed messages and retrieve them when their scheduled delivery time has elapsed.

**Note: All code in this project is generated through chat GPT.**

## Features

- **Scheduled Message Creation**: The service provides an API to create delayed messages by specifying the scheduled delivery time and the message payload.
- **Message Retrieval**: You can retrieve delayed messages that have reached their scheduled delivery time.
- **Message Update**: You have the ability to update the scheduled delivery time or payload of a delayed message.
- **Message Deletion**: You can delete delayed messages based on their message ID.

## Technology Stack

- Java
- AWS DynamoDB
- Spring Boot (Future Integration)
- JUnit (Future Integration)

## Setup Instructions

1. Clone the repository.
2. Open the project in your preferred IDE.
3. Configure your AWS credentials for DynamoDB access (ensure you have the necessary permissions).
4. Run the application.
5. Use the provided API endpoints to interact with the Delayed Message Service.

## API Contracts

The API contracts for the Delayed Message Service are defined as follows:

- **Create Delayed Message**
  - Endpoint: `/messages`
  - Method: `POST`
  - Request Body:
    ```json
    {
      "scheduledDeliveryTime": 1234567890,
      "payload": "Hello, World!"
    }
    ```

- **Get Delayed Message**
  - Endpoint: `/messages/{messageId}`
  - Method: `GET`

- **Update Delayed Message**
  - Endpoint: `/messages/{messageId}`
  - Method: `PUT`
  - Request Body:
    ```json
    {
      "scheduledDeliveryTime": 1234567890,
      "payload": "Hello, Updated World!"
    }
    ```

- **Delete Delayed Message**
  - Endpoint: `/messages/{messageId}`
  - Method: `DELETE`

## Contribution

This project is a demonstration of using chat GPT to generate code, and it is not actively maintained. However, feel free to fork the repository and adapt the code to your specific needs. Contributions are welcome.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
