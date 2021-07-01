---
title: dcl_samplerType (sm2, sm3 – ps asm)
description: Deklarieren Sie einen Pixelshader-Sampler.
ms.assetid: c90ff5b6-f89a-4993-8a5d-dbbc4a7896b0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7a6da220e50b43ce990c090c61d1caf84afec653
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129667"
---
# <a name="dcl_samplertype-sm2-sm3---ps-asm"></a><span data-ttu-id="6f536-103">dcl \_ samplerType (sm2, sm3 – ps asm)</span><span class="sxs-lookup"><span data-stu-id="6f536-103">dcl\_samplerType (sm2, sm3 - ps asm)</span></span>

<span data-ttu-id="6f536-104">Deklarieren Sie einen Pixelshader-Sampler.</span><span class="sxs-lookup"><span data-stu-id="6f536-104">Declare a pixel shader sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f536-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f536-105">Syntax</span></span>

<span data-ttu-id="6f536-106">dcl \_ samplerType s\#</span><span class="sxs-lookup"><span data-stu-id="6f536-106">dcl\_samplerType s\#</span></span>



 

<span data-ttu-id="6f536-107">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="6f536-107">where:</span></span>

-   <span data-ttu-id="6f536-108">\_samplerType definiert den Samplerdatentyp.</span><span class="sxs-lookup"><span data-stu-id="6f536-108">\_samplerType defines the sampler data type.</span></span> <span data-ttu-id="6f536-109">Dadurch wird bestimmt, wie viele Koordinaten für jede Texturkoordinate beim Sampling erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="6f536-109">This determines how many coordinates are required by each texture coordinate when sampling.</span></span> <span data-ttu-id="6f536-110">Die folgenden Texturkoordinatendimensionen sind definiert.</span><span class="sxs-lookup"><span data-stu-id="6f536-110">The following texture coordinate dimensions are defined.</span></span>
    -   <span data-ttu-id="6f536-111">\_2d</span><span class="sxs-lookup"><span data-stu-id="6f536-111">\_2d</span></span>
    -   <span data-ttu-id="6f536-112">\_Cube</span><span class="sxs-lookup"><span data-stu-id="6f536-112">\_cube</span></span>
    -   <span data-ttu-id="6f536-113">\_Volumen</span><span class="sxs-lookup"><span data-stu-id="6f536-113">\_volume</span></span>
-   <span data-ttu-id="6f536-114">s \# identifiziert einen Sampler, wobei s eine Abkürzung für den Sampler \# und die Samplernummer ist.</span><span class="sxs-lookup"><span data-stu-id="6f536-114">s\# identifies a sampler where s is an abbreviation for the sampler, and \# is the sampler number.</span></span> <span data-ttu-id="6f536-115">Sampler sind Pseudoregister, da Sie sie nicht direkt lesen oder schreiben können.</span><span class="sxs-lookup"><span data-stu-id="6f536-115">Samplers are pseudo registers because you cannot directly read or write to them.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f536-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f536-116">Remarks</span></span>



| <span data-ttu-id="6f536-117">Pixelshaderversionen</span><span class="sxs-lookup"><span data-stu-id="6f536-117">Pixel shader versions</span></span> | <span data-ttu-id="6f536-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="6f536-118">1\_1</span></span> | <span data-ttu-id="6f536-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="6f536-119">1\_2</span></span> | <span data-ttu-id="6f536-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6f536-120">1\_3</span></span> | <span data-ttu-id="6f536-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="6f536-121">1\_4</span></span> | <span data-ttu-id="6f536-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6f536-122">2\_0</span></span> | <span data-ttu-id="6f536-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6f536-123">2\_x</span></span> | <span data-ttu-id="6f536-124">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="6f536-124">2\_sw</span></span> | <span data-ttu-id="6f536-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6f536-125">3\_0</span></span> | <span data-ttu-id="6f536-126">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="6f536-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="6f536-127">dcl \_ samplerType</span><span class="sxs-lookup"><span data-stu-id="6f536-127">dcl\_samplerType</span></span>      |      |      |      |      | <span data-ttu-id="6f536-128">x</span><span class="sxs-lookup"><span data-stu-id="6f536-128">x</span></span>    | <span data-ttu-id="6f536-129">x</span><span class="sxs-lookup"><span data-stu-id="6f536-129">x</span></span>    | <span data-ttu-id="6f536-130">x</span><span class="sxs-lookup"><span data-stu-id="6f536-130">x</span></span>     | <span data-ttu-id="6f536-131">x</span><span class="sxs-lookup"><span data-stu-id="6f536-131">x</span></span>    | <span data-ttu-id="6f536-132">x</span><span class="sxs-lookup"><span data-stu-id="6f536-132">x</span></span>     |



 

<span data-ttu-id="6f536-133">Alle dcl \_ samplerType-Anweisungen müssen vor der ersten ausführbaren Anweisung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6f536-133">All dcl\_samplerType instructions must appear before the first executable instruction.</span></span>

## <a name="example"></a><span data-ttu-id="6f536-134">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6f536-134">Example</span></span>


```
dcl_cube t0.rgb;  // Define a 3D texture map.

add r0, r0, t0;   // Perturb texture coordinates. 
texld r0, s0, r0; // Load r0 with a color sampled from stage0
                  //   at perturbed texture coordinates r0.
                  // This is a dependent texture read.
```



## <a name="related-topics"></a><span data-ttu-id="6f536-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6f536-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f536-136">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="6f536-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




