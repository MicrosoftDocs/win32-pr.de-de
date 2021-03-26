---
title: dcl_tgsm_structured (SM5-ASM)
description: Deklarieren Sie einen Verweis auf einen Bereich des freigegebenen Speicherplatzes, der für die Compute-Shader s-Thread Gruppe verfügbar ist. Der Arbeitsspeicher wird als Array von-Strukturen angezeigt.
ms.assetid: C42CD506-58EB-4740-8403-3F9BF29F0CAE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a639d31c4449a0dfeb152c06b35cfb86c5cc30a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993039"
---
# <a name="dcl_tgsm_structured-sm5---asm"></a><span data-ttu-id="1601c-104">DCL \_ TGSM \_ strukturiert (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="1601c-104">dcl\_tgsm\_structured (sm5 - asm)</span></span>

<span data-ttu-id="1601c-105">Deklarieren Sie einen Verweis auf einen Bereich des freigegebenen Speicherplatzes, der für die Compute-Shader s-Thread Gruppe verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="1601c-105">Declare a reference to a region of shared memory space available to the compute shader s thread group.</span></span> <span data-ttu-id="1601c-106">Der Arbeitsspeicher wird als Array von-Strukturen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1601c-106">The memory is viewed as an array of structures.</span></span>



| <span data-ttu-id="1601c-107">DCL \_ TGSM \_ strukturiert g \# , structbytestride, structcount</span><span class="sxs-lookup"><span data-stu-id="1601c-107">dcl\_tgsm\_structured g\#, structByteStride, structCount</span></span> |
|----------------------------------------------------------|



 



| <span data-ttu-id="1601c-108">Element</span><span class="sxs-lookup"><span data-stu-id="1601c-108">Item</span></span>                                                                                                                                   | <span data-ttu-id="1601c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1601c-109">Description</span></span>                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1601c-110"><span id="g_"></span><span id="G_"></span>*selbst\#*</span><span class="sxs-lookup"><span data-stu-id="1601c-110"><span id="g_"></span><span id="G_"></span>*g\#*</span></span><br/>                                                                             | <span data-ttu-id="1601c-111">\[in \] einem Verweis auf einen Block mit gemeinsam genutzter Arbeitsspeicher Größe von *structbytestride* \* *structcount* bytes.</span><span class="sxs-lookup"><span data-stu-id="1601c-111">\[in\] A reference to a block of shared memory of size *structByteStride* \* *structCount* bytes.</span></span> <br/> |
| <span data-ttu-id="1601c-112"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structbytestride*</span><span class="sxs-lookup"><span data-stu-id="1601c-112"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span></span><br/> | <span data-ttu-id="1601c-113">\[in \] der Struktur Stride.</span><span class="sxs-lookup"><span data-stu-id="1601c-113">\[in\] The structure stride.</span></span> <span data-ttu-id="1601c-114">Dieser Wert ist ein uint in Bytes und muss ein Vielfaches von 4 sein.</span><span class="sxs-lookup"><span data-stu-id="1601c-114">This value is a uint in bytes and must be a multiple of 4.</span></span> <br/>           |
| <span data-ttu-id="1601c-115"><span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*structcount*</span><span class="sxs-lookup"><span data-stu-id="1601c-115"><span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*structCount*</span></span><br/>                     | <span data-ttu-id="1601c-116">\[in \] der Anzahl der Strukturen.</span><span class="sxs-lookup"><span data-stu-id="1601c-116">\[in\] The number of structures.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="1601c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1601c-117">Remarks</span></span>

<span data-ttu-id="1601c-118">Der gesamte Speicherplatz für "g" \# muss <= der Menge an gemeinsam genutzter verfügbarem Arbeitsspeicher pro Thread Gruppe, 32 KB oder 8192 32-Bit-Skaren.</span><span class="sxs-lookup"><span data-stu-id="1601c-118">The total storage for all g\# must be <= the amount of shared memory available per thread group, which is 32kB, or 8192 32-bit scalars.</span></span>

<span data-ttu-id="1601c-119">In einem Extremfall können Sie 8192 Gesamt-g s deklarieren \# , wenn beide einen *structbytestride* von 4 und einen *structcount* -Wert von 1 haben.</span><span class="sxs-lookup"><span data-stu-id="1601c-119">In an extreme case, you can declare 8192 total g\# s, if each has a *structByteStride* of 4 and a *structCount* of 1.</span></span>

<span data-ttu-id="1601c-120">Im umgekehrten Extremfall können Sie ein einzelnes g \# mit einem Struktur-Stride von 32 KB und einer Struktur Anzahl von 1 deklarieren.</span><span class="sxs-lookup"><span data-stu-id="1601c-120">In the opposite extreme, you can declare a single g\# with a structure stride of 32kB and a structure count of 1.</span></span>

<span data-ttu-id="1601c-121">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="1601c-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1601c-122">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="1601c-122">Vertex</span></span> | <span data-ttu-id="1601c-123">Hülle</span><span class="sxs-lookup"><span data-stu-id="1601c-123">Hull</span></span> | <span data-ttu-id="1601c-124">Domain</span><span class="sxs-lookup"><span data-stu-id="1601c-124">Domain</span></span> | <span data-ttu-id="1601c-125">Geometrie</span><span class="sxs-lookup"><span data-stu-id="1601c-125">Geometry</span></span> | <span data-ttu-id="1601c-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="1601c-126">Pixel</span></span> | <span data-ttu-id="1601c-127">Compute</span><span class="sxs-lookup"><span data-stu-id="1601c-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="1601c-128">X</span><span class="sxs-lookup"><span data-stu-id="1601c-128">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1601c-129">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="1601c-129">Minimum Shader Model</span></span>

<span data-ttu-id="1601c-130">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="1601c-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="1601c-131">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="1601c-131">Shader Model</span></span>                                              | <span data-ttu-id="1601c-132">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="1601c-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1601c-133">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="1601c-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1601c-134">ja</span><span class="sxs-lookup"><span data-stu-id="1601c-134">yes</span></span>       |
| [<span data-ttu-id="1601c-135">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="1601c-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1601c-136">nein</span><span class="sxs-lookup"><span data-stu-id="1601c-136">no</span></span>        |
| [<span data-ttu-id="1601c-137">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="1601c-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1601c-138">nein</span><span class="sxs-lookup"><span data-stu-id="1601c-138">no</span></span>        |
| [<span data-ttu-id="1601c-139">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1601c-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1601c-140">nein</span><span class="sxs-lookup"><span data-stu-id="1601c-140">no</span></span>        |
| [<span data-ttu-id="1601c-141">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1601c-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1601c-142">nein</span><span class="sxs-lookup"><span data-stu-id="1601c-142">no</span></span>        |
| [<span data-ttu-id="1601c-143">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1601c-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1601c-144">nein</span><span class="sxs-lookup"><span data-stu-id="1601c-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1601c-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1601c-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1601c-146">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1601c-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





