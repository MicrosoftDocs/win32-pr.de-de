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
# <a name="cropping-and-scaling-gdi-images"></a><span data-ttu-id="e9d9c-103">Zuschneiden und Skalieren von GDI+-Images</span><span class="sxs-lookup"><span data-stu-id="e9d9c-103">Cropping and scaling GDI+ images</span></span>

<span data-ttu-id="e9d9c-104">Die [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse stellt mehrere **DrawImage** -Methoden bereit, von denen einige über Quell-und Ziel Rechteck Parameter verfügen, die Sie zum Zuschneiden und Skalieren von Bildern verwenden können.</span><span class="sxs-lookup"><span data-stu-id="e9d9c-104">The [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides several **DrawImage** methods, some of which have source and destination rectangle parameters that you can use to crop and scale images.</span></span>

<span data-ttu-id="e9d9c-105">Im folgenden Beispiel wird ein [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus dem Datei Apple.gif erstellt.</span><span class="sxs-lookup"><span data-stu-id="e9d9c-105">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Apple.gif.</span></span> <span data-ttu-id="e9d9c-106">Der Code zeichnet das gesamte Apple-Image in seiner ursprünglichen Größe.</span><span class="sxs-lookup"><span data-stu-id="e9d9c-106">The code draws the entire apple image in its original size.</span></span> <span data-ttu-id="e9d9c-107">Der Code ruft dann die **DrawImage** -Methode eines [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts auf, um einen Teil des Apple-Bilds in einem Ziel Rechteck zu zeichnen, das größer ist als das ursprüngliche Apple-Image.</span><span class="sxs-lookup"><span data-stu-id="e9d9c-107">The code then calls the **DrawImage** method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object to draw a portion of the apple image in a destination rectangle that is larger than the original apple image.</span></span>

<span data-ttu-id="e9d9c-108">Mit der **DrawImage** -Methode wird bestimmt, welcher Teil des Apple gezeichnet werden soll, indem das Quell Rechteck betrachtet wird, das durch das dritte, vierte, fünfte und sechste Argument angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e9d9c-108">The **DrawImage** method determines which portion of the apple to draw by looking at the source rectangle, which is specified by the third, fourth, fifth, and sixth arguments.</span></span> <span data-ttu-id="e9d9c-109">In diesem Fall wird Apple auf 75 Prozent seiner Breite und 75 Prozent seiner Höhe zugeschnitten.</span><span class="sxs-lookup"><span data-stu-id="e9d9c-109">In this case, the apple is cropped to 75 percent of its width and 75 percent of its height.</span></span>

<span data-ttu-id="e9d9c-110">Mit der **DrawImage** -Methode wird festgelegt, wo der gezeichnete Apple gezeichnet werden soll und wie groß das abgeschnittene Apple ist, indem das Ziel Rechteck betrachtet wird, das durch das zweite Argument angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e9d9c-110">The **DrawImage** method determines where to draw the cropped apple and how big to make the cropped apple by looking at the destination rectangle, which is specified by the second argument.</span></span> <span data-ttu-id="e9d9c-111">In diesem Fall ist das Ziel Rechteck um 30 Prozent breiter und 30 Prozent höher als das ursprüngliche Bild.</span><span class="sxs-lookup"><span data-stu-id="e9d9c-111">In this case, the destination rectangle is 30 percent wider and 30 percent taller than the original image.</span></span>


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



<span data-ttu-id="e9d9c-112">Die folgende Abbildung zeigt das ursprüngliche Apple und das skalierte, ausgeschnittene Apple.</span><span class="sxs-lookup"><span data-stu-id="e9d9c-112">The following illustration shows the original apple and the scaled, cropped apple.</span></span>

![Abbildung zeigt ein Apple, dann ein vergrößerter Teil des ursprünglichen Apple](images/cropscale1.png)

 

 



