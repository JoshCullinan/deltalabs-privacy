---
title: DeltaLab Privacy Policy
---
<!-- DRAFT — have this reviewed before publishing; not legal advice. -->

# DeltaLab Privacy Policy

**Effective date: 7 July 2026**
**Last updated: 7 July 2026**

*DeltaLab is currently in TestFlight beta. This policy applies to the beta and to any future release. It may be revised as the app develops; the "last updated" date above always reflects the current version.*

## In short

DeltaLab is a convenience client for the National Health Laboratory Service (NHLS) TrakCare lab-results portal, built for South African doctors. You sign in with your **own** NHLS portal credentials, and the app fetches lab results directly from the NHLS portal to your device over HTTPS.

There is **no DeltaLab server**. We do not run a backend that receives, stores, or processes your login or any patient data. Patient results flow only between your device and NHLS — exactly as they would if you opened the NHLS portal in a web browser. We (the developer) never see them.

We collect almost nothing. There are no analytics, no tracking, no advertising, and no crash-reporting SDKs in the app.

## Who we are

DeltaLab is developed by Joshua Cullinan.

For any privacy question or request, contact: **joshcull1@gmail.com**.

## What the app does

DeltaLab presents a native search-and-results interface over the NHLS TrakCare portal. When you sign in, the app authenticates to NHLS on your behalf using the credentials you entered and requests patient lab results, episodes, and PDF reports directly from NHLS. Your access, and everything you can see, is exactly what your own NHLS account already permits.

## What we collect

**We do not operate a server and do not collect your personal information on any server we control.** Almost everything the app handles stays on your device.

The only information that ever leaves your device is:

- **Your NHLS credentials — sent only to NHLS, to log you in.** They are transmitted directly to the NHLS portal over HTTPS to authenticate you. They are not sent anywhere else, and never to the developer.
- **Patient lab data — exchanged only between your device and NHLS.** Requested from and returned by the NHLS portal over HTTPS. It does not pass through any developer-controlled system.
- **Subscription and update metadata — sent to Apple, RevenueCat, and Expo** (the third parties described below), to run the subscription and to deliver app updates. This does **not** include your name, email, NHLS credentials, or any patient data.

## What stays on your device

To make the app usable, some data is stored locally on your device. **None of it is transmitted to the developer or to any server we control.** All of it relies on your device's operating-system disk encryption.

- **NHLS credentials.** Your username, password, and portal URL are stored on-device only, in the iOS Keychain (via `expo-secure-store`). They are used solely to authenticate to NHLS and are never uploaded to us. Your login session cookie is held in memory only and is discarded when the app is terminated.
- **Recently viewed patients.** When you open a patient from search results, a "Recently viewed" entry is cached on-device so you can quickly return to a recent look-up.
- **Cached results and timelines.** Lab results and multi-episode timelines you have viewed may be cached on-device to speed up re-opening them.
- **PDF report cache (48 hours).** Lab-report PDFs you open are cached on-device and automatically deleted after 48 hours.
- **Theme and app settings.** Your display preferences are stored locally.
- **Diagnostic test-name list.** To help improve how the app recognises lab tests, the app keeps a local list of lab **test-name labels** it has encountered (for example the names of panels and analytes), together with counts. This list contains **no patient identifiers, no result values, and no medical-record numbers.** It is stored only on your device and is never sent anywhere automatically — it can only be exported by you, manually, via the iOS share sheet if you choose to send it to the developer to help with debugging.

Because these caches contain patient information, you should protect your device with a passcode/biometrics and treat it the way you would treat any device you use to view patient records.

### Deleting on-device data

You are in control of the on-device caches:

- **Recent tab → "Clear all"** removes all recently viewed patients and their cached results/timelines.
- **Settings → "Clear recent views"** does the same.
- **Long-press a recent entry → "Remove"** deletes a single entry.
- **Settings → "Clear all data & Logout"** clears your stored credentials and signs you out.
- The **PDF cache clears itself** automatically after 48 hours.
- Deleting the app removes all locally stored data.

## Third parties involved

DeltaLab relies on a small number of third parties. Each receives only what it needs for its specific function, and none of them receives patient data.

