---
title: LOD (SM 4.1-ASM)
description: Gibt die Detailebene (LOD) zurück, die für die Textur Filterung verwendet wird.
ms.assetid: A5931203-8CD7-4FC9-A4A4-CA981F38C7A3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c1ca5a22a735945b76a60c175c665c5cf58fb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719410"
---
# <a name="lod-sm41---asm"></a><span data-ttu-id="d93e0-103">LOD (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="d93e0-103">lod (sm4.1 - asm)</span></span>

<span data-ttu-id="d93e0-104">Gibt die Detailebene (LOD) zurück, die für die Textur Filterung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d93e0-104">Returns the level of detail (LOD) that would be used for texture filtering.</span></span>



| <span data-ttu-id="d93e0-105">LOD dest \[ . mask \] , srcaddress \[ . Swizzle \] , srkresource \[ . Swizzle \] , srcsampler</span><span class="sxs-lookup"><span data-stu-id="d93e0-105">lod dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler</span></span> |
|--------------------------------------------------------------------------------|



 



| <span data-ttu-id="d93e0-106">Element</span><span class="sxs-lookup"><span data-stu-id="d93e0-106">Item</span></span>                                                                                                               | <span data-ttu-id="d93e0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d93e0-107">Description</span></span>                                     |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="d93e0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d93e0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="d93e0-109">\[in \] der Adresse der Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="d93e0-109">\[in\] The address of the results.</span></span><br/>   |
| <span data-ttu-id="d93e0-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*</span><span class="sxs-lookup"><span data-stu-id="d93e0-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="d93e0-111">\[in \] einem Satz von Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="d93e0-111">\[in\] A set of texture coordinates.</span></span><br/> |
| <span data-ttu-id="d93e0-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*</span><span class="sxs-lookup"><span data-stu-id="d93e0-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="d93e0-113">\[in \] einem Textur Register.</span><span class="sxs-lookup"><span data-stu-id="d93e0-113">\[in\] A texture register.</span></span><br/>           |
| <span data-ttu-id="d93e0-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcsampler*</span><span class="sxs-lookup"><span data-stu-id="d93e0-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="d93e0-115">\[in \] einem Samplerregister.</span><span class="sxs-lookup"><span data-stu-id="d93e0-115">\[in\] A sampler register.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="d93e0-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d93e0-116">Remarks</span></span>

<span data-ttu-id="d93e0-117">Dies verhält sich wie die [Beispiel](sample--sm4---asm-.md) Anweisung, aber ein gefiltertes Beispiel wird nicht generiert.</span><span class="sxs-lookup"><span data-stu-id="d93e0-117">This behaves like the [sample](sample--sm4---asm-.md) instruction, but a filtered sample is not generated.</span></span> <span data-ttu-id="d93e0-118">Die-Anweisung berechnet den folgenden Vektor ("clampedlod", "nonclampedlod", "0", 0).</span><span class="sxs-lookup"><span data-stu-id="d93e0-118">The instruction computes the following vector (ClampedLOD, NonClampedLOD, 0, 0).</span></span> <span data-ttu-id="d93e0-119">Nonclampedlod ist ein berechneter Lod-Wert, der eine beliebige Klammer des Samplers oder der Textur ignoriert (d. h., er kann negative Werte zurückgeben). Clampedlod ist ein berechneter Lod-Wert, der von der eigentlichen **Beispiel** Anweisung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d93e0-119">NonClampedLOD is a computed LOD value that ignores any clamping from either the sampler or the texture (ie: it can return negative values.) ClampedLOD is a computed LOD value that would be used by the actual **sample** instruction.</span></span> <span data-ttu-id="d93e0-120">Das Swizzle in *srkresource* ermöglicht es, dass die zurückgegebenen Werte willkürlich durchlaufen werden, bevor Sie in das Ziel geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d93e0-120">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span>

<span data-ttu-id="d93e0-121">Wenn keine Ressource an den angegebenen Slot gebunden ist, wird 0 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d93e0-121">If there is no resource bound to the specified slot, 0 is returned.</span></span>

<span data-ttu-id="d93e0-122">Wenn der Sampler das anisotrope-Filtern verwendet, sollte die Lod dem Bruchteil der MIP-Ebene entsprechend der geringeren Achse des elliptischen Speicherplatzes entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d93e0-122">If the sampler is using anisotropic filtering the LOD should correspond to the fractional mip level based on the smaller axis of the elliptical footprint.</span></span>

<span data-ttu-id="d93e0-123">Dies gilt für die folgenden Textur Typen: Texture1D, Texture2D, Texture3D und texturecube.</span><span class="sxs-lookup"><span data-stu-id="d93e0-123">This is valid for the following texture types: Texture1D, Texture2D, Texture3D and TextureCube.</span></span>

<span data-ttu-id="d93e0-124">Die **Lod** -Anweisung ist nicht definiert, wenn Sie mit einem Sampler verwendet wird, der die MIP-Filterung für Punkte angibt, insbesondere jede d3d10 \_ Filter-Enumeration, die auf dem MIP- \_ Punkt endet</span><span class="sxs-lookup"><span data-stu-id="d93e0-124">The **lod** instruction is not defined when used with a sampler that specifies point mip filtering, specifically, any D3D10\_FILTER enum that ends in MIP\_POINT.</span></span> <span data-ttu-id="d93e0-125">(Ein Beispiel hierfür wäre d3d10 \_ Filter \_ minimale \_ mag- \_ MIP- \_ Punkt.)</span><span class="sxs-lookup"><span data-stu-id="d93e0-125">(An example of this would be D3D10\_FILTER\_MIN\_MAG\_MIP\_POINT.)</span></span>

<span data-ttu-id="d93e0-126">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="d93e0-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d93e0-127">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="d93e0-127">Vertex Shader</span></span> | <span data-ttu-id="d93e0-128">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="d93e0-128">Geometry Shader</span></span> | <span data-ttu-id="d93e0-129">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="d93e0-129">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="d93e0-130">x</span><span class="sxs-lookup"><span data-stu-id="d93e0-130">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d93e0-131">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="d93e0-131">Minimum Shader Model</span></span>

<span data-ttu-id="d93e0-132">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d93e0-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d93e0-133">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="d93e0-133">Shader Model</span></span>                                              | <span data-ttu-id="d93e0-134">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="d93e0-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d93e0-135">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="d93e0-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d93e0-136">ja</span><span class="sxs-lookup"><span data-stu-id="d93e0-136">yes</span></span>       |
| [<span data-ttu-id="d93e0-137">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="d93e0-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d93e0-138">ja</span><span class="sxs-lookup"><span data-stu-id="d93e0-138">yes</span></span>       |
| [<span data-ttu-id="d93e0-139">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="d93e0-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d93e0-140">nein</span><span class="sxs-lookup"><span data-stu-id="d93e0-140">no</span></span>        |
| [<span data-ttu-id="d93e0-141">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d93e0-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d93e0-142">nein</span><span class="sxs-lookup"><span data-stu-id="d93e0-142">no</span></span>        |
| [<span data-ttu-id="d93e0-143">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d93e0-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d93e0-144">nein</span><span class="sxs-lookup"><span data-stu-id="d93e0-144">no</span></span>        |
| [<span data-ttu-id="d93e0-145">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d93e0-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d93e0-146">nein</span><span class="sxs-lookup"><span data-stu-id="d93e0-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d93e0-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d93e0-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d93e0-148">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d93e0-148">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





