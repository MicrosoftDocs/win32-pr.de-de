---
description: 'Die folgende Abbildung zeigt zwei Kurven: eine geöffnete und eine geschlossene.'
ms.assetid: e0fb8ba1-1783-4b36-93d8-f1242425d8bd
title: Geöffnete und geschlossene Kurven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7587ec950f8a0abc21f8c9cfb000a7333e87297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571421"
---
# <a name="open-and-closed-curves"></a><span data-ttu-id="fc3b5-103">Geöffnete und geschlossene Kurven</span><span class="sxs-lookup"><span data-stu-id="fc3b5-103">Open and Closed Curves</span></span>

<span data-ttu-id="fc3b5-104">Die folgende Abbildung zeigt zwei Kurven: eine geöffnete und eine geschlossene.</span><span class="sxs-lookup"><span data-stu-id="fc3b5-104">The following illustration shows two curves: one open and one closed.</span></span>

![Abbildung einer geöffneten Kurve (eine gekrümmte Linie) und einer geschlossenen Kurve (der Umriss einer Form)](images/aboutgdip02-art24.png)

<span data-ttu-id="fc3b5-106">Geschlossene Kurven verfügen über ein inneres und können daher mit einem Pinsel gefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="fc3b5-106">Closed curves have an interior and therefore can be filled with a brush.</span></span> <span data-ttu-id="fc3b5-107">Die [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse in Windows GDI+ bietet die folgenden Methoden zum Auffüllen geschlossener Abbildungen und Kurven: [fillrechteck](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(constbrush_constrect_)), [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(constbrush_constrect_)), [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)), [FillPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpoint_inint)), [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)), [**Graphics:: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath)und [**Graphics:: FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion).</span><span class="sxs-lookup"><span data-stu-id="fc3b5-107">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class in Windows GDI+ provides the following methods for filling closed figures and curves: [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(constbrush_constrect_)), [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(constbrush_constrect_)), [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)), [FillPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpoint_inint)), [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)), [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath), and [**Graphics::FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion).</span></span> <span data-ttu-id="fc3b5-108">Jedes Mal, wenn Sie eine dieser Methoden aufrufen, müssen Sie die Adresse eines der spezifischen Pinseltypen ([**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)oder [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)) als Argument übergeben.</span><span class="sxs-lookup"><span data-stu-id="fc3b5-108">Whenever you call one of these methods, you must pass the address of one of the specific brush types ([**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush), or [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)) as an argument.</span></span>

<span data-ttu-id="fc3b5-109">Die [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)) -Methode ist ein begleitende der [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) -Methode.</span><span class="sxs-lookup"><span data-stu-id="fc3b5-109">The [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)) method is a companion to the [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) method.</span></span> <span data-ttu-id="fc3b5-110">Ebenso wie die DrawArc-Methode einen Teil der Gliederung einer Ellipse zeichnet, füllt die FillPie-Methode einen Teil des Inneren einer Ellipse aus.</span><span class="sxs-lookup"><span data-stu-id="fc3b5-110">Just as the DrawArc method draws a portion of the outline of an ellipse, the FillPie method fills a portion of the interior of an ellipse.</span></span> <span data-ttu-id="fc3b5-111">Im folgenden Beispiel wird ein Bogen gezeichnet und der entsprechende Teil des Inneren der Ellipse ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="fc3b5-111">The following example draws an arc and fills the corresponding portion of the interior of the ellipse.</span></span>


```
myGraphics.FillPie(&mySolidBrush, 0, 0, 140, 70, 0, 120);
myGraphics.DrawArc(&myPen, 0, 0, 140, 70, 0, 120);
```



<span data-ttu-id="fc3b5-112">Die folgende Abbildung zeigt den Bogen und den gefüllten Kreis.</span><span class="sxs-lookup"><span data-stu-id="fc3b5-112">The following illustration shows the arc and the filled pie.</span></span>

![Abbildung, die ein Segment einer ausgefüllten Ellipse anzeigt](images/aboutgdip02-art25.png)

