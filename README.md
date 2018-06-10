# Merge two separate git repositories into one
For example, imagine you have created your repository on your computer.
Then you create a new repository on Github and add a README and a LICENSE.
Technically, you have two separate repositories now. With "unrelated histories".

Here is how you merge the one you created on github into your local one and push it back onto github.

```
git init
git commit --allow-empty -m "Empty."
git add -A
git commit -m "First commit on my local."
git remote add github git@github.com:cooluser/coolrepo.git
git fetch github
git branch --set-upstream-to=github/master master
git pull --rebase --allow-unrelated-histories
git push
```

