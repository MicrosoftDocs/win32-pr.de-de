---
title: Tabellen Übertragungs Effekt
description: Verwenden Sie den Tabellen Übertragungs Effekt, um die Farb Intensitäten eines Bilds mithilfe einer Übertragungsfunktion zuzuordnen, die aus der Interpolation einer Liste mit von Ihnen bereitgestellten Werten erstellt wurde.
ms.assetid: FB426909-3C91-4709-9E3A-E45C7AE345A3
keywords:
- Tabellen Übertragungs Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d590e7f232ac3d4cecd434786353dfc5b8ea80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476752"
---
# <a name="table-transfer-effect"></a><span data-ttu-id="e077e-104">Tabellen Übertragungs Effekt</span><span class="sxs-lookup"><span data-stu-id="e077e-104">Table transfer effect</span></span>

<span data-ttu-id="e077e-105">Verwenden Sie den Tabellen Übertragungs Effekt, um die Farb Intensitäten eines Bilds mithilfe einer Übertragungsfunktion zuzuordnen, die aus der Interpolation einer Liste mit von Ihnen bereitgestellten Werten erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e077e-105">Use the table transfer effect to map the color intensities of an image using a transfer function created from interpolating a list of values you provide.</span></span>

<span data-ttu-id="e077e-106">Die CLSID für diesen Effekt ist CLSID \_ D2D1TableTransfer.</span><span class="sxs-lookup"><span data-stu-id="e077e-106">The CLSID for this effect is CLSID\_D2D1TableTransfer.</span></span>

-   [<span data-ttu-id="e077e-107">Beispiel Bild</span><span class="sxs-lookup"><span data-stu-id="e077e-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="e077e-108">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e077e-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="e077e-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e077e-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="e077e-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e077e-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="e077e-111">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="e077e-111">Example image</span></span>

<span data-ttu-id="e077e-112">Das Bild hier zeigt die Eingabe und die Ausgabe des Tabellen Übertragungs Effekts.</span><span class="sxs-lookup"><span data-stu-id="e077e-112">The image here shows the input and output of the table transfer effect.</span></span>



| <span data-ttu-id="e077e-113">Vorher</span><span class="sxs-lookup"><span data-stu-id="e077e-113">Before</span></span>                                                         |
|----------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)     |
| <span data-ttu-id="e077e-115">Nach</span><span class="sxs-lookup"><span data-stu-id="e077e-115">After</span></span>                                                          |
| ![das Bild nach der Transformation.](images/11-tabletransfer.png) |



 