<span data-ttu-id="fc3b5-114">Die [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)) -Methode ist ein begleitende der [DrawClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)) -Methode.</span><span class="sxs-lookup"><span data-stu-id="fc3b5-114">The [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)) method is a companion to the [DrawClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)) method.</span></span> <span data-ttu-id="fc3b5-115">Beide Methoden schließen die Kurve automatisch, indem Sie den Endpunkt mit dem Ausgangspunkt verbinden.</span><span class="sxs-lookup"><span data-stu-id="fc3b5-115">Both methods automatically close the curve by connecting the ending point to the starting point.</span></span> <span data-ttu-id="fc3b5-116">Im folgenden Beispiel wird eine Kurve gezeichnet, die durchläuft (0,0), (60, 20) und (40, 50).</span><span class="sxs-lookup"><span data-stu-id="fc3b5-116">The following example draws a curve that passes through (0, 0), (60, 20), and (40, 50).</span></span> <span data-ttu-id="fc3b5-117">Anschließend wird die Kurve automatisch geschlossen, indem (40, 50) mit dem Anfangspunkt (0,0) verbunden wird, und das innere wird mit einer voll Tonfarbe gefüllt.</span><span class="sxs-lookup"><span data-stu-id="fc3b5-117">Then, the curve is automatically closed by connecting (40, 50) to the starting point (0, 0), and the interior is filled with a solid color.</span></span>


```
Point myPointArray[] =
   {Point(10, 10), Point(60, 20),Point(40, 50)};
myGraphics.DrawClosedCurve(&myPen, myPointArray, 3);
myGraphics.FillClosedCurve(&mySolidBrush, myPointArray, 3, FillModeAlternate)
```



<span data-ttu-id="fc3b5-118">Ein Pfad kann aus mehreren Abbildungen (unter Pfaden) bestehen.</span><span class="sxs-lookup"><span data-stu-id="fc3b5-118">A path can consist of several figures (subpaths).</span></span> <span data-ttu-id="fc3b5-119">Die [**Graphics:: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) -Methode füllt das innere jeder Abbildung aus.</span><span class="sxs-lookup"><span data-stu-id="fc3b5-119">The [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method fills the interior of each figure.</span></span> <span data-ttu-id="fc3b5-120">Wenn eine Abbildung nicht geschlossen wird, füllt die **Graphics:: FillPath** -Methode den Bereich, der eingeschlossen werden würde, wenn die Abbildung geschlossen würde.</span><span class="sxs-lookup"><span data-stu-id="fc3b5-120">If a figure is not closed, the **Graphics::FillPath** method fills the area that would be enclosed if the figure were closed.</span></span> <span data-ttu-id="fc3b5-121">Im folgenden Beispiel wird ein Pfad gezeichnet und gefüllt, der aus einem Bogen, einem kardinalspline, einer Zeichenfolge und einem Kreis besteht.</span><span class="sxs-lookup"><span data-stu-id="fc3b5-121">The following example draws and fills a path that consists of an arc, a cardinal spline, a string, and a pie.</span></span>


```
myGraphics.FillPath(&mySolidBrush, &myGraphicsPath);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="fc3b5-122">In der folgenden Abbildung wird der Pfad vor und nach dem Auffüllen mit einem Pinsel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="fc3b5-122">The following illustration shows the path before and after it is filled with a solid brush.</span></span> <span data-ttu-id="fc3b5-123">Beachten Sie, dass der Text in der Zeichenfolge von der [**Grafik::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) -Methode beschrieben, aber nicht ausgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="fc3b5-123">Note that the text in the string is outlined, but not filled, by the [**Graphics::DrawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method.</span></span> <span data-ttu-id="fc3b5-124">Dabei handelt es sich um die [**Graphics:: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) -Methode, die das Innere der Zeichen in der Zeichenfolge zeichnet.</span><span class="sxs-lookup"><span data-stu-id="fc3b5-124">It is the [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method that paints the interiors of the characters in the string.</span></span>

![die Abbildung zeigt, dass zweimal Text und eine offene und eine geschlossene Kurve angezeigt werden. Diese sind beim ersten Mal leer und wurden beim zweiten Mal ausgefüllt.](images/aboutgdip02-art26.png)

 

 



