---
title: RETC (SM4-ASM)
description: Bedingter Rückgabe.
ms.assetid: D936099D-4A75-4AE2-9FE3-70ED213DF4D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e394bc6b947d91fafb09dbfdc075b0c60be2cf8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976441"
---
# <a name="retc-sm4---asm"></a><span data-ttu-id="24c6e-103">RETC (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="24c6e-103">retc (sm4 - asm)</span></span>

<span data-ttu-id="24c6e-104">Bedingter Rückgabe.</span><span class="sxs-lookup"><span data-stu-id="24c6e-104">Conditional return.</span></span>



| <span data-ttu-id="24c6e-105">RETC { \_ z </span><span class="sxs-lookup"><span data-stu-id="24c6e-105">retc{\_z</span></span>\|<span data-ttu-id="24c6e-106">\_NZ} src0. Select- \_ Komponente</span><span class="sxs-lookup"><span data-stu-id="24c6e-106">\_nz} src0.select\_component</span></span> |
|----------------------------------------|



 



| <span data-ttu-id="24c6e-107">Element</span><span class="sxs-lookup"><span data-stu-id="24c6e-107">Item</span></span>                                                            | <span data-ttu-id="24c6e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="24c6e-108">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="24c6e-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="24c6e-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="24c6e-110">\[im \] Register, um die Bedingung zu testen.</span><span class="sxs-lookup"><span data-stu-id="24c6e-110">\[in\] The register to test the condition against.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="24c6e-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24c6e-111">Remarks</span></span>

<span data-ttu-id="24c6e-112">Wenn in einer Unterroutine, wird diese Anweisung bedingt an die Anweisung nach dem-Befehl zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="24c6e-112">If within a subroutine, this instruction conditionally returns to the instruction after the call.</span></span> <span data-ttu-id="24c6e-113">Wenn Sie sich nicht innerhalb einer Unterroutine befinden, beendet diese Anweisung die Programmausführung.</span><span class="sxs-lookup"><span data-stu-id="24c6e-113">If not inside a subroutine, this instruction terminates program execution.</span></span>

<span data-ttu-id="24c6e-114">Das folgende Beispiel zeigt die Verwendung dieser Anweisung.</span><span class="sxs-lookup"><span data-stu-id="24c6e-114">The following example shows how to use this instruction.</span></span>

``` syntax
           ...
           call l3
           ...
           ret
           label l3
               ...
               retc_nz r0.x  // If any bit in r0.x is nonzero, then return
               retc_z  r1.x  // If all bits in r0.x are zero, then return.
               ...
           ret
```

### <a name="restrictions"></a><span data-ttu-id="24c6e-115">Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="24c6e-115">Restrictions</span></span>

-   <span data-ttu-id="24c6e-116">**RETC** kann beliebig oft in einem Programm vorkommen.</span><span class="sxs-lookup"><span data-stu-id="24c6e-116">**retc** can appear anywhere in a program, any number of times.</span></span>
-   <span data-ttu-id="24c6e-117">Die letzte Anweisung in einem Hauptprogramm oder einer Unterroutine darf keine **RETC- \_ z** -oder **RETC- \_ NZ** sein.</span><span class="sxs-lookup"><span data-stu-id="24c6e-117">The last instruction in a main program or subroutine cannot be a **retc\_z** or **retc\_nz**.</span></span> <span data-ttu-id="24c6e-118">Stattdessen kann der bedingungslose [ret](ret--sm4---asm-.md) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="24c6e-118">Instead, the unconditional [ret](ret--sm4---asm-.md) can be used.</span></span>
-   <span data-ttu-id="24c6e-119">Das 32-Bit-Register, das von *src0* bereitgestellt wird, wird auf einer Bitebene getestet.</span><span class="sxs-lookup"><span data-stu-id="24c6e-119">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="24c6e-120">Wenn ein Bit ungleich 0 (null) ist, gibt **ret \_ NZ** zurück.</span><span class="sxs-lookup"><span data-stu-id="24c6e-120">If any bit is nonzero, **ret\_nz** will return.</span></span> <span data-ttu-id="24c6e-121">Wenn alle Bits NULL sind, wird von **RETC \_ z** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="24c6e-121">If all bits are zero, **retc\_z** will return.</span></span>

<span data-ttu-id="24c6e-122">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="24c6e-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="24c6e-123">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="24c6e-123">Vertex Shader</span></span> | <span data-ttu-id="24c6e-124">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="24c6e-124">Geometry Shader</span></span> | <span data-ttu-id="24c6e-125">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="24c6e-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="24c6e-126">x</span><span class="sxs-lookup"><span data-stu-id="24c6e-126">x</span></span>             | <span data-ttu-id="24c6e-127">x</span><span class="sxs-lookup"><span data-stu-id="24c6e-127">x</span></span>               | <span data-ttu-id="24c6e-128">x</span><span class="sxs-lookup"><span data-stu-id="24c6e-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="24c6e-129">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="24c6e-129">Minimum Shader Model</span></span>

<span data-ttu-id="24c6e-130">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="24c6e-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="24c6e-131">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="24c6e-131">Shader Model</span></span>                                              | <span data-ttu-id="24c6e-132">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="24c6e-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="24c6e-133">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="24c6e-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="24c6e-134">ja</span><span class="sxs-lookup"><span data-stu-id="24c6e-134">yes</span></span>       |
| [<span data-ttu-id="24c6e-135">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="24c6e-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="24c6e-136">ja</span><span class="sxs-lookup"><span data-stu-id="24c6e-136">yes</span></span>       |
| [<span data-ttu-id="24c6e-137">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="24c6e-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="24c6e-138">ja</span><span class="sxs-lookup"><span data-stu-id="24c6e-138">yes</span></span>       |
| [<span data-ttu-id="24c6e-139">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="24c6e-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="24c6e-140">nein</span><span class="sxs-lookup"><span data-stu-id="24c6e-140">no</span></span>        |
| [<span data-ttu-id="24c6e-141">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="24c6e-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="24c6e-142">nein</span><span class="sxs-lookup"><span data-stu-id="24c6e-142">no</span></span>        |
| [<span data-ttu-id="24c6e-143">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="24c6e-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="24c6e-144">nein</span><span class="sxs-lookup"><span data-stu-id="24c6e-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="24c6e-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="24c6e-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24c6e-146">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="24c6e-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





