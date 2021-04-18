---
title: Else (SM4-ASM)
description: Startet einen Else-Block.
ms.assetid: CFF25E78-D986-4EC5-B542-B3396EFF88E1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e283a2621c916ac254daab9f055be0ffe1ba67d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976457"
---
# <a name="else-sm4---asm"></a><span data-ttu-id="2319a-103">Else (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="2319a-103">else (sm4 - asm)</span></span>

<span data-ttu-id="2319a-104">Startet einen **else** -Block.</span><span class="sxs-lookup"><span data-stu-id="2319a-104">Starts an **else** block.</span></span>



| <span data-ttu-id="2319a-105">else</span><span class="sxs-lookup"><span data-stu-id="2319a-105">else</span></span> |
|------|



 

## <a name="remarks"></a><span data-ttu-id="2319a-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2319a-106">Remarks</span></span>

<span data-ttu-id="2319a-107">Das tokenformat enthält den Offset der entsprechenden [EndIf](endif--sm4---asm-.md) -Anweisung im Shader.</span><span class="sxs-lookup"><span data-stu-id="2319a-107">The token format contains the offset of the corresponding [endif](endif--sm4---asm-.md) instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="2319a-108">Im folgenden Beispiel wird die Verwendung der **else** -Anweisung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="2319a-108">The following example shows how to use the **else** instruction.</span></span>

``` syntax
                if     // any of the various forms of if* statements
                   ...
                else   // (optional)
                   ...
                endif
```

<span data-ttu-id="2319a-109">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="2319a-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2319a-110">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="2319a-110">Vertex Shader</span></span> | <span data-ttu-id="2319a-111">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="2319a-111">Geometry Shader</span></span> | <span data-ttu-id="2319a-112">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="2319a-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2319a-113">x</span><span class="sxs-lookup"><span data-stu-id="2319a-113">x</span></span>             | <span data-ttu-id="2319a-114">x</span><span class="sxs-lookup"><span data-stu-id="2319a-114">x</span></span>               | <span data-ttu-id="2319a-115">x</span><span class="sxs-lookup"><span data-stu-id="2319a-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2319a-116">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="2319a-116">Minimum Shader Model</span></span>

<span data-ttu-id="2319a-117">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2319a-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2319a-118">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="2319a-118">Shader Model</span></span>                                              | <span data-ttu-id="2319a-119">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="2319a-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2319a-120">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="2319a-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2319a-121">ja</span><span class="sxs-lookup"><span data-stu-id="2319a-121">yes</span></span>       |
| [<span data-ttu-id="2319a-122">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="2319a-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2319a-123">ja</span><span class="sxs-lookup"><span data-stu-id="2319a-123">yes</span></span>       |
| [<span data-ttu-id="2319a-124">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="2319a-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2319a-125">ja</span><span class="sxs-lookup"><span data-stu-id="2319a-125">yes</span></span>       |
| [<span data-ttu-id="2319a-126">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2319a-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2319a-127">nein</span><span class="sxs-lookup"><span data-stu-id="2319a-127">no</span></span>        |
| [<span data-ttu-id="2319a-128">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2319a-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2319a-129">nein</span><span class="sxs-lookup"><span data-stu-id="2319a-129">no</span></span>        |
| [<span data-ttu-id="2319a-130">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2319a-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2319a-131">nein</span><span class="sxs-lookup"><span data-stu-id="2319a-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2319a-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2319a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2319a-133">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2319a-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




