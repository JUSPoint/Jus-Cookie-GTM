# JUS. Cookie Management (CMP) - GTM Template

Google Tag Manager custom template for [JUS.](https://www.jus.com.tr)  Consent Management Platform. Provides full Google Consent Mode v2 integration with GDPR and KVKK compliance out of the box.

## What This Template Does

- Sets default consent state to `denied` for all applicable consent types before any tags fire
- Loads the JUS. CMP SDK and displays the cookie consent banner
- Listens for user consent choices and updates Google Consent Mode accordingly
- Fires DataLayer events (`jus_consent_ready`, `jus_consent_updated`) for downstream tag triggering
- Supports regional consent defaults (EEA, Türkiye, custom country lists) with override tables

### Supported Consent Types

`ad_storage` · `ad_user_data` · `ad_personalization` · `analytics_storage` · `functionality_storage` · `personalization_storage` · `security_storage`

## Installation

1. In GTM, go to **Templates** > **Search Gallery** and find **JUS. Cookie Management (CMP)**
2. Add the template to your workspace
3. Create a new tag using this template
4. Enter your **GTM Key** (found in JUS. Dashboard under Cookie Management > Domains > Installation)
5. Set the trigger to **Consent Initialization - All Pages**
6. Save and publish

> For manual installation, import `template.tpl` via **Templates** > **New** > **Import**.

## Configuration

**GTM Key** — Your website identifier from the JUS. dashboard (UUID format).

**Default Consent** — All consent types default to `denied` for GDPR/KVKK compliance. `security_storage` defaults to `granted`.

**Region Behavior** — Choose between All Regions, EEA + Türkiye (recommended), EEA only, Türkiye only, or custom country codes.

**Advanced** — URL Passthrough, Ads Data Redaction, wait-for-update timeout, and debug logging are all configurable under advanced settings.

## Requirements

- Google Tag Manager (Web)
- A JUS. account with an active domain configuration
- Website served over HTTPS

## Support

- Documentation (English): [help.juspoint.com](https://help.juspoint.com)
- Documentation (Türkçe): [help.jus.com.tr](https://help.jus.com.tr)
- Email: support@jus.com.tr

## License

[Apache 2.0](LICENSE)
