---
title: Richtungsweisendes Effekt
description: Der direktionale Weichzeichnereffekt ähnelt dem gauischen weichungs Wert, mit der Ausnahme, dass Sie den Weichzeichner in eine bestimmte Richtung neigen können.
ms.assetid: 59328FA4-5C27-4A81-AAB2-C5B25B3615C6
keywords:
- direktionaler weich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e1c098d17929563cf69f4e61416fa0d93a88dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739856"
---
# <a name="directional-blur-effect"></a><span data-ttu-id="7d601-104">Richtungsweisendes Effekt</span><span class="sxs-lookup"><span data-stu-id="7d601-104">Directional blur effect</span></span>

<span data-ttu-id="7d601-105">Der direktionale Weichzeichnereffekt ähnelt dem [gauischen](gaussian-blur.md)weichungs Wert, mit der Ausnahme, dass Sie den Weichzeichner in eine bestimmte Richtung neigen können.</span><span class="sxs-lookup"><span data-stu-id="7d601-105">The directional blur effect is similar to [Gaussian blur](gaussian-blur.md), except you can skew the blur in a particular direction.</span></span> <span data-ttu-id="7d601-106">Mit diesem Effekt können Sie sehen, wie sich das Bild in Bewegung befindet oder ein animiertes Bild hervorgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="7d601-106">You can use this effect to make an image look as if it is in motion or to emphasize an animated image.</span></span>

<span data-ttu-id="7d601-107">Die CLSID für diesen Effekt ist CLSID \_ D2D1DirectionalBlur.</span><span class="sxs-lookup"><span data-stu-id="7d601-107">The CLSID for this effect is CLSID\_D2D1DirectionalBlur.</span></span>

