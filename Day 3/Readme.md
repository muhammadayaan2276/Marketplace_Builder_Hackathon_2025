# 🛠️ Marketplace Builder Hackathon - Day 3

## 🎯 Objective
The goal for Day 3 was to integrate an external API and migrate its data into Sanity CMS to establish a dynamic backend for the marketplace. The tasks included testing endpoints, adapting data to schema requirements, updating Sanity schemas, and ensuring the frontend displayed the data correctly.

## 🔍 Steps and Process
### 📡 API Analysis
- API URL: https://hackathon-apis.vercel.app/api/products
- The API provided details such as product information, categories, and images.
- Endpoints were validated using Postman to ensure accurate responses.

## 🛠️ Backend Setup
### Tools Utilized
- axios: To fetch data from the external API.
- next-sanity: For interacting with Sanity CMS.

## 🏗️ Schema Enhancements in Sanity CMS
- Expanded the product schema to include fields like dimensions, tags, and categories.
- Added a new schema to manage product categories.
- Linked products to their respective categories using a reference field.

## 🔄 Data Migration Workflow
- Data from the API was fetched using axios.
- Images were uploaded to Sanity, and their references were stored.
- API data was transformed to match the schema requirements before importing.
- The createOrReplace method was used for importing data into Sanity CMS.
- Errors during migration were handled with try-catch blocks, and issues were logged for debugging.

## 🖥️ Frontend Integration
- Reusable backend functions were created for fetching data:
- getAllProducts: Retrieves all product data.
- getPopularProducts: Fetches featured or popular products.
- getProductBySlug: Fetches product details using a slug.
- The data was rendered on the frontend to verify accuracy.

## 🚧 Challenges Faced and Their Solutions
### 🖼️ Handling Large Images
- Problem: Uploading large image files.
- Solution: Used Sanity’s asset manager with buffer support for efficient uploads.

## 🗂️ Schema Inconsistencies
- Problem: API fields didn’t align with the Sanity schema.
- Solution: Adjusted schemas and mapped fields appropriately in the migration script.

## ✅ Maintaining Data Integrity
- Problem: Ensuring complete and accurate data migration.
- Solution: Added validation steps to identify and fix missing or malformed data before import.

## ⚡ Performance Optimization
- Batched API requests to manage rate limits and boost performance.
- Cached frequently accessed API responses to minimize repetitive calls.
- Fetched only required fields to reduce data payload size.

## 🏆 Results
- Successfully migrated products and categories into Sanity CMS.
- Verified data in Sanity Studio for accuracy.
- Displayed the imported data dynamically in the frontend marketplace.

## 🔮 Future Recommendations
- Automate schema validation to identify mismatches before importing data.
- Improve error tracking by implementing detailed logs.
- Use Sanity webhooks for real-time data synchronization.

## 📜 Steps to Execute the Migration Script
### Requirements
- Installed Node.js.
- Configured Sanity project.
- Accessible external API.

## Steps:

 1. Clone the repository and navigate to the project directory:
 - git clone [repository-url]
 - cd [project-directory]
 
 2️. Install the dependencies:
- npm install 

3️. Run the migration script:
- node scripts/data-migration.mjs

4️. Validation:
- Verify the imported data in Sanity Studio.
- Check the frontend to ensure product listings and categories are displayed correctly.

## 📌 Day 3 Summary
The successful API integration and data migration into Sanity CMS prepared the system to manage dynamic content efficiently. This process ensured scalability and flexibility for future development, laying a robust foundation for the marketplace backend.

## 🏷️ Tags:
#TechArchitecture #APIIntegration #WebDevelopmentJourney #MarketplaceInnovation #HackathonChallenge #ModernEcommerce #NextjsDevelopment #Marketplace BuilderHackathon2025
