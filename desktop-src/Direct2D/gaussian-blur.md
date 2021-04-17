---
title: Gauscher Weichzeichnereffekt
description: Verwenden Sie den gauischen Weichzeichnereffekt, um auf der Grundlage der gauschen Funktion für das gesamte Eingabebild einen weich Zeiger zu erstellen.
ms.assetid: 6B8C9A0A-81D6-4CC2-B30B-995D4C2E59FC
keywords:
- Gauscher Weichzeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbe8b309a498315e389be45d382eca3ee1b98ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104558451"
---
# <a name="gaussian-blur-effect"></a><span data-ttu-id="10f57-104">Gauscher Weichzeichnereffekt</span><span class="sxs-lookup"><span data-stu-id="10f57-104">Gaussian blur effect</span></span>

<span data-ttu-id="10f57-105">Verwenden Sie den gauischen Weichzeichnereffekt, um auf der Grundlage der gauschen Funktion für das gesamte Eingabebild einen weich Zeiger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="10f57-105">Use the Gaussian blur effect to create a blur based on the Gaussian function over the entire input image.</span></span>

<span data-ttu-id="10f57-106">Mithilfe dieses Effekts können Sie Leuchten-und Schlag Schatten erstellen und mithilfe des zusammen [gesetzten](composite.md) Effekts das Ergebnis auf das ursprüngliche Bild anwenden.</span><span class="sxs-lookup"><span data-stu-id="10f57-106">You can use this effect to create glows and drop shadows and use the [composite](composite.md) effect to apply the result to the original image.</span></span> <span data-ttu-id="10f57-107">Es ist nützlich bei der Foto Verarbeitung für Filter wie Highlights und Shadows.</span><span class="sxs-lookup"><span data-stu-id="10f57-107">It is useful in photo processing for filters like highlights and shadows.</span></span> <span data-ttu-id="10f57-108">Sie können die Ausgabe dieses Effekts für die Eingabe in Beleuchtungseffekte verwenden, wie z. b. die Glanz [Beleuchtung](specular-lighting.md) oder [diffuse Beleuchtungs](diffuse-lighting.md) Effekte, da der Alphakanal verschwommen ist, und die Beleuchtungseffekte verwenden den Alphakanal, um die Oberflächengeometrie als Höhen Zuordnung zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="10f57-108">You can use the output of this effect for input into lighting effects, like the [Specular Lighting](specular-lighting.md) or [Diffuse Lighting](diffuse-lighting.md) effects, because the alpha channel is blurred, too and lighting effects use the alpha channel to determine surface geometry as a height map.</span></span>

<span data-ttu-id="10f57-109">Dieser Effekt wird vom integrierten [Schatten](drop-shadow.md) Effekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="10f57-109">This effect is used by the built-in [Shadow](drop-shadow.md) effect.</span></span>

<span data-ttu-id="10f57-110">Die CLSID für diesen Effekt ist CLSID \_ D2D1GaussianBlur.</span><span class="sxs-lookup"><span data-stu-id="10f57-110">The CLSID for this effect is CLSID\_D2D1GaussianBlur.</span></span>

