
# YouTube Transcript Microservice

## Prerequisites
- Python 3.7 or above
- `pip install virtualenv` (if not already installed)
- Ngrok account (free) from https://ngrok.com

## Setup Instructions

1. Create and activate virtual environment:
   ```
   python3 -m venv venv
   source venv/bin/activate
   ```

2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Run the app:
   ```
   python app.py
   ```

4. Open another terminal window and start ngrok:
   ```
   ngrok http 5001
   ```

5. Copy the HTTPS URL shown and set it in Supabase as:
   ```
   TRANSCRIPT_MICROSERVICE_URL=https://<your-ngrok-url>
   ```

6. Done! Supabase will use your local microservice as a fallback when YouTube direct extraction fails.
