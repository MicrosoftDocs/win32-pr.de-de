---
title: Schatteneffekt
description: Verwenden Sie den Schatteneffekt, um einen Schatten aus dem Alphakanal eines Bilds zu generieren.
ms.assetid: 53525584-10CF-46C2-9400-C4FB225D4693
keywords:
- Schatteneffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42fd8755078dd79f2b01b623b1839785beb3c3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340408"
---
# <a name="shadow-effect"></a><span data-ttu-id="b54e1-104">Schatteneffekt</span><span class="sxs-lookup"><span data-stu-id="b54e1-104">Shadow effect</span></span>

<span data-ttu-id="b54e1-105">Verwenden Sie den Schatteneffekt, um einen Schatten aus dem Alphakanal eines Bilds zu generieren.</span><span class="sxs-lookup"><span data-stu-id="b54e1-105">Use the shadow effect to generate a shadow from the alpha channel of an image.</span></span> <span data-ttu-id="b54e1-106">Der Schatten ist für höhere Alpha Werte transparenter und transparenter für niedrigere Alpha Werte.</span><span class="sxs-lookup"><span data-stu-id="b54e1-106">The shadow is more opaque for higher alpha values and more transparent for lower alpha values.</span></span> <span data-ttu-id="b54e1-107">Sie können den Grad der weich Zeichnung und die Farbe des Schattens festlegen.</span><span class="sxs-lookup"><span data-stu-id="b54e1-107">You can set the amount of blur and the color of the shadow.</span></span>

