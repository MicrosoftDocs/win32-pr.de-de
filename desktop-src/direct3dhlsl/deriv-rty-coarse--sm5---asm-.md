---
title: deriv_rty_coarse (SM5-ASM)
description: Berechnet die Änderungs Rate der Komponenten. | deriv_rty_coarse (SM5-ASM)
ms.assetid: 1EBCC0B9-BD3E-46DD-AC17-F7167F892195
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df7fd539adf8587118a6bdfdcb5959925e6a97f8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995606"
---
# <a name="deriv_rty_coarse-sm5---asm"></a><span data-ttu-id="3d4c6-104">DERIV \_ Eigenschaft \_ grob (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="3d4c6-104">deriv\_rty\_coarse (sm5 - asm)</span></span>

<span data-ttu-id="3d4c6-105">Berechnet die Änderungs Rate der Komponenten.</span><span class="sxs-lookup"><span data-stu-id="3d4c6-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="3d4c6-106">DERIV \_ Eigenschaft \_ grobe \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="3d4c6-106">deriv\_rty\_coarse\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|----------------------------------------------------------------------------|



 



| <span data-ttu-id="3d4c6-107">Element</span><span class="sxs-lookup"><span data-stu-id="3d4c6-107">Item</span></span>                                                            | <span data-ttu-id="3d4c6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d4c6-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="3d4c6-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="3d4c6-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="3d4c6-110">\[in \] der Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="3d4c6-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="3d4c6-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="3d4c6-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="3d4c6-112">\[in \] den Komponenten des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="3d4c6-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="3d4c6-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d4c6-113">Remarks</span></span>

<span data-ttu-id="3d4c6-114">Weitere Informationen finden Sie unter [DERIV \_ RTX \_ grob.](deriv-rtx-coarse--sm5---asm-.md)</span><span class="sxs-lookup"><span data-stu-id="3d4c6-114">For more information, see [deriv\_rtx\_coarse.](deriv-rtx-coarse--sm5---asm-.md)</span></span>

<span data-ttu-id="3d4c6-115">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="3d4c6-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3d4c6-116">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="3d4c6-116">Vertex</span></span> | <span data-ttu-id="3d4c6-117">Hülle</span><span class="sxs-lookup"><span data-stu-id="3d4c6-117">Hull</span></span> | <span data-ttu-id="3d4c6-118">Domain</span><span class="sxs-lookup"><span data-stu-id="3d4c6-118">Domain</span></span> | <span data-ttu-id="3d4c6-119">Geometrie</span><span class="sxs-lookup"><span data-stu-id="3d4c6-119">Geometry</span></span> | <span data-ttu-id="3d4c6-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="3d4c6-120">Pixel</span></span> | <span data-ttu-id="3d4c6-121">Compute</span><span class="sxs-lookup"><span data-stu-id="3d4c6-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="3d4c6-122">X</span><span class="sxs-lookup"><span data-stu-id="3d4c6-122">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3d4c6-123">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="3d4c6-123">Minimum Shader Model</span></span>

<span data-ttu-id="3d4c6-124">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="3d4c6-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="3d4c6-125">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="3d4c6-125">Shader Model</span></span>                                              | <span data-ttu-id="3d4c6-126">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="3d4c6-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3d4c6-127">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="3d4c6-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3d4c6-128">ja</span><span class="sxs-lookup"><span data-stu-id="3d4c6-128">yes</span></span>       |
| [<span data-ttu-id="3d4c6-129">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="3d4c6-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3d4c6-130">nein</span><span class="sxs-lookup"><span data-stu-id="3d4c6-130">no</span></span>        |
| [<span data-ttu-id="3d4c6-131">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="3d4c6-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3d4c6-132">nein</span><span class="sxs-lookup"><span data-stu-id="3d4c6-132">no</span></span>        |
| [<span data-ttu-id="3d4c6-133">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3d4c6-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3d4c6-134">nein</span><span class="sxs-lookup"><span data-stu-id="3d4c6-134">no</span></span>        |
| [<span data-ttu-id="3d4c6-135">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3d4c6-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3d4c6-136">nein</span><span class="sxs-lookup"><span data-stu-id="3d4c6-136">no</span></span>        |
| [<span data-ttu-id="3d4c6-137">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3d4c6-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3d4c6-138">nein</span><span class="sxs-lookup"><span data-stu-id="3d4c6-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3d4c6-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3d4c6-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d4c6-140">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3d4c6-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





