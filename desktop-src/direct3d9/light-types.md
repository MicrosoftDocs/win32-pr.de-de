---
description: Die Light Type-Eigenschaft definiert, welche Art von Lichtquelle Sie verwenden.
ms.assetid: 7718383a-6e49-4ad2-acc1-fc8fec0d4844
title: Light Types (Direct3D 9) (Lichttypen (Direct3D 9))
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd451fcf45e67f1d789b7481fcc1884282d2018db98ab26d27481bec5277031
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674418"
---
# <a name="light-types-direct3d-9"></a>Light Types (Direct3D 9) (Lichttypen (Direct3D 9))

Die Light Type-Eigenschaft definiert, welche Art von Lichtquelle Sie verwenden. Der Lichttyp wird mithilfe eines Werts aus der C++-Enumeration [**D3DLIGHTTYPE**](./d3dlighttype.md) im Type-Member der [**D3DLIGHT9-Struktur des Lichts**](d3dlight9.md) festgelegt. Es gibt drei Arten von Licht in Direct3D: Punktlichter, Spotlights und direktionale Beleuchtung. Jeder Typ überleert Objekte in einer Szene auf unterschiedliche Weise mit unterschiedlichem Rechenaufwand.

## <a name="point-light"></a>Punktuelles Licht

Punktlichter haben Farbe und Position innerhalb einer Szene, aber keine einzelne Richtung. Sie geben Licht gleichmäßig in alle Richtungen aus, wie in der folgenden Abbildung dargestellt.

![Abbildung des Punktlichts](images/ptlight.png)

Eine Glühbirne ist ein gutes Beispiel für ein Punktlicht. Punktlichter sind von Dämpfung und Bereich betroffen und beleuchten ein Gitternetz auf Scheitelpunkt-zu-Vertex-Basis. Während der Beleuchtung verwendet Direct3D die Position des Punktlichts im Raum und die Koordinaten des scheitelpunktbasierten Lichts, um einen Vektor für die Richtung des Lichts und den Abstand des Lichts zu ableiten. Beide werden zusammen mit dem Scheitelpunkt normal verwendet, um den Anteil des Lichts an der Oberfläche zu berechnen.

## <a name="directional-light"></a>Gerichtetes Licht

Richtungslichter haben nur Farbe und Richtung, nicht Position. Sie geben paralleles Licht aus. Dies bedeutet, dass das von direktionalen Lichten erzeugte Licht durch eine Szene in der gleichen Richtung bewegt wird. Imagine ein direktionales Licht als Lichtquelle in nahezu unendlicher Entfernung, z. B. bei der Solange. Richtungslichter sind nicht von der Dämpfung oder dem Bereich betroffen, sodass die von Ihnen angegebenen Richtungen und Farben die einzigen Faktoren sind, die berücksichtigt werden, wenn Direct3D Scheitelpunktfarben berechnet. Aufgrund der geringen Anzahl von Lichtfaktoren sind dies die am wenigsten rechenintensiven Beleuchtungen, die verwendet werden müssen.

## <a name="spotlight"></a>Spotlight

Spotlights weisen Farbe, Position und Richtung auf, in der sie Licht geben. Das von einem Blickpunkt ausgegebene Licht besteht aus einem hellen inneren Kegel und einem größeren äußeren Kegel, bei dem die Lichtstärke zwischen den beiden abnimmt, wie in der folgenden Abbildung dargestellt.

![Abbildung eines Blickpunkts mit einem inneren Kegel und einem äußeren Kegel](images/spotlt.png)

Spotlights sind von Falloff, Dämpfung und Bereich betroffen. Diese Faktoren und die Entfernung, die lichtversatzt, werden beim Berechnen von Beleuchtungseffekten für Objekte in einer Szene berücksichtigt. Die Berechnung dieser Effekte für jeden Scheitelpunkt macht Spotlights am rechenintensivsten aller Lichtlichter in Direct3D.

Die [**C++-Struktur D3DLIGHT9**](d3dlight9.md) enthält drei Member, die nur von Spotlights verwendet werden. Diese Member – Falloff, Theta und Phi – steuern, wie groß oder klein die inneren und äußeren Kegel eines Spotlightobjekts sind und wie das Licht zwischen ihnen abnimmt.

Der Theta-Wert ist der Bogenwinkel des inneren Kegels des Blickpunkts, und der Phi-Wert ist der Winkel für den äußeren Lichtkegel. Der Falloffwert steuert, wie die Lichtstärke zwischen dem äußeren Rand des inneren Kegels und dem inneren Rand des äußeren Kegels abnimmt. Die meisten Anwendungen legen Falloff auf 1.0 fest, um einen Falloff zu erstellen, der gleichmäßig zwischen den beiden Kegeln auftritt, aber Sie können bei Bedarf andere Werte festlegen.