-   [<span data-ttu-id="7d601-108">Beispiel Bild</span><span class="sxs-lookup"><span data-stu-id="7d601-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="7d601-109">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7d601-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="7d601-110">Optimierungs Modi</span><span class="sxs-lookup"><span data-stu-id="7d601-110">Optimization modes</span></span>](#optimization-modes)
-   [<span data-ttu-id="7d601-111">Rahmen Modi</span><span class="sxs-lookup"><span data-stu-id="7d601-111">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="7d601-112">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="7d601-112">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="7d601-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d601-113">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="7d601-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7d601-114">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="7d601-115">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="7d601-115">Example image</span></span>



| <span data-ttu-id="7d601-116">Vorher</span><span class="sxs-lookup"><span data-stu-id="7d601-116">Before</span></span>                                                          |
|-----------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)      |
| <span data-ttu-id="7d601-118">Nach</span><span class="sxs-lookup"><span data-stu-id="7d601-118">After</span></span>                                                           |
| ![das Bild nach der Transformation.](images/2-directionalblur.png) |



 


```C++
ComPtr<ID2D1Effect> directionalBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DirectionalBlur, &directionalBlurEffect);

directionalBlurEffect->SetInput(0, bitmap);
directionalBlurEffect->SetValue(D2D1_DIRECTIONALBLUR_PROP_STANDARD_DEVIATION, 7.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(directionalBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="7d601-120">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7d601-120">Effect properties</span></span>



| <span data-ttu-id="7d601-121">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="7d601-121">Display name and index enumeration</span></span>                                                       | <span data-ttu-id="7d601-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d601-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d601-123">StandardDeviation (Standardabweichung)</span><span class="sxs-lookup"><span data-stu-id="7d601-123">StandardDeviation</span></span><br/> <span data-ttu-id="7d601-124">D2D1 \_ directionalblur \_ Prop- \_ Standard \_ Abweichung</span><span class="sxs-lookup"><span data-stu-id="7d601-124">D2D1\_DIRECTIONALBLUR\_PROP\_STANDARD\_DEVIATION</span></span><br/> | <span data-ttu-id="7d601-125">Die auf das Bild anzuwendende Menge an weich.</span><span class="sxs-lookup"><span data-stu-id="7d601-125">The amount of blur to be applied to the image.</span></span> <span data-ttu-id="7d601-126">Sie können den weichungs Radius des Kernels berechnen, indem Sie die Standardabweichung um 3 multiplizieren.</span><span class="sxs-lookup"><span data-stu-id="7d601-126">You can compute the blur radius of the kernel by multiplying the standard deviation by 3.</span></span> <span data-ttu-id="7d601-127">Die Einheiten der Standardabweichung und des weichungs RADIUS sind Dips.</span><span class="sxs-lookup"><span data-stu-id="7d601-127">The units of both the standard deviation and blur radius are DIPs.</span></span> <span data-ttu-id="7d601-128">Durch den Wert 0 (null) wird dieser Effekt deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7d601-128">A value of 0 DIPs disables this effect.</span></span> <span data-ttu-id="7d601-129">Der Typ ist "float".</span><span class="sxs-lookup"><span data-stu-id="7d601-129">The type is FLOAT.</span></span><br/> <span data-ttu-id="7d601-130">Der Standardwert ist 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="7d601-130">The default value is 3.0f.</span></span><br/>                                                                            |
| <span data-ttu-id="7d601-131">Angle</span><span class="sxs-lookup"><span data-stu-id="7d601-131">Angle</span></span><br/> <span data-ttu-id="7d601-132">D2D1 \_ directionalweichungs \_ \_ Winkel</span><span class="sxs-lookup"><span data-stu-id="7d601-132">D2D1\_DIRECTIONALBLUR\_PROP\_ANGLE</span></span><br/>                           | <span data-ttu-id="7d601-133">Der Winkel des weichungs Winkels in Bezug auf die x-Achse, in Richtung gegen den Uhrzeigersinn.</span><span class="sxs-lookup"><span data-stu-id="7d601-133">The angle of the blur relative to the x-axis, in the counterclockwise direction.</span></span> <span data-ttu-id="7d601-134">Die Einheiten werden in Grad angegeben.</span><span class="sxs-lookup"><span data-stu-id="7d601-134">The units are specified in degrees.</span></span><br/> <span data-ttu-id="7d601-135">Der Weichzeichnerkernel wird zuerst mit dem gleichen Prozess wie für den [gauischen](gaussian-blur.md) Weichzeichnereffekt generiert.</span><span class="sxs-lookup"><span data-stu-id="7d601-135">The blur kernel is first generated using the same process as for the [Gaussian blur](gaussian-blur.md) effect.</span></span> <span data-ttu-id="7d601-136">Die Kernel Werte werden dann entsprechend dem weichzeichnerwinkel transformiert.</span><span class="sxs-lookup"><span data-stu-id="7d601-136">The kernel values are then transformed according to the blur angle.</span></span><br/> <span data-ttu-id="7d601-137">Der Typ ist "float".</span><span class="sxs-lookup"><span data-stu-id="7d601-137">The type is FLOAT.</span></span><br/> <span data-ttu-id="7d601-138">Der Standardwert ist 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="7d601-138">The default value is 0.0f.</span></span><br/> |
| <span data-ttu-id="7d601-139">Optimization</span><span class="sxs-lookup"><span data-stu-id="7d601-139">Optimization</span></span><br/> <span data-ttu-id="7d601-140">D2D1 \_ directionaloptimization- \_ Prop- \_ Optimierung</span><span class="sxs-lookup"><span data-stu-id="7d601-140">D2D1\_DIRECTIONALBLUR\_PROP\_OPTIMIZATION</span></span><br/>             | <span data-ttu-id="7d601-141">Der Optimierungs Modus.</span><span class="sxs-lookup"><span data-stu-id="7d601-141">The optimization mode.</span></span> <span data-ttu-id="7d601-142">Weitere Informationen finden Sie unter [Optimierungs Modi](#optimization-modes) .</span><span class="sxs-lookup"><span data-stu-id="7d601-142">See [Optimization modes](#optimization-modes) for more info.</span></span><br/> <span data-ttu-id="7d601-143">Der Typ ist "D2D1 \_ directionalblur \_ Optimization".</span><span class="sxs-lookup"><span data-stu-id="7d601-143">The type is D2D1\_DIRECTIONALBLUR\_OPTIMIZATION.</span></span><br/> <span data-ttu-id="7d601-144">Der Standardwert ist D2D1 \_ directionaloptimization \_ Optimization Balancing \_ ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="7d601-144">The default value is D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED.</span></span> <br/>                                                                                                                                                         |
| <span data-ttu-id="7d601-145">Bordermode</span><span class="sxs-lookup"><span data-stu-id="7d601-145">BorderMode</span></span><br/> <span data-ttu-id="7d601-146">D2D1 \_ directionalblur-Prop-Rahmen \_ \_ \_ Modus</span><span class="sxs-lookup"><span data-stu-id="7d601-146">D2D1\_DIRECTIONALBLUR\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="7d601-147">Der Modus, der verwendet wird, um den Rahmen des Bilds zu berechnen, weich oder hart.</span><span class="sxs-lookup"><span data-stu-id="7d601-147">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="7d601-148">Weitere Informationen finden Sie unter [Border Modes](#border-modes) .</span><span class="sxs-lookup"><span data-stu-id="7d601-148">See [Border modes](#border-modes) for more info.</span></span><br/> <span data-ttu-id="7d601-149">Der Typ ist "D2D1 \_ Border \_ Mode".</span><span class="sxs-lookup"><span data-stu-id="7d601-149">The type is D2D1\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="7d601-150">Der Standardwert ist D2D1 \_ Border \_ Mode \_ Soft.</span><span class="sxs-lookup"><span data-stu-id="7d601-150">The default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/>                                                                                                                                                                 |



 

## <a name="optimization-modes"></a><span data-ttu-id="7d601-151">Optimierungs Modi</span><span class="sxs-lookup"><span data-stu-id="7d601-151">Optimization modes</span></span>



| <span data-ttu-id="7d601-152">Name</span><span class="sxs-lookup"><span data-stu-id="7d601-152">Name</span></span>                                          | <span data-ttu-id="7d601-153">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d601-153">Description</span></span>                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d601-154">D2D1- \_ \_ Optimierungs Geschwindigkeit für directionalblur \_</span><span class="sxs-lookup"><span data-stu-id="7d601-154">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_SPEED</span></span>    | <span data-ttu-id="7d601-155">Wendet interne Optimierungen an, wie z. b. die vorab Skalierung bei relativ kleinen Radii.</span><span class="sxs-lookup"><span data-stu-id="7d601-155">Applies internal optimizations such as pre-scaling at relatively small radii.</span></span> <span data-ttu-id="7d601-156">Verwendet lineare Filterung.</span><span class="sxs-lookup"><span data-stu-id="7d601-156">Uses linear filtering.</span></span>                                  |
| <span data-ttu-id="7d601-157">D2D1 \_ directionalblur- \_ Optimierung \_ ausgeglichen</span><span class="sxs-lookup"><span data-stu-id="7d601-157">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED</span></span> | <span data-ttu-id="7d601-158">Verwendet die gleichen Optimierungs Schwellenwerte wie der Geschwindigkeits Modus, verwendet jedoch die drei lineare Filterung.</span><span class="sxs-lookup"><span data-stu-id="7d601-158">Uses the same optimization thresholds as Speed mode, but uses trilinear filtering.</span></span>                                                    |
| <span data-ttu-id="7d601-159">D2D1 \_ directionalblur- \_ Optimierungs \_ Qualität</span><span class="sxs-lookup"><span data-stu-id="7d601-159">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_QUALITY</span></span>  | <span data-ttu-id="7d601-160">Verwendet nur interne Optimierungen mit großen weichungs Radien, bei denen es weniger wahrscheinlich ist, dass Näherungen sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="7d601-160">Only uses internal optimizations with large blur radii, where approximations are less likely to be visible.</span></span> <span data-ttu-id="7d601-161">Verwendet die drei lineare Filterung.</span><span class="sxs-lookup"><span data-stu-id="7d601-161">Uses trilinear filtering.</span></span> |



 

## <a name="border-modes"></a><span data-ttu-id="7d601-162">Rahmen Modi</span><span class="sxs-lookup"><span data-stu-id="7d601-162">Border modes</span></span>



| <span data-ttu-id="7d601-163">Name</span><span class="sxs-lookup"><span data-stu-id="7d601-163">Name</span></span>                     | <span data-ttu-id="7d601-164">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d601-164">Description</span></span>                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d601-165">D2D1 \_ Border \_ Mode \_ Soft</span><span class="sxs-lookup"><span data-stu-id="7d601-165">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="7d601-166">Der Effekt füllt das Bild mit transparenten schwarzen Pixeln auf, da es den Weichzeichnerkernel anwendet, was zu einem weichen Rand führt.</span><span class="sxs-lookup"><span data-stu-id="7d601-166">The effect pads the image with transparent black pixels as it applies the blur kernel, resulting in a soft edge.</span></span> <br/>                                                                                             |
| <span data-ttu-id="7d601-167">D2D1 \_ Rahmen \_ Modus \_ hart</span><span class="sxs-lookup"><span data-stu-id="7d601-167">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="7d601-168">Der Effekt bindet die Ausgabe an die Größe des Eingabe Bilds.</span><span class="sxs-lookup"><span data-stu-id="7d601-168">The effect clamps the output to the size of the input image.</span></span> <span data-ttu-id="7d601-169">Wenn der Effekt den Weichzeichnerkernel anwendet, erweitert er das Eingabebild mit einer Rahmen Transformation für einen Spiegelungs Typ für Beispiele außerhalb der Eingabe Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="7d601-169">When the effect applies the blur kernel, it extends the input image with a mirror-type border transform for samples outside of the input bounds.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="7d601-170">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="7d601-170">Output bitmap</span></span>

<span data-ttu-id="7d601-171">Die Größe der Ausgabe Bitmap erhöht sich basierend auf der Standardabweichung, dem Winkel des Effekts und dem Rahmen Modus.</span><span class="sxs-lookup"><span data-stu-id="7d601-171">The size of the output bitmap increases based on the standard deviation, the angle of the effect, and the border mode.</span></span> <span data-ttu-id="7d601-172">Wenn der Border-Modus auf D2D1 \_ Border Mode Soft festgelegt ist \_ , wird \_ die Größe der Ausgabe Bitmap um die Größe des Weichzeichnerkernels erhöht, dargestellt in Pixel.</span><span class="sxs-lookup"><span data-stu-id="7d601-172">If the border mode is set to D2D1\_BORDER\_MODE\_SOFT the size of the output bitmap increases by the size of the blur kernel, represented in pixels.</span></span> <span data-ttu-id="7d601-173">Diese Gleichungen können verwendet werden, um die Größe der Ausgabe Bitmap zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="7d601-173">These equations can be used to calculate the size of the output bitmap.</span></span>



| <span data-ttu-id="7d601-174">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d601-174">Requirement</span></span> | <span data-ttu-id="7d601-175">Wert</span><span class="sxs-lookup"><span data-stu-id="7d601-175">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="7d601-176">Ergebnis der Ausgabe Bitmap X</span><span class="sxs-lookup"><span data-stu-id="7d601-176">Output Bitmap Growth X</span></span> | <span data-ttu-id="7d601-177">Standardabweichung (Dips) \* 6 \* ((Benutzer dpi)/96) \* cos (Winkel))</span><span class="sxs-lookup"><span data-stu-id="7d601-177">StandardDeviation (DIPs) \* 6 \* ((User DPI) / 96) \* cos(Angle))</span></span> |
| <span data-ttu-id="7d601-178">Ergebnis der Ausgabe Bitmap Y</span><span class="sxs-lookup"><span data-stu-id="7d601-178">Output Bitmap Growth Y</span></span> | <span data-ttu-id="7d601-179">Standardabweichung (Dips) \* 6 \* ((Benutzer dpi)/96) \* Sin (Winkel))</span><span class="sxs-lookup"><span data-stu-id="7d601-179">StandardDeviation (DIPs) \* 6 \* ((User DPI) / 96) \* sin(Angle))</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="7d601-180">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d601-180">Requirements</span></span>



| <span data-ttu-id="7d601-181">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d601-181">Requirement</span></span> | <span data-ttu-id="7d601-182">Wert</span><span class="sxs-lookup"><span data-stu-id="7d601-182">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7d601-183">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7d601-183">Minimum supported client</span></span> | <span data-ttu-id="7d601-184">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d601-184">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7d601-185">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7d601-185">Minimum supported server</span></span> | <span data-ttu-id="7d601-186">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d601-186">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7d601-187">Header</span><span class="sxs-lookup"><span data-stu-id="7d601-187">Header</span></span>                   | <span data-ttu-id="7d601-188">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="7d601-188">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="7d601-189">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7d601-189">Library</span></span>                  | <span data-ttu-id="7d601-190">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="7d601-190">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="7d601-191">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7d601-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d601-192">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="7d601-192">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

