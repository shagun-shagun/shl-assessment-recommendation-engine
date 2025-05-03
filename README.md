
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

## Evaluation & Optimization
- Used fuzzywuzzy's token_sort_ratio to allow approximate string matching
- Set match threshold to 62 based on multiple test iterations
- Cleaned and normalized input strings to improve accuracy
- Handled multiple comma-separated values (e.g. "developer, backend dev") in catalogue

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
