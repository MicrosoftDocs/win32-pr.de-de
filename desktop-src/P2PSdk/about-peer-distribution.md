---
description: Die Peer Distribution-API, die das BranchCache-Feature in Windows 7, Windows Server 2008 R2, Windows 8 und Windows Server 2012 unterstützt, bietet eine Reihe von Plattform-APIs, mit denen sich die Reaktionsfähigkeit von zentralisierten Anwendungen im Netzwerk erhöhen lässt, wenn von Remote Niederlassungen aus auf Sie zugegriffen wird, und die Verwendung der Netzwerk Sicherheitstechnologien verringert wird.
ms.assetid: feb9666e-563a-49f4-ad1c-f166a0faff31
title: Informationen zur Peer Verteilung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5b9a99a65ea2cfda6dc8ad9accd4d881529e87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865180"
---
# <a name="about-peer-distribution"></a>Informationen zur Peer Verteilung

Die Peer Distribution-API, die das BranchCache-Feature in Windows 7, Windows Server 2008 R2, Windows 8 und Windows Server 2012 unterstützt, bietet eine Reihe von Plattform-APIs, mit denen sich die Reaktionsfähigkeit von zentralisierten Anwendungen im Netzwerk erhöhen lässt, wenn von Remote Niederlassungen aus auf Sie zugegriffen wird, und die Verwendung der Netzwerk Sicherheitstechnologien verringert wird.

Das Peer Verteilungssystem bietet eine Reihe von Plattform-APIs, die von den Verlegern verwendet werden, die digitalen Inhalt und Consumer zur Verfügung stellen, die ihn anfordern. Um diese Rollen leicht zu unterscheiden, ist es möglicherweise einfacher, sich den Verleger in einer Server Rolle und den Consumer in einer Client Rolle vorzustellen. Abgesehen von diesen konzeptionellen Rollen ist der Peer Verteilungsdienst ein echtes Peer System, das durch die Fähigkeit eines Peer Verteilungs Knotens zum Veröffentlichen und nutzen digitaler Inhalte angezeigt wird. Die APIs der Peer Verteilungs Plattform werden für Verleger und Consumer durch eine Win32-Import Bibliothek (**peerdist. lib**) verfügbar gemacht.

Der Lebenszyklus von Inhalten, die von einem Verleger bereitgestellt und von einem Consumer mit dem Peer Verteilungsdienst abgerufen werden, besteht aus den folgenden Vorgängen:



|                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Inhalts Veröffentlichung** | Die Veröffentlichung erfolgt durch eine Beschreibung von Inhalten, die als **Inhaltsinformationen** bezeichnet werden, oder für kurze **Inhalts** Informationen. Diese Inhaltsinformationen können dann von einer Instanz des Peer Verteilungs Diensts verwendet werden, um den Inhalt zu authentifizieren und neu zu erstellen. Wenn Inhalt von einer Anwendung in den Peer Verteilungsdienst veröffentlicht wird, bei dem es sich um einen serverseitigen Vorgang handelt, wird dieser Inhalt mit der Identität des Herausgebers verknüpft, die auf der SID des Benutzers basiert, der dem Thread Zugriffs Token zugeordnet ist. Diese Bindung wird durchgeführt, um den Zugriff auf Inhalte durch nicht autorisierte Entitäten einzuschränken. Es ist jedoch wichtig zu beachten, dass der Zugriff auf die Inhaltsinformationen dem Zugriff auf den Inhalt selbst entspricht, da die Inhaltsinformationen verwendet werden können, um den Inhalt von Peers oder einem gehosteten Cache abzurufen.<br/> Es gibt eine neue Version der Inhalts Informationsdaten-Struktur in Windows 8. die vorherige Version wird jedoch weiterhin unterstützt. Um mit Windows 7-Clients zusammenarbeiten zu können, kann ein Administrator den Peer Verteilungsdienst so konfigurieren, dass er die vorherige Version der Inhalts Informationsdaten Struktur verwendet.<br/> |
| **Inhalts Abruf**   | Damit ein Consumer Inhalt aus dem Peer Verteilungsdienst abrufen kann, muss der Zugriff auf die veröffentlichten Inhaltsinformationen, die diesem Inhalt zugeordnet sind, gewährt werden. Der zum Veröffentlichen des Inhalts verwendete Peer Verteilungsdienst kann die zugehörigen Inhaltsinformationen bereitstellen. Nachdem der Consumer die Inhaltsinformationen erhalten hat, können andere Peer Verteilungs-APIs verwendet werden, um Inhalte des Peer Verteilungs Diensts anzufordern. Der Peer Verteilungsdienst versucht, den Inhalt aus dem lokalen Netzwerk abzurufen. Wenn der Inhalt nicht verfügbar ist, ist die Client Anwendung dafür verantwortlich, den Inhalt vom Quell Server abzurufen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Entfernen der Veröffentlichung** | Für Anwendungen, die Inhalte in den Peer Verteilungsdienst veröffentlicht haben, wurde die [**peerdistserverunpublish**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverunpublish) -Funktion bereitgestellt, damit die Veröffentlichung von Inhalten aufgehoben werden kann. Nachdem der Inhalt nicht mehr veröffentlicht wurde, stellt der lokale Peer Verteilungsdienst die Inhaltsinformationen, die diesem Inhalt zugeordnet sind, nicht mehr zur Verfügung.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="asynchronous-completions"></a>Asynchrone Vervollständigungen

