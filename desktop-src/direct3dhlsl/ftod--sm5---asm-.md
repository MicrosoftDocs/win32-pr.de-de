---
title: "\"f\" (SM5-ASM)"
description: Komponenten Weise Konvertierung von Gleit Komma Daten mit einfacher Genauigkeit in Gleit Komma Daten mit doppelter Genauigkeit.
ms.assetid: 95297556-41ED-4ED0-8F9A-16B7A440AF25
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6790735745805426d32aefcc5d5d771ade644e43
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313704"
---
# <a name="ftod-sm5---asm"></a><span data-ttu-id="9a86e-103">"f" (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="9a86e-103">ftod (sm5 - asm)</span></span>

<span data-ttu-id="9a86e-104">Komponenten Weise Konvertierung von Gleit Komma Daten mit einfacher Genauigkeit in Gleit Komma Daten mit doppelter Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="9a86e-104">Component-wise conversion from single-precision floating-point data to double-precision floating-point data.</span></span>



| <span data-ttu-id="9a86e-105">f: dest \[ . mask \] , \[ - \] src \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="9a86e-105">ftod dest\[.mask\], \[-\]src\[.swizzle\],</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="9a86e-106">Element</span><span class="sxs-lookup"><span data-stu-id="9a86e-106">Item</span></span>                                                            | <span data-ttu-id="9a86e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9a86e-107">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9a86e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="9a86e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="9a86e-109">\[in \] der Adresse der konvertierten Daten.</span><span class="sxs-lookup"><span data-stu-id="9a86e-109">\[in\] The address of the converted data.</span></span><br/> |
| <span data-ttu-id="9a86e-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9a86e-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9a86e-111">\[in \] den zu konvertierenden Daten.</span><span class="sxs-lookup"><span data-stu-id="9a86e-111">\[in\] The data to be converted.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="9a86e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a86e-112">Remarks</span></span>

<span data-ttu-id="9a86e-113">Jede Komponente der Quelle wird von der Darstellung mit einfacher Genauigkeit in die Darstellung mit doppelter Genauigkeit konvertiert.</span><span class="sxs-lookup"><span data-stu-id="9a86e-113">Each component of the source is converted from the single-precision representation to the double-precision representation.</span></span>

<span data-ttu-id="9a86e-114">Die gültigen *dest* -Masken sind. XY,. zw und. xyzw.</span><span class="sxs-lookup"><span data-stu-id="9a86e-114">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="9a86e-115">. XY empfängt das Ergebnis der ersten Konvertierung, und. zw empfängt das Ergebnis der zweiten Konvertierung.</span><span class="sxs-lookup"><span data-stu-id="9a86e-115">.xy receives the result of the first conversion, and .zw receives the result of the second conversion.</span></span>

<span data-ttu-id="9a86e-116">*dest* ist eine doppelte vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).</span><span class="sxs-lookup"><span data-stu-id="9a86e-116">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="9a86e-117">*src* ist ein Gleit Komma vec2 über x und y (ZW wird ignoriert) (postswizzle).</span><span class="sxs-lookup"><span data-stu-id="9a86e-117">*src* is a float vec2 across x and y (zw ignored) (post swizzle).</span></span>

<span data-ttu-id="9a86e-118">Bei<->Double-Konvertierungen können Implementierungen entweder float32 denorms beachten oder Sie leeren.</span><span class="sxs-lookup"><span data-stu-id="9a86e-118">For float32<->double conversions, implementations may either honor float32 denorms or may flush them.</span></span>

<span data-ttu-id="9a86e-119">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="9a86e-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9a86e-120">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="9a86e-120">Vertex</span></span> | <span data-ttu-id="9a86e-121">Hülle</span><span class="sxs-lookup"><span data-stu-id="9a86e-121">Hull</span></span> | <span data-ttu-id="9a86e-122">Domain</span><span class="sxs-lookup"><span data-stu-id="9a86e-122">Domain</span></span> | <span data-ttu-id="9a86e-123">Geometrie</span><span class="sxs-lookup"><span data-stu-id="9a86e-123">Geometry</span></span> | <span data-ttu-id="9a86e-124">Pixel</span><span class="sxs-lookup"><span data-stu-id="9a86e-124">Pixel</span></span> | <span data-ttu-id="9a86e-125">Compute</span><span class="sxs-lookup"><span data-stu-id="9a86e-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9a86e-126">X</span><span class="sxs-lookup"><span data-stu-id="9a86e-126">X</span></span>      | <span data-ttu-id="9a86e-127">X</span><span class="sxs-lookup"><span data-stu-id="9a86e-127">X</span></span>    | <span data-ttu-id="9a86e-128">X</span><span class="sxs-lookup"><span data-stu-id="9a86e-128">X</span></span>      | <span data-ttu-id="9a86e-129">X</span><span class="sxs-lookup"><span data-stu-id="9a86e-129">X</span></span>        | <span data-ttu-id="9a86e-130">X</span><span class="sxs-lookup"><span data-stu-id="9a86e-130">X</span></span>     | <span data-ttu-id="9a86e-131">X</span><span class="sxs-lookup"><span data-stu-id="9a86e-131">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9a86e-132">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="9a86e-132">Minimum Shader Model</span></span>

<span data-ttu-id="9a86e-133">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="9a86e-133">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="9a86e-134">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="9a86e-134">Shader Model</span></span>                                              | <span data-ttu-id="9a86e-135">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="9a86e-135">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9a86e-136">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="9a86e-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9a86e-137">ja</span><span class="sxs-lookup"><span data-stu-id="9a86e-137">yes</span></span>       |
| [<span data-ttu-id="9a86e-138">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="9a86e-138">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9a86e-139">nein</span><span class="sxs-lookup"><span data-stu-id="9a86e-139">no</span></span>        |
| [<span data-ttu-id="9a86e-140">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="9a86e-140">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9a86e-141">nein</span><span class="sxs-lookup"><span data-stu-id="9a86e-141">no</span></span>        |
| [<span data-ttu-id="9a86e-142">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9a86e-142">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9a86e-143">nein</span><span class="sxs-lookup"><span data-stu-id="9a86e-143">no</span></span>        |
| [<span data-ttu-id="9a86e-144">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9a86e-144">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9a86e-145">nein</span><span class="sxs-lookup"><span data-stu-id="9a86e-145">no</span></span>        |
| [<span data-ttu-id="9a86e-146">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9a86e-146">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9a86e-147">nein</span><span class="sxs-lookup"><span data-stu-id="9a86e-147">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9a86e-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9a86e-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a86e-149">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9a86e-149">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





