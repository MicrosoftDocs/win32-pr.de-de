---
title: dcl_thread_group (SM5-ASM)
description: Thread Gruppengröße deklarieren.
ms.assetid: CB8192C4-100D-49B6-94E7-6CD3AEC28149
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8141c80e82f1dfd1ae5a4d360d04fac32ba5221
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038360"
---
# <a name="dcl_thread_group-sm5---asm"></a><span data-ttu-id="8e8b1-103">DCL \_ \_ -Thread Gruppe (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="8e8b1-103">dcl\_thread\_group (sm5 - asm)</span></span>

<span data-ttu-id="8e8b1-104">Thread Gruppengröße deklarieren.</span><span class="sxs-lookup"><span data-stu-id="8e8b1-104">Declare thread group size.</span></span>



| <span data-ttu-id="8e8b1-105">DCL- \_ Thread \_ Gruppe x, y, z</span><span class="sxs-lookup"><span data-stu-id="8e8b1-105">dcl\_thread\_group x, y, z</span></span> |
|----------------------------|



 



| <span data-ttu-id="8e8b1-106">Element</span><span class="sxs-lookup"><span data-stu-id="8e8b1-106">Item</span></span>                                                   | <span data-ttu-id="8e8b1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e8b1-107">Description</span></span>                                                        |
|--------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="8e8b1-108"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="8e8b1-108"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="8e8b1-109">\[in \] einer 32-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="8e8b1-109">\[in\] An usigned 32-bit integer.</span></span> <span data-ttu-id="8e8b1-110">1 <= x <= 1024</span><span class="sxs-lookup"><span data-stu-id="8e8b1-110">1 <= x <= 1024</span></span> <br/> |
| <span data-ttu-id="8e8b1-111"><span id="y"></span><span id="Y"></span>*Teenie*</span><span class="sxs-lookup"><span data-stu-id="8e8b1-111"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="8e8b1-112">\[in \] einer 32-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="8e8b1-112">\[in\] An usigned 32-bit integer.</span></span> <span data-ttu-id="8e8b1-113">1 <= y <= 1024</span><span class="sxs-lookup"><span data-stu-id="8e8b1-113">1 <= y <= 1024</span></span><br/>  |
| <span data-ttu-id="8e8b1-114"><span id="z"></span><span id="Z"></span>*z*</span><span class="sxs-lookup"><span data-stu-id="8e8b1-114"><span id="z"></span><span id="Z"></span>*z*</span></span><br/> | <span data-ttu-id="8e8b1-115">\[in \] einer 32-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="8e8b1-115">\[in\] An usigned 32-bit integer.</span></span> <span data-ttu-id="8e8b1-116">1 <= z <= 64</span><span class="sxs-lookup"><span data-stu-id="8e8b1-116">1 <= z <= 64</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="8e8b1-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e8b1-117">Remarks</span></span>

<span data-ttu-id="8e8b1-118">x \* y \* z <= 1024</span><span class="sxs-lookup"><span data-stu-id="8e8b1-118">x\*y\*z <= 1024</span></span>

<span data-ttu-id="8e8b1-119">Diese Thread Gruppen Deklaration muss einmal in einem Compute-Shader vorkommen.</span><span class="sxs-lookup"><span data-stu-id="8e8b1-119">This thread group declaration must appear once in a compute shader.</span></span>

<span data-ttu-id="8e8b1-120">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="8e8b1-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8e8b1-121">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="8e8b1-121">Vertex</span></span> | <span data-ttu-id="8e8b1-122">Hülle</span><span class="sxs-lookup"><span data-stu-id="8e8b1-122">Hull</span></span> | <span data-ttu-id="8e8b1-123">Domain</span><span class="sxs-lookup"><span data-stu-id="8e8b1-123">Domain</span></span> | <span data-ttu-id="8e8b1-124">Geometrie</span><span class="sxs-lookup"><span data-stu-id="8e8b1-124">Geometry</span></span> | <span data-ttu-id="8e8b1-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="8e8b1-125">Pixel</span></span> | <span data-ttu-id="8e8b1-126">Compute</span><span class="sxs-lookup"><span data-stu-id="8e8b1-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="8e8b1-127">X</span><span class="sxs-lookup"><span data-stu-id="8e8b1-127">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8e8b1-128">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="8e8b1-128">Minimum Shader Model</span></span>

<span data-ttu-id="8e8b1-129">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="8e8b1-129">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="8e8b1-130">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="8e8b1-130">Shader Model</span></span>                                              | <span data-ttu-id="8e8b1-131">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="8e8b1-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8e8b1-132">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="8e8b1-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8e8b1-133">ja</span><span class="sxs-lookup"><span data-stu-id="8e8b1-133">yes</span></span>       |
| [<span data-ttu-id="8e8b1-134">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="8e8b1-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8e8b1-135">nein</span><span class="sxs-lookup"><span data-stu-id="8e8b1-135">no</span></span>        |
| [<span data-ttu-id="8e8b1-136">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="8e8b1-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8e8b1-137">nein</span><span class="sxs-lookup"><span data-stu-id="8e8b1-137">no</span></span>        |
| [<span data-ttu-id="8e8b1-138">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8e8b1-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8e8b1-139">nein</span><span class="sxs-lookup"><span data-stu-id="8e8b1-139">no</span></span>        |
| [<span data-ttu-id="8e8b1-140">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8e8b1-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8e8b1-141">nein</span><span class="sxs-lookup"><span data-stu-id="8e8b1-141">no</span></span>        |
| [<span data-ttu-id="8e8b1-142">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8e8b1-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8e8b1-143">nein</span><span class="sxs-lookup"><span data-stu-id="8e8b1-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8e8b1-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8e8b1-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e8b1-145">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8e8b1-145">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





