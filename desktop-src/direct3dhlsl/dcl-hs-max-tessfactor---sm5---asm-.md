---
title: dcl_hs_max_tessfactor (SM5-ASM)
description: Deklarieren Sie den maxtess Factor für den Patch.
ms.assetid: 7EF0FD81-69FE-49F6-95DF-0C452A90A713
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69bd20fc8f4a3687988e8b100975f74016a45ae6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993246"
---
# <a name="dcl_hs_max_tessfactor-sm5---asm"></a><span data-ttu-id="5c131-103">DCL \_ HS \_ Max \_ Tess Factor (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="5c131-103">dcl\_hs\_max\_tessfactor (sm5 - asm)</span></span>

<span data-ttu-id="5c131-104">Deklarieren Sie den maxtess Factor für den Patch.</span><span class="sxs-lookup"><span data-stu-id="5c131-104">Declare the maxTessFactor for the patch.</span></span>



| <span data-ttu-id="5c131-105">DCL \_ HS \_ Max. Mosaik \_ Faktor n</span><span class="sxs-lookup"><span data-stu-id="5c131-105">dcl\_hs\_max\_tessfactor n</span></span> |
|----------------------------|



 



| <span data-ttu-id="5c131-106">Element</span><span class="sxs-lookup"><span data-stu-id="5c131-106">Item</span></span>                                                   | <span data-ttu-id="5c131-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c131-107">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="5c131-108"><span id="n"></span><span id="N"></span>*Nr*</span><span class="sxs-lookup"><span data-stu-id="5c131-108"><span id="n"></span><span id="N"></span>*n*</span></span><br/> | <span data-ttu-id="5c131-109">\[in \] maxtess Factor.</span><span class="sxs-lookup"><span data-stu-id="5c131-109">\[in\] The maxTessFactor.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5c131-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c131-110">Remarks</span></span>

<span data-ttu-id="5c131-111">Maxtess Factor ist ein float32-Wert im Bereich {1,0... 64,0}.</span><span class="sxs-lookup"><span data-stu-id="5c131-111">The maxTessFactor is a float32 value in the range {1.0 ... 64.0}.</span></span>

<span data-ttu-id="5c131-112">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="5c131-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5c131-113">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="5c131-113">Vertex</span></span> | <span data-ttu-id="5c131-114">Hülle</span><span class="sxs-lookup"><span data-stu-id="5c131-114">Hull</span></span> | <span data-ttu-id="5c131-115">Domain</span><span class="sxs-lookup"><span data-stu-id="5c131-115">Domain</span></span> | <span data-ttu-id="5c131-116">Geometrie</span><span class="sxs-lookup"><span data-stu-id="5c131-116">Geometry</span></span> | <span data-ttu-id="5c131-117">Pixel</span><span class="sxs-lookup"><span data-stu-id="5c131-117">Pixel</span></span> | <span data-ttu-id="5c131-118">Compute</span><span class="sxs-lookup"><span data-stu-id="5c131-118">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="5c131-119">X</span><span class="sxs-lookup"><span data-stu-id="5c131-119">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5c131-120">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="5c131-120">Minimum Shader Model</span></span>

<span data-ttu-id="5c131-121">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="5c131-121">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="5c131-122">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="5c131-122">Shader Model</span></span>                                              | <span data-ttu-id="5c131-123">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="5c131-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5c131-124">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="5c131-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5c131-125">ja</span><span class="sxs-lookup"><span data-stu-id="5c131-125">yes</span></span>       |
| [<span data-ttu-id="5c131-126">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="5c131-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5c131-127">nein</span><span class="sxs-lookup"><span data-stu-id="5c131-127">no</span></span>        |
| [<span data-ttu-id="5c131-128">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="5c131-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5c131-129">nein</span><span class="sxs-lookup"><span data-stu-id="5c131-129">no</span></span>        |
| [<span data-ttu-id="5c131-130">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5c131-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5c131-131">nein</span><span class="sxs-lookup"><span data-stu-id="5c131-131">no</span></span>        |
| [<span data-ttu-id="5c131-132">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5c131-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5c131-133">nein</span><span class="sxs-lookup"><span data-stu-id="5c131-133">no</span></span>        |
| [<span data-ttu-id="5c131-134">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5c131-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5c131-135">nein</span><span class="sxs-lookup"><span data-stu-id="5c131-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5c131-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5c131-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c131-137">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5c131-137">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





