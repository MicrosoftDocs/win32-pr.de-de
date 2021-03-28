---
title: dcl_tgsm_raw (SM5-ASM)
description: Deklarieren Sie einen Verweis auf einen Bereich des freigegebenen Speicherplatzes, der für die Compute-Shader s-Thread Gruppe verfügbar ist.
ms.assetid: 8EA6931C-5B13-431F-A886-04F8C73CD22D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd20d8a0d8d2309b9b895a5cb5439877bb10d31a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719464"
---
# <a name="dcl_tgsm_raw-sm5---asm"></a><span data-ttu-id="5ede4-103">DCL \_ TGSM \_ RAW (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="5ede4-103">dcl\_tgsm\_raw (sm5 - asm)</span></span>

<span data-ttu-id="5ede4-104">Deklarieren Sie einen Verweis auf einen Bereich des freigegebenen Speicherplatzes, der für die Compute-Shader s-Thread Gruppe verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="5ede4-104">Declare a reference to a region of shared memory space available to the compute shader s thread group.</span></span>



| <span data-ttu-id="5ede4-105">DCL \_ TGSM \_ RAW g \# , byteCount</span><span class="sxs-lookup"><span data-stu-id="5ede4-105">dcl\_tgsm\_raw g\#, byteCount</span></span> |
|-------------------------------|



 



| <span data-ttu-id="5ede4-106">Element</span><span class="sxs-lookup"><span data-stu-id="5ede4-106">Item</span></span>                                                                                                       | <span data-ttu-id="5ede4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ede4-107">Description</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ede4-108"><span id="g_"></span><span id="G_"></span>*selbst\#*</span><span class="sxs-lookup"><span data-stu-id="5ede4-108"><span id="g_"></span><span id="G_"></span>*g\#*</span></span><br/>                                                 | <span data-ttu-id="5ede4-109">\[in \] einem Verweis auf einen Block der Größe *byteCount* des nicht typisierten freigegebenen Speichers.</span><span class="sxs-lookup"><span data-stu-id="5ede4-109">\[in\] A reference to a block of size *byteCount* of untyped shared memory.</span></span> <br/> |
| <span data-ttu-id="5ede4-110"><span id="byteCount"></span><span id="bytecount"></span><span id="BYTECOUNT"></span>*byteCount*</span><span class="sxs-lookup"><span data-stu-id="5ede4-110"><span id="byteCount"></span><span id="bytecount"></span><span id="BYTECOUNT"></span>*byteCount*</span></span><br/> | <span data-ttu-id="5ede4-111">\[in \] muss ein Vielfaches von 4 sein.</span><span class="sxs-lookup"><span data-stu-id="5ede4-111">\[in\] Must be a multiple of 4.</span></span> <br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="5ede4-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ede4-112">Remarks</span></span>

<span data-ttu-id="5ede4-113">Der Gesamtspeicher für alle g \# muss <= der pro Thread Gruppe verfügbare freigegebene Arbeitsspeicher (32 KB) sein.</span><span class="sxs-lookup"><span data-stu-id="5ede4-113">The total storage for all g\# must be <= the amount of shared memory available per thread group, which is 32kB.</span></span>

<span data-ttu-id="5ede4-114">In einem Extremfall können Sie 8192 Gesamt-g s deklarieren \# , jeweils mit einem *byteCount* von 4.</span><span class="sxs-lookup"><span data-stu-id="5ede4-114">In an extreme case, you can declare 8192 total g\# s, each with a *byteCount* of 4.</span></span>

<span data-ttu-id="5ede4-115">Im umgekehrten Extremfall können Sie ein einzelnes g \# mit einem *byteCount* von 32768 deklarieren.</span><span class="sxs-lookup"><span data-stu-id="5ede4-115">In the opposite extreme, you can declare a single g\# with a *byteCount* of 32768.</span></span>

> [!Note]  
> <span data-ttu-id="5ede4-116">CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen die [strukturierte DCL- \_ TGSM \_](dcl-tgsm-structured--sm5---asm-.md), aber nicht die **DCL- \_ TGSM- \_ Rohdaten**.</span><span class="sxs-lookup"><span data-stu-id="5ede4-116">cs\_4\_0 and cs\_4\_1 supports [dcl\_tgsm\_structured](dcl-tgsm-structured--sm5---asm-.md), but not **dcl\_tgsm\_raw**.</span></span>

 

<span data-ttu-id="5ede4-117">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="5ede4-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5ede4-118">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="5ede4-118">Vertex</span></span> | <span data-ttu-id="5ede4-119">Hülle</span><span class="sxs-lookup"><span data-stu-id="5ede4-119">Hull</span></span> | <span data-ttu-id="5ede4-120">Domain</span><span class="sxs-lookup"><span data-stu-id="5ede4-120">Domain</span></span> | <span data-ttu-id="5ede4-121">Geometrie</span><span class="sxs-lookup"><span data-stu-id="5ede4-121">Geometry</span></span> | <span data-ttu-id="5ede4-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="5ede4-122">Pixel</span></span> | <span data-ttu-id="5ede4-123">Compute</span><span class="sxs-lookup"><span data-stu-id="5ede4-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="5ede4-124">X</span><span class="sxs-lookup"><span data-stu-id="5ede4-124">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5ede4-125">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="5ede4-125">Minimum Shader Model</span></span>

<span data-ttu-id="5ede4-126">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="5ede4-126">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="5ede4-127">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="5ede4-127">Shader Model</span></span>                                              | <span data-ttu-id="5ede4-128">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="5ede4-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5ede4-129">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="5ede4-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5ede4-130">ja</span><span class="sxs-lookup"><span data-stu-id="5ede4-130">yes</span></span>       |
| [<span data-ttu-id="5ede4-131">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="5ede4-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5ede4-132">nein</span><span class="sxs-lookup"><span data-stu-id="5ede4-132">no</span></span>        |
| [<span data-ttu-id="5ede4-133">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="5ede4-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5ede4-134">nein</span><span class="sxs-lookup"><span data-stu-id="5ede4-134">no</span></span>        |
| [<span data-ttu-id="5ede4-135">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5ede4-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5ede4-136">nein</span><span class="sxs-lookup"><span data-stu-id="5ede4-136">no</span></span>        |
| [<span data-ttu-id="5ede4-137">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5ede4-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5ede4-138">nein</span><span class="sxs-lookup"><span data-stu-id="5ede4-138">no</span></span>        |
| [<span data-ttu-id="5ede4-139">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5ede4-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5ede4-140">nein</span><span class="sxs-lookup"><span data-stu-id="5ede4-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5ede4-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5ede4-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ede4-142">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5ede4-142">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





