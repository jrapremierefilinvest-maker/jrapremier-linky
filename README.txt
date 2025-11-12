
JRA Premier Linky - Netlify CMS package
--------------------------------------

Contents:
- index.html                (public linky page)
- admin/config.yml          (Netlify CMS config - edit repo name before use)
- admin/index.html          (Netlify CMS loader)
- content/links.json        (site links and buttons)
- content/faqs.json         (list of FAQ objects)
- content/faqs/*.md         (individual FAQ markdown files)
- profile.jpg               (placeholder image)

How to deploy (quick):
1) Create a new GitHub repo (e.g. 'jrapremier-linky').
2) Upload all files and commit to 'main' branch.
3) In Netlify, 'New site from Git' -> connect your GitHub repo -> deploy.
4) Go to https://<your-site>.netlify.app/admin to open the Netlify CMS admin UI.
   - The admin UI uses the GitHub backend; authenticate with GitHub to edit content.
5) Edit Links (single file) or create new FAQs via the admin UI. Changes auto-commit to the repo and Netlify auto-publishes.

How MIRA integration works:
- You can export content/faqs.json and use it as your canonical FAQ source for MIRA.
- Alternatively, point MIRA to fetch https://<your-site>.netlify.app/content/faqs.json
- The file contains intent triggers, canonical answers, buttons and action URLs.

Notes:
- Edit admin/config.yml: change 'repo' under 'backend' to match your GitHub repo path (user/repo).
- If you prefer Netlify Git Gateway or Identity, additional setup steps are needed (instructions available on Netlify docs).
