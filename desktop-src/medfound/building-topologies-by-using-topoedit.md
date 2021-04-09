---
description: Entwickeln von Topologien mithilfe von topoedit
ms.assetid: 04173f3d-3722-48ee-a6fb-9cdb2a897a33
title: Entwickeln von Topologien mithilfe von topoedit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92758911113c7500cb13fa814d07321435fafeb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128000"
---
# <a name="building-topologies-by-using-topoedit"></a>Entwickeln von Topologien mithilfe von topoedit

Eine Topologie muss über die folgenden drei Knoten verfügen:

-   Quellknoten: die Datenströme aus einer Mediendatei, die als Quelle für die Topologie verwendet werden.
-   Transformations Knoten: eine Media Foundation Transformation (MFT). Diese Knoten sind in der Regel Encoder, Decoder und Effekte für die Topologie.
-   Ausgabe Knoten: die streamsenke, die die Mediendaten, Video Frames oder Audiostreams zur Wiedergabe an die Medien Sitzung übergibt.

Weitere Informationen zur topologiestruktur finden Sie unter Informationen [zu Topologien](about-topologies.md).

Zum Erstellen einer Topologie müssen Sie die Knoten hinzufügen, die Knoten verbinden und die Topologie auflösen, damit Sie wiedergegeben werden kann.

Topologieknoten werden als Felder mit Text angezeigt, der den Namen des Knotens anzeigt. Grüne Felder stellen die Knoten dar, die vom Benutzer hinzugefügt werden. Wenn eine Topologie aufgelöst wird, kann topoedit der Topologie automatisch Transformations Knoten hinzufügen. Diese werden im **Topologiebereich** als blaue Felder angezeigt.

Topologieeingaben und-Ausgaben werden als schwarze Quadrate entlang der Kante des Knotens dargestellt. Die *Knoten Eingabe* wird auf der linken Seite des Knotens angezeigt, und die *Knoten Ausgabe* befindet sich auf der rechten Seite des Knotens.

Die topologieknoten sind über eine *Knoten Verbindung* verbunden, die als schwarze Linie angezeigt wird, um die Knoten Eingabe eines Knotens mit der Knoten Ausgabe eines anderen Knotens zu verbinden.

Die folgende Abbildung zeigt eine verbundene Topologie für eine Audioquelle.

![Darstellung der Verbindungen vom Quellknoten zu zwei Transformations Knoten und dann zum Ausgabe Knoten](images/e94b4cce-aa8a-497f-94c2-cc9dace17291.gif)

Dieser Abschnitt enthält die folgenden Themen:



| Thema                                                                                          | BESCHREIBUNG                                                    |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Hinzufügen von Quellknoten mit topoedit](adding-source-nodes-with-topoedit.md)                     | Beschreibt den Prozess des Hinzufügens von Quellknoten zu einer Topologie.    |
| [Hinzufügen von Transformations Knoten mit topoedit](adding-transform-nodes-with-topoedit.md)               | Beschreibt den Prozess des Hinzufügens von Transformations Knoten zu einer Topologie. |
| [Hinzufügen von Ausgabe Knoten mit topoedit](adding-output-nodes-with-topoedit.md)                     | Beschreibt den Prozess des Hinzufügens von Ausgabe Knoten zu einer Topologie.    |
| [Verbinden von topologieknoten und Trennen der Verbindung](connecting-and-disconnecting-topology-nodes.md) | Beschreibt den Prozess zum Verbinden von zwei Knoten.                 |
| [Auflösen einer Topologie mit topoedit](resolving-a-topology-with-topoedit.md)                   | Beschreibt den Prozess der topologieauflösung.                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Topoedit](topoedit.md)
</dt> </dl>

 

 



