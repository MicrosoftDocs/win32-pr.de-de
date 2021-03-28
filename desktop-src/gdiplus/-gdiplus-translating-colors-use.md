---
description: Eine Übersetzung Fügt einer oder mehreren der vier Farbkomponenten einen Wert hinzu. Die Farbmatrix Einträge, die Übersetzungen darstellen, werden in der folgenden Tabelle angegeben.
ms.assetid: a0d89989-9b98-42fb-8d87-206581e3c91e
title: Übersetzen von Farben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c769a24c02e977c3e32ff913852d4b6b8d54441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567896"
---
# <a name="translating-colors"></a><span data-ttu-id="6cd13-104">Übersetzen von Farben</span><span class="sxs-lookup"><span data-stu-id="6cd13-104">Translating Colors</span></span>

<span data-ttu-id="6cd13-105">Eine Übersetzung Fügt einer oder mehreren der vier Farbkomponenten einen Wert hinzu.</span><span class="sxs-lookup"><span data-stu-id="6cd13-105">A translation adds a value to one or more of the four color components.</span></span> <span data-ttu-id="6cd13-106">Die Farbmatrix Einträge, die Übersetzungen darstellen, werden in der folgenden Tabelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="6cd13-106">The color matrix entries that represent translations are given in the following table.</span></span>



| <span data-ttu-id="6cd13-107">Zu über setzende Komponente</span><span class="sxs-lookup"><span data-stu-id="6cd13-107">Component to be translated</span></span> | <span data-ttu-id="6cd13-108">Matrix Eintrag</span><span class="sxs-lookup"><span data-stu-id="6cd13-108">Matrix entry</span></span> |
|----------------------------|--------------|
| <span data-ttu-id="6cd13-109">Red</span><span class="sxs-lookup"><span data-stu-id="6cd13-109">Red</span></span>                        | <span data-ttu-id="6cd13-110">\[4 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="6cd13-110">\[4\]\[0\]</span></span>   |
| <span data-ttu-id="6cd13-111">Grün</span><span class="sxs-lookup"><span data-stu-id="6cd13-111">Green</span></span>                      | <span data-ttu-id="6cd13-112">\[4 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="6cd13-112">\[4\]\[1\]</span></span>   |
| <span data-ttu-id="6cd13-113">Blau</span><span class="sxs-lookup"><span data-stu-id="6cd13-113">Blue</span></span>                       | <span data-ttu-id="6cd13-114">\[4 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="6cd13-114">\[4\]\[2\]</span></span>   |
| <span data-ttu-id="6cd13-115">Alpha</span><span class="sxs-lookup"><span data-stu-id="6cd13-115">Alpha</span></span>                      | <span data-ttu-id="6cd13-116">\[4 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="6cd13-116">\[4\]\[3\]</span></span>   |



 

<span data-ttu-id="6cd13-117">Im folgenden Beispiel wird ein [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus dem Datei ColorBars.bmp erstellt.</span><span class="sxs-lookup"><span data-stu-id="6cd13-117">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars.bmp.</span></span> <span data-ttu-id="6cd13-118">Anschließend fügt der Code der roten Komponente jedes Pixels im Bild 0,75 hinzu.</span><span class="sxs-lookup"><span data-stu-id="6cd13-118">Then the code adds 0.75 to the red component of each pixel in the image.</span></span> <span data-ttu-id="6cd13-119">Das ursprüngliche Bild wird neben dem transformierten Bild gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6cd13-119">The original image is drawn alongside the transformed image.</span></span>


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f,  0.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  1.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 1.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 0.0f, 1.0f, 0.0f,
   0.75f, 0.0f, 0.0f, 0.0f, 1.0f};
   
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



<span data-ttu-id="6cd13-120">Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das transformierte Bild auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="6cd13-120">The following illustration shows the original image on the left and the transformed image on the right.</span></span>

![die Abbildung zeigt vierfarbige Balken, dann die gleichen Balken mit unterschiedlichen Farben.](images/colortrans2.png)

<span data-ttu-id="6cd13-122">In der folgenden Tabelle sind die Farb Vektoren für die vier Balken vor und nach der roten Übersetzung aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6cd13-122">The following table lists the color vectors for the four bars before and after the red translation.</span></span> <span data-ttu-id="6cd13-123">Beachten Sie, dass die rote Komponente in der zweiten Zeile nicht geändert wird, da der Höchstwert für eine Farbkomponente 1 ist.</span><span class="sxs-lookup"><span data-stu-id="6cd13-123">Note that because the maximum value for a color component is 1, the red component in the second row does not change.</span></span> <span data-ttu-id="6cd13-124">(Auf ähnliche Weise ist der minimale Wert für eine Farbkomponente 0.)</span><span class="sxs-lookup"><span data-stu-id="6cd13-124">(Similarly, the minimum value for a color component is 0.)</span></span>



| <span data-ttu-id="6cd13-125">Ursprünglich</span><span class="sxs-lookup"><span data-stu-id="6cd13-125">Original</span></span>           | <span data-ttu-id="6cd13-126">Übersetzt</span><span class="sxs-lookup"><span data-stu-id="6cd13-126">Translated</span></span>      |
|--------------------|-----------------|
| <span data-ttu-id="6cd13-127">Schwarz (0,0 (0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="6cd13-127">Black (0, 0, 0, 1)</span></span> | <span data-ttu-id="6cd13-128">(0.75, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="6cd13-128">(0.75, 0, 0, 1)</span></span> |
| <span data-ttu-id="6cd13-129">Rot (1, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="6cd13-129">Red (1, 0, 0, 1)</span></span>   | <span data-ttu-id="6cd13-130">(1, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="6cd13-130">(1, 0, 0, 1)</span></span>    |
| <span data-ttu-id="6cd13-131">Grün (0, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="6cd13-131">Green (0, 1, 0, 1)</span></span> | <span data-ttu-id="6cd13-132">(0.75, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="6cd13-132">(0.75, 1, 0, 1)</span></span> |
| <span data-ttu-id="6cd13-133">Blau (0,0 (0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="6cd13-133">Blue (0, 0, 1, 1)</span></span>  | <span data-ttu-id="6cd13-134">(0.75, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="6cd13-134">(0.75, 0, 1, 1)</span></span> |



 

 

 



