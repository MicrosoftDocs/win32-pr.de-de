---
title: dne (SM5-ASM)
description: Der Komponenten Weise Vergleich mit doppelter Genauigkeit und nicht Gleichheit.
ms.assetid: 7C69A86D-0820-4640-AF5A-2993EC77D2AA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae00e0e5f4c0269b14a7a0f330d5af8760a1312f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389545"
---
# <a name="dne-sm5---asm"></a><span data-ttu-id="47be4-103">dne (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="47be4-103">dne (sm5 - asm)</span></span>

<span data-ttu-id="47be4-104">Der Komponenten Weise Vergleich mit doppelter Genauigkeit und nicht Gleichheit.</span><span class="sxs-lookup"><span data-stu-id="47be4-104">Component-wise double-precision not equality comparison.</span></span>



| <span data-ttu-id="47be4-105">dne \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="47be4-105">dne\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="47be4-106">Element</span><span class="sxs-lookup"><span data-stu-id="47be4-106">Item</span></span>                                                            | <span data-ttu-id="47be4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47be4-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="47be4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="47be4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="47be4-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="47be4-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="47be4-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="47be4-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="47be4-111">\[in \] den Komponenten, die mit *Quelle1* verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="47be4-111">\[in\] The components to compare with *src1*.</span></span><br/>      |
| <span data-ttu-id="47be4-112"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="47be4-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="47be4-113">\[in \] den Komponenten, die mit *src0* verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="47be4-113">\[in\] The components to compare with *src0*.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="47be4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47be4-114">Remarks</span></span>

<span data-ttu-id="47be4-115">Diese Anweisung führt den Gleit Komma Vergleich mit doppelter Genauigkeit (*src0* ! = *Quelle1*) für jede Komponente aus und schreibt das Ergebnis in *dest*.</span><span class="sxs-lookup"><span data-stu-id="47be4-115">This instruction performs the double-precision floating-point comparison (*src0* != *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="47be4-116">Wenn der Vergleich true ist, wird 32-Bit 0xFFFFFFFF für diese Komponente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="47be4-116">If the comparison is true, then 32-bit 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="47be4-117">Andernfalls wird 32-Bit 0x00000000 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="47be4-117">Otherwise 32-bit 0x00000000 is returned.</span></span>

<span data-ttu-id="47be4-118">Der Vergleich mit Nan gibt true zurück.</span><span class="sxs-lookup"><span data-stu-id="47be4-118">Comparison with NaN returns true.</span></span>

<span data-ttu-id="47be4-119">Die gültigen *dest* -Masken sind eine oder zwei Komponenten.</span><span class="sxs-lookup"><span data-stu-id="47be4-119">The valid *dest* masks are any one or two components.</span></span> <span data-ttu-id="47be4-120">Das heißt:. x,. y,. z,. w,. XY,. XZ,. XW,. YZ,. yw,. zw die erste *dest* -Komponente in der Maske empfängt das 32-Bit-Ergebnis für den ersten Double-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="47be4-120">That is: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw The first *dest* component in the mask receives the 32-bit result for the first double comparison.</span></span> <span data-ttu-id="47be4-121">Die zweite Komponente in der Maske, falls vorhanden, empfängt das 32-Bit-Ergebnis für den zweiten doppelten Vergleich.</span><span class="sxs-lookup"><span data-stu-id="47be4-121">The second component in the mask, if present, receives the 32-bit result for the second double comparison.</span></span>

<span data-ttu-id="47be4-122">Die gültigen Werte für die Quellparameter lauten ". xyzw", ". xyxy", ". zwxy", ". zwzw".</span><span class="sxs-lookup"><span data-stu-id="47be4-122">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="47be4-123">Die folgenden *src* -Zuordnungen sind Post-Swizzle:</span><span class="sxs-lookup"><span data-stu-id="47be4-123">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="47be4-124">*src0* ist ein doppeltes vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).</span><span class="sxs-lookup"><span data-stu-id="47be4-124">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="47be4-125">*Quelle1* ist ein doppeltes vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).</span><span class="sxs-lookup"><span data-stu-id="47be4-125">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="47be4-126">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="47be4-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="47be4-127">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="47be4-127">Vertex</span></span> | <span data-ttu-id="47be4-128">Hülle</span><span class="sxs-lookup"><span data-stu-id="47be4-128">Hull</span></span> | <span data-ttu-id="47be4-129">Domain</span><span class="sxs-lookup"><span data-stu-id="47be4-129">Domain</span></span> | <span data-ttu-id="47be4-130">Geometrie</span><span class="sxs-lookup"><span data-stu-id="47be4-130">Geometry</span></span> | <span data-ttu-id="47be4-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="47be4-131">Pixel</span></span> | <span data-ttu-id="47be4-132">Compute</span><span class="sxs-lookup"><span data-stu-id="47be4-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="47be4-133">X</span><span class="sxs-lookup"><span data-stu-id="47be4-133">X</span></span>      | <span data-ttu-id="47be4-134">X</span><span class="sxs-lookup"><span data-stu-id="47be4-134">X</span></span>    | <span data-ttu-id="47be4-135">X</span><span class="sxs-lookup"><span data-stu-id="47be4-135">X</span></span>      | <span data-ttu-id="47be4-136">X</span><span class="sxs-lookup"><span data-stu-id="47be4-136">X</span></span>        | <span data-ttu-id="47be4-137">X</span><span class="sxs-lookup"><span data-stu-id="47be4-137">X</span></span>     | <span data-ttu-id="47be4-138">X</span><span class="sxs-lookup"><span data-stu-id="47be4-138">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="47be4-139">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="47be4-139">Minimum Shader Model</span></span>

<span data-ttu-id="47be4-140">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="47be4-140">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="47be4-141">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="47be4-141">Shader Model</span></span>                                              | <span data-ttu-id="47be4-142">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="47be4-142">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="47be4-143">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="47be4-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="47be4-144">ja</span><span class="sxs-lookup"><span data-stu-id="47be4-144">yes</span></span>       |
| [<span data-ttu-id="47be4-145">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="47be4-145">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="47be4-146">nein</span><span class="sxs-lookup"><span data-stu-id="47be4-146">no</span></span>        |
| [<span data-ttu-id="47be4-147">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="47be4-147">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="47be4-148">nein</span><span class="sxs-lookup"><span data-stu-id="47be4-148">no</span></span>        |
| [<span data-ttu-id="47be4-149">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47be4-149">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="47be4-150">nein</span><span class="sxs-lookup"><span data-stu-id="47be4-150">no</span></span>        |
| [<span data-ttu-id="47be4-151">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47be4-151">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="47be4-152">nein</span><span class="sxs-lookup"><span data-stu-id="47be4-152">no</span></span>        |
| [<span data-ttu-id="47be4-153">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47be4-153">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="47be4-154">nein</span><span class="sxs-lookup"><span data-stu-id="47be4-154">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="47be4-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="47be4-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47be4-156">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47be4-156">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





