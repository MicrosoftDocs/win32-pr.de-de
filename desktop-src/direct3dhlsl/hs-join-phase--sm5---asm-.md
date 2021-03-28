---
title: hs_join_phase (SM5-ASM)
description: Startet die joinphase in einem Hull-Shader.
ms.assetid: C53889BE-B65F-4F5F-8B87-7C5263FAC800
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54c45011209124d73fe866872772a3a787c538d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313710"
---
# <a name="hs_join_phase-sm5---asm"></a><span data-ttu-id="d6f29-103">HS \_ \_ -joinphase (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="d6f29-103">hs\_join\_phase (sm5 - asm)</span></span>

<span data-ttu-id="d6f29-104">Startet die joinphase in einem Hull-Shader.</span><span class="sxs-lookup"><span data-stu-id="d6f29-104">Start the join phase in a hull shader.</span></span>



| <span data-ttu-id="d6f29-105">HS- \_ Beitritts \_ Phase</span><span class="sxs-lookup"><span data-stu-id="d6f29-105">hs\_join\_phase</span></span> |
|-----------------|



 

## <a name="remarks"></a><span data-ttu-id="d6f29-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6f29-106">Remarks</span></span>

<span data-ttu-id="d6f29-107">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="d6f29-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d6f29-108">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="d6f29-108">Vertex</span></span> | <span data-ttu-id="d6f29-109">Hülle</span><span class="sxs-lookup"><span data-stu-id="d6f29-109">Hull</span></span> | <span data-ttu-id="d6f29-110">Domain</span><span class="sxs-lookup"><span data-stu-id="d6f29-110">Domain</span></span> | <span data-ttu-id="d6f29-111">Geometrie</span><span class="sxs-lookup"><span data-stu-id="d6f29-111">Geometry</span></span> | <span data-ttu-id="d6f29-112">Pixel</span><span class="sxs-lookup"><span data-stu-id="d6f29-112">Pixel</span></span> | <span data-ttu-id="d6f29-113">Compute</span><span class="sxs-lookup"><span data-stu-id="d6f29-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="d6f29-114">X</span><span class="sxs-lookup"><span data-stu-id="d6f29-114">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d6f29-115">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="d6f29-115">Minimum Shader Model</span></span>

<span data-ttu-id="d6f29-116">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="d6f29-116">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="d6f29-117">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="d6f29-117">Shader Model</span></span>                                              | <span data-ttu-id="d6f29-118">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="d6f29-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d6f29-119">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="d6f29-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d6f29-120">ja</span><span class="sxs-lookup"><span data-stu-id="d6f29-120">yes</span></span>       |
| [<span data-ttu-id="d6f29-121">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="d6f29-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d6f29-122">nein</span><span class="sxs-lookup"><span data-stu-id="d6f29-122">no</span></span>        |
| [<span data-ttu-id="d6f29-123">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="d6f29-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d6f29-124">nein</span><span class="sxs-lookup"><span data-stu-id="d6f29-124">no</span></span>        |
| [<span data-ttu-id="d6f29-125">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d6f29-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d6f29-126">nein</span><span class="sxs-lookup"><span data-stu-id="d6f29-126">no</span></span>        |
| [<span data-ttu-id="d6f29-127">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d6f29-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d6f29-128">nein</span><span class="sxs-lookup"><span data-stu-id="d6f29-128">no</span></span>        |
| [<span data-ttu-id="d6f29-129">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d6f29-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d6f29-130">nein</span><span class="sxs-lookup"><span data-stu-id="d6f29-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d6f29-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d6f29-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6f29-132">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d6f29-132">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




