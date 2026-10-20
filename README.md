Supermail

A developer-focused email API platform.

Supermail is an email API platform designed to help developers send emails, manage templates, configure sender domains, and track email activity through a centralized dashboard and REST API.

<p align="center">
  <img src="https://img.shields.io/badge/Next.js-Framework-black?logo=nextdotjs" alt="Next.js">
  <img src="https://img.shields.io/badge/TypeScript-Language-3178C6?logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Better_Auth-Authentication-333333" alt="Better Auth">
  <img src="https://img.shields.io/badge/PostgreSQL-Database-4169E1?logo=postgresql&logoColor=white" alt="PostgreSQL">
</p>

⸻

🔗 Quick Links

* Overview
* Technology Stack
* Architecture
* Getting Started
* Environment Variables
* Documentation
* Security
* Project Status
* Contributing
* License

Resource	Description
🌐 Website	Supermail’s official website — coming soon
📚 Documentation	Developer guides and API documentation — coming soon
🔌 API Reference	Endpoint reference and request examples — coming soon
💻 Repository	Source code, issues, and project development
🚀 Getting Started	Set up Supermail locally using this README

✨ Overview

Supermail is being developed as a centralized email-sending service for websites, applications, and backend services.

Planned Features

* REST API for sending emails.
* API key creation, management, and revocation.
* Email verification using codes and links.
* Reusable email templates.
* Sender identity and domain management.
* Email history and sending status.
* Usage tracking and quotas.
* Developer dashboard.
* API documentation.
* Hosted Supermail Cloud service.

Features will be marked as available once implemented and tested.

🧰 Technology Stack

<table>
  <thead>
    <tr>
      <th align="left">Technology</th>
      <th align="left">Purpose</th>
      <th align="left">Resources</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><img src="https://cdn.simpleicons.org/nextdotjs/000000" width="28" alt="Next.js logo"><br><strong>Next.js</strong></td>
      <td>Web application, dashboard, and API routes.</td>
      <td><a href="https://nextjs.org/">Website</a> · <a href="https://nextjs.org/docs">Docs</a></td>
    </tr>
    <tr>
      <td><img src="https://cdn.simpleicons.org/react/61DAFB" width="28" alt="React logo"><br><strong>React</strong></td>
      <td>Interactive interfaces and reusable components.</td>
      <td><a href="https://react.dev/">Website</a> · <a href="https://react.dev/learn">Docs</a></td>
    </tr>
    <tr>
      <td><img src="https://cdn.simpleicons.org/typescript/3178C6" width="28" alt="TypeScript logo"><br><strong>TypeScript</strong></td>
      <td>Type-safe frontend and backend development.</td>
      <td><a href="https://www.typescriptlang.org/">Website</a> · <a href="https://www.typescriptlang.org/docs/">Docs</a></td>
    </tr>
    <tr>
      <td><img src="https://cdn.simpleicons.org/tailwindcss/06B6D4" width="28" alt="Tailwind CSS logo"><br><strong>Tailwind CSS</strong></td>
      <td>Responsive styling and dashboard design.</td>
      <td><a href="https://tailwindcss.com/">Website</a> · <a href="https://tailwindcss.com/docs">Docs</a></td>
    </tr>
    <tr>
      <td><img src="https://cdn.simpleicons.org/betterauth/000000" width="28" alt="Better Auth logo"><br><strong>Better Auth</strong></td>
      <td>Authentication, sessions, and verification flows.</td>
      <td><a href="https://www.better-auth.com/">Website</a> · <a href="https://www.better-auth.com/docs">Docs</a></td>
    </tr>
    <tr>
      <td><img src="https://cdn.simpleicons.org/neon/00E599" width="28" alt="Neon logo"><br><strong>Neon</strong></td>
      <td>Hosted PostgreSQL database.</td>
      <td><a href="https://neon.com/">Website</a> · <a href="https://neon.com/docs">Docs</a></td>
    </tr>
    <tr>
      <td><img src="https://cdn.simpleicons.org/drizzle/8B5CF6" width="28" alt="Drizzle ORM logo"><br><strong>Drizzle ORM</strong></td>
      <td>Typed database queries and schema migrations.</td>
      <td><a href="https://orm.drizzle.team/">Website</a> · <a href="https://orm.drizzle.team/docs">Docs</a></td>
    </tr>
    <tr>
      <td><img src="https://cdn.simpleicons.org/bun/000000" width="28" alt="Bun logo"><br><strong>Bun</strong></td>
      <td>JavaScript runtime and package manager.</td>
      <td><a href="https://bun.sh/">Website</a> · <a href="https://bun.sh/docs">Docs</a></td>
    </tr>
    <tr>
      <td><img src="https://cdn.simpleicons.org/deno/000000" width="28" alt="Deno logo"><br><strong>Deno Deploy</strong></td>
      <td>Planned hosting for the Supermail application.</td>
      <td><a href="https://deno.com/deploy">Website</a> · <a href="https://docs.deno.com/deploy/">Docs</a></td>
    </tr>
    <tr>
      <td><img src="https://cdn.simpleicons.org/github/181717" width="28" alt="GitHub logo"><br><strong>BunMail</strong></td>
      <td>Email-sending engine integrated with Supermail.</td>
      <td><a href="https://github.com/mohamedboukari/bunmail">Repository</a></td>
    </tr>
  </tbody>
