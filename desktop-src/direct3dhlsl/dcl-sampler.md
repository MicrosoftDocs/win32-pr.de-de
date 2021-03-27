---
title: dcl_sampler (SM4-ASM)
description: DCL \_ -Sampler (SM4-ASM)
ms.assetid: 285a47fa-2d47-4ba9-90b9-3f4c61d5dce1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 45b6da3bcdb027a00edeb4f009773533424efeb8
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104391115"
---
# <a name="dcl_sampler-sm4---asm"></a><span data-ttu-id="9c3bc-103">DCL \_ -Sampler (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="9c3bc-103">dcl\_sampler (sm4 - asm)</span></span>

<span data-ttu-id="9c3bc-104">Deklariert ein Samplerregister.</span><span class="sxs-lookup"><span data-stu-id="9c3bc-104">Declares a sampler register.</span></span>



| <span data-ttu-id="9c3bc-105">DCL- \_ samplersn, Modus</span><span class="sxs-lookup"><span data-stu-id="9c3bc-105">dcl\_sampler sN, mode</span></span> |
|-----------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c3bc-106">Element</span><span class="sxs-lookup"><span data-stu-id="9c3bc-106">Item</span></span></th>
<th><span data-ttu-id="9c3bc-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9c3bc-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c3bc-108"><span id="sN"></span><span id="sn"></span><span id="SN"></span>s<em>N</em></span><span class="sxs-lookup"><span data-stu-id="9c3bc-108"><span id="sN"></span><span id="sn"></span><span id="SN"></span>s<em>N</em></span></span><br/></td>
<td><span data-ttu-id="9c3bc-109">in Ein Samplerregister, wobei <em>N</em> eine ganze Zahl ist, die die Registernummer bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9c3bc-109">[in] A sampler register, where <em>N</em> is an integer that denotes the register number.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c3bc-110"><span id="mode"></span><span id="MODE"></span><em>Spar</em></span><span class="sxs-lookup"><span data-stu-id="9c3bc-110"><span id="mode"></span><span id="MODE"></span><em>mode</em></span></span><br/></td>
<td><span data-ttu-id="9c3bc-111">in Ein Samplingmodus, der einschränkt, welche samplerzustände (aufgelistet in den Mitgliedern von <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>D3D10_SAMPLER_DESC</strong></a>) berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="9c3bc-111">[in] A sampler mode, which constrains which sampler states (listed in the members of <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>D3D10_SAMPLER_DESC</strong></a>) are honored.</span></span> <span data-ttu-id="9c3bc-112">Die Modi und Zustände werden in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9c3bc-112">The modes and states are listed in the following table.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9c3bc-113">Modus</span><span class="sxs-lookup"><span data-stu-id="9c3bc-113">Mode</span></span></th>
<th><span data-ttu-id="9c3bc-114">Samplerzustände berücksichtigt</span><span class="sxs-lookup"><span data-stu-id="9c3bc-114">Sampler States Honored</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c3bc-115">default</span><span class="sxs-lookup"><span data-stu-id="9c3bc-115">default</span></span></td>
<td><span data-ttu-id="9c3bc-116"><em>Filter</em> (kann nicht die Werte _COMPARISON oder _TEXT verwenden), <em>adressssu/V/W</em>, <em>minlod/maxlod</em>, <em>miplodbias</em>, <em>MaxAnisotropy</em>, <em>BorderColor [4]</em></span><span class="sxs-lookup"><span data-stu-id="9c3bc-116"><em>Filter</em> (may not use the _COMPARISON or _TEXT values), <em>AddressU/V/W</em>, <em>MinLOD/MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor[4]</em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c3bc-117">Vergleich</span><span class="sxs-lookup"><span data-stu-id="9c3bc-117">comparison</span></span></td>
<td><span data-ttu-id="9c3bc-118"><em>Filter</em>, <em>comparisonfunction</em>, <em>adressssu/V/W</em>, <em>minlod, maxlod</em>, <em>miplodbias</em>, <em>MaxAnisotropy</em>, <em>BorderColor [4]</em></span><span class="sxs-lookup"><span data-stu-id="9c3bc-118"><em>Filter</em>, <em>ComparisonFunction</em>, <em>AddressU/V/W</em>, <em>MinLOD,MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor[4]</em></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c3bc-119">ein</span><span class="sxs-lookup"><span data-stu-id="9c3bc-119">mono</span></span></td>
<td><span data-ttu-id="9c3bc-120"><em>Filter</em> (muss einer der _text Werte sein), <em>monofilterwidth</em>, <em>monofilterheight</em> (diese beiden Zustände sind Global Device State), <em>minlod</em>, <em>miplodbias</em>, <em>MaxAnisotropy</em></span><span class="sxs-lookup"><span data-stu-id="9c3bc-120"><em>Filter</em> (must be one of the _TEXT values), <em>MonoFilterWidth</em>, <em>MonoFilterHeight</em> (these two states are global device state), <em>MinLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em></span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9c3bc-121">Der Modus schränkt die Beispiel Anweisungen ein, die verwendet werden können. in dieser Tabelle werden die Textur Objektmethoden aufgelistet, die für die einzelnen Modi unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="9c3bc-121">The mode restricts the sample instructions that can be used; this table lists the texture-object methods that are supported for each mode.</span></span>



