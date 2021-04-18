---
description: Die PNRP-Namespace Anbieter-API verwendet die folgenden Funktionen.
ms.assetid: 7c9f2dd7-8dbc-4bbe-b53c-8036c79faa8a
title: PNRP-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0e811c2d10927064e380970456c76f30730ee4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347370"
---
# <a name="pnrp-functions"></a>PNRP-Funktionen

Die PNRP-Namespace Anbieter-API verwendet die folgenden Funktionen.



| Funktion                                                             | BESCHREIBUNG                                                                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Peer nametopeerhostname"**](/windows/desktop/api/P2P/nf-p2p-peernametopeerhostname)             | Codiert den angegebenen Peer Namen als Format, das mit einem nachfolgenden Aufrufen der Windows Sockets-Funktion [**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) verwendet werden kann. |
| [**"Peer hostnametopeername"**](/windows/desktop/api/P2P/nf-p2p-peerhostnametopeername)             | Decodiert einen von [**peernametopeerhostname**](/windows/desktop/api/P2P/nf-p2p-peernametopeerhostname) zurückgegebenen Hostnamen in die Peer Namen Zeichenfolge, die er darstellt.                            |
| [**Peerpnrpstartup**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartup)                           | Startet den PNRP-Dienst (Peer Name Resolution Protocol) für den aufrufenden Peer.                                                                                |
| [**Peerpnrpshutdown**](/windows/desktop/api/P2P/nf-p2p-peerpnrpshutdown)                         | Fährt eine ausgelaufende Instanz des Peer Name Resolution Protocol (PNRP)-Diensts herunter und gibt alle zugeordneten Ressourcen frei.                             |
| [**Peerpnrpregiester**](/windows/desktop/api/P2P/nf-p2p-peerpnrpregister)                         | Registriert einen Peer bei einer PNRP-Cloud und gibt ein Handle zurück, das für Registrierungs Updates verwendet werden kann.                                                           |
| [**Peerpnrpupdateregistration**](/windows/desktop/api/P2P/nf-p2p-peerpnrpupdateregistration)     | Aktualisiert die PNRP-Registrierungsinformationen für einen Namen.                                                                                                        |
| [**Peerpnrpunregister**](/windows/desktop/api/P2P/nf-p2p-peerpnrpunregister)                     | Aufheben der Registrierung eines Peers aus einer PNRP-Cloud.                                                                                                                        |
| [**Peerpnrprelösen**](/windows/desktop/api/P2P/nf-p2p-peerpnrpresolve)                           | Ruft die für einen bestimmten Peernamen registrierten Endpunkt Adressen ab.                                                                                        |
| [**Peerpnrpstartrelösen**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartresolve)                 | Startet einen asynchronen Peer namens Auflösungs Vorgang.                                                                                                       |
| [**Peerpnrpgetcloudinfo**](/windows/desktop/api/P2P/nf-p2p-peerpnrpgetcloudinfo)                 | Ruft Informationen zu den PNRP-Clouds (Peer Name Resolution Protocol) ab, an denen der aufrufende Peer teilnimmt.                                         |
| [**Peerpnrpdrelösungs**](/windows/desktop/api/P2P/nf-p2p-peerpnrpendresolve)                     | Schließt das Handle für einen asynchronen PNRP-Auflösungs Vorgang, der mit einem vorherigen [**peerpnrpstartreresolution**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartresolve)-aufgerufene Vorgang initiiert wurde.      |
| [PNRP und wsalookupservicebegin](pnrp-and-wsalookupservicebegin.md) | Startet den Prozess, mit dem eine Anwendung Namen auflösen und Netzwerk Clouds aufzählen kann.                                                                 |
| [PNRP und WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)     | Beendet eine Abfrage, die in einem vorherigen [**wsalookupservicebegin**](winsock-nsp-reference-links.md)-aufgerufene Vorgang initiiert wurde.                                             |
| [PNRP und WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)   | Entspricht Abfragen, die in einem vorherigen [**wsalookupservicebegin**](winsock-nsp-reference-links.md)-aufrufsvorgang angegeben wurden.                                                |
| [PNRP und wsanspioctl](pnrp-and-wsanspioctl.md)                     | Empfängt Benachrichtigungen zu Änderungen an der netzwerkcloudliste und zur Verfügbarkeit der Ergebnisse einer Anforderung zur Namensauflösung.                                     |
| [PNRP und wsasetservice](pnrp-and-wsasetservice.md)                 | Registriert oder entfernt [Peernamen](peer-names.md).                                                                                                           |



 

 

 
