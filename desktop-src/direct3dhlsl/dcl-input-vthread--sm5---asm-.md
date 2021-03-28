---
title: dcl_input vthread (SM5-ASM)
description: Deklarieren Sie Compute-Shadereingabe-IDs.
ms.assetid: C041863A-32B0-4588-A1A9-E416AF9B723C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf6a7bb19feef95eae9cc153911407b206fde16
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719482"
---
# <a name="dcl_input-vthread-sm5---asm"></a><span data-ttu-id="11f7d-103">DCL \_ -Eingabe-vthread (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="11f7d-103">dcl\_input vThread (sm5 - asm)</span></span>

<span data-ttu-id="11f7d-104">Deklarieren Sie Compute-Shadereingabe-IDs.</span><span class="sxs-lookup"><span data-stu-id="11f7d-104">Declare compute shader input IDs.</span></span>



| <span data-ttu-id="11f7d-105">DCL- \_ Eingabe {vThreadID.XYZ </span><span class="sxs-lookup"><span data-stu-id="11f7d-105">dcl\_input {vThreadID.xyz</span></span>\|<span data-ttu-id="11f7d-106">vThreadGroupID.XYZ </span><span class="sxs-lookup"><span data-stu-id="11f7d-106">vThreadGroupID.xyz</span></span>\| <span data-ttu-id="11f7d-107">vThreadIDInGroup.XYZ </span><span class="sxs-lookup"><span data-stu-id="11f7d-107">vThreadIDInGroup.xyz</span></span>\|<span data-ttu-id="11f7d-108">vthreadidingroupflatchten}</span><span class="sxs-lookup"><span data-stu-id="11f7d-108">vThreadIDInGroupFlattened}</span></span> |
|--------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="11f7d-109">Element</span><span class="sxs-lookup"><span data-stu-id="11f7d-109">Item</span></span>                                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="11f7d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11f7d-110">Description</span></span>                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="11f7d-111"><span id="vThreadID___vThreadGroupID___vThreadIDInGroup___vThreadIDInGroupFlattened"></span><span id="vthreadid___vthreadgroupid___vthreadidingroup___vthreadidingroupflattened"></span><span id="VTHREADID___VTHREADGROUPID___VTHREADIDINGROUP___VTHREADIDINGROUPFLATTENED"></span>*vthreadid \| vthreadgroupid \| vthreadidingroup \| vthreadidingroupflatchten*</span><span class="sxs-lookup"><span data-stu-id="11f7d-111"><span id="vThreadID___vThreadGroupID___vThreadIDInGroup___vThreadIDInGroupFlattened"></span><span id="vthreadid___vthreadgroupid___vthreadidingroup___vthreadidingroupflattened"></span><span id="VTHREADID___VTHREADGROUPID___VTHREADIDINGROUP___VTHREADIDINGROUPFLATTENED"></span>*vThreadID \| vThreadGroupID \| vThreadIDInGroup \| vThreadIDInGroupFlattened*</span></span><br/> | <span data-ttu-id="11f7d-112">\[im \] 32-Bit-Ganzzahl-ID-Wert ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="11f7d-112">\[in\] The 3-component unsigned 32-bit integer ID value.</span></span><br/> |



 

<span data-ttu-id="11f7d-113">die **DCL- \_ Eingabe** ist eine vorhandene Deklaration in anderen Shader-Stufen.</span><span class="sxs-lookup"><span data-stu-id="11f7d-113">**dcl\_input** is an existing declaration in other shader stages.</span></span> <span data-ttu-id="11f7d-114">Es wird im COMPUTE-Shader verwendet, um die verschiedenen ganzzahligen, ganzzahligen 32-Bit-ID-Werte mit drei Komponenten für den Compute-Shader zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="11f7d-114">It is used in the compute shader to declare the various 3-component unsigned 32-bit integer ID values unique to the compute shader.</span></span> <span data-ttu-id="11f7d-115">Sie lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="11f7d-115">They are:</span></span>

-   <span data-ttu-id="11f7d-116">vThreadID.xyz</span><span class="sxs-lookup"><span data-stu-id="11f7d-116">vThreadID.xyz</span></span>
-   <span data-ttu-id="11f7d-117">vGroupID.xyz</span><span class="sxs-lookup"><span data-stu-id="11f7d-117">vGroupID.xyz</span></span>
-   <span data-ttu-id="11f7d-118">vThreadIDInGroup.xyz</span><span class="sxs-lookup"><span data-stu-id="11f7d-118">vThreadIDInGroup.xyz</span></span>
-   <span data-ttu-id="11f7d-119">vthreadidingroupflatchten (einzelne Komponente)</span><span class="sxs-lookup"><span data-stu-id="11f7d-119">vThreadIDInGroupFlattened (single component)</span></span>

<span data-ttu-id="11f7d-120">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="11f7d-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="11f7d-121">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="11f7d-121">Vertex</span></span> | <span data-ttu-id="11f7d-122">Hülle</span><span class="sxs-lookup"><span data-stu-id="11f7d-122">Hull</span></span> | <span data-ttu-id="11f7d-123">Domain</span><span class="sxs-lookup"><span data-stu-id="11f7d-123">Domain</span></span> | <span data-ttu-id="11f7d-124">Geometrie</span><span class="sxs-lookup"><span data-stu-id="11f7d-124">Geometry</span></span> | <span data-ttu-id="11f7d-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="11f7d-125">Pixel</span></span> | <span data-ttu-id="11f7d-126">Compute</span><span class="sxs-lookup"><span data-stu-id="11f7d-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="11f7d-127">X</span><span class="sxs-lookup"><span data-stu-id="11f7d-127">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="11f7d-128">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="11f7d-128">Minimum Shader Model</span></span>

<span data-ttu-id="11f7d-129">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="11f7d-129">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="11f7d-130">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="11f7d-130">Shader Model</span></span>                                              | <span data-ttu-id="11f7d-131">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="11f7d-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="11f7d-132">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="11f7d-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="11f7d-133">ja</span><span class="sxs-lookup"><span data-stu-id="11f7d-133">yes</span></span>       |
| [<span data-ttu-id="11f7d-134">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="11f7d-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="11f7d-135">nein</span><span class="sxs-lookup"><span data-stu-id="11f7d-135">no</span></span>        |
| [<span data-ttu-id="11f7d-136">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="11f7d-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="11f7d-137">nein</span><span class="sxs-lookup"><span data-stu-id="11f7d-137">no</span></span>        |
| [<span data-ttu-id="11f7d-138">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="11f7d-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="11f7d-139">nein</span><span class="sxs-lookup"><span data-stu-id="11f7d-139">no</span></span>        |
| [<span data-ttu-id="11f7d-140">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="11f7d-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="11f7d-141">nein</span><span class="sxs-lookup"><span data-stu-id="11f7d-141">no</span></span>        |
| [<span data-ttu-id="11f7d-142">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="11f7d-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="11f7d-143">nein</span><span class="sxs-lookup"><span data-stu-id="11f7d-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="11f7d-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="11f7d-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11f7d-145">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="11f7d-145">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





