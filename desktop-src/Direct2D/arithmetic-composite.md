---
title: Arithmetischer zusammengesetzter Effekt
description: Verwenden Sie die arithmetischen zusammengesetzten Effekte, um 2 Bilder mit einer gewichteten Summe von Pixeln aus den Eingabe Bildern zu kombinieren.
ms.assetid: 6EC8CD61-5B51-4A8E-8A61-B291ABB5C5E0
keywords:
- arithmetischer zusammengesetzter Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c235ecb024c6b9e7adbce31c9f0cd65bc36cdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956938"
---
# <a name="arithmetic-composite-effect"></a><span data-ttu-id="194ee-104">Arithmetischer zusammengesetzter Effekt</span><span class="sxs-lookup"><span data-stu-id="194ee-104">Arithmetic composite effect</span></span>

<span data-ttu-id="194ee-105">Verwenden Sie die arithmetischen zusammengesetzten Effekte, um 2 Bilder mit einer gewichteten Summe von Pixeln aus den Eingabe Bildern zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="194ee-105">Use the arithmetic composite effect to combine 2 images using a weighted sum of pixels from the input images.</span></span>

<span data-ttu-id="194ee-106">Die CLSID für diesen Effekt ist CLSID \_ D2D1ArithmeticComposite.</span><span class="sxs-lookup"><span data-stu-id="194ee-106">The CLSID for this effect is CLSID\_D2D1ArithmeticComposite.</span></span>

