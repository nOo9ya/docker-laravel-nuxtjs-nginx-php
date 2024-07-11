# Nuxt.js Dockerfile-dev
FROM node:20.15-alpine

ARG WORK_DIR
ARG FRONTEND
ENV WORK_DIR=${WORK_DIR}
ENV FRONTEND=${FRONTEND}

# Install dependencies
WORKDIR ${WORK_DIR}

# Copy package.json and package-lock.json
COPY ./${FRONTEND}/package*.json ./

# Install dependencies if package.json exists
RUN npm install

# Copy application files
COPY ./${FRONTEND}/* .

# Expose port and start the application
EXPOSE 3000
CMD ["npm run build && npm run start"]