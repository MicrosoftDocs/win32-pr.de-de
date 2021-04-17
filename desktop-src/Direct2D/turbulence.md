---
title: Turbulenzen Effekt
description: Verwenden Sie den Turbulenz Effekt, um eine Bitmap basierend auf der Perlin-Rausch Funktion zu generieren.
ms.assetid: 86C1990E-958C-46D7-840A-E4A17F1D1740
keywords:
- Turbulenzen Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f67f615ec5b68ca285a048b68bc7bc8eab6e24
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104565902"
---
# <a name="turbulence-effect"></a><span data-ttu-id="0b17c-104">Turbulenzen Effekt</span><span class="sxs-lookup"><span data-stu-id="0b17c-104">Turbulence effect</span></span>

<span data-ttu-id="0b17c-105">Verwenden Sie den Turbulenz Effekt, um eine Bitmap basierend auf der Perlin-Rausch Funktion zu generieren.</span><span class="sxs-lookup"><span data-stu-id="0b17c-105">Use the turbulence effect to generate a bitmap based on the Perlin noise function.</span></span>

<span data-ttu-id="0b17c-106">Der Turbulenz Effekt hat kein Eingabebild.</span><span class="sxs-lookup"><span data-stu-id="0b17c-106">The turbulence effect has no input image.</span></span>

<span data-ttu-id="0b17c-107">Die CLSID für diesen Effekt ist CLSID \_ D2D1Turbulence.</span><span class="sxs-lookup"><span data-stu-id="0b17c-107">The CLSID for this effect is CLSID\_D2D1Turbulence.</span></span>

