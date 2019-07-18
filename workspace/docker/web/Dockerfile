FROM node:8.11.3-alpine

WORKDIR /var/www/portfolio/

RUN apk update && \
    apk add git && \
    apk add --no-cache curl && \
    curl -o- -L https://yarnpkg.com/install.sh | sh

ENV PATH $HOME/.yarn/bin:$HOME/.config/yarn/global/node_modules/.bin:$PATH

# ホットリロード
ENV CHOKIDAR_USEPOLLING=true
RUN yarn global add @vue/cli

EXPOSE 8080

CMD ["/bin/sh"]
