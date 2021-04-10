---
description: Die Light Type-Eigenschaft definiert, welche Art von Lichtquelle Sie verwenden.
ms.assetid: 7718383a-6e49-4ad2-acc1-fc8fec0d4844
title: Helle Typen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ae2c7fd5380b0f604181f36d784afe3f3fc3ff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041112"
---
# <a name="light-types-direct3d-9"></a>Helle Typen (Direct3D 9)

Die Light Type-Eigenschaft definiert, welche Art von Lichtquelle Sie verwenden. Der Light-Typ wird mithilfe eines Werts aus der [**D3DLIGHTTYPE**](./d3dlighttype.md) C++-Enumeration im Typmember der [**D3DLIGHT9**](d3dlight9.md) -Struktur des Lichts festgelegt. Es gibt drei Arten von Beleuchtung in Direct3D-Point-Lichtern,-Schein vorlichtern und direktionalen Lichtern. Jeder Typ beleuchtet Objekte in einer Szene mit unterschiedlichen Ebenen des Rechen Aufwands.

## <a name="point-light"></a>Punktuelles Licht

Punkt Leuchten haben Farbe und Position innerhalb einer Szene, aber keine Richtung. Sie lassen das Licht in alle Richtungen gleichermaßen aus, wie in der folgenden Abbildung dargestellt.

![Abbildung der Punktbeleuchtung](images/ptlight.png)

Eine Glühbirne ist ein gutes Beispiel für ein Punktlicht. Die Punktbeleuchtung ist von der Dämpfung und dem Bereich betroffen und beleuchtet ein Mesh auf der Grundlage von Scheitel Punkten. Während der Beleuchtung verwendet Direct3D die Position des Punkt Lichts im Raum und die Koordinaten des Vertex, die beleuchtet werden, um einen Vektor für die Richtung des Lichts abzuleiten, und die Entfernung, die das Licht bewegt hat. Beide werden zusammen mit dem Scheitelpunkt normal verwendet, um den Anteil des Lichts zur Beleuchtung der Oberfläche zu berechnen.

## <a name="directional-light"></a>Gerichtetes Licht

Direktionale Beleuchtung haben nur Farbe und Richtung, nicht Position. Sie geben parallele Beleuchtung aus. Dies bedeutet, dass alle durch direktionale Beleuchtung generierten Licht durch eine Szene in derselben Richtung laufen. Stellen Sie sich ein Direktionales Licht als Lichtquelle in nahezu unbegrenzter Entfernung vor, z. b. die Sonne. Direktionale Lichter sind von der Dämpfung oder dem Bereich nicht betroffen, sodass die von Ihnen angegebene Richtung und Farbe die einzigen Faktoren sind, die berücksichtigt werden, wenn Direct3D die Scheitelpunkt Farben berechnet. Aufgrund der geringen Anzahl von Beleuchtungs Faktoren sind dies die am wenigsten rechenintensiven Beleuchtung.

## <a name="spotlight"></a>Gerückt

Die Scheinwerfer haben Farbe, Position und Richtung, in der Sie Licht ausgeben. Das Licht, das von einem Spotlight ausgegeben wird, besteht aus einem hellen inneren Kegel und einem größeren äußeren Kegel, wobei die helle Intensität zwischen den beiden absinkt, wie in der folgenden Abbildung dargestellt.

![Abbildung eines Spotlight mit einem inneren Kegel und einem äußeren Kegel](images/spotlt.png)

Die Scheinwerfer sind von der Zuordnung, der Dämpfung und dem Bereich betroffen. Diese Faktoren und die Entfernungs Beleuchtung werden zu jedem Scheitelpunkt bewegt, wenn die Beleuchtungseffekte für Objekte in einer Szene berechnet werden. Wenn Sie diese Effekte für jeden Scheitelpunkt berechnen, werden die Lichter von allen Lichtern in Direct3D am Rechen stärksten beansprucht.

Die [**D3DLIGHT9**](d3dlight9.md) C++-Struktur enthält drei Member, die nur von-Schein Bern verwendet werden. Diese Member (fzuweisung, THTA und Phi) steuern, wie groß oder klein die inneren und äußeren Kegel eines Spotlight-Objekts sind, und wie sich das Licht zwischen Ihnen verringert.

Der Wert von "Teta" ist der radierwinkel des inneren Kegel des Spotlight, und der "Phi"-Wert ist der Winkel für den äußeren Lichtkegel. Der Wert "f-Wert" steuert, wie sich die Lichtintensität zwischen dem äußeren Rand des inneren Kegel und dem inneren Rand des äußeren Kegel absinkt. In den meisten Anwendungen wird fzuweisung auf 1,0 festgelegt, um fzuweisung zu erstellen, die gleichmäßig zwischen den beiden Kegeln erfolgt. Sie können jedoch auch andere Werte festlegen.

