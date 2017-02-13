# eyefiserver

Based on Jeff Tchang's [EyeFiServer 2.0](https://github.com/tachang/EyeFiServer), simplified for a quick Ubuntu installation with a few minor features added.

This for use with the old-style card.  Mine is an Eye-Fi Share 2GB.

## Installation

**NOTE: Never copy-paste commands starting with `sudo` from a GitHub README.  Make sure you know what you're doing.**

1. [Find your card's upload key](http://web.archive.org/web/20160520145844/http://support.photosmithapp.com/knowledgebase/articles/116903-why-do-i-see-multiple-eye-fi-card-upload-keys-ho) and paste it into settings.ini

2. Copy this directory to /usr/local/eyefiserver:

    ```bash
    cd ..
    sudo cp -R eyefiserver /usr/local/
    ```

3. Copy and set up the init script:

    ```bash
    sudo cp eyefiserver/eyefiserver.initd /etc/init.d/eyefiserver
    sudo chmod 755 /etc/init.d/eyefiserver
    sudo update-rc.d eyefiserver defaults
    ```

4. Start it up:

    ```bash
    sudo service eyefiserver start
    ```

If all goes well, great!  If not, please open an issue.