</table>

🏗️ Architecture

Supermail connects the developer dashboard, REST API, authentication, database, and email-sending engine.

1. A developer creates a Supermail account.
2. Better Auth manages authentication and sessions.
3. Neon stores Supermail’s application data.
4. The developer creates an API key.
5. Their application sends a request to the Supermail REST API.
6. Supermail validates the request, permissions, and usage limits.
7. The backend calls BunMail to send the email.
8. Supermail records the result and displays available message activity.

The Next.js application and BunMail may run as separate services because they have different runtime and deployment requirements.

📦 Getting Started

Prerequisites

* Bun
* Git
* A code editor such as Cursor
* A Neon account when database setup begins

1. Clone the repository

git clone YOUR_SUPERMAIL_REPOSITORY_URL
cd supermail

Replace YOUR_SUPERMAIL_REPOSITORY_URL with the actual repository URL.

2. Install dependencies

bun install

3. Configure environment variables

Create a .env.local file in the project root. Use .env.example as the template.

Do not commit real credentials or API keys.

4. Start the development server

bun run dev

Open http://localhost:3000 in your browser.

Database, authentication, and email-sending configuration will be required as their respective features are implemented.

⚙️ Environment Variables

The following variables are planned for the application. Some will become required only when their associated features are implemented.

Variable	Purpose
BETTER_AUTH_URL	Base URL of the Supermail application
BETTER_AUTH_SECRET	Secret used by Better Auth
DATABASE_URL	Neon PostgreSQL connection string
GOOGLE_CLIENT_ID	Google OAuth client ID, if enabled
GOOGLE_CLIENT_SECRET	Google OAuth client secret, if enabled
BUNMAIL_BASE_URL	Base URL of the BunMail service
BUNMAIL_API_KEY	Credential for the BunMail service

Use placeholders in .env.example and real values in local or production secret settings. Never publish production credentials.

📚 Documentation

The Supermail documentation website is planned to include:

* Introduction and quick start
* Account registration and email verification
* API key management
* Sending emails
* Templates
* Sender domains
* Email history and events
* Usage limits
* API reference
* Error handling and troubleshooting
* Self-hosting and deployment guides, if supported

Website and API links will be added here once they are published.

🔐 Security

Supermail is being designed with these security practices:

* Store API key hashes instead of reusable plaintext keys.
* Keep service credentials on the server.
* Authenticate and authorize protected requests.
* Isolate customer data.
* Validate API inputs.
* Enforce rate limits and usage quotas.
* Restrict sending to authorized sender identities.
* Avoid unnecessary retention of email content.
* Never log secrets or sensitive message content unnecessarily.

🚧 Project Status

Supermail is under active development.

The technology stack and feature list describe the intended implementation. They do not mean every feature is currently available.

The initial development milestones are:

1. Project foundation.
2. BunMail compatibility and delivery testing.
3. Neon and Drizzle integration.
4. Better Auth and email verification.
5. Dashboard and REST API.
6. Email sending and templates.
7. Security, testing, and deployment.
8. Private beta and launch.

🤝 Contributing

Contribution guidelines will be published when the repository’s development workflow is established.

Once contributions are enabled, please use GitHub Issues for bugs and feature suggestions and submit pull requests with focused changes.

📄 License

The Supermail project’s license will be specified here before public release.

Supermail’s license is separate from the licenses of its third-party dependencies and integrations.Copyright © 2026 ScribbleDoodle.
All rights reserved. This repository is public for deployment purposes only.
The source code may not be copied, modified, or redistributed.

ScribbleDoodle is a browser-based writing and document layout tool designed to make creating and formatting text simple and flexible. It lets users write, organize, and customize pages with adjustable line spacing, fonts, paper sizes, and visual layout controls, while also supporting features like project tabs, custom backgrounds, template uploads, and exporting documents to formats such as PDF or DOCX. The goal of ScribbleDoodle is to give writers, students, and creators an easy way to design and structure their documents while keeping the experience lightweight and creative, with future plans for AI tools that help improve writing, format documents automatically, and assist with editing.