- **NHLS (National Health Laboratory Service).** The source of all lab data. When you sign in, the app talks directly to the NHLS TrakCare portal using your credentials. Your use of NHLS is governed by NHLS's own terms and privacy practices and by your professional access arrangements with them.
- **Apple.** DeltaLab is distributed through Apple (currently via TestFlight). If you subscribe, **Apple processes the payment** and manages the auto-renewable subscription. The developer never receives your card or payment details. Apple's handling of your data is governed by [Apple's Privacy Policy](https://www.apple.com/legal/privacy/).
- **RevenueCat.** We use RevenueCat (the `react-native-purchases` SDK) to manage the Apple subscription and verify entitlement. RevenueCat receives an **anonymous app-user identifier**, along with **purchase/transaction history and receipt data** relayed from Apple. It does **not** receive your name, email, NHLS credentials, or any patient data. See [RevenueCat's Privacy Policy](https://www.revenuecat.com/privacy/).
- **Expo (EAS Update).** App updates are delivered over-the-air via Expo's EAS Update service. To fetch the correct update, the update client may transmit basic, **non-identifying** device and runtime metadata (such as app version, runtime version, and platform) to Expo's servers. No patient data or credentials are involved. See [Expo's Privacy Explained](https://expo.dev/privacy).

## Subscriptions and payment

DeltaLab offers an auto-renewable subscription, sold and billed by **Apple** through your Apple ID. Payment is handled entirely by Apple; we never see your payment method. Subscription status is checked via RevenueCat as described above.

You can view, manage, or cancel your subscription at any time in your Apple ID settings: **Settings → [your name] → Subscriptions** on your device, or at [apps.apple.com/account/subscriptions](https://apps.apple.com/account/subscriptions). Cancellation and refund handling follow Apple's standard terms; the developer cannot cancel or refund an Apple subscription on your behalf.

## How patient data is handled, and who is responsible (POPIA)

This section matters and is written plainly.

Patient lab results are **special personal information** under South Africa's Protection of Personal Information Act, 2013 (POPIA). In the context of DeltaLab:

- The patient data is **processed by you, the clinician, in your professional capacity**, using your own NHLS access — the same access you would use in a web browser. DeltaLab is simply a different window onto the records you are already authorised to view.
- **The developer is not a processor of that patient data.** We do not receive it, store it on any server, or process it on your behalf. It travels only between your device and NHLS. The on-device caches described above sit on **your** device, under your control.
- **You remain responsible for your own professional and POPIA obligations** when viewing, storing, or otherwise handling patient information on your device — for example, keeping your device secure, only accessing records you are entitled to see, and complying with your employer's and NHLS's information-governance rules. Using DeltaLab does not change or reduce those responsibilities.

Where the app does touch your **own** personal information (your NHLS credentials, subscription identifiers), we aim to process it lawfully and minimally, consistent with POPIA — in practice, by keeping credentials on-device and sharing only the minimum described above with Apple, RevenueCat, and Expo.

## Data retention

- **On-device credentials** are retained until you clear them (Settings → "Clear all data & Logout") or delete the app.
- **Recently viewed patients, cached results, and timelines** are retained until you clear them, or until the app evicts older entries to stay within its cache limits.
- **Cached PDF reports** are retained for a maximum of 48 hours, then automatically deleted.
- **The developer retains none of the above**, because none of it is transmitted to us.
- **Apple, RevenueCat, and Expo** retain the subscription/update data they receive according to their own retention policies (linked above).

## Your rights

Because the developer does not hold your personal information on any server, there is generally nothing for us to retrieve, correct, or delete on our side — you can delete on-device data yourself using the controls above.

For the personal information held by third parties:

- **Patient records:** direct requests to NHLS, the data custodian.
- **Subscription/payment data:** exercise your rights through Apple and RevenueCat.
- **Update metadata:** exercise your rights through Expo.

Under POPIA you have rights to access and correct your personal information, to object to processing in certain circumstances, and to lodge a complaint with the Information Regulator of South Africa (inforeg@justice.gov.za). If you have any question about how DeltaLab handles data, email us first at **joshcull1@gmail.com** and we will help point you to the right place.

## Security

- NHLS credentials are stored in the **iOS Keychain**, the operating system's protected credential store.
- On-device caches rely on **iOS device disk encryption**; protect your device with a passcode and biometrics.
- All communication with NHLS, and with the third-party services above, is over **HTTPS**.
- The session cookie is kept **in memory only** and discarded when the app terminates.

No method of storage or transmission is perfectly secure, but we have designed the app so that the developer never becomes a holder of your sensitive data in the first place.

## Children

DeltaLab is a professional tool for healthcare practitioners. It is **not directed at children** and is not intended for use by anyone under 18. We do not knowingly collect personal information from children. (Note that a clinician may legitimately view the lab records of paediatric *patients* through their NHLS access — that data is handled as described in the POPIA section above and never reaches the developer.)

## Changes to this policy

We may update this policy as the app evolves. When we do, we will change the "last updated" date at the top, and — for material changes — surface a notice in the app or via TestFlight release notes. Continued use after an update means you accept the revised policy.

## Contact

Questions, concerns, or privacy requests:

**Joshua Cullinan** — **joshcull1@gmail.com**
