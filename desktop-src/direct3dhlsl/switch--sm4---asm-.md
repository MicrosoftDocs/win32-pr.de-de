---
title: Switch (SM4-ASM)
description: Überträgt die Steuerung in Abhängigkeit vom Wert eines Selektor an einen anderen Anweisungsblock innerhalb des Switch-Texts.
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feed346b8aa33feecc13fe2a6ffad59c961b0173
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038336"
---
# <a name="switch-sm4---asm"></a><span data-ttu-id="f9e2b-103">Switch (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="f9e2b-103">switch (sm4 - asm)</span></span>

<span data-ttu-id="f9e2b-104">Überträgt die Steuerung in Abhängigkeit vom Wert eines Selektor an einen anderen Anweisungsblock innerhalb des Switch-Texts.</span><span class="sxs-lookup"><span data-stu-id="f9e2b-104">Transfers control to a different statement block within the switch body depending on the value of a selector.</span></span>



| <span data-ttu-id="f9e2b-105">Switch src0. ausgewählte \_ Komponente</span><span class="sxs-lookup"><span data-stu-id="f9e2b-105">switch src0.selected\_component</span></span> |
|---------------------------------|



 



| <span data-ttu-id="f9e2b-106">Element</span><span class="sxs-lookup"><span data-stu-id="f9e2b-106">Item</span></span>                                                            | <span data-ttu-id="f9e2b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9e2b-107">Description</span></span>                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="f9e2b-108"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f9e2b-108"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="f9e2b-109">\[in \] der Auswahl für die Switch-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="f9e2b-109">\[in\] The selector for the switch statement.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f9e2b-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9e2b-110">Remarks</span></span>

