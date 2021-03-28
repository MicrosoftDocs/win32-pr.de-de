---
title: dcl_hs_join_phase_instance_count (SM5-ASM)
description: Deklarieren Sie die Anzahl der joinphasen-Instanzen in einer Hull-Shader-joinphase.
ms.assetid: 9951B849-0537-4D08-9ADE-8CF6FF51A193
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34c3acc7074170ab4561a54e67668698d58b7ac1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389606"
---
# <a name="dcl_hs_join_phase_instance_count-sm5---asm"></a><span data-ttu-id="f8962-103">Anzahl der DCL \_ HS \_ \_ -joinphasen \_ Instanzen \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="f8962-103">dcl\_hs\_join\_phase\_instance\_count (sm5 - asm)</span></span>

<span data-ttu-id="f8962-104">Deklarieren Sie die Anzahl der joinphasen-Instanzen in einer Hull-Shader-joinphase.</span><span class="sxs-lookup"><span data-stu-id="f8962-104">Declare the join phase instance count in a hull shader join phase.</span></span>



| <span data-ttu-id="f8962-105">DCL \_ HS \_ \_ -joinphasen- \_ \_ Instanzanzahl {1... Max 32-Bit uint}</span><span class="sxs-lookup"><span data-stu-id="f8962-105">dcl\_hs\_join\_phase\_instance\_count {1... max 32-bit UINT}</span></span> |
|--------------------------------------------------------------|



 



| <span data-ttu-id="f8962-106">Element</span><span class="sxs-lookup"><span data-stu-id="f8962-106">Item</span></span>                                                   | <span data-ttu-id="f8962-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8962-107">Description</span></span>                           |
|--------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="f8962-108"><span id="N"></span><span id="n"></span>*Nr*</span><span class="sxs-lookup"><span data-stu-id="f8962-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="f8962-109">\[in \] der Instanzanzahl.</span><span class="sxs-lookup"><span data-stu-id="f8962-109">\[in\] The instance count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f8962-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8962-110">Remarks</span></span>

<span data-ttu-id="f8962-111">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="f8962-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f8962-112">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="f8962-112">Vertex</span></span> | <span data-ttu-id="f8962-113">Hülle</span><span class="sxs-lookup"><span data-stu-id="f8962-113">Hull</span></span> | <span data-ttu-id="f8962-114">Domain</span><span class="sxs-lookup"><span data-stu-id="f8962-114">Domain</span></span> | <span data-ttu-id="f8962-115">Geometrie</span><span class="sxs-lookup"><span data-stu-id="f8962-115">Geometry</span></span> | <span data-ttu-id="f8962-116">Pixel</span><span class="sxs-lookup"><span data-stu-id="f8962-116">Pixel</span></span> | <span data-ttu-id="f8962-117">Compute</span><span class="sxs-lookup"><span data-stu-id="f8962-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="f8962-118">X</span><span class="sxs-lookup"><span data-stu-id="f8962-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f8962-119">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="f8962-119">Minimum Shader Model</span></span>

<span data-ttu-id="f8962-120">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="f8962-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f8962-121">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="f8962-121">Shader Model</span></span>                                              | <span data-ttu-id="f8962-122">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="f8962-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f8962-123">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="f8962-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f8962-124">ja</span><span class="sxs-lookup"><span data-stu-id="f8962-124">yes</span></span>       |
| [<span data-ttu-id="f8962-125">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="f8962-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f8962-126">nein</span><span class="sxs-lookup"><span data-stu-id="f8962-126">no</span></span>        |
| [<span data-ttu-id="f8962-127">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="f8962-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f8962-128">nein</span><span class="sxs-lookup"><span data-stu-id="f8962-128">no</span></span>        |
| [<span data-ttu-id="f8962-129">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f8962-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f8962-130">nein</span><span class="sxs-lookup"><span data-stu-id="f8962-130">no</span></span>        |
| [<span data-ttu-id="f8962-131">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f8962-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f8962-132">nein</span><span class="sxs-lookup"><span data-stu-id="f8962-132">no</span></span>        |
| [<span data-ttu-id="f8962-133">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f8962-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f8962-134">nein</span><span class="sxs-lookup"><span data-stu-id="f8962-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f8962-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f8962-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8962-136">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f8962-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





