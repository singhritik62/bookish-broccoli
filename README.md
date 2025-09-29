## React Frontend Setup Guide (macOS)

xghoul@Ritiks-MacBook-Pro ~ % /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
xghoul@Ritiks-MacBook-Pro ~ % echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zshrc
xghoul@Ritiks-MacBook-Pro ~ % brew install nvm
nvm install --lts
xghoul@Ritiks-MacBook-Pro ~ % brew install --cask docker
xghoul@Ritiks-MacBook-Pro ~ % docker ps
xghoul@Ritiks-MacBook-Pro ~ % gh login auth 
xghoul@Ritiks-MacBook-Pro ~ % gh auth login

This guide provides step-by-step instructions to set up a React frontend project using Vite on macOS. It covers installing required tools and initializing your project.

---

### Prerequisites

- macOS system
- Terminal access

---

### 1. Install Homebrew

Homebrew is a package manager for macOS.

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

After installation, add Homebrew to your shell profile:

```bash
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zshrc
source ~/.zshrc
```

---

### 2. Install Node Version Manager (nvm) and Node.js

```bash
brew install nvm
mkdir ~/.nvm
echo 'export NVM_DIR="$HOME/.nvm"' >> ~/.zshrc
echo '[ -s "/opt/homebrew/opt/nvm/nvm.sh" ] && . "/opt/homebrew/opt/nvm/nvm.sh"' >> ~/.zshrc
source ~/.zshrc
nvm install --lts
nvm use --lts
```

---

### 3. Install Docker (optional, for containerization)

```bash
brew install --cask docker
open -a Docker
```

---

### 4. Install MySQL (optional, for database)

```bash
brew install mysql
brew services start mysql
```

To secure your MySQL installation:

```bash
mysql_secure_installation
```

---

### 5. Install Git and GitHub CLI

```bash
brew install git gh
```

Authenticate GitHub CLI:

```bash
gh auth login
```

---

### 6. Create Your React Project with Vite

```bash
mkdir my-react-app
cd my-react-app
npm create vite@latest client
# Follow prompts: Choose React, JavaScript
cd client
npm install
npm run dev
```

Your React app will be running at [http://localhost:5173/](http://localhost:5173/)

---

### 7. Initialize Git Repository (optional)

```bash
git init
git add .
git commit -m "Initial commit"
```

---

## Notes

- For Linux/Windows, installation steps will differ.
- For more details, see the official docs:
  - [Homebrew](https://brew.sh/)
  - [nvm](https://github.com/nvm-sh/nvm)
  - [Vite](https://vitejs.dev/)
  - [React](https://react.dev/)
  - [Docker](https://www.docker.com/)
  - [MySQL](https://dev.mysql.com/doc/)
  - [GitHub CLI](https://cli.github.com/)


