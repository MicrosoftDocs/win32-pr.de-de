---
description: 'Ein B&\# 233; Zier-Spline wird durch vier Punkte definiert: einen Startpunkt, zwei Kontrollpunkte und einen Endpunkt.'
ms.assetid: af19e82b-0d13-4fb0-981e-8d5dd1bbfb36
title: Zeichnen von Bezier-Splines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ea97d25f482372c387239e8f9083b31e3b2d912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755713"
---
# <a name="drawing-bezier-splines"></a><span data-ttu-id="f9f20-103">Zeichnen von Bezier-Splines</span><span class="sxs-lookup"><span data-stu-id="f9f20-103">Drawing Bezier Splines</span></span>

<span data-ttu-id="f9f20-104">Eine Bézier-Spline wird von vier Punkten definiert: einem Startpunkt, zwei Kontrollpunkten und einem Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="f9f20-104">A Bézier spline is defined by four points: a start point, two control points, and an end point.</span></span> <span data-ttu-id="f9f20-105">Im folgenden Beispiel wird eine Bézier-Spline mit dem Startpunkt (10, 100) und dem Endpunkt (200, 100) gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f9f20-105">The following example draws a Bézier spline with start point (10, 100) and end point (200, 100).</span></span> <span data-ttu-id="f9f20-106">Die Kontrollpunkte lauten (100, 10) und (150, 150):</span><span class="sxs-lookup"><span data-stu-id="f9f20-106">The control points are (100, 10) and (150, 150):</span></span>


```
Point p1(10, 100);   // start point
Point c1(100, 10);   // first control point
Point c2(150, 150);  // second control point
Point p2(200, 100);  // end point
Pen pen(Color(255, 0, 0, 255));
graphics.DrawBezier(&pen, p1, c1, c2, p2);
```



<span data-ttu-id="f9f20-107">In der folgenden Abbildung wird der resultierende Bézier-Spline zusammen mit dem Startpunkt, den Kontrollpunkten und dem Endpunkt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f9f20-107">The following illustration shows the resulting Bézier spline along with its start point, control points, and end point.</span></span> <span data-ttu-id="f9f20-108">Die Abbildung zeigt auch die zusammen Geviert-Hülle des Splines, bei der es sich um ein Polygon handelt, das durch Verbinden der vier Punkte mit geraden Linien gebildet wird.</span><span class="sxs-lookup"><span data-stu-id="f9f20-108">The illustration also shows the spline's convex hull, which is a polygon formed by connecting the four points with straight lines.</span></span>

![Abbildung, die eine Bézier-Spline mit zwei Endpunkten und zwei Kontrollpunkten zeigt](images/bezierspline1.png)

<span data-ttu-id="f9f20-110">Mit der [DrawBeziers](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint)) -Methode der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse können Sie eine Sequenz verbundener Bézier-Splines zeichnen.</span><span class="sxs-lookup"><span data-stu-id="f9f20-110">You can use the [DrawBeziers](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to draw a sequence of connected Bézier splines.</span></span> <span data-ttu-id="f9f20-111">Im folgenden Beispiel wird eine Kurve gezeichnet, die aus zwei verbundenen Bézier-Splines besteht.</span><span class="sxs-lookup"><span data-stu-id="f9f20-111">The following example draws a curve that consists of two connected Bézier splines.</span></span> <span data-ttu-id="f9f20-112">Der Endpunkt der ersten Bézier-Spline ist der Startpunkt der zweiten Bézier-Spline.</span><span class="sxs-lookup"><span data-stu-id="f9f20-112">The end point of the first Bézier spline is the start point of the second Bézier spline.</span></span>


```
Point p[] = {
   Point(10, 100),   // start point of first spline
   Point(75, 10),    // first control point of first spline
   Point(80, 50),    // second control point of first spline
   Point(100, 150),  // end point of first spline and 
                     // start point of second spline
   Point(125, 80),   // first control point of second spline
   Point(175, 200),  // second control point of second spline
   Point(200, 80)};  // end point of second spline
Pen pen(Color(255, 0, 0, 255));
graphics.DrawBeziers(&pen, p, 7);
```



<span data-ttu-id="f9f20-113">In der folgenden Abbildung sind die verbundenen Splines und die sieben Punkte dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f9f20-113">The following illustration shows the connected splines along with the seven points.</span></span>

![Darstellung von Endpunkten und Kontrollpunkten von zwei Splines, die einen der Endpunkte gemeinsam verwenden](images/bezierspline2.png)

 

 



