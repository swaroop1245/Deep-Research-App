# Deep Research App

An intelligent research application that leverages AI agents to perform comprehensive web research, generate detailed reports, and deliver findings via email. Built with OpenAI's Agents SDK, this application demonstrates advanced AI orchestration and asynchronous workflow management.

## 🚀 Features

- **Intelligent Search Planning**: Uses AI to plan and optimize web searches based on research queries
- **Parallel Web Search Execution**: Performs multiple searches concurrently for efficient data gathering
- **Automated Report Generation**: Creates comprehensive, well-structured research reports (5-10 pages, 1000+ words)
- **Email Delivery**: Automatically formats and sends research reports via email using SendGrid
- **Structured Outputs**: Uses Pydantic models for type-safe data validation and structured responses
- **Asynchronous Processing**: Built with async/await for optimal performance

## 🛠️ Technology Stack

- **OpenAI Agents SDK**: For AI agent orchestration and tool integration
- **Pydantic**: For data validation and structured outputs
- **SendGrid**: For email delivery
- **Python AsyncIO**: For concurrent task execution
- **Jupyter Notebooks**: For interactive development and execution
- **Python-dotenv**: For secure environment variable management

## 📋 Prerequisites

- Python 3.8 or higher
- OpenAI API key
- SendGrid API key (for email functionality)
- Jupyter Notebook or JupyterLab

## 🔧 Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd Deep-Research-App
```

2. Create a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Set up environment variables:
   - Create a `.env` file in the root directory
   - Add your API keys:
```env
OPENAI_API_KEY=your_openai_api_key_here
SENDGRID_API_KEY=your_sendgrid_api_key_here
```

## 📖 Usage

1. Open the Jupyter notebook:
```bash
jupyter notebook app.ipynb
```

2. Update the email addresses in the `send_email` function (Cell 4) with your verified SendGrid email addresses

3. Modify the research query in Cell 9:
```python
query = "Your research topic here"
```

4. Run all cells to execute the research pipeline:
   - The app will plan searches
   - Execute web searches in parallel
   - Generate a comprehensive report
   - Send the report via email

## 🏗️ Architecture

The application follows a multi-agent architecture:

1. **Planner Agent**: Analyzes the research query and creates an optimized search plan
2. **Search Agent**: Executes web searches using OpenAI's WebSearchTool
3. **Writer Agent**: Synthesizes search results into a detailed markdown report
4. **Email Agent**: Formats and sends the report via email

### Workflow

```
Query → Plan Searches → Execute Searches (Parallel) → Generate Report → Send Email
```

## 📝 Project Structure

```
Deep-Research-App/
├── app.ipynb              # Main application notebook
├── requirements.txt       # Python dependencies
├── .gitignore            # Git ignore rules
└── README.md             # Project documentation
```

## ⚠️ Important Notes

- **API Costs**: The WebSearchTool incurs costs (~$0.025 per search). Monitor usage to avoid unexpected charges.
- **Email Configuration**: Ensure your SendGrid account has verified sender and recipient email addresses.
- **Rate Limits**: Be mindful of API rate limits when running multiple searches.

## 🔒 Security

- Never commit `.env` files containing API keys
- Use environment variables for all sensitive credentials
- The `.gitignore` file is configured to exclude sensitive files

## 🎯 Use Cases

- Market research and competitive analysis
- Academic research and literature reviews
- Technology trend analysis
- Business intelligence gathering
- Content research for articles and reports

## 🤝 Contributing

This is a personal project, but suggestions and improvements are welcome!


## 👤 Author

Swaroop

---

**Note**: This project demonstrates proficiency in:
- AI/ML integration with OpenAI's Agents SDK
- Asynchronous programming in Python
- API integration and third-party service orchestration
- Structured data validation with Pydantic
- Software engineering best practices
