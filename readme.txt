=== WP Permalink Translator (HackIndex Patched) ===
Contributors: hossin277, joshuavanderpoll
Tags: Permalink Translator, Translator, Permalink
Requires at least: 4.0
Tested up to: 7.1
Stable tag: 1.7.7
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html
Donate link: https://www.buymeacoffee.com/4epLAXRYo

Translate Permalink to another languages. (HackIndex Patched)

== Description ==

= HackIndex Patched fork =
This is an unofficial fork of WP Permalink Translator by Hossin Asaadi. The original plugin is no longer maintained and its latest release (1.7.6) has a [known vulnerability](https://www.wordfence.com/threat-intel/vulnerabilities/id/b1c609fc-f719-4e2a-aaa6-80dc34025142). HackIndex maintains this fork for security fixes only.

* We fix security issues and keep the plugin working on current WordPress and PHP versions. We do not add features or change how the plugin works.
* It is a drop-in replacement: same plugin folder and settings, so your languages and translated permalinks are kept.
* HackIndex is not affiliated with or endorsed by Hossin Asaadi. Please do not contact the original author for support with this fork, open an issue on the fork instead.
* Original plugin: [WordPress.org](https://wordpress.org/plugins/wp-permalink-translator/) and [GitHub](https://github.com/hossinasaadi/wp-permalink-translator) by Hossin Asaadi.
* HackIndex fork and issues: [github.com/HackIndex-io/wp-permalink-translator](https://github.com/HackIndex-io/wp-permalink-translator)
* Licensed under the GPLv2 or later, like the original, and provided without any warranty.

Allow admins to translate Permalink to another languages.

Development
[https://github.com/hossinasaadi/wp-permalink-translator/](https://github.com/hossinasaadi/wp-permalink-translator/ "https://github.com/hossinasaadi/wp-permalink-translator")


== Installation ==

* Download and install using the built in WordPress plugin installer.
* Activate in the "Plugins" area of your admin by clicking the "Activate" link.
* click on WP Permalink Translator menu and change language as you want.


== Changelog ==

= 1.7.7 =
* Security: fixed Cross-Site Request Forgery ([CVE-2025-53274](https://www.cve.org/CVERecord?id=CVE-2025-53274), [Wordfence advisory](https://www.wordfence.com/threat-intel/vulnerabilities/id/b1c609fc-f719-4e2a-aaa6-80dc34025142)) that let an attacker change the languages or translate all post permalinks by tricking an administrator into visiting a page. Both forms now verify their nonce.
* Security: escaped the language fields on the settings page, so a value saved through that CSRF can no longer run scripts in the admin
* Fixed "seems_utf8() is deprecated" notices on WordPress 6.9 and later
* Tested with WordPress 7.1 and PHP 8.0 to 8.5

= 1.7.6 =
* fix some bugs.

= 1.7.5 =
* added tool to translate all posts at once.

 
== Upgrade Notice ==

= 1.7.5 =
Upgrade to more tools.

= 1.7 =
* fix some bugs.

 
== Upgrade Notice ==

= 1.7 =
Upgrade to fix some Bugs.