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
# <a name="drawing-with-opaque-and-semitransparent-brushes"></a><span data-ttu-id="eeba4-103">Zeichnen mit nicht transparenten und halbtransparenten Pinseln</span><span class="sxs-lookup"><span data-stu-id="eeba4-103">Drawing with Opaque and Semitransparent Brushes</span></span>

<span data-ttu-id="eeba4-104">Wenn Sie eine Form ausfüllen, müssen Sie die Adresse eines [**Pinsel**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) Objekts an eine der Füll Methoden der [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse übergeben.</span><span class="sxs-lookup"><span data-stu-id="eeba4-104">When you fill a shape, you must pass the address of a [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object to one of the fill methods of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="eeba4-105">Der einzige Parameter des [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) -Konstruktors ist ein [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="eeba4-105">The one parameter of the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) constructor is a [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="eeba4-106">Um eine nicht transparente Form auszufüllen, legen Sie den Alphaanteil der Farbe auf 255 fest.</span><span class="sxs-lookup"><span data-stu-id="eeba4-106">To fill an opaque shape, set the alpha component of the color to 255.</span></span> <span data-ttu-id="eeba4-107">Um eine halb transparente Form auszufüllen, legen Sie den Alphaanteil auf einen beliebigen Wert von 1 bis 254 fest.</span><span class="sxs-lookup"><span data-stu-id="eeba4-107">To fill a semitransparent shape, set the alpha component to any value from 1 through 254.</span></span>

<span data-ttu-id="eeba4-108">Wenn Sie eine halb transparente Form ausfüllen, wird die Farbe der Form mit den Hintergrundfarben gemischt.</span><span class="sxs-lookup"><span data-stu-id="eeba4-108">When you fill a semitransparent shape, the color of the shape is blended with the colors of the background.</span></span> <span data-ttu-id="eeba4-109">Die Alpha Komponente gibt an, wie die Form-und Hintergrundfarben gemischt werden. Alpha-Werte in der Nähe von 0 stellen eine höhere Gewichtung der Hintergrundfarben dar, und Alpha Werte in der Nähe von 255 platzieren die Farbe der Form.</span><span class="sxs-lookup"><span data-stu-id="eeba4-109">The alpha component specifies how the shape and background colors are mixed; alpha values near 0 place more weight on the background colors, and alpha values near 255 place more weigh on the shape color.</span></span>

<span data-ttu-id="eeba4-110">Im folgenden Beispiel wird ein Bild gezeichnet und anschließend drei Ellipsen aufgefüllt, die sich überlappen.</span><span class="sxs-lookup"><span data-stu-id="eeba4-110">The following example draws an image and then fills three ellipses that overlap the image.</span></span> <span data-ttu-id="eeba4-111">Für die erste Ellipse wird ein Alphaanteil von 255 verwendet. Die Ellipse ist daher nicht transparent.</span><span class="sxs-lookup"><span data-stu-id="eeba4-111">The first ellipse uses an alpha component of 255, so it is opaque.</span></span> <span data-ttu-id="eeba4-112">Die zweite und die dritte Ellipse verwenden einen Alphaanteil von 128. Sie sind daher halb transparent. Das Hintergrundbild scheint also durch die Ellipsen hindurch.</span><span class="sxs-lookup"><span data-stu-id="eeba4-112">The second and third ellipses use an alpha component of 128, so they are semitransparent; you can see the background image through the ellipses.</span></span> <span data-ttu-id="eeba4-113">Der aufzurufende [**Grafik:: setcompositingquality**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) bewirkt, dass die Mischung für die dritte Ellipse in Verbindung mit der Gammakorrektur erfolgt.</span><span class="sxs-lookup"><span data-stu-id="eeba4-113">The call to [**Graphics::SetCompositingQuality**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) causes the blending for the third ellipse to be done in conjunction with gamma correction.</span></span>


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



<span data-ttu-id="eeba4-114">Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes.</span><span class="sxs-lookup"><span data-stu-id="eeba4-114">The following illustration shows the output of the preceding code.</span></span>

![Abbildung der Darstellung eines Bilds, das durch drei Ellipsen überlagert wird: ein undurchsichtiges, ein wenig transparent, ein sehr transparent](images/compqualellipse.png)

 

 



