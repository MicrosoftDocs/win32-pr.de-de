---
title: Schleife (SM4-ASM)
description: Gibt eine Schleife an, die bis zu einer Break-Anweisung iteriert.
ms.assetid: 0BEFADF4-036E-4FDA-9681-10965D6BA9FC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 243bdf3b370d3505d787451162c22340acef3a45
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993103"
---
# <a name="loop-sm4---asm"></a><span data-ttu-id="5976a-103">Schleife (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="5976a-103">loop (sm4 - asm)</span></span>

<span data-ttu-id="5976a-104">Gibt eine Schleife an, die bis zu einer Break-Anweisung iteriert.</span><span class="sxs-lookup"><span data-stu-id="5976a-104">Specifies a loop which iterates until a break instruction is encountered.</span></span>



| <span data-ttu-id="5976a-105">loop</span><span class="sxs-lookup"><span data-stu-id="5976a-105">loop</span></span> |
|------|



 

## <a name="remarks"></a><span data-ttu-id="5976a-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5976a-106">Remarks</span></span>

<span data-ttu-id="5976a-107">die **Schleife** kann unbegrenzt durchlaufen werden, obwohl die allgemeine Ausführung des Shaders erzwungen werden kann, nachdem eine Reihe von Anweisungen ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="5976a-107">**loop** can iterate indefinitely, although overall execution of the Shader may be forced to terminate after some number of instructions are executed.</span></span>

<span data-ttu-id="5976a-108">Fluss Kontroll Blöcke können bis zu 64 tief pro Unterroutine und Main verschachteln.</span><span class="sxs-lookup"><span data-stu-id="5976a-108">Flow control blocks can nest up to 64 deep per subroutine and main.</span></span> <span data-ttu-id="5976a-109">Der HLSL-Compiler generiert keine Unterroutinen, die diesen Grenzwert überschreiten.</span><span class="sxs-lookup"><span data-stu-id="5976a-109">The HLSL compiler will not generate subroutines that exceed this limit.</span></span> <span data-ttu-id="5976a-110">Das Verhalten von Ablauf Steuerungs Anweisungen, die eine Tiefe von 64 Ebenen überschreiten, ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="5976a-110">Behavior of control flow instructions beyond 64 levels deep per subroutine is undefined.</span></span>

<span data-ttu-id="5976a-111">Das tokenformat enthält den Offset der entsprechenden [ENDLOOP](endloop--sm4---asm-.md) -Anweisung im Shader.</span><span class="sxs-lookup"><span data-stu-id="5976a-111">The token format contains the offset of the corresponding [endloop](endloop--sm4---asm-.md) instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="5976a-112">Im folgenden Beispiel wird gezeigt, wie die-Schleifen Anweisung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5976a-112">The following example shows how to use the loop instruction.</span></span>

``` syntax
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```

<span data-ttu-id="5976a-113">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="5976a-113">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5976a-114">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="5976a-114">Vertex Shader</span></span> | <span data-ttu-id="5976a-115">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="5976a-115">Geometry Shader</span></span> | <span data-ttu-id="5976a-116">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="5976a-116">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="5976a-117">x</span><span class="sxs-lookup"><span data-stu-id="5976a-117">x</span></span>             | <span data-ttu-id="5976a-118">x</span><span class="sxs-lookup"><span data-stu-id="5976a-118">x</span></span>               | <span data-ttu-id="5976a-119">x</span><span class="sxs-lookup"><span data-stu-id="5976a-119">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5976a-120">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="5976a-120">Minimum Shader Model</span></span>

<span data-ttu-id="5976a-121">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5976a-121">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5976a-122">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="5976a-122">Shader Model</span></span>                                              | <span data-ttu-id="5976a-123">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="5976a-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5976a-124">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="5976a-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5976a-125">ja</span><span class="sxs-lookup"><span data-stu-id="5976a-125">yes</span></span>       |
| [<span data-ttu-id="5976a-126">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="5976a-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5976a-127">ja</span><span class="sxs-lookup"><span data-stu-id="5976a-127">yes</span></span>       |
| [<span data-ttu-id="5976a-128">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="5976a-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5976a-129">ja</span><span class="sxs-lookup"><span data-stu-id="5976a-129">yes</span></span>       |
| [<span data-ttu-id="5976a-130">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5976a-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5976a-131">nein</span><span class="sxs-lookup"><span data-stu-id="5976a-131">no</span></span>        |
| [<span data-ttu-id="5976a-132">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5976a-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5976a-133">nein</span><span class="sxs-lookup"><span data-stu-id="5976a-133">no</span></span>        |
| [<span data-ttu-id="5976a-134">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5976a-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5976a-135">nein</span><span class="sxs-lookup"><span data-stu-id="5976a-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5976a-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5976a-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5976a-137">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5976a-137">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




