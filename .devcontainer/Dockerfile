

# [Choice] Node.js version: 20, 18, 16, 14
# or others from https://hub.docker.com/_/node
FROM node:20

# remove old yarn
RUN rm -rf /opt/yarn-v* /usr/local/bin/yarn /usr/local/bin/yarnpkg

# Install eslint typescript expo
RUN npm install -g eslint typescript expo @expo/cli @expo/ngrok@^4.1.0

# init for VS Code
RUN mkdir -p /workspace /.vscode-server 
RUN mkdir /workspace/App && chown $USERNAME:$USERNAME /workspace/App
WORKDIR /workspace/App 
ENV PATH /workspace/App/node_modules/.bin:$PATH

CMD /bin/sh -c "while sleep 86000; do :; done"

