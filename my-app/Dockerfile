FROM node:20
WORKDIR /testapp
COPY package*.json ./
RUN apt-get update && apt-get install -y \
    build-essential \
    python3 \
    && rm -rf /var/lib/apt/lists/*
RUN npm install
COPY . .
EXPOSE 3000
CMD ["npm", "start"]
