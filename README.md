# chromeos-esteid
ChromeOS support for EstEID 

As per
https://laptrinhx.com/smart-card-connector-app-for-chrome-os-661174347/


The middleware Apps are written based on the PC/SC API provided by the Connector App.
The actual features implemented by the Apps may vary, but the typical example would be to read the certificates stored on the smart card, inject them into the browser's network stack (using the chrome.certificateProvider Chrome API) and proxy digest signing operations occurring during TLS handshake phase to the smart card.


So we utiliye
https://github.com/GoogleChromeLabs/chromeos_smart_card_connector/blob/master/docs/connector-app-api.md
to access certs on card and
https://developer.chrome.com/extensions/certificateProvider
to provide certs to Chrome
