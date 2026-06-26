🧠 AI-Powered Intelligent Data & Vision Analytics Platform
A Unified Conversational System for Data Analysis, Machine Learning, and Computer Vision — built with Streamlit, LangChain, Groq, and OpenAI.

📘 Project Description
This project is a comprehensive AI platform that merges natural language processing, data analytics, machine learning, and computer vision — all accessible via a single Streamlit-based dashboard.

Users can interact with their data, documents, SQL databases, and images through chat-based interfaces powered by LangChain, Groq, and OpenAI.
It empowers professionals to conduct analytics, training, and visualization in one environment without switching tools.

🚀 Key Features
💬 Conversational Data Analysis – Query CSV, Excel, or SQL databases in natural language.
📄 Document Intelligence (RAG) – Upload PDFs and ask context-aware questions using Groq LLMs.
🤖 Machine Learning Suite – Train and evaluate Logistic Regression or Neural Network models, tracked via MLflow.
📸 Computer Vision Pro Suite – Perform image enhancement, object detection (YOLOv5), OCR, and real-time face or camera detection.
🧠 Conversational Memory – Retains chat history using LangChain memory integration.
⚡ Unified Dashboard – All modules integrated into a single Streamlit application.
🔑 Groq + OpenAI Support – Switch easily between local and API-based models.
⚙️ Project Requirements
Component	Required Version / Notes
Python	3.10 or higher
RAM	8 GB (16 GB recommended)
Dependencies	Listed in requirements.txt
Internet Connection	Required for API calls and model downloads
Optional GPU	NVIDIA CUDA (for PyTorch / YOLOv5 acceleration)
🗃️ Database Setup (SQL Chat Module)
A sample database Chinook.db is included in the project directory.
You may replace it with your own .db (SQLite) file.
The SQL chat module automatically connects and converts natural queries to SQL statements.
Example query:
“Show the top 10 customers with the highest total purchases.”

🔑 API Configuration
This project supports Groq (for LLM-based analysis) and OpenAI (for conversational agents).

API Provider	Use Case	Key Format
Groq	Chat with Data / PDFs / SQL	gsk_...
OpenAI	Conversational & general NLP	sk-...
To get your API keys:
Groq: https://console.groq.com → Create API Key
OpenAI: https://platform.openai.com/account/api-keys → Create Secret Key
You will be prompted to enter these keys in the Streamlit sidebar when running the app.

🧠 Running the Project Locally
1️⃣ Create and Activate Virtual Environment
python -m venv new_venv
# Windows
new_venv\Scripts\activate
# macOS/Linux
source new_venv/bin/activate
2️⃣ Install Required Dependencies
pip install -r requirements.txt
3️⃣ Run the Unified App
streamlit run app.py
Once launched, open your browser and navigate to:

http://localhost:8501
You’ll see a sidebar navigation panel with the following modules:

Chat with SQL
Chat with Pandas
Chat with Documents
Machine Learning
Computer Vision
Select any mode to start exploring its features.

🧪 (Optional) MLflow Experiment Tracking
To monitor ML experiment metrics and parameters:

mlflow ui
Then open:

http://localhost:5000
You can visualize accuracy, loss curves, parameters, and model logs here.

🧰 Troubleshooting
Issue	Possible Cause	Solution
ModuleNotFoundError	Missing dependency	Run pip install -r requirements.txt
groq.NotFoundError	Invalid API key	Regenerate key from Groq Console
OpenAIAuthenticationError	Wrong or expired OpenAI key	Update your OpenAI key
cv2.error	Invalid Gaussian Blur parameter	Use odd values like 3, 5, or 7
StreamlitDuplicateElementId	Duplicate buttons	Upgrade Streamlit (pip install --upgrade streamlit)
ValueError: y should be 1D	Wrong target column in ML	Select a categorical target column
🧱 Project Structure
streamlit_agent/
│
├── app.py                       # Unified Streamlit dashboard (main entry)
├── chat_pandas_df.py             # Chat with CSV / Excel datasets
├── chat_with_documents.py        # PDF Q&A using LangChain RAG
├── chat_with_sql_db.py           # SQL database natural language chat
├── machine_learning.py           # ML models (Logistic + Neural Network)
├── computer_vision.py            # Vision suite (YOLOv5, OCR, etc.)
├── Chinook.db                    # Sample SQLite database
├── requirements.txt              # Dependencies list
└── README.md                     # Documentation
🧩 Technologies Used
Streamlit – Interactive web app framework for data apps
LangChain – LLM orchestration, RAG, and conversational memory
Groq / OpenAI APIs – High-performance LLMs for text and document understanding
Pandas / NumPy – Data analysis and feature manipulation
Scikit-learn / PyTorch – Machine learning and neural networks
OpenCV / EasyOCR / YOLOv5 – Image processing and object detection
MLflow – Tracking ML experiments and model management
🧾 Example Use Cases
Business Analysts: Query structured or unstructured data conversationally.
Researchers: Summarize and interpret academic PDFs.
Data Scientists: Prototype and compare ML models with auto-logging.
Developers: Implement intelligent data and vision pipelines interactively.
🏁 Conclusion
The AI-Powered Intelligent Data & Vision Analytics Platform integrates data querying, ML modeling, and vision processing into a single, intuitive interface.
It allows users to analyze data, build models, and process images through conversational commands — bridging human insight with machine intelligence.

