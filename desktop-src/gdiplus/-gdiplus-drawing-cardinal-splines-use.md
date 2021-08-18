---
description: Eine Kardinalspline ist eine Kurve, die reibungslos durch einen bestimmten Satz von Punkten verläuft.
ms.assetid: 0bb84f55-18d0-4a4c-bc5b-7803aa807954
title: Zeichnen von Kardinalsplines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9124e27254fc77135d265d9bab98d2332c02d345e60add1fcd96fc68c814df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036818"
---
# <a name="drawing-cardinal-splines"></a>Zeichnen von Kardinalsplines

Eine Kardinalspline ist eine Kurve, die reibungslos durch einen bestimmten Satz von Punkten verläuft. Erstellen Sie zum Zeichnen einer [](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Kardinalspline ein Graphics-Objekt, und übergeben Sie die Adresse eines Arrays von Punkten an die [**Graphics::D rawCurve-Methode.**](/previous-versions//ms536070(v=vs.85)) Im folgenden Beispiel wird eine glockenförmige Kardinalspline ge zeichnet, die fünf bestimmte Punkte durchläuft:


```
Point points[] = {Point(0, 100),
                  Point(50, 80),
                  Point(100, 20),
                  Point(150, 80),
                  Point(200, 100)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawCurve(&pen, points, 5);
```



Die folgende Abbildung zeigt die Kurve und fünf Punkte.

![Abbildung einer Kardinalspline, die einen Satz von fünf Punkten durchläuft](images/cardinalspline1.png)

Sie können die [**Graphics::D rawClosedCurve-Methode**](/previous-versions//ms536143(v=vs.85)) der [**Graphics-Klasse**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) verwenden, um eine geschlossene Kardinalspline zu zeichnen. In einer geschlossenen Kardinalspline wird die Kurve bis zum letzten Punkt im Array fortgesetzt und mit dem ersten Punkt im Array verknüpft.

Im folgenden Beispiel wird eine geschlossene Kardinalspline ge zeichnet, die sechs bestimmte Punkte durchläuft.


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

![Abbildung einer geschlossenen Kardinalspline, die einen Satz von sechs Punkten durchläuft](images/cardinalspline1a.png)

Sie können die Art und Weise ändern, in der ein kardinaler Spline-Bruch verfälsiert wird, indem Sie ein argument-Argument an die [**Graphics::D rawCurve-Methode**](/previous-versions//ms536070(v=vs.85)) übergeben. Im folgenden Beispiel werden drei Kardinalsplines ge zeichnet, die denselben Satz von Punkten passieren:


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



Die folgende Abbildung zeigt die drei Splines zusammen mit ihren Werten für die Werte. Beachten Sie, dass die Punkte durch gerade Linien verbunden sind, wenn die 10-Punkte-Linie ist.

![Abbildung von drei Kardinalsplines, die denselben Satz von Punkten, aber unterschiedliche Darstellungen durchgehen](images/cardinalspline2.png)

 

 
