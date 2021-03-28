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
# <a name="drawing-opaque-and-semitransparent-lines"></a><span data-ttu-id="28f69-103">Zeichnen deckender und halb transparenter Linien</span><span class="sxs-lookup"><span data-stu-id="28f69-103">Drawing Opaque and Semitransparent Lines</span></span>

<span data-ttu-id="28f69-104">Wenn Sie eine Linie zeichnen, müssen Sie die Adresse eines [**Stift**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) Objekts an die [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) -Methode der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse übergeben.</span><span class="sxs-lookup"><span data-stu-id="28f69-104">When you draw a line, you must pass the address of a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object to the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="28f69-105">Einer der Parameter des **Stift** -Konstruktors ist ein [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="28f69-105">One of the parameters of the **Pen** constructor is a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="28f69-106">Um eine nicht transparente Linie zu zeichnen, legen Sie den Alphaanteil der Farbe auf 255 fest.</span><span class="sxs-lookup"><span data-stu-id="28f69-106">To draw an opaque line, set the alpha component of the color to 255.</span></span> <span data-ttu-id="28f69-107">Um eine halb transparente Linie zu zeichnen, legen Sie den Alphaanteil auf einen beliebigen Wert von 1 bis 254 fest.</span><span class="sxs-lookup"><span data-stu-id="28f69-107">To draw a semitransparent line, set the alpha component to any value from 1 through 254.</span></span>

<span data-ttu-id="28f69-108">Wenn Sie eine halb transparente Linie vor einem Hintergrund zeichnen, wird Linienfarbe mit den Hintergrundfarben gemischt.</span><span class="sxs-lookup"><span data-stu-id="28f69-108">When you draw a semitransparent line over a background, the color of the line is blended with the colors of the background.</span></span> <span data-ttu-id="28f69-109">Die Alpha Komponente gibt an, wie die Zeilen-und Hintergrundfarben gemischt werden. Alpha-Werte in der Nähe von 0 stellen eine höhere Gewichtung der Hintergrundfarben dar, und Alpha Werte in der Nähe von 255 platzieren die Linien Farbe stärker.</span><span class="sxs-lookup"><span data-stu-id="28f69-109">The alpha component specifies how the line and background colors are mixed; alpha values near 0 place more weight on the background colors, and alpha values near 255 place more weigh on the line color.</span></span>

<span data-ttu-id="28f69-110">Im folgenden Beispiel wird ein Bild gezeichnet und anschließend drei Zeilen gezeichnet, die das Bild als Hintergrund verwenden.</span><span class="sxs-lookup"><span data-stu-id="28f69-110">The following example draws an image and then draws three lines that use the image as a background.</span></span> <span data-ttu-id="28f69-111">Für die erste Linie wird ein Alphaanteil von 255 verwendet. Die Linie ist daher nicht transparent.</span><span class="sxs-lookup"><span data-stu-id="28f69-111">The first line uses an alpha component of 255, so it is opaque.</span></span> <span data-ttu-id="28f69-112">Die zweite und die dritte Linie verwenden einen Alphaanteil von 128. Sie sind daher halb transparent. Das Hintergrundbild scheint also durch die Linien hindurch.</span><span class="sxs-lookup"><span data-stu-id="28f69-112">The second and third lines use an alpha component of 128, so they are semitransparent; you can see the background image through the lines.</span></span> <span data-ttu-id="28f69-113">Der aufzurufende [**Grafik:: setcompositingquality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) bewirkt, dass die Mischung für die dritte Zeile in Verbindung mit der Gammakorrektur erfolgt.</span><span class="sxs-lookup"><span data-stu-id="28f69-113">The call to [**Graphics::SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) causes the blending for the third line to be done in conjunction with gamma correction.</span></span>


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



<span data-ttu-id="28f69-114">Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes.</span><span class="sxs-lookup"><span data-stu-id="28f69-114">The following illustration shows the output of the preceding code.</span></span>

![Darstellung eines Bilds, das durch drei Breite Linien überlagert wird: ein undurchsichtiges, ein leicht transparenter und ein sehr transparentes](images/compqualline.png)

 

 



