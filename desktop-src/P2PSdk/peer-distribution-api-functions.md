---
description: Der Microsoft Peer Distribution-Dienst unterstützt Funktionen sowohl für consumerrollen als auch für Verleger Rollen Szenarien.
ms.assetid: 3f5af891-4f5d-4523-8fe6-47fc6ff13b35
title: Peer Distribution-API-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2532ad8bf5cbb14e18bd16a14bb1be2d79c1791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367946"
---
# <a name="peer-distribution-api-functions"></a>Peer Distribution-API-Funktionen

Der Microsoft Peer Distribution-Dienst unterstützt Funktionen sowohl für consumerrollen als auch für Verleger Rollen Szenarien.

## <a name="the-following-functions-are-common-in-both-client-and-server-scenarios"></a>Die folgenden Funktionen sind in den Szenarien "Client" und "Server" üblich.



| Allgemeine Funktionen                                                                                       | BESCHREIBUNG                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**Peer-diststartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)                                                             | Erstellt eine neue Instanz des **peerdist- \_ \_ Instanzhandles** , die an alle anderen Peer Verteilungs-APIs übermittelt werden muss. |
| [**"Peer-distshutdown"**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistshutdown)                                                           | Gibt Ressourcen frei, die durch den [**callerdiststartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)-Befehl zugeordnet werden.                         |
| [**Peerdistgetstatus**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistgetstatus)                                                         | Gibt den aktuellen Status des Peer Verteilungs Diensts zurück.                                                        |
| [**Peer-distgetstatuusex**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistgetstatusex)                                                     | Gibt den aktuellen Status und die Funktionen des Peer Verteilungs Diensts zurück.                                   |
| [**Peer-distgezu verlappedresult**](/windows/desktop/api/peerdist/nf-peerdist-peerdistgetoverlappedresult)                                     | Ruft die Ergebnisse der asynchronen Vorgänge ab.                                                               |
| [**"Peer-distregisterforstatuschangenotifi"**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistregisterforstatuschangenotification)     | Fordert an, dass der Peer Verteilungsdienst den Aufrufer benachrichtigt, wenn eine Statusänderung auftritt.                      |
| [**Peer-distregisterforstatuschangenotificationex**](/windows/desktop/api/peerdist/nf-peerdist-peerdistregisterforstatuschangenotificationex) | Fordert an, dass der Peer Verteilungsdienst den Aufrufer benachrichtigt, wenn eine Statusänderung auftritt.                      |
| [**Peer-distunregisterforstatuschangenotifizierung**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistunregisterforstatuschangenotification) | Hebt die Registrierung der Status Änderungs Benachrichtigung für die Sitzung auf, die dem angegebenen Handle zugeordnet ist.                 |



 

## <a name="the-following-functions-are-only-supported-in-client-scenarios"></a>Die folgenden Funktionen werden nur in "Client"-Szenarien unterstützt.