-   [<span data-ttu-id="0b17c-108">Beispiel Bild</span><span class="sxs-lookup"><span data-stu-id="0b17c-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="0b17c-109">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0b17c-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="0b17c-110">Rausch Modi</span><span class="sxs-lookup"><span data-stu-id="0b17c-110">Noise modes</span></span>](#noise-modes)
-   [<span data-ttu-id="0b17c-111">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="0b17c-111">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="0b17c-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b17c-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="0b17c-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0b17c-113">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="0b17c-114">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="0b17c-114">Example image</span></span>

![ein Screenshot mit dem Effekt Beispiel zeigt die Ausgabe des Turbulenzen Effekts.](images/32-turbulence.png)

<span data-ttu-id="0b17c-116">Der Turbulenz Effekt berechnet die Summe von einem oder mehreren Oktaven der Perlin-Rausch Funktion.</span><span class="sxs-lookup"><span data-stu-id="0b17c-116">The Turbulence effect computes the sum of one or more octaves of the Perlin noise function.</span></span> <span data-ttu-id="0b17c-117">Perlin-Rauschen ist eine pseudo zufällige Funktion, deren Wert von der Häufigkeit, der Position und dem Ausgangswert abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="0b17c-117">Perlin noise is a pseudo-random function whose value depends on the frequency, position, and seed value.</span></span> <span data-ttu-id="0b17c-118">Der Effekt generiert die RGBA-Werte mithilfe einer dieser Gleichungen.</span><span class="sxs-lookup"><span data-stu-id="0b17c-118">The effect generates the RGBA values using one of these equations.</span></span>

<span data-ttu-id="0b17c-119">Wenn Sie das D2D1- \_ Turbulenz Rauschen-Summen-Summen Füll Modus auswählen, wird \_ \_ \_ diese Gleichung verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b17c-119">If you select the D2D1\_TURBULENCE\_NOISE\_FRACTAL\_SUM noise mode the effect uses this equation.</span></span>

![Screenshot, der die zum Generieren einer Bitmap verwendete "Turbulence"-Funktion anzeigt.](images/turbulence-equation1.png)

<span data-ttu-id="0b17c-121">Wenn Sie den \_ Rausch Modus D2D1 Turbulenz Rauschen auswählen, wird \_ \_ diese Gleichung verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b17c-121">If you select the D2D1\_TURBULENCE\_NOISE\_TURBULENCE noise mode the effect uses this equation.</span></span>

![die zum Generieren einer Bitmap verwendete "Turbulence"-Funktion.](images/turbulence-equation2.png)

> [!Note]  
> <span data-ttu-id="0b17c-123">Die `PerlinNoise` -Funktion hat einen Bereich von \[ -1, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="0b17c-123">The `PerlinNoise` function has a range of \[-1, 1\].</span></span>

 

<span data-ttu-id="0b17c-124">Dieser Effekt gibt Pixelwerte in einem prämultiplizierten Alpha aus.</span><span class="sxs-lookup"><span data-stu-id="0b17c-124">This effect outputs pixel values in premultiplied alpha.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="0b17c-125">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0b17c-125">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0b17c-126">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="0b17c-126">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="0b17c-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b17c-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0b17c-128">Offset</span><span class="sxs-lookup"><span data-stu-id="0b17c-128">Offset</span></span><br/> <span data-ttu-id="0b17c-129">D2D1_TURBULENCE_PROP_OFFSET</span><span class="sxs-lookup"><span data-stu-id="0b17c-129">D2D1_TURBULENCE_PROP_OFFSET</span></span><br/></td>
<td><span data-ttu-id="0b17c-130">Die Koordinaten, an denen die Turbulenzen ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0b17c-130">The coordinates where the turbulence output is generated.</span></span><br/> <span data-ttu-id="0b17c-131">Der Algorithmus, der zum Generieren des Perlin-Rauschens verwendet wird, ist Positions abhängig, sodass ein anderer Offset eine andere Ausgabe ergibt.</span><span class="sxs-lookup"><span data-stu-id="0b17c-131">The algorithm used to generate the Perlin noise is position dependent, so a different offset results in a different output.</span></span> <span data-ttu-id="0b17c-132">Diese Eigenschaft ist nicht gebunden, und die Einheiten werden in Dips angegeben.</span><span class="sxs-lookup"><span data-stu-id="0b17c-132">This property is not bounded and the units are specified in DIPs</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="0b17c-133">Der Offset hat nicht denselben Effekt wie eine Übersetzung, weil die Rausch funktionsausgabe unendlich ist und die Funktion die Kachel umschließt.</span><span class="sxs-lookup"><span data-stu-id="0b17c-133">The offset does not have the same effect as a translation because the noise function output is infinite and the function will wrap around the tile.</span></span>
</blockquote>
<br/> <span data-ttu-id="0b17c-134">Der Typ ist D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="0b17c-134">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="0b17c-135">Der Standardwert ist {0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="0b17c-135">The default value is {0.0f, 0.0f}.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b17c-136">Size</span><span class="sxs-lookup"><span data-stu-id="0b17c-136">Size</span></span><br/> <span data-ttu-id="0b17c-137">D2D1_TURBULENCE_PROP_SIZE</span><span class="sxs-lookup"><span data-stu-id="0b17c-137">D2D1_TURBULENCE_PROP_SIZE</span></span><br/></td>
<td><span data-ttu-id="0b17c-138">Die Größe der Turbulenz Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="0b17c-138">The size of the turbulence output.</span></span><br/> <span data-ttu-id="0b17c-139">Diese Eigenschaft ist nicht gebunden, und die Einheiten werden in Dips angegeben.</span><span class="sxs-lookup"><span data-stu-id="0b17c-139">This property is not bounded and the units are specified in DIPs</span></span> <br/>
<br/> <span data-ttu-id="0b17c-140">Der Typ ist D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="0b17c-140">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="0b17c-141">Der Standardwert ist {0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="0b17c-141">The default value is {0.0f, 0.0f}.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b17c-142">Basefrequency</span><span class="sxs-lookup"><span data-stu-id="0b17c-142">BaseFrequency</span></span><br/> <span data-ttu-id="0b17c-143">D2D1_TURBULENCE_PROP_BASE_FREQUENCY</span><span class="sxs-lookup"><span data-stu-id="0b17c-143">D2D1_TURBULENCE_PROP_BASE_FREQUENCY</span></span><br/></td>
<td><span data-ttu-id="0b17c-144">Die Basis Frequenzen in der X-und Y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="0b17c-144">The base frequencies in the X and Y direction.</span></span> <span data-ttu-id="0b17c-145">Diese Eigenschaft ist ein float-Wert und muss größer als 0 sein.</span><span class="sxs-lookup"><span data-stu-id="0b17c-145">This property is a float and must be greater than 0.</span></span> <span data-ttu-id="0b17c-146">Die Einheiten werden in 1/Dips angegeben.</span><span class="sxs-lookup"><span data-stu-id="0b17c-146">The units are specified in 1/DIPs.</span></span> <br/> <span data-ttu-id="0b17c-147">Der Wert 1 (1/Dips) für die Basisfrequenz führt dazu, dass der Perlin-Rausch einen gesamten Zeitraum zwischen zwei Pixeln vervollständigt.</span><span class="sxs-lookup"><span data-stu-id="0b17c-147">A value of 1 (1/DIPs) for the base frequency results in the Perlin noise completing an entire cycle between two pixels.</span></span> <span data-ttu-id="0b17c-148">Die einfache Interpolation für diese Pixel ergibt vollständig zufällige Pixel, da es keine Korrelation zwischen den Pixeln gibt.</span><span class="sxs-lookup"><span data-stu-id="0b17c-148">The ease interpolation for these pixels results in completely random pixels, since there is no correlation between the pixels.</span></span><br/> <span data-ttu-id="0b17c-149">Der Wert 0,1 (1/Dips) für die Basisfrequenz wiederholt die Perlin-Rausch Funktion alle 10 Dips.</span><span class="sxs-lookup"><span data-stu-id="0b17c-149">A value of 0.1(1/DIPs) for the base frequency, the Perlin noise function repeats every 10 DIPs.</span></span> <span data-ttu-id="0b17c-150">Dies führt zu einer Korrelation zwischen Pixeln, und der typische Turbulenz Effekt ist sichtbar.</span><span class="sxs-lookup"><span data-stu-id="0b17c-150">This results in correlation between pixels and the typical turbulence effect is visible.</span></span><br/> <span data-ttu-id="0b17c-151">Der Typ ist D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="0b17c-151">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="0b17c-152">Der Standardwert ist {0,01 f, 0,01 f}.</span><span class="sxs-lookup"><span data-stu-id="0b17c-152">The default value is {0.01f, 0.01f}.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b17c-153">Numuctaves</span><span class="sxs-lookup"><span data-stu-id="0b17c-153">NumOctaves</span></span><br/> <span data-ttu-id="0b17c-154">D2D1_TURBULENCE_PROP_NUM_OCTAVES</span><span class="sxs-lookup"><span data-stu-id="0b17c-154">D2D1_TURBULENCE_PROP_NUM_OCTAVES</span></span><br/></td>
<td><span data-ttu-id="0b17c-155">Die Anzahl der Oktaven für die Rausch Funktion.</span><span class="sxs-lookup"><span data-stu-id="0b17c-155">The number of octaves for the noise function.</span></span> <span data-ttu-id="0b17c-156">Diese Eigenschaft ist ein UInt32 und muss größer als 0 sein.</span><span class="sxs-lookup"><span data-stu-id="0b17c-156">This property is a UINT32 and must be greater than 0.</span></span><br/> <span data-ttu-id="0b17c-157">Der Typ ist "UInt32".</span><span class="sxs-lookup"><span data-stu-id="0b17c-157">The type is UINT32.</span></span><br/> <span data-ttu-id="0b17c-158">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="0b17c-158">The default value is 1.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b17c-159">Seed</span><span class="sxs-lookup"><span data-stu-id="0b17c-159">Seed</span></span><br/> <span data-ttu-id="0b17c-160">D2D1_TURBULENCE_PROP_SEED</span><span class="sxs-lookup"><span data-stu-id="0b17c-160">D2D1_TURBULENCE_PROP_SEED</span></span><br/></td>
<td><span data-ttu-id="0b17c-161">Der Seed für den Pseudo Zufallsgenerator.</span><span class="sxs-lookup"><span data-stu-id="0b17c-161">The seed for the pseudo random generator.</span></span> <span data-ttu-id="0b17c-162">Diese Eigenschaft ist unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="0b17c-162">This property is unbounded.</span></span><br/> <span data-ttu-id="0b17c-163">Der Typ ist "UInt32".</span><span class="sxs-lookup"><span data-stu-id="0b17c-163">The type is UINT32.</span></span><br/> <span data-ttu-id="0b17c-164">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="0b17c-164">The default value is 0.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b17c-165">Stördatenverkehr</span><span class="sxs-lookup"><span data-stu-id="0b17c-165">Noise</span></span><br/> <span data-ttu-id="0b17c-166">D2D1_TURBULENCE_PROP_NOISE</span><span class="sxs-lookup"><span data-stu-id="0b17c-166">D2D1_TURBULENCE_PROP_NOISE</span></span><br/></td>
<td><span data-ttu-id="0b17c-167">Der Turbulenz Füll Modus.</span><span class="sxs-lookup"><span data-stu-id="0b17c-167">The turbulence noise mode.</span></span> <span data-ttu-id="0b17c-168">Diese Eigenschaft kann entweder eine Dezimal-oder eine <em>Bruch</em> Zahl <em>sein.</em></span><span class="sxs-lookup"><span data-stu-id="0b17c-168">This property can be either <em>fractal sum</em> or <em>turbulence</em>.</span></span> <span data-ttu-id="0b17c-169">Gibt an, ob eine Bitmap auf der Grundlage von Dezimal Geräuschen oder der Turbulence-Funktion generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b17c-169">Indicates whether to generate a bitmap based on Fractal Noise or the Turbulence function.</span></span> <span data-ttu-id="0b17c-170">Weitere Informationen finden Sie unter <a href="#noise-modes">Rausch Modi</a> .</span><span class="sxs-lookup"><span data-stu-id="0b17c-170">See <a href="#noise-modes">Noise modes</a> for more info.</span></span> <br/> <span data-ttu-id="0b17c-171">Der Typ ist D2D1_TURBULENCE_NOISE.</span><span class="sxs-lookup"><span data-stu-id="0b17c-171">The type is D2D1_TURBULENCE_NOISE.</span></span><br/> <span data-ttu-id="0b17c-172">Der Standardwert ist D2D1_TURBULENCE_NOISE_FRACTAL_SUM.</span><span class="sxs-lookup"><span data-stu-id="0b17c-172">The default value is D2D1_TURBULENCE_NOISE_FRACTAL_SUM.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b17c-173">Stitchable</span><span class="sxs-lookup"><span data-stu-id="0b17c-173">Stitchable</span></span><br/> <span data-ttu-id="0b17c-174">D2D1_TURBULENCE_PROP_STITCHABLE</span><span class="sxs-lookup"><span data-stu-id="0b17c-174">D2D1_TURBULENCE_PROP_STITCHABLE</span></span><br/></td>
<td><span data-ttu-id="0b17c-175">Schaltet die zusammen Fügung ein oder aus.</span><span class="sxs-lookup"><span data-stu-id="0b17c-175">Turns stitching on or off.</span></span> <span data-ttu-id="0b17c-176">Die Basisfrequenz wird so angepasst, dass die Ausgabe Bitmap angeheftet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0b17c-176">The base frequency is adjusted so that output bitmap can be stitched.</span></span> <span data-ttu-id="0b17c-177">Dies ist hilfreich, wenn Sie mehrere Kopien der Ausgabe des Turbulenz Effekts Kacheln möchten.</span><span class="sxs-lookup"><span data-stu-id="0b17c-177">This is useful if you want to tile multiple copies of the turbulence effect output.</span></span>
<ul>
<li><span data-ttu-id="0b17c-178">True: die Ausgabe Bitmap kann (mit dem Kachel Effekt) ohne das Aussehen von Nähten gekachelt werden.</span><span class="sxs-lookup"><span data-stu-id="0b17c-178">True   The output bitmap can be tiled (using the tile effect) without the appearance of seams.</span></span> <span data-ttu-id="0b17c-179">Die Basisfrequenz wird so angepasst, dass die Ausgabe Bitmap angeheftet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0b17c-179">The base frequency is adjusted so that output bitmap can be stitched.</span></span></li>
<li><span data-ttu-id="0b17c-180">False: die Basisfrequenz wird nicht angepasst, sodass die Nähte zwischen den Kacheln auftreten können, wenn die Bitmap gekachelt ist.</span><span class="sxs-lookup"><span data-stu-id="0b17c-180">False   The base frequency is not adjusted, so seams may appear between tiles if the bitmap is tiled.</span></span></li>
</ul>
<br/> <span data-ttu-id="0b17c-181">Der Typ ist "bool".</span><span class="sxs-lookup"><span data-stu-id="0b17c-181">The type is BOOL.</span></span><br/> <span data-ttu-id="0b17c-182">Der Standardwert ist FALSE.</span><span class="sxs-lookup"><span data-stu-id="0b17c-182">The default value is FALSE.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="noise-modes"></a><span data-ttu-id="0b17c-183">Rausch Modi</span><span class="sxs-lookup"><span data-stu-id="0b17c-183">Noise modes</span></span>



| <span data-ttu-id="0b17c-184">Enumeration</span><span class="sxs-lookup"><span data-stu-id="0b17c-184">Enumeration</span></span>                           | <span data-ttu-id="0b17c-185">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b17c-185">Description</span></span>                                                                           |
|---------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b17c-186">D2D1 \_ Turbulenz Rauschen-Dezimalstellen \_ \_ \_ Summe</span><span class="sxs-lookup"><span data-stu-id="0b17c-186">D2D1\_TURBULENCE\_NOISE\_FRACTAL\_SUM</span></span> | <span data-ttu-id="0b17c-187">Berechnet eine Summe der Oktaven und verschiebt den Ausgabebereich von \[ -1, 1 \] in \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="0b17c-187">Computes a sum of the octaves, shifting the output range from \[-1, 1\], to \[0, 1\].</span></span> |
| <span data-ttu-id="0b17c-188">D2D1- \_ Turbulenzen \_ Rauschen- \_ Turbulenzen</span><span class="sxs-lookup"><span data-stu-id="0b17c-188">D2D1\_TURBULENCE\_NOISE\_TURBULENCE</span></span>   | <span data-ttu-id="0b17c-189">Berechnet eine Summe des absoluten Werts jeder Oktave.</span><span class="sxs-lookup"><span data-stu-id="0b17c-189">Computes a sum of the absolute value of each octave.</span></span>                                  |



 

> [!Note]  
> <span data-ttu-id="0b17c-190">Keiner der Modi enthält eine explizite Klammer der Ausgabewerte.</span><span class="sxs-lookup"><span data-stu-id="0b17c-190">Neither mode contains an explicit clamp of the output values.</span></span>

 

## <a name="output-bitmap"></a><span data-ttu-id="0b17c-191">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="0b17c-191">Output bitmap</span></span>

<span data-ttu-id="0b17c-192">Dieser Effekt generiert eine Bitmap mit logischer unbegrenzter groß.</span><span class="sxs-lookup"><span data-stu-id="0b17c-192">This effect generates a logically infinite sized bitmap.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b17c-193">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b17c-193">Requirements</span></span>



| <span data-ttu-id="0b17c-194">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b17c-194">Requirement</span></span> | <span data-ttu-id="0b17c-195">Wert</span><span class="sxs-lookup"><span data-stu-id="0b17c-195">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0b17c-196">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0b17c-196">Minimum supported client</span></span> | <span data-ttu-id="0b17c-197">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b17c-197">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="0b17c-198">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0b17c-198">Minimum supported server</span></span> | <span data-ttu-id="0b17c-199">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b17c-199">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="0b17c-200">Header</span><span class="sxs-lookup"><span data-stu-id="0b17c-200">Header</span></span>                   | <span data-ttu-id="0b17c-201">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="0b17c-201">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="0b17c-202">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0b17c-202">Library</span></span>                  | <span data-ttu-id="0b17c-203">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="0b17c-203">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="0b17c-204">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0b17c-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b17c-205">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="0b17c-205">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