-   [<span data-ttu-id="194ee-107">Formel</span><span class="sxs-lookup"><span data-stu-id="194ee-107">Formula</span></span>](#formula)
-   [<span data-ttu-id="194ee-108">Beispiel Bild</span><span class="sxs-lookup"><span data-stu-id="194ee-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="194ee-109">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="194ee-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="194ee-110">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="194ee-110">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="194ee-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="194ee-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="194ee-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="194ee-112">Related topics</span></span>](#related-topics)

## <a name="formula"></a><span data-ttu-id="194ee-113">Formel</span><span class="sxs-lookup"><span data-stu-id="194ee-113">Formula</span></span>

<span data-ttu-id="194ee-114">Die hier verwendete Formel wird verwendet, um diesen Effekt zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="194ee-114">The formula here is used to compute this effect.</span></span>

<span data-ttu-id="194ee-115">Ausgabe<sub>RGBA</sub> = C1 \* Quelle<sub>RGBA</sub> \* Ziel<sub>RGBA</sub> + C2 \* Quelle<sub>RGBA</sub> + C3 \* Ziel<sub>RGBA</sub> + C4</span><span class="sxs-lookup"><span data-stu-id="194ee-115">Output<sub>rgba</sub> = C1 \* Source<sub>rgba</sub> \* Destination<sub>rgba</sub> + C2 \* Source<sub>rgba</sub> + C3 \* Destination<sub>rgba</sub> + C4</span></span>

<span data-ttu-id="194ee-116">Dabei sind C1, C2, C3, C4 Koeffizienten, die Sie festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="194ee-116">Where C1, C2, C3, C4 are coefficients that you set.</span></span>

<span data-ttu-id="194ee-117">Die Koeffizienten entsprechen den Werten in einem D2D1 \_ Vector \_ 4f (x, y, z, w):</span><span class="sxs-lookup"><span data-stu-id="194ee-117">The coefficients map to the values in a D2D1\_VECTOR\_4F (x, y, z, w):</span></span>

-   <span data-ttu-id="194ee-118">x = C1</span><span class="sxs-lookup"><span data-stu-id="194ee-118">x = C1</span></span>
-   <span data-ttu-id="194ee-119">j = C2</span><span class="sxs-lookup"><span data-stu-id="194ee-119">y = C2</span></span>
-   <span data-ttu-id="194ee-120">z = C3</span><span class="sxs-lookup"><span data-stu-id="194ee-120">z = C3</span></span>
-   <span data-ttu-id="194ee-121">w = C4</span><span class="sxs-lookup"><span data-stu-id="194ee-121">w = C4</span></span>

## <a name="example-image"></a><span data-ttu-id="194ee-122">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="194ee-122">Example image</span></span>

<span data-ttu-id="194ee-123">Ein einfaches Beispiel besteht darin, die Quell-und Ziel Pixel hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="194ee-123">A simple example is to add the source and destination pixels.</span></span> <span data-ttu-id="194ee-124">Im Beispiel werden zwei abgerundete Rechtecke zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="194ee-124">In the example, 2 rounded rectangles are composited together.</span></span> <span data-ttu-id="194ee-125">Das Quell Rechteck ist blau, und das Ziel ist rot.</span><span class="sxs-lookup"><span data-stu-id="194ee-125">The source rectangle is blue and the destination is red.</span></span>

<span data-ttu-id="194ee-126">Das folgende Bild zeigt die Ausgabe des zusammengesetzten arithmetischen Effekts mit den Koeffizienten der Gleichung, die auf die hier aufgeführten Werte festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="194ee-126">The image here is the output of the Arithmetic Composite effect with the coefficients of the equation set to the values here.</span></span>

-   <span data-ttu-id="194ee-127">C1 = 0</span><span class="sxs-lookup"><span data-stu-id="194ee-127">C1 = 0</span></span>
-   <span data-ttu-id="194ee-128">C2 = 1</span><span class="sxs-lookup"><span data-stu-id="194ee-128">C2 = 1</span></span>
-   <span data-ttu-id="194ee-129">C3 = 1</span><span class="sxs-lookup"><span data-stu-id="194ee-129">C3 = 1</span></span>
-   <span data-ttu-id="194ee-130">C4 = 0</span><span class="sxs-lookup"><span data-stu-id="194ee-130">C4 = 0</span></span>

![ein Beispiel Bild, das zwei abgerundete Rechtecke der gleichen Größe anzeigt, die sich mithilfe des arithmetischen zusammengesetzten Effekts überlappen.](images/arithmetic-50-percent.png)

<span data-ttu-id="194ee-132">Das Ergebnis ist, dass die Pixelwerte für Quelle und Ziel hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="194ee-132">The result is that the pixel values for the source and destination are added.</span></span> <span data-ttu-id="194ee-133">Die Bereiche, in denen sich die Rechtecke nicht überlappen, sind alle 0.</span><span class="sxs-lookup"><span data-stu-id="194ee-133">The regions where the rectangles don't overlap the RGBA values are all 0.</span></span> <span data-ttu-id="194ee-134">Wenn sich die Rechtecke überlappen, ist der Wert Magenta, da R-und B-Werte beide den Höchstwert haben.</span><span class="sxs-lookup"><span data-stu-id="194ee-134">Where the rectangles overlap the color is magenta because the R and B values are both at maximum.</span></span>

<span data-ttu-id="194ee-135">Im folgenden finden Sie ein weiteres Beispiel Bild mit Code.</span><span class="sxs-lookup"><span data-stu-id="194ee-135">Here's another example image with code.</span></span>



| <span data-ttu-id="194ee-136">Vor Bild 1</span><span class="sxs-lookup"><span data-stu-id="194ee-136">Before image 1</span></span>                                                             |
|----------------------------------------------------------------------------|
| ![das erste Quell Bild vor dem Effekt.](images/default-before.jpg)    |
| <span data-ttu-id="194ee-138">Vor Abbildung 2</span><span class="sxs-lookup"><span data-stu-id="194ee-138">Before image 2</span></span>                                                             |
| ![Das zweite Bild vor dem Effekt.](images/4-arthimetic-composite2.jpg) |
| <span data-ttu-id="194ee-140">Nach</span><span class="sxs-lookup"><span data-stu-id="194ee-140">After</span></span>                                                                      |
| ![das Bild nach der Transformation.](images/4-arithmeticcomposite.png)        |



 


```C++
ComPtr<ID2D1Effect> arithmeticCompositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ArithmeticComposite, &arithmeticCompositeEffect);

arithmeticCompositeEffect->SetInput(0, bitmap);
arithmeticCompositeEffect->SetInput(1, bitmapTwo);
arithmeticCompositeEffect->SetValue(D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS, D2D1::Vector4F(0.0f, 0.5f, 0.5f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(arithmeticCompositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="194ee-142">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="194ee-142">Effect properties</span></span>



| <span data-ttu-id="194ee-143">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="194ee-143">Display name and index enumeration</span></span>                                               | <span data-ttu-id="194ee-144">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="194ee-144">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="194ee-145">Koeffizienten</span><span class="sxs-lookup"><span data-stu-id="194ee-145">Coefficients</span></span><br/> <span data-ttu-id="194ee-146">D2D1 \_ arithmeticcomposite- \_ Prop \_ -Koeffizienten</span><span class="sxs-lookup"><span data-stu-id="194ee-146">D2D1\_ARITHMETICCOMPOSITE\_PROP\_COEFFICIENTS</span></span><br/> | <span data-ttu-id="194ee-147">Die Koeffizienten für die Gleichung, die verwendet werden, um die beiden Eingabe Bilder zusammenzusetzen.</span><span class="sxs-lookup"><span data-stu-id="194ee-147">The coefficients for the equation used to composite the two input images.</span></span> <span data-ttu-id="194ee-148">Die Koeffizienten sind unitless und unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="194ee-148">The coefficients are unitless and unbounded.</span></span> <span data-ttu-id="194ee-149">Typ: D2D1 \_ Vector \_ 4f</span><span class="sxs-lookup"><span data-stu-id="194ee-149">Type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="194ee-150">Der Standardwert ist {1.0 f, 0,0 f, 0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="194ee-150">Default value is {1.0f, 0.0f, 0.0f, 0.0f}.</span></span><br/>                                                                                                                                                                                                                                 |
| <span data-ttu-id="194ee-151">Klamme Ausgabe</span><span class="sxs-lookup"><span data-stu-id="194ee-151">ClampOutput</span></span><br/> <span data-ttu-id="194ee-152">D2D1 \_ arithmeticcomposite- \_ Prop- \_ Klammer \_ Ausgabe</span><span class="sxs-lookup"><span data-stu-id="194ee-152">D2D1\_ARITHMETICCOMPOSITE\_PROP\_CLAMP\_OUTPUT</span></span><br/> | <span data-ttu-id="194ee-153">Der Effekt klemmt Farbwerte auf zwischen 0 und 1, bevor der Effekt die Werte an den nächsten Effekt im Diagramm übergibt.</span><span class="sxs-lookup"><span data-stu-id="194ee-153">The effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <br/> <span data-ttu-id="194ee-154">Wenn Sie diese Einstellung auf "true" festlegen, werden die Werte durch die Auswirkung fixiert.</span><span class="sxs-lookup"><span data-stu-id="194ee-154">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="194ee-155">Wenn Sie diese Einstellung auf "false" festlegen, werden die Farbwerte durch die Auswirkung nicht fixiert, aber andere Effekte und die Ausgabe Oberfläche können die Werte einspannen, wenn Sie nicht über eine hohe Genauigkeit verfügen.</span><span class="sxs-lookup"><span data-stu-id="194ee-155">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> <span data-ttu-id="194ee-156">Der Typ ist "bool".</span><span class="sxs-lookup"><span data-stu-id="194ee-156">Type is BOOL.</span></span><br/> <span data-ttu-id="194ee-157">Der Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="194ee-157">Default value is FALSE.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="194ee-158">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="194ee-158">Output bitmap</span></span>

<span data-ttu-id="194ee-159">Die Ausgabe Bitmap hängt von den Koeffizienten-Werten ab.</span><span class="sxs-lookup"><span data-stu-id="194ee-159">The output bitmap depends on the coefficient values.</span></span> <span data-ttu-id="194ee-160">Dies sind die möglichen Ausgabe Bitmapgrößen.</span><span class="sxs-lookup"><span data-stu-id="194ee-160">These are the possible output bitmap sizes.</span></span>

-   <span data-ttu-id="194ee-161">Wenn C1 der einzige Koeffizient ungleich NULL ist, ist die Ausgabegröße die Schnittmenge der Eingabe Rechtecke.</span><span class="sxs-lookup"><span data-stu-id="194ee-161">If C1 is the only non-zero coefficient, the output size is the intersection of the input rectangles.</span></span>
-   <span data-ttu-id="194ee-162">Wenn C2 der einzige Koeffizient ungleich NULL ist, entspricht die Ausgabegröße der Größe des Quell Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="194ee-162">If C2 is the only non-zero coefficient, the output size is the size of the Source rectangle.</span></span>
-   <span data-ttu-id="194ee-163">Wenn C3 der einzige Koeffizient ungleich NULL ist, entspricht die Ausgabegröße der Größe des Ziel Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="194ee-163">If C3 is the only non-zero coefficient, the output size is the size of the Destination rectangle..</span></span>
-   <span data-ttu-id="194ee-164">Wenn alle Koeffizienten NULL sind, ist die Ausgabegröße ein leeres Rechteck.</span><span class="sxs-lookup"><span data-stu-id="194ee-164">If all coefficients are zero, the output size is an empty rectangle.</span></span>
-   <span data-ttu-id="194ee-165">Für alle anderen Koeffizienten-Werte ist die Ausgabegröße die Vereinigung der Eingabe Rechtecke.</span><span class="sxs-lookup"><span data-stu-id="194ee-165">For all other coefficient values, the output size is the union of the input rectangles.</span></span>

## <a name="requirements"></a><span data-ttu-id="194ee-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="194ee-166">Requirements</span></span>



| <span data-ttu-id="194ee-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="194ee-167">Requirement</span></span> | <span data-ttu-id="194ee-168">Wert</span><span class="sxs-lookup"><span data-stu-id="194ee-168">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="194ee-169">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="194ee-169">Minimum supported client</span></span> | <span data-ttu-id="194ee-170">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="194ee-170">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="194ee-171">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="194ee-171">Minimum supported server</span></span> | <span data-ttu-id="194ee-172">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="194ee-172">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="194ee-173">Header</span><span class="sxs-lookup"><span data-stu-id="194ee-173">Header</span></span>                   | <span data-ttu-id="194ee-174">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="194ee-174">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="194ee-175">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="194ee-175">Library</span></span>                  | <span data-ttu-id="194ee-176">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="194ee-176">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="194ee-177">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="194ee-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="194ee-178">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="194ee-178">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

