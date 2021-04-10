---
title: Zusammengesetzter Effekt
description: Verwenden Sie den zusammengesetzten Effekt, um zwei oder mehr Bilder zu kombinieren. Dieser Effekt hat 13 verschiedene zusammengesetzte Modi.
ms.assetid: 60b878e9-1bc6-40d4-ade3-4bbd5c822c55
keywords:
- zusammengesetzter Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9872a66d031e8307f911ec7270af81397a80276
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956616"
---
# <a name="composite-effect"></a><span data-ttu-id="29225-105">Zusammengesetzter Effekt</span><span class="sxs-lookup"><span data-stu-id="29225-105">Composite effect</span></span>

<span data-ttu-id="29225-106">Verwenden Sie den zusammengesetzten Effekt, um zwei oder mehr Bilder zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="29225-106">Use the composite effect to combine 2 or more images.</span></span> <span data-ttu-id="29225-107">Dieser Effekt hat 13 verschiedene zusammengesetzte Modi.</span><span class="sxs-lookup"><span data-stu-id="29225-107">This effect has 13 different composite modes.</span></span> <span data-ttu-id="29225-108">T</span><span class="sxs-lookup"><span data-stu-id="29225-108">T</span></span>

<span data-ttu-id="29225-109">Der zusammengesetzte Effekt akzeptiert mindestens zwei Eingaben.</span><span class="sxs-lookup"><span data-stu-id="29225-109">The composite effect accepts 2 or more inputs.</span></span> <span data-ttu-id="29225-110">Wenn Sie 2 Bilder angeben, ist Destination die erste Eingabe (Index 0), und die Quelle ist die zweite Eingabe (Index 1).</span><span class="sxs-lookup"><span data-stu-id="29225-110">When you specify 2 images, destination is the first input (index 0) and the source is the second input (index 1).</span></span> <span data-ttu-id="29225-111">Wenn Sie mehr als 2 Eingaben angeben, werden die Bilder zusammengesetzt, beginnend mit der ersten Eingabe und der zweiten, usw.</span><span class="sxs-lookup"><span data-stu-id="29225-111">If you specify more than 2 inputs the images are composited starting with the first input and the second and so on.</span></span>

<span data-ttu-id="29225-112">Dieser Effekt implementiert alle Modi mit der Mischungs Einheit der Grafikverarbeitungseinheit (Graphics Processing Unit, GPU).</span><span class="sxs-lookup"><span data-stu-id="29225-112">This effect implements all of the modes using the blending unit of the graphics processing unit (GPU).</span></span>

<span data-ttu-id="29225-113">Die CLSID für diesen Effekt ist CLSID \_ D2D1Composite.</span><span class="sxs-lookup"><span data-stu-id="29225-113">The CLSID for this effect is CLSID\_D2D1Composite.</span></span>

