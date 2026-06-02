# 🚀 RENDER + CRON-JOB.ORG SETUP GUIDE

## ─── STEP 1: Render Deploy ───

1. https://render.com → Sign Up / Login
2. New → Web Service
3. Connect GitHub repo (bot files upload করো)
4. Settings:
   - Name: bd-alamin-signal-bot
   - Runtime: Python 3
   - Build Command: `pip install -r requirements.txt`
   - Start Command: `python Analyse_Bot.py`

5. Environment Variables (Add করো):
   - BOT_TOKEN = তোমার bot token
   - OWNER_ID  = তোমার Telegram user ID

6. → Create Web Service

---

## ─── STEP 2: cron-job.org (24/7 জাগিয়ে রাখার জন্য) ───

1. https://cron-job.org → Free Account
2. Create Cronjob:
   - URL: https://YOUR-APP-NAME.onrender.com/ping
   - Schedule: Every 5 minutes
3. Save করো ✅

---

## ─── FILES ───

| File             | কাজ                        |
|------------------|----------------------------|
| Analyse_Bot.py   | Main bot                   |
| requirements.txt | Python packages            |
| signal_data.pkl  | Auto-create হবে (PKL data) |

---

## ─── SIGNAL FORMAT ───

🚀 𝗕𝗗 𝗔𝗟𝗔𝗠𝗜𝗡 | 𝗩𝗜𝗣 𝗦𝗜𝗚𝗡𝗔𝗟 🚀

𝟭𝟬𝟬𝟯𝟭 | 𝗕𝗜𝗚 × 𝟳/𝟮 ✅
𝟭𝟬𝟬𝟯𝟮 | 𝗦𝗠𝗔𝗟𝗟 × 𝟯/𝟲 🎰
𝟭𝟬𝟬𝟯𝟯 | 𝗕𝗜𝗚 × 𝟴/𝟭

---

## ─── RESULT LOGIC ───

- 🎰 JACKPOT = exact number (7 বা 2) মিলেছে → Jackpot sticker + Win sticker
- ✅ WIN     = শুধু BIG/SMALL direction মিলেছে → Win sticker
- ❌ LOSS    = কিছুই মিলেনি → Loss sticker

## ─── SEASON OFF ───
Signal বন্ধ হলে পরের period এ:
1. Win/Loss/Jack sticker
2. Season Off sticker
3. Stats message:

📊 𝗦𝗘𝗔𝗦𝗢𝗡 𝗥𝗘𝗦𝗨𝗟𝗧
🎯 Total Signals : X
✅ Total Wins   : X
🎰 Total Jack   : X
❌ Total Loss   : X
