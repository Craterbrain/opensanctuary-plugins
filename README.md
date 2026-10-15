# OpenSanctuary plugins

Plugins for [OpenSanctuary](https://github.com/Craterbrain/opensanctuary), as source code.

| Plugin | What it does |
|---|---|
| `genius_lyrics` | Search Genius and import lyrics as song slides |
| `online_bibles` | Download public-domain Bible translations, look up passages online |
| `ytdlp` | Download video or audio (yt-dlp, installed and verified by the app) into the Media library |
| `stock_media` | Search free stock photos (Pexels and Pixabay) and add them as backgrounds |
| `sandbox_demo` | A small template: shows the schedule size, Previous/Next buttons, a ribbon button |
| `hello_world` | The smallest console-script plugin (legacy form, kept as a reference) |

## Status

This repository holds the **code only**. There are no packages or releases yet, and the plugins are not signed.

The same plugins also ship inside the OpenSanctuary app (`web/plugins/`), which is where the app's tests run them. This repository is a copy; the two are not synced automatically, so a change made in one has to be made in the other.

## Using one

Each folder under `plugins/` is a sandboxed plugin: `plugin.json` (what it asks for), an entry page, and its scripts. The pages load the app's SDK (`__os/sdk.js`) and theme, which the app serves to every plugin, so they are not in this repository.

To try one: zip the folder's contents (`cd plugins/stock_media && zip -r ../../stock_media.zip .`) and use **Settings → Plugins → Install plugin…** in OpenSanctuary. It stays off until you review and approve what it asks for.

To check a plugin before installing it: `os-next --check-plugin plugins/stock_media`.

Writing your own: see `docs/PLUGINS.md` and `docs/PLUGIN_PERMISSIONS.md` in the main repository.

## License

MIT, same as OpenSanctuary.
