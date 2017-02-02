# Squid Proxy

[Squid](http://www.squid-cache.org/) is a caching and forwarding HTTP web proxy. It has a wide variety of uses, from speeding up a web server by caching repeated requests; to caching web, DNS and other computer network lookups for a group of people sharing network resources, to aiding security by filtering traffic. Although primarily used for HTTP and FTP, Squid includes limited support for several other protocols including TLS, SSL, Internet Gopher and HTTPS.

## Basic config

The Squid blueprint is set up to provide a proxy server with basic auth by default.

| Config Key  | Description                                    | Default    |
|-------------|------------------------------------------------|------------|
| squid.port  | The port the proxy will be launched on         | 3128       |
| username    | The usernamed used by basicauth                | squid-user |
| password    | The password used by basicauth                 | C!0uDsfT   |
| settingsURL | A URL to a settings file to replace the default|            |

The key `settingsURL` can be used to override the default `squid.conf`. Note that if this is done however, the default config is not carried out and squid.port, username and password are ignored.

## Configuring a browser

To use the proxy server for a web browser follow the instructions provided by your browser, such as [firefox](https://support.mozilla.org/en-US/kb/advanced-panel-settings-in-firefox).

In linux run `export http_proxy=<proxy URL>` where proxy url is the address and port of your squid server.