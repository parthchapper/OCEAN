# 🧠 OCEAN Personality Test (Streamlit App)

This project is a **button-based OCEAN Personality Assessment** built with **Streamlit**.
Users answer 25 Likert-scale questions, submit their responses, and receive their results **via email**.

The app is fully **session-state safe**, uses **buttons instead of sliders**, prevents submission until **all questions are answered**, and securely sends results using **Streamlit Secrets**.

---

## 📁 Project Structure

```
.
├── app.py        # Main Streamlit application
├── README.md     # Instructions (this file)
```

---

## 🚀 Features

* OCEAN personality model:

  * Openness
  * Conscientiousness
  * Extraversion
  * Agreeableness
  * Emotional Stability
* Button-based Likert scale (1–5)
* Visual red indicator for selected answers
* Submit button disabled until all questions are answered
* Demographics + background information collected
* Email results automatically sent to the user
* Safe across reruns (no double-click bugs)

---

## 🛠 Requirements

* Python **3.9+**
* Streamlit
* Gmail account (or SMTP-compatible email)

Install dependencies:

```bash
pip install streamlit
```

---

## 🔐 Streamlit Secrets Setup

This app **requires email credentials** stored securely.

### Local Development

Create a file at:

```
.streamlit/secrets.toml
```

Add:

```toml
EMAIL = "your_email@gmail.com"
EMAIL_PASSWORD = "your_app_password"
```

⚠️ **Important:**
If using Gmail, you must create an **App Password**, not your normal Gmail password.

---

### Streamlit Cloud Deployment

1. Go to **App Settings → Secrets**
2. Paste:

```toml
EMAIL = "your_email@gmail.com"
EMAIL_PASSWORD = "your_app_password"
```

---

## ▶️ Running the App

From the project folder:

```bash
streamlit run app.py
```

The app will open in your browser automatically.

---

## 🧪 How the Test Works

1. User fills in personal information
2. Clicks **Start Test**
3. Answers all 25 questions using buttons (1–5)
4. A red bar appears under the selected number
5. Submit button activates only when all questions are answered
6. Scores are calculated for each OCEAN trait
7. Results are emailed to the provided email address

---

## 📧 Email Output

The email contains:

* User demographics
* Individual OCEAN trait scores
* Full question-by-question responses

---

## ❗ Common Issues & Fixes

### Buttons not responding?

* Make sure you're using **Streamlit ≥ 1.25**
* Do not run inside Jupyter Notebook

### Email not sending?

* Verify `EMAIL` and `EMAIL_PASSWORD`
* Ensure Gmail App Password is enabled
* Check spam folder

---

## 🔒 Privacy & Security

* No data is stored permanently
* No database used
* Email credentials are never exposed
* Session data resets on refresh

---

## 📌 File Name

The main application file **must be named**:

```
app.py
```

(Streamlit Cloud requires this)

---
