## HappyNewsDAO Project Checklist

### Module A: Signing up new journalists
- [x] Create a folder structure for the application process
- [x] Embed the Fresh Article Submission form in the Happy News DAO Twitter account
- [x] Implement functionality to automatically store journalist submissions to Google Sheets
- [x] Set up the necessary credentials and authentication for accessing the Google Sheets API
- [x] Write a script to receive a trigger when a new application is submitted
- [ ] Create a function to retrieve the latest application from Google Sheets 
- [ ] Integrate with Module E (Node.js API) to send the new application for sentiment analysis
- [ ] Implement a mechanism to receive the sentiment analysis results from Module E (Node.js API)
- [ ] Store the sentiment analysis results next to the original application in Google Sheets
- [ ] Send the application results (including sentiment analysis) to the applicant's Twitter account
- [ ] Ensure proper data privacy and security measures are in place when handling journalist information
- [ ] Handle errors and edge cases in the application submission and retrieval process
- [ ] Implement logging and monitoring to track the application submission and processing flow
- [ ] Test the end-to-end flow of application submission, sentiment analysis, and result handling
- [ ] Document the entire process, including setup instructions and any necessary configurations
- [ ] Review and optimize the performance and efficiency of the application submission and processing flow

### Module B: Article Verification and Interaction with Module E
- [ ] Research and select an appropriate AI tool or service for article verification.
- [ ] Integrate the selected AI tool or service into the dApp for article scanning and authenticity verification.
- [ ] Develop a mechanism to send the verified articles to Module E for sentiment analysis.
- [ ] Establish communication channels or APIs between Module B and Module E to facilitate the exchange of article data.
- [ ] Implement error handling and validation to ensure the smooth flow of data between the modules.
- [ ] Retrieve the sentiment analysis results from Module E and store them alongside the verified articles.
- [ ] Implement appropriate data structures and storage mechanisms to securely store the verified articles.
- [ ] Explore decentralized storage options like Filecoin for long-term storage of the verified articles.
- [ ] Implement logging and monitoring to track the article verification process and performance.
- [ ] Test the end-to-end flow of article verification and interaction with Module E.
- [ ] Document the entire process, including setup instructions and any necessary configurations.

### Module C: Payments and journalist compensation
- [ ] Design a payment system for receiving payments from Twitter.
- [ ] Develop a mechanism to calculate payments based on article clicks.
- [ ] Create a smart contract for managing payments and compensating journalists.
- [ ] Implement secure and decentralized payment transfer methods using Fantom.
- [ ] Utilize Covalent to query historical pay for journalists.
- [ ] Set up a database (e.g., Google Sheets) to store payment data securely.

### Module D: Twitter account management
- [x] Set up a dedicated Twitter account for HappyNewsDAO
- [x] Implement functionality to handle new articles submitted to HappyNewsDAO
- [ ] Develop a process to automatically publish articles to the Twitter account
- [ ] Integrate with the article verification module to ensure only authentic articles are published
- [ ] Implement a mechanism to count the number of impressions by each published article on Twitter
- [ ] Once an article reaches a certain threshold of "impressions," send it to Module F for permanent storage
- [ ] Publish articles to the Happy News website in Module G once they reach a certain threshold

  #### Steps for integrating Supabase into Module D:
  1. Set up a Supabase project:
     - [ ] Create a new Supabase project on the Supabase website.
     - [ ] Configure the project settings and obtain the required credentials (e.g., project URL, API key).
  2. Set up the Supabase client:
     - [ ] Install the Supabase client library in your project's dependencies.
     - [ ] Initialize the Supabase client using the obtained credentials.
  3. Create a table for tweeted articles:
     - [ ] Design a table schema to store information about tweeted articles, including unique identifiers and timestamps.
     - [ ] Use the Supabase client or the Supabase management interface to create the table in your Supabase project.
  4. Automate publishing process:
     - [ ] Implement a process to automatically publish new articles to the Twitter account.
     - [ ] Use the Twitter API to post tweets containing the article content and relevant information.
  5. Integration with article verification module:
     - [ ] Integrate with the article verification module (Module B) to ensure that only authentic and verified articles are published.
     - [ ] Retrieve verified articles from Module B and proceed with the publishing process.
  6. Count impressions:
     - [ ] Implement a mechanism to track the number of impressions generated by each published article on Twitter.
     - [ ] Utilize Twitter API analytics or custom tracking methods to count impressions.
  7. Threshold for permanent storage (Module F) and website publishing (Module G):
     - [ ] Define a threshold for the number of impressions an article needs to reach before being sent to Module F for permanent storage.
     - [ ] Implement the logic to check if an article has reached the threshold and trigger the process to store it permanently.
     - [ ] Similarly, define a threshold for publishing articles on the Happy News website (Module G) and implement the logic to initiate publication once the threshold is met.

