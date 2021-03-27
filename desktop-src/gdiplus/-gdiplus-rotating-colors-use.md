---
description: Die Drehung in einem vierdimensionalen Farbraum ist schwierig zu visualisieren.
ms.assetid: 099f76a3-2da3-4f2b-8f8d-557d144451dc
title: Drehen von Farben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea322179bd4a46021d181abedd1797d6bdda7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862528"
---
# <a name="rotating-colors"></a><span data-ttu-id="70a68-103">Drehen von Farben</span><span class="sxs-lookup"><span data-stu-id="70a68-103">Rotating Colors</span></span>

<span data-ttu-id="70a68-104">Die Drehung in einem vierdimensionalen Farbraum ist schwierig zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="70a68-104">Rotation in a four-dimensional color space is difficult to visualize.</span></span> <span data-ttu-id="70a68-105">Wir können das Visualisieren der Rotation vereinfachen, indem wir akzeptieren, dass eine der Farbkomponenten korrigiert wird.</span><span class="sxs-lookup"><span data-stu-id="70a68-105">We can make it easier to visualize rotation by agreeing to keep one of the color components fixed.</span></span> <span data-ttu-id="70a68-106">Angenommen, die Alpha Komponente muss bei 1 (vollständig nicht transparent) korrigiert bleiben.</span><span class="sxs-lookup"><span data-stu-id="70a68-106">Suppose we agree to keep the alpha component fixed at 1 (fully opaque).</span></span> <span data-ttu-id="70a68-107">Anschließend können wir einen dreidimensionalen Farbraum mit roten, grünen und blauen Achsen visualisieren, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="70a68-107">Then we can visualize a three-dimensional color space with red, green, and blue axes as shown in the following illustration.</span></span>

![Abbildung einer Perspektiven Ansicht eines dreidimensionalen Farbraum mit Achsen mit der Bezeichnung rot, grün und blau](images/recoloring03.png)

<span data-ttu-id="70a68-109">Eine Farbe kann sich als Punkt im 3D-Raum vorstellen.</span><span class="sxs-lookup"><span data-stu-id="70a68-109">A color can be thought of as a point in 3-D space.</span></span> <span data-ttu-id="70a68-110">Der Punkt (1, 0, 0) im Raum stellt z. b. die Farbe rot dar, und der Punkt (0, 1, 0) im Raum stellt die Farbe grün dar.</span><span class="sxs-lookup"><span data-stu-id="70a68-110">For example, the point (1, 0, 0) in space represents the color red, and the point (0, 1, 0) in space represents the color green.</span></span>

<span data-ttu-id="70a68-111">In der folgenden Abbildung wird gezeigt, was es bedeutet, die Farbe (1, 0, 0) durch einen Winkel von 60 Grad in der Red-Green Ebene zu drehen.</span><span class="sxs-lookup"><span data-stu-id="70a68-111">The following illustration shows what it means to rotate the color (1, 0, 0) through an angle of 60 degrees in the Red-Green plane.</span></span> <span data-ttu-id="70a68-112">Die Drehung in einer Ebene parallel zur Red-Green Ebene kann als Drehung der blauen Achse betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="70a68-112">Rotation in a plane parallel to the Red-Green plane can be thought of as rotation about the blue axis.</span></span>

![Abbildung, die anzeigt, dass der Punkt (1, 0, 0) um 60 Grad gedreht wird (0,5, 0,866, 0)](images/recoloring04.png)

<span data-ttu-id="70a68-114">In der folgenden Abbildung wird gezeigt, wie eine Farbmatrix initialisiert wird, um Drehungen zu jeder der drei Koordinatenachsen (rot, grün, blau) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="70a68-114">The following illustration shows how to initialize a color matrix to perform rotations about each of the three coordinate axes (red, green, blue).</span></span>

![Abbildung der Farb Matrizen, die Drehungen zu jeder der drei Koordinatenachsen ausführen](images/recoloring05.png)

<span data-ttu-id="70a68-116">Im folgenden Beispiel wird ein Bild, das alle eine Farbe (1, 0, 0,6) ist, und eine 60-Grad-Drehung der blauen Achse angewendet.</span><span class="sxs-lookup"><span data-stu-id="70a68-116">The following example takes an image that is all one color (1, 0, 0.6) and applies a 60-degree rotation about the blue axis.</span></span> <span data-ttu-id="70a68-117">Der Winkel der Drehung wird in einer Ebene durchlaufen, die parallel zum Red-Green Ebene ist.</span><span class="sxs-lookup"><span data-stu-id="70a68-117">The angle of the rotation is swept out in a plane that is parallel to the Red-Green plane.</span></span>


```
Image            image(L"RotationInput.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();
REAL             degrees = 60;
REAL             pi = acos(-1);  // the angle whose cosine is -1.
REAL             r = degrees * pi / 180;  // degrees to radians

ColorMatrix colorMatrix = {
   cos(r),  sin(r), 0.0f, 0.0f, 0.0f,
   -sin(r), cos(r), 0.0f, 0.0f, 0.0f,
   0.0f,    0.0f,   1.0f, 0.0f, 0.0f,
   0.0f,    0.0f,   0.0f, 1.0f, 0.0f,
   0.0f,    0.0f,   0.0f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(130, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



<span data-ttu-id="70a68-118">Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das Farb gedrehte Bild auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="70a68-118">The following illustration shows the original image on the left and the color-rotated image on the right.</span></span>

![Abbildung mit Rechtecke, die mit dem ursprünglichen Bild (violett rot) und einem Farb rotierten Bild (Meer grün) gefüllt sind](images/colortrans5.png)

<span data-ttu-id="70a68-120">Die im vorangehenden Codebeispiel ausgeführte Farb Drehung kann wie folgt visualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="70a68-120">The color rotation performed in the preceding code example can be visualized as follows.</span></span>

![die Abbildung zeigt einen 3D-Farbraum, und der Punkt (1, 0, 0,6) gedreht 60 Grad nach (0,5, 0,866, 0,6).](images/recoloring06.png)

 

 



