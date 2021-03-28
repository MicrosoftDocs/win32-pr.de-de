---
title: ENDLOOP (SM4-ASM)
description: Beendet eine Schleifen Anweisung.
ms.assetid: 0BEFADF4-036E-4FDA-9681-10965D6BA9FC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 655fa6addd19a6ce9f6f6b20a2677ef43cb8b751
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389485"
---
# <a name="endloop-sm4---asm"></a><span data-ttu-id="20169-103">ENDLOOP (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="20169-103">endloop (sm4 - asm)</span></span>

<span data-ttu-id="20169-104">Beendet eine Schleifen Anweisung.</span><span class="sxs-lookup"><span data-stu-id="20169-104">Ends a loop statement.</span></span>



| <span data-ttu-id="20169-105">ENDLOOP</span><span class="sxs-lookup"><span data-stu-id="20169-105">endloop</span></span> |
|---------|



 

## <a name="remarks"></a><span data-ttu-id="20169-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20169-106">Remarks</span></span>

<span data-ttu-id="20169-107">Das folgende Beispiel zeigt die Verwendung dieser Anweisung.</span><span class="sxs-lookup"><span data-stu-id="20169-107">The following example shows how to use this instruction.</span></span>

``` syntax
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```

<span data-ttu-id="20169-108">Das tokenformat enthält den Offset der entsprechenden Schleifen Anweisung im Shader.</span><span class="sxs-lookup"><span data-stu-id="20169-108">The token format contains the offset of the corresponding loop instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="20169-109">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="20169-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="20169-110">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="20169-110">Vertex Shader</span></span> | <span data-ttu-id="20169-111">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="20169-111">Geometry Shader</span></span> | <span data-ttu-id="20169-112">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="20169-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="20169-113">x</span><span class="sxs-lookup"><span data-stu-id="20169-113">x</span></span>             | <span data-ttu-id="20169-114">x</span><span class="sxs-lookup"><span data-stu-id="20169-114">x</span></span>               | <span data-ttu-id="20169-115">x</span><span class="sxs-lookup"><span data-stu-id="20169-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="20169-116">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="20169-116">Minimum Shader Model</span></span>

<span data-ttu-id="20169-117">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="20169-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="20169-118">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="20169-118">Shader Model</span></span>                                              | <span data-ttu-id="20169-119">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="20169-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="20169-120">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="20169-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="20169-121">ja</span><span class="sxs-lookup"><span data-stu-id="20169-121">yes</span></span>       |
| [<span data-ttu-id="20169-122">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="20169-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="20169-123">ja</span><span class="sxs-lookup"><span data-stu-id="20169-123">yes</span></span>       |
| [<span data-ttu-id="20169-124">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="20169-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="20169-125">ja</span><span class="sxs-lookup"><span data-stu-id="20169-125">yes</span></span>       |
| [<span data-ttu-id="20169-126">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="20169-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="20169-127">nein</span><span class="sxs-lookup"><span data-stu-id="20169-127">no</span></span>        |
| [<span data-ttu-id="20169-128">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="20169-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="20169-129">nein</span><span class="sxs-lookup"><span data-stu-id="20169-129">no</span></span>        |
| [<span data-ttu-id="20169-130">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="20169-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="20169-131">nein</span><span class="sxs-lookup"><span data-stu-id="20169-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="20169-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="20169-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20169-133">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="20169-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




