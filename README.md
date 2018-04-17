    NOTE: This repository is used for various tests.
    The official repository: https://github.com/robiso/wondercms
# WonderCMS 2.4.2 <sup>5 <sup>files,</sup> 13<sup>KB zip</sup></sup>

[![Docs](https://img.shields.io/readthedocs/pip/stable.svg?longCache=true&style=for-the-badge&v=100)](https://github.com/robiso/wondercms/wiki#wondercms-documentation) [![Number of downloads since first release on GitHub](https://img.shields.io/github/downloads/robiso/wondercms/total.svg?longCache=true&style=for-the-badge)](https://github.com/robiso/wondercms/releases) ![Maintaned](https://img.shields.io/maintenance/yes/2018.svg?longCache=true&style=for-the-badge) [![License](https://img.shields.io/github/license/mashape/apistatus.svg?longCache=true&style=for-the-badge)](https://github.com/robiso/wondercms/blob/master/license)  [![PayPal donate](https://img.shields.io/badge/Donate-PayPal-green.svg?longCache=true&style=for-the-badge)](https://paypal.me/WonderCMS)

## One of the smallest and most simple CMS
Fast, responsive, single user flat file CMS built with PHP and jQuery. Alive and kicking since 2008.

- **No configuration needed.**
- Runs on less than [50 functions](https://github.com/robiso/wondercms/wiki/List-of-all-functions) and a couple hundred lines of code.
- 5 file structure: [database.js](https://github.com/robiso/wondercms/wiki/Default-database.js#default-databasejs) (JSON format), [index.php](https://github.com/robiso/wondercms/blob/master/index.php), [theme.php](https://github.com/robiso/wondercms/blob/master/themes/default/theme.php), [style.css](https://github.com/robiso/wondercms/blob/master/themes/default/css/style.css) and [htaccess](https://github.com/robiso/wondercms/blob/master/.htaccess).
- Supports plugins ([hooks/listeners](https://github.com/robiso/wondercms/wiki/List-of-hooks)), [themes](https://github.com/robiso/wondercms/wiki/Create-theme-in-8-easy-steps), [backups](https://github.com/robiso/wondercms/wiki/Backup-all-files), [1 click updates](https://github.com/robiso/wondercms/wiki/One-click-update).
- Project goal: keep it simple, tiny, hassle free (infrequent-ish 1 click updates).

## <sup>[Demo](https://www.wondercms.com/demo) • [Download](https://www.wondercms.com/latest) • [Community](https://www.wondercms.com/community) • [Themes](https://www.wondercms.com/themes) • [Plugins](https://www.wondercms.com/plugins) • [News](https://www.wondercms.com/whatsnew) • [Donate](https://www.wondercms.com/patron) or [become a patron](https://www.wondercms.com/patron)

## 1 step install
- Unzip and upload to server.

OR clone from GitHub (via terminal): https://github.com/robiso/wondercms.git

## Requirements
WonderCMS works on most Apache servers/hosts (even free ones) by default.
- PHP 5.5. or greater
  - cURL extension
  - mbstring extension
  - Zip extension
- mod_rewrite module

One additional step is required for setting up WonderCMS on [NGINX](https://github.com/robiso/wondercms/wiki/NGINX-server-config) or [IIS](https://github.com/robiso/wondercms/wiki/IIS-server-config).

## Libraries used (6)
Libraries are loaded from Content Delivery Networks (CDNs) and include [SRI tags](https://github.com/robiso/wondercms/wiki/Add-SRI-tags-to-your-theme-libraries#3-steps-for-more-security).
- 3 libraries located in theme.php, always included:
  - <sup>jquery.min.js (1.12.4), bootstrap.min.js (3.3.7), bootstrap.min.css (3.3.7).</sup>
- 3 libraries located in index.php, included only when logged in:
  - <sup>autosize.min.js (4.0.0), taboverride.min.js (4.0.3), jquery.taboverride.min.js (4.0.0).</sup>

## Security features
- Track free, WonderCMS doesn't track users or store any cookies. Your WonderCMS installation is completely detached from WonderCMS servers. The one click updates are pushed from GitHub.
- Supports HTTPS out of the box.
  - [Check how to enable a permanent redirect on Apache or NGINX](https://github.com/robiso/wondercms/wiki/Always-redirect-to-https-and-www).
- All CSS and JS libraries include SubResource Integrity (SRI) tags. This prevents any changes to the libraries being loaded. If any changes are made, the libraries won't load for your and your visitors protection.
  - [Check how to add SRI tags to your custom theme](https://github.com/robiso/wondercms/wiki/Add-SRI-tags-to-your-theme-libraries#sri-subresource-integrity---3-steps-for-more-security). This step isn't necessary if you're using a theme from the official website.
- WonderCMS encourages you to change your default login URL. **Consider the custom login URL as your private username**.
  - Choosing a good login URL can prevent brute force attacks.
  - WonderCMS returns a 404 status on the login page, so search engines *shouldn't* visit/cache the login URL.
- The admin password is hashed using PHP's password_hash and password_verify functions.
  - Even if an attacker guesses your login URL (which should be difficult if you've chosen a good login URL), choosing a strong password prevents them from gaining admin privileges.
- WonderCMS includes CSRF verification tokens for action verification's. It additionally uses the hash_equals function to prevent CSRF token timing attacks.
- Transparent: downloads/updates are sent through GitHub (and not WonderCMS) servers.
- No known vulnerabilities.
   - Special thanks to yassineaddi, hypnito and other security researchers.

## Other features
 - no configuration required, unzip and upload
 - simple inline click and edit functionality
 - theme and plugin installer/updater
 - 1 click update and backup
 - [easy to theme](https://github.com/robiso/wondercms/wiki/Create-theme-in-8-easy-steps)
 - file uploader
 - lightweight
 - responsive
 - clean URLs
 - custom homepage
 - menu reordering and visibility
   - hiding a page from the menu doesn't hide the page for search engines
 - highlighted current page in menu
 - custom 404 page
 - basic SEO support
   - custom title, keywords and description for each page
 - [optional] functions.php file for loading your custom code
   - includes itself when you create it
   - the location of functions.php file should be inside the current active theme folder (same location as theme.php)

## List of donors and patrons
Also listed on the official [WonderCMS website](https://www.wondercms.com/donors).
- Martin Jablonka
- Veselin Kamenarov
- Håkon Wium Lie (creator of CSS)
- Kenneth Rasmussen
- David G.
- Victor Onofrei
- Matthew
- James Campbell
- Kirsten Hogan
- Denis Volin
- Jonathan Jacks
- Bizibul
- Bikespain
- Aleksandr

## What to (or not to) expect from WonderCMS
- WonderCMS is meant to be a small gift to the internet and a simple alternative to website creating. It's 100% free and doesn't not include any "powered by" links.
- WonderCMS doesn't track users and is not interested in any user data.
- WonderCMS is not a fast-pace development project. Unless there is a critical vulnerability, there is no point in rushing updates.
- WonderCMS is meant to be extremely simple and will not be over-bloated with features.
  - Specific features are added only if the majority of the WonderCMS community signals a wanted change.
  - Note: pull requests are welcome and appreciated.
- To make WonderCMS sustainable and compact, I will support a maximum of 25 plugins and 25 themes.
  - Once this "25 limit" is reached in each category, a simple voting system will be established. Users will be free to vote for their favorite plugins and themes to ensure they stay in the "chosen 25" pool. Votes will be held on a 6-month basis/twice per year (subject to change).
  - The voting system comes in handy when users feel one of the 25 plugins or themes can be replaced by a better one with similar functionality or when a plugin/theme is no longer actively maintained.
  - This is a good way to ensure a small but good quality set of themes/plugins. The "25 chosen ones" of each category will be easier to maintain and watch over by the whole community.
    - If there's enough support from WonderCMS users in the future, I can lift the "25" limit and fully dedicate to maintaining this project.
- WonderCMS doesn't include an "auto-update" feature.
  - In the unlikely event of this GitHub account being compromised, hackers would be able to deploy updates to all sites simultaneously.
  - These type of malicious attacks are currently prevented with the built in one click updater. This minimizes possible damage as users are encouraged to review code before using the 1 click update, so no damage is done automatically.
- If you run into any issues when using WonderCMS, you can always expect someone to *try* to help you in the [WonderCMS community](https://www.wondercms.com/community).
  - Since WonderCMS is completely free and noone is paid to provide support, it's important to remain patient and respectful while asking for help.

## Links
#### Website links
- [Official website](https://www.wondercms.com)
- [News/Changelog](https://www.wondercms.com/whatsnew)
- [Community](https://www.wondercms.com/community)
- [Donate](https://www.wondercms.com/donate)
- [Donors and patrons Hall of Fame](https://www.wondercms.com/donors)
- [List of contributors](https://www.wondercms.com/special-contributors)
- [All WonderCMS related links](https://www.wondercms.com/links)

#### Social links
- [Twitter](https://twitter.com/wondercms)
- [Reddit](https://reddit.com/r/WonderCMS)

#### Github links
- [Docs](https://github.com/robiso/wondercms/wiki#wondercms-documentation)
   - [Common questions](https://github.com/robiso/wondercms/wiki#common-questions--help)
   - [List of common errors](https://github.com/robiso/wondercms/wiki/List-of-common-errors#troubleshooting-common-errors)
- [Themes](https://github.com/robiso/wondercms-themes)
- [Plugins](https://github.com/robiso/wondercms-plugins)

#### Hosting and install tutorial links
- [Hosting with WonderCMS pre-installed](https://www.wondercms.com/hosting)
- [Install via cPanel - video tutorial](https://www.youtube.com/watch?v=5tykBmKAUkA&feature=youtu.be&t=25)
- [Deploy on Microsoft Azure](https://azure.microsoft.com/en-gb/try/app-service/web/wondercms/?Language=php&Step=template) ([2 minute Azure video tutorial](https://channel9.msdn.com/Blogs/Open/A-PHP-CMS-in-the-cloud-no-signup-needed-in-2-minutes))</sup>
