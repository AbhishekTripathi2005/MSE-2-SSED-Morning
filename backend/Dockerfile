FROM node:22-alpine

WORKDIR /app

# Install production dependencies
COPY package.json ./
RUN npm install --omit=dev --no-audit --no-fund

# Copy application source
COPY src ./src

ENV NODE_ENV=production
ENV PORT=3000

EXPOSE 3000

USER node

CMD ["node", "src/server.js"]
