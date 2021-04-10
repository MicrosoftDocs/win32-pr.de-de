---
description: Der primäre Sensor Datentyp für Umgebungslichtsensoren ist Beleuchtungs Kraft in Lux (dünn/Quadratmeter). Die in diesem Thema beschriebenen Prinzipien basieren auf der Aufnahme von Lux-Werten als Eingabe und der Reaktion auf diese Daten in einem Programm.
ms.assetid: 29855779-7c27-4cfe-b8af-b33bc86a1f62
title: Verstehen und Interpretieren von Lux-Werten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8012f983eeac29cc07b18ac2d27918d2df6ed52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042598"
---
# <a name="understanding-and-interpreting-lux-values"></a>Verstehen und Interpretieren von Lux-Werten

Der primäre Sensor Datentyp für Umgebungslichtsensoren ist Beleuchtungs Kraft in Lux (dünn/Quadratmeter). Die in diesem Thema beschriebenen Prinzipien basieren auf der Aufnahme von Lux-Werten als Eingabe und der Reaktion auf diese Daten in einem Programm.

Lux-Messwerte sind direkt proportional zu der Energie pro Quadratmeter, die pro Sekunde erfasst wird. Die menschliche Wahrnehmung von Licht Ebenen ist nicht so einfach. Die menschliche Wahrnehmung von Licht ist kompliziert, da unsere Augen ständig angepasst werden und andere biologische Prozesse unsere Wahrnehmung beeinträchtigen. Wir können uns diese Wahrnehmung jedoch aus einer vereinfachten Perspektive vorstellen, indem Sie mehrere interessante Bereiche mit bekannten oberen und niedrigeren Schwellenwerten erstellen.

Das folgende Beispiel DataSet stellt grobe Schwellenwerte für allgemeine Beleuchtungsbedingungen und den entsprechenden Beleuchtungs Schritt dar. Hier stellt jeder Beleuchtungs Schritt eine Änderung in der Beleuchtungs Umgebung dar.

> [!Note]  
> Dieses DataSet ist zur Veranschaulichung und für alle Benutzer oder Situationen möglicherweise nicht vollständig genau.

 



| Beleuchtungs Bedingung | Von (Lux) | An (Lux) | Mittelwert (Lux) | Beleuchtungs Schritt |
|--------------------|------------|----------|------------------|---------------|
| Schwarze Tonhöhe        | 0          | 10       | 5                | 1             |
| Sehr dunkel          | 11         | 50       | 30               | 2             |
| Dunkel innen       | 51         | 200      | 125              | 3             |
| Im Inneren        | 201        | 400      | 300              | 4             |
| Normal im Inneren     | 401        | 1000     | 700              | 5             |
| Hell im Inneren     | 1001       | 5.000     | 3000             | 6             |
| Dim im Außenbereich       | 5001       | 10.000   | 7.500             | 7             |
| Bewölkt im Außenbereich    | 10.001     | 30.000   | 20.000           | 8             |
| Direktes Sonnenlicht    | 30.001     | 100.000  | 65.000           | 9             |



 

Wenn wir diese Daten mithilfe der Mittelwerte aus dieser Tabelle visualisieren, sehen wir, dass die Beziehung zwischen Lux und Beleuchtungs Schritt nicht linear ist, wie im folgenden Diagramm gezeigt.

![lineare Beleuchtungs Diagramm](images/luxtostep.png)

Wenn wir diese Daten jedoch mithilfe einer logarithmischen Skalierung auf der x-Achse anzeigen, können wir sehen, dass eine ungefähr lineare Beziehung entsteht.

![logarithmische Beleuchtungs Diagramm](images/luxlogtostep.png)

### <a name="an-example-transform"></a>Eine Beispiel Transformation

Basierend auf dem Beispiel Dataset für Ambient-Light-Sensoren, die zuvor bereitgestellt wurden, können Sie die folgende Gleichung erreichen, um der menschlichen Wahrnehmung von Lux-Werten zuzuordnen. In diesem Beispiel liegen die erwarteten Werte zwischen 0 und 1 Million Lux.

![Lux-Wert Gleichung](images/sensor-lux-equation.jpg)

Diese Gleichung führt zu Werten, die sich zwischen 0,0 und 1,0 in einer ungefähr linearen Weise unterscheiden. Dieses Ergebnis gibt an, wie sich die von Menschen wahrgenommene Beleuchtung basierend auf dem zuvor gezeigten Beispiel Dataset geändert hat.

 

 



