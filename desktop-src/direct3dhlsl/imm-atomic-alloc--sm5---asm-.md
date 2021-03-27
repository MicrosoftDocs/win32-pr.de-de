---
title: imm_atomic_alloc (SM5-ASM)
description: Inkremente Sie den ausgeblendeten 32-Bit-Leistungs Zähler atomisch, der mit einer Anzahl oder angefügt ist, und fügen Sie den ursprünglichen Wert zurück.
ms.assetid: 534FA3C3-6FAC-41DC-AC07-0E53FEED000C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a97709629497bae9af0298789453ef1d1172b7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719427"
---
# <a name="imm_atomic_alloc-sm5---asm"></a><span data-ttu-id="dbc24-103">imm \_ Atomic- \_ Zuweisung (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="dbc24-103">imm\_atomic\_alloc (sm5 - asm)</span></span>

<span data-ttu-id="dbc24-104">Inkremente Sie den ausgeblendeten 32-Bit-Leistungs Zähler atomisch, der mit einer Anzahl oder angefügt ist, und fügen Sie den ursprünglichen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="dbc24-104">Atomically increment the hidden 32-bit counter stored with a Count or Append unordered access view (UAV), returning the original value.</span></span>



| <span data-ttu-id="dbc24-105">imm \_ Atomic- \_ Zuweisung dst0 \[ . \_ einzelkomponentenmaske \_ \] , dstuav</span><span class="sxs-lookup"><span data-stu-id="dbc24-105">imm\_atomic\_alloc dst0\[.single\_component\_mask\], dstUAV</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="dbc24-106">Element</span><span class="sxs-lookup"><span data-stu-id="dbc24-106">Item</span></span>                                                                                           | <span data-ttu-id="dbc24-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dbc24-107">Description</span></span>                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="dbc24-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="dbc24-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                | <span data-ttu-id="dbc24-109">\[in \] enthält den zurückgegebenen Leistungs Zählers.</span><span class="sxs-lookup"><span data-stu-id="dbc24-109">\[in\] Contains the returned counter value.</span></span><br/>                    |
| <span data-ttu-id="dbc24-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstuav*</span><span class="sxs-lookup"><span data-stu-id="dbc24-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="dbc24-111">\[in \] einem strukturierten Puffer-UAV mit dem count-oder Append-Flag.</span><span class="sxs-lookup"><span data-stu-id="dbc24-111">\[in\] A Structured Buffer UAV with the Count or Append flag.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="dbc24-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dbc24-112">Remarks</span></span>

<span data-ttu-id="dbc24-113">Es ist ein ausgeblendeter ganzzahliger 32-Bit-Zählerwert ohne Vorzeichen zugeordnet, der mit jeder Anzahl oder angefügten Puffer Ansicht verknüpft ist, die initialisiert wird, wenn die Sicht an die Pipeline gebunden ist, einschließlich der Option, den vorherigen Wert beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="dbc24-113">There is a hidden unsigned 32-bit integer counter value associated with each Count or Append Buffer view which is initialized when the view is bound to the pipeline, including the option to keep the previous value.</span></span>

<span data-ttu-id="dbc24-114">Diese Anweisung führt eine atomarische Inkrement des Leistungs Zählers durch und gibt den ursprünglichen an *dst0* zurück.</span><span class="sxs-lookup"><span data-stu-id="dbc24-114">This instruction does an atomic increment of the counter value, returning the original to *dst0*.</span></span>

<span data-ttu-id="dbc24-115">Bei einer Append-UAV ist der zurückgegebene Wert nur für die Dauer des Shader-Aufrufe gültig.</span><span class="sxs-lookup"><span data-stu-id="dbc24-115">For an Append UAV, the returned value is only valid for the duration of the shader invocation.</span></span> <span data-ttu-id="dbc24-116">Danach kann die Implementierung das Speicher Layout neu anordnen.</span><span class="sxs-lookup"><span data-stu-id="dbc24-116">after that the implementation may rearrange the memory layout.</span></span> <span data-ttu-id="dbc24-117">Alle Speicher Adressierung, die auf dem zurückgegebenen Wert basiert, muss auf den Shader-Aufruf beschränkt sein.</span><span class="sxs-lookup"><span data-stu-id="dbc24-117">Any memory addressing based on the returned value must be limited to the shader invocation.</span></span>

<span data-ttu-id="dbc24-118">Bei einer Append-UAV kann der HLSL-Compiler im Shader-Aufruf den zurückgegebenen Wert als Struktur Index verwenden, der für den Zugriff auf den strukturierten Puffer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dbc24-118">For an Append UAV, within the shader invocation the HLSL compiler can use the returned value as the struct index to use for accessing the structured buffer.</span></span> <span data-ttu-id="dbc24-119">Der Zugriff auf einen anderen Struktur Index als jene, die von Aufrufen an die Definition von " [ \_](imm-atomic-consume--sm5---asm-.md) **imm \_ Atomic \_** " oder "using" zurückgegeben werden, führt dazu, dass der Zugriff auf die Speicherorte innerhalb der UAV zufällig erfolgt und nur für die Lebensdauer des shaderaufruders festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="dbc24-119">Accessing any struct index other than those locations returned by call(s) to **imm\_atomic\_alloc** or [\_consume](imm-atomic-consume--sm5---asm-.md) produce undefined results in that exactly which memory location within the UAV is being accessed is random and only fixed for the lifetime of the shader invocation.</span></span>

