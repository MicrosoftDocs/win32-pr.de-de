---
title: Protokollbezeichner
description: Die folgenden Protokollbezeichner sind auch in Routprot.h für das Windows SDK und iprtmib.h für das Platform Software Development Kit (SDK) aufgeführt.
ms.assetid: f67138b8-de5d-4907-a464-672d57864ebf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dafcbcd028b5c8d4f58172565b34c93cff8d8f9ff766c055e3d8a956cfbb0aa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036470"
---
# <a name="protocol-identifiers"></a>Protokollbezeichner

Die folgenden Protokollbezeichner sind auch in Routprot.h für das Windows SDK und iprtmib.h für das Platform Software Development Kit (SDK) aufgeführt.

## <a name="ip-protocols"></a>IP-Protokolle

Die folgenden Routingprotokolle sind dem IP-Transport zugeordnet.



| Protokoll                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PROTO \_ IP \_ OTHER, MIB \_ IPPROTO \_ OTHER                        | Ein anderes Protokoll, das nicht in RFC 1354 angegeben ist.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| PROTO \_ IP \_ LOCAL, MIB \_ IPPROTO \_ LOCAL                        | Eine lokale Schnittstelle.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| PROTO \_ IP \_ NETMGMT, MIB \_ IPPROTO \_ NETMGMT                    | Eine statische Route. Dieser Wert wird verwendet, um Routeninformationen für IP-Routing zu identifizieren, die über die Netzwerkverwaltung festgelegt wurden, z. B. das Dynamic Host Configuration Protocol (DCHP), das Simple Network Management Protocol (SNMP) oder durch Aufrufe der [**Funktionen CreateIpForwardEntry,**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createipforwardentry) [**DeleteIpForwardEntry**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteipforwardentry)oder [**SetIpForwardEntry.**](/windows/desktop/api/iphlpapi/nf-iphlpapi-setipforwardentry)                                                                                              |
| PROTO \_ IP \_ ICMP, MIB \_ IPPROTO \_ ICMP                          | Das Ergebnis der ICMP-Umleitung.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| PROTO \_ IP \_ EGP, MIB \_ IPPROTO \_ EGP                            | The Exterior Gateway Protocol (EGP), ein protokoll für dynamisches Routing.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| PROTO \_ IP \_ GGP, MIB \_ IPPROTO \_ GGP                            | Das Gateway-zu-Gateway-Protokoll (GGP), ein protokoll für dynamisches Routing.                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| PROTO \_ IP \_ HELLO, MIB \_ IPPROTO \_ HELLO                        | Das Hellospeak-Protokoll, ein protokoll für dynamisches Routing. Dies ist ein historischer Eintrag, der nicht mehr verwendet wird und ein frühes Routingprotokoll war, das von den ursprünglichen ARPANET-Routern verwendet wurde, die eine spezielle Software namens Fuzzballroutingprotokoll namens Hellospeak verwendet haben, wie in RFC 891 und RFC 1305 beschrieben. Weitere Informationen finden Sie unter [https://www.ietf.org/rfc/rfc891.txt](https://www.ietf.org/rfc/rfc891.txt) und [https://www.ietf.org/rfc/rfc1305.txt](https://tools.ietf.org/html/rfc1305). |
| PROTO \_ IP \_ RIP, MIB \_ IPPROTO \_ RIP                            | Das California Routing Information Protocol (RIP) oder RIP-II, ein protokoll für dynamisches Routing.                                                                                                                                                                                                                                                                                                                                                                                                                               |
| PROTO \_ IP \_ IS \_ IS, MIB \_ IPPROTO \_ IS \_ IS                      | Das Is-IS-Protokoll (Intermediate System-to-Intermediate System), ein protokoll für dynamisches Routing. Das IS-IS-Protokoll wurde für die Verwendung in der OSI-Protokollsuite (Open Systems Interconnection) entwickelt.                                                                                                                                                                                                                                                                                                                      |
| PROTO \_ IP \_ ES \_ IS, MIB \_ IPPROTO \_ ES \_ IS                      | Das Es-IS-Protokoll (End System-to-Intermediate System), ein protokoll für dynamisches Routing. Das ES-IS-Protokoll wurde für die Verwendung in der OSI-Protokollsuite (Open Systems Interconnection) entwickelt.                                                                                                                                                                                                                                                                                                                               |
| PROTO \_ IP \_ CISCO, MIB \_ IPPROTO \_ CISCO                        | Cisco Interior Gateway Routing Protocol (IGRP), ein protokoll für dynamisches Routing.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| PROTO \_ IP \_ BBN, MIB \_ IPPROTO \_ BBN                            | Bolt, Beranek und Newman (BBN) Interior Gateway Protocol (IGP), die den SPF-Algorithmus (Shortest Path First) verwendet haben. Dies war ein frühes dynamisches Routingprotokoll.                                                                                                                                                                                                                                                                                                                                                   |
| PROTO \_ IP \_ OSPF, MIB \_ IPPROTO \_ OSPF                          | Das OSPF-Protokoll (Open Shortest Path First), ein protokoll für dynamisches Routing.                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| PROTO \_ IP \_ BGP, MIB \_ IPPROTO \_ BGP                            | Die Border Gateway Protocol (BGP), ein protokoll für dynamisches Routing.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| PROTO \_ IP \_ BOOTP, MIB \_ IPPROTO \_ BOOTP                        | Das Bootstrap-Protokoll.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| PROTO \_ IPV6 \_ DHCPRELAY, MIB \_ IPV6PROTO \_ HDCPRELAY            | Das DHCPv6 Relay-Protokoll.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| PROTO \_ IP \_ NT \_ AUTOSTATIC, MIB \_ IPNT \_ AUTOSTATIC             | Ein Windows Eintrag, der ursprünglich durch ein Routingprotokoll hinzugefügt wurde, aber jetzt statisch ist.                                                                                                                                                                                                                                                                                                                                                                                                                            |
| PROTO \_ IP \_ NT \_ STATIC, MIB \_ IPNT \_ STATIC                     | Ein Windows Eintrag, der als statische Route von der Routing-Benutzeroberfläche oder einem Routingbefehl hinzugefügt wurde.                                                                                                                                                                                                                                                                                                                                                                                                               |
| PROTO \_ IP \_ NT \_ STATIC \_ NON \_ DOD, MIB \_ IPNT \_ STATIC \_ NON \_ DOD | Ein Windows Eintrag, der als statische Route von der Routing-Benutzeroberfläche oder einem Routingbefehl hinzugefügt wurde, mit dem Ausnahme, dass diese Routen nicht zu Dial On Demand (DOD) führen.                                                                                                                                                                                                                                                                                                                                                        |



 

Routen mit dem Protokollbezeichner PROTO \_ IP \_ LOCAL umfassen Folgendes:

-   Die Loopbackroute
-   Die Subnetzroute
-   Übertragungsroute aller Netzwerke für subnetzierte Schnittstellen
-   Alle Broadcastrouten von "1"
-   Lokale Multicastroute
-   Route an das Remoteende eines HYPERLINK-Links

Der Bezeichner für den IP-Router-Manager ist:

IPRTRMGR \_ PID

Dieser Bezeichner kann anstelle eines Routingprotokollbezeichners für MIB-Aufrufe mit dem IP-Router-Manager verwendet werden. Dieser Bezeichner wird für MIB-II, Weiterleitungs-MIB und einige unternehmensspezifische Informationen verwendet. Dieser Bezeichner ist auch in Iprtrmib.h aufgeführt.

## <a name="ipx-protocols"></a>IPX-Protokolle

Die folgenden Routingprotokolle sind dem IPX-Transport zugeordnet.



| Protokoll            | BESCHREIBUNG                          |
|---------------------|--------------------------------------|
| IPX \_ PROTOCOL \_ RIP  | Routing Information Protocol für IPX |
| \_IPX-PROTOKOLL \_ SAP  | Dienstanzeigeprotokoll       |
| IPX \_ PROTOCOL \_ NLSP | NetWare Link Services-Protokoll       |



 

Der Bezeichner für den IPX-Router-Manager ist:

\_IPX-PROTOKOLLBASIS \_

Verwenden Sie diesen Bezeichner anstelle eines Routingprotokollbezeichners für MIB-Aufrufe mit dem IPX-Router-Manager.

 

 