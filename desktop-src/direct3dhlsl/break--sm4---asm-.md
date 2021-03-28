---
title: Break (SM4-ASM)
description: Verschiebt den Ausführungs Punkt in die Anweisung nach der nächsten endschleife oder Endswitch.
ms.assetid: 411FB361-FBD1-4180-8D81-2074BA8972B7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06396d062e9126091052126737e3e05c58dbdb16
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313662"
---
# <a name="break-sm4---asm"></a><span data-ttu-id="624c9-103">Break (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="624c9-103">break (sm4 - asm)</span></span>

<span data-ttu-id="624c9-104">Verschiebt den Ausführungs Punkt in die Anweisung nach der nächsten [endschleife](endloop--sm4---asm-.md) oder [Endswitch](endswitch--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="624c9-104">Moves the point of execution to the instruction after the next [endloop](endloop--sm4---asm-.md) or [endswitch](endswitch--sm4---asm-.md).</span></span>



| <span data-ttu-id="624c9-105">break</span><span class="sxs-lookup"><span data-stu-id="624c9-105">break</span></span> |
|-------|



 

## <a name="remarks"></a><span data-ttu-id="624c9-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="624c9-106">Remarks</span></span>

<span data-ttu-id="624c9-107">Das tokenformat enthält den Offset der entsprechenden **ENDLOOP** -oder **Endswitch** -Anweisung im Shader.</span><span class="sxs-lookup"><span data-stu-id="624c9-107">The token format contains the offset of the corresponding **endloop** or **endswitch** instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="624c9-108">Im folgenden Beispiel wird die **break** -Anweisung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="624c9-108">The following example shows the **break** instruction.</span></span>


```
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```



<span data-ttu-id="624c9-109">Diese Anweisung muss innerhalb einer **Schleifen** / **endschleife** oder in einem **Fall** in einem **Switch**- / **Endswitch** vorkommen.</span><span class="sxs-lookup"><span data-stu-id="624c9-109">This instruction must appear within a **loop**/**endloop** or in a **case** in a **switch**/**endswitch**.</span></span>

<span data-ttu-id="624c9-110">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="624c9-110">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="624c9-111">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="624c9-111">Vertex Shader</span></span> | <span data-ttu-id="624c9-112">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="624c9-112">Geometry Shader</span></span> | <span data-ttu-id="624c9-113">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="624c9-113">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="624c9-114">x</span><span class="sxs-lookup"><span data-stu-id="624c9-114">x</span></span>             | <span data-ttu-id="624c9-115">x</span><span class="sxs-lookup"><span data-stu-id="624c9-115">x</span></span>               | <span data-ttu-id="624c9-116">x</span><span class="sxs-lookup"><span data-stu-id="624c9-116">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="624c9-117">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="624c9-117">Minimum Shader Model</span></span>

<span data-ttu-id="624c9-118">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="624c9-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="624c9-119">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="624c9-119">Shader Model</span></span>                                              | <span data-ttu-id="624c9-120">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="624c9-120">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="624c9-121">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="624c9-121">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="624c9-122">ja</span><span class="sxs-lookup"><span data-stu-id="624c9-122">yes</span></span>       |
| [<span data-ttu-id="624c9-123">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="624c9-123">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="624c9-124">ja</span><span class="sxs-lookup"><span data-stu-id="624c9-124">yes</span></span>       |
| [<span data-ttu-id="624c9-125">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="624c9-125">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="624c9-126">ja</span><span class="sxs-lookup"><span data-stu-id="624c9-126">yes</span></span>       |
| [<span data-ttu-id="624c9-127">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="624c9-127">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="624c9-128">nein</span><span class="sxs-lookup"><span data-stu-id="624c9-128">no</span></span>        |
| [<span data-ttu-id="624c9-129">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="624c9-129">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="624c9-130">nein</span><span class="sxs-lookup"><span data-stu-id="624c9-130">no</span></span>        |
| [<span data-ttu-id="624c9-131">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="624c9-131">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="624c9-132">nein</span><span class="sxs-lookup"><span data-stu-id="624c9-132">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="624c9-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="624c9-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="624c9-134">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="624c9-134">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




