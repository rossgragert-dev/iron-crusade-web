# Iron Crusade — Public iPhone Web App

This public repository hosts only the **playable PWA release** of Iron Crusade. The editable source and in-development Alpha.10 remain in the **private** [iron-crusade](https://github.com/rossgragert-dev/iron-crusade) repository.

**Current approved release:** Alpha.9e.  
**Planned public URL after deployment:** https://rossgragert-dev.github.io/iron-crusade-web/

## Publish the first release from an iPhone

1. Download the **Iron_Crusade_Alpha9e_PWA_GitHubPages.zip** from the ChatGPT conversation.
2. In the iPhone Files app, rename the downloaded file to exactly **iron-crusade-pwa.zip** (retain the .zip extension).
3. In this repository on GitHub, choose **Add file → Upload files**, select the ZIP, and commit to `main`. Do not extract the ZIP when uploading.
4. In repository **Settings → Pages → Build and deployment**, select **Source: GitHub Actions**.
5. Open the **Actions** tab and select **Publish Iron Crusade PWA**. If a successful run hasn't started automatically, use **Run workflow** on branch `main`.
6. Open the public GitHub Pages URL shown on the Pages settings screen.

The deployment workflow validates and extracts the ZIP, then publishes its contents under the GitHub Pages project path. It doesn't upload our private source code.

## Install on iPhone and prepare offline mode

1. Open **https://rossgragert-dev.github.io/iron-crusade-web/offline-setup.html** in Safari.
2. Use Safari **Share → Add to Home Screen** and choose **Open as Web App** when offered.
3. Open the installed Home Screen icon. **Inside the installed app**, select **Prepare for offline play**. Wait for the **Ready** confirmation.
4. Select **Launch Game**, load each model once online if necessary, then test with Airplane Mode.

iPhone Safari and Home Screen installations can have separate storage. Offline support is best-effort: iOS may evict cached assets under storage pressure. Re-download the offline pack after each release.

## Future releases

Replace `iron-crusade-pwa.zip` in `main` and commit the change. GitHub Actions redeploys the public game. Change the service-worker cache version for each new release. Keep the previous ZIP available for rollback.

Do **not** delete the live Cloudflare deployment until the GitHub Pages version has passed iPhone online and offline tests.

## Isolated Alpha.10 preview (without changing the installed game)

The primary game at the repository root stays on approved **Alpha.9e**.

To test Claude's revised **Alpha.10** on iPhone:

1. Download `iron-crusade-alpha10-preview.zip` from the ChatGPT handoff.
2. Open this repository → **Add file → Upload files**, choose the ZIP, and commit to `main` (do not rename or unzip).
3. GitHub Actions checks the ZIP and publishes a separate online preview.
4. Open **https://rossgragert-dev.github.io/iron-crusade-web/preview/alpha10/** in Safari.
5. Compare city graphics, plasma/bolter/lascannon and missile impacts, audio, enemy animations and camera views.

**Important:** Alpha.10 preview is online-only until approved. Do not replace `iron-crusade-pwa.zip`, do not uninstall the Alpha.9e Home Screen app, and don't delete the Cloudflare fallback yet. The approved Alpha.9e game and offline cache remain unchanged.

## Avalon Warframes experimental RPG preview

The experimental **Alpha.10.1** build lives alongside (not over) the approved Alpha.9e Home Screen PWA and Alpha.10 preview.

1. Download the playable ZIP from ChatGPT and rename it **avalon-warframes-alpha101-preview.zip**.
2. Upload that ZIP to this public repository's `main` branch (do not unzip).
3. GitHub Actions verifies and publishes the preview at: https://rossgragert-dev.github.io/iron-crusade-web/preview/avalon-alpha101/
4. Test multi-touch camera switching while moving, five-second steerable boost, weapons and audio, pilot XP saving and skill upgrades.

This is a test build **not** a public original-IP Avalon RPG release. Its inherited 40K-inspired models are retained only for internal QA until original Avalon armor and weapon assets are created. Do not use the production PWA icon to install this unapproved preview.


## Avalon Warframes Alpha.11c environmental test preview

Alpha.11c is an experimental **online-only** graphical update; it does not replace the approved Alpha.9e PWA.

1. Download `avalon-warframes-alpha11c-preview.zip` from the ChatGPT conversation.
2. In this public repository choose **Add file → Upload files** and upload the ZIP to the root of `main` with its filename unchanged. **Do not unzip**.
3. The existing **Publish Iron Crusade PWA** GitHub Action validates and extracts it into an isolated preview path.
4. Open **https://rossgragert-dev.github.io/iron-crusade-web/preview/avalon-alpha11c/** on your phone in Safari. For runtime stats use `?qa=1`.

The approved Alpha.9e Home Screen app, Alpha.10 preview, and Alpha.10.1 preview are retained. Real iPhone FPS and touch tests are still pending.

## Avalon Alpha.11b Audio Fidelity on Alpha.11d graphics

This is an **isolated audio-only test preview** built on Alpha.11d graphics and gameplay. The ZIP must be named **exactly** `avalon-warframes-alpha11d-audio11b-preview.zip`; don't accept a duplicate `(1)` filename. Upload the unextracted ZIP to the root of `main` with **Add file → Upload files**. The Pages workflow automatically verifies 55 original WAV samples and publishes the test at:

https://rossgragert-dev.github.io/iron-crusade-web/preview/avalon-alpha11d-audio11b/

On iPhone, test sound through a 120-second battle (bolters, missiles, explosions, booster, footfalls), mute/unmute, rotate and resume after tab/phone interruption. Audio sampling checks were run; real iPhone listening and performance approval remain pending. Production Alpha.9e and previous previews remain unchanged.
