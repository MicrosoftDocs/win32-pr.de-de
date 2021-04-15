---
title: imm_atomic_consume (SM5-ASM)
description: Verringert den ausgeblendeten 32-Bit-Leistungs Zähler atomisch, der mit einer Anzahl oder angefügenter Zugriffs Ansicht (UAV) gespeichert wird, und gibt den neuen Wert zurück.
ms.assetid: 1115C318-2F86-4161-AC5C-2A61A262DC28
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1c6fe01ddb92b2ce870b16254f75c52cadd341
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993127"
---
# <a name="imm_atomic_consume-sm5---asm"></a><span data-ttu-id="88c1a-103">imm \_ Atomic \_ -Verbrauch (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="88c1a-103">imm\_atomic\_consume (sm5 - asm)</span></span>

<span data-ttu-id="88c1a-104">Verringert den ausgeblendeten 32-Bit-Leistungs Zähler atomisch, der mit einer Anzahl oder angefügenter Zugriffs Ansicht (UAV) gespeichert wird, und gibt den neuen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="88c1a-104">Atomically decrement the hidden 32-bit counter stored with a Count or Append unordered access view (UAV), returning the new value.</span></span>



| <span data-ttu-id="88c1a-105">"imm \_ Atomic" \_ dst0 \[ . \_ einzelkomponentenmaske \_ \] , dstuav</span><span class="sxs-lookup"><span data-stu-id="88c1a-105">imm\_atomic\_consume dst0\[.single\_component\_mask\], dstUAV</span></span> |
|---------------------------------------------------------------|



 



| <span data-ttu-id="88c1a-106">Element</span><span class="sxs-lookup"><span data-stu-id="88c1a-106">Item</span></span>                                                                                           | <span data-ttu-id="88c1a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="88c1a-107">Description</span></span>                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="88c1a-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="88c1a-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                | <span data-ttu-id="88c1a-109">\[in \] enthält den zurückgegebenen ursprünglichen Leistungs Zählers.</span><span class="sxs-lookup"><span data-stu-id="88c1a-109">\[in\] Contains the returned original counter value.</span></span><br/>           |
| <span data-ttu-id="88c1a-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstuav*</span><span class="sxs-lookup"><span data-stu-id="88c1a-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="88c1a-111">\[in \] einem strukturierten Puffer-UAV mit dem count-oder Append-Flag.</span><span class="sxs-lookup"><span data-stu-id="88c1a-111">\[in\] A structured buffer UAV with the Count or Append flag.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="88c1a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88c1a-112">Remarks</span></span>

<span data-ttu-id="88c1a-113">Eine Erläuterung zur Gültigkeit des zurückgegebenen zählungs Werts finden Sie unter " [imm \_ Atomic \_ zuordnungszahl](imm-atomic-alloc--sm5---asm-.md) ", je nachdem, ob die UAV "count" oder "append" ist</span><span class="sxs-lookup"><span data-stu-id="88c1a-113">See [imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) for a discussion about the validity of the returned count value depending on whether the UAV is Count or Append.</span></span> <span data-ttu-id="88c1a-114">Das gleiche gilt für **den \_ atomischen Atomic- \_ Verbrauch**.</span><span class="sxs-lookup"><span data-stu-id="88c1a-114">The same applies for **imm\_atomic\_consume**.</span></span>

<span data-ttu-id="88c1a-115">der unteilbare Wert für " **imm \_ Atomic \_** " führt einen atomaren Dekrement des Leistungs Zählers durch und gibt den neuen Wert an *dst0* zurück.</span><span class="sxs-lookup"><span data-stu-id="88c1a-115">**imm\_atomic\_consume** does an atomic decrement of the counter value, returning the new value to *dst0*.</span></span>

<span data-ttu-id="88c1a-116">Es gibt keine Klammer für die Anzahl, daher wird Sie bei einem Unterlauf umschlossen.</span><span class="sxs-lookup"><span data-stu-id="88c1a-116">There is no clamping of the count, so it wraps on underflow.</span></span>

<span data-ttu-id="88c1a-117">Der gleiche Shader kann nicht gleichzeitig sowohl einen " **imm \_ Atomic- \_ Zuweisungen** " als auch einen " **imm Atomic"- \_ \_ Verbrauch** auf derselben UAV</span><span class="sxs-lookup"><span data-stu-id="88c1a-117">The same shader cannot attempt both **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span> <span data-ttu-id="88c1a-118">Darüber hinaus kann die GPU nicht mehrere shaderaufrufe zulassen, um die Verwendung von " **imm \_ Atomic \_ zugc** " und " **imm \_ Atomic \_** " in derselben UAV zu mischen.</span><span class="sxs-lookup"><span data-stu-id="88c1a-118">Further, the GPU cannot allow multiple shader invocations to mix **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span>

