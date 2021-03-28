---
title: Umax (SM4-ASM)
description: Maximale ganzzahlige Ganzzahl ohne Vorzeichen.
ms.assetid: 86BCF7A7-99CA-481B-82B4-E0BA30963344
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceb1fda620facce31132f56ed888d18022ca27ec
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389535"
---
# <a name="umax-sm4---asm"></a><span data-ttu-id="dd807-103">Umax (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="dd807-103">umax (sm4 - asm)</span></span>

<span data-ttu-id="dd807-104">Maximale ganzzahlige Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="dd807-104">Component-wise unsigned integer maximum.</span></span>



| <span data-ttu-id="dd807-105">Umax dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="dd807-105">umax dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\],</span></span> |
|---------------------------------------------------------|



 



| <span data-ttu-id="dd807-106">Element</span><span class="sxs-lookup"><span data-stu-id="dd807-106">Item</span></span>                                                            | <span data-ttu-id="dd807-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd807-107">Description</span></span>                                                                                                            |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd807-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="dd807-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="dd807-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="dd807-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="dd807-110">*dest*  =  *src0*  >  *Quelle1* ?</span><span class="sxs-lookup"><span data-stu-id="dd807-110">*dest* = *src0* > *src1* ?</span></span> <span data-ttu-id="dd807-111">*src0* : *Quelle1*</span><span class="sxs-lookup"><span data-stu-id="dd807-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="dd807-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="dd807-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="dd807-113">\[im \] Wert, der mit *Quelle1* verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd807-113">\[in\] The value to compare to *src1*.</span></span><br/>                                                                      |
| <span data-ttu-id="dd807-114"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="dd807-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="dd807-115">\[im \] Wert, der mit *src0* verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd807-115">\[in\] The value to compare to *src0*.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="dd807-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd807-116">Remarks</span></span>

<span data-ttu-id="dd807-117">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="dd807-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="dd807-118">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="dd807-118">Vertex Shader</span></span> | <span data-ttu-id="dd807-119">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="dd807-119">Geometry Shader</span></span> | <span data-ttu-id="dd807-120">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="dd807-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="dd807-121">x</span><span class="sxs-lookup"><span data-stu-id="dd807-121">x</span></span>             | <span data-ttu-id="dd807-122">x</span><span class="sxs-lookup"><span data-stu-id="dd807-122">x</span></span>               | <span data-ttu-id="dd807-123">x</span><span class="sxs-lookup"><span data-stu-id="dd807-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="dd807-124">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="dd807-124">Minimum Shader Model</span></span>

<span data-ttu-id="dd807-125">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dd807-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="dd807-126">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="dd807-126">Shader Model</span></span>                                              | <span data-ttu-id="dd807-127">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="dd807-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="dd807-128">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="dd807-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="dd807-129">ja</span><span class="sxs-lookup"><span data-stu-id="dd807-129">yes</span></span>       |
| [<span data-ttu-id="dd807-130">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="dd807-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="dd807-131">ja</span><span class="sxs-lookup"><span data-stu-id="dd807-131">yes</span></span>       |
| [<span data-ttu-id="dd807-132">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="dd807-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="dd807-133">ja</span><span class="sxs-lookup"><span data-stu-id="dd807-133">yes</span></span>       |
| [<span data-ttu-id="dd807-134">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dd807-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="dd807-135">nein</span><span class="sxs-lookup"><span data-stu-id="dd807-135">no</span></span>        |
| [<span data-ttu-id="dd807-136">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dd807-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="dd807-137">nein</span><span class="sxs-lookup"><span data-stu-id="dd807-137">no</span></span>        |
| [<span data-ttu-id="dd807-138">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dd807-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="dd807-139">nein</span><span class="sxs-lookup"><span data-stu-id="dd807-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="dd807-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dd807-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd807-141">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dd807-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





