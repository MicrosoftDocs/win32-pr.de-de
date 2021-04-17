---
title: Rahmen-Effekt
description: Verwenden Sie den Rahmen Effekt, um ein Bild von den Rändern zu erweitern.
ms.assetid: D3D569F5-9496-4633-93E2-26665FFC3B37
keywords:
- Rahmen Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fb43ae8b3e9c4eb449a8231f8b4ffcacf7658b
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "104530413"
---
# <a name="border-effect"></a><span data-ttu-id="b60fd-104">Rahmen-Effekt</span><span class="sxs-lookup"><span data-stu-id="b60fd-104">Border effect</span></span>

<span data-ttu-id="b60fd-105">Verwenden Sie den Rahmen Effekt, um ein Bild von den Rändern zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="b60fd-105">Use the border effect to extend an image from the edges.</span></span> <span data-ttu-id="b60fd-106">Mit diesem Effekt können Sie die Pixel von den Rändern des Bilds wiederholen, die Pixel vom umgekehrten Ende des Bilds umschließen oder die Pixel über den bitmaprahmen hinweg spiegeln, um den Bitmapbereich zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="b60fd-106">You can use this effect to repeat the pixels from the edges of the image, wrap the pixels from the opposite end of the image, or mirror the pixels across the bitmap border to extend the bitmap region.</span></span>

<span data-ttu-id="b60fd-107">Die CLSID für diesen Effekt ist CLSID \_ D2D1Border.</span><span class="sxs-lookup"><span data-stu-id="b60fd-107">The CLSID for this effect is CLSID\_D2D1Border.</span></span>

## <a name="example-images"></a><span data-ttu-id="b60fd-108">Beispiel Bilder</span><span class="sxs-lookup"><span data-stu-id="b60fd-108">Example images</span></span>

<span data-ttu-id="b60fd-109">In den Beispielen wird die Ausgabe des Rahmen Effekts mithilfe der einzelnen Modi veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b60fd-109">The examples here show the output of the border effect using each mode.</span></span> <span data-ttu-id="b60fd-110">Die Ausgabegröße ist unendlich, aber diese Beispiel Bilder werden auf die doppelte Größe zugeschnitten.</span><span class="sxs-lookup"><span data-stu-id="b60fd-110">The output size is infinite, but these example images are cropped to twice the size.</span></span>

### <a name="mirror"></a><span data-ttu-id="b60fd-111">Spiegel</span><span class="sxs-lookup"><span data-stu-id="b60fd-111">Mirror</span></span>



| <span data-ttu-id="b60fd-112">Vorher</span><span class="sxs-lookup"><span data-stu-id="b60fd-112">Before</span></span>                                                    |
|-----------------------------------------------------------|
| ![Screenshot, der das Bild vor dem Effekt zeigt.](images/border-before.jpg) |
| <span data-ttu-id="b60fd-114">Nach</span><span class="sxs-lookup"><span data-stu-id="b60fd-114">After</span></span>                                                     |
| ![Screenshot, der das Bild nach der Transformation anzeigt.](images/10-border.png)   |



 

### <a name="clamp"></a><span data-ttu-id="b60fd-116">Clamp</span><span class="sxs-lookup"><span data-stu-id="b60fd-116">Clamp</span></span>



| <span data-ttu-id="b60fd-117">Vorher</span><span class="sxs-lookup"><span data-stu-id="b60fd-117">Before</span></span>                                                        |
|---------------------------------------------------------------|
| ![Screenshot, der das Bild vor dem Effekt einer Klammer anzeigt.](images/border-before.jpg)     |
| <span data-ttu-id="b60fd-119">Nach</span><span class="sxs-lookup"><span data-stu-id="b60fd-119">After</span></span>                                                         |
| ![Screenshot, der das Bild nach der Transformation für eine Klammer anzeigt.](images/10-border-clamp.png) |



 

### <a name="wrap"></a><span data-ttu-id="b60fd-121">Umschließen</span><span class="sxs-lookup"><span data-stu-id="b60fd-121">Wrap</span></span>



| <span data-ttu-id="b60fd-122">Vorher</span><span class="sxs-lookup"><span data-stu-id="b60fd-122">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![Screenshot, der das Bild vor dem Effekt für einen Umbruch anzeigt.](images/border-before.jpg)    |
| <span data-ttu-id="b60fd-124">Nach</span><span class="sxs-lookup"><span data-stu-id="b60fd-124">After</span></span>                                                        |
| ![Screenshot, der das Bild nach der Transformation für einen Umbruch anzeigt.](images/10-border-wrap.png) |



 


