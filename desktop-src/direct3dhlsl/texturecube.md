---
title: TextureCube-Objekt
description: Texturecube-Typ (wie er in Shader-Modell 4 vorhanden ist) plus Ressourcenvariablen. Dieses Textur Objekt unterstützt diese Methoden zusätzlich zu den Methoden in Shader Model 4.
ms.assetid: BC96D7BB-992E-48CC-A774-E211E1BB1720
keywords:
- Texturecube-Objekt HLSL
- Texturecube-Objekt HLSL, beschrieben
topic_type:
- apiref
api_name:
- TextureCube
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 939c79895ae1c24665fc70d6b6cf2ced19854e2b
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "104132137"
---
# <a name="texturecube-object"></a><span data-ttu-id="250b4-106">TextureCube-Objekt</span><span class="sxs-lookup"><span data-stu-id="250b4-106">TextureCube object</span></span>

<span data-ttu-id="250b4-107">**Texturecube** -Typ ([wie er in Shader-Modell 4 vorhanden](dx-graphics-hlsl-to-type.md)ist) plus Ressourcenvariablen.</span><span class="sxs-lookup"><span data-stu-id="250b4-107">**TextureCube** type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="250b4-108">Dieses Textur Objekt unterstützt diese Methoden zusätzlich zu den Methoden in Shader Model 4.</span><span class="sxs-lookup"><span data-stu-id="250b4-108">This texture object supports these methods in addition to the methods in Shader Model 4.</span></span>

-   [<span data-ttu-id="250b4-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="250b4-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="250b4-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="250b4-110">Methods</span></span>

<span data-ttu-id="250b4-111">Das **texturecube** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="250b4-111">The **TextureCube** object has these methods.</span></span>



| <span data-ttu-id="250b4-112">Methode</span><span class="sxs-lookup"><span data-stu-id="250b4-112">Method</span></span>                                                      | <span data-ttu-id="250b4-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="250b4-113">Description</span></span>                                                                                                                                             |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="250b4-114">**Informieren**</span><span class="sxs-lookup"><span data-stu-id="250b4-114">**Gather**</span></span>](texturecube-gather.md)                         | <span data-ttu-id="250b4-115">Gibt die vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="250b4-115">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                                                |
| [<span data-ttu-id="250b4-116">**Gatheralpha**</span><span class="sxs-lookup"><span data-stu-id="250b4-116">**GatherAlpha**</span></span>](texturecube-gatheralpha.md)               | <span data-ttu-id="250b4-117">Gibt die Alpha Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="250b4-117">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="250b4-118">**Gatherblue**</span><span class="sxs-lookup"><span data-stu-id="250b4-118">**GatherBlue**</span></span>](texturecube-gatherblue.md)                 | <span data-ttu-id="250b4-119">Gibt die blauen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="250b4-119">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                         |
| [<span data-ttu-id="250b4-120">**Gathercmp**</span><span class="sxs-lookup"><span data-stu-id="250b4-120">**GatherCmp**</span></span>](texturecube-gathercmp.md)                   | <span data-ttu-id="250b4-121">Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird der Vergleich mit einem Vergleichswert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="250b4-121">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span><br/>                      |
| [<span data-ttu-id="250b4-122">**Gathercmpalpha**</span><span class="sxs-lookup"><span data-stu-id="250b4-122">**GatherCmpAlpha**</span></span>](texturecube-gathercmpalpha.md)         | <span data-ttu-id="250b4-123">Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der Alpha Komponente mit einem Vergleichswert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="250b4-123">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span><br/> |
| [<span data-ttu-id="250b4-124">**Gathercmpblue**</span><span class="sxs-lookup"><span data-stu-id="250b4-124">**GatherCmpBlue**</span></span>](texturecube-gathercmpblue.md)           | <span data-ttu-id="250b4-125">Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der blauen Komponente mit einem Vergleichswert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="250b4-125">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span><br/>  |
| [<span data-ttu-id="250b4-126">**Gathercmpgreen**</span><span class="sxs-lookup"><span data-stu-id="250b4-126">**GatherCmpGreen**</span></span>](texturecube-gathercmpgreen.md)         | <span data-ttu-id="250b4-127">Für vier textexwerte, die in einem bilinearen Filterungs Vorgang verwendet werden, wird ein Vergleich der grünen Komponente mit einem Vergleichswert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="250b4-127">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span><br/> |
| [<span data-ttu-id="250b4-128">**Gathercmpred**</span><span class="sxs-lookup"><span data-stu-id="250b4-128">**GatherCmpRed**</span></span>](texturecube-gathercmpred.md)             | <span data-ttu-id="250b4-129">Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der roten Komponente mit einem Vergleichswert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="250b4-129">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span><br/>   |
| [<span data-ttu-id="250b4-130">**Gathergrün**</span><span class="sxs-lookup"><span data-stu-id="250b4-130">**GatherGreen**</span></span>](texturecube-gathergreen.md)               | <span data-ttu-id="250b4-131">Gibt die grünen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="250b4-131">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="250b4-132">**Gatherred**</span><span class="sxs-lookup"><span data-stu-id="250b4-132">**GatherRed**</span></span>](texturecube-gatherred.md)                   | <span data-ttu-id="250b4-133">Gibt die roten Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="250b4-133">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                          |
| [<span data-ttu-id="250b4-134">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="250b4-134">**Sample**</span></span>](texturecube-sample.md)                         | <span data-ttu-id="250b4-135">Stichproben eine Textur.</span><span class="sxs-lookup"><span data-stu-id="250b4-135">Samples a texture.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="250b4-136">**Samplebias**</span><span class="sxs-lookup"><span data-stu-id="250b4-136">**SampleBias**</span></span>](texturecube-samplebias.md)                 | <span data-ttu-id="250b4-137">Gibt eine Textur aus, nachdem der Bias-Wert auf die MipMap-Ebene angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="250b4-137">Samples a texture, after applying the bias value to the mipmap level.</span></span><br/>                                                                               |
| [<span data-ttu-id="250b4-138">**Samplecmp**</span><span class="sxs-lookup"><span data-stu-id="250b4-138">**SampleCmp**</span></span>](texturecube-samplecmp.md)                   | <span data-ttu-id="250b4-139">Abtastungen einer Textur mithilfe eines Vergleichs Werts zum ablehnen von Beispielen.</span><span class="sxs-lookup"><span data-stu-id="250b4-139">Samples a texture, using a comparison value to reject samples.</span></span><br/>                                                                                      |
| [<span data-ttu-id="250b4-140">**Samplecmplevelzero**</span><span class="sxs-lookup"><span data-stu-id="250b4-140">**SampleCmpLevelZero**</span></span>](texturecube-samplecmplevelzero.md) | <span data-ttu-id="250b4-141">Stichproben eine Textur (nur MipMap-Ebene 0) unter Verwendung eines Vergleichs Werts zum ablehnen von Beispielen.</span><span class="sxs-lookup"><span data-stu-id="250b4-141">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span><br/>                                                                |
| [<span data-ttu-id="250b4-142">**Samplegrad**</span><span class="sxs-lookup"><span data-stu-id="250b4-142">**SampleGrad**</span></span>](texturecube-samplegrad.md)                 | <span data-ttu-id="250b4-143">Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, in der der Beispiel Speicherort berechnet wird</span><span class="sxs-lookup"><span data-stu-id="250b4-143">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span><br/>                                                          |
| [<span data-ttu-id="250b4-144">**Samplelevel**</span><span class="sxs-lookup"><span data-stu-id="250b4-144">**SampleLevel**</span></span>](texturecube-samplelevel.md)               | <span data-ttu-id="250b4-145">Prüft eine Textur auf der angegebenen MipMap-Ebene.</span><span class="sxs-lookup"><span data-stu-id="250b4-145">Samples a texture on the specified mipmap level.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="250b4-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="250b4-146">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="250b4-147">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="250b4-147">Minimum Shader Model</span></span>

