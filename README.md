📍 Project Report: AI-Powered Cash Counter Surveillance using Gemini AI and OpenCV

🔍 Project Title

Smart Surveillance for Cash Counter Theft Detection using Gemini AI and OpenCV

📌 Objective

To develop a real-time monitoring system that detects suspicious activity—specifically money theft—at a cash counter using computer vision (OpenCV) and Google's Gemini AI for image analysis and description.

🧠 Key Features

Captures video frames in real-time using OpenCV.

Sends full-frame images every 4 seconds for AI analysis.

Uses Gemini AI (Google Generative AI) to detect if money theft is occurring.

Outputs observations in a structured format and stores them in a text file only when theft is detected.

Implements multithreading to ensure smooth real-time monitoring without lag.

Displays the surveillance feed with mouse position overlay for debugging and setup.

🛠️ Tech Stack

Programming Language: Python

Libraries Used: cv2, numpy, base64, threading, time, langchain-google-genai

AI Model: Gemini 2.0 Flash (via LangChain)

Image Encoding: Base64 (for transmitting frames to Gemini)

📂 Project Structure

cash-counter-surveillance/
️️️️️
├── full_frames/             # Directory for captured frames
├── observations.txt         # Output file with AI-detected theft observations
├── vid3.mp4                 # Input video for simulation
├── main.py                  # Main script for monitoring

⚠️ Gemini AI Prompt Logic

The AI receives the frame with a structured prompt asking:

| Suspicious Activity at Cash Counter | Observed? (Yes/No) | Suspect Description (If Yes) |

If "Yes" is returned, the description (clothing, appearance, etc.) is saved with the timestamp.

📊 Output Format (observations.txt)

Example:

2025-05-21_12-44-15 - | Money theft from cash counter? | Yes | Man in black hoodie taking money while cashier distracted |

💽 How It Works

Video feed is opened using OpenCV.

Every 4 seconds:

A frame is saved.

A thread sends it to Gemini AI.

If theft is detected, it is recorded in observations.txt.

Monitoring ends when user presses 'q'.

🌟 Applications

Small shops and retail counters

ATMs and banking halls

AI-integrated surveillance in public areas

✅ Future Improvements

Add object detection to automatically isolate cash counter region.

Real-time alert via SMS/email upon theft detection.

Integration with CCTV systems for live deployment.



