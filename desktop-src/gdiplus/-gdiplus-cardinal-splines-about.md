---
description: Bei einem kardinalspline handelt es sich um eine Sequenz von einzelnen Kurven, die mit einer größeren Kurve verknüpft sind.
ms.assetid: 4fc62f00-7006-4ade-bfcc-091a3a97d889
title: Kardinale Splines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d85c0163e405a6f9346f521b4057eb936108cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215609"
---
# <a name="cardinal-splines"></a>Kardinale Splines

Bei einem kardinalspline handelt es sich um eine Sequenz von einzelnen Kurven, die mit einer größeren Kurve verknüpft sind. Der Spline wird durch ein Array von Punkten und einen Tension-Parameter angegeben. Ein kardinaler Spline verläuft nahtlos durch jeden Punkt im Array. Es sind keine spitzen Ecken und keine abrupten Änderungen in der Genauigkeit der Kurve vorhanden. Die folgende Abbildung zeigt einen Satz von Punkten und einen kardinalspline, der die einzelnen Punkte im Satz durchläuft.

![Abbildung mit einem kardinalspline, der sechs definierte Punkte durchläuft](images/aboutgdip02-art09.gif)

Eine physische Spline ist ein dünner Teil des Holzes oder eines anderen flexiblen Materials. Vor der Einführung mathematischer Splines verwendeten Designer physische Splines zum Zeichnen von Kurven. Ein Designer würde den Spline in einem Papier Abschnitt platzieren und ihn an eine bestimmte Gruppe von Punkten verankern. Der Designer kann dann eine Kurve erstellen, indem er mit einem Stift entlang der Spline gezeichnet wird. Eine bestimmte Gruppe von Punkten kann abhängig von den Eigenschaften der physischen Spline eine Vielzahl von Kurven ergeben. Beispielsweise würde ein Spline mit einem hohen Widerstand zum wechseln eine andere Kurve als eine extrem flexible Spline ergeben.

Die Formeln für mathematische Splines basieren auf den Eigenschaften von flexiblen Stäbchen, sodass die Kurven, die von mathematischen Splines erzeugt werden, mit den Kurven vergleichbar sind, die von physischen Splines erzeugt wurden. Ebenso wie physische Splines mit unterschiedlichen Verspannungen durch einen bestimmten Satz von Punkten unterschiedliche Kurven bewirken, werden mathematische Splines mit unterschiedlichen Werten für den Tension-Parameter unterschiedliche Kurven durch einen bestimmten Satz von Punkten ergeben. Die folgende Abbildung zeigt vier kardinale Splines, die denselben Satz von Punkten passieren. Die Spannung wird für jede Spline angezeigt. Beachten Sie, dass eine Spannung von 0 unendlich viel physischer Spannung entspricht, sodass die Kurve die kürzeste Richtung (gerade Linien) zwischen Punkten erzwingt. Eine Spannung von 1 entspricht keiner physischen Spannung, sodass der Spline den Weg der geringsten Gesamt Kurve annehmen kann. Wenn Spannungswerte größer als 1 sind, verhält sich die Kurve wie eine komprimierte Spring-Kurve, die über einen längeren Pfad verfügt.

![Darstellung von vier kardinalen Splines durch die gleichen drei Punkte](images/aboutgdip02-art10.gif)

Beachten Sie, dass die vier Splines in der vorangehenden Abbildung die gleiche Tangenten Linie am Ausgangspunkt verwenden. Der Tangens ist die Linie, die vom Startpunkt bis zum nächsten Punkt entlang der Kurve gezeichnet wird. Ebenso ist der gemeinsame Tangens am Endpunkt die Linie, die vom Endpunkt zum vorherigen Punkt der Kurve gezeichnet wird.

Um einen kardinalspline zu zeichnen, benötigen Sie ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt, ein [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt und ein Array von [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) -Objekten. Das **graphics** -Objekt stellt die [DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpointf_inint_inreal)) -Methode bereit, die den Spline zeichnet, und das **Pen** -Objekt speichert Attribute der Spline, z. b. Linienstärke und Farbe. Das Array von **Point** -Objekten speichert die Punkte, die die Kurve übergibt. Im folgenden Beispiel wird ein kardinaler Spline gezeichnet, der die Punkte in *myPointArray* durchläuft. Der dritte Parameter ist die Spannung.


```
myGraphics.DrawCurve(&myPen, myPointArray, 3, 1.5f);
```



 

 



