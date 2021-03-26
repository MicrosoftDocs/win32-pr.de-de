---
description: Zum Zeichnen von Linien und Rechtecke benötigen Sie ein Grafik Objekt und ein Pen-Objekt. Das Grafik Objekt stellt die DrawLine-Methode bereit, und das Pen-Objekt speichert Features der Linie, z. b. Farbe und Breite.
ms.assetid: f2e4144f-f2f1-49db-bfdf-ffce3023b4cb
title: Verwenden eines Stifts zum Zeichnen von Linien und Rechtecken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b335caf7e2ecbad6bc49965ff757809c3b1179c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959444"
---
# <a name="using-a-pen-to-draw-lines-and-rectangles"></a><span data-ttu-id="8fb04-104">Verwenden eines Stifts zum Zeichnen von Linien und Rechtecken</span><span class="sxs-lookup"><span data-stu-id="8fb04-104">Using a Pen to Draw Lines and Rectangles</span></span>

<span data-ttu-id="8fb04-105">Zum Zeichnen von Linien und Rechtecke benötigen Sie ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und ein [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8fb04-105">To draw lines and rectangles, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="8fb04-106">Das **Grafik** Objekt stellt die [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) -Methode bereit, und das **Pen** -Objekt speichert Features der Linie, z. b. Farbe und Breite.</span><span class="sxs-lookup"><span data-stu-id="8fb04-106">The **Graphics** object provides the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method, and the **Pen** object stores features of the line, such as color and width.</span></span>

<span data-ttu-id="8fb04-107">Im folgenden Beispiel wird eine Zeile von (20, 10) nach (300, 100) gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8fb04-107">The following example draws a line from (20, 10) to (300, 100).</span></span> <span data-ttu-id="8fb04-108">Angenommen, **Grafik** ist ein vorhandenes [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt.</span><span class="sxs-lookup"><span data-stu-id="8fb04-108">Assume **graphics** is an existing [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>


```
Pen pen(Color(255, 0, 0, 0));
graphics.DrawLine(&pen, 20, 10, 300, 100);
```



<span data-ttu-id="8fb04-109">Die erste Code Anweisung verwendet den [**Stift**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Klassenkonstruktor, um einen schwarzen Stift zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8fb04-109">The first statement of code uses the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) class constructor to create a black pen.</span></span> <span data-ttu-id="8fb04-110">Das einzige Argument, das an den **Stift** -Konstruktor übergeben wird, ist ein [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8fb04-110">The one argument passed to the **Pen** constructor is a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="8fb04-111">Die Werte, die verwendet werden, um das **Color** -Objekt – (255, 0, 0, 0) – zu erstellen, entsprechen den Alpha-, rot-, grün-und blauen Komponenten der Farbe.</span><span class="sxs-lookup"><span data-stu-id="8fb04-111">The values used to construct the **Color** object — (255, 0, 0, 0) — correspond to the alpha, red, green, and blue components of the color.</span></span> <span data-ttu-id="8fb04-112">Diese Werte definieren einen nicht transparenten schwarzen Stift.</span><span class="sxs-lookup"><span data-stu-id="8fb04-112">These values define an opaque black pen.</span></span>

<span data-ttu-id="8fb04-113">Im folgenden Beispiel wird ein Rechteck mit der linken oberen Ecke bei (10, 10) gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8fb04-113">The following example draws a rectangle with its upper-left corner at (10, 10).</span></span> <span data-ttu-id="8fb04-114">Das Rechteck hat eine Breite von 100 und eine Höhe von 50.</span><span class="sxs-lookup"><span data-stu-id="8fb04-114">The rectangle has a width of 100 and a height of 50.</span></span> <span data-ttu-id="8fb04-115">Das zweite Argument, das an den [**Stift**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Konstruktor übergeben wird, gibt an, dass die Stift Breite 5 Pixel beträgt.</span><span class="sxs-lookup"><span data-stu-id="8fb04-115">The second argument passed to the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) constructor indicates that the pen width is 5 pixels.</span></span>


```
Pen blackPen(Color(255, 0, 0, 0), 5);
stat = graphics.DrawRectangle(&blackPen, 10, 10, 100, 50);
```



<span data-ttu-id="8fb04-116">Wenn das Rechteck gezeichnet wird, wird der Stift auf die Begrenzung des Rechtecks zentriert.</span><span class="sxs-lookup"><span data-stu-id="8fb04-116">When the rectangle is drawn, the pen is centered on the rectangle's boundary.</span></span> <span data-ttu-id="8fb04-117">Da die Stift Breite 5 beträgt, werden die Seiten des Rechtecks 5 Pixel breit gezeichnet, sodass 1 Pixel an der Grenze selbst gezeichnet wird, 2 Pixel im inneren gezeichnet werden und 2 Pixel auf der Außenseite gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="8fb04-117">Because the pen width is 5, the sides of the rectangle are drawn 5 pixels wide, such that 1 pixel is drawn on the boundary itself, 2 pixels are drawn on the inside, and 2 pixels are drawn on the outside.</span></span> <span data-ttu-id="8fb04-118">Weitere Informationen zur Ausrichtung von Pen finden Sie unter [Festlegen der Stift Breite und-Ausrichtung](-gdiplus-setting-pen-width-and-alignment-use.md).</span><span class="sxs-lookup"><span data-stu-id="8fb04-118">For more details on pen alignment, see [Setting Pen Width and Alignment](-gdiplus-setting-pen-width-and-alignment-use.md).</span></span>

<span data-ttu-id="8fb04-119">Die folgende Abbildung zeigt das resultierende Rechteck.</span><span class="sxs-lookup"><span data-stu-id="8fb04-119">The following illustration shows the resulting rectangle.</span></span> <span data-ttu-id="8fb04-120">Die gepunkteten Linien zeigen an, wo das Rechteck gezeichnet worden wäre, wenn die Stift Breite ein Pixel gewesen wäre.</span><span class="sxs-lookup"><span data-stu-id="8fb04-120">The dotted lines show where the rectangle would have been drawn if the pen width had been one pixel.</span></span> <span data-ttu-id="8fb04-121">Die erweiterte Ansicht der oberen linken Ecke des Rechtecks zeigt, dass die dicken schwarzen Linien auf diese gepunkteten Linien zentriert sind.</span><span class="sxs-lookup"><span data-stu-id="8fb04-121">The enlarged view of the upper-left corner of the rectangle shows that the thick black lines are centered on those dotted lines.</span></span>

![Abbildung eines Rechtecks, das mit einer dicken schwarzen Linie gezeichnet wird, die eine dünne, graue, gestrichelte Linie umgibt](images/pens1.png)

 

 



