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
# <a name="drawing-cardinal-splines"></a>Zeichnen von kardinalen Splines

Eine kardinale Splinekurve ist eine Kurve, die durch einen bestimmten Satz von Punkten reibungslos verläuft. Um einen kardinalspline zu zeichnen, erstellen Sie ein [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und übergeben die Adresse eines Arrays von Punkten an die [**Grafik::D rawcurve**](/previous-versions//ms536070(v=vs.85)) -Methode. Im folgenden Beispiel wird ein glockenförmiger kardinaler Spline gezeichnet, der fünf festgelegte Punkte durchläuft:


```
Point points[] = {Point(0, 100),
                  Point(50, 80),
                  Point(100, 20),
                  Point(150, 80),
                  Point(200, 100)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawCurve(&pen, points, 5);
```



In der folgenden Abbildung werden die Kurve und fünf Punkte dargestellt.

![Abbildung eines kardinalen Spline, der einen Satz von fünf Punkten durchläuft](images/cardinalspline1.png)

Sie können die [**Graphics::D rawclosedcurve**](/previous-versions//ms536143(v=vs.85)) -Methode der [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse verwenden, um einen geschlossenen kardinalspline zu zeichnen. In einer geschlossenen kardinalsplinekurve wird die Kurve bis zum letzten Punkt im Array fortgesetzt und stellt eine Verbindung mit dem ersten Punkt im Array her.

Im folgenden Beispiel wird eine geschlossene kardinale Spline gezeichnet, die sechs festgelegte Punkte durchläuft.


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



Die folgende Abbildung zeigt den geschlossenen Spline zusammen mit den sechs Punkten:

![Abbildung einer geschlossenen kardinalen Spline, die eine Reihe von sechs Punkten durchläuft](images/cardinalspline1a.png)

Sie können die Art und Weise ändern, in der sich ein kardinaler Spline befindet, indem Sie ein Spannungs Argument an die [**Grafik übergeben::D rawcurve**](/previous-versions//ms536070(v=vs.85)) -Methode Im folgenden Beispiel werden drei kardinale Splines gezeichnet, die denselben Satz von Punkten durchlaufen:


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



Die folgende Abbildung zeigt die drei Splines zusammen mit Ihren Spannungswerten. Beachten Sie, dass die Punkte durch gerade Linien verbunden sind, wenn die Spannung den Wert 0 hat.

![Abbildung von drei kardinalen Splines, die denselben Satz von Punkten durchlaufen, jedoch bei unterschiedlichen Spannungen](images/cardinalspline2.png)

 

 
