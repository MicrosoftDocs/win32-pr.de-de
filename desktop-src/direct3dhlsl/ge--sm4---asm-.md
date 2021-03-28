---
title: GE (SM4-ASM)
description: Der Komponenten Weise Vektor Gleit Komma Wert größer oder gleich.
ms.assetid: 658AF249-4935-41AF-972A-D8CDEABA76AA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c93d21d9ac044e2ad4d63e954a4732a15794b123
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389520"
---
# <a name="ge-sm4---asm"></a><span data-ttu-id="6c790-103">GE (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="6c790-103">ge (sm4 - asm)</span></span>

<span data-ttu-id="6c790-104">Der Komponenten Weise Vektor Gleit Komma Wert größer oder gleich.</span><span class="sxs-lookup"><span data-stu-id="6c790-104">Component-wise vector floating point greater-than-or-equal comparison.</span></span>



| <span data-ttu-id="6c790-105">ge dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="6c790-105">ge dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------|



 



| <span data-ttu-id="6c790-106">Element</span><span class="sxs-lookup"><span data-stu-id="6c790-106">Item</span></span>                                                            | <span data-ttu-id="6c790-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6c790-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="6c790-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="6c790-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="6c790-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="6c790-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="6c790-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6c790-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="6c790-111">\[in \] der-Komponente, die mit *Quelle1* verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6c790-111">\[in\] The component to compare to *src1*.</span></span><br/>         |
| <span data-ttu-id="6c790-112"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="6c790-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="6c790-113">\[in \] der-Komponente, die mit *src0* verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6c790-113">\[in\] The component to compare to *src0*.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="6c790-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c790-114">Remarks</span></span>

<span data-ttu-id="6c790-115">Führt den float-Vergleich (*src0*  >=  *Quelle1*) für jede Komponente aus und schreibt das Ergebnis in *dest*.</span><span class="sxs-lookup"><span data-stu-id="6c790-115">Performs the float comparison (*src0* >= *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="6c790-116">Wenn der Vergleich true ist, wird 0xFFFFFFFF für diese Komponente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c790-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="6c790-117">Andernfalls wird 0x0000000 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c790-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="6c790-118">Denorms werden vor dem Vergleich geleert, und die ursprünglichen Quell Register sind unverändert.</span><span class="sxs-lookup"><span data-stu-id="6c790-118">Denorms are flushed before comparison, and original source registers are untouched.</span></span> <span data-ttu-id="6c790-119">+ 0 ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="6c790-119">+0 equals -0.</span></span> <span data-ttu-id="6c790-120">Der Vergleich mit Nan gibt false zurück.</span><span class="sxs-lookup"><span data-stu-id="6c790-120">Comparison with NaN returns false.</span></span>

<span data-ttu-id="6c790-121">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="6c790-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6c790-122">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="6c790-122">Vertex Shader</span></span> | <span data-ttu-id="6c790-123">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="6c790-123">Geometry Shader</span></span> | <span data-ttu-id="6c790-124">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="6c790-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="6c790-125">x</span><span class="sxs-lookup"><span data-stu-id="6c790-125">x</span></span>             | <span data-ttu-id="6c790-126">x</span><span class="sxs-lookup"><span data-stu-id="6c790-126">x</span></span>               | <span data-ttu-id="6c790-127">x</span><span class="sxs-lookup"><span data-stu-id="6c790-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6c790-128">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="6c790-128">Minimum Shader Model</span></span>

<span data-ttu-id="6c790-129">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6c790-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6c790-130">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="6c790-130">Shader Model</span></span>                                              | <span data-ttu-id="6c790-131">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="6c790-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6c790-132">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="6c790-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6c790-133">ja</span><span class="sxs-lookup"><span data-stu-id="6c790-133">yes</span></span>       |
| [<span data-ttu-id="6c790-134">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="6c790-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6c790-135">ja</span><span class="sxs-lookup"><span data-stu-id="6c790-135">yes</span></span>       |
| [<span data-ttu-id="6c790-136">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="6c790-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6c790-137">ja</span><span class="sxs-lookup"><span data-stu-id="6c790-137">yes</span></span>       |
| [<span data-ttu-id="6c790-138">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6c790-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6c790-139">nein</span><span class="sxs-lookup"><span data-stu-id="6c790-139">no</span></span>        |
| [<span data-ttu-id="6c790-140">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6c790-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6c790-141">nein</span><span class="sxs-lookup"><span data-stu-id="6c790-141">no</span></span>        |
| [<span data-ttu-id="6c790-142">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6c790-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6c790-143">nein</span><span class="sxs-lookup"><span data-stu-id="6c790-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6c790-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6c790-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c790-145">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6c790-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





