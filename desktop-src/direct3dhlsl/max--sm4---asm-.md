---
title: Max (SM4-ASM)
description: Der Komponenten Weise Gleit Komma Wert.
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f24618897eacf250f2b924f6dde3745a32a7172
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389501"
---
# <a name="max-sm4---asm"></a><span data-ttu-id="483b6-103">Max (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="483b6-103">max (sm4 - asm)</span></span>

<span data-ttu-id="483b6-104">Der Komponenten Weise Gleit Komma Wert.</span><span class="sxs-lookup"><span data-stu-id="483b6-104">Component-wise float maximum.</span></span>



| <span data-ttu-id="483b6-105">Max \[ \_ \] . Sat dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="483b6-105">max\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="483b6-106">Element</span><span class="sxs-lookup"><span data-stu-id="483b6-106">Item</span></span>                                                            | <span data-ttu-id="483b6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="483b6-107">Description</span></span>                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="483b6-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="483b6-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="483b6-109">\[im \] Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="483b6-109">\[in\] The result of the operation.</span></span> <br/> <span data-ttu-id="483b6-110">*dest*  =  *src0*  >=  *Quelle1* ?</span><span class="sxs-lookup"><span data-stu-id="483b6-110">*dest* = *src0* >= *src1* ?</span></span> <span data-ttu-id="483b6-111">*src0* : *Quelle1*</span><span class="sxs-lookup"><span data-stu-id="483b6-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="483b6-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="483b6-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="483b6-113">\[in \] den Komponenten, die mit *Quelle1* verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="483b6-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                    |
| <span data-ttu-id="483b6-114"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="483b6-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="483b6-115">\[in \] den Komponenten, die mit *src0* verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="483b6-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="483b6-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="483b6-116">Remarks</span></span>

><span data-ttu-id="483b6-117">= wird anstelle von > verwendet, sodass, wenn min (x, y) = x, dann Max (x, y) = y ist.</span><span class="sxs-lookup"><span data-stu-id="483b6-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="483b6-118">Nan hat eine besondere Behandlung.</span><span class="sxs-lookup"><span data-stu-id="483b6-118">NaN has special handling.</span></span> <span data-ttu-id="483b6-119">Wenn ein Quell Operand NaN ist, wird der andere Quell Operand zurückgegeben, und die Auswahl erfolgt pro Komponente.</span><span class="sxs-lookup"><span data-stu-id="483b6-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="483b6-120">Wenn beide Nan sind, wird eine Nan-Darstellung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="483b6-120">If both are NaN, any NaN representation is returned.</span></span>

<span data-ttu-id="483b6-121">Denorms werden vor dem Vergleich mit einem Vorzeichen geleert.</span><span class="sxs-lookup"><span data-stu-id="483b6-121">Denorms are flushed with sign preserved before the comparison.</span></span> <span data-ttu-id="483b6-122">Das in *dest* geschriebene Ergebnis wird jedoch möglicherweise nicht denorm geleert.</span><span class="sxs-lookup"><span data-stu-id="483b6-122">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="483b6-123">In der folgenden Tabelle werden die Ergebnisse angezeigt, die bei der Ausführung der Anweisung mit verschiedenen Klassen von Zahlen erzielt wurden, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt</span><span class="sxs-lookup"><span data-stu-id="483b6-123">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="483b6-124">F bedeutet eine begrenzte reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="483b6-124">F means finite real number.</span></span>



