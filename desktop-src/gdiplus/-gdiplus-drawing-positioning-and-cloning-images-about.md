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
# <a name="drawing-positioning-and-cloning-images"></a><span data-ttu-id="25f52-103">Zeichnen, Positionieren und Klonen von Bildern</span><span class="sxs-lookup"><span data-stu-id="25f52-103">Drawing, Positioning, and Cloning Images</span></span>

<span data-ttu-id="25f52-104">Sie können die [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse verwenden, um Rasterbilder (Bitmaps) und Vektorbilder (Metadateien) zu laden und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="25f52-104">You can use the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class to load and display raster images (bitmaps) and vector images (metafiles).</span></span> <span data-ttu-id="25f52-105">Zum Anzeigen eines Bilds benötigen Sie ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und ein **Bild** Objekt.</span><span class="sxs-lookup"><span data-stu-id="25f52-105">To display an image, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and an **Image** object.</span></span> <span data-ttu-id="25f52-106">Das **Grafik** Objekt stellt die [**Grafik::D rawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) -Methode bereit, die die Adresse des **Image** -Objekts als Argument empfängt.</span><span class="sxs-lookup"><span data-stu-id="25f52-106">The **Graphics** object provides the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) method, which receives the address of the **Image** object as an argument.</span></span>

<span data-ttu-id="25f52-107">Im folgenden Beispiel wird ein [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus der Datei Climber.jpg erstellt und dann das Bild angezeigt.</span><span class="sxs-lookup"><span data-stu-id="25f52-107">The following example constructs an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Climber.jpg and then displays the image.</span></span> <span data-ttu-id="25f52-108">Der Zielpunkt für die obere linke Ecke des Bilds (10, 10) wird im zweiten und dritten Parameter der [**Grafik::D rawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) -Methode angegeben.</span><span class="sxs-lookup"><span data-stu-id="25f52-108">The destination point for the upper-left corner of the image, (10, 10), is specified in the second and third parameters of the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) method.</span></span>


```
Image myImage(L"Climber.jpg");
myGraphics.DrawImage(&myImage, 10, 10);
```



<span data-ttu-id="25f52-109">Der vorangehende Code hat zusammen mit einer bestimmten Datei (Climber.jpg) die folgende Ausgabe erzeugt.</span><span class="sxs-lookup"><span data-stu-id="25f52-109">The preceding code, along with a particular file, Climber.jpg, produced the following output.</span></span>

![Screenshot eines Fensters mit einem Foto](images/aboutgdip03-art04.png)

<span data-ttu-id="25f52-111">Sie können [**Bild**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) Objekte aus einer Vielzahl von Grafikdatei Formaten erstellen: BMP, GIF, JPEG, EXIF, PNG, TIFF, WMF, EMF und Symbol.</span><span class="sxs-lookup"><span data-stu-id="25f52-111">You can construct [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) objects from a variety of graphics file formats: BMP, GIF, JPEG, Exif, PNG, TIFF, WMF, EMF, and ICON.</span></span>

<span data-ttu-id="25f52-112">Im folgenden Beispiel werden [**Bild**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) Objekte aus einer Vielzahl von Dateitypen erstellt und dann die Bilder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="25f52-112">The following example constructs [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) objects from a variety of file types and then displays the images.</span></span>


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



<span data-ttu-id="25f52-113">Die [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse stellt eine [**Image:: Clone**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-image-clone) -Methode bereit, die Sie verwenden können, um eine Kopie eines vorhandenen **Bilds**, einer [**Metadatendatei**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile)oder eines [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Objekts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="25f52-113">The [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class provides a [**Image::Clone**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-image-clone) method that you can use to make a copy of an existing **Image**, [**Metafile**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile), or [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="25f52-114">Die [Clone](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat)) -Methode wird in der **Bitmap** -Klasse überladen, und eine der Variationen verfügt über einen Quell Rechteck Parameter, mit dem Sie den Teil des ursprünglichen Bilds angeben können, den Sie kopieren möchten.</span><span class="sxs-lookup"><span data-stu-id="25f52-114">The [Clone](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat)) method is overloaded in the **Bitmap** class, and one of the variations has a source-rectangle parameter that you can use to specify the portion of the original image that you want to copy.</span></span> <span data-ttu-id="25f52-115">Im folgenden Beispiel wird ein **Bitmap** -Objekt erstellt, indem die obere Hälfte eines vorhandenen **Bitmap** -Objekts geklont wird.</span><span class="sxs-lookup"><span data-stu-id="25f52-115">The following example creates a **Bitmap** object by cloning the top half of an existing **Bitmap** object.</span></span> <span data-ttu-id="25f52-116">Anschließend werden beide Bilder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="25f52-116">Then both images are displayed.</span></span>


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



<span data-ttu-id="25f52-117">Der vorangehende Code hat zusammen mit einer bestimmten Datei (Spiral.png) die folgende Ausgabe erzeugt.</span><span class="sxs-lookup"><span data-stu-id="25f52-117">The preceding code, along with a particular file, Spiral.png, produced the following output.</span></span>

![Abbildung eines Bilds, gefolgt von der oberen Hälfte des ursprünglicher-Bilds](images/aboutgdip03-art05.png)

 

 
