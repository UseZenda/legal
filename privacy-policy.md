---
layout: default
title: Privacy Policy
---

# Zenda Privacy Policy

**Version 1.0 — Effective 2 July 2026**

Zenda is a fitness and nutrition coaching app. Because coaching only works with an
honest picture of your body, your training, and your habits, Zenda processes data
that is deeply personal — including health data and body photos. This policy
explains exactly what we collect, why, where it goes, how long it lives, and the
rights you have over it. We have tried to write it so you can actually read it.

## 1. Who is responsible for your data

The data controller is:

**Zenda** — operated by Tauro Labs
Contact: **taurolabs@gmail.com**

If you have any question, request, or complaint about your data, email us. We
respond to data-rights requests within one month, as the GDPR requires.

## 2. What we collect

### Account data
- Email address and authentication credentials (managed by Supabase Auth).
- Name and nickname, if you provide them.

### Onboarding and profile data
When you set up Zenda you answer questions about yourself so the coach can build
your plan. This includes: age, gender, country, height, weight, target weight,
primary and secondary goals, training experience and preferences, available
equipment, dietary pattern, **allergies and intolerances**, foods you avoid,
**medical conditions**, **injuries and pain areas**, typical sleep, stress level,
timezone, and your preferred check-in day and language.

### Health and fitness data (Apple Health)
With your permission, Zenda reads from Apple Health: steps, sleep, water intake,
body weight, workouts, and the nutrition you log (calories, protein, carbohydrates,
fat). Zenda also writes back to Apple Health the weight and meals you log in the
app, so your records stay in one place.

Apple Health data is read on your device. Slices of it are sent to our servers only
for the specific features described in section 4 (for example, the 7-day metric
series inside a weekly check-in). We never use Apple Health data for advertising or
marketing, and we never sell it — this is both our promise and an Apple platform
requirement.

### Progress photos
If you choose to take progress photos (front/side/back), two copies exist:

1. **An encrypted copy for you.** Photos are encrypted on your device with
   AES-256-GCM before upload. The encryption key is generated on your device and
   stored only in your iCloud Keychain — it is never sent to us. We store only
   ciphertext we cannot read. This copy is what you see in the app, on any of your
   devices, and it stays until you delete it or your account.
2. **A temporary unencrypted copy for AI analysis.** So the AI coach can assess
   your progress, an unencrypted copy is uploaded to a private bucket, analysed,
   kept until your *next* check-in uses it for a side-by-side comparison, and then
   deleted. Any photo never consumed by a following check-in is automatically
   deleted within 30 days.

### AI-generated content
The plans, weekly reports, baseline assessments, coach notes, and macro estimates
generated for you are stored in your account so the app can display them.

### Technical data
- Device push-notification tokens (so we can tell you when your plan or report is
  ready).
- IP address, used transiently for rate limiting (abuse prevention). Rate-limit
  counters are deleted within 24 hours.
- We do **not** use analytics SDKs, advertising identifiers, or tracking of any
  kind.

## 3. Special-category data and your explicit consent

Health data — your weight, medical conditions, injuries, nutrition, sleep, workouts,
and body photos — is "special category" data under Article 9 of the GDPR. We process
it only with your **explicit consent**, which we ask for when you start using Zenda
(and again if this policy materially changes).

You can withdraw consent at any time by deleting your account in Settings, or by
emailing us. Because the entire service is built on this data, withdrawing consent
means Zenda can no longer coach you — but withdrawal is always available, and
deletion is immediate and complete (section 7).

## 4. Why we process your data (purposes and legal bases)

| Purpose | Data used | Legal basis |
|---|---|---|
| Creating and securing your account | Account data | Contract (Art. 6(1)(b)) |
| Building your training, nutrition, and target plan | Profile + onboarding data, baseline photos | Explicit consent (Art. 9(2)(a)) |
| Daily coaching (dashboard, coach notes, meal estimates) | Health metrics, meals, workouts, profile | Explicit consent (Art. 9(2)(a)) |
| Weekly check-ins and progress reports | Weekly metrics, weight, photos, your comments | Explicit consent (Art. 9(2)(a)) |
| Showing you your own progress photos | Encrypted photos | Explicit consent (Art. 9(2)(a)) |
| Push notifications about your plan/report | Device token | Contract (Art. 6(1)(b)) |
| Rate limiting and abuse prevention | IP address, request counters | Legitimate interest (Art. 6(1)(f)) — keeping the service available and our AI costs bounded |
| Complying with legal obligations | Whatever the obligation requires | Legal obligation (Art. 6(1)(c)) |

