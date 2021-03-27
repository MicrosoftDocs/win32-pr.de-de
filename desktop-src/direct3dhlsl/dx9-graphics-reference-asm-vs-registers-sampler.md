---
title: Sampler (Direct3D 9 ASM-vs)
description: Ein Sampler ist ein Eingabe-Pseudo Register für einen Vertex-Shader, der zum Identifizieren der Samplingphase verwendet wird. Es gibt vier Vertex-Shader-Samplern S0 in S3. Vier Textur Oberflächen können in einem einzelnen shaderdurchlauf gelesen werden.
ms.assetid: a4588ced-24e2-4d4e-93e4-35a985bafaa4
keywords:
- Sampler, Type (Direct3D 9 ASM-vs)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 685f261da9d56dc29c0632d01cabbf29cd13a00f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390956"
---
# <a name="sampler-direct3d-9-asm-vs"></a><span data-ttu-id="5fb0a-106">Sampler (Direct3D 9 ASM-vs)</span><span class="sxs-lookup"><span data-stu-id="5fb0a-106">Sampler (Direct3D 9 asm-vs)</span></span>

<span data-ttu-id="5fb0a-107">Ein Sampler ist ein Eingabe-Pseudo Register für einen Vertex-Shader, der zum Identifizieren der Samplingphase verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-107">A sampler is a input pseudo-register for a vertex shader, which is used to identify the sampling stage.</span></span> <span data-ttu-id="5fb0a-108">Es gibt vier Vertex-Shader-Samplers: S0 bis S3.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-108">There are four vertex shader samplers: s0 to s3.</span></span> <span data-ttu-id="5fb0a-109">Vier Textur Oberflächen können in einem einzelnen shaderdurchlauf gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-109">Four texture surfaces can be read in a single shader pass.</span></span>

<span data-ttu-id="5fb0a-110">Sampler (Direct3D 9 ASM-vs) s sind Pseudo Register, da Sie Sie nicht direkt lesen oder schreiben können.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-110">Sampler (Direct3D 9 asm-vs)s are pseudo registers because you cannot directly read or write to them.</span></span>

<span data-ttu-id="5fb0a-111">Eine samplingeinheit entspricht der Phase der Textur Stichprobe und kapselt den samplingspezifischen Zustand, der von [**setsamplerstate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate)bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-111">A sampling unit corresponds to the texture sampling stage, encapsulating the sampling-specific state provided by [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span></span> <span data-ttu-id="5fb0a-112">Jeder Sampler identifiziert eindeutig eine einzelne Textur Oberfläche, die auf den entsprechenden Sampler mithilfe von [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-112">Each sampler uniquely identifies a single texture surface, which is set to the corresponding sampler using the [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="5fb0a-113">Allerdings kann die gleiche Textur Oberfläche bei mehreren Samplers festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-113">However, the same texture surface can be set at multiple samplers.</span></span>

<span data-ttu-id="5fb0a-114">Bei der zeichnungszeit kann eine Textur nicht gleichzeitig als Renderziel und Textur in einer Phase festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-114">At draw time, a texture cannot be simultaneously set as a render target and a texture at a stage.</span></span>

<span data-ttu-id="5fb0a-115">Da vier Samplers vorhanden sind, können bis zu vier Textur Oberflächen in einem einzelnen shaderdurchlauf aus gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-115">Because there are four samplers, up to four texture surfaces can be read from in a single shader pass.</span></span> <span data-ttu-id="5fb0a-116">Ein Sampler kann als einziges Argument in der Textur Lade Anweisung angezeigt werden: [texldl-vs](texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="5fb0a-116">A sampler might appear as the only argument in the texture load instruction: [texldl - vs](texldl---vs.md).</span></span>

<span data-ttu-id="5fb0a-117">Wenn in vs \_ 3 \_ 0 ein Sampler verwendet wird, muss er am Anfang des Shader-Programms mithilfe der [DCL \_ -Anweisung samplertype (SM3-vs ASM)](dcl-samplertype---vs.md) deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-117">In vs\_3\_0, if a sampler is used, it needs to be declared at the beginning of the shader program using the [dcl\_samplerType (sm3 - vs asm)](dcl-samplertype---vs.md) instruction.</span></span>



| <span data-ttu-id="5fb0a-118">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="5fb0a-118">Vertex shader versions</span></span> | <span data-ttu-id="5fb0a-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="5fb0a-119">1\_1</span></span> | <span data-ttu-id="5fb0a-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5fb0a-120">2\_0</span></span> | <span data-ttu-id="5fb0a-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5fb0a-121">2\_sw</span></span> | <span data-ttu-id="5fb0a-122">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5fb0a-122">2\_x</span></span> | <span data-ttu-id="5fb0a-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5fb0a-123">3\_0</span></span> | <span data-ttu-id="5fb0a-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5fb0a-124">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="5fb0a-125">Sampler</span><span class="sxs-lookup"><span data-stu-id="5fb0a-125">Sampler</span></span>                |      |      |       |      | <span data-ttu-id="5fb0a-126">x</span><span class="sxs-lookup"><span data-stu-id="5fb0a-126">x</span></span>    | <span data-ttu-id="5fb0a-127">x</span><span class="sxs-lookup"><span data-stu-id="5fb0a-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="5fb0a-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5fb0a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fb0a-129">Vertex-Shader-Register</span><span class="sxs-lookup"><span data-stu-id="5fb0a-129">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> <dt>

[<span data-ttu-id="5fb0a-130">Scheitelpunkt Texturen in vs \_ 3 \_ 0 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5fb0a-130">Vertex Textures in vs\_3\_0 (DirectX HLSL)</span></span>](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0)
</dt> </dl>

 

 