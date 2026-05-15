# Quizify

Quizify is a comprehensive web-based quiz application built to provide an interactive and engaging platform for testing knowledge in computer science topics, with a focus on data structures and algorithms. The application emphasizes user experience through secure authentication, timed challenges, and detailed performance feedback. It serves as a tool for self-assessment, educational practice, or simulated exam environments.

## Project Overview

Quizify is designed as a single-page application (SPA) with multiple views, utilizing vanilla JavaScript for client-side logic and localStorage for data persistence. The app includes robust authentication guards to protect user sessions, automatic grading with visual feedback on incorrect answers, and a responsive design that adapts to various devices. Key components include user registration and login, a timed quiz interface, and a results page that highlights strengths and areas for improvement.

The project demonstrates modern web development practices, including modular JavaScript architecture, CSS utility frameworks for styling, and client-side routing through direct page navigation.

## Features

- **Authentication System**: Secure user registration and login with session management. Authentication guards automatically redirect users based on login status, ensuring private pages are accessible only to authenticated users.
- **Timed Quizzes**: Interactive quiz sessions with a countdown timer that adds urgency and simulates real exam conditions. Users must complete questions within the allotted time.
- **Question Management**: Multiple-choice questions with flagging capabilities for review. Questions are stored client-side and can be easily extended.
- **Automatic Grading**: Real-time calculation of scores based on correct answers. Each question is worth 1 point, with total scores displayed prominently.
- **Detailed Results Review**: Post-quiz analysis showing correct and incorrect answers. Wrong answers are highlighted in red, while correct answers (including the right choice for missed questions) are marked in green, enabling learning from mistakes.
- **Theme Switching**: Dark and light mode toggle for improved accessibility and user preference.
- **Responsive Design**: Mobile-first approach using Tailwind CSS, ensuring compatibility across devices.
- **Session Persistence**: User data, quiz progress, and results are stored in browser localStorage, allowing for seamless session continuity.

## Application Flow

1. **Entry Point**: Users land on the index page, where they can choose to register or login.
2. **Authentication**: New users register with username, email, and password. Existing users login. Authentication guards enforce access control:
   - Unauthenticated users are redirected to the index page if attempting to access private areas.
   - Authenticated users are automatically redirected to the landing page if on public pages.
3. **Landing Page**: Authenticated users access the main dashboard, where they can start the quiz or view options.
4. **Quiz Session**: Users navigate to the question page, where they answer multiple-choice questions under time pressure. Questions can be flagged for later review.
5. **Submission and Grading**: Upon completion or time expiration, answers are automatically graded. Scores are calculated by comparing user selections against correct answers.
6. **Results Page**: Detailed grade report displays overall score, individual question results, and visual indicators for correct/incorrect answers. Users can review their performance and learn from errors.
7. **Logout**: Users can end their session, clearing authentication data.

## Technologies Used

- **Frontend**: HTML5, CSS3 (Tailwind CSS for utility-based styling), Vanilla JavaScript (ES6+)
- **Storage**: Browser localStorage API for client-side data persistence
- **Build Tools**: Tailwind CLI for CSS compilation and development workflow
- **Fonts**: Google Fonts (Manrope) for typography
- **Icons and Assets**: Custom icons and images stored in the assets folder

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/Quizify.git
   cd Quizify
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Build the CSS:
   ```
   npm run build
   ```

4. For development with auto-reload:
   ```
   npm run dev
   ```

## Usage

1. Open `pages/index.html` in your web browser to start the application.
2. Register a new account or login with existing credentials.
3. From the landing page, initiate the quiz.
4. Answer the questions within the time limit, flagging any for review if needed.
5. Upon completion, view your detailed grade report, which highlights correct answers in green and incorrect ones in red, showing the correct choice for wrong answers.
6. Logout to end the session.

## Project Structure

- `pages/`: HTML files for different application views (index.html - entry/login, landing.html - dashboard, question.html - quiz, grade.html - results)
- `js/`: JavaScript modules handling specific functionalities:
  - `auth-guard.js`: Enforces authentication and page access control
  - `login.js` & `register.js`: Handle user authentication
  - `landing.js`: Manages the main dashboard
  - `exam.js`: Contains quiz questions and logic
  - `timer.js`: Implements the countdown timer
  - `grade.js`: Performs automatic grading and results display
  - `theme.js`: Handles theme switching
- `src/`: CSS source files (input.css, output.css) and compiled styles
- `assets/`: Static assets like icons and images
- `package.json`: Project dependencies and scripts

## Contributing

Contributions are welcome! Please fork the repository and submit pull requests for enhancements, bug fixes, or new features. Ensure code follows the existing modular structure and includes appropriate comments.

## License

This project is licensed under the ISC License.

## Project Structure

- `pages/`: HTML pages for different views (login, quiz, grade, etc.)
- `js/`: JavaScript files for functionality (auth, quiz logic, timer, etc.)
- `src/`: CSS source files and compiled output
- `assets/`: Images and icons

## Contributing

Feel free to fork the repository and submit pull requests for improvements or new features.

## License

This project is licensed under the ISC License.