```C++
ComPtr<ID2D1Effect> borderEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Border, &borderEffect);

borderEffect->SetInput(0, bitmap);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_X, D2D1_BORDER_EDGE_MODE_MIRROR);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_Y, D2D1_BORDER_EDGE_MODE_MIRROR);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(borderEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a><span data-ttu-id="b60fd-126">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b60fd-126">Effect properties</span></span>



| <span data-ttu-id="b60fd-127">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="b60fd-127">Display name and index enumeration</span></span>                                  | <span data-ttu-id="b60fd-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b60fd-128">Description</span></span>                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b60fd-129">Edgemodus X</span><span class="sxs-lookup"><span data-stu-id="b60fd-129">Edge Mode X</span></span><br/> <span data-ttu-id="b60fd-130">D2D1 \_ Border \_ Prop \_ Edge \_ Mode \_ X</span><span class="sxs-lookup"><span data-stu-id="b60fd-130">D2D1\_BORDER\_PROP\_EDGE\_MODE\_X</span></span><br/> | <span data-ttu-id="b60fd-131">Der edgemodus in der X-Richtung für den Effekt.</span><span class="sxs-lookup"><span data-stu-id="b60fd-131">The edge mode in the X direction for the effect.</span></span> <span data-ttu-id="b60fd-132">Sie können diese Einstellung auf Klammer, Umbruch oder Spiegelung festlegen.</span><span class="sxs-lookup"><span data-stu-id="b60fd-132">You can set this to clamp, wrap, or mirror.</span></span> <span data-ttu-id="b60fd-133">Weitere Informationen finden Sie unter [Edge-Modi](#edge-modes) .</span><span class="sxs-lookup"><span data-stu-id="b60fd-133">See [Edge modes](#edge-modes) for more info.</span></span><br/> <span data-ttu-id="b60fd-134">Der Typ ist D2D1 \_ Border \_ Edge \_ Mode.</span><span class="sxs-lookup"><span data-stu-id="b60fd-134">The type is D2D1\_BORDER\_EDGE\_MODE.</span></span><br/> <span data-ttu-id="b60fd-135">Der Standardwert ist D2D1 \_ Border \_ Edge \_ Mode \_ Clamp.</span><span class="sxs-lookup"><span data-stu-id="b60fd-135">The default value is D2D1\_BORDER\_EDGE\_MODE\_CLAMP.</span></span><br/> |
| <span data-ttu-id="b60fd-136">Edgemodus Y</span><span class="sxs-lookup"><span data-stu-id="b60fd-136">Edge Mode Y</span></span><br/> <span data-ttu-id="b60fd-137">D2D1 \_ Border \_ Prop \_ Edge \_ Mode \_ Y</span><span class="sxs-lookup"><span data-stu-id="b60fd-137">D2D1\_BORDER\_PROP\_EDGE\_MODE\_Y</span></span><br/> | <span data-ttu-id="b60fd-138">Der edgemodus in der Y-Richtung für den Effekt.</span><span class="sxs-lookup"><span data-stu-id="b60fd-138">The edge mode in the Y direction for the effect.</span></span> <span data-ttu-id="b60fd-139">Sie können diese Einstellung auf Klammer, Umbruch oder Spiegelung festlegen.</span><span class="sxs-lookup"><span data-stu-id="b60fd-139">You can set this to clamp, wrap, or mirror.</span></span> <span data-ttu-id="b60fd-140">Weitere Informationen finden Sie unter [Edge-Modi](#edge-modes) .</span><span class="sxs-lookup"><span data-stu-id="b60fd-140">See [Edge modes](#edge-modes) for more info.</span></span><br/> <span data-ttu-id="b60fd-141">Der Typ ist D2D1 \_ Border \_ Edge \_ Mode.</span><span class="sxs-lookup"><span data-stu-id="b60fd-141">The type is D2D1\_BORDER\_EDGE\_MODE.</span></span><br/> <span data-ttu-id="b60fd-142">Der Standardwert ist D2D1 \_ Border \_ Edge \_ Mode \_ Clamp.</span><span class="sxs-lookup"><span data-stu-id="b60fd-142">The default value is D2D1\_BORDER\_EDGE\_MODE\_CLAMP.</span></span><br/> |



 

## <a name="edge-modes"></a><span data-ttu-id="b60fd-143">Edge-Modi</span><span class="sxs-lookup"><span data-stu-id="b60fd-143">Edge modes</span></span>



| <span data-ttu-id="b60fd-144">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="b60fd-144">Display name and index enumeration</span></span>                            | <span data-ttu-id="b60fd-145">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b60fd-145">Description</span></span>                                          |
|---------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b60fd-146">Clamp</span><span class="sxs-lookup"><span data-stu-id="b60fd-146">Clamp</span></span><br/> <span data-ttu-id="b60fd-147">D2D1 \_ Border \_ Edge \_ Mode- \_ Klammer</span><span class="sxs-lookup"><span data-stu-id="b60fd-147">D2D1\_BORDER\_EDGE\_MODE\_CLAMP</span></span><br/>   | <span data-ttu-id="b60fd-148">Wiederholt die Pixel von den Rändern des Bilds.</span><span class="sxs-lookup"><span data-stu-id="b60fd-148">Repeats the pixels from the edges of the image.</span></span>      |
| <span data-ttu-id="b60fd-149">Umschließen</span><span class="sxs-lookup"><span data-stu-id="b60fd-149">Wrap</span></span><br/> <span data-ttu-id="b60fd-150">D2D1 \_ Border \_ Edge- \_ Modus \_ umschließen</span><span class="sxs-lookup"><span data-stu-id="b60fd-150">D2D1\_BORDER\_EDGE\_MODE\_WRAP</span></span><br/>     | <span data-ttu-id="b60fd-151">Verwendet Pixel vom gegenüberliegenden Endrand des Bilds.</span><span class="sxs-lookup"><span data-stu-id="b60fd-151">Uses pixels from the opposite end edge of the image.</span></span> |
| <span data-ttu-id="b60fd-152">Spiegel</span><span class="sxs-lookup"><span data-stu-id="b60fd-152">Mirror</span></span><br/> <span data-ttu-id="b60fd-153">D2D1 \_ - \_ \_ randmodusspiegelung \_</span><span class="sxs-lookup"><span data-stu-id="b60fd-153">D2D1\_BORDER\_EDGE\_MODE\_MIRROR</span></span><br/> | <span data-ttu-id="b60fd-154">Gibt Pixel über den Rand des Bilds wieder.</span><span class="sxs-lookup"><span data-stu-id="b60fd-154">Reflects pixels about the edge of the image.</span></span>         |



 

## <a name="output-bitmap"></a><span data-ttu-id="b60fd-155">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="b60fd-155">Output bitmap</span></span>

<span data-ttu-id="b60fd-156">Die Größe der Ausgabe Bitmap ist für alle Eingaben unbegrenzt, außer bei einem Eingabebild mit der Größe 0 (null).</span><span class="sxs-lookup"><span data-stu-id="b60fd-156">The output bitmap size is infinite for all inputs, except a 0 sized input image.</span></span> <span data-ttu-id="b60fd-157">Wenn die Höhe oder die Breite eines Eingabe Bilds 0 beträgt, ist die Ausgabegröße 0.</span><span class="sxs-lookup"><span data-stu-id="b60fd-157">If the height or the width of an input image is 0, the output size is 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="b60fd-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b60fd-158">Requirements</span></span>



| <span data-ttu-id="b60fd-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b60fd-159">Requirement</span></span> | <span data-ttu-id="b60fd-160">Wert</span><span class="sxs-lookup"><span data-stu-id="b60fd-160">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b60fd-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b60fd-161">Minimum supported client</span></span> | <span data-ttu-id="b60fd-162">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b60fd-162">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b60fd-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b60fd-163">Minimum supported server</span></span> | <span data-ttu-id="b60fd-164">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b60fd-164">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b60fd-165">Header</span><span class="sxs-lookup"><span data-stu-id="b60fd-165">Header</span></span>                   | <span data-ttu-id="b60fd-166">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="b60fd-166">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="b60fd-167">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b60fd-167">Library</span></span>                  | <span data-ttu-id="b60fd-168">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="b60fd-168">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="b60fd-169">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b60fd-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b60fd-170">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="b60fd-170">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

