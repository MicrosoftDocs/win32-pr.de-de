---
title: dtof (SM5-ASM)
description: Komponenten Weise Konvertierung von Gleit Komma Daten mit doppelter Genauigkeit in Gleit Komma Daten mit einfacher Genauigkeit.
ms.assetid: 1D2EF05C-06EF-44F0-AA0F-22D3057FF43E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a66e72cf4c2cb1ac49adc492a586b4cbb9eef3b4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313626"
---
# <a name="dtof-sm5---asm"></a><span data-ttu-id="5886f-103">dtof (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="5886f-103">dtof (sm5 - asm)</span></span>

<span data-ttu-id="5886f-104">Komponenten Weise Konvertierung von Gleit Komma Daten mit doppelter Genauigkeit in Gleit Komma Daten mit einfacher Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="5886f-104">Component-wise conversion from double-precision floating-point data to single-precision floating-point data.</span></span>



| <span data-ttu-id="5886f-105">dtof dest \[ . mask \] , \[ - \] src \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="5886f-105">dtof dest\[.mask\], \[-\]src\[.swizzle\],</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="5886f-106">Element</span><span class="sxs-lookup"><span data-stu-id="5886f-106">Item</span></span>                                                            | <span data-ttu-id="5886f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5886f-107">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5886f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="5886f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="5886f-109">\[in \] der Adresse der konvertierten Daten.</span><span class="sxs-lookup"><span data-stu-id="5886f-109">\[in\] The address of the converted data.</span></span><br/> |
| <span data-ttu-id="5886f-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5886f-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5886f-111">\[in \] den zu konvertierenden Daten.</span><span class="sxs-lookup"><span data-stu-id="5886f-111">\[in\] The data to be converted.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="5886f-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5886f-112">Remarks</span></span>

<span data-ttu-id="5886f-113">Jede Komponente der Quelle wird von der Darstellung mit doppelter Genauigkeit in die Darstellung mit einfacher Genauigkeit konvertiert und verwendet gleichmäßige Rundung.</span><span class="sxs-lookup"><span data-stu-id="5886f-113">Each component of the source is converted from the double-precision representation to the single-precision representation using round-to-nearest-even rounding.</span></span>

<span data-ttu-id="5886f-114">Die gültigen Streifen für den Quellparameter lauten. xyzw,. xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="5886f-114">The valid swizzles for the source parameter are .xyzw, .xyxy, .zwxy, .zwzw.</span></span>

<span data-ttu-id="5886f-115">Die gültigen *dest* -Masken sind eine oder zwei Komponenten.</span><span class="sxs-lookup"><span data-stu-id="5886f-115">The valid *dest* masks are any one or two components.</span></span> <span data-ttu-id="5886f-116">Das heißt:. x,. y,. z,. w,. XY,. XZ,. XW,. YZ,. yw,. zw das Ergebnis der ersten Konvertierung wird an die erste Komponente in der Maske weitergeleitet, und das Ergebnis der zweiten Komponente wechselt in die zweite Komponente in der Maske, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5886f-116">That is: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw The result of the first conversion goes to the first component in the mask, and the result of the second component goes in the second component in the mask, if present.</span></span>

<span data-ttu-id="5886f-117">die *dest* -Komponenten sind float32.</span><span class="sxs-lookup"><span data-stu-id="5886f-117">*dest* components are float32.</span></span>

<span data-ttu-id="5886f-118">*src* ist eine doppelte vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb) Post-Swizzle.</span><span class="sxs-lookup"><span data-stu-id="5886f-118">*src* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB) post swizzle.</span></span>

<span data-ttu-id="5886f-119">Bei<->Double-Konvertierungen können Implementierungen entweder float32 denorms beachten oder Sie leeren.</span><span class="sxs-lookup"><span data-stu-id="5886f-119">For float32<->double conversions, implementations may either honor float32 denorms or may flush them.</span></span>

<span data-ttu-id="5886f-120">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="5886f-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5886f-121">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="5886f-121">Vertex</span></span> | <span data-ttu-id="5886f-122">Hülle</span><span class="sxs-lookup"><span data-stu-id="5886f-122">Hull</span></span> | <span data-ttu-id="5886f-123">Domain</span><span class="sxs-lookup"><span data-stu-id="5886f-123">Domain</span></span> | <span data-ttu-id="5886f-124">Geometrie</span><span class="sxs-lookup"><span data-stu-id="5886f-124">Geometry</span></span> | <span data-ttu-id="5886f-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="5886f-125">Pixel</span></span> | <span data-ttu-id="5886f-126">Compute</span><span class="sxs-lookup"><span data-stu-id="5886f-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5886f-127">X</span><span class="sxs-lookup"><span data-stu-id="5886f-127">X</span></span>      | <span data-ttu-id="5886f-128">X</span><span class="sxs-lookup"><span data-stu-id="5886f-128">X</span></span>    | <span data-ttu-id="5886f-129">X</span><span class="sxs-lookup"><span data-stu-id="5886f-129">X</span></span>      | <span data-ttu-id="5886f-130">X</span><span class="sxs-lookup"><span data-stu-id="5886f-130">X</span></span>        | <span data-ttu-id="5886f-131">X</span><span class="sxs-lookup"><span data-stu-id="5886f-131">X</span></span>     | <span data-ttu-id="5886f-132">X</span><span class="sxs-lookup"><span data-stu-id="5886f-132">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5886f-133">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="5886f-133">Minimum Shader Model</span></span>

<span data-ttu-id="5886f-134">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="5886f-134">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="5886f-135">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="5886f-135">Shader Model</span></span>                                              | <span data-ttu-id="5886f-136">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="5886f-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5886f-137">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="5886f-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5886f-138">ja</span><span class="sxs-lookup"><span data-stu-id="5886f-138">yes</span></span>       |
| [<span data-ttu-id="5886f-139">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="5886f-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5886f-140">nein</span><span class="sxs-lookup"><span data-stu-id="5886f-140">no</span></span>        |
| [<span data-ttu-id="5886f-141">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="5886f-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5886f-142">nein</span><span class="sxs-lookup"><span data-stu-id="5886f-142">no</span></span>        |
| [<span data-ttu-id="5886f-143">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5886f-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5886f-144">nein</span><span class="sxs-lookup"><span data-stu-id="5886f-144">no</span></span>        |
| [<span data-ttu-id="5886f-145">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5886f-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5886f-146">nein</span><span class="sxs-lookup"><span data-stu-id="5886f-146">no</span></span>        |
| [<span data-ttu-id="5886f-147">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5886f-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5886f-148">nein</span><span class="sxs-lookup"><span data-stu-id="5886f-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5886f-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5886f-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5886f-150">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5886f-150">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





