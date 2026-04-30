# MySchool Tips Blog

Jekyll blog με tips και οδηγίες για το myschool. Δημοσιεύεται μέσω GitHub Pages.

## 🚀 Πώς να στήσεις το blog στο GitHub

### Βήμα 1: Δημιούργησε το repository

1. Πήγαινε στο [github.com/new](https://github.com/new)
2. Όνομα repository: `michaliskat.github.io`
   - ⚠️ Το όνομα πρέπει να είναι **ακριβώς** `<username>.github.io`
3. Επίλεξε **Public**
4. Πάτα **Create repository**

### Βήμα 2: Ανέβασε τα αρχεία

```bash
# Αρχικοποίησε git στον φάκελο του blog
cd /path/to/blog
git init
git add .
git commit -m "Initial commit: Jekyll blog για myschool tips"

# Σύνδεσε με το GitHub
git remote add origin https://github.com/MichalisKat/michaliskat.github.io.git
git branch -M main
git push -u origin main
```

### Βήμα 3: Ενεργοποίησε το GitHub Pages

1. Στο repository, πήγαινε **Settings → Pages**
2. Στο "Source" επίλεξε **Deploy from a branch**
3. Branch: **main**, Folder: **/ (root)**
4. Πάτα **Save**

Μετά από 1-2 λεπτά το blog θα είναι online στο:
`https://michaliskat.github.io`

---

## 📝 Πώς να γράψεις νέο post

Δημιούργησε αρχείο στον φάκελο `_posts/` με μορφή:

```
_posts/YYYY-MM-DD-titlos-arthrou.md
```

Παράδειγμα: `_posts/2026-05-01-neo-tip-myschool.md`

**Περιεχόμενο αρχείου:**

```markdown
---
layout: post
title: "Τίτλος του άρθρου"
date: 2026-05-01
categories: οδηγίες
---

Κείμενο άρθρου εδώ...
```

Μετά κάνε:
```bash
git add .
git commit -m "Νέο post: τίτλος"
git push
```

Το GitHub Pages θα ενημερωθεί αυτόματα σε 1-2 λεπτά.

---

## 🗂️ Δομή αρχείων

```
.
├── _config.yml          # Ρυθμίσεις Jekyll
├── _posts/              # Άρθρα blog
│   ├── 2026-04-30-eisagogi-sto-myschool.md
│   ├── 2026-04-30-kataxorisi-apousiwn.md
│   └── 2026-04-30-vathmolosies-trimino.md
├── index.md             # Αρχική σελίδα
├── about.md             # Σελίδα "Σχετικά"
└── README.md            # Αυτό το αρχείο
```

## 🔧 Τοπική εκτέλεση (προαιρετικό)

Αν θέλεις να βλέπεις το blog τοπικά πριν κάνεις push:

```bash
gem install bundler jekyll
bundle init
bundle add jekyll minima jekyll-feed jekyll-seo-tag
bundle exec jekyll serve
```

Άνοιξε το browser στο `http://localhost:4000`
