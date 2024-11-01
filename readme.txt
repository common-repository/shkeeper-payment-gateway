=== SHKeeper Payment Gateway ===
Plugin Name: Shkeeper Payment Gateway
Plugin URI: https://github.com/vsys-host/wp-shkeeper-plugin
Description: Crypto payments gateway to accept the payment on your woocommerce store.
Contributors: shkeeper
Tags: woocommerce, payment, gateway, shkeeper
Author: Virtual Systems
Author URI: https://vsys.host/
License: GPLv3
License URI: https://www.gnu.org/licenses/gpl-3.0.en.html
Stable tag: 1.1.0
Requires PHP: 7.4
Requires at least: 5.0
Tested up to: 6.6
WC requires at least: 5.7
WC tested up to: 9.3
Text Domain: shkeeper-payments-gateway
Domain Path: /languages

== Description ==

Shkeeper payment gateway plugin for CMS WordPress + WooCommerce. SHKeeper — is a self-hosted and open-source cryptocurrency payment processor. The unique combination of gateway and merchant. It allows you to accept payments in multiple cryptocurrencies without fees and intermediaries.

*Plugin has been tested on CMS WordPress 6.6 + WooCommerce 9.3

== Changelog ==

= 1.1.0 =
* Removed deprecated QR code generation library
* Added multiply transactions to an order
* Partial order status has been added
* Small fixes

== Frequently Asked Questions ==

= Fix WooCommerce There Are No Payment Methods Available Error =

When you install a new WooCommerce website, blocks is enabled by default. This will cause most payment methods to stop working showing the message: “There are no payment methods available. This may be an error on our side. Please contact us if you need any help placing your order“.

Fixing this issue is very easy:

* You need to install the classic editor plugin
* Edit your checkout page
* Replace all contents with this shortcode
`[woocommerce_checkout]`

= Demo test credentials =
You can use our demo SHKeeper installation to test module with your Magento 2. SHKeeper demo version working in a Testnet network, do not use it for real payments.
SHKeeper demo version is available from us, so you can try it yourself without installing it:

[SHKeeper demo](https://demo.shkeeper.io/)

**Login:** admin
**Password:** admin  

**SHKeeper API URL:**  ```https://demo.shkeeper.io/api/v1/```
**SHKeeper API Key:** Actual should be taken from demo.shkeeper.io  ```Wallets``` -> ```Manage```. API Key can be taken from the any of available Wallets.

## Installation
### Upload via WordPress Admin

Download Shkeeper plugin as a zip file to your PC.
To upload Shkeeper plugin, log in to your WordPress dashboard.
1. Navigate to Plugins > Add New.
2. Click the Upload Plugin button at the top of the screen.
3. Select the shkeeper.zip file from your local filesystem.
4. Click the Install Now button.
5. When the installation is complete, you’ll see “Plugin installed successfully.” Click the Activate Plugin button.
   
Detailed instruction can be found official WordPress [site](https://wordpress.org/support/article/managing-plugins/#upload-via-wordpress-admin)
### Manual Plugin Installation

In rare cases, you may need to install a plugin by manually transferring the files onto the server. This is recommended only when absolutely necessary, for example when your server is not configured to allow automatic installations.

This procedure requires you to be familiar with the process of transferring files using an SFTP client. It is recommended for advanced users and developers.

Detailed instructions can be found on official WordPress [site](https://wordpress.org/support/article/managing-plugins)


## Configuration

After successful installation you should configure plugin.

1. Go to `WooCommerce > Settings > Payments` and enable Shkeeper.
2. Click on Set up and configure the payment method. You will get the Shkeeper settings to be set.
3. Here, enable the Shkeeper and then enter the api key, api url and instructions with description for your customers, etc..
   * Enable/Disable – Disable the same to turn off and Enable the same to use.
   * Api key - Authorization and identification Shkeeper key. You can generate it in Shkeeper admin panel for any crypto wallet.
   * Api url - Shkeeper server api entry point. 
   * Title – The title to display to the customers on the Checkout page.
   * Description – The details to be shown to the customers, when they choose the Shkeeper option.
   * Instruction – Contains the explanation on how to pay by Shkeeper.
   * Enable for shipping methods - You can choose what shipping methods supports Shkeeper payments.
   * Accept for virtual orders - Disable or enable Skeeper for WooCommerce virtual orders.
   * Logging - Disable or enable Shkeeper plugin logging of communication with Shkeeper Api server.
4. Once done save the changes..
