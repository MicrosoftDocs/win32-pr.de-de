---
title: sample_d (SM4-ASM)
description: Stichproben von Daten aus dem angegebenen Element/der Textur mithilfe der angegebenen Adresse und des vom angegebenen Sampler identifizierten Filter Modus. | sample_d (SM4-ASM)
ms.assetid: 9CF57C4A-C0D1-4D57-A5EE-62BBBB291438
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe2d3ad310c18ff2bb10e101c95e0267d534fed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995638"
---
# <a name="sample_d-sm4---asm"></a><span data-ttu-id="8303d-104">Sample \_ d (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="8303d-104">sample\_d (sm4 - asm)</span></span>

<span data-ttu-id="8303d-105">Stichproben von Daten aus dem angegebenen Element/der Textur mithilfe der angegebenen Adresse und des vom angegebenen Sampler identifizierten Filter Modus.</span><span class="sxs-lookup"><span data-stu-id="8303d-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="8303d-106">ssample \_ d \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcaddress \[ . Swizzle \] , srkresource \[ . Swizzle \] , srcsampler, srcxderivatives \[ . Swizzle \] , srcyderivatives \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="8303d-106">ssample\_d\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler, srcXDerivatives\[.swizzle\], srcYDerivatives\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="8303d-107">Element</span><span class="sxs-lookup"><span data-stu-id="8303d-107">Item</span></span>                                                                                                                               | <span data-ttu-id="8303d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8303d-108">Description</span></span>                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8303d-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="8303d-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                    | <span data-ttu-id="8303d-110">\[in \] der Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="8303d-110">\[in\] The address of the results of the operation.</span></span><br/>                                                                  |
| <span data-ttu-id="8303d-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*</span><span class="sxs-lookup"><span data-stu-id="8303d-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                     | <span data-ttu-id="8303d-112">\[in \] einem Satz von Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="8303d-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="8303d-113">Weitere Informationen finden Sie in der [Beispiel](sample--sm4---asm-.md) Anweisung.</span><span class="sxs-lookup"><span data-stu-id="8303d-113">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/>      |
| <span data-ttu-id="8303d-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*</span><span class="sxs-lookup"><span data-stu-id="8303d-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                 | <span data-ttu-id="8303d-115">\[in \] einem Textur Register.</span><span class="sxs-lookup"><span data-stu-id="8303d-115">\[in\] A texture register.</span></span> <span data-ttu-id="8303d-116">Weitere Informationen finden Sie in der **Beispiel** Anweisung.</span><span class="sxs-lookup"><span data-stu-id="8303d-116">For more information see the **sample** instruction.</span></span><br/>                                      |
| <span data-ttu-id="8303d-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcsampler*</span><span class="sxs-lookup"><span data-stu-id="8303d-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                     | <span data-ttu-id="8303d-118">\[in \] einem Samplerregister.</span><span class="sxs-lookup"><span data-stu-id="8303d-118">\[in\] A sampler register.</span></span> <span data-ttu-id="8303d-119">Weitere Informationen finden Sie in der **Beispiel** Anweisung.</span><span class="sxs-lookup"><span data-stu-id="8303d-119">For more information see the **sample** instruction.</span></span><br/>                                      |
| <span data-ttu-id="8303d-120"><span id="srcXDerivatives"></span><span id="srcxderivatives"></span><span id="SRCXDERIVATIVES"></span>*srcxableitungen*</span><span class="sxs-lookup"><span data-stu-id="8303d-120"><span id="srcXDerivatives"></span><span id="srcxderivatives"></span><span id="SRCXDERIVATIVES"></span>*srcXDerivatives*</span></span><br/> | <span data-ttu-id="8303d-121">\[in \] den Ableitungen für die Quelladresse in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="8303d-121">\[in\] The derivatives for the source address in the x direction.</span></span> <span data-ttu-id="8303d-122">Weitere Informationen finden Sie im Abschnitt **Hinweise**.</span><span class="sxs-lookup"><span data-stu-id="8303d-122">For more information, see the **Remarks** section.</span></span><br/> |
| <span data-ttu-id="8303d-123"><span id="srcYDerivatives"></span><span id="srcyderivatives"></span><span id="SRCYDERIVATIVES"></span>*srcY-Ableitungen*</span><span class="sxs-lookup"><span data-stu-id="8303d-123"><span id="srcYDerivatives"></span><span id="srcyderivatives"></span><span id="SRCYDERIVATIVES"></span>*srcYDerivatives*</span></span><br/> | <span data-ttu-id="8303d-124">\[in \] den Ableitungen für die Quelladresse in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="8303d-124">\[in\] The derivatives for the source address in the y direction.</span></span> <span data-ttu-id="8303d-125">Weitere Informationen finden Sie im Abschnitt **Hinweise**.</span><span class="sxs-lookup"><span data-stu-id="8303d-125">For more information, see the **Remarks** section.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8303d-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8303d-126">Remarks</span></span>

<span data-ttu-id="8303d-127">Diese Anweisung verhält sich wie die [Beispiel](sample--sm4---asm-.md) Anweisung, mit der Ausnahme, dass Ableitungen für die Quelladresse in der x-und der y-Richtung von zusätzlichen Parametern, *srcxderivatives* bzw. *srcyderivatives*, bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8303d-127">This instruction behaves like the [sample](sample--sm4---asm-.md) instruction, except that derivatives for the source address in the x direction and the y direction are provided by extra parameters, *srcXDerivatives* and *srcYDerivatives*, respectively.</span></span> <span data-ttu-id="8303d-128">Diese Ableitungen befinden sich im normalisierten Texturkoordinaten Bereich.</span><span class="sxs-lookup"><span data-stu-id="8303d-128">These derivatives are in normalized texture coordinate space.</span></span>

