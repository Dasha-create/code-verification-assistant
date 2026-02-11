# ⚡ Code Review Assistant

A fast, interactive code review tool that helps you quickly identify common issues in Python, PHP, JavaScript, and TypeScript code.

![Code Review Assistant](https://img.shields.io/badge/languages-Python%20%7C%20PHP%20%7C%20JavaScript%20%7C%20TypeScript-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## 🎯 Features

- **Multi-Language Support**: Analyzes Python, PHP, JavaScript, and TypeScript
- **Instant Analysis**: Real-time code review with instant feedback
- **Security Focused**: Detects SQL injection, XSS vulnerabilities, and dangerous functions
- **Best Practices**: Identifies code quality issues and anti-patterns
- **Clean UI**: Modern, responsive interface with severity-based prioritization
- **No Installation**: Works directly in your browser

## 🚀 Quick Start

### Option 1: Use Online

1. Download `code-review-assistant.html`
2. Open it in any modern web browser
3. Paste your code and click "Analyze Code"

### Option 2: Clone Repository

```bash
git clone https://github.com/YOUR-USERNAME/code-review-assistant.git
cd code-review-assistant
# Open code-review-assistant.html in your browser
```

## 📋 What It Detects

### Python
- SQL injection vulnerabilities
- Bare except clauses
- Mutable default arguments
- Dangerous `eval()` and `exec()` usage
- Improper None comparisons
- Missing f-strings
- Global variable usage

### PHP
- SQL injection (unsanitized input)
- XSS vulnerabilities
- Deprecated `mysql_*` functions
- Loose comparisons (`==` vs `===`)
- Error suppression with `@`
- Dangerous `eval()` usage

### JavaScript/TypeScript
- `var` instead of `let`/`const`
- Loose equality (`==` vs `===`)
- XSS risks with `innerHTML`
- Dangerous `eval()` usage
- Console statements in production
- Callback hell indicators
- TypeScript `any` type usage
- Promise handling issues

## 🎨 Screenshots

The tool provides:
- Color-coded severity badges (High, Medium, Low)
- Line-by-line issue identification
- Clear explanations and recommendations
- Issue statistics dashboard

## 🛠️ Usage Example

```python
# Paste this Python code into the tool:
def get_user(user_id):
    query = f"SELECT * FROM users WHERE id = {user_id}"  # ⚠️ Will detect SQL injection
    cursor.execute(query)
```

The tool will flag:
- **HIGH**: Potential SQL Injection - Use parameterized queries instead

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Add detection rules for more issues
- Improve the UI/UX

## 📝 License

MIT License - feel free to use this tool in your projects!

## 🔮 Future Enhancements

- [ ] Add more language support (Go, Rust, Java)
- [ ] Custom rule configuration
- [ ] Export reports (PDF, JSON)
- [ ] Integration with CI/CD pipelines
- [ ] VSCode extension

## 👨‍💻 Author

Built to speed up code reviews and catch common issues early.

---

**Star ⭐ this repo if you find it useful!**
