---
title: ishl (SM4-ASM)
description: Nach links verschieben. | ishl (SM4-ASM)
ms.assetid: FA0213B8-8A76-4916-8B2F-0983C404A838
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e14225f8c8b0e46cf0ba6eda61f96e4563a904e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995582"
---
# <a name="ishl-sm4---asm"></a><span data-ttu-id="61fe2-104">ishl (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="61fe2-104">ishl (sm4 - asm)</span></span>

<span data-ttu-id="61fe2-105">Nach links verschieben.</span><span class="sxs-lookup"><span data-stu-id="61fe2-105">Shift left.</span></span>



| <span data-ttu-id="61fe2-106">dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1. Select- \_ Komponente</span><span class="sxs-lookup"><span data-stu-id="61fe2-106">dest\[.mask\], src0\[.swizzle\], src1.select\_component</span></span> |
|---------------------------------------------------------|



 



| <span data-ttu-id="61fe2-107">Element</span><span class="sxs-lookup"><span data-stu-id="61fe2-107">Item</span></span>                                                            | <span data-ttu-id="61fe2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61fe2-108">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="61fe2-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="61fe2-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="61fe2-110">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="61fe2-110">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="61fe2-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="61fe2-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="61fe2-112">\[in \] enthält die Werte, die verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="61fe2-112">\[in\] Contains the values to be shifted.</span></span><br/>          |
| <span data-ttu-id="61fe2-113"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="61fe2-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="61fe2-114">\[in \] enthält die UMSCHALT Menge.</span><span class="sxs-lookup"><span data-stu-id="61fe2-114">\[in\] Contains the shift amount.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="61fe2-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61fe2-115">Remarks</span></span>

<span data-ttu-id="61fe2-116">Diese Anweisung führt eine Komponenten Weise Verschiebung jedes 32-Bit-Werts in *src0* nach links durch eine ganzzahlige Bitzahl ohne Vorzeichen aus, die von der LSB 5 Bits (0-31 Range) in Quelle1 bereitgestellt wird *. Wählen Sie \_ Komponente* aus, und fügen Sie 0 ein.</span><span class="sxs-lookup"><span data-stu-id="61fe2-116">This instruction performs a component-wise shift of each 32-bit value in *src0* left by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1.select\_component*, inserting 0.</span></span> <span data-ttu-id="61fe2-117">Die 32-Bit-pro-Komponenten Ergebnisse werden in *dest* platziert.</span><span class="sxs-lookup"><span data-stu-id="61fe2-117">The 32-bit per component results are placed in *dest*.</span></span> <span data-ttu-id="61fe2-118">Die Anzahl ist ein Skalarwert, der auf alle Komponenten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="61fe2-118">The count is a scalar value applied to all components.</span></span>

<span data-ttu-id="61fe2-119">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="61fe2-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="61fe2-120">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="61fe2-120">Vertex Shader</span></span> | <span data-ttu-id="61fe2-121">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="61fe2-121">Geometry Shader</span></span> | <span data-ttu-id="61fe2-122">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="61fe2-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="61fe2-123">x</span><span class="sxs-lookup"><span data-stu-id="61fe2-123">x</span></span>             | <span data-ttu-id="61fe2-124">x</span><span class="sxs-lookup"><span data-stu-id="61fe2-124">x</span></span>               | <span data-ttu-id="61fe2-125">x</span><span class="sxs-lookup"><span data-stu-id="61fe2-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="61fe2-126">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="61fe2-126">Minimum Shader Model</span></span>

<span data-ttu-id="61fe2-127">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="61fe2-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="61fe2-128">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="61fe2-128">Shader Model</span></span>                                              | <span data-ttu-id="61fe2-129">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="61fe2-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="61fe2-130">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="61fe2-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="61fe2-131">ja</span><span class="sxs-lookup"><span data-stu-id="61fe2-131">yes</span></span>       |
| [<span data-ttu-id="61fe2-132">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="61fe2-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="61fe2-133">ja</span><span class="sxs-lookup"><span data-stu-id="61fe2-133">yes</span></span>       |
| [<span data-ttu-id="61fe2-134">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="61fe2-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="61fe2-135">ja</span><span class="sxs-lookup"><span data-stu-id="61fe2-135">yes</span></span>       |
| [<span data-ttu-id="61fe2-136">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="61fe2-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="61fe2-137">nein</span><span class="sxs-lookup"><span data-stu-id="61fe2-137">no</span></span>        |
| [<span data-ttu-id="61fe2-138">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="61fe2-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="61fe2-139">nein</span><span class="sxs-lookup"><span data-stu-id="61fe2-139">no</span></span>        |
| [<span data-ttu-id="61fe2-140">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="61fe2-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="61fe2-141">nein</span><span class="sxs-lookup"><span data-stu-id="61fe2-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="61fe2-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="61fe2-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61fe2-143">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="61fe2-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