-   [<span data-ttu-id="b54e1-108">Beispiel Bild</span><span class="sxs-lookup"><span data-stu-id="b54e1-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="b54e1-109">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b54e1-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="b54e1-110">Optimierungs Modi</span><span class="sxs-lookup"><span data-stu-id="b54e1-110">Optimization modes</span></span>](#optimization-modes)
-   [<span data-ttu-id="b54e1-111">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="b54e1-111">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="b54e1-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b54e1-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="b54e1-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b54e1-113">Related topics</span></span>](#related-topics)

<span data-ttu-id="b54e1-114">Die CLSID für diesen Effekt ist CLSID \_ D2D1Shadow.</span><span class="sxs-lookup"><span data-stu-id="b54e1-114">The CLSID for this effect is CLSID\_D2D1Shadow.</span></span>

## <a name="example-image"></a><span data-ttu-id="b54e1-115">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="b54e1-115">Example image</span></span>

<span data-ttu-id="b54e1-116">Das Beispiel hier zeigt die Ausgabe des Schatten Effekts übersetzt und rechts mit dem Quell Bild am ursprünglichen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="b54e1-116">The example here shows the output of the shadow effect translated down and right with the source image composited over it in the original location.</span></span> <span data-ttu-id="b54e1-117">Der Schatteneffekt gibt nur den Schatten aus.</span><span class="sxs-lookup"><span data-stu-id="b54e1-117">The shadow effect only outputs the shadow.</span></span>



| <span data-ttu-id="b54e1-118">Vorher</span><span class="sxs-lookup"><span data-stu-id="b54e1-118">Before</span></span>                                                  |
|---------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/8-crop.png)      |
| <span data-ttu-id="b54e1-120">Nach</span><span class="sxs-lookup"><span data-stu-id="b54e1-120">After</span></span>                                                   |
| ![das Bild nach der Transformation.](images/25-shadow.png) |



 


```C++
ComPtr<ID2D1Effect> shadowEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Shadow, &shadowEffect);

shadowEffect->SetInput(0, bitmap);

// Shadow is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInputEffect(0, shadowEffect.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F::Translation(20, 20));

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, affineTransformEffect.Get());
compositeEffect->SetInput(2, bitmap);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="b54e1-122">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b54e1-122">Effect properties</span></span>



| <span data-ttu-id="b54e1-123">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="b54e1-123">Display name and index enumeration</span></span>                                                        | <span data-ttu-id="b54e1-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b54e1-124">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b54e1-125">Blurstandardabweichung</span><span class="sxs-lookup"><span data-stu-id="b54e1-125">BlurStandardDeviation</span></span><br/> <span data-ttu-id="b54e1-126">D2D1 \_ Shadow \_ Prop \_ - \_ Standard \_ Abweichung</span><span class="sxs-lookup"><span data-stu-id="b54e1-126">D2D1\_SHADOW\_PROP\_BLUR\_STANDARD\_DEVIATION</span></span><br/> | <span data-ttu-id="b54e1-127">Der auf den Alpha-Kanal des Bilds anzuwendende Wert.</span><span class="sxs-lookup"><span data-stu-id="b54e1-127">The amount of blur to be applied to the alpha channel of the image.</span></span> <span data-ttu-id="b54e1-128">Sie können den weichungs Radius des Kernels berechnen, indem Sie die Standardabweichung um 3 multiplizieren.</span><span class="sxs-lookup"><span data-stu-id="b54e1-128">You can compute the blur radius of the kernel by multiplying the standard deviation by 3.</span></span> <span data-ttu-id="b54e1-129">Die Einheiten der Standardabweichung und des weichungs RADIUS sind Dips.</span><span class="sxs-lookup"><span data-stu-id="b54e1-129">The units of both the standard deviation and blur radius are DIPs.</span></span><br/> <span data-ttu-id="b54e1-130">Diese Eigenschaft ist identisch mit der [Gaußscher Weichzeichner](gaussian-blur.md) Eigenschaft Standardabweichung.</span><span class="sxs-lookup"><span data-stu-id="b54e1-130">This property is the same as the [Gaussian Blur](gaussian-blur.md) standard deviation property.</span></span> <br/> <span data-ttu-id="b54e1-131">Der Typ ist "float".</span><span class="sxs-lookup"><span data-stu-id="b54e1-131">The type is FLOAT.</span></span><br/> <span data-ttu-id="b54e1-132">Der Standardwert ist 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="b54e1-132">The default value is 3.0f.</span></span><br/> |
| <span data-ttu-id="b54e1-133">Color</span><span class="sxs-lookup"><span data-stu-id="b54e1-133">Color</span></span><br/> <span data-ttu-id="b54e1-134">D2D1 \_ Schatten- \_ Prop- \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="b54e1-134">D2D1\_SHADOW\_PROP\_COLOR</span></span><br/>                                     | <span data-ttu-id="b54e1-135">Die Farbe des Schlagschattens.</span><span class="sxs-lookup"><span data-stu-id="b54e1-135">The color of the drop shadow.</span></span> <span data-ttu-id="b54e1-136">Diese Eigenschaft ist ein D2D1 \_ Vector \_ 4f, definiert als: (R, G, B, a).</span><span class="sxs-lookup"><span data-stu-id="b54e1-136">This property is a D2D1\_VECTOR\_4F defined as: (R, G, B, A).</span></span> <span data-ttu-id="b54e1-137">Sie müssen diese Farbe in der geraden Alpha Angabe angeben.</span><span class="sxs-lookup"><span data-stu-id="b54e1-137">You must specify this color in straight alpha.</span></span><br/> <span data-ttu-id="b54e1-138">Der Typ ist "D2D1 \_ Vector \_ 4f".</span><span class="sxs-lookup"><span data-stu-id="b54e1-138">The type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="b54e1-139">Der Standardwert ist {0,0 f, 0,0 f, 0,0 f, 1.0 f}.</span><span class="sxs-lookup"><span data-stu-id="b54e1-139">The default value is {0.0f, 0.0f, 0.0f, 1.0f}.</span></span><br/>                                                                                                                                                                     |
| <span data-ttu-id="b54e1-140">Optimization</span><span class="sxs-lookup"><span data-stu-id="b54e1-140">Optimization</span></span><br/> <span data-ttu-id="b54e1-141">D2D1- \_ Schatten- \_ Prop- \_ Optimierung</span><span class="sxs-lookup"><span data-stu-id="b54e1-141">D2D1\_SHADOW\_PROP\_OPTIMIZATION</span></span><br/>                       | <span data-ttu-id="b54e1-142">Die Ebene der Leistungsoptimierung.</span><span class="sxs-lookup"><span data-stu-id="b54e1-142">The level of performance optimization.</span></span><br/> <span data-ttu-id="b54e1-143">Der Typ ist die D2D1- \_ Schatten \_ Optimierung.</span><span class="sxs-lookup"><span data-stu-id="b54e1-143">The type is D2D1\_SHADOW\_OPTIMIZATION.</span></span><br/> <span data-ttu-id="b54e1-144">Der Standardwert ist D2D1 \_ Schatten \_ Optimierung \_ ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="b54e1-144">The default value is D2D1\_SHADOW\_OPTIMIZATION\_BALANCED.</span></span><br/>                                                                                                                                                                                                                                                   |



 

## <a name="optimization-modes"></a><span data-ttu-id="b54e1-145">Optimierungs Modi</span><span class="sxs-lookup"><span data-stu-id="b54e1-145">Optimization modes</span></span>



| <span data-ttu-id="b54e1-146">Name</span><span class="sxs-lookup"><span data-stu-id="b54e1-146">Name</span></span>                                          | <span data-ttu-id="b54e1-147">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b54e1-147">Description</span></span>                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b54e1-148">D2D1- \_ \_ Optimierungs Geschwindigkeit für directionalblur \_</span><span class="sxs-lookup"><span data-stu-id="b54e1-148">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_SPEED</span></span>    | <span data-ttu-id="b54e1-149">Wendet interne Optimierungen an, wie z. b. die vorab Skalierung bei relativ kleinen Radii.</span><span class="sxs-lookup"><span data-stu-id="b54e1-149">Applies internal optimizations such as pre-scaling at relatively small radii.</span></span> <span data-ttu-id="b54e1-150">Verwendet lineare Filterung.</span><span class="sxs-lookup"><span data-stu-id="b54e1-150">Uses linear filtering.</span></span>                                  |
| <span data-ttu-id="b54e1-151">D2D1 \_ directionalblur- \_ Optimierung \_ ausgeglichen</span><span class="sxs-lookup"><span data-stu-id="b54e1-151">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED</span></span> | <span data-ttu-id="b54e1-152">Verwendet die gleichen Optimierungs Schwellenwerte wie der Geschwindigkeits Modus, verwendet jedoch die drei lineare Filterung.</span><span class="sxs-lookup"><span data-stu-id="b54e1-152">Uses the same optimization thresholds as Speed mode, but uses trilinear filtering.</span></span>                                                    |
| <span data-ttu-id="b54e1-153">D2D1 \_ directionalblur- \_ Optimierungs \_ Qualität</span><span class="sxs-lookup"><span data-stu-id="b54e1-153">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_QUALITY</span></span>  | <span data-ttu-id="b54e1-154">Verwendet nur interne Optimierungen mit großen weichungs Radien, bei denen es weniger wahrscheinlich ist, dass Näherungen sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="b54e1-154">Only uses internal optimizations with large blur radii, where approximations are less likely to be visible.</span></span> <span data-ttu-id="b54e1-155">Verwendet die drei lineare Filterung.</span><span class="sxs-lookup"><span data-stu-id="b54e1-155">Uses trilinear filtering.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="b54e1-156">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="b54e1-156">Output bitmap</span></span>

<span data-ttu-id="b54e1-157">Die Größe der Ausgabe Bitmap entspricht der Größe der weichzeichnerausgabe.</span><span class="sxs-lookup"><span data-stu-id="b54e1-157">The size of the output bitmap is the size of the blur output.</span></span> <span data-ttu-id="b54e1-158">Der Betrag, um den die Ausgabe Bitmap relativ zur ursprünglichen Bitmap vergrößert werden kann, kann mit der folgenden Formel berechnet werden:</span><span class="sxs-lookup"><span data-stu-id="b54e1-158">The amount the output bitmap growth relative to the original bitmap can be calculated using the following equation:</span></span>

<span data-ttu-id="b54e1-159">Vergrößerung der Bitmap (X und Y) = blurstandardabweichung (geräteunabhängige Pixel (Dips)) \* 6 \* (Benutzer dpi)/96</span><span class="sxs-lookup"><span data-stu-id="b54e1-159">Output Bitmap Growth (X and Y) = BlurStandardDeviation (device-independent pixels (DIPs))\*6\*(User DPI)/96</span></span>

<span data-ttu-id="b54e1-160">Die Ausgabe erhöht sich gleichmäßig in alle Richtungen. wenn die Größe beispielsweise um 10 Pixel in jeder Richtung zunimmt, befindet sich die obere linke Ecke der Bitmap bei (-5,-5), und die untere rechte wird um (105, 105), wie im Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b54e1-160">The output increases equally in all direction, so for example if the size increases by 10 pixels in each direction, the upper left corner of the bitmap is located at (-5, -5) and the lower right will be at (105, 105) as shown in the diagram here.</span></span>

![Diagramm der Größe der Ausgabegröße der Schatteneffekte.](images/drop-shadow-output-growth.png)

## <a name="requirements"></a><span data-ttu-id="b54e1-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b54e1-162">Requirements</span></span>



| <span data-ttu-id="b54e1-163">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b54e1-163">Requirement</span></span> | <span data-ttu-id="b54e1-164">Wert</span><span class="sxs-lookup"><span data-stu-id="b54e1-164">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b54e1-165">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b54e1-165">Minimum supported client</span></span> | <span data-ttu-id="b54e1-166">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b54e1-166">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b54e1-167">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b54e1-167">Minimum supported server</span></span> | <span data-ttu-id="b54e1-168">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b54e1-168">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b54e1-169">Header</span><span class="sxs-lookup"><span data-stu-id="b54e1-169">Header</span></span>                   | <span data-ttu-id="b54e1-170">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="b54e1-170">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="b54e1-171">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b54e1-171">Library</span></span>                  | <span data-ttu-id="b54e1-172">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="b54e1-172">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="b54e1-173">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b54e1-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b54e1-174">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="b54e1-174">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

