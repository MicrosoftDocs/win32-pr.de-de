---
title: ige (SM4-ASM)
description: Der Komponenten Weise Vektor Integer größer-oder-gleich-Vergleich.
ms.assetid: 3A3225D1-9A3D-4928-9041-38CB6DE16E2A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8709ebedb054dffe227340f2ccd3de572d92ffce
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101071"
---
# <a name="ige-sm4---asm"></a><span data-ttu-id="09f65-103">ige (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="09f65-103">ige (sm4 - asm)</span></span>

<span data-ttu-id="09f65-104">Der Komponenten Weise Vektor Integer größer-oder-gleich-Vergleich.</span><span class="sxs-lookup"><span data-stu-id="09f65-104">Component-wise vector integer greater-than-or-equal comparison.</span></span>



| <span data-ttu-id="09f65-105">ige dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="09f65-105">ige dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="09f65-106">Element</span><span class="sxs-lookup"><span data-stu-id="09f65-106">Item</span></span>                                                            | <span data-ttu-id="09f65-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="09f65-107">Description</span></span>                                           |
|-----------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="09f65-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="09f65-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="09f65-109">\[im \] Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="09f65-109">\[in\] The result of the operation.</span></span><br/>        |
| <span data-ttu-id="09f65-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="09f65-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="09f65-111">\[in \] der-Komponente, die mit *Quelle1* verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="09f65-111">\[in\] The component to compare to *src1*.</span></span><br/> |
| <span data-ttu-id="09f65-112"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="09f65-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="09f65-113">\[in \] der-Komponente, die mit *src0* verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="09f65-113">\[in\] The component to compare to *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="09f65-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09f65-114">Remarks</span></span>

<span data-ttu-id="09f65-115">Führt den ganzzahligen Vergleich (*src0*  >=  *Quelle1*) für jede Komponente aus und schreibt das Ergebnis in *dest*.</span><span class="sxs-lookup"><span data-stu-id="09f65-115">Performs the integer comparison (*src0* >= *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="09f65-116">Wenn der Vergleich true ist, wird 0xFFFFFFFF für diese Komponente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="09f65-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="09f65-117">Andernfalls wird 0x0000000 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="09f65-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="09f65-118">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="09f65-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="09f65-119">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="09f65-119">Vertex Shader</span></span> | <span data-ttu-id="09f65-120">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="09f65-120">Geometry Shader</span></span> | <span data-ttu-id="09f65-121">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="09f65-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="09f65-122">x</span><span class="sxs-lookup"><span data-stu-id="09f65-122">x</span></span>             | <span data-ttu-id="09f65-123">x</span><span class="sxs-lookup"><span data-stu-id="09f65-123">x</span></span>               | <span data-ttu-id="09f65-124">x</span><span class="sxs-lookup"><span data-stu-id="09f65-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="09f65-125">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="09f65-125">Minimum Shader Model</span></span>

<span data-ttu-id="09f65-126">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="09f65-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="09f65-127">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="09f65-127">Shader Model</span></span>                                              | <span data-ttu-id="09f65-128">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="09f65-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="09f65-129">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="09f65-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="09f65-130">ja</span><span class="sxs-lookup"><span data-stu-id="09f65-130">yes</span></span>       |
| [<span data-ttu-id="09f65-131">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="09f65-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="09f65-132">ja</span><span class="sxs-lookup"><span data-stu-id="09f65-132">yes</span></span>       |
| [<span data-ttu-id="09f65-133">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="09f65-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="09f65-134">ja</span><span class="sxs-lookup"><span data-stu-id="09f65-134">yes</span></span>       |
| [<span data-ttu-id="09f65-135">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="09f65-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="09f65-136">nein</span><span class="sxs-lookup"><span data-stu-id="09f65-136">no</span></span>        |
| [<span data-ttu-id="09f65-137">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="09f65-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="09f65-138">nein</span><span class="sxs-lookup"><span data-stu-id="09f65-138">no</span></span>        |
| [<span data-ttu-id="09f65-139">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="09f65-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="09f65-140">nein</span><span class="sxs-lookup"><span data-stu-id="09f65-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="09f65-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="09f65-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09f65-142">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="09f65-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





