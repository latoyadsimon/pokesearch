
Activity: deploy your own copy
GitHub: New repository, any name (e.g. my-pokesearch), Public, empty
Its Settings → Pages → Source: GitHub Actions
Clone the class code (box on the right)
Change one line: the base
Commit and push; watch the Actions tab
Open your URL, About, refresh. Post it in the chat
git clone -b unit-9-lecture-1-deploy-pages   https://github.com/kabeier/intro-react-code.git my-pokesearch
cd my-pokesearch
git switch -c main
vite.config.js, the only change:

- base: mode === 'production' ? '/pokesearch/' : '/',

+ base: mode === 'production' ? '/my-pokesearch/' : '/',
  your repo's name, exact spelling, both slashes

git commit -am "base for my repo"
git remote set-url origin https://github.com/<you></you>/my-pokesearch.git
git push -u origin main
