FROM node:24-alpine3.21

# Create non-root user
RUN addgroup -S app && adduser -S -G app app

# Set working directory
WORKDIR /app

# Copy package files and set permissions
COPY package*.json ./

# Switch to root to install dependencies
USER root
RUN chown -R app:app /app

# Switch to app user before installing
USER app
RUN npm install

# Copy rest of the files (as app user)
COPY --chown=app:app . .

# Expose Vite port
EXPOSE 5173

# Run dev server
CMD ["npm", "run", "dev"]
