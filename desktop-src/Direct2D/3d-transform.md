---
title: 3D-Transformationseffekt
description: Mit dem 3D-Transformations Effekt können Sie eine beliebige 4X4-Transformationsmatrix auf ein Bild anwenden.
ms.assetid: BC2F2837-40F0-4293-A190-8B5F81BB01B6
keywords:
- 3D--Transformations Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabe0c2c220038802b5218b54187a1ff89268bfa
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "104559862"
---
# <a name="3d-transform-effect"></a><span data-ttu-id="60ccc-104">3D-Transformationseffekt</span><span class="sxs-lookup"><span data-stu-id="60ccc-104">3D transform effect</span></span>

<span data-ttu-id="60ccc-105">Mit dem 3D-Transformations Effekt können Sie eine beliebige 4X4-Transformationsmatrix auf ein Bild anwenden.</span><span class="sxs-lookup"><span data-stu-id="60ccc-105">Use the 3D transform effect to apply an arbitrary 4x4 transform matrix to an image.</span></span>

<span data-ttu-id="60ccc-106">Dieser Effekt wendet die von Ihnen bereitgestellte Matrix (M?) auf die eckscheitel Punkte des Quell Bilds ( \[ x y z 1) an, \] indem diese Berechnung verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="60ccc-106">This effect applies the matrix (M?) you provide to the corner vertices of the source image (\[ x y z 1 \]) using this calculation:</span></span>

<span data-ttu-id="60ccc-107">\[x<sub>r</sub> y<sub>r</sub> z<sub>r</sub> 1 \] = \[ x y z 1 \] \* M?</span><span class="sxs-lookup"><span data-stu-id="60ccc-107">\[ x<sub>r</sub> y<sub>r</sub> z<sub>r</sub> 1 \]=\[ x y z 1 \]\*M?</span></span>

<span data-ttu-id="60ccc-108">Die CLSID für diesen Effekt ist CLSID \_ D2D13DTransform.</span><span class="sxs-lookup"><span data-stu-id="60ccc-108">The CLSID for this effect is CLSID\_D2D13DTransform.</span></span>

