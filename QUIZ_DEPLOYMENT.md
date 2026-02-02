# Maps Ground Truth Quiz - Deployment Guide

## Overview

The `quiz.html` file is a self-contained interactive quiz tool that tests knowledge on Maps Ground Truth topics including:

- **Speed Propagation Rules** (18 questions) - Country-specific junction behavior
- **Confidence Values** (15 questions) - When to use Confidence 0-8
- **Glossary & Concepts** (18 questions) - Core terms and definitions
- **Editing Legal Speed** (15 questions) - V_Value and workflow
- **Junctions & Roundabouts** (12 questions) - Rules for speed at intersections
- **Country-Specific Rules** (15 questions) - Rules for specific countries

## Features

- "Start Creating a Quiz" welcome screen
- Topic selection with 6 categories
- 10 randomly selected questions per quiz
- Instant feedback with explanations after each answer
- Score tracking and progress display
- Detailed results with question review
- Mobile-responsive design

---

## Deployment Options

### Option 1: GitHub Pages (Recommended)

1. **Create a GitHub repository** (or use an existing one)

2. **Upload the quiz.html file** to the repository

3. **Enable GitHub Pages**:
   - Go to repository Settings → Pages
   - Select "main" branch as source
   - Click Save

4. **Access URL** will be:
   ```
   https://[username].github.io/[repo-name]/quiz.html
   ```

5. **Embed in Confluence**:
   - In Confluence, edit your page
   - Add an "iframe" macro or use HTML macro with:
   ```html
   <iframe src="https://[username].github.io/[repo-name]/quiz.html" 
           width="100%" 
           height="800px" 
           frameborder="0"
           style="border: none;">
   </iframe>
   ```

---

### Option 2: Confluence Attachment

1. **Upload quiz.html** as an attachment to a Confluence page

2. **Get the attachment URL**:
   - Right-click on the attachment → Copy link address
   - URL format: `https://[domain]/wiki/download/attachments/[pageId]/quiz.html`

3. **Embed using iframe macro**:
   ```html
   <iframe src="[attachment-url]" 
           width="100%" 
           height="800px" 
           frameborder="0">
   </iframe>
   ```

**Note**: Some Confluence instances may restrict iframe sources. Check with your admin.

---

### Option 3: Company Static Hosting

If you have internal static hosting:

1. Upload `quiz.html` to your static server
2. Use the URL in Confluence iframe

---

## Confluence Macro Options

### Using HTML Macro
```html
<iframe src="YOUR_QUIZ_URL" width="100%" height="800px" frameborder="0"></iframe>
```

### Using Widget Connector Macro
- Paste the quiz URL directly
- Adjust dimensions as needed

### Recommended iframe settings
- Width: 100% (responsive)
- Height: 750-850px (to avoid scrolling inside iframe)
- Border: none

---

## Customization

### Adding New Questions

In the `quiz.html` file, find the `questionBanks` object and add questions:

```javascript
{
    question: "Your question text?",
    options: ["Option A", "Option B", "Option C", "Option D"],
    correct: 0,  // Index of correct answer (0-3)
    explanation: "Explanation shown after answering."
}
```

### Adding New Topics

Add a new entry to `questionBanks`:

```javascript
"new-topic-key": {
    name: "Topic Display Name",
    icon: "🎯",  // Emoji icon
    description: "Short description",
    questions: [
        // Array of question objects
    ]
}
```

### Changing Number of Questions

Find this line and change `10` to your desired number:
```javascript
currentQuestions = shuffleArray([...topic.questions]).slice(0, 10);
```

---

## Content Sources

All questions are derived from the Maps Ground Truth Project Confluence pages:

| Topic | Source Page |
|-------|-------------|
| Speed Propagation | [5. Speed Propagation Rules](https://mobileye-perfects.atlassian.net/wiki/spaces/REM/pages/1160773655) |
| Confidence Values | [Legal Speed Guide](https://mobileye-perfects.atlassian.net/wiki/spaces/REM/pages/1159495708) |
| Glossary | [1. Glossary and Concepts](https://mobileye-perfects.atlassian.net/wiki/spaces/REM/pages/1161101313) |
| Editing | [3. How to Edit Legal Speed](https://mobileye-perfects.atlassian.net/wiki/spaces/REM/pages/1160019991) |
| Junctions | [Day 2 - Legal Speed Training](https://mobileye-perfects.atlassian.net/wiki/spaces/REM/pages/727024139) |
| Country Rules | Various country-specific LS Rules pages |

---

## Troubleshooting

### Quiz doesn't load in Confluence
- Check if your Confluence allows iframes from external sources
- Try the attachment method instead
- Contact Confluence admin about Content Security Policy settings

### Questions appear in same order
- This shouldn't happen - questions are shuffled using Fisher-Yates algorithm
- Try clearing browser cache

### Styling looks different in iframe
- The quiz is self-contained with all styles inline
- Should render consistently across browsers

---

## File Info

- **File**: `quiz.html`
- **Size**: ~45KB
- **Dependencies**: None (self-contained)
- **Browser Support**: All modern browsers (Chrome, Firefox, Safari, Edge)
