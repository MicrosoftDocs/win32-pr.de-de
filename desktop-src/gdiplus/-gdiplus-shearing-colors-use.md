---
description: Durch das Scheren wird eine Farbkomponente um einen in einer anderen Farbkomponente proportionalen Betrag vergrößert oder verringert.
ms.assetid: 12f83f35-33f1-4ac9-b45d-f8700e54053a
title: Scheren von Farben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d632fded9f2b4d1e4682ae9f8ffbfedee85a46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131332"
---
# <a name="shearing-colors"></a><span data-ttu-id="3933f-103">Scheren von Farben</span><span class="sxs-lookup"><span data-stu-id="3933f-103">Shearing Colors</span></span>

<span data-ttu-id="3933f-104">Durch das Scheren wird eine Farbkomponente um einen in einer anderen Farbkomponente proportionalen Betrag vergrößert oder verringert.</span><span class="sxs-lookup"><span data-stu-id="3933f-104">Shearing increases or decreases a color component by an amount proportional to another color component.</span></span> <span data-ttu-id="3933f-105">Nehmen Sie z. b. die Transformation, bei der die rote Komponente um einen halben Wert der blauen Komponente erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="3933f-105">For example, consider the transformation where the red component is increased by one half the value of the blue component.</span></span> <span data-ttu-id="3933f-106">Bei einer solchen Transformation würde die Farbe (0,2, 0,5, 1) zu (0,7, 0,5, 1) werden.</span><span class="sxs-lookup"><span data-stu-id="3933f-106">Under such a transformation, the color (0.2, 0.5, 1) would become (0.7, 0.5, 1).</span></span> <span data-ttu-id="3933f-107">Die neue rote Komponente ist 0,2 + (1/2) (1) = 0,7.</span><span class="sxs-lookup"><span data-stu-id="3933f-107">The new red component is 0.2 + (1/2)(1) = 0.7.</span></span>

<span data-ttu-id="3933f-108">Im folgenden Beispiel wird ein [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus dem Datei ColorBars4.bmp erstellt.</span><span class="sxs-lookup"><span data-stu-id="3933f-108">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars4.bmp.</span></span> <span data-ttu-id="3933f-109">Anschließend wendet der Code die im vorherigen Absatz beschriebene Scheren Transformation auf jedes Pixel im Bild an.</span><span class="sxs-lookup"><span data-stu-id="3933f-109">Then the code applies the shearing transformation described in the preceding paragraph to each pixel in the image.</span></span>


```
Image            image(L"ColorBars4.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.5f, 0.0f, 1.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(150, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



<span data-ttu-id="3933f-110">Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das auf der rechten Seite gelauftene Bild.</span><span class="sxs-lookup"><span data-stu-id="3933f-110">The following illustration shows the original image on the left and the sheared image on the right.</span></span>

![die Abbildung zeigt vierfarbige Balken, dann die gleichen Balken mit unterschiedlichen Farben.](images/colortrans6.png)

<span data-ttu-id="3933f-112">Die folgende Tabelle zeigt die Farb Vektoren für die vier Balken vor und nach der Transformation für das Scheren-Diagramm.</span><span class="sxs-lookup"><span data-stu-id="3933f-112">The following table shows the color vectors for the four bars before and after the shearing transformation.</span></span>



| <span data-ttu-id="3933f-113">Ursprünglich</span><span class="sxs-lookup"><span data-stu-id="3933f-113">Original</span></span>           | <span data-ttu-id="3933f-114">Zert</span><span class="sxs-lookup"><span data-stu-id="3933f-114">Sheared</span></span>            |
|--------------------|--------------------|
| <span data-ttu-id="3933f-115">(0, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="3933f-115">(0, 0, 1, 1)</span></span>       | <span data-ttu-id="3933f-116">(0.5, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="3933f-116">(0.5, 0, 1, 1)</span></span>     |
| <span data-ttu-id="3933f-117">(0.5, 1, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="3933f-117">(0.5, 1, 0.5, 1)</span></span>   | <span data-ttu-id="3933f-118">(0.75, 1, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="3933f-118">(0.75, 1, 0.5, 1)</span></span>  |
| <span data-ttu-id="3933f-119">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="3933f-119">(1, 1, 0, 1)</span></span>       | <span data-ttu-id="3933f-120">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="3933f-120">(1, 1, 0, 1)</span></span>       |
| <span data-ttu-id="3933f-121">(0.4, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="3933f-121">(0.4, 0.4, 0.4, 1)</span></span> | <span data-ttu-id="3933f-122">(0.6, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="3933f-122">(0.6, 0.4, 0.4, 1)</span></span> |



 

 

 



