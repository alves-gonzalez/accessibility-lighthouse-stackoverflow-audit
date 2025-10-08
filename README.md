# Stack Overflow Accessibility Audit (Google Lighthouse)

## 👨‍💻 Author
**Alves Gonzalez**  
Software QA Engineer | Accessibility & Automation Testing  
📫 [LinkedIn](https://linkedin.com/in/alves-gonzalez)  
💻 [GitHub](https://github.com/alves-gonzalez)

---

## 📋 Overview
This project documents an **accessibility and performance audit** of [Stack Overflow](https://stackoverflow.com), conducted using **Google Lighthouse** in Chrome DevTools.

The goal of this project was to evaluate Stack Overflow’s adherence to **WCAG 2.1** accessibility standards and identify opportunities for improvement across accessibility, performance, and best practices.

---
## 🏁 Summary
This audit demonstrates the ability to evaluate and document accessibility compliance using **Lighthouse**, interpret WCAG 2.1 results, and communicate actionable recommendations. It’s an example of how I as a QA engineers can integrate accessibility testing into the software quality process.

## 🧠 Tools Used
- **Google Lighthouse** (in Chrome DevTools)
- **Device:** Desktop mode
- **Categories Audited:** Performance, Accessibility, Best Practices, SEO

---

## 📊 Results Summary

| Metric | Score |
|--------|--------|
| **Performance** | 94 |
| **Accessibility** | 88 |
| **Best Practices** | 78 |
| **SEO** | 100 |

> The Accessibility score of 88 indicates moderate compliance with WCAG 2.1, but still highlights important areas for improvement such as ARIA attributes and color contrast.

---

## ⚙️ Audit Details

### 🔍 ARIA Issues
- **Finding:** `[aria-*] attributes do not have valid values.`
- **Impact:** May cause confusion for users relying on screen readers.
- **Recommendation:** Review ARIA labels and ensure they match valid attribute values defined by WAI-ARIA specifications.

### 🎨 Contrast Issues
- **Finding:** Background and foreground colors do not have sufficient contrast ratios.
- **Impact:** Reduces readability for users with low vision or color blindness.
- **Recommendation:** Ensure color contrast ratios meet **WCAG 2.1 AA standards (4.5:1 for normal text, 3:1 for large text)**.

### ⚡ Performance Insights
| Issue | Estimated Savings |
|--------|--------------------|
| Improve image delivery | 227 KiB |
| Render-blocking requests | 170 ms |
| Use efficient cache lifetimes | 52 KiB |
| Forced reflow | Affects LCP |
| Legacy JavaScript | 9 KiB |

### 🕓 Key Metrics
| Metric | Value |
|--------|--------|
| **First Contentful Paint** | 0.8 s |
| **Largest Contentful Paint** | 1.4 s |
| **Total Blocking Time** | 0 ms |
| **Cumulative Layout Shift** | 0 |
| **Speed Index** | 1.2 s |

---

## 🖼️ Visual Reports
Screenshots of the Lighthouse audits are stored in the `/reports` folder:

- `Google Lighthouse Accessibility Report 1.png`
- `Google Lighthouse Accessibility Report 2.png`
- `Google Lighthouse Report Audit 1.png`
- `Google Lighthouse Metric Report 2.png`
- `Google Lighthouse insights Report 3.png`
- `Google Lighthouse Audit.png`

---

## 🧰 Recommendations Summary
1. **Validate all ARIA attributes** to ensure compatibility with assistive technologies.
2. **Improve text and background contrast ratios** to enhance readability.
3. **Optimize image delivery** (use next-gen formats like WebP or AVIF).
4. **Reduce render-blocking scripts** to improve loading performance.
5. **Ensure consistent caching and asset delivery** to improve best practice scores.

---

## 🧪 Next Steps
- Conduct a **manual accessibility review** using keyboard-only navigation and screen readers (e.g., NVDA or VoiceOver).
- Perform **axe DevTools** and **WAVE** audits to supplement Lighthouse automated testing.
- Re-run Lighthouse after fixes to validate improvements.
