---
title: Texture3D
description: Texture3D
ms.assetid: a3640aac-b503-4716-8bc6-105e96bea03c
keywords:
- Texture3D HLSL
topic_type:
- apiref
api_name:
- Texture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50b12f2184f6eca0fd7a68feb3e96d8d6fc65a61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037870"
---
# <a name="texture3d"></a><span data-ttu-id="b6353-104">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b6353-104">Texture3D</span></span>

<span data-ttu-id="b6353-105">Texture3D Type ([wie er in Shader Model 4 vorhanden](dx-graphics-hlsl-to-type.md)ist) plus Ressourcenvariablen.</span><span class="sxs-lookup"><span data-stu-id="b6353-105">Texture3D type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="b6353-106">Dieses Textur Objekt unterstützt zusätzlich zu den Methoden in Shader Model 4 die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="b6353-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="b6353-107">Methode</span><span class="sxs-lookup"><span data-stu-id="b6353-107">Method</span></span>                                                                  | <span data-ttu-id="b6353-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b6353-108">Description</span></span>                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6353-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="b6353-109">**GetDimensions**</span></span>](sm5-object-texture3d-getdimensions.md)             | <span data-ttu-id="b6353-110">Ruft die Ressourcen Dimensionen ab.</span><span class="sxs-lookup"><span data-stu-id="b6353-110">Gets the resource dimensions.</span></span>                                                              |
| [<span data-ttu-id="b6353-111">**Laden**</span><span class="sxs-lookup"><span data-stu-id="b6353-111">**Load**</span></span>](texture3d-load.md)                                          | <span data-ttu-id="b6353-112">Liest Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="b6353-112">Reads texture data.</span></span>                                                                        |
| <span data-ttu-id="b6353-113">[**MIPS. KOM\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="b6353-113">[**mips.Operator\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md)</span></span> | <span data-ttu-id="b6353-114">Ruft eine schreibgeschützte Ressourcen Variable ab.</span><span class="sxs-lookup"><span data-stu-id="b6353-114">Gets a read-only resource variable.</span></span>                                                        |
| <span data-ttu-id="b6353-115">[**KOM\[\]**](sm5-object-texture3d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="b6353-115">[**Operator\[\]**](sm5-object-texture3d-operatorindex.md)</span></span>              | <span data-ttu-id="b6353-116">Ruft eine schreibgeschützte Ressourcen Variable ab.</span><span class="sxs-lookup"><span data-stu-id="b6353-116">Gets a read-only resource variable.</span></span>                                                        |
| [<span data-ttu-id="b6353-117">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="b6353-117">**Sample**</span></span>](texture3d-sample.md)                                      | <span data-ttu-id="b6353-118">Stichproben eine Textur.</span><span class="sxs-lookup"><span data-stu-id="b6353-118">Samples a texture.</span></span>                                                                         |
| [<span data-ttu-id="b6353-119">**Samplebias**</span><span class="sxs-lookup"><span data-stu-id="b6353-119">**SampleBias**</span></span>](texture3d-samplebias.md)                              | <span data-ttu-id="b6353-120">Gibt eine Textur aus, nachdem der Bias-Wert auf die MipMap-Ebene angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b6353-120">Samples a texture, after applying the bias value to the mipmap level.</span></span>                      |
| [<span data-ttu-id="b6353-121">**Samplegrad**</span><span class="sxs-lookup"><span data-stu-id="b6353-121">**SampleGrad**</span></span>](texture3d-samplegrad.md)                              | <span data-ttu-id="b6353-122">Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, in der der Beispiel Speicherort berechnet wird</span><span class="sxs-lookup"><span data-stu-id="b6353-122">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span> |
| [<span data-ttu-id="b6353-123">**Samplelevel**</span><span class="sxs-lookup"><span data-stu-id="b6353-123">**SampleLevel**</span></span>](texture3d-samplelevel.md)                            | <span data-ttu-id="b6353-124">Prüft eine Textur auf der angegebenen MipMap-Ebene.</span><span class="sxs-lookup"><span data-stu-id="b6353-124">Samples a texture on the specified mipmap level.</span></span>                                           |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b6353-125">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="b6353-125">Minimum Shader Model</span></span>

<span data-ttu-id="b6353-126">Dieses Objekt wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b6353-126">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="b6353-127">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="b6353-127">Shader Model</span></span>                                                                | <span data-ttu-id="b6353-128">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="b6353-128">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="b6353-129">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="b6353-129">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="b6353-130">ja</span><span class="sxs-lookup"><span data-stu-id="b6353-130">yes</span></span>       |



 

<span data-ttu-id="b6353-131">Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="b6353-131">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b6353-132">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="b6353-132">Vertex</span></span> | <span data-ttu-id="b6353-133">Hülle</span><span class="sxs-lookup"><span data-stu-id="b6353-133">Hull</span></span> | <span data-ttu-id="b6353-134">Domain</span><span class="sxs-lookup"><span data-stu-id="b6353-134">Domain</span></span> | <span data-ttu-id="b6353-135">Geometrie</span><span class="sxs-lookup"><span data-stu-id="b6353-135">Geometry</span></span> | <span data-ttu-id="b6353-136">Pixel</span><span class="sxs-lookup"><span data-stu-id="b6353-136">Pixel</span></span> | <span data-ttu-id="b6353-137">Compute</span><span class="sxs-lookup"><span data-stu-id="b6353-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b6353-138">x</span><span class="sxs-lookup"><span data-stu-id="b6353-138">x</span></span>      | <span data-ttu-id="b6353-139">x</span><span class="sxs-lookup"><span data-stu-id="b6353-139">x</span></span>    | <span data-ttu-id="b6353-140">x</span><span class="sxs-lookup"><span data-stu-id="b6353-140">x</span></span>      | <span data-ttu-id="b6353-141">x</span><span class="sxs-lookup"><span data-stu-id="b6353-141">x</span></span>        | <span data-ttu-id="b6353-142">x</span><span class="sxs-lookup"><span data-stu-id="b6353-142">x</span></span>     | <span data-ttu-id="b6353-143">x</span><span class="sxs-lookup"><span data-stu-id="b6353-143">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b6353-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b6353-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6353-145">Shader Model 5-Objekte</span><span class="sxs-lookup"><span data-stu-id="b6353-145">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




