---
title: Informationen zum Zuschneiden und Skalieren von GDI+-Bilds
description: Sie können die DrawImage-Methode der Graphics-Klasse verwenden, um Bilder zu zeichnen und zu positionieren.
ms.assetid: 81d20adc-0481-4b1b-80aa-ae218fdecd84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9e69adb7f817c36b955ed313290cf0b762c279b4296e06ad52aa6175ff2c467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036838"
---
# <a name="about-cropping-and-scaling-gdi-images"></a>Informationen zum Zuschneiden und Skalieren von GDI+-Bilds

Sie können die [DrawImage-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) der [**Graphics-Klasse verwenden,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) um Bilder zu zeichnen und zu positionieren. DrawImage ist eine überladene Methode, daher gibt es mehrere Möglichkeiten, sie mit Argumenten zu versorgen. Eine Variante der [**Graphics::D rawImage-Methode**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) empfängt die Adresse eines [**Image-Objekts**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) und einen Verweis auf ein [**Rect-Objekt.**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) Das Rechteck gibt das Ziel für den Zeichnungsvorgang an. Das heißt, sie gibt das Rechteck an, in dem das Bild gezeichnet wird. Wenn sich die Größe des Zielrechtecks von der Größe des ursprünglichen Bilds unterscheiden, wird das Bild so skaliert, dass es dem Zielrechteck passt. Das folgende Beispiel zeichnet das gleiche Bild dreimal: einmal ohne Skalierung, einmal mit einer Erweiterung und einmal mit einer Komprimierung.


```
Bitmap myBitmap(L"Spiral.png");
Rect expansionRect(80, 10, 2 * myBitmap.GetWidth(), myBitmap.GetHeight());
Rect compressionRect(210, 10, myBitmap.GetWidth() / 2, 
   myBitmap.GetHeight() / 2);

myGraphics.DrawImage(&myBitmap, 10, 10);
myGraphics.DrawImage(&myBitmap, expansionRect);
myGraphics.DrawImage(&myBitmap, compressionRect);
```



Der vorangehende Code hat zusammen mit einer bestimmten Datei, Spiral.png, die folgende Ausgabe erzeugt.

![Abbildung mit drei Versionen eines Bilds: normal, gestreckt breit und verkleinern auf die Hälfte der ursprünglichen Größe](images/aboutgdip03-art06.png)

Einige Variationen der [**Graphics::D rawImage-Methode**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) verfügen über einen Source-Rectangle-Parameter sowie einen Destination-Rectangle-Parameter. Das Quellrechteck gibt den Teil des ursprünglichen Bilds an, der gezeichnet wird. Das Zielrechteck gibt an, wo dieser Teil des Bilds gezeichnet wird. Wenn sich die Größe des Zielrechtecks von der Größe des Quellrechtecks unterscheiden, wird das Bild so skaliert, dass es an das Zielrechteck passt.

Im folgenden Beispiel wird ein [**Bitmap-Objekt**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) aus der Datei Runner.jpg. Das gesamte Bild wird ohne Skalierung bei (0, 0) gezeichnet. Anschließend wird ein kleiner Teil des Bilds zweimal gezeichnet: einmal mit einer Komprimierung und einmal mit einer Erweiterung.


```
Bitmap myBitmap(L"Runner.jpg"); 

// The rectangle (in myBitmap) with upper-left corner (80, 70), 
// width 80, and height 45, encloses one of the runner's hands.

// Small destination rectangle for compressed hand.
Rect destRect1(200, 10, 20, 16);

// Large destination rectangle for expanded hand.
Rect destRect2(200, 40, 200, 160);

// Draw the original image at (0, 0).
myGraphics.DrawImage(&myBitmap, 0, 0);

// Draw the compressed hand.
myGraphics.DrawImage(
   &myBitmap, destRect1, 80, 70, 80, 45, UnitPixel);

// Draw the expanded hand. 
myGraphics.DrawImage(
   &myBitmap, destRect2, 80, 70, 80, 45, UnitPixel);
```



Die folgende Abbildung zeigt das nicht skalierte Bild sowie die komprimierten und erweiterten Bildteile.

![Screenshot, der ein Bild zeigt, dann einen Teil des Bilds komprimiert und dann den gleichen Teil erweitert](images/aboutgdip03-art07.png)

 

 