```C++
ComPtr<ID2D1Effect> tableTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1TableTransfer, &tableTransferEffect);

tableTransferEffect->SetInput(0, bitmap);

float table[2] = {0.75f, 1.0f};
tableTransferEffect->SetValue(D2D1_TABLETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tableTransferEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="e077e-117">Die Übertragungsfunktion basiert auf einer Liste von Eingaben V = (v0, v1, v2, v3, V?</span><span class="sxs-lookup"><span data-stu-id="e077e-117">The transfer function is based on a list of inputs V=(V0,V1,V2,V3, V?</span></span> <span data-ttu-id="e077e-118">, V<sub>N</sub>), wobei N die Anzahl der Elemente-1 ist.</span><span class="sxs-lookup"><span data-stu-id="e077e-118">,V<sub>N</sub>) where N is the number of elements - 1.</span></span>

<span data-ttu-id="e077e-119">Die Eingabe Pixel Intensität wird als C dargestellt. Die Ausgabe Pixel Intensität C kann mit der Gleichung berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="e077e-119">The input pixel intensity is represented as C. The output pixel intensity, C  can be calculated with the equation.</span></span>

<span data-ttu-id="e077e-120">Wählen Sie für einen Wert C einen Wert k aus, z. b.: k/N = C < (k + 1)/N</span><span class="sxs-lookup"><span data-stu-id="e077e-120">For a value C, pick a value k, such that: k/N = C < (k+1)/N</span></span>

<span data-ttu-id="e077e-121">Die Ausgabe c wird mithilfe der folgenden Gleichung berechnet: c ' = V?</span><span class="sxs-lookup"><span data-stu-id="e077e-121">The output C  is calculated using the following equation: C' = V?</span></span> <span data-ttu-id="e077e-122">+ (C-k/n) \* N \* (V??? 1?</span><span class="sxs-lookup"><span data-stu-id="e077e-122">+ (C -  k/N) \* N \* (V???1?</span></span> <span data-ttu-id="e077e-123">-V?)</span><span class="sxs-lookup"><span data-stu-id="e077e-123">- V?)</span></span>

<span data-ttu-id="e077e-124">Dieser Effekt kann bei geraden und vorab multiplizierten Alpha Bildern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e077e-124">This effect works on straight and premultiplied alpha images.</span></span> <span data-ttu-id="e077e-125">Der Effekt gibt prämultiplizierte Alpha Bitmaps aus.</span><span class="sxs-lookup"><span data-stu-id="e077e-125">The effect outputs premultiplied alpha bitmaps.</span></span>

<span data-ttu-id="e077e-126">So sieht das Diagramm der Tabellen Übertragungsfunktion aus, wenn die Table-Eigenschaft auf festgelegt ist `[0.0, 0.25, 1.0]` .</span><span class="sxs-lookup"><span data-stu-id="e077e-126">Here is what the graph of table transfer function looks like if the table property is set to `[0.0, 0.25, 1.0]`.</span></span>

![Pixel Intensität des Diagramms für die Tabellen Übertragungsfunktion.](images/table-transfer-graph.png)

## <a name="effect-properties"></a><span data-ttu-id="e077e-128">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e077e-128">Effect properties</span></span>

> [!Note]  
> <span data-ttu-id="e077e-129">Die Werte aller Kanäle der Tabellen Übertragungseigenschaften sind unitless und haben mindestens 0,0 und einen maximalen Wert von 1,0.</span><span class="sxs-lookup"><span data-stu-id="e077e-129">The values of all channels of the table transfer properties are unitless and have a minimum of 0.0 and a maximum 1.0.</span></span>

 



| <span data-ttu-id="e077e-130">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="e077e-130">Display name and index enumeration</span></span>                                           | <span data-ttu-id="e077e-131">Typ und Standardwert</span><span class="sxs-lookup"><span data-stu-id="e077e-131">Type and default value</span></span>                       | <span data-ttu-id="e077e-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e077e-132">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e077e-133">Redtable</span><span class="sxs-lookup"><span data-stu-id="e077e-133">RedTable</span></span><br/> <span data-ttu-id="e077e-134">D2D1 \_ tabletransfer \_ Prop ( \_ Rote \_ Tabelle)</span><span class="sxs-lookup"><span data-stu-id="e077e-134">D2D1\_TABLETRANSFER\_PROP\_RED\_TABLE</span></span><br/>         | <span data-ttu-id="e077e-135">Hafen\[\]</span><span class="sxs-lookup"><span data-stu-id="e077e-135">FLOAT\[\]</span></span><br/> <span data-ttu-id="e077e-136">{0,0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="e077e-136">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="e077e-137">Die Liste der Werte, die zum Definieren der Übertragungsfunktion für den roten Kanal verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e077e-137">The list of values used to define the transfer function for the Red channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="e077e-138">Reddeaktiviert</span><span class="sxs-lookup"><span data-stu-id="e077e-138">RedDisable</span></span><br/> <span data-ttu-id="e077e-139">D2D1 \_ tabletransfer \_ Prop \_ rot \_ Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="e077e-139">D2D1\_TABLETRANSFER\_PROP\_RED\_DISABLE</span></span><br/>     | <span data-ttu-id="e077e-140">BOOL</span><span class="sxs-lookup"><span data-stu-id="e077e-140">BOOL</span></span><br/> <span data-ttu-id="e077e-141">false</span><span class="sxs-lookup"><span data-stu-id="e077e-141">FALSE</span></span><br/>             | <span data-ttu-id="e077e-142">Wenn Sie diese Einstellung auf "true" festlegen, wird die Übertragungsfunktion nicht auf den roten Kanal angewendet.</span><span class="sxs-lookup"><span data-stu-id="e077e-142">If you set this to TRUE the effect does not apply the transfer function to the Red channel.</span></span> <span data-ttu-id="e077e-143">Wenn Sie diese Einstellung auf "false" festlegen, wird die redtabletransfer-Funktion auf den roten Kanal angewendet.</span><span class="sxs-lookup"><span data-stu-id="e077e-143">If you set this to FALSE it applies the RedTableTransfer function to the Red channel.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="e077e-144">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="e077e-144">GreenTable</span></span><br/> <span data-ttu-id="e077e-145">D2D1 \_ tabletransfer \_ Prop ( \_ grüne \_ Tabelle)</span><span class="sxs-lookup"><span data-stu-id="e077e-145">D2D1\_TABLETRANSFER\_PROP\_GREEN\_TABLE</span></span><br/>     | <span data-ttu-id="e077e-146">Hafen\[\]</span><span class="sxs-lookup"><span data-stu-id="e077e-146">FLOAT\[\]</span></span><br/> <span data-ttu-id="e077e-147">{0,0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="e077e-147">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="e077e-148">Die Liste der Werte, die zum Definieren der Übertragungsfunktion für den grünen Kanal verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e077e-148">The list of values used to define the transfer function for the Green channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="e077e-149">Greendeaktivieren</span><span class="sxs-lookup"><span data-stu-id="e077e-149">GreenDisable</span></span><br/> <span data-ttu-id="e077e-150">D2D1 \_ tabletransfer \_ Prop \_ grün \_ Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="e077e-150">D2D1\_TABLETRANSFER\_PROP\_GREEN\_DISABLE</span></span><br/> | <span data-ttu-id="e077e-151">BOOL</span><span class="sxs-lookup"><span data-stu-id="e077e-151">BOOL</span></span><br/> <span data-ttu-id="e077e-152">false</span><span class="sxs-lookup"><span data-stu-id="e077e-152">FALSE</span></span><br/>             | <span data-ttu-id="e077e-153">Wenn Sie diese Einstellung auf "true" festlegen, wird die Übertragungsfunktion nicht auf den grünen Kanal angewendet.</span><span class="sxs-lookup"><span data-stu-id="e077e-153">If you set this to TRUE the effect does not apply the transfer function to the Green channel.</span></span> <span data-ttu-id="e077e-154">Wenn Sie diese Einstellung auf "false" festlegen, wird die greentabletransfer-Funktion auf den grünen Kanal angewendet.</span><span class="sxs-lookup"><span data-stu-id="e077e-154">If you set this to FALSE it applies the GreenTableTransfer function to the Green channel.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="e077e-155">Bluetable</span><span class="sxs-lookup"><span data-stu-id="e077e-155">BlueTable</span></span><br/> <span data-ttu-id="e077e-156">D2D1 \_ tabletransfer \_ Prop ( \_ blaue \_ Tabelle)</span><span class="sxs-lookup"><span data-stu-id="e077e-156">D2D1\_TABLETRANSFER\_PROP\_BLUE\_TABLE</span></span><br/>       | <span data-ttu-id="e077e-157">Hafen\[\]</span><span class="sxs-lookup"><span data-stu-id="e077e-157">FLOAT\[\]</span></span><br/> <span data-ttu-id="e077e-158">{0,0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="e077e-158">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="e077e-159">Die Liste der Werte, die zum Definieren der Übertragungsfunktion für den blauen Kanal verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e077e-159">The list of values used to define the transfer function for the Blue channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="e077e-160">Bluedeaktiviert</span><span class="sxs-lookup"><span data-stu-id="e077e-160">BlueDisable</span></span><br/> <span data-ttu-id="e077e-161">D2D1 \_ tabletransfer \_ Prop \_ blau \_ Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="e077e-161">D2D1\_TABLETRANSFER\_PROP\_BLUE\_DISABLE</span></span><br/>   | <span data-ttu-id="e077e-162">BOOL</span><span class="sxs-lookup"><span data-stu-id="e077e-162">BOOL</span></span><br/> <span data-ttu-id="e077e-163">false</span><span class="sxs-lookup"><span data-stu-id="e077e-163">FALSE</span></span><br/>             | <span data-ttu-id="e077e-164">Wenn Sie diese Einstellung auf "true" festlegen, wird die Übertragungsfunktion nicht auf den blauen Kanal angewendet.</span><span class="sxs-lookup"><span data-stu-id="e077e-164">If you set this to TRUE the effect does not apply the transfer function to the Blue channel.</span></span> <span data-ttu-id="e077e-165">Wenn Sie diese Einstellung auf "false" festlegen, wird die bluetabletransfer-Funktion auf den blauen Kanal angewendet.</span><span class="sxs-lookup"><span data-stu-id="e077e-165">If you set this to FALSE it applies the BlueTableTransfer function to the Blue channel.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="e077e-166">Alpha kompatibel</span><span class="sxs-lookup"><span data-stu-id="e077e-166">AlphaTable</span></span><br/> <span data-ttu-id="e077e-167">D2D1 \_ Table \_ Transfer \_ Prop- \_ alpha \_ Tabelle</span><span class="sxs-lookup"><span data-stu-id="e077e-167">D2D1\_TABLE\_TRANSFER\_PROP\_ALPHA\_TABLE</span></span><br/>   | <span data-ttu-id="e077e-168">Hafen\[\]</span><span class="sxs-lookup"><span data-stu-id="e077e-168">FLOAT\[\]</span></span><br/> <span data-ttu-id="e077e-169">{0,0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="e077e-169">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="e077e-170">Die Liste der Werte, die zum Definieren der Übertragungsfunktion für den Alpha Kanal verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e077e-170">The list of values used to define the transfer function for the Alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="e077e-171">Alphadeaktivieren</span><span class="sxs-lookup"><span data-stu-id="e077e-171">AlphaDisable</span></span><br/> <span data-ttu-id="e077e-172">D2D1 \_ tabletransfer \_ Prop \_ alpha \_ Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="e077e-172">D2D1\_TABLETRANSFER\_PROP\_ALPHA\_DISABLE</span></span><br/> | <span data-ttu-id="e077e-173">BOOL</span><span class="sxs-lookup"><span data-stu-id="e077e-173">BOOL</span></span><br/> <span data-ttu-id="e077e-174">false</span><span class="sxs-lookup"><span data-stu-id="e077e-174">FALSE</span></span><br/>             | <span data-ttu-id="e077e-175">Wenn Sie diese Einstellung auf "true" festlegen, wird die Übertragungsfunktion nicht auf den Alpha Kanal angewendet.</span><span class="sxs-lookup"><span data-stu-id="e077e-175">If you set this to TRUE the effect does not apply the transfer function to the Alpha channel.</span></span> <span data-ttu-id="e077e-176">Wenn Sie diese Einstellung auf "false" festlegen, wird die Alpha atabletransfer-Funktion auf den Alpha Kanal angewendet.</span><span class="sxs-lookup"><span data-stu-id="e077e-176">If you set this to FALSE it applies the AlphaTableTransfer function to the Alpha channel.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="e077e-177">Klamme Ausgabe</span><span class="sxs-lookup"><span data-stu-id="e077e-177">ClampOutput</span></span><br/> <span data-ttu-id="e077e-178">D2D1 \_ tabletransfer \_ Prop \_ - \_ Ausgabe</span><span class="sxs-lookup"><span data-stu-id="e077e-178">D2D1\_TABLETRANSFER\_PROP\_CLAMP\_OUTPUT</span></span><br/>   | <span data-ttu-id="e077e-179">BOOL</span><span class="sxs-lookup"><span data-stu-id="e077e-179">BOOL</span></span><br/> <span data-ttu-id="e077e-180">false</span><span class="sxs-lookup"><span data-stu-id="e077e-180">FALSE</span></span><br/>             | <span data-ttu-id="e077e-181">Gibt an, ob der Effekt Farbwerte auf zwischen 0 und 1 zeigt, bevor der Effekt die Werte an den nächsten Effekt im Diagramm übergibt.</span><span class="sxs-lookup"><span data-stu-id="e077e-181">Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <span data-ttu-id="e077e-182">Der Effekt bindet die Werte, bevor die Alpha-angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e077e-182">The effect clamps the values before it premultiplies the alpha .</span></span><br/> <span data-ttu-id="e077e-183">Wenn Sie diese Einstellung auf "true" festlegen, werden die Werte durch die Auswirkung fixiert.</span><span class="sxs-lookup"><span data-stu-id="e077e-183">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="e077e-184">Wenn Sie diese Einstellung auf "false" festlegen, werden die Farbwerte durch die Auswirkung nicht fixiert, aber andere Effekte und die Ausgabe Oberfläche können die Werte einspannen, wenn Sie nicht über eine hohe Genauigkeit verfügen.</span><span class="sxs-lookup"><span data-stu-id="e077e-184">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e077e-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e077e-185">Requirements</span></span>



| <span data-ttu-id="e077e-186">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e077e-186">Requirement</span></span> | <span data-ttu-id="e077e-187">Wert</span><span class="sxs-lookup"><span data-stu-id="e077e-187">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e077e-188">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e077e-188">Minimum supported client</span></span> | <span data-ttu-id="e077e-189">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e077e-189">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e077e-190">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e077e-190">Minimum supported server</span></span> | <span data-ttu-id="e077e-191">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e077e-191">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e077e-192">Header</span><span class="sxs-lookup"><span data-stu-id="e077e-192">Header</span></span>                   | <span data-ttu-id="e077e-193">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="e077e-193">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="e077e-194">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e077e-194">Library</span></span>                  | <span data-ttu-id="e077e-195">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="e077e-195">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="e077e-196">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e077e-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e077e-197">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="e077e-197">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