<span data-ttu-id="dbc24-120">Bei einer UAV-Anzahl kann der zurückgegebene Wert von der Anwendung als Verweis auf einen festgelegten Speicherort innerhalb der UAV gespeichert werden, der nach dem Aufruf des Shader aussagekräftig ist.</span><span class="sxs-lookup"><span data-stu-id="dbc24-120">For a Count UAV, the returned value can be saved by the application as a reference to a fixed location within the UAV that is meaningful after the shader invocation is over.</span></span> <span data-ttu-id="dbc24-121">Auf jeden Speicherort in der Anzahl der UAV kann immer unabhängig von der Anzahl des Werts zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="dbc24-121">Any location in a Count UAV may always be accessed independent of what the count value is.</span></span>

<span data-ttu-id="dbc24-122">Es gibt keine Klammer für die Anzahl, sodass Sie bei einem Überlauf umbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="dbc24-122">There is no clamping of the count, so it wraps on overflow.</span></span>

<span data-ttu-id="dbc24-123">Der gleiche Shader kann nicht gleichzeitig sowohl einen " **imm \_ Atomic- \_ Zuweisungen** " als auch einen " **imm Atomic"- \_ \_ Verbrauch** auf derselben UAV</span><span class="sxs-lookup"><span data-stu-id="dbc24-123">The same shader cannot attempt both **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span> <span data-ttu-id="dbc24-124">Darüber hinaus kann die GPU nicht mehrere shaderaufrufe zulassen, um die Verwendung von " **imm \_ Atomic \_ zugc** " und " **imm \_ Atomic \_** " in derselben UAV zu mischen.</span><span class="sxs-lookup"><span data-stu-id="dbc24-124">Further, the GPU cannot allow multiple shader invocations to mix **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span>

<span data-ttu-id="dbc24-125">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="dbc24-125">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="dbc24-126">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="dbc24-126">Vertex</span></span> | <span data-ttu-id="dbc24-127">Hülle</span><span class="sxs-lookup"><span data-stu-id="dbc24-127">Hull</span></span> | <span data-ttu-id="dbc24-128">Domain</span><span class="sxs-lookup"><span data-stu-id="dbc24-128">Domain</span></span> | <span data-ttu-id="dbc24-129">Geometrie</span><span class="sxs-lookup"><span data-stu-id="dbc24-129">Geometry</span></span> | <span data-ttu-id="dbc24-130">Pixel</span><span class="sxs-lookup"><span data-stu-id="dbc24-130">Pixel</span></span> | <span data-ttu-id="dbc24-131">Compute</span><span class="sxs-lookup"><span data-stu-id="dbc24-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="dbc24-132">X</span><span class="sxs-lookup"><span data-stu-id="dbc24-132">X</span></span>     | <span data-ttu-id="dbc24-133">X</span><span class="sxs-lookup"><span data-stu-id="dbc24-133">X</span></span>       |



 

<span data-ttu-id="dbc24-134">Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="dbc24-134">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="dbc24-135">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="dbc24-135">Vertex</span></span> | <span data-ttu-id="dbc24-136">Hülle</span><span class="sxs-lookup"><span data-stu-id="dbc24-136">Hull</span></span> | <span data-ttu-id="dbc24-137">Domain</span><span class="sxs-lookup"><span data-stu-id="dbc24-137">Domain</span></span> | <span data-ttu-id="dbc24-138">Geometrie</span><span class="sxs-lookup"><span data-stu-id="dbc24-138">Geometry</span></span> | <span data-ttu-id="dbc24-139">Pixel</span><span class="sxs-lookup"><span data-stu-id="dbc24-139">Pixel</span></span> | <span data-ttu-id="dbc24-140">Compute</span><span class="sxs-lookup"><span data-stu-id="dbc24-140">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="dbc24-141">X</span><span class="sxs-lookup"><span data-stu-id="dbc24-141">X</span></span>      | <span data-ttu-id="dbc24-142">X</span><span class="sxs-lookup"><span data-stu-id="dbc24-142">X</span></span>    | <span data-ttu-id="dbc24-143">X</span><span class="sxs-lookup"><span data-stu-id="dbc24-143">X</span></span>      | <span data-ttu-id="dbc24-144">X</span><span class="sxs-lookup"><span data-stu-id="dbc24-144">X</span></span>        | <span data-ttu-id="dbc24-145">X</span><span class="sxs-lookup"><span data-stu-id="dbc24-145">X</span></span>     | <span data-ttu-id="dbc24-146">X</span><span class="sxs-lookup"><span data-stu-id="dbc24-146">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="dbc24-147">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="dbc24-147">Minimum Shader Model</span></span>

<span data-ttu-id="dbc24-148">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="dbc24-148">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="dbc24-149">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="dbc24-149">Shader Model</span></span>                                              | <span data-ttu-id="dbc24-150">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="dbc24-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="dbc24-151">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="dbc24-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="dbc24-152">ja</span><span class="sxs-lookup"><span data-stu-id="dbc24-152">yes</span></span>       |
| [<span data-ttu-id="dbc24-153">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="dbc24-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="dbc24-154">nein</span><span class="sxs-lookup"><span data-stu-id="dbc24-154">no</span></span>        |
| [<span data-ttu-id="dbc24-155">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="dbc24-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="dbc24-156">nein</span><span class="sxs-lookup"><span data-stu-id="dbc24-156">no</span></span>        |
| [<span data-ttu-id="dbc24-157">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dbc24-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="dbc24-158">nein</span><span class="sxs-lookup"><span data-stu-id="dbc24-158">no</span></span>        |
| [<span data-ttu-id="dbc24-159">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dbc24-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="dbc24-160">nein</span><span class="sxs-lookup"><span data-stu-id="dbc24-160">no</span></span>        |
| [<span data-ttu-id="dbc24-161">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dbc24-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="dbc24-162">nein</span><span class="sxs-lookup"><span data-stu-id="dbc24-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="dbc24-163">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dbc24-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbc24-164">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dbc24-164">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





