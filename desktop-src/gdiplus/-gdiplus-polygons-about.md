---
description: Ein Polygon ist eine geschlossene Abbildung mit drei oder mehr geraden Seiten.
ms.assetid: f1155341-83f3-4805-8d42-a1910515db31
title: Polygone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe67ec2d062579df0510c100a80d06715be4199e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751320"
---
# <a name="polygons"></a>Polygone

Ein Polygon ist eine geschlossene Abbildung mit drei oder mehr geraden Seiten. Ein Dreieck ist beispielsweise ein Polygon mit drei Seiten, ein Rechteck ist ein Polygon mit vier Seiten, und ein Pentagon ist ein Polygon mit fünf Seiten. Die folgende Abbildung zeigt mehrere Polygone.

![Abbildung mit fünf Polygonen verschiedener Formen, Größen und Farben](images/aboutgdip02-art07.png)

Zum Zeichnen eines Polygons benötigen Sie ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt, ein [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt und ein Array von [**Punkt**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) -(oder [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)-) Objekten. Das **Grafik** Objekt stellt die [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpoint_inint)) -Methode bereit. Das **Pen** -Objekt speichert Attribute des Polygons, z. b. Linienstärke und Farbe, und das Array von **Punkt** Objekten speichert die Punkte, die durch gerade Linien verbunden werden sollen. Die Adressen des **Stift** Objekts und das Array von **Punkt** Objekten werden als Argumente an die DrawPolygon-Methode übermittelt. Im folgenden Beispiel wird ein dreiseitiges Polygon gezeichnet. Beachten Sie, dass es nur drei Punkte in **myPointArray** gibt: (0,0), (50, 30) und (30, 60). Die DrawPolygon-Methode schließt das Polygon automatisch durch Zeichnen einer Linie von (30, 60) zurück zum Startpunkt (0,0).


```
Point myPointArray[] =
   {Point(0, 0), Point(50, 30), Point(30, 60)};
myGraphics.DrawPolygon(&myPen, myPointArray, 3);
```



Die folgende Abbildung zeigt das Polygon.

![Darstellung eines Dreiecks gegen Koordinatenachsen](images/aboutgdip02-art08.png)

 

 



