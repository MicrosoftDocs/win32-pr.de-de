---
title: verwerfen (SM4-ASM)
description: Markieren Sie die Ergebnisse des Pixel-Shaders bedingt, damit Sie verworfen werden, wenn das Ende des Programms erreicht ist.
ms.assetid: 566C4A9A-B32A-4AA6-A888-70F6965B1B5A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d98365ae6d80710f15cf7204f98d810be30a13
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103948315"
---
# <a name="discard-sm4---asm"></a><span data-ttu-id="1c716-103">verwerfen (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="1c716-103">discard (sm4 - asm)</span></span>

<span data-ttu-id="1c716-104">Markieren Sie die Ergebnisse des Pixel-Shaders bedingt, damit Sie verworfen werden, wenn das Ende des Programms erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="1c716-104">Conditionally flag results of Pixel Shader to be discarded when the end of the program is reached.</span></span>



| <span data-ttu-id="1c716-105">{ \_ z \ verwerfen</span><span class="sxs-lookup"><span data-stu-id="1c716-105">discard{\_z\</span></span>|<span data-ttu-id="1c716-106">\_NZ} src0. Select- \_ Komponente</span><span class="sxs-lookup"><span data-stu-id="1c716-106">\_nz} src0.select\_component</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="1c716-107">Element</span><span class="sxs-lookup"><span data-stu-id="1c716-107">Item</span></span>                                                            | <span data-ttu-id="1c716-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1c716-108">Description</span></span>                                                                                       |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c716-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1c716-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="1c716-110">\[\]der Wert, der bestimmt, ob das aktuelle Pixel, das verarbeitet wird, verworfen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1c716-110">\[in\] The value that determines whether to discard the current pixel being processed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1c716-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c716-111">Remarks</span></span>

<span data-ttu-id="1c716-112">Diese Anweisung gibt das aktuelle Pixel als beendet an, während die Ausführung fortgesetzt wird, sodass andere gleichzeitig ausgeführte Pixel ggf. Ableitungen erhalten können.</span><span class="sxs-lookup"><span data-stu-id="1c716-112">This instruction flags the current pixel as terminated, while continuing execution, so that other pixels executing in parallel may obtain derivatives if necessary.</span></span> <span data-ttu-id="1c716-113">Obwohl die Ausführung fortgesetzt wird, werden alle Pixel-Shader-Ausgaben geschrieben, bevor oder nachdem die **Verwerfungs** Anweisung verworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="1c716-113">Even though execution continues, all Pixel Shader output writes before or after the **discard** instruction are discarded.</span></span>

<span data-ttu-id="1c716-114">Bei **Verwerfen von \_ z**, wenn alle Bits in *src0. Select \_ Component* gleich 0 (null) sind, wird das Pixel verworfen.</span><span class="sxs-lookup"><span data-stu-id="1c716-114">For **discard\_z**, if all bits in *src0.select\_component* are zero, then the pixel is discarded.</span></span>

<span data-ttu-id="1c716-115">Bei **Verwerfen von \_ NZ** wird das Pixel verworfen, wenn Bits in *src0. Select- \_ Komponente* ungleich NULL sind.</span><span class="sxs-lookup"><span data-stu-id="1c716-115">For **discard\_nz**, if any bits in *src0.select\_component* are nonzero, then the pixel is discarded.</span></span>

<span data-ttu-id="1c716-116">Außerdem kann die **Verwerfungs** Anweisung in jedem Fluss Steuerungs Konstrukt vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="1c716-116">In addition, the **discard** instruction can be present inside any flow control construct.</span></span>

<span data-ttu-id="1c716-117">In einem Shader sind möglicherweise mehrere **Verwerfungs** Anweisungen vorhanden, und wenn eine ausgeführt wird, wird das Pixel beendet.</span><span class="sxs-lookup"><span data-stu-id="1c716-117">Multiple **discard** instructions may be present in a Shader, and if any is executed, the pixel is terminated.</span></span>

<span data-ttu-id="1c716-118">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="1c716-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1c716-119">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="1c716-119">Vertex Shader</span></span> | <span data-ttu-id="1c716-120">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="1c716-120">Geometry Shader</span></span> | <span data-ttu-id="1c716-121">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="1c716-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="1c716-122">x</span><span class="sxs-lookup"><span data-stu-id="1c716-122">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1c716-123">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="1c716-123">Minimum Shader Model</span></span>

<span data-ttu-id="1c716-124">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1c716-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1c716-125">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="1c716-125">Shader Model</span></span>                                              | <span data-ttu-id="1c716-126">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="1c716-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1c716-127">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="1c716-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1c716-128">ja</span><span class="sxs-lookup"><span data-stu-id="1c716-128">yes</span></span>       |
| [<span data-ttu-id="1c716-129">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="1c716-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1c716-130">ja</span><span class="sxs-lookup"><span data-stu-id="1c716-130">yes</span></span>       |
| [<span data-ttu-id="1c716-131">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="1c716-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1c716-132">ja</span><span class="sxs-lookup"><span data-stu-id="1c716-132">yes</span></span>       |
| [<span data-ttu-id="1c716-133">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c716-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1c716-134">nein</span><span class="sxs-lookup"><span data-stu-id="1c716-134">no</span></span>        |
| [<span data-ttu-id="1c716-135">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c716-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1c716-136">nein</span><span class="sxs-lookup"><span data-stu-id="1c716-136">no</span></span>        |
| [<span data-ttu-id="1c716-137">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c716-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1c716-138">nein</span><span class="sxs-lookup"><span data-stu-id="1c716-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1c716-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1c716-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c716-140">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c716-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





