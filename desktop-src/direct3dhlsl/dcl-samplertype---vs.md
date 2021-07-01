---
title: dcl_samplerType (sm3 – vs asm)
description: Deklarieren Sie einen Vertex-Shader-Sampler.
ms.assetid: 733307ac-24ab-4db7-bf70-58a83b4c39b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2fbcb934ad591274d743f09c810de2db42278261
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129868"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a><span data-ttu-id="72077-103">dcl \_ samplerType (sm3 – vs asm)</span><span class="sxs-lookup"><span data-stu-id="72077-103">dcl\_samplerType (sm3 - vs asm)</span></span>

<span data-ttu-id="72077-104">Deklarieren Sie einen Vertex-Shader-Sampler.</span><span class="sxs-lookup"><span data-stu-id="72077-104">Declare a vertex shader sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="72077-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="72077-105">Syntax</span></span>

<span data-ttu-id="72077-106">dcl \_ samplerType s\#</span><span class="sxs-lookup"><span data-stu-id="72077-106">dcl\_samplerType s\#</span></span>



 

<span data-ttu-id="72077-107">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="72077-107">where:</span></span>

-   <span data-ttu-id="72077-108">\_samplerType definiert den Samplerdatentyp.</span><span class="sxs-lookup"><span data-stu-id="72077-108">\_samplerType defines the sampler data type.</span></span> <span data-ttu-id="72077-109">Dadurch wird bestimmt, wie viele Koordinaten für jede Texturkoordinate beim Sampling erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="72077-109">This determines how many coordinates are required by each texture coordinate when sampling.</span></span> <span data-ttu-id="72077-110">Die folgenden Texturkoordinatendimensionen sind definiert.</span><span class="sxs-lookup"><span data-stu-id="72077-110">The following texture coordinate dimensions are defined.</span></span>
    -   <span data-ttu-id="72077-111">\_2d</span><span class="sxs-lookup"><span data-stu-id="72077-111">\_2d</span></span>
    -   <span data-ttu-id="72077-112">\_Cube</span><span class="sxs-lookup"><span data-stu-id="72077-112">\_cube</span></span>
    -   <span data-ttu-id="72077-113">\_Volumen</span><span class="sxs-lookup"><span data-stu-id="72077-113">\_volume</span></span>
-   <span data-ttu-id="72077-114">s \# identifiziert einen Sampler, wobei s eine Abkürzung für den \# Sampler und die Samplernummer ist.</span><span class="sxs-lookup"><span data-stu-id="72077-114">s\# identifies a sampler where s is an abbreviation for the sampler, and \# is the sampler number.</span></span> <span data-ttu-id="72077-115">[Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)sind Pseudoregister, da sie nicht direkt gelesen oder geschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="72077-115">[Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)s are pseudo registers because you cannot directly read or write to them.</span></span>

## <a name="remarks"></a><span data-ttu-id="72077-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72077-116">Remarks</span></span>



| <span data-ttu-id="72077-117">Vertex-Shaderversionen</span><span class="sxs-lookup"><span data-stu-id="72077-117">Vertex shader versions</span></span> | <span data-ttu-id="72077-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="72077-118">1\_1</span></span> | <span data-ttu-id="72077-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="72077-119">2\_0</span></span> | <span data-ttu-id="72077-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="72077-120">2\_x</span></span> | <span data-ttu-id="72077-121">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="72077-121">2\_sw</span></span> | <span data-ttu-id="72077-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="72077-122">3\_0</span></span> | <span data-ttu-id="72077-123">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="72077-123">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="72077-124">dcl \_ samplerType</span><span class="sxs-lookup"><span data-stu-id="72077-124">dcl\_samplerType</span></span>       |      |      |      |       | <span data-ttu-id="72077-125">x</span><span class="sxs-lookup"><span data-stu-id="72077-125">x</span></span>    | <span data-ttu-id="72077-126">x</span><span class="sxs-lookup"><span data-stu-id="72077-126">x</span></span>     |



 

<span data-ttu-id="72077-127">Alle dcl \_ samplerType-Anweisungen müssen vor der ersten ausführbaren Anweisung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="72077-127">All dcl\_samplerType instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72077-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="72077-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72077-129">Vertex-Shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="72077-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




