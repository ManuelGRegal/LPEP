# Linux Local Privilege Escalation and Persistence

**Máquina virtual LPEP.ova:**
En Virtualbox: Menú Archivo --> importar servicio virtualizado
- mirror#1: [LPEP.ova](https://drive.google.com/file/d/1IkBqFoVrpf_Nf5r_Y7oVB5DOdzRZoIsP/view?usp=sharing)
- mirror#2: [LPEP.ova](https://drive.google.com/file/d/1P5gd45UZydU1oJM_35wBWZOQ9rC2DmaX/view?usp=sharing)

Se trata de una máquina Linux Debian altamente vulnerable que al importarse se conecta a una red Host-only por defecto, y de esta forma no tendrá acceso al exterior ni del exterior (recomendado).

Para prácticas de persistencia es recomendable una máquina virtual Kali Linux conectada a la misma red Host-only que LPEP o tener un cliente ssh y netcat o ncat en el equipo anfitrión

**Enlaces de interés:**

[Payloads All The Things](https://github.com/swisskyrepo/PayloadsAllTheThings)
- [Linux - Persistence](https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Methodology%20and%20Resources/Linux%20-%20Persistence.md)
- [Linux - Privilege Escalation](https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Methodology%20and%20Resources/Linux%20-%20Privilege%20Escalation.md)
- [Reverse Shell Cheatsheet](https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Methodology%20and%20Resources/Reverse%20Shell%20Cheatsheet.md)

[GTFOBins](https://gtfobins.github.io/)

[Sagi Shahar - LPE Worksshop](https://github.com/sagishahar/lpeworkshop)

[C0nd4 - mimd map LPE](https://github.com/C0nd4/OSCP-Priv-Esc)

Herramientas de enumeración:
- [Linux Exploit Suggester](https://github.com/mzet-/linux-exploit-suggester)
- [LinPEAS - Linux Privilege Escalation Awesome Script](https://github.com/carlospolop/PEASS-ng/tree/master/linPEAS)
- [LinEnum](https://github.com/rebootuser/LinEnum)
- [linux-smart-enumeration](https://github.com/rebootuser/LinEnum)

En caso de problemas de acceso por ssh desde Kali:
```
kali@kali:~$ nano .ssh/config 
HostKeyAlgorithms ssh-rsa
PubkeyAcceptedKeyTypes ssh-rsa
```
RRSS:
- twitter: [@ManuelGRegal](https://twitter.com/@ManuelGRegal)
- Youtube: [https://www.youtube.com/@ManuelGRegal](https://www.youtube.com/@ManuelGRegal)
