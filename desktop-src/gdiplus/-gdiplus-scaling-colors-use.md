---
description: Eine Skalierungs Transformation multipliziert eine oder mehrere der vier Farbkomponenten mit einer Zahl. Die Farbmatrix Einträge, die die Skalierung darstellen, werden in der folgenden Tabelle angegeben.
ms.assetid: 08347831-7100-4220-a83b-693bb7b98ccb
title: Skalieren von Farben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 370155306f7b1a177358d7cf28d329ebb0d75f8c
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104218912"
---
# <a name="scaling-colors"></a><span data-ttu-id="05083-104">Skalieren von Farben</span><span class="sxs-lookup"><span data-stu-id="05083-104">Scaling Colors</span></span>

<span data-ttu-id="05083-105">Eine Skalierungs Transformation multipliziert eine oder mehrere der vier Farbkomponenten mit einer Zahl.</span><span class="sxs-lookup"><span data-stu-id="05083-105">A scaling transformation multiplies one or more of the four color components by a number.</span></span> <span data-ttu-id="05083-106">Die Farbmatrix Einträge, die die Skalierung darstellen, werden in der folgenden Tabelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="05083-106">The color matrix entries that represent scaling are given in the following table.</span></span>



| <span data-ttu-id="05083-107">Zu skalierbare Komponente</span><span class="sxs-lookup"><span data-stu-id="05083-107">Component to be scaled</span></span> | <span data-ttu-id="05083-108">Matrix Eintrag</span><span class="sxs-lookup"><span data-stu-id="05083-108">Matrix entry</span></span> |
|------------------------|--------------|
| <span data-ttu-id="05083-109">Red</span><span class="sxs-lookup"><span data-stu-id="05083-109">Red</span></span>                    | <span data-ttu-id="05083-110">\[0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="05083-110">\[0\]\[0\]</span></span>   |
| <span data-ttu-id="05083-111">Grün</span><span class="sxs-lookup"><span data-stu-id="05083-111">Green</span></span>                  | <span data-ttu-id="05083-112">\[1 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="05083-112">\[1\]\[1\]</span></span>   |
| <span data-ttu-id="05083-113">Blau</span><span class="sxs-lookup"><span data-stu-id="05083-113">Blue</span></span>                   | <span data-ttu-id="05083-114">\[2 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="05083-114">\[2\]\[2\]</span></span>   |
| <span data-ttu-id="05083-115">Alpha</span><span class="sxs-lookup"><span data-stu-id="05083-115">Alpha</span></span>                  | <span data-ttu-id="05083-116">\[3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="05083-116">\[3\]\[3\]</span></span>   |



 

<span data-ttu-id="05083-117">Im folgenden Beispiel wird ein [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus dem Datei ColorBars2.bmp erstellt.</span><span class="sxs-lookup"><span data-stu-id="05083-117">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars2.bmp.</span></span> <span data-ttu-id="05083-118">Anschließend skaliert der Code die blaue Komponente jedes Pixels im Bild um den Faktor 2.</span><span class="sxs-lookup"><span data-stu-id="05083-118">Then the code scales the blue component of each pixel in the image by a factor of 2.</span></span> <span data-ttu-id="05083-119">Das ursprüngliche Bild wird neben dem transformierten Bild gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="05083-119">The original image is drawn alongside the transformed image.</span></span>


```
Image            image(L"ColorBars2.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 2.0f, 0.0f, 0.0f,
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



<span data-ttu-id="05083-120">Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das skalierte Bild auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="05083-120">The following illustration shows the original image on the left and the scaled image on the right.</span></span>

![Zeigt vierfarbige Balken und dann die gleichen Balken mit unterschiedlichen Farben an.](images/colortrans3.png)

<span data-ttu-id="05083-122">In der folgenden Tabelle werden die Farb Vektoren für die vier Balken vor und nach der blauen Skalierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="05083-122">The following table shows the color vectors for the four bars before and after the blue scaling.</span></span> <span data-ttu-id="05083-123">Beachten Sie, dass die blaue Komponente in der vierten Farbleiste von 0,8 zu 0,6 gewechselt ist.</span><span class="sxs-lookup"><span data-stu-id="05083-123">Note that the blue component in the fourth color bar went from 0.8 to 0.6.</span></span> <span data-ttu-id="05083-124">Dies liegt daran, dass GDI+ nur den Bruch Teil des Ergebnisses beibehält.</span><span class="sxs-lookup"><span data-stu-id="05083-124">That is because GDI+ retains only the fractional part of the result.</span></span> <span data-ttu-id="05083-125">Beispiel: (2) (0,8) = 1,6 und der Bruchteil von 1,6 ist 0,6.</span><span class="sxs-lookup"><span data-stu-id="05083-125">For example, (2)(0.8) = 1.6, and the fractional part of 1.6 is 0.6.</span></span> <span data-ttu-id="05083-126">Wenn nur der Bruchteil beibehalten wird, wird sichergestellt, dass das Ergebnis immer im Intervall \[ 0, 1 liegt \] .</span><span class="sxs-lookup"><span data-stu-id="05083-126">Retaining only the fractional part ensures that the result is always in the interval \[0, 1\].</span></span>



| <span data-ttu-id="05083-127">Ursprünglich</span><span class="sxs-lookup"><span data-stu-id="05083-127">Original</span></span>           | <span data-ttu-id="05083-128">Läufig</span><span class="sxs-lookup"><span data-stu-id="05083-128">Scaled</span></span>             |
|--------------------|--------------------|
| <span data-ttu-id="05083-129">(0.4, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="05083-129">(0.4, 0.4, 0.4, 1)</span></span> | <span data-ttu-id="05083-130">(0.4, 0.4, 0.8, 1)</span><span class="sxs-lookup"><span data-stu-id="05083-130">(0.4, 0.4, 0.8, 1)</span></span> |
| <span data-ttu-id="05083-131">(0.4, 0.2, 0.2, 1)</span><span class="sxs-lookup"><span data-stu-id="05083-131">(0.4, 0.2, 0.2, 1)</span></span> | <span data-ttu-id="05083-132">(0.4, 0.2, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="05083-132">(0.4, 0.2, 0.4, 1)</span></span> |
| <span data-ttu-id="05083-133">(0.2, 0.4, 0.2, 1)</span><span class="sxs-lookup"><span data-stu-id="05083-133">(0.2, 0.4, 0.2, 1)</span></span> | <span data-ttu-id="05083-134">(0.2, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="05083-134">(0.2, 0.4, 0.4, 1)</span></span> |
| <span data-ttu-id="05083-135">(0.4, 0.4, 0.8, 1)</span><span class="sxs-lookup"><span data-stu-id="05083-135">(0.4, 0.4, 0.8, 1)</span></span> | <span data-ttu-id="05083-136">(0.4, 0.4, 0.6, 1)</span><span class="sxs-lookup"><span data-stu-id="05083-136">(0.4, 0.4, 0.6, 1)</span></span> |



 

<span data-ttu-id="05083-137">Im folgenden Beispiel wird ein [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus dem Datei ColorBars2.bmp erstellt.</span><span class="sxs-lookup"><span data-stu-id="05083-137">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars2.bmp.</span></span> <span data-ttu-id="05083-138">Anschließend werden im Code die roten, grünen und blauen Komponenten der einzelnen Pixel im Bild skaliert.</span><span class="sxs-lookup"><span data-stu-id="05083-138">Then the code scales the red, green, and blue components of each pixel in the image.</span></span> <span data-ttu-id="05083-139">Die roten Komponenten werden auf 25% herunterskaliert, die grünen Komponenten werden um 35% herunterskaliert, und die blauen Komponenten werden um 50% herunterskaliert.</span><span class="sxs-lookup"><span data-stu-id="05083-139">The red components are scaled down 25 percent, the green components are scaled down 35 percent, and the blue components are scaled down 50 percent.</span></span>


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   0.75f, 0.0f,  0.0f, 0.0f, 0.0f,
   0.0f,  0.65f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.5f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 1.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 0.0f, 1.0f};
   
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



<span data-ttu-id="05083-140">Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das skalierte Bild auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="05083-140">The following illustration shows the original image on the left and the scaled image on the right.</span></span>

![Abbildung, die vierfarbige Balken anzeigt, dann diese Balken mit unterschiedlichen Farben](images/colortrans4.png)

<span data-ttu-id="05083-142">In der folgenden Tabelle werden die Farb Vektoren für die vier Balken vor und nach der roten, grünen und blauen Skalierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="05083-142">The following table shows the color vectors for the four bars before and after the red, green and blue scaling.</span></span>



| <span data-ttu-id="05083-143">Ursprünglich</span><span class="sxs-lookup"><span data-stu-id="05083-143">Original</span></span>           | <span data-ttu-id="05083-144">Läufig</span><span class="sxs-lookup"><span data-stu-id="05083-144">Scaled</span></span>               |
|--------------------|----------------------|
| <span data-ttu-id="05083-145">(0.6, 0.6, 0.6, 1)</span><span class="sxs-lookup"><span data-stu-id="05083-145">(0.6, 0.6, 0.6, 1)</span></span> | <span data-ttu-id="05083-146">(0.45, 0.39, 0.3, 1)</span><span class="sxs-lookup"><span data-stu-id="05083-146">(0.45, 0.39, 0.3, 1)</span></span> |
| <span data-ttu-id="05083-147">(0, 1, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="05083-147">(0, 1, 1, 1)</span></span>       | <span data-ttu-id="05083-148">(0, 0.65, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="05083-148">(0, 0.65, 0.5, 1)</span></span>    |
| <span data-ttu-id="05083-149">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="05083-149">(1, 1, 0, 1)</span></span>       | <span data-ttu-id="05083-150">(0.75, 0.65, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="05083-150">(0.75, 0.65, 0, 1)</span></span>   |
| <span data-ttu-id="05083-151">(1, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="05083-151">(1, 0, 1, 1)</span></span>       | <span data-ttu-id="05083-152">(0.75, 0, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="05083-152">(0.75, 0, 0.5, 1)</span></span>    |



 

 

 