<span data-ttu-id="250b4-148">Dieses Objekt wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="250b4-148">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="250b4-149">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="250b4-149">Shader Model</span></span>                                                                | <span data-ttu-id="250b4-150">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="250b4-150">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="250b4-151">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="250b4-151">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="250b4-152">ja</span><span class="sxs-lookup"><span data-stu-id="250b4-152">yes</span></span>       |



 

<span data-ttu-id="250b4-153">Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="250b4-153">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="250b4-154">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="250b4-154">Vertex</span></span> | <span data-ttu-id="250b4-155">Hülle</span><span class="sxs-lookup"><span data-stu-id="250b4-155">Hull</span></span> | <span data-ttu-id="250b4-156">Domain</span><span class="sxs-lookup"><span data-stu-id="250b4-156">Domain</span></span> | <span data-ttu-id="250b4-157">Geometrie</span><span class="sxs-lookup"><span data-stu-id="250b4-157">Geometry</span></span> | <span data-ttu-id="250b4-158">Pixel</span><span class="sxs-lookup"><span data-stu-id="250b4-158">Pixel</span></span> | <span data-ttu-id="250b4-159">Compute</span><span class="sxs-lookup"><span data-stu-id="250b4-159">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="250b4-160">x</span><span class="sxs-lookup"><span data-stu-id="250b4-160">x</span></span>      | <span data-ttu-id="250b4-161">x</span><span class="sxs-lookup"><span data-stu-id="250b4-161">x</span></span>    | <span data-ttu-id="250b4-162">x</span><span class="sxs-lookup"><span data-stu-id="250b4-162">x</span></span>      | <span data-ttu-id="250b4-163">x</span><span class="sxs-lookup"><span data-stu-id="250b4-163">x</span></span>        | <span data-ttu-id="250b4-164">x</span><span class="sxs-lookup"><span data-stu-id="250b4-164">x</span></span>     | <span data-ttu-id="250b4-165">x</span><span class="sxs-lookup"><span data-stu-id="250b4-165">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="250b4-166">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="250b4-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="250b4-167">Shader Model 5-Objekte</span><span class="sxs-lookup"><span data-stu-id="250b4-167">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





