<div align="center">

<img src="./icon.png" width="160" alt="@tag app icon — blue lettering on white" />

# @tag for Apple Mail

### Mention people. Reuse replies. Make email easier.

Email mentions, reply templates, and HTML email previews — alongside Apple Mail.

![macOS](https://img.shields.io/badge/macOS-14%2B-111827?style=flat-square&logo=apple&logoColor=white)
![Architecture](https://img.shields.io/badge/Apple_Silicon-supported-007AFF?style=flat-square)
![Languages](https://img.shields.io/badge/languages-EN_%2F_RU-007AFF?style=flat-square)
![Status](https://img.shields.io/badge/status-early_release-F59E0B?style=flat-square)

[Features](#features) · [Installation](#installation) · [Getting started](#getting-started) · [Privacy](#privacy)

</div>

---

## A little less typing. A little more flow.

Keep your reusable replies, HTML content, and recipient mentions close to the message you're writing. One **tag** button in Mail opens your templates and HTML tools.

No email archive indexing. No automatic sending. No separate menu bar item.

## Features

| | What you can do |
| :--- | :--- |
| **@mentions in emails** | Search the current message’s **To** and **Cc** recipients by name, email, or login. Insert `@Name` or `@username` with a clickable email link. |
| **Reusable replies** | Create, edit, search, preview, and insert your own email templates. |
| **HTML emails** | Import an HTML file or paste source code, preview the result, and insert formatted content. |
| **Mail integration** | Open templates and HTML from one **tag** toolbar button. Access template commands through macOS Services. |
| **Your language** | English and Russian interfaces follow your Mac’s language settings. Your template content stays as you wrote it. |

## Installation

**Requires macOS 14 or later, an Apple Silicon Mac, and Apple Mail.**

1. Download the application ZIP from this repository’s **Releases** tab.
2. Extract it and move **@tag.app** to your **Applications** folder.
3. Open @tag for initial setup.
4. Enable **@tag** in **Mail → Settings → Extensions**.
5. Allow the installed copy in **System Settings → Privacy & Security → Accessibility** for inline suggestions and direct insertion.
6. Restart Mail, then open a new draft.

> **Current build:** ad-hoc signed and not notarized. macOS may block its first launch. Do not disable system security to run it. Intel binaries are not provided.

When upgrading from experimental versions, remove older app copies and obsolete toolbar entries. The current extension and Accessibility entry should both be named **@tag**. You may need to renew Accessibility permission after an update. Keep your local template library when updating.

## Getting started

### Mention someone already in the conversation

Add and confirm a recipient in **To** or **Cc**, then type `@` in the message body. Continue with their name or email login and select a suggestion.

```text
@name  →  @Name Surname
           ↳ mailto link to the recipient’s address
```

Mentioning someone does not add recipients or send the message. Suggestions are limited to the current message’s To and Cc fields; Bcc and your email archive are excluded.

### Turn a good reply into a reusable template

Click **tag** in Mail’s toolbar. Create a template, edit it, preview it, and insert it into your draft.

Use variables when you need them:

| Variable | Content |
| :--- | :--- |
| `{{name}}` | The name entered in the template’s name field |
| `{{date}}` | The current date |
| `{{signature}}` | Your saved signature text |

Russian equivalents `{{имя}}`, `{{дата}}`, and `{{подпись}}` are also supported.

### Bring your HTML into Mail

Open **tag → Insert HTML**, import a file or paste HTML source, preview it, and insert it into your message.

Choose **Mail → Format → Make Rich Text** for formatted content. HTML rendering may differ between email clients. Remote images are hidden in the preview; inserted HTML may retain HTTPS image links.

### Shortcuts

| Action | Shortcut |
| :--- | :--- |
| Open templates | **⌃ ⌥ T** |
| Open HTML tools | **⌃ ⌥ H** |

Right-click template commands may appear under **Services**, depending on your macOS and Mail settings.

## Privacy

**Your templates and settings stay on your Mac.**

- No analytics or automatic email-data uploads to the developer.
- No email archive scanning or indexing.
- No automatic email sending.
- Recipient suggestions use the current message’s To and Cc fields.
- MailKit supplies compose-session information, including the subject and recipients.
- Direct insertion uses Accessibility access and the system clipboard.
- Technical diagnostics stay local unless you choose to share them.

External images in inserted HTML may be loaded by Mail or the recipient’s email client. Their behavior is controlled by those apps and email services.

## Release notes & known limitations

@tag is currently an **early release distributed outside the Mac App Store**.

- Accessibility permission may need to be renewed after an update.
- Suggestions may be unavailable when multiple drafts have identical subjects.
- The final font-size preservation correction still needs further live validation in Mail.
- Automatic `+@` insertion and archive indexing are disabled.

## Feedback

Found a bug or have an idea? Open an **Issue** in this repository.

Include your macOS version, @tag build number, and steps to reproduce the problem. Use test recipients and remove private addresses, email content, and secrets from screenshots or logs.

---

<div align="center">

**Created by dvs01006**

An independent project. Not affiliated with or endorsed by Apple Inc.

</div>
