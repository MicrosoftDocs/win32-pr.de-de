---
description: Sie können die Image-Klasse verwenden, um Rasterbilder (Bitmaps) und Vektorbilder (Metadateien) zu laden und anzuzeigen.
ms.assetid: 0ad2a132-6db6-4099-81a2-10e1cd1b1f61
title: Zeichnen, Positionieren und Klonen von Bildern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e37e53ce3937d4f10b91a92e64feec57c6b39e718e7b551e4e4130569d4dd90d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015150"
---
# <a name="drawing-positioning-and-cloning-images"></a>Zeichnen, Positionieren und Klonen von Bildern

Sie können die [**Image-Klasse**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) verwenden, um Rasterbilder (Bitmaps) und Vektorbilder (Metadateien) zu laden und anzuzeigen. Um ein Bild anzuzeigen, benötigen Sie ein [**Grafikobjekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) und ein **Bildobjekt.** Das **Graphics-Objekt** stellt die [**Graphics::D rawImage-Methode**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) bereit, die die Adresse des **Image-Objekts** als Argument empfängt.

Im folgenden Beispiel wird ein [**Image-Objekt**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) aus der Datei Climber.jpg erstellt und dann das Bild angezeigt. Der Zielpunkt für die obere linke Ecke des Bilds (10, 10) wird im zweiten und dritten Parameter der [**Graphics::D rawImage-Methode**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) angegeben.


```
Image myImage(L"Climber.jpg");
myGraphics.DrawImage(&myImage, 10, 10);
```



Der vorangehende Code erzeugte zusammen mit einer bestimmten Datei Climber.jpg die folgende Ausgabe.

![Screenshot eines Fensters, das ein Foto enthält](images/aboutgdip03-art04.png)

Sie können [**Bildobjekte**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) aus einer Vielzahl von Grafikdateiformaten erstellen: BMP, GIF, JPEG, Exif, PNG, TIFF, WMF, EMF und ICON.

Im folgenden Beispiel werden [**Bildobjekte**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) aus einer Vielzahl von Dateitypen erstellt und dann die Bilder angezeigt.


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



Die [**Image-Klasse**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) stellt eine [**Image::Clone-Methode**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-image-clone) bereit, mit der Sie eine Kopie eines vorhandenen **Bild-,** [**Metadatei-**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile)oder [**Bitmapobjekts**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) erstellen können. Die [Clone-Methode](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat)) wird in der **Bitmap-Klasse** überladen, und eine der Variationen verfügt über einen Quellrechteckparameter, mit dem Sie den Teil des ursprünglichen Bilds angeben können, das Sie kopieren möchten. Im folgenden Beispiel wird ein **Bitmap-Objekt** erstellt, indem die obere Hälfte eines vorhandenen **Bitmap-Objekts** klont wird. Anschließend werden beide Bilder angezeigt.


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



Der vorangehende Code erzeugte zusammen mit einer bestimmten Datei Spiral.png die folgende Ausgabe.

![Abbildung eines Bilds, gefolgt von der oberen Hälfte des Orignal-Bilds](images/aboutgdip03-art05.png)

 

 
