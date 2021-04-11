---
title: Server Funktionen (Netzwerkverwaltung)
description: Die Netzwerk Management Server Funktionen führen administrative Aufgaben auf einem lokalen Server oder Remote Server aus. Die Serverfunktionen sind nachfolgend aufgeführt.
ms.assetid: 43e1285b-8c86-4af4-9834-fcd5ee8aceb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43758fa822ce60d484418431941a386681bb77d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104040008"
---
# <a name="server-functions-network-management"></a>Server Funktionen (Netzwerkverwaltung)

Die Netzwerk Management Server Funktionen führen administrative Aufgaben auf einem lokalen Server oder Remote Server aus. Die Serverfunktionen sind nachfolgend aufgeführt.



| Funktion                                       | BESCHREIBUNG                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**Netserverdiskerum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverdiskenum) | Gibt eine Liste lokaler Laufwerke auf einem Server zurück.                                   |
| [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)         | Listet alle sichtbaren Server eines bestimmten Typs (oder Typen) in der angegebenen Domäne auf. |
| [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo)   | Gibt Konfigurationsinformationen zu einem angegebenen Server zurück.                        |
| [**Netserverabfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo)   | Legt die Betriebsparameter für einen Server fest.                                        |



 

Nur ein Benutzer oder eine Anwendung mit Administrator Gruppenmitgliedschaft auf einem lokalen Server oder einem Remote Server kann administrative Aufgaben auf diesem Server ausführen, um den Betrieb des Servers, den Benutzer Zugriff und die Ressourcen Freigabe zu steuern. Die Parameter auf niedriger Ebene, die sich auf den Vorgang eines Servers auswirken, können durch Aufrufen der Funktionen [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo) und [**netserversetinfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo) überprüft und geändert werden. Diese Parameter werden in der LANMAN.INI Datei des Servers definiert.

Die meisten Netzwerk Management Server Funktionen werden nur auf einem Remote Server ausgeführt. Die [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum) -Funktion wird entweder auf einer lokalen Arbeitsstation oder auf einem Remote Server ausgeführt. Wenn Sie versuchen, andere Serverfunktionen auf einer lokalen Arbeitsstation auszuführen, geben die Funktionen den Fehler NERR \_ RemoteOnly zurück.

Server spezifische Informationen sind auf folgenden Ebenen verfügbar:

-   [**Server \_ Informationen \_ 100**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_100)
-   [**Server \_ Informationen \_ 101**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_101)
-   [**Server \_ Informationen \_ 102**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_102)
-   [**Server \_ Informationen \_ 402**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_402)
-   [**Server \_ Informationen \_ 403**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_403)
-   [**Server \_ Informationen \_ 1501**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1501)
-   [**Server \_ Informationen \_ 1502**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1502)
-   [**Server \_ Informationen \_ 1503**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1503)
-   [**Server \_ Informationen \_ 1506**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1506)
-   [**Server \_ Informationen \_ 1509**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1509)
-   [**Server \_ Informationen \_ 1510**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1510)
-   [**Server \_ Informationen \_ 1511**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1511)
-   [**Server \_ Informationen \_ 1512**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1512)
-   [**Server \_ Informationen \_ 1513**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1513)
-   [**Server \_ Informationen \_ 1515**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1515)
-   [**Server \_ Informationen \_ 1516**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1516)
-   [**Server \_ Informationen \_ 1518**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1518)
-   [**Server \_ Informationen \_ 1523**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1523)
-   [**Server \_ Informationen \_ 1528**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1528)
-   [**Server \_ Informationen \_ 1529**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1529)
-   [**Server \_ Informationen \_ 1530**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1530)
-   [**Server \_ Informationen \_ 1533**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1533)
-   [**Server \_ Informationen \_ 1536**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1536)
-   [**Server \_ Informationen \_ 1538**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1538)
-   [**Server \_ Informationen \_ 1539**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1539)
-   [**Server \_ Informationen \_ 1540**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1540)
-   [**Server \_ Informationen \_ 1541**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1541)
-   [**Server \_ Informationen \_ 1542**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1542)
-   [**Server \_ Informationen \_ 1544**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1544)
-   [**Server \_ Informationen \_ 1550**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1550)
-   [**Server \_ Informationen \_ 1552**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1552)

Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte Active Directory Service Interface (ADSI)-Methoden aufrufen, um die gleiche Funktionalität zu erreichen, die Sie durch Aufrufen der Network Management Server-Funktionen erreichen können. Weitere Informationen finden Sie unter [**iadscomputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).

Weitere Informationen finden Sie unter [Server-und Arbeitsstations-Transport Funktionen](server-and-workstation-transport-functions.md).

 

 
