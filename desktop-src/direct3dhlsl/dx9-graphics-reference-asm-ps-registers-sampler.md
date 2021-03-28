---
title: Sampler (Direct3D 9 ASM-PS)
description: Ein Sampler ist ein Eingabe-Pseudo Register für einen PixelShader, der zum Identifizieren der Samplingphase verwendet wird.
ms.assetid: 37cc28ae-fbd0-4f81-9e8e-f9609980d84e
keywords:
- Sampler, Typ (Direct3D 9 ASM-PS)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77875eed0827ad6bcb6d89111b13b6a31232dd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039168"
---
# <a name="sampler-direct3d-9-asm-ps"></a><span data-ttu-id="48c4b-104">Sampler (Direct3D 9 ASM-PS)</span><span class="sxs-lookup"><span data-stu-id="48c4b-104">Sampler (Direct3D 9 asm-ps)</span></span>

<span data-ttu-id="48c4b-105">Ein Sampler ist ein Eingabe-Pseudo Register für einen PixelShader, der zum Identifizieren der Samplingphase verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="48c4b-105">A sampler is a input pseudo-register for a pixel shader, which is used to identify the sampling stage.</span></span> <span data-ttu-id="48c4b-106">Es gibt 16 Pixel-Shader-samplingstaging-Register: S0 in S15.</span><span class="sxs-lookup"><span data-stu-id="48c4b-106">There are 16 pixel shader sampling stage registers: s0 to s15.</span></span> <span data-ttu-id="48c4b-107">Daher können bis zu 16 Textur Oberflächen in einem einzelnen shaderdurchlauf gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="48c4b-107">Therefore, up to 16 texture surfaces can be read in a single shader pass.</span></span> <span data-ttu-id="48c4b-108">Die Anweisungen, die ein Samplerregister verwenden, sind texld und texldp.</span><span class="sxs-lookup"><span data-stu-id="48c4b-108">The instructions that use a sampler register are texld and texldp.</span></span>

<span data-ttu-id="48c4b-109">Der Sampler muss vor der Verwendung mit der [DCL \_ -Anweisung samplertype (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="48c4b-109">Sampler must be declared before use with the [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md) instruction.</span></span>



| <span data-ttu-id="48c4b-110">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="48c4b-110">Pixel shader versions</span></span> | <span data-ttu-id="48c4b-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="48c4b-111">1\_1</span></span> | <span data-ttu-id="48c4b-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="48c4b-112">1\_2</span></span> | <span data-ttu-id="48c4b-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="48c4b-113">1\_3</span></span> | <span data-ttu-id="48c4b-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="48c4b-114">1\_4</span></span> | <span data-ttu-id="48c4b-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="48c4b-115">2\_0</span></span> | <span data-ttu-id="48c4b-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="48c4b-116">2\_sw</span></span> | <span data-ttu-id="48c4b-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="48c4b-117">2\_x</span></span> | <span data-ttu-id="48c4b-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="48c4b-118">3\_0</span></span> | <span data-ttu-id="48c4b-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="48c4b-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="48c4b-120">Sampler</span><span class="sxs-lookup"><span data-stu-id="48c4b-120">Sampler</span></span>               |      |      |      |      | <span data-ttu-id="48c4b-121">x</span><span class="sxs-lookup"><span data-stu-id="48c4b-121">x</span></span>    | <span data-ttu-id="48c4b-122">x</span><span class="sxs-lookup"><span data-stu-id="48c4b-122">x</span></span>     | <span data-ttu-id="48c4b-123">x</span><span class="sxs-lookup"><span data-stu-id="48c4b-123">x</span></span>    | <span data-ttu-id="48c4b-124">x</span><span class="sxs-lookup"><span data-stu-id="48c4b-124">x</span></span>    | <span data-ttu-id="48c4b-125">x</span><span class="sxs-lookup"><span data-stu-id="48c4b-125">x</span></span>     |



 

<span data-ttu-id="48c4b-126">Samplers sind Pseudo Register, da Sie Sie nicht direkt lesen oder schreiben können.</span><span class="sxs-lookup"><span data-stu-id="48c4b-126">Samplers are pseudo registers because you cannot directly read or write to them.</span></span>

<span data-ttu-id="48c4b-127">Eine samplingeinheit entspricht der Phase der Textur Stichprobe und kapselt den samplingspezifischen Zustand, der von [**setsamplerstate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate)bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="48c4b-127">A sampling unit corresponds to the texture sampling stage, encapsulating the sampling-specific state provided by [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span></span> <span data-ttu-id="48c4b-128">Jeder Sampler identifiziert eindeutig eine einzelne Textur Oberfläche, die auf den entsprechenden Sampler mithilfe von [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="48c4b-128">Each sampler uniquely identifies a single texture surface, which is set to the corresponding sampler using the [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="48c4b-129">Allerdings kann die gleiche Textur Oberfläche bei mehreren Samplers festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="48c4b-129">However, the same texture surface can be set at multiple samplers.</span></span>

<span data-ttu-id="48c4b-130">Bei der zeichnungszeit kann eine Textur nicht gleichzeitig als Renderziel und Textur in einer Phase festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="48c4b-130">At draw time, a texture cannot be simultaneously set as a render target and a texture at a stage.</span></span>

<span data-ttu-id="48c4b-131">Ein Sampler kann als einziges Argument in der Textur Lade Anweisung angezeigt werden: [texldl-PS](texldl---ps.md).</span><span class="sxs-lookup"><span data-stu-id="48c4b-131">A sampler might appear as the only argument in the texture load instruction: [texldl - ps](texldl---ps.md).</span></span>

<span data-ttu-id="48c4b-132">Wenn in PS \_ 3 \_ 0 ein Sampler verwendet wird, muss er am Anfang des Shader-Programms mithilfe der [DCL-Anweisung \_ samplertype (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="48c4b-132">In ps\_3\_0, if a sampler is used, it needs to be declared at the beginning of the shader program using the [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md) instruction.</span></span>

<span data-ttu-id="48c4b-133">Das Sampling einer Textur mit einer höheren Dimension als in den Texturkoordinaten vorhanden ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="48c4b-133">Sampling a texture with a higher dimension than is present in the texture coordinates is illegal.</span></span> <span data-ttu-id="48c4b-134">Das Sampling einer Textur mit einer niedrigeren Dimension als in den Texturkoordinaten vorhanden ist, ignoriert die zusätzlichen Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="48c4b-134">Sampling a texture with a lower dimension than is present in the texture coordinates will ignore the extra texture coordinates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48c4b-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="48c4b-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48c4b-136">Register</span><span class="sxs-lookup"><span data-stu-id="48c4b-136">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 