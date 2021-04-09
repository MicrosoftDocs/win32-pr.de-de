---
title: Morphologieeffekt
description: Verwenden Sie den morphologieeffekt, um die Randgrenzen eines Bilds dünn oder Thicken zu können.
ms.assetid: 4B3CFC51-D556-4729-B433-7307C80291F4
keywords:
- morphologieeffekte
- Dilate-Auswirkung
- Auswirkung Erodieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f43cf41810ae0b16c9bc96dd37473a0231fc132c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104727"
---
# <a name="morphology-effect"></a><span data-ttu-id="06590-106">Morphologieeffekt</span><span class="sxs-lookup"><span data-stu-id="06590-106">Morphology effect</span></span>

<span data-ttu-id="06590-107">Verwenden Sie den morphologieeffekt, um die Randgrenzen eines Bilds dünn oder Thicken zu können.</span><span class="sxs-lookup"><span data-stu-id="06590-107">Use the morphology effect to thin or thicken edge boundaries in an image.</span></span> <span data-ttu-id="06590-108">Dieser Effekt erstellt einen Kernel, der das 2fache der von Ihnen angegebenen Width-und Height-Werte ist.</span><span class="sxs-lookup"><span data-stu-id="06590-108">This effect creates a kernel that is 2 times the Width and Height values you specify.</span></span> <span data-ttu-id="06590-109">Dieser Effekt zentriert den Kernel auf dem Pixel, das er berechnet, und gibt den maximalen Wert im Kernel (bei der Vergrößerung) oder den minimalen Wert im Kernel (wenn das Eroding erfolgt) zurück.</span><span class="sxs-lookup"><span data-stu-id="06590-109">This effect centers the kernel on the pixel it is calculating and returns the maximum value in the kernel (if dilating) or minimum value in the kernel (if eroding).</span></span>

<span data-ttu-id="06590-110">Die CLSID für diesen Effekt ist CLSID \_ D2D1Morphology.</span><span class="sxs-lookup"><span data-stu-id="06590-110">The CLSID for this effect is CLSID\_D2D1Morphology.</span></span>

## <a name="example-images"></a><span data-ttu-id="06590-111">Beispiel Bilder</span><span class="sxs-lookup"><span data-stu-id="06590-111">Example images</span></span>

<span data-ttu-id="06590-112">Dieses Beispiel zeigt die Ausgabe der Auswirkung, wenn der eroeromodus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="06590-112">This example shows the output of the effect when using the erode mode.</span></span>



| <span data-ttu-id="06590-113">Vorher</span><span class="sxs-lookup"><span data-stu-id="06590-113">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg) |
| <span data-ttu-id="06590-115">Nach</span><span class="sxs-lookup"><span data-stu-id="06590-115">After</span></span>                                                      |
| ![das Bild nach der Transformation.](images/7-morphology.png) |



 


