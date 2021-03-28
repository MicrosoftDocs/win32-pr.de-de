---
title: dcl_indexRange (SM4-ASM)
description: DCL \_ -indexrange (SM4-ASM)
ms.assetid: 88af30f3-dbf9-4556-b170-a7371680f9b9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b0e2c250afd4ce52729a4c4bffeee0f33e4be6b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976497"
---
# <a name="dcl_indexrange-sm4---asm"></a><span data-ttu-id="b9bbe-103">DCL \_ -indexrange (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="b9bbe-103">dcl\_indexRange (sm4 - asm)</span></span>

<span data-ttu-id="b9bbe-104">Deklariert einen Bereich von Registern, auf die über den Index zugegriffen wird (eine im Shader berechnete Ganzzahl).</span><span class="sxs-lookup"><span data-stu-id="b9bbe-104">Declares a range of registers that will be accessed by index (an integer computed in the shader).</span></span>



| <span data-ttu-id="b9bbe-105">DCL \_ indexrange *minregisterm*, *maxRegisterN*</span><span class="sxs-lookup"><span data-stu-id="b9bbe-105">dcl\_indexRange *minRegisterM*, *maxRegisterN*</span></span> |
|------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b9bbe-106">Element</span><span class="sxs-lookup"><span data-stu-id="b9bbe-106">Item</span></span></th>
<th><span data-ttu-id="b9bbe-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b9bbe-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b9bbe-108"><span id="minRegisterM"></span><span id="minregisterm"></span><span id="MINREGISTERM"></span><em>minregisterm</em></span><span class="sxs-lookup"><span data-stu-id="b9bbe-108"><span id="minRegisterM"></span><span id="minregisterm"></span><span id="MINREGISTERM"></span><em>minRegisterM</em></span></span><br/></td>
<td><span data-ttu-id="b9bbe-109">in Das erste Register für den Zugriff nach Index.</span><span class="sxs-lookup"><span data-stu-id="b9bbe-109">[in] The first register to access by index.</span></span> <br/>
<ul>
<li><span data-ttu-id="b9bbe-110"><em>minregister</em> ist entweder <strong>v</strong> für ein Vertex-oder Pixel-Shader-Eingabe Register oder <strong>o</strong> für ein Vertex-Shader-Ausgabe Register.</span><span class="sxs-lookup"><span data-stu-id="b9bbe-110"><em>minRegister</em> is either <strong>v</strong> for a vertex or pixel shader input register, or <strong>o</strong> for a vertex shader output register.</span></span></li>
<li><span data-ttu-id="b9bbe-111"><em>M</em> ist eine ganze Zahl, die die Registernummer bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b9bbe-111"><em>M</em> is an integer that denotes the register number.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b9bbe-112"><span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em></span><span class="sxs-lookup"><span data-stu-id="b9bbe-112"><span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em></span></span><br/></td>
<td><span data-ttu-id="b9bbe-113">in Das letzte Register für den Zugriff nach Index.</span><span class="sxs-lookup"><span data-stu-id="b9bbe-113">[in] The last register to access by index.</span></span> <span data-ttu-id="b9bbe-114">Dieselbe Form wie " <em>minregister</em> " mit Ausnahme von " <em>N</em> " ist die Registernummer.</span><span class="sxs-lookup"><span data-stu-id="b9bbe-114">Same form as <em>minRegister</em> except <em>N</em> is the register number.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b9bbe-115">Die folgenden Einschränkungen gelten für alle Register:</span><span class="sxs-lookup"><span data-stu-id="b9bbe-115">The following restrictions apply to all registers:</span></span>

