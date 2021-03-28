---
title: if (SM4-ASM)
description: Verzweigung auf der Grundlage des logischen OR-Ergebnisses.
ms.assetid: 9F4CF9E0-4D9D-4300-B432-432C560F34BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 653c84be0d30a036bf93d852268e44bcca08bbcb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104992966"
---
# <a name="if-sm4---asm"></a><span data-ttu-id="d87dd-103">if (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d87dd-103">if (sm4 - asm)</span></span>

<span data-ttu-id="d87dd-104">Verzweigung auf der Grundlage des logischen OR-Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="d87dd-104">Branch based on logical OR result.</span></span>



| <span data-ttu-id="d87dd-105">Wenn { \_ z </span><span class="sxs-lookup"><span data-stu-id="d87dd-105">if{\_z</span></span>\|<span data-ttu-id="d87dd-106">\_NZ} src0. Select- \_ Komponente</span><span class="sxs-lookup"><span data-stu-id="d87dd-106">\_nz} src0.select\_component</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="d87dd-107">Element</span><span class="sxs-lookup"><span data-stu-id="d87dd-107">Item</span></span>                                                            | <span data-ttu-id="d87dd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d87dd-108">Description</span></span>                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="d87dd-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d87dd-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d87dd-110">\[\]enthält die Komponente, auf der die Bedingung getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d87dd-110">\[in\] Contains the component on which to test the condition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d87dd-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d87dd-111">Remarks</span></span>

<span data-ttu-id="d87dd-112">Das tokenformat enthält den Offset der entsprechenden endif-Anweisung im Shader.</span><span class="sxs-lookup"><span data-stu-id="d87dd-112">The token format contains the offset of the corresponding endif instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="d87dd-113">Das folgende Beispiel zeigt die Verwendung dieser Anweisung.</span><span class="sxs-lookup"><span data-stu-id="d87dd-113">The following example shows how to use this instruction.</span></span>

``` syntax
                if_z r0.x // if all bits in r0.x are zero
                   ...
                else // (optional)
                   ...
                endif
                if_nz r1.x // if any bit in r0.x is nonzero
                   ...
                else // (optional)
                   ...
                endif
```

### <a name="restrictions"></a><span data-ttu-id="d87dd-114">Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="d87dd-114">Restrictions</span></span>

-   <span data-ttu-id="d87dd-115">Die Quell Operanden (bei 4 Komponenten Vektoren) müssen eine einzelne Komponentenauswahl verwenden.</span><span class="sxs-lookup"><span data-stu-id="d87dd-115">The source operands (if 4 component vectors) must use a single component selector.</span></span>
-   <span data-ttu-id="d87dd-116">Das 32-Bit-Register, das von *src0* bereitgestellt wird, wird auf einer Bitebene getestet.</span><span class="sxs-lookup"><span data-stu-id="d87dd-116">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="d87dd-117">Wenn ein Bit ungleich 0 (null) ist, **Wenn \_ z** true ist.</span><span class="sxs-lookup"><span data-stu-id="d87dd-117">If any bit is nonzero, **if\_z** will be true.</span></span> <span data-ttu-id="d87dd-118">, Wenn alle Bits 0 (null) sind,, **Wenn \_ NZ** true ist.</span><span class="sxs-lookup"><span data-stu-id="d87dd-118">If all bits are zero, **if\_nz** will be true.</span></span>
-   <span data-ttu-id="d87dd-119">Fluss Kontroll Blöcke können bis zu 64 tief pro Unterroutine (und Main) verschachteln.</span><span class="sxs-lookup"><span data-stu-id="d87dd-119">Flow control blocks can nest up to 64 deep per subroutine (and main).</span></span> <span data-ttu-id="d87dd-120">Der HLSL-Compiler generiert keine Unterroutinen, die diesen Grenzwert überschreiten.</span><span class="sxs-lookup"><span data-stu-id="d87dd-120">The HLSL compiler will not generate subroutines that exceed this limit.</span></span> <span data-ttu-id="d87dd-121">Das Verhalten von Ablauf Steuerungs Anweisungen über 64 Ebenen tief (pro Unterroutine) ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="d87dd-121">Behavior of control flow instructions beyond 64 levels deep (per subroutine) is undefined.</span></span>

<span data-ttu-id="d87dd-122">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="d87dd-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d87dd-123">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="d87dd-123">Vertex Shader</span></span> | <span data-ttu-id="d87dd-124">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="d87dd-124">Geometry Shader</span></span> | <span data-ttu-id="d87dd-125">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="d87dd-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d87dd-126">x</span><span class="sxs-lookup"><span data-stu-id="d87dd-126">x</span></span>             | <span data-ttu-id="d87dd-127">x</span><span class="sxs-lookup"><span data-stu-id="d87dd-127">x</span></span>               | <span data-ttu-id="d87dd-128">x</span><span class="sxs-lookup"><span data-stu-id="d87dd-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d87dd-129">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="d87dd-129">Minimum Shader Model</span></span>

<span data-ttu-id="d87dd-130">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d87dd-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d87dd-131">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="d87dd-131">Shader Model</span></span>                                              | <span data-ttu-id="d87dd-132">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="d87dd-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d87dd-133">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="d87dd-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d87dd-134">ja</span><span class="sxs-lookup"><span data-stu-id="d87dd-134">yes</span></span>       |
| [<span data-ttu-id="d87dd-135">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="d87dd-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d87dd-136">ja</span><span class="sxs-lookup"><span data-stu-id="d87dd-136">yes</span></span>       |
| [<span data-ttu-id="d87dd-137">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="d87dd-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d87dd-138">ja</span><span class="sxs-lookup"><span data-stu-id="d87dd-138">yes</span></span>       |
| [<span data-ttu-id="d87dd-139">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d87dd-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d87dd-140">nein</span><span class="sxs-lookup"><span data-stu-id="d87dd-140">no</span></span>        |
| [<span data-ttu-id="d87dd-141">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d87dd-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d87dd-142">nein</span><span class="sxs-lookup"><span data-stu-id="d87dd-142">no</span></span>        |
| [<span data-ttu-id="d87dd-143">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d87dd-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d87dd-144">nein</span><span class="sxs-lookup"><span data-stu-id="d87dd-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d87dd-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d87dd-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d87dd-146">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d87dd-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





