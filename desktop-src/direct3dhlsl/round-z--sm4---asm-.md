---
title: round_z (SM4-ASM)
description: Gleit Komma Runde zum ganzzahligen Gleit Komma Wert. | round_z (SM4-ASM)
ms.assetid: 97C0E0F2-2571-4A94-BB04-B0CDBA0B5C0C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ed79a60bf122163b49411a3b3197ccdacba1311
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869723"
---
# <a name="round_z-sm4---asm"></a><span data-ttu-id="5e39d-104">Round \_ z (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="5e39d-104">round\_z (sm4 - asm)</span></span>

<span data-ttu-id="5e39d-105">Gleit Komma Runde zum ganzzahligen Gleit Komma Wert.</span><span class="sxs-lookup"><span data-stu-id="5e39d-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="5e39d-106">Round \_ z \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="5e39d-106">round\_z\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-----------------------------------------------------------------|



 



| <span data-ttu-id="5e39d-107">Element</span><span class="sxs-lookup"><span data-stu-id="5e39d-107">Item</span></span>                                                            | <span data-ttu-id="5e39d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5e39d-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="5e39d-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="5e39d-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="5e39d-110">\[in \] der Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="5e39d-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="5e39d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5e39d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5e39d-112">\[in \] den Komponenten des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="5e39d-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="5e39d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e39d-113">Remarks</span></span>

<span data-ttu-id="5e39d-114">Diese Anweisung führt eine Komponenten Weise Gleit Komma Runde der Werte in *src0* aus, wobei ganzzahlige Gleit Komma Werte in *dest* geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="5e39d-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span>

<span data-ttu-id="5e39d-115">**Round \_ z** rundet auf NULL.</span><span class="sxs-lookup"><span data-stu-id="5e39d-115">**round\_z** rounds towards zero.</span></span>

<span data-ttu-id="5e39d-116">In der folgenden Tabelle werden die Ergebnisse angezeigt, die beim Ausführen der Anweisung mit verschiedenen Klassen von Zahlen abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="5e39d-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="5e39d-117">**src**</span><span class="sxs-lookup"><span data-stu-id="5e39d-117">**src**</span></span>  | <span data-ttu-id="5e39d-118">**-INF**</span><span class="sxs-lookup"><span data-stu-id="5e39d-118">**-inf**</span></span> | <span data-ttu-id="5e39d-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="5e39d-119">**-F**</span></span> | <span data-ttu-id="5e39d-120">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="5e39d-120">**-denorm**</span></span> | <span data-ttu-id="5e39d-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="5e39d-121">**-0**</span></span> | <span data-ttu-id="5e39d-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="5e39d-122">**+0**</span></span> | <span data-ttu-id="5e39d-123">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="5e39d-123">**+denorm**</span></span> | <span data-ttu-id="5e39d-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="5e39d-124">**+F**</span></span> | <span data-ttu-id="5e39d-125">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="5e39d-125">**+inf**</span></span> | <span data-ttu-id="5e39d-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="5e39d-126">**NaN**</span></span> |
| <span data-ttu-id="5e39d-127">**dest**</span><span class="sxs-lookup"><span data-stu-id="5e39d-127">**dest**</span></span> | <span data-ttu-id="5e39d-128">-inf</span><span class="sxs-lookup"><span data-stu-id="5e39d-128">-inf</span></span>     | <span data-ttu-id="5e39d-129">-F</span><span class="sxs-lookup"><span data-stu-id="5e39d-129">-F</span></span>     | <span data-ttu-id="5e39d-130">-0</span><span class="sxs-lookup"><span data-stu-id="5e39d-130">-0</span></span>          | <span data-ttu-id="5e39d-131">-0</span><span class="sxs-lookup"><span data-stu-id="5e39d-131">-0</span></span>     | <span data-ttu-id="5e39d-132">+0</span><span class="sxs-lookup"><span data-stu-id="5e39d-132">+0</span></span>     | <span data-ttu-id="5e39d-133">+0</span><span class="sxs-lookup"><span data-stu-id="5e39d-133">+0</span></span>          | <span data-ttu-id="5e39d-134">+ F</span><span class="sxs-lookup"><span data-stu-id="5e39d-134">+F</span></span>     | <span data-ttu-id="5e39d-135">+inf</span><span class="sxs-lookup"><span data-stu-id="5e39d-135">+inf</span></span>     | <span data-ttu-id="5e39d-136">NaN</span><span class="sxs-lookup"><span data-stu-id="5e39d-136">NaN</span></span>     |



 

<span data-ttu-id="5e39d-137">F bedeutet eine endliche reelle Zahl.</span><span class="sxs-lookup"><span data-stu-id="5e39d-137">F means finite-real number.</span></span>

<span data-ttu-id="5e39d-138">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="5e39d-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5e39d-139">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="5e39d-139">Vertex Shader</span></span> | <span data-ttu-id="5e39d-140">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="5e39d-140">Geometry Shader</span></span> | <span data-ttu-id="5e39d-141">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="5e39d-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="5e39d-142">x</span><span class="sxs-lookup"><span data-stu-id="5e39d-142">x</span></span>             | <span data-ttu-id="5e39d-143">x</span><span class="sxs-lookup"><span data-stu-id="5e39d-143">x</span></span>               | <span data-ttu-id="5e39d-144">x</span><span class="sxs-lookup"><span data-stu-id="5e39d-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5e39d-145">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="5e39d-145">Minimum Shader Model</span></span>

<span data-ttu-id="5e39d-146">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5e39d-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5e39d-147">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="5e39d-147">Shader Model</span></span>                                              | <span data-ttu-id="5e39d-148">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="5e39d-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5e39d-149">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="5e39d-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5e39d-150">ja</span><span class="sxs-lookup"><span data-stu-id="5e39d-150">yes</span></span>       |
| [<span data-ttu-id="5e39d-151">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="5e39d-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5e39d-152">ja</span><span class="sxs-lookup"><span data-stu-id="5e39d-152">yes</span></span>       |
| [<span data-ttu-id="5e39d-153">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="5e39d-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5e39d-154">ja</span><span class="sxs-lookup"><span data-stu-id="5e39d-154">yes</span></span>       |
| [<span data-ttu-id="5e39d-155">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5e39d-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5e39d-156">nein</span><span class="sxs-lookup"><span data-stu-id="5e39d-156">no</span></span>        |
| [<span data-ttu-id="5e39d-157">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5e39d-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5e39d-158">nein</span><span class="sxs-lookup"><span data-stu-id="5e39d-158">no</span></span>        |
| [<span data-ttu-id="5e39d-159">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5e39d-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5e39d-160">nein</span><span class="sxs-lookup"><span data-stu-id="5e39d-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5e39d-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5e39d-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e39d-162">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5e39d-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