-   [<span data-ttu-id="10f57-111">Beispiel Bild</span><span class="sxs-lookup"><span data-stu-id="10f57-111">Example image</span></span>](#example-image)
-   [<span data-ttu-id="10f57-112">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="10f57-112">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="10f57-113">Optimierungs Modi</span><span class="sxs-lookup"><span data-stu-id="10f57-113">Optimization modes</span></span>](#optimization-modes)
-   [<span data-ttu-id="10f57-114">Rahmen Modi</span><span class="sxs-lookup"><span data-stu-id="10f57-114">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="10f57-115">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="10f57-115">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="10f57-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10f57-116">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="10f57-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="10f57-117">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="10f57-118">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="10f57-118">Example image</span></span>



| <span data-ttu-id="10f57-119">Vorher</span><span class="sxs-lookup"><span data-stu-id="10f57-119">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)   |
| <span data-ttu-id="10f57-121">Nach</span><span class="sxs-lookup"><span data-stu-id="10f57-121">After</span></span>                                                        |
| ![das Bild nach der Transformation.](images/1-gaussianblur.png) |



 


```C++
ComPtr<ID2D1Effect> gaussianBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect);

gaussianBlurEffect->SetInput(0, bitmap);
gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 3.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(gaussianBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="10f57-123">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="10f57-123">Effect properties</span></span>



| <span data-ttu-id="10f57-124">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="10f57-124">Display name and index enumeration</span></span>                                                    | <span data-ttu-id="10f57-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10f57-125">Description</span></span>                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10f57-126">StandardDeviation (Standardabweichung)</span><span class="sxs-lookup"><span data-stu-id="10f57-126">StandardDeviation</span></span><br/> <span data-ttu-id="10f57-127">D2D1 \_ gausianweichungs- \_ \_ Standard \_ Abweichung</span><span class="sxs-lookup"><span data-stu-id="10f57-127">D2D1\_GAUSSIANBLUR\_PROP\_STANDARD\_DEVIATION</span></span><br/> | <span data-ttu-id="10f57-128">Die auf das Bild anzuwendende Menge an weich.</span><span class="sxs-lookup"><span data-stu-id="10f57-128">The amount of blur to be applied to the image.</span></span> <span data-ttu-id="10f57-129">Sie können den weichungs Radius des Kernels berechnen, indem Sie die Standardabweichung um 3 multiplizieren.</span><span class="sxs-lookup"><span data-stu-id="10f57-129">You can compute the blur radius of the kernel by multiplying the standard deviation by 3.</span></span> <span data-ttu-id="10f57-130">Die Einheiten der Standardabweichung und des weichungs RADIUS sind Dips.</span><span class="sxs-lookup"><span data-stu-id="10f57-130">The units of both the standard deviation and blur radius are DIPs.</span></span> <span data-ttu-id="10f57-131">Mit einem Wert von NULL Dips wird dieser effektvoll ständig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="10f57-131">A value of zero DIPs disables this effect entirely.</span></span> <span data-ttu-id="10f57-132">Der Typ ist "float".</span><span class="sxs-lookup"><span data-stu-id="10f57-132">The type is FLOAT.</span></span><br/> <span data-ttu-id="10f57-133">Der Standardwert ist 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="10f57-133">The default value is 3.0f.</span></span><br/> |
| <span data-ttu-id="10f57-134">Optimization</span><span class="sxs-lookup"><span data-stu-id="10f57-134">Optimization</span></span><br/> <span data-ttu-id="10f57-135">D2D1 \_ gausianweich- \_ Prop- \_ Optimierung</span><span class="sxs-lookup"><span data-stu-id="10f57-135">D2D1\_GAUSSIANBLUR\_PROP\_OPTIMIZATION</span></span><br/>             | <span data-ttu-id="10f57-136">Der Optimierungs Modus.</span><span class="sxs-lookup"><span data-stu-id="10f57-136">The optimization mode.</span></span> <span data-ttu-id="10f57-137">Weitere Informationen finden Sie unter [Optimierungs Modi](#optimization-modes) .</span><span class="sxs-lookup"><span data-stu-id="10f57-137">See [Optimization modes](#optimization-modes) for more info.</span></span> <span data-ttu-id="10f57-138">Der Typ ist "D2D1 \_ gauanweich- \_ Optimierung".</span><span class="sxs-lookup"><span data-stu-id="10f57-138">The type is D2D1\_GAUSSIANBLUR\_OPTIMIZATION.</span></span><br/> <span data-ttu-id="10f57-139">Der Standardwert ist "D2D1 \_ gauanweich- \_ Optimierung" \_ .</span><span class="sxs-lookup"><span data-stu-id="10f57-139">The default value is D2D1\_GAUSSIANBLUR\_OPTIMIZATION\_BALANCED.</span></span><br/>                                                                                                            |
| <span data-ttu-id="10f57-140">Bordermode</span><span class="sxs-lookup"><span data-stu-id="10f57-140">BorderMode</span></span><br/> <span data-ttu-id="10f57-141">D2D1 \_ gausianweich-Prop-Rahmen \_ \_ \_ Modus</span><span class="sxs-lookup"><span data-stu-id="10f57-141">D2D1\_GAUSSIANBLUR\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="10f57-142">Der Modus, der verwendet wird, um den Rahmen des Bilds zu berechnen, weich oder hart.</span><span class="sxs-lookup"><span data-stu-id="10f57-142">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="10f57-143">Weitere Informationen finden Sie unter [Border Modes](#border-modes) .</span><span class="sxs-lookup"><span data-stu-id="10f57-143">See [Border modes](#border-modes) for more info.</span></span> <br/> <span data-ttu-id="10f57-144">Der Typ ist der D2D1 \_ gausid- \_ Rahmen \_ Modus.</span><span class="sxs-lookup"><span data-stu-id="10f57-144">The type is D2D1\_GAUSSIANBLUR\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="10f57-145">Der Standardwert ist D2D1 \_ Border \_ Mode \_ Soft.</span><span class="sxs-lookup"><span data-stu-id="10f57-145">The default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/>                                                                                   |



 

## <a name="optimization-modes"></a><span data-ttu-id="10f57-146">Optimierungs Modi</span><span class="sxs-lookup"><span data-stu-id="10f57-146">Optimization modes</span></span>



| <span data-ttu-id="10f57-147">Name</span><span class="sxs-lookup"><span data-stu-id="10f57-147">Name</span></span>                                          | <span data-ttu-id="10f57-148">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10f57-148">Description</span></span>                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10f57-149">D2D1- \_ \_ Optimierungs Geschwindigkeit für directionalblur \_</span><span class="sxs-lookup"><span data-stu-id="10f57-149">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_SPEED</span></span>    | <span data-ttu-id="10f57-150">Wendet interne Optimierungen an, wie z. b. die vorab Skalierung bei relativ kleinen Radii.</span><span class="sxs-lookup"><span data-stu-id="10f57-150">Applies internal optimizations such as pre-scaling at relatively small radii.</span></span> <span data-ttu-id="10f57-151">Verwendet lineare Filterung.</span><span class="sxs-lookup"><span data-stu-id="10f57-151">Uses linear filtering.</span></span>                                  |
| <span data-ttu-id="10f57-152">D2D1 \_ directionalblur- \_ Optimierung \_ ausgeglichen</span><span class="sxs-lookup"><span data-stu-id="10f57-152">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED</span></span> | <span data-ttu-id="10f57-153">Verwendet die gleichen Optimierungs Schwellenwerte wie der Geschwindigkeits Modus, verwendet jedoch die drei lineare Filterung.</span><span class="sxs-lookup"><span data-stu-id="10f57-153">Uses the same optimization thresholds as Speed mode, but uses trilinear filtering.</span></span>                                                    |
| <span data-ttu-id="10f57-154">D2D1 \_ directionalblur- \_ Optimierungs \_ Qualität</span><span class="sxs-lookup"><span data-stu-id="10f57-154">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_QUALITY</span></span>  | <span data-ttu-id="10f57-155">Verwendet nur interne Optimierungen mit großen weichungs Radien, bei denen es weniger wahrscheinlich ist, dass Näherungen sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="10f57-155">Only uses internal optimizations with large blur radii, where approximations are less likely to be visible.</span></span> <span data-ttu-id="10f57-156">Verwendet die drei lineare Filterung.</span><span class="sxs-lookup"><span data-stu-id="10f57-156">Uses trilinear filtering.</span></span> |



 

## <a name="border-modes"></a><span data-ttu-id="10f57-157">Rahmen Modi</span><span class="sxs-lookup"><span data-stu-id="10f57-157">Border modes</span></span>



| <span data-ttu-id="10f57-158">Name</span><span class="sxs-lookup"><span data-stu-id="10f57-158">Name</span></span>                     | <span data-ttu-id="10f57-159">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10f57-159">Description</span></span>                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10f57-160">D2D1 \_ Border \_ Mode \_ Soft</span><span class="sxs-lookup"><span data-stu-id="10f57-160">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="10f57-161">Der Effekt füllt das Bild mit transparenten schwarzen Pixeln auf, da es den Weichzeichnerkernel anwendet, was zu einem weichen Rand führt.</span><span class="sxs-lookup"><span data-stu-id="10f57-161">The effect pads the image with transparent black pixels as it applies the blur kernel, resulting in a soft edge.</span></span> <br/>                                                                                             |
| <span data-ttu-id="10f57-162">D2D1 \_ Rahmen \_ Modus \_ hart</span><span class="sxs-lookup"><span data-stu-id="10f57-162">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="10f57-163">Der Effekt bindet die Ausgabe an die Größe des Eingabe Bilds.</span><span class="sxs-lookup"><span data-stu-id="10f57-163">The effect clamps the output to the size of the input image.</span></span> <span data-ttu-id="10f57-164">Wenn der Effekt den Weichzeichnerkernel anwendet, erweitert er das Eingabebild mit einer Rahmen Transformation für einen Spiegelungs Typ für Beispiele außerhalb der Eingabe Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="10f57-164">When the effect applies the blur kernel, it extends the input image with a mirror-type border transform for samples outside of the input bounds.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="10f57-165">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="10f57-165">Output bitmap</span></span>

<span data-ttu-id="10f57-166">Die Ausgabe dieses Effekts kann größer als die Eingabe Bitmap sein, die auf dem weichzeichenradius und dem Rahmen Modus basiert.</span><span class="sxs-lookup"><span data-stu-id="10f57-166">The output of this effect can be larger than the input bitmap based on the blur radius and the border mode.</span></span> <span data-ttu-id="10f57-167">Wenn der Border-Modus auf D2D1 \_ Border Mode Soft festgelegt ist \_ , wird \_ die s imale der Ausgabe Bitmap um die Größe des Weichzeichnerkernels vergrößert, dargestellt in Pixel.</span><span class="sxs-lookup"><span data-stu-id="10f57-167">If the border mode is set to D2D1\_BORDER\_MODE\_SOFT the s ize of the output bitmap increases by the size of the blur kernel, represented in pixels.</span></span> <span data-ttu-id="10f57-168">Diese Tabelle stellt eine Gleichung bereit, mit der Sie die Ausgabe Bitmap berechnen können.</span><span class="sxs-lookup"><span data-stu-id="10f57-168">This table provides an equation that you can use to compute the output bitmap.</span></span>

`Output bitmap growth (X and Y) = StandardDeviation  (DIPs)*6*((User DPI)/96)`

<span data-ttu-id="10f57-169">Wenn also die Bildgröße um 10 Pixel in jeder Richtung zunimmt, befindet sich die obere linke Ecke des Bilds bei (-5,-5), während die untere Rechte bei (105, 105) liegt.</span><span class="sxs-lookup"><span data-stu-id="10f57-169">So, if the image size increases by 10 pixels in each direction the upper left corner of the image will be located at (-5, -5) while the lower right will be at (105, 105).</span></span>

## <a name="requirements"></a><span data-ttu-id="10f57-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10f57-170">Requirements</span></span>



| <span data-ttu-id="10f57-171">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10f57-171">Requirement</span></span> | <span data-ttu-id="10f57-172">Wert</span><span class="sxs-lookup"><span data-stu-id="10f57-172">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="10f57-173">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="10f57-173">Minimum supported client</span></span> | <span data-ttu-id="10f57-174">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10f57-174">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="10f57-175">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="10f57-175">Minimum supported server</span></span> | <span data-ttu-id="10f57-176">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10f57-176">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="10f57-177">Header</span><span class="sxs-lookup"><span data-stu-id="10f57-177">Header</span></span>                   | <span data-ttu-id="10f57-178">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="10f57-178">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="10f57-179">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="10f57-179">Library</span></span>                  | <span data-ttu-id="10f57-180">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="10f57-180">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="10f57-181">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="10f57-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10f57-182">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="10f57-182">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

