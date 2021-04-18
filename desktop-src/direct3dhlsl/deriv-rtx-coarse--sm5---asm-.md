---
title: deriv_rtx_coarse (SM5-ASM)
description: Berechnet die Änderungs Rate der Komponenten. | deriv_rtx_coarse (SM5-ASM)
ms.assetid: 57743BB2-251C-4EA7-BDA9-70B2ECEE3B3F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2355b6db6aef9e85959d6359053fea76b48af0a5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995398"
---
# <a name="deriv_rtx_coarse-sm5---asm"></a><span data-ttu-id="4c593-104">DERIV \_ RTX \_ grob (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="4c593-104">deriv\_rtx\_coarse (sm5 - asm)</span></span>

<span data-ttu-id="4c593-105">Berechnet die Änderungs Rate der Komponenten.</span><span class="sxs-lookup"><span data-stu-id="4c593-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="4c593-106">DERIV \_ RTX \_ grob \[ \_ sa \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="4c593-106">deriv\_rtx\_coarse\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|----------------------------------------------------------------------------|



 



| <span data-ttu-id="4c593-107">Element</span><span class="sxs-lookup"><span data-stu-id="4c593-107">Item</span></span>                                                            | <span data-ttu-id="4c593-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4c593-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="4c593-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="4c593-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="4c593-110">\[in \] der Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="4c593-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="4c593-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="4c593-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="4c593-112">\[in \] den Komponenten des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="4c593-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="4c593-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c593-113">Remarks</span></span>

<span data-ttu-id="4c593-114">Diese Anweisung berechnet die Rate der Inhalts Änderungen jeder float32-Komponente von *src0* (Post-Swizzle) in Bezug auf die Richtung renderTarget x Direction (RTX) oder renderTarget y (siehe [DERIV \_ Eigenschaft \_ grob](deriv-rty-coarse--sm5---asm-.md)).</span><span class="sxs-lookup"><span data-stu-id="4c593-114">This instruction computes the rate of change of contents of each float32 component of *src0* (post-swizzle), with regard to RenderTarget x direction (rtx) or RenderTarget y direction (see [deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md)).</span></span> <span data-ttu-id="4c593-115">Nur ein einzelnes x-, y-abgeleitetes Paar wird für jeden 2 x 2-Stempel von Pixel berechnet.</span><span class="sxs-lookup"><span data-stu-id="4c593-115">Only a single x,y derivative pair is computed for each 2x2 stamp of pixels.</span></span>

<span data-ttu-id="4c593-116">Die Daten im aktuellen pixelshaderaufruf können nicht an der Berechnung der angeforderten Ableitung beteiligt sein, da die Ableitung nur einmal pro 2 x 2 Quad berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="4c593-116">The data in the current pixel shader invocation may or may not participate in the calculation of the requested derivative, because the derivative will be calculated only once per 2x2 quad.</span></span> <span data-ttu-id="4c593-117">Beispielsweise könnte die x-Ableitung ein Delta von der obersten Zeile der Pixel sein, und die y-Richtung ([DERIV \_ Eigenschaft \_ grob](deriv-rty-coarse--sm5---asm-.md)) kann ein Delta aus der linken Spalte der Pixel sein.</span><span class="sxs-lookup"><span data-stu-id="4c593-117">For example, the x derivative could be a delta from the top row of pixels, and the y direction ([deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md)) could be a delta from the left column of pixels.</span></span> <span data-ttu-id="4c593-118">Die genaue Berechnung erfolgt bis zum Hardwarehersteller.</span><span class="sxs-lookup"><span data-stu-id="4c593-118">The exact calculation is up to the hardware vendor.</span></span> <span data-ttu-id="4c593-119">Es gibt auch keine Angabe, wie die 2 x 2-Quads über einen primitiven ausgerichtet oder gekachelt werden.</span><span class="sxs-lookup"><span data-stu-id="4c593-119">There is also no specification dictating how the 2x2 quads will be aligned or tiled over a primitive.</span></span>

<span data-ttu-id="4c593-120">Ableitungen werden auf einer groben Ebene berechnet, einmal pro 2 x 2 Pixel Quad.</span><span class="sxs-lookup"><span data-stu-id="4c593-120">Derivatives are calculated at a coarse level, once per 2x2 pixel quad.</span></span> <span data-ttu-id="4c593-121">Diese Anweisung und [DERIV \_ Eigenschaft \_ grob](deriv-rty-coarse--sm5---asm-.md) sind Alternativen zu [DERIV \_ RTX \_ Fine](deriv-rtx-fine--sm5---asm-.md) und [DERIV \_ Eigenschaft \_ ](deriv-rty-fine--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="4c593-121">This instruction and [deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md) are alternatives to [deriv\_rtx\_fine](deriv-rtx-fine--sm5---asm-.md) and [deriv\_rty\_fine](deriv-rty-fine--sm5---asm-.md).</span></span> <span data-ttu-id="4c593-122">Diese \_ groben und differenzierten \_ Anweisungen sind ein Ersatz für **DERIV \_ rtxderiv \_ Eigenschaft** aus früheren shadermodellen.</span><span class="sxs-lookup"><span data-stu-id="4c593-122">These \_coarse and \_fine derivative instructions are a replacement for **deriv\_rtxderiv\_rty** from previous shader models .</span></span>

<span data-ttu-id="4c593-123">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="4c593-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4c593-124">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="4c593-124">Vertex</span></span> | <span data-ttu-id="4c593-125">Hülle</span><span class="sxs-lookup"><span data-stu-id="4c593-125">Hull</span></span> | <span data-ttu-id="4c593-126">Domain</span><span class="sxs-lookup"><span data-stu-id="4c593-126">Domain</span></span> | <span data-ttu-id="4c593-127">Geometrie</span><span class="sxs-lookup"><span data-stu-id="4c593-127">Geometry</span></span> | <span data-ttu-id="4c593-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="4c593-128">Pixel</span></span> | <span data-ttu-id="4c593-129">Compute</span><span class="sxs-lookup"><span data-stu-id="4c593-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="4c593-130">X</span><span class="sxs-lookup"><span data-stu-id="4c593-130">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4c593-131">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="4c593-131">Minimum Shader Model</span></span>

<span data-ttu-id="4c593-132">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="4c593-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="4c593-133">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="4c593-133">Shader Model</span></span>                                              | <span data-ttu-id="4c593-134">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="4c593-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4c593-135">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="4c593-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4c593-136">ja</span><span class="sxs-lookup"><span data-stu-id="4c593-136">yes</span></span>       |
| [<span data-ttu-id="4c593-137">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="4c593-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4c593-138">nein</span><span class="sxs-lookup"><span data-stu-id="4c593-138">no</span></span>        |
| [<span data-ttu-id="4c593-139">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="4c593-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4c593-140">nein</span><span class="sxs-lookup"><span data-stu-id="4c593-140">no</span></span>        |
| [<span data-ttu-id="4c593-141">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4c593-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4c593-142">nein</span><span class="sxs-lookup"><span data-stu-id="4c593-142">no</span></span>        |
| [<span data-ttu-id="4c593-143">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4c593-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4c593-144">nein</span><span class="sxs-lookup"><span data-stu-id="4c593-144">no</span></span>        |
| [<span data-ttu-id="4c593-145">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4c593-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4c593-146">nein</span><span class="sxs-lookup"><span data-stu-id="4c593-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4c593-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4c593-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c593-148">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4c593-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