| Clientfunktionen                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Peer-distclientopencontent"**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)                               | Öffnet ein Peer-und Rückgabe **\_ Inhalts \_ handle** , das auf diesen Inhalt verweist, und gibt es zurück.                                                                                                                                                                                                                                                                     |
| [**Peer distclientclosecontent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientclosecontent)                             | Schließt das **\_ Inhalts \_ handle** von "Peer".                                                                                                                                                                                                                                                                                                        |
| [**Peer distclientgetinformationbyhandle**](/windows/desktop/api/peerdist/nf-peerdist-peerdistclientgetinformationbyhandle)         | Ruft zusätzliche Informationen vom Peer Verteilungsdienst für ein bestimmtes Inhalts Handle ab.                                                                                                                                                                                                                                               |
| [**"Peer-distclientaddcontentinformation"**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientaddcontentinformation)           | Fügt Inhaltsinformationen hinzu, die dann dem **Peer-Content- \_ \_ handle** zugeordnet werden. Einem "Peer"- **\_ Inhalts \_ handle** können Inhaltsinformationen zugeordnet werden.                                                                                                                                                                        |
| [**"Peer-distclientcompletecontentinformation"**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientcompletecontentinformation) | Gibt das Ende der Inhaltsinformationen an.                                                                                                                                                                                                                                                                                                    |
| [**"Peer-distclientadddata"**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientadddata)                                       | Wird verwendet, um Inhalt im lokalen Cache bereitzustellen. Dies erfolgt in der Regel, wenn Daten nicht im lokalen Netzwerk gefunden werden, wie dies angezeigt wird, wenn für " [**Peer-distclientblockread**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientblockread) " oder " [**Peer-distclientstreamread**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientstreamread) " ein **Fehler \_ Timeout** oder ein **Peer \_ Fehler \_ fehlt \_**. |
| [**Peer distclientblockread**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientblockread)                                   | Bietet zufälligen Zugriff auf den inhaltstream.                                                                                                                                                                                                                                                                                                    |
| [**Peer distclientstreamread**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientstreamread)                                 | Ermöglicht den sequenziellen Zugriff auf den inhaltstream.                                                                                                                                                                                                                                                                                                |
| [**Peer distclientflushcontent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent)                             | Entfernt Inhalt, der zuvor dem lokalen Peer Verteilungssystem hinzugefügt wurde.                                                                                                                                                                                                                                                            |
| [**"Peer-distclientcancelasyncoperation"**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientcancelasyncoperation)             | Bricht einen asynchronen Vorgang ab, der einer [über](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Lapp enden Struktur und dem von " [**Peer-distclientopencontent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)" zurückgegebenen Inhalts Handle zugeordnet ist.                                                                                                                     |



 

## <a name="the-following-functions-are-only-supported-in-server-scenarios"></a>Die folgenden Funktionen werden nur in "Server"-Szenarien unterstützt.



| Server Funktionen                                                                             | BESCHREIBUNG                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Peer-distserverpublishstream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream)                           | Erstellt das **Peer Handler- \_ \_ Streamhandle** , das mit " [**Peer-distserverpublishaddtostream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishaddtostream) " zum Erstellen von Inhaltsinformationen für den Inhaltsstream verwendet werden kann. |
| [**Peer-distserverpublishaddto-Stream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishaddtostream)                 | Fügt dem Stream, auf den vom Peer-Stream-handle verwiesen wird, Daten hinzu.                                                                                                                                  |
| [**Peer-distserverpublishcompletestream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishcompletestream)           | Wird aufgerufen, um anzugeben, dass alle Daten dem Stream hinzugefügt wurden.                                                                                                                                     |
| [**"Peer-distserverclosestreamhandle"**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverclosestreamhandle)                   | Schließt das Streamhandle.                                                                                                                                                                          |
| [**Peer-distserverunpublish**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverunpublish)                                   | Veröffentlicht zuvor veröffentlichte Inhalte im Peer Verteilungsdienst.                                                                                                                         |
| [**Peer-distserveropencontentinformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)         | Öffnet ein **Peer- \_ ContentInfo- \_ handle** für veröffentlichte Inhalte.                                                                                                                                   |
| [**Peer-distserveropencontentinformationex**](/windows/desktop/api/peerdist/nf-peerdist-peerdistserveropencontentinformationex)     | Öffnet ein **Peer- \_ ContentInfo- \_ handle** für veröffentlichte Inhalte.                                                                                                                                   |
| [**Peer-distserverretrievecontentinformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverretrievecontentinformation) | Ruft die dem veröffentlichten Inhalt zugeordneten Inhaltsinformationen ab.                                                                                                                               |
| [**Peer-distserverclosecontentinformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverclosecontentinformation)       | **Peer-Manager \_ ContentInfo- \_ handle** , das von " [**Peer-distserveropencontentinformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)" geöffnet wurde.                                                                  |
| [**"Peer-distservercancelasyncoperation"**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistservercancelasyncoperation)             | Bricht den asynchronen Vorgang ab, der mit dem Inhalts Bezeichner und der [über](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Lapp enden Struktur verknüpft ist.                                             |



 

 

 
