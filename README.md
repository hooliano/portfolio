# Portfolio Template

A one-page portfolio you can personalize in about 20 minutes. Plain HTML and CSS: no installs, no build step, no frameworks.

```
portfolio-template/
├── index.html    your content: text, links, projects
├── style.css     your design: colors, fonts, layout
├── script.js     small dynamic touches (see section 2 below)
├── images/       your photo and project screenshots
└── README.md     this file
```

## 1. Get it running

1. **Get the files.** Clone this repo, or click **Code → Download ZIP** on GitHub and unzip it.
2. **Open the folder in VS Code** with **File → Open Folder**. Pick the whole `portfolio-template` folder, not just one file.
3. **Install the Live Server extension** (search "Live Server" in the Extensions tab).
4. **Right-click `index.html` → Open with Live Server.** The page opens in your browser and reloads every time you save.

## 2. Make it yours

Press **Ctrl+Shift+F** (**Cmd+Shift+F** on Mac) and search for `EDIT`. Every spot you need to change has a comment starting with `EDIT`. Anything in `[square brackets]` is a blank to fill in.

- [ ] **Name.** It appears in the page title, header logo, headline, photo description, and footer.
- [ ] **Intro sentence** in the hero.
- [ ] **Photo.** Save yours in `images/` (for example `images/me.jpg`), then update the `src` and `alt` in `index.html`. A portrait crop under 500 KB works best.
- [ ] **About paragraphs and skills.** Only list skills you can talk about in an interview.
- [ ] **Projects.** Replace the three samples with your real work: screenshot, title, description, tools, and links. Delete any sample you don't have a real project for. Two strong projects beat three weak ones.
- [ ] **Contact.** Email, GitHub, and LinkedIn.
- [ ] **Check it on a phone-sized screen.** In Chrome, press F12, then click the device icon at the top of the panel.

**Writing a project description:** say what it does, what you used, and one concrete result. "Shows a five-day forecast for any city, built with JavaScript and a public weather API" beats "A cool weather app."

## 3. What script.js does

You don't need to edit this file, but it's worth reading — it's short and commented top to bottom. It adds three things HTML and CSS can't do on their own:

- **Footer year.** Sets `&copy; <span id="year">` to the current year automatically.
- **Active nav link.** Adds an `active` class to whichever header link matches the section you're currently reading, using an `IntersectionObserver`.
- **Copy email button.** Click the **Copy** button next to your email to put it on the clipboard, with a "Copied!" confirmation. It falls back to selecting the text if clipboard access is blocked (which is normal when opening the page directly as a file, before it's deployed).

## 4. Change the look

Everything visual starts in **section 1 (THEME)** at the top of `style.css`. Change a color there and it updates across the page. Three ready-made color presets are in the comment right below it. Copy one over the colors above it.

To change fonts, pick a pair on [Google Fonts](https://fonts.google.com), replace the `<link>` near the top of `index.html`, and update `--font-heading` and `--font-body` in `style.css`.

## 5. Put it online

**Netlify (fastest).**
1. Go to [app.netlify.com/drop](https://app.netlify.com/drop) and sign in.
2. Drag your whole `portfolio-template` folder onto the page.
3. You get a live link in seconds. Rename it under **Site configuration → Change site name**.

**GitHub Pages.**
1. Push the project to a GitHub repo.
2. Go to **Settings → Pages**.
3. Under **Source**, choose **Deploy from a branch**, then pick `main` and `/ (root)`, and click **Save**.
4. After about a minute, your site is at `https://your-username.github.io/repo-name/`.

Put the link on your resume, LinkedIn, and GitHub profile.

## 6. Using AI on this template

Good prompts include **context** (what you have), a **goal** (what you want), and **constraints** (what to leave alone). Try these:

- *"Here is my `style.css`. Change the accent color to a deep green and keep all text readable. Only edit the `:root` section."*
- *"Make the project cards show two columns on tablets and one on phones. Explain every line you change."*
- *"Here are my About paragraphs and some facts about me: [paste]. Tighten them to under 80 words."* Then rewrite the result in your own voice.
- *"My photo isn't showing. Here is my folder structure and my `<img>` tag: [paste both]."*
- *"Explain `grid-template-columns: repeat(auto-fit, minmax(min(100%, 300px), 1fr))` in plain English."*

Three rules:
1. When something breaks, paste the exact error or a screenshot, not "it doesn't work."
2. Run the code and read it before you keep it.
3. If you can't explain a line, don't ship it. Ask the AI to explain it first.

Never paste passwords, API keys, or anything private into an AI tool.

## Troubleshooting

| Problem | Fix |
|---|---|
| Image doesn't show | The path and capitalization must match exactly. `images/Me.jpg` and `images/me.jpg` are different files once the site is online. |
| CSS changes don't appear | Save the file, then hard refresh (Ctrl+Shift+R). Confirm `index.html` still has `<link rel="stylesheet" href="style.css">`. |
| Fonts look different | Fonts load from Google Fonts, so they need an internet connection. |
| Site is blank after deploying | `index.html` must be at the top level of the folder you uploaded, not inside another folder. |
| Page looks broken after an edit | Undo with Ctrl+Z, or ask an AI to find the problem: paste the section you changed. |

## What's next

Part 2 of the workshop redesigns this site in Figma and rebuilds it in React, so keep your finished version.
