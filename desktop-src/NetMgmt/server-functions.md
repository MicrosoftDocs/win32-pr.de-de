---
title: Serverfunktionen (Netzwerkverwaltung)
description: Die Netzwerkverwaltungsserverfunktionen führen administrative Aufgaben auf einem lokalen oder Remoteserver aus. Die Serverfunktionen sind im Folgenden aufgeführt.
ms.assetid: 43e1285b-8c86-4af4-9834-fcd5ee8aceb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086abbd23682c17bb1bbfee6180067ca0947a848a4a8dfadb36ba1b87ef13c11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117983134"
---
# <a name="server-functions-network-management"></a>Serverfunktionen (Netzwerkverwaltung)

Die Netzwerkverwaltungsserverfunktionen führen administrative Aufgaben auf einem lokalen oder Remoteserver aus. Die Serverfunktionen sind im Folgenden aufgeführt.



| Funktion                                       | Beschreibung                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**NetServerDiskEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverdiskenum) | Gibt eine Liste der lokalen Laufwerke auf einem Server zurück.                                   |
| [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)         | Listet alle sichtbaren Server eines bestimmten Typs (oder Typen) in der angegebenen Domäne auf. |
| [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo)   | Gibt Konfigurationsinformationen zu einem angegebenen Server zurück.                        |
| [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo)   | Legt die Betriebsparameter für einen Server fest.                                        |



 

Nur ein Benutzer oder eine Anwendung mit Administratorgruppenmitgliedschaft auf einem lokalen oder Remoteserver kann administrative Aufgaben auf diesem Server ausführen, um den Betrieb, den Benutzerzugriff und die Ressourcenfreigabe des Servers zu steuern. Die Low-Level-Parameter, die sich auf den Vorgang eines Servers auswirken, können untersucht und geändert werden, indem die [**Funktionen NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo) und [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo) aufgerufen werden. Diese Parameter werden in der LANMAN.INI-Datei des Servers definiert.

Die meisten Netzwerkverwaltungsserverfunktionen werden nur auf einem Remoteserver ausgeführt. Die [**NetServerEnum-Funktion**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum) wird entweder auf einer lokalen Arbeitsstation oder auf einem Remoteserver ausgeführt. Wenn Sie versuchen, andere Serverfunktionen auf einer lokalen Arbeitsstation auszuführen, geben die Funktionen den Fehler NERR \_ RemoteOnly zurück.

Serverspezifische Informationen sind auf den folgenden Ebenen verfügbar:

-   [**SERVER \_ INFO \_ 100**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_100)
-   [**SERVERINFO \_ \_ 101**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_101)
-   [**SERVER \_ INFO \_ 102**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_102)
-   [**SERVER \_ INFO \_ 402**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_402)
-   [**SERVER \_ INFO \_ 403**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_403)
-   [**SERVERINFO \_ \_ 1501**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1501)
-   [**SERVER \_ INFO \_ 1502**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1502)
-   [**SERVER \_ INFO \_ 1503**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1503)
-   [**SERVER \_ INFO \_ 1506**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1506)
-   [**SERVER \_ INFO \_ 1509**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1509)
-   [**SERVERINFO \_ \_ 1510**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1510)
-   [**SERVERINFO \_ \_ 1511**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1511)
-   [**SERVER \_ INFO \_ 1512**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1512)
-   [**SERVER \_ INFO \_ 1513**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1513)
-   [**SERVERINFO \_ \_ 1515**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1515)
-   [**SERVERINFO \_ \_ 1516**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1516)
-   [**SERVER \_ INFO \_ 1518**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1518)
-   [**SERVERINFO \_ \_ 1523**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1523)
-   [**SERVERINFO \_ \_ 1528**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1528)
-   [**SERVERINFO \_ \_ 1529**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1529)
-   [**SERVERINFO \_ \_ 1530**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1530)
-   [**SERVERINFO \_ \_ 1533**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1533)
-   [**SERVERINFO \_ \_ 1536**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1536)
-   [**SERVERINFO \_ \_ 1538**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1538)
-   [**SERVER \_ INFO \_ 1539**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1539)
-   [**SERVERINFO \_ \_ 1540**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1540)
-   [**SERVERINFO \_ \_ 1541**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1541)
-   [**SERVER \_ INFO \_ 1542**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1542)
-   [**SERVER \_ INFO \_ 1544**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1544)
-   [**SERVER \_ INFO \_ 1550**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1550)
-   [**SERVERINFO \_ \_ 1552**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1552)

Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte ADSI-Methoden (Active Directory Service Interface) aufrufen, um die gleiche Funktionalität zu erreichen, die Sie durch Aufrufen der Funktionen des Netzwerkverwaltungsservers erreichen können. Weitere Informationen finden Sie unter [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).

Weitere Informationen finden Sie unter [Server- und Arbeitsstationstransportfunktionen.](server-and-workstation-transport-functions.md)

 

 