## 5. AI processing — what actually happens

Zenda's coaching is generated by Claude, an AI model operated by **Anthropic, PBC**
(USA). When a feature needs the AI, we send it the relevant slice of your data:

- **Plan generation:** your onboarding profile and an exercise catalogue.
- **Baseline (Day 0) analysis:** your baseline photos, profile, and plan context.
- **Weekly reports:** your week's metrics, weight, comments, and this week's +
  last week's photos.
- **Daily coach notes:** a compact summary of recent training and habits.
- **Meal estimates:** the meal description you type.

Anthropic processes this data as our processor to generate the response and does
not use it to train its models. AI output is advisory coaching content — it never
produces legal or similarly significant automated decisions about you (Art. 22).
A human (us) is reachable at any time via the contact address above.

AI content can be wrong. Calorie and macro estimates are approximations. Always
apply your own judgement, especially around allergies and medical conditions — see
the Health Disclaimer.

## 6. Who receives your data (processors)

We share your data only with the processors needed to run Zenda, under data
processing agreements:

| Processor | Role | Location |
|---|---|---|
| **Supabase, Inc.** | Backend: database, authentication, file storage, serverless functions | Cloud infrastructure (project region), USA-headquartered |
| **Anthropic, PBC** | AI model (Claude) for coaching content | USA |
| **Apple, Inc.** | Push-notification delivery (APNs); iCloud Keychain (your photo key, on your devices) | USA/global |

Where data leaves the EEA, transfers rely on the EU–US Data Privacy Framework
(where the recipient is certified) and/or Standard Contractual Clauses.

We never sell your data. We never share it with advertisers. There are no other
recipients unless the law compels us.

## 7. How long we keep things (retention)

| Data | Retention |
|---|---|
| Unencrypted photos for AI analysis | Until your next check-in consumes them (then deleted), never more than 30 days |
| Encrypted progress photos | Until you delete them or your account |
| AI job queue records | Deleted within 24 hours of completion |
| Check-in input snapshots | Deleted within 24 hours of the report being produced |
| Coach notes | Deleted after 90 days |
| Weekly report long-form text | Compacted after 90 days (headline data kept) |
| IP rate-limit counters | Deleted within 24 hours |
| Superseded plans/baselines | Deleted daily (only the newest is kept) |
| Account, profile, reports, workouts, consents | Until you delete your account |

**Account deletion is real deletion.** Settings → Delete Account removes your
storage files (photos, encrypted and not), every database row about you, and your
authentication record — immediately, not a soft delete.

## 8. Your rights

Under the GDPR you can:

- **Access / port** — Settings → Export My Data gives you a machine-readable JSON
  file of everything we hold about you (Art. 15, 20).
- **Rectify** — edit your profile, goals, and preferences in Settings (Art. 16).
- **Erase** — Settings → Delete Account, or email us (Art. 17).
- **Withdraw consent** — at any time, without affecting prior processing (Art. 7(3)).
- **Restrict or object** — email us (Art. 18, 21).
- **Complain** — to a supervisory authority. Our lead authority is the Irish
  Data Protection Commission (www.dataprotection.ie); you may also complain to
  the authority of your own country.

Exercising rights is free. We may ask you to verify your identity.

If you are outside the EU/EEA, we apply the same standards to your data, and local
law may grant you similar rights (for example under UK GDPR or applicable US state
privacy laws) — the contact route is the same.

## 9. Children

Zenda is not for children. You must be at least **16 years old** to use Zenda. We
do not knowingly process data of anyone under 16; if we learn we have, we will
delete it.

## 10. Security

- Body photos: client-side AES-256-GCM encryption; the key never leaves your
  iCloud Keychain.
- All traffic uses TLS. Database access is protected by row-level security so each
  account can only ever read its own rows.
- Temporary AI photo copies live in a private bucket, are consumed and deleted on
  a strict schedule, and are never publicly accessible.
- AI prompts wrap your text in a data-only frame to prevent it being interpreted
  as instructions.

No system is perfectly secure; if a breach affects your rights, we will notify you
and the supervisory authority as the GDPR requires.

## 11. Changes to this policy

If we change this policy in a way that matters, the app will ask you to review and
re-accept it before continuing, and material changes to what we do with health data
will always require fresh explicit consent. The version and date at the top tell
you what you agreed to.

## 12. Contact

**taurolabs@gmail.com** — data-protection questions, rights requests, complaints,
or anything unclear in this policy.
