# Windows Setup SOP

### 1. Visual Studio Code
<https://code.visualstudio.com/>

extensions:
- Git lens - Git supercharged


### 2. Mongo DB
version: 7.0.31
<https://www.mongodb.com/try/download/community>

```bash
mongod --version
```
*If `mongod` command not found, could be environment variable not created yet. Check in:  
View advanced system settings > Environment Variable > Path  
Make sure bin path `C:\Program Files\MongoDB\Server\7.0\bin` is added.*

Install MongoDB Compass
<https://www.mongodb.com/try/download/compass>

Install MongoDB Command Line Database Tools
<https://www.mongodb.com/try/download/database-tools>

### 3. Redis Insight
<https://redis.io/insight/>

### 4. Postman
<https://dl.pstmn.io/download/latest/win64>

### 5. Git

Git Bash: <https://git-scm.com/install/windows>
- Generate your SSH key pairs in "C:\Users\Username\.ssh"
```
ssh-keygen -t ed25519
```
- Add your ssh public key : <https://github.com/settings/keys>

### 6. Docker
<https://www.docker.com/products/docker-desktop/>

### 7. Ngrok
<https://ngrok.com/download/windows>

### 8. Node.js
<https://nodejs.org/en/download>
v22.22.2 (LTS)

```bash
node -v
```
### 9. OPEN-VPN and VPN access
<https://openvpn.net/downloads/openvpn-connect-v3-windows.msi>

### 10. Discord
<https://discord.com/api/downloads/distributions/app/installers/latest?channel=stable&platform=win&arch=x64>

### 11. Telegram
<https://telegram.org/dl/desktop/win64>


# Mac Setup SOP
### 1. Visual Studio Code
<https://code.visualstudio.com/>

extensions:
- Git lens - Git supercharged
- Biome (formatter)

`cmd+shift+P` to open command palette, select `Shell Command: Install 'code' command in PATH`

### 2. Iterm2 (Terminal)
<https://iterm2.com/downloads.html>

install oh-my-zsh via curl:
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### 3. Install HomeBrew (Package manager)
`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`


### 4. Install Git

```bash
brew install git
git --version #to verify
```

- Generate your SSH key pairs in `$HOME/.ssh`
```bash
ssh-keygen -t ed25519
```
- Add your ssh public key : <https://github.com/settings/keys>


- Insert your ssh config in ~/.ssh/config
```bash
vi ~/.ssh/config

#press i and insert config, example:
Host github
    HostName github.com
    User git
    IdentityFile ~/.ssh/your_key_name
    IdentitiesOnly yes
```
- Setup your commit identity
```bash
git config --global user.name "Your Personal Name"
git config --global user.email "your-email@example.com"
```

### 5. Mongo DB
```bash
brew tap mongodb/brew
brew install mongodb-community@7.0
mongod --version #to verify
```

Install MongoDB Compass
<https://www.mongodb.com/try/download/compass>


### 6. Redis Insight
<https://redis.io/insight/>

### 7. Postman
- for arm64
<https://dl.pstmn.io/download/latest/osx_arm64>

### 8. Docker
<https://desktop.docker.com/mac/main/arm64/Docker.dmg>

### 9. Ngrok
<https://ngrok.com/download/mac-os>

`brew install ngrok`

### 10. Node.js
<https://nodejs.org/en/download>

```bash
# Download and install nvm:
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.4/install.sh | bash

# in lieu of restarting the shell
\. "$HOME/.nvm/nvm.sh"

# Download and install Node.js:
nvm install 22

# Verify the Node.js version:
node -v # Should print "v22.22.2".

# Verify npm version:
npm -v # Should print "10.9.7".
```

### 9. OPEN-VPN and VPN access
<https://openvpn.net/client/>

### 10. Discord
<https://discord.com/api/download?platform=osx>

### 11. Telegram
<https://telegram.org/dl/desktop/mac>