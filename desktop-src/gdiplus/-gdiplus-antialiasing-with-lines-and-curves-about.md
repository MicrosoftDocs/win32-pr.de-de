---
description: Wenn Sie Windows GDI+ zum Zeichnen einer Linie verwenden, geben Sie den Ausgangspunkt und den Endpunkt der Linie an, aber Sie müssen keine Informationen über die einzelnen Pixel in der Zeile angeben.
ms.assetid: 7c4869c1-76ff-42d1-abf1-387121943b2a
title: Antialiasing bei Linien und Kurven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c817d3e11b4699c9fc892b41dcc827c0861f192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755776"
---
# <a name="antialiasing-with-lines-and-curves"></a><span data-ttu-id="aed94-103">Antialiasing bei Linien und Kurven</span><span class="sxs-lookup"><span data-stu-id="aed94-103">Antialiasing with Lines and Curves</span></span>

<span data-ttu-id="aed94-104">Wenn Sie Windows GDI+ zum Zeichnen einer Linie verwenden, geben Sie den Ausgangspunkt und den Endpunkt der Linie an, aber Sie müssen keine Informationen über die einzelnen Pixel in der Zeile angeben.</span><span class="sxs-lookup"><span data-stu-id="aed94-104">When you use Windows GDI+ to draw a line, you provide the starting point and ending point of the line, but you don't have to provide any information about the individual pixels on the line.</span></span> <span data-ttu-id="aed94-105">GDI+ funktioniert in Verbindung mit der Anzeigetreiber Software, um zu bestimmen, welche Pixel eingeschaltet werden, um die Zeile auf einem bestimmten Anzeigegerät anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="aed94-105">GDI+ works in conjunction with the display driver software to determine which pixels will be turned on to show the line on a particular display device.</span></span>

<span data-ttu-id="aed94-106">Angenommen, eine gerade rote Linie wechselt vom Punkt (4, 2) bis zum Punkt (16, 10).</span><span class="sxs-lookup"><span data-stu-id="aed94-106">Consider a straight red line that goes from the point (4, 2) to the point (16, 10).</span></span> <span data-ttu-id="aed94-107">Angenommen, das Koordinatensystem hat seinen Ursprung in der oberen linken Ecke, und die Maßeinheit ist das Pixel.</span><span class="sxs-lookup"><span data-stu-id="aed94-107">Assume the coordinate system has its origin in the upper-left corner and that the unit of measure is the pixel.</span></span> <span data-ttu-id="aed94-108">Nehmen Sie auch an, dass die x-Achse nach rechts und die y-Achse nach unten zeigt.</span><span class="sxs-lookup"><span data-stu-id="aed94-108">Also assume that the x-axis points to the right and the y-axis points down.</span></span> <span data-ttu-id="aed94-109">Die folgende Abbildung zeigt eine vergrößerte Ansicht der roten Linie, die auf einem mehrfarbigen Hintergrund gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="aed94-109">The following illustration shows an enlarged view of the red line drawn on a multicolored background.</span></span>

![Darstellung der in einem mehrfarbigen Hintergrund ausgeführten roten Pixel](images/aboutgdip02-art33.png)

<span data-ttu-id="aed94-111">Beachten Sie, dass die zum Rendering der Zeile verwendeten roten Pixel nicht transparent sind.</span><span class="sxs-lookup"><span data-stu-id="aed94-111">Note that the red pixels used to render the line are opaque.</span></span> <span data-ttu-id="aed94-112">Es gibt keine teilweise transparenten Pixel, die an der Anzeige der Zeile beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="aed94-112">There are no partially transparent pixels involved in displaying the line.</span></span> <span data-ttu-id="aed94-113">Diese Art von Zeilen Rendering gibt der Linie eine verzweigte Darstellung, und die Linie sieht etwas wie eine Treppe aus.</span><span class="sxs-lookup"><span data-stu-id="aed94-113">This type of line rendering gives the line a jagged appearance, and the line looks a bit like a staircase.</span></span> <span data-ttu-id="aed94-114">Diese Methode zum Darstellen einer Linie mit einer Treppe wird als Aliasing bezeichnet. die Treppe ist ein Alias für die theoretische Zeile.</span><span class="sxs-lookup"><span data-stu-id="aed94-114">This technique of representing a line with a staircase is called aliasing; the staircase is an alias for the theoretical line.</span></span>