<span data-ttu-id="88c1a-119">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="88c1a-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="88c1a-120">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="88c1a-120">Vertex</span></span> | <span data-ttu-id="88c1a-121">Hülle</span><span class="sxs-lookup"><span data-stu-id="88c1a-121">Hull</span></span> | <span data-ttu-id="88c1a-122">Domain</span><span class="sxs-lookup"><span data-stu-id="88c1a-122">Domain</span></span> | <span data-ttu-id="88c1a-123">Geometrie</span><span class="sxs-lookup"><span data-stu-id="88c1a-123">Geometry</span></span> | <span data-ttu-id="88c1a-124">Pixel</span><span class="sxs-lookup"><span data-stu-id="88c1a-124">Pixel</span></span> | <span data-ttu-id="88c1a-125">Compute</span><span class="sxs-lookup"><span data-stu-id="88c1a-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="88c1a-126">X</span><span class="sxs-lookup"><span data-stu-id="88c1a-126">X</span></span>     | <span data-ttu-id="88c1a-127">X</span><span class="sxs-lookup"><span data-stu-id="88c1a-127">X</span></span>       |



 

<span data-ttu-id="88c1a-128">Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="88c1a-128">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="88c1a-129">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="88c1a-129">Vertex</span></span> | <span data-ttu-id="88c1a-130">Hülle</span><span class="sxs-lookup"><span data-stu-id="88c1a-130">Hull</span></span> | <span data-ttu-id="88c1a-131">Domain</span><span class="sxs-lookup"><span data-stu-id="88c1a-131">Domain</span></span> | <span data-ttu-id="88c1a-132">Geometrie</span><span class="sxs-lookup"><span data-stu-id="88c1a-132">Geometry</span></span> | <span data-ttu-id="88c1a-133">Pixel</span><span class="sxs-lookup"><span data-stu-id="88c1a-133">Pixel</span></span> | <span data-ttu-id="88c1a-134">Compute</span><span class="sxs-lookup"><span data-stu-id="88c1a-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="88c1a-135">X</span><span class="sxs-lookup"><span data-stu-id="88c1a-135">X</span></span>      | <span data-ttu-id="88c1a-136">X</span><span class="sxs-lookup"><span data-stu-id="88c1a-136">X</span></span>    | <span data-ttu-id="88c1a-137">X</span><span class="sxs-lookup"><span data-stu-id="88c1a-137">X</span></span>      | <span data-ttu-id="88c1a-138">X</span><span class="sxs-lookup"><span data-stu-id="88c1a-138">X</span></span>        | <span data-ttu-id="88c1a-139">X</span><span class="sxs-lookup"><span data-stu-id="88c1a-139">X</span></span>     | <span data-ttu-id="88c1a-140">X</span><span class="sxs-lookup"><span data-stu-id="88c1a-140">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="88c1a-141">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="88c1a-141">Minimum Shader Model</span></span>

<span data-ttu-id="88c1a-142">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="88c1a-142">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="88c1a-143">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="88c1a-143">Shader Model</span></span>                                              | <span data-ttu-id="88c1a-144">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="88c1a-144">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="88c1a-145">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="88c1a-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="88c1a-146">ja</span><span class="sxs-lookup"><span data-stu-id="88c1a-146">yes</span></span>       |
| [<span data-ttu-id="88c1a-147">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="88c1a-147">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="88c1a-148">nein</span><span class="sxs-lookup"><span data-stu-id="88c1a-148">no</span></span>        |
| [<span data-ttu-id="88c1a-149">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="88c1a-149">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="88c1a-150">nein</span><span class="sxs-lookup"><span data-stu-id="88c1a-150">no</span></span>        |
| [<span data-ttu-id="88c1a-151">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="88c1a-151">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="88c1a-152">nein</span><span class="sxs-lookup"><span data-stu-id="88c1a-152">no</span></span>        |
| [<span data-ttu-id="88c1a-153">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="88c1a-153">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="88c1a-154">nein</span><span class="sxs-lookup"><span data-stu-id="88c1a-154">no</span></span>        |
| [<span data-ttu-id="88c1a-155">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="88c1a-155">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="88c1a-156">nein</span><span class="sxs-lookup"><span data-stu-id="88c1a-156">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="88c1a-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="88c1a-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88c1a-158">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="88c1a-158">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





