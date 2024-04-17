
# Use the official Node.js image from the Docker Hub
# with the specified Node.js version.
ARG NODE_VERSION=14.21.3
FROM node:${NODE_VERSION}-alpine



# Create a directory for the application.
WORKDIR /usr/src/app

# Copy the package.json and package-lock.json files.
# This step is separated to take advantage of Docker's caching mechanism.
COPY package*.json ./

RUN npm install axios
RUN npm install
# Switch to a non-root user.


# Copy the rest of the application source code.
COPY . .

# Expose the port that the application will listen on.
EXPOSE 3000

# Command to run the application.
CMD ["npm", "start"]
