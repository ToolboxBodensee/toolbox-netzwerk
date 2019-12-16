 Toolbox Bodensee Netzwerk
=========================

## grobe Verkabelung:

*Die Verbindung von den wichtigsten Geräten!*

```
[@] Internet
[T] Telekom DSL
[R] Gateway
[A] APU
[F] Freifunk Offloader
[Sⁿ] Switch
[Seⁿ] Server

 [@]
  |
 [T]----[R]   [A]       [F]
         |     |         |
         '-----'===[S¹]--' <-Netzwerkraum
                   |||
            [S⁴]---'|'-------[S] <- 3D Druck [OG]      
       Bespr.raum   |'-------[S] <- Cyberlabor [OG]
                    |'-------[S] <- Lounge [EG] [nicht aufgebaut]
                    |
        [S³]-------[S²] <<-- Keller
       Rack1     Rack2
        |||        |||
       [Srv¹]    [Srv²]
 ```

## Geräte Hostnamen:

Die Interne Domain der Toolbox ist [tbbs.me.](https://tbbs.me.)<br/>
*Ist DNSSEC validiert und wird von L3D betreut*

### wichtige Teile des Netzes:

```
[R] Gateway
 + Unify Gateway:
   * PPPoE 
   * Routing
   
[A] APU2 ``dhcp.tbbs.me``
   * DHCP
   * DNS
   * ... 

[S¹] Switch im Netzwerkraum:
 + cheerilee.tbbs.me.

[S²] rechter Switch im Keller mit direkten Uplink:
 + princess-luna.tbbs.me.

[S³] linker Switch im Keller:
 + nightmare-moon.tbbs.me.

[S⁴] Besprechungsraum Switch (ruum42)

[Srv¹] Server im linken Rack im Keller
 + HIER in der Datei nicht weiter Dokumentiert

[Srv²] Server im rechten Rack im Keller
 + HIER in der Datei nicht weiter Dokumentiert
```


 Switche
----
S¹ bis S³ sind cisco switche und per ansible administriert. S⁴ ist ein passiver Switch. Dumm - aber leise.

 Static IPs
--------------

We currently only use the ``172.23.16.0/20`` subnet for all devices. 

VMs in the openstack-installation get random IP-adresses from the range ``172.23.23/24`` from DHCP-Server during vm-boot.

The DHCP-Server don't gives random IPs from the ``172.23.31/24`` range to clients in the network. How to give a device one static IP is described at networking-FAQ in the Toolbox-Wiki: [How-To_Satische-IP im Toolbox-Netzwerk]https://wiki.toolbox-bodensee.de/doku.php?id=netzwerk:faq#wie_kann_ich_dafuer_sorgen_dass_mein_geraet_im_toolbox-netz_eine_statische-ip_hat)
Follow this guideline to enable a static IP for your device`
