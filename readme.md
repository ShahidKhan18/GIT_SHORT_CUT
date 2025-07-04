# 🚀 Bashrc Setup for Git Commit Shortcuts

## ✅ **Objective**

Set up **git commit shortcuts**, rename functions, and useful aliases for an efficient, standardised, and productive development workflow.

---

## 🔹 **1. Open `.bashrc` in VS Code**

```bash
code ~/.bashrc
```




## 🔹**2. Paste the following at the end of your `.bashrc`**

```bash

##########################################
# 🚀 Git Commit Shortcuts Functions
##########################################


function gm-init() { git commit -m ":tada: INIT : $*"; }
function gm-feature() { git commit -m ":sparkles: FEATURE : $*"; }
function gm-fix() { git commit -m ":bug: FIX : $*"; }
function gm-delete() { git commit -m ":fire: DELETE : $*"; }
function gm-refactor() { git commit -m ":hammer: REFACTOR : $*"; }
function gm-docs() { git commit -m ":books: DOCS : $*"; }
function gm-style() { git commit -m ":lipstick: STYLE : $*"; }
function gm-test() { git commit -m ":white_check_mark: TEST : $*"; }
function gm-deploy() { git commit -m ":rocket: DEPLOY : $*"; }
function gm-upgrade() { git commit -m ":arrow_up: UPGRADE : $*"; }
function gm-config() { git commit -m ":wrench: CONFIG : $*"; }

##########################################
# 🔄 gmr-init : rename last commit keeping INIT type and emoji
##########################################
function gmr-init() { git commit --amend -m ":tada: INIT : $*"; }

##########################################
# 🆘 gm-help : display commit shortcut guide
##########################################
function gm-help() {
  echo ""
  echo "Git Commit Shortcuts Help"
  echo "-----------------------------"
  echo "gm-init       INIT : initial project setup"
  echo "gm-feature    FEATURE : adding new features or enhancements"
  echo "gm-fix        FIX : bug fixes"
  echo "gm-delete     DELETE : removing files, code, or modules"
  echo "gm-refactor   REFACTOR : code restructuring without behaviour change"
  echo "gm-docs       DOCS : documentation updates"
  echo "gm-style      STYLE : UI, CSS, or formatting changes"
  echo "gm-test       TEST : adding or updating tests"
  echo "gm-deploy     DEPLOY : deployment or CI/CD related changes"
  echo "gm-upgrade    UPGRADE : upgrading dependencies"
  echo "gm-config     CONFIG : configuration or environment changes"
  echo "gmr-init      RENAME INIT : rename last commit keeping INIT type"
  echo ""
  echo "Git Aliases:"
  echo "ga        : git add ."
  echo "gs        : git status"
  echo "gc        : git commit"
  echo "gp        : git push"
  echo "gl        : git pull"
  echo "gco       : git checkout"
  echo "gb        : git branch"
  echo "gcm       : git checkout main"
  echo "gpl       : git pull origin main"
  echo "gps       : git push origin main"
  echo "grh       : git reset --hard HEAD~1 (rollback last commit permanently)"
  echo "grs       : git reset --soft HEAD~1 (rollback last commit keep changes staged)"
  echo "gld       : git log --oneline --graph --decorate --all (git log pretty display)"
  echo "gbd       : delete local branch (usage: gbd branch_name)"
  echo "gbdr      : delete remote branch (usage: gbdr branch_name)"
  echo "gbr       : rename current branch (usage: gbr new_name)"
  echo ""
}

##########################################
# 🔹 Git Aliases
##########################################

alias ga="git add ."
alias gs="git status"
alias gc="git commit"
alias gp="git push"
alias gl="git pull"
alias gco="git checkout"
alias gb="git branch"
alias gcm="git checkout main"
alias gpl="git pull origin main"
alias gps="git push origin main"
alias grh="git reset --hard HEAD~1"
alias grs="git reset --soft HEAD~1"
alias gld="git log --oneline --graph --decorate --all"

function gbd() { git branch -d $1; }
function gbdr() { git push origin --delete $1; }
function gbr() { git branch -m $1; }

```
## 🔹 **3. Save and apply changes**
source ~/.bashrc

## 🔹**4. Usage Examples**
```bash
ga
gm-feature added login functionality
gm-fix fixed bug in user auth
gmr-init initialised ecommerce backend
gm-help
```
