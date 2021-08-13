---
description: Der COM+-Dienst für Komponenten in der Warteschlange erweitert das COM-Programmiermodell, indem er eine Umgebung bietet, in der eine Komponente entweder synchron (Echtzeit) oder asynchron (in der Warteschlange) aufgerufen werden kann.
ms.assetid: fd455679-b2b3-487f-8494-9ea296ce2c89
title: Architektur von Warteschlangenkomponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93914fd82a14c73b134098a759c8d61e324b6cda65d03de23f9c3ea2fcfb53f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117916205"
---
# <a name="queued-components-architecture"></a>Architektur von Warteschlangenkomponenten

Der COM+-Dienst für Komponenten in der Warteschlange erweitert das COM-Programmiermodell, indem er eine Umgebung bietet, in der eine Komponente entweder synchron (Echtzeit) oder asynchron (in der Warteschlange) aufgerufen werden kann. Eine Komponente muss nicht wissen, ob sie in einem Echtzeit- oder in einem Warteschlangenkontext eingesetzt wird.

Messaginganwendungen sind wie E-Mail-Transaktionen zwischen Programmen. Der Anfordernde sendet eine Nachricht an den Server. Wenn der Server darauf zukommt, wird die Nachricht verarbeitet. Wie E-Mails muss auch ein Messagingsystem die Netzwerkdetails verarbeiten und sicherstellen, dass die Nachricht vom Client zum Server übertragen wird. Im Framework für Warteschlangenkomponenten ist Message Queuing dafür verantwortlich.

Der COM+-Komponentendienst in der Warteschlange besteht aus den folgenden Teilen:

-   Aufzeichnung (für die Client- oder Sendeseite)
-   Listener (für die Server- oder Empfangsseite)
-   Player (für die Server- oder Empfangsseite)

![Diagramm, das den Pfad vom Client zum Server zeigt: Client, Aufzeichnung, Warteschlange, Listener, Player, Server.](images/d732774b-1ca6-45ad-bce0-a95b0bfc3edb.png)

## <a name="the-recorder"></a>The Recorder

In einem typischen Szenario mit Komponenten in der Warteschlange ruft der Client eine Komponente in der Warteschlange auf. Der Aufruf erfolgt an die Aufzeichnung von Komponenten in der Warteschlange, die sie als Teil einer Nachricht an den Server packt und in eine Warteschlange einreiht. Die Aufzeichnung marshallt den Sicherheitskontext des Clients in die Nachricht und zeichnet alle Methodenaufrufe des Clients auf. In seiner Rolle als Proxy für die Serverkomponente wählt die Aufzeichnung Schnittstellen aus den Warteschlangenschnittstellen im COM+-Katalog aus.

Eine Darstellung der Aufzeichnung wird an die Message Queuing nachricht gesendet, die an einen Server gesendet werden soll. Wenn die in der Warteschlange enthaltene Komponente über die Transaktionsattributeinstellung Erforderlich oder Unterstützt verfügt, akzeptiert Message Queuing die Übermittlung der Nachricht nur, wenn die clientseitige Transaktion einen Commit ausgeführt und die Message Queuing-Warteschlange transaktional ist. Dies ist der normalerweise standardmäßig eingerichtete Standard. Wenn die Transaktionsattributeinstellung Neu erforderlich ist, Message Queuing die Nachricht auch dann akzeptieren, wenn die clientseitige Transaktion abgebrochen wird. Weitere Informationen zu Transaktionen finden Sie unter [Transactional Message Queuing](transactional-message-queuing.md).

## <a name="the-listener"></a>Der Listener

Der Listener für komponenten in der Warteschlange ruft die Nachricht aus der Warteschlange ab und übergibt sie an den Player für komponenten in der Warteschlange.

## <a name="the-player"></a>Der Player

Der Player demarshaliert den Sicherheitskontext des Clients auf serverseitiger Seite, ruft dann die Serverkomponente auf und sendet die gleichen Methodenaufrufe. Die Methodenaufrufe werden erst dann vom Player abgespielt, wenn die Clientkomponente abgeschlossen ist und die Transaktion, die die Methode aufgezeichnet hat, Commits aufruft.

## <a name="the-message-mover"></a>Der Nachrichten-Mover

Der Message Mover für Warteschlangenkomponenten ist ein Hilfsprogramm, das alle fehlerhaften Message Queuing aus einer Warteschlange in eine andere verschiebt, damit sie wiederholt werden können. Das Nachrichten-Mover-Hilfsprogramm ist ein Automation-Objekt, das mit einem VBScript aufgerufen werden kann. Weitere Informationen finden Sie unter [Behandeln von Fehlern.](handling-errors-in-queued-components.md)

 

 



