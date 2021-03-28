---
title: sample_b (SM4-ASM)
description: Stichproben von Daten aus dem angegebenen Element/der Textur mithilfe der angegebenen Adresse und des vom angegebenen Sampler identifizierten Filter Modus. | sample_b (SM4-ASM)
ms.assetid: FC0DF03E-9C21-4E88-96ED-EEFE86017E7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e82696ecc5b01847f87b39cbfeba0c665bcde4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219323"
---
# <a name="sample_b-sm4---asm"></a><span data-ttu-id="7d7d9-104">Beispiel \_ b (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="7d7d9-104">sample\_b (sm4 - asm)</span></span>

<span data-ttu-id="7d7d9-105">Stichproben von Daten aus dem angegebenen Element/der Textur mithilfe der angegebenen Adresse und des vom angegebenen Sampler identifizierten Filter Modus.</span><span class="sxs-lookup"><span data-stu-id="7d7d9-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="7d7d9-106">Sample \_ b \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcaddress \[ . Swizzle \] , srkresource \[ . Swizzle \] , srcsampler, srclodbias. Select- \_ Komponente</span><span class="sxs-lookup"><span data-stu-id="7d7d9-106">sample\_b\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler, srcLODBias.select\_component</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="7d7d9-107">Element</span><span class="sxs-lookup"><span data-stu-id="7d7d9-107">Item</span></span>                                                                                                               | <span data-ttu-id="7d7d9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d7d9-108">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d7d9-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="7d7d9-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="7d7d9-110">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="7d7d9-110">\[in\] The address of the result of the operation.</span></span><br/>                                                              |
| <span data-ttu-id="7d7d9-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*</span><span class="sxs-lookup"><span data-stu-id="7d7d9-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="7d7d9-112">\[in \] einem Satz von Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="7d7d9-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="7d7d9-113">Weitere Informationen finden Sie in der [Beispiel](sample--sm4---asm-.md) Anweisung.</span><span class="sxs-lookup"><span data-stu-id="7d7d9-113">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="7d7d9-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*</span><span class="sxs-lookup"><span data-stu-id="7d7d9-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="7d7d9-115">\[in \] einem Textur Register.</span><span class="sxs-lookup"><span data-stu-id="7d7d9-115">\[in\] A texture register.</span></span> <span data-ttu-id="7d7d9-116">Weitere Informationen finden Sie in der **Beispiel** Anweisung.</span><span class="sxs-lookup"><span data-stu-id="7d7d9-116">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="7d7d9-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcsampler*</span><span class="sxs-lookup"><span data-stu-id="7d7d9-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="7d7d9-118">\[in \] einem Samplerregister.</span><span class="sxs-lookup"><span data-stu-id="7d7d9-118">\[in\] A sampler register.</span></span> <span data-ttu-id="7d7d9-119">Weitere Informationen finden Sie in der **Beispiel** Anweisung.</span><span class="sxs-lookup"><span data-stu-id="7d7d9-119">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="7d7d9-120"><span id="srcLODBias"></span><span id="srclodbias"></span><span id="SRCLODBIAS"></span>*srclodbias*</span><span class="sxs-lookup"><span data-stu-id="7d7d9-120"><span id="srcLODBias"></span><span id="srclodbias"></span><span id="SRCLODBIAS"></span>*srcLODBias*</span></span><br/>     | <span data-ttu-id="7d7d9-121">\[\]Weitere Informationen zu diesem Parameter finden Sie im Abschnitt " **Hinweise** ".</span><span class="sxs-lookup"><span data-stu-id="7d7d9-121">\[in\] See the **Remarks** section for information about this parameter.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="7d7d9-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d7d9-122">Remarks</span></span>

<span data-ttu-id="7d7d9-123">Die Quelldaten können von jedem Ressourcentyp (außer Puffern) stammen.</span><span class="sxs-lookup"><span data-stu-id="7d7d9-123">The source data may come from any Resource Type, other than Buffers.</span></span> <span data-ttu-id="7d7d9-124">Im Rahmen der Anweisungs Ausführung wird eine zusätzliche Abweichung auf die Detailebene angewendet.</span><span class="sxs-lookup"><span data-stu-id="7d7d9-124">An additional bias is applied to the level of detail computed as part of the instruction execution.</span></span>

