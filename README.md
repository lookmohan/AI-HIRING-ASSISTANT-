
# TalentScout Hiring Assistant 

The **TalentScout Hiring Assistant** is an intelligent Streamlit chatbot designed to streamline the initial technical screening process for recruitment agencies. It collects candidate details, analyzes technical skills, and dynamically generates customized technical questions using HuggingFace's Zephyr-7b-beta LLM.

## 🚀 Overview

**Key Features:**

- **Candidate Profile Collection**: Gathers basic info (name, contact, experience)
- **Tech Stack Analysis**: Parses and normalizes technology input
- **Dynamic Question Generation**: 3 custom technical questions per specified tech
- **Assessment Workflow**: Smooth, step-by-step interview flow with progress tracking
- **Response Review**: Lets candidates review and confirm answers

## 🧠 Technical Highlights

| Feature              | Description                                               |
|---------------------|-----------------------------------------------------------|
| **Prompt Engineering** | Carefully constructed prompts for precision and structure |
| **Context Management** | Maintains conversation state throughout the session       |
| **Input Validation**   | Ensures data integrity and completeness                  |
| **Privacy-Focused**    | No persistent storage, all data is session-only          |

## ⚙️ Installation

### ✅ Prerequisites

- Python 3.8+
- HuggingFace API token (get from [https://huggingface.co](https://huggingface.co))
- Git (optional, for cloning repo)

### 🛠 Setup Instructions

1. **Clone the repository:**

```bash
git clone https://github.com/yourusername/talentscout-hiring-assistant.git
cd talentscout-hiring-assistant
```

2. **Create and activate virtual environment:**

```bash
python -m venv venv
# On Linux/macOS
source venv/bin/activate
# On Windows
venv\Scripts\activate
```

3. **Install dependencies:**

```bash
pip install -r requirements.txt
```

4. **Create `.env` file with your HuggingFace token:**

```env
HF_TOKEN=your_huggingface_token_here
```

## ▶️ Usage

Launch the application:

```bash
streamlit run app.py
```

Follow the step-by-step process:

- Fill in your candidate profile
- Enter your tech stack (e.g., Python, JavaScript, Docker)
- Answer the generated technical questions
- Review your responses
- Submit and download the summary (optional)

## 🧱 Technical Architecture

| Component      | Technology               | Purpose                        |
|----------------|--------------------------|--------------------------------|
| **Frontend**   | Streamlit                | UI and interaction             |
| **LLM**        | Zephyr-7b-beta (HuggingFace) | Dynamic question generation    |
| **State Mgmt** | Streamlit Session State  | Maintain conversation flow     |
| **Parsing**    | Custom Python logic      | Normalize tech stack input     |

## ✍️ Prompt Engineering Strategy

Sample prompt used:

```
Generate exactly 3 technical questions about {tech} for a candidate with {years_experience} years of experience.
Difficulty level: {difficulty}
The questions should:
- Be technical and specific to {tech}
- Cover different aspects (syntax, architecture, debugging)
- Require detailed answers
```

Prompts are designed to:

- Encourage question diversity
- Adjust for candidate experience level
- Maintain parsing-friendly structure

## 🧩 Challenges and Solutions

| Challenge                        | Solution Implemented                             |
|----------------------------------|--------------------------------------------------|
| Inconsistent tech stack inputs   | Robust parser and normalization rules            |
| Inconsistent LLM responses       | Strict prompts + fallback to default question bank|
| Managing session transitions     | Clear state initialization and transitions       |
| Ensuring quality questions       | Filters + validation layers + backup questions   |

## 🔐 Compliance and Security

- **Privacy**: All data remains in memory (not saved)
- **GDPR Compliant**: No persistent logs or database
- **Secure Tokens**: HuggingFace API keys stored via `.env` file

## 🔮 Future Enhancements

- Sentiment analysis on answers
- Multilingual candidate support
- Persistent cloud storage (optional)
- Customizable question templates by role/tech

## 📽️ Demo

![Demo Thumbnail](https://img.youtube.com/vi/VIDEO_ID/0.jpg)

> Replace `VIDEO_ID` with your actual YouTube video ID if available.

## 📄 License

This project is licensed under the **MIT License**.

## 📬 Contact

For questions or feedback:

- **Name**: Mohanraj R 
- **Email**: mohanraj9677011@gmail.com  
- **Portfolio/LinkedIn**: https://linkedin.com/in/moganraj


