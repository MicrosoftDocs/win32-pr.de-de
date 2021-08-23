---
description: 'Es kann manchmal sein, dass Sie eine Bitmap im Off-Screen-Format erstellen möchten, die die folgenden Merkmale aufweist:'
ms.assetid: 2a7590ce-daf4-4892-a838-603e3f89b1bb
title: Verwenden des Compositing-Modus zum Steuern des Alphablendings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ea2fc9d5be10e3a73bacf7f5a6dc5cbecb8c2992ac8cd961701f55fc2cb524d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611986"
---
# <a name="using-compositing-mode-to-control-alpha-blending"></a>Verwenden des Compositing-Modus zum Steuern des Alphablendings

Es kann manchmal sein, dass Sie eine Bitmap im Off-Screen-Format erstellen möchten, die die folgenden Merkmale aufweist:

-   Farben haben Alphawerte, die kleiner als 255 sind.
-   Farben werden beim Erstellen der Bitmap nicht alphablendet.
-   Wenn Sie die fertige Bitmap anzeigen, werden Farben in der Bitmap mit den Hintergrundfarben auf dem Anzeigegerät kombiniert.

Um eine solche Bitmap zu [](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) erstellen, erstellen Sie ein leeres Bitmap-Objekt, und erstellen Sie dann ein [**Grafikobjekt**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basierend auf dieser Bitmap. Legen Sie den Compositing-Modus des **Grafikobjekts** auf CompositingModeSourceCopy fest.

Im folgenden Beispiel wird ein [**Grafikobjekt basierend**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) auf einem [**Bitmap-Objekt**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) erstellt. Der Code verwendet das **Grafikobjekt** zusammen mit zwei halbtransparenten Pinseln (Alpha = 160), um die Bitmap zu zeichnen. Der Code füllt eine rote Ellipse und eine grüne Ellipse mithilfe der halbtransparenten Pinsel. Die grüne Ellipse überlappt die rote Ellipse, aber das grüne wird nicht mit dem roten überblendet, da der Compositing-Modus des **Graphics-Objekts** auf CompositingModeSourceCopy festgelegt ist.

Als Nächstes bereitet der Code das Zeichnen auf dem Bildschirm vor, indem [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) aufruft und ein [**Grafikobjekt**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basierend auf einem Gerätekontext erstellt wird. Der Code zeichnet die Bitmap zweimal auf dem Bildschirm: einmal auf einem weißen Hintergrund und einmal auf einem mehrfarbigen Hintergrund. Die Pixel in der Bitmap, die Teil der beiden Ausellipsen sind, haben eine Alphakomponente von 160, sodass die Ausellipsen mit den Hintergrundfarben auf dem Bildschirm kombiniert werden.


```
// Create a blank bitmap.
Bitmap bitmap(180, 100);
// Create a Graphics object that can be used to draw on the bitmap.
Graphics bitmapGraphics(&bitmap);
// Create a red brush and a green brush, each with an alpha value of 160.
SolidBrush redBrush(Color(210, 255, 0, 0));
SolidBrush greenBrush(Color(210, 0, 255, 0));
// Set the compositing mode so that when overlapping ellipses are drawn,
// the colors of the ellipses are not blended.
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
// Fill an ellipse using a red brush that has an alpha value of 160.
bitmapGraphics.FillEllipse(&redBrush, 0, 0, 150, 70);
// Fill a second ellipse using green brush that has an alpha value of 160. 
// The green ellipse overlaps the red ellipse, but the green is not 
// blended with the red.
bitmapGraphics.FillEllipse(&greenBrush, 30, 30, 150, 70);
// Prepare to draw on the screen.
hdc = BeginPaint(hWnd, &ps);
Graphics* pGraphics = new Graphics(hdc);
pGraphics->SetCompositingQuality(CompositingQualityGammaCorrected);
// Draw a multicolored background.
SolidBrush brush(Color((ARGB)Color::Aqua));
pGraphics->FillRectangle(&brush, 200, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Yellow));
pGraphics->FillRectangle(&brush, 260, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Fuchsia));
pGraphics->FillRectangle(&brush, 320, 0, 60, 100);
   
// Display the bitmap on a white background.
pGraphics->DrawImage(&bitmap, 0, 0);
// Display the bitmap on a multicolored background.
pGraphics->DrawImage(&bitmap, 200, 0);
delete pGraphics;
EndPaint(hWnd, &ps);
```



Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes. Beachten Sie, dass die Ausellipsen mit dem Hintergrund kombiniert werden, aber nicht miteinander kombiniert werden.

![Abbildung mit zwei unterschiedlich farbigen Ellipsen, von denen jede mit ihrem mehrfarbigen Hintergrund kombiniert wird](images/sourcecopy.png)

Das vorangehende Codebeispiel verfügt über die folgende Anweisung:


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
```



Wenn die Ausellipsen miteinander und mit dem Hintergrund kombiniert werden sollen, ändern Sie diese Anweisung wie folgt:


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceOver);
```



Die folgende Abbildung zeigt die Ausgabe des überarbeiteten Codes.

![Verwenden des Compositingmodus zum Steuern der Alphablendingdarstellung](images/sourceover.png)

 

 



