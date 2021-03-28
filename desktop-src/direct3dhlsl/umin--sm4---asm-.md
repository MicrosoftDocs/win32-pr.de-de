---
title: Umschlag (SM4-ASM)
description: Minimale ganzzahlige Ganzzahl ohne Vorzeichen.
ms.assetid: 134B128F-7B47-4819-A576-80766EDB14C9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 059b9660e4969b252c867a009a920259c92bff18
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101078"
---
# <a name="umin-sm4---asm"></a><span data-ttu-id="2437a-103">Umschlag (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="2437a-103">umin (sm4 - asm)</span></span>

<span data-ttu-id="2437a-104">Minimale ganzzahlige Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="2437a-104">Component-wise unsigned integer minimum.</span></span>



| <span data-ttu-id="2437a-105">"enin dest \[ . Mask" \] , "src0 \[ . Swizzle" \] , "Quelle1 \[ . Swizzle" \] ,</span><span class="sxs-lookup"><span data-stu-id="2437a-105">umin dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\],</span></span> |
|---------------------------------------------------------|



 



| <span data-ttu-id="2437a-106">Element</span><span class="sxs-lookup"><span data-stu-id="2437a-106">Item</span></span>                                                            | <span data-ttu-id="2437a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2437a-107">Description</span></span>                                                                                                            |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2437a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="2437a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="2437a-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="2437a-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="2437a-110">*dest*  =  *src0*  <  *Quelle1* ?</span><span class="sxs-lookup"><span data-stu-id="2437a-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="2437a-111">*src0* : *Quelle1*</span><span class="sxs-lookup"><span data-stu-id="2437a-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="2437a-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2437a-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="2437a-113">\[im \] Wert, der mit *Quelle1* verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2437a-113">\[in\] The value to compare to *src1*.</span></span><br/>                                                                      |
| <span data-ttu-id="2437a-114"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="2437a-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="2437a-115">\[im \] Wert, der mit *src0* verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2437a-115">\[in\] The value to compare to *src0*.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="2437a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2437a-116">Remarks</span></span>

<span data-ttu-id="2437a-117">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="2437a-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2437a-118">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="2437a-118">Vertex Shader</span></span> | <span data-ttu-id="2437a-119">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="2437a-119">Geometry Shader</span></span> | <span data-ttu-id="2437a-120">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="2437a-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2437a-121">x</span><span class="sxs-lookup"><span data-stu-id="2437a-121">x</span></span>             | <span data-ttu-id="2437a-122">x</span><span class="sxs-lookup"><span data-stu-id="2437a-122">x</span></span>               | <span data-ttu-id="2437a-123">x</span><span class="sxs-lookup"><span data-stu-id="2437a-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2437a-124">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="2437a-124">Minimum Shader Model</span></span>

<span data-ttu-id="2437a-125">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2437a-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2437a-126">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="2437a-126">Shader Model</span></span>                                              | <span data-ttu-id="2437a-127">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="2437a-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2437a-128">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="2437a-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2437a-129">ja</span><span class="sxs-lookup"><span data-stu-id="2437a-129">yes</span></span>       |
| [<span data-ttu-id="2437a-130">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="2437a-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2437a-131">ja</span><span class="sxs-lookup"><span data-stu-id="2437a-131">yes</span></span>       |
| [<span data-ttu-id="2437a-132">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="2437a-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2437a-133">ja</span><span class="sxs-lookup"><span data-stu-id="2437a-133">yes</span></span>       |
| [<span data-ttu-id="2437a-134">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2437a-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2437a-135">nein</span><span class="sxs-lookup"><span data-stu-id="2437a-135">no</span></span>        |
| [<span data-ttu-id="2437a-136">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2437a-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2437a-137">nein</span><span class="sxs-lookup"><span data-stu-id="2437a-137">no</span></span>        |
| [<span data-ttu-id="2437a-138">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2437a-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2437a-139">nein</span><span class="sxs-lookup"><span data-stu-id="2437a-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2437a-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2437a-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2437a-141">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2437a-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





