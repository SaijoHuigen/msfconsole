![layout for msfconsole](https://github.com/SaijoHuigen/msfconsole/assets/162563633/2f39bda3-a054-4f19-827c-46b608b01992)During Enumeration, we have to look at our target and identify which public-facing services are running on it. For example, is it an HTTP server? Is it an FTP server? Is it an SQL Database? These different target typologies vary substantially in the real world. We will need to start with a thorough scan of the target's IP address to determine what service is running and what version is installed for each service.

The MSF engagement structure can be divided into five main categories.
•	Enumeration
•	Preparation
•	Exploitation
•	Privilege Escalation
•	Post-Exploitation

Many people often think that the failure of the exploit disproves the existence of the suspected vulnerability. However, this is only proof that the Metasploit exploit does not work and not that the vulnerability does not exist. This is because many exploits require customization according to the target hosts to make the exploit work. Therefore, automated tools such as the Metasploit framework should only be considered a support tool and not a substitute for our manual skills.

type/os/service/name
,,,,,,,,,,,,,,,,,,,,,,,
exploit/windows/ftp/scriptftp_list

ype	Description
Auxiliary:	Scanning, fuzzing, sniffing, and admin capabilities. Offer extra assistance and functionality.
Encoders:	Ensure that payloads are intact to their destination.
Exploits:	Defined as modules that exploit a vulnerability that will allow for the payload delivery.
NOPs:	(No Operation code) Keep the payload sizes consistent across exploit attempts.
Payloads:	Code runs remotely and calls back to the attacker machine to establish a connection (or shell).
Plugins:	Additional scripts can be integrated within an assessment with msfconsole and coexist.
Post:	Wide array of modules to gather information, pivot deeper, etc.

Auxiliary:	Scanning, fuzzing, sniffing, and admin capabilities. Offer extra assistance and functionality.
Exploits:	Defined as modules that exploit a vulnerability that will allow for the payload delivery.
Post:	Wide array of modules to gather information, pivot deeper, etc.

The OS tag specifies which operating system and architecture the module was created for. Naturally, different operating systems require different code to be run to get the desired results.

We can also make our search a bit more coarse and reduce it to one category of services. For example, for the CVE, we could specify the year (cve:<year>), the platform Windows (platform:<os>), the type of module we want to find (type:<auxiliary/exploit/post>), the reliability rank (rank:<rank>), and the search name (<pattern>). This would reduce our results to only those that match all of the above.