<span data-ttu-id="f9e2b-111">Ein **Switch**- / [endswitchkonstrukt](endswitch--sm4---asm-.md) verhält sich genau  wie ein switchkonstrukt in der Programmiersprache C, mit der folgenden Ausnahme: bei Standard Anweisungen für D3D11 [Case](case--sm4---asm-.md) / [](default--sm4---asm-.md) , die bis zum nächsten **Fall** den Standardwert ohne Unterbrechung durchlaufen, /  kann kein Code enthalten sein. [](break--sm4---asm-.md)</span><span class="sxs-lookup"><span data-stu-id="f9e2b-111">A **switch**/[endswitch](endswitch--sm4---asm-.md) construct behaves exactly as a **switch** construct in the C language, with the following exception: for D3D11 [case](case--sm4---asm-.md)/[default](default--sm4---asm-.md) statements that fall through to the next **case**/**default** without a [break](break--sm4---asm-.md) cannot have any code in them.</span></span> <span data-ttu-id="f9e2b-112">Es ist zulässig, dass mehrere **Case** -Anweisungen (einschließlich **Standard**) sequenziell angezeigt werden und denselben Codeblock gemeinsam nutzen.</span><span class="sxs-lookup"><span data-stu-id="f9e2b-112">It is permitted for multiple **case** statements, including **default**, to appear sequentially, sharing the same code block.</span></span>

<span data-ttu-id="f9e2b-113">Die Bedingung muss eine 32-Bit-Register Komponente oder eine sofortige Menge sein.</span><span class="sxs-lookup"><span data-stu-id="f9e2b-113">The condition must be a 32-bit register component or immediate quantity.</span></span> <span data-ttu-id="f9e2b-114">Der Gleichheits Vergleich ist bitweise (Integer).</span><span class="sxs-lookup"><span data-stu-id="f9e2b-114">The equality comparison is bitwise (integer).</span></span>

<span data-ttu-id="f9e2b-115">Wie bei jeder shaderanweisung in D3D11 kann das **switchkonstrukt von** Hardware nicht direkt implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f9e2b-115">As with any Shader instruction in the D3D11, hardware may or may not implement the **switch** construct directly.</span></span>

<span data-ttu-id="f9e2b-116">**Switch** -Anweisungen können eingebettet werden.</span><span class="sxs-lookup"><span data-stu-id="f9e2b-116">**Switch** statements can be nested.</span></span> <span data-ttu-id="f9e2b-117">Jeder **Switch** -Block zählt als 1 Ebene für die Schachtelungs Schachtelungs Tiefe von 64 pro Unterroutine und Main, unabhängig von der Anzahl der **Case** -Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="f9e2b-117">Each **switch** block counts as 1 level against the flow control nesting depth limit of 64 per subroutine and main, independent of the number of **case** statements.</span></span> <span data-ttu-id="f9e2b-118">Der HLSL-Compiler generiert keine Unterroutinen, die diesen Grenzwert überschreiten.</span><span class="sxs-lookup"><span data-stu-id="f9e2b-118">The HLSL compiler will not generate subroutines that exceed this limit.</span></span> <span data-ttu-id="f9e2b-119">Das Verhalten von Ablauf Steuerungs Anweisungen, die eine Tiefe von 64 Ebenen überschreiten, ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="f9e2b-119">Behavior of control flow instructions beyond 64 levels deep per subroutine is undefined.</span></span>

<span data-ttu-id="f9e2b-120">Das folgende Beispiel zeigt die Verwendung dieser Anweisung.</span><span class="sxs-lookup"><span data-stu-id="f9e2b-120">The following example shows how to use this instruction.</span></span>

``` syntax
                ...
                switch r0.x
                default: // falling through
                case 3
                    switch r1.x
                    case 4
                        ...
                        break
                    case 5
                        ...
                        break
                    endswitch
                    break
                case 0
                    break
                endswitch
```

<span data-ttu-id="f9e2b-121">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="f9e2b-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f9e2b-122">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="f9e2b-122">Vertex Shader</span></span> | <span data-ttu-id="f9e2b-123">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="f9e2b-123">Geometry Shader</span></span> | <span data-ttu-id="f9e2b-124">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="f9e2b-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="f9e2b-125">x</span><span class="sxs-lookup"><span data-stu-id="f9e2b-125">x</span></span>             | <span data-ttu-id="f9e2b-126">x</span><span class="sxs-lookup"><span data-stu-id="f9e2b-126">x</span></span>               | <span data-ttu-id="f9e2b-127">x</span><span class="sxs-lookup"><span data-stu-id="f9e2b-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f9e2b-128">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="f9e2b-128">Minimum Shader Model</span></span>

<span data-ttu-id="f9e2b-129">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f9e2b-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f9e2b-130">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="f9e2b-130">Shader Model</span></span>                                              | <span data-ttu-id="f9e2b-131">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="f9e2b-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f9e2b-132">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="f9e2b-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f9e2b-133">ja</span><span class="sxs-lookup"><span data-stu-id="f9e2b-133">yes</span></span>       |
| [<span data-ttu-id="f9e2b-134">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="f9e2b-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f9e2b-135">ja</span><span class="sxs-lookup"><span data-stu-id="f9e2b-135">yes</span></span>       |
| [<span data-ttu-id="f9e2b-136">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="f9e2b-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f9e2b-137">ja</span><span class="sxs-lookup"><span data-stu-id="f9e2b-137">yes</span></span>       |
| [<span data-ttu-id="f9e2b-138">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f9e2b-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f9e2b-139">nein</span><span class="sxs-lookup"><span data-stu-id="f9e2b-139">no</span></span>        |
| [<span data-ttu-id="f9e2b-140">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f9e2b-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f9e2b-141">nein</span><span class="sxs-lookup"><span data-stu-id="f9e2b-141">no</span></span>        |
| [<span data-ttu-id="f9e2b-142">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f9e2b-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f9e2b-143">nein</span><span class="sxs-lookup"><span data-stu-id="f9e2b-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f9e2b-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9e2b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9e2b-145">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f9e2b-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





