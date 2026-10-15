# Mémo Cisco IOS

## Navigation

    enable
    → Passer en mode privilégié

    configure terminal
    → Entrer en mode configuration globale

    exit
    → Revenir au mode précédent

    end
    → Retour direct au mode privilégié

    ?
    → Afficher les commandes disponibles

    show running-config
    → Afficher la configuration en cours
  
    copy running-config startup-config
    → Sauvegarder la configuration

---

## Configuration d'une interface

    interface g0/0
    → Sélectionner l'interface
    
    ip address 192.168.1.250 255.255.255.0
    → Configurer l'adresse IP
    
    no shutdown
    → Activer l'interface
    
    show ip interface brief
    → Vérifier les interfaces

---

## DHCP
    
    ip dhcp excluded-address 192.168.1.240 192.168.1.250
    → Exclure des adresses
    
    ip dhcp pool DHCP_LAN1
    → Créer un pool DHCP
    
    network 192.168.1.0 255.255.255.0
    → Définir le réseau
    
    default-router 192.168.1.250
    → Définir la passerelle
    
    dns-server 192.168.1.250
    → Définir le serveur DNS
    
    show ip dhcp pool
    → Afficher les pools DHCP
    
    show ip dhcp binding
    → Afficher les adresses distribuées

---

## Vérification

    ping 192.168.1.250
    → Tester la communication
    
    show running-config
    → Vérifier la configuration
    
    show ip interface brief
    → Vérifier les interfaces

---

## Astuce Cisco

    Router>
    ↓
    enable
    
    Router#
    ↓
    configure terminal
    
    Router(config)#
    ↓
    interface g0/0
    
    Router(config-if)#
    ↓
    exit
    
    Router(config)#
    ↓
    ip dhcp pool DHCP_LAN1
    
    Router(dhcp-config)#

Attention :

Les commandes "show" fonctionnent généralement depuis :

Router#

ou avec :

do show running-config

depuis les sous-modes.
