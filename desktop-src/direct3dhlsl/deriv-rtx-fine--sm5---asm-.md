---
title: deriv_rtx_fine (SM5-ASM)
description: Berechnet die Änderungs Rate der Komponenten. | deriv_rtx_fine (SM5-ASM)
ms.assetid: 5752C85B-2965-489C-BF27-968FAF5EAA52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73061e3220704cf2c19e28b4d6d434fda43fb941
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995607"
---
# <a name="deriv_rtx_fine-sm5---asm"></a><span data-ttu-id="03f24-104">DERIV \_ RTX \_ einwandfrei (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="03f24-104">deriv\_rtx\_fine (sm5 - asm)</span></span>

<span data-ttu-id="03f24-105">Berechnet die Änderungs Rate der Komponenten.</span><span class="sxs-lookup"><span data-stu-id="03f24-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="03f24-106">DERIV \_ RTX \_ fein \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="03f24-106">deriv\_rtx\_fine\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="03f24-107">Element</span><span class="sxs-lookup"><span data-stu-id="03f24-107">Item</span></span>                                                            | <span data-ttu-id="03f24-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03f24-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="03f24-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="03f24-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="03f24-110">\[in \] der Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="03f24-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="03f24-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="03f24-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="03f24-112">\[in \] den Komponenten des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="03f24-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="03f24-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03f24-113">Remarks</span></span>

<span data-ttu-id="03f24-114">Diese Anweisung berechnet die Rate der Inhalts Änderungen jeder float32-Komponente von *src0* (Post-Swizzle) in Bezug auf die Richtung renderTarget x Direction (RTX) oder renderTarget y (siehe [DERIV \_ Eigenschaft \_ Fine](deriv-rty-fine--sm5---asm-.md)).</span><span class="sxs-lookup"><span data-stu-id="03f24-114">This instruction computes the rate of change of contents of each float32 component of *src0* (post-swizzle), with regard to RenderTarget x direction (rtx) or RenderTarget y direction (see [deriv\_rty\_fine](deriv-rty-fine--sm5---asm-.md)).</span></span> <span data-ttu-id="03f24-115">Jedes Pixel im 2 x 2-Stempel erhält ein eindeutiges Paar von x/y-abgeleiteten Berechnungen.</span><span class="sxs-lookup"><span data-stu-id="03f24-115">Each pixel in the 2x2 stamp gets a unique pair of x/y derivative calculations</span></span>

<span data-ttu-id="03f24-116">Die Daten im aktuellen Pixelshader-Aufruf sind immer an der Berechnung der angeforderten Ableitung beteiligt.</span><span class="sxs-lookup"><span data-stu-id="03f24-116">The data in the current pixel shader invocation always participates in the calculation of the requested derivative.</span></span> <span data-ttu-id="03f24-117">Im 2 x 2-Pixel-Quad liegt das aktuelle Pixel in. die x-Ableitung ist das Delta der Zeile von 2 Pixeln, einschließlich des aktuellen Pixels.</span><span class="sxs-lookup"><span data-stu-id="03f24-117">In the 2x2 pixel quad the current pixel falls within, the x derivative is the delta of the row of 2 pixels including the current pixel.</span></span> <span data-ttu-id="03f24-118">Die y-Ableitung ist das Delta der Spalte mit 2 Pixeln, einschließlich des aktuellen Pixels.</span><span class="sxs-lookup"><span data-stu-id="03f24-118">The y derivative is the delta of the column of 2 pixels including the current pixel.</span></span> <span data-ttu-id="03f24-119">Es gibt keine Spezifikation, die bestimmt, wie die 2 x 2-Quads durch ein primitiv ausgerichtet oder gekachelt werden.</span><span class="sxs-lookup"><span data-stu-id="03f24-119">There is no specification dictating how the 2x2 quads will be aligned or tiled over a primitive.</span></span>

