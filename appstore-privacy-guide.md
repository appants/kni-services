# App Store Connect — Data & Privacy Disclosure Guide
## Fifteen — Picture Puzzle

This document tells you exactly what to select in App Store Connect under
**App Privacy → Data Types**.

---

## Privacy Policy URL

Enter this in App Store Connect → App Information → Privacy Policy URL:

```
https://www.kni-services.com/privacy-policy
```

(Upload the privacy-policy.html file to that path on your server first.)

---

## App Store Connect — Data Types Checklist

Go to: App Store Connect → Your App → App Privacy → Get Started (or Edit)

Answer the question "Does this app collect data?" → **YES**

---

### ✅ DATA YOU DO COLLECT (select these)

#### 1. Identifiers
- **Device ID**
  - Used for: Analytics
  - Linked to identity: **No**
  - Used for tracking: **No**

#### 2. Usage Data
- **App Interactions** (taps, game events, feature usage)
  - Used for: Analytics
  - Linked to identity: **No**
  - Used for tracking: **No**

- **Other Usage Data** (moves count, time to solve, game completions)
  - Used for: Analytics, App Functionality
  - Linked to identity: **No**
  - Used for tracking: **No**

#### 3. Diagnostics
- **Crash Data**
  - Used for: App Functionality (error tracking)
  - Linked to identity: **No**
  - Used for tracking: **No**

---

### ❌ DATA YOU DO NOT COLLECT (leave these unchecked)

- Contact Info (name, email, phone, address)
- Health & Fitness
- Financial Info
- Location (precise or coarse)
- Sensitive Info
- Contacts
- User Content — Photos ← **important: photos never leave the device**
- Browsing History
- Search History
- Purchases (until RevenueCat is added)

---

## Nutrition Label Preview

After filling in the above, your App Privacy card on the App Store will show:

```
Data Not Linked to You
  • Identifiers
  • Usage Data
  • Diagnostics
```

There will be NO "Data Used to Track You" section because you are
not using any advertising networks or cross-app tracking.

---

## When You Add RevenueCat (v2.0)

You will need to add these additional data types at that point:

- **Purchase History** → Linked to identity: No → Used for: App Functionality
- If RevenueCat links to a user account: change "Linked to identity" to YES

Update both the privacy policy (Section 5, add RevenueCat) and the
App Store disclosure at the same time as the IAP submission.

---

## Google Play (Data Safety Section)

When you submit to Google Play, fill in the Data Safety section as follows:

**Does your app collect or share any of the required user data types?** → YES

| Data type        | Collected | Shared | Required | Encrypted | Delete option |
|-----------------|-----------|--------|----------|-----------|---------------|
| Device ID        | Yes       | No     | No       | Yes       | No            |
| App interactions | Yes       | No     | No       | Yes       | No            |
| App info & perf  | Yes       | No     | No       | Yes       | No            |

**Is all collected data transmitted securely?** → YES
**Do you provide a way for users to request data deletion?** → NO
  (acceptable since no PII is collected — note this in your store description)

---

## Checklist Before Submitting

- [ ] Upload privacy-policy.html to https://www.kni-services.com/privacy-policy
- [ ] Verify the page loads on mobile (Apple will check this)
- [ ] Enter the URL in App Store Connect → App Information → Privacy Policy URL
- [ ] Complete the Data Types section in App Store Connect → App Privacy
- [ ] Submit with your next build
