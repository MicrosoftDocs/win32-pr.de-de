---
title: round_pi (SM4-ASM)
description: Gleit Komma Runde zum ganzzahligen Gleit Komma Wert. | round_pi (SM4-ASM)
ms.assetid: AA4E4C2E-A4B0-4892-8660-1EF57767F4C4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6016cc03f28852c938b1be62d3aaca39dae5dcfb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995639"
---
# <a name="round_pi-sm4---asm"></a><span data-ttu-id="2d514-104">Round \_ PI (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="2d514-104">round\_pi (sm4 - asm)</span></span>

<span data-ttu-id="2d514-105">Gleit Komma Runde zum ganzzahligen Gleit Komma Wert.</span><span class="sxs-lookup"><span data-stu-id="2d514-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="2d514-106">Round \_ Pi \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="2d514-106">round\_pi\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="2d514-107">Element</span><span class="sxs-lookup"><span data-stu-id="2d514-107">Item</span></span>                                                            | <span data-ttu-id="2d514-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d514-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="2d514-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="2d514-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="2d514-110">\[in \] der Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="2d514-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="2d514-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2d514-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="2d514-112">\[in \] den Komponenten des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="2d514-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="2d514-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d514-113">Remarks</span></span>

<span data-ttu-id="2d514-114">Diese Anweisung führt eine Komponenten Weise Gleit Komma Runde der Werte in *src0* aus, wobei ganzzahlige Gleit Komma Werte in *dest* geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2d514-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span>

<span data-ttu-id="2d514-115">**Round \_ Pi** rundet auf + unendlich, häufig als ceil () bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="2d514-115">**round\_pi** rounds towards +infinity, commonly known as ceil().</span></span>

<span data-ttu-id="2d514-116">In der folgenden Tabelle werden die Ergebnisse angezeigt, die beim Ausführen der Anweisung mit verschiedenen Klassen von Zahlen abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="2d514-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="2d514-117">F bedeutet eine endliche reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="2d514-117">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="2d514-118">**src**</span><span class="sxs-lookup"><span data-stu-id="2d514-118">**src**</span></span>  | <span data-ttu-id="2d514-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="2d514-119">**-inf**</span></span> | <span data-ttu-id="2d514-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="2d514-120">**-F**</span></span> | <span data-ttu-id="2d514-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="2d514-121">**-denorm**</span></span> | <span data-ttu-id="2d514-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="2d514-122">**-0**</span></span> | <span data-ttu-id="2d514-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="2d514-123">**+0**</span></span> | <span data-ttu-id="2d514-124">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="2d514-124">**+denorm**</span></span> | <span data-ttu-id="2d514-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="2d514-125">**+F**</span></span> | <span data-ttu-id="2d514-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="2d514-126">**+inf**</span></span> | <span data-ttu-id="2d514-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="2d514-127">**NaN**</span></span> |
| <span data-ttu-id="2d514-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="2d514-128">**dest**</span></span> | <span data-ttu-id="2d514-129">-inf</span><span class="sxs-lookup"><span data-stu-id="2d514-129">-inf</span></span>     | <span data-ttu-id="2d514-130">-F</span><span class="sxs-lookup"><span data-stu-id="2d514-130">-F</span></span>     | <span data-ttu-id="2d514-131">-0</span><span class="sxs-lookup"><span data-stu-id="2d514-131">-0</span></span>          | <span data-ttu-id="2d514-132">-0</span><span class="sxs-lookup"><span data-stu-id="2d514-132">-0</span></span>     | <span data-ttu-id="2d514-133">+0</span><span class="sxs-lookup"><span data-stu-id="2d514-133">+0</span></span>     | <span data-ttu-id="2d514-134">+0</span><span class="sxs-lookup"><span data-stu-id="2d514-134">+0</span></span>          | <span data-ttu-id="2d514-135">+ F</span><span class="sxs-lookup"><span data-stu-id="2d514-135">+F</span></span>     | <span data-ttu-id="2d514-136">+inf</span><span class="sxs-lookup"><span data-stu-id="2d514-136">+inf</span></span>     | <span data-ttu-id="2d514-137">NaN</span><span class="sxs-lookup"><span data-stu-id="2d514-137">NaN</span></span>     |



 

<span data-ttu-id="2d514-138">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="2d514-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2d514-139">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="2d514-139">Vertex Shader</span></span> | <span data-ttu-id="2d514-140">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="2d514-140">Geometry Shader</span></span> | <span data-ttu-id="2d514-141">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="2d514-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2d514-142">x</span><span class="sxs-lookup"><span data-stu-id="2d514-142">x</span></span>             | <span data-ttu-id="2d514-143">x</span><span class="sxs-lookup"><span data-stu-id="2d514-143">x</span></span>               | <span data-ttu-id="2d514-144">x</span><span class="sxs-lookup"><span data-stu-id="2d514-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2d514-145">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="2d514-145">Minimum Shader Model</span></span>

<span data-ttu-id="2d514-146">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2d514-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2d514-147">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="2d514-147">Shader Model</span></span>                                              | <span data-ttu-id="2d514-148">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="2d514-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2d514-149">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="2d514-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2d514-150">ja</span><span class="sxs-lookup"><span data-stu-id="2d514-150">yes</span></span>       |
| [<span data-ttu-id="2d514-151">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="2d514-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2d514-152">ja</span><span class="sxs-lookup"><span data-stu-id="2d514-152">yes</span></span>       |
| [<span data-ttu-id="2d514-153">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="2d514-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2d514-154">ja</span><span class="sxs-lookup"><span data-stu-id="2d514-154">yes</span></span>       |
| [<span data-ttu-id="2d514-155">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d514-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2d514-156">nein</span><span class="sxs-lookup"><span data-stu-id="2d514-156">no</span></span>        |
| [<span data-ttu-id="2d514-157">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d514-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2d514-158">nein</span><span class="sxs-lookup"><span data-stu-id="2d514-158">no</span></span>        |
| [<span data-ttu-id="2d514-159">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d514-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2d514-160">nein</span><span class="sxs-lookup"><span data-stu-id="2d514-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2d514-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2d514-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d514-162">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d514-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





