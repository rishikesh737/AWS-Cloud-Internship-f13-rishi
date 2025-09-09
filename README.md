#AWS Cloud Internship Projects
This repository serves as a portfolio of the projects I completed during my internship as an AWS Cloud Intern at F13 Technologies. The work showcased here demonstrates my practical experience with various AWS services and my ability to build full-stack, scalable applications.

I primarily used JavaScript and ReactJS for the front-end components and leveraged the AWS Amplify CLI and AWS Console for backend configuration and deployment.

##1. Event Management Platform
( NOTE : The live site will be decommissioned as backend AWS services are removed )
This project is a complete event management platform designed to handle the full event lifecycle, from event creation and attendee registration to digital ticket issuance and validation. It features separate user interfaces for event organizers and attendees.

🚀 How the App Works
The platform provides a comprehensive set of features to streamline event management:

User & Admin Interfaces: The application provides two distinct user interfaces. Organizers can create and manage their events and view registrant data, while attendees can browse events, register, and download their digital tickets.

Authentication & User Roles: AWS Cognito is used to implement secure sign-up and login flows. User roles (organizer, attendee) are managed through Cognito Groups to ensure proper access control.

Data Management: Amazon DynamoDB serves as the NoSQL database to store critical data, including event details, user registrations, and ticket metadata such as a QR code ID and its validation status.

Ticket Generation: A serverless AWS Lambda function is triggered automatically upon successful registration to generate a PDF ticket. This ticket includes an embedded QR code for seamless validation at event entry points.

Payment Integration: The system supports simulated payments via an optional integration with Stripe in test mode.

🛠️ Technologies Used
This application is built on a scalable, serverless architecture using a combination of web technologies and AWS services.

Frontend:

ReactJS & JavaScript: For building dynamic and responsive user interfaces.

Backend & Cloud Services:

AWS Cognito: For user authentication and role management.

Amazon DynamoDB: A fast, flexible NoSQL database for structured data storage.

AWS Lambda: Serverless compute for generating tickets.

AWS S3 & CloudFront: Used for hosting the front-end application and storing ticket PDFs.

Stripe: Integrated in test mode for mock payment processing.

🔗 Deployment & Version Control:
GitHub: The primary platform for version control.

AWS Amplify Console: Used for continuous deployment and hosting, automating the build and deployment process to a global Content Delivery Network (CDN).

##2. AI Chatbot for IT Support
( NOTE : The live site will be decommissioned as backend AWS services are removed )
This project involves a chatbot that acts as a first-line IT support assistant. It is designed to handle common user queries and seamlessly escalate unrecognized issues to human agents via email.

🚀 How the App Works
The chatbot provides an intelligent and automated IT support experience:

Bot Development: Amazon Lex is used to build the core chatbot. It is trained to understand user intents such as "Password reset," "Wi-Fi issues," and "Email access troubleshooting."

Backend Response Handling: AWS Lambda functions are used to query a DynamoDB-based FAQ database for relevant responses.

Fallback Workflow: If the chatbot cannot find a suitable answer, the user's query is automatically routed to an Amazon SES email address (or stored in a database) for human review and response.

Frontend Integration: The chatbot is embedded on a webpage hosted via AWS S3, providing real-time interaction and fallback suggestions.

Monitoring & Feedback Loop: All user queries are logged in DynamoDB to monitor the bot's performance and confidence scores, providing valuable data for future training and improvement.

🛠️ Technologies Used
This application leverages AWS's powerful AI and serverless services to create an intelligent and automated support solution.

Frontend:

HTML & JavaScript: For the user interface and embedding the chatbot.

Backend & Cloud Services:

Amazon Lex: An AI service for building conversational interfaces.

Amazon DynamoDB: A NoSQL database for storing FAQs and user query logs.

AWS Lambda: Serverless functions for backend logic and database queries.

Amazon SES: A scalable email service for sending alerts and notifications.

IAM: For managing and securing access to AWS resources.

🔗 Deployment & Version Control:
GitHub: The primary platform for version control.

AWS S3: Used for hosting the front-end application.

##3. Daily Expense Tracker with Analytics Dashboard
( NOTE : The live site will be decommissioned as backend AWS services are removed )
This is a personal finance web application that allows users to track expenses, categorize them, and gain valuable insights into their spending habits through interactive charts and graphs.

🚀 How the App Works
The application empowers users to manage their finances effectively:

User Authentication: Secure user registration and login are implemented using AWS Cognito, ensuring data privacy.

Expense Logging: The application uses REST APIs (created with API Gateway and Lambda) to log user transactions in a DynamoDB database. Each transaction includes details like category, date, amount, and notes.

Frontend Dashboard: A responsive web dashboard, built with React, allows users to add, edit, and delete expenses. The dashboard features visualizations (using Chart.js) to show weekly, monthly, and annual spending trends.

Analytics & Alerts: The dashboard provides budget insights and can generate alerts (via SNS or on-page prompts) when spending approaches a set limit.

Personalized Experience: The application offers a personalized greeting based on the time of day and user's profile, along with a theme toggle for a light or dark interface.

🛠️ Technologies Used
This application is built on a robust full-stack architecture leveraging cutting-edge web technologies and AWS cloud services.

Frontend:

ReactJS & JavaScript: For building dynamic and interactive user interfaces.

Chart.js: A JavaScript library for creating data visualizations.

Backend & Cloud Services:

AWS Cognito: For user authentication.

Amazon API Gateway: For creating and managing REST APIs.

AWS Lambda: Serverless functions handling business logic.

Amazon DynamoDB: A NoSQL database for storing user transactions.

AWS Amplify & S3: For deployment and hosting.

🔗 Deployment & Version Control:
GitHub: The primary platform for version control.

AWS Amplify: Used for continuous deployment and hosting of the front-end.

Repository Links:

<a href="https://github.com/rishikesh737/EventSphereFrontEnd">Event Management Platform </a>

<a href="https://github.com/rishikesh737/IT-Support-Chatbot-AWS">AI Chatbot for IT Support </a>

<a href="https://github.com/rishikesh737/expense-tracker-fullstack">Daily Expense Tracker </a>