-   [<span data-ttu-id="29225-114">Beispiel Bild</span><span class="sxs-lookup"><span data-stu-id="29225-114">Example image</span></span>](#example-image)
-   [<span data-ttu-id="29225-115">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="29225-115">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="29225-116">Modustypen</span><span class="sxs-lookup"><span data-stu-id="29225-116">Mode types</span></span>](#mode-types)
-   [<span data-ttu-id="29225-117">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="29225-117">Sample code</span></span>](#sample-code)
-   [<span data-ttu-id="29225-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29225-118">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="29225-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="29225-119">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="29225-120">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="29225-120">Example image</span></span>

<span data-ttu-id="29225-121">Das Bild hier zeigt zwei abgerundete Rechtecke mit der gleichen Größe, die sich überlappen.</span><span class="sxs-lookup"><span data-stu-id="29225-121">The image here shows 2 rounded rectangles of the same size that overlap.</span></span> <span data-ttu-id="29225-122">Das blaue Rechteck ist die Quelle, und das rote Rechteck ist das Ziel.</span><span class="sxs-lookup"><span data-stu-id="29225-122">The blue rectangle is the source and the red rectangle is the destination.</span></span> <span data-ttu-id="29225-123">Die Bilder wurden mit dem Quell-über-Modus zusammengesetzt.</span><span class="sxs-lookup"><span data-stu-id="29225-123">The images were composited with the Source Over mode.</span></span>

![ein Beispiel Bild, das zwei abgerundete Rechtecke mit der gleichen Größe anzeigt, die sich über die Quelle über den Modus überlappen.](images/composite-over.png)

<span data-ttu-id="29225-125">Im folgenden finden Sie ein weiteres Beispiel für die Verwendung des Standardmodus.</span><span class="sxs-lookup"><span data-stu-id="29225-125">Here's another example using the default mode.</span></span>



| <span data-ttu-id="29225-126">Vor Bild 1</span><span class="sxs-lookup"><span data-stu-id="29225-126">Before image 1</span></span>                                                          |
|-------------------------------------------------------------------------|
| ![das erste Quell Bild vor dem Effekt.](images/default-before.jpg) |
| <span data-ttu-id="29225-128">Vor Abbildung 2</span><span class="sxs-lookup"><span data-stu-id="29225-128">Before image 2</span></span>                                                          |
| ![Das zweite Bild vor dem Effekt.](images/3-composite(2of2).png)    |
| <span data-ttu-id="29225-130">Nach</span><span class="sxs-lookup"><span data-stu-id="29225-130">After</span></span>                                                                   |
| ![das Bild nach der Transformation.](images/3-composite.png)               |



 


```C++
ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInput(0, bitmap);
compositeEffect->SetInput(1, bitmapTwo);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="29225-132">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="29225-132">Effect properties</span></span>



| <span data-ttu-id="29225-133">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="29225-133">Display name and index enumeration</span></span>                     | <span data-ttu-id="29225-134">Typ und Standardwert</span><span class="sxs-lookup"><span data-stu-id="29225-134">Type and default value</span></span>                                                          | <span data-ttu-id="29225-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29225-135">Description</span></span>                   |
|--------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="29225-136">Mode</span><span class="sxs-lookup"><span data-stu-id="29225-136">Mode</span></span><br/> <span data-ttu-id="29225-137">D2D1- \_ Verbund- \_ Prop- \_ Modus</span><span class="sxs-lookup"><span data-stu-id="29225-137">D2D1\_COMPOSITE\_PROP\_MODE</span></span><br/> | <span data-ttu-id="29225-138">D2D1- \_ Verbund \_ Modus</span><span class="sxs-lookup"><span data-stu-id="29225-138">D2D1\_COMPOSITE\_MODE</span></span><br/> <span data-ttu-id="29225-139">D2D1-Quelle für den zusammen \_ gesetzten \_ Modus \_ \_</span><span class="sxs-lookup"><span data-stu-id="29225-139">D2D1\_COMPOSITE\_MODE\_SOURCE\_OVER</span></span><br/> | <span data-ttu-id="29225-140">Der für den Effekt verwendete Modus.</span><span class="sxs-lookup"><span data-stu-id="29225-140">The mode used for the effect.</span></span> |



 

## <a name="mode-types"></a><span data-ttu-id="29225-141">Modustypen</span><span class="sxs-lookup"><span data-stu-id="29225-141">Mode types</span></span>

<span data-ttu-id="29225-142">In der hier aufgeführten Tabelle werden die Modi dieses Effekts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="29225-142">The table here shows the modes of this effect.</span></span> <span data-ttu-id="29225-143">Die in der Tabelle aufgeführten Gleichungen verwenden die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="29225-143">The equations listed in the table use these elements:</span></span>

-   <span data-ttu-id="29225-144">O = Ausgabe</span><span class="sxs-lookup"><span data-stu-id="29225-144">O = Output</span></span>
-   <span data-ttu-id="29225-145">S = Quelle</span><span class="sxs-lookup"><span data-stu-id="29225-145">S = Source</span></span>
-   <span data-ttu-id="29225-146">Sa = quellalpha</span><span class="sxs-lookup"><span data-stu-id="29225-146">SA = Source Alpha</span></span>
-   <span data-ttu-id="29225-147">D = Ziel</span><span class="sxs-lookup"><span data-stu-id="29225-147">D = Destination</span></span>
-   <span data-ttu-id="29225-148">Da = zielalpha</span><span class="sxs-lookup"><span data-stu-id="29225-148">DA = Destination Alpha</span></span>



| <span data-ttu-id="29225-149">Enumeration</span><span class="sxs-lookup"><span data-stu-id="29225-149">Enumeration</span></span>                                  | <span data-ttu-id="29225-150">Gleichung</span><span class="sxs-lookup"><span data-stu-id="29225-150">Equation</span></span>                          | <span data-ttu-id="29225-151">Größe der Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="29225-151">Output Bitmap Size</span></span>                                                                                      |
|----------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29225-152">D2D1-Quelle für den zusammen \_ gesetzten \_ Modus \_ \_</span><span class="sxs-lookup"><span data-stu-id="29225-152">D2D1\_COMPOSITE\_MODE\_SOURCE\_OVER</span></span>          | <span data-ttu-id="29225-153">O = S + (1 SA) \* D</span><span class="sxs-lookup"><span data-stu-id="29225-153">O = S + (1   SA) \* D</span></span>             | <span data-ttu-id="29225-154">Union von Quell-und Ziel Bitmaps</span><span class="sxs-lookup"><span data-stu-id="29225-154">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="29225-155">D2D1 \_ - \_ \_ Ziel im Verbund Modus \_ über</span><span class="sxs-lookup"><span data-stu-id="29225-155">D2D1\_COMPOSITE\_MODE\_DESTINATION\_OVER</span></span>     | <span data-ttu-id="29225-156">O = (1 da) \* S + D</span><span class="sxs-lookup"><span data-stu-id="29225-156">O = (1   DA) \* S + D</span></span>             | <span data-ttu-id="29225-157">Union von Quell-und Ziel Bitmaps</span><span class="sxs-lookup"><span data-stu-id="29225-157">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="29225-158">D2D1 \_ \_ Quelle im zusammengesetzten Modus \_ \_ in</span><span class="sxs-lookup"><span data-stu-id="29225-158">D2D1\_COMPOSITE\_MODE\_SOURCE\_IN</span></span>            | <span data-ttu-id="29225-159">O = da \* S</span><span class="sxs-lookup"><span data-stu-id="29225-159">O = DA \* S</span></span>                       | <span data-ttu-id="29225-160">Schnittmenge von Quell-und Ziel Bitmaps</span><span class="sxs-lookup"><span data-stu-id="29225-160">Intersection of source and destination bitmaps</span></span>                                                          |
| <span data-ttu-id="29225-161">D2D1 \_ - \_ \_ Ziel im Verbund Modus \_ in</span><span class="sxs-lookup"><span data-stu-id="29225-161">D2D1\_COMPOSITE\_MODE\_DESTINATION\_IN</span></span>       | <span data-ttu-id="29225-162">O = SA \* D</span><span class="sxs-lookup"><span data-stu-id="29225-162">O = SA \* D</span></span>                       | <span data-ttu-id="29225-163">Schnittmenge von Quell-und Ziel Bitmaps</span><span class="sxs-lookup"><span data-stu-id="29225-163">Intersection of source and destination bitmaps</span></span>                                                          |
| <span data-ttu-id="29225-164">D2D1-Quelle für zusammen \_ gesetzten \_ Modus \_ \_</span><span class="sxs-lookup"><span data-stu-id="29225-164">D2D1\_COMPOSITE\_MODE\_SOURCE\_OUT</span></span>           | <span data-ttu-id="29225-165">O = (1-da) \* S</span><span class="sxs-lookup"><span data-stu-id="29225-165">O = (1 - DA) \* S</span></span>                 | <span data-ttu-id="29225-166">Der Bereich der Quell Bitmap.</span><span class="sxs-lookup"><span data-stu-id="29225-166">Region of the source bitmap</span></span>                                                                             |
| <span data-ttu-id="29225-167">D2D1-Ziel für den zusammen \_ gesetzten \_ Modus \_ \_</span><span class="sxs-lookup"><span data-stu-id="29225-167">D2D1\_COMPOSITE\_MODE\_DESTINATION\_OUT</span></span>      | <span data-ttu-id="29225-168">O = (1-SA) \* D</span><span class="sxs-lookup"><span data-stu-id="29225-168">O = (1 - SA) \* D</span></span>                 | <span data-ttu-id="29225-169">Der Bereich der Ziel Bitmap.</span><span class="sxs-lookup"><span data-stu-id="29225-169">Region of the destination bitmap</span></span>                                                                        |
| <span data-ttu-id="29225-170">D2D1-Quelle im zusammen \_ gesetzten \_ Modus \_ \_</span><span class="sxs-lookup"><span data-stu-id="29225-170">D2D1\_COMPOSITE\_MODE\_SOURCE\_ATOP</span></span>          | <span data-ttu-id="29225-171">O = da \* S + (1-SA) \* D</span><span class="sxs-lookup"><span data-stu-id="29225-171">O = DA \* S + (1 - SA) \* D</span></span>       | <span data-ttu-id="29225-172">Der Bereich der Ziel Bitmap.</span><span class="sxs-lookup"><span data-stu-id="29225-172">Region of the destination bitmap</span></span>                                                                        |
| <span data-ttu-id="29225-173">D2D1-Ziel für den \_ Verbund \_ Modus oberhalb \_ \_</span><span class="sxs-lookup"><span data-stu-id="29225-173">D2D1\_COMPOSITE\_MODE\_DESTINATION\_ATOP</span></span>     | <span data-ttu-id="29225-174">O = (1-da) \* S + SA \* D</span><span class="sxs-lookup"><span data-stu-id="29225-174">O = (1 - DA) \* S + SA \* D</span></span>       | <span data-ttu-id="29225-175">Der Bereich der Quell Bitmap.</span><span class="sxs-lookup"><span data-stu-id="29225-175">Region of the source bitmap</span></span>                                                                             |
| <span data-ttu-id="29225-176">D2D1 im zusammen \_ gesetzten \_ Modus- \_ Xor</span><span class="sxs-lookup"><span data-stu-id="29225-176">D2D1\_COMPOSITE\_MODE\_XOR</span></span>                   | <span data-ttu-id="29225-177">O = (1-da) \* S + (1-SA) \* D</span><span class="sxs-lookup"><span data-stu-id="29225-177">O = (1 - DA) \* S + (1 - SA) \* D</span></span> | <span data-ttu-id="29225-178">Union von Quell-und Ziel Bitmaps</span><span class="sxs-lookup"><span data-stu-id="29225-178">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="29225-179">D2D1 \_ Composite- \_ Modus \_ Plus</span><span class="sxs-lookup"><span data-stu-id="29225-179">D2D1\_COMPOSITE\_MODE\_PLUS</span></span>                  | <span data-ttu-id="29225-180">O = S + D</span><span class="sxs-lookup"><span data-stu-id="29225-180">O = S + D</span></span>                         | <span data-ttu-id="29225-181">Union von Quell-und Ziel Bitmaps</span><span class="sxs-lookup"><span data-stu-id="29225-181">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="29225-182">D2D1 \_ - \_ \_ Quell \_ Kopie im zusammengesetzten Modus</span><span class="sxs-lookup"><span data-stu-id="29225-182">D2D1\_COMPOSITE\_MODE\_SOURCE\_COPY</span></span>          | <span data-ttu-id="29225-183">O = S</span><span class="sxs-lookup"><span data-stu-id="29225-183">O = S</span></span>                             | <span data-ttu-id="29225-184">Der Bereich der Quell Bitmap.</span><span class="sxs-lookup"><span data-stu-id="29225-184">Region of the source bitmap</span></span>                                                                             |
| <span data-ttu-id="29225-185">D2D1 \_ \_ \_ gebundene \_ Quell \_ Kopie im zusammengesetzten Modus</span><span class="sxs-lookup"><span data-stu-id="29225-185">D2D1\_COMPOSITE\_MODE\_BOUNDED\_SOURCE\_COPY</span></span> | <span data-ttu-id="29225-186">O = S (nur, wenn Quelle vorhanden ist)</span><span class="sxs-lookup"><span data-stu-id="29225-186">O = S (only where source exists)</span></span>  | <span data-ttu-id="29225-187">Union von Quell-und Ziel Bitmaps.</span><span class="sxs-lookup"><span data-stu-id="29225-187">Union of source and destination bitmaps.</span></span> <span data-ttu-id="29225-188">Das Ziel wird nicht überschrieben, wenn die Quelle nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="29225-188">Destination is not overwritten where the source doesn't exist.</span></span> |
| <span data-ttu-id="29225-189">D2D1-Maske im zusammen \_ gesetzten \_ Modus \_ \_ umkehren</span><span class="sxs-lookup"><span data-stu-id="29225-189">D2D1\_COMPOSITE\_MODE\_MASK\_INVERT</span></span>          | <span data-ttu-id="29225-190">O = (1 D) \* S + (1 SA) \* D</span><span class="sxs-lookup"><span data-stu-id="29225-190">O = (1   D) \* S + (1   SA) \* D</span></span>  | <span data-ttu-id="29225-191">Union von Quell-und Ziel Bitmaps. Die Alpha Werte sind unverändert.</span><span class="sxs-lookup"><span data-stu-id="29225-191">Union of source and destination bitmaps.The alpha values are unchanged.</span></span>                                 |



 

<span data-ttu-id="29225-192">Die Abbildung zeigt ein Beispiel für jeden der Modi mit Bildern mit einer Deckkraft von 1,0 oder 0,5.</span><span class="sxs-lookup"><span data-stu-id="29225-192">The figure here shows an example of each of the modes with images that have an opacity of 1.0 or 0.5.</span></span>

![ein Beispiel Bild für jeden Modus, bei dem die Deckkraft auf 1,0 oder 0,5 festgelegt ist.](images/composite-types.png)

## <a name="sample-code"></a><span data-ttu-id="29225-194">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="29225-194">Sample code</span></span>

<span data-ttu-id="29225-195">Um ein Beispiel für diesen Effekt zu erhalten, laden Sie das [Beispiel Direct2D Composite Effect Modes](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample)herunter.</span><span class="sxs-lookup"><span data-stu-id="29225-195">For an example of this effect, download the [Direct2D composite effect modes sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).</span></span>

## <a name="requirements"></a><span data-ttu-id="29225-196">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29225-196">Requirements</span></span>



| <span data-ttu-id="29225-197">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29225-197">Requirement</span></span> | <span data-ttu-id="29225-198">Wert</span><span class="sxs-lookup"><span data-stu-id="29225-198">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="29225-199">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29225-199">Minimum supported client</span></span> | <span data-ttu-id="29225-200">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29225-200">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="29225-201">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29225-201">Minimum supported server</span></span> | <span data-ttu-id="29225-202">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29225-202">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="29225-203">Header</span><span class="sxs-lookup"><span data-stu-id="29225-203">Header</span></span>                   | <span data-ttu-id="29225-204">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="29225-204">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="29225-205">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="29225-205">Library</span></span>                  | <span data-ttu-id="29225-206">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="29225-206">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="29225-207">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="29225-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29225-208">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="29225-208">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

