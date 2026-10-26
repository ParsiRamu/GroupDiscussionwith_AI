# Group Discussion AI

A local Flask application for practicing group discussions with four AI participants. Choose a suggested topic or enter your own, then discuss using text or your microphone.

## Requirements

- Python 3
- A Gemini API key

## Setup

1. Open a terminal in the repository folder and move into the application directory:

   ```powershell
   cd "Major project"
   ```

2. Create and activate a virtual environment:

   **Windows (PowerShell):**

   ```powershell
   python -m venv venv
   .\venv\Scripts\Activate.ps1
   ```

   **macOS / Linux:**

   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Install the Python dependencies:

   ```bash
   python -m pip install -r requirements.txt
   ```

4. Create a Gemini API key through [Google AI Studio](https://aistudio.google.com/app/apikey). Set it as an environment variable in the same terminal where you will run the app. Do not put the key in source code or commit it to Git.

   **Windows (PowerShell):**

   ```powershell
   $env:GEMINI_API_KEY = "your_api_key"
   ```

   **macOS / Linux:**

   ```bash
   export GEMINI_API_KEY="your_api_key"
   ```

## Start the application

From the `Major project` directory, with the virtual environment active and the API key set, run:

```bash
python app.py
```

When the terminal reports that the app has started, open [http://localhost:5000](http://localhost:5000) in your browser.

## Start your first discussion

1. On the welcome page, select **START**.
2. Choose one of the suggested topics, or choose **Custom** and enter a topic.
3. Enter your name and select **Start GD**.
4. On the discussion page, select **Start** to begin.
5. Contribute by typing a message or using the microphone. If you use the microphone, allow microphone access when your browser asks.
6. Use **Pause** to pause and resume the discussion, or **End** to finish and view your score.

The app starts four AI participants for each discussion. AI replies are generated using the configured Gemini API key.

## Stop the application

In the terminal running Flask, press `Ctrl+C`.

## Troubleshooting

- **The app cannot generate AI replies:** Check that `GEMINI_API_KEY` is set in the same terminal session used to start the app, and verify that the key is valid and has access to the Gemini API.
- **The page does not load:** Confirm that the Flask process is still running and that you opened `http://localhost:5000`.
- **Microphone input does not work:** Allow microphone access for the local site in your browser. Text input can be used instead.

This project starts Flask in debug mode for local development. Do not expose the development server to the public internet.