<span data-ttu-id="8303d-129">Die r-, g-und b-Komponenten von *srcxderivatives* (POS-Swizzle) stellen du/DX, DV/DX und DW/DX bereit.</span><span class="sxs-lookup"><span data-stu-id="8303d-129">The r, g and b components of *srcXDerivatives* (POS-swizzle) provide du/dx, dv/dx and dw/dx.</span></span> <span data-ttu-id="8303d-130">Die Komponente "a" (POS-Swizzle) wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8303d-130">The 'a' component (POS-swizzle) is ignored.</span></span>

<span data-ttu-id="8303d-131">Die r-, g-und b-Komponenten von *srcyderivatives* (POS-Swizzle) stellen du/dy, DV/DY und DW/dy bereit.</span><span class="sxs-lookup"><span data-stu-id="8303d-131">The r, g and b components of *srcYDerivatives* (POS-swizzle) provide du/dy, dv/dy and dw/dy.</span></span> <span data-ttu-id="8303d-132">Die Komponente "a" (POS-Swizzle) wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8303d-132">The 'a' component (POS-swizzle) is ignored.</span></span>

<span data-ttu-id="8303d-133">Anders als bei der **Beispiel** Anweisung, die eine einzelne Lod-Berechnung für einen 2 x 2-Stempel freigeben darf, muss **Sample \_ d** Lod bei der Verwendung im Pixelshader vollständig einzeln berechnen.</span><span class="sxs-lookup"><span data-stu-id="8303d-133">Unlike the **sample** instruction, which is permitted to share a single LOD calculation across a 2x2 stamp, **sample\_d** must calculate LOD completely independently, per-pixel when used in the Pixel Shader.</span></span>

<span data-ttu-id="8303d-134">Wenn die abgeleiteten Eingaben für **Stichprobe \_ d** aus den Anweisungen für die Ableitung von Anweisungen im Pixelshader stammen und die Werte INF/Nan enthalten, entspricht das Verhalten von **Beispiel \_ d** möglicherweise nicht der **Beispiel** Anweisung, die implizit die Ableitung berechnet.</span><span class="sxs-lookup"><span data-stu-id="8303d-134">If the derivative inputs to **sample\_d** came from derivative calculation instructions in the Pixel Shader and the values include INF/NaN, the behavior of **sample\_d** may not match the **sample** instruction, which implicitly computes the derivative.</span></span> <span data-ttu-id="8303d-135">Die INF/NaN-Werte können die Lod-Berechnung anders beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="8303d-135">The INF/NaN values may affect the LOD calculation differently.</span></span>

<span data-ttu-id="8303d-136">Wenn Sie aus einem Eingabe Slot abrufen, an das nichts gebunden ist, wird 0 für alle Komponenten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8303d-136">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

### <a name="restrictions"></a><span data-ttu-id="8303d-137">Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="8303d-137">Restrictions</span></span>

-   <span data-ttu-id="8303d-138">**Stichprobe \_ d** erbt die gleichen Einschränkungen wie die **Beispiel** Anweisung und zusätzlich eine Einschränkung unten für die zusätzlichen Parameter.</span><span class="sxs-lookup"><span data-stu-id="8303d-138">**sample\_d** inherits the same restrictions as the **sample** instruction, plus additional an restriction below for its additional parameters.</span></span>
-   <span data-ttu-id="8303d-139">*srcxderivatives* und *srcyderivatives* müssen Temp (r \# /x \# ), constantbuffer (CB \# ), Eingabe (v)- \# Register oder unmittelbare Werte sein.</span><span class="sxs-lookup"><span data-stu-id="8303d-139">*srcXDerivatives* and *srcYDerivatives* must be temp (r\#/x\#), constantBuffer (cb\#), input (v\#) registers or immediate value(s).</span></span>

<span data-ttu-id="8303d-140">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="8303d-140">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8303d-141">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="8303d-141">Vertex Shader</span></span> | <span data-ttu-id="8303d-142">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="8303d-142">Geometry Shader</span></span> | <span data-ttu-id="8303d-143">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="8303d-143">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="8303d-144">X</span><span class="sxs-lookup"><span data-stu-id="8303d-144">X</span></span>             | <span data-ttu-id="8303d-145">X</span><span class="sxs-lookup"><span data-stu-id="8303d-145">X</span></span>               | <span data-ttu-id="8303d-146">w</span><span class="sxs-lookup"><span data-stu-id="8303d-146">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8303d-147">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="8303d-147">Minimum Shader Model</span></span>

<span data-ttu-id="8303d-148">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8303d-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8303d-149">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="8303d-149">Shader Model</span></span>                                              | <span data-ttu-id="8303d-150">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="8303d-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8303d-151">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="8303d-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8303d-152">ja</span><span class="sxs-lookup"><span data-stu-id="8303d-152">yes</span></span>       |
| [<span data-ttu-id="8303d-153">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="8303d-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8303d-154">ja</span><span class="sxs-lookup"><span data-stu-id="8303d-154">yes</span></span>       |
| [<span data-ttu-id="8303d-155">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="8303d-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8303d-156">ja</span><span class="sxs-lookup"><span data-stu-id="8303d-156">yes</span></span>       |
| [<span data-ttu-id="8303d-157">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8303d-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8303d-158">nein</span><span class="sxs-lookup"><span data-stu-id="8303d-158">no</span></span>        |
| [<span data-ttu-id="8303d-159">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8303d-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8303d-160">nein</span><span class="sxs-lookup"><span data-stu-id="8303d-160">no</span></span>        |
| [<span data-ttu-id="8303d-161">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8303d-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8303d-162">nein</span><span class="sxs-lookup"><span data-stu-id="8303d-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8303d-163">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8303d-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8303d-164">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8303d-164">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





