---
title: dmuvc (SM5-ASM)
description: Bedingter Wechsel in Komponenten. | dmuvc (SM5-ASM)
ms.assetid: E376FE08-E251-4BE5-9F15-99B3B67A29C8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e364e6340733c42ae69412db726851329eb2809d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104393930"
---
# <a name="dmovc-sm5---asm"></a><span data-ttu-id="1c712-104">dmuvc (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="1c712-104">dmovc (sm5 - asm)</span></span>

<span data-ttu-id="1c712-105">Bedingter Wechsel in Komponenten.</span><span class="sxs-lookup"><span data-stu-id="1c712-105">Component-wise conditional move.</span></span>



| <span data-ttu-id="1c712-106">dmuvc \[ \_ Sat \] dest \[ . mask \] , src0 \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle2 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="1c712-106">dmovc\[\_sat\] dest\[.mask\], src0\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\], \[-\]src2\[\_abs\]\[.swizzle\],</span></span> |
|-----------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="1c712-107">Element</span><span class="sxs-lookup"><span data-stu-id="1c712-107">Item</span></span>                                                            | <span data-ttu-id="1c712-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1c712-108">Description</span></span>                                                                                              |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c712-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="1c712-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="1c712-110">\[im Verschiebungs \] Ziel.</span><span class="sxs-lookup"><span data-stu-id="1c712-110">\[in\] The move destination.</span></span><br/> <span data-ttu-id="1c712-111">Wenn *src0*, dann *dest*  =  *Quelle1* Else *dest*  =  *Quelle2*.</span><span class="sxs-lookup"><span data-stu-id="1c712-111">If *src0*, then *dest* = *src1* else *dest* = *src2*.</span></span><br/> |
| <span data-ttu-id="1c712-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1c712-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="1c712-113">\[in \] den Komponenten, mit denen die Bedingung getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1c712-113">\[in\] The components to test the condition against.</span></span><br/>                                          |
| <span data-ttu-id="1c712-114"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="1c712-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="1c712-115">\[in \] den Komponenten, die verschoben werden sollen, wenn die Bedingung erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="1c712-115">\[in\] The components to move if the condition is true.</span></span><br/>                                       |
| <span data-ttu-id="1c712-116"><span id="src2"></span><span id="SRC2"></span>*Quelle2*</span><span class="sxs-lookup"><span data-stu-id="1c712-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="1c712-117">\[in \] den zu Verschieb-Komponenten, wenn die Bedingung false ist.</span><span class="sxs-lookup"><span data-stu-id="1c712-117">\[in\] The components to move if the condition is false.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="1c712-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c712-118">Remarks</span></span>

<span data-ttu-id="1c712-119">Das folgende Beispiel zeigt die Verwendung dieser Anweisung.</span><span class="sxs-lookup"><span data-stu-id="1c712-119">The following example shows how to use this instruction.</span></span>

``` syntax
                if(the dest mask contains .xy)
                {
                    if(the first 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the first double from src1 (post swizzle)
                        into dest.xy
                    }
                    else
                    {
                        copy the first double from src2 (post swizzle)
                        into dest.xy
                    }
                }
                if(the dest mask contains .zw)
                {
                    if(the second 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the second double from src1 (post swizzle)
                        into dest.zw
                    }
                    else
                    {
                        copy the second double from src2 (post swizzle)
                        into dest.zw
                    }
                }
```

<span data-ttu-id="1c712-120">Gültige Masken für dest sind. XY,. ZW,. xyzw.</span><span class="sxs-lookup"><span data-stu-id="1c712-120">The valid masks for dest are .xy, .zw, .xyzw.</span></span>

<span data-ttu-id="1c712-121">Die gültigen Streifen für *src0* sind alles.</span><span class="sxs-lookup"><span data-stu-id="1c712-121">The valid swizzles for *src0* are anything.</span></span> <span data-ttu-id="1c712-122">Die ersten beiden Komponenten nach dem wischen werden verwendet, um die 2 32-Bit-Bedingungs Werte zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="1c712-122">The first two components post-swizzle are used to indentify two 32-bit condition values.</span></span>

<span data-ttu-id="1c712-123">Die gültigen Streifen für *Quelle1* und *Quelle2* , die doppelte enthalten, sind. xyzw,. xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="1c712-123">The valid swizzles for *src1* and *src2* containing doubles are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="1c712-124">sind ". XY", ". zw" und ". xyzw".</span><span class="sxs-lookup"><span data-stu-id="1c712-124">are .xy, .zw, and .xyzw.</span></span>

