---
title: ISHR (SM4-ASM)
description: Arithmetische UMSCHALT Rechte (Zeichen Erweiterung). | ISHR (SM4-ASM)
ms.assetid: AFE46BBA-A6B2-4691-A3F4-A4141F1578DB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7516543c5501ed886c5c1fa98d093062e3099a0f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995733"
---
# <a name="ishr-sm4---asm"></a><span data-ttu-id="9be8d-104">ISHR (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="9be8d-104">ishr (sm4 - asm)</span></span>

<span data-ttu-id="9be8d-105">Arithmetische UMSCHALT Rechte (Zeichen Erweiterung).</span><span class="sxs-lookup"><span data-stu-id="9be8d-105">Arithmetic shift right (sign extending).</span></span>



| <span data-ttu-id="9be8d-106">ISHR dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1. Select- \_ Komponente</span><span class="sxs-lookup"><span data-stu-id="9be8d-106">ishr dest\[.mask\], src0\[.swizzle\], src1.select\_component</span></span> |
|--------------------------------------------------------------|



 



| <span data-ttu-id="9be8d-107">Element</span><span class="sxs-lookup"><span data-stu-id="9be8d-107">Item</span></span>                                                            | <span data-ttu-id="9be8d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9be8d-108">Description</span></span>                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="9be8d-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="9be8d-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="9be8d-110">\[in \] enthält das Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="9be8d-110">\[in\] Contains the result of the operation.</span></span><br/> |
| <span data-ttu-id="9be8d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9be8d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9be8d-112">\[in \] enthält den Wert, der verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="9be8d-112">\[in\] Contains the value to be shifted.</span></span><br/>     |
| <span data-ttu-id="9be8d-113"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="9be8d-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="9be8d-114">\[in \] enthält die UMSCHALT Menge.</span><span class="sxs-lookup"><span data-stu-id="9be8d-114">\[in\] Contains the shift amount.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="9be8d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9be8d-115">Remarks</span></span>

<span data-ttu-id="9be8d-116">Diese Anweisung führt eine Komponenten Weise arithmetische Verschiebung jedes 32-Bit-Werts in *src0* rechts durch eine ganzzahlige Bitzahl ohne Vorzeichen aus, die von der LSB 5 Bits (0-31 Range) in Quelle1 bereitgestellt wird *. Wählen Sie \_ Component* aus, und replizieren Sie den Wert von Bit 31.</span><span class="sxs-lookup"><span data-stu-id="9be8d-116">This instruction performs a component-wise arithmetic shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1.select\_component*, replicating the value of bit 31.</span></span> <span data-ttu-id="9be8d-117">Das 32-Bit pro Komponenten Ergebnis wird in *dest* platziert.</span><span class="sxs-lookup"><span data-stu-id="9be8d-117">The 32-bit per component result is placed in *dest*.</span></span> <span data-ttu-id="9be8d-118">Die Anzahl ist ein Skalarwert, der auf alle Komponenten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="9be8d-118">The count is a scalar value applied to all components.</span></span>

<span data-ttu-id="9be8d-119">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="9be8d-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9be8d-120">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="9be8d-120">Vertex Shader</span></span> | <span data-ttu-id="9be8d-121">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="9be8d-121">Geometry Shader</span></span> | <span data-ttu-id="9be8d-122">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="9be8d-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9be8d-123">x</span><span class="sxs-lookup"><span data-stu-id="9be8d-123">x</span></span>             | <span data-ttu-id="9be8d-124">x</span><span class="sxs-lookup"><span data-stu-id="9be8d-124">x</span></span>               | <span data-ttu-id="9be8d-125">x</span><span class="sxs-lookup"><span data-stu-id="9be8d-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9be8d-126">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="9be8d-126">Minimum Shader Model</span></span>

<span data-ttu-id="9be8d-127">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9be8d-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9be8d-128">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="9be8d-128">Shader Model</span></span>                                              | <span data-ttu-id="9be8d-129">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="9be8d-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9be8d-130">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="9be8d-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9be8d-131">ja</span><span class="sxs-lookup"><span data-stu-id="9be8d-131">yes</span></span>       |
| [<span data-ttu-id="9be8d-132">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="9be8d-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9be8d-133">ja</span><span class="sxs-lookup"><span data-stu-id="9be8d-133">yes</span></span>       |
| [<span data-ttu-id="9be8d-134">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="9be8d-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9be8d-135">ja</span><span class="sxs-lookup"><span data-stu-id="9be8d-135">yes</span></span>       |
| [<span data-ttu-id="9be8d-136">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9be8d-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9be8d-137">nein</span><span class="sxs-lookup"><span data-stu-id="9be8d-137">no</span></span>        |
| [<span data-ttu-id="9be8d-138">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9be8d-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9be8d-139">nein</span><span class="sxs-lookup"><span data-stu-id="9be8d-139">no</span></span>        |
| [<span data-ttu-id="9be8d-140">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9be8d-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9be8d-141">nein</span><span class="sxs-lookup"><span data-stu-id="9be8d-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9be8d-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9be8d-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9be8d-143">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9be8d-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