-   <span data-ttu-id="b9bbe-116">Die min-und Max-Register müssen denselben Typ aufweisen und dieselben Komponenten Masken aufweisen (Wenn Masken deklariert sind).</span><span class="sxs-lookup"><span data-stu-id="b9bbe-116">The min and max registers must be the same type and have the same component masks (if masks are declared).</span></span>
-   <span data-ttu-id="b9bbe-117">Ein Register kann mehrere Index Bereiche enthalten, solange Sie sich nicht überlappen.</span><span class="sxs-lookup"><span data-stu-id="b9bbe-117">A register may have multiple index ranges, as long as they do no not overlap.</span></span>
-   <span data-ttu-id="b9bbe-118">Die minimale Registernummer muss kleiner als die maximale Registernummer sein.</span><span class="sxs-lookup"><span data-stu-id="b9bbe-118">The min register number must be less than the max register number.</span></span>
-   <span data-ttu-id="b9bbe-119">Ein Indexregister darf keinen [System Wert](dx-graphics-hlsl-semantics.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="b9bbe-119">An index register cannot contain a [system-value](dx-graphics-hlsl-semantics.md).</span></span>
-   <span data-ttu-id="b9bbe-120">Die Indizierung eines Registers außerhalb der maximalen Index Deklaration erzeugt nicht definierte Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="b9bbe-120">Indexing a register outside of the max index declaration produces undefined results.</span></span>

<span data-ttu-id="b9bbe-121">Pixel-Shader-Eingabe Register müssen denselben Interpolations Modus verwenden. Pixel-Shader-Ausgabe Register können nicht indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="b9bbe-121">Pixel shader input registers must use the same interpolation mode; pixel shader output registers are not indexable.</span></span>

<span data-ttu-id="b9bbe-122">Ein Geometrie-Shader-Eingabe Register hat zwei Dimensionen (vertexachse, Attribut Achse); der Index Bereich gilt nur für die Attribut Achse, da die vertexachse immer vollständig indizierbar ist.</span><span class="sxs-lookup"><span data-stu-id="b9bbe-122">A geometry shader input register has two dimensions (vertex axis, attribute axis); the index range applies only to the attribute axis because the vertex axis is always fully indexable.</span></span>

<span data-ttu-id="b9bbe-123">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="b9bbe-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b9bbe-124">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="b9bbe-124">Vertex Shader</span></span> | <span data-ttu-id="b9bbe-125">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="b9bbe-125">Geometry Shader</span></span> | <span data-ttu-id="b9bbe-126">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="b9bbe-126">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b9bbe-127">x</span><span class="sxs-lookup"><span data-stu-id="b9bbe-127">x</span></span>             | <span data-ttu-id="b9bbe-128">x</span><span class="sxs-lookup"><span data-stu-id="b9bbe-128">x</span></span>               | <span data-ttu-id="b9bbe-129">x</span><span class="sxs-lookup"><span data-stu-id="b9bbe-129">x</span></span>            |



 

<span data-ttu-id="b9bbe-130">Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b9bbe-130">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="b9bbe-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b9bbe-131">Example</span></span>

<span data-ttu-id="b9bbe-132">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="b9bbe-132">Here is an example.</span></span>


```
dcl_indexRange v1, v3
dcl_indexRange v4, v9
```



## <a name="minimum-shader-model"></a><span data-ttu-id="b9bbe-133">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="b9bbe-133">Minimum Shader Model</span></span>

<span data-ttu-id="b9bbe-134">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b9bbe-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b9bbe-135">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="b9bbe-135">Shader Model</span></span>                                              | <span data-ttu-id="b9bbe-136">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="b9bbe-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b9bbe-137">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="b9bbe-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b9bbe-138">ja</span><span class="sxs-lookup"><span data-stu-id="b9bbe-138">yes</span></span>       |
| [<span data-ttu-id="b9bbe-139">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="b9bbe-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b9bbe-140">ja</span><span class="sxs-lookup"><span data-stu-id="b9bbe-140">yes</span></span>       |
| [<span data-ttu-id="b9bbe-141">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="b9bbe-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b9bbe-142">ja</span><span class="sxs-lookup"><span data-stu-id="b9bbe-142">yes</span></span>       |
| [<span data-ttu-id="b9bbe-143">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b9bbe-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b9bbe-144">nein</span><span class="sxs-lookup"><span data-stu-id="b9bbe-144">no</span></span>        |
| [<span data-ttu-id="b9bbe-145">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b9bbe-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b9bbe-146">nein</span><span class="sxs-lookup"><span data-stu-id="b9bbe-146">no</span></span>        |
| [<span data-ttu-id="b9bbe-147">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b9bbe-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b9bbe-148">nein</span><span class="sxs-lookup"><span data-stu-id="b9bbe-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b9bbe-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b9bbe-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9bbe-150">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b9bbe-150">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





