---
description: Wenn Sie eine Linie zeichnen, müssen Sie die Adresse eines Stift Objekts an die DrawLine-Methode der Grafikklasse übergeben.
ms.assetid: 4524908f-f9c2-4807-b045-eb9e43a6668b
title: Zeichnen deckender und halb transparenter Linien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f751e5808440c1051b3cd996f7ebcb2df0ccbcd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555648"
---
# <a name="drawing-opaque-and-semitransparent-lines"></a>Zeichnen deckender und halb transparenter Linien

Wenn Sie eine Linie zeichnen, müssen Sie die Adresse eines [**Stift**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) Objekts an die [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) -Methode der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse übergeben. Einer der Parameter des **Stift** -Konstruktors ist ein [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) -Objekt. Um eine nicht transparente Linie zu zeichnen, legen Sie den Alphaanteil der Farbe auf 255 fest. Um eine halb transparente Linie zu zeichnen, legen Sie den Alphaanteil auf einen beliebigen Wert von 1 bis 254 fest.

Wenn Sie eine halb transparente Linie vor einem Hintergrund zeichnen, wird Linienfarbe mit den Hintergrundfarben gemischt. Die Alpha Komponente gibt an, wie die Zeilen-und Hintergrundfarben gemischt werden. Alpha-Werte in der Nähe von 0 stellen eine höhere Gewichtung der Hintergrundfarben dar, und Alpha Werte in der Nähe von 255 platzieren die Linien Farbe stärker.

Im folgenden Beispiel wird ein Bild gezeichnet und anschließend drei Zeilen gezeichnet, die das Bild als Hintergrund verwenden. Für die erste Linie wird ein Alphaanteil von 255 verwendet. Die Linie ist daher nicht transparent. Die zweite und die dritte Linie verwenden einen Alphaanteil von 128. Sie sind daher halb transparent. Das Hintergrundbild scheint also durch die Linien hindurch. Der aufzurufende [**Grafik:: setcompositingquality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) bewirkt, dass die Mischung für die dritte Zeile in Verbindung mit der Gammakorrektur erfolgt.


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

![Darstellung eines Bilds, das durch drei Breite Linien überlagert wird: ein undurchsichtiges, ein leicht transparenter und ein sehr transparentes](images/compqualline.png)

 

 



