FROM ghcr.io/ptero-eggs/yolks:nodejs_22

ENV NODE_ENV=production

ENV COREPACK_HOME=/usr/local/share/.cache/node/corepack

RUN corepack enable \
 && corepack prepare pnpm@9.15.9 --activate \
 && apt-get update \
 && apt-get install -y --no-install-recommends \
      libcairo2 \
      libpango-1.0-0 \
      libpangocairo-1.0-0 \
      libjpeg62-turbo \
      libgif7 \
      librsvg2-2 \
 && rm -rf /var/lib/apt/lists/*

WORKDIR /home/container

RUN mkdir -p storage logs
