---
title: Fülleffekt
description: Verwenden Sie den Blend-Effekt, um 2 Bilder zu kombinieren. Dieser Effekt hat 26 Blend-Modi.
ms.assetid: 39D8BAA3-8FF3-4F10-99A0-B26FCA3018AE
keywords:
- Blend-Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e248d1f7f41721d173510b8d10feac9be2e08f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859229"
---
# <a name="blend-effect"></a><span data-ttu-id="17124-105">Fülleffekt</span><span class="sxs-lookup"><span data-stu-id="17124-105">Blend effect</span></span>

<span data-ttu-id="17124-106">Verwenden Sie den Blend-Effekt, um 2 Bilder zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="17124-106">Use the blend effect to combine 2 images.</span></span> <span data-ttu-id="17124-107">Dieser Effekt hat 26 Blend-Modi.</span><span class="sxs-lookup"><span data-stu-id="17124-107">This effect has 26 blend modes.</span></span>

<span data-ttu-id="17124-108">Die CLSID für diesen Effekt ist CLSID \_ D2D1Blend.</span><span class="sxs-lookup"><span data-stu-id="17124-108">The CLSID for this effect is CLSID\_D2D1Blend.</span></span>

-   [<span data-ttu-id="17124-109">Kombination von Beispielen</span><span class="sxs-lookup"><span data-stu-id="17124-109">Blending examples</span></span>](#blending-examples)
-   [<span data-ttu-id="17124-110">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="17124-110">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="17124-111">Blend-Modi</span><span class="sxs-lookup"><span data-stu-id="17124-111">Blend modes</span></span>](#blend-modes)
-   [<span data-ttu-id="17124-112">HSL-Farb Raum Konvertierungen</span><span class="sxs-lookup"><span data-stu-id="17124-112">HSL color space conversions</span></span>](#hsl-color-space-conversions)
    -   [<span data-ttu-id="17124-113">Umstellen von RGB in HSL</span><span class="sxs-lookup"><span data-stu-id="17124-113">Converting from RGB to HSL</span></span>](#converting-from-rgb-to-hsl)
    -   [<span data-ttu-id="17124-114">Umstellen von HSL in RGB</span><span class="sxs-lookup"><span data-stu-id="17124-114">Converting from HSL to RGB</span></span>](#converting-from-hsl-to-rgb)
-   [<span data-ttu-id="17124-115">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="17124-115">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="17124-116">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="17124-116">Sample code</span></span>](#sample-code)
-   [<span data-ttu-id="17124-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17124-117">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="17124-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="17124-118">Related topics</span></span>](#related-topics)

## <a name="blending-examples"></a><span data-ttu-id="17124-119">Kombination von Beispielen</span><span class="sxs-lookup"><span data-stu-id="17124-119">Blending examples</span></span>

<span data-ttu-id="17124-120">Im folgenden finden Sie ein Beispiel Bild für jeden Blend-Modus des Blend-Effekts.</span><span class="sxs-lookup"><span data-stu-id="17124-120">Here is an example image of every blend mode of the blend effect.</span></span> <span data-ttu-id="17124-121">Eine vollständige Liste der Blend-Modi und der entsprechenden moduseigenschaften finden Sie im nächsten Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="17124-121">A full list of the blend modes and the corresponding mode properties are in the next section</span></span>

![Beispiel: Screenshot aller verfügbaren Blend-Modi.](images/blend-modes.png)

<span data-ttu-id="17124-123">Im folgenden finden Sie ein weiteres Beispiel für die Verwendung des Ausschluss Modus.</span><span class="sxs-lookup"><span data-stu-id="17124-123">Here is another example using the exclusion mode.</span></span>



| <span data-ttu-id="17124-124">Vor Bild 1</span><span class="sxs-lookup"><span data-stu-id="17124-124">Before image 1</span></span>                                                             |
|----------------------------------------------------------------------------|
| ![das erste Quell Bild vor dem Effekt.](images/default-before.jpg)    |
| <span data-ttu-id="17124-126">Vor Abbildung 2</span><span class="sxs-lookup"><span data-stu-id="17124-126">Before image 2</span></span>                                                             |
| ![Das zweite Bild vor dem Effekt.](images/4-arthimetic-composite2.jpg) |
| <span data-ttu-id="17124-128">Nach</span><span class="sxs-lookup"><span data-stu-id="17124-128">After</span></span>                                                                      |
| ![das Bild nach der Transformation.](images/5-blend.png)                      |



 


```C++
ComPtr<ID2D1Effect> blendEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Blend, &blendEffect);

blendEffect->SetInput(0, bitmap);
blendEffect->SetInput(1, bitmapTwo);
blendEffect->SetValue(D2D1_BLEND_PROP_MODE, D2D1_BLEND_MODE_EXCLUSION);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(blendEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="17124-130">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="17124-130">Effect properties</span></span>



| <span data-ttu-id="17124-131">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="17124-131">Display name and index enumeration</span></span>                 | <span data-ttu-id="17124-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17124-132">Description</span></span>                                                                                                                                                                               |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17124-133">Mode</span><span class="sxs-lookup"><span data-stu-id="17124-133">Mode</span></span><br/> <span data-ttu-id="17124-134">D2D1 \_ Blend- \_ Prop- \_ Modus</span><span class="sxs-lookup"><span data-stu-id="17124-134">D2D1\_BLEND\_PROP\_MODE</span></span><br/> | <span data-ttu-id="17124-135">Der für den Effekt verwendete Blend-Modus.</span><span class="sxs-lookup"><span data-stu-id="17124-135">The blend mode used for the effect.</span></span> <span data-ttu-id="17124-136">Weitere Informationen finden Sie unter [Blend-Modi](#blend-modes) .</span><span class="sxs-lookup"><span data-stu-id="17124-136">See [Blend modes](#blend-modes) for more info.</span></span> <span data-ttu-id="17124-137">Der Typ ist der D2D1 \_ Blend- \_ Modus.</span><span class="sxs-lookup"><span data-stu-id="17124-137">The type is D2D1\_BLEND\_MODE.</span></span><br/> <span data-ttu-id="17124-138">Der Standardwert ist D2D1 \_ Blend \_ Mode \_ Multiplikation.</span><span class="sxs-lookup"><span data-stu-id="17124-138">The default value is D2D1\_BLEND\_MODE\_MULTIPLY.</span></span><br/> |



 

## <a name="blend-modes"></a><span data-ttu-id="17124-139">Füllmethoden</span><span class="sxs-lookup"><span data-stu-id="17124-139">Blend modes</span></span>

<span data-ttu-id="17124-140">In der hier aufgeführten Tabelle werden alle Blend-Modi dieses Effekts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="17124-140">The table here shows all the blend modes of this effect.</span></span> <span data-ttu-id="17124-141">Die Hilfsfunktionen, die erforderlich sind, um die Ausgabe des Effekts zu berechnen, finden Sie im nächsten Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="17124-141">The helper functions necessary to compute the output of the effect are in the next section.</span></span>

<span data-ttu-id="17124-142">Farbe: O <sub>prgb</sub>  =  *f*(f <sub>RGB</sub>, B <sub>RGB</sub>) \* f <sub>a</sub> \* B <sub>a</sub> + f <sub>RGB</sub> \* f <sub>a</sub> \* (1-B <sub>a</sub>) + B <sub>RGB</sub> \* b <sub>A</sub> \* (1-f <sub>a</sub>)</span><span class="sxs-lookup"><span data-stu-id="17124-142">Color: O <sub>PRGB</sub> = *f*(F<sub>RGB</sub>, B<sub>RGB</sub>) \* F<sub>A</sub> \* B<sub>A</sub> + F<sub>RGB</sub> \* F<sub>A</sub> \* (1 - B<sub>A</sub>) + B<sub>RGB</sub> \* B<sub>A</sub> \* (1 - F<sub>A</sub>)</span></span>

<span data-ttu-id="17124-143">Alpha: O<sub>a</sub> = F<sub>a</sub> \* (1-B<sub>a</sub>) + B<sub>a</sub></span><span class="sxs-lookup"><span data-stu-id="17124-143">Alpha: O<sub>A</sub> = F<sub>A</sub> \* (1 - B<sub>A</sub>) + B<sub>A</sub></span></span>

<span data-ttu-id="17124-144">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="17124-144">Where:</span></span>

-   <span data-ttu-id="17124-145">O<sub>prgb</sub> ist die vorab multiplizierte Ausgabe Farbe</span><span class="sxs-lookup"><span data-stu-id="17124-145">O<sub>PRGB</sub> is the pre-multiplied output color</span></span>
-   <span data-ttu-id="17124-146">O<sub>A</sub> ist Ausgabe Alpha</span><span class="sxs-lookup"><span data-stu-id="17124-146">O<sub>A</sub> is Output Alpha</span></span>
-   <span data-ttu-id="17124-147">B<sub>RGB</sub> ist die nicht vorab multiplizierte Zielfarbe</span><span class="sxs-lookup"><span data-stu-id="17124-147">B<sub>RGB</sub> is the un-pre-multiplied destination color</span></span>
-   <span data-ttu-id="17124-148">B<sub>a</sub> ist Destination Alpha</span><span class="sxs-lookup"><span data-stu-id="17124-148">B<sub>A</sub> is destination alpha</span></span>
-   <span data-ttu-id="17124-149">F<sub>RGB</sub> ist die nicht vorab multiplizierte Quellfarbe</span><span class="sxs-lookup"><span data-stu-id="17124-149">F<sub>RGB</sub> is the un-pre-multiplied source color</span></span>
-   <span data-ttu-id="17124-150">F<sub>A</sub> ist Quell-Alpha</span><span class="sxs-lookup"><span data-stu-id="17124-150">F<sub>A</sub> is source alpha</span></span>
-   <span data-ttu-id="17124-151">*f*(S <sub>RGB</sub>, D <sub>RGB</sub>) ist eine Blend-Funktion, die je nach Blend-Modus variiert.</span><span class="sxs-lookup"><span data-stu-id="17124-151">*f*(S<sub>RGB</sub>, D<sub>RGB</sub>) is a blend function that varies per-blend-mode</span></span>

<span data-ttu-id="17124-152">Einige der Blend-Modi erfordern eine Konvertierung in den und aus dem Farbton-, Sättigungs-und Helligkeits Raum (HSL) in RGB.</span><span class="sxs-lookup"><span data-stu-id="17124-152">Some of the blend modes require conversion to and from the hue, saturation, luminosity (HSL) color space to RGB.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="17124-153">Enumeration</span><span class="sxs-lookup"><span data-stu-id="17124-153">Enumeration</span></span></th>
<th><span data-ttu-id="17124-154">Gleichung</span><span class="sxs-lookup"><span data-stu-id="17124-154">Equation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="17124-155">D2D1_BLEND_MODE_DARKEN</span><span class="sxs-lookup"><span data-stu-id="17124-155">D2D1_BLEND_MODE_DARKEN</span></span></td>
<td><span data-ttu-id="17124-156">Einfache Blend-Formel nur für Alpha.</span><span class="sxs-lookup"><span data-stu-id="17124-156">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-darken-1.png" alt="mathematical formula for a darken effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17124-157">D2D1_BLEND_MODE_MULTIPLY</span><span class="sxs-lookup"><span data-stu-id="17124-157">D2D1_BLEND_MODE_MULTIPLY</span></span></td>
<td><span data-ttu-id="17124-158">Einfache Blend-Formel nur für Alpha.</span><span class="sxs-lookup"><span data-stu-id="17124-158">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-multiply-1.png" alt="Mathematical formula for a mutiply effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17124-159">D2D1_BLEND_MODE_COLOR_BURN</span><span class="sxs-lookup"><span data-stu-id="17124-159">D2D1_BLEND_MODE_COLOR_BURN</span></span></td>
<td><span data-ttu-id="17124-160">Grundlegende Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="17124-160">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-colorburn-1.png" alt="Mathematical formula for a coor burn effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17124-161">D2D1_BLEND_MODE_LINEAR_BURN</span><span class="sxs-lookup"><span data-stu-id="17124-161">D2D1_BLEND_MODE_LINEAR_BURN</span></span></td>
<td><span data-ttu-id="17124-162">Grundlegende Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="17124-162">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-linearburn-1.png" alt="Mathematical formula for a linear burn effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17124-163">D2D1_BLEND_MODE_DARKER_COLOR</span><span class="sxs-lookup"><span data-stu-id="17124-163">D2D1_BLEND_MODE_DARKER_COLOR</span></span></td>
<td><span data-ttu-id="17124-164">Einfache Blend-Formel nur für Alpha.</span><span class="sxs-lookup"><span data-stu-id="17124-164">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-darkencolor-1.png" alt="Mathematical formla for a darken color effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17124-165">D2D1_BLEND_MODE_LIGHTEN</span><span class="sxs-lookup"><span data-stu-id="17124-165">D2D1_BLEND_MODE_LIGHTEN</span></span></td>
<td><span data-ttu-id="17124-166">Einfache Blend-Formel nur für Alpha.</span><span class="sxs-lookup"><span data-stu-id="17124-166">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-lighten-1.png" alt="Mathematical formula for a lighten effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17124-167">D2D1_BLEND_MODE_SCREEN</span><span class="sxs-lookup"><span data-stu-id="17124-167">D2D1_BLEND_MODE_SCREEN</span></span></td>
<td><span data-ttu-id="17124-168">Einfache Blend-Formel nur für Alpha.</span><span class="sxs-lookup"><span data-stu-id="17124-168">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-screen-1.png" alt="Mathematical formula for a screen effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17124-169">D2D1_BLEND_MODE_COLOR_DODGE</span><span class="sxs-lookup"><span data-stu-id="17124-169">D2D1_BLEND_MODE_COLOR_DODGE</span></span></td>
<td><span data-ttu-id="17124-170">Grundlegende Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="17124-170">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-colordodge-1.png" alt="Mathematical formula for a color dodge effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17124-171">D2D1_BLEND_MODE_LINEAR_DODGE</span><span class="sxs-lookup"><span data-stu-id="17124-171">D2D1_BLEND_MODE_LINEAR_DODGE</span></span></td>
<td><span data-ttu-id="17124-172">Grundlegende Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="17124-172">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-lineardodge-1.png" alt="Mathematical formula for a linear dodge effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17124-173">D2D1_BLEND_MODE_LIGHTER_COLOR</span><span class="sxs-lookup"><span data-stu-id="17124-173">D2D1_BLEND_MODE_LIGHTER_COLOR</span></span></td>
<td><span data-ttu-id="17124-174">Einfache Blend-Formel nur für Alpha.</span><span class="sxs-lookup"><span data-stu-id="17124-174">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-lightercolor-1.png" alt="Mathematical formula for a lighter color effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17124-175">D2D1_BLEND_MODE_OVERLAY</span><span class="sxs-lookup"><span data-stu-id="17124-175">D2D1_BLEND_MODE_OVERLAY</span></span></td>
<td><span data-ttu-id="17124-176">Grundlegende Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="17124-176">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-overlay-1.png" alt="Mathematical formula for an overlay effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17124-177">D2D1_BLEND_MODE_SOFT_LIGHT</span><span class="sxs-lookup"><span data-stu-id="17124-177">D2D1_BLEND_MODE_SOFT_LIGHT</span></span></td>
<td><span data-ttu-id="17124-178">Grundlegende Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="17124-178">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-softlight-1.png" alt="Mathematical formula for a soft light effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17124-179">D2D1_BLEND_MODE_HARD_LIGHT</span><span class="sxs-lookup"><span data-stu-id="17124-179">D2D1_BLEND_MODE_HARD_LIGHT</span></span></td>
<td><span data-ttu-id="17124-180">Grundlegende Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="17124-180">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-hardlight-1.png" alt="Mathematical formula for a hard light effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17124-181">D2D1_BLEND_MODE_VIVID_LIGHT</span><span class="sxs-lookup"><span data-stu-id="17124-181">D2D1_BLEND_MODE_VIVID_LIGHT</span></span></td>
<td><span data-ttu-id="17124-182">Grundlegende Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="17124-182">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-vividlight-1.png" alt="Mathematical formula for a vivid light effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17124-183">D2D1_BLEND_MODE_LINEAR_LIGHT</span><span class="sxs-lookup"><span data-stu-id="17124-183">D2D1_BLEND_MODE_LINEAR_LIGHT</span></span></td>
<td><span data-ttu-id="17124-184">Grundlegende Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="17124-184">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-linearlight-1.png" alt="Mathematical formula for a linear light effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17124-185">D2D1_BLEND_MODE_PIN_LIGHT</span><span class="sxs-lookup"><span data-stu-id="17124-185">D2D1_BLEND_MODE_PIN_LIGHT</span></span></td>
<td><span data-ttu-id="17124-186">Grundlegende Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="17124-186">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-pinlight-1.png" alt="Mathematical formula for a pin light effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17124-187">D2D1_BLEND_MODE_HARD_MIX</span><span class="sxs-lookup"><span data-stu-id="17124-187">D2D1_BLEND_MODE_HARD_MIX</span></span></td>
<td><span data-ttu-id="17124-188">Grundlegende Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="17124-188">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-hardmix-1.png" alt="Mathematical formula for a hard mix effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17124-189">D2D1_BLEND_MODE_DIFFERENCE</span><span class="sxs-lookup"><span data-stu-id="17124-189">D2D1_BLEND_MODE_DIFFERENCE</span></span></td>
<td><span data-ttu-id="17124-190">Einfache Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = Abs (f<sub>RGB</sub> - B<sub>RGB</sub>)</span><span class="sxs-lookup"><span data-stu-id="17124-190">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = abs(F<sub>RGB</sub> - B<sub>RGB</sub>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17124-191">D2D1_BLEND_MODE_EXCLUSION</span><span class="sxs-lookup"><span data-stu-id="17124-191">D2D1_BLEND_MODE_EXCLUSION</span></span></td>
<td><span data-ttu-id="17124-192">Grundlegende Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = f<sub>RGB</sub> + b<sub>RGB</sub>   2 \* f<sub>RGB</sub> \* b<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="17124-192">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = F<sub>RGB</sub> + B<sub>RGB</sub>   2 \* F<sub>RGB</sub> \* B<sub>RGB</sub></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17124-193">D2D1_BLEND_MODE_HUE</span><span class="sxs-lookup"><span data-stu-id="17124-193">D2D1_BLEND_MODE_HUE</span></span></td>
<td><span data-ttu-id="17124-194">Einfache Blend-Formel nur für Alpha.</span><span class="sxs-lookup"><span data-stu-id="17124-194">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-hue-1.png" alt="Mathematical formula for a hue blend effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17124-195">D2D1_BLEND_MODE_SATURATION</span><span class="sxs-lookup"><span data-stu-id="17124-195">D2D1_BLEND_MODE_SATURATION</span></span></td>
<td><span data-ttu-id="17124-196">Einfache Blend-Formel nur für Alpha.</span><span class="sxs-lookup"><span data-stu-id="17124-196">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-saturation-1.png" alt="Mathematical formula for a sturation blend effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17124-197">D2D1_BLEND_MODE_COLOR</span><span class="sxs-lookup"><span data-stu-id="17124-197">D2D1_BLEND_MODE_COLOR</span></span></td>
<td><span data-ttu-id="17124-198">Einfache Blend-Formel nur für Alpha.</span><span class="sxs-lookup"><span data-stu-id="17124-198">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-color-1.png" alt="Mathematical formula for a color blend effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17124-199">D2D1_BLEND_MODE_LUMINOSITY</span><span class="sxs-lookup"><span data-stu-id="17124-199">D2D1_BLEND_MODE_LUMINOSITY</span></span></td>
<td><span data-ttu-id="17124-200">Einfache Blend-Formel nur für Alpha.</span><span class="sxs-lookup"><span data-stu-id="17124-200">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-luminosity-1.png" alt="Mathematical formula for a luminosity blend effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17124-201">D2D1_BLEND_MODE_DISSOLVE</span><span class="sxs-lookup"><span data-stu-id="17124-201">D2D1_BLEND_MODE_DISSOLVE</span></span></td>
<td><span data-ttu-id="17124-202">Gegeben:</span><span class="sxs-lookup"><span data-stu-id="17124-202">Given:</span></span>
<ul>
<li><span data-ttu-id="17124-203">Eine Szenen Koordinaten-XY für das aktuelle Pixel</span><span class="sxs-lookup"><span data-stu-id="17124-203">A scene coordinate XY for the current pixel</span></span></li>
<li><span data-ttu-id="17124-204">Ein deterministischer Pseudozufallszahlen Generator Rand (XY), der auf der Ausgangswert-Koordinate (XY) basiert, mit einer unausgewogenen Verteilung der Werte von [0,0]</span><span class="sxs-lookup"><span data-stu-id="17124-204">A deterministic pseudo-random number generator rand(XY) based on seed coordinate XY, with unbiased distribution of values from [0, 1]</span></span></li>
</ul>
<br/> <img src="images/blend-mode-dissolve-1.png" alt="Mathematical formula for a dissolve blend effect." /><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17124-205">D2D1_BLEND_MODE_SUBTRACT</span><span class="sxs-lookup"><span data-stu-id="17124-205">D2D1_BLEND_MODE_SUBTRACT</span></span></td>
<td><span data-ttu-id="17124-206">Einfache Blend-Formel nur für Alpha.</span><span class="sxs-lookup"><span data-stu-id="17124-206">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-subtract-1.png" alt="Mathematical formula for a subtract blend effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17124-207">D2D1_BLEND_MODE_DIVISION</span><span class="sxs-lookup"><span data-stu-id="17124-207">D2D1_BLEND_MODE_DIVISION</span></span></td>
<td><span data-ttu-id="17124-208">Einfache Blend-Formel nur für Alpha.</span><span class="sxs-lookup"><span data-stu-id="17124-208">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-division-1.png" alt="Mathematical formula for a division blend effect." /></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="17124-209">Für alle Blend-Modi wird der Ausgabewert vorab multipliziert und an den Bereich \[ 0, 1 gebunden \] .</span><span class="sxs-lookup"><span data-stu-id="17124-209">For all Blend modes, the output value is premultiplied and clamped to the range \[0, 1\].</span></span>

 

## <a name="hsl-color-space-conversions"></a><span data-ttu-id="17124-210">HSL-Farb Raum Konvertierungen</span><span class="sxs-lookup"><span data-stu-id="17124-210">HSL color space conversions</span></span>

<span data-ttu-id="17124-211">Die Komponente "Brillanz" wird mithilfe der RGB-Gewichtungen berechnet:</span><span class="sxs-lookup"><span data-stu-id="17124-211">The luminosity component is computed using the RGB weights here:</span></span>

-   <span data-ttu-id="17124-212">*k*<sub>R</sub> = 0,30</span><span class="sxs-lookup"><span data-stu-id="17124-212">*k*<sub>R</sub> = 0.30</span></span>
-   <span data-ttu-id="17124-213">*k*<sub>G</sub> = 0,59</span><span class="sxs-lookup"><span data-stu-id="17124-213">*k*<sub>G</sub> = 0.59</span></span>
-   <span data-ttu-id="17124-214">*k*<sub>B</sub> = 0,11</span><span class="sxs-lookup"><span data-stu-id="17124-214">*k*<sub>B</sub> = 0.11</span></span>

### <a name="converting-from-rgb-to-hsl"></a><span data-ttu-id="17124-215">Umstellen von RGB in HSL</span><span class="sxs-lookup"><span data-stu-id="17124-215">Converting from RGB to HSL</span></span>

![mathematische Formel, die die Transformation zwischen RGB-Farbe und HSL-Farbe beschreibt.](images/blend-rgb-to-hsl-1.png)

<span data-ttu-id="17124-217">Dabei werden *S* und *L* im Bereich von \[ \] -1,0, 5,0  und L im Bereich von 0,0, 1,0 und H platziert \[ \] .</span><span class="sxs-lookup"><span data-stu-id="17124-217">This places *S* and *L* in the range \[0.0, 1.0\] and *H* in the range \[-1.0, 5.0\].</span></span>

### <a name="converting-from-hsl-to-rgb"></a><span data-ttu-id="17124-218">Umstellen von HSL in RGB</span><span class="sxs-lookup"><span data-stu-id="17124-218">Converting from HSL to RGB</span></span>

<span data-ttu-id="17124-219">Um die andere Methode zu konvertieren, verwenden wir die Umkehrung der vorherigen Berechnungen.</span><span class="sxs-lookup"><span data-stu-id="17124-219">To convert the other way we use the inverse of the previous calculations.</span></span>

<span data-ttu-id="17124-220">Wenn *S* = 0, dann *R*  =  *G*  =  *B*  =  *L*</span><span class="sxs-lookup"><span data-stu-id="17124-220">If *S* = 0 then *R* = *G* = *B* = *L*</span></span>

<span data-ttu-id="17124-221">Andernfalls gibt es sechs von Hue abhängige Fälle:</span><span class="sxs-lookup"><span data-stu-id="17124-221">Otherwise there are six hue-dependant cases:</span></span>

<span data-ttu-id="17124-222">Wenn *H* größer als 0 ist, befinden sich die Werte im red/Magenta-Sektor, in dem *R*  >  *B*  >  *G* ist.</span><span class="sxs-lookup"><span data-stu-id="17124-222">If *H* is greater than 0, the values are in the red/magenta sector where *R* > *B* > *G*.</span></span>

![mathematische equaiton-Schritt 1 von sechs, der die HSL-Farbe in RGB umwandelt.](images/blend-hsl-to-rgb-1rm.png)

<span data-ttu-id="17124-224">Wenn *H* größer oder gleich 0 und kleiner als 1 ist, befinden sich die Werte im roten/gelben Sektor, in dem *R*  >  *G*  >  *B* liegt.</span><span class="sxs-lookup"><span data-stu-id="17124-224">If *H* is greater than or equal to 0 and less than 1, the values are in the red/yellow sector where *R* > *G* > *B*.</span></span>

![mathematische equaiton-Schritt 2 von sechs, der die HSL-Farbe in RGB umwandelt.](images/blend-hsl-to-rgb-1ry.png)

<span data-ttu-id="17124-226">Wenn *H* größer oder gleich 1 und kleiner als 2 ist, befinden sich die Werte im gelben/grünen Sektor, in dem *G*  >  *R*  >  *B*.</span><span class="sxs-lookup"><span data-stu-id="17124-226">If *H* is greater than or equal to 1 and less than 2, the values are in the yellow/green sector where *G* > *R* > *B*.</span></span>

![mathematische equaiton-Schritt 3 von sechs, der die HSL-Farbe in RGB umwandelt.](images/blend-hsl-to-rgb-1yg.png)

<span data-ttu-id="17124-228">Wenn *H* größer oder gleich 2 und kleiner als 3 ist, befinden sich die Werte im grünen/Cyan-Sektor, in dem *G*  >  *B*  >  *R* liegt.</span><span class="sxs-lookup"><span data-stu-id="17124-228">If *H* is greater than or equal to 2 and less than 3, the values are in the green/cyan sector where *G* > *B* > *R*.</span></span>

![mathematische equaiton-Schritt 4 von sechs, die die HSL-Farbe in RGB umwandelt.](images/blend-hsl-to-rgb-1gc.png)

<span data-ttu-id="17124-230">Wenn *H* größer oder gleich 3 und kleiner als 4 ist, befinden sich die Werte im Cyan/Blue-Sektor, in dem *B*  >  *G*  >  *R* liegt.</span><span class="sxs-lookup"><span data-stu-id="17124-230">If *H* is greater than or equal to 3 and less than 4, the values are in the cyan/blue sector where *B* > *G* > *R*.</span></span>

![mathematische equaiton Step 5 of Six, um die HSL-Farbe in RGB umzuwandeln.](images/blend-hsl-to-rgb-1cb.png)

<span data-ttu-id="17124-232">Wenn *H* größer oder gleich 4 ist, befinden sich die Werte im Blue/Magenta-Sektor, in dem *B*  >  *R*  >  *G* ist.</span><span class="sxs-lookup"><span data-stu-id="17124-232">If *H* is greater than or equal to 4, the values are in the blue/magenta sector where *B* > *R* > *G*.</span></span>

![mathematische equaiton-Schritt 6 von sechs, die die HSL-Farbe in RGB umwandelt.](images/blend-hsl-to-rgb-1bm.png)

<span data-ttu-id="17124-234">Da die Mischungs Modi beliebige Kombinationen von HSL-Komponenten aus zwei unterschiedlichen Farben bilden, ist es üblich, dass der konvertierte RGB-Wert außerhalb des Spiel Bereichs liegt, d. h., eine oder mehrere channelkomponenten liegen möglicherweise außerhalb des gültigen Bereichs von \[ 0,0, 1,0 \] .</span><span class="sxs-lookup"><span data-stu-id="17124-234">Because the blending modes make arbitrary combinations of HSL components from two different colors, it is common for the converted RGB value to be out-of-gamut, that is, one or more channel components may be outside the legal range of \[0.0, 1.0\].</span></span> <span data-ttu-id="17124-235">Diese Farben werden wieder in den Farbskala eingefügt, indem die Sättigung minimal reduziert und sowohl Farbton als auch Helligkeit beibehalten werden:</span><span class="sxs-lookup"><span data-stu-id="17124-235">These colors are brought back into gamut by minimally reducing the saturation, while preserving both hue and luminosity:</span></span>

![mathematische Formel, die die Korrekturen beschreibt, die für nicht von Farbskala Instanzen erforderlich sind.](images/blend-gamut-correction.png)

## <a name="output-bitmap"></a><span data-ttu-id="17124-237">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="17124-237">Output bitmap</span></span>

<span data-ttu-id="17124-238">Das Ausgabe Bitmap für diesen Effekt ist immer die Größe der Union der beiden Eingabe Bilder.</span><span class="sxs-lookup"><span data-stu-id="17124-238">The output bitmap for this effect is always the size of the union of the two input images.</span></span>

## <a name="sample-code"></a><span data-ttu-id="17124-239">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="17124-239">Sample code</span></span>

<span data-ttu-id="17124-240">Um ein Beispiel für diesen Effekt zu erhalten, laden Sie das [Beispiel Direct2D Composite Effect Modes](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample)herunter.</span><span class="sxs-lookup"><span data-stu-id="17124-240">For an example of this effect, download the [Direct2D composite effect modes sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).</span></span>

## <a name="requirements"></a><span data-ttu-id="17124-241">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17124-241">Requirements</span></span>



| <span data-ttu-id="17124-242">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17124-242">Requirement</span></span> | <span data-ttu-id="17124-243">Wert</span><span class="sxs-lookup"><span data-stu-id="17124-243">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="17124-244">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17124-244">Minimum supported client</span></span> | <span data-ttu-id="17124-245">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17124-245">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="17124-246">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17124-246">Minimum supported server</span></span> | <span data-ttu-id="17124-247">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17124-247">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="17124-248">Header</span><span class="sxs-lookup"><span data-stu-id="17124-248">Header</span></span>                   | <span data-ttu-id="17124-249">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="17124-249">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="17124-250">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="17124-250">Library</span></span>                  | <span data-ttu-id="17124-251">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="17124-251">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="17124-252">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="17124-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17124-253">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="17124-253">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

