# Google Analytics Setup Guide

## 🚀 Quick Setup Steps:

### 1. Create Google Analytics 4 Property
1. Go to [Google Analytics](https://analytics.google.com/)
2. Click "Start measuring" 
3. Create account: "SkillShare"
4. Create property: "Data Science Roadmap"
5. Select industry: "Education"
6. Select time zone: Your timezone
7. Create data stream: "Web"
8. Enter website URL: `https://data-science-roadmap.vercel.app`
9. Enhanced measurement: ✅ Enable
10. Create stream

### 2. Get Your Measurement ID
- After creating stream, you'll see **Measurement ID** (format: G-XXXXXXXXXX)
- Copy this ID

### 3. Replace in Your Code
In `index.html`, replace `GA_MEASUREMENT_ID` with your actual ID:

```html
<!-- Replace G-XXXXXXXXXX with your actual ID -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  gtag('config', 'G-XXXXXXXXXX', {
    page_title: 'SkillShare Data Science Roadmap',
    page_location: 'https://data-science-roadmap.vercel.app/',
    content_group1: 'Data Science Roadmap'
  });
</script>
```

### 4. Deploy Changes
```bash
git add .
git commit -m "Add Google Analytics tracking"
git push origin main
```

## 📊 What You Can Track:

### Basic Metrics:
- **Users**: Unique visitors
- **Sessions**: Total visits
- **Page Views**: Total page views
- **Bounce Rate**: % who leave immediately
- **Session Duration**: Average time on site

### Advanced Metrics:
- **Traffic Sources**: Where visitors come from
- **Popular Pages**: Which sections are most viewed
- **User Behavior**: How users navigate your site
- **Conversion Goals**: Track specific actions

### Real-Time Data:
- **Active Users**: Currently on your site
- **Live Events**: Real-time interactions
- **Geographic Data**: Where users are located

## 🎯 Important Events to Track:

### 1. Section Interactions:
```javascript
// Add to your JavaScript section clicks
gtag('event', 'section_view', {
  'section_name': 'machine_learning',
  'content_type': 'educational'
});
```

### 2. External Link Clicks:
```javascript
// Track when users click resource links
gtag('event', 'resource_click', {
  'link_url': 'https://example.com',
  'resource_type': 'tutorial'
});
```

### 3. Scroll Depth:
```javascript
// Track how far users scroll
gtag('event', 'scroll_depth', {
  'percentage_scrolled': '75'
});
```

## 📱 Mobile App Tracking (Future):
If you create mobile app later:
- Use same Measurement ID
- Enable app + web data streams
- Cross-device tracking

## 🔍 Privacy & Compliance:
- ✅ GDPR compliant
- ✅ No personal data collected
- ✅ Anonymous user tracking
- ✅ Cookie consent can be added later

## 📈 Key Reports to Monitor:

### 1. Acquisition Report:
- Organic Search (Google)
- Direct Traffic
- Social Media
- Referral Sites

### 2. Behavior Report:
- Most popular roadmap sections
- Time spent on each section
- Exit pages

### 3. Audience Report:
- Geographic distribution
- Device types (mobile/desktop)
- New vs returning users

## 🎯 Goals to Set Up:

### 1. Engagement Goal:
- Users who spend 5+ minutes
- Users who view 3+ sections

### 2. Learning Goal:
- Users who click external resources
- Users who complete roadmap sections

## 📊 Dashboard Setup:
Create custom dashboard with:
- Daily active users
- Top 5 sections
- Traffic sources
- Mobile vs desktop

## ⚡ Performance Monitoring:
- Page load times
- Core Web Vitals
- Error tracking
- Conversion rates

---

**Next Steps:**
1. Create your GA4 property
2. Replace `GA_MEASUREMENT_ID` with your actual ID
3. Deploy and start tracking!
4. Check real-time data after 24 hours
