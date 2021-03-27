---
title: UGE (SM4-ASM)
description: Die Komponenten Weise Vektor-Ganzzahl ohne Vorzeichen, größer-als-oder-gleich-Vergleich.
ms.assetid: CA8E19EC-619F-4C19-B6FD-91650B5DAF9F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4aecd9e39aa94c69acefff0f6a0fdf843cec5d8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857767"
---
# <a name="uge-sm4---asm"></a><span data-ttu-id="0b79e-103">UGE (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="0b79e-103">uge (sm4 - asm)</span></span>

<span data-ttu-id="0b79e-104">Die Komponenten Weise Vektor-Ganzzahl ohne Vorzeichen, größer-als-oder-gleich-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="0b79e-104">Component-wise vector unsigned integer greater-than-or-equal comparison.</span></span>



| <span data-ttu-id="0b79e-105">UGE dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="0b79e-105">uge dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="0b79e-106">Element</span><span class="sxs-lookup"><span data-stu-id="0b79e-106">Item</span></span>                                                            | <span data-ttu-id="0b79e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b79e-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="0b79e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="0b79e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="0b79e-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="0b79e-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="0b79e-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="0b79e-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="0b79e-111">\[in \] den Komponenten, die mit *Quelle1* verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0b79e-111">\[in\] The components to compare to *src1*.</span></span><br/>        |
| <span data-ttu-id="0b79e-112"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="0b79e-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="0b79e-113">\[in \] den Komponenten, die mit *src0* verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0b79e-113">\[in\] The components to compare to *src0*.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="0b79e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b79e-114">Remarks</span></span>

<span data-ttu-id="0b79e-115">Diese Anweisung führt den Vergleich der Ganzzahl ohne Vorzeichen (*src0*  >=  *Quelle1*) für jede Komponente aus und schreibt das Ergebnis in *dest*.</span><span class="sxs-lookup"><span data-stu-id="0b79e-115">This instruction performs the unsigned integer comparison (*src0* >= *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="0b79e-116">Wenn der Vergleich true ist, wird 0xFFFFFFFF für diese Komponente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0b79e-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="0b79e-117">Andernfalls wird 0x0000000 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0b79e-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="0b79e-118">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="0b79e-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0b79e-119">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="0b79e-119">Vertex Shader</span></span> | <span data-ttu-id="0b79e-120">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="0b79e-120">Geometry Shader</span></span> | <span data-ttu-id="0b79e-121">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="0b79e-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="0b79e-122">x</span><span class="sxs-lookup"><span data-stu-id="0b79e-122">x</span></span>             | <span data-ttu-id="0b79e-123">x</span><span class="sxs-lookup"><span data-stu-id="0b79e-123">x</span></span>               | <span data-ttu-id="0b79e-124">x</span><span class="sxs-lookup"><span data-stu-id="0b79e-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0b79e-125">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="0b79e-125">Minimum Shader Model</span></span>

<span data-ttu-id="0b79e-126">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0b79e-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0b79e-127">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="0b79e-127">Shader Model</span></span>                                              | <span data-ttu-id="0b79e-128">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="0b79e-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0b79e-129">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="0b79e-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0b79e-130">ja</span><span class="sxs-lookup"><span data-stu-id="0b79e-130">yes</span></span>       |
| [<span data-ttu-id="0b79e-131">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="0b79e-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0b79e-132">ja</span><span class="sxs-lookup"><span data-stu-id="0b79e-132">yes</span></span>       |
| [<span data-ttu-id="0b79e-133">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="0b79e-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0b79e-134">ja</span><span class="sxs-lookup"><span data-stu-id="0b79e-134">yes</span></span>       |
| [<span data-ttu-id="0b79e-135">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b79e-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0b79e-136">nein</span><span class="sxs-lookup"><span data-stu-id="0b79e-136">no</span></span>        |
| [<span data-ttu-id="0b79e-137">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b79e-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0b79e-138">nein</span><span class="sxs-lookup"><span data-stu-id="0b79e-138">no</span></span>        |
| [<span data-ttu-id="0b79e-139">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b79e-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0b79e-140">nein</span><span class="sxs-lookup"><span data-stu-id="0b79e-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0b79e-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0b79e-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b79e-142">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b79e-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