```C++
ComPtr<ID2D1Effect> morphologyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Morphology, &morphologyEffect);

morphologyEffect->SetInput(0, bitmap);

morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_MODE, D2D1_MORPHOLOGY_MODE_ERODE);
morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_WIDTH, 14);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(morphologyEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a><span data-ttu-id="06590-117">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="06590-117">Effect properties</span></span>



| <span data-ttu-id="06590-118">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="06590-118">Display name and index enumeration</span></span>                          | <span data-ttu-id="06590-119">Typ und Standardwert</span><span class="sxs-lookup"><span data-stu-id="06590-119">Type and default value</span></span>                                                     | <span data-ttu-id="06590-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06590-120">Description</span></span>                                                                                                                                                       |
|-------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06590-121">Mode</span><span class="sxs-lookup"><span data-stu-id="06590-121">Mode</span></span><br/> <span data-ttu-id="06590-122">D2D1 \_ Morphology- \_ Prop- \_ Modus</span><span class="sxs-lookup"><span data-stu-id="06590-122">D2D1\_MORPHOLOGY\_PROP\_MODE</span></span><br/>     | <span data-ttu-id="06590-123">D2D1- \_ \_ morphologiemodus</span><span class="sxs-lookup"><span data-stu-id="06590-123">D2D1\_MORPHOLOGY\_MODE</span></span><br/> <span data-ttu-id="06590-124">D2D1 \_ \_ morphologiemodus \_ Erodieren</span><span class="sxs-lookup"><span data-stu-id="06590-124">D2D1\_MORPHOLOGY\_MODE\_ERODE</span></span><br/> | <span data-ttu-id="06590-125">Der morphologiemodus.</span><span class="sxs-lookup"><span data-stu-id="06590-125">The morphology mode.</span></span> <span data-ttu-id="06590-126">Die verfügbaren Modi sind erodiert (Flatten) und Dilate (Thicken).</span><span class="sxs-lookup"><span data-stu-id="06590-126">The available modes are erode (flatten) and dilate (thicken).</span></span><br/> <span data-ttu-id="06590-127">Weitere Informationen finden Sie unter [morphologiemodi](#morphology-modes) .</span><span class="sxs-lookup"><span data-stu-id="06590-127">See [Morphology modes](#morphology-modes) for more info.</span></span><br/> |
| <span data-ttu-id="06590-128">Breite</span><span class="sxs-lookup"><span data-stu-id="06590-128">Width</span></span><br/> <span data-ttu-id="06590-129">Breite der D2D1- \_ morphologiebreite \_ \_</span><span class="sxs-lookup"><span data-stu-id="06590-129">D2D1\_MORPHOLOGY\_PROP\_WIDTH</span></span><br/>   | <span data-ttu-id="06590-130">UINT</span><span class="sxs-lookup"><span data-stu-id="06590-130">UINT</span></span><br/> <span data-ttu-id="06590-131">1</span><span class="sxs-lookup"><span data-stu-id="06590-131">1</span></span><br/>                                               | <span data-ttu-id="06590-132">Größe des Kernels in der X-Richtung.</span><span class="sxs-lookup"><span data-stu-id="06590-132">Size of the kernel in the X direction.</span></span> <span data-ttu-id="06590-133">Die Einheiten befinden sich in Dips.</span><span class="sxs-lookup"><span data-stu-id="06590-133">The units are in DIPs.</span></span> <span data-ttu-id="06590-134">Die Werte müssen zwischen 1 und 100 (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="06590-134">Values must be between 1 and 100 inclusive.</span></span>                                                         |
| <span data-ttu-id="06590-135">Höhe</span><span class="sxs-lookup"><span data-stu-id="06590-135">Height</span></span><br/> <span data-ttu-id="06590-136">D2D1 \_ Morphology \_ Prop \_ Height</span><span class="sxs-lookup"><span data-stu-id="06590-136">D2D1\_MORPHOLOGY\_PROP\_HEIGHT</span></span><br/> | <span data-ttu-id="06590-137">UINT</span><span class="sxs-lookup"><span data-stu-id="06590-137">UINT</span></span><br/> <span data-ttu-id="06590-138">1</span><span class="sxs-lookup"><span data-stu-id="06590-138">1</span></span><br/>                                               | <span data-ttu-id="06590-139">Größe des Kernels in der Y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="06590-139">Size of the kernel in the Y direction.</span></span> <span data-ttu-id="06590-140">Die Einheiten befinden sich in Dips.</span><span class="sxs-lookup"><span data-stu-id="06590-140">The units are in DIPs.</span></span> <span data-ttu-id="06590-141">Die Werte müssen zwischen 1 und 100 (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="06590-141">Values must be between 1 and 100 inclusive.</span></span>                                                         |



 

## <a name="morphology-modes"></a><span data-ttu-id="06590-142">Morphologiemodi</span><span class="sxs-lookup"><span data-stu-id="06590-142">Morphology modes</span></span>



| <span data-ttu-id="06590-143">Name</span><span class="sxs-lookup"><span data-stu-id="06590-143">Name</span></span>                           | <span data-ttu-id="06590-144">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06590-144">Description</span></span>                                                    |
|--------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="06590-145">D2D1 \_ \_ morphologiemodus \_ Erodieren</span><span class="sxs-lookup"><span data-stu-id="06590-145">D2D1\_MORPHOLOGY\_MODE\_ERODE</span></span>  | <span data-ttu-id="06590-146">Der maximale Wert jedes RGB-Kanals im Kernel wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="06590-146">The maximum value from each RGB channel in the kernel is used.</span></span> |
| <span data-ttu-id="06590-147">D2D1 \_ \_ morphologiemodus \_ Dilate</span><span class="sxs-lookup"><span data-stu-id="06590-147">D2D1\_MORPHOLOGY\_MODE\_DILATE</span></span> | <span data-ttu-id="06590-148">Der minimale Wert jedes RGB-Kanals im Kernel wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="06590-148">The minimum value from each RGB channel in the kernel is used.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="06590-149">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="06590-149">Output bitmap</span></span>

<span data-ttu-id="06590-150">Beim Dilate-Modus wächst die Größe der Ausgabe Bitmap:</span><span class="sxs-lookup"><span data-stu-id="06590-150">For DILATE mode, the Output Bitmap size grows:</span></span> 

| <span data-ttu-id="06590-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06590-151">Requirement</span></span> | <span data-ttu-id="06590-152">Wert</span><span class="sxs-lookup"><span data-stu-id="06590-152">Value</span></span> |
|--------------------------|-----------------------------------------|
| <span data-ttu-id="06590-153">Ergebnis der Ausgabe Bitmap X =</span><span class="sxs-lookup"><span data-stu-id="06590-153">Output Bitmap Growth X =</span></span> | <span data-ttu-id="06590-154">INT (float (Width) \* ((Benutzer dpi)/96))</span><span class="sxs-lookup"><span data-stu-id="06590-154">INT(FLOAT(Width) \* ((User DPI) / 96))</span></span>  |
| <span data-ttu-id="06590-155">Ergebnis der Ausgabe Bitmap Y =</span><span class="sxs-lookup"><span data-stu-id="06590-155">Output Bitmap Growth Y =</span></span> | <span data-ttu-id="06590-156">INT (float (Height) \* ((Benutzer dpi)/96))</span><span class="sxs-lookup"><span data-stu-id="06590-156">INT(FLOAT(Height) \* ((User DPI) / 96))</span></span> |



 

<span data-ttu-id="06590-157">Für den eroeromodus verkleinert sich die Größe der Ausgabe Bitmap:</span><span class="sxs-lookup"><span data-stu-id="06590-157">For ERODE mode, the Output Bitmap size shrinks:</span></span>

| <span data-ttu-id="06590-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06590-158">Requirement</span></span> | <span data-ttu-id="06590-159">Wert</span><span class="sxs-lookup"><span data-stu-id="06590-159">Value</span></span> |
|--------------------------|------------------------------------------|
| <span data-ttu-id="06590-160">Ergebnis der Ausgabe Bitmap X =</span><span class="sxs-lookup"><span data-stu-id="06590-160">Output Bitmap Growth X =</span></span> | <span data-ttu-id="06590-161">INT (float (-Width) \* ((Benutzer dpi)/96))</span><span class="sxs-lookup"><span data-stu-id="06590-161">INT(FLOAT(-Width) \* ((User DPI) / 96))</span></span>  |
| <span data-ttu-id="06590-162">Ergebnis der Ausgabe Bitmap Y =</span><span class="sxs-lookup"><span data-stu-id="06590-162">Output Bitmap Growth Y =</span></span> | <span data-ttu-id="06590-163">INT (float (-Height) \* ((Benutzer dpi)/96))</span><span class="sxs-lookup"><span data-stu-id="06590-163">INT(FLOAT(-Height) \* ((User DPI) / 96))</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="06590-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06590-164">Requirements</span></span>



| <span data-ttu-id="06590-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06590-165">Requirement</span></span> | <span data-ttu-id="06590-166">Wert</span><span class="sxs-lookup"><span data-stu-id="06590-166">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="06590-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06590-167">Minimum supported client</span></span> | <span data-ttu-id="06590-168">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06590-168">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="06590-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06590-169">Minimum supported server</span></span> | <span data-ttu-id="06590-170">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06590-170">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="06590-171">Header</span><span class="sxs-lookup"><span data-stu-id="06590-171">Header</span></span>                   | <span data-ttu-id="06590-172">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="06590-172">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="06590-173">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="06590-173">Library</span></span>                  | <span data-ttu-id="06590-174">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="06590-174">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="06590-175">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="06590-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06590-176">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="06590-176">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