-   [<span data-ttu-id="60ccc-109">Beispiel Bild</span><span class="sxs-lookup"><span data-stu-id="60ccc-109">Example image</span></span>](#example-image)
-   [<span data-ttu-id="60ccc-110">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="60ccc-110">Effect properties</span></span>](#effect-properties)
    -   [<span data-ttu-id="60ccc-111">Interpolations Modi</span><span class="sxs-lookup"><span data-stu-id="60ccc-111">Interpolation modes</span></span>](#interpolation-modes)
    -   [<span data-ttu-id="60ccc-112">Rahmen Modi</span><span class="sxs-lookup"><span data-stu-id="60ccc-112">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="60ccc-113">4X4-Transformations Matrix Klasse</span><span class="sxs-lookup"><span data-stu-id="60ccc-113">4x4 Transform Matrix Class</span></span>](#4x4-transform-matrix-class)
-   [<span data-ttu-id="60ccc-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60ccc-114">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="60ccc-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="60ccc-115">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="60ccc-116">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="60ccc-116">Example image</span></span>



| <span data-ttu-id="60ccc-117">Vorher</span><span class="sxs-lookup"><span data-stu-id="60ccc-117">Before</span></span>                                                        |
|---------------------------------------------------------------|
| ![das Bild vor der Transformation.](images/default-before.jpg) |
| <span data-ttu-id="60ccc-119">Nach</span><span class="sxs-lookup"><span data-stu-id="60ccc-119">After</span></span>                                                         |
| ![das Bild nach der Transformation.](images/24-3dtransform.png)  |



 


```C++
ComPtr<ID2D1Effect> D2D13DTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DTransform, &D2D13DTransformEffect);

D2D13DTransformEffect->SetInput(0, bitmap);

// You can use the helper methods in D2D1::Matrix4x4F to create common matrix transformations.
D2D1_MATRIX_4X4_F matrix = 
    D2D1::Matrix4x4F::Translation(0.0f, -192.0f, 0.0f) *
    D2D1::Matrix4x4F::RotationY(30.0f) *
    D2D1::Matrix4x4F::Translation(0.0f, 192.0f, 0.0f);

D2D13DTransformEffect->SetValue(D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(D2D13DTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="60ccc-121">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="60ccc-121">Effect properties</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="60ccc-122">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="60ccc-122">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="60ccc-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60ccc-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="60ccc-124">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="60ccc-124">InterpolationMode</span></span><br/> <span data-ttu-id="60ccc-125">D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE</span><span class="sxs-lookup"><span data-stu-id="60ccc-125">D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE</span></span><br/></td>
<td><span data-ttu-id="60ccc-126">Der Interpolations Modus, den der Effekt für das Bild verwendet.</span><span class="sxs-lookup"><span data-stu-id="60ccc-126">The interpolation mode the effect uses on the image.</span></span> <span data-ttu-id="60ccc-127">Es gibt fünf Skalierungs Modi, die die Qualität und Geschwindigkeit unterliegen.</span><span class="sxs-lookup"><span data-stu-id="60ccc-127">There are 5 scale modes that range in quality and speed.</span></span><br/> <span data-ttu-id="60ccc-128">Der Typ ist D2D1_3DTRANSFORM_INTERPOLATION_MODE.</span><span class="sxs-lookup"><span data-stu-id="60ccc-128">Type is D2D1_3DTRANSFORM_INTERPOLATION_MODE.</span></span><br/> <span data-ttu-id="60ccc-129">Der Standardwert ist D2D1_3DTRANSFORM_INTERPOLATION_MODE_LINEAR.</span><span class="sxs-lookup"><span data-stu-id="60ccc-129">Default value is D2D1_3DTRANSFORM_INTERPOLATION_MODE_LINEAR.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="60ccc-130">Bordermode</span><span class="sxs-lookup"><span data-stu-id="60ccc-130">BorderMode</span></span><br/> <span data-ttu-id="60ccc-131">D2D1_3DTRANSFORM_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="60ccc-131">D2D1_3DTRANSFORM_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="60ccc-132">Der Modus, der verwendet wird, um den Rahmen des Bilds zu berechnen, weich oder hart.</span><span class="sxs-lookup"><span data-stu-id="60ccc-132">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="60ccc-133">Weitere Informationen finden Sie unter <a href="https://www.bing.com/search?q=Border+modes">Border Modes</a> .</span><span class="sxs-lookup"><span data-stu-id="60ccc-133">See <a href="https://www.bing.com/search?q=Border+modes">Border modes</a> for more info.</span></span><br/> <span data-ttu-id="60ccc-134">Der Typ ist D2D1_BORDER_MODE.</span><span class="sxs-lookup"><span data-stu-id="60ccc-134">Type is D2D1_BORDER_MODE.</span></span><br/> <span data-ttu-id="60ccc-135">Der Standardwert ist D2D1_BORDER_MODE_SOFT.</span><span class="sxs-lookup"><span data-stu-id="60ccc-135">Default value is D2D1_BORDER_MODE_SOFT.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="60ccc-136">TransformMatrix</span><span class="sxs-lookup"><span data-stu-id="60ccc-136">TransformMatrix</span></span><br/> <span data-ttu-id="60ccc-137">D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX</span><span class="sxs-lookup"><span data-stu-id="60ccc-137">D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX</span></span><br/></td>
<td><span data-ttu-id="60ccc-138">Eine 4X4-Transformationsmatrix, die auf die Projektionsebene angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="60ccc-138">A 4x4 transform matrix applied to the projection plane.</span></span> <span data-ttu-id="60ccc-139">Die folgende Matrix Berechnung wird verwendet, um Punkte von einem 3D-Koordinatensystem zum transformierten 2D-Koordinatensystem zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="60ccc-139">The following matrix calculation is used to map points from one 3D coordinate system to the transformed 2D coordinate system.</span></span> <br/><img src="images/3d-transform-matrix1.png" alt="3D Depth Matrix" /><span data-ttu-id="60ccc-140">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="60ccc-140">Where:</span></span><dl> <span data-ttu-id="60ccc-141">X, Y, Z = Eingabe Projektions Ebenen-Koordinaten</span><span class="sxs-lookup"><span data-stu-id="60ccc-141">X, Y, Z = Input projection plane coordinates</span></span><br />
<span data-ttu-id="60ccc-142">M<sub>x, y</sub> = Transformations Matrix Elemente</span><span class="sxs-lookup"><span data-stu-id="60ccc-142">M<sub>x,y</sub> = Transform Matrix elements</span></span><br />
<span data-ttu-id="60ccc-143">X, Y, Z = Koordinaten der Ausgabe Projektionsebene</span><span class="sxs-lookup"><span data-stu-id="60ccc-143">X , Y , Z  =Output projection plane coordinates</span></span><br />
</dl> <br/> <span data-ttu-id="60ccc-144">Die einzelnen Matrix Elemente sind nicht gebunden und sind unitless.</span><span class="sxs-lookup"><span data-stu-id="60ccc-144">The individual matrix elements are not bounded and are unitless.</span></span> <br/> <span data-ttu-id="60ccc-145">Der Typ ist D2D1_MATRIX_4X4_F.</span><span class="sxs-lookup"><span data-stu-id="60ccc-145">Type is D2D1_MATRIX_4X4_F.</span></span><br/> <span data-ttu-id="60ccc-146">Der Standardwert ist Matrix4x4F (1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="60ccc-146">Default value is Matrix4x4F(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1).</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-modes"></a><span data-ttu-id="60ccc-147">Interpolations Modi</span><span class="sxs-lookup"><span data-stu-id="60ccc-147">Interpolation modes</span></span>



| <span data-ttu-id="60ccc-148">Enumeration</span><span class="sxs-lookup"><span data-stu-id="60ccc-148">Enumeration</span></span>                                                   | <span data-ttu-id="60ccc-149">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60ccc-149">Description</span></span>                                                                                                                                                |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60ccc-150">D2D1 \_ 3dtransform- \_ Interpolations \_ Modus \_ Nächster \_ Nachbar</span><span class="sxs-lookup"><span data-stu-id="60ccc-150">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="60ccc-151">Verwendet den nächsten einzelnen Punkt und verwendet diesen.</span><span class="sxs-lookup"><span data-stu-id="60ccc-151">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="60ccc-152">Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das niedrigste Qualitätsbild aus.</span><span class="sxs-lookup"><span data-stu-id="60ccc-152">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                 |
| <span data-ttu-id="60ccc-153">D2D1 \_ 3dtransform- \_ Interpolations \_ Modus \_ linear</span><span class="sxs-lookup"><span data-stu-id="60ccc-153">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="60ccc-154">Verwendet ein vier-Punkt-Beispiel und eine lineare interpolung.</span><span class="sxs-lookup"><span data-stu-id="60ccc-154">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="60ccc-155">Dieser Modus verwendet mehr Verarbeitungszeit als der nächstgelegene Nachbar Modus, gibt aber ein Image mit höherer Qualität aus.</span><span class="sxs-lookup"><span data-stu-id="60ccc-155">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span> |
| <span data-ttu-id="60ccc-156">D2D1 \_ 3dtransform- \_ Interpolations \_ Modus ( \_ kubisch)</span><span class="sxs-lookup"><span data-stu-id="60ccc-156">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="60ccc-157">Verwendet einen 16-beispielkubischen Kernel für Interpolationen.</span><span class="sxs-lookup"><span data-stu-id="60ccc-157">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="60ccc-158">In diesem Modus wird die meiste Verarbeitungszeit verwendet, es wird jedoch ein Image mit höherer Qualität ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="60ccc-158">This mode uses the most processing time, but outputs a higher quality image.</span></span>                              |
| <span data-ttu-id="60ccc-159">D2D1 \_ 3dtransform \_ Interpolations \_ Modus \_ \_ Multisample \_ linear</span><span class="sxs-lookup"><span data-stu-id="60ccc-159">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="60ccc-160">Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für eine gute Edge-Antialiasing.</span><span class="sxs-lookup"><span data-stu-id="60ccc-160">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="60ccc-161">Dieser Modus eignet sich gut zum horizontalen Herunterskalieren um kleine Beträge in Bildern mit wenigen Pixeln.</span><span class="sxs-lookup"><span data-stu-id="60ccc-161">This mode is good for scaling down by small amounts on images with few pixels.</span></span>    |
| <span data-ttu-id="60ccc-162">D2D1 \_ 3dtransform- \_ Interpolations \_ Modus \_ anisotrope</span><span class="sxs-lookup"><span data-stu-id="60ccc-162">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="60ccc-163">Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap zu modellieren.</span><span class="sxs-lookup"><span data-stu-id="60ccc-163">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                           |



 

> [!Note]  
> <span data-ttu-id="60ccc-164">Wenn Sie keinen Modus auswählen, wird der Effekt standardmäßig auf den D2D1 \_ 3dtransform- \_ Interpolations \_ Modus linear festgelegt \_ .</span><span class="sxs-lookup"><span data-stu-id="60ccc-164">If you don't select a mode, the effect defaults to D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="60ccc-165">Der anisotrope-Modus generiert bei der Skalierung Mipmaps. Wenn Sie jedoch die **zwischengespeicherte** Eigenschaft für die Effekte, die für diesen Effekt eingegeben werden, auf true festlegen, werden die Mipmaps bei ausreichend kleinen Bildern nicht jedes Mal generiert.</span><span class="sxs-lookup"><span data-stu-id="60ccc-165">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

### <a name="border-modes"></a><span data-ttu-id="60ccc-166">Rahmen Modi</span><span class="sxs-lookup"><span data-stu-id="60ccc-166">Border modes</span></span>



| <span data-ttu-id="60ccc-167">Name</span><span class="sxs-lookup"><span data-stu-id="60ccc-167">Name</span></span>                     | <span data-ttu-id="60ccc-168">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60ccc-168">Description</span></span>                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60ccc-169">D2D1 \_ Border \_ Mode \_ Soft</span><span class="sxs-lookup"><span data-stu-id="60ccc-169">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="60ccc-170">Der Effekt füllt das Bild mit transparenten schwarzen Pixeln, während es interpoliert, was zu einem weichen Rand führt.</span><span class="sxs-lookup"><span data-stu-id="60ccc-170">The effect pads the image with transparent black pixels as it interpolates, resulting in a soft edge.</span></span><br/> |
| <span data-ttu-id="60ccc-171">D2D1 \_ Rahmen \_ Modus \_ hart</span><span class="sxs-lookup"><span data-stu-id="60ccc-171">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="60ccc-172">Der Effekt bindet die Ausgabe an die Größe des Eingabe Bilds.</span><span class="sxs-lookup"><span data-stu-id="60ccc-172">The effect clamps the output to the size of the input image.</span></span> <br/>                                         |



 

## <a name="4x4-transform-matrix-class"></a><span data-ttu-id="60ccc-173">4X4-Transformations Matrix Klasse</span><span class="sxs-lookup"><span data-stu-id="60ccc-173">4x4 Transform Matrix Class</span></span>

<span data-ttu-id="60ccc-174">Direct2D stellt eine 4X4-Matrix Klasse zum Bereitstellen von Hilfsfunktionen zum Transformieren des Bilds in drei Dimensionen bereit.</span><span class="sxs-lookup"><span data-stu-id="60ccc-174">Direct2D provides a 4x4 matrix class to provide helper functions for transforming the image in 3 dimensions.</span></span> <span data-ttu-id="60ccc-175">Weitere Informationen und eine Beschreibung aller Klassenmember finden Sie im Thema [**Matrix4x4F**](/windows/desktop/api/d2d1_1helper/nl-d2d1_1helper-matrix4x4f) .</span><span class="sxs-lookup"><span data-stu-id="60ccc-175">See the [**Matrix4x4F**](/windows/desktop/api/d2d1_1helper/nl-d2d1_1helper-matrix4x4f) topic for more info and a description of all the class members.</span></span>



| <span data-ttu-id="60ccc-176">Funktion</span><span class="sxs-lookup"><span data-stu-id="60ccc-176">Function</span></span>                                | <span data-ttu-id="60ccc-177">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60ccc-177">Description</span></span>                                                                                    | <span data-ttu-id="60ccc-178">Matrix</span><span class="sxs-lookup"><span data-stu-id="60ccc-178">Matrix</span></span>                                                 |
|-----------------------------------------|------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="60ccc-179">Matrix4x4F:: Scale (X, Y, Z)</span><span class="sxs-lookup"><span data-stu-id="60ccc-179">Matrix4x4F::Scale(X, Y, Z)</span></span>              | <span data-ttu-id="60ccc-180">Generiert eine Transformationsmatrix, die die Projektionsebene in der X-, Y-und/oder Z-Richtung skaliert.</span><span class="sxs-lookup"><span data-stu-id="60ccc-180">Generates a transform matrix that scales the projection plane in the X, Y, and/or Z direction.</span></span> | ![scale3d-Matrix](images/3d-transform-matrix2.png)     |
| <span data-ttu-id="60ccc-182">Schrägt (X)</span><span class="sxs-lookup"><span data-stu-id="60ccc-182">SkewX(X)</span></span>                                | <span data-ttu-id="60ccc-183">Generiert eine Transformationsmatrix, die die Projektionsebene in der X-Richtung verzippt.</span><span class="sxs-lookup"><span data-stu-id="60ccc-183">Generates a transform matrix that skews the projection plane in the X direction.</span></span>               | ![Zeigt eine schiefe Matrix in der X-Richtung an.](images/matrix4x4-skewx.png)             |
| <span data-ttu-id="60ccc-185">Schief (Y)</span><span class="sxs-lookup"><span data-stu-id="60ccc-185">SkewY(Y)</span></span>                                | <span data-ttu-id="60ccc-186">Generiert eine Transformationsmatrix, die die Projektionsebene in der Y-Richtung verzippt.</span><span class="sxs-lookup"><span data-stu-id="60ccc-186">Generates a transform matrix that skews the projection plane in the Y direction.</span></span>               | ![Schiefe Matrix](images/matrix4x4-skewy.png)             |
| <span data-ttu-id="60ccc-188">Übersetzung (X, Y, Z)</span><span class="sxs-lookup"><span data-stu-id="60ccc-188">Translation(X, Y, Z)</span></span>                    | <span data-ttu-id="60ccc-189">Generiert eine Transformationsmatrix, die die Projektionsebene in der X-, Y-oder Z-Richtung übersetzt.</span><span class="sxs-lookup"><span data-stu-id="60ccc-189">Generates a transform matrix that translates the projection plane in the X, Y, or Z direction.</span></span> | ![Matrix übersetzen](images/3d-transform-matrix4.png)   |
| <span data-ttu-id="60ccc-191">RotationX (X)</span><span class="sxs-lookup"><span data-stu-id="60ccc-191">RotationX(X)</span></span>                            | <span data-ttu-id="60ccc-192">Generiert eine Transformationsmatrix, die die Projektionsebene um die X-Achse dreht.</span><span class="sxs-lookup"><span data-stu-id="60ccc-192">Generates a transform matrix that rotates the projection plane about the X axis.</span></span>               | ![x-Matrix drehen](images/3d-transform-matrix5.png)    |
| <span data-ttu-id="60ccc-194">RotationY (Y)</span><span class="sxs-lookup"><span data-stu-id="60ccc-194">RotationY(Y)</span></span>                            | <span data-ttu-id="60ccc-195">Generiert eine Transformationsmatrix, die die Projektionsebene um die Y-Achse dreht.</span><span class="sxs-lookup"><span data-stu-id="60ccc-195">Generates a transform matrix that rotates the projection plane about the Y axis.</span></span>               | ![y-Matrix drehen](images/3d-transform-matrix6.png)    |
| <span data-ttu-id="60ccc-197">RotationZ (z)</span><span class="sxs-lookup"><span data-stu-id="60ccc-197">RotationZ(Z)</span></span>                            | <span data-ttu-id="60ccc-198">Generiert eine Transformationsmatrix, die die Projektionsebene um die Z-Achse dreht.</span><span class="sxs-lookup"><span data-stu-id="60ccc-198">Generates a transform matrix that rotates the projection plane about the Z axis.</span></span>               | ![z-Matrix drehen](images/3d-transform-matrix7.png)    |
| <span data-ttu-id="60ccc-200">PerspectiveProjection (D)</span><span class="sxs-lookup"><span data-stu-id="60ccc-200">PerspectiveProjection(D)</span></span>                | <span data-ttu-id="60ccc-201">Eine perspektivische Transformation mit einem tiefen Wert von D.</span><span class="sxs-lookup"><span data-stu-id="60ccc-201">A perspective transformation with a depth value of D.</span></span>                                          | ![Perspektiven Matrix](images/3d-transform-matrix8.png) |
| <span data-ttu-id="60ccc-203">Rotationarbiaryaxis (X, Y, Z, Grad)</span><span class="sxs-lookup"><span data-stu-id="60ccc-203">RotationArbitraryAxis(X, Y, Z, degrees)</span></span> | <span data-ttu-id="60ccc-204">Dreht die Projektionsebene um die von Ihnen angegebene Achse.</span><span class="sxs-lookup"><span data-stu-id="60ccc-204">Rotates the projection plane about the axis you specify.</span></span>                                       |                                                        |



 

## <a name="requirements"></a><span data-ttu-id="60ccc-205">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60ccc-205">Requirements</span></span>



| <span data-ttu-id="60ccc-206">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60ccc-206">Requirement</span></span> | <span data-ttu-id="60ccc-207">Wert</span><span class="sxs-lookup"><span data-stu-id="60ccc-207">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="60ccc-208">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60ccc-208">Minimum supported client</span></span> | <span data-ttu-id="60ccc-209">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60ccc-209">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="60ccc-210">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60ccc-210">Minimum supported server</span></span> | <span data-ttu-id="60ccc-211">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60ccc-211">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="60ccc-212">Header</span><span class="sxs-lookup"><span data-stu-id="60ccc-212">Header</span></span>                   | <span data-ttu-id="60ccc-213">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="60ccc-213">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="60ccc-214">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="60ccc-214">Library</span></span>                  | <span data-ttu-id="60ccc-215">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="60ccc-215">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="60ccc-216">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="60ccc-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60ccc-217">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="60ccc-217">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

