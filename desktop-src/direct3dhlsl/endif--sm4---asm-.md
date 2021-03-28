---
title: umdif (SM4-ASM)
description: Beendet eine if-Anweisung.
ms.assetid: 9F4CF9E0-4D9D-4300-B432-432C560F34BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d3fa6cf0efd395843212f6bacac478285e496c2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038304"
---
# <a name="endif-sm4---asm"></a><span data-ttu-id="c37a6-103">umdif (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c37a6-103">endif (sm4 - asm)</span></span>

<span data-ttu-id="c37a6-104">Beendet eine [if](if--sm4---asm-.md) -Anweisung.</span><span class="sxs-lookup"><span data-stu-id="c37a6-104">Ends an [if](if--sm4---asm-.md) statement.</span></span>



| <span data-ttu-id="c37a6-105">endif</span><span class="sxs-lookup"><span data-stu-id="c37a6-105">endif</span></span> |
|-------|



 

## <a name="remarks"></a><span data-ttu-id="c37a6-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c37a6-106">Remarks</span></span>

<span data-ttu-id="c37a6-107">Im folgenden Beispiel wird gezeigt, wie die Anweisung "-Anweisung" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c37a6-107">The following example shows how to use the endif instruction.</span></span>

``` syntax
                if     // any of the various forms of if* statements
                   ...
                else   // (optional)
                   ...
                endif
```

<span data-ttu-id="c37a6-108">Das tokenformat enthält den Offset der entsprechenden **if** -Anweisung im Shader.</span><span class="sxs-lookup"><span data-stu-id="c37a6-108">The token format contains the offset of the corresponding **if** instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="c37a6-109">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="c37a6-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c37a6-110">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="c37a6-110">Vertex Shader</span></span> | <span data-ttu-id="c37a6-111">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="c37a6-111">Geometry Shader</span></span> | <span data-ttu-id="c37a6-112">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="c37a6-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c37a6-113">x</span><span class="sxs-lookup"><span data-stu-id="c37a6-113">x</span></span>             | <span data-ttu-id="c37a6-114">x</span><span class="sxs-lookup"><span data-stu-id="c37a6-114">x</span></span>               | <span data-ttu-id="c37a6-115">x</span><span class="sxs-lookup"><span data-stu-id="c37a6-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c37a6-116">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="c37a6-116">Minimum Shader Model</span></span>

<span data-ttu-id="c37a6-117">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c37a6-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c37a6-118">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="c37a6-118">Shader Model</span></span>                                              | <span data-ttu-id="c37a6-119">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="c37a6-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c37a6-120">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="c37a6-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c37a6-121">ja</span><span class="sxs-lookup"><span data-stu-id="c37a6-121">yes</span></span>       |
| [<span data-ttu-id="c37a6-122">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="c37a6-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c37a6-123">ja</span><span class="sxs-lookup"><span data-stu-id="c37a6-123">yes</span></span>       |
| [<span data-ttu-id="c37a6-124">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="c37a6-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c37a6-125">ja</span><span class="sxs-lookup"><span data-stu-id="c37a6-125">yes</span></span>       |
| [<span data-ttu-id="c37a6-126">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c37a6-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c37a6-127">nein</span><span class="sxs-lookup"><span data-stu-id="c37a6-127">no</span></span>        |
| [<span data-ttu-id="c37a6-128">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c37a6-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c37a6-129">nein</span><span class="sxs-lookup"><span data-stu-id="c37a6-129">no</span></span>        |
| [<span data-ttu-id="c37a6-130">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c37a6-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c37a6-131">nein</span><span class="sxs-lookup"><span data-stu-id="c37a6-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c37a6-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c37a6-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c37a6-133">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c37a6-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




