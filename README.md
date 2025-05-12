1) How much data your publisher program will send to the message broker in one run?

    The program sends five messages, each containing a serialized UserCreatedEventMessage using Borsh. Each message includes a user ID and user name, with an estimated size of about 24 bytes. The total data sent is roughly 120 bytes

2) The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?

    The URL being the same in both the publisher and subscriber programs means that they are connecting to the same RabbitMQ message broker instance running locally on the default AMQP port 5672, using the default username and password guest. This ensures that both programs are communicating through the same messaging server, allowing the messages published by the sender to be received by the subscriber

- Running RabbitMQ as message broker.

    ![alt text](img/image.png)

- Sending and processing event.

    ![alt text](img/image2.png)