---
title: ine (SM4-ASM)
description: Nicht gleicher Vergleich der Komponenten weisen Vektor Ganzzahl.
ms.assetid: 5BED97D3-8FF6-4F1C-819B-DC8B4A4F2CCA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b74a68cf4b1b3c7473f8264e8b83910f4cb0677
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993167"
---
# <a name="ine-sm4---asm"></a><span data-ttu-id="bf5c3-103">ine (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="bf5c3-103">ine (sm4 - asm)</span></span>

<span data-ttu-id="bf5c3-104">Nicht gleicher Vergleich der Komponenten weisen Vektor Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="bf5c3-104">Component-wise vector integer not-equal comparison.</span></span>



| <span data-ttu-id="bf5c3-105">ine dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="bf5c3-105">ine dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="bf5c3-106">Element</span><span class="sxs-lookup"><span data-stu-id="bf5c3-106">Item</span></span>                                                            | <span data-ttu-id="bf5c3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf5c3-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="bf5c3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="bf5c3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="bf5c3-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="bf5c3-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="bf5c3-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="bf5c3-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="bf5c3-111">\[in \] enthält den Wert, der mit *Quelle1* verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf5c3-111">\[in\] Contains the value to compare to *src1*.</span></span><br/>    |
| <span data-ttu-id="bf5c3-112"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="bf5c3-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="bf5c3-113">\[in \] enthält den Wert, der mit *src0* verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf5c3-113">\[in\] Contains the value to compare to *src0*.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="bf5c3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf5c3-114">Remarks</span></span>

<span data-ttu-id="bf5c3-115">Führt den ganzzahligen Vergleich (*src0* ! = *Quelle1*) für jede Komponente aus und schreibt das Ergebnis in *dest*.</span><span class="sxs-lookup"><span data-stu-id="bf5c3-115">Performs the integer comparison (*src0* != *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="bf5c3-116">Wenn der Vergleich true ist, wird 0xFFFFFFFF für diese Komponente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bf5c3-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="bf5c3-117">Andernfalls wird 0x0000000 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bf5c3-117">Otherwise 0x0000000 is returned</span></span>

<span data-ttu-id="bf5c3-118">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="bf5c3-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="bf5c3-119">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="bf5c3-119">Vertex Shader</span></span> | <span data-ttu-id="bf5c3-120">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="bf5c3-120">Geometry Shader</span></span> | <span data-ttu-id="bf5c3-121">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="bf5c3-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="bf5c3-122">x</span><span class="sxs-lookup"><span data-stu-id="bf5c3-122">x</span></span>             | <span data-ttu-id="bf5c3-123">x</span><span class="sxs-lookup"><span data-stu-id="bf5c3-123">x</span></span>               | <span data-ttu-id="bf5c3-124">x</span><span class="sxs-lookup"><span data-stu-id="bf5c3-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bf5c3-125">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="bf5c3-125">Minimum Shader Model</span></span>

<span data-ttu-id="bf5c3-126">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bf5c3-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bf5c3-127">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="bf5c3-127">Shader Model</span></span>                                              | <span data-ttu-id="bf5c3-128">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="bf5c3-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bf5c3-129">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="bf5c3-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bf5c3-130">ja</span><span class="sxs-lookup"><span data-stu-id="bf5c3-130">yes</span></span>       |
| [<span data-ttu-id="bf5c3-131">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="bf5c3-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bf5c3-132">ja</span><span class="sxs-lookup"><span data-stu-id="bf5c3-132">yes</span></span>       |
| [<span data-ttu-id="bf5c3-133">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="bf5c3-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bf5c3-134">ja</span><span class="sxs-lookup"><span data-stu-id="bf5c3-134">yes</span></span>       |
| [<span data-ttu-id="bf5c3-135">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf5c3-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bf5c3-136">nein</span><span class="sxs-lookup"><span data-stu-id="bf5c3-136">no</span></span>        |
| [<span data-ttu-id="bf5c3-137">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf5c3-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bf5c3-138">nein</span><span class="sxs-lookup"><span data-stu-id="bf5c3-138">no</span></span>        |
| [<span data-ttu-id="bf5c3-139">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf5c3-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bf5c3-140">nein</span><span class="sxs-lookup"><span data-stu-id="bf5c3-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bf5c3-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bf5c3-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf5c3-142">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf5c3-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





