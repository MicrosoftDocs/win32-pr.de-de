---
title: 2D-affiner Transformationseffekt
description: Der 2D-affine Transformations Effekt wendet eine räumliche Transformation auf ein Bild an, das auf einer 3x2-Matrix basiert, indem die Direct2D-Matrix Transformation und alle sechs Interpolations Modi verwendet werden.
ms.assetid: E8973EBE-764C-4220-BB1E-3BFD4853582D
keywords:
- 2D-affiner Transformationseffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3017992d34cd98095f01192ea948684a6b52e53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106563"
---
# <a name="2d-affine-transform-effect"></a><span data-ttu-id="5c4d7-104">2D-affiner Transformationseffekt</span><span class="sxs-lookup"><span data-stu-id="5c4d7-104">2D affine transform effect</span></span>

<span data-ttu-id="5c4d7-105">Der 2D-affine Transformations Effekt wendet eine räumliche Transformation auf ein Bild an, das auf einer 3x2-Matrix basiert, indem die Direct2D-Matrix [Transformation](direct2d-transforms-overview.md) und alle sechs Interpolations Modi verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-105">The 2D affine transform effect applies a spatial transform to a image based on a 3X2 matrix using the Direct2D matrix [transform](direct2d-transforms-overview.md) and any of six interpolation modes.</span></span> <span data-ttu-id="5c4d7-106">Mit diesem Effekt können Sie ein Bild drehen, skalieren, neigen oder übersetzen.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-106">You can use this effect to rotate, scale, skew, or translate an image.</span></span> <span data-ttu-id="5c4d7-107">Sie können diese Vorgänge auch kombinieren.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-107">Or, you can combine these operations.</span></span> <span data-ttu-id="5c4d7-108">Affine-Übertragungen behalten parallele Zeilen und das Verhältnis von Entfernungen zwischen drei Punkten eines Bilds bei.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-108">Affine transfers preserve parallel lines and the ratio of distances between any three points in an image.</span></span>

<span data-ttu-id="5c4d7-109">Die CLSID für diesen Effekt ist CLSID \_ D2D12DAffineTransform.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-109">The CLSID for this effect is CLSID\_D2D12DAffineTransform.</span></span>

