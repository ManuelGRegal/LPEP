# Linux Local Privilege Escalation and Persistence

**Máquina virtual LPEP.ova:**
En Virtualbox: Menú Archivo --> importar servicio virtualizado
- mirror#1: [LPEP.ova](https://drive.google.com/file/d/1dTq2rq3cpb-1v5lMf6YWj-vq7bQbKj3A/view?usp=sharing)
- mirror#2: [LPEP.ova](https://drive.google.com/file/d/1qb-78PQYAILP3DXBbjRLEPGKgl6ncxDz/view?usp=sharing)
- md5sum: 251c9578ad0914fd82417f8859f4411a

Se trata de una máquina Linux Debian altamente vulnerable que al importarse se conecta a una red Host-only por defecto, y de esta forma no tendrá acceso al exterior ni del exterior (recomendado).

Para prácticas de persistencia es recomendable una máquina virtual Kali Linux conectada a la misma red Host-only que LPEP o tener un cliente ssh y netcat o ncat en el equipo anfitrión

**Máquina virtual Dump1.ova:**
En Virtualbox: Menú Archivo --> importar servicio virtualizado
- mirror#1: [Dump1.ova](https://drive.google.com/file/d/1RlJ0EHfkfrNYbEJjBbcbhSZqVj53AVOp/view?usp=sharing)
- mirror#2: [Dump1.ova](https://drive.google.com/file/d/1TqrEcTHGS72NvABfQuusZAWuWLazd794/view?usp=sharing)
- md5sum: d36b1f13cd7a201855a243cec2b31a04

Se trata de una máquina Linux Debian creada a partir de la máquina Dump de [VulNyx](https://vulnyx.com), altamente vulnerable que al importarse se conecta a una red Host-only por defecto, y de esta forma no tendrá acceso al exterior ni del exterior (recomendado).

**Enlaces de interés:**

[Payloads All The Things](https://github.com/swisskyrepo/PayloadsAllTheThings)
- [Linux - Persistence](https://swisskyrepo.github.io/InternalAllTheThings/redteam/persistence/linux-persistence/)
- [Linux - Privilege Escalation](https://swisskyrepo.github.io/InternalAllTheThings/redteam/escalation/linux-privilege-escalation/)
- [Reverse Shell Cheatsheet](https://swisskyrepo.github.io/InternalAllTheThings/cheatsheets/shell-reverse-cheatsheet/)

[GTFOBins](https://gtfobins.github.io/)

[Sagi Shahar - LPE Worksshop](https://github.com/sagishahar/lpeworkshop)

[C0nd4 - mimd map LPE](https://github.com/C0nd4/OSCP-Priv-Esc)

Herramientas de enumeración:
- [Linux Exploit Suggester](https://github.com/The-Z-Labs/linux-exploit-suggester)
- [LinPEAS - Linux Privilege Escalation Awesome Script](https://github.com/carlospolop/PEASS-ng/tree/master/linPEAS)
- [LinEnum](https://github.com/rebootuser/LinEnum)
- [linux-smart-enumeration](https://github.com/diego-treitos/linux-smart-enumeration)

[Reverse Shell Generator](https://www.revshells.com/)

En caso de problemas de acceso por ssh desde Kali:
```bash
kali@kali:~$ ssh user@192.168.56.130      
Unable to negotiate with 192.168.56.130 port 22: no matching host key type found. Their offer: ssh-rsa,ssh-dss
```
Añadir las siguientes líneas al fichero de configuración del cliente ssh:
```
kali@kali:~$ sudo nano /etc/ssh/ssh_config

HostKeyAlgorithms = +ssh-rsa
PubkeyAcceptedAlgorithms = +ssh-rsa
```
O
```
kali@kali:~$ nano .ssh/config
Host *
HostKeyAlgorithms +ssh-rsa
PubkeyAcceptedAlgorithms +ssh-rsa
```

RRSS:
- twitter: [@ManuelGRegal](https://twitter.com/@ManuelGRegal)
- Youtube: [https://www.youtube.com/@ManuelGRegal](https://www.youtube.com/@ManuelGRegal)
