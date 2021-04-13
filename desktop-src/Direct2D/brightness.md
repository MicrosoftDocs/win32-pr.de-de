---
title: Helligkeits Effekt
description: Verwenden Sie den Helligkeits Effekt, um die Helligkeit des Bilds zu steuern.
ms.assetid: 5088D4D4-DFC8-45D3-B1C3-D576742D931C
keywords:
- Helligkeits Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88dd9797aa125e7099ba4a706bac730a30715f6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104554065"
---
# <a name="brightness-effect"></a><span data-ttu-id="23a7e-104">Helligkeits Effekt</span><span class="sxs-lookup"><span data-stu-id="23a7e-104">Brightness effect</span></span>

<span data-ttu-id="23a7e-105">Verwenden Sie den Helligkeits Effekt, um die Helligkeit des Bilds zu steuern.</span><span class="sxs-lookup"><span data-stu-id="23a7e-105">Use the brightness effect to control the brightness of the image.</span></span>

<span data-ttu-id="23a7e-106">Die CLSID für diesen Effekt ist CLSID \_ D2D1Brightness.</span><span class="sxs-lookup"><span data-stu-id="23a7e-106">The CLSID for this effect is CLSID\_D2D1Brightness.</span></span>

-   [<span data-ttu-id="23a7e-107">Beispiel Bild</span><span class="sxs-lookup"><span data-stu-id="23a7e-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="23a7e-108">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="23a7e-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="23a7e-109">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="23a7e-109">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="23a7e-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23a7e-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="23a7e-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="23a7e-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="23a7e-112">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="23a7e-112">Example image</span></span>



| <span data-ttu-id="23a7e-113">Vorher</span><span class="sxs-lookup"><span data-stu-id="23a7e-113">Before</span></span>                                                      |
|-------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)  |
| <span data-ttu-id="23a7e-115">Nach</span><span class="sxs-lookup"><span data-stu-id="23a7e-115">After</span></span>                                                       |
| ![das Bild nach der Transformation.](images/34-brightness.png) |



 


