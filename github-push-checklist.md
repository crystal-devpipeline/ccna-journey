### GitHub Push Checklist

# 1. Navigate to your repo folder
cd ~/Desktop/ccna-journey

# 2. Check the status of your repo
git status

# 3. Stage all changes
git add .

# 4. Commit the changes
git commit -m "Add: updated DHCP notes"

# 5. Push to GitHub (SSH method)
git push origin main

# ✅ No password prompts if SSH is set up correctly!

---

### 🔐 SSH Authentication Setup (One-Time Setup)

# 1. Generate a new SSH key
ssh-keygen -t ed25519 -C "crystalsorensen007@gmail.com" -f ~/.ssh/id_ed25519_ccna

# 2. Add the key to your SSH agent
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519_ccna

# 3. Copy the public key to your clipboard
cat ~/.ssh/id_ed25519_ccna.pub | pbcopy

# 4. Go to GitHub > Settings > SSH and GPG Keys > New SSH Key
#    - Title: MacBook Pro
#    - Paste the key and save

# 5. Point your local repo to use SSH
cd ~/Desktop/ccna-journey
git remote set-url origin git@github.com:crystal-devpipeline/ccna-journey.git

# 6. Verify SSH works
ssh -T git@github.com

# 7. Push with confidence 💥
git push origin main

---

### 📁 Suggested Repo Structure for `ccna-journey`

```
ccna-journey/
├── README.md                # Overview of your CCNA journey
├── study-log.md             # Daily/weekly progress notes
├── notes/                   # Written topic notes (markdown or text files)
│   ├── dhcp-notes.md
│   └── osi-model.md
├── labs/                    # Packet Tracer or CLI-based lab instructions
│   ├── lab01-basic-routing.md
│   └── lab02-switching.md
├── scripts/                 # Bash or Python scripts for automation/testing
│   └── ping-sweep.sh
└── resources/               # Helpful links, cheat sheets, or diagrams
    └── subnetting-chart.png
```

---
