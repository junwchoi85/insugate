# Insugate

### **Project Overview**

This project is the complete rebuild of the Insugate website, replacing the legacy PHP system with a modern, cloud-native architecture in a single, large-scale deployment event (Big Bang approach). The goal is to establish a robust and scalable platform with enhanced functionality, improved performance, and a superior user experience.

### **1. Current System Analysis (Legacy)**

The existing system is a monolithic application with a mixed technology stack of PHP, MySQL, and Java/JSP, running on an Apache/Tomcat environment. This architecture has reached its technical limits in terms of scalability and maintenance.

* **Technology Stack**: PHP (EUC-KR encoded), MySQL, jQuery, JavaScript.
* **Core Functionality**: The system manages guarantee insurance applications and related administrative tasks.
* **Architecture**: The core system is tightly coupled, making feature development and maintenance difficult.

### **2. Target System Architecture **

The new system will be a complete overhaul, built on a microservices architecture and deployed to the Google Cloud Platform.

* **Frontend**: A modern Single Page Application (SPA) developed with **Angular 20**, providing a highly responsive and dynamic user interface. The application will be deployed to Firebase Hosting for fast, global delivery.
* **Backend**: A suite of microservices developed using **Java 21** and the **Spring Boot** framework. Key components include:
    * **Spring Security** for modern, token-based authentication (e.g., JWT).
    * **Spring AI** to integrate conversational features (chatbots) into the customer support workflow.
* **Database**: **MySQL** will be used for persistent data storage, hosted on a managed service like Google Cloud SQL to ensure high availability and scalability.
* **Asynchronous Messaging**: **Apache Kafka** will be implemented to handle asynchronous communication between microservices, ensuring a decoupled and resilient system. For example, a new application event could be published to a Kafka topic, and multiple services (e.g., notification, billing) could consume this event independently.
* **Deployment**: The entire application will be containerized with **Docker** and orchestrated using **Kubernetes** on the **Google Cloud Kubernetes Engine (GKE)**, enabling automated scaling, self-healing, and efficient resource management.

### **3. Key Features & User Stories**

The renewed system will provide a comprehensive set of features for both end-users and administrators.

#### **User Perspective (End-User)**
* **Sign-up/Login**: Users can sign up with an ID/password or through social login. Business registration documents must be submitted for approval.
* **Application**: A streamlined process allows users to apply for guarantee insurance and complete payment.
* **My Page**: A central hub for users to view and manage their profile, application history, and policy status.
* **Support Chatbot**: An integrated **Spring AI** chatbot will provide instant answers to common questions and assist with the application process.

#### **Administrator Perspective (Admin)**
* **User Management**: Administrators can efficiently review and manage user accounts, including document verification and account approval.
* **Application Management**: A robust dashboard will allow administrators to search, filter, and manage all insurance applications.
* **Operational Efficiency**: Routine tasks will be automated through APIs, reducing manual work and increasing overall efficiency.
