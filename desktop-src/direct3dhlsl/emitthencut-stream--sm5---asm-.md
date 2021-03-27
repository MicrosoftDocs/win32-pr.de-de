---
title: emitThenCut_stream (SM5-ASM)
description: Entspricht einem Ausgabe Befehl gefolgt von einem Befehl zum Ausschneiden. | emitThenCut_stream (SM5-ASM)
ms.assetid: E9D84647-E29B-4E31-9E95-9F7A173293D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae3129f2a3fb50664a5dbf070c7a1dae9bf5d6e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981209"
---
# <a name="emitthencut_stream-sm5---asm"></a><span data-ttu-id="fd846-104">emitthenausschneide Daten \_ Strom (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="fd846-104">emitThenCut\_stream (sm5 - asm)</span></span>

<span data-ttu-id="fd846-105">Entspricht einem Ausgabe [Befehl gefolgt von einem Befehl zum](emit--sm4---asm-.md) [Ausschneiden](cut--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="fd846-105">Equivalent to an [emit](emit--sm4---asm-.md) command followed by a [cut](cut--sm4---asm-.md) command.</span></span>



| <span data-ttu-id="fd846-106">emitthencut \_ Stream streamindex</span><span class="sxs-lookup"><span data-stu-id="fd846-106">emitThenCut\_stream streamIndex</span></span> |
|---------------------------------|



 



| <span data-ttu-id="fd846-107">Element</span><span class="sxs-lookup"><span data-stu-id="fd846-107">Item</span></span>                                                                                                               | <span data-ttu-id="fd846-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd846-108">Description</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="fd846-109"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span><span class="sxs-lookup"><span data-stu-id="fd846-109"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span></span><br/> | <span data-ttu-id="fd846-110">\[im \] Stream-Index.</span><span class="sxs-lookup"><span data-stu-id="fd846-110">\[in\] The stream index.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fd846-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd846-111">Remarks</span></span>

<span data-ttu-id="fd846-112">Dieser Vorgang ist nützlich, wenn der letzte Scheitelpunkt in einer Topologie wissentlich ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fd846-112">This operation is useful when knowingly outputting the last vertex in a topology.</span></span>

<span data-ttu-id="fd846-113">Wenn Streams nicht deklariert wurden, müssen Sie [emitthencut](emitthencut--sm4---asm-.md) anstelle des **emitthencut- \_ Streams** verwenden.</span><span class="sxs-lookup"><span data-stu-id="fd846-113">If streams have not been declared, then you must use [emitThenCut](emitthencut--sm4---asm-.md) instead of **emitThenCut\_stream**.</span></span>

<span data-ttu-id="fd846-114">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="fd846-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="fd846-115">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="fd846-115">Vertex</span></span> | <span data-ttu-id="fd846-116">Hülle</span><span class="sxs-lookup"><span data-stu-id="fd846-116">Hull</span></span> | <span data-ttu-id="fd846-117">Domain</span><span class="sxs-lookup"><span data-stu-id="fd846-117">Domain</span></span> | <span data-ttu-id="fd846-118">Geometrie</span><span class="sxs-lookup"><span data-stu-id="fd846-118">Geometry</span></span> | <span data-ttu-id="fd846-119">Pixel</span><span class="sxs-lookup"><span data-stu-id="fd846-119">Pixel</span></span> | <span data-ttu-id="fd846-120">Compute</span><span class="sxs-lookup"><span data-stu-id="fd846-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="fd846-121">X</span><span class="sxs-lookup"><span data-stu-id="fd846-121">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fd846-122">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="fd846-122">Minimum Shader Model</span></span>

<span data-ttu-id="fd846-123">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="fd846-123">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="fd846-124">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="fd846-124">Shader Model</span></span>                                              | <span data-ttu-id="fd846-125">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="fd846-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fd846-126">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="fd846-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fd846-127">ja</span><span class="sxs-lookup"><span data-stu-id="fd846-127">yes</span></span>       |
| [<span data-ttu-id="fd846-128">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="fd846-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fd846-129">nein</span><span class="sxs-lookup"><span data-stu-id="fd846-129">no</span></span>        |
| [<span data-ttu-id="fd846-130">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="fd846-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fd846-131">nein</span><span class="sxs-lookup"><span data-stu-id="fd846-131">no</span></span>        |
| [<span data-ttu-id="fd846-132">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fd846-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fd846-133">nein</span><span class="sxs-lookup"><span data-stu-id="fd846-133">no</span></span>        |
| [<span data-ttu-id="fd846-134">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fd846-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fd846-135">nein</span><span class="sxs-lookup"><span data-stu-id="fd846-135">no</span></span>        |
| [<span data-ttu-id="fd846-136">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fd846-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fd846-137">nein</span><span class="sxs-lookup"><span data-stu-id="fd846-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fd846-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fd846-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd846-139">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fd846-139">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





