---
title: Skalierungseffekt
description: Verwenden Sie diesen Effekt, um ein Bild nach oben oder unten zu skalieren. Der Effekt hat sechs Skalierungs Modi nächster Nachbar, linear, kubisch, Multisample linear, anisotrope und High Quality kubisch.
ms.assetid: 99DFA8DB-384B-4F64-90A2-0D3D7E1ACF27
keywords:
- Skalierungs Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3af77bc24db387fff0854e0432c270fa2ce6d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391830"
---
# <a name="scale-effect"></a><span data-ttu-id="ce7e6-105">Skalierungseffekt</span><span class="sxs-lookup"><span data-stu-id="ce7e6-105">Scale effect</span></span>

<span data-ttu-id="ce7e6-106">Verwenden Sie diesen Effekt, um ein Bild nach oben oder unten zu skalieren.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-106">Use this effect to scale an image up or down.</span></span> <span data-ttu-id="ce7e6-107">Der Effekt hat sechs Skalierungs Modi: nächster Nachbar, linear, kubisch, Multisample linear, anisotrope und High Quality kubisch.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-107">The effect has six scaling modes: nearest neighbor, linear, cubic, multi-sample linear, anisotropic, and high quality cubic.</span></span>

<span data-ttu-id="ce7e6-108">Die CLSID für diesen Effekt ist CLSID \_ D2D1Scale.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-108">The CLSID for this effect is CLSID\_D2D1Scale.</span></span>

