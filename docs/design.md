# Context and Scope

This project aims to be a platform to serve humanitarian workers and those in crisis areas around the world through functionality for uploading user data, tracking trends, and receiving data insights to most efficiently observe the needs people require. The platform will allow for data uploading of multiple formats (csv, images, etc.) directly on the UI, maintain strong data availability for data and insights, and include an agentic aspect for AI-assisted decisions. The platform will serve as a repository for storing data, scaling for data needs, and most importantly providing a platform for quick and easy insights to assist efficient and effective decision making.

# Goals and non-goals

- Users can upload data in any type of format (CSV, tsv, images, etc.)
- Database and storage system will be ACID compliant
- (Eventually) Use distributed processing and Spark for massive data
- Platform will be secure, and not be susceptible to data leakage across accounts or onto the web
- Will be an all-in-one platform, but geared for less technical folks and for ease of use compared to platforms like Databricks and Snowflake which are meant for more data-savvy users
- Shared workspaces can be created for organizations
- Data can be downloaded from other connected sources
- (Later) The AI will be able to process the information, store context for decision making, and parse the raw files as they are when offering insights

- The platform will not be integrated as an agent like OpenClaw to schedule or notify others about tasks
- There will be limited functionality in the platform for data visualization and creating visuals with the agent
- The main agent will be limited in its scope in helping create data solutions or visualizations, as the platform will be primarily for providing a space to upload data, track changes, and see simple & quick insights.

# Design 

## Diagram 

Visual Diagram will be added later (focus on tradeoffs)
## APIs: 
- Service to upload images and data to the platform
- Server will pull needed and previously uploaded information from the database
- Pulling data from other sources such as Google or Salesforce (must implement this integration)
- Python and FastAPI will serve the APIs
- Claude-based agent to serve insights from user queries

## Data storage
- Uploaded files and images will be stored in S3
- Postgres database will store the actual numerical figures extracted from the uploads
- A redis or dynamodb database will serve as a cache for the most frequently requested information

# Alternatives Considered
- (Highlight tradeoffs / reasons for selections)
- 