Die Peer Verteilungs-API unterstützt ein asynchrones API-Modell, und als Ergebnis können Peer Verteilungs-APIs die Verwendung von e/a-Abschlussports oder Ereignissen als Signalmechanismen für die Verarbeitung von asynchronen Peer Verteilungs Vorgangs Vervollständigungen ermöglichen. Für beide Mechanismen verwendet die Peer Verteilung eine [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur. Im allgemeinen übernimmt die Peer Verteilung den Besitz einer **über** Lapp enden Struktur und aller out-Parameter, die der Client an asynchrone API-Funktionen übergibt. Der Client darf erst auf diese Ressourcen zugreifen, wenn die asynchrone Funktion abgeschlossen ist. Sobald die asynchronen Funktionen abgeschlossen sind, benötigt der Peer Verteilungsdienst keinen Zugriff mehr auf diese Ressourcen, und Sie können wieder verwendet werden, wenn die aufrufende Anwendung geeignet ist.

Es gibt keinen asynchronen Abschluss, wenn die Funktion einen Fehlercode zurückgibt, der nicht mit dem **\_ \_ ausstehenden Fehler**-e/a aussteht. Die Rückgabe eines anderen Werts als Fehler-e/a steht **\_ \_ aus** , dass der-Rückruf synchron fehlgeschlagen ist. Wenn die Peer Verteilungs-API die Fehler-e/a aussteht, muss der Aufrufer auf den asynchronen Abschluss warten. **\_ \_**

Der Fehlercode des asynchronen Abschlusses kann auf zwei Arten abgerufen werden:

**E/a-Abschluss Port basierte Vervollständigung**

Der Benutzer ruft den e/a-Abschlussport-Mechanismus auf, indem er die folgenden API-Funktionen mit einem Vervollständigungs Port Handle und einem Abschluss Schlüssel

<dl>

[**"Peer-distregisterforstatuschangenotifi"**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistregisterforstatuschangenotification)  
[**Peer-distserverpublishstream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream)  
[**Peer-distserveropencontentinformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)  
[**"Peer-distclientopencontent"**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)  
</dl>

Der Benutzer erstellt einen Abschlussport durch Aufrufen von [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport). Dieses Vervollständigungs Port Handle kann gleichzeitig für andere asynchrone e/a-Vorgänge und für Peer Verteilungs spezifische Vorgänge verwendet werden.

Der Aufrufer sollte die [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion verwenden, um den asynchronen Abschluss zu verwalten. Wenn der asynchrone Vorgang fehlschlägt, gibt die Funktion **GetQueuedCompletionStatus** den Wert **false** zurück, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den entsprechenden Fehlercode zurück. Der Aufrufer sollte alle Felder der [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp enden Struktur ignorieren, wenn der Fehlercode etwas anderes als **Fehler \_ Erfolg** ist. Der asynchrone Vorgang ist erfolgreich, wenn die **GetQueuedCompletionStatus** -Funktion " **true**" zurückgibt.

Weitere Informationen finden Sie unter e [/a-Abschlussports](/windows/desktop/FileIO/i-o-completion-ports).

**Ereignisbasierter Abschluss**

Wenn der Aufrufer ein gültiges Ereignis Handle für das *hevent* -Feld der [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp enden Struktur festlegt, verwendet die Peer Verteilung diese, um zu signalisieren, dass der zugehörige asynchrone e/a-Vorgang abgeschlossen wurde.

Ein Thread Aufrufer kann überlappende Vorgänge verwalten, indem er in einer der Wait-Funktionen ein Handle für das Manual-Reset-Ereignis Objekt der [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp enden Struktur angibt. Nachdem das Ereignis signalisiert wurde, muss [**der Aufrufer**](https://www.bing.com/search?q=**PeerGetOverlappedResult**) das übergeben der entsprechenden **über** Lapp enden Struktur aufrufen. " **Peer Name** " gibt " **false** " zurück, und der Aufrufer muss [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) aufrufen, um den Fehlercode abzurufen. Der Aufrufer sollte alle Felder der **über** Lapp enden Struktur ignorieren, wenn der Fehlercode etwas anderes als **Fehler \_ Erfolg** ist. Der asynchrone Vorgang ist erfolgreich, wenn die Funktion " **Peer** der Funktion" " **true**" zurückgibt.

Wenn der Aufrufer einen Abschlussport zusammen mit einem Ereignis bereitstellt, wird das Ereignis als Abschlussmechanismus verwendet.

**Windows 7:** Verwenden Sie die [**getroverlappedresult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) -Funktion anstelle von " [**Peer**](https://www.bing.com/search?q=**PeerGetOverlappedResult**)User User".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Peer Distribution-API-Referenz](peer-distribution-api-reference.md)
</dt> </dl>

 

