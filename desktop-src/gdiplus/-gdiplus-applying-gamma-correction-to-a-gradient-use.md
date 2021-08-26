---
description: Sie können die Gammakorrektur für einen Farbverlaufspinsel aktivieren, indem Sie TRUE an die PathGradientBrush::SetGammaCorrection-Methode dieses Pinsels übergeben.
ms.assetid: 47472e41-f469-44f4-8b39-cf3982b79f9e
title: Anwenden der Gammakorrektur auf einen Farbverlauf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eae76306e5c68804d76777d9fc80c65d06904702487a8b60f80659b9d16a96ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888540"
---
# <a name="applying-gamma-correction-to-a-gradient"></a>Anwenden der Gammakorrektur auf einen Farbverlauf

Sie können die Gammakorrektur für einen Farbverlaufspinsel aktivieren, indem Sie **TRUE** an die [**PathGradientBrush::SetGammaCorrection-Methode**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) dieses Pinsels übergeben. Sie können die Gammakorrektur deaktivieren, indem Sie **FALSE** an die **PathGradientBrush::SetGammaCorrection-Methode** übergeben. Die Gammakorrektur ist standardmäßig deaktiviert.

Im folgenden Beispiel wird ein linearer Farbverlaufspinsel erstellt und dieser Pinsel verwendet, um zwei Rechtecke auszufüllen. Das erste Rechteck wird ohne Gammakorrektur gefüllt, und das zweite Rechteck wird mit Gammakorrektur gefüllt.


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 255, 0, 0),   // Opaque red
   Color(255, 0, 0, 255));  // Opaque blue

graphics.FillRectangle(&linGrBrush, 0, 0, 200, 50);
linGrBrush.SetGammaCorrection(TRUE);
graphics.FillRectangle(&linGrBrush, 0, 60, 200, 50); 
```



Die folgende Abbildung zeigt die beiden ausgefüllten Rechtecke. Das obere Rechteck ohne Gammakorrektur wird in der Mitte dunkel angezeigt. Das untere Rechteck mit Gammakorrektur scheint eine einheitlichere Intensität zu haben.

![Abbildung mit zwei Rechtecke: Die farbige Füllung des ersten variiert in der Intensität, die Füllung des zweiten unterscheidet sich weniger.](images/gammagradient1.png)

Im folgenden Beispiel wird ein Pfadfarbepinsel basierend auf einem sternförmigen Pfad erstellt. Der Code verwendet den Pfadverlaufspinsel mit deaktivierter Gammakorrektur (Standardeinstellung), um den Pfad zu füllen. Anschließend übergibt der Code **TRUE** an die [**PathGradientBrush::SetGammaCorrection-Methode,**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) um die Gammakorrektur für den Pfadfarbverlaufspinsel zu ermöglichen. Der Aufruf von [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) legt die Welttransformation eines [**Graphics-Objekts**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fest, sodass der nachfolgende Aufruf von [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) einen Stern auffüllt, der sich rechts vom ersten Stern befindet.


```
// Put the points of a polygon in an array.
Point points[] = {Point(75, 0), Point(100, 50), 
                  Point(150, 50), Point(112, 75),
                  Point(150, 150), Point(75, 100), 
                  Point(0, 150), Point(37, 75), 
                  Point(0, 50), Point(50, 50)};

// Use the array of points to construct a path.
GraphicsPath path;
path.AddLines(points, 10);

// Use the path to construct a path gradient brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to red.
pthGrBrush.SetCenterColor(Color(255, 255, 0, 0));

// Set the colors of the points in the array.
Color colors[] = {Color(255, 0, 0, 0),   Color(255, 0, 255, 0),
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255), 
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0), 
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255),
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0)};

int count = 10;
pthGrBrush.SetSurroundColors(colors, &count);

// Fill the path with the path gradient brush.
graphics.FillPath(&pthGrBrush, &path);
pthGrBrush.SetGammaCorrection(TRUE);
graphics.TranslateTransform(200.0f, 0.0f);
graphics.FillPath(&pthGrBrush, &path);
```



Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes. Der Stern auf der rechten Seite weist eine Gammakorrektur auf. Beachten Sie, dass der Stern auf der linken Seite, der keine Gammakorrektur aufwies, dunkle Bereiche aufwies.

![Abbildung von zwei Fünf-Point-Starts mit farbiger Farbverlaufsfüllung; Die erste hat dunkle Bereiche, die zweite nicht.](images/gammagradient2.png)

 

 



