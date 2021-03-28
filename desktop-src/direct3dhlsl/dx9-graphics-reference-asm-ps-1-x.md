---
title: ps_1_1, ps_1_2 ps_1_3, ps_1_4
description: Der Pixelshader-Assembler besteht aus einer Reihe von Anweisungen, die auf Pixeldaten in Registern angewendet werden.
ms.assetid: 51b59f98-2fa8-4280-bc36-f4328a646168
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 761721a4de64e8a9168bcfea49ce7adf567ea7ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206226"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4"></a><span data-ttu-id="c091f-103">PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="c091f-103">ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4</span></span>

<span data-ttu-id="c091f-104">Der Pixelshader-Assembler besteht aus einer Reihe von Anweisungen, die auf Pixeldaten in Registern angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c091f-104">The pixel shader assembler is made up of a set of instructions that operate on pixel data contained in registers.</span></span> <span data-ttu-id="c091f-105">Vorgänge werden als Anweisungen ausgedrückt, die aus einem Operator und einem oder mehreren Operanden bestehen.</span><span class="sxs-lookup"><span data-stu-id="c091f-105">Operations are expressed as instructions comprised of an operator and one or more operands.</span></span> <span data-ttu-id="c091f-106">In den Anweisungen werden Register zum Übertragen von Daten in den und aus dem Pixelshader Alu verwendet.</span><span class="sxs-lookup"><span data-stu-id="c091f-106">Instructions use registers to transfer data in and out of the pixel shader ALU.</span></span> <span data-ttu-id="c091f-107">Register können auch in einigen Anweisungen verwendet werden, um temporäre Ergebnisse zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c091f-107">Registers can also be used by some instructions to hold temporary results.</span></span>

> [!Note]  
> <span data-ttu-id="c091f-108">Die HLSL-Unterstützung für Pixel Shader 1. x ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="c091f-108">HLSL support for pixel shader 1.x is deprecated.</span></span>

 

## <a name="instructions"></a><span data-ttu-id="c091f-109">Instructions</span><span class="sxs-lookup"><span data-stu-id="c091f-109">Instructions</span></span>

<span data-ttu-id="c091f-110">Es gibt zwei Hauptkategorien von pixelshaderanweisungen: arithmetische Anweisungen und Anweisungen zur Textur Adressierung.</span><span class="sxs-lookup"><span data-stu-id="c091f-110">There are two main categories of pixel shader instructions: arithmetic instructions and texture addressing instructions.</span></span> <span data-ttu-id="c091f-111">Arithmetische Anweisungen ändern von Farbdaten.</span><span class="sxs-lookup"><span data-stu-id="c091f-111">Arithmetic instructions modify color data.</span></span> <span data-ttu-id="c091f-112">Textur Adressierungs Vorgänge verarbeiten Texturkoordinaten Daten und in den meisten Fällen eine Textur.</span><span class="sxs-lookup"><span data-stu-id="c091f-112">Texture addressing operations process texture coordinate data and in most cases, sample a texture.</span></span> <span data-ttu-id="c091f-113">Pixelshaderanweisungen werden pro Pixel ausgeführt. Das heißt, Sie haben keine Kenntnis von anderen Pixeln in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c091f-113">Pixel shader instructions are run on a per-pixel basis; that is, they have no knowledge of other pixels in the pipeline.</span></span>

<span data-ttu-id="c091f-114">Textur Adressierungs Anweisungen verwenden jeweils einen Slot, aber arithmetische Anweisungen können kombiniert werden, um sowohl Farbkomponenten (RGB) als auch eine Alpha Komponenten Anweisung in einem einzelnen Slot zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c091f-114">Texture addressing instructions each consume one slot, but arithmetic instructions can be paired to enable both color components (RGB) and an alpha component instruction in a single slot.</span></span>

<span data-ttu-id="c091f-115">[PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4 Anweisungen](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md) enthalten eine Liste der verfügbaren Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="c091f-115">[ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md) contains a list of the available instructions.</span></span>

