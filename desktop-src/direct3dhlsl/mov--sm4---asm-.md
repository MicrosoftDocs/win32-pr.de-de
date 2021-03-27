---
title: MOV (SM4-ASM)
description: Komponenten weises verschieben. | MOV (SM4-ASM)
ms.assetid: A8865237-59D3-4332-9F09-157E10C4FFC6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f029cd8a31a9348e729681878773c225b87b9fbb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219137"
---
# <a name="mov-sm4---asm"></a><span data-ttu-id="d32f4-104">MOV (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d32f4-104">mov (sm4 - asm)</span></span>

<span data-ttu-id="d32f4-105">Komponenten weises verschieben.</span><span class="sxs-lookup"><span data-stu-id="d32f4-105">Component-wise move.</span></span>



| <span data-ttu-id="d32f4-106">Anweisung: MOV \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="d32f4-106">Instruction: mov\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------|



 



| <span data-ttu-id="d32f4-107">Element</span><span class="sxs-lookup"><span data-stu-id="d32f4-107">Item</span></span>                                                            | <span data-ttu-id="d32f4-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d32f4-108">Description</span></span>                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d32f4-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d32f4-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d32f4-110">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="d32f4-110">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="d32f4-111">*dest*  =  *src0*</span><span class="sxs-lookup"><span data-stu-id="d32f4-111">*dest* = *src0*</span></span><br/> |
| <span data-ttu-id="d32f4-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d32f4-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d32f4-113">\[in \] den zu Verschieb-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="d32f4-113">\[in\] The components to move.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="d32f4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d32f4-114">Remarks</span></span>

<span data-ttu-id="d32f4-115">Bei den Modifizierern, mit Ausnahme von Swizzle, wird davon ausgegangen, dass die Daten Gleit Komma sind.</span><span class="sxs-lookup"><span data-stu-id="d32f4-115">The modifiers, other than swizzle, assume the data is floating point.</span></span> <span data-ttu-id="d32f4-116">Das Fehlen von Modifizierern verschiebt Daten nur, ohne Bits zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d32f4-116">The absence of modifiers just moves data without altering bits.</span></span>

<span data-ttu-id="d32f4-117">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="d32f4-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d32f4-118">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="d32f4-118">Vertex Shader</span></span> | <span data-ttu-id="d32f4-119">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="d32f4-119">Geometry Shader</span></span> | <span data-ttu-id="d32f4-120">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="d32f4-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d32f4-121">x</span><span class="sxs-lookup"><span data-stu-id="d32f4-121">x</span></span>             | <span data-ttu-id="d32f4-122">x</span><span class="sxs-lookup"><span data-stu-id="d32f4-122">x</span></span>               | <span data-ttu-id="d32f4-123">x</span><span class="sxs-lookup"><span data-stu-id="d32f4-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d32f4-124">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="d32f4-124">Minimum Shader Model</span></span>

<span data-ttu-id="d32f4-125">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d32f4-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d32f4-126">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="d32f4-126">Shader Model</span></span>                                              | <span data-ttu-id="d32f4-127">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="d32f4-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d32f4-128">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="d32f4-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d32f4-129">ja</span><span class="sxs-lookup"><span data-stu-id="d32f4-129">yes</span></span>       |
| [<span data-ttu-id="d32f4-130">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="d32f4-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d32f4-131">ja</span><span class="sxs-lookup"><span data-stu-id="d32f4-131">yes</span></span>       |
| [<span data-ttu-id="d32f4-132">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="d32f4-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d32f4-133">ja</span><span class="sxs-lookup"><span data-stu-id="d32f4-133">yes</span></span>       |
| [<span data-ttu-id="d32f4-134">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d32f4-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d32f4-135">nein</span><span class="sxs-lookup"><span data-stu-id="d32f4-135">no</span></span>        |
| [<span data-ttu-id="d32f4-136">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d32f4-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d32f4-137">nein</span><span class="sxs-lookup"><span data-stu-id="d32f4-137">no</span></span>        |
| [<span data-ttu-id="d32f4-138">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d32f4-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d32f4-139">nein</span><span class="sxs-lookup"><span data-stu-id="d32f4-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d32f4-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d32f4-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d32f4-141">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d32f4-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





