---
title: round_ni (sm4 – asm)
description: Gleitkommagerundet auf ganzzahligen Gleitkommawert. | round_ni (sm4 – asm)
ms.assetid: 6DEF818B-AFF9-4B44-950E-320EACE1CAC4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2487715bbb2596653b1ca985a2e0390457feecbf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998577"
---
# <a name="round_ni-sm4---asm"></a><span data-ttu-id="7d690-104">round \_ ni (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="7d690-104">round\_ni (sm4 - asm)</span></span>

<span data-ttu-id="7d690-105">Gleitkommagerundet auf ganzzahligen Gleitkommawert.</span><span class="sxs-lookup"><span data-stu-id="7d690-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="7d690-106">round \_ ni \[ \_ sat \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swizzle\]</span><span class="sxs-lookup"><span data-stu-id="7d690-106">round\_ni\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="7d690-107">Element</span><span class="sxs-lookup"><span data-stu-id="7d690-107">Item</span></span>                                                            | <span data-ttu-id="7d690-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d690-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="7d690-109"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="7d690-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="7d690-110">\[in \] Die Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="7d690-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="7d690-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="7d690-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="7d690-112">\[in \] Die Komponenten im Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7d690-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="7d690-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7d690-113">Remarks</span></span>

<span data-ttu-id="7d690-114">Diese Anweisung führt eine komponentenweise Gleitkommarunde der Werte in *src0* aus und schreibt ganzzahlige Gleitkommawerte in *dest*.</span><span class="sxs-lookup"><span data-stu-id="7d690-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span> <span data-ttu-id="7d690-115">**round \_ ni** rundet auf -infinity, häufig als floor() bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7d690-115">**round\_ni** rounds toward -infinity, commonly known as floor().</span></span>

<span data-ttu-id="7d690-116">Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Zahlenklassen erzielt werden.</span><span class="sxs-lookup"><span data-stu-id="7d690-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="7d690-117">F bedeutet endliche reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="7d690-117">F means finite-real number.</span></span>



| <span data-ttu-id="7d690-118">**src**</span><span class="sxs-lookup"><span data-stu-id="7d690-118">**src**</span></span>  | <span data-ttu-id="7d690-119">**-inf**</span><span class="sxs-lookup"><span data-stu-id="7d690-119">**-inf**</span></span> | <span data-ttu-id="7d690-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="7d690-120">**-F**</span></span> | <span data-ttu-id="7d690-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="7d690-121">**-denorm**</span></span> | <span data-ttu-id="7d690-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="7d690-122">**-0**</span></span> | <span data-ttu-id="7d690-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="7d690-123">**+0**</span></span> | <span data-ttu-id="7d690-124">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="7d690-124">**+denorm**</span></span> | <span data-ttu-id="7d690-125">**+F**</span><span class="sxs-lookup"><span data-stu-id="7d690-125">**+F**</span></span> | <span data-ttu-id="7d690-126">**+inf**</span><span class="sxs-lookup"><span data-stu-id="7d690-126">**+inf**</span></span> | <span data-ttu-id="7d690-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="7d690-127">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="7d690-128">**Dest**</span><span class="sxs-lookup"><span data-stu-id="7d690-128">**dest**</span></span> | <span data-ttu-id="7d690-129">-inf</span><span class="sxs-lookup"><span data-stu-id="7d690-129">-inf</span></span>     | <span data-ttu-id="7d690-130">-F</span><span class="sxs-lookup"><span data-stu-id="7d690-130">-F</span></span>     | <span data-ttu-id="7d690-131">-0</span><span class="sxs-lookup"><span data-stu-id="7d690-131">-0</span></span>          | <span data-ttu-id="7d690-132">-0</span><span class="sxs-lookup"><span data-stu-id="7d690-132">-0</span></span>     | <span data-ttu-id="7d690-133">+0</span><span class="sxs-lookup"><span data-stu-id="7d690-133">+0</span></span>     | <span data-ttu-id="7d690-134">+0</span><span class="sxs-lookup"><span data-stu-id="7d690-134">+0</span></span>          | <span data-ttu-id="7d690-135">+F</span><span class="sxs-lookup"><span data-stu-id="7d690-135">+F</span></span>     | <span data-ttu-id="7d690-136">+inf</span><span class="sxs-lookup"><span data-stu-id="7d690-136">+inf</span></span>     | <span data-ttu-id="7d690-137">NaN</span><span class="sxs-lookup"><span data-stu-id="7d690-137">NaN</span></span>     |



 

<span data-ttu-id="7d690-138">Diese Anweisung gilt für die folgenden Shaderstufen:</span><span class="sxs-lookup"><span data-stu-id="7d690-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7d690-139">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="7d690-139">Vertex Shader</span></span> | <span data-ttu-id="7d690-140">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="7d690-140">Geometry Shader</span></span> | <span data-ttu-id="7d690-141">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="7d690-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="7d690-142">x</span><span class="sxs-lookup"><span data-stu-id="7d690-142">x</span></span>             | <span data-ttu-id="7d690-143">x</span><span class="sxs-lookup"><span data-stu-id="7d690-143">x</span></span>               | <span data-ttu-id="7d690-144">x</span><span class="sxs-lookup"><span data-stu-id="7d690-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7d690-145">Minimales Shadermodell</span><span class="sxs-lookup"><span data-stu-id="7d690-145">Minimum Shader Model</span></span>

<span data-ttu-id="7d690-146">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7d690-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7d690-147">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="7d690-147">Shader Model</span></span>                                              | <span data-ttu-id="7d690-148">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="7d690-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7d690-149">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="7d690-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7d690-150">ja</span><span class="sxs-lookup"><span data-stu-id="7d690-150">yes</span></span>       |
| [<span data-ttu-id="7d690-151">Shadermodell 4.1</span><span class="sxs-lookup"><span data-stu-id="7d690-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7d690-152">ja</span><span class="sxs-lookup"><span data-stu-id="7d690-152">yes</span></span>       |
| [<span data-ttu-id="7d690-153">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="7d690-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7d690-154">ja</span><span class="sxs-lookup"><span data-stu-id="7d690-154">yes</span></span>       |
| [<span data-ttu-id="7d690-155">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7d690-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7d690-156">nein</span><span class="sxs-lookup"><span data-stu-id="7d690-156">no</span></span>        |
| [<span data-ttu-id="7d690-157">Shadermodell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7d690-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7d690-158">nein</span><span class="sxs-lookup"><span data-stu-id="7d690-158">no</span></span>        |
| [<span data-ttu-id="7d690-159">Shadermodell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7d690-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7d690-160">nein</span><span class="sxs-lookup"><span data-stu-id="7d690-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7d690-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7d690-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d690-162">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7d690-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





