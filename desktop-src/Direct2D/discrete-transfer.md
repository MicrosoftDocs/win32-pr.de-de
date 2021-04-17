---
title: Diskreter Übertragungs Effekt
description: Verwenden Sie den diskreten Übertragungs Effekt, um die Farb Intensitäten eines Bilds mithilfe einer Schritt Übertragungsfunktion zuzuordnen, die aus einer Liste mit von Ihnen bereitgestellten Werten erstellt wurde.
ms.assetid: 5A612002-2B1D-4FC3-B364-AACD9FD44BEC
keywords:
- diskreter Übertragungs Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c05ef08f9ddf053eaa686cb0f88d4183194d9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104567575"
---
# <a name="discrete-transfer-effect"></a><span data-ttu-id="11ec5-104">Diskreter Übertragungs Effekt</span><span class="sxs-lookup"><span data-stu-id="11ec5-104">Discrete transfer effect</span></span>

<span data-ttu-id="11ec5-105">Verwenden Sie den diskreten Übertragungs Effekt, um die Farb Intensitäten eines Bilds mithilfe einer Schritt Übertragungsfunktion zuzuordnen, die aus einer Liste mit von Ihnen bereitgestellten Werten erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="11ec5-105">Use the discrete transfer effect to map the color intensities of an image using a step transfer function created from a list of values you provide.</span></span>

<span data-ttu-id="11ec5-106">Die CLSID für diesen Effekt ist CLSID \_ D2D1DiscreteTransfer.</span><span class="sxs-lookup"><span data-stu-id="11ec5-106">The CLSID for this effect is CLSID\_D2D1DiscreteTransfer.</span></span>

-   [<span data-ttu-id="11ec5-107">Beispiel Bild</span><span class="sxs-lookup"><span data-stu-id="11ec5-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="11ec5-108">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11ec5-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="11ec5-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11ec5-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="11ec5-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="11ec5-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="11ec5-111">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="11ec5-111">Example image</span></span>

<span data-ttu-id="11ec5-112">Das Bild hier zeigt die Eingabe und die Ausgabe des diskreten Übertragungs Effekts.</span><span class="sxs-lookup"><span data-stu-id="11ec5-112">The image here shows the input and output of the discrete transfer effect.</span></span>



| <span data-ttu-id="11ec5-113">Vorher</span><span class="sxs-lookup"><span data-stu-id="11ec5-113">Before</span></span>                                                            |
|-------------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)        |
| <span data-ttu-id="11ec5-115">Nach</span><span class="sxs-lookup"><span data-stu-id="11ec5-115">After</span></span>                                                             |
| ![das Bild nach der Transformation.](images/12-discretetransfer.png) |



 


