---
description: Eine reguläre Kurve ist ein Satz hervorgehobener Pixel in einer Raster Anzeige (oder Punkte auf einer gedruckten Seite), die den Umkreis (oder einen Teil des Umkreis Bereichs) eines gleich enden Abschnitts definieren.
ms.assetid: b7a1b544-8b50-45ba-918c-17472c46c8b8
title: Kurven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e694edeb535dbc7dbd4191a5a2b0b44556b810e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863672"
---
# <a name="curves"></a>Kurven

Eine reguläre Kurve ist ein Satz hervorgehobener Pixel in einer Raster Anzeige (oder Punkte auf einer gedruckten Seite), die den Umkreis (oder einen Teil des Umkreis Bereichs) eines gleich enden Abschnitts definieren. Eine unregelmäßige Kurve ist ein Satz von Pixeln, die eine Kurve definieren, die nicht in den Umkreis eines gleich enden Abschnitts passt. Der Endpunkt wird von einer Kurve ausgeschlossen, so wie er von einer Zeile ausgeschlossen wird.

Wenn eine Anwendung eine der Kurven Zeichnungsfunktionen aufruft, unterbricht GDI die Kurve in eine Reihe von extrem kleinen, diskreten Liniensegmenten. Nach dem Bestimmen der Endpunkte (Startpunkt und Endpunkt) für jedes dieser Zeilen Segmente bestimmt GDI, welche Pixel (oder Punkte) die einzelnen Zeilen durch Anwenden des zugehörigen DDA definieren.

Eine Anwendung kann eine Ellipse oder einen Teil einer Ellipse durch Aufrufen der [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc) -Funktion zeichnen. Diese Funktion zeichnet die Kurve innerhalb des Umkreis Bereichs eines unsichtbaren Rechtecks, das als umschließendes Rechteck bezeichnet wird. Die Größe der Ellipse wird durch zwei unsichtbare radiale angegeben, die von der Mitte des Rechtecks auf die Seiten des Rechtecks ausgedehnt werden. Die folgende Abbildung zeigt einen Bogen (Teil einer Ellipse), der mithilfe der **Bogen** Funktion gezeichnet wurde.

![Diagramm, das einen Bogen anzeigt, der drei Quartale eines vollständigen Kreises darstellt](images/cslcv-03.png)

Beim Aufrufen der [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc) -Funktion gibt eine Anwendung die Koordinaten des umgebenden Rechtecks und der radiale an. In der vorangehenden Abbildung werden das Rechteck und die radiale mit gestrichelten Linien dargestellt, während der eigentliche Bogen mithilfe einer durchgezogenen Linie gezeichnet wurde.

Wenn Sie den Bogen eines anderen Objekts zeichnen, kann die Anwendung die Funktionen [**setarcdirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) und [**getarcdirection**](/windows/desktop/api/Wingdi/nf-wingdi-getarcdirection) zum Steuern der Richtung (im Uhrzeigersinn oder gegen den Uhrzeigersinn), in der das Objekt gezeichnet wird, aufgerufen werden. Die Standardrichtung für das Zeichnen von Bögen und anderen Objekten ist gegen den Uhrzeigersinn.

Anwendungen können nicht nur Ellipsen oder Teile von Ellipsen zeichnen, sondern auch unregelmäßige Kurven mit den Namen Bézier-Kurven zeichnen. Eine *Bézier-Kurve* ist eine unregelmäßige Kurve, deren Krümmung durch vier Kontrollpunkte (P1, P2, P3 und P4) definiert wird. Die Kontrollpunkte P1 und P4 definieren die Start-und Endpunkte der Kurve, und die Steuerungs Punkte P2 und P3 definieren die Form der Kurve, indem Sie Punkte markieren, an denen die Kurve die Ausrichtung kehrt, wie im folgenden Diagramm dargestellt.

![Abbildung der zwei Bézier-Kurven, die jeweils zwischen einem Start-und Endpunkt und jeweils zwei Kontrollpunkten angezeigt werden](images/cslcv-04.png)

Eine Anwendung kann unregelmäßige Kurven zeichnen, indem Sie die [**polybezier**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier) -Funktion aufrufen und die entsprechenden Steuerungs Punkte bereitstellt.

 

 



