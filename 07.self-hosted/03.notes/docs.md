---
title: NOTES
slug: notes
menu: NOTES
date: 08-08-2016
published: true
visible: true
taxonomy:
    category: docs
routes:
    aliases:
        - /self-hosted/notes
---

```
      # Notes related to Barracuda add-ons configurable via _XTRAS_LIST variable.

        * Configuration file location: /root/.barracuda.cnf

          ###
          ### Xtras included with "ALL" wildcard:
          ###
          ### ADM --- Adminer DB Manager
          ### CGP --- Collectd Graph Panel
          ### CSF --- Firewall
          ### CSS --- RVM for Compass + NPM for Gulp/Bower
          ### FTP --- Pure-FTPd server with forced FTPS
          ### WMN --- Webmin Control Panel
          ###
          ### Xtras which need to be listed explicitly:
          ###
          ### HVM --- HHVM Engine -- once installed, use ~/static/control/hhvm.info
          ###         to enable per Octopus instance. Available on Wheezy and Trusty.
          ###
          ### BDD --- SQL Buddy DB Manager
          ### BND --- Bind9 DNS Server (available on Debian only)
          ### BZR --- Bazaar
          ### CHV --- Chive DB Manager
          ### FMG --- FFmpeg support
          ### GIT --- Latest Git from sources
          ### IMG --- Image Optimize binaries: advdef advpng jpegoptim jpegtran optipng pngcrush pngquant
          ### SR1 --- Apache Solr 1 with Jetty 7
          ### SR3 --- Apache Solr 3 with Jetty 8
          ### SR4 --- Apache Solr 4 with Jetty 8 or 9
          ###
          ### Examples:
          ###
          ### _XTRAS_LIST=""
          ### _XTRAS_LIST="ALL"
          ### _XTRAS_LIST="ALL GIT SR3"
          ### _XTRAS_LIST="ADM CSF CGP CHV FTP"
          ###

        * Configuration file template: docs/cnf/barracuda.cnf


      # Notes related to Barracuda install on public server with or w/o _EASY_SETUP=PUBLIC

        NOTE: 123.45.67.89 below is a placeholder for your server public, real IP address.

        NOTE: f-q-d-n below is a placeholder for your real wildcard-enabled-hostname.
              See our DNS wildcard configuration example for reference: http://bit.ly/UM2nRb

        NOTE: With _EASY_SETUP=PUBLIC option (default) Barracuda will install automatically
              only services listed below:

        * Your Aegir Master Instance control panel will be available at https://master.f-q-d-n
        * Your Fast DNS Cache Server (pdnsd) will listen on 127.0.0.1:53
        * Your Adminer MariaDB Manager will be available at https://adminer.master.f-q-d-n
        * Your CSF/LFD Firewall will support integrated Nginx Abuse Guard.

        NOTE: With _EASY_SETUP=NO option (default is PUBLIC) Barracuda will offer installation
              of services listed below:

        * Your Aegir Master Instance control panel will be available at https://master.f-q-d-n
        * Your Fast DNS Cache Server (pdnsd) will listen on 127.0.0.1:53
        * Your (optional) Adminer MariaDB Manager will be available at https://adminer.master.f-q-d-n
        * Your (optional) Bind9 DNS Server will listen on 123.45.67.89:53
        * Your (optional) Chive MariaDB Manager will be available at https://chive.master.f-q-d-n
        * Your (optional) Collectd Graph Panel will be available at https://cgp.master.f-q-d-n
        * Your (optional) CSF/LFD Firewall will support integrated Nginx Abuse Guard.
        * Your (optional) MultiCore Apache Solr 1.4.1 with Jetty 7 will listen on 127.0.0.1:8077
        * Your (optional) MultiCore Apache Solr 3.6.2 with Jetty 8 will listen on 127.0.0.1:8088
        * Your (optional) MultiCore Apache Solr 4.9.1 with Jetty 9 will listen on 127.0.0.1:8099
        * Your (optional) SQL Buddy MariaDB Manager will be available at https://sqlbuddy.master.f-q-d-n
        * Your (optional) Webmin Control Panel will be available at https://f-q-d-n:10000

        NOTE: If your outgoing SMTP requires using relayhost, define _SMTP_RELAY_HOST first.

        NOTE: Adminer, Chive, SQL Buddy and Collectd will work only if adminer. chive. sqlbuddy.
              and cgp. subdomains point to your IP (we recommend using wildcard DNS to simplify it).
              But don't worry, you can add proper DNS entries for those subdomains later,
              if you didn't enable wildcard DNS before running Barracuda installer.
              Only system hostname must have proper DNS configuration before installing Barracuda.


      # Notes related to Barracuda install on localhost with _EASY_SETUP=LOCAL

        NOTE: With _EASY_SETUP=LOCAL option (not enabled by default) Barracuda will configure
              your local DNS and hostname automatically. No external DNS configuration needed.

        NOTE: With _EASY_SETUP=LOCAL option (not enabled by default) Barracuda will install
              automatically only services listed below:

        * Your Aegir Master Instance control panel will be available at https://aegir.local
        * Your Fast DNS Cache Server (pdnsd) will listen on 127.0.0.1:53
        * Your Adminer MariaDB Manager will be available at https://adminer.aegir.local


      # Notes related to Barracuda and Octopus customized install and upgrades

        NOTE: While BOA system installed per docs/INSTALL.txt comes with many options
              set by default to make it as easy as possible, you may want to customize
              it further on upgrade, by editing various settings stored in the BOA config
              files, respectively:

              /root/.barracuda.cnf  - check docs/cnf/barracuda.cnf template
              /root/.o1.octopus.cnf - check docs/cnf/octopus.cnf template
              /root/.o2.octopus.cnf - check docs/cnf/octopus.cnf template
              etc.

              Please read docs/UPGRADE.txt for simple upgrades how-to.
```