<span data-ttu-id="c091f-116">Wenn die multisamplinggrad-Funktion aktiviert ist, werden Pixel-Shader nur einmal pro Pixel und nicht einmal für jedes Subpixel ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c091f-116">When multisampling is enabled, pixel shaders only get run once per pixel, not once for every subpixel.</span></span> <span data-ttu-id="c091f-117">Multisampling erhöht nur die Auflösung von Polygon Rändern sowie tiefen-und Schablonen Tests.</span><span class="sxs-lookup"><span data-stu-id="c091f-117">Multisampling only increases the resolution of polygon edges, as well as depth and stencil tests.</span></span> <span data-ttu-id="c091f-118">Wenn z. b. 3X3-multisamplinggrad aktiviert ist und ein Dreieck, das rasterisiert wird, fünf der neun Subpixel für ein bestimmtes Pixel abdeckt, wird der Pixelshader einmal ausgeführt, und das gleiche Farbergebnis wird auf alle fünf Subpixel angewendet.</span><span class="sxs-lookup"><span data-stu-id="c091f-118">For example, if 3x3 multisampling is enabled, and a triangle being rasterized is found to cover five of the nine subpixels for a particular pixel, the pixel shader gets run once and the same color result is applied to all five subpixels.</span></span>

## <a name="registers"></a><span data-ttu-id="c091f-119">Register</span><span class="sxs-lookup"><span data-stu-id="c091f-119">Registers</span></span>

<span data-ttu-id="c091f-120">[PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 Register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) listet die verschiedenen Register auf, die von Shader Alu verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c091f-120">[ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) lists the different registers used by the shader ALU.</span></span>

## <a name="modifiers"></a><span data-ttu-id="c091f-121">Modifizierer</span><span class="sxs-lookup"><span data-stu-id="c091f-121">Modifiers</span></span>

<span data-ttu-id="c091f-122">[Modifiziererer für PS \_ 1 \_ X](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-1-x.md) können verwendet werden, um die Funktionalität einer Anweisung oder die aus einem Register gelesenen oder geschriebenen Daten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c091f-122">[Modifiers for ps\_1\_X](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-1-x.md) can be used to change the functionality of an instruction, or the data read from or written to a register.</span></span>

<span data-ttu-id="c091f-123">Direct3D 9 erfordert Zwischenberechnungen, um mindestens eine 8-Bit-Genauigkeit für alle Oberflächen Formate beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="c091f-123">Direct3D 9 requires intermediate computations to maintain at least 8-bit precision for all surface formats.</span></span> <span data-ttu-id="c091f-124">Es wird empfohlen, eine höhere Genauigkeit (12-Bit) für in-Stage-Mathematik und eine Sättigung von 8 Bits zwischen Textur Phasen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c091f-124">Both higher precision (12-bit) for in-stage math, and saturation to 8-bits between texture stages are recommended.</span></span> <span data-ttu-id="c091f-125">Es werden keine änderbaren Rundungs Modi oder Ausnahmen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c091f-125">No modifiable rounding modes or exceptions are supported.</span></span> <span data-ttu-id="c091f-126">Multiplikation sollte mit einer Round-to-Next-Genauigkeit unterstützt werden, um den Genauigkeits Verlust minimal zu halten.</span><span class="sxs-lookup"><span data-stu-id="c091f-126">Multiplication should be supported with a round-to-nearest precision to keep precision loss to a minimum.</span></span>

## <a name="sampler-count"></a><span data-ttu-id="c091f-127">Sampleranzahl</span><span class="sxs-lookup"><span data-stu-id="c091f-127">Sampler Count</span></span>

<span data-ttu-id="c091f-128">Die Anzahl der verfügbaren Textur-Samplern ist:</span><span class="sxs-lookup"><span data-stu-id="c091f-128">The number of texture samplers available is:</span></span>

-   <span data-ttu-id="c091f-129">Für PS \_ 1 \_ 0-PS \_ 1 \_ 3 beträgt der Höchstwert 4.</span><span class="sxs-lookup"><span data-stu-id="c091f-129">For ps\_1\_0 - ps\_1\_3, the maximum is 4.</span></span>
-   <span data-ttu-id="c091f-130">Für PS \_ 1 \_ 4 ist der Höchstwert 6.</span><span class="sxs-lookup"><span data-stu-id="c091f-130">For ps\_1\_4, the maximum is 6.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c091f-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c091f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c091f-132">Pixel-Shader</span><span class="sxs-lookup"><span data-stu-id="c091f-132">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