<span data-ttu-id="1c712-125">Die folgenden *src* -Zuordnungen finden Sie nachfolgend:</span><span class="sxs-lookup"><span data-stu-id="1c712-125">The following *src* mappings below are post-swizzle:</span></span>

-   <span data-ttu-id="1c712-126">*dest* ist eine doppelte vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).</span><span class="sxs-lookup"><span data-stu-id="1c712-126">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="1c712-127">*src0* ist ein 32-Bit-/Komponenten-vec2 über x und y hinweg (ZW wird ignoriert).</span><span class="sxs-lookup"><span data-stu-id="1c712-127">*src0* is a 32bit/component vec2 across x and y (zw ignored).</span></span>
-   <span data-ttu-id="1c712-128">*Quelle1* ist ein doppeltes vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).</span><span class="sxs-lookup"><span data-stu-id="1c712-128">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="1c712-129">*Quelle2* ist ein doppeltes vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).</span><span class="sxs-lookup"><span data-stu-id="1c712-129">*src2* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="1c712-130">Bei den Modifizierern auf *Quelle1* und *Quelle2*, mit Ausnahme von Swizzle, wird davon ausgegangen, dass die Daten doppelt sind.</span><span class="sxs-lookup"><span data-stu-id="1c712-130">The modifiers on *src1* and *src2*, other than swizzle, assume the data is double.</span></span> <span data-ttu-id="1c712-131">Das Fehlen von Modifizierern verschiebt Daten, ohne Bits zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1c712-131">The absence of modifiers moves data without altering bits.</span></span>

<span data-ttu-id="1c712-132">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="1c712-132">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1c712-133">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="1c712-133">Vertex</span></span> | <span data-ttu-id="1c712-134">Hülle</span><span class="sxs-lookup"><span data-stu-id="1c712-134">Hull</span></span> | <span data-ttu-id="1c712-135">Domain</span><span class="sxs-lookup"><span data-stu-id="1c712-135">Domain</span></span> | <span data-ttu-id="1c712-136">Geometrie</span><span class="sxs-lookup"><span data-stu-id="1c712-136">Geometry</span></span> | <span data-ttu-id="1c712-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="1c712-137">Pixel</span></span> | <span data-ttu-id="1c712-138">Compute</span><span class="sxs-lookup"><span data-stu-id="1c712-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1c712-139">X</span><span class="sxs-lookup"><span data-stu-id="1c712-139">X</span></span>      | <span data-ttu-id="1c712-140">X</span><span class="sxs-lookup"><span data-stu-id="1c712-140">X</span></span>    | <span data-ttu-id="1c712-141">X</span><span class="sxs-lookup"><span data-stu-id="1c712-141">X</span></span>      | <span data-ttu-id="1c712-142">X</span><span class="sxs-lookup"><span data-stu-id="1c712-142">X</span></span>        | <span data-ttu-id="1c712-143">X</span><span class="sxs-lookup"><span data-stu-id="1c712-143">X</span></span>     | <span data-ttu-id="1c712-144">X</span><span class="sxs-lookup"><span data-stu-id="1c712-144">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1c712-145">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="1c712-145">Minimum Shader Model</span></span>

<span data-ttu-id="1c712-146">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="1c712-146">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="1c712-147">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="1c712-147">Shader Model</span></span>                                              | <span data-ttu-id="1c712-148">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="1c712-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1c712-149">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="1c712-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1c712-150">ja</span><span class="sxs-lookup"><span data-stu-id="1c712-150">yes</span></span>       |
| [<span data-ttu-id="1c712-151">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="1c712-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1c712-152">nein</span><span class="sxs-lookup"><span data-stu-id="1c712-152">no</span></span>        |
| [<span data-ttu-id="1c712-153">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="1c712-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1c712-154">nein</span><span class="sxs-lookup"><span data-stu-id="1c712-154">no</span></span>        |
| [<span data-ttu-id="1c712-155">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c712-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1c712-156">nein</span><span class="sxs-lookup"><span data-stu-id="1c712-156">no</span></span>        |
| [<span data-ttu-id="1c712-157">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c712-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1c712-158">nein</span><span class="sxs-lookup"><span data-stu-id="1c712-158">no</span></span>        |
| [<span data-ttu-id="1c712-159">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c712-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1c712-160">nein</span><span class="sxs-lookup"><span data-stu-id="1c712-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1c712-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1c712-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c712-162">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c712-162">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