```C++
ComPtr<ID2D1Effect> brightnessEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Brightness, &brightnessEffect);

brightnessEffect->SetValue(D2D1_BRIGHTNESS_PROP_BLACK_POINT, D2D1::Vector2F(0.0f, 0.2f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(brightnessEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="23a7e-117">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="23a7e-117">Effect properties</span></span>



| <span data-ttu-id="23a7e-118">Anzeige Name der Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="23a7e-118">Property Display Name</span></span>                                                 | <span data-ttu-id="23a7e-119">Typ und Standardwert</span><span class="sxs-lookup"><span data-stu-id="23a7e-119">Type and default value</span></span>                              | <span data-ttu-id="23a7e-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23a7e-120">Description</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23a7e-121">WhitePoint</span><span class="sxs-lookup"><span data-stu-id="23a7e-121">WhitePoint</span></span><br/> <span data-ttu-id="23a7e-122">D2D1 Helligkeit-Trennzeichen \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="23a7e-122">D2D1\_BRIGHTNESS\_PROP\_WHITE\_POINT</span></span><br/> | <span data-ttu-id="23a7e-123">D2D1 \_ Vector \_ 2F</span><span class="sxs-lookup"><span data-stu-id="23a7e-123">D2D1\_VECTOR\_2F</span></span><br/> <span data-ttu-id="23a7e-124">{1.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="23a7e-124">{1.0f, 1.0f}</span></span><br/> | <span data-ttu-id="23a7e-125">Der obere Teil der Helligkeits Übertragungs Kurve.</span><span class="sxs-lookup"><span data-stu-id="23a7e-125">The upper portion of the brightness transfer curve.</span></span> <span data-ttu-id="23a7e-126">Der weiße Punkt passt die Darstellung der helleren Teile des Bilds an.</span><span class="sxs-lookup"><span data-stu-id="23a7e-126">The white point adjusts the appearance of the brighter portions of the image.</span></span> <span data-ttu-id="23a7e-127">Diese Eigenschaft gilt für den x-Wert und den y-Wert in dieser Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="23a7e-127">This property is for both the x value and the y value, in that order.</span></span> <span data-ttu-id="23a7e-128">Jeder Wert dieser Eigenschaft liegt zwischen 0 und 1 (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="23a7e-128">Each of the values of this property are between 0 and 1, inclusive.</span></span> |
| <span data-ttu-id="23a7e-129">Blackpoint</span><span class="sxs-lookup"><span data-stu-id="23a7e-129">BlackPoint</span></span><br/> <span data-ttu-id="23a7e-130">D2D1 Helligkeit-Trennzeichen \_ \_ \_ schwarz \_ Punkt</span><span class="sxs-lookup"><span data-stu-id="23a7e-130">D2D1\_BRIGHTNESS\_PROP\_BLACK\_POINT</span></span><br/> | <span data-ttu-id="23a7e-131">D2D1 \_ Vector \_ 2F</span><span class="sxs-lookup"><span data-stu-id="23a7e-131">D2D1\_VECTOR\_2F</span></span><br/> <span data-ttu-id="23a7e-132">{0,0 f, 0,0 f}</span><span class="sxs-lookup"><span data-stu-id="23a7e-132">{0.0f, 0.0f}</span></span><br/> | <span data-ttu-id="23a7e-133">Der untere Teil der Helligkeits Übertragungs Kurve.</span><span class="sxs-lookup"><span data-stu-id="23a7e-133">The lower portion of the brightness transfer curve.</span></span> <span data-ttu-id="23a7e-134">Der schwarze Punkt passt die Darstellung der dunkleren Teile des Bilds an.</span><span class="sxs-lookup"><span data-stu-id="23a7e-134">The black point adjusts the appearance of the darker portions of the image.</span></span> <span data-ttu-id="23a7e-135">Diese Eigenschaft gilt für den x-Wert und den y-Wert in dieser Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="23a7e-135">This property is for both the x value and the y value, in that order.</span></span> <span data-ttu-id="23a7e-136">Jeder Wert dieser Eigenschaft liegt zwischen 0 und 1 (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="23a7e-136">Each of the values of this property are between 0 and 1, inclusive.</span></span>   |



 

<span data-ttu-id="23a7e-137">Dieser Effekt verwendet die angegebenen weißen und schwarzen Punkte, um eine Übertragungsfunktion zu generieren, mit der die Bitmap angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="23a7e-137">This effect uses the specified white and black points to generate a transfer function used to adjust the bitmap.</span></span> <span data-ttu-id="23a7e-138">In der nächsten Gleichung wird die Übertragungsfunktion beschrieben.</span><span class="sxs-lookup"><span data-stu-id="23a7e-138">The next equation describes the transfer function.</span></span> <span data-ttu-id="23a7e-139">Die Eingabe Intensitäten werden zwischen 0 und 1 definiert.</span><span class="sxs-lookup"><span data-stu-id="23a7e-139">The input intensities are defined between 0 and 1.</span></span>

![Helligkeits Algorithmus](images/brightness-formula1.png)

<span data-ttu-id="23a7e-141">Der Effekt Algorithmus implementiert eine Gleichung, die die Übertragungsfunktion erstellt.</span><span class="sxs-lookup"><span data-stu-id="23a7e-141">The effect algorithm implements an equation that creates the transfer function.</span></span> <span data-ttu-id="23a7e-142">Mit dieser Funktion werden die Bild Pixel angepasst.</span><span class="sxs-lookup"><span data-stu-id="23a7e-142">We use this function to adjust the image pixels.</span></span> <span data-ttu-id="23a7e-143">Der x-und der y-Wert des schwarzen Punkts und der weiße Punkt sind die Koordinaten in zwei Dimensionen, die mit der Transformation verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="23a7e-143">The x and y values of the black point and the white point are the coordinates in two dimensions that are connected to form the transform.</span></span> <span data-ttu-id="23a7e-144">Jeder Teil der endgültigen Ausgabe Gleichung:</span><span class="sxs-lookup"><span data-stu-id="23a7e-144">Each part of the final output equation:</span></span>

1.  <span data-ttu-id="23a7e-145">Konvertiert die Bilddaten aus dem linearen Raum mithilfe dieser Gleichung in einen nichtlinearen Raum:</span><span class="sxs-lookup"><span data-stu-id="23a7e-145">Converts the image data from linear space to non-linear space using this equation:</span></span>![Hilfsfunktion 1](images/brightness-formula2.png)

2.  <span data-ttu-id="23a7e-147">Passt das Bild entsprechend den folgenden Werten an:</span><span class="sxs-lookup"><span data-stu-id="23a7e-147">Adjusts the image according to these values:</span></span>
    -   <span data-ttu-id="23a7e-148">*Input* ist die Pixel Intensität der Eingabebild Werte zwischen 0 und 1.</span><span class="sxs-lookup"><span data-stu-id="23a7e-148">*input* is the input image pixel intensity values from 0 to 1.</span></span>

    -   <span data-ttu-id="23a7e-149">*White PT. (x, y)* der Speicherort der Transformations Kurve für hellere Pixel Intensitäten.</span><span class="sxs-lookup"><span data-stu-id="23a7e-149">*White Pt. (x, y)* the location of the transform curve for brighter pixel intensities.</span></span>

    -   <span data-ttu-id="23a7e-150">*Schwarz PT. (x, y)* ist der Speicherort der Transformations Kurve für schwächer-Pixel Intensitäten.</span><span class="sxs-lookup"><span data-stu-id="23a7e-150">*Black Pt. (x, y)* is the location of the transform curve for dimmer pixel intensities.</span></span>

3.  <span data-ttu-id="23a7e-151">Konvertiert die Bilddaten mit dieser Gleichung zurück in den linearen Raum:</span><span class="sxs-lookup"><span data-stu-id="23a7e-151">Converts the image data back to linear space using this equation:</span></span> ![Hilfsfunktion 2](images/brightness-formula3.png)

<span data-ttu-id="23a7e-153">Hier werden die endgültige Ausgabe Gleichung und die Komponenten Teile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="23a7e-153">The final output equation and the component parts are shown here.</span></span>

![die gesamten Berechnungen für die Helligkeitsanpassung](images/brightness-formula4.png)

## <a name="output-bitmap"></a><span data-ttu-id="23a7e-155">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="23a7e-155">Output bitmap</span></span>

<span data-ttu-id="23a7e-156">Die Größe der Ausgabe Bitmap entspricht der Größe der Eingabe Bitmap.</span><span class="sxs-lookup"><span data-stu-id="23a7e-156">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="23a7e-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23a7e-157">Requirements</span></span>



| <span data-ttu-id="23a7e-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23a7e-158">Requirement</span></span> | <span data-ttu-id="23a7e-159">Wert</span><span class="sxs-lookup"><span data-stu-id="23a7e-159">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="23a7e-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="23a7e-160">Minimum supported client</span></span> | <span data-ttu-id="23a7e-161">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23a7e-161">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="23a7e-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="23a7e-162">Minimum supported server</span></span> | <span data-ttu-id="23a7e-163">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23a7e-163">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="23a7e-164">Header</span><span class="sxs-lookup"><span data-stu-id="23a7e-164">Header</span></span>                   | <span data-ttu-id="23a7e-165">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="23a7e-165">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="23a7e-166">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="23a7e-166">Library</span></span>                  | <span data-ttu-id="23a7e-167">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="23a7e-167">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="23a7e-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="23a7e-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23a7e-169">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="23a7e-169">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

