# MathDoc Benchmark Dashboard

[![Deploy to GitHub Pages](https://github.com/your-username/MathDoc-benchmark/workflows/Deploy%20MathDoc%20to%20GitHub%20Pages/badge.svg)](https://github.com/your-username/MathDoc-benchmark/actions)

📊 **Interactive leaderboard dashboard** for the MathDoc benchmark - evaluating structured extraction from noisy scanned high-school mathematics exams.

## 🎯 Benchmark Overview

**MathDoc** evaluates how models handle:
- **Noisy, scanned exam papers** (3,609 questions)
- **Structured extraction** tasks (question text, options, formulas)
- **Active Refusal** - the ability to say "I don't know"

## 📈 Dashboard Features

### 1. Question Types Distribution
- Doughnut chart showing 3,609 questions breakdown:
  - Choice: 1,250 questions
  - Fill-in-the-Blank: 1,100 questions
  - Subjective: 1,259 questions

### 2. Top 3 Models Battle
- Radar chart comparing top models across **5 complete metrics**:
  - ✅ Stem Accuracy
  - ✅ Visual Similarity
  - ✅ Recall
  - ✅ Precision
  - ✅ Refusal F1 Score

### 3. Average Question Length
- Bar chart showing character count by question type:
  - Choice: 180 chars
  - Blank: 110 chars
  - Subjective: 195 chars

### 4. Average Formula Ratio
- Bar chart showing formula content percentage:
  - Choice: 50%
  - Blank: 47%
  - Subjective: 44%

## 🚀 Live Demo

Visit the dashboard: **[https://your-username.github.io/MathDoc-benchmark/](https://your-username.github.io/MathDoc-benchmark/)**

## 🛠️ Tech Stack

- **Vue 3** - Reactive UI framework
- **Chart.js** - Beautiful data visualizations
- **Tailwind CSS** - Utility-first styling
- **No build step required** - Pure HTML/JS, CDN-hosted libraries

## 📦 Setup Locally

```bash
# Clone the repository
git clone https://github.com/your-username/MathDoc-benchmark.git

# Open in browser
open MathDoc-benchmark/index.html
# or
python -m http.server 8000
# Visit http://localhost:8000
```

## 📝 Customization

Edit `index.html` to modify:

### Update Model Data
```javascript
datasets: {
    'solve': [
        { model: "Your-Model", type: "Open Source",
          stem: 85.0, visual: 50.0, recall: 40.0,
          precision: 70.0, refusalF1: 55.0, final: 62.0 },
        // ...
    ]
}
```

### Update Statistics
```javascript
datasetStats: {
    choice: 1250,
    blank: 1100,
    subjective: 1259
},
avgLength: {
    choice: 180,
    blank: 110,
    subjective: 195
},
formulaRatio: {
    choice: 50,
    blank: 47,
    subjective: 44
}
```

## 📄 Citation

```bibtex
@article{mathdoc2026,
  title={MathDoc: Benchmarking Structured Extraction from Noisy Scanned High-School Mathematics Exams},
  author={...},
  journal={...},
  year={2026}
}
```

## 🤝 Contributing

Feel free to submit issues and pull requests!

## 📊 Dataset

**Data Source**: 2013-2023 National College Entrance Examination (Gaokao) Mathematics Papers
- **Total Questions**: 3,609
- **Question Types**: Choice, Fill-in-the-Blank, Subjective
- **Challenges**: Handwritten annotations, complex formulas, noise

---

**Made with ❤️ for the MathDoc benchmark project**
