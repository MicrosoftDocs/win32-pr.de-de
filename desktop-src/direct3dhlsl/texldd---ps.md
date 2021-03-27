---
title: texldd-PS
description: Modelliert eine Textur mit zusätzlichen Farbverlaufs Eingaben.
ms.assetid: 6d6b3180-d82e-4be4-929b-e5a6431bec38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72f3c4aaf9ac7e6beaad1343c024aa28bd2a85ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390343"
---
# <a name="texldd---ps"></a><span data-ttu-id="59720-103">texldd-PS</span><span class="sxs-lookup"><span data-stu-id="59720-103">texldd - ps</span></span>

<span data-ttu-id="59720-104">Modelliert eine Textur mit zusätzlichen Farbverlaufs Eingaben.</span><span class="sxs-lookup"><span data-stu-id="59720-104">Samples a texture with additional gradient inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="59720-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="59720-105">Syntax</span></span>



| <span data-ttu-id="59720-106">texldd, DST, src0, Quelle1, Quelle2, src3</span><span class="sxs-lookup"><span data-stu-id="59720-106">texldd, dst, src0, src1, src2, src3</span></span> |
|-------------------------------------|



 

<span data-ttu-id="59720-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="59720-107">Where:</span></span>

-   <span data-ttu-id="59720-108">DST ist ein Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="59720-108">dst is a destination register.</span></span>
-   <span data-ttu-id="59720-109">src0 ist ein Quell Register, das die Texturkoordinaten für das Textur Beispiel bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="59720-109">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="59720-110">Siehe [Texturkoordinaten Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="59720-110">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="59720-111">Quelle1 identifiziert die Quell-Samplerregister \# , bei der \# angibt, welche Textur samplingnummer Stichproben geben soll.</span><span class="sxs-lookup"><span data-stu-id="59720-111">src1 identifies the source sampler register (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="59720-112">Der Sampler hat ihm eine Textur und einen von der [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) -Enumeration definierten Steuerelement Zustand zugeordnet (z.</span><span class="sxs-lookup"><span data-stu-id="59720-112">The sampler has associated with it a texture and a control state defined by the [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) enumeration (ex.</span></span> <span data-ttu-id="59720-113">D3DSAMP \_ MinFilter).</span><span class="sxs-lookup"><span data-stu-id="59720-113">D3DSAMP\_MINFILTER).</span></span>
-   <span data-ttu-id="59720-114">Quelle2 ist ein Eingabe Quellen Register, das den x-Farbverlauf angibt.</span><span class="sxs-lookup"><span data-stu-id="59720-114">src2 is an input source register that specifies the x gradient.</span></span>
-   <span data-ttu-id="59720-115">src3 ist ein Eingabe Quellen Register, das den y-Farbverlauf angibt.</span><span class="sxs-lookup"><span data-stu-id="59720-115">src3 is an input source register that specifies the y gradient.</span></span>

## <a name="remarks"></a><span data-ttu-id="59720-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59720-116">Remarks</span></span>



| <span data-ttu-id="59720-117">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="59720-117">Pixel shader versions</span></span> | <span data-ttu-id="59720-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="59720-118">1\_1</span></span> | <span data-ttu-id="59720-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="59720-119">1\_2</span></span> | <span data-ttu-id="59720-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="59720-120">1\_3</span></span> | <span data-ttu-id="59720-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="59720-121">1\_4</span></span> | <span data-ttu-id="59720-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="59720-122">2\_0</span></span> | <span data-ttu-id="59720-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="59720-123">2\_x</span></span> | <span data-ttu-id="59720-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="59720-124">2\_sw</span></span> | <span data-ttu-id="59720-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="59720-125">3\_0</span></span> | <span data-ttu-id="59720-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="59720-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="59720-127">texldd</span><span class="sxs-lookup"><span data-stu-id="59720-127">texldd</span></span>                |      |      |      |      |      | <span data-ttu-id="59720-128">Stuben \*</span><span class="sxs-lookup"><span data-stu-id="59720-128">x \*</span></span> | <span data-ttu-id="59720-129">x</span><span class="sxs-lookup"><span data-stu-id="59720-129">x</span></span>     | <span data-ttu-id="59720-130">x</span><span class="sxs-lookup"><span data-stu-id="59720-130">x</span></span>    | <span data-ttu-id="59720-131">x</span><span class="sxs-lookup"><span data-stu-id="59720-131">x</span></span>     |



 

<span data-ttu-id="59720-132">\* Diese Anweisung wird nur von PS \_ 2 a unterstützt \_ .</span><span class="sxs-lookup"><span data-stu-id="59720-132">\* This instruction is only supported by ps\_2\_a.</span></span> <span data-ttu-id="59720-133">Sie wird von PS 2 b nicht unterstützt \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="59720-133">It is not supported by ps\_2\_b.</span></span> <span data-ttu-id="59720-134">Weitere Informationen zu Profilen finden Sie unter [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile).</span><span class="sxs-lookup"><span data-stu-id="59720-134">For more information about profiles, see [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile).</span></span>

<span data-ttu-id="59720-135">Diese Anweisung unterscheidet eine Textur mithilfe der Texturkoordinaten bei src0, dem durch Quelle1 angegebenen Sampler und den Gradienten DSX und DSY aus Quelle2 und src3.</span><span class="sxs-lookup"><span data-stu-id="59720-135">This instruction samples a texture using the texture coordinates at src0, the sampler specified by src1, and the gradients DSX and DSY coming from src2 and src3.</span></span> <span data-ttu-id="59720-136">Die Werte für x und y-Farbverlauf werden verwendet, um die entsprechende MipMap-Ebene der Textur für die Stichprobenentnahme auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="59720-136">The x and y gradient values are used to select the appropriate mipmap level of the texture for sampling.</span></span>

<span data-ttu-id="59720-137">Alle Quellen unterstützen willkürliche Streifen.</span><span class="sxs-lookup"><span data-stu-id="59720-137">All sources support arbitrary swizzles.</span></span>

<span data-ttu-id="59720-138">Alle Schreib Masken sind auf dem Ziel gültig.</span><span class="sxs-lookup"><span data-stu-id="59720-138">All write masks are valid on the destination.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59720-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="59720-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59720-140">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="59720-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 