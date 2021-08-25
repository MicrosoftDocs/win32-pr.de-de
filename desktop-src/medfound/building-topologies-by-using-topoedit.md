---
description: Erstellen von Topologien mit TopoEdit
ms.assetid: 04173f3d-3722-48ee-a6fb-9cdb2a897a33
title: Erstellen von Topologien mit TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88e678e0c25cbfe56c2633091820468a6c0313663847870a4de5c912a5edae95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959435"
---
# <a name="building-topologies-by-using-topoedit"></a>Erstellen von Topologien mit TopoEdit

Eine Topologie muss über die folgenden drei Knoten verfügen:

-   Quellknoten: Die Datenströme aus einer Mediendatei, die als Quelle für die Topologie verwendet werden.
-   Transformationsknoten: Eine Media Foundation Transformation (MFT). Diese Knoten sind in der Regel Encoder, Decoder und Effekte für die Topologie.
-   Ausgabeknoten: Die Streamsenke, die die Mediendaten, Videoframes oder Audiostreams zur Wiedergabe an die Mediensitzung übergibt.

Informationen zur Topologiestruktur finden Sie unter [Informationen zu Topologien.](about-topologies.md)

Um eine Topologie zu erstellen, müssen Sie die Knoten hinzufügen, die Knoten verbinden und die Topologie auflösen, damit sie abgespielt werden kann.

Topologieknoten werden als Felder angezeigt, und text zeigt den Namen des Knotens an. Grüne Felder stellen die Knoten dar, die vom Benutzer hinzugefügt werden. Wenn eine Topologie aufgelöst wird, kann TopoEdit der Topologie automatisch Transformationsknoten hinzufügen. Diese werden im Topologiebereich als **blaue Felder angezeigt.**

Topologieeingaben und -ausgaben werden durch als schwarze Quadrate am Rand des Knotens dargestellt. Die *Knoteneingabe* wird auf der linken Seite  des Knotens angezeigt, und die Knotenausgabe befindet sich auf der rechten Seite des Knotens.

Die Topologieknoten werden über  eine Knotenverbindung verbunden, die als schwarze Linie angezeigt wird und die Knoteneingabe eines Knotens mit der Knotenausgabe eines anderen Knotens verbindet.

Die folgende Abbildung zeigt eine verbundene Topologie für eine Audioquelle.

![Abbildung: Verbindungen vom Quellknoten, zu zwei Transformationsknoten und dann zum Ausgabeknoten](images/e94b4cce-aa8a-497f-94c2-cc9dace17291.gif)

Dieser Abschnitt enthält die folgenden Themen:



| Thema                                                                                          | Beschreibung                                                    |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Hinzufügen von Quellknoten mit TopoEdit](adding-source-nodes-with-topoedit.md)                     | Beschreibt den Prozess des Hinzufügens von Quellknoten zu einer Topologie.    |
| [Hinzufügen von Transformationsknoten mit TopoEdit](adding-transform-nodes-with-topoedit.md)               | Beschreibt den Prozess des Hinzufügens von Transformationsknoten zu einer Topologie. |
| [Hinzufügen von Ausgabeknoten mit TopoEdit](adding-output-nodes-with-topoedit.md)                     | Beschreibt den Prozess des Hinzufügens von Ausgabeknoten zu einer Topologie.    |
| [Verbinden und Trennen von Topologieknoten](connecting-and-disconnecting-topology-nodes.md) | Beschreibt den Prozess zum Verbinden von zwei Knoten.                 |
| [Auflösen einer Topologie mit TopoEdit](resolving-a-topology-with-topoedit.md)                   | Beschreibt den Prozess der Topologieauflösung.                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



