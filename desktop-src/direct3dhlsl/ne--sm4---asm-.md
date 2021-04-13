---
title: ne (SM4-ASM)
description: Nicht gleicher Vergleich für den Komponenten weisen Vektor Gleit Komma Wert.
ms.assetid: 5BED97D3-8FF6-4F1C-819B-DC8B4A4F2CCA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e53ff726047bd1870e6c836f4508bdf87001b3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389540"
---
# <a name="ne-sm4---asm"></a><span data-ttu-id="c69f1-103">ne (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c69f1-103">ne (sm4 - asm)</span></span>

<span data-ttu-id="c69f1-104">Nicht gleicher Vergleich für den Komponenten weisen Vektor Gleit Komma Wert.</span><span class="sxs-lookup"><span data-stu-id="c69f1-104">Component-wise vector floating point not-equal comparison.</span></span>



| <span data-ttu-id="c69f1-105">ne dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="c69f1-105">ne dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------|



 



| <span data-ttu-id="c69f1-106">Element</span><span class="sxs-lookup"><span data-stu-id="c69f1-106">Item</span></span>                                                            | <span data-ttu-id="c69f1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c69f1-107">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="c69f1-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c69f1-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="c69f1-109">\[im \] Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="c69f1-109">\[in\] The result of the operation.</span></span><br/>         |
| <span data-ttu-id="c69f1-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c69f1-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c69f1-111">\[in \] den Komponenten, die mit *Quelle1* verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c69f1-111">\[in\] The components to compare to *src1*.</span></span><br/> |
| <span data-ttu-id="c69f1-112"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="c69f1-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="c69f1-113">\[in \] den Komponenten, die mit *src0* verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c69f1-113">\[in\] The components to compare to *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c69f1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c69f1-114">Remarks</span></span>

<span data-ttu-id="c69f1-115">Diese Anweisung führt den float-Vergleich (*src0* ! = *Quelle1*) für jede Komponente aus und schreibt das Ergebnis in *dest*.</span><span class="sxs-lookup"><span data-stu-id="c69f1-115">This instruction performs the float comparison (*src0* != *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="c69f1-116">Wenn der Vergleich true ist, wird 0xFFFFFFFF für diese Komponente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c69f1-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="c69f1-117">Andernfalls wird 0x0000000 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c69f1-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="c69f1-118">Denorms werden geleert, bevor der Vergleich mit der ursprünglichen Quelle unverändert registriert wird.</span><span class="sxs-lookup"><span data-stu-id="c69f1-118">Denorms are flushed before comparison with original source registers untouched.</span></span>

<span data-ttu-id="c69f1-119">+ 0 ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="c69f1-119">+0 equals -0.</span></span>

<span data-ttu-id="c69f1-120">Der Vergleich mit Nan gibt true zurück.</span><span class="sxs-lookup"><span data-stu-id="c69f1-120">Comparison with NaN returns true.</span></span>

<span data-ttu-id="c69f1-121">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="c69f1-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c69f1-122">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="c69f1-122">Vertex Shader</span></span> | <span data-ttu-id="c69f1-123">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="c69f1-123">Geometry Shader</span></span> | <span data-ttu-id="c69f1-124">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="c69f1-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c69f1-125">x</span><span class="sxs-lookup"><span data-stu-id="c69f1-125">x</span></span>             | <span data-ttu-id="c69f1-126">x</span><span class="sxs-lookup"><span data-stu-id="c69f1-126">x</span></span>               | <span data-ttu-id="c69f1-127">x</span><span class="sxs-lookup"><span data-stu-id="c69f1-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c69f1-128">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="c69f1-128">Minimum Shader Model</span></span>

<span data-ttu-id="c69f1-129">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c69f1-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c69f1-130">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="c69f1-130">Shader Model</span></span>                                              | <span data-ttu-id="c69f1-131">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="c69f1-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c69f1-132">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="c69f1-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c69f1-133">ja</span><span class="sxs-lookup"><span data-stu-id="c69f1-133">yes</span></span>       |
| [<span data-ttu-id="c69f1-134">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="c69f1-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c69f1-135">ja</span><span class="sxs-lookup"><span data-stu-id="c69f1-135">yes</span></span>       |
| [<span data-ttu-id="c69f1-136">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="c69f1-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c69f1-137">ja</span><span class="sxs-lookup"><span data-stu-id="c69f1-137">yes</span></span>       |
| [<span data-ttu-id="c69f1-138">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c69f1-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c69f1-139">nein</span><span class="sxs-lookup"><span data-stu-id="c69f1-139">no</span></span>        |
| [<span data-ttu-id="c69f1-140">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c69f1-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c69f1-141">nein</span><span class="sxs-lookup"><span data-stu-id="c69f1-141">no</span></span>        |
| [<span data-ttu-id="c69f1-142">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c69f1-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c69f1-143">nein</span><span class="sxs-lookup"><span data-stu-id="c69f1-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c69f1-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c69f1-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c69f1-145">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c69f1-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





