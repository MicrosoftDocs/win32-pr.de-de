---
description: Der Microsoft-Peerverteilungsdienst unterstützt Funktionen sowohl für Consumerrollen- als auch für Herausgeberrollenszenarien.
ms.assetid: 3f5af891-4f5d-4523-8fe6-47fc6ff13b35
title: Peerverteilungs-API-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a594313300c6bf39a2ea4f08efba89d1ed757ba4b8a50eda074466b94433e1e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612321"
---
# <a name="peer-distribution-api-functions"></a>Peerverteilungs-API-Funktionen

Der Microsoft-Peerverteilungsdienst unterstützt Funktionen sowohl für Consumerrollen- als auch für Herausgeberrollenszenarien.

## <a name="the-following-functions-are-common-in-both-client-and-server-scenarios"></a>Die folgenden Funktionen sind sowohl in Client- als auch in Serverszenarien üblich.



| Allgemeine Funktionen                                                                                       | Beschreibung                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)                                                             | Erstellt eine neue **PEERDIST \_ INSTANCE \_ HANDLE-Instanz,** die an alle anderen Peerverteilungs-APIs übergeben werden muss. |
| [**PeerDistShutdown**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistshutdown)                                                           | Gibt ressourcen frei, die durch den Aufruf von [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)zugeordnet werden.                         |
| [**PeerDistGetStatus**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistgetstatus)                                                         | Gibt den aktuellen Status des Peerverteilungsdiensts zurück.                                                        |
| [**PeerDistGetStatusEx**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistgetstatusex)                                                     | Gibt den aktuellen Status und die Funktionen des Peerverteilungsdiensts zurück.                                   |
| [**PeerDistGetOverlappedResult**](/windows/desktop/api/peerdist/nf-peerdist-peerdistgetoverlappedresult)                                     | Ruft die Ergebnisse asynchroner Vorgänge ab.                                                               |
| [**PeerDistRegisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistregisterforstatuschangenotification)     | Fordert an, dass der Peerverteilungsdienst den Aufrufer benachrichtigt, wenn eine Statusänderung auftritt.                      |
| [**PeerDistRegisterForStatusChangeNotificationEx**](/windows/desktop/api/peerdist/nf-peerdist-peerdistregisterforstatuschangenotificationex) | Fordert an, dass der Peerverteilungsdienst den Aufrufer benachrichtigt, wenn eine Statusänderung auftritt.                      |
| [**PeerDistUnregisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistunregisterforstatuschangenotification) | Deregistrierung der Statusänderungsbenachrichtigung für die Sitzung, die dem angegebenen Handle zugeordnet ist.                 |



 

## <a name="the-following-functions-are-only-supported-in-client-scenarios"></a>Die folgenden Funktionen werden nur in Clientszenarien unterstützt.



