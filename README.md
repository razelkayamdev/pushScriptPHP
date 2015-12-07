Push Script
====

* convert p12 to pem

        openssl pkcs12 -in path.p12 -out cert.pem -clcerts -nokeys
        openssl pkcs12 -in path.p12 -out key.pem -nocerts -nodes

* unite pem files

        cat cert.pem key.pem > certificate.pem

* place certificate.pem in script folder.

* edit sendPush.php

        $deviceToken = 'device.push.token.here';
        $passphrase = 'p12.pass.phrase.here';

* send push
        
        php sendPush.php