|                    |          |              |          |         |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="483b6-125">**src0 Quelle1->**</span><span class="sxs-lookup"><span data-stu-id="483b6-125">**src0 src1->**</span></span> | <span data-ttu-id="483b6-126">**-INF**</span><span class="sxs-lookup"><span data-stu-id="483b6-126">**-inf**</span></span> | <span data-ttu-id="483b6-127">**F**</span><span class="sxs-lookup"><span data-stu-id="483b6-127">**F**</span></span>        | <span data-ttu-id="483b6-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="483b6-128">**+inf**</span></span> | <span data-ttu-id="483b6-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="483b6-129">**NaN**</span></span> |
| <span data-ttu-id="483b6-130">**-INF**</span><span class="sxs-lookup"><span data-stu-id="483b6-130">**-inf**</span></span>           | <span data-ttu-id="483b6-131">-inf</span><span class="sxs-lookup"><span data-stu-id="483b6-131">-inf</span></span>     | <span data-ttu-id="483b6-132">src1</span><span class="sxs-lookup"><span data-stu-id="483b6-132">src1</span></span>         | <span data-ttu-id="483b6-133">+inf</span><span class="sxs-lookup"><span data-stu-id="483b6-133">+inf</span></span>     | <span data-ttu-id="483b6-134">-inf</span><span class="sxs-lookup"><span data-stu-id="483b6-134">-inf</span></span>    |
| <span data-ttu-id="483b6-135">**F**</span><span class="sxs-lookup"><span data-stu-id="483b6-135">**F**</span></span>              | <span data-ttu-id="483b6-136">src0</span><span class="sxs-lookup"><span data-stu-id="483b6-136">src0</span></span>     | <span data-ttu-id="483b6-137">src0 oder Quelle1</span><span class="sxs-lookup"><span data-stu-id="483b6-137">src0 or src1</span></span> | <span data-ttu-id="483b6-138">+inf</span><span class="sxs-lookup"><span data-stu-id="483b6-138">+inf</span></span>     | <span data-ttu-id="483b6-139">src0</span><span class="sxs-lookup"><span data-stu-id="483b6-139">src0</span></span>    |
| <span data-ttu-id="483b6-140">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="483b6-140">**+inf**</span></span>           | <span data-ttu-id="483b6-141">+inf</span><span class="sxs-lookup"><span data-stu-id="483b6-141">+inf</span></span>     | <span data-ttu-id="483b6-142">+inf</span><span class="sxs-lookup"><span data-stu-id="483b6-142">+inf</span></span>         | <span data-ttu-id="483b6-143">+inf</span><span class="sxs-lookup"><span data-stu-id="483b6-143">+inf</span></span>     | <span data-ttu-id="483b6-144">+inf</span><span class="sxs-lookup"><span data-stu-id="483b6-144">+inf</span></span>    |
| <span data-ttu-id="483b6-145">**NaN**</span><span class="sxs-lookup"><span data-stu-id="483b6-145">**NaN**</span></span>            | <span data-ttu-id="483b6-146">-inf</span><span class="sxs-lookup"><span data-stu-id="483b6-146">-inf</span></span>     | <span data-ttu-id="483b6-147">src1</span><span class="sxs-lookup"><span data-stu-id="483b6-147">src1</span></span>         | <span data-ttu-id="483b6-148">+inf</span><span class="sxs-lookup"><span data-stu-id="483b6-148">+inf</span></span>     | <span data-ttu-id="483b6-149">NaN</span><span class="sxs-lookup"><span data-stu-id="483b6-149">NaN</span></span>     |



 

<span data-ttu-id="483b6-150">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="483b6-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="483b6-151">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="483b6-151">Vertex Shader</span></span> | <span data-ttu-id="483b6-152">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="483b6-152">Geometry Shader</span></span> | <span data-ttu-id="483b6-153">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="483b6-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="483b6-154">x</span><span class="sxs-lookup"><span data-stu-id="483b6-154">x</span></span>             | <span data-ttu-id="483b6-155">x</span><span class="sxs-lookup"><span data-stu-id="483b6-155">x</span></span>               | <span data-ttu-id="483b6-156">x</span><span class="sxs-lookup"><span data-stu-id="483b6-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="483b6-157">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="483b6-157">Minimum Shader Model</span></span>

<span data-ttu-id="483b6-158">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="483b6-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="483b6-159">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="483b6-159">Shader Model</span></span>                                              | <span data-ttu-id="483b6-160">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="483b6-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="483b6-161">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="483b6-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="483b6-162">ja</span><span class="sxs-lookup"><span data-stu-id="483b6-162">yes</span></span>       |
| [<span data-ttu-id="483b6-163">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="483b6-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="483b6-164">ja</span><span class="sxs-lookup"><span data-stu-id="483b6-164">yes</span></span>       |
| [<span data-ttu-id="483b6-165">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="483b6-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="483b6-166">ja</span><span class="sxs-lookup"><span data-stu-id="483b6-166">yes</span></span>       |
| [<span data-ttu-id="483b6-167">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="483b6-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="483b6-168">nein</span><span class="sxs-lookup"><span data-stu-id="483b6-168">no</span></span>        |
| [<span data-ttu-id="483b6-169">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="483b6-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="483b6-170">nein</span><span class="sxs-lookup"><span data-stu-id="483b6-170">no</span></span>        |
| [<span data-ttu-id="483b6-171">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="483b6-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="483b6-172">nein</span><span class="sxs-lookup"><span data-stu-id="483b6-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="483b6-173">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="483b6-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="483b6-174">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="483b6-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





