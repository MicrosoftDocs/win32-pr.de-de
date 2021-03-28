---
title: min (SM4-ASM)
description: Minimaler Gleit Komma Wert für die Komponente.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e584aee077735b717bf76d148d4d0db4357a7d95
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101106"
---
# <a name="min-sm4---asm"></a><span data-ttu-id="eff36-103">min (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="eff36-103">min (sm4 - asm)</span></span>

<span data-ttu-id="eff36-104">Minimaler Gleit Komma Wert für die Komponente.</span><span class="sxs-lookup"><span data-stu-id="eff36-104">Component-wise float minimum.</span></span>



| <span data-ttu-id="eff36-105">Min \[ \_ \] . SA dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="eff36-105">min\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="eff36-106">Element</span><span class="sxs-lookup"><span data-stu-id="eff36-106">Item</span></span>                                                            | <span data-ttu-id="eff36-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eff36-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eff36-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="eff36-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="eff36-109">\[im \] Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="eff36-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="eff36-110">*dest*  =  *src0*  <  *Quelle1* ?</span><span class="sxs-lookup"><span data-stu-id="eff36-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="eff36-111">*src0* : *Quelle1*</span><span class="sxs-lookup"><span data-stu-id="eff36-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="eff36-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="eff36-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="eff36-113">\[in \] den Komponenten, die mit *Quelle1* verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eff36-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                  |
| <span data-ttu-id="eff36-114"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="eff36-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="eff36-115">\[in \] den Komponenten, die mit *src0* verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eff36-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                  |



 

## <a name="remarks"></a><span data-ttu-id="eff36-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eff36-116">Remarks</span></span>

><span data-ttu-id="eff36-117">= wird anstelle von > verwendet, sodass, wenn min (x, y) = x, dann Max (x, y) = y ist.</span><span class="sxs-lookup"><span data-stu-id="eff36-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="eff36-118">Nan hat eine besondere Behandlung.</span><span class="sxs-lookup"><span data-stu-id="eff36-118">NaN has special handling.</span></span> <span data-ttu-id="eff36-119">Wenn ein Quell Operand NaN ist, wird der andere Quell Operand zurückgegeben, und die Auswahl erfolgt pro Komponente.</span><span class="sxs-lookup"><span data-stu-id="eff36-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="eff36-120">Wenn beide Nan sind, wird eine Nan-Darstellung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eff36-120">If both are NaN, any NaN representation is returned.</span></span> <span data-ttu-id="eff36-121">Dies entspricht neuen IEEE 754r-Regeln.</span><span class="sxs-lookup"><span data-stu-id="eff36-121">This conforms to new IEEE 754R rules.</span></span>

<span data-ttu-id="eff36-122">Denorms werden vor dem Vergleich geleert, wobei das Vorzeichen beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="eff36-122">Denorms are flushed, with the sign preserved, before comparison.</span></span> <span data-ttu-id="eff36-123">Das in *dest* geschriebene Ergebnis wird jedoch möglicherweise nicht denorm geleert.</span><span class="sxs-lookup"><span data-stu-id="eff36-123">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="eff36-124">In der folgenden Tabelle werden die Ergebnisse angezeigt, die bei der Ausführung der Anweisung mit verschiedenen Klassen von Zahlen erzielt wurden, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt</span><span class="sxs-lookup"><span data-stu-id="eff36-124">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="eff36-125">F bedeutet eine begrenzte reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="eff36-125">F means finite real number.</span></span>



