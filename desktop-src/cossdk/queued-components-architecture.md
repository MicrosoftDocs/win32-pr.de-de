---
description: Der von com+ in der Warteschlange befindliche Komponenten Dienst erweitert das COM-Programmiermodell durch Bereitstellen einer Umgebung, in der eine Komponente synchron (in Echtzeit) oder asynchron (in der Warteschlange) aufgerufen werden kann.
ms.assetid: fd455679-b2b3-487f-8494-9ea296ce2c89
title: Architektur der Warteschlangen Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8a2f6e1012bd3c11a27a44214ee28e84d5bd404
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104564554"
---
# <a name="queued-components-architecture"></a>Architektur der Warteschlangen Komponenten

Der von com+ in der Warteschlange befindliche Komponenten Dienst erweitert das COM-Programmiermodell durch Bereitstellen einer Umgebung, in der eine Komponente synchron (in Echtzeit) oder asynchron (in der Warteschlange) aufgerufen werden kann. Eine Komponente muss nicht wissen, ob Sie in einem echt Zeit-oder in einem Warteschlangen Kontext verwendet wird.

Messaging Anwendungen sind e-Mail-Transaktionen zwischen Programmen. Der Anforderer sendet eine Nachricht an den Server. Wenn der Server die Nachricht erhält, wird die Nachricht verarbeitet. Wie bei e-Mail auch, muss ein Messaging System die Netzwerk Details verarbeiten und sicherstellen, dass die Nachricht vom Client zum Server verschoben wird. Im Framework der in der Warteschlange befindlichen Komponenten ist Message Queuing dafür verantwortlich.

Der Dienst für die com+-Warteschlangen Komponenten besteht aus den folgenden Teilen:

-   Recorder (für die Client-oder Sendeseite)
-   Listener (für den Server oder die Empfangsseite)
-   Player (für die Server-oder Empfangsseite)

![Diagramm, das den Pfad vom Client zum Server anzeigt: Client, Recorder, Queue, Listener, Player, Server.](images/d732774b-1ca6-45ad-bce0-a95b0bfc3edb.png)

## <a name="the-recorder"></a>Der Recorder

In einem typischen Szenario mit in der Warteschlange befindlichen Komponenten ruft der Client eine in der Warteschlange befindliche Komponente auf. Der-Befehl wird an den in der Warteschlange befindlichen Komponenten Recorder ausgegeben, der ihn als Teil einer Nachricht an den Server verpackt und in eine Warteschlange einfügt. Die Aufzeichnung Marshalls den Sicherheitskontext des Clients in die Nachricht und zeichnet alle Methodenaufrufe des Clients auf. In seiner Rolle als Proxy für die Serverkomponente wählt die Aufzeichnung Schnittstellen aus den Warteschlangen fähigen Schnittstellen im com+-Katalog aus.

Eine Darstellung der Aufzeichnung wird an Message Queuing als Nachricht gesendet, die an einen Server gesendet werden soll. Wenn für die in der Warteschlange befindliche Komponente die Einstellung für das Transaktions Attribut erforderlich oder unterstützt festgelegt ist, akzeptiert Message Queuing nur dann die Übermittlung der Nachricht, wenn die Client seitige Transaktion einen Commit ausführt und die Message Queuing Warteschlange transaktional ist. Dies ist die Standardeinstellung. Wenn für die Einstellung des Transaktions Attributs neu erforderlich ist, kann Message Queuing die Nachricht auch dann akzeptieren, wenn die Client seitige Transaktion abgebrochen wird. Weitere Informationen zu Transaktionen finden Sie unter [transaktionale Message Queuing](transactional-message-queuing.md).

## <a name="the-listener"></a>Der Listener

Der in der Warteschlange befindliche Komponenten Listener Ruft die Nachricht aus der Warteschlange ab und übergibt sie an den Player der in der Warteschlange befindlichen Komponenten.

## <a name="the-player"></a>Der Player

Der Player gibt den Sicherheitskontext des Clients auf der Serverseite aus und ruft dann die Serverkomponente auf und führt die gleichen Methodenaufrufe aus. Die Methodenaufrufe werden vom Player nicht wiedergegeben, bis die Client Komponente abgeschlossen ist, und die Transaktion, die die Methode aufgezeichnet hat, führt Commits aus.

## <a name="the-message-mover"></a>Der Nachrichten Verschiebe Vorgang

Der Nachrichten Verschiebungsvorgang in der Warteschlange ist ein Hilfsprogramm, das alle fehlgeschlagenen Message Queuing Nachrichten aus einer Warteschlange in eine andere verschiebt, damit Sie wiederholt werden können. Das Hilfsprogramm für den Nachrichten Verschiebungsvorgang ist ein Automatisierungs Objekt, das mit einem VBScript aufgerufen werden kann. Weitere Informationen finden Sie unter [Behandeln von Fehlern](handling-errors-in-queued-components.md).

 

 



