# AIMless

*A WebRTC chat app with absolutely no purpose, direction, or server*

```
💀 10KB of pure chaos
🚫 Zero dependencies 
🤝 Two users max (more would require planning)
📋 Connection via clipboard (like animals)
```

---

## What The Hell Is This?

I crammed an entire P2P encrypted chat application into a single HTML file. No backend. No build step. No npm. It's literally one file you can email to your mom (please don't).

**Current Status:** Somehow works™

**Production Ready?** *nervous laughter*

---

## 🎪 The Circus Installation Guide

### Method 1: YOLO Mode
```bash
# Just fucking double-click index.html
# Yes, from your Downloads folder
# Yes, it actually works
```

### Method 2: Slightly Less Cursed
```bash
python3 -m http.server 8000
# Congrats, you're now a sysadmin
```

### Method 3: Peak Web Development
```bash
# Email index.html to your friend
# They open it
# You're now chatting P2P
# Web developers hate this one weird trick
```

---

## 🤡 How To Connect (Prepare for Pain)

### Step 1: The Ritual Begins
- One person clicks **Host** (the brave one)
- Other person clicks **Peer** (the coward)
- Both contemplate life choices

### Step 2: The Copypasta Dance
1. **Host** clicks "Create Offer"
2. A wild Base64 blob appears! 
3. Copy this cursed string
4. Send it via:
   - Discord (will probably mangle it)
   - Email (boomer mode)
   - Carrier pigeon (most reliable)
   - Writing it on paper (absolute madness)

### Step 3: The Exchange
```
Host: "Here's my blob bro"
Peer: "Thanks, here's mine"
Host: "Why are we like this"
Peer: "I don't know"
[CONNECTION ESTABLISHED]
```

### Step 4: Success(?)
When all three pills turn green, you've achieved P2P. Your ISP is confused. Your firewall is crying. But you're chatting.

---

## 🏗️ Architecture (lmao)

```
index.html (10KB of nightmares)
├── CSS (dark mode because we code at 3am)
├── HTML (two divs and a dream)
└── JavaScript (where the magic/curse happens)
    ├── Copy/paste "signaling" (revolutionary)
    ├── WebRTC (doing heavy lifting)
    └── Error handling (console.error lol)
```

### State Management
```javascript
let role = 'host';  // or 'peer', we don't judge
let pc, dc;         // undefined until they're not
```

### The Entire Signaling Server
```javascript
// Step 1: Copy
navigator.clipboard.writeText(blob)

// Step 2: Paste
// There is no step 3
```

---

## 🔬 Technical "Features"

### Non-Trickle ICE (Because We're Lazy)
```javascript
// Wait 300ms and pray all candidates arrived
setTimeout(() => {
  $('local').value = pack(pc.localDescription);
}, 300);
```

### Blob Format Detection (Pattern Matching Go Brrr)
```javascript
if (looksLikeJson(raw))      // Probably JSON
else if (isBase64(raw))      // Probably Base64  
else if (looksLikeSdp(raw))  // Definitely cursed
else throw new Error('¯\\_(ツ)_/¯');
```

### "Database"
```javascript
const database = []; // That's it. That's the database.
// Oh wait, we don't even have that.
```

---

## 🎨 UI/UX Masterclass

- **Three pills** that change colors (green = good, red = bad, revolutionary UX)
- **Two textareas** for your blob needs
- **One chat box** (wanting more is capitalism)
- **Dark theme** (because light attracts bugs)

### Connection Status Pills

| Pill | What It Means | What It Really Means |
|------|---------------|---------------------|
| PC: `idle` | Not started | Procrastinating |
| PC: `connecting` | Trying | WebRTC doing WebRTC things |
| PC: `connected` | Working | Holy shit it worked |
| ICE: `checking` | Finding path | NAT traversal go brrr |
| DC: `open` | Can chat | Time to send memes |

---

## 🚨 Security "Model"

- ✅ **E2E Encrypted** (thanks WebRTC, we did nothing)
- ✅ **No cookies** (we're not monsters)
- ✅ **No tracking** (we literally don't care)
- ✅ **No server logs** (what server?)
- ⚠️ **No authentication** (your friend might be three squirrels in a trenchcoat)
- ⚠️ **Blob contains your IP** (share wisely, or don't, we're not your mom)

---

## 💀 Known Issues (Features)

| "Bug" | Status | Workaround |
|-------|--------|------------|
| Can't connect through corporate firewall | Won't fix | Quit your job |
| Copy button fails on `file://` | Browser's fault | Ctrl+C like a caveman |
| Only supports 2 users | By design | Make better friends |
| No message history | RAM is temporary | Remember harder |
| No mobile app | This IS the app | Your phone has a browser, Kevin |
| Sometimes just doesn't work | Yes | Try again (or don't) |

---

## 🤔 Philosophy

> "Why would you do this?"  
> — Everyone

> "Your scientists were so preoccupied with whether they could, they didn't stop to think if they should."  
> — Dr. Ian Malcolm, about this project probably

This project exists because:
1. Signaling servers are a scam by Big WebSocket
2. We were told it couldn't be done in one file
3. Sometimes you just need to chat without AWS knowing about it
4. `npm install` is for cowards

---

## 🔮 Roadmap

- [x] Make it work
- [x] Make it cursed
- [ ] Make it worse
- [ ] Add blockchain (just kidding, we're not that evil)
- [ ] Group chat (would require actual effort)
- [ ] File transfer (you have email for that)

---

## 🙏 Credits

- **WebRTC**: For doing 99% of the work
- **Google's STUN servers**: Thanks for the free infrastructure, nerds
- **Stack Overflow**: You know why
- **The void**: For staring back

---

## 📜 License

MIT (Memes Included, Thanks)

Do whatever you want with this cursed code. Email it. Print it. Fax it. Deploy it to production (don't). We're not responsible for the consequences.

---

<p align="center">
  <sub>A project that shouldn't exist, but does</sub><br>
  <sub>10KB of bad decisions</sub><br>
  <sub>🔥 This is fine 🔥</sub>
</p>

<p align="center">
  <br>
  <i>"It's not a bug, it's the entire project"</i>
</p>
