---
description: 'Ein B&\# 233;Zier-Spline ist eine Kurve, die durch vier Punkte angegeben wird: zwei Endpunkte (p1 und p2) und zwei Kontrollpunkte (c1 und c2).'
ms.assetid: 3ee279ea-20cc-4089-b1a5-13bf1c7c4942
title: Bézier-Splines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87bcc9c56baa9cd1b3e93187ef00f9d6a2c8c1d218262c946028ed70429de18d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119399570"
---
# <a name="bezier-splines"></a>Bézier-Splines

Ein Bézier-Spline ist eine Kurve, die durch vier Punkte angegeben wird: zwei Endpunkte (p1 und p2) und zwei Kontrollpunkte (c1 und c2). Die Kurve beginnt bei p1 und endet bei p2. Die Kurve verläuft nicht durch die Kontrollpunkte, aber die Kontrollpunkte fungieren als Magnete, ziehen die Kurve in bestimmte Richtungen und beeinflussen die Art und Weise, wie die Kurve verläuft. Die folgende Abbildung zeigt eine Bézierkurve zusammen mit ihren Endpunkten und Kontrollpunkten.

![Abbildung mit einem Bézier-Spline mit zwei Endpunkten und zwei Steuerpunkten](images/aboutgdip02-art11a.png)

Beachten Sie, dass die Kurve bei p1 beginnt und sich zum Kontrollpunkt c1 bewegt. Die Tangenslinie zur Kurve bei p1 ist die Linie, die von p1 bis c1 gezeichnet wird. Beachten Sie auch, dass die Tangensenlinie am Endpunkt p2 die Linie ist, die von c2 bis p2 gezeichnet wird.

Um einen Bézier-Spline zu zeichnen, benötigen Sie ein [**Graphics-Objekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) und ein [**Stiftobjekt.**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) Das **Graphics-Objekt** stellt die [DrawBezier-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inint_inint_inint_inint_inint_inint_inint_inint)) bereit, und das **Stiftobjekt** speichert Attribute der Kurve, z. B. Linienbreite und Farbe. Die Adresse des **Stiftobjekts** wird als eines der Argumente an die DrawBezier-Methode übergeben. Die verbleibenden Argumente, die an die DrawBezier-Methode übergeben werden, sind die Endpunkte und die Steuerungspunkte. Im folgenden Beispiel wird ein Bézier-Spline mit Startpunkt (0, 0), Kontrollpunkten (40, 20) und (80, 150) und Endpunkt (100, 10) zeichnet.


```
myGraphics.DrawBezier(&myPen, 0, 0, 40, 20, 80, 150, 100, 10);
```



Die folgende Abbildung zeigt die Kurve, die Steuerpunkte und zwei Tangenslinien.

![Abbildung mit einem Bézier-Spline mit zwei Endpunkten, zwei Kontrollpunkten und zwei Tangenslinien](images/aboutgdip02-art12.png)

Bézier-Splines wurden ursprünglich von Einem Bézier für den Entwurf in der Automobilindustrie entwickelt. Sie haben sich seitdem in vielen Arten von computergestütztem Design als sehr nützlich erwiesen und werden auch verwendet, um die Konturen von Schriftarten zu definieren. Béziersplines können eine Vielzahl von Formen ergeben, von denen einige in der folgenden Abbildung dargestellt werden.

![Abbildung mit drei Bézier-Splines](images/aboutgdip02-art13.png)

 

 



