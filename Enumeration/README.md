# THM ENU00 : ****Enumeration****

## OSINT

### Maltego

> ✏️ Note
>
> Maltego permettent d'effectuer une observation critique des cibles à l'aide de différentes transformations intégrées et, comme il s'agit d'un logiciel libre, il permet d'écrire des transformations ou des modules personnalisés.


### TinEye

> ✏️ Note
>
> TinEye est un moteur de recherche d'images inversé qui permet de trouver l'endroit où une image apparaît sur le web. Il peut être utilisé pour trouver l'origine d'une image, repérer les violations de droits d'auteur ou simplement découvrir plus d'informations sur une image

[https://tineye.com/](https://tineye.com/)


### OsintFramework

> ✏️ Note
>
> Site regroupent des outils ou ressources gratuits, l'objectif est d'aider les gens à trouver des ressources OSINT gratuites. 
> Certains des sites inclus peuvent nécessiter un enregistrement ou offrir plus de données contre un abonnement.
> Mais vous devriez être en mesure d'obtenir au moins une partie de l'information disponible gratuitement.

[OSINT Framework](https://osintframework.com/)


### Google Dorking

> ✏️ Note
>
> GoogleDorks est une façon d’utiliser le moteur de recherche de google pour affine les informations rechercher
> 
> - [GHDB](https://www.exploit-db.com/google-hacking-database)
> - [https://astuces-informatique.com/](https://astuces-informatique.com/google-dorks-pirater-sites-web-bases-donnees/)
> - [https://www.it-connect.fr/](https://www.it-connect.fr/google-dorks-google-hacking-exploiter-toute-la-puissance-de-google/)


#### Filetype

```python
## Pour trouver un cv en pdf
filetype:pdf cv # txt, docx, mp3, 
```

#### Site

```python
## Pour rechercher dans un site
site:NomDuSite Motcles
```

#### Intitle

```python
## Pour rechercher dans les titre HTML de la page
intitle: "page de connection"
#ou
allintitle "page de connection"
```

#### Define

```python
## Pour rechercher la cause d'une erreur
define: "sql syntax error"
```

#### Link

```python
## Pour rechercher des site vulnerable aux injection SQL
link: index.php?Id=
```

#### Book

```python
## Pour rechercher un livre 
book: NomDuLivre
```

#### Indexof

```python
## 
index of / esxi key
```


### DNS Records

#### Commande

##### Whois

> ✏️ Note
>
> WHOIS écoute les demandes entrantes sur le port TCP 43. L'agent d'enregistrement du domaine est responsable de la mise à jour des enregistrements WHOIS pour les noms de domaine qu'il loue.

```bash
whois site.lan
```

##### Nslookup

> ✏️ Note
>
> Pour trouver l'adresse IP d'un nom de domaine, utilisez nslookup, qui signifie Name Server Look Up (recherche de serveur de noms).

```bash
## -IPV4  -cible  -ServerDNS
nslookup -type=A tryhackme.com 1.1.1.1

## -MailServer  -cible
nslookup -type=MX tryhackme.com

## -TextRecord  -cible
nslookup -type=txt thmlabs.com
```


##### Dig

> ✏️ Note
>
> Pour des requêtes DNS plus avancées et des fonctionnalités supplémentaires, vous pouvez utiliser dig, l'acronyme de "Domain Information Groper”.

```bash
dig tryhackme.com MX
```

#### En ligne

##### DNSDumpster

> ✏️ Note
>
> Site web permettant de remonter les empreinte détaillée des systèmes Internet d'une organisation. Une ressource tactique qui peut être utilisée à la fois par les attaquants et les défenseurs.

##### Shodan

> ✏️ Note
>
> [Shodan.io](http://shodan.io/) permet d'obtenir diverses informations sur le réseau du client, sans s'y connecter activement. 
> En outre, du côté défensif, vous pouvez utiliser différents services de [Shodan.io](http://shodan.io/) pour connaître les appareils connectés et exposés appartenant à votre organisation.


### Wappalyzer

> ✏️ Note
>
> Wappalyzer ([https://www.wappalyzer.com/](https://www.wappalyzer.com/)) est un outil en ligne et une extension de navigateur qui permet d'identifier les technologies utilisées par un site web, comme les frameworks, les systèmes de gestion de contenu (CMS), les processeurs de paiement et bien d'autres encore, et il peut même trouver les numéros de version.


### The Harvester

> ✏️ Note
>
> The Harvester est un outil permettant de collecter des comptes de messagerie, des sous-domaines, des hôtes virtuels, des ports ouverts/bannières et des noms d'employés à partir de différentes sources publiques telles que les moteurs de recherche, les serveurs de clés PGP et la base de données informatique SHODAN.

[https://github.com/laramies/theHarvester](https://github.com/laramies/theHarvester)

```bash
# Search on Google
theHarvester -d test-site.com -l 500 -b google

# Search LinkedIn 
theHarvester -d test-site.com -l 500 -b linkedin

-b netcraft  
```


### Shodan

> ✏️ Note
>
> Shodan est un moteur de recherche pour les appareils connectés à l'internet. Il permet aux utilisateurs de rechercher des types d'appareils spécifiques et de recueillir des informations à leur sujet, telles que le type d'appareil, les ports ouverts, l'emplacement et d'autres détails. Shodan peut être utilisé pour la recherche en sécurité, la surveillance des réseaux et la reconnaissance. C'est un outil puissant pour les attaquants comme pour les défenseurs.

[Shodan](https://www.shodan.io)

#### En ligne

```bash
os:windows
country:FR
city:paris
title:"test"
```

#### Commande

```bash
shodan host 10.10.10.10
shodan search windows
shodan search --fields ip_str,port,org windows
shodan count windows

shodan search camera country:FR
shodan search --fields ip_str,port webcamxp

shodan count wordpress 1.4.7
shodan download wordpressfile "wordpress 1.4.7"
```

[Install command](https://youtu.be/eAOIw6hPBZw?t=98)


### Amass

> ✏️ Note
>
> Amass est un outil open-source de cartographie et de reconnaissance de réseaux qui permet aux utilisateurs d'identifier des adresses IP, des domaines et d'autres informations connexes. 
> Il utilise des techniques actives et passives telles que le DNS brute forcing, le web scraping et les requêtes API pour collecter des données sur une cible. Amass peut également être utilisé pour l'énumération et la cartographie des sous-domaines, l'analyse des réseaux et le renseignement sur les réseaux. 

[GitHub - owasp-amass/amass: In-depth Attack Surface Mapping and Asset Discovery](https://github.com/OWASP/Amass)

```bash
amass enum -d site-test.com -src - active
```


## Nmap

```bash

nmap -sN -Pn -T 1 -sC -sV -p-

nmap -Pn -T 5 -sC -sV -vvvv -p-

nmap -sU -Pn -sC -sV -p-
```


## Automated Discovery

> ✏️ Note
>
> Automated discovery est le processus qui consiste à utiliser des outils pour découvrir du contenu plutôt que de le faire manuellement. <br>
> Ce processus est automatisé car il contient généralement des centaines, des milliers, voire des millions de requêtes adressées à un serveur web. <br>
> Ces requêtes vérifient si un fichier ou un répertoire existe sur un site web, ce qui nous donne accès à des ressources dont nous ignorions l'existence auparavant. <br>
> Ce processus est rendu possible par l'utilisation d'une ressource appelée liste de mots.  https://github.com/danielmiessler/SecLists


### Hidden Website Pages

> ✏️ Note
>
> La plupart des entreprises disposent d'une page de portail d'administration, qui permet à leur personnel d'accéder aux contrôles administratifs de base pour les opérations quotidiennes.  <br>
> Souvent, ces pages ne sont pas privées, ce qui permet aux attaquants de trouver des pages cachées qui montrent ou donnent accès à des contrôles administratifs ou à des données sensibles.

#### For Dir

##### Using Gobuster

```
gobuster -u <http://fakebank.com> -w wordlist.txt dir

```


#### For Page

##### Using ffuf

```
ffuf -w /usr/share/wordlists/SecLists/Discovery/Web-Content/common.txt -u <http://10.10.207.36/FUZZ>

```

##### Using dirb

```
dirb <http://10.10.207.36/> /usr/share/wordlists/SecLists/Discovery/Web-Content/common.txt

```

##### Using Gobuster

```
gobuster dir --url <http://10.10.207.36/> -w /usr/share/wordlists/SecLists/Discovery/Web-Content/common.txt

```


#### For Subdomain

> ✏️ Note
>
> L'énumération des sous-domaines est le processus qui consiste à trouver des sous-domaines valides pour un domaine, mais pourquoi le faire ? <br>
> Nous le faisons pour étendre notre surface d'attaque et essayer de découvrir plus de points de vulnérabilité potentiels.

##### DNSrecon

```
dnsrecon -t brt -d acmeitsupport.thm

```

##### Using Sublist3r

- [GitHub - Sublist3r](https://github.com/aboul3la/Sublist3r)

```
./sublist3r.py -d acmeitsupport.thm

```


## System Discovery

> ✏️ Note
>
> Le System Discovery et de collecte d'informations sur les systèmes informatiques et leurs composants, tels que les systèmes d'exploitation, 
> les applications, les services et les connexions réseau. 
> 
> Il s'agit d'une étape cruciale de la cybersécurité, car elle permet d'identifier les vulnérabilités et les risques potentiels qui pourraient être exploités.


### Linux

#### System

```bash
# Return the hostname of the target machine
hostname

# Print system information
uname -a
cat /proc/version
cat /etc/issue

# Print the running processes
ps -A   #View all running processes
ps axjf #View process tree
ps aux  #show processes for all users

# Show environmental variables
env

# List all commands can run in Root
sudo -l

# Show the privilege of a file
ls -la

# Provide a general overview of group memberships
id ${user}

# Discover users on the system
cat /etc/passwd
cat /etc/passwd | cut -d ":" -f 1
cat :etc/passwd | grep home 

# Look at earlier commands
history

#find command
find . -name flag1.txt      #find the file named “flag1.txt” in the current directory
find /home -name flag1.txt  #find the file names “flag1.txt” in the /home directory
find / -type d -name config #find the directory named config under “/”
find / -type f -perm 0777   #find files with the 777 permissions (files readable, writable, and executable by all users)
find / -perm a=x            #find executable files
find /home -user frank      #find all files for user “frank”
find / -mtime 10            #find files that were modified in the last 10 days
find / -atime 10            #find files that were accessed in the last 10 day
find / -cmin -60            #find files changed within the last hour (60 minutes)
find / -amin -60            #find files accesses within the last hour (60 minutes)
find / -size 50M            #find files with a 50 MB size
find / -size -50M           #find files smaller than 50 MB size
find / -size -5M 2>/dev/nul #redirect errors to “/dev/null”

```


#### Reseau

```bash
# NETWORK
ifconfig
ip a

# See which network routes exist
ip route

# Show information on existing connections
netstat -a  #shows all listening ports and established connections
netstat -at #can also be used to list TCP protocols respectively
netstat -au #can also be used to list UDP protocols respectively
netstat -l  #list ports in “listening” mode
netstat -s  #list network usage statistics by protocol
netstat -p  #list connections with the service name and PID.
netstat -i  #Shows interface statistics

netstat -ano #Do not resolve names and Display timers
netstat -ltp #list listening ports with the service name and PID
```
