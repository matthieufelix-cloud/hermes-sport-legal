# HERMES Sport Platform legal pages

Static legal-information site for the private HERMES Sport Platform HUAWEI Health Service Kit test
integration. The site contains no JavaScript, analytics, cookies, forms, application credentials, or
personal sport data.

The distinct French page at `mobile/privacy/` covers the Android HERMES Sport companion and its
isolated AppGallery review instance. Keep it aligned with the shipped APK and review-server retention.

## Review before publication

The operator identity, public contact address, country, and governing law have been customized.
The app name must remain exactly `HERMES Sport Platform`, including capitalization. Review the text
against the actual deployment and do not publish claims that are not operationally true.

Check that no placeholder remains:

```powershell
rg "REPLACE_WITH_" --glob "*.html" .
```

The command must return no match before publication or submission to HUAWEI.

## Publish with GitHub Pages

1. Create a new **public** GitHub repository named `hermes-sport-legal`. Do not use the private
   application repository.
2. Commit this directory as the root of the new repository and push its `main` branch.
3. In GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Select branch `main`, folder `/ (root)`, and save.
6. Wait for GitHub Pages to report the public URL, then test all three pages in a private browser
   window.

For the GitHub account `matthieufelix-cloud` and the repository name above, the expected fields are:

- Privacy policy: `https://matthieufelix-cloud.github.io/hermes-sport-legal/privacy/`
- Android privacy policy: `https://matthieufelix-cloud.github.io/hermes-sport-legal/mobile/privacy/`
- User agreement: `https://matthieufelix-cloud.github.io/hermes-sport-legal/terms/`

Do not enter these URLs in HUAWEI until GitHub Pages returns HTTP 200 and the publication reminder
has disappeared from both documents.
