# Create a new repository on the command line

echo "# git-fetch--git-merge--example" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/brucestull/git-fetch--git-merge--example.git
git push -u origin main