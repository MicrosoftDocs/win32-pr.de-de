---
title: SQRT (SM4-ASM)
description: Komponenten Weise Quadratwurzel.
ms.assetid: B860D656-7F01-484F-909F-A5C9A61C52C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0a12afaf5b2366dac15c953d509a6814b48a6b9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389542"
---
# <a name="sqrt-sm4---asm"></a><span data-ttu-id="3f40d-103">SQRT (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="3f40d-103">sqrt (sm4 - asm)</span></span>

<span data-ttu-id="3f40d-104">Komponenten Weise Quadratwurzel.</span><span class="sxs-lookup"><span data-stu-id="3f40d-104">Component-wise square root.</span></span>



| <span data-ttu-id="3f40d-105">Sqrt \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="3f40d-105">sqrt\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="3f40d-106">Element</span><span class="sxs-lookup"><span data-stu-id="3f40d-106">Item</span></span>                                                            | <span data-ttu-id="3f40d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f40d-107">Description</span></span>                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="3f40d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="3f40d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="3f40d-109">\[im \] Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="3f40d-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="3f40d-110">*dest* = sqrt (*src0*)</span><span class="sxs-lookup"><span data-stu-id="3f40d-110">*dest* = sqrt(*src0*)</span></span><br/> |
| <span data-ttu-id="3f40d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="3f40d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="3f40d-112">\[in \] den Komponenten, für die die Quadratwurzel übernommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f40d-112">\[in\] The components for which to take the square root.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="3f40d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f40d-113">Remarks</span></span>

<span data-ttu-id="3f40d-114">Genauigkeit ist 1 ULP.</span><span class="sxs-lookup"><span data-stu-id="3f40d-114">Precision is 1 ulp.</span></span>

<span data-ttu-id="3f40d-115">In der folgenden Tabelle werden die Ergebnisse angezeigt, die bei der Ausführung der Anweisung mit verschiedenen Klassen von Zahlen erzielt wurden, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt</span><span class="sxs-lookup"><span data-stu-id="3f40d-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="3f40d-116">F bedeutet eine endliche reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="3f40d-116">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
|          | <span data-ttu-id="3f40d-117">**-INF**</span><span class="sxs-lookup"><span data-stu-id="3f40d-117">**-inf**</span></span> | <span data-ttu-id="3f40d-118">**-F**</span><span class="sxs-lookup"><span data-stu-id="3f40d-118">**-F**</span></span> | <span data-ttu-id="3f40d-119">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="3f40d-119">**-denorm**</span></span> | <span data-ttu-id="3f40d-120">**-0**</span><span class="sxs-lookup"><span data-stu-id="3f40d-120">**-0**</span></span> | <span data-ttu-id="3f40d-121">**+0**</span><span class="sxs-lookup"><span data-stu-id="3f40d-121">**+0**</span></span> | <span data-ttu-id="3f40d-122">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="3f40d-122">**+denorm**</span></span> | <span data-ttu-id="3f40d-123">**+ F**</span><span class="sxs-lookup"><span data-stu-id="3f40d-123">**+F**</span></span> | <span data-ttu-id="3f40d-124">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="3f40d-124">**+inf**</span></span> | <span data-ttu-id="3f40d-125">**NaN**</span><span class="sxs-lookup"><span data-stu-id="3f40d-125">**NaN**</span></span> |
| <span data-ttu-id="3f40d-126">**dest**</span><span class="sxs-lookup"><span data-stu-id="3f40d-126">**dest**</span></span> | <span data-ttu-id="3f40d-127">NaN</span><span class="sxs-lookup"><span data-stu-id="3f40d-127">NaN</span></span>      | <span data-ttu-id="3f40d-128">NaN</span><span class="sxs-lookup"><span data-stu-id="3f40d-128">NaN</span></span>    | <span data-ttu-id="3f40d-129">-0</span><span class="sxs-lookup"><span data-stu-id="3f40d-129">-0</span></span>          | <span data-ttu-id="3f40d-130">-0</span><span class="sxs-lookup"><span data-stu-id="3f40d-130">-0</span></span>     | <span data-ttu-id="3f40d-131">+0</span><span class="sxs-lookup"><span data-stu-id="3f40d-131">+0</span></span>     | <span data-ttu-id="3f40d-132">+0</span><span class="sxs-lookup"><span data-stu-id="3f40d-132">+0</span></span>          | <span data-ttu-id="3f40d-133">+ F</span><span class="sxs-lookup"><span data-stu-id="3f40d-133">+F</span></span>     | <span data-ttu-id="3f40d-134">+inf</span><span class="sxs-lookup"><span data-stu-id="3f40d-134">+inf</span></span>     | <span data-ttu-id="3f40d-135">NaN</span><span class="sxs-lookup"><span data-stu-id="3f40d-135">NaN</span></span>     |



 

<span data-ttu-id="3f40d-136">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="3f40d-136">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3f40d-137">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="3f40d-137">Vertex Shader</span></span> | <span data-ttu-id="3f40d-138">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="3f40d-138">Geometry Shader</span></span> | <span data-ttu-id="3f40d-139">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="3f40d-139">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="3f40d-140">x</span><span class="sxs-lookup"><span data-stu-id="3f40d-140">x</span></span>             | <span data-ttu-id="3f40d-141">x</span><span class="sxs-lookup"><span data-stu-id="3f40d-141">x</span></span>               | <span data-ttu-id="3f40d-142">x</span><span class="sxs-lookup"><span data-stu-id="3f40d-142">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3f40d-143">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="3f40d-143">Minimum Shader Model</span></span>

<span data-ttu-id="3f40d-144">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3f40d-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3f40d-145">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="3f40d-145">Shader Model</span></span>                                              | <span data-ttu-id="3f40d-146">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="3f40d-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3f40d-147">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="3f40d-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3f40d-148">ja</span><span class="sxs-lookup"><span data-stu-id="3f40d-148">yes</span></span>       |
| [<span data-ttu-id="3f40d-149">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="3f40d-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3f40d-150">ja</span><span class="sxs-lookup"><span data-stu-id="3f40d-150">yes</span></span>       |
| [<span data-ttu-id="3f40d-151">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="3f40d-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3f40d-152">ja</span><span class="sxs-lookup"><span data-stu-id="3f40d-152">yes</span></span>       |
| [<span data-ttu-id="3f40d-153">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3f40d-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3f40d-154">nein</span><span class="sxs-lookup"><span data-stu-id="3f40d-154">no</span></span>        |
| [<span data-ttu-id="3f40d-155">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3f40d-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3f40d-156">nein</span><span class="sxs-lookup"><span data-stu-id="3f40d-156">no</span></span>        |
| [<span data-ttu-id="3f40d-157">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3f40d-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3f40d-158">nein</span><span class="sxs-lookup"><span data-stu-id="3f40d-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3f40d-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3f40d-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f40d-160">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3f40d-160">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





