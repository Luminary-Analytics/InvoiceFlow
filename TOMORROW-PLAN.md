# InvoiceFlow - Launch Plan

**Created:** January 25, 2026  
**Goal:** Get InvoiceFlow live and generating revenue

---

## 🎯 Tomorrow's Tasks (30-45 min total)

### 1. Push to GitHub (5 min)
```powershell
cd C:\Repos\NewStartup
git add .
git commit -m "Initial commit - InvoiceFlow invoice generator"
git branch -M main
# Create repo at github.com/richbellantoni/invoiceflow (or similar)
git remote add origin https://github.com/YOUR_USERNAME/invoiceflow.git
git push -u origin main
```

### 2. Deploy to Render (10 min)
1. Go to [render.com](https://render.com) → Sign up/Login
2. Click **New** → **Static Site**
3. Connect GitHub → Select `invoiceflow` repo
4. Settings auto-detect from `render.yaml`
5. Click **Create Static Site**
6. Wait ~2 min → Site live at `invoiceflow.onrender.com`

### 3. Test the Live Site (5 min)
- [ ] Create a test invoice
- [ ] Download PDF
- [ ] Check mobile view
- [ ] Verify Pro modal works

### 4. Buy Domain (10 min)
**Recommended:** `invoiceflow.app` (~$14/yr at Namecheap or Porkbun)

**Alternatives if taken:**
- invoiceflow.io
- getinvoiceflow.com
- invoiceflowapp.com
- makeinvoice.app

### 5. Connect Domain to Render (10 min)
1. Render Dashboard → Your site → Settings → Custom Domains
2. Add `invoiceflow.app` and `www.invoiceflow.app`
3. At your registrar, add DNS records:
   - CNAME: `@` → `invoiceflow.onrender.com`
   - CNAME: `www` → `invoiceflow.onrender.com`
4. Wait 5-30 min for DNS propagation
5. HTTPS auto-enabled by Render

---

## 📅 This Week's Tasks

### Day 2-3: Payments
- [ ] Create Stripe account
- [ ] Create product: "InvoiceFlow Pro" - $9/month
- [ ] Create Payment Link
- [ ] Update `checkout()` function in index.html with Stripe link
- [ ] Set success URL to `https://yourdomain.com/?pro=success`
- [ ] Add code to handle success and unlock Pro

### Day 3-4: Analytics & SEO
- [ ] Set up Google Search Console
- [ ] Submit sitemap (just the main URL for now)
- [ ] Set up Plausible or Umami analytics
- [ ] Verify meta tags look good on social preview

### Day 4-5: Launch Marketing
- [ ] Product Hunt (schedule for Tuesday or Wednesday AM)
- [ ] Post on r/SideProject
- [ ] Post on r/freelance (helpful, not spammy)
- [ ] Submit to Indie Hackers
- [ ] Submit to BetaList
- [ ] Submit to AlternativeTo
- [ ] LinkedIn post about the launch

---

## 🚀 Future Improvements (Prioritized)

### High Impact / Low Effort
1. **Email capture** - Add "Get invoice tips" newsletter signup (ConvertKit/Buttondown)
2. **Social proof** - Add testimonials section (even if simulated at first)
3. **Template gallery** - Show 3-4 invoice styles (1 free, rest Pro-locked)
4. **Referral program** - "Share for 1 month free" viral loop

### High Impact / Medium Effort
5. **Blog/SEO content** - Target "free invoice generator" keywords
   - "How to Invoice as a Freelancer"
   - "Invoice Template for Photographers"
   - "When to Send an Invoice"
6. **Invoice history** - Save past invoices (still localStorage, no backend)
7. **Logo upload** - Let Pro users add their logo to invoices
8. **Recurring invoices** - Auto-generate monthly invoices

### Medium Impact / Medium Effort
9. **Multiple templates** - 5-10 different invoice designs
10. **Client database** - Save client info for reuse
11. **Email sending** - Send invoice directly via email (needs backend or service)
12. **Custom colors** - Let Pro users pick brand colors

### Bigger Features (Later)
13. **User accounts** - Real login/signup (Firebase Auth or similar)
14. **Cloud sync** - Save invoices to server, access anywhere
15. **Payment tracking** - Mark invoices as paid/unpaid
16. **Reports** - Revenue dashboard, client stats
17. **Multi-user** - Teams/organizations

---

## 💰 Revenue Milestones

| Milestone | Pro Subscribers | MRR | How to Get There |
|-----------|-----------------|-----|------------------|
| $100/mo | 12 | Launch + friends/family |
| $500/mo | 56 | SEO + content + directories |
| $1000/mo | 112 | Product Hunt + sustained traffic |
| $2000/mo | 223 | Strong SEO + word of mouth |

**Key metric:** At 2% conversion, need ~5,600 monthly visitors for $1000 MRR

---

## 🔧 Technical Debt to Address

1. **Scripts folder** - The `scripts/ralph/` folder has some kind of automation script. Review if needed or remove.
2. **Single HTML file** - Works for now, but consider splitting CSS/JS if it grows
3. **No backend** - Limits features. Consider Supabase or Firebase if user accounts become necessary.

---

## 📝 Notes

- The app is production-ready and fully functional
- All monetization UI is built, just needs Stripe connection
- SEO meta tags are in place
- Mobile responsive design works well

**Remember:** Perfect is the enemy of shipped. Get it live first, improve later.

---

## Quick Commands

```powershell
# Open the app locally
cd C:\Repos\NewStartup
start public\index.html

# Git workflow
git status
git add .
git commit -m "message"
git push

# Check file structure
Get-ChildItem -Recurse -File | Select Name
```

---

Good luck, Rich! 🚀
