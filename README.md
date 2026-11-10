# Meal Kits Made Easy

Static site for the cookbook by Stephanie Wright. No build step.

## Deploy (Git Bash)

    cd "/c/Users/ken/Desktop/claude/Meal Kits Made Easy"
    git init -b main
    git add .
    git commit -m "Launch site for Meal Kits Made Easy"
    gh repo create meal-kits-made-easy --private --source=. --push

No GitHub CLI? Create an empty repo named meal-kits-made-easy on github.com, then:

    git remote add origin https://github.com/YOUR-USERNAME/meal-kits-made-easy.git
    git push -u origin main

Then in Vercel: Add New > Project > import the repo. Framework preset "Other",
leave build command and output directory empty, Deploy. Add the domain under
Settings > Domains.

## Notes

- Domain: mealkitsmadeeasy.com (set www as primary in Vercel, redirect the apex).
- Prices on the page are hardcoded ($49.99 hardcover, $39.99 paperback). If
  the IngramSpark price changes, update index.html in four places.
- The book PDF is in .gitignore on purpose. Never commit it.
