---
title: Exp (SM4-ASM)
description: Komponenten weiser 2exponent.
ms.assetid: 12EB865A-BF71-4B4B-854F-9DA056B18AE0
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 774be1230bdb02a6179ea5662ca2237c2cefc200
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038310"
---
# <a name="exp-sm4---asm"></a><span data-ttu-id="c7f22-103">Exp (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c7f22-103">exp (sm4 - asm)</span></span>

<span data-ttu-id="c7f22-104">Komponenten weiser 2exponent.</span><span class="sxs-lookup"><span data-stu-id="c7f22-104">Component-wise 2exponent.</span></span>



| <span data-ttu-id="c7f22-105">exp \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="c7f22-105">exp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="c7f22-106">Element</span><span class="sxs-lookup"><span data-stu-id="c7f22-106">Item</span></span>                                                            | <span data-ttu-id="c7f22-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7f22-107">Description</span></span>                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="c7f22-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c7f22-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="c7f22-109">\[im \] Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="c7f22-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="c7f22-110">*dest* = 2 *src0*</span><span class="sxs-lookup"><span data-stu-id="c7f22-110">*dest* = 2 *src0*</span></span><br/> |
| <span data-ttu-id="c7f22-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c7f22-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c7f22-112">\[im \] Exponenten.</span><span class="sxs-lookup"><span data-stu-id="c7f22-112">\[in\] The exponent.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="c7f22-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7f22-113">Remarks</span></span>

<span data-ttu-id="c7f22-114">Diese Anweisung folgt der Limit-Theorie.</span><span class="sxs-lookup"><span data-stu-id="c7f22-114">This instruction follows limit theory.</span></span> <span data-ttu-id="c7f22-115">Der maximale relative Fehler ist 2-21.</span><span class="sxs-lookup"><span data-stu-id="c7f22-115">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="c7f22-116">In der folgenden Tabelle werden die Ergebnisse angezeigt, die bei der Ausführung der Anweisung mit verschiedenen Klassen von Zahlen erzielt wurden, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt</span><span class="sxs-lookup"><span data-stu-id="c7f22-116">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="c7f22-117">In dieser Tabelle steht F für eine endliche reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="c7f22-117">In this table F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="c7f22-118">**src**</span><span class="sxs-lookup"><span data-stu-id="c7f22-118">**src**</span></span>  | <span data-ttu-id="c7f22-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="c7f22-119">**-inf**</span></span> | <span data-ttu-id="c7f22-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="c7f22-120">**-F**</span></span> | <span data-ttu-id="c7f22-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="c7f22-121">**-denorm**</span></span> | <span data-ttu-id="c7f22-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="c7f22-122">**-0**</span></span> | <span data-ttu-id="c7f22-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="c7f22-123">**+0**</span></span> | <span data-ttu-id="c7f22-124">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="c7f22-124">**+denorm**</span></span> | <span data-ttu-id="c7f22-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="c7f22-125">**+F**</span></span> | <span data-ttu-id="c7f22-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="c7f22-126">**+inf**</span></span> | <span data-ttu-id="c7f22-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="c7f22-127">**NaN**</span></span> |
| <span data-ttu-id="c7f22-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="c7f22-128">**dest**</span></span> | <span data-ttu-id="c7f22-129">0</span><span class="sxs-lookup"><span data-stu-id="c7f22-129">0</span></span>        | <span data-ttu-id="c7f22-130">+ F</span><span class="sxs-lookup"><span data-stu-id="c7f22-130">+F</span></span>     | <span data-ttu-id="c7f22-131">1</span><span class="sxs-lookup"><span data-stu-id="c7f22-131">1</span></span>           | <span data-ttu-id="c7f22-132">1</span><span class="sxs-lookup"><span data-stu-id="c7f22-132">1</span></span>      | <span data-ttu-id="c7f22-133">1</span><span class="sxs-lookup"><span data-stu-id="c7f22-133">1</span></span>      | <span data-ttu-id="c7f22-134">1</span><span class="sxs-lookup"><span data-stu-id="c7f22-134">1</span></span>           | <span data-ttu-id="c7f22-135">+ F</span><span class="sxs-lookup"><span data-stu-id="c7f22-135">+F</span></span>     | <span data-ttu-id="c7f22-136">+inf</span><span class="sxs-lookup"><span data-stu-id="c7f22-136">+inf</span></span>     | <span data-ttu-id="c7f22-137">NaN</span><span class="sxs-lookup"><span data-stu-id="c7f22-137">NaN</span></span>     |



 

<span data-ttu-id="c7f22-138">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="c7f22-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c7f22-139">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="c7f22-139">Vertex Shader</span></span> | <span data-ttu-id="c7f22-140">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="c7f22-140">Geometry Shader</span></span> | <span data-ttu-id="c7f22-141">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="c7f22-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c7f22-142">x</span><span class="sxs-lookup"><span data-stu-id="c7f22-142">x</span></span>             | <span data-ttu-id="c7f22-143">x</span><span class="sxs-lookup"><span data-stu-id="c7f22-143">x</span></span>               | <span data-ttu-id="c7f22-144">x</span><span class="sxs-lookup"><span data-stu-id="c7f22-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c7f22-145">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="c7f22-145">Minimum Shader Model</span></span>

<span data-ttu-id="c7f22-146">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c7f22-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c7f22-147">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="c7f22-147">Shader Model</span></span>                                              | <span data-ttu-id="c7f22-148">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="c7f22-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c7f22-149">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="c7f22-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c7f22-150">ja</span><span class="sxs-lookup"><span data-stu-id="c7f22-150">yes</span></span>       |
| [<span data-ttu-id="c7f22-151">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="c7f22-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c7f22-152">ja</span><span class="sxs-lookup"><span data-stu-id="c7f22-152">yes</span></span>       |
| [<span data-ttu-id="c7f22-153">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="c7f22-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c7f22-154">ja</span><span class="sxs-lookup"><span data-stu-id="c7f22-154">yes</span></span>       |
| [<span data-ttu-id="c7f22-155">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7f22-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c7f22-156">nein</span><span class="sxs-lookup"><span data-stu-id="c7f22-156">no</span></span>        |
| [<span data-ttu-id="c7f22-157">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7f22-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c7f22-158">nein</span><span class="sxs-lookup"><span data-stu-id="c7f22-158">no</span></span>        |
| [<span data-ttu-id="c7f22-159">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7f22-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c7f22-160">nein</span><span class="sxs-lookup"><span data-stu-id="c7f22-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c7f22-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c7f22-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7f22-162">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7f22-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





