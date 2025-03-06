from ubuntu/bind9

copy config_file/named.conf /etc/bind/named.conf
copy config_file/m1-8.zone /etc/bind/zones/m1-8.zone

run apt update && apt install nano
run chown -R bind:bind /etc/bind/zones && chmod -R 770 /etc/bind/zones

cmd ["/usr/sbin/named", "-g", "-c", "/etc/bind/named.conf", "-u", "bind"]
