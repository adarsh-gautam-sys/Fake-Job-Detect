# FakeJobDetect 🔍

A modern web application that analyzes job postings to detect potential scams or fake listings using heuristic-based analysis.

## Features

- ✅ Real-time analysis of job postings
- ✅ Suspicious phrase detection
- ✅ Email, URL, and phone number extraction
- ✅ Visual score indicator (0-100)
- ✅ Warning flags with explanations
- ✅ Animated loading states
- ✅ Fully responsive design
- ✅ Modern UI with TailwindCSS

## Installation

1. Make sure you have Node.js installed (v14 or higher)
2. Open a terminal in the `my-fakejob` directory
3. Install dependencies:

```bash
npm install
```

## Running the App

Start the development server:

```bash
npm run dev
```

The app will open at `http://localhost:5173` (or similar port).

## How to Use

1. Copy a job posting from any job board
2. Paste it into the text area on the left
3. Click "🔍 Analyze Job"
4. View the results on the right panel:
   - Fake likelihood score (circular indicator)
   - Summary verdict (Likely Legit / Possibly Suspicious / Likely Fake)
   - Warning flags with specific reasons
   - Extracted emails, URLs, and phone numbers
   - Highlighted suspicious phrases in the text

## How It Works

The analyzer uses heuristic-based detection to identify suspicious patterns:

- **Personal email domains** (gmail, yahoo, etc.)
- **Lack of company website**
- **Too-good-to-be-true salaries** (>$100k without specifics)
- **Suspicious phrases** like "urgent hiring", "apply now", "training fee"
- **Phone without email** (less professional)
- **Poor grammar** and excessive capitalization
- **Vague descriptions** with multiple generic phrases
- **Financial information requests** (bank details, etc.)

The final score (0-100) indicates the likelihood the job is fake.

## Tech Stack

- **React** - UI framework
- **Vite** - Build tool and dev server
- **TailwindCSS** - Styling
- **JavaScript** - Logic and analysis

## Project Structure

```
my-fakejob/
├── src/
│   ├── components/
│   │   ├── Header.jsx       # App header
│   │   ├── Footer.jsx       # App footer
│   │   └── ScoreIndicator.jsx  # Circular score indicator
│   ├── analyzer.js          # Core detection logic
│   ├── App.jsx              # Main application
│   ├── index.css            # Global styles
│   └── main.jsx             # Entry point
├── tailwind.config.js        # Tailwind configuration
└── package.json             # Dependencies

```

## Development

- Build for production: `npm run build`
- Preview production build: `npm run preview`
- Lint code: `npm run lint`

## License

This is a prototype project for educational purposes.
