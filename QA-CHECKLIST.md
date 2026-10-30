# Release QA checklist

Run on a real phone with the release candidate from the internal track or TestFlight.
Mark each item pass / fail / unsure, with a screenshot. Automated smoke flows in `.maestro/` already cover onboarding, barcode search and the add product page for a typed unknown barcode, so this list covers what an emulator cannot.

## Camera and permissions
- Fresh install: the camera permission prompt appears, and "Later" leaves the app usable.
- Grant camera access in settings, return to the app: the scanner starts without a restart.
- Scan a well-known product (e.g. Nutella 3017620422003): the product card appears within a few seconds.
- Scan a barcode that is not in the database: the "Add this product" button opens the add product page.
- On the scan screen with the camera running, press back: the app goes to the background, no black screen.

## Product page
- Nutri-Score, NOVA and Green-Score sections open and show text, not empty boxes.
- A product with no photo: adding a photo from the camera uploads and shows it.

## Account
- Log in, log out, log in again: preferences survive.

## Offline
- Airplane mode, open a product scanned earlier: it shows from the local history.
- Airplane mode, search: a clear error, no crash or endless spinner.

## Display
- Dark mode and AMOLED: no unreadable text or white flashes on home, search and product page.
- Largest system font size: no clipped buttons in onboarding and on the product page.
- One non-English language (e.g. French): no untranslated or overflowing labels on home and product page.

## This release
- Each item in the release notes: open the changed screen and check it does what the note says.
