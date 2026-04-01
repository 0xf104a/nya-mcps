FROM ghcr.io/0xf104a/meowmeow:2.0-alpha7

RUN apk add --no-cache \
    chromium-headless-shell \
    chromium \
    nss \
    freetype \
    harfbuzz \
    ca-certificates \
    ttf-freefont \
    nodejs \
    npm

COPY configs/meow.conf /etc/MeowMeow/meow.conf
COPY configs/routes.conf /etc/MeowMeow/routes.conf

ENV PLAYWRIGHT_SKIP_BROWSER_DOWNLOAD=1
ENV CHROMIUM_PATH=/usr/bin/chromium-browser
RUN npm install -g @playwright/mcp@v0.0.69
