# Super Restrictive Hosts List for AdGuard

A comprehensive hosts file designed to block distracting websites and services while preserving essential tools needed for software development.

## What This Blocks

This hosts list implements an aggressive blocking strategy targeting:

### Search Engines (ALL major ones)
- Google Search (google.com, www.google.com, etc.)
- Bing
- Yahoo
- DuckDuckGo
- Baidu
- Yandex
- Ask.com
- AOL Search
- Ecosia
- Brave Search
- Qwant

### Google Services
- **All googlevideo.com subdomains** (blocks video streaming)
- Google Play Store (play.google.com, play.googleapis.com)
- Google Maps
- Google News
- Google Shopping
- Google Scholar
- Google Trends
- Google Translate

**Exceptions (Allowed):**
- firebase.google.com (for development)
- gmail.com and its dependencies
- accounts.google.com (needed for Gmail authentication)

### Wikipedia & Educational
- All Wikipedia language variants (en, es, fr, de, etc.)
- Wikimedia Commons
- Wikidata, Wikiquote, Wiktionary, etc.
- Coursera
- Udemy
- Khan Academy

### Major News Sites
**US News:**
- CNN, New York Times, Wall Street Journal
- Washington Post, USA Today, LA Times
- Fox News, NBC News, ABC News, CBS News
- Bloomberg, Reuters, AP News
- NPR, Politico, HuffPost
- Time, Newsweek, The Atlantic, The New Yorker
- Forbes, Fortune, Business Insider
- Vice, Vox, Slate, The Hill, Axios

**UK News:**
- BBC, The Guardian, Telegraph
- The Independent, Daily Mail, Mirror
- The Sun, Express, Evening Standard
- Financial Times

**International:**
- Al Jazeera, RT, Sky News
- Euronews, France 24, Deutsche Welle
- Der Spiegel, Le Monde, El País

**Tech News:**
- TechCrunch, The Verge, Wired
- Engadget, Ars Technica, CNET
- ZDNet, Gizmodo, Mashable, VentureBeat

### Social Media (Complete Block)
- Facebook/Meta (including Messenger)
- Twitter/X
- Instagram
- TikTok
- LinkedIn
- Reddit
- Pinterest
- Snapchat
- WhatsApp Web
- Telegram Web
- Discord Web
- Tumblr
- Mastodon (major instances)
- Threads
- Twitch

### Video & Entertainment
- YouTube (via googlevideo.com blocking)
- Netflix
- Hulu
- Disney+
- Prime Video
- HBO Max
- Vimeo
- Dailymotion
- Spotify Web Player

### Shopping & E-commerce
- Amazon.com (shopping site, not AWS)
- eBay
- AliExpress
- Etsy
- Walmart
- Target

### Gaming
- Steam Store (web)
- Epic Games Store
- IGN, GameSpot, Polygon

### Other Popular Sites
- IMDb
- Quora
- Medium
- BuzzFeed
- 9gag
- Imgur
- Giphy
- ESPN and other sports sites
- Dating sites (Tinder, Bumble, Match)
- Travel booking sites (Booking.com, Airbnb, Expedia, TripAdvisor)

## Installation in AdGuard

### For AdGuard Home:
1. Open AdGuard Home admin panel
2. Go to **Filters** → **DNS blocklists**
3. Click **Add blocklist** → **Add a custom list**
4. Give it a name (e.g., "Super Restrictive Hosts")
5. Upload or paste the contents of `adguard-restrictive-hosts.txt`
6. Save and apply

### For AdGuard Browser Extension:
1. Open AdGuard extension settings
2. Go to **Filters** → **Custom**
3. Click **Add custom filter**
4. Import the `adguard-restrictive-hosts.txt` file
5. Enable the filter

### For AdGuard for Android/iOS:
1. Open AdGuard app
2. Go to **Protection** → **DNS protection**
3. Tap **DNS filtering**
4. Tap **DNS filters**
5. Tap **Add filter** → **Custom filter**
6. Import the hosts file
7. Enable the filter

## Format Compatibility

This hosts list uses the standard hosts file format:
```
127.0.0.1 domain.com
```

It also includes AdGuard-specific syntax for wildcard blocking:
```
||googlevideo.com^
```

Both formats work in AdGuard. The 127.0.0.1 format is also compatible with:
- System hosts files (/etc/hosts on Linux/macOS, C:\Windows\System32\drivers\etc\hosts on Windows)
- Pi-hole
- Most other DNS-based blocking solutions

## Important Notes

### What's NOT Blocked
This list is designed for developers, so the following are intentionally allowed:
- **GitHub** and other development platforms
- **Stack Overflow** and programming Q&A sites
- **AWS, Google Cloud, Azure** (cloud services)
- **Firebase.google.com** (for development)
- **Gmail.com** and email services
- **Documentation sites** (MDN, DevDocs, etc.)
- **Package managers** (npm, PyPI, RubyGems, etc.)

### Limitations
- Some services may still be accessible through alternative domains or IPs
- Apps may bypass hosts-based blocking using hardcoded IPs or DoH (DNS over HTTPS)
- This blocks web access but may not block native mobile apps
- VPNs and proxies can bypass these blocks

### Customization
To allow specific sites:
1. Open the `adguard-restrictive-hosts.txt` file
2. Comment out (add `#` at the beginning) or remove the lines for domains you want to allow
3. Re-import the modified file into AdGuard

Example:
```
# 127.0.0.1 reddit.com  (commented out to allow Reddit)
```

## Use Case

This hosts list is designed for:
- **Focus and productivity**: Block distractions during work/study hours
- **Digital wellbeing**: Reduce time spent on social media and news
- **Developers**: Maintain access to essential development tools while blocking everything else

## File Location

The hosts file is located at: `adguard-restrictive-hosts.txt`

## Statistics

- **Total Entries**: 570+ blocked domains
- **Categories**: 15+ major categories
- **Last Updated**: 2026-01-13

## Contributing

If you find sites that should be added to this restrictive list, feel free to suggest them. The goal is to block anything not strictly necessary for software development work.

## License

This hosts list follows the same license as the main repository (Apache 2.0).

## Disclaimer

This is an extremely restrictive hosts list that blocks most of the internet. Use at your own discretion and modify as needed for your specific requirements.
