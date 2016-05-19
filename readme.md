# Naked domain problem

This is the fix for the "naked domain problem". You could use this docker image on a ip/server and refer the A record of your DNS to it.

Normally you would use wwwizer, but now you can place it on your own server.

# Installation

# Step 1

Adjust `/conf/nginx.conf` to your needs. So change the redirects:

```return 301 https://www.yourdomain.com$request_uri;```

# Step 2 for ssl

Remember to put your certificates into the `conf/` folder. And change the certificate line to your desired certificate and key:

```ssl_certificate_key certificate.key;```

and

```ssl_certificate certificate.crt;```