In der folgenden Abbildung wird die Beziehung zwischen den Werten für diese Member und deren Auswirkung auf die innere und äußere Ampel eines Spotlight gezeigt.

![Abbildung der Beziehung der Werte von "Phi" und "-TA" zu den Spotlight-Kegeln](images/spotlt2.png)

Die Scheinwerfer geben einen Lichtkegel aus, der aus zwei Teilen besteht: einem hellen inneren Kegel und einem äußeren Kegel. Light ist am besten im Inneren Kegel und nicht außerhalb des äußeren Kegel vorhanden, und die Lichtintensität wird zwischen den beiden Bereichen abgeschwächt. Diese Art der Dämpfung wird häufig als fzuweisung bezeichnet.

Die Menge an Licht, die ein Scheitelpunkt empfängt, basiert auf der Position des Scheitel Punkts im Inneren oder äußeren Kegel. Direct3D berechnet das Punktprodukt für den Richtungsvektor (L) des Spotlight und den Vektor vom Licht bis zum Scheitelpunkt (D). Dieser Wert entspricht dem Kosinus des Winkels zwischen den beiden Vektoren und fungiert als Indikator für die Position des Scheitel Punkts, der mit den Kegel Winkeln des Lichts verglichen werden kann, um zu bestimmen, wo sich der Scheitelpunkt im Inneren oder äußeren Kegel befinden könnte. Die folgende Abbildung stellt eine grafische Darstellung der Zuordnung zwischen diesen beiden Vektoren bereit.

![Abbildung des Fokus für Spotlight-Richtung und des Vektors vom Scheitelpunkt bis zum Spotlight](images/spotalg1.png)

Das System vergleicht diesen Wert mit dem Kosinus der inneren und äußeren Kegelwinkel des Spotlight. In der [**D3DLIGHT9**](d3dlight9.md) -Struktur des Lichts stellen die Member "-" und "Phi" die gesamtkegel Winkel für die inneren und äußeren Kegel dar. Da die Dämpfung auftritt, während der Scheitelpunkt vom Mittelpunkt der Beleuchtung entfernt wird (anstatt über den gesamten Kegelwinkel), dividiert die Common Language Runtime diese Kegelwinkel in der Hälfte, bevor Sie Ihre kosinen berechnen.

Wenn das Punktprodukt der Vektoren L und D kleiner als oder gleich dem Kosinus des äußeren Kegel Winkels ist, liegt der Scheitelpunkt hinter dem äußeren Kegel und empfängt kein Licht. Wenn das Punktprodukt von L und D größer als der Kosinus des inneren Kegel Winkels ist, befindet sich der Scheitelpunkt innerhalb des inneren Kegel und empfängt die maximale Menge an Licht, wobei immer noch die Dämpfung der Entfernung in Erwägung gezogen wird. Wenn sich der Scheitelpunkt zwischen den beiden Regionen befindet, wird "f-Zuweisung" mit der folgenden Gleichung berechnet.

![Formel für helle Intensität bei Scheitelpunkt nach der Zuordnung](images/falloff.png)

Hierbei gilt:

-   I <sub>f</sub> ist eine leichte Intensität nach der Zuordnung
-   Alpha ist der Winkel zwischen den Vektoren L und D.
-   Die-TA ist der innere Kegelwinkel.
-   Phi ist der äußere Kegelwinkel.
-   p ist die Zuordnung

Mit dieser Formel wird ein Wert zwischen 0,0 und 1,0 generiert, mit dem die Intensität des Lichts im Scheitelpunkt für die Zuordnung von fzuweisung skaliert wird. Die Dämpfung als Faktor der Entfernung des Scheitel Punkts vom Licht wird ebenfalls angewendet. Das folgende Diagramm zeigt, wie sich verschiedene Werte für die Zuordnung von Werten auf die Zuordnung der logischen Zuordnung auswirken können.

![Diagramm der Lichtintensität im Vergleich zum Scheitelpunkt Abstand vom Licht](images/fallgraf.png)

Die Auswirkungen verschiedener Werte für die Zuordnung von Werten auf die eigentliche Beleuchtung sind geringfügig, und es wird eine geringe Leistungs Einbuße entstehen, indem die Zuordnung der logischen Zuordnung mit anderen Werten als 1,0 für die Zuordnung von Werten erfolgt. Aus diesen Gründen wird dieser Wert normalerweise auf 1,0 festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beleuchtung und Materialien](lights-and-materials.md)
</dt> </dl>

 

 
