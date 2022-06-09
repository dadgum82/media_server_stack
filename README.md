# media_server_stack
This content is for educational purposes only!!

Software Used
* https://sonarr.tv/
* https://radarr.video/
* plex

docker commands
sudo docker-compose up -d

 ./run_tests

sudo docker-compose down



nosuid,nodev,nofail,x-gvfs-show,rw,exec




sudo docker inspect -f '{{range.NetworkSettings.Networks}}{{.IPAddress}}{{end}}' media-server-stack_sonarr


sudo docker inspect -f '{{range.NetworkSettings.Networks}}{{.IPAddress}}{{end}}' media-server-stack_prowlarr

http://<ip address>:9696
http://localhost:8989

docker-compose up --force-recreate


http://haugene.github.io/docker-transmission-openvpn/faq/#how_do_i_verify_that_my_traffic_is_using_vpn

How do I verify that my traffic is using VPN¶

There are many ways of doing this, and I welcome you to add to this list if you have any suggestions.

You can exec into the container and through the shell use curl to ask for your public IP. There are multiple endpoints for this but here are a few suggestions:
    curl http://ipinfo.io/ip
    curl http://ipecho.net/plain
    curl icanhazip.com

Or you could use a test torrent service to download a torrent file and then you can get the IP from that tracker.
    http://ipmagnet.services.cbcdn.com/
    https://torguard.net/checkmytorrentipaddress.php



*********************
******************
sudo docker exec -it docker_transmission-openvpn_1 /bin/bash
sudo docker exec -it deluge-vpn /bin/bash



**********************************
*IP ADDRESSESS
******************************
It is a virtual network so you need to look up the ips.
localhost does not work

sudo docker ps
-- get the CONTAINER ID
sudo docker inspect <CONTAINER ID>
--  get the ip address


Or you could use a test torrent service to download a torrent file and then you can get the IP from that tracker.
    http://ipmagnet.services.cbcdn.com/
    https://torguard.net/checkmytorrentipaddress.php



*********************
******************
sudo docker exec -it docker_transmission-openvpn_1 /bin/bash
sudo docker exec -it deluge-vpn /bin/bash



**********************************
*IP ADDRESSESS
******************************
It is a virtual network so you need to look up the ips.
localhost does not work

sudo docker ps
-- get the CONTAINER ID
sudo docker inspect <CONTAINER ID>
--  get the ip address



root@plex:/home/waffles/docker# ip address

