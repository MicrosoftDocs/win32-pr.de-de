---
title: EQ (SM4-ASM)
description: Vergleichspunkt-Gleichheits Vergleich in Komponenten weiser Vektor.
ms.assetid: 925578E4-0161-45A9-840F-14AA65FF4F33
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f47dc7bda7b1c61c251ace061fc75897788b968
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389482"
---
# <a name="eq-sm4---asm"></a><span data-ttu-id="31980-103">EQ (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="31980-103">eq (sm4 - asm)</span></span>

<span data-ttu-id="31980-104">Vergleichspunkt-Gleichheits Vergleich in Komponenten weiser Vektor.</span><span class="sxs-lookup"><span data-stu-id="31980-104">Component-wise vector floating point equality comparison.</span></span>



| <span data-ttu-id="31980-105">EQ dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="31980-105">eq dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------|



 



| <span data-ttu-id="31980-106">Element</span><span class="sxs-lookup"><span data-stu-id="31980-106">Item</span></span>                                                            | <span data-ttu-id="31980-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="31980-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="31980-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="31980-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="31980-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="31980-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="31980-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="31980-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="31980-111">\[in \] der Komponente, die an *Quelle1* comapre ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="31980-111">\[in\] The component to comapre to *src1*.</span></span><br/>         |
| <span data-ttu-id="31980-112"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="31980-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="31980-113">\[in \] der Komponente, die an *src0* comapre ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="31980-113">\[in\] The component to comapre to *src0*.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="31980-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31980-114">Remarks</span></span>

<span data-ttu-id="31980-115">Führt den float-Vergleich (*src0*  ==  *Quelle1*) für jede Komponente aus und schreibt das Ergebnis in *dest*.</span><span class="sxs-lookup"><span data-stu-id="31980-115">Performs the float comparison (*src0* == *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="31980-116">Wenn der Vergleich true ist, wird 0xFFFFFFFF für diese Komponente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="31980-116">If the comparison is true, 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="31980-117">Andernfalls wird 0x0000000 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="31980-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="31980-118">Denorms werden vor dem Vergleich geleert (die ursprüngliche Quelle wird unverändert registriert).</span><span class="sxs-lookup"><span data-stu-id="31980-118">Denorms are flushed before comparison (original source registers untouched).</span></span> <span data-ttu-id="31980-119">+ 0 ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="31980-119">+0 equals -0.</span></span> <span data-ttu-id="31980-120">Der Vergleich mit Nan gibt false zurück.</span><span class="sxs-lookup"><span data-stu-id="31980-120">Comparison with NaN returns false.</span></span>

<span data-ttu-id="31980-121">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="31980-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="31980-122">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="31980-122">Vertex Shader</span></span> | <span data-ttu-id="31980-123">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="31980-123">Geometry Shader</span></span> | <span data-ttu-id="31980-124">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="31980-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="31980-125">x</span><span class="sxs-lookup"><span data-stu-id="31980-125">x</span></span>             | <span data-ttu-id="31980-126">x</span><span class="sxs-lookup"><span data-stu-id="31980-126">x</span></span>               | <span data-ttu-id="31980-127">x</span><span class="sxs-lookup"><span data-stu-id="31980-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="31980-128">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="31980-128">Minimum Shader Model</span></span>

<span data-ttu-id="31980-129">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="31980-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="31980-130">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="31980-130">Shader Model</span></span>                                              | <span data-ttu-id="31980-131">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="31980-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="31980-132">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="31980-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="31980-133">ja</span><span class="sxs-lookup"><span data-stu-id="31980-133">yes</span></span>       |
| [<span data-ttu-id="31980-134">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="31980-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="31980-135">ja</span><span class="sxs-lookup"><span data-stu-id="31980-135">yes</span></span>       |
| [<span data-ttu-id="31980-136">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="31980-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="31980-137">ja</span><span class="sxs-lookup"><span data-stu-id="31980-137">yes</span></span>       |
| [<span data-ttu-id="31980-138">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="31980-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="31980-139">nein</span><span class="sxs-lookup"><span data-stu-id="31980-139">no</span></span>        |
| [<span data-ttu-id="31980-140">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="31980-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="31980-141">nein</span><span class="sxs-lookup"><span data-stu-id="31980-141">no</span></span>        |
| [<span data-ttu-id="31980-142">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="31980-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="31980-143">nein</span><span class="sxs-lookup"><span data-stu-id="31980-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="31980-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="31980-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31980-145">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="31980-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





