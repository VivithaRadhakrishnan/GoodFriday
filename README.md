# St. Joseph Youth Association Website

A single-file website for the Assoication — no build tools, no Node.js, no npm.
Just open `index.html` in any browser.

---

## 📁 Folder Structure

```
sjya-website/
├── index.html          ← The entire website (edit this)
├── images/             ← Put ALL your photos here
│   ├── hero.jpg
│   ├── founding.jpg
│   ├── generations.jpg
│   ├── member1.jpg ... member8.jpg
│   └── banner.jpg      ← The Good Friday banner photo (already included)
└── README.md           ← This file
```

---

## 🖼️ How to Add Real Photos

Search for `📌` in `index.html` — every placeholder has a comment showing exactly what to replace.

**Example — replacing the hero image:**
```html
<!-- BEFORE (placeholder) -->
<ImgBox alt="Members carrying crates..." h={320}/>

<!-- AFTER (your real photo) -->
<img src="images/hero.jpg" alt="Members carrying crates of water bottles"
     style="width:100%;max-width:680px;border-radius:16px;object-fit:cover;height:320px" />
```

**Photo suggestions:**
| File name        | Where it appears          |
|------------------|---------------------------|
| hero.jpg         | Landing page hero section |
| founding.jpg     | "Our Origin Story" section |
| generations.jpg  | Brotherhood page          |
| member1–8.jpg    | Family Grid gallery       |

---

## ✏️ How to Edit Content

All text is inside `index.html`. Use Ctrl+F (Find) to search for keywords.

- **Stats** (bottles, buns, years): search for `val:6000` or `val:5000`
- **Timeline entries**: search for `const timeline=`
- **Contact email**: search for `stjosephyouth@example.com`
- **Association name / city**: search for `SJYA` or `CHENNAI`

---

## 🚀 Publishing to GitHub Pages (Free Hosting)

### Step 1 — Create a GitHub repository
1. Go to https://github.com/new
2. Name it: `sjya-website` (or anything you like)
3. Set it to **Public**
4. Click **Create repository**

### Step 2 — Upload your files
**Option A — GitHub website (easiest):**
1. Open your new repository
2. Click **Add file → Upload files**
3. Drag the entire `sjya-website` folder contents (index.html + images folder)
4. Click **Commit changes**

**Option B — Git command line:**
```bash
cd sjya-website
git init
git add .
git commit -m "Initial website"
git remote add origin https://github.com/VivithaRadhakrishnan/sjya-website.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages
1. In your repository, click **Settings**
2. Scroll to **Pages** in the left sidebar
3. Under **Source**, select **Deploy from a branch**
4. Choose **main** branch, **/ (root)** folder
5. Click **Save**

### Step 4 — Your website is live!
After ~2 minutes, your site will be at:
```
https://VivithaRadhakrishnan.github.io/sjya-website/
```

---

## 📱 QR Code

Once your site is live at the GitHub Pages URL above, generate a free QR code at:
- https://qr.io  
- https://www.qr-code-generator.com

Paste your URL → Download the QR code image → Print or share!

---

## 🔧 Common Edits

**Change the contact email:**
Search for `stjosephyouth@example.com` and replace with the real email.

**Add a new timeline entry:**
Find `const timeline=[` and add a new object following the same pattern:
```js
{
  period: "2026",
  title: "Your Title Here",
  icon: "🙏",
  highlight: false,          // true = gold milestone styling
  stat: { label: "Bottles", value: 6500, suffix: "" },
  desc: "Your description here."
},
```

**Change the stats bar numbers:**
Search for `val:36` (years), `val:6000` (bottles), `val:5000` (buns) and update.