|                    |          |              |          |         |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="eff36-126">**src0 Quelle1->**</span><span class="sxs-lookup"><span data-stu-id="eff36-126">**src0 src1->**</span></span> | <span data-ttu-id="eff36-127">**-INF**</span><span class="sxs-lookup"><span data-stu-id="eff36-127">**-inf**</span></span> | <span data-ttu-id="eff36-128">**F**</span><span class="sxs-lookup"><span data-stu-id="eff36-128">**F**</span></span>        | <span data-ttu-id="eff36-129">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="eff36-129">**+inf**</span></span> | <span data-ttu-id="eff36-130">**NaN**</span><span class="sxs-lookup"><span data-stu-id="eff36-130">**NaN**</span></span> |
| <span data-ttu-id="eff36-131">**-INF**</span><span class="sxs-lookup"><span data-stu-id="eff36-131">**-inf**</span></span>           | <span data-ttu-id="eff36-132">-inf</span><span class="sxs-lookup"><span data-stu-id="eff36-132">-inf</span></span>     | <span data-ttu-id="eff36-133">-inf</span><span class="sxs-lookup"><span data-stu-id="eff36-133">-inf</span></span>         | <span data-ttu-id="eff36-134">-inf</span><span class="sxs-lookup"><span data-stu-id="eff36-134">-inf</span></span>     | <span data-ttu-id="eff36-135">-inf</span><span class="sxs-lookup"><span data-stu-id="eff36-135">-inf</span></span>    |
| <span data-ttu-id="eff36-136">**F**</span><span class="sxs-lookup"><span data-stu-id="eff36-136">**F**</span></span>              | <span data-ttu-id="eff36-137">-inf</span><span class="sxs-lookup"><span data-stu-id="eff36-137">-inf</span></span>     | <span data-ttu-id="eff36-138">src0 oder Quelle1</span><span class="sxs-lookup"><span data-stu-id="eff36-138">src0 or src1</span></span> | <span data-ttu-id="eff36-139">src0</span><span class="sxs-lookup"><span data-stu-id="eff36-139">src0</span></span>     | <span data-ttu-id="eff36-140">src0</span><span class="sxs-lookup"><span data-stu-id="eff36-140">src0</span></span>    |
| <span data-ttu-id="eff36-141">**-INF**</span><span class="sxs-lookup"><span data-stu-id="eff36-141">**-inf**</span></span>           | <span data-ttu-id="eff36-142">-inf</span><span class="sxs-lookup"><span data-stu-id="eff36-142">-inf</span></span>     | <span data-ttu-id="eff36-143">src1</span><span class="sxs-lookup"><span data-stu-id="eff36-143">src1</span></span>         | <span data-ttu-id="eff36-144">+inf</span><span class="sxs-lookup"><span data-stu-id="eff36-144">+inf</span></span>     | <span data-ttu-id="eff36-145">+inf</span><span class="sxs-lookup"><span data-stu-id="eff36-145">+inf</span></span>    |
| <span data-ttu-id="eff36-146">**NaN**</span><span class="sxs-lookup"><span data-stu-id="eff36-146">**NaN**</span></span>            | <span data-ttu-id="eff36-147">-inf</span><span class="sxs-lookup"><span data-stu-id="eff36-147">-inf</span></span>     | <span data-ttu-id="eff36-148">src1</span><span class="sxs-lookup"><span data-stu-id="eff36-148">src1</span></span>         | <span data-ttu-id="eff36-149">+inf</span><span class="sxs-lookup"><span data-stu-id="eff36-149">+inf</span></span>     | <span data-ttu-id="eff36-150">NaN</span><span class="sxs-lookup"><span data-stu-id="eff36-150">NaN</span></span>     |



 

<span data-ttu-id="eff36-151">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="eff36-151">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="eff36-152">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="eff36-152">Vertex Shader</span></span> | <span data-ttu-id="eff36-153">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="eff36-153">Geometry Shader</span></span> | <span data-ttu-id="eff36-154">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="eff36-154">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="eff36-155">x</span><span class="sxs-lookup"><span data-stu-id="eff36-155">x</span></span>             | <span data-ttu-id="eff36-156">x</span><span class="sxs-lookup"><span data-stu-id="eff36-156">x</span></span>               | <span data-ttu-id="eff36-157">x</span><span class="sxs-lookup"><span data-stu-id="eff36-157">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="eff36-158">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="eff36-158">Minimum Shader Model</span></span>

<span data-ttu-id="eff36-159">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eff36-159">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="eff36-160">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="eff36-160">Shader Model</span></span>                                              | <span data-ttu-id="eff36-161">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="eff36-161">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="eff36-162">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="eff36-162">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="eff36-163">ja</span><span class="sxs-lookup"><span data-stu-id="eff36-163">yes</span></span>       |
| [<span data-ttu-id="eff36-164">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="eff36-164">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="eff36-165">ja</span><span class="sxs-lookup"><span data-stu-id="eff36-165">yes</span></span>       |
| [<span data-ttu-id="eff36-166">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="eff36-166">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="eff36-167">ja</span><span class="sxs-lookup"><span data-stu-id="eff36-167">yes</span></span>       |
| [<span data-ttu-id="eff36-168">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eff36-168">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="eff36-169">nein</span><span class="sxs-lookup"><span data-stu-id="eff36-169">no</span></span>        |
| [<span data-ttu-id="eff36-170">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eff36-170">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="eff36-171">nein</span><span class="sxs-lookup"><span data-stu-id="eff36-171">no</span></span>        |
| [<span data-ttu-id="eff36-172">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eff36-172">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="eff36-173">nein</span><span class="sxs-lookup"><span data-stu-id="eff36-173">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="eff36-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eff36-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eff36-175">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eff36-175">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





