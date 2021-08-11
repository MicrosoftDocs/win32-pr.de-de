---
description: Wenn Sie eine Form ausfüllen, müssen Sie die Adresse eines Brush-Objekts an eine der Füllmethoden der Graphics-Klasse übergeben.
ms.assetid: 42e36c32-ed20-4c5f-bcba-004d795babe3
title: Zeichnen mit nicht transparenten und halbtransparenten Pinseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce5bb89c460c9769f805fb33af9eb91e9d8207448e702476aff4d25dec33a18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248874"
---
# <a name="drawing-with-opaque-and-semitransparent-brushes"></a>Zeichnen mit nicht transparenten und halbtransparenten Pinseln

Wenn Sie eine Form ausfüllen, müssen Sie die Adresse eines [**Brush-Objekts**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) an eine der Füllmethoden der [**Graphics-Klasse**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) übergeben. Der eine Parameter des [**SolidBrush-Konstruktors**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) ist ein [**Color-Objekt.**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) Um eine nicht transparente Form auszufüllen, legen Sie den Alphaanteil der Farbe auf 255 fest. Um eine halb transparente Form auszufüllen, legen Sie den Alphaanteil auf einen beliebigen Wert von 1 bis 254 fest.

Wenn Sie eine halb transparente Form ausfüllen, wird die Farbe der Form mit den Hintergrundfarben gemischt. Die Alphakomponente gibt an, wie form- und hintergrundfarben gemischt werden. Alphawerte nahe 0 legen mehr Gewichtung auf die Hintergrundfarben, und Alphawerte nahe 255 wägen die Formfarbe stärker ab.

Das folgende Beispiel zeichnet ein Bild und füllt dann drei Ellipsen aus, die das Bild überlappen. Für die erste Ellipse wird ein Alphaanteil von 255 verwendet. Die Ellipse ist daher nicht transparent. Die zweite und die dritte Ellipse verwenden einen Alphaanteil von 128. Sie sind daher halb transparent. Das Hintergrundbild scheint also durch die Ellipsen hindurch. Der Aufruf von [**Graphics::SetCompositingQuality**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) bewirkt, dass das Blending für die dritte Ellipse in Verbindung mit der Gammakorrektur erfolgt.


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 50, 50, image.GetWidth(), image.GetHeight());
SolidBrush opaqueBrush(Color(255, 0, 0, 255));
SolidBrush semiTransBrush(Color(128, 0, 0, 255));
graphics.FillEllipse(&opaqueBrush, 35, 45, 45, 30);
graphics.FillEllipse(&semiTransBrush, 86, 45, 45, 30);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.FillEllipse(&semiTransBrush, 40, 90, 86, 30);
```



Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes.

![Abbildung, die ein Bild zeigt, das von drei Ausellipsen überlagert ist: eine nicht transparent, eine etwas transparent, eine sehr transparent](images/compqualellipse.png)

 

 



