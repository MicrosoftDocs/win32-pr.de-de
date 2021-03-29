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
# <a name="about-cropping-and-scaling-gdi-images"></a><span data-ttu-id="eca38-103">Informationen zum Zuschneiden und Skalieren von GDI+-Bilds</span><span class="sxs-lookup"><span data-stu-id="eca38-103">About cropping and scaling GDI+ images</span></span>

<span data-ttu-id="eca38-104">Sie können die [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) -Methode der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse verwenden, um Bilder zu zeichnen und zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="eca38-104">You can use the [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to draw and position images.</span></span> <span data-ttu-id="eca38-105">DrawImage ist eine überladene Methode, daher gibt es mehrere Möglichkeiten, Sie mit Argumenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="eca38-105">DrawImage is an overloaded method, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="eca38-106">Eine Variation der [**Grafik::D rawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) -Methode empfängt die Adresse eines [**Bild**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) Objekts und einen Verweis auf ein [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="eca38-106">One variation of the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) method receives the address of an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object and a reference to a [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) object.</span></span> <span data-ttu-id="eca38-107">Das Rechteck gibt das Ziel für den Zeichnungs Vorgang an. Das heißt, es gibt das Rechteck an, in dem das Bild gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="eca38-107">The rectangle specifies the destination for the drawing operation; that is, it specifies the rectangle in which the image will be drawn.</span></span> <span data-ttu-id="eca38-108">Wenn sich die Größe des Ziel Rechtecks von der Größe des ursprünglichen Bilds unterscheidet, wird das Bild so skaliert, dass es an das Ziel Rechteck angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="eca38-108">If the size of the destination rectangle is different from the size of the original image, the image is scaled to fit the destination rectangle.</span></span> <span data-ttu-id="eca38-109">Im folgenden Beispiel wird das gleiche Bild dreimal gezeichnet: einmal ohne Skalierung, einmal mit einer Erweiterung und einmal mit einer Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="eca38-109">The following example draws the same image three times: once with no scaling, once with an expansion, and once with a compression.</span></span>


```
Bitmap myBitmap(L"Spiral.png");
Rect expansionRect(80, 10, 2 * myBitmap.GetWidth(), myBitmap.GetHeight());
Rect compressionRect(210, 10, myBitmap.GetWidth() / 2, 
   myBitmap.GetHeight() / 2);

myGraphics.DrawImage(&myBitmap, 10, 10);
myGraphics.DrawImage(&myBitmap, expansionRect);
myGraphics.DrawImage(&myBitmap, compressionRect);
```



<span data-ttu-id="eca38-110">Der vorangehende Code hat zusammen mit einer bestimmten Datei (Spiral.png) die folgende Ausgabe erzeugt.</span><span class="sxs-lookup"><span data-stu-id="eca38-110">The preceding code, along with a particular file, Spiral.png, produced the following output.</span></span>

![die Abbildung zeigt drei Versionen eines Bilds: normal, gestreckt und auf die Hälfte der ursprünglichen Größe verkleinert.](images/aboutgdip03-art06.png)

<span data-ttu-id="eca38-112">Einige Variationen der [**Grafik::D rawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) -Methode verfügt über einen Parameter des Quell Rechtecks und einen Parameter für das Ziel Rechteck.</span><span class="sxs-lookup"><span data-stu-id="eca38-112">Some variations of the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) method have a source-rectangle parameter as well as a destination-rectangle parameter.</span></span> <span data-ttu-id="eca38-113">Das Quell Rechteck gibt den Teil des ursprünglichen Bilds an, der gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="eca38-113">The source rectangle specifies the portion of the original image that will be drawn.</span></span> <span data-ttu-id="eca38-114">Das Ziel Rechteck gibt an, wo der Teil des Bilds gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="eca38-114">The destination rectangle specifies where that portion of the image will be drawn.</span></span> <span data-ttu-id="eca38-115">Wenn sich die Größe des Ziel Rechtecks von der Größe des Quell Rechtecks unterscheidet, wird das Bild so skaliert, dass es an das Ziel Rechteck angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="eca38-115">If the size of the destination rectangle is different from the size of the source rectangle, the image is scaled to fit the destination rectangle.</span></span>

<span data-ttu-id="eca38-116">Im folgenden Beispiel wird ein [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Objekt aus dem Datei Runner.jpg erstellt.</span><span class="sxs-lookup"><span data-stu-id="eca38-116">The following example constructs a [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object from the file Runner.jpg.</span></span> <span data-ttu-id="eca38-117">Das gesamte Bild wird ohne Skalierung bei (0,0) gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="eca38-117">The entire image is drawn with no scaling at (0, 0).</span></span> <span data-ttu-id="eca38-118">Anschließend wird ein kleiner Teil des Bilds zweimal gezeichnet: einmal mit einer Komprimierung und einmal mit einer Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="eca38-118">Then a small portion of the image is drawn twice: once with a compression and once with an expansion.</span></span>


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



<span data-ttu-id="eca38-119">Die folgende Abbildung zeigt das nicht skalierte Bild und die komprimierten und erweiterten Bild Teile.</span><span class="sxs-lookup"><span data-stu-id="eca38-119">The following illustration shows the unscaled image, and the compressed and expanded image portions.</span></span>

![Screenshot, der ein Bild anzeigt, ein Teil des Bilds und dann der gleiche Teil erweitert](images/aboutgdip03-art07.png)

 

 