-   [<span data-ttu-id="5c4d7-110">Beispiel Bild</span><span class="sxs-lookup"><span data-stu-id="5c4d7-110">Example image</span></span>](#example-image)
-   [<span data-ttu-id="5c4d7-111">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5c4d7-111">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="5c4d7-112">Rahmen Modi</span><span class="sxs-lookup"><span data-stu-id="5c4d7-112">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="5c4d7-113">Interpolations Modi</span><span class="sxs-lookup"><span data-stu-id="5c4d7-113">Interpolation modes</span></span>](#interpolation-modes)
-   [<span data-ttu-id="5c4d7-114">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="5c4d7-114">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="5c4d7-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c4d7-115">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="5c4d7-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5c4d7-116">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="5c4d7-117">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="5c4d7-117">Example image</span></span>



| <span data-ttu-id="5c4d7-118">Vorher</span><span class="sxs-lookup"><span data-stu-id="5c4d7-118">Before</span></span>                                                             |
|--------------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)         |
| <span data-ttu-id="5c4d7-120">Nach</span><span class="sxs-lookup"><span data-stu-id="5c4d7-120">After</span></span>                                                              |
| ![das Bild nach der Transformation.](images/21-2daffinetransform.png) |



 


```C++
ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInput(0, bitmap);

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F(0.9f, -0.1f,   0.1f, 0.9f,   8.0f, 45.0f);

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(affineTransformEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="5c4d7-122">Dieser Vorgang führt diesen Matrix Vorgang aus:</span><span class="sxs-lookup"><span data-stu-id="5c4d7-122">This effect performs this matrix operation:</span></span>

![affine Matrix Vorgang](images/affine-matrix-calculation.png)

<span data-ttu-id="5c4d7-124">Obwohl die Eingabe Matrix als 3 x 2-Matrix definiert ist, wird die letzte Spalte mit 0, 0 und 1 aufgefüllt, um eine quadratische Matrix zu bilden.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-124">Although the input matrix is defined as a 3x2 matrix, the last column is padded with 0, 0 and 1 to produce a square matrix.</span></span> <span data-ttu-id="5c4d7-125">Dies ermöglicht die Matrix Multiplikation, sodass Transformationen in eine einzelne Matrix verkettet werden können.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-125">This allows for matrix multiplication, so that transforms can be concatenated into a single matrix.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="5c4d7-126">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5c4d7-126">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c4d7-127">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="5c4d7-127">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="5c4d7-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c4d7-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5c4d7-129">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="5c4d7-129">InterpolationMode</span></span><br/> <span data-ttu-id="5c4d7-130">D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE</span><span class="sxs-lookup"><span data-stu-id="5c4d7-130">D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE</span></span><br/></td>
<td><span data-ttu-id="5c4d7-131">Der Interpolations Modus, der zum Skalieren des Bilds verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-131">The interpolation mode used to scale the image.</span></span> <span data-ttu-id="5c4d7-132">Es gibt sechs Skalierungs Modi mit hoher Qualität und Geschwindigkeit.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-132">There are 6 scale modes that range in quality and speed.</span></span><br/> <span data-ttu-id="5c4d7-133">Der Typ ist D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-133">Type is D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE.</span></span><br/> <span data-ttu-id="5c4d7-134">Der Standardwert ist D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-134">Default value is D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c4d7-135">Bordermode</span><span class="sxs-lookup"><span data-stu-id="5c4d7-135">BorderMode</span></span><br/> <span data-ttu-id="5c4d7-136">D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="5c4d7-136">D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="5c4d7-137">Der Modus, der verwendet wird, um den Rahmen des Bilds zu berechnen, weich oder hart.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-137">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="5c4d7-138">Weitere Informationen finden Sie unter <a href="https://www.bing.com/search?q=Border+modes">Border Modes</a> .</span><span class="sxs-lookup"><span data-stu-id="5c4d7-138">See <a href="https://www.bing.com/search?q=Border+modes">Border modes</a> for more info.</span></span> <br/> <span data-ttu-id="5c4d7-139">Der Typ ist D2D1_BORDER_MODE.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-139">Type is D2D1_BORDER_MODE.</span></span><br/> <span data-ttu-id="5c4d7-140">Der Standardwert ist D2D1_BORDER_MODE_SOFT.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-140">Default value is D2D1_BORDER_MODE_SOFT.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c4d7-141">TransformMatrix</span><span class="sxs-lookup"><span data-stu-id="5c4d7-141">TransformMatrix</span></span><br/> <span data-ttu-id="5c4d7-142">D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX</span><span class="sxs-lookup"><span data-stu-id="5c4d7-142">D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX</span></span><br/></td>
<td><span data-ttu-id="5c4d7-143">Die 3 x 2-Matrix zum Transformieren des Bilds mithilfe der Direct2D Matrix <a href="direct2d-transforms-overview.md">Transformation</a>.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-143">The 3x2 matrix to transform the image using the Direct2D matrix <a href="direct2d-transforms-overview.md">transform</a>.</span></span> <br/> <span data-ttu-id="5c4d7-144">Der Typ ist D2D1_MATRIX_3X2_F.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-144">Type is D2D1_MATRIX_3X2_F.</span></span><br/> <span data-ttu-id="5c4d7-145">Der Standardwert ist Matrix3x2F:: Identity ().</span><span class="sxs-lookup"><span data-stu-id="5c4d7-145">Default value is Matrix3x2F::Identity().</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c4d7-146">Schärfe</span><span class="sxs-lookup"><span data-stu-id="5c4d7-146">Sharpness</span></span><br/> <span data-ttu-id="5c4d7-147">D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS</span><span class="sxs-lookup"><span data-stu-id="5c4d7-147">D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS</span></span><br/></td>
<td><span data-ttu-id="5c4d7-148">Im hochwertigen kubischen Interpolations Modus ist die Schärfe des Skalierungs Filters ein Gleit Komma Wert zwischen 0 und 1.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-148">In the high quality cubic interpolation mode, the sharpness level of the scaling filter as a float between 0 and 1.</span></span> <span data-ttu-id="5c4d7-149">Die Werte sind unitless.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-149">The values are unitless.</span></span> <span data-ttu-id="5c4d7-150">Mit der Schärfe können Sie die Qualität eines Bilds anpassen, wenn Sie das Bild skalieren.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-150">You can use sharpness to adjust the quality of an image when you scale the image.</span></span><br/> <span data-ttu-id="5c4d7-151">Der Schärfe Faktor wirkt sich auf die Form des Kernels aus.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-151">The sharpness factor affects the shape of the kernel.</span></span> <span data-ttu-id="5c4d7-152">Je höher der Schärfe Faktor, desto kleiner der Kernel.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-152">The higher the sharpness factor, the smaller the kernel.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5c4d7-153">Diese Eigenschaft wirkt sich nur auf den hochwertigen kubischen Interpolations Modus aus.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-153">This property affects only the high quality cubic interpolation mode.</span></span>
</blockquote>
<br/> <span data-ttu-id="5c4d7-154">Der Typ ist "float".</span><span class="sxs-lookup"><span data-stu-id="5c4d7-154">Type is FLOAT.</span></span><br/> <span data-ttu-id="5c4d7-155">Der Standardwert ist 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-155">Default value is 1.0f.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="border-modes"></a><span data-ttu-id="5c4d7-156">Rahmen Modi</span><span class="sxs-lookup"><span data-stu-id="5c4d7-156">Border modes</span></span>



| <span data-ttu-id="5c4d7-157">Name</span><span class="sxs-lookup"><span data-stu-id="5c4d7-157">Name</span></span>                     | <span data-ttu-id="5c4d7-158">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c4d7-158">Description</span></span>                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c4d7-159">D2D1 \_ Border \_ Mode \_ Soft</span><span class="sxs-lookup"><span data-stu-id="5c4d7-159">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="5c4d7-160">Der Effekt füllt das Bild mit transparenten schwarzen Pixeln, während es interpoliert, was zu einem weichen Rand führt.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-160">The effect pads the image with transparent black pixels as it interpolates, resulting in a soft edge.</span></span><br/> |
| <span data-ttu-id="5c4d7-161">D2D1 \_ Rahmen \_ Modus \_ hart</span><span class="sxs-lookup"><span data-stu-id="5c4d7-161">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="5c4d7-162">Der Effekt bindet die Ausgabe an die Größe des Eingabe Bilds.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-162">The effect clamps the output to the size of the input image.</span></span> <br/>                                         |



 

## <a name="interpolation-modes"></a><span data-ttu-id="5c4d7-163">Interpolations Modi</span><span class="sxs-lookup"><span data-stu-id="5c4d7-163">Interpolation modes</span></span>



| <span data-ttu-id="5c4d7-164">Enumeration</span><span class="sxs-lookup"><span data-stu-id="5c4d7-164">Enumeration</span></span>                                                         | <span data-ttu-id="5c4d7-165">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c4d7-165">Description</span></span>                                                                                                                                                                                          |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c4d7-166">D2D1 \_ 2daffinetransform- \_ Interpolations \_ Modus \_ Nächster \_ Nachbar</span><span class="sxs-lookup"><span data-stu-id="5c4d7-166">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="5c4d7-167">Verwendet den nächsten einzelnen Punkt und verwendet diesen.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-167">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="5c4d7-168">Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das niedrigste Qualitätsbild aus.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-168">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                                                           |
| <span data-ttu-id="5c4d7-169">D2D1 \_ 2daffinetransform- \_ Interpolations \_ Modus \_ linear</span><span class="sxs-lookup"><span data-stu-id="5c4d7-169">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="5c4d7-170">Verwendet ein vier-Punkt-Beispiel und eine lineare interpolung.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-170">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="5c4d7-171">Dieser Modus verwendet mehr Verarbeitungszeit als der nächstgelegene Nachbar Modus, gibt aber ein Image mit höherer Qualität aus.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-171">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span>                                           |
| <span data-ttu-id="5c4d7-172">D2D1 \_ 2daffinetransform- \_ Interpolations \_ Modus ( \_ kubisch)</span><span class="sxs-lookup"><span data-stu-id="5c4d7-172">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="5c4d7-173">Verwendet einen 16-beispielkubischen Kernel für Interpolationen.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-173">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="5c4d7-174">In diesem Modus wird die meiste Verarbeitungszeit verwendet, es wird jedoch ein Image mit höherer Qualität ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-174">This mode uses the most processing time, but outputs a higher quality image.</span></span>                                                                        |
| <span data-ttu-id="5c4d7-175">D2D1 \_ 2daffinetransform \_ Interpolations \_ Modus \_ \_ Multisample \_ linear</span><span class="sxs-lookup"><span data-stu-id="5c4d7-175">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="5c4d7-176">Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für eine gute Edge-Antialiasing.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-176">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="5c4d7-177">Dieser Modus eignet sich gut zum horizontalen Herunterskalieren um kleine Beträge in Bildern mit wenigen Pixeln.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-177">This mode is good for scaling down by small amounts on images with few pixels.</span></span>                                              |
| <span data-ttu-id="5c4d7-178">D2D1 \_ 2daffinetransform- \_ Interpolations \_ Modus \_ anisotrope</span><span class="sxs-lookup"><span data-stu-id="5c4d7-178">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="5c4d7-179">Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap zu modellieren.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-179">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                                                                     |
| <span data-ttu-id="5c4d7-180">D2D1 \_ 2daffinetransform \_ Interpolations \_ Modus \_ High \_ Quality \_ kubisch</span><span class="sxs-lookup"><span data-stu-id="5c4d7-180">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_HIGH\_QUALITY\_CUBIC</span></span>  | <span data-ttu-id="5c4d7-181">Verwendet einen kubischen Kernel mit hoher Qualität für eine Variable Größe, um das Abbild vorab zu skalieren, wenn eine downstreamingmatrix an der Transformationsmatrix beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-181">Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix.</span></span> <span data-ttu-id="5c4d7-182">Verwendet dann den kubischen Interpolations Modus für die endgültige Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-182">Then uses the cubic interpolation mode for the final output.</span></span> |



 

> [!Note]  
> <span data-ttu-id="5c4d7-183">Wenn Sie keinen Modus auswählen, wird der Effekt standardmäßig auf den D2D1 \_ 2daffinetransform- \_ Interpolations \_ Modus \_ linear.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-183">If you don't select a mode, the effect defaults to D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="5c4d7-184">Der anisotrope-Modus generiert bei der Skalierung Mipmaps. Wenn Sie jedoch die **zwischengespeicherte** Eigenschaft für die Effekte, die für diesen Effekt eingegeben werden, auf true festlegen, werden die Mipmaps bei ausreichend kleinen Bildern nicht jedes Mal generiert.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-184">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

## <a name="output-bitmap"></a><span data-ttu-id="5c4d7-185">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="5c4d7-185">Output bitmap</span></span>

<span data-ttu-id="5c4d7-186">Die Größe der Ausgabe Bitmap hängt von der Transformationsmatrix ab, die auf das Bild angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-186">The size of the output bitmap depends on the transform matrix that is applied to the image.</span></span>

<span data-ttu-id="5c4d7-187">Der Effekt führt den Transformations Vorgang aus und wendet dann ein Begrenzungs Rahmen um das Ergebnis an.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-187">The effect performs the transform operation and then applies a bounding box around the result.</span></span> <span data-ttu-id="5c4d7-188">Die Ausgabe Bitmap ist die Größe des umgebenden Felds.</span><span class="sxs-lookup"><span data-stu-id="5c4d7-188">The output bitmap is the size of the bounding box.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c4d7-189">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c4d7-189">Requirements</span></span>



| <span data-ttu-id="5c4d7-190">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c4d7-190">Requirement</span></span> | <span data-ttu-id="5c4d7-191">Wert</span><span class="sxs-lookup"><span data-stu-id="5c4d7-191">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5c4d7-192">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c4d7-192">Minimum supported client</span></span> | <span data-ttu-id="5c4d7-193">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c4d7-193">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="5c4d7-194">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c4d7-194">Minimum supported server</span></span> | <span data-ttu-id="5c4d7-195">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c4d7-195">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="5c4d7-196">Header</span><span class="sxs-lookup"><span data-stu-id="5c4d7-196">Header</span></span>                   | <span data-ttu-id="5c4d7-197">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="5c4d7-197">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="5c4d7-198">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5c4d7-198">Library</span></span>                  | <span data-ttu-id="5c4d7-199">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="5c4d7-199">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="5c4d7-200">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5c4d7-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c4d7-201">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="5c4d7-201">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

