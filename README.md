# Secure Internal Chatbot System — Washington Sentinels

Team Members:

Kyle Kitching
William Anderson
Victoria Salomon
Michael Tamirat

## Project Description:

This prototype demonstrates a secure, in-house chatbot system designed for the fictional NFL team Washington Sentinels. The goal is to showcase how a centralized chat platform can support multiple internal roles while protecting sensitive information and enforcing role-based access.

This proof-of-concept focuses on a live injury-report workflow, enabling users to query a 12-player injury database and — when authorized — update medical information in real time.

## Key Security Features Demonstrated

Role-Based Access Control (RBAC)
The chatbot adjusts its responses based on the logged-in user’s role.
Example: Only the Team Physician can update injuries.

Data Access Separation
Medical details and write-access are limited to authorized users.
Non-clinical roles see only generalized information.

Audit Logging & Query Database
Every user query is automatically logged with:

Username

Role

Timestamp

Query ID

Status (new, reviewed, answered, ignored)

Optional analyst notes

This simulates real-world compliance features used in sports medicine or HIPAA-adjacent environments.

Simulated Authentication & MFA
Includes:

Username + password input

6-digit MFA code simulation
Represents a secure login flow without storing real credentials.

Secure-by-Design Architecture
Centralized system where:

Sensitive medical updates stay inside the physician workflow

All role interactions occur through a single unified UI

No PHI is used; all data is fictional and safe

## Setup & Run Instructions
1. Clone the Repository
git clone https://github.com/YOUR_USERNAME/Secure-Internal-Chatbot-Design.git
cd Secure-Internal-Chatbot-Design

2. Create & Activate a Virtual Environment

Windows:

python -m venv venv
venv\Scripts\activate

3. Install Dependencies
pip install -r requirements.txt

4. Launch the Application
streamlit run app.py


The app will open in your browser at:

http://localhost:8501
