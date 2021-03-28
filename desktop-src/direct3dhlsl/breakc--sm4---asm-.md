---
title: breakc (SM4-ASM)
description: Verschiebt den Ausführungs Punkt bedingt an die Anweisung nach der nächsten endschleife oder Endswitch.
ms.assetid: 5735EF88-1E8C-4142-8442-9328D78999A7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a1c859f7d1e0ee6368f5b9984775ef9bfaba1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389550"
---
# <a name="breakc-sm4---asm"></a><span data-ttu-id="c6845-103">breakc (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c6845-103">breakc (sm4 - asm)</span></span>

<span data-ttu-id="c6845-104">Verschiebt den Ausführungs Punkt bedingt an die Anweisung nach der nächsten [endschleife](endloop--sm4---asm-.md) oder [Endswitch](endswitch--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="c6845-104">Conditionally moves the point of execution to the instruction after the next [endloop](endloop--sm4---asm-.md) or [endswitch](endswitch--sm4---asm-.md).</span></span>



| <span data-ttu-id="c6845-105">breakc { \_ z </span><span class="sxs-lookup"><span data-stu-id="c6845-105">breakc{\_z</span></span>\|<span data-ttu-id="c6845-106">\_NZ} src0. Select- \_ Komponente</span><span class="sxs-lookup"><span data-stu-id="c6845-106">\_nz} src0.select\_component</span></span> |
|------------------------------------------|



 



| <span data-ttu-id="c6845-107">Element</span><span class="sxs-lookup"><span data-stu-id="c6845-107">Item</span></span>                                                            | <span data-ttu-id="c6845-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6845-108">Description</span></span>                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="c6845-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c6845-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c6845-110">\[in \] der Komponente, für die die Bedingung getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6845-110">\[in\] The component on which to test the condition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c6845-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6845-111">Remarks</span></span>

<span data-ttu-id="c6845-112">Das tokenformat enthält den Offset der entsprechenden **ENDLOOP** -Anweisung im Shader.</span><span class="sxs-lookup"><span data-stu-id="c6845-112">The token format contains the offset of the corresponding **endloop** instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="c6845-113">Im folgenden Beispiel wird die **breakc** -Anweisung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="c6845-113">The following example shows the **breakc** instruction.</span></span>


```
                loop
                    // example of termination condition
                    breakc_z  r0.x // break if all bits in r0.x are 0
                    breakc_nz r1.x // break if any bit in r1.x is nonzero
                    ...
                endloop

```



<span data-ttu-id="c6845-114">Diese Anweisung muss in einer **Schleifen** / **endschleife** oder **Switch**- / **Endswitch** vorkommen.</span><span class="sxs-lookup"><span data-stu-id="c6845-114">This instruction must appear within a **loop**/**endloop** or **switch**/**endswitch**.</span></span>

<span data-ttu-id="c6845-115">Das 32-Bit-Register, das von *src0* bereitgestellt wird, wird auf einer Bitebene getestet.</span><span class="sxs-lookup"><span data-stu-id="c6845-115">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="c6845-116">Wenn ein Bit ungleich 0 (null) ist, führt **breakc \_ NZ** die Unterbrechung aus.</span><span class="sxs-lookup"><span data-stu-id="c6845-116">If any bit is nonzero, **breakc\_nz** will perform the break.</span></span> <span data-ttu-id="c6845-117">Wenn alle Bits NULL sind, führt **breakc \_ z** die Unterbrechung aus.</span><span class="sxs-lookup"><span data-stu-id="c6845-117">If all bits are zero, **breakc\_z** will perform the break.</span></span>

<span data-ttu-id="c6845-118">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="c6845-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c6845-119">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="c6845-119">Vertex Shader</span></span> | <span data-ttu-id="c6845-120">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="c6845-120">Geometry Shader</span></span> | <span data-ttu-id="c6845-121">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="c6845-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c6845-122">x</span><span class="sxs-lookup"><span data-stu-id="c6845-122">x</span></span>             | <span data-ttu-id="c6845-123">x</span><span class="sxs-lookup"><span data-stu-id="c6845-123">x</span></span>               | <span data-ttu-id="c6845-124">x</span><span class="sxs-lookup"><span data-stu-id="c6845-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c6845-125">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="c6845-125">Minimum Shader Model</span></span>

<span data-ttu-id="c6845-126">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c6845-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c6845-127">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="c6845-127">Shader Model</span></span>                                              | <span data-ttu-id="c6845-128">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="c6845-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c6845-129">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="c6845-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c6845-130">ja</span><span class="sxs-lookup"><span data-stu-id="c6845-130">yes</span></span>       |
| [<span data-ttu-id="c6845-131">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="c6845-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c6845-132">ja</span><span class="sxs-lookup"><span data-stu-id="c6845-132">yes</span></span>       |
| [<span data-ttu-id="c6845-133">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="c6845-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c6845-134">ja</span><span class="sxs-lookup"><span data-stu-id="c6845-134">yes</span></span>       |
| [<span data-ttu-id="c6845-135">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c6845-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c6845-136">nein</span><span class="sxs-lookup"><span data-stu-id="c6845-136">no</span></span>        |
| [<span data-ttu-id="c6845-137">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c6845-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c6845-138">nein</span><span class="sxs-lookup"><span data-stu-id="c6845-138">no</span></span>        |
| [<span data-ttu-id="c6845-139">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c6845-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c6845-140">nein</span><span class="sxs-lookup"><span data-stu-id="c6845-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c6845-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c6845-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6845-142">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c6845-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





