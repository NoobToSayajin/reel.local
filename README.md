# Baie

<a name="haut-de-page">

<details>
  <summary>Index</summary>
  <ol>
    <li><a href="#roadmap">Roadmap</a></li>
    <li>
    <a>Adressage<a>
      <ul>
        <li><a href="#schema">Schéma</a></li>
        <li><a href="#table-d-adresses">Table d'adresses</a></li>
      </ul>
    </li>
  </ol>
  <details>
    <summary>
    <a href="#projet-reel">Projet Réel</a>
    </summary>
    <ol>
      <li>
        <a href="#configuration-pfsense">Configuration PFSense</a>
        <ul>
          <li><a href="#master">Master</a></li>
        </ul>
      </li>
      <li>
        <a href="#configuration-router">Configuration Router</a>
        <ul>
          <li><a href="#router-r1">Router R1</a></li>
          <li><a href="#router-r2">Router R2</a></li>
          <li><a href="#router-r3">Router R3</a></li>
        </ul>
      </li>
      <li>
        <a href="#configuration-switch">Configuration Switch</a>
        <ul>
          <li><a href="#cataclyst-3550">Cataclyst-3550</a></li>
          <li><a href="#cataclyst-2950">Cataclyst-2950</a></li>
          <li><a href="#allied">Allied</a></li>
        </ul>
      </li>
      <li>
        <a href="#configuration-server">Configuration Servers</a>
        <ul>
          <li>
            <a href="#windows-server-2019">Windows Server 2019</a>
            <ul>
              <li><a href="#master">Master</a></li>
            </ul>
          </li>
          <li>
            <a href="#debian">Debian</a>
            <ul>
              <li><a href="#glpi-ocs">GLPI-OCS</a></li>
            </ul>
          </li>
        </ul>
      </li>
    </ol>
  </details>
</details>

## Roadmap

## Plan d'adressage

<a href="schema"></a>

PFsense

|Pfsense          |Inteface|             IP|CIDR|Link to|
|:----------------|-------:|--------------:|---:|------:|
|Master           |     rl0|   192.168.1.96|  24|    WAN|
|Master           |     rl1|     10.0.0.254|  24| LAN-R1|

Router

|Router|Inteface|            IP|CIDR|  Vlan|      Link to|
|:-----|-------:|-------------:|---:|-----:|------------:|
|R1    |  F0/0/0|    10.0.0.241|  24|Vlan 1|      PFsense|
|R1    |    F0/0|-------------:|  24|      |           R2|
|R1    |    F0/1|192.168.10.254|  24|      |           R3|
|------|--------|--------------|----|------|-------------|
|R2    |    F0/0|-------------:|  24|      |           R1|
|R2    |    F0/0|-------------:|  24|      |           R3|
|------|--------|--------------|----|------|-------------|
|R3    |    F0/0|-------------:|  24|      |           R1|
|R3    |    F0/0|-------------:|  24|      |           R2|

<p align="right">{<a href="#haut-de-page">Haut de page</a>}</p>

## Projet Reel

### Configuration PFsense

#### Master

- [x] WAN + upstream
- [x] LAN

<p align="right">{<a href="#haut-de-page">Haut de page</a>}</p>

### Configuration Router

#### Router R1

- [ ] hostname
- [ ] ip route
- interface :
  - [ ] FastEthernet 0/0/0
  - [ ] FastEthernet 0/0
  - [ ] FastEthernet 0/1
- connexion distante :
  - [ ] console
  - [ ] telnet
  - [ ] ssh
- [ ] DNS
- [ ] OSPF

#### Router R2

- [ ] hostname
- interface :
  - [ ] FastEthernet 0/0
  - [ ] FastEthernet 0/1
- connexion distante :
  - [ ] console
  - [ ] telnet
  - [ ] ssh
- [ ] DNS
- [ ] OSPF

#### Router R3

- [ ] hostname
- interface :
  - [ ] FastEthernet 0/0
  - [ ] FastEthernet 0/1
- connexion distante :
  - [ ] console
  - [ ] telnet
  - [ ] ssh
- [ ] DNS
- [ ] OSPF

<p align="right">{<a href="#haut-de-page">Haut de page</a>}</p>

## Configuration Switch

### Cataclyst 3550

### Cataclyst 2950

### Allied

<p align="right">{<a href="#haut-de-page">Haut de page</a>}</p>
