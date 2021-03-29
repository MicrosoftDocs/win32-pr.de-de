---
description: Sie können die Image-Klasse verwenden, um Rasterbilder (Bitmaps) und Vektorbilder (Metadateien) zu laden und anzuzeigen.
ms.assetid: 0ad2a132-6db6-4099-81a2-10e1cd1b1f61
title: Zeichnen, Positionieren und Klonen von Bildern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa265a8f75cbfcaf0ff614ded4466482e5b986b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215587"
---
# <a name="drawing-positioning-and-cloning-images"></a>Zeichnen, Positionieren und Klonen von Bildern

Sie können die [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse verwenden, um Rasterbilder (Bitmaps) und Vektorbilder (Metadateien) zu laden und anzuzeigen. Zum Anzeigen eines Bilds benötigen Sie ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und ein **Bild** Objekt. Das **Grafik** Objekt stellt die [**Grafik::D rawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) -Methode bereit, die die Adresse des **Image** -Objekts als Argument empfängt.

Im folgenden Beispiel wird ein [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus der Datei Climber.jpg erstellt und dann das Bild angezeigt. Der Zielpunkt für die obere linke Ecke des Bilds (10, 10) wird im zweiten und dritten Parameter der [**Grafik::D rawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) -Methode angegeben.


```
Image myImage(L"Climber.jpg");
myGraphics.DrawImage(&myImage, 10, 10);
```



Der vorangehende Code hat zusammen mit einer bestimmten Datei (Climber.jpg) die folgende Ausgabe erzeugt.

![Screenshot eines Fensters mit einem Foto](images/aboutgdip03-art04.png)

Sie können [**Bild**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) Objekte aus einer Vielzahl von Grafikdatei Formaten erstellen: BMP, GIF, JPEG, EXIF, PNG, TIFF, WMF, EMF und Symbol.

Im folgenden Beispiel werden [**Bild**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) Objekte aus einer Vielzahl von Dateitypen erstellt und dann die Bilder angezeigt.


```
Image myBMP(L"SpaceCadet.bmp");
Image myEMF(L"Metafile1.emf");
Image myGIF(L"Soda.gif");
Image myJPEG(L"Mango.jpg");
Image myPNG(L"Flowers.png");
Image myTIFF(L"MS.tif");

myGraphics.DrawImage(&myBMP, 10, 10);
myGraphics.DrawImage(&myEMF, 220, 10);
myGraphics.DrawImage(&myGIF, 320, 10);
myGraphics.DrawImage(&myJPEG, 380, 10);
myGraphics.DrawImage(&myPNG, 150, 200);
myGraphics.DrawImage(&myTIFF, 300, 200);
```



Die [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse stellt eine [**Image:: Clone**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-image-clone) -Methode bereit, die Sie verwenden können, um eine Kopie eines vorhandenen **Bilds**, einer [**Metadatendatei**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile)oder eines [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Objekts zu erstellen. Die [Clone](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat)) -Methode wird in der **Bitmap** -Klasse überladen, und eine der Variationen verfügt über einen Quell Rechteck Parameter, mit dem Sie den Teil des ursprünglichen Bilds angeben können, den Sie kopieren möchten. Im folgenden Beispiel wird ein **Bitmap** -Objekt erstellt, indem die obere Hälfte eines vorhandenen **Bitmap** -Objekts geklont wird. Anschließend werden beide Bilder angezeigt.


```
Bitmap* originalBitmap = new Bitmap(L"Spiral.png");
RectF sourceRect(
   0.0f,
   0.0f, 
   (REAL)(originalBitmap->GetWidth()), 
   (REAL)(originalBitmap->GetHeight())/2.0f);

Bitmap* secondBitmap = originalBitmap->Clone(sourceRect, PixelFormatDontCare);

myGraphics.DrawImage(originalBitmap, 10, 10);
myGraphics.DrawImage(secondBitmap, 100, 10);
```



Der vorangehende Code hat zusammen mit einer bestimmten Datei (Spiral.png) die folgende Ausgabe erzeugt.

![Abbildung eines Bilds, gefolgt von der oberen Hälfte des ursprünglicher-Bilds](images/aboutgdip03-art05.png)

 

 
