---
description: Informationen zum Filter Graph-Manager
ms.assetid: a227539a-7f9a-4f8d-99fe-f9ab67df9ef4
title: Informationen zum Filter Graph-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedf716b84ee62818e323bfaa082b6252e5faad0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522240"
---
# <a name="about-the-filter-graph-manager"></a>Informationen zum Filter Graph-Manager

Der [Filter Graph-Manager](filter-graph-manager.md) ist ein COM-Objekt, mit dem die Filter in einem Filter Diagramm gesteuert werden. Sie führt viele Funktionen aus, einschließlich der folgenden:

-   Koordinieren von Zustandsänderungen zwischen den Filtern.
-   Einrichten einer verweisuhr.
-   Ereignisse werden zurück an die Anwendung übermittelt.
-   Bereitstellen von Methoden für Anwendungen zum Erstellen des Filter Diagramms.

Jede dieser Funktionen wird hier kurz beschrieben. Details finden Sie an anderer Stelle in der Dokumentation.

**Statusänderungen**. Zustandsänderungen innerhalb von Filtern müssen in einer bestimmten Reihenfolge erfolgen. Daher gibt die Anwendung keine Status Änderungs Befehle direkt an die Filter aus. Stattdessen wird dem Filter Graph-Manager ein einziger Befehl erteilt, der den Befehl an jeden Filter verteilt. Die Suche funktioniert auf ähnliche Weise: die Anwendung gibt dem Filter Graph-Manager einen Suchbefehl, der Sie an die Filter verteilt.

Die **Referenzuhr**. Alle Filter im Diagramm verwenden dieselbe Uhr, die als *Referenzuhr* bezeichnet wird. Die Referenzuhr stellt sicher, dass alle Streams synchronisiert werden. Die Uhrzeit, zu der ein Video Frame oder ein Audiobeispiel gerendert werden soll, wird als *Präsentationszeit* bezeichnet. Die Präsentationszeit wird relativ zur Referenzuhr gemessen. Der Filter Graph-Manager wählt eine Referenzuhr aus, normalerweise entweder die Uhr auf der Soundkarte oder die Systemuhr.

**Graph-Ereignisse**. Der Filter Graph-Manager verwendet eine Ereignis Warteschlange, um die Anwendung über Ereignisse zu informieren, die im Filter Diagramm auftreten. Dieser Mechanismus ähnelt einer Windows-Nachrichten Schleife.

**Graph-erbauungsmethoden**. Der Filter Graph-Manager bietet Methoden für die Anwendung zum Hinzufügen von Filtern zum Diagramm, zum Verbinden von Filtern mit anderen Filtern und zum Trennen von Filtern.

Eine Funktion, die der Filter Graph-Manager nicht verarbeitet, ist das Verschieben von Daten von einem Filter zum nächsten. Dies erfolgt durch die Filter selbst über die PIN-Verbindungen. Die Verarbeitung erfolgt immer in einem separaten Thread.

> [!Note]  
> Filter sind immer frei, wenn Sie sich im gleichen Prozess wie der Filter Graph-Manager befinden und aus Prozess internen Servern geladen werden. Daher werden Methodenaufrufe nicht zwischen Filtern oder zwischen Filtern und dem Filter Diagramm-Manager gemarshallt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenfluss im Filter Diagramm](data-flow-in-the-filter-graph.md)
</dt> <dt>

[Ereignis Benachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Festlegen der diagrammuhr](setting-the-graph-clock.md)
</dt> <dt>

[Uhrzeit und Uhren in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



