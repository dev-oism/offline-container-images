FROM node:lts-alpine

# Update system packages

RUN apk upgrade --no-cache

# Install required tools

RUN apk add --no-cache \
    ansible-core \
    bash \
    ca-certificates \
    curl \
    git


# Update npm global packages

RUN npm update -g

# Install semantic-release and plugins

RUN npm install -g \
    conventional-changelog-conventionalcommits \    
    semantic-release \
    @semantic-release/gitlab \
    @semantic-release/changelog \
    @semantic-release/exec \
    @semantic-release/git \
    @semantic-release/commit-analyzer \
    @semantic-release/release-notes-generator

# Set working dir

WORKDIR /app

CMD [ "/bin/sh" ]