---
title: DLT (SM5-ASM)
description: Der Komponenten Weise kleiner-als-Vergleich mit doppelter Genauigkeit.
ms.assetid: A9DE5007-4ADD-403D-A2B7-EAE475E9DCCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88fd45ebde621ed2c5f5aafc013741d6ee34c318
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976361"
---
# <a name="dlt-sm5---asm"></a><span data-ttu-id="6ff19-103">DLT (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="6ff19-103">dlt (sm5 - asm)</span></span>

<span data-ttu-id="6ff19-104">Der Komponenten Weise kleiner-als-Vergleich mit doppelter Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="6ff19-104">Component-wise double-precision less-than comparison.</span></span>



| <span data-ttu-id="6ff19-105">DLT \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="6ff19-105">dlt\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="6ff19-106">Element</span><span class="sxs-lookup"><span data-stu-id="6ff19-106">Item</span></span>                                                            | <span data-ttu-id="6ff19-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ff19-107">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="6ff19-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="6ff19-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="6ff19-109">\[in \] der Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="6ff19-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="6ff19-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6ff19-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="6ff19-111">\[in \] den Komponenten, die mit *Quelle1* verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6ff19-111">\[in\] The components to compare to *src1*.</span></span><br/>         |
| <span data-ttu-id="6ff19-112"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="6ff19-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="6ff19-113">\[in \] den Komponenten, die mit *src0* verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6ff19-113">\[in\] The components to compare to *src0*.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="6ff19-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ff19-114">Remarks</span></span>

<span data-ttu-id="6ff19-115">Diese Anweisung führt den Gleit Komma Vergleich mit doppelter Genauigkeit (*src0*  <  *Quelle1*) für jede Komponente aus und schreibt das Ergebnis in *dest*.</span><span class="sxs-lookup"><span data-stu-id="6ff19-115">This instruction performs the double-precision floating-point comparison (*src0* < *src1*) for each component and writes the result to *dest*.</span></span>

<span data-ttu-id="6ff19-116">Wenn der Vergleich true ist, wird 32-Bit 0xFFFFFFFF für diese Komponente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ff19-116">If the comparison is true, then 32-bit 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="6ff19-117">Andernfalls wird 32-Bit 0x00000000 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ff19-117">Otherwise 32-bit 0x00000000 is returned.</span></span>

<span data-ttu-id="6ff19-118">Der Vergleich mit Nan gibt false zurück.</span><span class="sxs-lookup"><span data-stu-id="6ff19-118">Comparison with NaN returns false.</span></span>

<span data-ttu-id="6ff19-119">Die gültigen *dest* -Masken sind eine oder zwei Komponenten.</span><span class="sxs-lookup"><span data-stu-id="6ff19-119">The valid *dest* masks are any one or two components.</span></span> <span data-ttu-id="6ff19-120">Das heißt:. x,. y,. z,. w,. XY,. XZ,. XW,. YZ,. yw,. zw die erste *dest* -Komponente in der Maske empfängt das 32-Bit-Ergebnis für den ersten Double-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="6ff19-120">That is: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw The first *dest* component in the mask receives the 32-bit result for the first double comparison.</span></span> <span data-ttu-id="6ff19-121">Die zweite Komponente in der Maske (falls vorhanden) empfängt das 32-Bit-Ergebnis für den zweiten doppelten Vergleich.</span><span class="sxs-lookup"><span data-stu-id="6ff19-121">The second component in the mask (if present) receives the 32-bit result for the second double comparison.</span></span>

<span data-ttu-id="6ff19-122">Die gültigen Werte für die Quellparameter lauten ". xyzw", ". xyxy", ". zwxy", ". zwzw".</span><span class="sxs-lookup"><span data-stu-id="6ff19-122">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="6ff19-123">Die folgenden *src* -Zuordnungen sind Post-Swizzle:</span><span class="sxs-lookup"><span data-stu-id="6ff19-123">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="6ff19-124">*src0* ist ein doppeltes vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).</span><span class="sxs-lookup"><span data-stu-id="6ff19-124">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="6ff19-125">*Quelle1* ist ein doppeltes vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).</span><span class="sxs-lookup"><span data-stu-id="6ff19-125">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="6ff19-126">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="6ff19-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6ff19-127">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="6ff19-127">Vertex</span></span> | <span data-ttu-id="6ff19-128">Hülle</span><span class="sxs-lookup"><span data-stu-id="6ff19-128">Hull</span></span> | <span data-ttu-id="6ff19-129">Domain</span><span class="sxs-lookup"><span data-stu-id="6ff19-129">Domain</span></span> | <span data-ttu-id="6ff19-130">Geometrie</span><span class="sxs-lookup"><span data-stu-id="6ff19-130">Geometry</span></span> | <span data-ttu-id="6ff19-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="6ff19-131">Pixel</span></span> | <span data-ttu-id="6ff19-132">Compute</span><span class="sxs-lookup"><span data-stu-id="6ff19-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6ff19-133">X</span><span class="sxs-lookup"><span data-stu-id="6ff19-133">X</span></span>      | <span data-ttu-id="6ff19-134">X</span><span class="sxs-lookup"><span data-stu-id="6ff19-134">X</span></span>    | <span data-ttu-id="6ff19-135">X</span><span class="sxs-lookup"><span data-stu-id="6ff19-135">X</span></span>      | <span data-ttu-id="6ff19-136">X</span><span class="sxs-lookup"><span data-stu-id="6ff19-136">X</span></span>        | <span data-ttu-id="6ff19-137">X</span><span class="sxs-lookup"><span data-stu-id="6ff19-137">X</span></span>     | <span data-ttu-id="6ff19-138">X</span><span class="sxs-lookup"><span data-stu-id="6ff19-138">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6ff19-139">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="6ff19-139">Minimum Shader Model</span></span>

<span data-ttu-id="6ff19-140">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="6ff19-140">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6ff19-141">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="6ff19-141">Shader Model</span></span>                                              | <span data-ttu-id="6ff19-142">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="6ff19-142">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6ff19-143">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="6ff19-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6ff19-144">ja</span><span class="sxs-lookup"><span data-stu-id="6ff19-144">yes</span></span>       |
| [<span data-ttu-id="6ff19-145">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="6ff19-145">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6ff19-146">nein</span><span class="sxs-lookup"><span data-stu-id="6ff19-146">no</span></span>        |
| [<span data-ttu-id="6ff19-147">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="6ff19-147">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6ff19-148">nein</span><span class="sxs-lookup"><span data-stu-id="6ff19-148">no</span></span>        |
| [<span data-ttu-id="6ff19-149">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6ff19-149">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6ff19-150">nein</span><span class="sxs-lookup"><span data-stu-id="6ff19-150">no</span></span>        |
| [<span data-ttu-id="6ff19-151">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6ff19-151">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6ff19-152">nein</span><span class="sxs-lookup"><span data-stu-id="6ff19-152">no</span></span>        |
| [<span data-ttu-id="6ff19-153">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6ff19-153">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6ff19-154">nein</span><span class="sxs-lookup"><span data-stu-id="6ff19-154">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6ff19-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6ff19-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ff19-156">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6ff19-156">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





