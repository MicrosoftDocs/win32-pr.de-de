---
title: dcl_hs_fork_phase_instance_count (SM5-ASM)
description: Deklarieren Sie die Instanzanzahl der Verzweigungs Phase in einer Hull-shaderphase.
ms.assetid: E38C48BB-3439-4F63-8DF8-21CF562CF5E6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3459b43c22f60699445f3ef05e5323e268eeb71
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389605"
---
# <a name="dcl_hs_fork_phase_instance_count-sm5---asm"></a><span data-ttu-id="cb4a3-103">Anzahl der DCL \_ HS \_ -Verzweigungs \_ Phasen \_ \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="cb4a3-103">dcl\_hs\_fork\_phase\_instance\_count (sm5 - asm)</span></span>

<span data-ttu-id="cb4a3-104">Deklarieren Sie die Instanzanzahl der Verzweigungs Phase in einer Hull-shaderphase.</span><span class="sxs-lookup"><span data-stu-id="cb4a3-104">Declare the fork phase instance count in a hull shader fork phase.</span></span>



| <span data-ttu-id="cb4a3-105">Anzahl der Instanzen der DCL \_ HS \_ -Verzweigungs \_ Phase \_ \_ {1... Max. 32-Bit-uint}</span><span class="sxs-lookup"><span data-stu-id="cb4a3-105">dcl\_hs\_fork\_phase\_instance\_count {1...max 32-bit UINT}</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="cb4a3-106">Element</span><span class="sxs-lookup"><span data-stu-id="cb4a3-106">Item</span></span>                                                   | <span data-ttu-id="cb4a3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb4a3-107">Description</span></span>                           |
|--------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="cb4a3-108"><span id="N"></span><span id="n"></span>*Nr*</span><span class="sxs-lookup"><span data-stu-id="cb4a3-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="cb4a3-109">\[in \] der Instanzanzahl.</span><span class="sxs-lookup"><span data-stu-id="cb4a3-109">\[in\] The instance count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cb4a3-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb4a3-110">Remarks</span></span>

<span data-ttu-id="cb4a3-111">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="cb4a3-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="cb4a3-112">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="cb4a3-112">Vertex</span></span> | <span data-ttu-id="cb4a3-113">Hülle</span><span class="sxs-lookup"><span data-stu-id="cb4a3-113">Hull</span></span> | <span data-ttu-id="cb4a3-114">Domain</span><span class="sxs-lookup"><span data-stu-id="cb4a3-114">Domain</span></span> | <span data-ttu-id="cb4a3-115">Geometrie</span><span class="sxs-lookup"><span data-stu-id="cb4a3-115">Geometry</span></span> | <span data-ttu-id="cb4a3-116">Pixel</span><span class="sxs-lookup"><span data-stu-id="cb4a3-116">Pixel</span></span> | <span data-ttu-id="cb4a3-117">Compute</span><span class="sxs-lookup"><span data-stu-id="cb4a3-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="cb4a3-118">X</span><span class="sxs-lookup"><span data-stu-id="cb4a3-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="cb4a3-119">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="cb4a3-119">Minimum Shader Model</span></span>

<span data-ttu-id="cb4a3-120">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="cb4a3-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="cb4a3-121">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="cb4a3-121">Shader Model</span></span>                                              | <span data-ttu-id="cb4a3-122">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="cb4a3-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="cb4a3-123">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="cb4a3-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="cb4a3-124">ja</span><span class="sxs-lookup"><span data-stu-id="cb4a3-124">yes</span></span>       |
| [<span data-ttu-id="cb4a3-125">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="cb4a3-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="cb4a3-126">nein</span><span class="sxs-lookup"><span data-stu-id="cb4a3-126">no</span></span>        |
| [<span data-ttu-id="cb4a3-127">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="cb4a3-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="cb4a3-128">nein</span><span class="sxs-lookup"><span data-stu-id="cb4a3-128">no</span></span>        |
| [<span data-ttu-id="cb4a3-129">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cb4a3-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="cb4a3-130">nein</span><span class="sxs-lookup"><span data-stu-id="cb4a3-130">no</span></span>        |
| [<span data-ttu-id="cb4a3-131">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cb4a3-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="cb4a3-132">nein</span><span class="sxs-lookup"><span data-stu-id="cb4a3-132">no</span></span>        |
| [<span data-ttu-id="cb4a3-133">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cb4a3-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="cb4a3-134">nein</span><span class="sxs-lookup"><span data-stu-id="cb4a3-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="cb4a3-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cb4a3-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb4a3-136">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cb4a3-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





