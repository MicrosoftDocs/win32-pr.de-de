---
description: 'Sie können die Gammakorrektur für einen Farbverlaufs Pinsel aktivieren, indem Sie true an die PathGradientBrush:: setgammacorrection-Methode dieses Pinsels übergeben.'
ms.assetid: 47472e41-f469-44f4-8b39-cf3982b79f9e
title: Anwenden der Gamma Korrektur auf einen Farbverlauf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e51673e8be4fd289286ce5e4e3e8f7c5469724
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131388"
---
# <a name="applying-gamma-correction-to-a-gradient"></a>Anwenden der Gamma Korrektur auf einen Farbverlauf

Sie können die Gammakorrektur für einen Farbverlaufs Pinsel aktivieren, indem Sie **true** an die [**PathGradientBrush:: setgammacorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) -Methode dieses Pinsels übergeben. Sie können die Gammakorrektur deaktivieren, indem Sie **false** an die **PathGradientBrush:: setgammacorrection** -Methode übergeben. Die Gamma Korrektur ist standardmäßig deaktiviert.

Im folgenden Beispiel wird ein linearer Farbverlaufs Pinsel erstellt und mithilfe dieses Pinsels zwei Rechtecke gefüllt. Das erste Rechteck wird ohne Gammakorrektur gefüllt, und das zweite Rechteck ist mit der Gammakorrektur gefüllt.


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



Die folgende Abbildung zeigt die zwei gefüllten Rechtecke. Das obere Rechteck, das keine Gammakorrektur hat, wird in der Mitte dunkel angezeigt. Das untere Rechteck, das über eine Gammakorrektur verfügt, scheint eine einheitlichere Intensität zu haben.

![Abbildung mit zwei Rechtecke: die farbige Füllung der ersten variiert in der Intensität, die Füllung der zweiten variiert weniger](images/gammagradient1.png)

Im folgenden Beispiel wird ein Pfad Farbverlaufs Pinsel basierend auf einem sternförmigen Pfad erstellt. Im Code wird der Pfad Farbverlaufs Pinsel mit deaktivierter Gammakorrektur (Standardeinstellung) verwendet, um den Pfad auszufüllen. Dann übergibt der Code " **true** " an die [**PathGradientBrush:: setgammacorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) -Methode, um die Gammakorrektur für den Pfad Farbverlaufs Pinsel zu aktivieren. Der-Befehl " [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) " legt die globale Transformation eines [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts fest, sodass der nachfolgende aufzurufende [**Grafik:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) einen Stern füllt, der sich rechts vom ersten Stern befindet.


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



Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes. Der Stern auf der rechten Seite verfügt über eine Gammakorrektur. Beachten Sie, dass der Stern auf der linken Seite, der nicht über eine Gammakorrektur verfügt, Bereiche enthält, die dunkel erscheinen.

![Abbildung von 2 5-pointiert beginnt mit farbiger Farbverlaufsfüllung. der erste verfügt über dunkle Bereiche, die zweite nicht](images/gammagradient2.png)

 

 



