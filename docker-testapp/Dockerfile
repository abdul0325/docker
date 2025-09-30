# 1. Use official Node image
FROM node:18-alpine

# 2. Set working directory inside container
WORKDIR /testapp

# 3. Copy only package.json and package-lock.json (better caching)
COPY package*.json ./

# 4. Install dependencies
RUN npm install

# 5. Copy the rest of your source code
COPY . .

# 6. Expose app port
EXPOSE 5050

# 7. Set environment variables
ENV MONGO_DB_USERNAME=abdul \
    MONGO_DB_PASSWORD=rehman

# 8. Start the app
CMD ["node", "server.js"]
