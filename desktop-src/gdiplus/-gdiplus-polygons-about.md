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
# <a name="polygons"></a><span data-ttu-id="1b648-103">Polygone</span><span class="sxs-lookup"><span data-stu-id="1b648-103">Polygons</span></span>

<span data-ttu-id="1b648-104">Ein Polygon ist eine geschlossene Abbildung mit drei oder mehr geraden Seiten.</span><span class="sxs-lookup"><span data-stu-id="1b648-104">A polygon is a closed figure with three or more straight sides.</span></span> <span data-ttu-id="1b648-105">Ein Dreieck ist beispielsweise ein Polygon mit drei Seiten, ein Rechteck ist ein Polygon mit vier Seiten, und ein Pentagon ist ein Polygon mit fünf Seiten.</span><span class="sxs-lookup"><span data-stu-id="1b648-105">For example, a triangle is a polygon with three sides, a rectangle is a polygon with four sides, and a pentagon is a polygon with five sides.</span></span> <span data-ttu-id="1b648-106">Die folgende Abbildung zeigt mehrere Polygone.</span><span class="sxs-lookup"><span data-stu-id="1b648-106">The following illustration shows several polygons.</span></span>

![Abbildung mit fünf Polygonen verschiedener Formen, Größen und Farben](images/aboutgdip02-art07.png)

<span data-ttu-id="1b648-108">Zum Zeichnen eines Polygons benötigen Sie ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt, ein [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt und ein Array von [**Punkt**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) -(oder [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)-) Objekten.</span><span class="sxs-lookup"><span data-stu-id="1b648-108">To draw a polygon, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object, and an array of [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (or [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)) objects.</span></span> <span data-ttu-id="1b648-109">Das **Grafik** Objekt stellt die [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpoint_inint)) -Methode bereit.</span><span class="sxs-lookup"><span data-stu-id="1b648-109">The **Graphics** object provides the [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpoint_inint)) method.</span></span> <span data-ttu-id="1b648-110">Das **Pen** -Objekt speichert Attribute des Polygons, z. b. Linienstärke und Farbe, und das Array von **Punkt** Objekten speichert die Punkte, die durch gerade Linien verbunden werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1b648-110">The **Pen** object stores attributes of the polygon, such as line width and color, and the array of **Point** objects stores the points to be connected by straight lines.</span></span> <span data-ttu-id="1b648-111">Die Adressen des **Stift** Objekts und das Array von **Punkt** Objekten werden als Argumente an die DrawPolygon-Methode übermittelt.</span><span class="sxs-lookup"><span data-stu-id="1b648-111">The addresses of the **Pen** object and the array of **Point** objects are passed as arguments to the DrawPolygon method.</span></span> <span data-ttu-id="1b648-112">Im folgenden Beispiel wird ein dreiseitiges Polygon gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1b648-112">The following example draws a three-sided polygon.</span></span> <span data-ttu-id="1b648-113">Beachten Sie, dass es nur drei Punkte in **myPointArray** gibt: (0,0), (50, 30) und (30, 60).</span><span class="sxs-lookup"><span data-stu-id="1b648-113">Note that there are only three points in **myPointArray**: (0, 0), (50, 30), and (30, 60).</span></span> <span data-ttu-id="1b648-114">Die DrawPolygon-Methode schließt das Polygon automatisch durch Zeichnen einer Linie von (30, 60) zurück zum Startpunkt (0,0).</span><span class="sxs-lookup"><span data-stu-id="1b648-114">The DrawPolygon method automatically closes the polygon by drawing a line from (30, 60) back to the starting point (0, 0);</span></span>


```
Point myPointArray[] =
   {Point(0, 0), Point(50, 30), Point(30, 60)};
myGraphics.DrawPolygon(&myPen, myPointArray, 3);
```



<span data-ttu-id="1b648-115">Die folgende Abbildung zeigt das Polygon.</span><span class="sxs-lookup"><span data-stu-id="1b648-115">The following illustration shows the polygon.</span></span>

![Darstellung eines Dreiecks gegen Koordinatenachsen](images/aboutgdip02-art08.png)

 

 