<span data-ttu-id="aed94-115">Ein anspruchsvolleres Verfahren zum Rendern einer Linie besteht darin, teilweise transparente Pixel zusammen mit reinen roten Pixeln zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="aed94-115">A more sophisticated technique for rendering a line involves using partially transparent pixels along with pure red pixels.</span></span> <span data-ttu-id="aed94-116">Pixel werden auf "rein rot" oder auf eine Mischung aus rot und die Hintergrundfarbe festgelegt, je nachdem, wie nah Sie auf die Linie sind.</span><span class="sxs-lookup"><span data-stu-id="aed94-116">Pixels are set to pure red or to some blend of red and the background color depending on how close they are to the line.</span></span> <span data-ttu-id="aed94-117">Diese Art des Renderings wird als Antialiasing bezeichnet und führt zu einer Zeile, die das menschliche Auge als nahtloser ansieht.</span><span class="sxs-lookup"><span data-stu-id="aed94-117">This type of rendering is called antialiasing and results in a line that the human eye perceives as more smooth.</span></span> <span data-ttu-id="aed94-118">In der folgenden Abbildung wird gezeigt, wie bestimmte Pixel mit dem Hintergrund kombiniert werden, um eine Zeile mit einem-oder-Alias zu bilden.</span><span class="sxs-lookup"><span data-stu-id="aed94-118">The following illustration shows how certain pixels are blended with the background to produce an antialiased line.</span></span>

![Abbildung, die Pixel zeigt, die im gleichen Hintergrund Schattierungen von rot sind](images/aboutgdip02-art34.png)

<span data-ttu-id="aed94-120">Antialiasing (Glättung) kann auch auf Kurven angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="aed94-120">Antialiasing (smoothing) can also be applied to curves.</span></span> <span data-ttu-id="aed94-121">Die folgende Abbildung zeigt eine vergrößerte Ansicht einer gegläten Ellipse.</span><span class="sxs-lookup"><span data-stu-id="aed94-121">The following illustration shows an enlarged view of a smoothed ellipse.</span></span>

![Abbildung einer Ellipse, die aus unterschiedlichen Schattierungen von blauen Pixeln in einem weißen Hintergrund besteht](images/aboutgdip02-art35.png)

<span data-ttu-id="aed94-123">In der folgenden Abbildung wird die gleiche Ellipse in der tatsächlichen Größe angezeigt, einmal ohne Antialiasing und einmal mit Antialiasing.</span><span class="sxs-lookup"><span data-stu-id="aed94-123">The following illustration shows the same ellipse in its actual size, once without antialiasing and once with antialiasing.</span></span>

![Screenshot von zwei Ellipsen: der eine mit Antialiasing wird benachrichtigt.](images/aboutgdip02-art36.png)

<span data-ttu-id="aed94-125">Zum Zeichnen von Linien und Kurven, die Antialiasing verwenden, erstellen Sie ein [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und übergeben Sie " *SmoothingModeAntiAlias* " an die zugehörige [**Grafik:: sezmuothingmode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode) -Methode.</span><span class="sxs-lookup"><span data-stu-id="aed94-125">To draw lines and curves that use antialiasing, create a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and pass *SmoothingModeAntiAlias* to its [**Graphics::SetSmoothingMode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode) method.</span></span> <span data-ttu-id="aed94-126">Anschließend wird eine der Zeichnungs Methoden desselben **Grafik** Objekts aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="aed94-126">Then call one of the drawing methods of that same **Graphics** object.</span></span>


```
myGraphics.SetSmoothingMode(SmoothingModeAntiAlias);
myGraphics.DrawLine(&myPen, 0, 0, 12, 8);
```



<span data-ttu-id="aed94-127">" **SmoothingModeAntiAlias** " ist ein Element der " [**SmoothingMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) "-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="aed94-127">**SmoothingModeAntiAlias** is an element of the [**SmoothingMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) enumeration.</span></span>

 

 



