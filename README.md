# TOEFL/IELTS Vocabulary Prep Backend

This backend is designed to support an AI-powered vocabulary preparation app for TOEFL and IELTS exams. It utilizes OpenAI's API (or a similar language model) to generate vocabulary questions, options, and explanations in JSON format, which are then served to the frontend (Android app). The backend is built using **Express.js** and follows a simple REST API structure.

## Features
- **Question Generation**: Dynamically generates questions with multiple-choice options, correct answers, meanings, and explanations.
- **Integration with AI**: Queries OpenAI's API for content generation.
- **JSON Response**: Delivers data in a structured JSON format for easy consumption by the frontend.
- **Scalability**: Can be hosted on platforms like Render, Vercel, or Railway for free or paid deployments.

## API Endpoints

### `GET /toeflQuestions`
- **Description**: Fetches a TOEFL question, options, and related data.
- **Response Format**:
  ```json
  {
    "question": "Aberration",
    "options": [
      "A. Deviation from the normal",
      "B. Extreme happiness",
      "C. A type of bird",
      "D. A rare event"
    ],
    "answer": "A. Deviation from the normal",
    "meaning": "A departure from what is normal, usual, or expected.",
    "explanation": "The word 'aberration' refers to something that deviates from the usual or normal course."
  }
  ```

### `GET /ieltsQuestions`
- **Description**: Fetches an IELTS question, options, and related data.
- **Response Format**: Same as `/toeflQuestions`.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/toefl-ielts-backend.git
   cd toefl-ielts-backend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up environment variables:
   - Create a `.env` file in the root directory.
   - Add your API key for OpenAI:
     ```
     OPENAI_API_KEY=your_openai_api_key
     ```

4. Run the server:
   ```bash
   npm start
   ```

5. Access the backend at `http://localhost:5000`.

## Deployment
You can deploy this backend to any platform that supports Node.js applications. Popular options include:
- **Render**
- **Railway**
- **Vercel**

## Tech Stack
- **Node.js**: Backend runtime.
- **Express.js**: Lightweight web framework.
- **Axios**: For API requests to OpenAI.
- **dotenv**: To manage environment variables.

## Contributions
Feel free to fork this repository and contribute to enhance the functionality. Open issues or create pull requests for suggestions and improvements!

## License
This project is licensed under the MIT License.
