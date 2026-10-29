# WP Permalink Translator (HackIndex Patched)

> [!IMPORTANT]
> This is an unofficial fork of [WP Permalink Translator](https://wordpress.org/plugins/wp-permalink-translator/) by [Hossin Asaadi](https://github.com/hossinasaadi/wp-permalink-translator). HackIndex is not affiliated with or endorsed by the original author.

The original plugin is no longer maintained and its latest release (1.7.6) has a [known vulnerability](https://www.wordfence.com/threat-intel/vulnerabilities/id/b1c609fc-f719-4e2a-aaa6-80dc34025142). HackIndex maintains this fork for security fixes only:

- We fix security issues and keep the plugin working on current WordPress and PHP versions.
- We do not add features or change how the plugin works.
- It is a drop-in replacement: same plugin folder and option names, so your languages and translated permalinks are kept.

Need help with this fork? [Open an issue](https://github.com/HackIndex-io/wp-permalink-translator/issues) here, please don't contact the original author about it.

## What it does

Translates the permalink (slug) of a post to another language with Google Translate when the post is published, for example from Persian to English. Set the languages under **WP Permalink Translator** in the admin menu, where you can also translate the permalinks of existing posts.

## Security fixes

### 1.7.7

- Cross-Site Request Forgery ([CVE-2025-53274](https://www.cve.org/CVERecord?id=CVE-2025-53274), [Wordfence advisory](https://www.wordfence.com/threat-intel/vulnerabilities/id/b1c609fc-f719-4e2a-aaa6-80dc34025142)): the settings forms printed a nonce but never checked it, so a page that an administrator visited could change the languages or translate (rename) the permalinks of all posts. Both forms now verify their nonce.
- The language fields on the settings page are escaped, so a value saved through that CSRF can no longer run scripts in the admin
- Fixed `seems_utf8()` deprecation notices on WordPress 6.9 and later
- Tested with WordPress 7.1 and PHP 8.0 to 8.5

## Install

1. Download `wp-permalink-translator.zip` from the [latest release](https://github.com/HackIndex-io/wp-permalink-translator/releases/latest).
2. Deactivate and delete the original plugin. Your settings and permalinks are kept.
3. Upload the zip in **Plugins > Add New > Upload Plugin** and activate it.

WordPress does not update this fork automatically. Watch this repo's releases to get new security fixes.

## License

GPLv2 or later, like the original. See [LICENSE](LICENSE). Provided without any warranty.

All credit for the plugin goes to [Hossin Asaadi](https://github.com/hossinasaadi/wp-permalink-translator). The full upstream history is kept in this repository.
