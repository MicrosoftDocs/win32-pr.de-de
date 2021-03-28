---
description: Eine kardinale Splinekurve ist eine Kurve, die durch einen bestimmten Satz von Punkten reibungslos verläuft.
ms.assetid: 0bb84f55-18d0-4a4c-bc5b-7803aa807954
title: Zeichnen von kardinalen Splines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c780cb4486f579acb57170a8eda4fd187a421ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570357"
---
# <a name="drawing-cardinal-splines"></a><span data-ttu-id="0de22-103">Zeichnen von kardinalen Splines</span><span class="sxs-lookup"><span data-stu-id="0de22-103">Drawing Cardinal Splines</span></span>

<span data-ttu-id="0de22-104">Eine kardinale Splinekurve ist eine Kurve, die durch einen bestimmten Satz von Punkten reibungslos verläuft.</span><span class="sxs-lookup"><span data-stu-id="0de22-104">A cardinal spline is a curve that passes smoothly through a given set of points.</span></span> <span data-ttu-id="0de22-105">Um einen kardinalspline zu zeichnen, erstellen Sie ein [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und übergeben die Adresse eines Arrays von Punkten an die [**Grafik::D rawcurve**](/previous-versions//ms536070(v=vs.85)) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0de22-105">To draw a cardinal spline, create a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and pass the address of an array of points to the [**Graphics::DrawCurve**](/previous-versions//ms536070(v=vs.85)) method.</span></span> <span data-ttu-id="0de22-106">Im folgenden Beispiel wird ein glockenförmiger kardinaler Spline gezeichnet, der fünf festgelegte Punkte durchläuft:</span><span class="sxs-lookup"><span data-stu-id="0de22-106">The following example draws a bell-shaped cardinal spline that passes through five designated points:</span></span>


```
Point points[] = {Point(0, 100),
                  Point(50, 80),
                  Point(100, 20),
                  Point(150, 80),
                  Point(200, 100)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawCurve(&pen, points, 5);
```



<span data-ttu-id="0de22-107">In der folgenden Abbildung werden die Kurve und fünf Punkte dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0de22-107">The following illustration shows the curve and five points.</span></span>

![Abbildung eines kardinalen Spline, der einen Satz von fünf Punkten durchläuft](images/cardinalspline1.png)

<span data-ttu-id="0de22-109">Sie können die [**Graphics::D rawclosedcurve**](/previous-versions//ms536143(v=vs.85)) -Methode der [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse verwenden, um einen geschlossenen kardinalspline zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="0de22-109">You can use the [**Graphics::DrawClosedCurve**](/previous-versions//ms536143(v=vs.85)) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to draw a closed cardinal spline.</span></span> <span data-ttu-id="0de22-110">In einer geschlossenen kardinalsplinekurve wird die Kurve bis zum letzten Punkt im Array fortgesetzt und stellt eine Verbindung mit dem ersten Punkt im Array her.</span><span class="sxs-lookup"><span data-stu-id="0de22-110">In a closed cardinal spline, the curve continues through the last point in the array and connects with the first point in the array.</span></span>

<span data-ttu-id="0de22-111">Im folgenden Beispiel wird eine geschlossene kardinale Spline gezeichnet, die sechs festgelegte Punkte durchläuft.</span><span class="sxs-lookup"><span data-stu-id="0de22-111">The following example draws a closed cardinal spline that passes through six designated points.</span></span>


```
Point points[] = {Point(60, 60),
   Point(150, 80),
   Point(200, 40),
   Point(180, 120),
   Point(120, 100),
   Point(80, 160)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawClosedCurve(&pen, points, 6);
```



<span data-ttu-id="0de22-112">Die folgende Abbildung zeigt den geschlossenen Spline zusammen mit den sechs Punkten:</span><span class="sxs-lookup"><span data-stu-id="0de22-112">The following illustration shows the closed spline along with the six points:</span></span>

![Abbildung einer geschlossenen kardinalen Spline, die eine Reihe von sechs Punkten durchläuft](images/cardinalspline1a.png)

<span data-ttu-id="0de22-114">Sie können die Art und Weise ändern, in der sich ein kardinaler Spline befindet, indem Sie ein Spannungs Argument an die [**Grafik übergeben::D rawcurve**](/previous-versions//ms536070(v=vs.85)) -Methode</span><span class="sxs-lookup"><span data-stu-id="0de22-114">You can change the way a cardinal spline bends by passing a tension argument to the [**Graphics::DrawCurve**](/previous-versions//ms536070(v=vs.85)) method.</span></span> <span data-ttu-id="0de22-115">Im folgenden Beispiel werden drei kardinale Splines gezeichnet, die denselben Satz von Punkten durchlaufen:</span><span class="sxs-lookup"><span data-stu-id="0de22-115">The following example draws three cardinal splines that pass through the same set of points:</span></span>


```
Point points[] = {Point(20, 50),
                  Point(100, 10),
                  Point(200, 100),
                  Point(300, 50),
                  Point(400, 80)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawCurve(&pen, points, 5, 0.0f);  // tension 0.0
graphics.DrawCurve(&pen, points, 5, 0.6f);  // tension 0.6
graphics.DrawCurve(&pen, points, 5, 1.0f);  // tension 1.0
```



<span data-ttu-id="0de22-116">Die folgende Abbildung zeigt die drei Splines zusammen mit Ihren Spannungswerten.</span><span class="sxs-lookup"><span data-stu-id="0de22-116">The following illustration shows the three splines along with their tension values.</span></span> <span data-ttu-id="0de22-117">Beachten Sie, dass die Punkte durch gerade Linien verbunden sind, wenn die Spannung den Wert 0 hat.</span><span class="sxs-lookup"><span data-stu-id="0de22-117">Note that when the tension is 0, the points are connected by straight lines.</span></span>

![Abbildung von drei kardinalen Splines, die denselben Satz von Punkten durchlaufen, jedoch bei unterschiedlichen Spannungen](images/cardinalspline2.png)

 

 
