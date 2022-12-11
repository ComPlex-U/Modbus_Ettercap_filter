sudo nano /etc/ettercap/etter.conf 

[privs]
ec_uid = 0                # nobody is the default
ec_gid = 0                # nobody is the default
 
and 

#---------------
#     Linux 
#---------------

   redir_command_on = "iptables -t nat -A PREROUTING -i %iface -p tcp -d %destination --dpo>
   redir_command_off = "iptables -t nat -D PREROUTING -i %iface -p tcp -d %destination --dp>

# pendant for IPv6 - Note that you need iptables v1.4.16 or newer to use IPv6 redirect
   redir6_command_on = "ip6tables -t nat -A PREROUTING -i %iface -p tcp -d %destination --d>
   redir6_command_off = "ip6tables -t nat -D PREROUTING -i %iface -p tcp -d %destination -->





sudo etterfilter ./etter.filter -o ./modbusfilter.ef


open ettercap 
select ip 1 to slave 2 to pool 
filter load filter 
mitm menu
arp poisoning (ok) 
 