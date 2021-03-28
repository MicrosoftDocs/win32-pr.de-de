---
title: fcall(SM5-ASM)
description: Schnittstellen Funktionsaufrufe.
ms.assetid: C21784A0-D2F4-4DDE-9AC4-4F21351BCA6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57ea40fec51cf4155b0932f6ce4a7b80d3180dd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389586"
---
# <a name="fcall-sm5---asm"></a><span data-ttu-id="18517-103">fcall(SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="18517-103">fcall (sm5 - asm)</span></span>

<span data-ttu-id="18517-104">Schnittstellen Funktionsaufrufe.</span><span class="sxs-lookup"><span data-stu-id="18517-104">Interface function call.</span></span>



| <span data-ttu-id="18517-105">fcallcenter FP \# \[ arrayIndex \] \[ CallSite\]</span><span class="sxs-lookup"><span data-stu-id="18517-105">fcall fp\#\[arrayIndex\]\[callSite\]</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="18517-106">Element</span><span class="sxs-lookup"><span data-stu-id="18517-106">Item</span></span>                                                                                                           | <span data-ttu-id="18517-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18517-107">Description</span></span>                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18517-108"><span id="fp_"></span><span id="FP_"></span>*FP\#*</span><span class="sxs-lookup"><span data-stu-id="18517-108"><span id="fp_"></span><span id="FP_"></span>*fp\#*</span></span><br/>                                                  | <span data-ttu-id="18517-109">\[im \] Funktionszeiger.</span><span class="sxs-lookup"><span data-stu-id="18517-109">\[in\] The function pointer.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="18517-110"><span id="arrayIndex"></span><span id="arrayindex"></span><span id="ARRAYINDEX"></span>*Array Index*</span><span class="sxs-lookup"><span data-stu-id="18517-110"><span id="arrayIndex"></span><span id="arrayindex"></span><span id="ARRAYINDEX"></span>*arrayIndex*</span></span><br/> | <span data-ttu-id="18517-111">\[in \] optional.</span><span class="sxs-lookup"><span data-stu-id="18517-111">\[in\] Optional.</span></span> <span data-ttu-id="18517-112">Gibt einen Offset im Funktionszeiger Array an.</span><span class="sxs-lookup"><span data-stu-id="18517-112">Specifies an offset into the function pointer array.</span></span> <span data-ttu-id="18517-113">Dieser Parameter muss eine Literale Ganzzahl ohne Vorzeichen sein, wenn FP \# nicht als Indexable deklariert wurde.</span><span class="sxs-lookup"><span data-stu-id="18517-113">This parameter must be a literal unsigned integer if fp\# was not declared as indexable.</span></span> <span data-ttu-id="18517-114">Andernfalls weist Arrayindex möglicherweise die Form "literalbasis + Offset" aus einem Shader-Register auf.</span><span class="sxs-lookup"><span data-stu-id="18517-114">Otherwise, arrayIndex may be of the form literal base + offset from a shader register.</span></span> <span data-ttu-id="18517-115">Beispiel: fcallfp1 \[ R1. w + 0 \] \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="18517-115">For example, fcall fp1\[r1.w + 0\]\[0\] .</span></span><br/> |
| <span data-ttu-id="18517-116"><span id="_callSite"></span><span id="_callsite"></span><span id="_CALLSITE"></span>*CallSite*</span><span class="sxs-lookup"><span data-stu-id="18517-116"><span id="_callSite"></span><span id="_callsite"></span><span id="_CALLSITE"></span> *callSite*</span></span><br/>     | <span data-ttu-id="18517-117">\[in \] optional.</span><span class="sxs-lookup"><span data-stu-id="18517-117">\[in\] Optional.</span></span> <span data-ttu-id="18517-118">Eine Literale Abweichung ohne Vorzeichen in der ausgewählten Funktions Tabelle, wobei eine Funktions Text-FB ausgewählt wird, die \# ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="18517-118">A literal unsigned integer offset into the selected function table, selecting a function body fb\# to execute.</span></span> <br/>                                                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="18517-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18517-119">Remarks</span></span>

<span data-ttu-id="18517-120">*FP \#* \[ *arrayIndex* \] \[ \] löst eine bestimmte Funktions Tabelle aus, die aus der API außerhalb des Shaders aus den in der Deklaration von *FP \#* aufgelisteten Funktionstabellen Optionen ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="18517-120">*fp\#*\[*arrayIndex*\]\[\] resolves to a particular function table, selected from the API outside the shader from the function table choices listed in the declaration of *fp\#*.</span></span>

<span data-ttu-id="18517-121">Die Summe von \# in *FP \#* und *arrayIndex* wählen Sie die Funktions Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="18517-121">The sum of \# in *fp\#* and *arrayIndex* select the function table.</span></span> <span data-ttu-id="18517-122">Wenn eine Schnittstelle beispielsweise als FP4 \[ 4 \] \[ 3 \] (Array Größe 4) deklariert ist, sind die folgenden **fcalls** äquivalent: fcallfp4 \[ 2 \] \[ 3 \] und FP5 \[ 1 \] \[ 3 \] , da 4 + 2 = 5 + 1 ist.</span><span class="sxs-lookup"><span data-stu-id="18517-122">For example, if an interface is declared as fp4\[4\]\[3\] (array size of 4), the following **fcall** s are equivalent: fcall fp4\[2\]\[3\] and fp5\[1\]\[3\], because 4+2 = 5+1.</span></span>

