---
title: continuec (SM4-ASM)
description: Führt die Ausführung am Anfang der aktuellen Schleife bedingt aus.
ms.assetid: 1A5B1951-CE1E-479C-AE0F-FC5FB93E0DE9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d480d8828f8f68af1f6a2ff4f52224041d5241df
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976368"
---
# <a name="continuec-sm4---asm"></a><span data-ttu-id="0ffef-103">continuec (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="0ffef-103">continuec (sm4 - asm)</span></span>

<span data-ttu-id="0ffef-104">Führt die Ausführung am Anfang der aktuellen Schleife bedingt aus.</span><span class="sxs-lookup"><span data-stu-id="0ffef-104">Conditionally continues execution at the beginning of the current loop.</span></span>



| <span data-ttu-id="0ffef-105">continuec { \_ z </span><span class="sxs-lookup"><span data-stu-id="0ffef-105">continuec{\_z</span></span>\|<span data-ttu-id="0ffef-106">\_NZ} src0. Select- \_ Komponente</span><span class="sxs-lookup"><span data-stu-id="0ffef-106">\_nz} src0.select\_component</span></span> |
|---------------------------------------------|



 



| <span data-ttu-id="0ffef-107">Begriff</span><span class="sxs-lookup"><span data-stu-id="0ffef-107">Term</span></span>                                                            | <span data-ttu-id="0ffef-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ffef-108">Description</span></span>                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="0ffef-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="0ffef-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="0ffef-110">\[in \] der Komponente, für die die Bedingung getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0ffef-110">\[in\] The component against which to test the condition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0ffef-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ffef-111">Remarks</span></span>

<span data-ttu-id="0ffef-112">**continuec** kann nur innerhalb einer [Schleife](loop--sm4---asm-.md) oder einer [endschleife](endloop--sm4---asm-.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0ffef-112">**continuec** can be used only inside a [loop](loop--sm4---asm-.md) or [endloop](endloop--sm4---asm-.md).</span></span>

<span data-ttu-id="0ffef-113">Im folgenden Beispiel wird gezeigt, wie die **continuec** -Anweisung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0ffef-113">The following example shows how to use the **continuec** instruction.</span></span>


```
                loop
                    if_na r0.x
                        break
                    endif
                    continuec_z r1.x  // if all bits of r1.x are zero then
                                      // continue at beginning of loop.
                    ...
                    continuec_nz r3.y // if any bit in r3.y is set then
                                      // continue at beginning of loop.

                    ...
                endloop

```



<span data-ttu-id="0ffef-114">Das tokenformat enthält den Offset der entsprechenden Schleifen Anweisung im Shader.</span><span class="sxs-lookup"><span data-stu-id="0ffef-114">The token format contains the offset of the corresponding loop instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="0ffef-115">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="0ffef-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0ffef-116">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="0ffef-116">Vertex Shader</span></span> | <span data-ttu-id="0ffef-117">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="0ffef-117">Geometry Shader</span></span> | <span data-ttu-id="0ffef-118">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="0ffef-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="0ffef-119">x</span><span class="sxs-lookup"><span data-stu-id="0ffef-119">x</span></span>             | <span data-ttu-id="0ffef-120">x</span><span class="sxs-lookup"><span data-stu-id="0ffef-120">x</span></span>               | <span data-ttu-id="0ffef-121">x</span><span class="sxs-lookup"><span data-stu-id="0ffef-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0ffef-122">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="0ffef-122">Minimum Shader Model</span></span>

<span data-ttu-id="0ffef-123">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0ffef-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0ffef-124">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="0ffef-124">Shader Model</span></span>                                              | <span data-ttu-id="0ffef-125">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="0ffef-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0ffef-126">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="0ffef-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0ffef-127">ja</span><span class="sxs-lookup"><span data-stu-id="0ffef-127">yes</span></span>       |
| [<span data-ttu-id="0ffef-128">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="0ffef-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0ffef-129">ja</span><span class="sxs-lookup"><span data-stu-id="0ffef-129">yes</span></span>       |
| [<span data-ttu-id="0ffef-130">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="0ffef-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0ffef-131">ja</span><span class="sxs-lookup"><span data-stu-id="0ffef-131">yes</span></span>       |
| [<span data-ttu-id="0ffef-132">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0ffef-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0ffef-133">nein</span><span class="sxs-lookup"><span data-stu-id="0ffef-133">no</span></span>        |
| [<span data-ttu-id="0ffef-134">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0ffef-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0ffef-135">nein</span><span class="sxs-lookup"><span data-stu-id="0ffef-135">no</span></span>        |
| [<span data-ttu-id="0ffef-136">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0ffef-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0ffef-137">nein</span><span class="sxs-lookup"><span data-stu-id="0ffef-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0ffef-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0ffef-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ffef-139">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0ffef-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





