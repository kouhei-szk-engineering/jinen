FROM wordpress:latest

# 必要なツール郡をインストール
RUN apt-get update
RUN apt-get -y install wget unzip

# WP プラグイン (zip) ダウンロード
WORKDIR /tmp/wp-plugins
RUN wget https://downloads.wordpress.org/plugin/contact-form-7.4.6.zip
RUN wget https://downloads.wordpress.org/plugin/syntaxhighlighter.zip
RUN wget https://downloads.wordpress.org/plugin/wp-emmet.zip
RUN wget https://downloads.wordpress.org/plugin/agp-font-awesome-collection.zip
# RUN wget https://downloads.wordpress.org/plugin/akismet.3.2.zip
RUN wget https://downloads.wordpress.org/plugin/backwpup.3.3.6.zip
RUN wget https://downloads.wordpress.org/plugin/better-delete-revision.1.6.1.zip
RUN wget https://downloads.wordpress.org/plugin/css-javascript-toolbox.8.3.1.zip
RUN wget https://downloads.wordpress.org/plugin/dashboard-sticky-notes.1.0.3.zip
RUN wget https://downloads.wordpress.org/plugin/ewww-image-optimizer.3.2.6.zip
RUN wget https://downloads.wordpress.org/plugin/p3-profiler.1.5.3.9.zip
RUN wget https://downloads.wordpress.org/plugin/ptengine-real-time-web-analytics-and-heatmap.zip
RUN wget https://downloads.wordpress.org/plugin/wc-shortcodes.zip
RUN wget https://downloads.wordpress.org/plugin/simple-map.4.7.0.zip
RUN wget https://downloads.wordpress.org/plugin/wordfence.6.3.1.zip
RUN wget https://downloads.wordpress.org/plugin/wp-multibyte-patch.2.8.1.zip

# Zip ファイルを解凍してインストール
RUN unzip './*.zip' -d /usr/src/wordpress/wp-content/plugins

# 不要になった一時ファイルを削除
RUN apt-get clean
RUN rm -rf /tmp/*

# サーバが読めるように wp-content 以下の所有者を変更
RUN chown -R www-data:www-data /usr/src/wordpress/wp-content

WORKDIR /var/www/html
