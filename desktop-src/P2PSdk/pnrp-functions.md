---
description: Die PNRP-Namespaceanbieter-API verwendet die folgenden Funktionen.
ms.assetid: 7c9f2dd7-8dbc-4bbe-b53c-8036c79faa8a
title: PNRP-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f109684be61bf1a9a194acb89b22fd4a50be652a6615a18a789e157ca2a5d909
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034380"
---
# <a name="pnrp-functions"></a>PNRP-Funktionen

Die PNRP-Namespaceanbieter-API verwendet die folgenden Funktionen.



| Funktion                                                             | BESCHREIBUNG                                                                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerNameToPeerHostName**](/windows/desktop/api/P2P/nf-p2p-peernametopeerhostname)             | Codiert den angegebenen Peernamen als Format, das mit einem nachfolgenden Aufruf der [**funktion getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) Windows Sockets verwendet werden kann. |
| [**PeerHostNameToPeerName**](/windows/desktop/api/P2P/nf-p2p-peerhostnametopeername)             | Decodiert einen host-Namen, der [**von PeerNameToPeerHostName zurückgegeben wird,**](/windows/desktop/api/P2P/nf-p2p-peernametopeerhostname) in die Peernamenzeichenfolge, die er darstellt.                            |
| [**PeerPnrpStartup**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartup)                           | Startet den PNRP-Dienst (Peer Name Resolution Protocol) für den aufrufenden Peer.                                                                                |
| [**PeerPnrpShutdown**](/windows/desktop/api/P2P/nf-p2p-peerpnrpshutdown)                         | Fährt eine ausgeführte Instanz des PNRP-Diensts (Peer Name Resolution Protocol) herunter und gibt alle zugeordneten Ressourcen frei.                             |
| [**PeerPnrpRegister**](/windows/desktop/api/P2P/nf-p2p-peerpnrpregister)                         | Registriert einen Peer bei einer PNRP-Cloud und gibt ein Handle zurück, das für Registrierungsupdates verwendet werden kann.                                                           |
| [**PeerPnrpUpdateRegistration**](/windows/desktop/api/P2P/nf-p2p-peerpnrpupdateregistration)     | Aktualisiert die PNRP-Registrierungsinformationen für einen Namen.                                                                                                        |
| [**PeerPnrpUnregister**](/windows/desktop/api/P2P/nf-p2p-peerpnrpunregister)                     | Aufheben der Registrierung eines Peers bei einer PNRP-Cloud.                                                                                                                        |
| [**PeerPnrpResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpresolve)                           | Erhält die Endpunktadressen, die für einen bestimmten Peernamen registriert sind.                                                                                        |
| [**PeerPnrpStartResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartresolve)                 | Startet einen asynchronen Peernamensauflösungsvorgang.                                                                                                       |
| [**PeerPnrpGetCloudInfo**](/windows/desktop/api/P2P/nf-p2p-peerpnrpgetcloudinfo)                 | Ruft Informationen zu den PNRP-Clouds (Peer Name Resolution Protocol) ab, an denen der aufrufende Peer beteiligt ist.                                         |
| [**PeerPnrpEndResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpendresolve)                     | Schließt das Handle für einen asynchronen PNRP-Auflösungsvorgang, der mit einem vorherigen Aufruf von [**PeerPnrpStartResolve initiiert wurde.**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartresolve)      |
| [PNRP und WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md) | Startet den Prozess, der es einer Anwendung ermöglicht, Namen aufzulösen und Netzwerk clouds aufzuzählen.                                                                 |
| [PNRP und WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)     | Beendet eine Abfrage, die in einem vorherigen Aufruf von [**WSALookupServiceBegin initiiert wurde.**](winsock-nsp-reference-links.md)                                             |
| [PNRP und WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)   | Entspricht Abfragen, die in einem vorherigen Aufruf von [**WSALookupServiceBegin angegeben wurden.**](winsock-nsp-reference-links.md)                                                |
| [PNRP und WSANSPIoctl](pnrp-and-wsanspioctl.md)                     | Empfängt Benachrichtigungen über Änderungen an der Netzwerk-Cloudliste und die Verfügbarkeit der Ergebnisse einer Namensauflösungsanforderung.                                     |
| [PNRP und WSASetService](pnrp-and-wsasetservice.md)                 | Registriert oder entfernt [Peernamen.](peer-names.md)                                                                                                           |



 

 

 
