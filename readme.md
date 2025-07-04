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


##########################################
# ��� Git Commit Shortcuts Functions using Gitmoji shortcodes
##########################################

##########################################
# ��� gmr : general rename function
# Usage: gmr type "new message part"
# Example: gmr fix "updated auth validation"
##########################################
function gmr() {
  type=$1
  shift
  message=$*

  case $type in
    fix)
      git commit --amend -m ":bug: FIX : $message"
      ;;
    init)
      git commit --amend -m ":tada: INIT : $message"
      ;;
    feature)
      git commit --amend -m ":sparkles: FEATURE : $message"
      ;;
    delete)
      git commit --amend -m ":fire: DELETE : $message"
      ;;
    refactor)
      git commit --amend -m ":hammer: REFACTOR : $message"
      ;;
    docs)
      git commit --amend -m ":books: DOCS : $message"
      ;;
    style)
      git commit --amend -m ":lipstick: STYLE : $message"
      ;;
    test)
      git commit --amend -m ":white_check_mark: TEST : $message"
      ;;
    deploy)
      git commit --amend -m ":rocket: DEPLOY : $message"
      ;;
    upgrade)
      git commit --amend -m ":arrow_up: UPGRADE : $message"
      ;;
    config)
      git commit --amend -m ":wrench: CONFIG : $message"
      ;;
    *)
      echo "Invalid type. Supported types: fix, feature, delete, refactor, docs, style, test, deploy, upgrade, config"
      ;;
  esac
}



# :tada: INIT : initial project setup
function gm-init() {
  git commit -m ":tada: INIT : $*"
}

# :sparkles: FEATURE : new features or enhancements
function gm-feature() {
  git commit -m ":sparkles: FEATURE : $*"
}

# :bug: FIX : bug fixes
function gm-fix() {
  git commit -m ":bug: FIX : $*"
}

# :fire: DELETE : remove files/code/modules
function gm-delete() {
  git commit -m ":fire: DELETE : $*"
}

# :hammer: REFACTOR : code restructuring without behaviour change
function gm-refactor() {
  git commit -m ":hammer: REFACTOR : $*"
}

# :books: DOCS : documentation updates
function gm-docs() {
  git commit -m ":books: DOCS : $*"
}

# :lipstick: STYLE : UI/CSS/formatting changes
function gm-style() {
  git commit -m ":lipstick: STYLE : $*"
}

# :white_check_mark: TEST : adding/updating tests
function gm-test() {
  git commit -m ":white_check_mark: TEST : $*"
}

# :rocket: DEPLOY : deployment or CI/CD related
function gm-deploy() {
  git commit -m ":rocket: DEPLOY : $*"
}

# :arrow_up: UPGRADE : upgrading dependencies
function gm-upgrade() {
  git commit -m ":arrow_up: UPGRADE : $*"
}

# :wrench: CONFIG : configuration/environment changes
function gm-config() {
  git commit -m ":wrench: CONFIG : $*"
}

##########################################
# ��� GM HELP : display commit shortcut guide and usage description (no emojis)
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
  echo "gmr type message : rename last commit with specified type and new message (usage: gmr fix updated bug message)"

  echo ""
  echo "Git Aliases and Shortcuts:"
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
  echo "Usage Example:"
  echo "git add . && gm-fix fixed user login bug"
  echo ""
}

##########################################
# ��� Git Aliases for Frequent Operations
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
alias grh="git reset --hard HEAD~1"    # Rollback last commit permanently
alias grs="git reset --soft HEAD~1"    # Rollback last commit keep changes staged
alias gld="git log --oneline --graph --decorate --all"  # Git log pretty display
alias cls="clear" # To Clear Screan
# Delete local branch
function gbd() {
  git branch -d $1
}

# Delete remote branch
function gbdr() {
  git push origin --delete $1
}

# Rename current branch
function gbr() {
  git branch -m $1
}


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
