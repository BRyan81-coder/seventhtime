
# Flask AI Endpoint for SharePoint List Analysis

This Flask application provides an endpoint `/analyze-lists` that accepts POST requests with JSON payloads containing two SharePoint lists. The app parses the lists, performs a placeholder analysis (e.g., counts items in each list), and returns a JSON summary.

## Setup

1. Clone the repository:
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name

2. Create a virtual environment and install dependencies:
   python -m venv venv
   source venv/bin/activate  # On Windows use venv\Scriptsctivate
   pip install -r requirements.txt

3. Run the app:
   python app.py

## Test the Endpoint

Use curl to test the endpoint locally:

curl -X POST http://localhost:5000/analyze-lists   -H "Content-Type: application/json"   -d '{"list1": [{"id": 1}, {"id": 2}], "list2": [{"id": 3}]}'

Expected response:

{
  "list1_count": 2,
  "list2_count": 1
}
