Product Launch Intelligence Agent — Gemini setup

1. Extract this ZIP into your project folder.
2. Activate your existing virtual environment in PowerShell:
   .\.venv\Scripts\Activate.ps1

   If you do not have a virtual environment yet:
   py -m venv .venv
   .\.venv\Scripts\Activate.ps1

3. Install the dependencies:
   python -m pip install --upgrade pip
   python -m pip install -r requirements_gemini.txt

4. Create a .env file by copying .env.example, then replace both placeholders
   with your own API keys. Never share or commit the real .env file.
   Gemini key: https://aistudio.google.com/
   Firecrawl key: https://www.firecrawl.dev/

5. Start the app:
   streamlit run product_launch_intelligence_agent_gemini.py

Changes made:
- Replaced OpenAIChat / gpt-4o with Agno's Gemini adapter.
- Changed the sidebar key from OPENAI_API_KEY to GOOGLE_API_KEY.
- Updated requirements to include google-genai, firecrawl-py, and python-dotenv.
- Kept the existing three specialist agents, team instructions, Firecrawl tools,
  and Streamlit UI.

Notes:
- Gemini's free tier is subject to model availability, quotas, and rate limits.
- Firecrawl is a separate service and may impose its own free-plan limits.
- This is a code/configuration migration, not a guarantee that provider quotas
  or all runtime behavior will be available on every account.
