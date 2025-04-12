# Use the specified base image
FROM node:19.7.0-alpine

# Set the NODE_ENV environment variable
ENV NODE_ENV=production

# Create a new directory 'labone' and set ownership
RUN mkdir /labone && chown node:node /labone

# Set 'labone' as the working directory
WORKDIR /labone

# Set the user to 'node'
USER node

# Copy all source files and set ownership to 'node'
COPY --chown=node:node . .

# Install dependencies
RUN npm install

# Expose port 3000
EXPOSE 3000

# Set the default execution command
CMD ["node", "src/index.js"]