| <span data-ttu-id="9c3bc-122">Ein Sampler, der in diesem Modus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9c3bc-122">A Sampler Operating in this Mode</span></span> | <span data-ttu-id="9c3bc-123">Kann diese Texture-Object Methoden verwenden</span><span class="sxs-lookup"><span data-stu-id="9c3bc-123">Can Use these Texture-Object Methods</span></span>                                                                                                           |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c3bc-124">default</span><span class="sxs-lookup"><span data-stu-id="9c3bc-124">default</span></span>                          | <span data-ttu-id="9c3bc-125">[Sample](dx-graphics-hlsl-to-sample.md), [samplelevel](dx-graphics-hlsl-to-samplelevel.md), [samplegrad](dx-graphics-hlsl-to-samplegrad.md)</span><span class="sxs-lookup"><span data-stu-id="9c3bc-125">[Sample](dx-graphics-hlsl-to-sample.md), [SampleLevel](dx-graphics-hlsl-to-samplelevel.md), [SampleGrad](dx-graphics-hlsl-to-samplegrad.md)</span></span> |
| <span data-ttu-id="9c3bc-126">Vergleich</span><span class="sxs-lookup"><span data-stu-id="9c3bc-126">comparison</span></span>                       | <span data-ttu-id="9c3bc-127">[Samplecmp](dx-graphics-hlsl-to-samplecmp.md), [samplecmplevelzero](dx-graphics-hlsl-to-samplecmplevelzero.md)</span><span class="sxs-lookup"><span data-stu-id="9c3bc-127">[SampleCmp](dx-graphics-hlsl-to-samplecmp.md), [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)</span></span>                               |
| <span data-ttu-id="9c3bc-128">ein</span><span class="sxs-lookup"><span data-stu-id="9c3bc-128">mono</span></span>                             | [<span data-ttu-id="9c3bc-129">Samplelevel</span><span class="sxs-lookup"><span data-stu-id="9c3bc-129">SampleLevel</span></span>](dx-graphics-hlsl-to-samplelevel.md)                                                                                             |



 

<span data-ttu-id="9c3bc-130">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="9c3bc-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9c3bc-131">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="9c3bc-131">Vertex Shader</span></span> | <span data-ttu-id="9c3bc-132">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="9c3bc-132">Geometry Shader</span></span> | <span data-ttu-id="9c3bc-133">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="9c3bc-133">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9c3bc-134">x</span><span class="sxs-lookup"><span data-stu-id="9c3bc-134">x</span></span>             | <span data-ttu-id="9c3bc-135">x</span><span class="sxs-lookup"><span data-stu-id="9c3bc-135">x</span></span>               | <span data-ttu-id="9c3bc-136">x\*</span><span class="sxs-lookup"><span data-stu-id="9c3bc-136">x\*</span></span>          |



 

<span data-ttu-id="9c3bc-137">\* -Die Verwendung eines Samplers im Mono-Modus wird nur in einem Pixelshader unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9c3bc-137">\* - Using a sampler in mono mode is supported only in a pixel shader.</span></span>

<span data-ttu-id="9c3bc-138">Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9c3bc-138">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="9c3bc-139">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9c3bc-139">Example</span></span>

<span data-ttu-id="9c3bc-140">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9c3bc-140">Here is an example.</span></span>


```
dcl_sampler s3, default
```



## <a name="minimum-shader-model"></a><span data-ttu-id="9c3bc-141">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="9c3bc-141">Minimum Shader Model</span></span>

<span data-ttu-id="9c3bc-142">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9c3bc-142">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9c3bc-143">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="9c3bc-143">Shader Model</span></span>                                              | <span data-ttu-id="9c3bc-144">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="9c3bc-144">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9c3bc-145">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="9c3bc-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9c3bc-146">ja</span><span class="sxs-lookup"><span data-stu-id="9c3bc-146">yes</span></span>       |
| [<span data-ttu-id="9c3bc-147">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="9c3bc-147">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9c3bc-148">ja</span><span class="sxs-lookup"><span data-stu-id="9c3bc-148">yes</span></span>       |
| [<span data-ttu-id="9c3bc-149">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="9c3bc-149">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9c3bc-150">ja</span><span class="sxs-lookup"><span data-stu-id="9c3bc-150">yes</span></span>       |
| [<span data-ttu-id="9c3bc-151">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9c3bc-151">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9c3bc-152">nein</span><span class="sxs-lookup"><span data-stu-id="9c3bc-152">no</span></span>        |
| [<span data-ttu-id="9c3bc-153">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9c3bc-153">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9c3bc-154">nein</span><span class="sxs-lookup"><span data-stu-id="9c3bc-154">no</span></span>        |
| [<span data-ttu-id="9c3bc-155">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9c3bc-155">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9c3bc-156">nein</span><span class="sxs-lookup"><span data-stu-id="9c3bc-156">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9c3bc-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9c3bc-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c3bc-158">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9c3bc-158">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

