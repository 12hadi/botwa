FROM node:lts-buster
RUN git clone https:github.com/SamPandey001/Zero-Two-MDgit /root/SamPandey001/
WORKDIR /root/SamPandey001/
RUN apt-get update && \
  apt-get install -y \
  ffmpeg \
  imagemagick \
  webp && \
  apt-get upgrade -y && \
  rm -rf /var/lib/apt/lists/*
RUN npm install --location=global npm@8.13.2
RUN npm install --location=global nodemon 
RUN npm --omit=dev install
RUN npm install --location=global chalk
RUN npm i cfonts
RUN npm install --location=global pm2

CMD ["pm2-runtime", "start", "franxx.js"]
