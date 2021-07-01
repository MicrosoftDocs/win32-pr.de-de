---
description: Die Peerverteilungs-API, die das BranchCache-Feature in Windows 7, Windows Server 2008 R2, Windows 8 und Windows Server 2012 unterstützt, bietet eine Reihe von Plattform-APIs, die die Netzwerkreaktionsfähigkeit zentralisierter Anwendungen erhöhen können, wenn von Remotebüros aus zugegriffen wird, und hilft dabei, die Allgemeine WAN-Auslastung (Wide Area Network) zu reduzieren, ohne die Netzwerksicherheitstechnologien zu beeinträchtigen.
ms.assetid: feb9666e-563a-49f4-ad1c-f166a0faff31
title: Informationen zur Peerverteilung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c996aed35ac691284ba61b757d6ff5a88033aad
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120435"
---
# <a name="about-peer-distribution"></a>Informationen zur Peerverteilung

Die Peerverteilungs-API, die das BranchCache-Feature in Windows 7, Windows Server 2008 R2, Windows 8 und Windows Server 2012 unterstützt, bietet eine Reihe von Plattform-APIs, die die Netzwerkreaktionsfähigkeit zentralisierter Anwendungen erhöhen können, wenn von Remotebüros aus zugegriffen wird, und hilft dabei, die Allgemeine WAN-Auslastung (Wide Area Network) zu reduzieren, ohne die Netzwerksicherheitstechnologien zu beeinträchtigen.

Das Peerverteilungssystem bietet eine Reihe von Plattform-APIs, die sowohl von den Herausgebern genutzt werden, die digitale Inhalte bereitstellen, als auch von Consumern, die sie anfordern. Um diese Rollen leicht unterscheiden zu können, ist es möglicherweise einfacher, sich den Herausgeber in einer Serverrolle und den Consumer in einer Clientrolle zu vorstellen. Abgesehen davon ist es wichtig zu beachten, dass der Peerverteilungsdienst abgesehen von diesen konzeptionellen Rollen ein echtes Peersystem ist, wie die Fähigkeit jedes Peerverteilungsknotens zeigt, digitale Inhalte sowohl zu veröffentlichen als auch zu nutzen. Die Peerverteilungsplattform-APIs werden für Herausgeber und Consumer durch eine Win32-Importbibliothek (**PeerDist.Lib**) verfügbar gemacht.

Der Lebenszyklus von Inhalten, die von einem Herausgeber bereitgestellt und von einem Consumer mit dem Peerverteilungsdienst abgerufen werden, besteht aus den folgenden Vorgängen:



|                         | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Inhaltsveröffentlichung** | Die Veröffentlichung erfolgt, um eine Beschreibung des Inhalts zu erstellen, der als **Inhaltsinformationen** bezeichnet wird, oder **kurz Inhaltsinformationen.** Diese Inhaltsinformationen können dann von einer Instanz des Peerverteilungsdiensts verwendet werden, um den Inhalt zu authentifizieren und neu zu erstellen. Wenn Inhalt von einer Anwendung im Peerverteilungsdienst veröffentlicht wird, was konzeptionell ein serverseitiger Vorgang ist, wird dieser Inhalt der Verlegeridentität zugeordnet, die auf der SID des Benutzers basiert, der dem Threadzugriffstoken zugeordnet ist. Diese Bindung wird ausgeführt, um den Zugriff auf Inhalte durch nicht autorisierte Entitäten zu beschränken. Es ist jedoch wichtig zu beachten, dass der Zugriff auf die Inhaltsinformationen dem Zugriff auf den Inhalt selbst entspricht, da die Inhaltsinformationen verwendet werden können, um den Inhalt von Peers oder einem gehosteten Cache abzurufen.<br/> Es gibt eine neue Version der Inhaltsinformationsdatenstruktur in Windows 8. die vorherige Version wird jedoch weiterhin unterstützt. Für die Zusammenarbeit mit Windows 7-Clients kann ein Administrator den Peerverteilungsdienst so konfigurieren, dass er die vorherige Version der Inhaltsinformationsdatenstruktur verwendet.<br/> |
| **Abrufen von Inhalten**   | Damit ein Consumer Inhalte aus dem Peerverteilungsdienst abrufen kann, muss der Zugriff auf die veröffentlichten Inhaltsinformationen bereitgestellt werden, die diesem Inhalt zugeordnet sind. Der Peerverteilungsdienst, der zum Veröffentlichen des Inhalts verwendet wird, kann die zugehörigen Inhaltsinformationen bereitstellen. Sobald der Consumer über die Inhaltsinformationen verfügt, können andere Peerverteilungs-APIs verwendet werden, um Inhalte vom Peerverteilungsdienst anzufordern. Der Peerverteilungsdienst versucht, den Inhalt aus dem lokalen Netzwerk abzurufen. Wenn der Inhalt nicht verfügbar ist, ist die Clientanwendung für das Abrufen des Inhalts vom Quellserver verantwortlich.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Entfernen der Veröffentlichung** | Für Anwendungen, die Inhalte im Peerverteilungsdienst veröffentlicht haben, wurde die [**Funktion PeerDistServerUnpublish**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverunpublish) bereitgestellt, um die Veröffentlichung von Inhalten zu ermöglichen. Sobald die Veröffentlichung des Inhalts aufgehoben wurde, stellt der lokale Peerverteilungsdienst die Inhaltsinformationen, die diesem Inhalt zugeordnet sind, nicht mehr bereit.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="asynchronous-completions"></a>Asynchrone Vervollständigungen

