# Networking-L1
<br> This directory contents screenshots of every Linux Networking task that shoud be done. Some tasks were done with few steps that were also shot.
Every screenshot's name consists of number of task, name of working machine and short explanation of the content. </br>
<br> Task terms and conditions are described in [this](https://github.com/marinaimeninnik/Networking-L1/blob/main/Task_Linux_Net.pdf) PDF-file. </br>
<br>Server machine - Linux Ubuntu 22.04, Client1 machine - CentOs7, Client2 machine - Linux Ubuntu 22.04. All machines were created and managed on VirtualBox.</br>
<br> Next there is described all solution path with screenshots and other links. </br>
<br>1 Task. What should be done: On Server_1 set up static address for all interfaces.</br>
<br>There is a screenshot of network manager settins of Server machine that displays static addresses that were set up.</br>
<br>![Static Serv1](https://github.com/marinaimeninnik/Networking-L1/blob/main/Task%201%20-%20Server%20-%20static%20addresse%20on%20all%20interfaces.png)</br>
<br>Also there were done configurations on [Client1](https://github.com/marinaimeninnik/Networking-L1/blob/main/Task%201%20-%20Client1-%20static%20addresse%20on%20all%20interfaces.png) and [Client2](https://github.com/marinaimeninnik/Networking-L1/blob/main/Task%201%20-%20Client2-%20static%20addresses%20on%20all%20interfaces.png) mashines for next tasks.</br>
<br>2 and 3 Task. 2. Configurate DHCP service on Server_1 that will configurate Int1 Client_1 and Client_2 addresses. 3. Check the connection between virtual machines with ping and traceroute commands. Explain the result.</br>
<br>The DHCP was turned on in network manager settings and connection betwwen all virtual machines was established</br>
<br>Server - Client 1 connection </br>
<br>![serv-cli1](https://github.com/marinaimeninnik/Networking-L1/blob/main/Task%201-3%20-%20Server-%20static%20address%20ping%20net2%20(client1-server).png)</br>
<br>Client 2 - Client 1 connection </br>
<br>![cli2-cli1](https://github.com/marinaimeninnik/Networking-L1/blob/main/Task%201-3%20-%20Client2-%20static%20address%20ping%20net4%20(client2-client1).png)</br>
<br>Client 1 - Client 2 connection </br>
<br>![cli1-cli2](https://github.com/marinaimeninnik/Networking-L1/blob/main/Task%201-3%20-%20Client1-%20static%20address%20ping%20net4%20(client1-client2).png) </br>
<br>4 Task. Set two IP addresses on virtual interface lo Client_1 following next rule: 172.17.D+10.1/24 та 172.17.D+20.1/24. Configurate routing in such way that traffic from Client_2 to 172.17.D+10.1 goes through Server_1 and to 172.17.D+20.1 through Net4. Use traceroute command to check.</br>
<br>Lo Client 1 interface configuration</br>
<br>![locli1](https://github.com/marinaimeninnik/Networking-L1/blob/main/Task%204%20-%20Client-1%20ip%20add%20addresses%20lo.png)</br>
<br>Traffic from Client 2 to 172.17.d+10.1 goes via Server </br>
<br>![Cli2ViaServer](https://github.com/marinaimeninnik/Networking-L1/blob/main/Task%204%20-%20Client-2%20to%20172_17_d%2B10_1%20via%20Server.png) </br>
<br>Traffic from Client 2 to 172.17.d+20.1 goes via Net4 </br>
<br>![Cli2ViaNet4](https://github.com/marinaimeninnik/Networking-L1/blob/main/Task%204%20-%20Client-2%20to%20172_17_d%2B20_1%20via%20Net4.png) </br>
<br>[Client 1 interfaces sittings](https://github.com/marinaimeninnik/Networking-L1/blob/main/Task%204%20-%20Client-1%20net%20config.png)</br>
<br>[Client 1 route recordings](https://github.com/marinaimeninnik/Networking-L1/blob/main/Task%204%20-%20Client-1%20route%20records.png)</br>
<br>[Client 2 netplan configurations](https://github.com/marinaimeninnik/Networking-L1/blob/main/Task%204%20-%20Client-2%20netplan%20config.png)</br>
<br>[Server netplan config](https://github.com/marinaimeninnik/Networking-L1/blob/main/Task%204%20-%20Server%20netplan%20config.png)</br>
<br>5 Task. Make address and mask summarizing for 172.17.D+10.1 and 172.17.D+20.1, however pefix has to be the maximum. Delete routes that have been set previosly and replace them on summarized route that should path via Server_1.</br>
<br>The summarizing have been made and Client's 2 netplan config have been changed. </br>
<br>![sum](https://github.com/marinaimeninnik/Networking-L1/blob/main/Task%205%20-%20Client-2%20netplan%20config.png) </br>
<br>Traffic from Client 2 reaches summarized address (172.17.0.0) via Server.</br>
<br>![Cli2SumServer](https://github.com/marinaimeninnik/Networking-L1/blob/main/Task%205%20-%20Client-2%20reach%20172_17_0_0%20via%20server.png)</br>
<br>[Server route records](https://github.com/marinaimeninnik/Networking-L1/blob/main/Task%205%20-%20Server%20route%20records.png)</br>
<br>6 Task. Configure SSH in such way that Client 1 and Client 2 will be able to connect to each other and to Server 1.</br>
<br>7 Task. The way of firewall configuration on Server 1 has to be: -connection through SSH to Client 1 is allowed and to Client 2 is not allowed; -ping has to pass from Client 2 to 172.17.D+10.1 but has not pass to 172.17.D+20.1</br>
<br>8 Task. If in n.3 Client 1 and Client 2 internet connection routing was configured, you should delete this </br>
8. Якщо в п.3 була налаштована маршрутизація для доступу Client_1 та Client_2 до мережі Інтернет – видалити відповідні записи. На Server_1 налаштувати NAT сервіс таким чином, щоб з Client_1 та Client_2 проходив ping в мережу Інтернет

