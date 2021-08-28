---
description: Eine reguläre Kurve ist ein Satz hervorgehobener Pixel auf einer Rasteranzeige (oder Punkte auf einer gedruckten Seite), die den Umkreis (oder einen Teil des Umkreisbereichs) eines Konic-Abschnitts definieren.
ms.assetid: b7a1b544-8b50-45ba-918c-17472c46c8b8
title: Kurven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed6b7c0f6ad03a9ebe16dcffe85694397f6127ff15c2d9d3a9e68f79257a0e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119452240"
---
# <a name="curves"></a>Kurven

Eine reguläre Kurve ist ein Satz hervorgehobener Pixel auf einer Rasteranzeige (oder Punkte auf einer gedruckten Seite), die den Umkreis (oder einen Teil des Umkreisbereichs) eines Konic-Abschnitts definieren. Eine unregelmäßige Kurve ist eine Gruppe von Pixeln, die eine Kurve definieren, die nicht in den Umkreis eines Konic-Abschnitts passt. Der Endpunkt wird von einer Kurve genauso ausgeschlossen, wie er von einer Linie ausgeschlossen wird.

Wenn eine Anwendung eine der Funktionen zum Zeichnen von Kurven aufruft, unterteilt GDI die Kurve in eine Reihe extrem kleiner, diskreter Liniensegmente. Nachdem die Endpunkte (Startpunkt und Endpunkt) für jedes dieser Liniensegmente bestimmt wurden, bestimmt GDI, welche Pixel (oder Punkte) die einzelnen Zeilen definieren, indem die zugehörige DDA angewendet wird.

Eine Anwendung kann eine Ellipse oder einen Teil einer Ellipse zeichnen, indem sie die [**Arc-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-arc) aufruft. Diese Funktion zeichnet die Kurve innerhalb des Umkreises eines unsichtbaren Rechtecks, das als umgebendes Rechteck bezeichnet wird. Die Größe der Ellipse wird durch zwei unsichtbare Radiale angegeben, die sich von der Mitte des Rechtecks bis zu den Seiten des Rechtecks erstrecken. Die folgende Abbildung zeigt einen Bogen (Teil einer Ellipse), der mithilfe der **Arc-Funktion** gezeichnet wurde.

![Diagramm mit einem Bogen, der drei Viertel eines vollständigen Kreises darstellt](images/cslcv-03.png)

Beim Aufrufen der [**Arc-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-arc) gibt eine Anwendung die Koordinaten des umgrenzenden Rechtecks und der Radiale an. Die obige Abbildung zeigt das Rechteck und radiale Linien mit gestrichelten Linien, während der tatsächliche Bogen mit einer durchgezogenen Linie gezeichnet wurde.

Beim Zeichnen des Bogens eines anderen Objekts kann die Anwendung die Funktionen [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) und [**GetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-getarcdirection) aufrufen, um die Richtung (im Uhrzeigersinn oder gegen den Uhrzeigersinn) zu steuern, in der das Objekt gezeichnet wird. Die Standardrichtung für das Zeichnen von Bogen und anderen Objekten ist gegen den Uhrzeigersinn.

Zusätzlich zum Zeichnen von Ellipsen oder Teilen von Ellipsen können Anwendungen unregelmäßige Kurven zeichnen, die als Bézierkurven bezeichnet werden. Eine *Bézierkurve* ist eine unregelmäßige Kurve, deren Krümmung durch vier Kontrollpunkte (p1, p2, p3 und p4) definiert wird. Die Kontrollpunkte p1 und p4 definieren die Start- und Endpunkte der Kurve, und die Kontrollpunkte p2 und p3 definieren die Form der Kurve, indem sie Punkte markieren, an denen die Kurve die Ausrichtung umkehrt, wie im folgenden Diagramm dargestellt.

![Abbildung mit zwei Bézierkurven, die jeweils zwischen einem Start- und Endpunkt und jeweils zwei Steuerpunkten stehen](images/cslcv-04.png)

Eine Anwendung kann unregelmäßige Kurven zeichnen, indem sie die [**PolyBezier-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier) aufruft und die entsprechenden Kontrollpunkte liefert.

 

 



