FROM tgagor/gemini-cli:v0.45@sha256:8523945cd03885973abdb90fa9bf6232c523add8a5c6a6386b87a07e441f4a4e

RUN apk add --no-cache python3 py3-pip build-base git npm && \
    git clone https://github.com/cruzyjapan/Gemini-CLI-UI.git && \
    cd Gemini-CLI-UI && \
    npm install && \
    cp .env.example .env && \
    mkdir /share && \
    npm run dev

LABEL \
  org.opencontainers.image.title="Home Assistant Gemini CLI" \
  org.opencontainers.image.description="Runs Gemini CLI within your Home Assistant setup providing remote development vid web-interface" \
  org.opencontainers.image.source="https://github.com/crazyrokr/ha-gemini-cli" \
  org.opencontainers.image.licenses="GNU General Public License 3.0"
