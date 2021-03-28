---
title: dcl_input voutputcontrolpointid (SM5-ASM)
description: Deklarieren Sie die ID des Ausgabe Steuerungs Punkts in einer Hull-Shader-Steuerungspunkt Phase.
ms.assetid: 376ECA4F-DD71-4466-8A9D-E92A536832BC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cee49a8a825f25b0fbbccff027d5ad1b9ade514
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038374"
---
# <a name="dcl_input-voutputcontrolpointid-sm5---asm"></a><span data-ttu-id="d5d80-103">DCL- \_ Eingabe voutputcontrolpointid (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="d5d80-103">dcl\_input vOutputControlPointID (sm5 - asm)</span></span>

<span data-ttu-id="d5d80-104">Deklarieren Sie die ID des Ausgabe Steuerungs Punkts in einer Hull-Shader-Steuerungspunkt Phase.</span><span class="sxs-lookup"><span data-stu-id="d5d80-104">Declare the output control point ID in a hull shader control point phase.</span></span>



| <span data-ttu-id="d5d80-105">DCL- \_ Eingabe voutputcontrolpointid</span><span class="sxs-lookup"><span data-stu-id="d5d80-105">dcl\_input vOutputControlPointID</span></span> |
|----------------------------------|



 



| <span data-ttu-id="d5d80-106">Element</span><span class="sxs-lookup"><span data-stu-id="d5d80-106">Item</span></span>                                                                                                                                                       | <span data-ttu-id="d5d80-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5d80-107">Description</span></span>                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="d5d80-108"><span id="vOutputControlPointID"></span><span id="voutputcontrolpointid"></span><span id="VOUTPUTCONTROLPOINTID"></span>*voutputcontrolpointid*</span><span class="sxs-lookup"><span data-stu-id="d5d80-108"><span id="vOutputControlPointID"></span><span id="voutputcontrolpointid"></span><span id="VOUTPUTCONTROLPOINTID"></span>*vOutputControlPointID*</span></span><br/> | <span data-ttu-id="d5d80-109">\[in \] der Ausgabe Steuerungspunkt-ID.</span><span class="sxs-lookup"><span data-stu-id="d5d80-109">\[in\] The output control point ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d5d80-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5d80-110">Remarks</span></span>

<span data-ttu-id="d5d80-111">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="d5d80-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d5d80-112">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="d5d80-112">Vertex</span></span> | <span data-ttu-id="d5d80-113">Hülle</span><span class="sxs-lookup"><span data-stu-id="d5d80-113">Hull</span></span> | <span data-ttu-id="d5d80-114">Domain</span><span class="sxs-lookup"><span data-stu-id="d5d80-114">Domain</span></span> | <span data-ttu-id="d5d80-115">Geometrie</span><span class="sxs-lookup"><span data-stu-id="d5d80-115">Geometry</span></span> | <span data-ttu-id="d5d80-116">Pixel</span><span class="sxs-lookup"><span data-stu-id="d5d80-116">Pixel</span></span> | <span data-ttu-id="d5d80-117">Compute</span><span class="sxs-lookup"><span data-stu-id="d5d80-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="d5d80-118">X</span><span class="sxs-lookup"><span data-stu-id="d5d80-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d5d80-119">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="d5d80-119">Minimum Shader Model</span></span>

<span data-ttu-id="d5d80-120">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="d5d80-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="d5d80-121">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="d5d80-121">Shader Model</span></span>                                              | <span data-ttu-id="d5d80-122">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="d5d80-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d5d80-123">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="d5d80-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d5d80-124">ja</span><span class="sxs-lookup"><span data-stu-id="d5d80-124">yes</span></span>       |
| [<span data-ttu-id="d5d80-125">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="d5d80-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d5d80-126">nein</span><span class="sxs-lookup"><span data-stu-id="d5d80-126">no</span></span>        |
| [<span data-ttu-id="d5d80-127">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="d5d80-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d5d80-128">nein</span><span class="sxs-lookup"><span data-stu-id="d5d80-128">no</span></span>        |
| [<span data-ttu-id="d5d80-129">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5d80-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d5d80-130">nein</span><span class="sxs-lookup"><span data-stu-id="d5d80-130">no</span></span>        |
| [<span data-ttu-id="d5d80-131">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5d80-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d5d80-132">nein</span><span class="sxs-lookup"><span data-stu-id="d5d80-132">no</span></span>        |
| [<span data-ttu-id="d5d80-133">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5d80-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d5d80-134">nein</span><span class="sxs-lookup"><span data-stu-id="d5d80-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d5d80-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d5d80-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5d80-136">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5d80-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





