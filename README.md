# Mire Sirens

A community-maintained continuation of the Fen Light addon family for Kodi, picking up after the original Fen Light (Tikipeter, retired late 2024) and Fen Light AM (AnonyMouse, discontinued 2026) were taken down.

Mire Sirens is a clean, no-keys-included fork. You bring your own credentials.

## What's in this fork

- **Plugin id preserved**: `plugin.video.fenlight` (so existing FENtastical / Fen Light themed skins keep working)
- **Display name**: Mire Sirens
- **All previous shared API keys removed**: Trakt client/secret, TMDB key. The defaults are empty; users must register their own.
- **Updater**: points at this repo's GitHub Pages site (`isleysharleen.github.io`)
- **Auto-migration**: detects legacy keys from Tikipeter or AnonyMouse on first run and clears them with a friendly dialog

Everything else is identical to Fen Light AM v2.2.04. All scrapers, debrid integrations, Trakt/TMDB workflows, AI similar lookups, MDbList ratings, etc. work the same.

## Installation

### Easy (via the repository)

1. Add this URL as a Kodi file source: `https://isleysharleen.github.io/packages/`
2. Install `repository.miresirens-1.0.0.zip` from that source
3. Then install Mire Sirens from inside the new repository

### Manual (zip-only)

Download `plugin.video.fenlight-1.0.0.zip` and install via Kodi -> Add-ons -> Install from zip file.

## First-run setup (required)

Mire Sirens ships without API keys. You must register your own — both are free and take about two minutes each.

### TMDb API key (required for metadata, posters, browsing)

You need TWO TMDb credentials. Both are free and come from the same TMDb account.

**1. TMDb API Key (v3 auth)** — used for metadata

1. Sign up at https://www.themoviedb.org
2. Go to https://www.themoviedb.org/settings/api
3. Request a developer key (instant approval for personal use)
4. Copy the **API Key (v3 auth)** value
5. In Mire Sirens, go to Tools -> Settings -> Accounts -> TMDb -> paste the key

**2. TMDb v4 Read Access Token** — used for lists, favorites, watchlist

This is on the SAME settings page, just below the v3 API key.

1. On the same page (https://www.themoviedb.org/settings/api), find **API Read Access Token (v4 auth)**
2. Copy the long string (starts with `eyJ`)
3. The first time Mire Sirens needs it (when you authenticate your TMDb account or open a TMDb list), a popup will prompt you to paste it. Or paste it directly into Settings -> Accounts -> TMDb -> "TMDb v4 Read Access Token".

### Trakt application (required if you want Trakt sync)

1. Sign in at https://trakt.tv
2. Go to https://trakt.tv/oauth/applications -> Create new application
3. Name: anything (e.g. "Mire Sirens - <your name>")
4. Redirect URI: `urn:ietf:wg:oauth:2.0:oob`
5. Save. You'll get a **Client ID** and **Client Secret**
6. In Mire Sirens, go to Tools -> Settings -> Accounts -> Trakt -> paste both, then authorize

### Optional services (nothing needed unless you use them)

- Real Debrid / Premiumize / AllDebrid / TorBox / Easynews — link via their normal device-auth in addon settings
- Google Gemini / Groq — paste your API key in settings if you want AI similar recommendations
- OMDb / RPDb — same pattern

## License

This is a personal-use fork of Fen Light AM (itself a fork of Fen Light by Tikipeter). Distributed under the same terms.

## Acknowledgements

- **Tikipeter** — original author of Fen and Fen Light
- **AnonyMouse** — author of Fen Light AM
- **isleysharleen** — Mire Sirens fork

The Mire Sirens name is a riff on Fen Light's wetland-mythology theme, with a nod to the Gotham City Sirens.
