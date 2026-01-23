# Qualiti7 — Training Platform Architecture

> Public architecture and system overview for the **Qualiti7** bilingual (EN/FR) training and course-sales platform.  
> The full production source code is maintained in a private repository.

---

## Overview

**Qualiti7** is a bilingual (English / French) training management and course-sales platform designed to support professional IT and technical training programs.

The system has been in real-world production use and supports the full lifecycle of training delivery — from marketing and registration to administration, communication, and reporting.

This public repository exists to **document the platform’s architecture, design decisions, and production patterns**, without exposing proprietary source code or sensitive configuration.

---

<img width="400" height="940" alt="qualiti7 com_en" src="https://github.com/user-attachments/assets/14d0ac68-5680-4454-9aa9-543bd9e2fea3" />

## Platform Capabilities

### 🌐 Public Site
- Bilingual content (EN / FR)
- Course catalog and course detail pages
- Scheduled offerings (in-person, online, webinars)
- Registration workflow
- Payment integration (external provider)
- Automated confirmation and follow-up emails

### 🧑‍💼 Admin Backend
- Secure admin authentication
- Course and training offering management
- Trainer and partner management
- Registrations and attendance tracking
- Events and webinars
- Automated and scheduled email notifications
- File uploads (images, PDFs, course materials)

---

## Technical Stack (Production)

| Layer | Technology |
|-----|-----------|
| Backend | PHP 8.x |
| Database | MySQL |
| Architecture | Custom MVC-style structure |
| Dependency Management | Composer |
| Email | PHPMailer (SMTP) |
| Frontend | HTML / CSS / JavaScript |
| Admin UI | Bootstrap + legacy jQuery |
| CI/CD | GitHub Actions (automated FTP deployment) |
| Hosting | Shared hosting (production & staging) |

---

## Architecture Highlights

- Custom **MVC-style architecture** (Controllers / Models / Views)
- **Prepared statements** and input sanitization for database safety
- **Environment-based configuration** (no secrets committed)
- Stateless request handling suitable for shared hosting
- Automated CI deployment with no manual server uploads
- Bilingual templating strategy for EN / FR content

The system reflects **incremental, production-driven design**, balancing robustness with the constraints of shared hosting environments.

---

## Deployment Model (Production)

- `main` branch → production environment  
- `staging` branch → staging environment  
- Composer dependencies installed in CI
- `vendor/` generated during deployment
- Secrets stored in CI environment variables
- FTP-based deployment adapted to shared hosting

> Deployment credentials, payment keys, and email configuration are intentionally omitted from this repository.

---

## What This Repository Contains

This public repository may include:
- Architectural documentation
- Sanitized configuration examples
- Database schema (without production data)
- Redacted screenshots or UI samples
- Notes on workflows and system behavior

It does **not** include:
- Production source code
- Payment or email credentials
- Customer or registration data
- Proprietary business logic

---

## Why a Public Architecture Repository?

This repository exists to:
- Demonstrate **real-world system design**, not toy examples
- Showcase experience maintaining a **long-running production platform**
- Document architectural trade-offs and constraints
- Provide context for private, client-facing or commercial work

---

## Status

**Production system — source private.**  
This repository is maintained as a **technical architecture and systems showcase**.

---

## Contact

For questions about the platform architecture or collaboration inquiries, feel free to reach out via GitHub.
