---
title: Debug (SM5-ASM)
description: Vergleichsweise Gleichheits Vergleich mit doppelter Genauigkeit.
ms.assetid: 99806989-D3A0-43F4-832A-5F1BD9C59A11
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ed263deec975815f29050d2de0a877a312258c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104516490"
---
# <a name="deq-sm5---asm"></a><span data-ttu-id="be710-103">Debug (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="be710-103">deq (sm5 - asm)</span></span>

<span data-ttu-id="be710-104">Vergleichsweise Gleichheits Vergleich mit doppelter Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="be710-104">Component-wise double-precision equality comparison.</span></span>



| <span data-ttu-id="be710-105">DEQ \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="be710-105">deq\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="be710-106">Element</span><span class="sxs-lookup"><span data-stu-id="be710-106">Item</span></span>                                                            | <span data-ttu-id="be710-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be710-107">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="be710-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="be710-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="be710-109">\[in \] der Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="be710-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="be710-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="be710-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="be710-111">\[in \] den Komponenten, die mit *Quelle1* verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="be710-111">\[in\] The components to compare to *src1*.</span></span><br/>         |
| <span data-ttu-id="be710-112"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="be710-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="be710-113">\[in \] den Komponenten, die mit *src0* verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="be710-113">\[in\] The components to compare to *src0*.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="be710-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be710-114">Remarks</span></span>

<span data-ttu-id="be710-115">Diese Anweisung führt den Gleit Komma Vergleich mit doppelter Genauigkeit (*src0*  ==  *Quelle1*) für jede Komponente aus und schreibt das Ergebnis in *dest*.</span><span class="sxs-lookup"><span data-stu-id="be710-115">This instruction performs the double-precision floating-point comparison (*src0* == *src1*) for each component and writes the result to *dest*.</span></span>

<span data-ttu-id="be710-116">Wenn der Vergleich true ist, wird 32-Bit 0xFFFFFFFF für diese Komponente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="be710-116">If the comparison is true, then 32-bit 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="be710-117">Andernfalls wird 32-Bit 0x00000000 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="be710-117">Otherwise 32-bit 0x00000000 is returned.</span></span>

<span data-ttu-id="be710-118">Der Vergleich mit Nan gibt false zurück.</span><span class="sxs-lookup"><span data-stu-id="be710-118">Comparison with NaN returns false.</span></span>

<span data-ttu-id="be710-119">Die gültigen *dest* -Masken sind eine oder zwei Komponenten.</span><span class="sxs-lookup"><span data-stu-id="be710-119">The valid *dest* masks are any one or 2 components.</span></span> <span data-ttu-id="be710-120">Das heißt:. x,. y,. z,. w,. XY,. XZ,. XW,. YZ,. yw,. zw die erste *dest* -Komponente in der Maske empfängt das 32-Bit-Ergebnis für den ersten Double-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="be710-120">That is: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw The first *dest* component in the mask receives the 32-bit result for the first double comparison.</span></span> <span data-ttu-id="be710-121">Die zweite Komponente in der Maske, falls vorhanden, empfängt das 32-Bit-Ergebnis für den zweiten doppelten Vergleich.</span><span class="sxs-lookup"><span data-stu-id="be710-121">The second component in the mask, if present, receives the 32-bit result for the second double comparison.</span></span>

<span data-ttu-id="be710-122">Die gültigen Werte für die Quellparameter lauten ". xyzw", ". xyxy", ". zwxy", ". zwzw".</span><span class="sxs-lookup"><span data-stu-id="be710-122">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="be710-123">Die folgenden *src* -Zuordnungen sind Post-Swizzle:</span><span class="sxs-lookup"><span data-stu-id="be710-123">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="be710-124">*src0* ist ein doppeltes vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).</span><span class="sxs-lookup"><span data-stu-id="be710-124">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="be710-125">*Quelle1* ist ein doppeltes vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).</span><span class="sxs-lookup"><span data-stu-id="be710-125">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="be710-126">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="be710-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="be710-127">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="be710-127">Vertex</span></span> | <span data-ttu-id="be710-128">Hülle</span><span class="sxs-lookup"><span data-stu-id="be710-128">Hull</span></span> | <span data-ttu-id="be710-129">Domain</span><span class="sxs-lookup"><span data-stu-id="be710-129">Domain</span></span> | <span data-ttu-id="be710-130">Geometrie</span><span class="sxs-lookup"><span data-stu-id="be710-130">Geometry</span></span> | <span data-ttu-id="be710-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="be710-131">Pixel</span></span> | <span data-ttu-id="be710-132">Compute</span><span class="sxs-lookup"><span data-stu-id="be710-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="be710-133">X</span><span class="sxs-lookup"><span data-stu-id="be710-133">X</span></span>      | <span data-ttu-id="be710-134">X</span><span class="sxs-lookup"><span data-stu-id="be710-134">X</span></span>    | <span data-ttu-id="be710-135">X</span><span class="sxs-lookup"><span data-stu-id="be710-135">X</span></span>      | <span data-ttu-id="be710-136">X</span><span class="sxs-lookup"><span data-stu-id="be710-136">X</span></span>        | <span data-ttu-id="be710-137">X</span><span class="sxs-lookup"><span data-stu-id="be710-137">X</span></span>     | <span data-ttu-id="be710-138">X</span><span class="sxs-lookup"><span data-stu-id="be710-138">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="be710-139">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="be710-139">Minimum Shader Model</span></span>

<span data-ttu-id="be710-140">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="be710-140">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="be710-141">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="be710-141">Shader Model</span></span>                                              | <span data-ttu-id="be710-142">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="be710-142">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="be710-143">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="be710-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="be710-144">ja</span><span class="sxs-lookup"><span data-stu-id="be710-144">yes</span></span>       |
| [<span data-ttu-id="be710-145">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="be710-145">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="be710-146">nein</span><span class="sxs-lookup"><span data-stu-id="be710-146">no</span></span>        |
| [<span data-ttu-id="be710-147">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="be710-147">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="be710-148">nein</span><span class="sxs-lookup"><span data-stu-id="be710-148">no</span></span>        |
| [<span data-ttu-id="be710-149">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="be710-149">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="be710-150">nein</span><span class="sxs-lookup"><span data-stu-id="be710-150">no</span></span>        |
| [<span data-ttu-id="be710-151">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="be710-151">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="be710-152">nein</span><span class="sxs-lookup"><span data-stu-id="be710-152">no</span></span>        |
| [<span data-ttu-id="be710-153">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="be710-153">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="be710-154">nein</span><span class="sxs-lookup"><span data-stu-id="be710-154">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="be710-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="be710-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be710-156">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="be710-156">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





