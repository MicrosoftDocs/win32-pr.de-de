---
title: Auswirkung der Verschiebungs Zuordnung
description: Verwenden Sie den Verschiebungs Zuordnungs Effekt, um die Pixel des Eingabe Bilds anhand der Intensität der Werte eines zweiten Eingabe Bilds zu übertragen.
ms.assetid: 07AA64B1-B570-428E-924F-D7DF3E4DB3F8
keywords:
- Auswirkung der Verschiebungs Zuordnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0ad2deb0c584ccc9c55faebd60f803d66efa42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102951"
---
# <a name="displacement-map-effect"></a><span data-ttu-id="c1941-104">Auswirkung der Verschiebungs Zuordnung</span><span class="sxs-lookup"><span data-stu-id="c1941-104">Displacement map effect</span></span>

<span data-ttu-id="c1941-105">Verwenden Sie den Verschiebungs Zuordnungs Effekt, um die Pixel des Eingabe Bilds anhand der Intensität der Werte eines zweiten Eingabe Bilds zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="c1941-105">Use the displacement map effect to displace the pixels of the input image by the intensity values of a second input image.</span></span>

<span data-ttu-id="c1941-106">Die CLSID für diesen Effekt ist CLSID \_ D2D1DisplacementMap.</span><span class="sxs-lookup"><span data-stu-id="c1941-106">The CLSID for this effect is CLSID\_D2D1DisplacementMap.</span></span>

