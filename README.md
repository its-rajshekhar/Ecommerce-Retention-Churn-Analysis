# E-Commerce Customer Retention & Churn Strategy (UrbanKart)
**Author:** Raj Shekhar Mishra | Lucknow  
**Date:** November 2025

---

## 🎯 Executive Summary

UrbanKart (fictional) experienced a notable drop in retention—repeat purchase rates fell from ~45% to ~31% within one quarter while acquisition costs rose. This project is an end-to-end diagnosis and action plan combining cohort analysis, behavioral segmentation, product-level fixes, CRM flows, and ROI modelling. The recommendations are prioritized for short-term wins (0–90 days) and structural long-term improvements.

**Primary outcomes:**  
- Root-cause map of churn drivers (product, experience, incentives)  
- A three-pillar retention program: *Engage | Reward | Retain* 
- ROI model showing projected retention lift +16pp and 3× ROI on reactivation campaign

---

## 📌 Problem Statement

UrbanKart is acquiring users but failing to convert acquisition into sustainable revenue because first-time buyers are not returning. The objective is to design measurable retention levers to improve unit economics and LTV.

**Key metrics to improve:** D30 retention, repeat purchase rate, LTV, CAC/LTV ratio.

---

## 🔎 Data & Context (Simulated + Field Inputs)

- Dataset: simulated 3 months of funnel and cohort activity (see `retention_data_sample.csv`).  
- Qualitative inputs: 20 short interviews with customers in Lucknow & Kanpur.  
- Focus areas: onboarding activation, post-order communication, rewards visibility, delivery experience.

---

## 📊 Key Observations

1. **First 15 days matter:** users who reorder within 15 days show 75% lower long-term churn.  
2. **Guest checkout costs:** guest checkout users churn 2× faster vs registered users.  
3. **Delivery & tracking friction:** orders with delayed tracking updates have 1.8× higher churn.  
4. **Reward UX failure:** users report that cashback is confusing and not visible in wallet.

---

## 🧠 Deep Analysis (highlights)

- **Cohort analysis:** Jan cohort D30 = 42%, Feb cohort D30 = 31%, Mar cohort D30 = 30%.  
- **Segmentation:** High AOV (>₹1500) users are 2.4× more likely to be repeat purchasers.  
- **Behavioral hooks:** post-purchase prompts, reorder CTAs, and visible wallet balance strongly correlate with retention.

---

## 🧭 Retention Strategy (Engage | Reward | Retain)

### 1) ENGAGE (Day 0–15)
- Welcome flow: Day0 (order thank you + product suggestions), Day3 (top categories), Day7 (discount on 2nd order).  
- One-tap reorder CTA on order success page and order history widget.

### 2) REWARD (Day 15–60)
- **UrbanPoints** loyalty program: 1 point per ₹1 spent; visible wallet on homepage & checkout.  
- Tiered rewards: Silver/Gold tiers with cashback boosters & free delivery thresholds.

### 3) RETAIN (60+ days)
- Predictive churn model (rule-based initially) to flag at-risk users for targeted reactivation.  
- Reduce refund turnaround from 5 → 2 days and give instant micro-credit for minor delivery issues.

---

## 📈 Impact Modelling (conservative projection)

| Metric | Baseline | Projected (3 months) |
|--------|---------:|---------------------:|
| D30 Retention | 31% | 48% |
| Avg LTV | ₹860 | ₹1,200 |
| Campaign ROI | 1.8x | 3.1x |

**Assumptions:** See `assumptions.md`.

---

## 🗺 Implementation Roadmap (90 days)

**Weeks 0–2:** Implement welcome & push flows; instrument dashboards for D1/D7/D30.  
**Weeks 3–6:** Launch reactivation email series; first UrbanPoints beta.  
**Weeks 7–10:** Expand loyalty to top 25% AOV users; test wallet visibility.  
**Weeks 11–12:** Deploy basic churn scoring and targeted incentives for high-LTV at-risk users.

---

## 🧩 Product & Tech Hooks (what your PM/Eng team would do)
- Integrate Firebase for push & event tracking.  
- Add “wallet balance” UI component and checkout highlight for available rewards.  
- Track events: order_completed, reorder_clicked, wallet_viewed, refund_requested.

---

## ⚠️ Risks & Mitigations
- **Over-subsidize loyalty** → Mitigation: cap early redemptions; measure incremental lift.  
- **UX confusion** → Mitigation: AB test wallet visibility & coupon messaging.  
- **Data quality** → Mitigation: instrument correct events and verify data pipelines.

---

## 👤 Reflection — Raj
> “Retention is the multiplication of small product, marketing, and operations improvements. Fix the UX frictions and your acquisition gets 2–3× more valuable.”

---

## 📁 Files included
- README.md (this file)  
- methodology.md  
- assumptions.md  
- interview-notes.md  
- EXECUTIVE_SUMMARY.md  
- ABOUT.md  
- CHANGELOG.md  
- retention_data_sample.csv  
- LICENSE