### Module E: dApp core logic and self-improvement features (the steps here are intentionally not exhaustive and complete)
- [ ] Design and implement the core logic of the dApp
- [ ] Develop an AI API integration for self-improvement features
- [ ] Implement sentiment analysis using Langchain for article sentiment analysis
- [ ] Store and update self-improvement features using appropriate decentralized storage solutions

### Module F: Storing Articles on Filecoin
- [ ] Set up a Filecoin storage node or connect to an existing Filecoin network
- [ ] Define the data structure for storing articles on Filecoin (e.g., JSON format)
- [ ] Implement functionality to package and encrypt articles for storage on Filecoin
- [ ] Develop a trigger mechanism to count the number of clicks on published articles in Module D
- [ ] Implement logic to track the number of impressions per click and calculate when an article reaches 100,000 clicks
- [ ] Integrate with the Filecoin storage node to initiate storage deals for approved articles
- [ ] Configure and optimize Filecoin storage parameters (e.g., replication factor, deal duration)
- [ ] Handle errors and edge cases in the article storage process (e.g., deal failures, network interruptions)
- [ ] Implement logging and monitoring to track the article storage flow and performance
- [ ] Test the end-to-end flow of article storage on Filecoin after reaching 100,000 clicks
- [ ] Document the entire process, including setup instructions and any necessary configurations

### Module G: Updating HappyNews.DAO Website with Permanent Storage
- [ ] Set up a web server or hosting environment for the HappyNews.DAO website
- [ ] Define the file structure and directory for storing articles on the website
- [ ] Develop a trigger mechanism to detect when an article has been permanently stored on Module F
- [ ] Implement logic to retrieve the IPFS hash of the permanently stored article from Module F
- [ ] Configure the integration with Pinata to retrieve the article file using the IPFS hash
- [ ] Handle any necessary transformations or formatting of the article file for display on the website
- [ ] Develop an integration with Unstoppable Domains API or SDK to update the website with the new article
- [ ] Automatically retrieve the latest article IPFS hash from Module F
- [ ] Update the website content by associating the IPFS hash of the article file with the website content
- [ ] Verify the successful update of the HappyNews.DAO website with the new article
- [ ] Implement logging and monitoring to track the website update process and performance
- [ ] Test the end-to-end flow of updating the HappyNews.DAO website with permanently stored articles
- [ ] Document the entire process, including setup instructions and any necessary configurations

### Smart contract development
- [ ] Identify the required functionalities for each module and define smart contract interfaces
- [ ] Write smart contracts in a suitable programming language (e.g., Vyper)
- [ ] Test and debug smart contracts to ensure accuracy and security
- [ ] Deploy smart contracts to Fantom network 

### GitHub repository setup
- [x] Create a new repository on GitHub for the HappyNewsDAO project
- [x] Initialize the repository with a suitable project structure
- [ ] Commit and push the initial codebase, including smart contracts and dApp implementation
- [ ] Continuously update and maintain the repository with new features and bug fixes

### Continuous autonomous operation
- [ ] Implement monitoring and error handling mechanisms for the dApp
- [ ] Set up automated testing processes to ensure ongoing functionality
- [ ] Consider implementing decentralized governance mechanisms for DAO decision-making
- [ ] Regularly review and update the project to adapt to evolving technologies and requirements

## Tools and Resources

- [Unstoppable Domains](https://unstoppabledomains.com) - Decentralized website domain for "HappyNews.DAO"
- [Google Sheets](https://www.google.com/sheets/about/) - Online spreadsheet tool for storing journalist submissions
- [Node.js](https://nodejs.org) - JavaScript runtime for executing server-side code
- [Pinata](https://www.pinata.cloud) - IPFS hosting and storage service for decentralized file management
- [Unstoppable SDKs](https://unstoppabledomains.com/sdk) - Software development kits for integrating with Unstoppable Domains
- [Langchain](https://python.langchain.com/en/latest/index.html) - AI-powered language analysis tool for sentiment analysis
- [Weaviate](https://www.semi.technology/developers/weaviate/current/introduction/index.html) - Knowledge Graph system for semantic search and data exploration
- [Power BI](https://powerbi.microsoft.com) - Business analytics tool for data visualization and reporting
- [Fantom](https://fantom.foundation) - A scalable, high-performance blockchain platform
- [Covalent](https://www.covalenthq.com) - Blockchain data provider for querying historical pay for journalists
- [Filecoin](https://filecoin.io) - Decentralized storage network for storing articles and files
- [Vyper](https://github.com/vyperlang/vyper) - Pythonic smart contract language for Ethereum
- [GitHub](https://github.com) - Web-based hosting service for version control and collaboration
- [Flask](https://flask.palletsprojects.com/en/2.3.x/) - Web framework for building API endpoints in Python
- [Twitter API](https://developer.twitter.com/en/docs) - API for integrating with Twitter functionality
- [Postman](https://twitter.com/getpostman) - Collaboration platform for API development, testing, and documentation
- [Vercel](https://twitter.com/vercel) - Cloud platform for static site hosting and serverless functions
- [Supabase](https://twitter.com/supabase) - Open-source Firebase alternative with a PostgreSQL database




