---
title: exp (sm4 - asm)
description: Komponentenweise 2exponent.
ms.assetid: 12EB865A-BF71-4B4B-854F-9DA056B18AE0
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b24c74394a5e8ac7a6c945e2c9b63e6f242daa1
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999077"
---
# <a name="exp-sm4---asm"></a><span data-ttu-id="06be9-103">exp (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="06be9-103">exp (sm4 - asm)</span></span>

<span data-ttu-id="06be9-104">Komponentenweise 2exponent.</span><span class="sxs-lookup"><span data-stu-id="06be9-104">Component-wise 2exponent.</span></span>



| <span data-ttu-id="06be9-105">exp \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="06be9-105">exp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="06be9-106">Element</span><span class="sxs-lookup"><span data-stu-id="06be9-106">Item</span></span>                                                            | <span data-ttu-id="06be9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06be9-107">Description</span></span>                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="06be9-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="06be9-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="06be9-109">\[in \] Das Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="06be9-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="06be9-110">*dest* = 2 *src0*</span><span class="sxs-lookup"><span data-stu-id="06be9-110">*dest* = 2 *src0*</span></span><br/> |
| <span data-ttu-id="06be9-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="06be9-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="06be9-112">\[in \] Der Exponent.</span><span class="sxs-lookup"><span data-stu-id="06be9-112">\[in\] The exponent.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="06be9-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="06be9-113">Remarks</span></span>

<span data-ttu-id="06be9-114">Diese Anweisung folgt der Limit-Theorie.</span><span class="sxs-lookup"><span data-stu-id="06be9-114">This instruction follows limit theory.</span></span> <span data-ttu-id="06be9-115">Der maximale relative Fehler ist 2–21.</span><span class="sxs-lookup"><span data-stu-id="06be9-115">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="06be9-116">Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Zahlenklassen erzielt werden, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt.</span><span class="sxs-lookup"><span data-stu-id="06be9-116">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="06be9-117">In dieser Tabelle steht F für finite-real number.</span><span class="sxs-lookup"><span data-stu-id="06be9-117">In this table F means finite-real number.</span></span>



| <span data-ttu-id="06be9-118">**src**</span><span class="sxs-lookup"><span data-stu-id="06be9-118">**src**</span></span>  | <span data-ttu-id="06be9-119">**-inf**</span><span class="sxs-lookup"><span data-stu-id="06be9-119">**-inf**</span></span> | <span data-ttu-id="06be9-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="06be9-120">**-F**</span></span> | <span data-ttu-id="06be9-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="06be9-121">**-denorm**</span></span> | <span data-ttu-id="06be9-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="06be9-122">**-0**</span></span> | <span data-ttu-id="06be9-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="06be9-123">**+0**</span></span> | <span data-ttu-id="06be9-124">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="06be9-124">**+denorm**</span></span> | <span data-ttu-id="06be9-125">**+F**</span><span class="sxs-lookup"><span data-stu-id="06be9-125">**+F**</span></span> | <span data-ttu-id="06be9-126">**+inf**</span><span class="sxs-lookup"><span data-stu-id="06be9-126">**+inf**</span></span> | <span data-ttu-id="06be9-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="06be9-127">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="06be9-128">**Dest**</span><span class="sxs-lookup"><span data-stu-id="06be9-128">**dest**</span></span> | <span data-ttu-id="06be9-129">0</span><span class="sxs-lookup"><span data-stu-id="06be9-129">0</span></span>        | <span data-ttu-id="06be9-130">+F</span><span class="sxs-lookup"><span data-stu-id="06be9-130">+F</span></span>     | <span data-ttu-id="06be9-131">1</span><span class="sxs-lookup"><span data-stu-id="06be9-131">1</span></span>           | <span data-ttu-id="06be9-132">1</span><span class="sxs-lookup"><span data-stu-id="06be9-132">1</span></span>      | <span data-ttu-id="06be9-133">1</span><span class="sxs-lookup"><span data-stu-id="06be9-133">1</span></span>      | <span data-ttu-id="06be9-134">1</span><span class="sxs-lookup"><span data-stu-id="06be9-134">1</span></span>           | <span data-ttu-id="06be9-135">+F</span><span class="sxs-lookup"><span data-stu-id="06be9-135">+F</span></span>     | <span data-ttu-id="06be9-136">+inf</span><span class="sxs-lookup"><span data-stu-id="06be9-136">+inf</span></span>     | <span data-ttu-id="06be9-137">NaN</span><span class="sxs-lookup"><span data-stu-id="06be9-137">NaN</span></span>     |



 

<span data-ttu-id="06be9-138">Diese Anweisung gilt für die folgenden Shaderstufen:</span><span class="sxs-lookup"><span data-stu-id="06be9-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="06be9-139">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="06be9-139">Vertex Shader</span></span> | <span data-ttu-id="06be9-140">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="06be9-140">Geometry Shader</span></span> | <span data-ttu-id="06be9-141">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="06be9-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="06be9-142">x</span><span class="sxs-lookup"><span data-stu-id="06be9-142">x</span></span>             | <span data-ttu-id="06be9-143">x</span><span class="sxs-lookup"><span data-stu-id="06be9-143">x</span></span>               | <span data-ttu-id="06be9-144">x</span><span class="sxs-lookup"><span data-stu-id="06be9-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="06be9-145">Shader-Mindestmodell</span><span class="sxs-lookup"><span data-stu-id="06be9-145">Minimum Shader Model</span></span>

<span data-ttu-id="06be9-146">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="06be9-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="06be9-147">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="06be9-147">Shader Model</span></span>                                              | <span data-ttu-id="06be9-148">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="06be9-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="06be9-149">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="06be9-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="06be9-150">ja</span><span class="sxs-lookup"><span data-stu-id="06be9-150">yes</span></span>       |
| [<span data-ttu-id="06be9-151">Shadermodell 4.1</span><span class="sxs-lookup"><span data-stu-id="06be9-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="06be9-152">ja</span><span class="sxs-lookup"><span data-stu-id="06be9-152">yes</span></span>       |
| [<span data-ttu-id="06be9-153">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="06be9-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="06be9-154">ja</span><span class="sxs-lookup"><span data-stu-id="06be9-154">yes</span></span>       |
| [<span data-ttu-id="06be9-155">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="06be9-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="06be9-156">nein</span><span class="sxs-lookup"><span data-stu-id="06be9-156">no</span></span>        |
| [<span data-ttu-id="06be9-157">Shadermodell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="06be9-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="06be9-158">nein</span><span class="sxs-lookup"><span data-stu-id="06be9-158">no</span></span>        |
| [<span data-ttu-id="06be9-159">Shadermodell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="06be9-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="06be9-160">nein</span><span class="sxs-lookup"><span data-stu-id="06be9-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="06be9-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="06be9-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06be9-162">Shadermodell 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="06be9-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





