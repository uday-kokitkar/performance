=== Performance Lab ===

Contributors:      wordpressdotorg
Requires at least: 5.8
Tested up to:      5.9
Requires PHP:      5.6
Stable tag:        1.0.0-beta.1
License:           GPLv2 or later
License URI:       https://www.gnu.org/licenses/gpl-2.0.html
Tags:              performance, images, javascript, site health, measurement, object caching

Performance plugin from the WordPress Performance Group, which is a collection of standalone performance modules.

== Description ==

The Performance Lab plugin is a collection of modules focused on enhancing performance of your site, most of which should eventually be merged into WordPress core. The plugin allows to individually enable and test the modules to get their benefits before they become available in WordPress core, and to provide feedback to further improve the solutions.

Currently the plugin includes the following performance modules:

* **WebP Uploads:** Creates WebP versions for new JPEG image uploads if supported by the server.
* **WebP Support:** Adds a WebP support check in Site Health status.
* **Persistent Object Cache Health Check:** Adds a persistent object cache check for sites with non-trivial amounts of data in Site Health status.
* **Audit Enqueued Assets:** Adds a CSS and JS resource check in Site Health status.

== Installation ==

= Installation from within WordPress =

1. Visit **Plugins > Add New**.
2. Search for **Performance Lab**.
3. Install and activate the Performance Lab plugin.

= Manual installation =

1. Upload the entire `performance-lab` folder to the `/wp-content/plugins/` directory.
2. Visit **Plugins**.
3. Activate the Performance Lab plugin.

= After activation =

1. Visit the new **Settings > Performance** menu.
2. Enable the individual modules you would like to use.

== Frequently Asked Questions ==

= What is the purpose of this plugin? =

The primary purpose of the Performance Lab plugin is to allow testing of various performance modules for which the goal is to eventually land in WordPress core. It is essentially a collection of "feature plugins", which makes it different from other performance plugins that offer performance features which are not targeted at WordPress core and potentially rely on functionality that would not be feasible to use in WordPress core. The list of available modules will regularly change: Existing modules may be removed after they have been released in WordPress core, while new modules may be added in any release.

= Can I use this plugin on my production site? =

Per the primary purpose of the plugin (see above), it can mostly be considered a beta testing plugin for the various performance modules it includes. However, unless a module is explicitly marked as "experimental", it has been tested and established to a degree where it should be okay to use in production. Still, as with every plugin, you are doing so at your own risk.

= Where can I submit my plugin feedback? =

Especially since this is a collection of WordPress core feature plugins, providing feedback is encouraged and much appreciated! You can submit your feedback either in the [plugin support forum](https://wordpress.org/support/plugin/performance-lab/) or, if you have a specific issue to report, in its [GitHub repository](https://github.com/WordPress/performance).

= How can I contribute to the plugin? =

Contributions welcome! There are several ways to contribute:

* Raise an issue or submit a pull request in the [Github repository for the plugin](https://github.com/WordPress/performance)
* Translate the plugin into your language at [translate.wordpress.org](https://translate.wordpress.org/projects/wp-plugins/performance-lab)
* Join the weekly chat (Tuesdays at 16:00 UTC) in the [#performance channel on Slack](https://wordpress.slack.com/archives/performance)

== Changelog ==

= 1.0.0-beta.1 =

**Features**

* Images: Add WebP for uploads module. ([32](https://github.com/WordPress/performance/pull/32))
* Images: Support retry mechanism for generating sub-sizes in additional MIME types on constrained environments. ([188](https://github.com/WordPress/performance/pull/188))
* Images: Update `the_content` with the appropiate image format. ([152](https://github.com/WordPress/performance/pull/152))
* Site Health: Add WebP support in site health. ([141](https://github.com/WordPress/performance/pull/141))
* Site Health: Add module to alert about excessive JS and CSS assets. ([54](https://github.com/WordPress/performance/pull/54))
* Object Cache: Add Site Health check module for persistent object cache. ([111](https://github.com/WordPress/performance/pull/111))
* Infrastructure: Add settings screen to toggle modules. ([30](https://github.com/WordPress/performance/pull/30))
* Infrastructure: Added admin pointer. ([199](https://github.com/WordPress/performance/pull/199))

**Enhancements**

* Object Cache: Always recommend object cache on multisite. ([200](https://github.com/WordPress/performance/pull/200))
* Images: Create image sub-sizes in additional MIME types using `sources` for storage. ([147](https://github.com/WordPress/performance/pull/147))
* Images: Update module directories to be within their focus directory. ([58](https://github.com/WordPress/performance/pull/58))
* Site Health: Enhance detection of enqueued frontend assets. ([136](https://github.com/WordPress/performance/pull/136))
* Infrastructure: Add link to Settings screen to the plugin's entry in plugins list table. ([197](https://github.com/WordPress/performance/pull/197))
* Infrastructure: Enable all non-experimental modules on plugin activation. ([191](https://github.com/WordPress/performance/pull/191))
* Infrastructure: Include generated module-i18n.php file in repository. ([196](https://github.com/WordPress/performance/pull/196))
* Infrastructure: Introduce `perflab_active_modules` filter to control which modules are active. ([87](https://github.com/WordPress/performance/pull/87))
* Infrastructure: Remove unnecessary question marks from checkbox labels. ([110](https://github.com/WordPress/performance/pull/110))
* Infrastructure: Rename `object-caching` to `object-cache`. ([108](https://github.com/WordPress/performance/pull/108))

**Bug Fixes**

* Images: Ensure the `-scaled` image remains in the original uploaded format. ([143](https://github.com/WordPress/performance/pull/143))
* Images: Fix typo to access to the correct image properties. ([203](https://github.com/WordPress/performance/pull/203))
* Infrastructure: Ensure that module header fields can be translated. ([60](https://github.com/WordPress/performance/pull/60))

**Documentation**

* Site Health: Mark Site Health Audit Enqueued Assets module as experimental for now. ([205](https://github.com/WordPress/performance/pull/205))
* Infrastructure: Add `readme.txt` and related update script. ([72](https://github.com/WordPress/performance/pull/72))
* Infrastructure: Add changelog generator script. ([51](https://github.com/WordPress/performance/pull/51))
* Infrastructure: Add contribution documentation. ([47](https://github.com/WordPress/performance/pull/47))
* Infrastructure: Add release documentation. ([138](https://github.com/WordPress/performance/pull/138))
* Infrastructure: Define module specification in documentation. ([26](https://github.com/WordPress/performance/pull/26))
