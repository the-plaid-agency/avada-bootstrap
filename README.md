# AVADA Bootstrap by THE PLAID AGENCY
This repo contains the opinionated defaults for the AVADA theme for Wordpress by THE PLAID AGENCY.

After many years of making AVADA websites, we've settled on a number of commons settings that we believe creates a good starting point for our websites.

## Create site on Pantheon

First, you will need to create a new site on Pantheon.

1. Log into Pantheon
2. In the Dashboard, click "Create New Site"
3. For the site name, always prefix the name with a prefix (usually 2-3 characters) that summarizes the organization. So for example, for a new website that belongs to THE PLAID AGENCY, a fitting name might be `tpa-sitename`. Or `plaid-sitename`. This is important so if we have multiple websites for a single organization, which is very common, they will be organized togeter on the dashboard and in filesystems.
4. Choose `THE PLAID AGENCY` as the organization.
5. Choose `Wordpress` as the CMS.
6. Click Deploy!

## Installing Wordpress

Once the site is deployed, you'll need to install Wordpress:

1. Click the `Site Admin` button in the top left of the dashboard.
2. Select `English (United States)` for the language.
3. Type in the site title.
4. Set the username to `plaidadmin`. You can use the auto-generated password, as it is usually very strong.
5. Make sure to record the login credentials in **Keeweb**!
6. Set your email.
7. You can leave the search engine visibility setting unchecked for now unless told otherwise.

## Configuring Wordpress

Now that Wordpress is installed, login to the admin dashboard:

1. Right away, go to the `Plugins` page.
2. Delete `Akismet` and `Hello Dolly`. Completely useless, I wish they wouldn't add them by default.
3. Next, go to `Appearance > Themes` and delete all Wordpress themes except for the default one (currently Twenty Ninetween).

Now, Wordpress has a clean slate and is ready for you to begin configuring it.

## Upload and Enable AVADA Theme

Next, we'll want to upload the AVADA theme.

1. Download the latest AVADA package from Themeforest.
2. Upload the theme via SFTP. You can find SFTP information in the Pantheon Dashboard under the yellow `Connect with SFTP` button. Make sure the site is in SFTP mode. You will need an SSH key added to your Pantheon account in order to connect.
3. Upload both the `Avada` and `Avada Child` theme to `/wp-content/themes/` folder.
4. Go back to `Appearance > Themes` and enable the `Avada Child` theme. Make sure you enable the **Child** theme and not the default one!
5. Now you can delete the `Twenty Nineteen` since it is no longer needed.

Okay, now we have AVADA ready to go.

## Configure the AVADA Theme

Now we'll begin setting up a clean slate for AVADA.

1. Once AVADA is enabled, you'll need to install `Fusion Core` and `Fusion Builder`. You'll see a large error message at the top of your screen unitl you install these.
2. Go to `Avada > Fusion Patcher` and click `Apply Patch` for each patch from top to bottom. Wait for the page to completely finish loading before clicking the next one.
3. Now, go to `Avada > Registration` and follow the instructions to set up an API key for the site. Make sure you set the site name on Envato as the same name for the site. So in our example above, it would be `tpa-sitename`.
4. Next, go to `Avada > Theme Options` and scroll down to `Import/Export`. You'll want to use the `Import from URL` button to import the latest `fusion_options_backup_DD-MM-YYYY.json` settings file. In order to get the URL, click the file on Github and then click the `Raw` button. This will link you directly to the file. Now, you can copy the URL of this page into the box in AVADA.
5. Click `Save Changes` to update all the settings.
6. Now, go to `Fusion Builder > Settings`.
7. Set `Fusion Builder Auto Activation` to `On`.
5. Scroll down to `Post Types` and uncheck `Post`.
9. Scroll down to `Import Fusion Builder Content`. Click `Browse` and select the `fusion_template-plaidtester.WordPress.YYYY-MM-DD.xml` file from this repo. You'll need to download this file, as there is no option to import it from a URL. Once the file is selected, click `Import`.
10. Scroll down and click `Save Settings`.

Now, AVADA should be be good to start developing! Please refer to the Best Practices guide when developing the website.

## Add Required plugins

Yay! AVADA is installed. Amazing. Now, here is a list of plugins you'll want to install:

- [Disable Gutenberg](https://wordpress.org/plugins/disable-gutenberg/)
- [Ninja Forms](https://wordpress.org/plugins/ninja-forms/)
- [Pantheon Advanced Page Cache](https://wordpress.org/plugins/pantheon-advanced-page-cache/)
- [Pantheon HUD](https://wordpress.org/plugins/pantheon-hud/)
- [Sendgrid](https://wordpress.org/plugins/sendgrid-email-delivery-simplified/)
- [Wordpress Native PHP Sessions](https://wordpress.org/plugins/wp-native-php-sessions/)
- [WP-CFM](https://wordpress.org/plugins/wp-cfm/)
- [Yoast SEO](https://wordpress.org/plugins/wordpress-seo/)