Die folgende Abbildung zeigt die Beziehung zwischen den Werten für diese Member und wie sie sich auf die inneren und äußeren Lichtkegel eines Blickpunkts auswirken können.

![Abbildung, wie sich die Phi- und Theta-Werte auf die Spotlight-Kegel beziehen](images/spotlt2.png)

Spotlights geben einen Lichtkegel aus, der aus zwei Teilen besteht: einem hellen inneren Kegel und einem äußeren Kegel. Das Licht ist im inneren Kegel hellsten und außerhalb des äußeren Kegels nicht vorhanden, und die Lichtstärke wird zwischen den beiden Bereichen abgedämpft. Diese Art der Dämpfung wird häufig als Falloff bezeichnet.

Die Lichtmenge, die ein Scheitelpunkt empfängt, basiert auf der Position des Scheitelpunkts in den inneren oder äußeren Kegeln. Direct3D berechnet das Punktprodukt des Richtungsvektors (L) des Blickpunkts und den Vektor vom Licht zum Scheitelpunkt (D). Dieser Wert entspricht dem Kosinus des Winkels zwischen den beiden Vektoren und dient als Indikator für die Position des Scheitelpunkts, der mit den Kegelwinkeln des Lichts verglichen werden kann, um zu bestimmen, wo sich der Scheitelpunkt in den inneren oder äußeren Kegeln befindet. Die folgende Abbildung zeigt eine grafische Darstellung der Zuordnung zwischen diesen beiden Vektoren.

![Abbildung des Blickpunktrichtungsvektors und des Vektors vom Scheitelpunkt zum Blickpunkt](images/spotalg1.png)

Das System vergleicht diesen Wert mit dem Kosinus der inneren und äußeren Kegelwinkel des Blickpunkts. In der [**D3DLIGHT9-Struktur**](d3dlight9.md) des Lichts stellen die Theta- und Phi-Member die gesamten Kegelwinkel für die inneren und äußeren Kegel dar. Da die Dämpfung auftritt, wenn der Scheitelpunkt vom Mittelpunkt des Lichts entfernt wird (und nicht über den gesamten Kegelwinkel), teilt die Laufzeit diese Kegelwinkel vor der Berechnung ihrer Kosinus in die Hälfte auf.

Wenn das Punktprodukt der Vektoren L und D kleiner oder gleich dem Kosinus des äußeren Kegelwinkels ist, liegt der Scheitelpunkt über dem äußeren Kegel und empfängt kein Licht. Wenn das Punktprodukt von L und D größer als der Kosinus des inneren Kegelwinkels ist, befindet sich der Scheitelpunkt innerhalb des inneren Kegels und empfängt die maximale Lichtmenge, die Dämpfung über die Entfernung wird dennoch in Betracht ziehen. Wenn sich der Scheitelpunkt zwischen den beiden Regionen befindet, wird der Falloff mit der folgenden Gleichung berechnet.

![Formel für lichtintensiven Scheitelpunkt nach dem Falloff](images/falloff.png)

Hierbei gilt:

-   I <sub>f is</sub> light intensity after falloff
-   Alpha ist der Winkel zwischen den Vektoren L und D.
-   Theta ist der innere Kegelwinkel
-   Phi ist der äußere Kegelwinkel
-   p ist der Falloff

Diese Formel generiert einen Wert zwischen 0,0 und 1,0, der die Intensität des Lichts am Scheitelpunkt skaliert, um den Falloff zu berücksichtigen. Die Dämpfung als Faktor des Abstands des Scheitelpunkts vom Licht wird ebenfalls angewendet. Das folgende Diagramm zeigt, wie sich unterschiedliche Falloffwerte auf die Falloffkurve auswirken können.

![Diagramm der Lichtstärke im Vergleich zum Scheitelpunktabstand vom Licht](images/fallgraf.png)

Die Auswirkungen verschiedener Falloffwerte auf die tatsächliche Beleuchtung sind gering, und es kommt zu einer geringen Leistungsschrümmung, wenn die Falloffkurve mit anderen Falloffwerten als 1,0 umgestaltiert wird. Aus diesen Gründen wird dieser Wert in der Regel auf 1,0 festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Licht und Materialien](lights-and-materials.md)
</dt> </dl>

 

 
