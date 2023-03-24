# Mullvad-with-custom-DNS
Send your internet traffic trough a private VPN while using the Power of NextDNS or other solutions for ultimate privacy!

[I use this video of TechLore as inspiration](https://www.youtube.com/watch?v=xIXG3cFT6O4).

## Regular situation

Your ISP sees all the internet traffic you access and also manages the DNS. This is extremely privacy-intrusive and does not support Adblocking.

## Benefit of VPNs 
- Your ISP can't scan your internet usage
- Outside sites don't know where you are (Yes you too Github!)
- You can use public Wifis without security issues
- Noone sees you connect to Tor or other "services of interest"

## Benefits of custom DNS
- Your network requests will less likely used to track you
- You can get rid of all AdBlockers if you DNS filters all these ads
- No App, not even your Operating System can track you, as you can block any connection you want
- Never again setup UBlock, AdGuard etc. on all devices
- Get privacy on iOS, Windows, Stock OEM Android and other toxic Operating systems, anywhere you want

# Setup for Linux
1. Install the Mullvad App
- Download the [RPM](https://mullvad.net/download/app/rpm/latest/) or the [DEB](https://mullvad.net/download/app/deb/latest/) here
- Install, login, setup all GUI configs, enable autostart
- Enable the systemd services

```
sudo systemctl enable mullvad-daemon
sudo systemctl enable mullvad-early-boot-blocking
```

2. Setup custom DNS
```
mullvad dns set custom DNS-NAME
```

# Setup for Android
1. Install [the App from F-Droid](https://f-droid.org/en/packages/net.mullvad.mullvadvpn)
2. Set all the GUI settings
3. Go to Settings->Internet->VPN and enable "always on VPN" and "block connections without VPN"
4. Go back to Internet->Private DNS and enter the hostname of your server

