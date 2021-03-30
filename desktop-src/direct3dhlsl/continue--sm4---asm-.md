---
title: Continue (SM4-ASM)
description: Setzt die Ausführung am Anfang der aktuellen Schleife fort.
ms.assetid: 3F0021B2-50D1-407C-9EE4-1CB679E184BF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc53b023e998fcf131a387fc009cfc8cb133ff6a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993063"
---
# <a name="continue-sm4---asm"></a><span data-ttu-id="b4942-103">Continue (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="b4942-103">continue (sm4 - asm)</span></span>

<span data-ttu-id="b4942-104">Setzt die Ausführung am Anfang der aktuellen Schleife fort.</span><span class="sxs-lookup"><span data-stu-id="b4942-104">Continues execution at the beginning of the current loop.</span></span>



| <span data-ttu-id="b4942-105">continue</span><span class="sxs-lookup"><span data-stu-id="b4942-105">continue</span></span> |
|----------|



 

## <a name="remarks"></a><span data-ttu-id="b4942-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4942-106">Remarks</span></span>

<span data-ttu-id="b4942-107">**Continue** kann nur innerhalb einer [Schleife](loop--sm4---asm-.md) oder einer [endschleife](endloop--sm4---asm-.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4942-107">**continue** can be used only inside a [loop](loop--sm4---asm-.md) or [endloop](endloop--sm4---asm-.md).</span></span>

<span data-ttu-id="b4942-108">Im folgenden Beispiel wird gezeigt, wie die **Continue** -Anweisung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b4942-108">The following example shows how to use the **continue** instruction.</span></span>


```
                loop
                    if_na r0.x
                        break
                    endif
                    if_z r1.x
                        ...
                        continue
                    endif
                    ...
                endloop
```



<span data-ttu-id="b4942-109">Das tokenformat enthält den Offset der entsprechenden Schleifen Anweisung im Shader.</span><span class="sxs-lookup"><span data-stu-id="b4942-109">The token format contains the offset of the corresponding loop instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="b4942-110">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="b4942-110">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b4942-111">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="b4942-111">Vertex Shader</span></span> | <span data-ttu-id="b4942-112">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="b4942-112">Geometry Shader</span></span> | <span data-ttu-id="b4942-113">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="b4942-113">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b4942-114">x</span><span class="sxs-lookup"><span data-stu-id="b4942-114">x</span></span>             | <span data-ttu-id="b4942-115">x</span><span class="sxs-lookup"><span data-stu-id="b4942-115">x</span></span>               | <span data-ttu-id="b4942-116">x</span><span class="sxs-lookup"><span data-stu-id="b4942-116">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b4942-117">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="b4942-117">Minimum Shader Model</span></span>

<span data-ttu-id="b4942-118">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b4942-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b4942-119">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="b4942-119">Shader Model</span></span>                                              | <span data-ttu-id="b4942-120">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="b4942-120">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b4942-121">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="b4942-121">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b4942-122">ja</span><span class="sxs-lookup"><span data-stu-id="b4942-122">yes</span></span>       |
| [<span data-ttu-id="b4942-123">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="b4942-123">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b4942-124">ja</span><span class="sxs-lookup"><span data-stu-id="b4942-124">yes</span></span>       |
| [<span data-ttu-id="b4942-125">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="b4942-125">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b4942-126">ja</span><span class="sxs-lookup"><span data-stu-id="b4942-126">yes</span></span>       |
| [<span data-ttu-id="b4942-127">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b4942-127">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b4942-128">nein</span><span class="sxs-lookup"><span data-stu-id="b4942-128">no</span></span>        |
| [<span data-ttu-id="b4942-129">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b4942-129">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b4942-130">nein</span><span class="sxs-lookup"><span data-stu-id="b4942-130">no</span></span>        |
| [<span data-ttu-id="b4942-131">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b4942-131">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b4942-132">nein</span><span class="sxs-lookup"><span data-stu-id="b4942-132">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b4942-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b4942-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4942-134">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b4942-134">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




