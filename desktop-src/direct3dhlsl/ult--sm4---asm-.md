---
title: ULT (SM4-ASM)
description: Die Komponenten Weise Vektor-Ganzzahl ohne Vorzeichen, die kleiner als der Vergleich ist.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 624c09d182e9ecfd4d1b603f6fd2c34b83d768ed
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993031"
---
# <a name="ult-sm4---asm"></a><span data-ttu-id="6ae71-103">ULT (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="6ae71-103">ult (sm4 - asm)</span></span>

<span data-ttu-id="6ae71-104">Die Komponenten Weise Vektor-Ganzzahl ohne Vorzeichen, die kleiner als der Vergleich ist.</span><span class="sxs-lookup"><span data-stu-id="6ae71-104">Component-wise vector unsigned integer less-than comparison.</span></span>



| <span data-ttu-id="6ae71-105">ULT dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="6ae71-105">ult dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="6ae71-106">Element</span><span class="sxs-lookup"><span data-stu-id="6ae71-106">Item</span></span>                                                            | <span data-ttu-id="6ae71-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ae71-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="6ae71-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="6ae71-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="6ae71-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="6ae71-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="6ae71-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6ae71-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="6ae71-111">\[im \] Wert, der mit *Quelle1* verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6ae71-111">\[in\] The value to compare to *src1*.</span></span><br/>             |
| <span data-ttu-id="6ae71-112"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="6ae71-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="6ae71-113">\[im \] Wert, der mit *Quelle1* verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6ae71-113">\[in\] The value to compare to *src1*.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="6ae71-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ae71-114">Remarks</span></span>

<span data-ttu-id="6ae71-115">Führt den Vergleich der Ganzzahl ohne Vorzeichen (*src0*  <  *Quelle1*) für jede Komponente aus und schreibt das Ergebnis in *dest*.</span><span class="sxs-lookup"><span data-stu-id="6ae71-115">Performs the unsigned integer comparison (*src0* < *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="6ae71-116">Wenn der Vergleich true ist, gibt diese Anweisung 0xFFFFFFFF für diese Komponente zurück.</span><span class="sxs-lookup"><span data-stu-id="6ae71-116">If the comparison is true, this instruction returns 0xFFFFFFFF for that component.</span></span> <span data-ttu-id="6ae71-117">Andernfalls wird 0x0000000 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ae71-117">Otherwise it returns 0x0000000.</span></span>

<span data-ttu-id="6ae71-118">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="6ae71-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6ae71-119">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="6ae71-119">Vertex Shader</span></span> | <span data-ttu-id="6ae71-120">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="6ae71-120">Geometry Shader</span></span> | <span data-ttu-id="6ae71-121">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="6ae71-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="6ae71-122">x</span><span class="sxs-lookup"><span data-stu-id="6ae71-122">x</span></span>             | <span data-ttu-id="6ae71-123">x</span><span class="sxs-lookup"><span data-stu-id="6ae71-123">x</span></span>               | <span data-ttu-id="6ae71-124">x</span><span class="sxs-lookup"><span data-stu-id="6ae71-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6ae71-125">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="6ae71-125">Minimum Shader Model</span></span>

<span data-ttu-id="6ae71-126">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6ae71-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6ae71-127">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="6ae71-127">Shader Model</span></span>                                              | <span data-ttu-id="6ae71-128">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="6ae71-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6ae71-129">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="6ae71-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6ae71-130">ja</span><span class="sxs-lookup"><span data-stu-id="6ae71-130">yes</span></span>       |
| [<span data-ttu-id="6ae71-131">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="6ae71-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6ae71-132">ja</span><span class="sxs-lookup"><span data-stu-id="6ae71-132">yes</span></span>       |
| [<span data-ttu-id="6ae71-133">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="6ae71-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6ae71-134">ja</span><span class="sxs-lookup"><span data-stu-id="6ae71-134">yes</span></span>       |
| [<span data-ttu-id="6ae71-135">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6ae71-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6ae71-136">nein</span><span class="sxs-lookup"><span data-stu-id="6ae71-136">no</span></span>        |
| [<span data-ttu-id="6ae71-137">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6ae71-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6ae71-138">nein</span><span class="sxs-lookup"><span data-stu-id="6ae71-138">no</span></span>        |
| [<span data-ttu-id="6ae71-139">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6ae71-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6ae71-140">nein</span><span class="sxs-lookup"><span data-stu-id="6ae71-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6ae71-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6ae71-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ae71-142">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6ae71-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





