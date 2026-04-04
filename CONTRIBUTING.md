# 🤝 Contributing to .edu Email Benefits Hub

Thank you for helping keep this guide current and comprehensive! This document explains how to contribute.

---

## 📋 Table of Contents

- [Before You Start](#-before-you-start)
- [Adding a New Benefit](#-adding-a-new-benefit)
- [Adding a New Category](#-adding-a-new-category)
- [Reporting Issues](#-reporting-issues)
- [Updating Existing Benefits](#-updating-existing-benefits)
- [Pull Request Process](#-pull-request-process)
- [Code of Conduct](#-code-of-conduct)

---

## ✅ Before You Start

### Have you tested the benefit?

**This is mandatory.** Before submitting:

1. **Sign up with a `.edu` email address** (yours or a test account)
2. **Complete the verification process** end-to-end
3. **Confirm the benefit works** as described
4. **Note the verification time** — instant, 24 hours, etc.
5. **Take a screenshot** (optional but helpful) for verification disputes

### Is the benefit already listed?

Search the README for the service name. If it exists, check if it needs updating rather than adding duplicates.

### Does the benefit belong to student deals, or is it something else?

This repository focuses on **benefits verified using a `.edu` email address**. 

**In scope:**
- Tools offering free/discounted access to `.edu` email holders
- Services with automatic `.edu` verification
- Benefits unlocked via GitHub Education Pack (uses `.edu` verification)

**Out of scope:**
- Discounts requiring SheerID or student ID photo uploads (unless `.edu` is also accepted)
- Hardware retailer discounts (Apple, Dell, etc.) — these are in the main Student Deals Hub
- Non-verified student discounts or rumours
- Expired benefits

---

## 🆕 Adding a New Benefit

### Step 1: Find the right category

Benefits are organized into 10 categories. Match your benefit to one:

| Category | Includes | Example Services |
|---|---|---|
| **Software & Development** | IDEs, code tools, databases, hosting, version control | JetBrains, GitHub, MongoDB |
| **Design & Creative Tools** | Design software, CAD, 3D modelling, vector graphics | Figma, Adobe, Autodesk |
| **Cloud Services & Credits** | Cloud platforms, compute credits, infrastructure | AWS, Azure, Google Cloud |
| **Learning Platforms** | Courses, interactive coding, certifications | DataCamp, Coursera, LinkedIn Learning |
| **Productivity & Office Suites** | Office tools, note-taking, collaboration | Microsoft Office, Notion, Miro |
| **AI & Research Tools** | AI assistants, ML platforms, research databases | Perplexity, Notion AI, Vertex AI |
| **Professional Services** | Career tools, networking, premium subscriptions | LinkedIn Premium, Amazon Prime Student |
| **Communication Tools** | Messaging, video conferencing, chat platforms | Slack, Zoom, Discord |
| **Hardware & Devices** | Discounts on computers, phones, peripherals | Apple, Microsoft, Dell |
| **Entertainment & Streaming** | Music, video, entertainment subscriptions | Spotify, YouTube Premium, Apple Music |

**If none fit:** Propose a new category in your PR description. Maintainers will review.

### Step 2: Gather the information

You'll need:

| Field | Example | Notes |
|---|---|---|
| **Service Name** | JetBrains All IDEs | Official brand name |
| **Direct Student Link** | https://www.jetbrains.com/community/education/ | Link to signup page, NOT homepage |
| **Benefit Type** | 🟢 **FREE 1 year** | Use emoji: 🟢 FREE, 🟡 DISCOUNT, 🟣 CREDITS |
| **Description** | Every professional IDE in one licence — IntelliJ, PyCharm, WebStorm... | 1–2 sentences explaining student value |
| **Verification Method** | `.edu` email auto-verify | How students claim it |
| **Currently Active** | ✅ Yes | Verify it's working NOW |

### Step 3: Add to the README

Open `README.md` and find your category's table.

**Markdown table format:**
```markdown
| [Service Name](direct-link) | 🟢 **FREE** | Description of what the student gets | `.edu` email auto-verify | [→ Claim](link) |
```

**Example:**
```markdown
| [Figma Professional](https://www.figma.com/education/) | 🟢 **FREE** | Collaborative UI/UX design and prototyping — the industry-standard tool at top tech companies | `.edu` email auto-verify | [→ Claim](https://www.figma.com/education/) |
```

**Formatting rules:**
- Use `[Service Name](link)` for the service title (clickable)
- Emoji codes: `🟢` (green = free), `🟡` (yellow = discount), `🟣` (purple = credits)
- Keep descriptions **under 120 characters** — one to two sentences max
- Use **bold** only for the benefit type (e.g., `**FREE**`, `**50% OFF**`)
- Always include the `[→ Claim](link)` button at the end

### Step 4: Update the main header count

The very first line says `50+ free tools`. If you're adding to the list, increment this count in the header. No need if you're updating existing entries.

### Step 5: Submit a PR

See [Pull Request Process](#-pull-request-process) below.

---

## 🆕 Adding a New Category

**When to propose a new category:**
- You have 3+ related benefits that don't fit existing categories
- The category is broad enough for future contributions
- Example: "Open Source Tools" (for free, open-source utilities specific to students)

**How to propose:**

1. **Open an Issue first** (don't submit a PR yet)
   - Title: `[Proposal] New Category: [Category Name]`
   - Describe why it's needed
   - List the 3+ benefits that would fit

2. **Maintainers will review** and either approve or suggest modifications

3. **Once approved:** Create a section following this format:

```markdown
### 🎯 Category Name

| Service | Benefit | Verification | Link |
|---|---|---|---|
| [Service 1](link) | 🟢 **Type** | Description | Method | [→ Claim](link) |
| [Service 2](link) | 🟡 **Type** | Description | Method | [→ Claim](link) |
```

4. **Add to Table of Contents** (near the top):
```markdown
  - [Category Name](#-category-name)
```

---

## 🐛 Reporting Issues

Found a benefit that **no longer works** or **has incorrect information**?

### Option 1: Issue (for discussion)
Open a GitHub Issue with:
- **Title:** `[Issue] ServiceName: benefit expired / incorrect info`
- **Description:** What's wrong and when you tested it
- **Example:** "JetBrains free license is now only 1 year, not lifetime"

### Option 2: PR (for quick fixes)
If you know the fix:
1. Edit the README directly
2. Title your PR: `fix: ServiceName verification method / benefit changed`
3. Describe the change in the PR description

---

## ✏️ Updating Existing Benefits

**Common updates:**
- Verification method changed (e.g., from SheerID to `.edu` auto-verify)
- Benefit tier changed (e.g., free → discounted)
- Expiration date changed (e.g., 1 year → 2 years)
- Benefit removed or service discontinued

### How to update:

1. **Locate the benefit** in the README
2. **Edit the row** with new information
3. **Note the change in your PR description**

**Example PR:**
```markdown
Fix: Updated Spotify Premium Student verification

- Changed from SheerID to `.edu` email auto-verify
- Benefit remains 50% OFF (~$5.99/month)
- Verified working on 2025-04-01
```

---

## 🔄 Pull Request Process

### 1. Fork and clone

```bash
git clone https://github.com/yourusername/edu-email-benefits.git
cd edu-email-benefits
```

### 2. Create a feature branch

Use a descriptive branch name:

```bash
# For adding a benefit
git checkout -b add/figma-benefit

# For fixing an issue
git checkout -b fix/jetbrains-expired

# For updating a category
git checkout -b update/cloud-services

# For new categories
git checkout -b feature/new-category-gaming
```

### 3. Make your changes

Edit `README.md` with your new benefit(s).

**Before committing, verify:**
- [ ] Benefit is verified (tested with `.edu` email)
- [ ] Link is correct and goes to student signup page
- [ ] Description is concise and clear
- [ ] Formatting matches existing entries
- [ ] Emoji is appropriate (`🟢` / `🟡` / 🟣)
- [ ] Main header count is updated if adding new benefits

### 4. Commit with a clear message

```bash
# Good commit messages:
git commit -m "add: Figma Professional with .edu auto-verify"
git commit -m "fix: Update JetBrains verification method to .edu email"
git commit -m "update: Adobe CC discount now 65% off"

# Avoid:
# ❌ "update"
# ❌ "fixed stuff"
# ❌ "changes"
```

### 5. Push and open a PR

```bash
git push origin add/figma-benefit
```

Then open a PR on GitHub with:

**Title:** Clear, one-line description
```
Add: Figma Professional .edu email benefit
```

**Description:** More details
```markdown
- Verified benefit is currently active (tested April 1, 2025)
- Figma Professional is FREE for `.edu` email holders
- Verification is instant
- Added to "Design & Creative Tools" section
```

### 6. Respond to feedback

Maintainers may request:
- More details on verification
- Formatting changes
- Evidence (screenshot, link verification)
- Tests with your `.edu` email

Please respond within 7 days. Stale PRs may be closed.

---

## 📋 Checklist Before Submitting

- [ ] I have tested this benefit myself with a `.edu` email
- [ ] The benefit is currently active (not expired)
- [ ] The link goes directly to the student signup page
- [ ] The description is 1–2 sentences, under 120 characters
- [ ] The verification method is accurate
- [ ] The emoji matches the benefit type (🟢 FREE, 🟡 DISCOUNT, 🟣 CREDITS)
- [ ] The formatting matches other entries in the section
- [ ] The main header count is updated if needed
- [ ] I've searched for duplicates (not already in the list)
- [ ] My commit message is clear and descriptive

---

## 🎯 What Makes a Good Contribution

✅ **Good contributions:**
- Service is widely used by students (not obscure)
- Benefit is substantial (e.g., free, 50%+ discount, significant credits)
- Verification is documented and works
- Belongs in one of the 10 categories (or proposes a valid new one)
- Evidence provided (screenshot, tested link)

❌ **Contributions we'll likely reject:**
- Rumoured benefits ("I heard GitHub gives...") without verification
- Expired or no-longer-active benefits
- Duplicate entries
- Benefits not aligned with `.edu` email verification
- Low-value discounts (e.g., 5% off)
- Spam or promotional links
- Services unrelated to student workflow

---

## 🚀 Speeding Up Your PR

**To get merged faster:**

1. **Test thoroughly** — save a screenshot of successful `.edu` verification
2. **Propose one benefit per PR** — avoid bundling unrelated changes
3. **Check for duplicates** — search the README before proposing
4. **Use the exact template** — match formatting to existing entries
5. **Link to the student signup page** — not the homepage or pricing page

---

## ❓ FAQ

### Q: Can I add a benefit I heard about but haven't tested?
**A:** No. Please test it yourself first with a `.edu` email. We only list verified, currently-active benefits.

### Q: How long until my PR is reviewed?
**A:** Usually 3–7 days. Maintainers are volunteers. If it's been longer, feel free to comment with a gentle ping.

### Q: Can I update multiple benefits in one PR?
**A:** If they're related (e.g., all Cloud Services updates), yes. Otherwise, keep PRs focused on one change.

### Q: What if a service is region-locked (e.g., US only)?
**A:** Add a note like: `(US colleges only)` or `(UK/EU verified)` in the description or verification column.

### Q: How do I know if a `.edu` email works in my country?
**A:** The service will tell you during signup. If it's rejected, the benefit likely isn't available in your region.

### Q: Can I request a benefit be added if I can't test it?
**A:** Open an issue instead. Title it `[Request] ServiceName student benefit`. Maintainers may investigate or ask for more details.

---

## 📫 Code of Conduct

By contributing, you agree to:

- **Be respectful** — treat other contributors with kindness
- **Be honest** — only propose benefits you've verified
- **Be helpful** — improve others' contributions with constructive feedback
- **Be inclusive** — consider students worldwide (region-locked benefits are fine, just note them)
- **No spam** — no promotional links, self-promotion, or commercial advertising

**Zero tolerance:** Harassment, discrimination, or bad faith contributions will result in a permanent ban.

---

## 🎓 Contributors

Thanks to these amazing students and developers for keeping this guide current:

- [Aashish Poudel](https://github.com/Aashish-po) — Founder, maintainer
- You? Submit your first PR! 🎉

---

## 📞 Questions or suggestions?

- **Open an issue** for bugs or feature requests
- **Start a discussion** for general questions
- **Email the maintainers** for sensitive topics

---

<p align="center">
  Every contribution helps thousands of students unlock free tools &nbsp;·&nbsp;
  Thank you! 🎓
</p>
