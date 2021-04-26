---
title: max (sm4 - asm)
description: Komponentenweiser Float-Höchstwert.
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64d88c581828f2563f6d5d8a6c57de6400f9bbf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994727"
---
# <a name="max-sm4---asm"></a><span data-ttu-id="dd1f3-103">max (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="dd1f3-103">max (sm4 - asm)</span></span>

<span data-ttu-id="dd1f3-104">Komponentenweiser Float-Höchstwert.</span><span class="sxs-lookup"><span data-stu-id="dd1f3-104">Component-wise float maximum.</span></span>



| <span data-ttu-id="dd1f3-105">max \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle \] , \[ - \] src1 abs \[ \_ \] \[ .swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="dd1f3-105">max\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="dd1f3-106">Element</span><span class="sxs-lookup"><span data-stu-id="dd1f3-106">Item</span></span>                                                            | <span data-ttu-id="dd1f3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd1f3-107">Description</span></span>                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd1f3-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="dd1f3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="dd1f3-109">\[in \] Das Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="dd1f3-109">\[in\] The result of the operation.</span></span> <br/> <span data-ttu-id="dd1f3-110">*dest*  =  *src0*  >=  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="dd1f3-110">*dest* = *src0* >= *src1* ?</span></span> <span data-ttu-id="dd1f3-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="dd1f3-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="dd1f3-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="dd1f3-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="dd1f3-113">\[in \] Die Komponenten, die mit *src1* verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dd1f3-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                    |
| <span data-ttu-id="dd1f3-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="dd1f3-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="dd1f3-115">\[in \] Die Komponenten, die mit *src0* verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dd1f3-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="dd1f3-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dd1f3-116">Remarks</span></span>

><span data-ttu-id="dd1f3-117">= wird anstelle von > verwendet, sodass bei min(x,y) = x dann max(x,y) = y.</span><span class="sxs-lookup"><span data-stu-id="dd1f3-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="dd1f3-118">NaN verfügt über eine spezielle Behandlung.</span><span class="sxs-lookup"><span data-stu-id="dd1f3-118">NaN has special handling.</span></span> <span data-ttu-id="dd1f3-119">Wenn ein Quelloperand NaN ist, wird der andere Quelloperand zurückgegeben, und die Auswahl erfolgt pro Komponente.</span><span class="sxs-lookup"><span data-stu-id="dd1f3-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="dd1f3-120">Wenn beide NaN sind, wird eine beliebige NaN-Darstellung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dd1f3-120">If both are NaN, any NaN representation is returned.</span></span>

<span data-ttu-id="dd1f3-121">Denormen werden mit vor dem Vergleich beibehaltenem Vorzeichen geleert.</span><span class="sxs-lookup"><span data-stu-id="dd1f3-121">Denorms are flushed with sign preserved before the comparison.</span></span> <span data-ttu-id="dd1f3-122">Das in *dest* geschriebene Ergebnis kann jedoch denormiert werden.</span><span class="sxs-lookup"><span data-stu-id="dd1f3-122">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="dd1f3-123">Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Klassen von Zahlen erzielt werden, vorausgesetzt, dass weder Überlauf noch Unterlauf auftreten.</span><span class="sxs-lookup"><span data-stu-id="dd1f3-123">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="dd1f3-124">F bedeutet endliche reale Zahl.</span><span class="sxs-lookup"><span data-stu-id="dd1f3-124">F means finite real number.</span></span>



| <span data-ttu-id="dd1f3-125">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="dd1f3-125">**src0 src1->**</span></span> | <span data-ttu-id="dd1f3-126">**-inf**</span><span class="sxs-lookup"><span data-stu-id="dd1f3-126">**-inf**</span></span> | <span data-ttu-id="dd1f3-127">**F**</span><span class="sxs-lookup"><span data-stu-id="dd1f3-127">**F**</span></span>        | <span data-ttu-id="dd1f3-128">**+inf**</span><span class="sxs-lookup"><span data-stu-id="dd1f3-128">**+inf**</span></span> | <span data-ttu-id="dd1f3-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="dd1f3-129">**NaN**</span></span> |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="dd1f3-130">**-inf**</span><span class="sxs-lookup"><span data-stu-id="dd1f3-130">**-inf**</span></span>           | <span data-ttu-id="dd1f3-131">-inf</span><span class="sxs-lookup"><span data-stu-id="dd1f3-131">-inf</span></span>     | <span data-ttu-id="dd1f3-132">src1</span><span class="sxs-lookup"><span data-stu-id="dd1f3-132">src1</span></span>         | <span data-ttu-id="dd1f3-133">+inf</span><span class="sxs-lookup"><span data-stu-id="dd1f3-133">+inf</span></span>     | <span data-ttu-id="dd1f3-134">-inf</span><span class="sxs-lookup"><span data-stu-id="dd1f3-134">-inf</span></span>    |
| <span data-ttu-id="dd1f3-135">**F**</span><span class="sxs-lookup"><span data-stu-id="dd1f3-135">**F**</span></span>              | <span data-ttu-id="dd1f3-136">src0</span><span class="sxs-lookup"><span data-stu-id="dd1f3-136">src0</span></span>     | <span data-ttu-id="dd1f3-137">src0 oder src1</span><span class="sxs-lookup"><span data-stu-id="dd1f3-137">src0 or src1</span></span> | <span data-ttu-id="dd1f3-138">+inf</span><span class="sxs-lookup"><span data-stu-id="dd1f3-138">+inf</span></span>     | <span data-ttu-id="dd1f3-139">src0</span><span class="sxs-lookup"><span data-stu-id="dd1f3-139">src0</span></span>    |
| <span data-ttu-id="dd1f3-140">**+inf**</span><span class="sxs-lookup"><span data-stu-id="dd1f3-140">**+inf**</span></span>           | <span data-ttu-id="dd1f3-141">+inf</span><span class="sxs-lookup"><span data-stu-id="dd1f3-141">+inf</span></span>     | <span data-ttu-id="dd1f3-142">+inf</span><span class="sxs-lookup"><span data-stu-id="dd1f3-142">+inf</span></span>         | <span data-ttu-id="dd1f3-143">+inf</span><span class="sxs-lookup"><span data-stu-id="dd1f3-143">+inf</span></span>     | <span data-ttu-id="dd1f3-144">+inf</span><span class="sxs-lookup"><span data-stu-id="dd1f3-144">+inf</span></span>    |
| <span data-ttu-id="dd1f3-145">**NaN**</span><span class="sxs-lookup"><span data-stu-id="dd1f3-145">**NaN**</span></span>            | <span data-ttu-id="dd1f3-146">-inf</span><span class="sxs-lookup"><span data-stu-id="dd1f3-146">-inf</span></span>     | <span data-ttu-id="dd1f3-147">src1</span><span class="sxs-lookup"><span data-stu-id="dd1f3-147">src1</span></span>         | <span data-ttu-id="dd1f3-148">+inf</span><span class="sxs-lookup"><span data-stu-id="dd1f3-148">+inf</span></span>     | <span data-ttu-id="dd1f3-149">NaN</span><span class="sxs-lookup"><span data-stu-id="dd1f3-149">NaN</span></span>     |



 

<span data-ttu-id="dd1f3-150">Diese Anweisung gilt für die folgenden Shaderstufen:</span><span class="sxs-lookup"><span data-stu-id="dd1f3-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="dd1f3-151">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="dd1f3-151">Vertex Shader</span></span> | <span data-ttu-id="dd1f3-152">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="dd1f3-152">Geometry Shader</span></span> | <span data-ttu-id="dd1f3-153">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="dd1f3-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="dd1f3-154">x</span><span class="sxs-lookup"><span data-stu-id="dd1f3-154">x</span></span>             | <span data-ttu-id="dd1f3-155">x</span><span class="sxs-lookup"><span data-stu-id="dd1f3-155">x</span></span>               | <span data-ttu-id="dd1f3-156">x</span><span class="sxs-lookup"><span data-stu-id="dd1f3-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="dd1f3-157">Minimales Shadermodell</span><span class="sxs-lookup"><span data-stu-id="dd1f3-157">Minimum Shader Model</span></span>

<span data-ttu-id="dd1f3-158">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dd1f3-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="dd1f3-159">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="dd1f3-159">Shader Model</span></span>                                              | <span data-ttu-id="dd1f3-160">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="dd1f3-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="dd1f3-161">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="dd1f3-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="dd1f3-162">ja</span><span class="sxs-lookup"><span data-stu-id="dd1f3-162">yes</span></span>       |
| [<span data-ttu-id="dd1f3-163">Shadermodell 4.1</span><span class="sxs-lookup"><span data-stu-id="dd1f3-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="dd1f3-164">ja</span><span class="sxs-lookup"><span data-stu-id="dd1f3-164">yes</span></span>       |
| [<span data-ttu-id="dd1f3-165">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="dd1f3-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="dd1f3-166">ja</span><span class="sxs-lookup"><span data-stu-id="dd1f3-166">yes</span></span>       |
| [<span data-ttu-id="dd1f3-167">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dd1f3-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="dd1f3-168">nein</span><span class="sxs-lookup"><span data-stu-id="dd1f3-168">no</span></span>        |
| [<span data-ttu-id="dd1f3-169">Shadermodell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dd1f3-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="dd1f3-170">nein</span><span class="sxs-lookup"><span data-stu-id="dd1f3-170">no</span></span>        |
| [<span data-ttu-id="dd1f3-171">Shadermodell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dd1f3-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="dd1f3-172">nein</span><span class="sxs-lookup"><span data-stu-id="dd1f3-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="dd1f3-173">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dd1f3-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd1f3-174">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dd1f3-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





