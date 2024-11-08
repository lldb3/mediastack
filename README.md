# mediastack

Full media management stack:
- traefik reverse proxy (automatic DNS_01 challenge)
- arr-stack
- wireguard + transmission setup (credits to SebDanielsson )
- automatic updates using Watchtower with Pushover notifications

## Setup requirements

Look at the .env.example file and fillout with your own details:
- Your domain name
- For Pushover notifications, add the pushover URL and HOSTNAME variable that will appear in the notification title


The token for DNS Challenge is to be put in `/secrets/cloudflare_api_token`, so:
```shell
cd PROJECT_DIR
mkdir secrets
echo 'MY_API_KEY' > secrets/cloudflare_api_token
chmod 400 secrets/cloudflare_api_token
```

For the wireguard configuration, it's important to check out the source project's [readme.md](https://github.com/sebdanielsson/compose-transmission-wireguard/blob/main/README.md)





