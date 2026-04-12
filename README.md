<div align="center">

Dilakna Godagamage - Portfolio

<img src="https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/Flask-2.x-000000?style=for-the-badge&logo=flask&logoColor=white" />
<img src="https://img.shields.io/badge/Deployed%20on-Render-46E3B7?style=for-the-badge&logo=render&logoColor=white" />
<img src="https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge" />
<img src="https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge" />
<img src="https://img.shields.io/github/last-commit/DilaknaH/portfolio?style=for-the-badge&color=blue" />

<br/>

**A modern, fully responsive personal portfolio website built with Python & Flask — deployed permanently for free.**

[Live Demo](portfolio-rho-vert-79.vercel.app)

</div>

---

## 📋 Table of Contents

- [About](#-about)
- [Tech Stack](#-tech-stack)
- [Features](#-features)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Local Development](#local-development)
- [Environment Variables](#-environment-variables)
- [Migrating from Streamlit](#-migrating-from-streamlit)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)

---

##  About

This is my personal portfolio , built to showcase projects, skills, and experience in a clean, professional, and permanently hosted environment.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Backend | Python 3.10+, Flask 2.x |
| Frontend | HTML5, CSS3, Jinja2 Templates |
| Static Assets | Bootstrap 5 / Tailwind CSS |
| Deployment | Render / Railway / Vercel |
| Version Control | Git & GitHub |

---

##  Features

- ⚡ **Fast & Lightweight** — minimal dependencies, fast load times
- 📱 **Fully Responsive** — works on all screen sizes
- 🎨 **Custom Theming** — easily personalizable via CSS variables
- 📬 **Contact Form** — with email integration (no backend cost)
- 🌐 **Permanent Free Hosting** — no sleep timers, no expiry
- 🔒 **Environment Variable Support** — for secrets management

---

## Project Structure

```
portfolio/
├── app.py                  # Flask application entry point
├── requirements.txt        # Python dependencies
├── Procfile                # For Render/Railway deployment
├── runtime.txt             # Python version pin
├── .env.example            # Environment variable template
├── static/
│   ├── css/
│   │   └── style.css
│   ├── js/
│   │   └── main.js
│   └── images/
│       └── profile.jpg
├── templates/
│   ├── base.html
│   ├── index.html
│   ├── projects.html
│   └── contact.html
└── README.md
```

---

##  Getting Started

### Prerequisites

- Python 3.10 or higher
- pip (Python package manager)
- Git

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/DilaknaH/portfolio.git
   cd portfolio
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate        # macOS/Linux
   venv\Scripts\activate           # Windows
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**
   ```bash
   cp .env.example .env
   # Edit .env with your values
   ```

5. **Run locally**
   ```bash
   python app.py
   ```
   Visit `http://localhost:5000` in your browser.

---

## ☁️ Deployment Guide (Free & Permanent)

> ⚠️ **Why not Streamlit Cloud?** Streamlit Community Cloud puts apps to sleep after inactivity and has limited customization. The options below are **always-on, free, and professional.**

---

## Environment Variables

Create a `.env` file in the root directory. Never commit this file — it's in `.gitignore`.

```env
# Flask
FLASK_ENV=production
SECRET_KEY=your-secret-key-here

# Contact form (e.g. EmailJS or Formspree)
CONTACT_EMAIL=your@email.com
EMAILJS_SERVICE_ID=your_service_id
EMAILJS_TEMPLATE_ID=your_template_id
EMAILJS_PUBLIC_KEY=your_public_key
```

See `.env.example` for the full template.

---

## Migrating from Streamlit

If your portfolio was originally built with Streamlit, here's how to migrate:

| Streamlit | Flask Equivalent |
|---|---|
| `st.title("Hello")` | `<h1>Hello</h1>` in HTML template |
| `st.write("text")` | `<p>text</p>` or `{{ variable }}` in Jinja2 |
| `st.image("img.png")` | `<img src="{{ url_for('static', filename='images/img.png') }}">` |
| `st.columns(2)` | CSS Flexbox / Bootstrap Grid |
| `st.sidebar` | HTML `<nav>` sidebar |
| `st.form` | HTML `<form>` with Flask route handler |

**Minimal Flask app skeleton:**

```python
# app.py
from flask import Flask, render_template, request

app = Flask(__name__)

@app.route("/")
def home():
    return render_template("index.html")

@app.route("/contact", methods=["POST"])
def contact():
    name = request.form.get("name")
    email = request.form.get("email")
    message = request.form.get("message")
    # Handle form submission
    return render_template("index.html", success=True)

if __name__ == "__main__":
    app.run(debug=True)
```

---

## Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add some amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

---

## License

Distributed under the **MIT License**. See [`LICENSE`](LICENSE) for more information.

```
MIT License

Copyright (c) 2024 Dilakna H

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
```

---

##  Contact

**Dilakna Godagamage**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square&logo=linkedin)](https://linkedin.com/in/your-profile)
[![Email](https://img.shields.io/badge/Email-your@email.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:your@email.com)

---

<div align="center">

Made with ❤️ by [Dilakna H](https://github.com/DilaknaH)

⭐ Star this repo if you found it helpful!

</div>
