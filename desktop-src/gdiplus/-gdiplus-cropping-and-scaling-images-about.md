---
title: Informationen zum Zuschneiden und Skalieren von GDI+-Bilds
description: Sie können die DrawImage-Methode der Grafikklasse verwenden, um Bilder zu zeichnen und zu positionieren.
ms.assetid: 81d20adc-0481-4b1b-80aa-ae218fdecd84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b44a13b5cee632e6ceafe327f94eca48edd93dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131353"
---
# <a name="about-cropping-and-scaling-gdi-images"></a>Informationen zum Zuschneiden und Skalieren von GDI+-Bilds

Sie können die [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) -Methode der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse verwenden, um Bilder zu zeichnen und zu positionieren. DrawImage ist eine überladene Methode, daher gibt es mehrere Möglichkeiten, Sie mit Argumenten bereitzustellen. Eine Variation der [**Grafik::D rawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) -Methode empfängt die Adresse eines [**Bild**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) Objekts und einen Verweis auf ein [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) -Objekt. Das Rechteck gibt das Ziel für den Zeichnungs Vorgang an. Das heißt, es gibt das Rechteck an, in dem das Bild gezeichnet wird. Wenn sich die Größe des Ziel Rechtecks von der Größe des ursprünglichen Bilds unterscheidet, wird das Bild so skaliert, dass es an das Ziel Rechteck angepasst wird. Im folgenden Beispiel wird das gleiche Bild dreimal gezeichnet: einmal ohne Skalierung, einmal mit einer Erweiterung und einmal mit einer Komprimierung.


```
Bitmap myBitmap(L"Spiral.png");
Rect expansionRect(80, 10, 2 * myBitmap.GetWidth(), myBitmap.GetHeight());
Rect compressionRect(210, 10, myBitmap.GetWidth() / 2, 
   myBitmap.GetHeight() / 2);

myGraphics.DrawImage(&myBitmap, 10, 10);
myGraphics.DrawImage(&myBitmap, expansionRect);
myGraphics.DrawImage(&myBitmap, compressionRect);
```



Der vorangehende Code hat zusammen mit einer bestimmten Datei (Spiral.png) die folgende Ausgabe erzeugt.

![die Abbildung zeigt drei Versionen eines Bilds: normal, gestreckt und auf die Hälfte der ursprünglichen Größe verkleinert.](images/aboutgdip03-art06.png)

Einige Variationen der [**Grafik::D rawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) -Methode verfügt über einen Parameter des Quell Rechtecks und einen Parameter für das Ziel Rechteck. Das Quell Rechteck gibt den Teil des ursprünglichen Bilds an, der gezeichnet wird. Das Ziel Rechteck gibt an, wo der Teil des Bilds gezeichnet wird. Wenn sich die Größe des Ziel Rechtecks von der Größe des Quell Rechtecks unterscheidet, wird das Bild so skaliert, dass es an das Ziel Rechteck angepasst wird.

Im folgenden Beispiel wird ein [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Objekt aus dem Datei Runner.jpg erstellt. Das gesamte Bild wird ohne Skalierung bei (0,0) gezeichnet. Anschließend wird ein kleiner Teil des Bilds zweimal gezeichnet: einmal mit einer Komprimierung und einmal mit einer Erweiterung.


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



Die folgende Abbildung zeigt das nicht skalierte Bild und die komprimierten und erweiterten Bild Teile.

![Screenshot, der ein Bild anzeigt, ein Teil des Bilds und dann der gleiche Teil erweitert](images/aboutgdip03-art07.png)

 

 



