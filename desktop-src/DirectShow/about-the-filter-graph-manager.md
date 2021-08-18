---
description: Informationen zum Filter Graph Manager
ms.assetid: a227539a-7f9a-4f8d-99fe-f9ab67df9ef4
title: Informationen zum Filter Graph Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38ce7c9c9af137853efba501cace7680b533c13994a559102fd08dc48efa2076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074864"
---
# <a name="about-the-filter-graph-manager"></a>Informationen zum Filter Graph Manager

Der [Filter Graph Manager](filter-graph-manager.md) ist ein COM-Objekt, das die Filter in einem Filterdiagramm steuert. Er führt viele Funktionen aus, einschließlich der folgenden:

-   Koordinieren von Zustandsänderungen zwischen den Filtern.
-   Einrichten einer Referenzuhr.
-   Kommunizieren von Ereignissen zurück an die Anwendung.
-   Bereitstellen von Methoden für Anwendungen zum Erstellen des Filterdiagramms.

Jede dieser Funktionen wird hier kurz beschrieben. Details finden Sie an anderer Stelle in der Dokumentation.

**Statusänderungen.** Zustandsänderungen innerhalb von Filtern müssen in einer bestimmten Reihenfolge erfolgen. Aus diesem Grund gibt die Anwendung keine Befehle zur Zustandsänderung direkt an die Filter aus. Stattdessen wird dem Filter-manager ein einzelner Befehl Graph, der den Befehl an jeden Filter verteilt. Suchen funktioniert auf ähnliche Weise: Die Anwendung gibt dem Filter-Graph-Manager einen Suchbefehl, der sie an die Filter verteilt.

**Referenzuhr**. Alle Filter im Diagramm verwenden dieselbe Uhr, die als *Verweisuhr bezeichnet wird.* Die Referenzuhr stellt sicher, dass alle Streams synchronisiert werden. Die Zeit, zu der ein Videoframe oder Audiobeispiel gerendert werden soll, wird als *Präsentationszeit bezeichnet.* Die Präsentationszeit wird relativ zur Referenzuhr gemessen. Der Filter Graph Manager wählt eine Referenzuhr aus, in der Regel entweder die Uhr auf der Soundkarte oder die Systemuhr.

**Graph Ereignisse .** Der Filter Graph-Manager verwendet eine Ereigniswarteschlange, um die Anwendung von Ereignissen zu informieren, die im Filterdiagramm auftreten. Dieser Mechanismus ähnelt einer nachrichtenschleife Windows Nachrichtenschleife.

**Graph-Building-Methoden**. Der Filter Graph-Manager stellt Methoden für die Anwendung zum Hinzufügen von Filtern zum Diagramm, zum Verbinden von Filtern mit anderen Filtern und zum Trennen von Filtern zur Seite.

Eine Funktion, die Graph-Manager nicht verarbeitet, ist das Verschieben von Daten von einem Filter in den nächsten. Dies erfolgt durch die Filter selbst über ihre Stecknadelverbindungen. Die Verarbeitung erfolgt immer in einem separaten Thread.

> [!Note]  
> Filter sind immer Freethreading, befinden sich im gleichen Prozess wie der Filter Graph Manager und werden von Prozessservern geladen. Daher werden Methodenaufrufe nicht zwischen Filtern oder zwischen Filtern und dem Filter Graph Manager gemarshallt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Daten Flow im Filter-Graph](data-flow-in-the-filter-graph.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Festlegen der Graph Uhr](setting-the-graph-clock.md)
</dt> <dt>

[Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