### <a name="restrictions"></a><span data-ttu-id="18517-123">Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="18517-123">Restrictions</span></span>

-   <span data-ttu-id="18517-124">Wenn *arrayIndex* dynamische Indizierung verwendet, ist das Verhalten nicht definiert, wenn *arrayIndex* bei angrenzenden shaderaufrufen abweicht, die in Lockstep ausgeführt werden könnten.</span><span class="sxs-lookup"><span data-stu-id="18517-124">If *arrayIndex* uses dynamic indexing, behavior is undefined if *arrayIndex* diverges on adjacent shader invocations, which could be executing in lockstep.</span></span> <span data-ttu-id="18517-125">Der HLSL-Compiler versucht, diesen Fall zu unterbinden.</span><span class="sxs-lookup"><span data-stu-id="18517-125">The HLSL compiler will attempt to disallow this case.</span></span>

    <span data-ttu-id="18517-126">Angrenzende Aufrufe können aufgrund der Fluss Steuerung inaktiv sein, da Sie die Ausführung von Gleichschritt nicht unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="18517-126">Adjacent invocations can be inactive due to flow control, because it doesn t break lockstep execution.</span></span>

-   <span data-ttu-id="18517-127">Wenn *FP \#*  +  *arrayIndex* einen Out-of-Bounds-Index angibt, ist das Verhalten nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="18517-127">If *fp\#* + *arrayIndex* specifies an out of bounds index, behavior is undefined.</span></span>
-   <span data-ttu-id="18517-128">In den hier beschriebenen undefinierten Fällen bedeutet dies, dass das Verhalten des aktuellen D3D-Geräts nicht definiert ist, einschließlich der Möglichkeit, dass das Gerät verloren geht.</span><span class="sxs-lookup"><span data-stu-id="18517-128">For the undefined cases described here, it means the behavior of the current D3D device becomes undefined, including the possibility of Device Lost.</span></span> <span data-ttu-id="18517-129">Es wird jedoch kein Speicher außerhalb des aktuellen D3D-Geräts aufgerufen oder als Code ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="18517-129">However no memory outside the current D3D device will be accessed or executed as code.</span></span>

<span data-ttu-id="18517-130">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="18517-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="18517-131">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="18517-131">Vertex</span></span> | <span data-ttu-id="18517-132">Hülle</span><span class="sxs-lookup"><span data-stu-id="18517-132">Hull</span></span> | <span data-ttu-id="18517-133">Domain</span><span class="sxs-lookup"><span data-stu-id="18517-133">Domain</span></span> | <span data-ttu-id="18517-134">Geometrie</span><span class="sxs-lookup"><span data-stu-id="18517-134">Geometry</span></span> | <span data-ttu-id="18517-135">Pixel</span><span class="sxs-lookup"><span data-stu-id="18517-135">Pixel</span></span> | <span data-ttu-id="18517-136">Compute</span><span class="sxs-lookup"><span data-stu-id="18517-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="18517-137">X</span><span class="sxs-lookup"><span data-stu-id="18517-137">X</span></span>      | <span data-ttu-id="18517-138">X</span><span class="sxs-lookup"><span data-stu-id="18517-138">X</span></span>    | <span data-ttu-id="18517-139">X</span><span class="sxs-lookup"><span data-stu-id="18517-139">X</span></span>      | <span data-ttu-id="18517-140">X</span><span class="sxs-lookup"><span data-stu-id="18517-140">X</span></span>        | <span data-ttu-id="18517-141">X</span><span class="sxs-lookup"><span data-stu-id="18517-141">X</span></span>     | <span data-ttu-id="18517-142">X</span><span class="sxs-lookup"><span data-stu-id="18517-142">X</span></span>       |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="18517-143">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="18517-143">Minimum Shader Model</span></span>

<span data-ttu-id="18517-144">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="18517-144">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="18517-145">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="18517-145">Shader Model</span></span>                                              | <span data-ttu-id="18517-146">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="18517-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="18517-147">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="18517-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="18517-148">ja</span><span class="sxs-lookup"><span data-stu-id="18517-148">yes</span></span>       |
| [<span data-ttu-id="18517-149">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="18517-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="18517-150">nein</span><span class="sxs-lookup"><span data-stu-id="18517-150">no</span></span>        |
| [<span data-ttu-id="18517-151">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="18517-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="18517-152">nein</span><span class="sxs-lookup"><span data-stu-id="18517-152">no</span></span>        |
| [<span data-ttu-id="18517-153">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="18517-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="18517-154">nein</span><span class="sxs-lookup"><span data-stu-id="18517-154">no</span></span>        |
| [<span data-ttu-id="18517-155">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="18517-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="18517-156">nein</span><span class="sxs-lookup"><span data-stu-id="18517-156">no</span></span>        |
| [<span data-ttu-id="18517-157">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="18517-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="18517-158">nein</span><span class="sxs-lookup"><span data-stu-id="18517-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="18517-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="18517-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18517-160">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="18517-160">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





