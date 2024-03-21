# decoupage de reseaux IP

## le decoupage symetrique

pour le reseaux 172.16.1.0/24 et pour faire le decoupage symetrique, il faut faire le decoupage pour que chaque section est aux moins 50 ip de disponible
le calcul:
- 50 equipent par section donc 2^6 - 2 = 64 -2 = 62. Nous avons donc en tout 62 ip disponible par section
- pour le calcul du masque on est a 32 - 6 = 26 donc nous sommes en /26

|        | Adresse réseau | Adresse de broadcast | Adresse de debut de plage | Adresse de fin de ligne |
| :-: | :------------: | :------------------: | :------: | :-----------: |
| pôle informatique |172.16.1.0/26|172.16.1.63|172.16.1.1|172.16.1.62|
| pole dDévelopement |172.16.1.64/26|172.16.1.128|172.16.1.65|172.16.1.127|
| Pole administratif |172.16.1.129/26|172.16.1.192|172.16.1.130|172.16.191|
| Pole technicien |172.16.1.193/26|172.16.1.256|172.16.1.194|172.16.1.255|


## le decoupage assymetrique

pour le reseaux 172.16.1.0/24 et pour faire le decoupage asymetrique, il faut faire le decoupage pour chaque section
- pour le pole informatique il nous faut 50 equipements 2^6 -2 = 64 - 2 = 62 ip possibles
- pour le pole developement il nous faut 12 equipements 2^4 - 2 = 16 - 2 = 14 ip disponible
- pour le pole administratif il nous faut 20 equipements 2^5 - 2 = 32 - 2 = 30 ip disponible
- pour le pole technicien il nous faut 15 equipements 2^5 - 2 =32 - 2 = 30 ip disponible
- Pour le masque on est toujours en /26

|        | Adresse réseau | Adresse de broadcast | Adresse de debut de plage | Adresse de fin de ligne |
| :-: | :------------: | :------------------: | :------: | :-----------: |
| pôle informatique |172.16.1.0/26|172.16.1.63|172.16.0.1|172.16.0.62|
| pole Dévelopement |172.16.1.64/26|172.16.1.80|172.16.1.65|172.16.1.79|
| Pole administratif |172.16.1.81/26|172.16.1.113|172.16.1.115|172.16.1.112|
| Pole technicien |172.16.1.114/26|172.16.1.146|172.16.1.115|172.16.1.145|