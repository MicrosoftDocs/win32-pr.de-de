---
description: Windows GDI+ stellt die Image-und Bitmap-Klassen zum Speichern und Bearbeiten von Bildern bereit.
ms.assetid: fcd7f3d9-8bad-44f8-8c9c-c2f5df4a7241
title: Verwenden einer Farbmatrix zum Transformieren einer einzelnen Farbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db56d0a64c36c08a5415d76e3fb184158d473268
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565513"
---
# <a name="using-a-color-matrix-to-transform-a-single-color"></a><span data-ttu-id="c712a-103">Verwenden einer Farbmatrix zum Transformieren einer einzelnen Farbe</span><span class="sxs-lookup"><span data-stu-id="c712a-103">Using a Color Matrix to Transform a Single Color</span></span>

<span data-ttu-id="c712a-104">Windows GDI+ stellt die [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -und [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Klassen zum Speichern und Bearbeiten von Bildern bereit.</span><span class="sxs-lookup"><span data-stu-id="c712a-104">Windows GDI+ provides the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) and [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) classes for storing and manipulating images.</span></span> <span data-ttu-id="c712a-105">**Image** -und **Bitmap** -Objekte speichern die Farbe jedes Pixels als 32-Bit-Zahl: 8 Bits für Rot, grün, blau und alpha.</span><span class="sxs-lookup"><span data-stu-id="c712a-105">**Image** and **Bitmap** objects store the color of each pixel as a 32-bit number: 8 bits each for red, green, blue, and alpha.</span></span> <span data-ttu-id="c712a-106">Jede der vier Komponenten ist eine Zahl zwischen 0 und 255, wobei 0 keine Intensität und 255 die volle Intensität darstellt.</span><span class="sxs-lookup"><span data-stu-id="c712a-106">Each of the four components is a number from 0 through 255, with 0 representing no intensity and 255 representing full intensity.</span></span> <span data-ttu-id="c712a-107">Die Alpha Komponente gibt die Transparenz der Farbe an: 0 ist vollständig transparent, und 255 ist vollständig undurchsichtig.</span><span class="sxs-lookup"><span data-stu-id="c712a-107">The alpha component specifies the transparency of the color: 0 is fully transparent, and 255 is fully opaque.</span></span>

<span data-ttu-id="c712a-108">Ein Farb Vektor ist ein 4-Tupel im Formular (rot, grün, blau, Alpha).</span><span class="sxs-lookup"><span data-stu-id="c712a-108">A color vector is a 4-tuple of the form (red, green, blue, alpha).</span></span> <span data-ttu-id="c712a-109">Der Farb Vektor (0, 255, 0, 255) stellt z. b. eine nicht transparente Farbe dar, die nicht rot oder blau ist, aber grün mit voller Intensität aufweist.</span><span class="sxs-lookup"><span data-stu-id="c712a-109">For example, the color vector (0, 255, 0, 255) represents an opaque color that has no red or blue, but has green at full intensity.</span></span>

<span data-ttu-id="c712a-110">Eine weitere Konvention für das darstellen von Farben verwendet die Zahl 1 für die maximale Intensität und die Zahl 0 für die minimale Intensität.</span><span class="sxs-lookup"><span data-stu-id="c712a-110">Another convention for representing colors uses the number 1 for maximum intensity and the number 0 for minimum intensity.</span></span> <span data-ttu-id="c712a-111">Mithilfe dieser Konvention würde die im vorangehenden Absatz beschriebene Farbe durch den Vektor (0, 1, 0, 1) dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c712a-111">Using that convention, the color described in the preceding paragraph would be represented by the vector (0, 1, 0, 1).</span></span> <span data-ttu-id="c712a-112">GDI+ verwendet die Konvention 1 als vollständige Intensität, wenn Farb Transformationen durchführt werden.</span><span class="sxs-lookup"><span data-stu-id="c712a-112">GDI+ uses the convention of 1 as full intensity when it performs color transformations.</span></span>

<span data-ttu-id="c712a-113">Sie können lineare Transformationen (Drehung, Skalierung und ähnliches) auf Farb Vektoren anwenden, indem Sie eine Multiplikation mit einer 4 × 4-Matrix durchführen.</span><span class="sxs-lookup"><span data-stu-id="c712a-113">You can apply linear transformations (rotation, scaling, and the like) to color vectors by multiplying by a 4 ×4 matrix.</span></span> <span data-ttu-id="c712a-114">Es ist jedoch nicht möglich, eine 4 × 4-Matrix zum Durchführen einer Übersetzung (Nonlinear) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c712a-114">However, you cannot use a 4 ×4 matrix to perform a translation (nonlinear).</span></span> <span data-ttu-id="c712a-115">Wenn Sie jedem der Farb Vektoren eine dummyminietkoordinate (z. b. die Zahl 1) hinzufügen, können Sie eine beliebige Kombination aus linearen Transformationen und Übersetzungen mit einer 5 × 5-Matrix anwenden.</span><span class="sxs-lookup"><span data-stu-id="c712a-115">If you add a dummy fifth coordinate (for example, the number 1) to each of the color vectors, you can use a 5 ×5 matrix to apply any combination of linear transformations and translations.</span></span> <span data-ttu-id="c712a-116">Eine Transformation, die aus einer linearen Transformation, gefolgt von einer Übersetzung, besteht, wird als affine Transformation bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c712a-116">A transformation consisting of a linear transformation followed by a translation is called an affine transformation.</span></span> <span data-ttu-id="c712a-117">Eine 5 × 5-Matrix, die eine affine-Transformation darstellt, wird für eine Transformation mit vier Leerzeichen als homogene Matrix bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c712a-117">A 5 ×5 matrix that represents an affine transformation is called a homogeneous matrix for a 4-space transformation.</span></span> <span data-ttu-id="c712a-118">Das-Element in der fünften Zeile und fünften Spalte einer homogenen 5 × 5-Matrix muss 1 sein, und alle anderen Einträge in der fünften Spalte müssen 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="c712a-118">The element in the fifth row and fifth column of a 5 ×5 homogeneous matrix must be 1, and all of the other entries in the fifth column must be 0.</span></span>

<span data-ttu-id="c712a-119">Nehmen Sie beispielsweise an, Sie möchten mit der Farbe (0,2, 0,0, 0,4, 1,0) beginnen und die folgenden Transformationen anwenden:</span><span class="sxs-lookup"><span data-stu-id="c712a-119">For example, suppose you want to start with the color (0.2, 0.0, 0.4, 1.0) and apply the following transformations:</span></span>

1.  <span data-ttu-id="c712a-120">Doppelte der roten Komponente</span><span class="sxs-lookup"><span data-stu-id="c712a-120">Double the red component</span></span>
2.  <span data-ttu-id="c712a-121">Fügen Sie 0,2 der roten, grünen und blauen Komponenten hinzu.</span><span class="sxs-lookup"><span data-stu-id="c712a-121">Add 0.2 to the red, green, and blue components</span></span>

<span data-ttu-id="c712a-122">Die folgende Matrix Multiplikation führt das Transformations Paar in der aufgeführten Reihenfolge aus.</span><span class="sxs-lookup"><span data-stu-id="c712a-122">The following matrix multiplication will perform the pair of transformations in the order listed.</span></span>

![Abbildung, die eine 5x1-Matrix mit Zahlen multipliziert mit einer 5 x 5-Matrix zum Erstellen einer neuen 5x1-Matrix anzeigt](images/recoloring01.png)

<span data-ttu-id="c712a-124">Die Elemente einer Farbmatrix werden nach Zeile und Spalte indiziert (null basiert).</span><span class="sxs-lookup"><span data-stu-id="c712a-124">The elements of a color matrix are indexed (zero-based) by row and then column.</span></span> <span data-ttu-id="c712a-125">Der Eintrag in der fünften Zeile und die dritte Spalte der Matrix m werden z. b. durch M \[ 4 \] \[ 2 angegeben \] .</span><span class="sxs-lookup"><span data-stu-id="c712a-125">For example, the entry in the fifth row and third column of matrix M is denoted by M\[4\]\[2\].</span></span>

<span data-ttu-id="c712a-126">Die 5 × 5-Identitätsmatrix (in der folgenden Abbildung dargestellt) verfügt über 1 s auf der diagonalen und an allen anderen Orten.</span><span class="sxs-lookup"><span data-stu-id="c712a-126">The 5 ×5 identity matrix (shown in the following illustration) has 1s on the diagonal and 0s everywhere else.</span></span> <span data-ttu-id="c712a-127">Wenn Sie einen Farb Vektor anhand der Identitätsmatrix multiplizieren, wird der Farb Vektor nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="c712a-127">If you multiply a color vector by the identity matrix, the color vector does not change.</span></span> <span data-ttu-id="c712a-128">Eine bequeme Möglichkeit zum bilden der Matrix einer Farb Transformation besteht darin, mit der Identitätsmatrix zu beginnen und eine kleine Änderung vorzunehmen, die die gewünschte Transformation erzeugt.</span><span class="sxs-lookup"><span data-stu-id="c712a-128">A convenient way to form the matrix of a color transformation is to start with the identity matrix and make a small change that produces the desired transformation.</span></span>

![Abbildung, die eine 5 x 5-Identitätsmatrix zeigt 1 s oben links nach unten rechts Diagonal und 0s überall sonst](images/recoloring02.png)

<span data-ttu-id="c712a-130">Eine ausführlichere Erörterung von Matrizen und Transformationen finden Sie unter [Koordinatensysteme und Transformationen](-gdiplus-coordinate-systems-and-transformations-about.md).</span><span class="sxs-lookup"><span data-stu-id="c712a-130">For a more detailed discussion of matrices and transformations, see [Coordinate Systems and Transformations](-gdiplus-coordinate-systems-and-transformations-about.md).</span></span>

<span data-ttu-id="c712a-131">Im folgenden Beispiel wird ein Bild mit allen Farben (0,2, 0,0, 0,4, 1,0) angenommen, und die in den vorherigen Abschnitten beschriebene Transformation wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="c712a-131">The following example takes an image that is all one color (0.2, 0.0, 0.4, 1.0) and applies the transformation described in the preceding paragraphs.</span></span>


```
Image            image(L"InputColor.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   2.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 1.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
   0.2f, 0.2f, 0.2f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10);

graphics.DrawImage(
   &image, 
   Rect(120, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



<span data-ttu-id="c712a-132">Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das transformierte Bild auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="c712a-132">The following illustration shows the original image on the left and the transformed image on the right.</span></span>

![<span data-ttu-id="c712a-133">Darstellung eines Rechtecks, das durch eine dunkle voll Tonfarbe und dann durch eine hellere voll Tonfarbe gefüllt ist</span><span class="sxs-lookup"><span data-stu-id="c712a-133">illustration showing a rectangle filled by a dark solid color and then one filled by a lighter solid color</span></span> ](images/colortrans1.png)

<span data-ttu-id="c712a-134">Der Code im vorherigen Beispiel führt die folgenden Schritte aus, um die Neueinfärbung durchzuführen:</span><span class="sxs-lookup"><span data-stu-id="c712a-134">The code in the preceding example uses the following steps to perform the recoloring:</span></span>

1.  <span data-ttu-id="c712a-135">Initialisieren Sie eine [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c712a-135">Initialize a [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) structure.</span></span>
2.  <span data-ttu-id="c712a-136">Erstellen Sie ein [**imageattributobjekt**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) , und übergeben Sie die Adresse der [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) -Struktur an die [**imageattribute:: SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) -Methode des **imageattribute** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="c712a-136">Create an [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object and pass the address of the [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) structure to the [**ImageAttributes::SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) method of the **ImageAttributes** object.</span></span>
3.  <span data-ttu-id="c712a-137">Übergeben Sie die Adresse des [**imageattributobjekts**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) an die [DrawImage-Methoden](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) Methode eines [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts.</span><span class="sxs-lookup"><span data-stu-id="c712a-137">Pass the address of the [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object to the [DrawImage Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) method of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

 

 



