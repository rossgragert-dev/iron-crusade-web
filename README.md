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
