---
description: Wenn Sie eine Linie zeichnen, müssen Sie die Adresse eines Stiftobjekts an die DrawLine-Methode der Graphics-Klasse übergeben.
ms.assetid: 4524908f-f9c2-4807-b045-eb9e43a6668b
title: Zeichnen deckender und halb transparenter Linien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14cdf31a80be9ac2a0cf61a2a8eb82f530dc3558c876cba9190a79f42ac35baa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036758"
---
# <a name="drawing-opaque-and-semitransparent-lines"></a>Zeichnen deckender und halb transparenter Linien

Wenn Sie eine Linie zeichnen, müssen Sie die Adresse eines [**Stiftobjekts**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) an die [DrawLine-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) der [**Graphics-Klasse**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) übergeben. Einer der Parameter des **Stiftkonstruktors** ist ein [**Color-Objekt.**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) Um eine nicht transparente Linie zu zeichnen, legen Sie den Alphaanteil der Farbe auf 255 fest. Um eine halb transparente Linie zu zeichnen, legen Sie den Alphaanteil auf einen beliebigen Wert von 1 bis 254 fest.

Wenn Sie eine halb transparente Linie vor einem Hintergrund zeichnen, wird Linienfarbe mit den Hintergrundfarben gemischt. Die Alphakomponente gibt an, wie die Linien- und Hintergrundfarben gemischt werden. Alphawerte in der Nähe von 0 legen mehr Gewichtung auf die Hintergrundfarben fest, und Alphawerte in der Nähe von 255 platzieren die Linienfarbe stärker.

Das folgende Beispiel zeichnet ein Bild und zeichnet dann drei Linien, die das Bild als Hintergrund verwenden. Für die erste Linie wird ein Alphaanteil von 255 verwendet. Die Linie ist daher nicht transparent. Die zweite und die dritte Linie verwenden einen Alphaanteil von 128. Sie sind daher halb transparent. Das Hintergrundbild scheint also durch die Linien hindurch. Der Aufruf von [**Graphics::SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) bewirkt, dass die Überblendung für die dritte Zeile in Verbindung mit der Gammakorrektur durchgeführt wird.


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 10, 5, image.GetWidth(), image.GetHeight());
Pen opaquePen(Color(255, 0, 0, 255), 15);
Pen semiTransPen(Color(128, 0, 0, 255), 15);
graphics.DrawLine(&opaquePen, 0, 20, 100, 20);
graphics.DrawLine(&semiTransPen, 0, 40, 100, 40);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.DrawLine(&semiTransPen, 0, 60, 100, 60);
```



Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes.

![Abbildung, die ein Bild zeigt, das von drei breiten Linien überlagert ist: eine nicht transparent, eine leicht transparent und eine sehr transparent](images/compqualline.png)

 

 



