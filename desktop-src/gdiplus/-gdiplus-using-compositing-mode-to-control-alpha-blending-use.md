---
description: 'Es kann vorkommen, dass Sie eine Offscreen-Bitmap erstellen möchten, die über die folgenden Eigenschaften verfügt:'
ms.assetid: 2a7590ce-daf4-4892-a838-603e3f89b1bb
title: Verwenden des Compositing-Modus zum Steuern der Alpha Mischung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db54c71ac9687a1ddf28db09b922b7799d0ebaa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978912"
---
# <a name="using-compositing-mode-to-control-alpha-blending"></a>Verwenden des Compositing-Modus zum Steuern der Alpha Mischung

Es kann vorkommen, dass Sie eine Offscreen-Bitmap erstellen möchten, die über die folgenden Eigenschaften verfügt:

-   Farben haben alpha-Werte, die kleiner als 255 sind.
-   Farben werden bei der Erstellung der Bitmap nicht mit einander gemischt.
-   Wenn Sie die fertige Bitmap anzeigen, werden Farben in der Bitmap mit den Hintergrundfarben auf dem Anzeigegerät gemischt.

Um eine solche Bitmap zu erstellen, erstellen Sie ein leeres [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Objekt, und erstellen Sie dann auf der Grundlage dieser Bitmap ein [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt. Legen Sie den Zusammensetzung-Modus des **Grafik** Objekts auf compositingmodesourcecopy fest.

Im folgenden Beispiel wird ein [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt erstellt, das auf einem [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Objekt basiert. Der Code verwendet das **Grafik** Objekt zusammen mit zwei semitransparenten Pinseln (Alpha = 160), um die Bitmap zu zeichnen. Der Code füllt eine rote Ellipse und eine grüne Ellipse mithilfe der semitransparenten Pinsel. Die grüne Ellipse überlappt die rote Ellipse, das grüne wird jedoch nicht mit der roten Ellipse kombiniert, da der Zusammensetzung-Modus des **Grafik** Objekts auf compositingmodesourcecopy festgelegt ist.

Im nächsten Schritt bereitet der Code das Zeichnen auf dem Bildschirm vor, indem [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) aufgerufen und ein [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt auf der Grundlage eines Geräte Kontexts erstellt wird. Der Code zeichnet die Bitmap zweimal auf dem Bildschirm: einmal auf einem weißen Hintergrund und einmal in einem mehrfarbigen Hintergrund. Die Pixel in der Bitmap, die Teil der beiden Ellipsen sind, haben eine Alpha Komponente von 160, sodass die Ellipsen mit den Hintergrundfarben auf dem Bildschirm kombiniert werden.


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



Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes. Beachten Sie, dass die Ellipsen mit dem Hintergrund kombiniert werden, aber nicht miteinander vermischt werden.

![Abbildung: zwei anders farbige Ellipsen, die jeweils mit dem mehrfarbigen Hintergrund kombiniert werden](images/sourcecopy.png)

Das vorangehende Codebeispiel enthält die folgende-Anweisung:


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
```



Wenn Sie möchten, dass die Ellipsen miteinander und mit dem Hintergrund kombiniert werden sollen, ändern Sie die Anweisung wie folgt:


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceOver);
```



Die folgende Abbildung zeigt die Ausgabe des überarbeiteten Codes.

![Verwenden des Zusammensetzung-Modus zum Steuern der Alpha Blending-Darstellung](images/sourceover.png)

 

 



