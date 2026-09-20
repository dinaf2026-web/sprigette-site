# sprigette-site

The public pages for **Sprigette**, an offline Android plant identifier published by
Northbourne Health LLC. Served by GitHub Pages so the Play Console listing has a
reachable privacy-policy URL.

- `index.html` — what the app is
- `privacy.html` — the privacy policy
- `terms.html` — terms of use

## Do not hand-edit these files

Every page here is **generated**. The sources live in the app repository:

| Page | Built from |
|---|---|
| `privacy.html` | `docs/privacy-policy.md` |
| `terms.html` | `onb_terms_body` in `app/src/main/res/values/strings_onboarding.xml` |
| `index.html` | a template inside the generator |

The generator is `tools/site/build_site.py` in the app repository. Change the source,
re-run the generator, and copy the output here. Editing a page directly creates a second
copy of the policy that will drift away from the one shipped inside the app — which has
already happened twice.

`app/src/main/assets/legal/privacy-policy.md` is asserted byte-identical to
`docs/privacy-policy.md` by a test, so the policy on this site and the policy in the app
are the same document.

`_headers` is a Netlify/Cloudflare directive file kept so this folder matches the
generator's output exactly. **GitHub Pages does not read it**, so the headers it declares
are not applied here.