<span data-ttu-id="03f24-120">Ableitungen werden auf feiner Ebene berechnet (eindeutige Berechnung des x/y-abgeleiteten Paars für jedes Pixel in einem 2 x 2 Quad).</span><span class="sxs-lookup"><span data-stu-id="03f24-120">Derivatives are calculated at a fine level (unique calculation of the x/y derivative pair for each pixel in a 2x2 quad).</span></span> <span data-ttu-id="03f24-121">Diese Anweisung und [DERIV \_ Eigenschaft \_ ](deriv-rty-fine--sm5---asm-.md) sind Alternativen zu [DERIV \_ RTX \_ grob](deriv-rtx-coarse--sm5---asm-.md) und [DERIV \_ Eigenschaft \_ grob](deriv-rty-coarse--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="03f24-121">This instruction and [deriv\_rty\_fine](deriv-rty-fine--sm5---asm-.md) are alternatives to [deriv\_rtx\_coarse](deriv-rtx-coarse--sm5---asm-.md) and [deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md).</span></span> <span data-ttu-id="03f24-122">Diese \_ groben und differenzierten \_ Anweisungen sind ein Ersatz für **DERIV \_ RTX** . diese \_ groben und differenzierten \_ Anweisungen sind ein Ersatz für **DERIV \_ RTX** und **DERIV \_ Eigenschaft** aus früheren Shader-Modellen.</span><span class="sxs-lookup"><span data-stu-id="03f24-122">These \_coarse and \_fine derivative instructions are a replacement for **deriv\_rtx** These \_coarse and \_fine derivative instructions are a replacement for **deriv\_rtx** and **deriv\_rty** from previous shader models.</span></span>

<span data-ttu-id="03f24-123">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="03f24-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="03f24-124">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="03f24-124">Vertex</span></span> | <span data-ttu-id="03f24-125">Hülle</span><span class="sxs-lookup"><span data-stu-id="03f24-125">Hull</span></span> | <span data-ttu-id="03f24-126">Domain</span><span class="sxs-lookup"><span data-stu-id="03f24-126">Domain</span></span> | <span data-ttu-id="03f24-127">Geometrie</span><span class="sxs-lookup"><span data-stu-id="03f24-127">Geometry</span></span> | <span data-ttu-id="03f24-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="03f24-128">Pixel</span></span> | <span data-ttu-id="03f24-129">Compute</span><span class="sxs-lookup"><span data-stu-id="03f24-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="03f24-130">X</span><span class="sxs-lookup"><span data-stu-id="03f24-130">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="03f24-131">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="03f24-131">Minimum Shader Model</span></span>

<span data-ttu-id="03f24-132">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="03f24-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="03f24-133">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="03f24-133">Shader Model</span></span>                                              | <span data-ttu-id="03f24-134">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="03f24-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="03f24-135">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="03f24-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="03f24-136">ja</span><span class="sxs-lookup"><span data-stu-id="03f24-136">yes</span></span>       |
| [<span data-ttu-id="03f24-137">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="03f24-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="03f24-138">nein</span><span class="sxs-lookup"><span data-stu-id="03f24-138">no</span></span>        |
| [<span data-ttu-id="03f24-139">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="03f24-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="03f24-140">nein</span><span class="sxs-lookup"><span data-stu-id="03f24-140">no</span></span>        |
| [<span data-ttu-id="03f24-141">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="03f24-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="03f24-142">nein</span><span class="sxs-lookup"><span data-stu-id="03f24-142">no</span></span>        |
| [<span data-ttu-id="03f24-143">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="03f24-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="03f24-144">nein</span><span class="sxs-lookup"><span data-stu-id="03f24-144">no</span></span>        |
| [<span data-ttu-id="03f24-145">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="03f24-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="03f24-146">nein</span><span class="sxs-lookup"><span data-stu-id="03f24-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="03f24-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="03f24-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03f24-148">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="03f24-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





