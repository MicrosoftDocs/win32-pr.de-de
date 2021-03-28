---
title: dcl_stream (SM5-ASM)
description: Deklarieren eines Geometry-shaderausgabestreams.
ms.assetid: 0A8B8AB5-B7B0-46BB-91E8-B2E8E3D64B74
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f46903c3257c280788e91c25700743a23c146fe
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389593"
---
# <a name="dcl_stream-sm5---asm"></a><span data-ttu-id="c7f18-103">DCL \_ -Stream (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="c7f18-103">dcl\_stream (sm5 - asm)</span></span>

<span data-ttu-id="c7f18-104">Deklarieren eines Geometry-shaderausgabestreams.</span><span class="sxs-lookup"><span data-stu-id="c7f18-104">Declare a geometry shader output stream.</span></span>



| <span data-ttu-id="c7f18-105">DCL- \_ Stream m\#</span><span class="sxs-lookup"><span data-stu-id="c7f18-105">dcl\_stream m\#</span></span> |
|-----------------|



 



| <span data-ttu-id="c7f18-106">Element</span><span class="sxs-lookup"><span data-stu-id="c7f18-106">Item</span></span>                                                       | <span data-ttu-id="c7f18-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7f18-107">Description</span></span>                             |
|------------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="c7f18-108"><span id="m_"></span><span id="M_"></span>*800\#*</span><span class="sxs-lookup"><span data-stu-id="c7f18-108"><span id="m_"></span><span id="M_"></span>*m\#*</span></span><br/> | <span data-ttu-id="c7f18-109">\[in \] Stream 0.. 3 (M0... m3).</span><span class="sxs-lookup"><span data-stu-id="c7f18-109">\[in\] Stream 0..3 (m0..m3).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c7f18-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7f18-110">Remarks</span></span>

<span data-ttu-id="c7f18-111">Ein angegebener Datenstrom kann nur einmal deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="c7f18-111">A given stream can only be declared once.</span></span>

<span data-ttu-id="c7f18-112">Wenn keine Streams deklariert werden, wird angenommen, dass die Deklarationen der Ausgabe-und Ausgabe Topologie für Stream 0 gelten.</span><span class="sxs-lookup"><span data-stu-id="c7f18-112">If no streams are declared, output and output topology declarations are assumed to be for stream 0.</span></span>

<span data-ttu-id="c7f18-113">Der erste **DCL- \_ Stream** darf nicht nach einer **DCL- \_ Ausgabe** oder **DCL \_ outputtopology** -Anweisungen stehen.</span><span class="sxs-lookup"><span data-stu-id="c7f18-113">The first **dcl\_stream** cannot appear after any **dcl\_output** or **dcl\_outputTopology** statements.</span></span>

<span data-ttu-id="c7f18-114">Alle **DCL \_** -Ausgaben oder **DCL \_ outputtoplogie** -Anweisungen nach jeder **DCL \_ Stream** m- \# Anweisung definieren die Ausgaben für Stream m \# .</span><span class="sxs-lookup"><span data-stu-id="c7f18-114">Any **dcl\_output** or **dcl\_outputToplogy** statements after any **dcl\_stream** m\# statement define the outputs for stream m\#.</span></span>

<span data-ttu-id="c7f18-115">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="c7f18-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c7f18-116">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="c7f18-116">Vertex</span></span> | <span data-ttu-id="c7f18-117">Hülle</span><span class="sxs-lookup"><span data-stu-id="c7f18-117">Hull</span></span> | <span data-ttu-id="c7f18-118">Domain</span><span class="sxs-lookup"><span data-stu-id="c7f18-118">Domain</span></span> | <span data-ttu-id="c7f18-119">Geometrie</span><span class="sxs-lookup"><span data-stu-id="c7f18-119">Geometry</span></span> | <span data-ttu-id="c7f18-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="c7f18-120">Pixel</span></span> | <span data-ttu-id="c7f18-121">Compute</span><span class="sxs-lookup"><span data-stu-id="c7f18-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="c7f18-122">X</span><span class="sxs-lookup"><span data-stu-id="c7f18-122">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c7f18-123">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="c7f18-123">Minimum Shader Model</span></span>

<span data-ttu-id="c7f18-124">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c7f18-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c7f18-125">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="c7f18-125">Shader Model</span></span>                                              | <span data-ttu-id="c7f18-126">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="c7f18-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c7f18-127">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="c7f18-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c7f18-128">ja</span><span class="sxs-lookup"><span data-stu-id="c7f18-128">yes</span></span>       |
| [<span data-ttu-id="c7f18-129">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="c7f18-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c7f18-130">nein</span><span class="sxs-lookup"><span data-stu-id="c7f18-130">no</span></span>        |
| [<span data-ttu-id="c7f18-131">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="c7f18-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c7f18-132">nein</span><span class="sxs-lookup"><span data-stu-id="c7f18-132">no</span></span>        |
| [<span data-ttu-id="c7f18-133">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7f18-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c7f18-134">nein</span><span class="sxs-lookup"><span data-stu-id="c7f18-134">no</span></span>        |
| [<span data-ttu-id="c7f18-135">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7f18-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c7f18-136">nein</span><span class="sxs-lookup"><span data-stu-id="c7f18-136">no</span></span>        |
| [<span data-ttu-id="c7f18-137">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7f18-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c7f18-138">nein</span><span class="sxs-lookup"><span data-stu-id="c7f18-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c7f18-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c7f18-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7f18-140">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7f18-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