```C++
ComPtr<ID2D1Effect> discreteTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DiscreteTransfer, &discreteTransferEffect);

discreteTransferEffect->SetInput(0, bitmap);

float table[3] = {0.0f, 0.5f, 1.0f};
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_RED_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_GREEN_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(discreteTransferEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="11ec5-117">Die Übertragungsfunktion basiert auf der Liste der Eingaben: V = (v0, v1, v2, v3, V?</span><span class="sxs-lookup"><span data-stu-id="11ec5-117">The transfer function is based on the list of inputs: V=(V0,V1,V2,V3,V?</span></span> <span data-ttu-id="11ec5-118">, V<sub>N</sub>), wobei N die Anzahl der Elemente-1 ist.</span><span class="sxs-lookup"><span data-stu-id="11ec5-118">,V<sub>N</sub>) where N is the number of elements - 1.</span></span>

<span data-ttu-id="11ec5-119">Die Eingabe Pixel Intensität wird als C dargestellt. Die Ausgabe Pixel Intensität, C wird mit der Gleichung berechnet:</span><span class="sxs-lookup"><span data-stu-id="11ec5-119">The input pixel intensity is represented as C. The output pixel intensity, C  is calculated with the equation:</span></span>

<span data-ttu-id="11ec5-120">Wählen Sie für einen Wert C den Wert k aus, um Folgendes zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="11ec5-120">For a value C, pick a value k, such that:</span></span>

![die Formel für den Prozess.](images/discrete-transfer1.png)

<span data-ttu-id="11ec5-122">Die Ausgabe c kann mit der Gleichung berechnet werden: c ' = V?</span><span class="sxs-lookup"><span data-stu-id="11ec5-122">The output C  can be calculated using the equation: C' = V?</span></span>

<span data-ttu-id="11ec5-123">Dieser Effekt kann bei geraden und vorab multiplizierten Alpha Bildern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="11ec5-123">This effect works on straight and premultiplied alpha images.</span></span> <span data-ttu-id="11ec5-124">Der Effekt gibt prämultiplizierte Alpha Bitmaps aus.</span><span class="sxs-lookup"><span data-stu-id="11ec5-124">The effect outputs premultiplied alpha bitmaps.</span></span>

<span data-ttu-id="11ec5-125">So sieht das Diagramm der diskreten Übertragungsfunktion aus, wenn die Eingaben sind `[0.25, 0.5, 0.75, 1.0]` .</span><span class="sxs-lookup"><span data-stu-id="11ec5-125">Here is what the graph of discrete transfer function looks like if the inputs are `[0.25, 0.5, 0.75, 1.0]`.</span></span>

![Pixel Intensität des Diagramms für die diskrete Übertragungsfunktion.](images/discrete-transfer-graph.png)

## <a name="effect-properties"></a><span data-ttu-id="11ec5-127">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11ec5-127">Effect properties</span></span>

> [!Note]  
> <span data-ttu-id="11ec5-128">Die Werte aller Kanäle der diskreten Übertragungseigenschaften sind unitless und haben mindestens 0,0 und einen maximalen Wert von 1,0.</span><span class="sxs-lookup"><span data-stu-id="11ec5-128">The values of all channels of the discrete transfer properties are unitless and have a minimum of 0.0 and a maximum 1.0.</span></span>

 



| <span data-ttu-id="11ec5-129">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="11ec5-129">Display name and index enumeration</span></span>                                              | <span data-ttu-id="11ec5-130">Typ und Standardwert</span><span class="sxs-lookup"><span data-stu-id="11ec5-130">Type and default value</span></span>                       | <span data-ttu-id="11ec5-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11ec5-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11ec5-132">Redtable</span><span class="sxs-lookup"><span data-stu-id="11ec5-132">RedTable</span></span><br/> <span data-ttu-id="11ec5-133">D2D1 \_ diskretetransfer \_ ( \_ Rote \_ Tabelle)</span><span class="sxs-lookup"><span data-stu-id="11ec5-133">D2D1\_DISCRETETRANSFER\_PROP\_RED\_TABLE</span></span><br/>         | <span data-ttu-id="11ec5-134">Hafen\[\]</span><span class="sxs-lookup"><span data-stu-id="11ec5-134">FLOAT\[\]</span></span><br/> <span data-ttu-id="11ec5-135">{0,0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="11ec5-135">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="11ec5-136">Die Liste der Werte, die zum Definieren der Übertragungsfunktion für den roten Kanal verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="11ec5-136">The list of values used to define the transfer function for the Red channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="11ec5-137">Reddeaktiviert</span><span class="sxs-lookup"><span data-stu-id="11ec5-137">RedDisable</span></span><br/> <span data-ttu-id="11ec5-138">D2D1 \_ diskretetransfer-unter \_ Stützung \_ rot \_ Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="11ec5-138">D2D1\_DISCRETETRANSFER\_PROP\_RED\_DISABLE</span></span><br/>     | <span data-ttu-id="11ec5-139">BOOL</span><span class="sxs-lookup"><span data-stu-id="11ec5-139">BOOL</span></span><br/> <span data-ttu-id="11ec5-140">false</span><span class="sxs-lookup"><span data-stu-id="11ec5-140">FALSE</span></span><br/>             | <span data-ttu-id="11ec5-141">Wenn Sie diese Einstellung auf "true" festlegen, wird die Übertragungsfunktion nicht auf den roten Kanal angewendet.</span><span class="sxs-lookup"><span data-stu-id="11ec5-141">If you set this to TRUE the effect does not apply the transfer function to the Red channel.</span></span> <span data-ttu-id="11ec5-142">Wenn Sie diese Einstellung auf "false" festlegen, wendet der Effekt die reddiskretetransfer-Funktion auf den roten Kanal an.</span><span class="sxs-lookup"><span data-stu-id="11ec5-142">If you set this to FALSE the effect applies the RedDiscreteTransfer function to the Red channel.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="11ec5-143">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="11ec5-143">GreenTable</span></span><br/> <span data-ttu-id="11ec5-144">D2D1 \_ diskretetransfer-unter \_ Stützung für \_ grüne \_ Tabelle</span><span class="sxs-lookup"><span data-stu-id="11ec5-144">D2D1\_DISCRETETRANSFER\_PROP\_GREEN\_TABLE</span></span><br/>     | <span data-ttu-id="11ec5-145">Hafen\[\]</span><span class="sxs-lookup"><span data-stu-id="11ec5-145">FLOAT\[\]</span></span><br/> <span data-ttu-id="11ec5-146">{0,0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="11ec5-146">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="11ec5-147">Die Liste der Werte, die die Übertragungsfunktion für den grünen Kanal definieren.</span><span class="sxs-lookup"><span data-stu-id="11ec5-147">The list of values that define the transfer function for the Green channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="11ec5-148">Greendeaktivieren</span><span class="sxs-lookup"><span data-stu-id="11ec5-148">GreenDisable</span></span><br/> <span data-ttu-id="11ec5-149">D2D1 \_ diskretetransfer- \_ Prop \_ grün \_ Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="11ec5-149">D2D1\_DISCRETETRANSFER\_PROP\_GREEN\_DISABLE</span></span><br/> | <span data-ttu-id="11ec5-150">BOOL</span><span class="sxs-lookup"><span data-stu-id="11ec5-150">BOOL</span></span><br/> <span data-ttu-id="11ec5-151">false</span><span class="sxs-lookup"><span data-stu-id="11ec5-151">FALSE</span></span><br/>             | <span data-ttu-id="11ec5-152">Wenn Sie diese Einstellung auf "true" festlegen, wird die Übertragungsfunktion nicht auf den grünen Kanal angewendet.</span><span class="sxs-lookup"><span data-stu-id="11ec5-152">If you set this to TRUE the effect does not apply the transfer function to the Green channel.</span></span> <span data-ttu-id="11ec5-153">Wenn Sie diese Einstellung auf "false" festlegen, wendet der Effekt die greendiskretetransfer-Funktion auf den grünen Kanal an.</span><span class="sxs-lookup"><span data-stu-id="11ec5-153">If you set this to FALSE the effect applies the GreenDiscreteTransfer function to the Green channel.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="11ec5-154">Bluetable</span><span class="sxs-lookup"><span data-stu-id="11ec5-154">BlueTable</span></span><br/> <span data-ttu-id="11ec5-155">D2D1 \_ diskretetransfer- \_ Prop ( \_ blaue \_ Tabelle)</span><span class="sxs-lookup"><span data-stu-id="11ec5-155">D2D1\_DISCRETETRANSFER\_PROP\_BLUE\_TABLE</span></span><br/>       | <span data-ttu-id="11ec5-156">Hafen\[\]</span><span class="sxs-lookup"><span data-stu-id="11ec5-156">FLOAT\[\]</span></span><br/> <span data-ttu-id="11ec5-157">{0,0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="11ec5-157">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="11ec5-158">Die Liste der Werte, die die Übertragungsfunktion für den blauen Kanal definieren.</span><span class="sxs-lookup"><span data-stu-id="11ec5-158">The list of values that define the transfer function for the Blue channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="11ec5-159">Bluedeaktiviert</span><span class="sxs-lookup"><span data-stu-id="11ec5-159">BlueDisable</span></span><br/> <span data-ttu-id="11ec5-160">D2D1 \_ diskretetransfer- \_ Prop \_ blau \_ Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="11ec5-160">D2D1\_DISCRETETRANSFER\_PROP\_BLUE\_DISABLE</span></span><br/>   | <span data-ttu-id="11ec5-161">BOOL</span><span class="sxs-lookup"><span data-stu-id="11ec5-161">BOOL</span></span><br/> <span data-ttu-id="11ec5-162">false</span><span class="sxs-lookup"><span data-stu-id="11ec5-162">FALSE</span></span><br/>             | <span data-ttu-id="11ec5-163">Wenn Sie diese Einstellung auf "true" festlegen, wird die Übertragungsfunktion nicht auf den blauen Kanal angewendet.</span><span class="sxs-lookup"><span data-stu-id="11ec5-163">If you set this to TRUE the effect does not apply the transfer function to the Blue channel.</span></span> <span data-ttu-id="11ec5-164">Wenn Sie diese Einstellung auf "false" festlegen, wird die bluediskretetransfer-Funktion auf den blauen Kanal angewendet.</span><span class="sxs-lookup"><span data-stu-id="11ec5-164">If you set this to FALSE the effect applies the BlueDiscreteTransfer function to the Blue channel.</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="11ec5-165">Alpha kompatibel</span><span class="sxs-lookup"><span data-stu-id="11ec5-165">AlphaTable</span></span><br/> <span data-ttu-id="11ec5-166">D2D1 \_ diskretetransfer- \_ Prop- \_ alpha \_ Tabelle</span><span class="sxs-lookup"><span data-stu-id="11ec5-166">D2D1\_DISCRETETRANSFER\_PROP\_ALPHA\_TABLE</span></span><br/>     | <span data-ttu-id="11ec5-167">Hafen\[\]</span><span class="sxs-lookup"><span data-stu-id="11ec5-167">FLOAT\[\]</span></span><br/> <span data-ttu-id="11ec5-168">{0,0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="11ec5-168">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="11ec5-169">Die Liste der Werte, die die Übertragungsfunktion für den Alpha Kanal definieren.</span><span class="sxs-lookup"><span data-stu-id="11ec5-169">The list of values that define the transfer function for the Alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="11ec5-170">Alphadeaktivieren</span><span class="sxs-lookup"><span data-stu-id="11ec5-170">AlphaDisable</span></span><br/> <span data-ttu-id="11ec5-171">D2D1 \_ diskretetransfer- \_ Prop- \_ alpha \_ Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="11ec5-171">D2D1\_DISCRETETRANSFER\_PROP\_ALPHA\_DISABLE</span></span><br/> | <span data-ttu-id="11ec5-172">BOOL</span><span class="sxs-lookup"><span data-stu-id="11ec5-172">BOOL</span></span><br/> <span data-ttu-id="11ec5-173">false</span><span class="sxs-lookup"><span data-stu-id="11ec5-173">FALSE</span></span><br/>             | <span data-ttu-id="11ec5-174">Wenn Sie diese Einstellung auf "true" festlegen, wird die Übertragungsfunktion nicht auf den Alpha Kanal angewendet.</span><span class="sxs-lookup"><span data-stu-id="11ec5-174">If you set this to TRUE the effect does not apply the transfer function to the Alpha channel.</span></span> <span data-ttu-id="11ec5-175">Wenn Sie diese Einstellung auf false festlegen, wird die alphadiskretetransfer-Funktion auf den Alpha Kanal angewendet.</span><span class="sxs-lookup"><span data-stu-id="11ec5-175">If you set this to FALSE the effect applies the AlphaDiscreteTransfer function to the Alpha channel.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="11ec5-176">Klamme Ausgabe</span><span class="sxs-lookup"><span data-stu-id="11ec5-176">ClampOutput</span></span><br/> <span data-ttu-id="11ec5-177">D2D1 \_ diskretetransfer- \_ Prop- \_ Klemm \_ Ausgabe</span><span class="sxs-lookup"><span data-stu-id="11ec5-177">D2D1\_DISCRETETRANSFER\_PROP\_CLAMP\_OUTPUT</span></span><br/>   | <span data-ttu-id="11ec5-178">BOOL</span><span class="sxs-lookup"><span data-stu-id="11ec5-178">BOOL</span></span><br/> <span data-ttu-id="11ec5-179">false</span><span class="sxs-lookup"><span data-stu-id="11ec5-179">FALSE</span></span><br/>             | <span data-ttu-id="11ec5-180">Gibt an, ob der Effekt Farbwerte auf zwischen 0 und 1 zeigt, bevor der Effekt die Werte an den nächsten Effekt im Diagramm übergibt.</span><span class="sxs-lookup"><span data-stu-id="11ec5-180">Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <span data-ttu-id="11ec5-181">Der Effekt bindet die Werte, bevor die Alpha-angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="11ec5-181">The effect clamps the values before it premultiplies the alpha.</span></span><br/> <span data-ttu-id="11ec5-182">Wenn Sie diese Einstellung auf "true" festlegen, werden die Werte durch die Auswirkung fixiert.</span><span class="sxs-lookup"><span data-stu-id="11ec5-182">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="11ec5-183">Wenn Sie diese Einstellung auf "false" festlegen, werden die Farbwerte durch die Auswirkung nicht fixiert, aber andere Effekte und die Ausgabe Oberfläche können die Werte einspannen, wenn Sie nicht über eine hohe Genauigkeit verfügen.</span><span class="sxs-lookup"><span data-stu-id="11ec5-183">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="11ec5-184">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11ec5-184">Requirements</span></span>



| <span data-ttu-id="11ec5-185">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11ec5-185">Requirement</span></span> | <span data-ttu-id="11ec5-186">Wert</span><span class="sxs-lookup"><span data-stu-id="11ec5-186">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="11ec5-187">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11ec5-187">Minimum supported client</span></span> | <span data-ttu-id="11ec5-188">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11ec5-188">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="11ec5-189">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11ec5-189">Minimum supported server</span></span> | <span data-ttu-id="11ec5-190">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11ec5-190">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="11ec5-191">Header</span><span class="sxs-lookup"><span data-stu-id="11ec5-191">Header</span></span>                   | <span data-ttu-id="11ec5-192">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="11ec5-192">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="11ec5-193">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="11ec5-193">Library</span></span>                  | <span data-ttu-id="11ec5-194">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="11ec5-194">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="11ec5-195">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="11ec5-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11ec5-196">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="11ec5-196">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

