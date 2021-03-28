---
title: hs_control_point_phase (SM5-ASM)
description: Startet die Steuerungspunkt Phase in einem Hull-Shader.
ms.assetid: 9CF26691-C04F-4728-8418-40F313ABBE4A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aba3f591fcd656e64609513dca7b9126496a86d6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038356"
---
# <a name="hs_control_point_phase-sm5---asm"></a><span data-ttu-id="97ad8-103">HS \_ \_ -Steuerungspunkt \_ Phase (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="97ad8-103">hs\_control\_point\_phase (sm5 - asm)</span></span>

<span data-ttu-id="97ad8-104">Startet die Steuerungspunkt Phase in einem Hull-Shader.</span><span class="sxs-lookup"><span data-stu-id="97ad8-104">Start the control point phase in a hull shader.</span></span>



| <span data-ttu-id="97ad8-105">HS- \_ Steuerungs \_ Punkt \_ Phase</span><span class="sxs-lookup"><span data-stu-id="97ad8-105">hs\_control\_point\_phase</span></span> |
|---------------------------|



 

## <a name="remarks"></a><span data-ttu-id="97ad8-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97ad8-106">Remarks</span></span>

<span data-ttu-id="97ad8-107">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="97ad8-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="97ad8-108">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="97ad8-108">Vertex</span></span> | <span data-ttu-id="97ad8-109">Hülle</span><span class="sxs-lookup"><span data-stu-id="97ad8-109">Hull</span></span> | <span data-ttu-id="97ad8-110">Domain</span><span class="sxs-lookup"><span data-stu-id="97ad8-110">Domain</span></span> | <span data-ttu-id="97ad8-111">Geometrie</span><span class="sxs-lookup"><span data-stu-id="97ad8-111">Geometry</span></span> | <span data-ttu-id="97ad8-112">Pixel</span><span class="sxs-lookup"><span data-stu-id="97ad8-112">Pixel</span></span> | <span data-ttu-id="97ad8-113">Compute</span><span class="sxs-lookup"><span data-stu-id="97ad8-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="97ad8-114">X</span><span class="sxs-lookup"><span data-stu-id="97ad8-114">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="97ad8-115">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="97ad8-115">Minimum Shader Model</span></span>

<span data-ttu-id="97ad8-116">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="97ad8-116">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="97ad8-117">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="97ad8-117">Shader Model</span></span>                                              | <span data-ttu-id="97ad8-118">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="97ad8-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="97ad8-119">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="97ad8-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="97ad8-120">ja</span><span class="sxs-lookup"><span data-stu-id="97ad8-120">yes</span></span>       |
| [<span data-ttu-id="97ad8-121">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="97ad8-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="97ad8-122">nein</span><span class="sxs-lookup"><span data-stu-id="97ad8-122">no</span></span>        |
| [<span data-ttu-id="97ad8-123">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="97ad8-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="97ad8-124">nein</span><span class="sxs-lookup"><span data-stu-id="97ad8-124">no</span></span>        |
| [<span data-ttu-id="97ad8-125">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="97ad8-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="97ad8-126">nein</span><span class="sxs-lookup"><span data-stu-id="97ad8-126">no</span></span>        |
| [<span data-ttu-id="97ad8-127">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="97ad8-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="97ad8-128">nein</span><span class="sxs-lookup"><span data-stu-id="97ad8-128">no</span></span>        |
| [<span data-ttu-id="97ad8-129">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="97ad8-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="97ad8-130">nein</span><span class="sxs-lookup"><span data-stu-id="97ad8-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="97ad8-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="97ad8-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97ad8-132">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="97ad8-132">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




