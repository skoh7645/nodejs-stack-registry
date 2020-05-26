# Install the app dependencies in a full Node docker image
FROM registry.access.redhat.com/ubi8/nodejs-12:1-36

# Copying individual files/folders as buildah 1.9.0 does not honour .dockerignore
COPY package*.json /projects/
COPY *.js /projects/

# Install stack dependencies
WORKDIR /projects
ENV PORT=3000

EXPOSE 3000
CMD ["npm", "install"]
