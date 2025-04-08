# DocTalk: Context-Constrained LLM Assistant

A powerful, open-source multimodal AI assistant that operates strictly within user-provided context, featuring comprehensive input support and intelligent prompt feedback.

![License](https://img.shields.io/badge/license-MIT-blue.svg)

## 🌟 Features

### Core Functionality
- 🔐 **Secure User Authentication**
  - Custom JWT-based authentication
  - Personal dashboards with saved sessions
  - Encrypted password storage

- 💬 **Smart Context Management**
  - PDF document analysis and context-bound responses
  - URL content scraping and webpage-scoped interactions
  - Topic-constrained conversations
  - Persistent chat history with session resumption

- 📸 **Multimodal Input Support**
  - Image upload with OCR text extraction
  - Real-time voice interaction
  - Live camera feed analysis
  - Text-based chat interface

- 🌍 **Offline-Capable Translation**
  - Real-time text translation
  - Voice input translation
  - Support for multiple languages

- 📝 **Prompt Quality Enhancement**
  - End-of-session prompt analysis
  - Concrete improvement suggestions
  - Example prompts for better interaction

## 🛠️ Technology Stack

### Frontend
- React.js with Tailwind CSS
- Native Web APIs for device access
- Real-time WebSocket communication

### Backend
- FastAPI (Python)
- JWT + Passlib authentication
- SQLite/PostgreSQL database

### AI/ML Components
- Local LLM: Mistral 7B/LLaMA 2/Phi-2
- Tesseract OCR for image processing
- Whisper.cpp for speech recognition
- OpenNMT/M2M-100 for translation
- MediaPipe/OpenCV for computer vision

## 🚀 Getting Started

### Prerequisites
```bash
# Python 3.8+
python --version

# Node.js 16+
node --version

# PostgreSQL (optional)
psql --version
```

### Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/doctalk.git
cd doctalk
```

2. Set up the backend
```bash
# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Set up environment variables
cp .env.example .env
# Edit .env with your configurations
```

3. Set up the frontend
```bash
cd frontend
npm install
cp .env.example .env.local
# Edit .env.local with your configurations
```

4. Initialize the database
```bash
python scripts/init_db.py
```

5. Start the development servers
```bash
# Backend (from root directory)
uvicorn app.main:app --reload

# Frontend (from frontend directory)
npm run dev
```

## 📚 Documentation

Detailed documentation is available in the `/docs` directory:
- [API Documentation](docs/api.md)
- [Architecture Overview](docs/architecture.md)
- [Deployment Guide](docs/deployment.md)
- [Contributing Guidelines](docs/contributing.md)

## 🔧 Configuration

Key configuration options in `.env`:
```env
# Backend
SECRET_KEY=your_secret_key
DATABASE_URL=postgresql://user:password@localhost/doctalk
MODEL_PATH=/path/to/local/llm

# Frontend
NEXT_PUBLIC_API_URL=http://localhost:8000
```

## 🌐 Deployment

### Local Deployment
Follow the installation steps above for a local development setup.

### Cloud Deployment (Free Tier Options)
- Frontend: Vercel/Netlify
- Backend: Render/Railway
- Database: Supabase/Railway

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Hugging Face](https://huggingface.co/) for open-source models
- [FastAPI](https://fastapi.tiangolo.com/) for the amazing web framework
- [React](https://reactjs.org/) for the frontend framework
- All other open-source contributors

## 📞 Contact

Your Name - [@yourusername](https://twitter.com/yourusername)

Project Link: [https://github.com/yourusername/doctalk](https://github.com/yourusername/doctalk) 