---
title: DRCP (SM5-ASM)
description: Berechnet eine gegenseitige Komponenten Weise doppelte Genauigkeit.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b678f4e8b3464817215de9132298fdde1f6feec
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313692"
---
# <a name="drcp-sm5---asm"></a><span data-ttu-id="9204a-103">DRCP (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="9204a-103">drcp (sm5 - asm)</span></span>

<span data-ttu-id="9204a-104">Berechnet eine gegenseitige Komponenten Weise doppelte Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="9204a-104">Computes a component-wise double-precision reciprocal.</span></span>



| <span data-ttu-id="9204a-105">RCP \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="9204a-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="9204a-106">Element</span><span class="sxs-lookup"><span data-stu-id="9204a-106">Item</span></span>                                                            | <span data-ttu-id="9204a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9204a-107">Description</span></span>                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9204a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="9204a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="9204a-109">\[in \] der Adresse der Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="9204a-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="9204a-110">*dest*  =  **1,0**  /  *src0*.</span><span class="sxs-lookup"><span data-stu-id="9204a-110">*dest* = **1.0** / *src0*.</span></span> <span data-ttu-id="9204a-111">Der Ergebniswert muss auf 1,0 ULP genau sein.</span><span class="sxs-lookup"><span data-stu-id="9204a-111">The result value must be accurate to 1.0 ULP</span></span><br/> |
| <span data-ttu-id="9204a-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9204a-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9204a-113">\[in \] der Zahl, von der die gegenseitige übernommen wird.</span><span class="sxs-lookup"><span data-stu-id="9204a-113">\[in\] The number to take the reciprocal of.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="9204a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9204a-114">Remarks</span></span>

<span data-ttu-id="9204a-115">Die DRCP-Anweisung wird vom HLSL-Compiler nur ausgegeben, wenn Sie explizit über die systeminterne Funktion RCP () aufgerufen wird, wenn ein Double als Argument verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9204a-115">The DRCP instruction is emitted by the HLSL compiler only when explicitly called via the rcp() intrinsic, when a double is used as the argument.</span></span> <span data-ttu-id="9204a-116">Die Genauigkeit dieser Anweisung muss 1,0 ULP sein.</span><span class="sxs-lookup"><span data-stu-id="9204a-116">The accuracy of this instruction is required to be 1.0 ULP.</span></span>

<span data-ttu-id="9204a-117">Shader, die diese Anweisung verwenden, werden mit einem shaderflag gekennzeichnet, das dazu führt, dass Sie nicht gebunden werden, es sei denn, die folgenden Bedingungen sind erfüllt.</span><span class="sxs-lookup"><span data-stu-id="9204a-117">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="9204a-118">Das System unterstützt DirectX 11,1.</span><span class="sxs-lookup"><span data-stu-id="9204a-118">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="9204a-119">Das System enthält einen WDDM 1,2-Treiber.</span><span class="sxs-lookup"><span data-stu-id="9204a-119">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="9204a-120">Der Treiber meldet die Unterstützung für diese Anweisung über **D3D11 \_ Feature \_ Data \_ D3D11 \_ options. "Extendeddoublesshaderinstructions** " ist auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9204a-120">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="9204a-121">In der folgenden Tabelle werden die Ergebnisse angezeigt, die bei der Ausführung der Anweisung mit verschiedenen Klassen von Zahlen erzielt wurden, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt</span><span class="sxs-lookup"><span data-stu-id="9204a-121">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="9204a-122">In dieser Tabelle steht F für eine endliche reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="9204a-122">In this table F means finite-real number.</span></span>



