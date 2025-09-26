FROM yourls:latest

RUN curl -sSL https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions -o - | sh -s gd @composer
ENV PLUGIN_DIR="/var/www/html/user/plugins"
RUN PLUGIN_OWNER="seandrickson" && \
    PLUGIN_REPO="YOURLS-QRCode-Plugin" && \
    PLUGIN_FOLDER="seans-qrcode" && \
    mkdir -p "$PLUGIN_DIR/$PLUGIN_FOLDER" && \
    curl -o "$PLUGIN_DIR/$PLUGIN_FOLDER/Plugin.zip" "https://codeload.github.com/$PLUGIN_OWNER/$PLUGIN_REPO/zip/refs/heads/master" && \
    unzip -ju "$PLUGIN_DIR/$PLUGIN_FOLDER/Plugin.zip" "$PLUGIN_REPO-master/$PLUGIN_FOLDER/*" -d "$PLUGIN_DIR/$PLUGIN_FOLDER/" && \
    rm "$PLUGIN_DIR/$PLUGIN_FOLDER/Plugin.zip" && \
    cd "$PLUGIN_DIR//$PLUGIN_FOLDER" && \
    composer update && \
    composer install --no-dev
RUN PLUGIN_OWNER="paramedicspecialist" && \
    PLUGIN_REPO="YOURLS_ReverseProxySupport" && \
    PLUGIN_FOLDER="reverse-proxy-support" && \
    mkdir -p "$PLUGIN_DIR/$PLUGIN_FOLDER" && \
    curl -o "$PLUGIN_DIR/$PLUGIN_FOLDER/Plugin.zip" "https://codeload.github.com/$PLUGIN_OWNER/$PLUGIN_REPO/zip/refs/heads/master" && \
    unzip -ju "$PLUGIN_DIR/$PLUGIN_FOLDER/Plugin.zip" "$PLUGIN_REPO-master/$PLUGIN_FOLDER/*" -d "$PLUGIN_DIR/$PLUGIN_FOLDER/" && \
    rm "$PLUGIN_DIR/$PLUGIN_FOLDER/Plugin.zip"
RUN PLUGIN_OWNER="dgw" && \
    PLUGIN_REPO="yourls-dont-track-admins" && \
    PLUGIN_FOLDER="dont-track-admins" && \
    mkdir -p "$PLUGIN_DIR/$PLUGIN_FOLDER" && \
    curl -o "$PLUGIN_DIR/$PLUGIN_FOLDER/Plugin.zip" "https://codeload.github.com/$PLUGIN_OWNER/$PLUGIN_REPO/zip/refs/heads/master" && \
    unzip -ju "$PLUGIN_DIR/$PLUGIN_FOLDER/Plugin.zip" "$PLUGIN_REPO-master/*" -d "$PLUGIN_DIR/$PLUGIN_FOLDER/" && \
    rm "$PLUGIN_DIR/$PLUGIN_FOLDER/Plugin.zip"
RUN PLUGIN_OWNER="guessi" && \
    PLUGIN_REPO="yourls-dont-log-health-checker" && \
    PLUGIN_FOLDER="dont-log-health-checker" && \
    mkdir -p "$PLUGIN_DIR/$PLUGIN_FOLDER" && \
    curl -o "$PLUGIN_DIR/$PLUGIN_FOLDER/Plugin.zip" "https://codeload.github.com/$PLUGIN_OWNER/$PLUGIN_REPO/zip/refs/heads/master" && \
    unzip -ju "$PLUGIN_DIR/$PLUGIN_FOLDER/Plugin.zip" "$PLUGIN_REPO-master/plugin.php" -d "$PLUGIN_DIR/$PLUGIN_FOLDER/" && \
    rm "$PLUGIN_DIR/$PLUGIN_FOLDER/Plugin.zip"
RUN PLUGIN_OWNER="vaughany" && \
    PLUGIN_REPO="yourls-popular-clicks-extended" && \
    PLUGIN_FOLDER="popular-links-extended" && \
    mkdir -p "$PLUGIN_DIR/$PLUGIN_FOLDER" && \
    curl -o "$PLUGIN_DIR/$PLUGIN_FOLDER/Plugin.zip" "https://codeload.github.com/$PLUGIN_OWNER/$PLUGIN_REPO/zip/refs/heads/master" && \
    unzip -ju "$PLUGIN_DIR/$PLUGIN_FOLDER/Plugin.zip" "$PLUGIN_REPO-master/plugin.php" -d "$PLUGIN_DIR/$PLUGIN_FOLDER/" && \
    rm "$PLUGIN_DIR/$PLUGIN_FOLDER/Plugin.zip"
RUN PLUGIN_OWNER="YOURLS" && \
    PLUGIN_REPO="timezones" && \
    PLUGIN_FOLDER="timezones" && \
    mkdir -p "$PLUGIN_DIR/$PLUGIN_FOLDER" && \
    curl -o "$PLUGIN_DIR/$PLUGIN_FOLDER/Plugin.zip" "https://codeload.github.com/$PLUGIN_OWNER/$PLUGIN_REPO/zip/refs/heads/master" && \
    unzip -ju "$PLUGIN_DIR/$PLUGIN_FOLDER/Plugin.zip" "$PLUGIN_REPO-master/*" -d "$PLUGIN_DIR/$PLUGIN_FOLDER/" && \
    rm "$PLUGIN_DIR/$PLUGIN_FOLDER/Plugin.zip"