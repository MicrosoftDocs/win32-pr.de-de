---
description: Sie können sich die Projektions Transformation als Steuerung der Interna der Kamera vorstellen. Es ist analog zur Auswahl eines Lens für die Kamera.
ms.assetid: 09e6e887-7657-4654-be19-2e83dcbc91cf
title: Projektions Transformation (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b518583dd534bec9784590150233847274ca71
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213927"
---
# <a name="projection-transform-direct3d-9"></a><span data-ttu-id="4e31d-103">Projektions Transformation (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4e31d-103">Projection Transform (Direct3D 9)</span></span>

<span data-ttu-id="4e31d-104">Sie können sich die Projektions Transformation als Steuerung der Interna der Kamera vorstellen. Es ist analog zur Auswahl eines Lens für die Kamera.</span><span class="sxs-lookup"><span data-stu-id="4e31d-104">You can think of the projection transformation as controlling the camera's internals; it is analogous to choosing a lens for the camera.</span></span> <span data-ttu-id="4e31d-105">Dies ist die komplizierteste der drei Transformations Typen.</span><span class="sxs-lookup"><span data-stu-id="4e31d-105">This is the most complicated of the three transformation types.</span></span> <span data-ttu-id="4e31d-106">Diese Erörterung der Projektions Transformation ist in die folgenden Themen gegliedert.</span><span class="sxs-lookup"><span data-stu-id="4e31d-106">This discussion of the projection transformation is organized into the following topics.</span></span>

<span data-ttu-id="4e31d-107">Die Projektions Matrix ist in der Regel eine Skalierungs-und Perspektiven Projektion.</span><span class="sxs-lookup"><span data-stu-id="4e31d-107">The projection matrix is typically a scale and perspective projection.</span></span> <span data-ttu-id="4e31d-108">Die Projektions Transformation konvertiert die Anzeige Frustration in eine Cuboid-Form.</span><span class="sxs-lookup"><span data-stu-id="4e31d-108">The projection transformation converts the viewing frustum into a cuboid shape.</span></span> <span data-ttu-id="4e31d-109">Da das Near-Ende der Anzeige von Frustum kleiner als das Ende ist, wirkt sich dies auf das Erweitern von Objekten aus, die sich in der Nähe der Kamera befinden. auf diese Weise wird die Perspektive auf die Szene angewendet.</span><span class="sxs-lookup"><span data-stu-id="4e31d-109">Because the near end of the viewing frustum is smaller than the far end, this has the effect of expanding objects that are near to the camera; this is how perspective is applied to the scene.</span></span>

<span data-ttu-id="4e31d-110">Beim [Anzeigen von "Frustum](viewports-and-clipping.md)" wird der Abstand zwischen der Kamera und dem Ursprung des Anzeige Transformations Bereichs willkürlich als D definiert, sodass die Projektions Matrix wie in der folgenden Abbildung aussieht.</span><span class="sxs-lookup"><span data-stu-id="4e31d-110">In [the viewing frustum](viewports-and-clipping.md), the distance between the camera and the origin of the viewing transform space is defined arbitrarily as D, so the projection matrix looks like the following illustration.</span></span>

![Abbildung der Projektions Matrix](images/projmat1.png)

<span data-ttu-id="4e31d-112">Die Anzeige Matrix übersetzt die Kamera in den Ursprung, indem Sie in die z-Richtung nach-D übersetzt. Die Übersetzungs Matrix ähnelt der folgenden Abbildung.</span><span class="sxs-lookup"><span data-stu-id="4e31d-112">The viewing matrix translates the camera to the origin by translating in the z direction by - D. The translation matrix is like the following illustration.</span></span>

![Darstellung der Übersetzungs Matrix](images/projmat2.png)

<span data-ttu-id="4e31d-114">Das Multiplizieren der Übersetzungs Matrix durch die Projektions Matrix (T \* P) liefert die zusammengesetzte Projektions Matrix, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4e31d-114">Multiplying the translation matrix by the projection matrix (T\*P) gives the composite projection matrix, as shown in the following illustration.</span></span>

![Abbildung der zusammengesetzten Projektions Matrix](images/projmat3.png)

<span data-ttu-id="4e31d-116">Die Transformation für Perspektiven konvertiert ein Anzeige-Frustum in einen neuen Koordinaten Bereich.</span><span class="sxs-lookup"><span data-stu-id="4e31d-116">The perspective transform converts a viewing frustum into a new coordinate space.</span></span> <span data-ttu-id="4e31d-117">Beachten Sie, dass die Frustration zu Cuboid wird und dass der Ursprung von der oberen rechten Ecke der Szene in den Mittelpunkt wechselt, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4e31d-117">Notice that the frustum becomes cuboid and also that the origin moves from the upper-right corner of the scene to the center, as shown in the following diagram.</span></span>

![Diagramm der Art und Weise, in der die perspektivische Transformation die Anzeige Frustration in einen neuen Koordinaten Bereich ändert](images/cuboid.png)

<span data-ttu-id="4e31d-119">In der Transformation für Perspektiven sind die Begrenzungen der x-und y-Richtungen-1 und 1.</span><span class="sxs-lookup"><span data-stu-id="4e31d-119">In the perspective transform, the limits of the x- and y-directions are -1 and 1.</span></span> <span data-ttu-id="4e31d-120">Die Grenzwerte für die z-Richtung sind 0 für die Vorderseite und 1 für die Backplane.</span><span class="sxs-lookup"><span data-stu-id="4e31d-120">The limits of the z-direction are 0 for the front plane and 1 for the back plane.</span></span>

<span data-ttu-id="4e31d-121">Diese Matrix übersetzt und skaliert Objekte auf der Grundlage einer angegebenen Entfernung von der Kamera auf die Near Clipping-Ebene, berücksichtigt jedoch nicht das Sichtfeld (Field of View, FOV), und die z-Werte, die für Objekte in der Entfernung erzeugt werden, können nahezu identisch sein, sodass Tiefe Vergleiche schwierig werden.</span><span class="sxs-lookup"><span data-stu-id="4e31d-121">This matrix translates and scales objects based on a specified distance from the camera to the near clipping plane, but it doesn't consider the field of view (fov), and the z-values that it produces for objects in the distance can be nearly identical, making depth comparisons difficult.</span></span> <span data-ttu-id="4e31d-122">Die folgende Matrix behandelt diese Probleme und passt die Scheitel Punkte an, um das Seitenverhältnis des Viewports zu berücksichtigen, sodass es eine gute Wahl für die perspektivische Projektion ist.</span><span class="sxs-lookup"><span data-stu-id="4e31d-122">The following matrix addresses these issues, and it adjusts vertices to account for the aspect ratio of the viewport, making it a good choice for the perspective projection.</span></span>

![Abbildung einer Matrix für die perspektivische Projektion](images/prjmatx1.png)

<span data-ttu-id="4e31d-124">In dieser Matrix ist "Zn" der z-Wert der Near Clipping-Ebene.</span><span class="sxs-lookup"><span data-stu-id="4e31d-124">In this matrix, Zₙ is the z-value of the near clipping plane.</span></span> <span data-ttu-id="4e31d-125">Die Variablen "w", "h" und "Q" haben folgende Bedeutungen.</span><span class="sxs-lookup"><span data-stu-id="4e31d-125">The variables w, h, and Q have the following meanings.</span></span> <span data-ttu-id="4e31d-126">Beachten Sie, dass FOV<sub>w</sub> und fovk die horizontalen und vertikalen Ansichts Felder des Viewports im Bogenmaße darstellen.</span><span class="sxs-lookup"><span data-stu-id="4e31d-126">Note that fov<sub>w</sub> and fovₖ represent the viewport's horizontal and vertical fields of view, in radians.</span></span>

![Gleichungen der Variablen Bedeutungen](images/prjmatx2.png)

<span data-ttu-id="4e31d-128">Für Ihre Anwendung ist die Verwendung von Feld-of-View-Winkeln zum Definieren der Koeffizienten für die x-und y-Skalierung möglicherweise nicht so praktisch wie die horizontale und vertikale Abmessungen des Viewports (im Kamerabereich).</span><span class="sxs-lookup"><span data-stu-id="4e31d-128">For your application, using field-of-view angles to define the x- and y-scaling coefficients might not be as convenient as using the viewport's horizontal and vertical dimensions (in camera space).</span></span> <span data-ttu-id="4e31d-129">Wenn die mathematische Funktion funktioniert, verwenden die beiden folgenden Gleichungen für w und h die Abmessungen des Viewports und entsprechen den vorangehenden Gleichungen.</span><span class="sxs-lookup"><span data-stu-id="4e31d-129">As the math works out, the following two equations for w and h use the viewport's dimensions, and are equivalent to the preceding equations.</span></span>

![Gleichungen der w-und h-Variablen Bedeutungen](images/prjmatx3.png)

<span data-ttu-id="4e31d-131">In diesen Formeln stellt "Zn" die Position der Near Clipping-Ebene dar, und die V<sub>w</sub> -und die VH-Variablen stellen die Breite und Höhe des Viewports im Kamerabereich dar.</span><span class="sxs-lookup"><span data-stu-id="4e31d-131">In these formulas, Zₙ represents the position of the near clipping plane, and the V<sub>w</sub> and Vₕ variables represent the width and height of the viewport, in camera space.</span></span>

<span data-ttu-id="4e31d-132">Bei einer C++-Anwendung entsprechen diese beiden Dimensionen direkt den Elementen Width und Height der [**D3DVIEWPORT9**](d3dviewport9.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4e31d-132">For a C++ application, these two dimensions correspond directly to the Width and Height members of the [**D3DVIEWPORT9**](d3dviewport9.md) structure.</span></span>

<span data-ttu-id="4e31d-133">Egal, welche Formel Sie verwenden möchten, achten Sie darauf, dass Sie den Wert für "Zn" so groß wie möglich festlegen, da z-Werte, die sich extrem nahe an der Kamera befinden, nicht um viel variieren.</span><span class="sxs-lookup"><span data-stu-id="4e31d-133">Whatever formula you decide to use, be sure to set Zₙ to as large a value as possible, because z-values extremely close to the camera don't vary by much.</span></span> <span data-ttu-id="4e31d-134">Dies macht Tiefe Vergleiche mit 16-Bit-z-Puffern etwas kompliziert.</span><span class="sxs-lookup"><span data-stu-id="4e31d-134">This makes depth comparisons using 16-bit z-buffers somewhat complicated.</span></span>

<span data-ttu-id="4e31d-135">Wie bei den Transformationen der Welt und Sicht wird die [**IDirect3DDevice9:: setTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) -Methode aufgerufen, um die Projektions Transformation festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4e31d-135">As with the world and view transformations, you call the [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) method to set the projection transform.</span></span>

## <a name="setting-up-a-projection-matrix"></a><span data-ttu-id="4e31d-136">Einrichten einer Projektions Matrix</span><span class="sxs-lookup"><span data-stu-id="4e31d-136">Setting Up a Projection Matrix</span></span>

<span data-ttu-id="4e31d-137">Mit der folgenden ProjectionMatrix-Beispiel Funktion werden die Front-und Back-clippingflächen sowie das horizontale und vertikale Feld von Sicht Winkeln festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4e31d-137">The following ProjectionMatrix sample function sets the front and back clipping planes, as well as the horizontal and vertical field of view angles.</span></span> <span data-ttu-id="4e31d-138">Die Felder der Ansicht sollten kleiner als PI-Bogenmaße sein.</span><span class="sxs-lookup"><span data-stu-id="4e31d-138">The fields of view should be less than pi radians.</span></span>


```
D3DXMATRIX 
ProjectionMatrix(const float near_plane, // Distance to near clipping 
                                         // plane
                 const float far_plane,  // Distance to far clipping 
                                         // plane
                 const float fov_horiz,  // Horizontal field of view 
                                         // angle, in radians
                 const float fov_vert)   // Vertical field of view 
                                         // angle, in radians
{
    float    h, w, Q;

    w = (float)1/tan(fov_horiz*0.5);  // 1/tan(x) == cot(x)
    h = (float)1/tan(fov_vert*0.5);   // 1/tan(x) == cot(x)
    Q = far_plane/(far_plane - near_plane);

    D3DXMATRIX ret;
    ZeroMemory(&ret, sizeof(ret));

    ret(0, 0) = w;
    ret(1, 1) = h;
    ret(2, 2) = Q;
    ret(3, 2) = -Q*near_plane;
    ret(2, 3) = 1;
    return ret;
}   // End of ProjectionMatrix
```



<span data-ttu-id="4e31d-139">Legen Sie nach dem Erstellen der Matrix mit [**IDirect3DDevice9:: setTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) eine D3DTS- \_ Projektion fest.</span><span class="sxs-lookup"><span data-stu-id="4e31d-139">After creating the matrix, set it with [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) specifying D3DTS\_PROJECTION.</span></span>

<span data-ttu-id="4e31d-140">Die D3DX Utility Library bietet die folgenden Funktionen, die Ihnen beim Einrichten der Projektions Matrix helfen.</span><span class="sxs-lookup"><span data-stu-id="4e31d-140">The D3DX utility library provides the following functions to help you set up your projection matrix.</span></span>

-   [<span data-ttu-id="4e31d-141">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="4e31d-141">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
-   [<span data-ttu-id="4e31d-142">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="4e31d-142">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
-   [<span data-ttu-id="4e31d-143">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="4e31d-143">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
-   [<span data-ttu-id="4e31d-144">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="4e31d-144">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
-   [<span data-ttu-id="4e31d-145">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="4e31d-145">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
-   [<span data-ttu-id="4e31d-146">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="4e31d-146">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)

## <a name="a-w-friendly-projection-matrix"></a><span data-ttu-id="4e31d-147">Eine W-freundliche Projektions Matrix</span><span class="sxs-lookup"><span data-stu-id="4e31d-147">A W-Friendly Projection Matrix</span></span>

<span data-ttu-id="4e31d-148">Direct3D kann die w-Komponente eines Scheitel Punkts verwenden, der von der Welt-, Sicht-und Projektions Matrizen transformiert wurde, um Tiefe basierte Berechnungen in tiefen Puffern oder Nebeleffekten auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4e31d-148">Direct3D can use the w-component of a vertex that has been transformed by the world, view, and projection matrices to perform depth-based calculations in depth-buffer or fog effects.</span></span> <span data-ttu-id="4e31d-149">Für Berechnungen wie diese ist es erforderlich, dass die Projektions Matrix w normalisiert, damit Sie dem Raum z entspricht.</span><span class="sxs-lookup"><span data-stu-id="4e31d-149">Computations such as these require that your projection matrix normalize w to be equivalent to world-space z.</span></span> <span data-ttu-id="4e31d-150">Kurz gesagt, wenn die Projektions Matrix einen (3, 4) Koeffizienten enthält, der nicht 1 ist, müssen Sie alle Koeffizienten mit der Umkehrung des (3, 4) Koeffizienten skalieren, um eine korrekte Matrix zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4e31d-150">In short, if your projection matrix includes a (3,4) coefficient that is not 1, you must scale all the coefficients by the inverse of the (3,4) coefficient to make a proper matrix.</span></span> <span data-ttu-id="4e31d-151">Wenn Sie keine konforme Matrix bereitstellen, werden die Nebeleffekte und die tiefen Pufferung nicht ordnungsgemäß angewendet.</span><span class="sxs-lookup"><span data-stu-id="4e31d-151">If you don't provide a compliant matrix, fog effects and depth buffering are not applied correctly.</span></span>

<span data-ttu-id="4e31d-152">In der folgenden Abbildung ist eine nicht kompatible Projektions Matrix dargestellt, und die gleiche Matrix wird so skaliert, dass der Augen relative Nebel aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="4e31d-152">The following illustration shows a noncompliant projection matrix, and the same matrix scaled so that eye-relative fog will be enabled.</span></span>

![Abbildungen einer nicht kompatiblen Projektions Matrix und einer Matrix mit augenblickativem Nebel](images/eyerlmx.png)

<span data-ttu-id="4e31d-154">In den vorangehenden Matrizen werden alle Variablen als ungleich Null angenommen.</span><span class="sxs-lookup"><span data-stu-id="4e31d-154">In the preceding matrices, all variables are assumed to be nonzero.</span></span> <span data-ttu-id="4e31d-155">Weitere Informationen über Eye-relative Nebel finden Sie unter [Eye-relative im Vergleich zu Z-basierter Tiefe](pixel-fog.md).</span><span class="sxs-lookup"><span data-stu-id="4e31d-155">For more information about eye-relative fog, see [Eye-Relative vs. Z-Based Depth](pixel-fog.md).</span></span> <span data-ttu-id="4e31d-156">Weitere Informationen zur w-basierten tiefen Pufferung finden Sie unter [tiefen Puffer (Direct3D 9)](depth-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="4e31d-156">For information about w-based depth buffering, see [Depth Buffers (Direct3D 9)](depth-buffers.md).</span></span>

<span data-ttu-id="4e31d-157">Direct3D verwendet die aktuell festgelegte Projektions Matrix in den w-basierten tiefen Berechnungen.</span><span class="sxs-lookup"><span data-stu-id="4e31d-157">Direct3D uses the currently set projection matrix in its w-based depth calculations.</span></span> <span data-ttu-id="4e31d-158">Daher müssen Anwendungen eine konforme Projektions Matrix festlegen, um die gewünschten w-basierten Funktionen zu erhalten, auch wenn Sie keine Direct3D für Transformationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4e31d-158">As a result, applications must set a compliant projection matrix to receive the desired w-based features, even if they do not use Direct3D for transforms.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e31d-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4e31d-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e31d-160">Transformationen</span><span class="sxs-lookup"><span data-stu-id="4e31d-160">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 
