
# SHL Assessment Recommendation Engine

This is a FastAPI-based backend application that recommends SHL assessments based on the user's job role, experience level, and industry.

## Features
- Built with FastAPI and deployed via ngrok
- Accepts job_role, level, and industry as input
- Uses fuzzy string matching to handle partial or related input terms
- Returns recommended assessments from SHL’s sample product catalog

## Technologies Used
- Python
- FastAPI
- pandas
- fuzzywuzzy
- Uvicorn
- Pyngrok

## How to Use
1. Open the live app URL (shared via ngrok)
2. Navigate to /docs to access Swagger UI
3. Use the *POST /recommend* endpoint with this format:
```json
{
  "job_role": "software development",
  "level": "entry",
  "industry": "technology"
}
