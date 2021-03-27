---
title: TextureCubeArray-Objekt
description: Texturecubearray-Typ (wie in Shader-Modell 4 vorhanden) und Ressourcenvariablen. Dieses Textur Objekt unterstützt diese Methoden zusätzlich zu den Methoden in Shader Model 4.
ms.assetid: 62AAF0F9-D552-4FFA-B681-749D6DC205BD
keywords:
- Texturecubearray-Objekt HLSL
- Texturecubearray-Objekt HLSL, beschrieben
topic_type:
- apiref
api_name:
- TextureCubeArray
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e559214626fadbc08b8e9cd4d5568358f130779c
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "104995246"
---
# <a name="texturecubearray-object"></a><span data-ttu-id="e9ebc-106">TextureCubeArray-Objekt</span><span class="sxs-lookup"><span data-stu-id="e9ebc-106">TextureCubeArray object</span></span>

<span data-ttu-id="e9ebc-107">**Texturecubearray** -Typ ([wie in Shader-Modell 4 vorhanden](dx-graphics-hlsl-to-type.md)) und Ressourcenvariablen.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-107">**TextureCubeArray** type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="e9ebc-108">Dieses Textur Objekt unterstützt diese Methoden zusätzlich zu den Methoden in Shader Model 4.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-108">This texture object supports these methods in addition to the methods in Shader Model 4.</span></span>

