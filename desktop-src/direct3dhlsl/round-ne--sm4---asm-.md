---
title: round_ne (SM4-ASM)
description: Gleit Komma Runde zum ganzzahligen Gleit Komma Wert. | round_ne (SM4-ASM)
ms.assetid: 2D1A0786-F7DB-4D69-9F56-82ECD1EE7ABA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c6f5e332453318dc0ad1a7806c3506343ff3b6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981649"
---
# <a name="round_ne-sm4---asm"></a><span data-ttu-id="f472f-104">Round \_ ne (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="f472f-104">round\_ne (sm4 - asm)</span></span>

<span data-ttu-id="f472f-105">Gleit Komma Runde zum ganzzahligen Gleit Komma Wert.</span><span class="sxs-lookup"><span data-stu-id="f472f-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="f472f-106">Round \_ ne \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="f472f-106">round\_ne\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="f472f-107">Element</span><span class="sxs-lookup"><span data-stu-id="f472f-107">Item</span></span>                                                            | <span data-ttu-id="f472f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f472f-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="f472f-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="f472f-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="f472f-110">\[in \] der Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="f472f-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="f472f-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f472f-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="f472f-112">\[in \] den Komponenten des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="f472f-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="f472f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f472f-113">Remarks</span></span>

<span data-ttu-id="f472f-114">Diese Anweisung führt eine Komponenten Weise Gleit Komma Runde der Werte in *src0* aus, wobei ganzzahlige Gleit Komma Werte in *dest* geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f472f-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span> <span data-ttu-id="f472f-115">**Round \_ ne** rundet auf den nächstgelegenen gleich.</span><span class="sxs-lookup"><span data-stu-id="f472f-115">**round\_ne** rounds towards nearest even.</span></span>

<span data-ttu-id="f472f-116">In der folgenden Tabelle werden die Ergebnisse angezeigt, die beim Ausführen der Anweisung mit verschiedenen Klassen von Zahlen abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="f472f-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="f472f-117">F bedeutet eine endliche reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="f472f-117">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="f472f-118">**src**</span><span class="sxs-lookup"><span data-stu-id="f472f-118">**src**</span></span>  | <span data-ttu-id="f472f-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="f472f-119">**-inf**</span></span> | <span data-ttu-id="f472f-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="f472f-120">**-F**</span></span> | <span data-ttu-id="f472f-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="f472f-121">**-denorm**</span></span> | <span data-ttu-id="f472f-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="f472f-122">**-0**</span></span> | <span data-ttu-id="f472f-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="f472f-123">**+0**</span></span> | <span data-ttu-id="f472f-124">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="f472f-124">**+denorm**</span></span> | <span data-ttu-id="f472f-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="f472f-125">**+F**</span></span> | <span data-ttu-id="f472f-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="f472f-126">**+inf**</span></span> | <span data-ttu-id="f472f-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="f472f-127">**NaN**</span></span> |
| <span data-ttu-id="f472f-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="f472f-128">**dest**</span></span> | <span data-ttu-id="f472f-129">-inf</span><span class="sxs-lookup"><span data-stu-id="f472f-129">-inf</span></span>     | <span data-ttu-id="f472f-130">-F</span><span class="sxs-lookup"><span data-stu-id="f472f-130">-F</span></span>     | <span data-ttu-id="f472f-131">-0</span><span class="sxs-lookup"><span data-stu-id="f472f-131">-0</span></span>          | <span data-ttu-id="f472f-132">-0</span><span class="sxs-lookup"><span data-stu-id="f472f-132">-0</span></span>     | <span data-ttu-id="f472f-133">+0</span><span class="sxs-lookup"><span data-stu-id="f472f-133">+0</span></span>     | <span data-ttu-id="f472f-134">+0</span><span class="sxs-lookup"><span data-stu-id="f472f-134">+0</span></span>          | <span data-ttu-id="f472f-135">+ F</span><span class="sxs-lookup"><span data-stu-id="f472f-135">+F</span></span>     | <span data-ttu-id="f472f-136">+inf</span><span class="sxs-lookup"><span data-stu-id="f472f-136">+inf</span></span>     | <span data-ttu-id="f472f-137">NaN</span><span class="sxs-lookup"><span data-stu-id="f472f-137">NaN</span></span>     |



 

<span data-ttu-id="f472f-138">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="f472f-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f472f-139">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="f472f-139">Vertex Shader</span></span> | <span data-ttu-id="f472f-140">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="f472f-140">Geometry Shader</span></span> | <span data-ttu-id="f472f-141">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="f472f-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="f472f-142">x</span><span class="sxs-lookup"><span data-stu-id="f472f-142">x</span></span>             | <span data-ttu-id="f472f-143">x</span><span class="sxs-lookup"><span data-stu-id="f472f-143">x</span></span>               | <span data-ttu-id="f472f-144">x</span><span class="sxs-lookup"><span data-stu-id="f472f-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f472f-145">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="f472f-145">Minimum Shader Model</span></span>

<span data-ttu-id="f472f-146">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f472f-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f472f-147">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="f472f-147">Shader Model</span></span>                                              | <span data-ttu-id="f472f-148">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="f472f-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f472f-149">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="f472f-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f472f-150">ja</span><span class="sxs-lookup"><span data-stu-id="f472f-150">yes</span></span>       |
| [<span data-ttu-id="f472f-151">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="f472f-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f472f-152">ja</span><span class="sxs-lookup"><span data-stu-id="f472f-152">yes</span></span>       |
| [<span data-ttu-id="f472f-153">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="f472f-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f472f-154">ja</span><span class="sxs-lookup"><span data-stu-id="f472f-154">yes</span></span>       |
| [<span data-ttu-id="f472f-155">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f472f-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f472f-156">nein</span><span class="sxs-lookup"><span data-stu-id="f472f-156">no</span></span>        |
| [<span data-ttu-id="f472f-157">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f472f-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f472f-158">nein</span><span class="sxs-lookup"><span data-stu-id="f472f-158">no</span></span>        |
| [<span data-ttu-id="f472f-159">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f472f-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f472f-160">nein</span><span class="sxs-lookup"><span data-stu-id="f472f-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f472f-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f472f-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f472f-162">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f472f-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





