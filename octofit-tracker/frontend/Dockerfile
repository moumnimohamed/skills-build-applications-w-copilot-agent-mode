FROM node:20-alpine

WORKDIR /app

# Copy package files
COPY package*.json ./
COPY vite.config.js ./
COPY index.html ./
COPY tsconfig.json ./
COPY tsconfig.node.json ./

# Install dependencies
RUN npm install

# Copy source code
COPY src ./src
COPY public ./public

# Expose port
EXPOSE 5173

# Start the development server
CMD ["npm", "run", "dev", "--", "--host"]
