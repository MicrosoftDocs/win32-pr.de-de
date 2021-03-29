---
description: Wenn Sie eine Form ausfüllen, müssen Sie die Adresse eines Pinsel Objekts an eine der Füll Methoden der Grafikklasse übergeben.
ms.assetid: 42e36c32-ed20-4c5f-bcba-004d795babe3
title: Zeichnen mit nicht transparenten und halbtransparenten Pinseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877f922fff21f964349afbe1762cc458e60391b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131349"
---
# <a name="drawing-with-opaque-and-semitransparent-brushes"></a>Zeichnen mit nicht transparenten und halbtransparenten Pinseln

Wenn Sie eine Form ausfüllen, müssen Sie die Adresse eines [**Pinsel**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) Objekts an eine der Füll Methoden der [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse übergeben. Der einzige Parameter des [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) -Konstruktors ist ein [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) -Objekt. Um eine nicht transparente Form auszufüllen, legen Sie den Alphaanteil der Farbe auf 255 fest. Um eine halb transparente Form auszufüllen, legen Sie den Alphaanteil auf einen beliebigen Wert von 1 bis 254 fest.

Wenn Sie eine halb transparente Form ausfüllen, wird die Farbe der Form mit den Hintergrundfarben gemischt. Die Alpha Komponente gibt an, wie die Form-und Hintergrundfarben gemischt werden. Alpha-Werte in der Nähe von 0 stellen eine höhere Gewichtung der Hintergrundfarben dar, und Alpha Werte in der Nähe von 255 platzieren die Farbe der Form.

Im folgenden Beispiel wird ein Bild gezeichnet und anschließend drei Ellipsen aufgefüllt, die sich überlappen. Für die erste Ellipse wird ein Alphaanteil von 255 verwendet. Die Ellipse ist daher nicht transparent. Die zweite und die dritte Ellipse verwenden einen Alphaanteil von 128. Sie sind daher halb transparent. Das Hintergrundbild scheint also durch die Ellipsen hindurch. Der aufzurufende [**Grafik:: setcompositingquality**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) bewirkt, dass die Mischung für die dritte Ellipse in Verbindung mit der Gammakorrektur erfolgt.


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

![Abbildung der Darstellung eines Bilds, das durch drei Ellipsen überlagert wird: ein undurchsichtiges, ein wenig transparent, ein sehr transparent](images/compqualellipse.png)

 

 



