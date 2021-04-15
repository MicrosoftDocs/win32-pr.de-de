---
title: dcl_samplerType (SM3-vs ASM)
description: Deklarieren Sie einen Vertex-Shadersampler.
ms.assetid: 733307ac-24ab-4db7-bf70-58a83b4c39b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 556655d793e94b9290fcd1a4a40fdf7f797e80ae
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993206"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a><span data-ttu-id="28439-103">DCL \_ -samplertype (SM3-vs ASM)</span><span class="sxs-lookup"><span data-stu-id="28439-103">dcl\_samplerType (sm3 - vs asm)</span></span>

<span data-ttu-id="28439-104">Deklarieren Sie einen Vertex-Shadersampler.</span><span class="sxs-lookup"><span data-stu-id="28439-104">Declare a vertex shader sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="28439-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="28439-105">Syntax</span></span>



|                      |
|----------------------|
| <span data-ttu-id="28439-106">DCL- \_ samplertype s\#</span><span class="sxs-lookup"><span data-stu-id="28439-106">dcl\_samplerType s\#</span></span> |



 

<span data-ttu-id="28439-107">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="28439-107">where:</span></span>

-   <span data-ttu-id="28439-108">\_samplertype definiert den samplerdatentyp.</span><span class="sxs-lookup"><span data-stu-id="28439-108">\_samplerType defines the sampler data type.</span></span> <span data-ttu-id="28439-109">Dies bestimmt, wie viele Koordinaten bei der Stichprobenentnahme für jede Textur Koordinate erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="28439-109">This determines how many coordinates are required by each texture coordinate when sampling.</span></span> <span data-ttu-id="28439-110">Die folgenden Texturkoordinaten Dimensionen sind definiert.</span><span class="sxs-lookup"><span data-stu-id="28439-110">The following texture coordinate dimensions are defined.</span></span>
    -   <span data-ttu-id="28439-111">\_2D</span><span class="sxs-lookup"><span data-stu-id="28439-111">\_2d</span></span>
    -   <span data-ttu-id="28439-112">\_Cube</span><span class="sxs-lookup"><span data-stu-id="28439-112">\_cube</span></span>
    -   <span data-ttu-id="28439-113">\_Handels</span><span class="sxs-lookup"><span data-stu-id="28439-113">\_volume</span></span>
-   <span data-ttu-id="28439-114">s \# identifiziert einen Sampler, bei dem s eine Abkürzung für den Sampler und \# die samplernummer ist.</span><span class="sxs-lookup"><span data-stu-id="28439-114">s\# identifies a sampler where s is an abbreviation for the sampler, and \# is the sampler number.</span></span> <span data-ttu-id="28439-115">[Sampler (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)s sind Pseudo Register, da Sie Sie nicht direkt lesen oder schreiben können.</span><span class="sxs-lookup"><span data-stu-id="28439-115">[Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)s are pseudo registers because you cannot directly read or write to them.</span></span>

## <a name="remarks"></a><span data-ttu-id="28439-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28439-116">Remarks</span></span>



| <span data-ttu-id="28439-117">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="28439-117">Vertex shader versions</span></span> | <span data-ttu-id="28439-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="28439-118">1\_1</span></span> | <span data-ttu-id="28439-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="28439-119">2\_0</span></span> | <span data-ttu-id="28439-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="28439-120">2\_x</span></span> | <span data-ttu-id="28439-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="28439-121">2\_sw</span></span> | <span data-ttu-id="28439-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="28439-122">3\_0</span></span> | <span data-ttu-id="28439-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="28439-123">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="28439-124">DCL- \_ samplertype</span><span class="sxs-lookup"><span data-stu-id="28439-124">dcl\_samplerType</span></span>       |      |      |      |       | <span data-ttu-id="28439-125">x</span><span class="sxs-lookup"><span data-stu-id="28439-125">x</span></span>    | <span data-ttu-id="28439-126">x</span><span class="sxs-lookup"><span data-stu-id="28439-126">x</span></span>     |



 

<span data-ttu-id="28439-127">Alle DCL- \_ samplertype-Anweisungen müssen vor der ersten ausführbaren Anweisung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="28439-127">All dcl\_samplerType instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28439-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="28439-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28439-129">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="28439-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




