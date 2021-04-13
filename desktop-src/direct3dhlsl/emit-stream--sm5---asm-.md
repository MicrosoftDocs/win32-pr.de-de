---
title: emit_stream (SM5-ASM)
description: Gibt einen Scheitelpunkt für einen angegebenen Stream aus.
ms.assetid: 5DBB0BEC-6EA4-4C04-A3D2-853E48260226
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f56c2582453d18120e3e95b27af9c7613728fa62
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389525"
---
# <a name="emit_stream-sm5---asm"></a><span data-ttu-id="db042-103">\_Ausgabestream (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="db042-103">emit\_stream (sm5 - asm)</span></span>

<span data-ttu-id="db042-104">Gibt einen Scheitelpunkt für einen angegebenen Stream aus.</span><span class="sxs-lookup"><span data-stu-id="db042-104">Emit a vertex to a given stream.</span></span>



| <span data-ttu-id="db042-105">\_Stream streamindex ausgeben</span><span class="sxs-lookup"><span data-stu-id="db042-105">emit\_stream streamIndex</span></span> |
|--------------------------|



 



| <span data-ttu-id="db042-106">Element</span><span class="sxs-lookup"><span data-stu-id="db042-106">Item</span></span>                                                                                                               | <span data-ttu-id="db042-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db042-107">Description</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="db042-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span><span class="sxs-lookup"><span data-stu-id="db042-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span></span><br/> | <span data-ttu-id="db042-109">\[im \] Stream-Index.</span><span class="sxs-lookup"><span data-stu-id="db042-109">\[in\] The stream index.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="db042-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db042-110">Remarks</span></span>

<span data-ttu-id="db042-111">Diese Anweisung bewirkt, dass alle deklarierten o- \# Register für den angegebenen Stream aus dem Geometry-Shader gelesen werden, um einen Scheitelpunkt zu generieren.</span><span class="sxs-lookup"><span data-stu-id="db042-111">This instruction causes all declared o\# registers for the given stream to be read out of the geometry shader to generate a vertex.</span></span> <span data-ttu-id="db042-112">Die Ausgabe gibt an, dass alle Daten in allen Ausgabe Registern für alle Streams nicht initialisiert werden, nicht nur der Stream, der an ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="db042-112">Afer the emit, all data in all output registers for all streams become uninitialized, not just the stream emitted to.</span></span>

<span data-ttu-id="db042-113">*streamindex* muss ein unmittelbarer Wert \[ von 0.. 3 \] für einen deklarierten Stream sein.</span><span class="sxs-lookup"><span data-stu-id="db042-113">*streamIndex* must be an immediate value \[0..3\] for a declared stream.</span></span>

<span data-ttu-id="db042-114">Wenn mehrere **\_ ausgabestreamaufrufe** ausgegeben werden, werden primitive generiert.</span><span class="sxs-lookup"><span data-stu-id="db042-114">As multiple **emit\_stream** calls are issued, primitives are generated.</span></span>

### <a name="restrictions"></a><span data-ttu-id="db042-115">Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="db042-115">Restrictions</span></span>

-   <span data-ttu-id="db042-116">**der \_ Ausgabestream** kann beliebig oft in einem Geometry-Shader vorkommen, einschließlich innerhalb der Fluss Steuerung.</span><span class="sxs-lookup"><span data-stu-id="db042-116">**emit\_stream** can appear any number of times in a geometry shader, including within flow control.</span></span>
-   <span data-ttu-id="db042-117">Wenn Streams nicht deklariert wurden, müssen Sie die [Ausgabe anstelle des](emit--sm4---asm-.md) Ausgabestreams verwenden. **\_**</span><span class="sxs-lookup"><span data-stu-id="db042-117">If streams have not been declared, then you must use [emit](emit--sm4---asm-.md) instead of **emit\_stream**.</span></span>

<span data-ttu-id="db042-118">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="db042-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="db042-119">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="db042-119">Vertex</span></span> | <span data-ttu-id="db042-120">Hülle</span><span class="sxs-lookup"><span data-stu-id="db042-120">Hull</span></span> | <span data-ttu-id="db042-121">Domain</span><span class="sxs-lookup"><span data-stu-id="db042-121">Domain</span></span> | <span data-ttu-id="db042-122">Geometrie</span><span class="sxs-lookup"><span data-stu-id="db042-122">Geometry</span></span> | <span data-ttu-id="db042-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="db042-123">Pixel</span></span> | <span data-ttu-id="db042-124">Compute</span><span class="sxs-lookup"><span data-stu-id="db042-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="db042-125">X</span><span class="sxs-lookup"><span data-stu-id="db042-125">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="db042-126">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="db042-126">Minimum Shader Model</span></span>

<span data-ttu-id="db042-127">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="db042-127">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="db042-128">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="db042-128">Shader Model</span></span>                                              | <span data-ttu-id="db042-129">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="db042-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="db042-130">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="db042-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="db042-131">ja</span><span class="sxs-lookup"><span data-stu-id="db042-131">yes</span></span>       |
| [<span data-ttu-id="db042-132">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="db042-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="db042-133">nein</span><span class="sxs-lookup"><span data-stu-id="db042-133">no</span></span>        |
| [<span data-ttu-id="db042-134">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="db042-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="db042-135">nein</span><span class="sxs-lookup"><span data-stu-id="db042-135">no</span></span>        |
| [<span data-ttu-id="db042-136">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db042-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="db042-137">nein</span><span class="sxs-lookup"><span data-stu-id="db042-137">no</span></span>        |
| [<span data-ttu-id="db042-138">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db042-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="db042-139">nein</span><span class="sxs-lookup"><span data-stu-id="db042-139">no</span></span>        |
| [<span data-ttu-id="db042-140">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db042-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="db042-141">nein</span><span class="sxs-lookup"><span data-stu-id="db042-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="db042-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="db042-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db042-143">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db042-143">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





