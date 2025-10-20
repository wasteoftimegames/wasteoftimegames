# Keep main branch for source
git checkout main
git add .
git commit -m "Save source code"

# Build Hugo
hugo -b https://wasteoftimegames.github.io/

# Deploy public/ to gh-pages
cd public
git init
git remote add origin https://github.com/wasteoftimegames/wasteoftimegames.git
git checkout -b gh-pages
git add .
git commit -m "Deploy site"
git push -u origin gh-pages --force