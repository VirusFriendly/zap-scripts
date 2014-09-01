Zap-Scripts
===========


zapWin.ps1 and zapOSX.sh
These scripts copy the config.xml and ZAP scripts to the default locations where zap should be. I hate having to look up these locations, so I just script them cause I'm lazy :)

config.xml
Mainly contains new "Passive Scan Rules." These are different than "Passive Rules." Passive Scan Rules tag http responses to help quickly isolate json files, javascript, dart (is this even used in the wild?), and websockets. You can also ignore responses with security measures such as NoMimeSniff, Anti-Clickjacking and XSS protections so you don't waste time on such pages.

SwitchyOptions.bak
This file has nothing to do with ZAP, but is used for SwitchySharp extension for Chrome (zomg, I'm not using firefox, such a sin! :P). Chrome goes nuts when going to anything Google through an SSL proxy, so I save all the google excludes here.

ZAP Scripts/Passive Rules
Cloudflare.zst, Rack.zst, Stingray.zst
These passive rules trigger an informational alert on the presence of caching proxies. This is useful in understanding the depth of the architecture (Identifying Cloud applications or potentially insecure relays).
