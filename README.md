# Meal Kits Made Easy

Static site for the cookbook by Stephanie Wright. No build step.

Repo: https://github.com/kennywright10-rgb/MealKitsMadeEasy

## Deploy (Git Bash)

    cd "/c/Users/ken/Desktop/claude/Meal Kits Made Easy"
    git init -b main
    git remote add origin https://github.com/kennywright10-rgb/MealKitsMadeEasy.git
    git add .
    git commit -m "Launch site for Meal Kits Made Easy"
    git push -u origin main

If the push is rejected because the repo already has a README or license:

    git pull origin main --allow-unrelated-histories --no-edit
    git push -u origin main

Then in Vercel: Add New > Project > import MealKitsMadeEasy. Framework preset
"Other", leave build command and output directory empty, Deploy. Add
mealkitsmadeeasy.com under Settings > Domains.

## Updates after launch

    git add .
    git commit -m "Describe the change"
    git push

## Notes

- Domain: mealkitsmadeeasy.com (set www as primary in Vercel, redirect the apex).
- Prices on the page are hardcoded ($49.99 hardcover, $39.99 paperback). If
  the IngramSpark price changes, search index.html for 49.99 and 39.99.
- The book PDF is in .gitignore on purpose. Never commit it.
