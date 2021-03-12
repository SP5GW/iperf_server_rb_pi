# iperf_server_rb_pi

Description how to configure headless Pi 
(no monitor or keyboard/mouse connected)
and then how to install and run iperf3 
server as systemd service.

Assumption is that headless Pi is 
connected over wire (eth0) directly to 
main switch or home gateway. Iperf server shall
be accessed over Pi's static eth0 ip 
address (examples based on TR-398 standard):
  TCP Uplink test:
   iperf3 -c 192.168.1.7 --parallel 5 --omit 2 
  TCP Downlink test:
   iperf3 -c 192.168.1.7 --parallel 5 --omit 2 --reverse

  UDP Uplink test:
   iperf3 -c 192.168.1.7 --udp --parallel 5 --omit 2
  UDP Downlink test:
   iperf3 -c 192.168.1.7 --udp --parallel 5 --omit 2 --reverse

Note: Replace 192.168.1.7 with ip address of your headless pi.
