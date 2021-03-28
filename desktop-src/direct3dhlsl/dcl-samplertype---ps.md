---
title: dcl_samplerType (SM2, SM3-PS ASM)
description: Deklarieren Sie einen Pixel-Shadersampler.
ms.assetid: c90ff5b6-f89a-4993-8a5d-dbbc4a7896b0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 934931d6063ac264a2e6685104f8ed6fbdaaa64e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038369"
---
# <a name="dcl_samplertype-sm2-sm3---ps-asm"></a><span data-ttu-id="f8a41-103">DCL- \_ samplertype (SM2, SM3-PS ASM)</span><span class="sxs-lookup"><span data-stu-id="f8a41-103">dcl\_samplerType (sm2, sm3 - ps asm)</span></span>

<span data-ttu-id="f8a41-104">Deklarieren Sie einen Pixel-Shadersampler.</span><span class="sxs-lookup"><span data-stu-id="f8a41-104">Declare a pixel shader sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8a41-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8a41-105">Syntax</span></span>



|                      |
|----------------------|
| <span data-ttu-id="f8a41-106">DCL- \_ samplertype s\#</span><span class="sxs-lookup"><span data-stu-id="f8a41-106">dcl\_samplerType s\#</span></span> |



 

<span data-ttu-id="f8a41-107">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="f8a41-107">where:</span></span>

-   <span data-ttu-id="f8a41-108">\_samplertype definiert den samplerdatentyp.</span><span class="sxs-lookup"><span data-stu-id="f8a41-108">\_samplerType defines the sampler data type.</span></span> <span data-ttu-id="f8a41-109">Dies bestimmt, wie viele Koordinaten bei der Stichprobenentnahme für jede Textur Koordinate erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f8a41-109">This determines how many coordinates are required by each texture coordinate when sampling.</span></span> <span data-ttu-id="f8a41-110">Die folgenden Texturkoordinaten Dimensionen sind definiert.</span><span class="sxs-lookup"><span data-stu-id="f8a41-110">The following texture coordinate dimensions are defined.</span></span>
    -   <span data-ttu-id="f8a41-111">\_2D</span><span class="sxs-lookup"><span data-stu-id="f8a41-111">\_2d</span></span>
    -   <span data-ttu-id="f8a41-112">\_Cube</span><span class="sxs-lookup"><span data-stu-id="f8a41-112">\_cube</span></span>
    -   <span data-ttu-id="f8a41-113">\_Handels</span><span class="sxs-lookup"><span data-stu-id="f8a41-113">\_volume</span></span>
-   <span data-ttu-id="f8a41-114">s \# identifiziert einen Sampler, bei dem s eine Abkürzung für den Sampler und \# die samplernummer ist.</span><span class="sxs-lookup"><span data-stu-id="f8a41-114">s\# identifies a sampler where s is an abbreviation for the sampler, and \# is the sampler number.</span></span> <span data-ttu-id="f8a41-115">Samplers sind Pseudo Register, da Sie Sie nicht direkt lesen oder schreiben können.</span><span class="sxs-lookup"><span data-stu-id="f8a41-115">Samplers are pseudo registers because you cannot directly read or write to them.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8a41-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8a41-116">Remarks</span></span>



| <span data-ttu-id="f8a41-117">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="f8a41-117">Pixel shader versions</span></span> | <span data-ttu-id="f8a41-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="f8a41-118">1\_1</span></span> | <span data-ttu-id="f8a41-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="f8a41-119">1\_2</span></span> | <span data-ttu-id="f8a41-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f8a41-120">1\_3</span></span> | <span data-ttu-id="f8a41-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="f8a41-121">1\_4</span></span> | <span data-ttu-id="f8a41-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f8a41-122">2\_0</span></span> | <span data-ttu-id="f8a41-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f8a41-123">2\_x</span></span> | <span data-ttu-id="f8a41-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f8a41-124">2\_sw</span></span> | <span data-ttu-id="f8a41-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f8a41-125">3\_0</span></span> | <span data-ttu-id="f8a41-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f8a41-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="f8a41-127">DCL- \_ samplertype</span><span class="sxs-lookup"><span data-stu-id="f8a41-127">dcl\_samplerType</span></span>      |      |      |      |      | <span data-ttu-id="f8a41-128">x</span><span class="sxs-lookup"><span data-stu-id="f8a41-128">x</span></span>    | <span data-ttu-id="f8a41-129">x</span><span class="sxs-lookup"><span data-stu-id="f8a41-129">x</span></span>    | <span data-ttu-id="f8a41-130">x</span><span class="sxs-lookup"><span data-stu-id="f8a41-130">x</span></span>     | <span data-ttu-id="f8a41-131">x</span><span class="sxs-lookup"><span data-stu-id="f8a41-131">x</span></span>    | <span data-ttu-id="f8a41-132">x</span><span class="sxs-lookup"><span data-stu-id="f8a41-132">x</span></span>     |



 

<span data-ttu-id="f8a41-133">Alle DCL- \_ samplertype-Anweisungen müssen vor der ersten ausführbaren Anweisung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f8a41-133">All dcl\_samplerType instructions must appear before the first executable instruction.</span></span>

## <a name="example"></a><span data-ttu-id="f8a41-134">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f8a41-134">Example</span></span>


```
dcl_cube t0.rgb;  // Define a 3D texture map.

add r0, r0, t0;   // Perturb texture coordinates. 
texld r0, s0, r0; // Load r0 with a color sampled from stage0
                  //   at perturbed texture coordinates r0.
                  // This is a dependent texture read.
```



## <a name="related-topics"></a><span data-ttu-id="f8a41-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f8a41-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8a41-136">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="f8a41-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




