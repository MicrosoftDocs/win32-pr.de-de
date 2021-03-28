---
title: Texture1DArray
description: Texture1DArray
ms.assetid: 3d793423-3d79-48c1-aa78-f9d93b79e0b6
keywords:
- Texture1DArray HLSL
topic_type:
- apiref
api_name:
- Texture1DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 39cea5692e29ead74ba20c4a35ab8d43a1b19d42
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038100"
---
# <a name="texture1darray"></a><span data-ttu-id="5d688-104">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="5d688-104">Texture1DArray</span></span>

<span data-ttu-id="5d688-105">Texture1DArray Type ([wie er in Shader Model 4 vorhanden](dx-graphics-hlsl-to-type.md)ist) plus Ressourcenvariablen.</span><span class="sxs-lookup"><span data-stu-id="5d688-105">Texture1DArray type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="5d688-106">Dieses Textur Objekt unterstützt zusätzlich zu den Methoden in Shader Model 4 die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="5d688-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="5d688-107">Methode</span><span class="sxs-lookup"><span data-stu-id="5d688-107">Method</span></span>                                                                       | <span data-ttu-id="5d688-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d688-108">Description</span></span>                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d688-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="5d688-109">**GetDimensions**</span></span>](sm5-object-texture1darray-getdimensions.md)             | <span data-ttu-id="5d688-110">Ruft die Ressourcen Dimensionen ab.</span><span class="sxs-lookup"><span data-stu-id="5d688-110">Gets the resource dimensions.</span></span>                                                              |
| [<span data-ttu-id="5d688-111">**Laden**</span><span class="sxs-lookup"><span data-stu-id="5d688-111">**Load**</span></span>](texture1darray-load.md)                                          | <span data-ttu-id="5d688-112">Liest Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="5d688-112">Reads texture data.</span></span>                                                                        |
| <span data-ttu-id="5d688-113">[**MIPS. KOM\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="5d688-113">[**mips.Operator\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md)</span></span> | <span data-ttu-id="5d688-114">Ruft eine schreibgeschützte Ressourcen Variable ab.</span><span class="sxs-lookup"><span data-stu-id="5d688-114">Gets a read-only resource variable.</span></span>                                                        |
| <span data-ttu-id="5d688-115">[**KOM\[\]**](sm5-object-texture1darray-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="5d688-115">[**Operator\[\]**](sm5-object-texture1darray-operatorindex.md)</span></span>              | <span data-ttu-id="5d688-116">Ruft eine schreibgeschützte Ressourcen Variable ab.</span><span class="sxs-lookup"><span data-stu-id="5d688-116">Gets a read-only resource variable.</span></span>                                                        |
| [<span data-ttu-id="5d688-117">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="5d688-117">**Sample**</span></span>](texture1darray-sample.md)                                      | <span data-ttu-id="5d688-118">Stichproben eine Textur.</span><span class="sxs-lookup"><span data-stu-id="5d688-118">Samples a texture.</span></span>                                                                         |
| [<span data-ttu-id="5d688-119">**Samplebias**</span><span class="sxs-lookup"><span data-stu-id="5d688-119">**SampleBias**</span></span>](texture1darray-samplebias.md)                              | <span data-ttu-id="5d688-120">Gibt eine Textur aus, nachdem der Bias-Wert auf die MipMap-Ebene angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="5d688-120">Samples a texture, after applying the bias value to the mipmap level.</span></span>                      |
| [<span data-ttu-id="5d688-121">**Samplecmp**</span><span class="sxs-lookup"><span data-stu-id="5d688-121">**SampleCmp**</span></span>](texture1darray-samplecmp.md)                                | <span data-ttu-id="5d688-122">Abtastungen einer Textur mithilfe eines Vergleichs Werts zum ablehnen von Beispielen.</span><span class="sxs-lookup"><span data-stu-id="5d688-122">Samples a texture, using a comparison value to reject samples.</span></span>                             |
| [<span data-ttu-id="5d688-123">**Samplecmplevelzero**</span><span class="sxs-lookup"><span data-stu-id="5d688-123">**SampleCmpLevelZero**</span></span>](texture1darray-samplecmplevelzero.md)              | <span data-ttu-id="5d688-124">Stichproben eine Textur (nur MipMap-Ebene 0) unter Verwendung eines Vergleichs Werts zum ablehnen von Beispielen.</span><span class="sxs-lookup"><span data-stu-id="5d688-124">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>       |
| [<span data-ttu-id="5d688-125">**Samplegrad**</span><span class="sxs-lookup"><span data-stu-id="5d688-125">**SampleGrad**</span></span>](texture1darray-samplegrad.md)                              | <span data-ttu-id="5d688-126">Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, in der der Beispiel Speicherort berechnet wird</span><span class="sxs-lookup"><span data-stu-id="5d688-126">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span> |
| [<span data-ttu-id="5d688-127">**Samplelevel**</span><span class="sxs-lookup"><span data-stu-id="5d688-127">**SampleLevel**</span></span>](texture1darray-samplelevel.md)                            | <span data-ttu-id="5d688-128">Prüft eine Textur auf der angegebenen MipMap-Ebene.</span><span class="sxs-lookup"><span data-stu-id="5d688-128">Samples a texture on the specified mipmap level.</span></span>                                           |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5d688-129">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="5d688-129">Minimum Shader Model</span></span>

<span data-ttu-id="5d688-130">Dieses Objekt wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5d688-130">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="5d688-131">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="5d688-131">Shader Model</span></span>                                                                | <span data-ttu-id="5d688-132">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="5d688-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="5d688-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="5d688-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="5d688-134">ja</span><span class="sxs-lookup"><span data-stu-id="5d688-134">yes</span></span>       |



 

<span data-ttu-id="5d688-135">Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="5d688-135">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="5d688-136">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="5d688-136">Vertex</span></span> | <span data-ttu-id="5d688-137">Hülle</span><span class="sxs-lookup"><span data-stu-id="5d688-137">Hull</span></span> | <span data-ttu-id="5d688-138">Domain</span><span class="sxs-lookup"><span data-stu-id="5d688-138">Domain</span></span> | <span data-ttu-id="5d688-139">Geometrie</span><span class="sxs-lookup"><span data-stu-id="5d688-139">Geometry</span></span> | <span data-ttu-id="5d688-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="5d688-140">Pixel</span></span> | <span data-ttu-id="5d688-141">Compute</span><span class="sxs-lookup"><span data-stu-id="5d688-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5d688-142">x</span><span class="sxs-lookup"><span data-stu-id="5d688-142">x</span></span>      | <span data-ttu-id="5d688-143">x</span><span class="sxs-lookup"><span data-stu-id="5d688-143">x</span></span>    | <span data-ttu-id="5d688-144">x</span><span class="sxs-lookup"><span data-stu-id="5d688-144">x</span></span>      | <span data-ttu-id="5d688-145">x</span><span class="sxs-lookup"><span data-stu-id="5d688-145">x</span></span>        | <span data-ttu-id="5d688-146">x</span><span class="sxs-lookup"><span data-stu-id="5d688-146">x</span></span>     | <span data-ttu-id="5d688-147">x</span><span class="sxs-lookup"><span data-stu-id="5d688-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5d688-148">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5d688-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d688-149">Shader Model 5-Objekte</span><span class="sxs-lookup"><span data-stu-id="5d688-149">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




