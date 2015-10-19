# nginx-bot-honeypot
A naive approach to the illumination and filtering of bad site-crawlers using nginx.  This project provides a base configuration for adding bot handling logic to your nginx server configuration.  To accomplish this, a few things are required:

- Your robots.txt file must explicitly deny access to the honeypot page so that good bots know not to touch it.
- Your robots.txt file should explicitly specify a request throttle that matches the rate in the nginx configuration
```
User-agent: *
Disallow: /honeypot.html
Crawl-delay: 1
```