<span data-ttu-id="7d7d9-125">Diese Anweisung verhält sich wie die [Beispiel](sample--sm4---asm-.md) Anweisung mit dem Hinzufügen des angegebenen *srclodbias* -Werts auf den Detail Wert, der als Teil der Anweisungs Ausführung berechnet wurde, bevor die MIP-Karte ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="7d7d9-125">This instruction behaves like the [sample](sample--sm4---asm-.md) instruction with the addition of applying the specified *srcLODBias* value to the level of detail value computed as part of the instruction execution prior to selecting the mip map(s).</span></span> <span data-ttu-id="7d7d9-126">Der *srclodbias* -Wert wird der berechneten LOD auf Pixel Basis zusammen mit dem Sampler-miplodbias-Wert hinzugefügt, vor der Klammer an minlod und maxlod.</span><span class="sxs-lookup"><span data-stu-id="7d7d9-126">The *srcLODBias* value is added to the computed LOD on a per-pixel basis, along with the sampler MipLODBias value, prior to the clamp to MinLOD and MaxLOD.</span></span>

### <a name="restrictions"></a><span data-ttu-id="7d7d9-127">Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="7d7d9-127">Restrictions</span></span>

-   <span data-ttu-id="7d7d9-128">**Beispiel \_ b** erbt dieselben Einschränkungen wie die [Beispiel](sample--sm4---asm-.md) Anweisung sowie zusätzliche Einschränkungen für den zusätzlichen Parameter.</span><span class="sxs-lookup"><span data-stu-id="7d7d9-128">**sample\_b** inherits the same restrictions as the [sample](sample--sm4---asm-.md) instruction, plus additional restrictions for its additional parameter.</span></span>
-   <span data-ttu-id="7d7d9-129">Der Bereich von *srclodbias* ist (-16,0 f bis 15,99 f). Werte außerhalb dieses Bereichs führen zu undefinierten Ergebnissen.</span><span class="sxs-lookup"><span data-stu-id="7d7d9-129">The range of *srcLODBias* is (-16.0f to 15.99f); values outside of this range will produce undefined results.</span></span>
-   <span data-ttu-id="7d7d9-130">*srclodbias* muss eine einzelne Komponentenauswahl verwenden, wenn es sich nicht um eine sofortige skalare handelt.</span><span class="sxs-lookup"><span data-stu-id="7d7d9-130">*srcLODBias* must use a single component selector if it is not a scalar immediate.</span></span>

<span data-ttu-id="7d7d9-131">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="7d7d9-131">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7d7d9-132">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="7d7d9-132">Vertex Shader</span></span> | <span data-ttu-id="7d7d9-133">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="7d7d9-133">Geometry Shader</span></span> | <span data-ttu-id="7d7d9-134">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="7d7d9-134">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="7d7d9-135">x</span><span class="sxs-lookup"><span data-stu-id="7d7d9-135">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7d7d9-136">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="7d7d9-136">Minimum Shader Model</span></span>

<span data-ttu-id="7d7d9-137">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7d7d9-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7d7d9-138">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="7d7d9-138">Shader Model</span></span>                                              | <span data-ttu-id="7d7d9-139">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="7d7d9-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7d7d9-140">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="7d7d9-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7d7d9-141">ja</span><span class="sxs-lookup"><span data-stu-id="7d7d9-141">yes</span></span>       |
| [<span data-ttu-id="7d7d9-142">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="7d7d9-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7d7d9-143">ja</span><span class="sxs-lookup"><span data-stu-id="7d7d9-143">yes</span></span>       |
| [<span data-ttu-id="7d7d9-144">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="7d7d9-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7d7d9-145">ja</span><span class="sxs-lookup"><span data-stu-id="7d7d9-145">yes</span></span>       |
| [<span data-ttu-id="7d7d9-146">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7d7d9-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7d7d9-147">nein</span><span class="sxs-lookup"><span data-stu-id="7d7d9-147">no</span></span>        |
| [<span data-ttu-id="7d7d9-148">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7d7d9-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7d7d9-149">nein</span><span class="sxs-lookup"><span data-stu-id="7d7d9-149">no</span></span>        |
| [<span data-ttu-id="7d7d9-150">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7d7d9-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7d7d9-151">nein</span><span class="sxs-lookup"><span data-stu-id="7d7d9-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7d7d9-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7d7d9-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d7d9-153">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7d7d9-153">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





