---
description: Sie können ein Bild drehen, reflektieren und verzerren, indem Sie Zielpunkte für die obere linke, obere Rechte und untere linke Ecke des ursprünglichen Bilds angeben.
ms.assetid: 1e982d84-8749-451b-89a8-81440fcee439
title: Rotation, Spiegelung und Neigung von Bildern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5637cb8be0290d96a164042086e997bc878c0227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959446"
---
# <a name="rotating-reflecting-and-skewing-images"></a><span data-ttu-id="c9d44-103">Rotation, Spiegelung und Neigung von Bildern</span><span class="sxs-lookup"><span data-stu-id="c9d44-103">Rotating, Reflecting, and Skewing Images</span></span>

<span data-ttu-id="c9d44-104">Sie können ein Bild drehen, reflektieren und verzerren, indem Sie Zielpunkte für die obere linke, obere Rechte und untere linke Ecke des ursprünglichen Bilds angeben.</span><span class="sxs-lookup"><span data-stu-id="c9d44-104">You can rotate, reflect, and skew an image by specifying destination points for the upper-left, upper-right, and lower-left corners of the original image.</span></span> <span data-ttu-id="c9d44-105">Die drei Zielpunkte bestimmen eine affine Transformation, die das ursprüngliche rechteckige Bild einem Parallelogram zuordnet.</span><span class="sxs-lookup"><span data-stu-id="c9d44-105">The three destination points determine an affine transformation that maps the original rectangular image to a parallelogram.</span></span> <span data-ttu-id="c9d44-106">(Die untere rechte Ecke des ursprünglichen Bilds wird der vierten Ecke des parallelograms zugeordnet, das aus den drei angegebenen Zielpunkten berechnet wird.)</span><span class="sxs-lookup"><span data-stu-id="c9d44-106">(The lower-right corner of the original image is mapped to the fourth corner of the parallelogram, which is calculated from the three specified destination points.)</span></span>

<span data-ttu-id="c9d44-107">Angenommen, das ursprüngliche Bild ist ein Rechteck mit der oberen linken Ecke bei (0,0), der oberen rechten Ecke bei (100, 0) und der unteren linken Ecke bei (0, 50).</span><span class="sxs-lookup"><span data-stu-id="c9d44-107">For example, suppose the original image is a rectangle with upper-left corner at (0, 0), upper-right corner at (100, 0), and lower-left corner at (0, 50).</span></span> <span data-ttu-id="c9d44-108">Nehmen wir nun an, dass die drei Punkte den Zielpunkten folgendermaßen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="c9d44-108">Now suppose we map those three points to destination points as follows.</span></span>



| <span data-ttu-id="c9d44-109">Ursprünglicher Punkt</span><span class="sxs-lookup"><span data-stu-id="c9d44-109">Original point</span></span>       | <span data-ttu-id="c9d44-110">Zielpunkt</span><span class="sxs-lookup"><span data-stu-id="c9d44-110">Destination point</span></span> |
|----------------------|-------------------|
| <span data-ttu-id="c9d44-111">Oben links (0,0)</span><span class="sxs-lookup"><span data-stu-id="c9d44-111">Upper-left (0, 0)</span></span>    | <span data-ttu-id="c9d44-112">(200, 20)</span><span class="sxs-lookup"><span data-stu-id="c9d44-112">(200, 20)</span></span>         |
| <span data-ttu-id="c9d44-113">Upper-Right (100, 0)</span><span class="sxs-lookup"><span data-stu-id="c9d44-113">Upper-right (100, 0)</span></span> | <span data-ttu-id="c9d44-114">(110, 100)</span><span class="sxs-lookup"><span data-stu-id="c9d44-114">(110, 100)</span></span>        |
| <span data-ttu-id="c9d44-115">Unten links (0, 50)</span><span class="sxs-lookup"><span data-stu-id="c9d44-115">Lower-left (0, 50)</span></span>   | <span data-ttu-id="c9d44-116">(250, 30)</span><span class="sxs-lookup"><span data-stu-id="c9d44-116">(250, 30)</span></span>         |



 

<span data-ttu-id="c9d44-117">Die folgende Abbildung zeigt das ursprüngliche Bild und das dem Parallelogram zugeordnete Bild.</span><span class="sxs-lookup"><span data-stu-id="c9d44-117">The following illustration shows the original image and the image mapped to the parallelogram.</span></span> <span data-ttu-id="c9d44-118">Das ursprüngliche Bild wurde verzerrt, reflektiert, gedreht und übersetzt.</span><span class="sxs-lookup"><span data-stu-id="c9d44-118">The original image has been skewed, reflected, rotated, and translated.</span></span> <span data-ttu-id="c9d44-119">Die x-Achse entlang des oberen Rands des ursprünglichen Bilds wird der Zeile zugeordnet, die durchlaufen wird (200, 20) und (110, 100).</span><span class="sxs-lookup"><span data-stu-id="c9d44-119">The x-axis along the top edge of the original image is mapped to the line that runs through (200, 20) and (110, 100).</span></span> <span data-ttu-id="c9d44-120">Die y-Achse entlang des linken Rands des ursprünglichen Bilds wird der Zeile zugeordnet, die durchlaufen wird (200, 20) und (250, 30).</span><span class="sxs-lookup"><span data-stu-id="c9d44-120">The y-axis along the left edge of the original image is mapped to the line that runs through (200, 20) and (250, 30).</span></span>

![die Abbildung zeigt farbige Streifen am Ursprung der Koordinatenachsen und die gleichen Streifen an einer anderen Position, Drehung und Größe.](images/stripes1.png)

<span data-ttu-id="c9d44-122">Im folgenden Beispiel werden die in der obigen Abbildung gezeigten Bilder erzeugt.</span><span class="sxs-lookup"><span data-stu-id="c9d44-122">The following example produces the images shown in the preceding illustration.</span></span>


```
Point destinationPoints[] = {
   Point(200, 20),   // destination for upper-left point of original
   Point(110, 100),  // destination for upper-right point of original
   Point(250, 30)};  // destination for lower-left point of original
Image image(L"Stripes.bmp");
// Draw the image unaltered with its upper-left corner at (0, 0).
graphics.DrawImage(&image, 0, 0);
// Draw the image mapped to the parallelogram.
graphics.DrawImage(&image, destinationPoints, 3); 
```



<span data-ttu-id="c9d44-123">Die folgende Abbildung zeigt eine ähnliche Transformation, die auf ein Foto Bild angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c9d44-123">The following illustration shows a similar transformation applied to a photographic image.</span></span>

![Darstellung des gleichen Fotos zweimal die zweite ist umgekehrt, verzerrt und hat unterschiedliche Größe, Drehung und Position.](images/transformedclimber.png)

<span data-ttu-id="c9d44-125">Die folgende Abbildung zeigt eine ähnliche Transformation, die auf eine Metadatei angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c9d44-125">The following illustration shows a similar transformation applied to a metafile.</span></span>

![Darstellung von Formen und Text, dann erneut, aber umgekehrt, verzerrt und mit unterschiedlichen Standorten, Drehung und Größe](images/transformedmetafile.png)

 

 