-   [<span data-ttu-id="ce7e6-109">Beispiel Bild</span><span class="sxs-lookup"><span data-stu-id="ce7e6-109">Example image</span></span>](#example-image)
-   [<span data-ttu-id="ce7e6-110">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ce7e6-110">Effect properties</span></span>](#effect-properties)
    -   [<span data-ttu-id="ce7e6-111">Rahmen Modi</span><span class="sxs-lookup"><span data-stu-id="ce7e6-111">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="ce7e6-112">Interpolations Modi</span><span class="sxs-lookup"><span data-stu-id="ce7e6-112">Interpolation modes</span></span>](#interpolation-modes)
-   [<span data-ttu-id="ce7e6-113">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="ce7e6-113">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="ce7e6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce7e6-114">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="ce7e6-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ce7e6-115">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="ce7e6-116">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="ce7e6-116">Example image</span></span>

<span data-ttu-id="ce7e6-117">Dieses Beispiel zeigt, wie der Skalierungs Effekt in den 2fachen der Eingabe vergrößert wird und auf die ursprüngliche Größe zugreift.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-117">This example shows the scale effect zooming in 2 times the input and cropping to the original size.</span></span>



| <span data-ttu-id="ce7e6-118">Vorher</span><span class="sxs-lookup"><span data-stu-id="ce7e6-118">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg) |
| <span data-ttu-id="ce7e6-120">Nach</span><span class="sxs-lookup"><span data-stu-id="ce7e6-120">After</span></span>                                                      |
| ![das Bild nach der Transformation.](images/22-scale.png)     |



 


```C++
ComPtr<ID2D1Effect> scaleEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Scale, &scaleEffect);

scaleEffect->SetInput(0, bitmap);

scaleEffect->SetValue(D2D1_SCALE_PROP_CENTER_POINT, D2D1::Vector2F(256.0f, 192.0f));
scaleEffect->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(2.0f, 2.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(scaleEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="ce7e6-122">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ce7e6-122">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce7e6-123">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="ce7e6-123">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="ce7e6-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce7e6-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce7e6-125">Skalieren</span><span class="sxs-lookup"><span data-stu-id="ce7e6-125">Scale</span></span><br/> <span data-ttu-id="ce7e6-126">D2D1_SCALE_PROP_SCALE</span><span class="sxs-lookup"><span data-stu-id="ce7e6-126">D2D1_SCALE_PROP_SCALE</span></span><br/></td>
<td><span data-ttu-id="ce7e6-127">Der Skalierungs Betrag in der X-und Y-Richtung als Verhältnis zwischen der Ausgabegröße und der Eingabe Größe.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-127">The scale amount in the X and Y direction as a ratio of the output size to the input size.</span></span> <span data-ttu-id="ce7e6-128">Diese Eigenschaft ist eine D2D1_VECTOR_2Fdefined wie: (X Scale, Y Scale).</span><span class="sxs-lookup"><span data-stu-id="ce7e6-128">This property a D2D1_VECTOR_2Fdefined as: (X scale, Y scale).</span></span> <span data-ttu-id="ce7e6-129">Die Skalierungs Beträge sind float, unitless und müssen positiv oder 0 sein.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-129">The scale amounts are FLOAT, unitless, and must be positive or 0.</span></span><br/> <span data-ttu-id="ce7e6-130">Der Typ ist D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-130">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="ce7e6-131">Der Standardwert ist {1.0 f, 1.0 f}.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-131">The default value is {1.0f, 1.0f}.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce7e6-132">CenterPoint</span><span class="sxs-lookup"><span data-stu-id="ce7e6-132">CenterPoint</span></span><br/> <span data-ttu-id="ce7e6-133">D2D1_SCALE_PROP_CENTER_POINT</span><span class="sxs-lookup"><span data-stu-id="ce7e6-133">D2D1_SCALE_PROP_CENTER_POINT</span></span><br/></td>
<td><span data-ttu-id="ce7e6-134">Der Mittelpunkt der Bildskalierung.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-134">The image scaling center point.</span></span> <span data-ttu-id="ce7e6-135">Diese Eigenschaft ist eine D2D1_VECTOR_2F, die wie folgt definiert ist: (Punkt X, Punkt Y).</span><span class="sxs-lookup"><span data-stu-id="ce7e6-135">This property is a D2D1_VECTOR_2F defined as: (point X, point Y).</span></span> <span data-ttu-id="ce7e6-136">Die Einheiten befinden sich in Dips.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-136">The units are in DIPs.</span></span><br/> <span data-ttu-id="ce7e6-137">Verwenden Sie die Mittelpunkt Eigenschaft, um einen anderen Punkt als die linke obere Ecke zu skalieren.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-137">Use the center point property to scale around a point other than the upper-left corner.</span></span><br/> <span data-ttu-id="ce7e6-138">Der Typ ist D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-138">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="ce7e6-139">Der Standardwert ist {0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-139">The default value is {0.0f, 0.0f}.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce7e6-140">Bordermode</span><span class="sxs-lookup"><span data-stu-id="ce7e6-140">BorderMode</span></span><br/> <span data-ttu-id="ce7e6-141">D2D1_SCALE_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="ce7e6-141">D2D1_SCALE_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="ce7e6-142">Der Modus, der verwendet wird, um den Rahmen des Bilds zu berechnen, weich oder hart.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-142">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="ce7e6-143">Weitere Informationen finden Sie unter <a href="#border-modes">Border Modes</a> .</span><span class="sxs-lookup"><span data-stu-id="ce7e6-143">See <a href="#border-modes">Border modes</a> for more info.</span></span> <br/> <span data-ttu-id="ce7e6-144">Der Typ ist D2D1_BORDER_MODE.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-144">The type is D2D1_BORDER_MODE.</span></span><br/> <span data-ttu-id="ce7e6-145">Der Standardwert ist D2D1_BORDER_MODE_SOFT.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-145">The default value is D2D1_BORDER_MODE_SOFT.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce7e6-146">Schärfe</span><span class="sxs-lookup"><span data-stu-id="ce7e6-146">Sharpness</span></span><br/> <span data-ttu-id="ce7e6-147">D2D1_SCALE_PROP_SHARPNESS</span><span class="sxs-lookup"><span data-stu-id="ce7e6-147">D2D1_SCALE_PROP_SHARPNESS</span></span><br/></td>
<td><span data-ttu-id="ce7e6-148">Im hochwertigen kubischen Interpolations Modus ist die Schärfe des Skalierungs Filters ein Gleit Komma Wert zwischen 0 und 1.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-148">In the high quality cubic interpolation mode, the sharpness level of the scaling filter as a float between 0 and 1.</span></span> <span data-ttu-id="ce7e6-149">Die Werte sind unitless.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-149">The values are unitless.</span></span> <span data-ttu-id="ce7e6-150">Mit der Schärfe können Sie die Qualität eines Bilds anpassen, wenn Sie das Bild nach unten skalieren.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-150">You can use sharpness to adjust the quality of an image when you scale the image down.</span></span><br/> <span data-ttu-id="ce7e6-151">Der Schärfe Faktor wirkt sich auf die Form des Kernels aus.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-151">The sharpness factor affects the shape of the kernel.</span></span> <span data-ttu-id="ce7e6-152">Je höher der Schärfe Faktor, desto kleiner der Kernel.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-152">The higher the sharpness factor, the smaller the kernel.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ce7e6-153">Diese Eigenschaft wirkt sich nur auf den hochwertigen kubischen Interpolations Modus aus.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-153">This property affects only the high quality cubic interpolation mode.</span></span>
</blockquote>
<br/> <span data-ttu-id="ce7e6-154">Der Typ ist "float".</span><span class="sxs-lookup"><span data-stu-id="ce7e6-154">The type is FLOAT.</span></span><br/> <span data-ttu-id="ce7e6-155">Der Standardwert ist 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-155">The default value is 0.0f.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce7e6-156">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="ce7e6-156">InterpolationMode</span></span><br/> <span data-ttu-id="ce7e6-157">D2D1_SCALE_PROP_INTERPOLATION_MODE</span><span class="sxs-lookup"><span data-stu-id="ce7e6-157">D2D1_SCALE_PROP_INTERPOLATION_MODE</span></span><br/></td>
<td><span data-ttu-id="ce7e6-158">Der Interpolations Modus, den der Effekt zum Skalieren des Bilds verwendet.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-158">The interpolation mode the effect uses to scale the image.</span></span> <span data-ttu-id="ce7e6-159">Es gibt sechs Skalierungs Modi mit hoher Qualität und Geschwindigkeit.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-159">There are 6 scale modes that range in quality and speed.</span></span> <span data-ttu-id="ce7e6-160">Weitere Informationen finden Sie unter <a href="#interpolation-modes">Interpolations Modi</a> .</span><span class="sxs-lookup"><span data-stu-id="ce7e6-160">See <a href="#interpolation-modes">Interpolation modes</a> for more info.</span></span> <br/> <span data-ttu-id="ce7e6-161">Der Typ ist D2D1_SCALE_INTERPOLATION_MODE.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-161">The type is D2D1_SCALE_INTERPOLATION_MODE.</span></span><br/> <span data-ttu-id="ce7e6-162">Der Standardwert ist D2D1_SCALE_INTERPOLATION_MODE_LINEAR.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-162">The default value is D2D1_SCALE_INTERPOLATION_MODE_LINEAR.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="border-modes"></a><span data-ttu-id="ce7e6-163">Rahmen Modi</span><span class="sxs-lookup"><span data-stu-id="ce7e6-163">Border modes</span></span>



| <span data-ttu-id="ce7e6-164">Name</span><span class="sxs-lookup"><span data-stu-id="ce7e6-164">Name</span></span>                     | <span data-ttu-id="ce7e6-165">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce7e6-165">Description</span></span>                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce7e6-166">D2D1 \_ Border \_ Mode \_ Soft</span><span class="sxs-lookup"><span data-stu-id="ce7e6-166">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="ce7e6-167">Der Effekt füllt das Eingabebild mit transparenten schwarzen Pixeln für Stichproben außerhalb der Eingabe Grenzen auf, wenn es den zuordnerkerntyp anwendet.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-167">The effect pads the input image with transparent black pixels for samples outside of the input bounds when it applies the convolution kernel.</span></span> <span data-ttu-id="ce7e6-168">Dadurch wird ein weicher Edge für das Bild erstellt, und im Prozess wird die Ausgabe Bitmap um die Größe des Kernels erweitert.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-168">This creates a soft edge for the image, and in the process expands the output bitmap by the size of the kernel.</span></span><br/> |
| <span data-ttu-id="ce7e6-169">D2D1 \_ Rahmen \_ Modus \_ hart</span><span class="sxs-lookup"><span data-stu-id="ce7e6-169">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="ce7e6-170">Die Auswirkung erweitert das Eingabebild durch eine Spiegelungs Typen-Rahmen Transformation für Beispiele außerhalb der Eingabe Grenzen.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-170">The effect extends the input image with a mirror-type border transform for samples outside of the input bounds.</span></span> <span data-ttu-id="ce7e6-171">Die Größe der Ausgabe Bitmap entspricht der Größe der Eingabe Bitmap.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-171">The size of the output bitmap is equal to the size of the input bitmap.</span></span><br/>                                                                       |



 

\`

## <a name="interpolation-modes"></a><span data-ttu-id="ce7e6-172">Interpolations Modi</span><span class="sxs-lookup"><span data-stu-id="ce7e6-172">Interpolation modes</span></span>



| <span data-ttu-id="ce7e6-173">Enumeration</span><span class="sxs-lookup"><span data-stu-id="ce7e6-173">Enumeration</span></span>                                             | <span data-ttu-id="ce7e6-174">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce7e6-174">Description</span></span>                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce7e6-175">D2D1 \_ Scale \_ Interpolations \_ Modus \_ Nächster \_ Nachbar</span><span class="sxs-lookup"><span data-stu-id="ce7e6-175">D2D1\_SCALE\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="ce7e6-176">Verwendet den nächsten einzelnen Punkt und verwendet diesen.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-176">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="ce7e6-177">Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das niedrigste Qualitätsbild aus.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-177">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                                                           |
| <span data-ttu-id="ce7e6-178">D2D1 \_ - \_ Interpolations \_ Modus \_ linear</span><span class="sxs-lookup"><span data-stu-id="ce7e6-178">D2D1\_SCALE\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="ce7e6-179">Verwendet ein vier-Punkt-Beispiel und eine lineare interpolung.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-179">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="ce7e6-180">Dieser Modus verwendet mehr Verarbeitungszeit als der nächstgelegene Nachbar Modus, gibt aber ein Image mit höherer Qualität aus.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-180">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span>                                           |
| <span data-ttu-id="ce7e6-181">D2D1 \_ - \_ Skalierungs Modus für Interpolations \_ Modus \_</span><span class="sxs-lookup"><span data-stu-id="ce7e6-181">D2D1\_SCALE\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="ce7e6-182">Verwendet einen 16-beispielkubischen Kernel für Interpolationen.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-182">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="ce7e6-183">In diesem Modus wird die meiste Verarbeitungszeit verwendet, es wird jedoch ein Image mit höherer Qualität ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-183">This mode uses the most processing time, but outputs a higher quality image.</span></span>                                                                        |
| <span data-ttu-id="ce7e6-184">D2D1 \_ Scale \_ Interpolations \_ Modus \_ \_ Multisample \_ linear</span><span class="sxs-lookup"><span data-stu-id="ce7e6-184">D2D1\_SCALE\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="ce7e6-185">Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für eine gute Edge-Antialiasing.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-185">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="ce7e6-186">Dieser Modus eignet sich gut zum horizontalen Herunterskalieren um kleine Beträge in Bildern mit wenigen Pixeln.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-186">This mode is good for scaling down by small amounts on images with few pixels.</span></span>                                              |
| <span data-ttu-id="ce7e6-187">D2D1 \_ Scale \_ Interpolations \_ Modus \_ anisotrope</span><span class="sxs-lookup"><span data-stu-id="ce7e6-187">D2D1\_SCALE\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="ce7e6-188">Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap zu modellieren.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-188">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                                                                     |
| <span data-ttu-id="ce7e6-189">D2D1 \_ Scale- \_ Interpolations \_ Modus \_ High \_ Quality \_ kubisch</span><span class="sxs-lookup"><span data-stu-id="ce7e6-189">D2D1\_SCALE\_INTERPOLATION\_MODE\_HIGH\_QUALITY\_CUBIC</span></span>  | <span data-ttu-id="ce7e6-190">Verwendet einen kubischen Kernel mit hoher Qualität für eine Variable Größe, um das Abbild vorab zu skalieren, wenn eine downstreamingmatrix an der Transformationsmatrix beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-190">Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix.</span></span> <span data-ttu-id="ce7e6-191">Verwendet dann den kubischen Interpolations Modus für die endgültige Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-191">Then uses the cubic interpolation mode for the final output.</span></span> |



 

> [!Note]  
> <span data-ttu-id="ce7e6-192">Wenn Sie keinen Modus auswählen, wird der Effekt standardmäßig auf den D2D1 \_ Scale \_ Interpolations \_ Modus \_ linear.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-192">If you don't select a mode, the effect defaults to D2D1\_SCALE\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="ce7e6-193">Der anisotrope-Modus generiert bei der Skalierung Mipmaps. Wenn Sie jedoch die **zwischengespeicherte** Eigenschaft für die Effekte, die für diesen Effekt eingegeben werden, auf true festlegen, werden die Mipmaps bei ausreichend kleinen Bildern nicht jedes Mal generiert.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-193">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

## <a name="output-bitmap"></a><span data-ttu-id="ce7e6-194">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="ce7e6-194">Output bitmap</span></span>

<span data-ttu-id="ce7e6-195">Der Speicherort und die Größe der Ausgabe Bitmap sind abhängig vom angegebenen Skalierungsfaktor und dem Mittelpunkt.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-195">The location and size of the output bitmap depends on the specified scale factor and the center point.</span></span>

<span data-ttu-id="ce7e6-196">Mit dieser Formel können Sie die Größe der Ausgabe Bitmap berechnen:</span><span class="sxs-lookup"><span data-stu-id="ce7e6-196">You can calculate the size of the output bitmap using this equation:</span></span><dl> <span data-ttu-id="ce7e6-197">Bitmapsize? (Pixel) = Skalieren? \* Ursprüngliche Bitmapgröße?</span><span class="sxs-lookup"><span data-stu-id="ce7e6-197">BitmapSize?(Pixels)=Scale?\*Original Bitmap Size?</span></span> <span data-ttu-id="ce7e6-198">(Dips) \* (Userdpi/96)</span><span class="sxs-lookup"><span data-stu-id="ce7e6-198">(DIPs)\*(UserDPI/96)</span></span>  
<span data-ttu-id="ce7e6-199">Bitmapsize<sub>y</sub>(Pixel) =<sub>y</sub> \* ursprüngliche Bitmapgröße skalieren<sub>y</sub> (Dips) \* (userdpi/96)</span><span class="sxs-lookup"><span data-stu-id="ce7e6-199">BitmapSize<sub>y</sub>(Pixels)=Scale<sub>y</sub>\*Original Bitmap Size<sub>y</sub> (DIPs)\*(UserDPI/96)</span></span>  
</dl>

<span data-ttu-id="ce7e6-200">Der Effekt rundet Bruchteile von Pixeln auf das nächste ganze Pixel ab.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-200">The effect rounds fractions of pixels up to the nearest whole pixel.</span></span>

<span data-ttu-id="ce7e6-201">Der Speicherort der Bitmap ist (0,0) oder der Wert der Mittelpunkt Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ce7e6-201">The location of the bitmap is (0, 0) or the value of the center point property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce7e6-202">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce7e6-202">Requirements</span></span>



| <span data-ttu-id="ce7e6-203">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce7e6-203">Requirement</span></span> | <span data-ttu-id="ce7e6-204">Wert</span><span class="sxs-lookup"><span data-stu-id="ce7e6-204">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ce7e6-205">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce7e6-205">Minimum supported client</span></span> | <span data-ttu-id="ce7e6-206">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce7e6-206">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ce7e6-207">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce7e6-207">Minimum supported server</span></span> | <span data-ttu-id="ce7e6-208">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce7e6-208">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ce7e6-209">Header</span><span class="sxs-lookup"><span data-stu-id="ce7e6-209">Header</span></span>                   | <span data-ttu-id="ce7e6-210">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="ce7e6-210">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="ce7e6-211">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ce7e6-211">Library</span></span>                  | <span data-ttu-id="ce7e6-212">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="ce7e6-212">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="ce7e6-213">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ce7e6-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce7e6-214">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="ce7e6-214">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

