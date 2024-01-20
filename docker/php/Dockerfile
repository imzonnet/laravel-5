FROM cyberduck/php-fpm-laravel:5.6

WORKDIR /var/www/html

RUN chown -R www-data /var/www

USER www-data

# Install nvm
RUN curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash

# Add nvm to bash so that it's sourced every time a new shell is started
RUN echo 'export NVM_DIR="$HOME/.nvm"' >> ~/.bashrc
RUN echo '[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"' >> ~/.bashrc
RUN echo '[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"' >> ~/.bashrc

# Install Node.js 16 using nvm
RUN /bin/bash -c "source ~/.nvm/nvm.sh && nvm install 16.8 && nvm use 16.8"

