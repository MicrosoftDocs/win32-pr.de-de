---
title: Zuschneiden und Skalieren von GDI+-Images
description: Die Grafikklasse stellt mehrere DrawImage-Methoden bereit, von denen einige über Quell-und Ziel Rechteck Parameter verfügen, die Sie zum Zuschneiden und Skalieren von Bildern verwenden können.
ms.assetid: cad64615-d8e6-4c03-a6c7-c98267a8f159
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c70a7b4f7aa0374602326ab856a01bbadc0047
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988211"
---
# <a name="cropping-and-scaling-gdi-images"></a>Zuschneiden und Skalieren von GDI+-Images

Die [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse stellt mehrere **DrawImage** -Methoden bereit, von denen einige über Quell-und Ziel Rechteck Parameter verfügen, die Sie zum Zuschneiden und Skalieren von Bildern verwenden können.

Im folgenden Beispiel wird ein [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus dem Datei Apple.gif erstellt. Der Code zeichnet das gesamte Apple-Image in seiner ursprünglichen Größe. Der Code ruft dann die **DrawImage** -Methode eines [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts auf, um einen Teil des Apple-Bilds in einem Ziel Rechteck zu zeichnen, das größer ist als das ursprüngliche Apple-Image.

Mit der **DrawImage** -Methode wird bestimmt, welcher Teil des Apple gezeichnet werden soll, indem das Quell Rechteck betrachtet wird, das durch das dritte, vierte, fünfte und sechste Argument angegeben wird. In diesem Fall wird Apple auf 75 Prozent seiner Breite und 75 Prozent seiner Höhe zugeschnitten.

Mit der **DrawImage** -Methode wird festgelegt, wo der gezeichnete Apple gezeichnet werden soll und wie groß das abgeschnittene Apple ist, indem das Ziel Rechteck betrachtet wird, das durch das zweite Argument angegeben wird. In diesem Fall ist das Ziel Rechteck um 30 Prozent breiter und 30 Prozent höher als das ursprüngliche Bild.


```
Image image(L"Apple.gif");
UINT width = image.GetWidth();
UINT height = image.GetHeight();
// Make the destination rectangle 30 percent wider and
// 30 percent taller than the original image.
// Put the upper-left corner of the destination
// rectangle at (150, 20).
Rect destinationRect(150, 20, 1.3 * width, 1.3 * height);
// Draw the image unaltered with its upper-left corner at (0, 0).
graphics.DrawImage(&image, 0, 0);
// Draw a portion of the image. Scale that portion of the image
// so that it fills the destination rectangle.
graphics.DrawImage(
   &image,
   destinationRect,
   0, 0,              // upper-left corner of source rectangle
   0.75 * width,      // width of source rectangle
   0.75 * height,     // height of source rectangle
   UnitPixel);
```



Die folgende Abbildung zeigt das ursprüngliche Apple und das skalierte, ausgeschnittene Apple.

![Abbildung zeigt ein Apple, dann ein vergrößerter Teil des ursprünglichen Apple](images/cropscale1.png)

 

 



