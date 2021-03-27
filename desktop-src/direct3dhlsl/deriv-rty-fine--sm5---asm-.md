---
title: deriv_rty_fine (SM5-ASM)
description: Berechnet die Änderungs Rate der Komponenten. | deriv_rty_fine (SM5-ASM)
ms.assetid: 7C5769A6-443C-4208-BD09-3DF3C5902624
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f0274fd04ae88ee412c95947691628754ba197
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995487"
---
# <a name="deriv_rty_fine-sm5---asm"></a><span data-ttu-id="3e6d8-104">DERIV \_ Eigenschaft \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="3e6d8-104">deriv\_rty\_fine (sm5 - asm)</span></span>

<span data-ttu-id="3e6d8-105">Berechnet die Änderungs Rate der Komponenten.</span><span class="sxs-lookup"><span data-stu-id="3e6d8-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="3e6d8-106">DERIV \_ Eigenschaft \_ Fine \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="3e6d8-106">deriv\_rty\_fine\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="3e6d8-107">Element</span><span class="sxs-lookup"><span data-stu-id="3e6d8-107">Item</span></span>                                                            | <span data-ttu-id="3e6d8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e6d8-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="3e6d8-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="3e6d8-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="3e6d8-110">\[in \] der Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="3e6d8-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="3e6d8-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="3e6d8-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="3e6d8-112">\[in \] den Komponenten des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="3e6d8-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="3e6d8-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e6d8-113">Remarks</span></span>

<span data-ttu-id="3e6d8-114">Weitere Informationen finden Sie unter [DERIV \_ RTX \_ prima.](deriv-rtx-fine--sm5---asm-.md)</span><span class="sxs-lookup"><span data-stu-id="3e6d8-114">For more information, see [deriv\_rtx\_fine.](deriv-rtx-fine--sm5---asm-.md)</span></span>

<span data-ttu-id="3e6d8-115">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="3e6d8-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3e6d8-116">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="3e6d8-116">Vertex</span></span> | <span data-ttu-id="3e6d8-117">Hülle</span><span class="sxs-lookup"><span data-stu-id="3e6d8-117">Hull</span></span> | <span data-ttu-id="3e6d8-118">Domain</span><span class="sxs-lookup"><span data-stu-id="3e6d8-118">Domain</span></span> | <span data-ttu-id="3e6d8-119">Geometrie</span><span class="sxs-lookup"><span data-stu-id="3e6d8-119">Geometry</span></span> | <span data-ttu-id="3e6d8-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="3e6d8-120">Pixel</span></span> | <span data-ttu-id="3e6d8-121">Compute</span><span class="sxs-lookup"><span data-stu-id="3e6d8-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="3e6d8-122">X</span><span class="sxs-lookup"><span data-stu-id="3e6d8-122">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3e6d8-123">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="3e6d8-123">Minimum Shader Model</span></span>

<span data-ttu-id="3e6d8-124">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="3e6d8-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="3e6d8-125">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="3e6d8-125">Shader Model</span></span>                                              | <span data-ttu-id="3e6d8-126">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="3e6d8-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3e6d8-127">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="3e6d8-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3e6d8-128">ja</span><span class="sxs-lookup"><span data-stu-id="3e6d8-128">yes</span></span>       |
| [<span data-ttu-id="3e6d8-129">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="3e6d8-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3e6d8-130">nein</span><span class="sxs-lookup"><span data-stu-id="3e6d8-130">no</span></span>        |
| [<span data-ttu-id="3e6d8-131">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="3e6d8-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3e6d8-132">nein</span><span class="sxs-lookup"><span data-stu-id="3e6d8-132">no</span></span>        |
| [<span data-ttu-id="3e6d8-133">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3e6d8-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3e6d8-134">nein</span><span class="sxs-lookup"><span data-stu-id="3e6d8-134">no</span></span>        |
| [<span data-ttu-id="3e6d8-135">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3e6d8-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3e6d8-136">nein</span><span class="sxs-lookup"><span data-stu-id="3e6d8-136">no</span></span>        |
| [<span data-ttu-id="3e6d8-137">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3e6d8-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3e6d8-138">nein</span><span class="sxs-lookup"><span data-stu-id="3e6d8-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3e6d8-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3e6d8-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e6d8-140">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3e6d8-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





