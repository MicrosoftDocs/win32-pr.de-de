---
title: Ausgabe (SM4-ASM)
description: Gibt einen Scheitelpunkt aus.
ms.assetid: FDD18CCD-8088-46BD-897C-434B77FF81E6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b17711b6f9cf5d707fb8eae3465100a78620c0c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719356"
---
# <a name="emit-sm4---asm"></a><span data-ttu-id="e46d0-103">Ausgabe (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="e46d0-103">emit (sm4 - asm)</span></span>

<span data-ttu-id="e46d0-104">Gibt einen Scheitelpunkt aus.</span><span class="sxs-lookup"><span data-stu-id="e46d0-104">Emit a vertex.</span></span>



| <span data-ttu-id="e46d0-105">ausgeben</span><span class="sxs-lookup"><span data-stu-id="e46d0-105">emit</span></span> |
|------|



 

## <a name="remarks"></a><span data-ttu-id="e46d0-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e46d0-106">Remarks</span></span>

<span data-ttu-id="e46d0-107">die **Ausgabe bewirkt,** dass alle deklarierten o- \# Register aus dem Geometry-Shader ausgelesen werden, um einen Scheitelpunkt zu generieren.</span><span class="sxs-lookup"><span data-stu-id="e46d0-107">**emit** causes all declared o\# registers to be read out of the Geometry Shader to generate a vertex.</span></span>

<span data-ttu-id="e46d0-108">Wenn mehrere **Ausgabe** Aufrufe ausgegeben werden, werden primitive generiert.</span><span class="sxs-lookup"><span data-stu-id="e46d0-108">As multiple **emit** calls are issued, primitives are generated.</span></span>

<span data-ttu-id="e46d0-109">die **Ausgabe kann beliebig** oft in einem Geometry-Shader vorkommen, einschließlich innerhalb der Fluss Steuerung.</span><span class="sxs-lookup"><span data-stu-id="e46d0-109">**emit** can appear any number of times in a Geometry Shader, including within flow control.</span></span>

<span data-ttu-id="e46d0-110">Wenn Streams deklariert wurden, müssen Sie den [ \_ Ausgabestream](emit-stream--sm5---asm-.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="e46d0-110">If streams have been declared, you must use [emit\_stream](emit-stream--sm5---asm-.md).</span></span>

<span data-ttu-id="e46d0-111">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="e46d0-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e46d0-112">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="e46d0-112">Vertex Shader</span></span> | <span data-ttu-id="e46d0-113">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="e46d0-113">Geometry Shader</span></span> | <span data-ttu-id="e46d0-114">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="e46d0-114">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="e46d0-115">x</span><span class="sxs-lookup"><span data-stu-id="e46d0-115">x</span></span>               |              |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="e46d0-116">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="e46d0-116">Minimum Shader Model</span></span>

<span data-ttu-id="e46d0-117">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e46d0-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e46d0-118">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="e46d0-118">Shader Model</span></span>                                              | <span data-ttu-id="e46d0-119">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="e46d0-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e46d0-120">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="e46d0-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e46d0-121">ja</span><span class="sxs-lookup"><span data-stu-id="e46d0-121">yes</span></span>       |
| [<span data-ttu-id="e46d0-122">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="e46d0-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e46d0-123">ja</span><span class="sxs-lookup"><span data-stu-id="e46d0-123">yes</span></span>       |
| [<span data-ttu-id="e46d0-124">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="e46d0-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e46d0-125">ja</span><span class="sxs-lookup"><span data-stu-id="e46d0-125">yes</span></span>       |
| [<span data-ttu-id="e46d0-126">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e46d0-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e46d0-127">nein</span><span class="sxs-lookup"><span data-stu-id="e46d0-127">no</span></span>        |
| [<span data-ttu-id="e46d0-128">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e46d0-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e46d0-129">nein</span><span class="sxs-lookup"><span data-stu-id="e46d0-129">no</span></span>        |
| [<span data-ttu-id="e46d0-130">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e46d0-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e46d0-131">nein</span><span class="sxs-lookup"><span data-stu-id="e46d0-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e46d0-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e46d0-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e46d0-133">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e46d0-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




