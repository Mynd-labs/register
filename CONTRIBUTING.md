# Contributing to Mynd Domains — Rules, Guidelines, and Taboos

This document defines the rules, guidelines, strict policies, and taboos
for the Mynd Domains community. By submitting an application, you
acknowledge that you have read, understood, and agreed to every section
below.

---

## Table of contents

- [1. Community rules](#1-community-rules)
- [2. Application guidelines](#2-application-guidelines)
- [3. Strict rules (zero tolerance)](#3-strict-rules-zero-tolerance)
- [4. Taboos (will get you banned)](#4-taboos-will-get-you-banned)
- [5. Content policy](#5-content-policy)
- [6. Technical requirements](#6-technical-requirements)
- [7. Code of conduct](#7-code-of-conduct)
- [8. Enforcement](#8-enforcement)

---

## 1. Community rules

These are the baseline expectations for every member of the Mynd Domains
community.

### 1.1 Be honest

- Use your real name in applications.
- Describe your project accurately.
- Do not impersonate another person or organization.
- Do not create multiple accounts to request multiple subdomains.

### 1.2 Be respectful

- Treat maintainers, reviewers, and other applicants with respect.
- Do not spam, harass, or derail discussions in PRs or Discord.
- Accept maintainer decisions gracefully. You may appeal once via Discord.

### 1.3 Be patient

- Reviews take 24–48 hours for initial response, 3–7 days for a decision.
- Do not ping maintainers before 48 hours have passed.
- Do not open multiple PRs for the same subdomain.

### 1.4 Be a participant

- Join the Discord server and participate in the community.
- Help other builders when you can.
- Share what you're building — we love seeing projects come to life.

---

## 2. Application guidelines

### 2.1 Eligibility

You are eligible to apply if:

- You are a real person (no bots, no organizations).
- You have a GitHub account.
- You have joined the Mynd Labs Discord server.
- You have a genuine project to host.

### 2.2 Subdomain choice

- Choose a subdomain that reflects you or your project.
- Avoid requesting names that impersonate brands, celebrities, or
  organizations you don't represent.
- Avoid requesting admin-looking names (`admin`, `root`, `www`, `mail`,
  `api`, `status`, etc.) — these are reserved.
- One subdomain per person. If you need a second, open a PR explaining
  why, and a maintainer will review.

### 2.3 Project description

- Write a **genuine, specific** description of your project.
- Minimum 50 characters. Maximum 2,000 characters.
- Do **not** copy-paste generic text or use AI-generated filler.
- Explain what the project does, who it's for, and what stage it's at.

**Good example:**
> A web-based task manager for students that syncs with Google Calendar. Built with Next.js and Supabase. Currently in beta with 30 users.

**Bad example:**
> A website. Please give me a domain. Thank you.

### 2.4 Purpose statement

- Explain **why** you need a Mynd Domains subdomain specifically.
- Reference what you'll use it for (portfolio, project hosting, API, etc.).
- Do not write "because I want a free domain."

---

## 3. Strict rules (zero tolerance)

Violation of any of these rules will result in **immediate rejection** of
your application and may result in a **permanent ban** from the Mynd
Domains community.

### 3.1 No false information

- Providing a fake name, fake email, or someone else's Discord/GitHub
  username is an immediate, non-negotiable rejection.
- If we discover false information after approval, the subdomain is
  revoked without notice.

### 3.2 No squatting

- Requesting a subdomain you do not intend to use is prohibited.
- "Intend to use" means the subdomain must resolve to active content
  within 90 days of approval.

### 3.3 No trademark abuse

- You may not request a subdomain that contains a trademarked name,
  brand, or organization you do not own or represent.
- This includes, but is not limited to: company names, product names,
  celebrity names, and government agency names.

### 3.4 No circumvention

- Do not attempt to bypass the review process.
- Do not open multiple PRs for the same subdomain.
- Do not contact maintainers privately to expedite your review.
- Do not edit another applicant's application file.

### 3.5 No multi-accounting

- One person gets one subdomain. Creating multiple GitHub or Discord
  accounts to request multiple subdomains is prohibited and will result
  in all associated subdomains being revoked.

---

## 4. Taboos (will get you banned)

These are the absolute hard limits. Crossing any of these will result in
an **immediate, permanent ban** from the Mynd Domains community and
**revocation of all associated subdomains**. There is no appeal.

### 4.1 No illegal content

You may not host, link to, or facilitate access to:

- Child sexual abuse material (CSAM) — reported to authorities.
- Content that sexualizes minors in any form.
- Terrorist content or content promoting terrorism.
- Content that facilitates human trafficking.
- Content that promotes or facilitates self-harm or suicide.
- Pirated software, media, or copyrighted material distributed without
  authorization.

### 4.2 No malware or abuse

You may not use a Mynd Domains subdomain to:

- Host malware, ransomware, or spyware.
- Distribute phishing pages or credential harvesting tools.
- Launch DDoS attacks or botnets.
- Scan for vulnerabilities on systems you don't own.
- Send spam or operate a command-and-control server.

### 4.3 No hate speech or harassment

You may not host content that:

- Promotes hatred, discrimination, or violence against any group based on
  race, ethnicity, religion, gender, sexual orientation, disability, or
  nationality.
- Doxes, harasses, or threatens any individual.
- Promotes or glorifies sexual violence.
- Contains non-consensual intimate imagery.

### 4.4 No fraud or deception

You may not use a Mynd Domains subdomain to:

- Impersonate another person, brand, or organization.
- Run pyramid schemes, Ponzi schemes, or other financial fraud.
- Sell counterfeit goods.
- Facilitate gambling operations targeting minors.
- Run pump-and-dump or market manipulation schemes.

### 4.5 No weaponization

You may not use a Mynd Domains subdomain to:

- Sell or distribute firearms, weapons, or explosives illegally.
- Provide instructions for manufacturing weapons or explosives.
- Facilitate drug trafficking or distribution.

---

## 5. Content policy

### 5.1 What's allowed

- Personal portfolios and blogs.
- Open-source project documentation and demos.
- Student projects and learning exercises.
- Small business landing pages.
- Web tools, APIs, and applications.
- Creative work (art, writing, music).

### 5.2 What's not allowed (in addition to Section 4)

- Adult content (pornography) — Mynd Domains is a community for builders,
  not an adult hosting service.
- Gambling sites (unless explicitly approved and age-gated).
- Sites that scrape or mirror other sites without permission.
- Sites that primarily serve ads with no original content.
- Sites that exist solely to redirect to another URL.

### 5.3 NSFW content

- No NSFW content, period. This includes artistic nudity.
- If your project is borderline, ask a maintainer in Discord before
  applying.

---

## 6. Technical requirements

### 6.1 DNS configuration

After approval, you can configure your subdomain via PR:

| Record type | Use case |
|---|---|
| `A` | Point to an IPv4 address |
| `AAAA` | Point to an IPv6 address |
| `CNAME` | Point to another domain (Vercel, Netlify, GitHub Pages, etc.) |
| `URL` | Redirect to another URL |

### 6.2 SSL/TLS

- SSL is provided automatically via Cloudflare's edge.
- You do not need to configure certificates yourself.
- If you need a custom certificate, contact maintainers on Discord.

### 6.3 Uptime

- Your subdomain must resolve to active content within 90 days.
- Subdomains that return errors or timeouts for 30+ consecutive days may
  be flagged for revocation.
- If you need temporary downtime (maintenance, migration), notify
  maintainers on Discord.

---

## 7. Code of conduct

We follow the [Contributor Covenant 2.1](https://www.contributor-covenant.org/version/2/1/code_of_conduct/)
in addition to the rules above. In summary:

- Be kind and constructive.
- Respect differences of opinion.
- Give and accept feedback gracefully.
- Focus on what's best for the community.

Violations of the code of conduct should be reported to
`hello@myndlabs.tech` or to any maintainer privately on Discord.

---

## 8. Enforcement

### 8.1 Enforcement levels

| Level | Action | Trigger |
|---|---|---|
| 1 | **Warning** | Minor first-time violation (e.g., vague description) |
| 2 | **PR rejection** | Rule violation that can be fixed (e.g., reserved subdomain) |
| 3 | **PR closure** | Unfixable rule violation (e.g., squatting, trademark abuse) |
| 4 | **Subdomain revocation** | Post-approval violation (e.g., hosting prohibited content) |
| 5 | **Community ban** | Taboo violation (Section 4) or repeated Level 3–4 violations |

### 8.2 Appeals

- You may appeal a Level 2–4 decision **once** via Discord.
- Appeals must be made within 7 days of the decision.
- Level 5 bans are **not appealable**.

### 8.3 Reporting violations

If you discover a Mynd Domains subdomain being used in violation of these
rules:

1. Do **not** confront the owner directly.
2. Email `abuse@myndlabs.tech` with the subdomain and evidence.
3. Or DM a maintainer on Discord.

Reports are confidential. Retaliation against reporters is itself a
Level 5 violation.

---

By submitting an application, you confirm that:

- You have read this document in full.
- You understand and agree to all rules, guidelines, and consequences.
- You have joined the Mynd Labs Discord server.
- All information in your application is truthful.

---

Maintained by [Mynd Labs](https://myndlabs.tech).
