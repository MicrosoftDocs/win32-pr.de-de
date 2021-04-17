---
title: InEG (SM4-ASM)
description: 2-Ergänzung.
ms.assetid: 20C1EEC8-E349-4398-8EE3-EDD01EBCD4B1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec4da3e0cbb08bee7bd732a4da8175705d1e1a0f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389564"
---
# <a name="ineg-sm4---asm"></a><span data-ttu-id="aceea-103">InEG (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="aceea-103">ineg (sm4 - asm)</span></span>

<span data-ttu-id="aceea-104">2-Ergänzung.</span><span class="sxs-lookup"><span data-stu-id="aceea-104">2's complement.</span></span>



| <span data-ttu-id="aceea-105">InEG dest \[ . mask \] , src0 \[ . Swizzle</span><span class="sxs-lookup"><span data-stu-id="aceea-105">ineg dest\[.mask\], src0\[.swizzle</span></span> |
|------------------------------------|



 



| <span data-ttu-id="aceea-106">Element</span><span class="sxs-lookup"><span data-stu-id="aceea-106">Item</span></span>                                                            | <span data-ttu-id="aceea-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aceea-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="aceea-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="aceea-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="aceea-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="aceea-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="aceea-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="aceea-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="aceea-111">\[in \] enthält die Werte für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="aceea-111">\[in\] Contains the values for the operation.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="aceea-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aceea-112">Remarks</span></span>

<span data-ttu-id="aceea-113">Diese Anweisung führt das Komplement der einzelnen 32-Bit-Werte in *src0* auf Komponenten Weise 2 aus.</span><span class="sxs-lookup"><span data-stu-id="aceea-113">This instruction performs component-wise 2's complement of each 32-bit value in *src0*.</span></span> <span data-ttu-id="aceea-114">Die 32-Bit-Ergebnisse werden in *dest* gespeichert.</span><span class="sxs-lookup"><span data-stu-id="aceea-114">The 32-bit results are stored in *dest*.</span></span>

<span data-ttu-id="aceea-115">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="aceea-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="aceea-116">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="aceea-116">Vertex Shader</span></span> | <span data-ttu-id="aceea-117">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="aceea-117">Geometry Shader</span></span> | <span data-ttu-id="aceea-118">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="aceea-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="aceea-119">x</span><span class="sxs-lookup"><span data-stu-id="aceea-119">x</span></span>             | <span data-ttu-id="aceea-120">x</span><span class="sxs-lookup"><span data-stu-id="aceea-120">x</span></span>               | <span data-ttu-id="aceea-121">x</span><span class="sxs-lookup"><span data-stu-id="aceea-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="aceea-122">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="aceea-122">Minimum Shader Model</span></span>

<span data-ttu-id="aceea-123">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aceea-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="aceea-124">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="aceea-124">Shader Model</span></span>                                              | <span data-ttu-id="aceea-125">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="aceea-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="aceea-126">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="aceea-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="aceea-127">ja</span><span class="sxs-lookup"><span data-stu-id="aceea-127">yes</span></span>       |
| [<span data-ttu-id="aceea-128">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="aceea-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="aceea-129">ja</span><span class="sxs-lookup"><span data-stu-id="aceea-129">yes</span></span>       |
| [<span data-ttu-id="aceea-130">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="aceea-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="aceea-131">ja</span><span class="sxs-lookup"><span data-stu-id="aceea-131">yes</span></span>       |
| [<span data-ttu-id="aceea-132">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aceea-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="aceea-133">nein</span><span class="sxs-lookup"><span data-stu-id="aceea-133">no</span></span>        |
| [<span data-ttu-id="aceea-134">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aceea-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="aceea-135">nein</span><span class="sxs-lookup"><span data-stu-id="aceea-135">no</span></span>        |
| [<span data-ttu-id="aceea-136">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aceea-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="aceea-137">nein</span><span class="sxs-lookup"><span data-stu-id="aceea-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="aceea-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aceea-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aceea-139">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aceea-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





