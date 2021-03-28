---
title: round_ni (SM4-ASM)
description: Gleit Komma Runde zum ganzzahligen Gleit Komma Wert. | round_ni (SM4-ASM)
ms.assetid: 6DEF818B-AFF9-4B44-950E-320EACE1CAC4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3daafd64e76bd8c04acf7812b096f7374befef6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104050788"
---
# <a name="round_ni-sm4---asm"></a><span data-ttu-id="ede4e-104">Round \_ NI (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ede4e-104">round\_ni (sm4 - asm)</span></span>

<span data-ttu-id="ede4e-105">Gleit Komma Runde zum ganzzahligen Gleit Komma Wert.</span><span class="sxs-lookup"><span data-stu-id="ede4e-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="ede4e-106">Round \_ NI \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="ede4e-106">round\_ni\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="ede4e-107">Element</span><span class="sxs-lookup"><span data-stu-id="ede4e-107">Item</span></span>                                                            | <span data-ttu-id="ede4e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ede4e-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="ede4e-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="ede4e-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ede4e-110">\[in \] der Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="ede4e-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="ede4e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ede4e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ede4e-112">\[in \] den Komponenten des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="ede4e-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="ede4e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ede4e-113">Remarks</span></span>

<span data-ttu-id="ede4e-114">Diese Anweisung führt eine Komponenten Weise Gleit Komma Runde der Werte in *src0* aus, wobei ganzzahlige Gleit Komma Werte in *dest* geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ede4e-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span> <span data-ttu-id="ede4e-115">**Round \_ NI** rundet auf unendlich, häufig als Floor () bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ede4e-115">**round\_ni** rounds toward -infinity, commonly known as floor().</span></span>

<span data-ttu-id="ede4e-116">In der folgenden Tabelle werden die Ergebnisse angezeigt, die beim Ausführen der Anweisung mit verschiedenen Klassen von Zahlen abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="ede4e-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="ede4e-117">F bedeutet eine endliche reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="ede4e-117">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="ede4e-118">**src**</span><span class="sxs-lookup"><span data-stu-id="ede4e-118">**src**</span></span>  | <span data-ttu-id="ede4e-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="ede4e-119">**-inf**</span></span> | <span data-ttu-id="ede4e-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="ede4e-120">**-F**</span></span> | <span data-ttu-id="ede4e-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="ede4e-121">**-denorm**</span></span> | <span data-ttu-id="ede4e-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="ede4e-122">**-0**</span></span> | <span data-ttu-id="ede4e-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="ede4e-123">**+0**</span></span> | <span data-ttu-id="ede4e-124">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="ede4e-124">**+denorm**</span></span> | <span data-ttu-id="ede4e-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="ede4e-125">**+F**</span></span> | <span data-ttu-id="ede4e-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="ede4e-126">**+inf**</span></span> | <span data-ttu-id="ede4e-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="ede4e-127">**NaN**</span></span> |
| <span data-ttu-id="ede4e-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="ede4e-128">**dest**</span></span> | <span data-ttu-id="ede4e-129">-inf</span><span class="sxs-lookup"><span data-stu-id="ede4e-129">-inf</span></span>     | <span data-ttu-id="ede4e-130">-F</span><span class="sxs-lookup"><span data-stu-id="ede4e-130">-F</span></span>     | <span data-ttu-id="ede4e-131">-0</span><span class="sxs-lookup"><span data-stu-id="ede4e-131">-0</span></span>          | <span data-ttu-id="ede4e-132">-0</span><span class="sxs-lookup"><span data-stu-id="ede4e-132">-0</span></span>     | <span data-ttu-id="ede4e-133">+0</span><span class="sxs-lookup"><span data-stu-id="ede4e-133">+0</span></span>     | <span data-ttu-id="ede4e-134">+0</span><span class="sxs-lookup"><span data-stu-id="ede4e-134">+0</span></span>          | <span data-ttu-id="ede4e-135">+ F</span><span class="sxs-lookup"><span data-stu-id="ede4e-135">+F</span></span>     | <span data-ttu-id="ede4e-136">+inf</span><span class="sxs-lookup"><span data-stu-id="ede4e-136">+inf</span></span>     | <span data-ttu-id="ede4e-137">NaN</span><span class="sxs-lookup"><span data-stu-id="ede4e-137">NaN</span></span>     |



 

<span data-ttu-id="ede4e-138">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="ede4e-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ede4e-139">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="ede4e-139">Vertex Shader</span></span> | <span data-ttu-id="ede4e-140">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="ede4e-140">Geometry Shader</span></span> | <span data-ttu-id="ede4e-141">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="ede4e-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ede4e-142">x</span><span class="sxs-lookup"><span data-stu-id="ede4e-142">x</span></span>             | <span data-ttu-id="ede4e-143">x</span><span class="sxs-lookup"><span data-stu-id="ede4e-143">x</span></span>               | <span data-ttu-id="ede4e-144">x</span><span class="sxs-lookup"><span data-stu-id="ede4e-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ede4e-145">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="ede4e-145">Minimum Shader Model</span></span>

<span data-ttu-id="ede4e-146">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ede4e-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ede4e-147">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="ede4e-147">Shader Model</span></span>                                              | <span data-ttu-id="ede4e-148">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ede4e-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ede4e-149">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="ede4e-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ede4e-150">ja</span><span class="sxs-lookup"><span data-stu-id="ede4e-150">yes</span></span>       |
| [<span data-ttu-id="ede4e-151">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="ede4e-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ede4e-152">ja</span><span class="sxs-lookup"><span data-stu-id="ede4e-152">yes</span></span>       |
| [<span data-ttu-id="ede4e-153">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="ede4e-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ede4e-154">ja</span><span class="sxs-lookup"><span data-stu-id="ede4e-154">yes</span></span>       |
| [<span data-ttu-id="ede4e-155">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ede4e-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ede4e-156">nein</span><span class="sxs-lookup"><span data-stu-id="ede4e-156">no</span></span>        |
| [<span data-ttu-id="ede4e-157">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ede4e-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ede4e-158">nein</span><span class="sxs-lookup"><span data-stu-id="ede4e-158">no</span></span>        |
| [<span data-ttu-id="ede4e-159">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ede4e-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ede4e-160">nein</span><span class="sxs-lookup"><span data-stu-id="ede4e-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ede4e-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ede4e-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ede4e-162">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ede4e-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





