# Mynd Domains — Subdomain Registry

> The official application registry for Mynd Domains subdomains.

Every Mynd Domains subdomain (`yourname.mynd.my.id`) is requested through a
Pull Request in this repository. There is no web form bypass, no email
shortcut, and no exceptions — **a merged PR is the only way to receive a
subdomain**.

---

## Table of contents

- [How it works](#how-it-works)
- [Before you apply](#before-you-apply)
- [Application fields](#application-fields)
- [How to apply](#how-to-apply)
- [Review process](#review-process)
- [After approval](#after-approval)
- [Subdomain rules](#subdomain-rules)
- [Grounds for rejection](#grounds-for-rejection)
- [Grounds for revocation](#grounds-for-revocation)
- [Need help?](#need-help)

---

## How it works

```
1. Join the Mynd Labs Discord     (mandatory)
2. Read the rules                  (CONTRIBUTING.md)
3. Fill out the application form   (on mynd.my.id/claim)
4. A PR is auto-created here       (you get the link)
5. Maintainers review your PR
6. PR is merged → subdomain is yours
7. PR is closed → subdomain is denied
```

The web form at [mynd.my.id/claim](https://mynd.my.id/claim) handles steps
3–4 automatically: it validates your input, posts a notification to our
Discord, creates a branch with your application file, and opens a PR in
this repository. You receive the PR link immediately.

You can also submit a PR manually if you prefer — see
[Manual application](#manual-application) below.

## Before you apply

You **must** meet all of the following before submitting an application:

| Requirement | Why |
|---|---|
| **Join the Mynd Labs Discord** | All applicants must be members of our Discord server. This is where we contact you, share updates, and provide support. Invite: `discord.gg/jpJ9n2y5mD` |
| **Have a GitHub account** | Your application is a PR on GitHub. You need an account to receive the PR. |
| **Have a real project** | We do not issue subdomains for squatters, placeholder projects, or domain hoarding. |
| **Read and accept the rules** | See [CONTRIBUTING.md](./CONTRIBUTING.md) for the full rules, guidelines, and taboos. |

## Application fields

Your application is stored as a JSON file at
`applications/{your-github-username}.json`.

| Field | Required | Description |
|---|---|---|
| `subdomain` | ✅ | The subdomain you want (e.g., `myproject`). Must be 1–63 chars, lowercase alphanumeric + hyphens (RFC 1035). |
| `name` | ✅ | Your full name (first and last). |
| `email` | ✅ | A valid email where we can reach you. |
| `github` | ✅ | Your GitHub username (without `@`). Must match the PR author. |
| `discord` | ✅ | Your Discord username (with discriminator, e.g., `username` or `username#1234`). Must match a member of our server. |
| `project` | ✅ | The name of your project. |
| `description` | ✅ | A clear description of what you are building. 50–2000 characters. |
| `purpose` | ✅ | Why you need a Mynd Domains subdomain specifically. 20–1000 characters. |
| `url` | ❌ | If your project is already live somewhere, link it. |
| `categories` | ❌ | Tags describing your project (e.g., `["portfolio", "blog", "api"]`). Max 5. |
| `acceptedRules` | ✅ | Must be `true`. Indicates you have read and accepted the rules. |
| `joinedDiscord` | ✅ | Must be `true`. Indicates you have joined the Discord server. |

## How to apply

### Via the web form (recommended)

1. Go to [mynd.my.id/claim](https://mynd.my.id/claim)
2. Click **"Claim your domain"**
3. Fill out all fields
4. Check both boxes (rules acceptance + Discord join)
5. Submit
6. You will receive your PR link immediately
7. Watch the PR for maintainer feedback

### Manual application

1. Fork this repository
2. Copy `template.json` to `applications/{your-github-username}.json`
3. Fill in all required fields
4. Commit to a branch named `add-{your-subdomain}`
5. Open a PR against `main`
6. Use the PR title: `register: {your-subdomain}.mynd.my.id`
7. Use the PR body template (shown when you open the PR)

## Review process

| Step | Action | Timeline |
|---|---|---|
| 1 | **Automated checks** — bot validates your JSON against the schema | Instant |
| 2 | **Initial review** — a maintainer checks for completeness and rule compliance | 24–48 hours |
| 3 | **Discussion** — maintainers may ask questions or request changes | Varies |
| 4 | **Decision** — PR is merged (approved) or closed (denied) | 3–7 days |

You will be notified via GitHub when your PR status changes. If we need
more information, we may also contact you via Discord.

## After approval

Once your PR is merged:

1. Your subdomain DNS record is provisioned within 24 hours.
2. You will receive a confirmation message on Discord.
3. You can configure your subdomain to point to:
   - A static host (A/AAAA records)
   - A platform (CNAME to Vercel, Netlify, GitHub Pages, etc.)
   - A redirect (URL record)
4. DNS changes can be requested by opening a new PR in this repository.

## Subdomain rules

- Subdomain must be **1–63 characters** (RFC 1035 label length).
- Only **lowercase letters, numbers, and hyphens** are allowed.
- Cannot **start or end with a hyphen**.
- Cannot be a **reserved name** (see [RESERVED.md](./RESERVED.md)).
- One subdomain per person unless you have explicit maintainer approval.
- Subdomain must be **actively used within 90 days** of approval, or it
  may be revoked.

## Grounds for rejection

Your application will be rejected if:

- You have not joined the Discord server.
- Your GitHub username doesn't match the PR author.
- Your project description is vague, copied, or AI-generated filler.
- You're requesting a subdomain you don't intend to use (squatters).
- You're requesting a trademarked or well-known brand name you don't own.
- Your project promotes illegal content, hate speech, or harm.
- You've been previously banned from the Mynd Labs community.
- You provide false information in your application.

## Grounds for revocation

An approved subdomain may be revoked if:

- The subdomain is not actively used within 90 days.
- The content hosted violates our [Community Guidelines](./CONTRIBUTING.md).
- The owner is banned from the Mynd Labs community.
- The owner requests revocation voluntarily.
- The subdomain is found to be used for phishing, malware, or abuse.
- The owner provided false information during the application process.

## Manual application

<details>
<summary>Click to expand manual PR instructions</summary>

1. **Fork** this repository.
2. **Clone** your fork locally:
   ```bash
   git clone https://github.com/YOUR_USERNAME/register.git
   cd register
   ```
3. **Create a branch**:
   ```bash
   git checkout -b add-your-subdomain
   ```
4. **Copy the template**:
   ```bash
   cp template.json applications/your-github-username.json
   ```
5. **Edit** `applications/your-github-username.json` and fill in all fields.
6. **Commit**:
   ```bash
   git add applications/your-github-username.json
   git commit -m "register: your-subdomain.mynd.my.id"
   ```
7. **Push and open a PR** against `main`.

</details>

## Need help?

- **Discord:** `discord.gg/jpJ9n2y5mD` (fastest)
- **GitHub Issues:** Open an issue in this repository
- **Email:** hello@myndlabs.tech

---

Maintained by [Mynd Labs](https://myndlabs.tech).
