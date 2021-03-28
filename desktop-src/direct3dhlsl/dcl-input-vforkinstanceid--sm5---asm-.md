---
title: dcl_input vforkinstanceid (SM5-ASM)
description: Deklarieren Sie die Instanz-ID in einer Hull-Shader-Verzweigungs Phase.
ms.assetid: AA73E8B6-C6D7-4483-B46E-C733341F552C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ce5fcf111a59abb0c9a6ccb36de63d94dcb11e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038375"
---
# <a name="dcl_input-vforkinstanceid-sm5---asm"></a><span data-ttu-id="7356f-103">DCL \_ -Eingabe vforkinstanceid (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="7356f-103">dcl\_input vForkInstanceID (sm5 - asm)</span></span>

<span data-ttu-id="7356f-104">Deklarieren Sie die Instanz-ID in einer Hull-Shader-Verzweigungs Phase.</span><span class="sxs-lookup"><span data-stu-id="7356f-104">Declare the instance ID in a hull shader fork phase.</span></span>



| <span data-ttu-id="7356f-105">DCL \_ -Eingabe vforkinstanceid</span><span class="sxs-lookup"><span data-stu-id="7356f-105">dcl\_input vForkInstanceID</span></span> |
|----------------------------|



 



| <span data-ttu-id="7356f-106">Element</span><span class="sxs-lookup"><span data-stu-id="7356f-106">Item</span></span>                                                                                                                               | <span data-ttu-id="7356f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7356f-107">Description</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span data-ttu-id="7356f-108"><span id="vForkInstanceID"></span><span id="vforkinstanceid"></span><span id="VFORKINSTANCEID"></span>*vforkinstanceid*</span><span class="sxs-lookup"><span data-stu-id="7356f-108"><span id="vForkInstanceID"></span><span id="vforkinstanceid"></span><span id="VFORKINSTANCEID"></span>*vForkInstanceID*</span></span><br/> | <span data-ttu-id="7356f-109">\[in \] der Instanz-ID.</span><span class="sxs-lookup"><span data-stu-id="7356f-109">\[in\] The instance ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7356f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7356f-110">Remarks</span></span>

<span data-ttu-id="7356f-111">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="7356f-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7356f-112">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="7356f-112">Vertex</span></span> | <span data-ttu-id="7356f-113">Hülle</span><span class="sxs-lookup"><span data-stu-id="7356f-113">Hull</span></span> | <span data-ttu-id="7356f-114">Domain</span><span class="sxs-lookup"><span data-stu-id="7356f-114">Domain</span></span> | <span data-ttu-id="7356f-115">Geometrie</span><span class="sxs-lookup"><span data-stu-id="7356f-115">Geometry</span></span> | <span data-ttu-id="7356f-116">Pixel</span><span class="sxs-lookup"><span data-stu-id="7356f-116">Pixel</span></span> | <span data-ttu-id="7356f-117">Compute</span><span class="sxs-lookup"><span data-stu-id="7356f-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="7356f-118">X</span><span class="sxs-lookup"><span data-stu-id="7356f-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7356f-119">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="7356f-119">Minimum Shader Model</span></span>

<span data-ttu-id="7356f-120">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="7356f-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="7356f-121">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="7356f-121">Shader Model</span></span>                                              | <span data-ttu-id="7356f-122">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="7356f-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7356f-123">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="7356f-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7356f-124">ja</span><span class="sxs-lookup"><span data-stu-id="7356f-124">yes</span></span>       |
| [<span data-ttu-id="7356f-125">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="7356f-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7356f-126">nein</span><span class="sxs-lookup"><span data-stu-id="7356f-126">no</span></span>        |
| [<span data-ttu-id="7356f-127">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="7356f-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7356f-128">nein</span><span class="sxs-lookup"><span data-stu-id="7356f-128">no</span></span>        |
| [<span data-ttu-id="7356f-129">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7356f-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7356f-130">nein</span><span class="sxs-lookup"><span data-stu-id="7356f-130">no</span></span>        |
| [<span data-ttu-id="7356f-131">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7356f-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7356f-132">nein</span><span class="sxs-lookup"><span data-stu-id="7356f-132">no</span></span>        |
| [<span data-ttu-id="7356f-133">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7356f-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7356f-134">nein</span><span class="sxs-lookup"><span data-stu-id="7356f-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7356f-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7356f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7356f-136">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7356f-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





