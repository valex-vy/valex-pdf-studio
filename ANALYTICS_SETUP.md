# 📊 Google Analytics Setup & Dashboard Guide

## Overview

This guide helps you monitor visitor analytics for Valex PDF Studio using Google Analytics 4 and real-time visitor counting.

---

## 1. Google Analytics 4 Setup

### View Your Analytics

1. **Visit Google Analytics:** https://analytics.google.com
2. **Select Property:** "Valex PDF Studio" (ID: `G-EW0G1D2EVL`)
3. **View Reports:**
   - **Realtime Dashboard** - Live visitors right now
   - **Acquisition** - Where users come from
   - **Engagement** - Feature usage and interactions
   - **Events** - Conversion tracking

---

## 2. Real-Time Visitor Count

### On Your Website
A live visitor counter appears in the **bottom-left corner** of your site:
```
👥 Visitors: 1,234
```

This updates automatically using the CountAPI.

### API Endpoint
```
https://api.countapi.xyz/hit/valex-pdf-studio/visits
```

Get the current count:
```
https://api.countapi.xyz/get/valex-pdf-studio/visits
```

---

## 3. Key Analytics Metrics

### What's Being Tracked:

| Event | What It Measures |
|-------|-----------------|
| `page_view` | Each time someone visits |
| `tab_switch` | Which PDF tool they use |
| `pdf_converted` | File-to-PDF conversions |
| `pdf_to_images` | PDF extraction as images |
| `pdf_to_text` | PDF to text extraction |
| `pdf_to_word` | PDF to Word conversion |
| `pdfs_merged` | PDF merge operations |
| `pdf_compressed` | PDF compression usage |
| `theme_toggle` | Dark mode preference |

---

## 4. Custom Dashboard in GA4

### Create a Business Dashboard

1. **Login to Google Analytics**
2. **Click:** Dashboards → New Dashboard
3. **Name it:** "Valex PDF Studio - Business Metrics"

### Add These Cards:

#### Card 1: Active Users (Real-Time)
- **Metric:** Realtime active users
- **Dimensions:** None
- **Comparison:** Day before

#### Card 2: Conversions by Tool
- **Metric:** Event count
- **Dimensions:** Event Name
- **Filter:** Contains "pdf" or "conversion"

#### Card 3: Top Conversion Path
- **Metric:** Event count
- **Dimensions:** Event Name → Landing Page
- **Sorting:** Count descending

#### Card 4: User Engagement
- **Metric:** Average engagement time
- **Dimensions:** Country
- **Filter:** Engagement time > 30 seconds

#### Card 5: Conversion Rate
- **Metric:** Conversion rate
- **Dimensions:** Traffic source
- **Calculation:** (Conversions / Sessions) × 100

---

## 5. Setting Up Goals/Conversions

### Mark Conversions

1. **Go to:** Admin → Conversions
2. **Create Conversion:** "PDF Conversion"
   - **Event Name:** `pdf_converted`
   - **Conversion Category:** Purchase (or custom)

3. **Create Conversion:** "Feature Usage"
   - **Event Name:** `pdf_to_images` OR `pdf_to_text` OR `pdfs_merged`

### View Conversion Funnel

1. **Navigate:** Exploration → Funnel
2. **Set Steps:**
   - Step 1: Landing page → "/"
   - Step 2: Tab switch → Event = "tab_switch"
   - Step 3: Conversion → Event contains "pdf"

---

## 6. Weekly Analytics Report

### Check Every Monday:

1. **Realtime Viewers:** How many are using it RIGHT NOW?
2. **Weekly Users:** Sessions → Compare to last week
3. **Top Tool:** Which PDF feature is most popular?
4. **Conversion Rate:** What % of visitors use a conversion tool?
5. **Geography:** Where are your users from?
6. **Devices:** Mobile vs Desktop split

---

## 7. Monetization Insights

### Use Analytics for Ad Placement:

- **High Engagement Areas:** Place ads around high-conversion tools
- **User Journey:** Understand where to add premium features
- **Geography:** Target high-value regions first
- **Device:** Mobile optimization = higher revenue potential

### Key Metrics for Monetization:
```
Monetization Score = (Conversions × Average Session Duration) / Bounce Rate
```

---

## 8. Troubleshooting

### Visitor Count Not Updating?
```
1. Check browser console (F12)
2. Verify: https://api.countapi.xyz/get/valex-pdf-studio/visits
3. Ensure site is public/live
```

### GA4 Not Showing Events?
```
1. Check GA4 event collection is enabled
2. Wait 24-48 hours for events to appear
3. Use Realtime tab to verify events fire
```

### Low Visitor Count?
```
1. Share on social media
2. Optimize for SEO
3. Add to directories (ProductHunt, etc.)
4. Get backlinks from relevant sites
```

---

## 9. Optimization Tips

### To Increase Conversions:

1. **Fast Page Load** - Optimize JS bundle size
2. **Mobile-First Design** - Most users are mobile
3. **Clear CTAs** - Make conversion tools obvious
4. **A/B Testing** - Test different layouts
5. **User Feedback** - Add survey to gather insights

### To Increase Users:

1. **SEO Optimization** - Target keywords like "free PDF converter"
2. **Social Sharing** - Add share buttons
3. **Email Marketing** - Collect emails for newsletter
4. **Referral Program** - Reward users who refer friends
5. **Content Marketing** - Blog posts about PDF tips

---

## 10. Advanced Features

### Set Up Custom Reports

**Report 1: Daily Revenue Potential**
```
Metric: Event Count (pdf_converted)
Dimension: Date
Filter: Date is (last 7 days)
Goal: Show growth trend
```

**Report 2: User Quality Scoring**
```
Metric: Average Engagement Time
Dimension: User ID (anonymized)
Filter: Engagement time > 1 minute
Goal: Find high-value user segments
```

---

## 🎯 Success Metrics

Track these monthly:

| Metric | Target | Current |
|--------|--------|---------|
| Monthly Users | 1,000+ | |
| Daily Active Users | 50+ | |
| Conversion Rate | 15%+ | |
| Avg Session Duration | 2+ min | |
| Bounce Rate | <50% | |
| Mobile %Conversion | 20%+ | |

---

## 📞 Support

For questions about analytics:
- Google Analytics Support: https://support.google.com/analytics
- CountAPI Docs: https://countapi.xyz
- Email: support@valexndichu.com

---

**Last Updated:** May 27, 2026
**Next Review:** June 27, 2026
