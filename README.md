# oneliner</br>
F5
</br>
cat hosts | while read host do; do curl -sk "https://$host/mgmt/shared/authn/login" | grep -q 'resterrorresponse' && printf "$host \0331;41mF5 iControl REST API Exposed\e[0m\n"; done
