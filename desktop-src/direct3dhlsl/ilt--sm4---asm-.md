---
title: ILT (SM4-ASM)
description: Der Komponenten Weise Vektor Integerwert ist kleiner als der Vergleich.
ms.assetid: 5F06E568-6234-4778-8169-D8352FAB5297
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2c2e5e47272412bb483e4782e9a6c35e971293c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313632"
---
# <a name="ilt-sm4---asm"></a><span data-ttu-id="79e7a-103">ILT (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="79e7a-103">ilt (sm4 - asm)</span></span>

<span data-ttu-id="79e7a-104">Der Komponenten Weise Vektor Integerwert ist kleiner als der Vergleich.</span><span class="sxs-lookup"><span data-stu-id="79e7a-104">Component-wise vector integer less-than comparison.</span></span>



| <span data-ttu-id="79e7a-105">ILT dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="79e7a-105">ilt dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="79e7a-106">Element</span><span class="sxs-lookup"><span data-stu-id="79e7a-106">Item</span></span>                                                            | <span data-ttu-id="79e7a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79e7a-107">Description</span></span>                                       |
|-----------------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="79e7a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="79e7a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="79e7a-109">Das Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="79e7a-109">The result of the operation.</span></span><br/>           |
| <span data-ttu-id="79e7a-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="79e7a-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="79e7a-111">\[im \] Wert, der mit *Quelle1* verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="79e7a-111">\[in\] The value to compare to *src1*.</span></span><br/> |
| <span data-ttu-id="79e7a-112"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="79e7a-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="79e7a-113">\[im \] Wert, der mit *src0* verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="79e7a-113">\[in\] The value to compare to *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="79e7a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79e7a-114">Remarks</span></span>

<span data-ttu-id="79e7a-115">Führt den ganzzahligen Vergleich *(src0*  <  *Quelle1*) für jede Komponente aus und schreibt das Ergebnis in *dest*.</span><span class="sxs-lookup"><span data-stu-id="79e7a-115">Performs the integer comparison *(src0* < *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="79e7a-116">Wenn der Vergleich true ist, wird 0xFFFFFFFF für diese Komponente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="79e7a-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="79e7a-117">Andernfalls wird 0x0000000 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="79e7a-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="79e7a-118">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="79e7a-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="79e7a-119">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="79e7a-119">Vertex Shader</span></span> | <span data-ttu-id="79e7a-120">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="79e7a-120">Geometry Shader</span></span> | <span data-ttu-id="79e7a-121">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="79e7a-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="79e7a-122">x</span><span class="sxs-lookup"><span data-stu-id="79e7a-122">x</span></span>             | <span data-ttu-id="79e7a-123">x</span><span class="sxs-lookup"><span data-stu-id="79e7a-123">x</span></span>               | <span data-ttu-id="79e7a-124">x</span><span class="sxs-lookup"><span data-stu-id="79e7a-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="79e7a-125">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="79e7a-125">Minimum Shader Model</span></span>



| <span data-ttu-id="79e7a-126">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="79e7a-126">Shader Model</span></span>                                              | <span data-ttu-id="79e7a-127">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="79e7a-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="79e7a-128">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="79e7a-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="79e7a-129">ja</span><span class="sxs-lookup"><span data-stu-id="79e7a-129">yes</span></span>       |
| [<span data-ttu-id="79e7a-130">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="79e7a-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="79e7a-131">ja</span><span class="sxs-lookup"><span data-stu-id="79e7a-131">yes</span></span>       |
| [<span data-ttu-id="79e7a-132">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="79e7a-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="79e7a-133">ja</span><span class="sxs-lookup"><span data-stu-id="79e7a-133">yes</span></span>       |
| [<span data-ttu-id="79e7a-134">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="79e7a-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="79e7a-135">nein</span><span class="sxs-lookup"><span data-stu-id="79e7a-135">no</span></span>        |
| [<span data-ttu-id="79e7a-136">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="79e7a-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="79e7a-137">nein</span><span class="sxs-lookup"><span data-stu-id="79e7a-137">no</span></span>        |
| [<span data-ttu-id="79e7a-138">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="79e7a-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="79e7a-139">nein</span><span class="sxs-lookup"><span data-stu-id="79e7a-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="79e7a-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="79e7a-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79e7a-141">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="79e7a-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





