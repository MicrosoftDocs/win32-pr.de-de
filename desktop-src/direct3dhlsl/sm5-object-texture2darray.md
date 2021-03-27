---
title: Texture2DArray
description: Texture2DArray
ms.assetid: 78ab2feb-4d67-4f6f-bffe-48d55183ce28
keywords:
- Texture2DArray HLSL
topic_type:
- apiref
api_name:
- Texture2DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1aefa9171ed634934ea5e1306973fe3b22abdfa
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "104981000"
---
# <a name="texture2darray"></a><span data-ttu-id="cd6b5-104">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="cd6b5-104">Texture2DArray</span></span>

<span data-ttu-id="cd6b5-105">Texture2DArray Type ([wie er in Shader Model 4 vorhanden](dx-graphics-hlsl-to-type.md)ist) plus Ressourcenvariablen.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-105">Texture2DArray type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="cd6b5-106">Dieses Textur Objekt unterstützt zusätzlich zu den Methoden in Shader Model 4 die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="cd6b5-107">Methode</span><span class="sxs-lookup"><span data-stu-id="cd6b5-107">Method</span></span>                                                                      | <span data-ttu-id="cd6b5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd6b5-108">Description</span></span>                                                                                                                                         |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd6b5-109">**Informieren**</span><span class="sxs-lookup"><span data-stu-id="cd6b5-109">**Gather**</span></span>](texture2darray-gather.md)                                      | <span data-ttu-id="cd6b5-110">Gibt die vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-110">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>                                                                |
| [<span data-ttu-id="cd6b5-111">**Gatherred**</span><span class="sxs-lookup"><span data-stu-id="cd6b5-111">**GatherRed**</span></span>](texture2darray-gatherred.md)                                | <span data-ttu-id="cd6b5-112">Gibt die roten Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-112">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                          |
| [<span data-ttu-id="cd6b5-113">**Gathergrün**</span><span class="sxs-lookup"><span data-stu-id="cd6b5-113">**GatherGreen**</span></span>](texture2darray-gathergreen.md)                            | <span data-ttu-id="cd6b5-114">Gibt die grünen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-114">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                        |
| [<span data-ttu-id="cd6b5-115">**Gatherblue**</span><span class="sxs-lookup"><span data-stu-id="cd6b5-115">**GatherBlue**</span></span>](texture2darray-gatherblue.md)                              | <span data-ttu-id="cd6b5-116">Gibt die blauen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-116">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                         |
| [<span data-ttu-id="cd6b5-117">**Gatheralpha**</span><span class="sxs-lookup"><span data-stu-id="cd6b5-117">**GatherAlpha**</span></span>](texture2darray-gatheralpha.md)                            | <span data-ttu-id="cd6b5-118">Gibt die Alpha Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-118">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                        |
| [<span data-ttu-id="cd6b5-119">**Gathercmp**</span><span class="sxs-lookup"><span data-stu-id="cd6b5-119">**GatherCmp**</span></span>](texture2darray-gathercmp.md)                                | <span data-ttu-id="cd6b5-120">Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird der Vergleich mit einem Vergleichswert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-120">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>                      |
| [<span data-ttu-id="cd6b5-121">**Gathercmpred**</span><span class="sxs-lookup"><span data-stu-id="cd6b5-121">**GatherCmpRed**</span></span>](texture2darray-gathercmpred.md)                          | <span data-ttu-id="cd6b5-122">Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der roten Komponente mit einem Vergleichswert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-122">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>   |
| [<span data-ttu-id="cd6b5-123">**Gathercmpgreen**</span><span class="sxs-lookup"><span data-stu-id="cd6b5-123">**GatherCmpGreen**</span></span>](texture2darray-gathercmpgreen.md)                      | <span data-ttu-id="cd6b5-124">Für vier textexwerte, die in einem bilinearen Filterungs Vorgang verwendet werden, wird ein Vergleich der grünen Komponente mit einem Vergleichswert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-124">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span> |
| [<span data-ttu-id="cd6b5-125">**Gathercmpblue**</span><span class="sxs-lookup"><span data-stu-id="cd6b5-125">**GatherCmpBlue**</span></span>](texture2darray-gathercmpblue.md)                        | <span data-ttu-id="cd6b5-126">Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der blauen Komponente mit einem Vergleichswert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-126">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span>  |
| [<span data-ttu-id="cd6b5-127">**Gathercmpalpha**</span><span class="sxs-lookup"><span data-stu-id="cd6b5-127">**GatherCmpAlpha**</span></span>](texture2darray-gathercmpalpha.md)                      | <span data-ttu-id="cd6b5-128">Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der Alpha Komponente mit einem Vergleichswert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-128">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span> |
| [<span data-ttu-id="cd6b5-129">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="cd6b5-129">**GetDimensions**</span></span>](sm5-object-texture2darray-getdimensions.md)             | <span data-ttu-id="cd6b5-130">Ruft die Ressourcen Dimensionen ab.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-130">Gets the resource dimensions.</span></span>                                                                                                                       |
| [<span data-ttu-id="cd6b5-131">**Laden**</span><span class="sxs-lookup"><span data-stu-id="cd6b5-131">**Load**</span></span>](texture2darray-load.md)                                          | <span data-ttu-id="cd6b5-132">Liest Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-132">Reads texture data.</span></span>                                                                                                                                 |
| <span data-ttu-id="cd6b5-133">[**MIPS. KOM\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="cd6b5-133">[**mips.Operator\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md)</span></span> | <span data-ttu-id="cd6b5-134">Ruft eine schreibgeschützte Ressourcen Variable ab.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-134">Gets a read-only resource variable.</span></span>                                                                                                                 |
| <span data-ttu-id="cd6b5-135">[**KOM\[\]**](sm5-object-texture2darray-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="cd6b5-135">[**Operator\[\]**](sm5-object-texture2darray-operatorindex.md)</span></span>              | <span data-ttu-id="cd6b5-136">Ruft eine schreibgeschützte Ressourcen Variable ab.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-136">Gets a read-only resource variable.</span></span>                                                                                                                 |
| [<span data-ttu-id="cd6b5-137">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="cd6b5-137">**Sample**</span></span>](texture2darray-sample.md)                                      | <span data-ttu-id="cd6b5-138">Stichproben eine Textur.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-138">Samples a texture.</span></span>                                                                                                                                  |
| [<span data-ttu-id="cd6b5-139">**Samplebias**</span><span class="sxs-lookup"><span data-stu-id="cd6b5-139">**SampleBias**</span></span>](texture2darray-samplebias.md)                              | <span data-ttu-id="cd6b5-140">Gibt eine Textur aus, nachdem der Bias-Wert auf die MipMap-Ebene angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-140">Samples a texture, after applying the bias value to the mipmap level.</span></span>                                                                               |
| [<span data-ttu-id="cd6b5-141">**Samplecmp**</span><span class="sxs-lookup"><span data-stu-id="cd6b5-141">**SampleCmp**</span></span>](texture2darray-samplecmp.md)                                | <span data-ttu-id="cd6b5-142">Abtastungen einer Textur mithilfe eines Vergleichs Werts zum ablehnen von Beispielen.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-142">Samples a texture, using a comparison value to reject samples.</span></span>                                                                                      |
| [<span data-ttu-id="cd6b5-143">**Samplecmplevelzero**</span><span class="sxs-lookup"><span data-stu-id="cd6b5-143">**SampleCmpLevelZero**</span></span>](texture2darray-samplecmplevelzero.md)              | <span data-ttu-id="cd6b5-144">Stichproben eine Textur (nur MipMap-Ebene 0) unter Verwendung eines Vergleichs Werts zum ablehnen von Beispielen.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-144">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>                                                                |
| [<span data-ttu-id="cd6b5-145">**Samplegrad**</span><span class="sxs-lookup"><span data-stu-id="cd6b5-145">**SampleGrad**</span></span>](texture2darray-samplegrad.md)                              | <span data-ttu-id="cd6b5-146">Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, in der der Beispiel Speicherort berechnet wird</span><span class="sxs-lookup"><span data-stu-id="cd6b5-146">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span>                                                          |
| [<span data-ttu-id="cd6b5-147">**Samplelevel**</span><span class="sxs-lookup"><span data-stu-id="cd6b5-147">**SampleLevel**</span></span>](texture2darray-samplelevel.md)                            | <span data-ttu-id="cd6b5-148">Prüft eine Textur auf der angegebenen MipMap-Ebene.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-148">Samples a texture on the specified mipmap level.</span></span>                                                                                                    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="cd6b5-149">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="cd6b5-149">Minimum Shader Model</span></span>

<span data-ttu-id="cd6b5-150">Dieses Objekt wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-150">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="cd6b5-151">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="cd6b5-151">Shader Model</span></span>                                                                | <span data-ttu-id="cd6b5-152">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="cd6b5-152">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="cd6b5-153">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="cd6b5-153">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="cd6b5-154">ja</span><span class="sxs-lookup"><span data-stu-id="cd6b5-154">yes</span></span>       |



 

<span data-ttu-id="cd6b5-155">Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="cd6b5-155">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="cd6b5-156">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="cd6b5-156">Vertex</span></span> | <span data-ttu-id="cd6b5-157">Hülle</span><span class="sxs-lookup"><span data-stu-id="cd6b5-157">Hull</span></span> | <span data-ttu-id="cd6b5-158">Domain</span><span class="sxs-lookup"><span data-stu-id="cd6b5-158">Domain</span></span> | <span data-ttu-id="cd6b5-159">Geometrie</span><span class="sxs-lookup"><span data-stu-id="cd6b5-159">Geometry</span></span> | <span data-ttu-id="cd6b5-160">Pixel</span><span class="sxs-lookup"><span data-stu-id="cd6b5-160">Pixel</span></span> | <span data-ttu-id="cd6b5-161">Compute</span><span class="sxs-lookup"><span data-stu-id="cd6b5-161">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="cd6b5-162">x</span><span class="sxs-lookup"><span data-stu-id="cd6b5-162">x</span></span>      | <span data-ttu-id="cd6b5-163">x</span><span class="sxs-lookup"><span data-stu-id="cd6b5-163">x</span></span>    | <span data-ttu-id="cd6b5-164">x</span><span class="sxs-lookup"><span data-stu-id="cd6b5-164">x</span></span>      | <span data-ttu-id="cd6b5-165">x</span><span class="sxs-lookup"><span data-stu-id="cd6b5-165">x</span></span>        | <span data-ttu-id="cd6b5-166">x</span><span class="sxs-lookup"><span data-stu-id="cd6b5-166">x</span></span>     | <span data-ttu-id="cd6b5-167">x</span><span class="sxs-lookup"><span data-stu-id="cd6b5-167">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="cd6b5-168">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cd6b5-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd6b5-169">Shader Model 5-Objekte</span><span class="sxs-lookup"><span data-stu-id="cd6b5-169">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




