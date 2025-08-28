# student_enquiry_chatbot

## Overview
This is an intelligent chatbot application designed to provide automated student enquiry services for educational institutions. The chatbot uses natural language processing (NLP) and machine learning to understand student queries and provide relevant information about college admissions, courses, fees, facilities, and other academic services.

## Key Features

### 🤖 **Intelligent Chat Interface**
- Web-based chatbot interface with real-time conversation capabilities
- Natural language understanding for student queries
- Context-aware responses based on trained intent recognition

### 🎓 **Comprehensive Information Coverage**
The chatbot provides information on:
- **Admissions**: Application process, requirements, and deadlines
- **Academic Programs**: Available courses, degrees, and specializations
- **Fees Structure**: Tuition fees, payment details, and financial information
- **Scholarships**: Merit-based scholarships and financial aid programs
- **Campus Facilities**: Infrastructure, hostels, labs, library, and recreational facilities
- **Placements**: Career opportunities, placement statistics, and recruitment information
- **Contact Information**: Phone numbers, email addresses, and office locations
- **College Hours**: Operating times and working days

### 🔧 **Technical Architecture**

#### **Machine Learning Components**
- **Neural Network Model**: Custom PyTorch-based neural network for intent classification
- **NLP Processing**: NLTK for text tokenization and stemming using Lancaster Stemmer
- **Training Pipeline**: Automated model training with configurable epochs and learning rates
- **Bag-of-Words**: Feature extraction for text input processing

#### **Web Application**
- **Backend**: Flask web framework for API endpoints and server management
- **Frontend**: HTML templates with responsive design for chat interface
- **RESTful API**: JSON-based communication between frontend and backend
- **Static Files**: CSS and JavaScript for enhanced user experience

#### **Data Management**
- **Intent Database**: Comprehensive JSON dataset with 863+ intent patterns
- **Model Persistence**: Trained model weights and vocabulary saved as .pth files
- **Cross-Platform Compatibility**: Proper file path handling for different operating systems

## Project Structure
```
project/
├── code/
│   ├── app.py                 # Main Flask application
│   ├── model_train.py         # Neural network training script
│   ├── model.pth             # Trained model weights
│   ├── data.pth              # Vocabulary and labels
│   ├── templates/            # HTML templates for web interface
│   │   ├── home.html
│   │   ├── chat.html
│   │   ├── login.html
│   │   └── register.html
│   └── static/               # CSS and JavaScript files
└── dataset/
    └── intents.json          # Training data with student queries and responses
```

## Technology Stack
- **Programming Language**: Python 3.x
- **Web Framework**: Flask
- **Machine Learning**: PyTorch, NumPy
- **Natural Language Processing**: NLTK
- **Frontend**: HTML5, CSS3, JavaScript
- **Data Format**: JSON

## Installation & Setup

### Prerequisites
Ensure you have Python 3.x installed on your system.

### Dependencies Installation
Install the required Python packages:
```bash
pip install flask torch numpy nltk
```

### NLTK Data Download
Download required NLTK data (punkt tokenizer):
```python
import nltk
nltk.download('punkt')
```

### Project Setup Commands

1. **Navigate to the code directory**:
```bash
cd path/to/your/project/code
```

2. **Train the Model** (if needed):
```bash
python model_train.py
```
This command will:
- Load the training data from intents.json
- Train the neural network model
- Save the trained model as [model.pth](file://c:\Users\bindu\Downloads\code-20250827T134235Z-1-001\model.pth)
- Save vocabulary and labels as [data.pth](file://c:\Users\bindu\Downloads\code-20250827T134235Z-1-001\data.pth)

3. **Run the Application**:
```bash
python app.py
```
This starts the Flask development server.

4. **Access the Application**:
Open your web browser and navigate to:
```
http://localhost:5000
```
or
```
http://127.0.0.1:5000
```

### Development Commands

**Check Python Version**:
```bash
python --version
```

**Install Dependencies from Requirements** (if available):
```bash
pip install -r requirements.txt
```

**Run in Debug Mode** (for development):
```bash
python app.py
```
(Debug mode is already enabled in the code with `app.run(debug=True)`)

**Stop the Server**:
Press `Ctrl+C` in the terminal where the server is running.

## API Endpoints

### Web Routes
- `GET /` - Home page
- `GET /login` - Login page
- `GET /register` - Registration page
- `GET /chat` - Chat interface

### API Routes
- `POST /get_response` - Get chatbot response
  ```json
  Request: {"message": "your question here"}
  Response: {"response": "chatbot answer"}
  ```

## Usage Examples

### Testing the Chatbot
Once the server is running, you can test the chatbot with queries like:
- "Hello" (greeting)
- "What courses do you offer?" (course information)
- "What are the fees?" (fee structure)
- "Tell me about admissions" (admission process)
- "What are the college timings?" (operating hours)

## Use Cases
- **Student Support**: 24/7 automated assistance for student inquiries
- **Admission Guidance**: Information for prospective students
- **Academic Advising**: Course and program information
- **Campus Services**: Facility and service details
- **Administrative Queries**: Contact information and office hours

## Benefits
- **Reduces Manual Workload**: Automates repetitive student inquiries
- **Improves Response Time**: Instant answers to common questions
- **Scalable Solution**: Can handle multiple concurrent users
- **Consistent Information**: Provides standardized responses
- **Cost-Effective**: Reduces need for human support staff for basic queries

## Troubleshooting

**Common Issues and Solutions**:

1. **Module not found errors**:
```bash
pip install missing_module_name
```

2. **Port already in use**:
```bash
# Kill process using port 5000
netstat -ano | findstr :5000
taskkill /PID <process_id> /F
```

3. **File path issues**:
Ensure you're running commands from the correct directory and that all required files exist.

This project demonstrates the practical application of machine learning and web development technologies to solve real-world problems in educational institutions, providing an efficient and user-friendly solution for student information services.