Die Peerverteilungs-API unterstützt ein asynchrones API-Modell. Daher ermöglichen Peerverteilungs-APIs die Verwendung von E/A-Abschlussports oder Ereignissen als Signalisierungsmechanismen für die Verarbeitung asynchroner Peerverteilungsvorgangsabschlusse. Für beide Mechanismen verwendet die Peerverteilung eine [**OVERLAPPED-Struktur.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Im Allgemeinen übernimmt die Peerverteilung den Besitz einer **OVERLAPPED-Struktur** und aller Out-Parameter, die der Client an asynchrone API-Funktionen übergibt. Der Client darf erst auf diese Ressourcen zugreifen, wenn die asynchrone Funktion abgeschlossen ist. Sobald die asynchronen Funktionen abgeschlossen sind, benötigt der Peerverteilungsdienst keinen Zugriff mehr auf diese Ressourcen und kann wiederverwendet werden, wenn die aufrufende Anwendung dies für geeignet hält.

Es gibt keine asynchrone Vervollständigung, wenn die Funktion einen anderen Fehlercode als **ERROR \_ IO \_ PENDING** zurückgibt. Die Rückgabe eines anderen Werts als **ERROR \_ IO \_ PENDING** bedeutet, dass der Aufruf synchron fehlgeschlagen ist. Wenn die Peerverteilungs-API **ERROR \_ IO \_ PENDING** zurückgibt, muss der Aufrufer auf den asynchronen Abschluss warten.

Der Fehlercode der asynchronen Vervollständigung kann auf zwei Arten abgerufen werden:

**Auf E/A-Abschlussport basierende Vervollständigung**

Der Benutzer ruft den E/A-Abschlussportmechanismus auf, indem er ein Abschlussporthandle und einen Abschlussschlüssel für die folgenden API-Funktionen bereitstellt:

<dl>

[**PeerDistRegisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistregisterforstatuschangenotification)  
[**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream)  
[**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)  
[**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)  
</dl>

Der Benutzer erstellt einen Abschlussport, indem [**er CreateIoCompletionPort aufruft.**](/windows/desktop/FileIO/createiocompletionport) Dieses Abschlussporthandle kann gleichzeitig für andere asynchrone E/A-Vorgänge sowie für peerverteilungsspezifische Vorgänge verwendet werden.

Der Aufrufer sollte die [**GetQueuedCompletionStatus-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) verwenden, um die asynchrone Vervollständigung zu verwalten. Wenn der asynchrone Vorgang fehlschlägt, gibt die **GetQueuedCompletionStatus-Funktion** **FALSE** zurück, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den entsprechenden Fehlercode zurück. Der Aufrufer sollte alle Felder der [**OVERLAPPED-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) ignorieren, wenn der Fehlercode etwas anderes als **ERROR \_ SUCCESS** ist. Der asynchrone Vorgang ist erfolgreich, wenn die **GetQueuedCompletionStatus-Funktion** **TRUE** zurückgibt.

Weitere Informationen finden Sie unter [E/A-Abschlussports.](/windows/desktop/FileIO/i-o-completion-ports)

**Ereignisbasierte Vervollständigung**

Wenn der Aufrufer ein gültiges Ereignishandle für das *hEvent-Feld* der [**OVERLAPPED-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) festlegt, wird es von der Peerverteilung verwendet, um zu signalisieren, dass der zugeordnete asynchrone E/A-Vorgang abgeschlossen wurde.

Ein Threadaufrufer kann überlappende Vorgänge verwalten, indem er ein Handle für das Ereignisobjekt für manuelles Zurücksetzen der [**OVERLAPPED-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) in einer der Wartefunktionen angibt. Nachdem das Ereignis signalisiert wurde, muss der Aufrufer [**PeerGetOverlappedResult**](https://www.bing.com/search?q=**PeerGetOverlappedResult**) aufrufen und die entsprechende **OVERLAPPED-Struktur** übergeben. **PeerGetOverlappedResult** gibt **FALSE** zurück, und der Aufrufer muss [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) aufrufen, um den Fehlercode abzurufen. Der Aufrufer sollte alle Felder der **OVERLAPPED-Struktur** ignorieren, wenn der Fehlercode etwas anderes als **ERROR \_ SUCCESS** ist. Der asynchrone Vorgang ist erfolgreich, wenn die **PeerGetOverlappedResult-Funktion** **TRUE** zurückgibt.

Wenn der Aufrufer einen Abschlussport zusammen mit einem Ereignis bereitstellt, wird das Ereignis als Vervollständigungsmechanismus verwendet.

**Windows 7:** Verwenden Sie die [**GetOverlappedResult-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) anstelle von [**PeerGetOverlappedResult.**](https://www.bing.com/search?q=**PeerGetOverlappedResult**)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Peerverteilungs-API-Referenz](peer-distribution-api-reference.md)
</dt> </dl>

 

