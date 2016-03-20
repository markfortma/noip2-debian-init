# noip2-debian-init

1. Download the no-ip.com Dynamic DNS Update Client from noip.com
   - wget http://www.noip.com/client/linux/noip-duc-linux.tar.gz
2. Extract
   - tar xzf noip-duc-linux.tar.gz
3. Make
   - cd noip-2.9.1/
   - make
   - make install (as root)
4. Copy startup scripts to init.d/
   - chmod 0755 noip2.sh
   - cp noip2.sh /etc/init.d/noip2 (as root)
5. Update service hooks/symlinks
   - update-rc.d noip2 defaults (as root)
6. Create configuration
   - noip2 -C (as root)
7. Start the noip-duc
   - service noip2 start (as root)