-   [<span data-ttu-id="c1941-107">Beispiel Bild</span><span class="sxs-lookup"><span data-stu-id="c1941-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="c1941-108">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c1941-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="c1941-109">Farbkanäle</span><span class="sxs-lookup"><span data-stu-id="c1941-109">Color channels</span></span>](#color-channels)
-   [<span data-ttu-id="c1941-110">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="c1941-110">Output Bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="c1941-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1941-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="c1941-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c1941-112">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="c1941-113">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="c1941-113">Example image</span></span>



| <span data-ttu-id="c1941-114">Vorher</span><span class="sxs-lookup"><span data-stu-id="c1941-114">Before</span></span>                                                           |
|------------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)       |
| <span data-ttu-id="c1941-116">Nach</span><span class="sxs-lookup"><span data-stu-id="c1941-116">After</span></span>                                                            |
| ![das Bild nach der Transformation.](images/19-displacementmap.png) |



 


```C++
ComPtr<ID2D1Effect> displacementMapEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DisplacementMap, &displacementMapEffect);

displacementMapEffect->SetInput(0, bitmap);
displacementMapEffect->SetValue(D2D1_DISPLACEMENTMAP_PROP_SCALE, 100.0f);

// The second input of the displacement effect determines how the input image is transformed.
// For this example, we will use a turbulence effect as the second input to randomly distort the image.
ComPtr<ID2D1Effect> turbulenceEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Turbulence, &turbulenceEffect);
displacementMapEffect->SetInputEffect(1, turbulenceEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(displacementMapEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="c1941-118">Die Speicherorte der Pixel in der Ausgabe werden mithilfe der folgenden Formel bestimmt:</span><span class="sxs-lookup"><span data-stu-id="c1941-118">The locations of the pixels in the output are determined using this formula:</span></span>

<span data-ttu-id="c1941-119">C ' (x, y) = c (x + Skala \* (xchannelselector (Verschiebungs Bitmap (x, y))-0,5), y + Skala \* (ychannelselector (Verschiebungs Bitmap (x, y))-0,5))</span><span class="sxs-lookup"><span data-stu-id="c1941-119">C' (x,y)=C(x+ scale\*(XChannelSelector(Displacement Bitmap (x,y))-0.5),y+ scale\*(YChannelSelector(Displacement Bitmap (x,y))-0.5))</span></span>

<span data-ttu-id="c1941-120">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="c1941-120">Where:</span></span><dl> <span data-ttu-id="c1941-121">*C (x, y)* ist das Ausgabe Pixel bei (x, y).</span><span class="sxs-lookup"><span data-stu-id="c1941-121">*C  (x, y)* is the output pixel at (x, y).</span></span>  
<span data-ttu-id="c1941-122">*C (x, y)* ist das Eingabe Pixel bei (x, y).</span><span class="sxs-lookup"><span data-stu-id="c1941-122">*C (x, y)* is the input pixel at (x, y).</span></span>  
<span data-ttu-id="c1941-123">Die *Verschiebungs Bitmap (x, y)* ist die Verschiebungs Pixel Intensität an den angegebenen Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="c1941-123">*Displacement Bitmap (x, y)* is the displacement pixel intensity at the specified coordinates</span></span>  
<span data-ttu-id="c1941-124">*Xchannelselector* die Intensität des ausgewählten RGBA-Kanals aus der Verschiebungs Bitmap, die das Eingabebild in der X-Richtung verschiebt.</span><span class="sxs-lookup"><span data-stu-id="c1941-124">*XChannelSelector* the intensity of the selected RGBA channel from the displacement bitmap that displaces the input image in the X direction.</span></span>  
<span data-ttu-id="c1941-125">*Ychannelselector* die Intensität des ausgewählten RGBA-Kanals aus der Verschiebungs Bitmap, die das Eingabebild in der Y-Richtung verschiebt.</span><span class="sxs-lookup"><span data-stu-id="c1941-125">*YChannelSelector* the intensity of the selected RGBA channel from the displacement bitmap that displaces the input image in the Y direction.</span></span>  
</dl>

<span data-ttu-id="c1941-126">Der Effekt zeigt das Eingabebild anhand der Skalierungs Eigenschaft und der Intensität des Verschiebungs Bilds neu an.</span><span class="sxs-lookup"><span data-stu-id="c1941-126">The effect resamples the input image according to the scale property and the intensity of the displacement image.</span></span> <span data-ttu-id="c1941-127">Sie verwendet die bilineare interpolung, wenn eine Stichprobenentnahme zwischen Pixeln im Eingabebild erfolgt.</span><span class="sxs-lookup"><span data-stu-id="c1941-127">It uses bilinear interpolation if sampling from between pixels in the input image.</span></span>

<span data-ttu-id="c1941-128">Dieser Effekt kann bei geraden und vorab multiplizierten Alpha Bildern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1941-128">This effect works on straight and premultiplied alpha images.</span></span> <span data-ttu-id="c1941-129">Das Alpha Format der Ausgabe ist mit dem Eingabeformat identisch.</span><span class="sxs-lookup"><span data-stu-id="c1941-129">The output alpha format is the same as the input format.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="c1941-130">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c1941-130">Effect properties</span></span>



| <span data-ttu-id="c1941-131">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="c1941-131">Display name and index enumeration</span></span>                                                   | <span data-ttu-id="c1941-132">Typ und Standardwert</span><span class="sxs-lookup"><span data-stu-id="c1941-132">Type and default value</span></span>                                                   | <span data-ttu-id="c1941-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1941-133">Description</span></span>                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1941-134">Skalieren</span><span class="sxs-lookup"><span data-stu-id="c1941-134">Scale</span></span><br/> <span data-ttu-id="c1941-135">D2D1 \_ Verschiebungen der Verschiebungen \_ \_</span><span class="sxs-lookup"><span data-stu-id="c1941-135">D2D1\_DISPLACEMENTMAP\_PROP\_SCALE</span></span><br/>                       | <span data-ttu-id="c1941-136">GLEITKOMMAZAHL</span><span class="sxs-lookup"><span data-stu-id="c1941-136">FLOAT</span></span><br/> <span data-ttu-id="c1941-137">0,0 f</span><span class="sxs-lookup"><span data-stu-id="c1941-137">0.0f</span></span><br/>                                         | <span data-ttu-id="c1941-138">Multipliziert die Intensität des ausgewählten Kanals vom Verschiebungs Bild.</span><span class="sxs-lookup"><span data-stu-id="c1941-138">Multiplies the intensity of the selected channel from the displacement image.</span></span> <span data-ttu-id="c1941-139">Je höher Sie diese Eigenschaft festlegen, desto mehr werden die Pixel durch die Auswirkung verlagert.</span><span class="sxs-lookup"><span data-stu-id="c1941-139">The higher you set this property, the more the effect displaces the pixels</span></span><br/>                       |
| <span data-ttu-id="c1941-140">Xchannelselect</span><span class="sxs-lookup"><span data-stu-id="c1941-140">XChannelSelect</span></span><br/> <span data-ttu-id="c1941-141">D2D1 \_ Verschiebungen in der \_ X- \_ Kanal-Prop \_ \_ auswählen</span><span class="sxs-lookup"><span data-stu-id="c1941-141">D2D1\_DISPLACEMENTMAP\_PROP\_X\_CHANNEL\_SELECT</span></span><br/> | <span data-ttu-id="c1941-142">D2D1 \_ - \_ kanalselektor</span><span class="sxs-lookup"><span data-stu-id="c1941-142">D2D1\_CHANNEL\_SELECTOR</span></span><br/> <span data-ttu-id="c1941-143">D2D1 \_ \_ kanalselektor \_ A</span><span class="sxs-lookup"><span data-stu-id="c1941-143">D2D1\_CHANNEL\_SELECTOR\_A</span></span><br/> | <span data-ttu-id="c1941-144">Der Effekt extrahiert die Intensität aus diesem Farbkanal und verwendet diese, um das Bild in der X-Richtung räumlich zu verzahnen.</span><span class="sxs-lookup"><span data-stu-id="c1941-144">The effect extracts the intensity from this color channel and uses it to spatially displace the image in the X direction.</span></span> <span data-ttu-id="c1941-145">Weitere Informationen finden Sie unter [Color Channels](#color-channels) .</span><span class="sxs-lookup"><span data-stu-id="c1941-145">See [Color channels](#color-channels) for more info.</span></span><br/> |
| <span data-ttu-id="c1941-146">Ychannelselect</span><span class="sxs-lookup"><span data-stu-id="c1941-146">YChannelSelect</span></span><br/> <span data-ttu-id="c1941-147">D2D1 \_ Verschiebungen der Zuordnung für \_ Y- \_ \_ Kanal \_ auswählen</span><span class="sxs-lookup"><span data-stu-id="c1941-147">D2D1\_DISPLACEMENTMAP\_PROP\_Y\_CHANNEL\_SELECT</span></span><br/> | <span data-ttu-id="c1941-148">D2D1 \_ - \_ kanalselektor</span><span class="sxs-lookup"><span data-stu-id="c1941-148">D2D1\_CHANNEL\_SELECTOR</span></span><br/> <span data-ttu-id="c1941-149">D2D1 \_ \_ kanalselektor \_ A</span><span class="sxs-lookup"><span data-stu-id="c1941-149">D2D1\_CHANNEL\_SELECTOR\_A</span></span><br/> | <span data-ttu-id="c1941-150">Der Effekt extrahiert die Intensität aus diesem Farbkanal und verwendet diese, um das Bild in der Y-Richtung räumlich zu verzahnen.</span><span class="sxs-lookup"><span data-stu-id="c1941-150">The effect extracts the intensity from this color channel and uses it to spatially displace the image in the Y direction.</span></span> <span data-ttu-id="c1941-151">Weitere Informationen finden Sie unter [Color Channels](#color-channels) .</span><span class="sxs-lookup"><span data-stu-id="c1941-151">See [Color channels](#color-channels) for more info.</span></span><br/> |



 

## <a name="color-channels"></a><span data-ttu-id="c1941-152">Farbkanäle</span><span class="sxs-lookup"><span data-stu-id="c1941-152">Color channels</span></span>



| <span data-ttu-id="c1941-153">Enumeration</span><span class="sxs-lookup"><span data-stu-id="c1941-153">Enumeration</span></span>                | <span data-ttu-id="c1941-154">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1941-154">Description</span></span>                                                      |
|----------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c1941-155">D2D1 \_ - \_ kanalselektor \_ R</span><span class="sxs-lookup"><span data-stu-id="c1941-155">D2D1\_CHANNEL\_SELECTOR\_R</span></span> | <span data-ttu-id="c1941-156">Der Effekt extrahiert die Intensität der Ausgabe des roten Kanals.</span><span class="sxs-lookup"><span data-stu-id="c1941-156">The effect extracts the intensity output from the red channel.</span></span>   |
| <span data-ttu-id="c1941-157">D2D1 \_ Kanal \_ Auswahl \_ G</span><span class="sxs-lookup"><span data-stu-id="c1941-157">D2D1\_CHANNEL\_SELECTOR\_G</span></span> | <span data-ttu-id="c1941-158">Der Effekt extrahiert die Intensität der Ausgabe aus dem grünen Kanal.</span><span class="sxs-lookup"><span data-stu-id="c1941-158">The effect extracts the intensity output from the green channel.</span></span> |
| <span data-ttu-id="c1941-159">D2D1 \_ - \_ kanalselektor \_ B</span><span class="sxs-lookup"><span data-stu-id="c1941-159">D2D1\_CHANNEL\_SELECTOR\_B</span></span> | <span data-ttu-id="c1941-160">Der Effekt extrahiert die Intensität der Ausgabe aus dem blauen Kanal.</span><span class="sxs-lookup"><span data-stu-id="c1941-160">The effect extracts the intensity output from the blue channel.</span></span>  |
| <span data-ttu-id="c1941-161">D2D1 \_ \_ kanalselektor \_ A</span><span class="sxs-lookup"><span data-stu-id="c1941-161">D2D1\_CHANNEL\_SELECTOR\_A</span></span> | <span data-ttu-id="c1941-162">Der Effekt extrahiert die Intensität der Ausgabe aus dem Alphakanal.</span><span class="sxs-lookup"><span data-stu-id="c1941-162">The effect extracts the intensity output from the alpha channel.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="c1941-163">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="c1941-163">Output Bitmap</span></span>

<span data-ttu-id="c1941-164">Sie können die maximale Größe der Ausgabe Bitmap mit den folgenden Gleichungen ermitteln:</span><span class="sxs-lookup"><span data-stu-id="c1941-164">You can determine the maximum size of the output bitmap with these equations:</span></span>

<span data-ttu-id="c1941-165">Ausgabe Bitmap?</span><span class="sxs-lookup"><span data-stu-id="c1941-165">Output Bitmap?</span></span> <span data-ttu-id="c1941-166">Pixel = (Eingabe Bitmapgröße?) ( Dips) + Skalierung \* (Benutzer dpi/96)</span><span class="sxs-lookup"><span data-stu-id="c1941-166">Pixels=(Input Bitmap Size?(DIPs)+Scale)\*(User DPI/96)</span></span>

<span data-ttu-id="c1941-167">Ausgabe Bitmap<sub>y</sub> Pixel = (Eingabe Bitmapgröße<sub>y</sub>(Dips) + Skala) \* (Benutzer dpi/96)</span><span class="sxs-lookup"><span data-stu-id="c1941-167">Output Bitmap<sub>y</sub> Pixels=(Input Bitmap Size<sub>y</sub>(DIPs) + Scale)\*(User DPI/96)</span></span>

## <a name="requirements"></a><span data-ttu-id="c1941-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1941-168">Requirements</span></span>



| <span data-ttu-id="c1941-169">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1941-169">Requirement</span></span> | <span data-ttu-id="c1941-170">Wert</span><span class="sxs-lookup"><span data-stu-id="c1941-170">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c1941-171">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1941-171">Minimum supported client</span></span> | <span data-ttu-id="c1941-172">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1941-172">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c1941-173">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1941-173">Minimum supported server</span></span> | <span data-ttu-id="c1941-174">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1941-174">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c1941-175">Header</span><span class="sxs-lookup"><span data-stu-id="c1941-175">Header</span></span>                   | <span data-ttu-id="c1941-176">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="c1941-176">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="c1941-177">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c1941-177">Library</span></span>                  | <span data-ttu-id="c1941-178">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="c1941-178">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="c1941-179">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c1941-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1941-180">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="c1941-180">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

