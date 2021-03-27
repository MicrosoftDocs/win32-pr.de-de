---
description: Viele CAD-Anwendungen stellen Funktionen bereit, die Objekte drehen, die im Client Bereich gezeichnet werden.
ms.assetid: 85d8fe2c-5ad9-4e98-b6ff-ca0a78abeee5
title: Drehung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17be42f2826cbad09333b2c37b607dc50c7c9d0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980680"
---
# <a name="rotation"></a><span data-ttu-id="ce9e7-103">Drehung</span><span class="sxs-lookup"><span data-stu-id="ce9e7-103">Rotation</span></span>

<span data-ttu-id="ce9e7-104">Viele CAD-Anwendungen stellen Funktionen bereit, die Objekte drehen, die im Client Bereich gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="ce9e7-104">Many CAD applications provide features that rotate objects drawn in the client area.</span></span> <span data-ttu-id="ce9e7-105">Anwendungen, die rotationsfunktionen enthalten, verwenden die [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) -Funktion, um die entsprechende Welt Raum-und Seiten Raum Transformation festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ce9e7-105">Applications that include rotation capabilities use the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate world-space to page-space transformation.</span></span> <span data-ttu-id="ce9e7-106">Diese Funktion empfängt einen Zeiger auf eine [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) -Struktur, die die entsprechenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="ce9e7-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="ce9e7-107">Die eM11-, eM12-, eM21-und eM22-Member von XForm geben jeweils, den Kosinus, den Sinus, den negativen Sinus und Kosinus des Drehwinkels an.</span><span class="sxs-lookup"><span data-stu-id="ce9e7-107">The eM11, eM12, eM21, and eM22 members of XFORM specify respectively, the cosine, sine, negative sine, and cosine of the angle of rotation.</span></span>

<span data-ttu-id="ce9e7-108">Wenn die *Drehung* erfolgt, werden die Punkte, die ein Objekt bilden, in Bezug auf den Ursprung des Koordinaten Raums gedreht.</span><span class="sxs-lookup"><span data-stu-id="ce9e7-108">When *rotation* occurs, the points that constitute an object are rotated with respect to the coordinate-space origin.</span></span> <span data-ttu-id="ce9e7-109">Die folgende Abbildung zeigt ein Rechteck von 20 bis 20 Einheiten, das 30 Grad gedreht wurde, wenn es aus dem weltweiten Koordinatenraum in den Bereich der Seiten Koordinate kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ce9e7-109">The following illustration shows a 20-by-20-unit rectangle rotated 30 degrees when copied from world-coordinate space to page-coordinate space.</span></span>

![Abbildung, die zwei Koordinaten Bereiche anzeigt. Jeder hat eine rechge an einem anderen Speicherort und mit einer anderen Drehung.](images/cstrn-11.png)

<span data-ttu-id="ce9e7-111">In der obigen Abbildung wurde jeder Punkt im Rechteck in Bezug auf den Koordinatenraum Ursprung um 30 Grad gedreht.</span><span class="sxs-lookup"><span data-stu-id="ce9e7-111">In the preceding illustration, each point in the rectangle was rotated 30 degrees with respect to the coordinate-space origin.</span></span>

