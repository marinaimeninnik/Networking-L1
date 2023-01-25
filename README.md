# Networking-L1
<br> This repository contents screenshots of results of every Linux Networking task that shoud be done. Some tasks were done with several steps that were also shot.
Every screenshot's name consists of task's number, name of working machine and short explanation of the content. </br>
<br> Task's terms and conditions are described in [thisPDF-file](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task_Linux_Net.pdf). </br>
<br>Server machine - Linux Ubuntu 22.04, Client1 machine - CentOs7, Client2 machine - Linux Ubuntu 22.04. All machines were created and managed on VirtualBox.</br>
<br> Next there is described all solution path with screenshots and other links. </br>
<br>1st Task. What should be done: On Server_1 set up static address for all interfaces.</br>
<br>There is a screenshot of network manager settins of Server machine that displays static addresses that were set up.</br>
<br>![Static Serv1](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%201%20-%20Server%20-%20static%20addresse%20on%20all%20interfaces.png)</br>
<br>Also there were done configurations on [Client1](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%201%20-%20Client1-%20static%20addresse%20on%20all%20interfaces.png) and [Client2](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%201%20-%20Client2-%20static%20addresses%20on%20all%20interfaces.png) mashines for next tasks.</br>
<br>2nd and 3rd Task. 2. Configurate DHCP service on Server_1 that will configurate Int1 Client_1 and Client_2 addresses. 3. Check the connection between virtual machines with ping and traceroute commands. Explain the result.</br>
<br>The DHCP was turned on in network manager settings and connection between all virtual machines was established</br>
<br>Server - Client 1 connection </br>
<br>![serv-cli1](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%201-3%20-%20Server-%20static%20address%20ping%20net2%20(client1-server).png)</br>
<br>Client 2 - Client 1 connection </br>
<br>![cli2-cli1](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%201-3%20-%20Client2-%20static%20address%20ping%20net4%20(client2-client1).png)</br>
<br>Client 1 - Client 2 connection </br>
<br>![cli1-cli2](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%201-3%20-%20Client1-%20static%20address%20ping%20net4%20(client1-client2).png) </br>
<br>4th Task. Set two IP addresses on virtual interface lo Client_1 following next rule: 172.17.D+10.1/24 та 172.17.D+20.1/24. Configurate routing in such way that traffic from Client_2 to 172.17.D+10.1 goes through Server_1 and to 172.17.D+20.1 through Net4. Use traceroute command to check.</br>
<br>Lo Client 1 interface configuration</br>
<br>![locli1](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%204%20-%20Client-1%20ip%20add%20addresses%20lo.png)</br>
<br>Traffic from Client 2 to 172.17.d+10.1 goes via Server </br>
<br>![Cli2ViaServer](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%204%20-%20Client-2%20to%20172_17_d%2B10_1%20via%20Server.png) </br>
<br>Traffic from Client 2 to 172.17.d+20.1 goes via Net4 </br>
<br>![Cli2ViaNet4](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%204%20-%20Client-2%20to%20172_17_d%2B20_1%20via%20Net4.png) </br>
<br>[Client 1 interfaces sittings](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%204%20-%20Client-1%20net%20config.png)</br>
<br>[Client 1 route recordings](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%204%20-%20Client-1%20route%20records.png)</br>
<br>[Client 2 netplan configurations](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%204%20-%20Client-2%20netplan%20config.png)</br>
<br>[Server netplan config](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%204%20-%20Server%20netplan%20config.png)</br>
<br>5th Task. Make address and mask summarizing for 172.17.D+10.1 and 172.17.D+20.1, however pefix has to be the maximum. Delete routes that have been set previosly and replace them on summarized route that should path via Server_1.</br>
<br>The summarizing have been made and Client's 2 netplan config have been changed. </br>
<br>![sum](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%205%20-%20Client-2%20netplan%20config.png) </br>
<br>Traffic from Client 2 reaches summarized address (172.17.0.0) via Server.</br>
<br>![Cli2SumServer](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%205%20-%20Client-2%20reach%20172_17_0_0%20via%20server.png)</br>
<br>[Server route records](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%205%20-%20Server%20route%20records.png)</br>
<br>6th Task. Configure SSH in such way that Client 1 and Client 2 will be able to connect to each other and to Server 1.</br>
<br>Client 1 was configured like [this](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%206%20-%20client1%20ssh_config.png)</br>
<br>Client 2 was configured like [this](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%206%20-%20client2%20ssh_config.png)</br>
<br>As a result I checked SSH connection from Client 1 to Server and from Client 1 to Client 2 </br>
<br>![Cli1ServCli2](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%206%20-%20ssh%20connections%20client1%20to%20server%20and%20client2.png)</br>
<br>Also SSH connection from Client 2 to Server and to Client 1 was set up:</br>
<br>![Cli2ServCli1](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%206%20-%20ssh%20connections%20client2%20to%20server%20and%20client1.png)</br>
<br>7th Task. The way of firewall configuration on Server 1 has to be: -connection via SSH from Client 1 is allowed and from Client 2 is not allowed; -ping has to pass from Client 2 to 172.17.D+10.1 but has not pass to 172.17.D+20.1</br>
Server's firewall was configurated as needed to be. So, as we can see, SSH connection from Client 1 is allowed:
<br>![Cli1FWtask](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%207%20-%20ssh%20connection%20allow%20client1%20to%20server.png)</br>
<br>SSH connection from Client 2 is not allowed so as ping is passing from Client 2 to 172.17.D+10.1 but is not passing to 172.17.D+20.1</br>
<br>![Cli2FWtask](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%207%20-%20ssh%20connection%20deny%20client2%20to%20server%20and%20172_17_46_1%20allow%20to%20172_17_36_1.png)</br>
<br>8th Task. If in 3rd task Client's 1 and Client's 2 internet connection routing was configured, you should delete theese records. Configure NAT service in such way that ping from Client 1 and Client 2 should pass through to internet network.</br>
<br>Because of in 3rd task Client's 1 and Client's 2 internet connection routing was configured, theese records were deleted and NAT service was configured:</br>
<br>![ServNATConf](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%208%20-%20Server%20nat%20configurations.png)</br>
<br>And here is successfull [ping to google public DNS server from Client 1](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%208%20-%20Client1%20ping%20to%20internet.png) as a proof of internet connection. So as [Client's 2 ping to google public DNS server](https://github.com/marinaimeninnik/Networking-L1/blob/main/Pictures/Task%208%20-%20Client2%20ping%20to%20internet.png).</br>

