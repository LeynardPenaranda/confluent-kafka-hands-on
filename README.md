# confluent-kafka-hands-on

Welcome to the **confluent-kafka-hands-on** repository! 🚀  
This project is a hands-on walkthrough of using **Confluent Kafka** with Python, covering topic creation, client setup, producer configuration, and sending messages into a Kafka topic.

This repository is aimed at helping you understand:

- 📌 Creating and managing topics in Confluent Cloud  
- 🔑 Creating a Kafka client and getting connection credentials  
- 🧾 Preparing source data for Kafka messages  
- 🧑‍💻 Initializing a producer using `confluent-kafka`  
- 📤 Sending a single message to a Kafka topic  
- 🔄 Understanding the basic message flow from local data to Confluent Cloud  

---

## 🖥️ Creating a Kafka cluster and topic in Confluent Cloud

### 🔹 Creating a new topic in the cluster
After creating a cluster in **Confluent Kafka**, the next step is to create a topic where messages will be stored and consumed. In this project, the topic created is named **`ecommerce`**.

<p align="center">
  <img src="https://github.com/LeynardPenaranda/confluent-kafka-hands-on/blob/main/images/sending-one-message/creating%20new%20topic%20in%20the%20cluster_0.png" width="900" alt="Creating a new topic in the Confluent Kafka cluster">
</p>

---

### 🔹 Topic successfully created inside the cluster
Once the topic is created, Confluent confirms that the new topic is available inside the cluster and ready to receive messages.

<p align="center">
  <img src="https://github.com/LeynardPenaranda/confluent-kafka-hands-on/blob/main/images/sending-one-message/topic%20successfully%20created.png" width="900" alt="Topic successfully created inside the cluster">
</p>

---

## 📨 Producing a manual test message in the topic

### 🔹 Producing a manual message inside the `ecommerce` topic
Before sending messages programmatically, a manual message was first produced directly inside the **`ecommerce`** topic. In this example, the message was created with an empty value and a key of **`123`**.

<p align="center">
  <img src="https://github.com/LeynardPenaranda/confluent-kafka-hands-on/blob/main/images/sending-one-message/produce%20a%20message%20inside%20the%20topic%20ecommerce.png" width="900" alt="Producing a manual message inside the ecommerce topic">
</p>

---

### 🔹 Manual message successfully created
This confirms that the topic is working correctly and is able to receive messages inside the cluster.

<p align="center">
  <img src="https://github.com/LeynardPenaranda/confluent-kafka-hands-on/blob/main/images/sending-one-message/message%20created%20successfully.png" width="900" alt="Manual message created successfully">
</p>

---

## 🔑 Creating a Kafka client and getting configuration

### 🔹 Creating a new client in Confluent
To connect an external application such as Python or Google Colab to Confluent Cloud, a new client must be created. This provides the required configuration, including the **API key** and **API secret**.

<p align="center">
  <img src="https://github.com/LeynardPenaranda/confluent-kafka-hands-on/blob/main/images/sending-one-message/creating%20a%20client%20in%20cluster_0.png" width="900" alt="Creating a new client in Confluent Kafka">
</p>

---

## 📂 Preparing the source data in Google Colab

### 🔹 Uploading `customer.csv` and converting it to `customers.json`
In Google Colab, the source file **`customer.csv`** was uploaded and converted into **`customers.json`** so the data could be used for producing Kafka messages.

<p align="center">
  <img src="https://github.com/LeynardPenaranda/confluent-kafka-hands-on/blob/main/images/sending-one-message/created%20a%20json%20file%20of%20customer.csv%20in%20google%20colab.png" width="900" alt="Creating a JSON file from customer.csv in Google Colab">
</p>

---

## ⚙️ Initializing the Kafka configuration and producer

### 🔹 Initializing the configuration and creating a producer
Using the configuration generated from the Confluent client, the Kafka connection settings were initialized in **Google Colab**. After that, a **producer** was created using the `confluent-kafka` library.

<p align="center">
  <img src="https://github.com/LeynardPenaranda/confluent-kafka-hands-on/blob/main/images/sending-one-message/initialize%20the%20configuration%20and%20created%20a%20producer.png" width="900" alt="Initializing the configuration and creating a producer">
</p>

---

## 📤 Sending one message to Confluent Kafka

### 🔹 Reading `customers.json` and selecting the first record
For this first exercise, only **one message** is sent to Confluent Kafka. The topic name from Confluent was stored in a variable named **`topic`**, then the `customers.json` file was opened and stored in a variable named **`customers_data`**. From there, the first record and its key were selected.

<p align="center">
  <img src="https://github.com/LeynardPenaranda/confluent-kafka-hands-on/blob/main/images/sending-one-message/opening%20the%20customers.json%20and%20taking%20its%20first%20value%20and%20key.png" width="900" alt="Opening customers.json and selecting the first key and value">
</p>

---

### 🔹 Converting the key and value to bytes before sending
Since Kafka expects message keys and values in byte format, the selected key and value were first converted to bytes. After that, the message was sent to Confluent using the producer created earlier.

<p align="center">
  <img src="https://github.com/LeynardPenaranda/confluent-kafka-hands-on/blob/main/images/sending-one-message/converting%20the%20key%20and%20value%20first%20to%20bytes%20then%20sending%20the%20first%20message%20to%20Confluent.png" width="900" alt="Converting key and value to bytes before sending to Confluent">
</p>

---

### 🔹 Successfully sending the first message to the `ecommerce` topic
This confirms that the Python producer was able to connect to Confluent Cloud and successfully publish the first message to the **`ecommerce`** topic.

<p align="center">
  <img src="https://github.com/LeynardPenaranda/confluent-kafka-hands-on/blob/main/images/sending-one-message/successfully%20send%20the%20first%20message%20to%20ecommerce%20topic.png" width="900" alt="Successfully sending the first message to the ecommerce topic">
</p>

---

## 💡 Additional notes

- This walkthrough focuses on **sending one message only** to Confluent Kafka.
- The **next step** in this project is **sending multiple messages to Confluent Kafka**.
- The setup shown here is intended for **learning and hands-on practice** using Confluent Cloud.
- Always keep your **API key**, **API secret**, and Kafka client configuration secure. Never expose real credentials in a public repository.

---

Feel free to explore the code and screenshots in this repository to better understand the full message flow using **Confluent Kafka** and Python. Happy learning and happy streaming! 🎉
