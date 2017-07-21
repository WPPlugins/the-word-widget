=== The Word Widget ===
Contributors: HSteeb
Tags: bible, bibel, losung, devotional, verse of the day, votd, daily, täglich, sidebar, widget, An Bíobla Naofa, Bibelen, Bibel für Schwoba, Biblia Tysiąclecia, Bybel in Afrikaans, Chinese Union Version, English Standard Version, Hoffnung für Alle, Jubiläums-Bibel, Karoli, Kutsal Kitap, Leonberger Bibel, Neue Evangelistische Übersetzung, Modern Hebrew, New Arabic Version, Ketab el Hayat, Neue Evangelistische Übersetzung, Nuova Riveduta, O‘zbek tilidagi Muqaddas Kitob, Reina-Valera, Schlachter, Segond, Thai Holy Bible, Urdu Geo Version

Requires at least: not known
Tested up to: 4.8
Stable tag: trunk
License: GPLv2 or later
License URI: https://www.gnu.org/licenses/gpl-2.0.html

Shows two Bible sayings per day: "The Word" by project Bible 2.0, available in ca. 20 languages, got remotely for each day

== Description ==

The plugin provides a widget which you can place into one of the widget areas provided by your theme (in the WordPress admin area: Appearance | Widgets).

The widget configuration retrieves the list of available Bible editions of the current year remotely from <https://bible2.net> and lets you select one Bible edition. On each day, the widget retrieves the two sayings for the day from bible2.net and displays them.

### Project Bible 2.0

Project [Bible 2.0](https://bible2.net/) collects cross-references between selected Bible verses, formats the verses nicely and publishes two cross-referenced verses ("sayings") for each day of the year in ca. 20 languages, available for free download and as a remote service.

### Bible Editions Available

Dated 2017-06-03 - for up-to-date information, see <https://bible2.net/download/bible-editions-available/>.

For **2017**, The Word is available in the following Bible editions and languages:

* An Bíobla Naofa 1981 (Gaeilge Irish ga)
* Bibel für Schwoba (Schwäbisch Swabian swg)
* Bibelen (Dansk Danish da)
* Biblia Tysiąclecia (Polski Polish pl)
* Bybel in Afrikaans (1983-vertaling) (Afrikaans af)
* Chinese Union Version (Simplified Chinese) (简体字 Simplified Chinese zh-Hans)
* Chinese Union Version (Traditional Chinese) (繁體字 Traditional Chinese zh-Hant) 
* English Standard Version (English en)
* Hoffnung für Alle (Deutsch German de)
* Jubiläums-Bibel (русский Russian ru)
* Karoli 1990 (Magyar Hungarian hu)
* Kutsal Kitap 2001 (Türkçe Turkish tr)
* Leonberger Bibel (Deutsch German de)
* Neue Evangelistische Übersetzung (Deutsch German de)
* Modern Hebrew 2004 (עברית Hebrew he)
* New Arabic Version (Ketab el Hayat) (العَرَبِيةُ‎Arabic ar)
* Nuova Riveduta 1994 (Italiano Italian it)
* O‘zbek tilidagi Muqaddas Kitob (2012) Cyrillic (Oʻzbekcha Usbek (Cyrillic) uz-Cyrl)
* O‘zbek tilidagi Muqaddas Kitob (2012) Latin (Oʻzbekcha Usbek (Latin) uz-Latn)
* Reina-Valera 1995 (Español Spanish es)
* Schlachter 2000 (Deutsch German de)
* Segond 21 (Français French fr)
* Thai Holy Bible 1971 (ภาษาไทย Thai th)
* Urdu Geo Version (اُردُو Urdu ur)

Not / no more available:

* Almeida Revista E Atualizada (Português Portuguese pt) (the license for the Bible text terminated 2017-03-16, see <https://bible2.net/2017/03/portuguese-almeida-revista-e-atualizada-permission-terminated/>)
* Farsi
* Kiswahili Contemporary Version 2006
* Romanian
* Zimbrisch

### System Requirements

* PHP: tested with 5.3.10, 5.5.9, 5.6, 7.0
* SimpleXML: the widget needs the "SimpleXML" PHP library. If it is not available, the widget configuration (see "Appearance | Widgets" in the Installation chapter) will show an error message. For PHP 5.6, the commands `sudo apt-get install php5.6-xml` and `service apache2 restart` may help (use `php7.0-xml` for PHP 7.0).

### Adapting the Layout 

The widget output uses the following CSS classes which you may adapt in your stylesheet (CSS):

* TheWord
* TL
* Parol
* IL
* L
* SL
	
An example css file is included in the plugin zip file. It includes CSS to either show the verses with line breaks (on a wider display) or without the line breaks (on a smaller display). You may need to adapt the rules, depending on the actual width of your widget area.

### Plugin License

The WordPress plugin is licensed under GPLv2 or later.

### License for Bible Texts (got remotely per day)

The license conditions for the Bible texts (verses) are defined by the publisher of the respective Bible edition. They are contained in the .twd XML files, and are also shown in <https://bible2.net/copyright/>.

### License for Related Bible References (got remotely per day)

The project Bible 2.0 provides pairs of related Bible references.

The Word associates one pair of Bible references with a certain day, respectively.

The association of Bible references into pairs and of such pairs to days of a certain year is subject to

| Licence "Creative Commons 2.0
| <https://creativecommons.org/licenses/by-nc-nd/2.0/>
| (Attribution, Noncommercial, No Derivative Works).

With each publication, the following statement with a link to <https://bible2.net> must be available for the user (e.g. by adding a link to the copyright page):

  Association of Bible references by project Bible 2.0


== Installation ==

1. unpack the zip file into your WordPress plugin folder `/wp-content/plugins/`;
2. in the WordPress admin area, in Plugins | Installed Plugins, activate the plugin;
3. in the WordPress admin area, in Appearance | Widgets, put the widget "The Word" into one of your widget areas;
4. in the widget area, in "The Word" widget, select a Bible edition, press the "Save" button.

== Screenshots ==

1. The widget configuration
2. The widget in a wider widget area (line breaks preserved)
3. The widget in a small widget area (no line breaks)

== Changelog ==

= 0.7 =
* use https protocol to access bible2.net
* tested up to WordPress 4.8

= 0.6 =
* if the SimpleXML module is missing, the widget configuration form shows a detailed info.

= 0.5 =
* if the widget form (for admin) fails to retrieve the list of Bible editions from bible2.net, the form shows a detailed log of its actions, and some environment info (`allow_url_fopen`, `php_version()`, `$wp_version`, `$required_php_version`).

= 0.4 =
* on restricted server configurations,
* the plugin now falls back to a safer method to retrieve data from bible2.net
* (if PHP setting allow_url_fopen=Off, simplexml_load_file fails,
*  then the plugin uses the WordPress method wg_remote_get)

= 0.3 =
* the widget does not store a .twd file per year but uses the daily online service

= 0.2 =
* the widget form (for admin) retrieves the list of Bible editions from bible2.net,
* ... lets admin select the Bible edition
* ... and retrieves The Word .twd file for the selected Bible edition from bible2.net.
* the widget shows The Word from the Bible edition selected in the widget form.

= 0.1 =
* initial version

== Upgrade Notice ==
