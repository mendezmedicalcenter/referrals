# Mendez Referrals

Standalone Referrals Dashboard & Daily Log for Mendez Medical Center.

- **Single file, no build step.** Everything lives in `index.html` (HTML + CSS + vanilla JS).
- **Installable PWA** — "Add to Home Screen" via `manifest.json` + `logo.png`.
- **Offline / local.** Referrals are stored in the browser's `localStorage` (key `ref_referrals_v1`).
  No server or Google account required — the Google Apps Script backend was replaced with a
  local storage shim implementing the same API (getReferralOptions, getReferralsForDate,
  getReferralDashboard, addReferral, updateReferral, deleteReferral, searchPatients).

## Features
Dashboard overview (pending / in progress / completed / patients / total), Daily Log table with
per-employee filtering, live wait timers, status workflow (Pending -> In Progress -> Completed,
with move-back), New Referral modal with multi-specialty entry (# of referrals), insurance
type -> plan and specialty -> subspecialty dependent dropdowns, group-home flag, patient
search suggestions, edit / delete (single or whole patient group), date picker, full-screen mode, and print.

## Run
Open `index.html` in a browser, or serve the folder statically (e.g. Vercel / any static host).

> Copied from the original Mendez Referrals Apps Script app (v1.7); the UI/logic are the same,
> only the backend was swapped for local storage so it runs as one static file.