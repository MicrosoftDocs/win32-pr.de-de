---
title: Protokoll Bezeichner
description: Die folgenden Protokoll Bezeichner sind auch in routprot. h für die Windows SDK und iprtmib. h für das Platform Software Development Kit (SDK) aufgeführt.
ms.assetid: f67138b8-de5d-4907-a464-672d57864ebf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59ac515eb4b5090c0b4f75fd923d8345538ff5e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315945"
---
# <a name="protocol-identifiers"></a>Protokoll Bezeichner

Die folgenden Protokoll Bezeichner sind auch in routprot. h für die Windows SDK und iprtmib. h für das Platform Software Development Kit (SDK) aufgeführt.

## <a name="ip-protocols"></a>IP-Protokolle

Die folgenden Routing Protokolle sind dem IP-Transport zugeordnet.



| Protokoll                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Proto \_ IP \_ other, MIB \_ ipproto \_ other                        | Ein anderes Protokoll, das in RFC 1354 nicht angegeben ist.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Proto \_ IP \_ local, MIB \_ ipproto \_ local                        | Eine lokale Schnittstelle.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Proto \_ IP \_ netmgmt, MIB \_ ipproto \_ netmgmt                    | Eine statische Route. Dieser Wert wird verwendet, um Routeninformationen für IP-Routing festzulegen, die über die Netzwerkverwaltung festgelegt werden, z. b. das Dynamic Host Configuration-Protokoll (DCHP), das Simple Network Management-Protokoll (SNMP) oder Aufrufe an die Funktionen " [**mpateipforwardentry**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createipforwardentry)", " [**deleteipforwardentry**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteipforwardentry)" oder " [**setipforward**](/windows/desktop/api/iphlpapi/nf-iphlpapi-setipforwardentry)                                                                                              |
| Proto \_ IP \_ ICMP, MIB \_ ipproto \_ ICMP                          | Das Ergebnis der ICMP-Umleitung.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Proto \_ IP \_ EGP, MIB \_ ipproto \_ EGP                            | Das Protokoll des externen Gateways (EGP), ein dynamisches Routing Protokoll.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Proto \_ IP \_ GGP, MIB \_ ipproto \_ GGP                            | Das Gateway-zu-Gateway-Protokoll (GGP), ein dynamisches Routing Protokoll.                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Proto \_ IP \_ Hello, MIB \_ ipproto \_ Hello                        | Das Protokoll "hellospeak", ein dynamisches Routing Protokoll. Dabei handelt es sich um einen Vergangenheits Eintrag, der nicht mehr verwendet wird. er war ein frühes Routing Protokoll, das von den ursprünglichen ARPANET-Routern verwendet wird, die spezielle Software, die als "Fuzzball-Routing Protokoll" bezeichnet wurde, wie in RFC 891 und RFC 1305 beschrieben. Weitere Informationen finden Sie unter [https://www.ietf.org/rfc/rfc891.txt](https://www.ietf.org/rfc/rfc891.txt) und [https://www.ietf.org/rfc/rfc1305.txt](https://tools.ietf.org/html/rfc1305). |
| Proto \_ IP \_ RIP, MIB \_ ipproto \_ RIP                            | Das Berkeley Routing Information Protocol (RIP) oder RIP-II, ein dynamisches Routing Protokoll.                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Proto \_ IP ist ist \_ \_ , MIB \_ ipproto \_ ist \_                      | Das zwischen System-zu-zwischen-System Protokoll (is-is), ein dynamisches Routing Protokoll. Das is-is-Protokoll wurde für die Verwendung in der Open Systems-Verbindungsprotokoll Suite (OSI) entwickelt.                                                                                                                                                                                                                                                                                                                      |
| Proto \_ IP \_ es \_ ist, MIB \_ ipproto \_ es \_ ist                      | Das System-zu-zwischen-System (es-is)-Protokoll, ein dynamisches Routing Protokoll. Das es-is-Protokoll wurde für die Verwendung in der Open Systems-Verbindungsprotokoll Suite (OSI) entwickelt.                                                                                                                                                                                                                                                                                                                               |
| Proto \_ IP \_ Cisco, MIB \_ ipproto \_ Cisco                        | Das Cisco Interior Gateway Routing Protocol (IGRP), ein dynamisches Routing Protokoll.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Proto \_ IP \_ BBN, MIB \_ ipproto \_ BBN                            | Das Bolt-, Beranek-und Newman (BBN) Interior Gateway-Protokoll (IGP), das den kürzesten Path First-Algorithmus (SPF) verwendet hat. Dies war ein frühes dynamisches Routing Protokoll.                                                                                                                                                                                                                                                                                                                                                   |
| Proto \_ IP \_ OSPF, MIB \_ ipproto \_ OSPF                          | Das OSPF-Protokoll (Open kürzeste Path First), ein dynamisches Routing Protokoll.                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Proto \_ IP \_ BGP, MIB \_ ipproto \_ BGP                            | Die Border Gateway Protocol (BGP), ein dynamisches Routing Protokoll.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Proto \_ IP \_ BOOTP, MIB \_ ipproto \_ BOOTP                        | Das Bootstrap-Protokoll.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Proto \_ IPv6 \_ dhcprelay, MIB \_ IPV6PROTO \_ hdcprelay            | Das DHCPv6 Relay-Protokoll.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Proto \_ IP \_ NT \_ AUTOSTATIC, MIB \_ ipnt \_ AUTOSTATIC             | Ein Windows-spezifischer Eintrag, der ursprünglich durch ein Routing Protokoll hinzugefügt wurde, aber jetzt statisch ist.                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Proto \_ IP \_ NT \_ static, MIB \_ ipnt \_ static                     | Ein Windows-spezifischer Eintrag, der als statische Route von der Routing Benutzeroberfläche oder einem Routing Befehl hinzugefügt wurde.                                                                                                                                                                                                                                                                                                                                                                                                               |
| Proto \_ IP \_ NT \_ static \_ Non \_ DoD, MIB \_ ipnt \_ static \_ Non \_ DoD | Ein Windows-spezifischer Eintrag, der als statische Route von der Routing Benutzeroberfläche oder einem Routing Befehl hinzugefügt wird, außer diese Routen verursachen keine "Dial on Demand" (DoD).                                                                                                                                                                                                                                                                                                                                                        |



 

Die Routen mit der Protokoll Kennung "Proto \_ IP \_ local" umfassen Folgendes:

-   Die Loopback Route
-   Die Subnetzroute
-   Broadcast Route für alle Netzwerke für subnetzschnittstellen
-   Alle "1" s Broadcast Route
-   Lokale Multicast Route
-   Weiterleiten an das Remote Ende eines PPP-Links

Der Bezeichner für den IP-Router-Manager lautet:

iprtrmgr- \_ PID

Dieser Bezeichner kann anstelle eines Routing Protokoll Bezeichners für MIB-Aufrufe mit dem IP-routermanager verwendet werden. Dieser Bezeichner wird für MIB-II, Weiterleitungs-MIB und einige unternehmensspezifische Informationen verwendet. Dieser Bezeichner ist auch in iprtrmib. h aufgeführt.

## <a name="ipx-protocols"></a>IPX-Protokolle

Die folgenden Routing Protokolle sind dem IPX-Transport zugeordnet.



| Protokoll            | BESCHREIBUNG                          |
|---------------------|--------------------------------------|
| IPX- \_ Protokoll ( \_ RIP)  | Routing Informations Protokoll für IPX |
| IPX- \_ Protokoll ( \_ SAP)  | Dienst Ankündigungs Protokoll       |
| IPX- \_ Protokoll ( \_ nlsp) | NetWare Link Services-Protokoll       |



 

Der Bezeichner für den IPX-Router-Manager lautet:

IPX- \_ Protokoll \_ Basis

Verwenden Sie diesen Bezeichner anstelle eines Routing Protokoll Bezeichners für MIB-Aufrufe mit dem IPX-routermanager.

 

 