# 🎯 AI Resume Tailor

**Transform your job applications with AI-powered resume tailoring and interview prep**

AI Resume Tailor is a multi-agent system built with CrewAI that automatically analyzes job postings, profiles candidates, and generates perfectly tailored resumes and interview materials. Say goodbye to generic applications and hello to personalized, data-driven job hunting.

## ✨ What It Does

🔍 **Job Analysis**: Scrapes and analyzes job postings to extract key requirements  
👤 **Profile Building**: Creates comprehensive candidate profiles from GitHub and personal info  
📄 **Resume Tailoring**: Automatically customizes resumes to match specific job requirements  
🎤 **Interview Prep**: Generates targeted interview questions and talking points  

## 🤖 Meet Your AI Crew

- **🔬 Tech Job Researcher**: Extracts and analyzes job requirements
- **👥 Personal Profiler**: Builds comprehensive candidate profiles  
- **📝 Resume Strategist**: Tailors resumes for maximum impact
- **🎭 Interview Preparer**: Creates custom interview materials

## 🚀 Quick Start

### Prerequisites
- Python 3.8+
- OpenAI API key
- Serper API key (for web search)

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/ai-resume-tailor.git
cd ai-resume-tailor
```

2. **Install dependencies**
```bash
pip install crewai==0.28.8 crewai_tools==0.1.6 langchain_community==0.0.29 python-dotenv
```

3. **Set up environment variables**
Create a `.env` file in the project root:
```env
OPENAI_API_KEY=your_openai_api_key_here
SERPER_API_KEY=your_serper_api_key_here
```

### Usage

1. **Update your information**
   - Edit `fake_resume.md` with your actual resume
   - Modify the `personal_writeup` in the notebook with your background

2. **Run the application**
```bash
jupyter notebook L7_job_application_crew.ipynb
```

3. **Customize the job application inputs**
```python
job_application_inputs = {
    'job_posting_url': 'YOUR_TARGET_JOB_URL',
    'github_url': 'YOUR_GITHUB_PROFILE',
    'personal_writeup': 'YOUR_PROFESSIONAL_SUMMARY'
}
```

4. **Execute and get results**
   - `tailored_resume.md` - Your customized resume
   - `interview_materials.md` - Interview prep materials

## 📁 Project Structure

```
ai-resume-tailor/
├── L7_job_application_crew.ipynb  # Main notebook
├── utils.py                       # Helper functions
├── fake_resume.md                 # Template resume (replace with yours)
├── .env                          # API keys (create this)
├── requirements.txt              # Dependencies
└── README.md                     # This file
```

## 🛠️ How It Works

1. **Job Analysis**: The Researcher agent scrapes the job posting URL and extracts key requirements
2. **Profile Creation**: The Profiler agent analyzes your GitHub and personal information
3. **Resume Optimization**: The Resume Strategist tailors your resume to match job requirements
4. **Interview Preparation**: The Interview Preparer creates relevant questions and talking points

All agents work asynchronously where possible, with smart task dependencies ensuring the right information flows between agents.

## 🎯 Example Output

After running the crew, you'll get:

- **Tailored Resume**: A markdown file with your resume optimized for the specific job
- **Interview Materials**: Custom questions and talking points based on the job requirements and your background

## 🔧 Customization

### Adding New Agents
Create new agents by extending the existing pattern:
```python
new_agent = Agent(
    role="Your Agent Role",
    goal="What the agent should accomplish",
    tools=[relevant_tools],
    backstory="Agent's background and expertise"
)
```

### Modifying Tools
The system uses several CrewAI tools:
- `SerperDevTool`: Web search
- `ScrapeWebsiteTool`: Website content extraction
- `FileReadTool`: Local file reading
- `MDXSearchTool`: Semantic search within documents

## 🤝 Contributing

Contributions are welcome! Please feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Built with [CrewAI](https://github.com/joaomdmoura/crewAI)
- [Full Tutorial](https://learn.deeplearning.ai/courses/multi-ai-agent-systems-with-crewai/lesson/a8ecj/build-a-crew-to-tailor-job-applications)
- 

## 📞 Support

Having issues? Check out:
- [CrewAI Documentation](https://docs.crewai.com/)
- [OpenAI API Documentation](https://platform.openai.com/docs)
- [Serper API Documentation](https://serper.dev/api-key)

---

**⭐ Star this repo if AI Resume Tailor helped you land your dream job!**