-   [<span data-ttu-id="e9ebc-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="e9ebc-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e9ebc-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="e9ebc-110">Methods</span></span>

<span data-ttu-id="e9ebc-111">Das **texturecubearray** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-111">The **TextureCubeArray** object has these methods.</span></span>



| <span data-ttu-id="e9ebc-112">Methode</span><span class="sxs-lookup"><span data-stu-id="e9ebc-112">Method</span></span>                                                           | <span data-ttu-id="e9ebc-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9ebc-113">Description</span></span>                                                                                                                                              |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9ebc-114">**Informieren**</span><span class="sxs-lookup"><span data-stu-id="e9ebc-114">**Gather**</span></span>](texturecubearray-gather.md)                         | <span data-ttu-id="e9ebc-115">Gibt die vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-115">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                                                |
| [<span data-ttu-id="e9ebc-116">**Gatheralpha**</span><span class="sxs-lookup"><span data-stu-id="e9ebc-116">**GatherAlpha**</span></span>](texturecubearray-gatheralpha.md)               | <span data-ttu-id="e9ebc-117">Gibt die Alpha Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-117">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="e9ebc-118">**Gatherblue**</span><span class="sxs-lookup"><span data-stu-id="e9ebc-118">**GatherBlue**</span></span>](texturecubearray-gatherblue.md)                 | <span data-ttu-id="e9ebc-119">Gibt die blauen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-119">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                         |
| [<span data-ttu-id="e9ebc-120">**Gathercmp**</span><span class="sxs-lookup"><span data-stu-id="e9ebc-120">**GatherCmp**</span></span>](texturecubearray-gathercmp.md)                   | <span data-ttu-id="e9ebc-121">Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird der Vergleich mit einem Vergleichswert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-121">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span><br/>                      |
| [<span data-ttu-id="e9ebc-122">**Gathercmpalpha**</span><span class="sxs-lookup"><span data-stu-id="e9ebc-122">**GatherCmpAlpha**</span></span>](texturecubearray-gathercmpalpha.md)         | <span data-ttu-id="e9ebc-123">Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der Alpha Komponente mit einem Vergleichswert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-123">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span><br/> |
| [<span data-ttu-id="e9ebc-124">**Gathercmpblue**</span><span class="sxs-lookup"><span data-stu-id="e9ebc-124">**GatherCmpBlue**</span></span>](texturecubearray-gathercmpblue.md)           | <span data-ttu-id="e9ebc-125">Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der blauen Komponente mit einem Vergleichswert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-125">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span><br/>  |
| [<span data-ttu-id="e9ebc-126">**Gathercmpgreen**</span><span class="sxs-lookup"><span data-stu-id="e9ebc-126">**GatherCmpGreen**</span></span>](texturecubearray-gathercmpgreen.md)         | <span data-ttu-id="e9ebc-127">Für vier textexwerte, die in einem bilinearen Filterungs Vorgang verwendet werden, wird ein Vergleich der grünen Komponente mit einem Vergleichswert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-127">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span><br/> |
| [<span data-ttu-id="e9ebc-128">**Gathercmpred**</span><span class="sxs-lookup"><span data-stu-id="e9ebc-128">**GatherCmpRed**</span></span>](texturecubearray-gathercmpred.md)             | <span data-ttu-id="e9ebc-129">Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der roten Komponente mit einem Vergleichswert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-129">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span><br/>   |
| [<span data-ttu-id="e9ebc-130">**Gathergrün**</span><span class="sxs-lookup"><span data-stu-id="e9ebc-130">**GatherGreen**</span></span>](texturecubearray-gathergreen.md)               | <span data-ttu-id="e9ebc-131">Gibt die grünen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-131">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="e9ebc-132">**Gatherred**</span><span class="sxs-lookup"><span data-stu-id="e9ebc-132">**GatherRed**</span></span>](texturecubearray-gatherred.md)                   | <span data-ttu-id="e9ebc-133">Gibt die roten Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-133">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                          |
| [<span data-ttu-id="e9ebc-134">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="e9ebc-134">**Sample**</span></span>](texturecubearray-sample.md)                         | <span data-ttu-id="e9ebc-135">Stichproben eine Textur.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-135">Samples a texture.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="e9ebc-136">**Samplebias**</span><span class="sxs-lookup"><span data-stu-id="e9ebc-136">**SampleBias**</span></span>](texturecubearray-samplebias.md)                 | <span data-ttu-id="e9ebc-137">Gibt eine Textur aus, nachdem der Bias-Wert auf die MipMap-Ebene angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-137">Samples a texture, after applying the bias value to the mipmap level.</span></span><br/>                                                                               |
| [<span data-ttu-id="e9ebc-138">**Samplecmp**</span><span class="sxs-lookup"><span data-stu-id="e9ebc-138">**SampleCmp**</span></span>](texturecubearray-samplecmp.md)                   | <span data-ttu-id="e9ebc-139">Abtastungen einer Textur mithilfe eines Vergleichs Werts zum ablehnen von Beispielen.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-139">Samples a texture, using a comparison value to reject samples.</span></span><br/>                                                                                      |
| [<span data-ttu-id="e9ebc-140">**Samplecmplevelzero**</span><span class="sxs-lookup"><span data-stu-id="e9ebc-140">**SampleCmpLevelZero**</span></span>](texturecubearray-samplecmplevelzero.md) | <span data-ttu-id="e9ebc-141">Stichproben eine Textur (nur MipMap-Ebene 0) unter Verwendung eines Vergleichs Werts zum ablehnen von Beispielen.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-141">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span><br/>                                                                |
| [<span data-ttu-id="e9ebc-142">**Samplegrad**</span><span class="sxs-lookup"><span data-stu-id="e9ebc-142">**SampleGrad**</span></span>](texturecubearray-samplegrad.md)                 | <span data-ttu-id="e9ebc-143">Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, in der der Beispiel Speicherort berechnet wird</span><span class="sxs-lookup"><span data-stu-id="e9ebc-143">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span><br/>                                                          |
| [<span data-ttu-id="e9ebc-144">**Samplelevel**</span><span class="sxs-lookup"><span data-stu-id="e9ebc-144">**SampleLevel**</span></span>](texturecubearray-samplelevel.md)               | <span data-ttu-id="e9ebc-145">Prüft eine Textur auf der angegebenen MipMap-Ebene.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-145">Samples a texture on the specified mipmap level.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="e9ebc-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9ebc-146">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="e9ebc-147">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="e9ebc-147">Minimum Shader Model</span></span>

<span data-ttu-id="e9ebc-148">Dieses Objekt wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e9ebc-148">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="e9ebc-149">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="e9ebc-149">Shader Model</span></span>                                                                | <span data-ttu-id="e9ebc-150">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="e9ebc-150">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="e9ebc-151">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="e9ebc-151">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="e9ebc-152">ja</span><span class="sxs-lookup"><span data-stu-id="e9ebc-152">yes</span></span>       |



 

<span data-ttu-id="e9ebc-153">Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e9ebc-153">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e9ebc-154">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="e9ebc-154">Vertex</span></span> | <span data-ttu-id="e9ebc-155">Hülle</span><span class="sxs-lookup"><span data-stu-id="e9ebc-155">Hull</span></span> | <span data-ttu-id="e9ebc-156">Domain</span><span class="sxs-lookup"><span data-stu-id="e9ebc-156">Domain</span></span> | <span data-ttu-id="e9ebc-157">Geometrie</span><span class="sxs-lookup"><span data-stu-id="e9ebc-157">Geometry</span></span> | <span data-ttu-id="e9ebc-158">Pixel</span><span class="sxs-lookup"><span data-stu-id="e9ebc-158">Pixel</span></span> | <span data-ttu-id="e9ebc-159">Compute</span><span class="sxs-lookup"><span data-stu-id="e9ebc-159">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e9ebc-160">x</span><span class="sxs-lookup"><span data-stu-id="e9ebc-160">x</span></span>      | <span data-ttu-id="e9ebc-161">x</span><span class="sxs-lookup"><span data-stu-id="e9ebc-161">x</span></span>    | <span data-ttu-id="e9ebc-162">x</span><span class="sxs-lookup"><span data-stu-id="e9ebc-162">x</span></span>      | <span data-ttu-id="e9ebc-163">x</span><span class="sxs-lookup"><span data-stu-id="e9ebc-163">x</span></span>        | <span data-ttu-id="e9ebc-164">x</span><span class="sxs-lookup"><span data-stu-id="e9ebc-164">x</span></span>     | <span data-ttu-id="e9ebc-165">x</span><span class="sxs-lookup"><span data-stu-id="e9ebc-165">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e9ebc-166">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e9ebc-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9ebc-167">Shader Model 5-Objekte</span><span class="sxs-lookup"><span data-stu-id="e9ebc-167">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





