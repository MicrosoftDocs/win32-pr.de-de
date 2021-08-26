---
description: Der primäre Sensordatentyp für Umgebungslichtsensoren ist die Leuchtdichte in Lux (Auslassungszeichen pro Quadratmeter). Die in diesem Thema beschriebenen Prinzipien basieren auf der Eingabe von Lux-Werten und der Reaktion auf diese Daten in einem Programm.
ms.assetid: 29855779-7c27-4cfe-b8af-b33bc86a1f62
title: Grundlegendes zu und Interpretieren von Lux-Werten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05b4bc9c3efa73f91d54a9c88231180ec2807964b753e175bc13755b54c2743
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126533"
---
# <a name="understanding-and-interpreting-lux-values"></a>Grundlegendes zu und Interpretieren von Lux-Werten

Der primäre Sensordatentyp für Umgebungslichtsensoren ist die Leuchtdichte in Lux (Auslassungszeichen pro Quadratmeter). Die in diesem Thema beschriebenen Prinzipien basieren auf der Eingabe von Lux-Werten und der Reaktion auf diese Daten in einem Programm.

Lux-Messwerte sind direkt proportional zur Energie pro Quadrat, die pro Sekunde aufgenommen wird. Die Menschliche Wahrnehmung von Lichtpegeln ist nicht so einfach. Die menschliche Wahrnehmung des Lichts ist kompliziert, da sich unsere Augen ständig anpassen und andere prozesse die Wahrnehmung beeinflussen. Wir können uns diese Wahrnehmung jedoch aus einer vereinfachten Perspektive vorstellen, indem wir mehrere interessante Bereiche mit bekannten oberen und unteren Schwellenwerten erstellen.

Das folgende Beispieldatensatz stellt grobe Schwellenwerte für allgemeine Beleuchtungsbedingungen und den entsprechenden Beleuchtungsschritt dar. Hier stellt jeder Beleuchtungsschritt eine Änderung der Beleuchtungsumgebung dar.

> [!Note]  
> Dieses DataSet dient zur Veranschaulichung und ist möglicherweise nicht für alle Benutzer oder Situationen vollständig genau.

 



| Beleuchtungsbedingung | Von (Lux) | To (Lux) | Mittelwert (Lux) | Beleuchtungsschritt |
|--------------------|------------|----------|------------------|---------------|
| Pitch Black        | 0          | 10       | 5                | 1             |
| Sehr dunkel          | 11         | 50       | 30               | 2             |
| Dunkle Gebäude       | 51         | 200      | 125              | 3             |
| Dim Indoors        | 201        | 400      | 300              | 4             |
| Normale Gebäude     | 401        | 1000     | 700              | 5             |
| Helle Gebäude     | 1001       | 5.000     | 3000             | 6             |
| Dim Outdoors       | 5001       | 10.000   | 7.500             | 7             |
| Cloudy Outdoors    | 10,001     | 30.000   | 20.000           | 8             |
| Direktes Geleit    | 30,001     | 100.000  | 65,000           | 9             |



 

Wenn wir diese Daten mithilfe der Mittelwerte aus dieser Tabelle visualisieren, sehen wir, dass die Beziehung zwischen Lux und Beleuchtung nicht linear ist, wie im folgenden Diagramm gezeigt.

![Linearer Beleuchtungsgraph](images/luxtostep.png)

Wenn wir diese Daten jedoch mithilfe einer logarithmischen Skala auf der X-Achse anzeigen, sehen wir, dass eine grob lineare Beziehung entsteht.

![Logarithmischer Beleuchtungsgraph](images/luxlogtostep.png)

### <a name="an-example-transform"></a>Beispieltransformation

Basierend auf dem zuvor bereitgestellten Beispieldatensatz für Umgebungslichtsensoren konnten Sie zur folgenden Gleichung gelangen, um lux-Werte der menschlichen Wahrnehmung zuzuordnen. In diesem Beispiel reichen die erwarteten Werte von 0 Lux bis 1.000.000 Lux.

![Lux-Wertgleichung](images/sensor-lux-equation.jpg)

Diese Gleichung führt zu Werten, die ungefähr linear zwischen 0,0 und 1,0 variieren. Dieses Ergebnis gibt an, wie sich die vom Menschen wahrgenommene Beleuchtung basierend auf dem zuvor gezeigten Beispieldatensatz geändert hat.

 

 



