---
title: round_z (sm4 – asm)
description: Gleitkommagerundet auf ganzzahligen Gleitkommawert. | round_z (sm4 – asm)
ms.assetid: 97C0E0F2-2571-4A94-BB04-B0CDBA0B5C0C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc874c6d0a1f26902086af300784c55950b71569
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997127"
---
# <a name="round_z-sm4---asm"></a><span data-ttu-id="f8c65-104">round \_ z (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="f8c65-104">round\_z (sm4 - asm)</span></span>

<span data-ttu-id="f8c65-105">Gleitkommagerundet auf ganzzahligen Gleitkommawert.</span><span class="sxs-lookup"><span data-stu-id="f8c65-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="f8c65-106">round \_ z \[ \_ sat \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="f8c65-106">round\_z\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-----------------------------------------------------------------|



 



| <span data-ttu-id="f8c65-107">Element</span><span class="sxs-lookup"><span data-stu-id="f8c65-107">Item</span></span>                                                            | <span data-ttu-id="f8c65-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8c65-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="f8c65-109"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="f8c65-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="f8c65-110">\[in \] Die Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="f8c65-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="f8c65-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f8c65-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="f8c65-112">\[in \] Die Komponenten im Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f8c65-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="f8c65-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f8c65-113">Remarks</span></span>

<span data-ttu-id="f8c65-114">Diese Anweisung führt eine komponentenweise Gleitkommarunde der Werte in *src0* aus und schreibt ganzzahlige Gleitkommawerte in *dest*.</span><span class="sxs-lookup"><span data-stu-id="f8c65-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span>

<span data-ttu-id="f8c65-115">**round \_ z** rundet auf 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f8c65-115">**round\_z** rounds towards zero.</span></span>

<span data-ttu-id="f8c65-116">Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Zahlenklassen erzielt werden.</span><span class="sxs-lookup"><span data-stu-id="f8c65-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



| <span data-ttu-id="f8c65-117">**src**</span><span class="sxs-lookup"><span data-stu-id="f8c65-117">**src**</span></span>  | <span data-ttu-id="f8c65-118">**-inf**</span><span class="sxs-lookup"><span data-stu-id="f8c65-118">**-inf**</span></span> | <span data-ttu-id="f8c65-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="f8c65-119">**-F**</span></span> | <span data-ttu-id="f8c65-120">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="f8c65-120">**-denorm**</span></span> | <span data-ttu-id="f8c65-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="f8c65-121">**-0**</span></span> | <span data-ttu-id="f8c65-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="f8c65-122">**+0**</span></span> | <span data-ttu-id="f8c65-123">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="f8c65-123">**+denorm**</span></span> | <span data-ttu-id="f8c65-124">**+F**</span><span class="sxs-lookup"><span data-stu-id="f8c65-124">**+F**</span></span> | <span data-ttu-id="f8c65-125">**+inf**</span><span class="sxs-lookup"><span data-stu-id="f8c65-125">**+inf**</span></span> | <span data-ttu-id="f8c65-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="f8c65-126">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="f8c65-127">**Dest**</span><span class="sxs-lookup"><span data-stu-id="f8c65-127">**dest**</span></span> | <span data-ttu-id="f8c65-128">-inf</span><span class="sxs-lookup"><span data-stu-id="f8c65-128">-inf</span></span>     | <span data-ttu-id="f8c65-129">-F</span><span class="sxs-lookup"><span data-stu-id="f8c65-129">-F</span></span>     | <span data-ttu-id="f8c65-130">-0</span><span class="sxs-lookup"><span data-stu-id="f8c65-130">-0</span></span>          | <span data-ttu-id="f8c65-131">-0</span><span class="sxs-lookup"><span data-stu-id="f8c65-131">-0</span></span>     | <span data-ttu-id="f8c65-132">+0</span><span class="sxs-lookup"><span data-stu-id="f8c65-132">+0</span></span>     | <span data-ttu-id="f8c65-133">+0</span><span class="sxs-lookup"><span data-stu-id="f8c65-133">+0</span></span>          | <span data-ttu-id="f8c65-134">+F</span><span class="sxs-lookup"><span data-stu-id="f8c65-134">+F</span></span>     | <span data-ttu-id="f8c65-135">+inf</span><span class="sxs-lookup"><span data-stu-id="f8c65-135">+inf</span></span>     | <span data-ttu-id="f8c65-136">NaN</span><span class="sxs-lookup"><span data-stu-id="f8c65-136">NaN</span></span>     |



 

<span data-ttu-id="f8c65-137">F bedeutet endliche reale Zahl.</span><span class="sxs-lookup"><span data-stu-id="f8c65-137">F means finite-real number.</span></span>

<span data-ttu-id="f8c65-138">Diese Anweisung gilt für die folgenden Shaderstufen:</span><span class="sxs-lookup"><span data-stu-id="f8c65-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f8c65-139">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="f8c65-139">Vertex Shader</span></span> | <span data-ttu-id="f8c65-140">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="f8c65-140">Geometry Shader</span></span> | <span data-ttu-id="f8c65-141">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="f8c65-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="f8c65-142">x</span><span class="sxs-lookup"><span data-stu-id="f8c65-142">x</span></span>             | <span data-ttu-id="f8c65-143">x</span><span class="sxs-lookup"><span data-stu-id="f8c65-143">x</span></span>               | <span data-ttu-id="f8c65-144">x</span><span class="sxs-lookup"><span data-stu-id="f8c65-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f8c65-145">Minimales Shadermodell</span><span class="sxs-lookup"><span data-stu-id="f8c65-145">Minimum Shader Model</span></span>

<span data-ttu-id="f8c65-146">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8c65-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f8c65-147">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="f8c65-147">Shader Model</span></span>                                              | <span data-ttu-id="f8c65-148">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="f8c65-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f8c65-149">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="f8c65-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f8c65-150">ja</span><span class="sxs-lookup"><span data-stu-id="f8c65-150">yes</span></span>       |
| [<span data-ttu-id="f8c65-151">Shadermodell 4.1</span><span class="sxs-lookup"><span data-stu-id="f8c65-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f8c65-152">ja</span><span class="sxs-lookup"><span data-stu-id="f8c65-152">yes</span></span>       |
| [<span data-ttu-id="f8c65-153">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="f8c65-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f8c65-154">ja</span><span class="sxs-lookup"><span data-stu-id="f8c65-154">yes</span></span>       |
| [<span data-ttu-id="f8c65-155">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f8c65-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f8c65-156">nein</span><span class="sxs-lookup"><span data-stu-id="f8c65-156">no</span></span>        |
| [<span data-ttu-id="f8c65-157">Shadermodell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f8c65-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f8c65-158">nein</span><span class="sxs-lookup"><span data-stu-id="f8c65-158">no</span></span>        |
| [<span data-ttu-id="f8c65-159">Shadermodell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f8c65-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f8c65-160">nein</span><span class="sxs-lookup"><span data-stu-id="f8c65-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f8c65-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f8c65-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8c65-162">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f8c65-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