|               |          |        |        |        |        |          |         |
|---------------|----------|--------|--------|--------|--------|----------|---------|
| <span data-ttu-id="9204a-123">**src**-></span><span class="sxs-lookup"><span data-stu-id="9204a-123">**src**-></span></span>  | <span data-ttu-id="9204a-124">**-INF**</span><span class="sxs-lookup"><span data-stu-id="9204a-124">**-inf**</span></span> | <span data-ttu-id="9204a-125">**-F**</span><span class="sxs-lookup"><span data-stu-id="9204a-125">**-F**</span></span> | <span data-ttu-id="9204a-126">**-0**</span><span class="sxs-lookup"><span data-stu-id="9204a-126">**-0**</span></span> | <span data-ttu-id="9204a-127">**+0**</span><span class="sxs-lookup"><span data-stu-id="9204a-127">**+0**</span></span> | <span data-ttu-id="9204a-128">**+ F**</span><span class="sxs-lookup"><span data-stu-id="9204a-128">**+F**</span></span> | <span data-ttu-id="9204a-129">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="9204a-129">**+inf**</span></span> | <span data-ttu-id="9204a-130">**NaN**</span><span class="sxs-lookup"><span data-stu-id="9204a-130">**NaN**</span></span> |
| <span data-ttu-id="9204a-131">**dest**-></span><span class="sxs-lookup"><span data-stu-id="9204a-131">**dest**-></span></span> | <span data-ttu-id="9204a-132">-0</span><span class="sxs-lookup"><span data-stu-id="9204a-132">-0</span></span>       | <span data-ttu-id="9204a-133">-F</span><span class="sxs-lookup"><span data-stu-id="9204a-133">-F</span></span>     | <span data-ttu-id="9204a-134">-inf</span><span class="sxs-lookup"><span data-stu-id="9204a-134">-inf</span></span>   | <span data-ttu-id="9204a-135">+inf</span><span class="sxs-lookup"><span data-stu-id="9204a-135">+inf</span></span>   | <span data-ttu-id="9204a-136">+ F</span><span class="sxs-lookup"><span data-stu-id="9204a-136">+F</span></span>     | <span data-ttu-id="9204a-137">+0</span><span class="sxs-lookup"><span data-stu-id="9204a-137">+0</span></span>       | <span data-ttu-id="9204a-138">NaN</span><span class="sxs-lookup"><span data-stu-id="9204a-138">NaN</span></span>     |



 

<span data-ttu-id="9204a-139">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="9204a-139">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9204a-140">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="9204a-140">Vertex</span></span> | <span data-ttu-id="9204a-141">Hülle</span><span class="sxs-lookup"><span data-stu-id="9204a-141">Hull</span></span> | <span data-ttu-id="9204a-142">Domain</span><span class="sxs-lookup"><span data-stu-id="9204a-142">Domain</span></span> | <span data-ttu-id="9204a-143">Geometrie</span><span class="sxs-lookup"><span data-stu-id="9204a-143">Geometry</span></span> | <span data-ttu-id="9204a-144">Pixel</span><span class="sxs-lookup"><span data-stu-id="9204a-144">Pixel</span></span> | <span data-ttu-id="9204a-145">Compute</span><span class="sxs-lookup"><span data-stu-id="9204a-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9204a-146">X</span><span class="sxs-lookup"><span data-stu-id="9204a-146">X</span></span>      | <span data-ttu-id="9204a-147">X</span><span class="sxs-lookup"><span data-stu-id="9204a-147">X</span></span>    | <span data-ttu-id="9204a-148">X</span><span class="sxs-lookup"><span data-stu-id="9204a-148">X</span></span>      | <span data-ttu-id="9204a-149">X</span><span class="sxs-lookup"><span data-stu-id="9204a-149">X</span></span>        | <span data-ttu-id="9204a-150">X</span><span class="sxs-lookup"><span data-stu-id="9204a-150">X</span></span>     | <span data-ttu-id="9204a-151">X</span><span class="sxs-lookup"><span data-stu-id="9204a-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9204a-152">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="9204a-152">Minimum Shader Model</span></span>

<span data-ttu-id="9204a-153">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="9204a-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="9204a-154">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="9204a-154">Shader Model</span></span>                                              | <span data-ttu-id="9204a-155">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="9204a-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9204a-156">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="9204a-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9204a-157">ja</span><span class="sxs-lookup"><span data-stu-id="9204a-157">yes</span></span>       |
| [<span data-ttu-id="9204a-158">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="9204a-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9204a-159">nein</span><span class="sxs-lookup"><span data-stu-id="9204a-159">no</span></span>        |
| [<span data-ttu-id="9204a-160">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="9204a-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9204a-161">nein</span><span class="sxs-lookup"><span data-stu-id="9204a-161">no</span></span>        |
| [<span data-ttu-id="9204a-162">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9204a-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9204a-163">nein</span><span class="sxs-lookup"><span data-stu-id="9204a-163">no</span></span>        |
| [<span data-ttu-id="9204a-164">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9204a-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9204a-165">nein</span><span class="sxs-lookup"><span data-stu-id="9204a-165">no</span></span>        |
| [<span data-ttu-id="9204a-166">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9204a-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9204a-167">nein</span><span class="sxs-lookup"><span data-stu-id="9204a-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9204a-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9204a-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9204a-169">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9204a-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





