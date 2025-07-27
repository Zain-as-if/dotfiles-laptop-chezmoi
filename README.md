DOTFILES USING CHEZMOI

Install Dot Files:
```
pacman -S chezmoi
chezmoi init --apply https://github.com/$GITHUB_USERNAME/dotfiles.git
```

Add/Edit Files:
```
chezmoi add [FILE]
chezmoi add [DIRECTORY] [DIRECTORY_NAME]

# Edit Source State
chezmoi edit [FILE]
# Apply Changes
chezmoi -v apply

# See Changes Chezmoi Would Make
chezmoi diff

# Commit Changes + Push
chezmoi cd
git add .
git commit -m "[Commit Msg]"

git remote add origin git@github.com:Zain-as-if/dotfiles-laptop-chezmoi.git
git branch -M main
git push -u origin main

# Exit Shell Return To Where You Were
exit
