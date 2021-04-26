---
title: min (sm4 - asm)
description: Komponentenweiser gleitkommamindest.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8791589b77edc66eeab4b48f10f4a9b16b5cb2d9
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993897"
---
# <a name="min-sm4---asm"></a><span data-ttu-id="2d76f-103">min (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="2d76f-103">min (sm4 - asm)</span></span>

<span data-ttu-id="2d76f-104">Komponentenweiser gleitkommamindest.</span><span class="sxs-lookup"><span data-stu-id="2d76f-104">Component-wise float minimum.</span></span>



| <span data-ttu-id="2d76f-105">min \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle \] , \[ - \] src1 abs \[ \_ \] \[ .swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="2d76f-105">min\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="2d76f-106">Element</span><span class="sxs-lookup"><span data-stu-id="2d76f-106">Item</span></span>                                                            | <span data-ttu-id="2d76f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d76f-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d76f-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="2d76f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="2d76f-109">\[in \] Das Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="2d76f-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="2d76f-110">*dest*  =  *src0*  <  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="2d76f-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="2d76f-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="2d76f-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="2d76f-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2d76f-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="2d76f-113">\[in \] Die Komponenten, die mit *src1* verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2d76f-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                  |
| <span data-ttu-id="2d76f-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="2d76f-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="2d76f-115">\[in \] Die Komponenten, die mit *src0* verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2d76f-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                  |



 

## <a name="remarks"></a><span data-ttu-id="2d76f-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2d76f-116">Remarks</span></span>

><span data-ttu-id="2d76f-117">= wird anstelle von > verwendet, sodass bei min(x,y) = x dann max(x,y) = y.</span><span class="sxs-lookup"><span data-stu-id="2d76f-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="2d76f-118">NaN verfügt über eine spezielle Behandlung.</span><span class="sxs-lookup"><span data-stu-id="2d76f-118">NaN has special handling.</span></span> <span data-ttu-id="2d76f-119">Wenn ein Quelloperand NaN ist, wird der andere Quelloperand zurückgegeben, und die Auswahl erfolgt pro Komponente.</span><span class="sxs-lookup"><span data-stu-id="2d76f-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="2d76f-120">Wenn beide NaN sind, wird eine beliebige NaN-Darstellung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2d76f-120">If both are NaN, any NaN representation is returned.</span></span> <span data-ttu-id="2d76f-121">Dies entspricht den neuen IEEE 754R-Regeln.</span><span class="sxs-lookup"><span data-stu-id="2d76f-121">This conforms to new IEEE 754R rules.</span></span>

<span data-ttu-id="2d76f-122">Denormen werden geleert, wobei das Vorzeichen vor dem Vergleich beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="2d76f-122">Denorms are flushed, with the sign preserved, before comparison.</span></span> <span data-ttu-id="2d76f-123">Das in *dest* geschriebene Ergebnis kann jedoch denormiert werden.</span><span class="sxs-lookup"><span data-stu-id="2d76f-123">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="2d76f-124">Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Zahlenklassen erzielt werden, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt.</span><span class="sxs-lookup"><span data-stu-id="2d76f-124">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="2d76f-125">F bedeutet endliche reale Zahl.</span><span class="sxs-lookup"><span data-stu-id="2d76f-125">F means finite real number.</span></span>



| <span data-ttu-id="2d76f-126">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="2d76f-126">**src0 src1->**</span></span> | <span data-ttu-id="2d76f-127">**-inf**</span><span class="sxs-lookup"><span data-stu-id="2d76f-127">**-inf**</span></span> | <span data-ttu-id="2d76f-128">**F**</span><span class="sxs-lookup"><span data-stu-id="2d76f-128">**F**</span></span>        | <span data-ttu-id="2d76f-129">**+inf**</span><span class="sxs-lookup"><span data-stu-id="2d76f-129">**+inf**</span></span> | <span data-ttu-id="2d76f-130">**NaN**</span><span class="sxs-lookup"><span data-stu-id="2d76f-130">**NaN**</span></span> |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="2d76f-131">**-inf**</span><span class="sxs-lookup"><span data-stu-id="2d76f-131">**-inf**</span></span>           | <span data-ttu-id="2d76f-132">-inf</span><span class="sxs-lookup"><span data-stu-id="2d76f-132">-inf</span></span>     | <span data-ttu-id="2d76f-133">-inf</span><span class="sxs-lookup"><span data-stu-id="2d76f-133">-inf</span></span>         | <span data-ttu-id="2d76f-134">-inf</span><span class="sxs-lookup"><span data-stu-id="2d76f-134">-inf</span></span>     | <span data-ttu-id="2d76f-135">-inf</span><span class="sxs-lookup"><span data-stu-id="2d76f-135">-inf</span></span>    |
| <span data-ttu-id="2d76f-136">**F**</span><span class="sxs-lookup"><span data-stu-id="2d76f-136">**F**</span></span>              | <span data-ttu-id="2d76f-137">-inf</span><span class="sxs-lookup"><span data-stu-id="2d76f-137">-inf</span></span>     | <span data-ttu-id="2d76f-138">src0 oder src1</span><span class="sxs-lookup"><span data-stu-id="2d76f-138">src0 or src1</span></span> | <span data-ttu-id="2d76f-139">src0</span><span class="sxs-lookup"><span data-stu-id="2d76f-139">src0</span></span>     | <span data-ttu-id="2d76f-140">src0</span><span class="sxs-lookup"><span data-stu-id="2d76f-140">src0</span></span>    |
| <span data-ttu-id="2d76f-141">**-inf**</span><span class="sxs-lookup"><span data-stu-id="2d76f-141">**-inf**</span></span>           | <span data-ttu-id="2d76f-142">-inf</span><span class="sxs-lookup"><span data-stu-id="2d76f-142">-inf</span></span>     | <span data-ttu-id="2d76f-143">src1</span><span class="sxs-lookup"><span data-stu-id="2d76f-143">src1</span></span>         | <span data-ttu-id="2d76f-144">+inf</span><span class="sxs-lookup"><span data-stu-id="2d76f-144">+inf</span></span>     | <span data-ttu-id="2d76f-145">+inf</span><span class="sxs-lookup"><span data-stu-id="2d76f-145">+inf</span></span>    |
| <span data-ttu-id="2d76f-146">**NaN**</span><span class="sxs-lookup"><span data-stu-id="2d76f-146">**NaN**</span></span>            | <span data-ttu-id="2d76f-147">-inf</span><span class="sxs-lookup"><span data-stu-id="2d76f-147">-inf</span></span>     | <span data-ttu-id="2d76f-148">src1</span><span class="sxs-lookup"><span data-stu-id="2d76f-148">src1</span></span>         | <span data-ttu-id="2d76f-149">+inf</span><span class="sxs-lookup"><span data-stu-id="2d76f-149">+inf</span></span>     | <span data-ttu-id="2d76f-150">NaN</span><span class="sxs-lookup"><span data-stu-id="2d76f-150">NaN</span></span>     |



 

<span data-ttu-id="2d76f-151">Diese Anweisung gilt für die folgenden Shaderstufen:</span><span class="sxs-lookup"><span data-stu-id="2d76f-151">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2d76f-152">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="2d76f-152">Vertex Shader</span></span> | <span data-ttu-id="2d76f-153">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="2d76f-153">Geometry Shader</span></span> | <span data-ttu-id="2d76f-154">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="2d76f-154">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2d76f-155">x</span><span class="sxs-lookup"><span data-stu-id="2d76f-155">x</span></span>             | <span data-ttu-id="2d76f-156">x</span><span class="sxs-lookup"><span data-stu-id="2d76f-156">x</span></span>               | <span data-ttu-id="2d76f-157">x</span><span class="sxs-lookup"><span data-stu-id="2d76f-157">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2d76f-158">Minimales Shadermodell</span><span class="sxs-lookup"><span data-stu-id="2d76f-158">Minimum Shader Model</span></span>

<span data-ttu-id="2d76f-159">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2d76f-159">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2d76f-160">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="2d76f-160">Shader Model</span></span>                                              | <span data-ttu-id="2d76f-161">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="2d76f-161">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2d76f-162">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="2d76f-162">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2d76f-163">ja</span><span class="sxs-lookup"><span data-stu-id="2d76f-163">yes</span></span>       |
| [<span data-ttu-id="2d76f-164">Shadermodell 4.1</span><span class="sxs-lookup"><span data-stu-id="2d76f-164">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2d76f-165">ja</span><span class="sxs-lookup"><span data-stu-id="2d76f-165">yes</span></span>       |
| [<span data-ttu-id="2d76f-166">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="2d76f-166">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2d76f-167">ja</span><span class="sxs-lookup"><span data-stu-id="2d76f-167">yes</span></span>       |
| [<span data-ttu-id="2d76f-168">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d76f-168">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2d76f-169">nein</span><span class="sxs-lookup"><span data-stu-id="2d76f-169">no</span></span>        |
| [<span data-ttu-id="2d76f-170">Shadermodell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d76f-170">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2d76f-171">nein</span><span class="sxs-lookup"><span data-stu-id="2d76f-171">no</span></span>        |
| [<span data-ttu-id="2d76f-172">Shadermodell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d76f-172">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2d76f-173">nein</span><span class="sxs-lookup"><span data-stu-id="2d76f-173">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2d76f-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2d76f-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d76f-175">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d76f-175">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





