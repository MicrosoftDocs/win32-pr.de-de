---
description: Die Welt Transformation ist eine Eigenschaft der Grafikklasse.
ms.assetid: 22f43b29-ea7b-4faf-9795-2242bf704ed3
title: Verwenden der globalen Transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2138df1bbd2be6d3329695fc6898da49da93b3b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214566"
---
# <a name="using-the-world-transformation"></a><span data-ttu-id="51516-103">Verwenden der globalen Transformation</span><span class="sxs-lookup"><span data-stu-id="51516-103">Using the World Transformation</span></span>

<span data-ttu-id="51516-104">Die Welt Transformation ist eine Eigenschaft der [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse.</span><span class="sxs-lookup"><span data-stu-id="51516-104">The world transformation is a property of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="51516-105">Die Zahlen, die die globale Transformation angeben, werden in einem [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) Objekt gespeichert, das eine 3 × 3-Matrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="51516-105">The numbers that specify the world transformation are stored in a [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object, which represents a 3 ×3 matrix.</span></span> <span data-ttu-id="51516-106">Die **Matrix** -und **Grafik** Klassen verfügen über mehrere Methoden zum Festlegen der Zahlen in der Transformations Matrix der Welt.</span><span class="sxs-lookup"><span data-stu-id="51516-106">The **Matrix** and **Graphics** classes have several methods for setting the numbers in the world transformation matrix.</span></span> <span data-ttu-id="51516-107">Die Beispiele in diesem Abschnitt manipulieren Rechtecke, da Rechtecke leicht gezeichnet werden können, und es ist leicht, die Auswirkungen von Transformationen auf Rechtecke anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="51516-107">The examples in this section manipulate rectangles because rectangles are easy to draw and it is easy to see the effects of transformations on rectangles.</span></span>

<span data-ttu-id="51516-108">Wir beginnen mit dem Erstellen eines 50 nach 50-Rechtecks und der Suche am Ursprung (0,0).</span><span class="sxs-lookup"><span data-stu-id="51516-108">We start by creating a 50 by 50 rectangle and locating it at the origin (0, 0).</span></span> <span data-ttu-id="51516-109">Der Ursprung befindet sich in der oberen linken Ecke des Client Bereichs.</span><span class="sxs-lookup"><span data-stu-id="51516-109">The origin is at the upper-left corner of the client area.</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="51516-110">Der folgende Code wendet eine Skalierungs Transformation an, die das Rechteck um den Faktor 1,75 in der x-Richtung erweitert und das Rechteck um den Faktor 0,5 in der y-Richtung verkleinert:</span><span class="sxs-lookup"><span data-stu-id="51516-110">The following code applies a scaling transformation that expands the rectangle by a factor of 1.75 in the x direction and shrinks the rectangle by a factor of 0.5 in the y direction:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="51516-111">Das Ergebnis ist ein Rechteck, das in der x-Richtung länger und kürzer in der y-Richtung als die ursprüngliche ist.</span><span class="sxs-lookup"><span data-stu-id="51516-111">The result is a rectangle that is longer in the x direction and shorter in the y direction than the original.</span></span>

<span data-ttu-id="51516-112">Um das Rechteck zu drehen, anstatt es zu skalieren, verwenden Sie den folgenden Code anstelle des vorangehenden Codes:</span><span class="sxs-lookup"><span data-stu-id="51516-112">To rotate the rectangle instead of scaling it, use the following code instead of the preceding code:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.RotateTransform(28.0f);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="51516-113">Verwenden Sie den folgenden Code, um das Rechteck zu übersetzen:</span><span class="sxs-lookup"><span data-stu-id="51516-113">To translate the rectangle, use the following code:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.DrawRectangle(&pen, rect);
```



 

 



