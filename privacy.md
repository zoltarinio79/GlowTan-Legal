---
title: Privacy Policy
---

## GlowTan Privacy Policy

Effective date: 2026-05-04

This policy describes the data behavior implemented in the current GlowTan codebase. It should replace the existing public privacy-policy copy before App Store submission.

## Summary

GlowTan stores your skin profile, saved locations, tanning history, routine overrides, and progress photos locally on your device. GlowTan also sends limited off-device data for core app functionality, purchases, weather/UV guidance, and behavior analytics.

GlowTan does not sell personal data, does not show ads, and does not use data for third-party tracking.

## Data Stored Locally On Device

GlowTan stores the following locally using SwiftData, files in the app sandbox, and UserDefaults:

- Skin and sun-safety profile answers, including skin type, goals, concerns, activity type, default SPF, and preferences.
- Saved locations selected by the user.
- Session history events, routine overrides, and weekly progress state.
- Optional progress photos and thumbnails.
- App preferences, including temperature unit, reminder preference, install date, rating-prompt timing, analytics queue, and progress-photo consent state.

Progress photos are stored locally in the app sandbox. The current code does not upload photo image data to Supabase, RevenueCat, WeatherKit, or another backend.

## Data Sent Off Device

### Weather and UV

GlowTan uses Apple WeatherKit to fetch weather and UV data. When using current location, the app sends device location coordinates to Apple WeatherKit. When using a saved location, the app sends that saved location's coordinates to Apple WeatherKit. Weather responses are cached locally for offline fallback.

### Purchases and Subscriptions

GlowTan uses Apple In-App Purchase and RevenueCat to load subscription offerings, make purchases, restore purchases, and check whether the `pro` entitlement is active. RevenueCat receives purchase and entitlement data needed to provide subscription access. GlowTan does not receive your payment card number or Apple ID.

### Behavior Analytics

GlowTan sends behavior analytics to Supabase through the `analytics-ingest` Edge Function. These events are used to understand activation, retention, engagement, monetization, safety, and product quality.

Each analytics event can include:

- Event ID.
- App-generated install ID.
- App-generated session ID.
- Event name.
- Event timestamp.
- App version.
- Build number.
- Platform, currently `ios`.
- Event properties listed below.

Analytics event properties currently sent by the app include:

- `timezone`
- `granted`
- `source`
- `linked_to_session`
- `kind`
- `total_minutes`
- `uv_bucket`
- `reason`
- `package_id`
- `plan`
- `entitlement_id`
- `completed_glows_this_week`
- `progress_photos_count`

The Supabase Edge Function accepts only the app's allowlisted analytics event names and sanitizes property keys/values. String property values are truncated server-side. The app does not send names, email addresses, phone numbers, contacts, raw location coordinates, skin questionnaire answers, or progress photo image data in analytics events.

## Data Controls

You can edit profile and preference data in the app where controls are provided. Some local data can be removed through in-app flows where deletion controls exist. You can remove all local app data by deleting GlowTan from your device.

GlowTan does not currently provide user accounts. Because there is no account sign-up, login, profile on a GlowTan server, or account identifier controlled by GlowTan, account deletion is not applicable to the current app architecture. Subscription cancellation and refund requests are handled through Apple.

## Third-Party Services

GlowTan uses:

- Apple WeatherKit for weather and UV data.
- Apple In-App Purchase for subscription payments.
- RevenueCat for subscription offerings, purchases, restores, and entitlement checks.
- Supabase for behavior analytics ingestion and storage.

## Contact

For privacy questions, contact: glowtan@ghostnoteapps.com


