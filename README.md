# 🚀 AI-Based Social Media Automation System

A modern full-stack web application designed to simplify social media content creation, AI caption generation, and automated publishing to Facebook and Instagram from a single, centralized dashboard.

---

## 📌 1. Project Overview
The **AI-Based Social Media Automation System** is a web platform built to automate and streamline content publishing. Users can easily create posts manually or leverage AI to generate engaging captions and relevant hashtags tailored to specific topics, audiences, and tones. 

### Key Capabilities:
* **Unified Dashboard:** Manage Facebook and Instagram posts from a single interface.
* **AI Content Creation:** Automatic caption & hashtag generator using OpenAI API.
* **Meta API Integration:** Direct publishing to Facebook Pages and Instagram Professional accounts.
* **Post History & Analytics:** Real-time publishing status (Published, Partial, Failed).

---

## 🪓 2. Problem Statement
Managing social media accounts manually across multiple platforms is time-consuming and fragmented:
* Creating engaging captions and hashtags consistently is challenging for many users.
* Publishing content manually on Facebook and Instagram separately requires repetitive manual effort.
* Tracking post history and debugging failed attempts across multiple dashboards is difficult.

**The Solution:** This system centralizes manual creation, AI-assisted content generation, and multi-platform publishing into one cohesive web application.

---

## 🎯 3. Project Objectives
* Develop a responsive, user-friendly SaaS-style interface.
* Implement secure user authentication and authorization.
* Provide an AI assistant for automatic caption and hashtag generation.
* Connect official **Facebook Graph API** and **Instagram Platform API**.
* Support cross-posting to Facebook and Instagram with real-time status tracking.
* Maintain complete post history, media previews, and error logs.

---

## ✨ 4. Main Features & Functionalities

### 🔐 4.1 User Authentication & Security
* Secure registration, login, and profile management.
* Strict authorization ensures users only access their own connected accounts and posts.

### 📊 4.2 Centralized Dashboard
* High-level summary of total posts, successful publishes, failed attempts, and connected social accounts.
* Real-time metrics backed by actual database records.

### 🤖 4.3 AI Content Generator
* Integrated with **OpenAI API**.
* Inputs: Topic, target audience, tone, keywords, and objective.
* Output: Smart captions and optimized hashtags with full edit/preview controls before publishing.

### 📝 4.4 Manual Post Creation & Media Management
* Custom post editor supporting text and image uploads.
* Built-in validation for image formats and media constraints before submitting requests.

### 🌐 4.5 Meta API Integrations (Facebook & Instagram)
* **Facebook Graph API:** Authenticated posting directly to eligible Facebook Pages.
* **Instagram Platform API:** Support for Instagram Business & Creator accounts.
* **Multi-Platform Publishing:** Send content to Facebook, Instagram, or both simultaneously with independent status tracking per channel.

### 📋 4.6 History & Error Handling
* Comprehensive log displaying statuses: `Draft`, `Publishing`, `Published`, `Partially Published`, and `Failed`.
* Detailed error messages for token expiration, rate limits, or media validation issues.

---

## 🛠 5. Technology Stack

| Component | Technology | Purpose |
| :--- | :--- | :--- |
| **Frontend** | React.js, TypeScript, Tailwind CSS | Modern Responsive SaaS UI |
| **Backend** | Python, Django REST Framework | Business Logic & RESTful APIs |
| **Database** | PostgreSQL | Relational storage for users, posts, and tokens |
| **AI Integration** | OpenAI API | Automatic Caption & Hashtag Generation |
| **Social APIs** | Meta APIs (Facebook & Instagram) | Official Publishing Integration |
| **Async Tasks** | Celery & Redis (Optional) | Background task queue for publishing |
| **Version Control**| Git & GitHub | Source Code Management |

---

## 🔄 6. System Workflow

1. **Authentication:** User logs into the platform.
2. **Account Linking:** User connects Facebook Page and/or Instagram Professional Account via OAuth.
3. **Content Creation:** User writes a post manually OR inputs parameters for AI content generation.
4. **Media & Destination:** User uploads media, previews the post layout, and selects destination platform(s) (Facebook / Instagram).
5. **Backend Processing:** Django REST API validates inputs, tokens, and media specifications.
6. **API Dispatch:** Backend dispatches requests to Meta Graph APIs.
7. **Status Update:** Results are saved in PostgreSQL and status updates are reflected on the Dashboard.

---

## 🗄 7. Database Architecture

The PostgreSQL database manages the following core entities:
* `Users`: Authentication data and profile info.
* `Social Accounts`: Access tokens, account IDs, and connection status.
* `Posts`: Caption text, uploaded media links, owner IDs, and creation timestamps.
* `Post Publications`: Per-platform status tracking (`SUCCESS`, `FAILED`, error logs, platform post IDs).
* `Activity Logs`: Audit trails for major application events.

---

## 🔒 8. Security & Privacy
* Passwords secured using Django's default PBKDF2 hashing algorithm.
* Social media access tokens and API secret keys stored encrypted server-side; **never exposed to frontend API payloads**.
* Environment variables (`.env`) used for all sensitive configuration credentials.

---

## 📋 9. Project Scope & Future Roadmap

### ✅ In Scope (Current Implementation)
* Full Auth & Dashboard system.
* AI-assisted caption generation.
* Image uploads & preview.
* Direct publishing to Facebook Pages & Instagram Professional accounts.
* Multi-platform status logging.

### ❌ Out of Scope (Future Enhancements)
* Scheduled or recurring post publishing.
* Advanced social media analytics.
* Automated collection of detailed engagement metrics.
* Subscription and payment management.

---

## 🏁 10. Conclusion
This project demonstrates practical full-stack software development by combining **AI processing**, **relational database management**, and **official enterprise APIs (Meta)** into a streamlined product tailored for modern digital content creators focusing on Facebook and Instagram.