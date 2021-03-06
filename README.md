```
  ________________      ________                      
 /_  __/ ____/ __ \_  _/_  __/ /_  ___  ____ ___  ___ 
  / / / __/ / / / / |/_// / / __ \/ _ \/ __ `__ \/ _ \
 / / / /___/ /_/ />  < / / / / / /  __/ / / / / /  __/
/_/ /_____/_____/_/|_|/_/ /_/ /_/\___/_/ /_/ /_/\___/ 
                                                      
```

# TEDxTheme

This theme has been designed and coded by [The Working Group](http://twg.ca) and [TEDxToronto](http://www.tedxtoronto.com) and modified by [Alex Justesen](http://alexjustesen.com) in the hopes that other TEDx organizations will find this easy to use to promote and manage their own events.

### Requirements

#### Server
* **PHP** v5.2.4 or greater
* **MySQL** (or any MariaDB version) v5.0.15 or greater
* **Apache** mod_rewrite module enabled

#### Software
* **WordPress** v4.8 or greater
* **Advanced Custom Fields** WordPress plugin
* **Option Tree** WordPress plugin

### Installation (Production)
* Download the latest theme release [TEDx Theme](https://github.com/alexjustesen/TEDxSpringfieldTheme/releases)
* Set the Permalink Settings to customer structure `/blog/%postname%/`

### Installation (Developers)
* Clone/fork or download the latest repo zip from (https://github.com/alexjustesen/TEDxSpringfieldTheme) and install it to `./wp-content/themes/`.
* Run using bash command line in the theme folder `npm install` then `bower install` to install builder dependencies
* Run `gulp` or `gulp default` to build the theme files
* Set the Permalink Settings to customer structure `/blog/%postname%/`


### Development
We've done our best to setup an efficient workflow using [Gulp.js](http://gulpjs.com/) and [Bower](http://bower.io/). You'll need to have `npm` installed before getting started. Development requires an understanding of the following commands:

* `npm install` - Install development dependencies.
* `bower install` - Install packages to `./vendor` directory.
* `gulp default` - Is the default Gulp function that compiles and moves all the site assets to the `./dist` directory.
* `gulp clean` - Cleans out the build and dist folders.
* `gulp zip` - Packages the WordPress Theme zip file. !IMPORTANT make sure to run `gulp default` first to build the `./dist` directory.


### Change Log

#### v1.3.0 (Jan 17, 2018)
- Released v1.3.0

#### v1.3.0-rc1 (Dec 18, 2017)
- `page_templates/template_home.php`
  * Removed banner container, support for acf will come in v2.0

#### v1.3.0-beta2 (Dec 13, 2017)
- `includes/admin/plugin_dependencies.php`
  * removed hardcoded link
- `includes/controls/textarea_custom_control.php`
  * removed php short tags
- `includes/theme_support.php`
  * added automatic feed links theme support
- `includes/theme/enqueue_scripts.php`
  * updated versions to 1.3.0-beta2
- `header.php`
  * moved navbar container to outside the wp_nav_menu function
  * removed php short tags
  * renamed navbar container id
  * wrapped urls in esc_url to sanitize the values
- `footer.php`
  * removed php short tags
  * replaced copywrite tag with html equivalent

#### v1.3.0-beta (Dec 12, 2017)
- `assets/js/application.js`
  * removed cta slideDown function
  * removed navbar viewport function
- `assets/scss/application.scss`
  * created new cta style classes
  * removed unused css code
  * updated hex code values to use color palette variables
- `assets/scss/initializers/_bootstrap_override.scss`
  * updated styles to reflect tedx color palette
- `includes/theme_setup.php`
  * added cta button target options
  * added cta enable checkbox
  * added logo customizer default image
  * changed cta text customizer input field to textarea type
  * changed event date customizer input field to date type
  * moved cta options to its own customizer section
- `partials/_call_to_action.php`
  * created file with cta code from `header.php`
  * made coding improvements
  * updated cta UI
- `header.php`
  * added brand to navbar for xs and sm screens
  * added icon to date text
  * added icon to location text
  * cleaned up .navbar code
  * fixed issue with event date code error
  * moved cta code to `partials/_call_to_action.php`
  * removed ng-app reference, angularjs not used
  * to include cta, code now looks tedx_cta_enable = "1"
- `style.css`
  * added core wordpress styles
  * added text domain
  * updated to v1.3.0

#### v1.2.0 (Nov 1, 2017)
- Released v1.2.0
- Minor UI updates for blog sticky posts

#### v1.2.0-rc1 (Oct 23, 2017)
- Minor UI updates for `talk_shortcode.php`
- Minor UI updates for `footer.php`

#### v1.2.0-beta2 (Oct 17, 2017)
- Added bootstrap navbar border-radius override
- Added `comments.php` to make theme compliant with theme standards
- Fixed undefined variable error in `single-talk.php` with `get_excerpt` function
- Moved `tedx_helpers.php` to includes root
- Removed `.video-container` class in favor of the defaul bootstrap responsive embed class

#### v1.2.0-beta (Oct 2, 2017)
- Added matchHeight JS library
- Added matchHeight function to fix alighnment issues on the team page where a col height was different
- Cleaned up js code contained in `application.js`
- Fixed issue where blank custom post values for team custom post would not save
- Removed unused code from `application.scss`
- Removed unused code from `application.js`

#### v1.2.0-alpha (Sept 27, 2017)
- Added team categories
- Added team cateogry support to the shortcode
- Minor UI changes to the navbar
- Minor wording changes and link updates to the footer
- Updated team member shortcode template to the new design

#### v1.1.0 (Sept 18, 2017)
- Fixed an issue with the `save_custom_fields` function causing a undefined index error

#### v1.1.0-beta2 (Sept 18, 2017)
- Fixed issue with header cta logic
- Removed js console outputs

#### v1.1.0-beta (Sept 17, 2017)
- Fixed issue with header cta text/button still showing when blank

#### v1.1.0-alpha3 (Sept 4, 2017)
- Improved: Scroll up buttons speed
- Improved: Installation instructions in `readme.md`
- Removed: text-decoration from `.scrollup` css class

#### v1.1.0-alpha2 (Sept 1, 2017)
- Added: `responsive-toolkit` package to assist with viewport changes
- Removed: logo link option in the customizer, was replaced with the home_url() wordpress function
- Update: header UI and implemented responsive-toolkit js function to change navbar position on <=sm viewport devices

#### v1.1.0-alpha (Aug 29, 2017)
- Added: `dollarshaveclub/shave` package to bower for text truncation
- New: Video card design for featured/past talks
- New: Header design to include social links for Facebook, Instagram and Twitter
- New: Created a new call to action in the header
- New: Navigation bar and menu walker
- New: Search form
- New: Implemented `shave()` js function to truncate text where needed
- New: Speaker profile
- Fixed: `.gitirnore` to exclude the `./vendor` directory
- Fixed: `gulp images` function to move all images for frontend and admin
- Fixed: `gulp clean`, was referencing an invalid directory
- Fixed: `gulp fonts`, was missing reference to Bootstrap fonts
- Fixed: logo anchor to use `home_url()` instead of a custom function
- Fixed: js scrollup function
- Fixed: Speaker custom post meta not saving blank values
- Removed: DNS prefetch from `header.php` in favor of using a plugin
- Removed: Facebook and Twitter share buttons from speaker profiles, recommend using a plugin instead
- Removed: Twitter button and widget JS from `footer.php`
- Removed: Facebook sdk from `header.php`
- Removed: WP customize option for twitter button code
- Removed: Support for AngularJS
- Removed: Selective menu walker
- Removed: `gulp watch` function
- Removed: `gulp package` function, use `gulp zip` instead
- Updated: `.gitignore` to exclude the `./vendor` directory
- Updated: jQuery package to v3.2.1
- Updated: `screenshot.png` to `screenshot.jpg` to reduce theme package size
- Updated: `footer.php` UI and added reference to GitHub repo for download

#### v1.0.2 (Oct 3, 2016)
- Corrected the team member placeholder in `includes/custom_post_types/team.php`
- Corrected the text at the bottom of `footer.php` to meet the TEDx guidelines
- Removed link to the legal notice in `footer.php`

#### v1.0.1 (Sept 30, 2016)
- Removed reference to http protocol in `shortcode_templates/talk_shortcode.php` to support http and https
- Updated `screenshot.png` to match current theme preview

#### v1.0.0 (Sept 23, 2016)
- Forked from TEDxTheme and renamed to TEDxSpringfieldTheme
- Removed TWG and Jet Cooper images from `footer.php`
- Added Built by 'Alex Justesen' to `footer.php`
- Removed banner text and button from `page_templates/template_home.php`
- Removed speaker video preview from `shortcode_templates/speaker_card_shortcode.php`
- Removed related speaker video preview from `sidebar-speaker.php`
- Removed http protocol from YouTube preview image from `shortcode_templates/talk_shortcode.php` to support http and https protocols