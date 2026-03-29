# CS 3321 Study Hub

A comprehensive interactive study application for mastering Software Engineering concepts through evidence-based learning techniques.

**🔗 [Live Demo](https://aimal-cs3321-study.netlify.app)** | **⭐ 50+ Active Users**

## Overview

CS 3321 Study Hub is a single-page web application designed to help students prepare for exams using **spaced repetition** and **active recall**—two of the most effective learning techniques supported by cognitive science research.

Built entirely in vanilla JavaScript with no backend required, the app has been deployed across 4 Computer Science courses at University of Houston–Downtown, serving 50+ active student users.

## Key Features

### 📚 Learn Topics
Read structured explanations and definitions before testing yourself. Topics are organized by chapter with definitions, examples, and key concepts.

### 🎓 Study Flashcards (Spaced Repetition)
- Intelligent card ordering: weakest cards appear more frequently
- Rate your confidence on each card (Didn't Know / Partially / Knew It)
- Progress automatically tracked in browser storage
- Optimize study time by focusing on weak areas

### 🧠 Quiz Mode
- **Multiple choice and true/false questions** across selectable chapters
- Immediate feedback on answers with detailed explanations
- Choose which chapters to focus on
- Perfect for targeted practice before exams

### 📋 Exam 2 Mock Exam
- **Full-length practice exam** simulating real testing conditions
- **Balanced question distribution** across all chapters
- **Randomized question order** using Fisher-Yates shuffle algorithm—ensures different questions each attempt, preventing memorization
- 25 questions pulled from 69-question pool
- Detailed results showing performance by topic
- Timer and score calculation

### 📖 Browse All Cards
Review all questions by chapter in a structured format with immediate answer viewing.

### 📊 Progress Tracking
- Session banner shows your score and progress
- Topic cards display color-coded performance
- All data persists using browser localStorage
- Resume your learning exactly where you left off

## Technical Implementation

### Architecture
- **Vanilla JavaScript** DOM manipulation and event-driven architecture
- **Single-page application (SPA)** — instant navigation without page reloads
- **Client-side state management** — all data stays in the browser
- **localStorage persistence** — progress syncs across sessions
- **Responsive design** — works on desktop, tablet, and mobile

### Key Algorithms

#### Fisher-Yates Shuffle (O(n) time complexity)
```javascript
// Ensures unbiased randomization of questions
// Prevents students from memorizing question sequences
function shuffleArray(array) {
  for (let i = array.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [array[i], array[j]] = [array[j], array[i]];
  }
  return array;
}
```

#### Balanced Question Selection
Mock exams intelligently select questions to maintain proportional topic coverage:
- Analyzes total question pool across all topics
- Calculates target question counts per chapter (e.g., 25% of exam = 25% of questions)
- Randomly selects from each chapter bucket
- Shuffles final list for unpredictability

#### Spaced Repetition
Cards appear more frequently based on user confidence ratings:
- **Didn't know (1)**: Card is prioritized and appears sooner
- **Partially (2)**: Medium frequency
- **Knew it (3)**: Card deprioritized, appears less often

### Technology Stack
| Technology | Purpose |
|-----------|---------|
| **HTML5** | Semantic markup and accessibility |
| **CSS3** | Modern styling with flexbox, gradients, animations |
| **Vanilla JavaScript** | DOM manipulation, event handling, state management |
| **localStorage API** | Persistent progress tracking without database |
| **Netlify** | Free, instant deployment with zero configuration |

## Question Bank

- **Total Questions**: 69 multiple-choice and true/false questions
- **Chapter Coverage**: 7 chapters of Software Engineering content
- **Difficulty Variety**: Mixed difficulty levels matching actual exam format
- **Quality Assurance**: Questions validated against actual class quizzes

## Getting Started

### Online (Recommended)
Visit the [live demo](https://aimal-cs3321-study.netlify.app) — no installation required.

### Local Development
1. Clone this repository
2. Open `index.html` in your web browser
3. No build tools or server required

## User Impact & Iteration

This app was built through iterative user feedback:

### Challenge 1: Predictable Question Order
**Problem**: Questions appeared in the same order every time, allowing memorization instead of learning.

**Solution**: Implemented Fisher-Yates shuffle algorithm ensuring true randomization.

**Result**: Users reported exams felt genuinely different on each attempt.

### Challenge 2: Limited Question Variety
**Problem**: Small question pool meant repeated questions across multiple quiz attempts.

**Solution**: Expanded question pool from 25 to 69 questions, selecting 25 per exam.

**Result**: Multiple exam attempts without exhausting the question bank, enabling true spaced repetition.

### Challenge 3: Question Quality Mismatch
**Problem**: Self-created questions didn't match actual exam format and difficulty.

**Solution**: Analyzed actual class quiz questions and rewrote existing questions to match format, difficulty, and style.

**Result**: Mock exam feels like a realistic simulation of actual exams, improving confidence and preparation quality.

## How It Works: Learning Science

**Spaced Repetition**: Reviewing material at increasing intervals strengthens long-term retention. This app implements spaced repetition by prioritizing weaker cards.

**Active Recall**: Testing yourself on material is more effective than passive reading. The quiz and flashcard modes force active recall.

**Immediate Feedback**: Getting instant feedback on quiz answers reinforces learning and corrects misconceptions immediately.

**Low Cognitive Load**: The simple, distraction-free interface reduces cognitive load, allowing students to focus on learning.

## Browser Support

- Chrome/Chromium (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Works on mobile devices

## Data & Privacy

- **All data stays in your browser** — nothing is sent to external servers
- localStorage stores: quiz responses, progress, confidence ratings
- Clear browser data to reset progress
- No account or login required

## Future Enhancements

- Backend storage for syncing progress across devices
- Collaborative study features (share progress with classmates)
- Adaptive difficulty based on performance
- Analytics dashboard showing detailed progress trends
- Export progress reports
- Spaced repetition scheduling with notification reminders

## Deployment

Deployed to **Netlify** — free, fast, and zero-configuration:
1. Push to GitHub
2. Netlify automatically deploys on every push
3. Live at custom domain instantly

## Technical Metrics

| Metric | Value |
|--------|-------|
| Build Size | ~50KB (single HTML file) |
| Load Time | <1s (no dependencies) |
| Browser Support | All modern browsers |
| Mobile Responsive | Yes |
| Offline Capable | Yes (after first load) |

## About This Project

This project demonstrates:
- **Problem identification**: Built to solve a real problem students faced (ineffective study methods)
- **Full-stack thinking**: Frontend + state management + deployment
- **Algorithm implementation**: Fisher-Yates shuffle, balanced selection
- **User-centric development**: Iterated based on actual user feedback
- **Scalability**: Same architecture successfully deployed across 4 different CS courses
- **Learning science**: Built on evidence-based learning techniques (spaced repetition, active recall)

## Questions or Feedback?

This app was built for students, by a student. If you have suggestions for improvement, feel free to reach out or open an issue.

---

**Built with ❤️ for CS 3321 at University of Houston–Downtown**