| Clientfunktionen                                                                             | Beschreibung                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)                               | Öffnet und gibt ein **PEERDIST \_ CONTENT \_ HANDLE** zurück, um auf diesen Inhalt zu verweisen.                                                                                                                                                                                                                                                                     |
| [**PeerDistClientCloseContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientclosecontent)                             | Schließt das **PEERDIST \_ CONTENT \_ HANDLE.**                                                                                                                                                                                                                                                                                                        |
| [**PeerDistClientGetInformationByHandle**](/windows/desktop/api/peerdist/nf-peerdist-peerdistclientgetinformationbyhandle)         | Ruft zusätzliche Informationen vom Peerverteilungsdienst für ein bestimmtes Inhaltshandle ab.                                                                                                                                                                                                                                               |
| [**PeerDistClientAddContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientaddcontentinformation)           | Fügt Inhaltsinformationen hinzu, die dann dem **PEERDIST \_ CONTENT \_ HANDLE** zugeordnet werden. Ein **PEERDIST \_ CONTENT \_ HANDLE** kann beliebigen Inhaltsinformationen zugeordnet werden.                                                                                                                                                                        |
| [**PeerDistClientCompleteContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientcompletecontentinformation) | Gibt das Ende der Inhaltsinformationen an.                                                                                                                                                                                                                                                                                                    |
| [**PeerDistClientAddData**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientadddata)                                       | Wird zum Bereitstellen von Inhalt für den lokalen Cache verwendet. Dies geschieht in der Regel, wenn daten im lokalen Netzwerk nicht gefunden werden konnten, wie angegeben, wenn [**Entweder PeerDistClientBlockRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientblockread) oder [**PeerDistClientStreamRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientstreamread) mit **ERROR \_ TIMEOUT** oder **PEERDIST \_ ERROR MISSING \_ \_ DATA** abgeschlossen wurden. |
| [**PeerDistClientBlockRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientblockread)                                   | Ermöglicht zufälligen Zugriff auf den Inhaltsstream.                                                                                                                                                                                                                                                                                                    |
| [**PeerDistClientStreamRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientstreamread)                                 | Stellt sequenziellen Zugriff auf den Inhaltsstream bereit.                                                                                                                                                                                                                                                                                                |
| [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent)                             | Entfernt Inhalte, die zuvor dem lokalen Peerverteilungssystem hinzugefügt wurden.                                                                                                                                                                                                                                                            |
| [**PeerDistClientCancelAsyncOperation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientcancelasyncoperation)             | Bricht einen asynchronen Vorgang ab, der einer [OVERLAPPED-Struktur](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) und dem von [**PeerDistClientOpenContent zurückgegebenen**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)Inhaltshandle zugeordnet ist.                                                                                                                     |



 

## <a name="the-following-functions-are-only-supported-in-server-scenarios"></a>Die folgenden Funktionen werden nur in "Server"-Szenarien unterstützt.



| Serverfunktionen                                                                             | Beschreibung                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream)                           | Erstellt das **PEERDIST \_ STREAM \_ HANDLE,** das mit [**PeerDistServerPublishAddToStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishaddtostream) verwendet werden kann, um Inhaltsinformationen für den Inhaltsstream zu erstellen. |
| [**PeerDistServerPublishAddToStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishaddtostream)                 | Fügt dem Stream, auf den vom PeerDist-Datenstromhandle verwiesen wird, Daten hinzu.                                                                                                                                  |
| [**PeerDistServerPublishCompleteStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishcompletestream)           | Wird aufgerufen, um anzugeben, dass dem Stream alle Daten hinzugefügt wurden.                                                                                                                                     |
| [**PeerDistServerCloseStreamHandle**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverclosestreamhandle)                   | Schließt das Datenstromhandle.                                                                                                                                                                          |
| [**PeerDistServerUnpublish**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverunpublish)                                   | Veröffentlichungen zuvor veröffentlichter Inhalte im Peerverteilungsdienst werden aufgehoben.                                                                                                                         |
| [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)         | Öffnet ein **PEERDIST \_ \_ CONTENTINFO-HANDLE** für veröffentlichten Inhalt.                                                                                                                                   |
| [**PeerDistServerOpenContentInformationEx**](/windows/desktop/api/peerdist/nf-peerdist-peerdistserveropencontentinformationex)     | Öffnet ein **PEERDIST \_ \_ CONTENTINFO-HANDLE** für veröffentlichten Inhalt.                                                                                                                                   |
| [**PeerDistServerRetrieveContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverretrievecontentinformation) | Ruft die Inhaltsinformationen ab, die veröffentlichten Inhalten zugeordnet sind.                                                                                                                               |
| [**PeerDistServerCloseContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverclosecontentinformation)       | **PEERDIST \_ CONTENTINFO \_ HANDLE** wird von [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)geöffnet.                                                                  |
| [**PeerDistServerCancelAsyncOperation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistservercancelasyncoperation)             | Bricht den asynchronen Vorgang ab, der dem Inhaltsbezeichner und der [OVERLAPPED-Struktur](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) zugeordnet ist.                                             |



 

 

 
