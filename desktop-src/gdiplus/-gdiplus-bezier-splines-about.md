---
description: 'Ein B&\# 233; Zier-Splinekurve ist eine Kurve, die von vier Punkten angegeben wird: zwei Endpunkte (P1 und P2) und zwei Kontrollpunkte (C1 und C2).'
ms.assetid: 3ee279ea-20cc-4089-b1a5-13bf1c7c4942
title: Bézier-Splines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd725e64f9ba0035849d2d1d6fbc03d5efa0b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131385"
---
# <a name="bezier-splines"></a><span data-ttu-id="a51eb-103">Bézier-Splines</span><span class="sxs-lookup"><span data-stu-id="a51eb-103">Bezier Splines</span></span>

<span data-ttu-id="a51eb-104">Eine Bézier-Spline ist eine Kurve, die von vier Punkten angegeben wird: zwei Endpunkte (P1 und P2) und zwei Kontrollpunkte (C1 und C2).</span><span class="sxs-lookup"><span data-stu-id="a51eb-104">A Bézier spline is a curve specified by four points: two end points (p1 and p2) and two control points (c1 and c2).</span></span> <span data-ttu-id="a51eb-105">Die Kurve beginnt bei P1 und endet bei P2.</span><span class="sxs-lookup"><span data-stu-id="a51eb-105">The curve begins at p1 and ends at p2.</span></span> <span data-ttu-id="a51eb-106">Die Kurve übergibt nicht die Steuerungs Punkte, aber die Steuerungs Punkte fungieren als Magnete, ziehen die Kurve in bestimmte Richtungen und beeinflussen die Kurven Kurven.</span><span class="sxs-lookup"><span data-stu-id="a51eb-106">The curve doesn't pass through the control points, but the control points act as magnets, pulling the curve in certain directions and influencing the way the curve bends.</span></span> <span data-ttu-id="a51eb-107">In der folgenden Abbildung wird eine Bézier-Kurve zusammen mit den zugehörigen Endpunkten und Steuerungs Punkten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a51eb-107">The following illustration shows a Bézier curve along with its endpoints and control points.</span></span>

![Abbildung, die eine Bézier-Spline mit zwei Endpunkten und zwei Kontrollpunkten zeigt](images/aboutgdip02-art11a.png)

<span data-ttu-id="a51eb-109">Beachten Sie, dass die Kurve bei P1 beginnt und zum Kontrollpunkt C1 wechselt.</span><span class="sxs-lookup"><span data-stu-id="a51eb-109">Note that the curve starts at p1 and moves toward the control point c1.</span></span> <span data-ttu-id="a51eb-110">Die Tangente an der Kurve bei P1 ist die Linie, die von P1 bis C1 gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="a51eb-110">The tangent line to the curve at p1 is the line drawn from p1 to c1.</span></span> <span data-ttu-id="a51eb-111">Beachten Sie außerdem, dass die tangential Linie am Endpunkt P2 die Linie ist, die von C2 zu P2 gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="a51eb-111">Also note that the tangent line at the endpoint p2 is the line drawn from c2 to p2.</span></span>

<span data-ttu-id="a51eb-112">Um einen Bézier-Spline zu zeichnen, benötigen Sie ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und ein [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a51eb-112">To draw a Bézier spline, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="a51eb-113">Das **Grafik** Objekt stellt die [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inint_inint_inint_inint_inint_inint_inint_inint)) -Methode bereit, und das **Pen** -Objekt speichert Attribute der Kurve, z. b. Linienstärke und Farbe.</span><span class="sxs-lookup"><span data-stu-id="a51eb-113">The **Graphics** object provides the [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inint_inint_inint_inint_inint_inint_inint_inint)) method, and the **Pen** object stores attributes of the curve, such as line width and color.</span></span> <span data-ttu-id="a51eb-114">Die Adresse des **Stift** Objekts wird als eines der Argumente an die DrawBezier-Methode übermittelt.</span><span class="sxs-lookup"><span data-stu-id="a51eb-114">The address of the **Pen** object is passed as one of the arguments to the DrawBezier method.</span></span> <span data-ttu-id="a51eb-115">Die übrigen Argumente, die an die DrawBezier-Methode übermittelt werden, sind die Endpunkte und die Steuerungs Punkte.</span><span class="sxs-lookup"><span data-stu-id="a51eb-115">The remaining arguments passed to the DrawBezier method are the endpoints and the control points.</span></span> <span data-ttu-id="a51eb-116">Im folgenden Beispiel wird eine Bézier-Spline mit Startpunkt (0,0), Kontrollpunkten (40, 20) und (80, 150) und Endpunkt (100, 10) gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a51eb-116">The following example draws a Bézier spline with starting point (0, 0), control points (40, 20) and (80, 150), and ending point (100, 10).</span></span>


```
myGraphics.DrawBezier(&myPen, 0, 0, 40, 20, 80, 150, 100, 10);
```



<span data-ttu-id="a51eb-117">In der folgenden Abbildung sind die Kurve, die Kontrollpunkte und zwei Tangenten Linien dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a51eb-117">The following illustration shows the curve, the control points, and two tangent lines.</span></span>

![Abbildung, die eine Bézier-Spline mit zwei Endpunkten, zwei Kontrollpunkten und zwei Tangenten Linien anzeigt](images/aboutgdip02-art12.png)

<span data-ttu-id="a51eb-119">Die Bézier-Splines wurden ursprünglich von Pierre Bézier zum Entwerfen in der Automobilindustrie entwickelt.</span><span class="sxs-lookup"><span data-stu-id="a51eb-119">Bézier splines were originally developed by Pierre Bézier for design in the automotive industry.</span></span> <span data-ttu-id="a51eb-120">Sie haben sich in vielen Arten von computergestütztem Design bewährt und werden auch verwendet, um die Umschriften von Schriftarten zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a51eb-120">They have since proven to be very useful in many types of computer-aided design and are also used to define the outlines of fonts.</span></span> <span data-ttu-id="a51eb-121">Die Bézier-Splines können eine Vielzahl von Formen ergeben, von denen einige in der folgenden Abbildung dargestellt sind.</span><span class="sxs-lookup"><span data-stu-id="a51eb-121">Bézier splines can yield a wide variety of shapes, some of which are shown in the following illustration.</span></span>

![Abbildung mit drei Bézier-Splines](images/aboutgdip02-art13.png)

 

 



