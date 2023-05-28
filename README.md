# Happy News DAO Project

Welcome to the Happy News repository! This repository contains the source code for Happy News DAO, a platform dedicated to sharing positive news articles and uplifting stories from anyone around the world.

This project aims to create a decentralized news platform where journalists can submit and publish news articles while ensuring authenticity, sentiment analysis, and proper payment processing. The project is divided into multiple modules, each responsible for specific functionalities. Happy News is meant to be autonomous and operate without any human input once a "Fresh Article" is submitted on the twitter profile page. After that, each module below is meant to be autonomous and not require any human input, aside from Module E, which will be monitored for the "self-adjusting" sentiment features and analysis that process the "Fresh Articles" as they are submitted.

## Website

To access the live version of the HappyNews.DAO website, visit [HappyNews.DAO](happynews.dao). Please note that to view the website, you'll need a compatible web browser.

- For Google Chrome users, it is recommended to install the [Unstoppable Domains Extension](https://unstoppabledomains.com/extension) to seamlessly access decentralized domain hosting.

- Brave browser users can directly visit [HappyNews.DAO](happynews.dao) without the need for any additional extensions. If you don't have the Brave browser, you can download it from the official website: [Download Brave Browser](https://brave.com/)

## Prerequisites

- Web browser (Google Chrome or Brave)
- [Unstoppable Domains Extension](https://unstoppabledomains.com/extension) (for Google Chrome users)

## Modules Overview

### Module A: Signing up new journalists and Article Submission
- Description: Handles the process of onboarding new journalists and facilitates article submission through a Google Form on the Twitter profile page. It also stores journalist information in Weaviate or a dedicated Google Sheet tab and updates their information for each fresh article submission.
- Interfaces/APIs:
  - User registration: Allows journalists to sign up through the Google Form by providing necessary information and credentials.
  - Article submission: Receives articles submitted through the Google Form.
  - Integration with Module E: Sends the submitted articles to Module E for analysis.
  - User storage: Stores journalist information securely in Weaviate or a dedicated Google Sheet tab.

### Module B: Article Scanning and Verification Processes
- Description: Handles the processes and procedures of article verification and the interaction with Module E for sentiment analysis.
- Interfaces/APIs:
  - Article submission: Receives new articles from journalists.
  - Article verification: Performs checks to ensure the articles' authenticity and integrity.
  - Integration with Module E: Sends the verified articles to Module E for sentiment analysis.
  - Storage: Stores the verified articles securely.

### Module C: Payments and Journalist Payouts
- Description: Handles payment processing received from Twitter and facilitates payments to journalists.
- Interfaces/APIs:
  - Payment receipt: Receives payments from Twitter.
  - Payment processing: Calculates appropriate payments for journalists.
  - Journalist payout: Manages the payout process to ensure timely and accurate payments.
  - Folder organization: Utilizes appropriate folders for managing payment records.

### Module D: Twitter Account and Article Integration
- Description: Handles the management of the Twitter account and integration with the HappyNewsDAO platform.
- Interfaces/APIs:
  - Article submission from Twitter: Receives new articles posted on the Twitter account.
  - Integration with HappyNewsDAO: Ensures seamless integration of new articles into the HappyNewsDAO platform.
  - Monitoring and synchronization: Monitors the Twitter account for new articles and synchronizes them with the platform.

### Module E: dApp core logic and self-improvement features (the steps here are intentionally not exhaustive and complete)
- Description: Handles the core logic of the entire project, including sentiment analysis, self-improvement features, and storage of historical sentiment analysis scores using Weaviate.
- Interfaces/APIs:
  - Sentiment analysis integration: Integrates with Module B to perform sentiment analysis on articles.
  - Core logic: Implements the overall logic for the project, coordinating various modules and functionalities.
  - Storage of sentiment analysis scores: Utilizes Weaviate for storing and querying historical sentiment analysis scores.

### Module F: Storing Articles on Filecoin
- Description: Stores articles on the Filecoin decentralized storage network after reaching a certain threshold.
- Interfaces/APIs:
  - Article threshold tracking: Monitors the number of impressions and clicks on published articles.
  - Integration with Filecoin: Initiates storage deals for approved articles on the Filecoin network.
  - Error handling and monitoring: Handles errors and monitors the article storage process.

### Module G: Updating HappyNews.DAO Website with Permanent Storage
- Description: Updates the HappyNews.DAO website with the permanently stored articles from Module F.
- Interfaces/APIs:
  - Article storage detection: Detects when an article has been permanently stored on Module F.
  - Integration with Pinata: Retrieves the article file using the IPFS hash and updates the website.

## Dependencies and Integration
- The modules interact with each other through well-defined interfaces/APIs.
- Dependencies between modules should be managed through appropriate versioning and referencing mechanisms.
- Each module should be developed independently, allowing for modular updates and maintenance.

## Tools and Technologies
- Node.js: Node.js is a JavaScript runtime environment that enables server-side execution of JavaScript code. It provides a robust platform for developing backend components and integrating various modules of the project.
- Ethereum Smart Contracts (Vyper): Vyper is a smart contract programming language specifically designed for the Ethereum platform. By writing smart contracts in Vyper, the project can leverage the Ethereum network's decentralization and execute self-executing code autonomously.
- IPFS (InterPlanetary File System) with Filecoin integration: IPFS is a distributed file system that enables decentralized storage and retrieval of files. By integrating with Filecoin, a blockchain-based decentralized storage network, the project can securely store articles in a distributed manner.
- Langchain: Langchain is an AI-powered language analysis tool that can be utilized for sentiment analysis and language processing. By incorporating Langchain into the sentiment analysis process, the project can automate sentiment analysis and improve the accuracy of the analysis.
- Fantom (Blockchain platform): Fantom is a high-performance, scalable, and secure blockchain platform. By deploying smart contracts on the Fantom network, the project can ensure the execution of autonomous and decentralized logic.
- Google Sheets API: The Google Sheets API allows the project to interact with Google Sheets, which can be utilized for various purposes such as user registration, application process tracking, and storage of journalist information.
- Twitter API: The Twitter API enables the project to access and retrieve articles posted on the Twitter account associated with the Happy News DAO platform. This allows seamless integration of new articles into the platform.
- Pinata (IPFS hosting and storage service): Pinata is a service that simplifies IPFS file hosting and management. It can be used to host and retrieve articles stored on IPFS, ensuring reliable and efficient access to the files.
- Unstoppable Domains API: The Unstoppable Domains API allows the project to integrate with decentralized domain systems, enabling the registration and management of decentralized domain names for the Happy News DAO website.
- Weaviate (Knowledge Graph for sentiment analysis data storage): Weaviate is a knowledge graph system that can be used to store and query historical sentiment analysis scores. It provides a scalable and efficient solution for managing sentiment analysis data.
- Github: (Version control and project management): GitHub is used as the version control system and project management tool for the Happy News DAO project. It allows for collaborative development, code sharing, and issue tracking.

## Processes and Autonomy
To ensure autonomous operation of the project, several key processes will be implemented:
- Journalist Onboarding: Module A can utilize automated user registration and application processes, minimizing the need for manual intervention in the onboarding of new journalists.
- Article Scanning and Verification: Module B should implement robust and automated processes to scan and verify the authenticity of articles. By incorporating AI algorithms and techniques, the system can detect AI-generated content and ensure human authenticity.
- Sentiment Analysis: Module E, with the integration of Langchain, can perform sentiment analysis autonomously. The sentiment analysis process should continuously improve through self-adjusting features, allowing the project to adapt and enhance accuracy over time.
- Payment Processing: Module C can leverage smart contracts and blockchain technology to automate payment processing. Once triggered by specific conditions (e.g., article publication and readership metrics), the smart contracts can autonomously calculate and facilitate timely and accurate journalist payouts.
- File Storage: Module F can track article metrics, such as impressions and clicks, to determine when to store articles on the Filecoin network. The integration with Filecoin should handle storage deals autonomously, ensuring articles are permanently stored without human intervention.
- Website Updates: Module G can detect when an article has been permanently stored on Filecoin and autonomously update the HappyNews.DAO website.

## Challenges Faced
During the development of the Happy News DAO project, we are encountering several challenges, including:
- Designing a fully decentralized and autonomous platform without requiring human input, except for Module E.
- Implementing robust article verification processes to ensure authenticity and prevent AI-generated content.
- Coordinating the integration and synchronization of multiple modules to operate seamlessly and maintain decentralization.
- Ensuring the security and privacy of sensitive information, such as journalist details and sentiment analysis results.
- Learning the new web3 tools and determining their efficiency and requirements within the Happy News project.

## Strategies Employed
To address the challenges faced, we are employing the following strategies:
- Conduct extensive research and experimentation to identify the most suitable technologies and frameworks for each module.
- Collaborate closely with the team members to design and implement well-defined interfaces/APIs for seamless integration between modules.
- Implement rigorous testing and code reviews to identify and resolve any issues or vulnerabilities.
- Incorporate secure storage mechanisms, such as IPFS and encryption, to protect sensitive information.
- Leverage decentralized technologies, such as blockchain and IPFS, to ensure data integrity and reliability.

## Future Enhancements
Some future improvements and features that could be considered include:
- Implement a decentralized governance mechanism for decision-making within the DAO.
- Enhance the article scanning and verification processes with advanced AI algorithms and natural language processing techniques.
- Expand the payment system to support additional cryptocurrencies and payment gateways.
- Integrate with additional social media platforms to broaden the reach and impact of the news platform.
- Enable user feedback and rating systems to improve the quality and credibility of published articles.


