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
# <a name="drawing-bezier-splines"></a>Zeichnen von Bezier-Splines

Eine Bézier-Spline wird von vier Punkten definiert: einem Startpunkt, zwei Kontrollpunkten und einem Endpunkt. Im folgenden Beispiel wird eine Bézier-Spline mit dem Startpunkt (10, 100) und dem Endpunkt (200, 100) gezeichnet. Die Kontrollpunkte lauten (100, 10) und (150, 150):


```
Point p1(10, 100);   // start point
Point c1(100, 10);   // first control point
Point c2(150, 150);  // second control point
Point p2(200, 100);  // end point
Pen pen(Color(255, 0, 0, 255));
graphics.DrawBezier(&pen, p1, c1, c2, p2);
```



In der folgenden Abbildung wird der resultierende Bézier-Spline zusammen mit dem Startpunkt, den Kontrollpunkten und dem Endpunkt dargestellt. Die Abbildung zeigt auch die zusammen Geviert-Hülle des Splines, bei der es sich um ein Polygon handelt, das durch Verbinden der vier Punkte mit geraden Linien gebildet wird.

![Abbildung, die eine Bézier-Spline mit zwei Endpunkten und zwei Kontrollpunkten zeigt](images/bezierspline1.png)

Mit der [DrawBeziers](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint)) -Methode der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse können Sie eine Sequenz verbundener Bézier-Splines zeichnen. Im folgenden Beispiel wird eine Kurve gezeichnet, die aus zwei verbundenen Bézier-Splines besteht. Der Endpunkt der ersten Bézier-Spline ist der Startpunkt der zweiten Bézier-Spline.


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



In der folgenden Abbildung sind die verbundenen Splines und die sieben Punkte dargestellt.

![Darstellung von Endpunkten und Kontrollpunkten von zwei Splines, die einen der Endpunkte gemeinsam verwenden](images/bezierspline2.png)

 

 



