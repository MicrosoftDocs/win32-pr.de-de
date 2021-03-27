---
title: ret (SM4-ASM)
description: Return-Anweisung.
ms.assetid: 1B690036-99C5-441D-9DD3-E09D43E48AFF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d834cd9f32d6e38f40666ab235f705c0fc80513f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719380"
---
# <a name="ret-sm4---asm"></a><span data-ttu-id="fe767-103">ret (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="fe767-103">ret (sm4 - asm)</span></span>

<span data-ttu-id="fe767-104">Return-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="fe767-104">Return statement.</span></span>



| <span data-ttu-id="fe767-105">TZI</span><span class="sxs-lookup"><span data-stu-id="fe767-105">ret</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="fe767-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe767-106">Remarks</span></span>

<span data-ttu-id="fe767-107">Wenn Sie in einer Unterroutine sind, kehren Sie nach dem-Befehl zur Anweisung zurück.</span><span class="sxs-lookup"><span data-stu-id="fe767-107">If within a subroutine, return to the instruction after the call.</span></span> <span data-ttu-id="fe767-108">Wenn nicht innerhalb einer Unterroutine, beenden Sie die Ausführung des Programms.</span><span class="sxs-lookup"><span data-stu-id="fe767-108">If not inside a subroutine, terminate program execution.</span></span>

<span data-ttu-id="fe767-109">Das folgende Beispiel zeigt die Verwendung dieser Anweisung.</span><span class="sxs-lookup"><span data-stu-id="fe767-109">The following example shows how to use this instruction.</span></span>

``` syntax
 
               ...
                call l3
                ...
                ret
                label l3
                    ...
                ret
```

### <a name="restrictions"></a><span data-ttu-id="fe767-110">Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="fe767-110">Restrictions</span></span>

-   <span data-ttu-id="fe767-111">**ret** kann beliebig oft in einem Programm vorkommen.</span><span class="sxs-lookup"><span data-stu-id="fe767-111">**ret** can appear anywhere in a program, any number of times.</span></span>
-   <span data-ttu-id="fe767-112">Wenn eine [Bezeichnungs Anweisung in](label--sm4---asm-.md) einem Shader vorkommt, muss Ihr ein **ret** -Befehl vorangestellt sein, der in keiner der Fluss Steuerungs Anweisungen enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="fe767-112">If a [label](label--sm4---asm-.md) instruction appears in a Shader, it must be preceded by a **ret** command that is not nested in any flow control statements.</span></span>
-   <span data-ttu-id="fe767-113">Wenn sich Unterroutinen in einem Shader befinden, muss die letzte Anweisung im Shader ein **ret** sein.</span><span class="sxs-lookup"><span data-stu-id="fe767-113">If there are subroutines in a Shader, the last instruction in the Shader must be a **ret**.</span></span>

<span data-ttu-id="fe767-114">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="fe767-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="fe767-115">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="fe767-115">Vertex Shader</span></span> | <span data-ttu-id="fe767-116">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="fe767-116">Geometry Shader</span></span> | <span data-ttu-id="fe767-117">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="fe767-117">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="fe767-118">x</span><span class="sxs-lookup"><span data-stu-id="fe767-118">x</span></span>             | <span data-ttu-id="fe767-119">x</span><span class="sxs-lookup"><span data-stu-id="fe767-119">x</span></span>               | <span data-ttu-id="fe767-120">x</span><span class="sxs-lookup"><span data-stu-id="fe767-120">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fe767-121">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="fe767-121">Minimum Shader Model</span></span>

<span data-ttu-id="fe767-122">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fe767-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fe767-123">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="fe767-123">Shader Model</span></span>                                              | <span data-ttu-id="fe767-124">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="fe767-124">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fe767-125">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="fe767-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fe767-126">ja</span><span class="sxs-lookup"><span data-stu-id="fe767-126">yes</span></span>       |
| [<span data-ttu-id="fe767-127">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="fe767-127">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fe767-128">ja</span><span class="sxs-lookup"><span data-stu-id="fe767-128">yes</span></span>       |
| [<span data-ttu-id="fe767-129">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="fe767-129">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fe767-130">ja</span><span class="sxs-lookup"><span data-stu-id="fe767-130">yes</span></span>       |
| [<span data-ttu-id="fe767-131">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fe767-131">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fe767-132">nein</span><span class="sxs-lookup"><span data-stu-id="fe767-132">no</span></span>        |
| [<span data-ttu-id="fe767-133">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fe767-133">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fe767-134">nein</span><span class="sxs-lookup"><span data-stu-id="fe767-134">no</span></span>        |
| [<span data-ttu-id="fe767-135">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fe767-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fe767-136">nein</span><span class="sxs-lookup"><span data-stu-id="fe767-136">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fe767-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fe767-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe767-138">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fe767-138">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




