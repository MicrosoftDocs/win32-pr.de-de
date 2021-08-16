---
description: Vorteile der Warteschlangenverarbeitung
ms.assetid: dc1fc03f-1e2c-481c-95a7-f8d7b1e06bb0
title: Vorteile der Warteschlangenverarbeitung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02c41d902d9e72af40b70ccc95efe33e2857c8ef07953c70ef1fc0879ba676ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308784"
---
# <a name="benefits-of-queued-processing"></a>Vorteile der Warteschlangenverarbeitung

Beim Entwerfen neuer Anwendungen müssen Entwickler die Auswirkungen der Codierungskomponenten auf die (synchrone) Echtzeitverarbeitung und die Warteschlangenverarbeitung (asynchron) berücksichtigen. Die Auswahl hängt von den Anforderungen der jeweiligen Anwendung ab, die von der zugrunde liegenden Geschäftslogik bestimmt werden. Als Richtlinie bietet die Warteschlangenverarbeitung gegenüber der Echtzeitverarbeitung die folgenden Vorteile:

-   Geringere Abhängigkeit von der Komponentenverfügbarkeit
-   Kürzere Lebensdauer von Komponenten
-   Unterbrechungsfreie Produktivität bei Verwendung getrennter Anwendungen
-   Nachrichtenzuverlässigkeit
-   Effiziente Serverplanung

## <a name="component-availability"></a>Komponentenverfügbarkeit

Wenn in einer Echtzeitverarbeitungsanwendung nur eine Komponente der Transaktion nicht verfügbar ist – möglicherweise aufgrund von Serverüberladungen oder Netzwerkproblemen –, wird der gesamte Prozess blockiert und kann nicht abgeschlossen werden. Im Gegensatz dazu trennt eine Anwendung, die den COM+-Dienst für komponenten in der Warteschlange verwendet, die Transaktion in Aktivitäten, die jetzt abgeschlossen werden müssen, und solche, die zu einem späteren Zeitpunkt abgeschlossen werden können. Beispielsweise können Nachrichten zur späteren Verarbeitung in die Warteschlange gestellt werden, damit die anfordernde Komponente für andere Aufgaben frei ist.

## <a name="component-lifetimes"></a>Lebensdauer von Komponenten

Eine Anwendung, die den Dienst für Komponenten in der Warteschlange verwendet, ermöglicht der Serverkomponente, unabhängig vom Client zu arbeiten. Daher können Serverkomponenten schneller abgeschlossen werden. In einem Echtzeitsystem ist die Serverkomponente von dem Zeitpunkt, zu dem sie erstellt wird, bis zum Ende der Entität des Objekts vorhanden. Der Server wartet darauf, dass der Client Methodenaufrufe sendet und Ergebnisse zurückgegeben werden. Dies negiert das schnelle Durchfahren von Serverobjekten und schränkt die Serverskalierbarkeit ein.

## <a name="disconnected-applications"></a>Nicht verbundenen Anwendungen

Die zunehmende Verwendung von Laptops, Notebooks und Handflächencomputern hat die Notwendigkeit von Anwendungen geschaffen, die gelegentlich getrennte Clients oder mobile Benutzer bedienen. In einem System in der Warteschlange können diese Benutzer in einem nicht verbundenen Szenario oder ohne Verbindung mit dem Server weiterhin arbeiten, und sie können später eine Verbindung mit den Datenbanken oder Servern herstellen, um ihre Anforderungen zu verarbeiten. Beispielsweise kann ein Vertriebsmitarbeiter Bestellungen von Kunden übernehmen und später eine Verbindung mit der Versandabteilung herstellen, um diese Bestellungen zu verarbeiten.

Wenn Sie über eine Komponente verfügen, die entweder verbunden oder getrennt ausgeführt werden kann, werden Nachrichten in eine Richtung gesendet, und es ist selten notwendig, hin und her zu wechseln. Beispielsweise empfängt die Versandkomponente im Auftragsszenario die Nachricht und verarbeitet sie. Möglicherweise wird eine weitere Komponente für die Abrechnung oder Überwachung generiert. Der Client committ, bevor der Server überhaupt gestartet wird. Die Nachricht wird erst gesendet, wenn ein Commit für die Anwendung besteht.

Die folgende Abbildung zeigt den Informationsfluss in einem nicht verbundenen Szenario.

![Diagramm, das den Informationsfluss zwischen Client und Server zeigt.](images/b1818188-0294-4bd8-8bbe-9fe8eea9e09a.png)

## <a name="message-reliability"></a>Nachrichtenzuverlässigkeit

Message Queuing ist ein leistungsstarkes Tool, das Datenbanktechniken verwendet, um Daten auf stabile Weise zu schützen. Im Falle eines Serverfehlers stellt Message Queuing sicher, dass für Transaktionen ein Rollback ausgeführt wird, damit Nachrichten nicht verloren gehen und daten nicht beschädigt werden.

## <a name="server-scheduling"></a>Serverplanung

Eine Anwendung, die Komponenten in der Warteschlange verwendet, eignet sich gut für die Zeitverschiebung der Komponentenausführung, die unkritische Arbeit auf einen zeitraumswechselten Zeitraum verschiebt. Dies ist dasselbe nützliche Konzept, das auch auf die herkömmliche Batchmodusverarbeitung angewendet wurde. Ähnliche Anforderungen können für die zusammenhängende Ausführung durch den Server verzögert werden, anstatt dass der Server sofort auf eine Vielzahl von Anforderungen reagieren muss.

 

 



