# 🛠️ Full Setup Guide to grab THE SWARM ROLE in Gensyn Discord

## 1. Install Go on your system/VPS (Linux)
   a) install go 

```bash
cd ~
wget https://go.dev/dl/go1.24.0.linux-amd64.tar.gz
sudo rm -rf /usr/local/go
sudo tar -C /usr/local -xzf go1.24.0.linux-amd64.tar.gz
```
   b) Update Your PATH
```bashecho 'export PATH=$PATH:/usr/local/go/bin' >> ~/.bashrc
echo 'export GOPATH=$HOME/go' >> ~/.bashrc
echo 'export PATH=$PATH:$GOPATH/bin' >> ~/.bashrc
```
  c) reload your .bashrc
```bash
source ~/.bashrc
```
  d) Verify Go Installation 
```bash
go version
```
this will give you output like : go version go1.24.0 linux/amd64

## 2. Install brew on your system/VPS (Linux)
   a) install Homebrew
```bah
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
   b) Add Homebrew to Your PATH
```bash
echo 'export PATH="/home/linuxbrew/.linuxbrew/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```
   c) Verify Homebrew Installation
```bash
brew --version
```
   d) install go using hombrew (optional)
   (However, since we have already installed go manually, you may skip this command and go to next command)
```bash
brew install go
```
## 3. Set Temporary Pssword for Sudo (This part is only for those who are connecting vps via SSH key others should skip this part)

   a) Set Password for your user
```bash
sudo passwd yourusername
```
⚠️ Replace `yourusername` with your actual user account name. Example : sudo passwd bunny You'll be prompted to enter a password

## 4. 🤖 Pre-Setup Telegram Bot

   a) Create tg Bot
- Go to https://t.me/BotFather or @BotFather
- Type /newbot and follow the prompts.
- Choose name and username for your bot
- Once Created, Bot father will give you a meesgae tha contains, Token like `1234567890:ABCDEFG00000Cq7Rod8o010NxPzr1s`, keep this token safe

   b) Get your Chat UserId
- Send any message to your bot to start the interaction
- Then, Visit this URL (Replace `YOUR_BOT_TOKEN` with actual token):
```bash
https://api.telegram.org/botYOUR_BOT_TOKEN/getUpdates
```
You eill get a respone with your Chat Id. If it returns an empty result, try sending multiple message again, then refrsh the url again

Save Your Chat ID also for futher Process

## 5. Install and Configure GSwarm

   a) Install GSwarm
```bash
go install github.com/Deep-Commit/gswarm/cmd/gswarm@latest
```

  b) Verify GSwarm Installation
```bash
gswarm --version
```

  c) Start GSwarm 
```bash
gswarm
```
🔄️ Now, You will now need to input your Bot Token, Chat ID, and EOA address (which you can find on Gensyn Dashboard)

Follow the prompts:
- Enter your BOT TOKEN
- Enter Your Chat ID
- Enter EOA Address (From Dashboard)

## 6. Linking Discord & Telegram (For The Swarm Role)

   a) Get Verification code from Discord
- in the Gensyn Discord, go to the swarm-link channel
- Type `/link-telegram` and you will receive verification code.

   b) Verify Code in Telegram Bot
- Go to your Telegram Bot.
- Type `/verify (code)`, replace (code) with the actual verification code you got from Discord.

  Once Verified, you will get message from the bot
"✅ **Account Successfully Linked!**

Accounts linked successfully

🎉 You can now use both Discord and Telegram to interact with G-Swarm!"

This is means you have been verified, and your role will automatically be assigned.


---

✔️ Done!
Congratulations, you have completed the installation and configuration of Go, GSwarm, Telegram bot, and linked Discord. You should now be all set!

If you encounter any issues or need further help, feel free to reach out again. Enjoy using GSwarm!

---

Track Gensyn Peer ID, Score, Wins, and Transactions Using Telegram Bot
Track Gensyn Updates via Telegram

To keep track of your Peer ID, score, wins, and transactions in Gensyn, you can use the [gensynupdate_bot](https://gensynupdate_bot) on Telegram.

Or Search for the @gensynupdate_bot on Telegram

Start the bot and follow the prompts to track updates related to your Peer ID, score, and transactions.

The bot will send you notifications whenever there’s an update or a change in your stats.

