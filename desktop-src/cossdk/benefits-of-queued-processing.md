---
description: Vorteile der Verarbeitung in der Warteschlange
ms.assetid: dc1fc03f-1e2c-481c-95a7-f8d7b1e06bb0
title: Vorteile der Verarbeitung in der Warteschlange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a0d2068d70ecf611ec334632c8b8f819319ef3
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "104550815"
---
# <a name="benefits-of-queued-processing"></a>Vorteile der Verarbeitung in der Warteschlange

Beim Entwerfen neuer Anwendungen müssen Entwickler die Auswirkungen der Codierungs Komponenten auf eine (synchrone) Echtzeitverarbeitung und eine in der Warteschlange eingereihte (asynchrone) Verarbeitung in Erwägung gezogen. Die Auswahl hängt von den Anforderungen der jeweiligen Anwendung ab, die von der zugrunde liegenden Geschäftslogik bestimmt werden. Als Richtlinie bietet die Verarbeitung in der Warteschlange die folgenden Vorteile gegenüber der Echtzeitverarbeitung:

-   Reduzierte Abhängigkeit von Verfügbarkeit der Komponente
-   Kürzere Lebensdauer von Komponenten
-   Ununterbrochene Produktivität bei der Verwendung von getrennten Anwendungen
-   Nachrichten Zuverlässigkeit
-   Effiziente Server Planung

## <a name="component-availability"></a>Komponenten Verfügbarkeit

Wenn in einer echt Zeit Verarbeitungs Anwendung nur eine Komponente der Transaktion verfügbar ist – möglicherweise aufgrund von Serverüberlastung oder Netzwerkproblemen – wird der gesamte Prozess blockiert und kann nicht abgeschlossen werden. Im Gegensatz dazu trennt eine Anwendung, die den com+-Warteschlangen Dienst in der Warteschlange verwendet, die Transaktion in Aktivitäten, die jetzt abgeschlossen werden müssen, und die, die zu einem späteren Zeitpunkt abgeschlossen werden können. Beispielsweise können Nachrichten zur späteren Verarbeitung in die Warteschlange eingereiht werden, damit die anfordernde Komponente für andere Aufgaben frei ist.

## <a name="component-lifetimes"></a>Lebensdauer von Komponenten

Eine Anwendung, die den Dienst für in der Warteschlange befindliche Komponenten verwendet, ermöglicht die unabhängige Funktionsweise der Serverkomponente. Daher können Serverkomponenten schneller ausgeführt werden. In einem Echtzeitsystem ist die Serverkomponente ab dem Zeitpunkt vorhanden, zu dem Sie erstellt wird, bis das Objekt schließlich freigegeben wird. Der Server wartet, bis der Client Methodenaufrufe durchführt und Ergebnisse zurückgegeben werden, die das schnelle Radfahren von Server Objekten negiert und die Server Skalierbarkeit einschränkt.

## <a name="disconnected-applications"></a>Nicht verbundene Anwendungen

Durch die zunehmende Verwendung von Laptops, Notebooks und Palmen Computern wurde eine Anforderung für Anwendungen hergestellt, die gelegentlich nicht verbundene Clients oder mobile Benutzer bedienen. In einem in der Warteschlange befindlichen System können diese Benutzer weiterhin in einem getrennten Szenario arbeiten oder wenn Sie nicht mit dem Server verbunden sind. Sie können später eine Verbindung mit den Datenbanken oder Servern herstellen, um Ihre Anforderungen zu verarbeiten. Beispielsweise kann ein Vertriebsmitarbeiter Bestellungen von Kunden nehmen und später eine Verbindung mit der Versandabteilung herstellen, um diese Bestellungen zu verarbeiten.

Wenn Sie über eine Komponente verfügen, die entweder verbunden oder getrennt ausgeführt werden kann, werden Nachrichten in eine Richtung verschoben, und es ist selten notwendig, hin und her zu wechseln. Beispielsweise empfängt die Liefer Komponente im Bestell Szenario die Nachricht und verarbeitet sie. Möglicherweise wird eine andere Komponente für die Abrechnung oder Überwachung generiert. Der Client führt einen Commit aus, bevor der Server jemals gestartet wird. Die Nachricht wird erst gesendet, wenn die Anwendung einen Commit ausführt.

Die folgende Abbildung zeigt den Informationsfluss in einem getrennten Szenario.

![Diagramm, das den Informationsfluss zwischen Client und Server anzeigt.](images/b1818188-0294-4bd8-8bbe-9fe8eea9e09a.png)

## <a name="message-reliability"></a>Nachrichten Zuverlässigkeit

Message Queuing ist ein leistungsfähiges Tool, das Daten Bank Techniken verwendet, um Daten auf robuste Weise zu schützen. Bei einem Server Fehler stellt Message Queuing sicher, dass für die Transaktionen ein Rollback ausgeführt wird, sodass keine Nachrichten verloren gehen und die Daten nicht beschädigt sind.

## <a name="server-scheduling"></a>Server Planung

Eine Anwendung, die in der Warteschlange befindliche Komponenten verwendet, eignet sich gut für die Zeit Verschiebe Ausführung von Komponenten, bei der unkritische Arbeit auf einen außerhalb der Spitzenzeiten beschränkt wird. Dabei handelt es sich um dasselbe nützliche Konzept, das auf die herkömmliche Verarbeitung im Batch Modus angewendet wurde. Ähnliche Anforderungen können für eine zusammenhängende Ausführung durch den Server verzögert werden, anstatt dass der Server sofort auf eine Vielzahl von Anforderungen reagieren muss.

 

 