<span data-ttu-id="ce9e7-112">Der folgende Algorithmus berechnet die neue x-Koordinate (x ") für einen Punkt (x, y), der in Bezug auf den Koordinatenraum Ursprung von Winkel a gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="ce9e7-112">The following algorithm computes the new x-coordinate (x ') for a point (x,y ) that is rotated by angle A with respect to the coordinate-space origin.</span></span>

``` syntax
x' = (x * cos A) - (y * sin A) 
```

<span data-ttu-id="ce9e7-113">Der folgende Algorithmus berechnet die y-Koordinate (y ") für einen Punkt (x, y), der durch den Winkel a in Bezug auf den Ursprung gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="ce9e7-113">The following algorithm computes the y-coordinate (y ') for a point (x,y ) that is rotated by the angle A with respect to the origin.</span></span>

``` syntax
y' = (x * sin A) + (y * cos A) 
```

<span data-ttu-id="ce9e7-114">Die beiden Drehungs Transformationen können wie folgt in einer 2 x 2-Matrix kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="ce9e7-114">The two rotation transformations can be combined in a 2-by-2 matrix as follows.</span></span>

``` syntax
|x' y'| == |x y| * | cos A   sin A| 
                   |-sin A   cos A| 
```

<span data-ttu-id="ce9e7-115">Die 2 x 2-Matrix, die die Drehung erzeugt hat, enthält die folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="ce9e7-115">The 2-by-2 matrix that produced the rotation contains the following values.</span></span>

``` syntax
| .8660    .5000| 
|-.5000    .8660| 
```

## <a name="rotation-algorithm-derivation"></a><span data-ttu-id="ce9e7-116">Ableitung von Rotations Algorithmen</span><span class="sxs-lookup"><span data-stu-id="ce9e7-116">Rotation Algorithm Derivation</span></span>

<span data-ttu-id="ce9e7-117">Rotations Algorithmen basieren auf dem Additions Theorem von Trigonometry, das besagt, dass die trigonometrische Funktion einer Summe von zwei Winkeln (a1 und a2) in Form der trigonometrischen Funktionen der beiden Winkel ausgedrückt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ce9e7-117">Rotation algorithms are based on trigonometry's addition theorem stating that the trigonometric function of a sum of two angles (A1 and A2 ) can be expressed in terms of the trigonometric functions of the two angles.</span></span>

``` syntax
sin(A1 + A2) = (sin A1 * cos A2) + (cos A1 * sin A2) 
cos(A1 + A2) = (cos A1 * cos A2) - (sin A1 * sin A2) 
```

<span data-ttu-id="ce9e7-118">In der folgenden Abbildung wird eine Punkt-p-Drehung gegen den Uhrzeigersinn zu einer neuen Position p "gezeigt.</span><span class="sxs-lookup"><span data-stu-id="ce9e7-118">The following illustration shows a point p rotated counterclockwise to a new position p'.</span></span> <span data-ttu-id="ce9e7-119">Darüber hinaus werden zwei Dreiecke angezeigt, die durch eine Linie gebildet werden, die vom Koordinatenraum Ursprung bis zu jedem Punkt gezeichnet wird, und eine Linie, die von jedem Punkt durch die x-Achse gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="ce9e7-119">In addition, it shows two triangles formed by a line drawn from the coordinate-space origin to each point and a line drawn from each point through the x-axis.</span></span>

![das Diagramm zeigt den Ursprung, p und p "und zwei Dreiecke](images/cstrn-12.png)

<span data-ttu-id="ce9e7-121">Bei Verwendung von Trigonometry kann die x-Koordinate von Punkt p durch Multiplizieren der Länge der Hypotenuse h durch den Kosinus von a1 abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ce9e7-121">Using trigonometry, the x-coordinate of point p can be obtained by multiplying the length of the hypotenuse h by the cosine of A1.</span></span>

``` syntax
x = h * cos A1 
```

<span data-ttu-id="ce9e7-122">Die y-Koordinate von Punkt p kann abgerufen werden, indem die Länge der Hypotenuse h mit dem Sinus von a1 multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="ce9e7-122">The y-coordinate of point p can be obtained by multiplying the length of the hypotenuse h by the sine of A1.</span></span>

``` syntax
y = h * sin A1 
```

<span data-ttu-id="ce9e7-123">Ebenso kann die x-Koordinate des Punkts p ' abgerufen werden, indem die Länge der Hypotenuse h durch den Kosinus von (a1 + a2) multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="ce9e7-123">Likewise, the x-coordinate of point p' can be obtained by multiplying the length of the hypotenuse h by the cosine of (A1 +A2 ).</span></span>

``` syntax
x' = h * cos (A1 + A2) 
```

<span data-ttu-id="ce9e7-124">Schließlich kann die y-Koordinate von Punkt p ' abgerufen werden, indem die Länge der Hypotenuse h mit dem Sinus von (a1 + a2) multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="ce9e7-124">Finally, the y-coordinate of point p' can be obtained by multiplying the length of the hypotenuse h by the sine of (A1 +A2 ).</span></span>

``` syntax
y' = h * sin (A1 + A2) 
```

<span data-ttu-id="ce9e7-125">Mit dem Additions-Theorem werden die vorangehenden Algorithmen wie folgt verwendet:</span><span class="sxs-lookup"><span data-stu-id="ce9e7-125">Using the addition theorem, the preceding algorithms become the following:</span></span>

``` syntax
x' = (h * cos A1 * cos A2) - (h * sin A1 * sin A2) 
y' = (h * cos A1 * sin A2) + (h * sin A1 * cos A2) 
```

<span data-ttu-id="ce9e7-126">Die Rotations Algorithmen für einen bestimmten Punkt, der durch den Winkel a2 gedreht wird, können durch die Ersetzung von x für jedes Vorkommen von (h \* cos a1) und durch Ersetzen von y für jedes Vorkommen von (h \* Sin a1) abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ce9e7-126">The rotation algorithms for a given point rotated by angle A2 can be obtained by substituting x for each occurrence of (h \* cos A1 ) and by substituting y for each occurrence of (h \* sin A1 ).</span></span>

``` syntax
x' = (x * cos A2) - (y * sin A2) 
y' = (x * sin A2) + (y * cos A2) 
```

 

 



