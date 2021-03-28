---
title: breakp-PS
description: Unterbrechen Sie die aktuelle Schleife bedingt bei den nächstgelegenen ENDLOOP-PS oder ENDREP-PS. Verwenden Sie eine der Komponenten des Prädikats "Register" als Bedingung, um zu bestimmen, ob die Anweisung durchgeführt werden soll.
ms.assetid: be219239-fccb-4561-8b71-083c47ba915b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e358debb2377f08574997acd96c11f83d32e66c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389551"
---
# <a name="breakp---ps"></a><span data-ttu-id="bab2c-104">breakp-PS</span><span class="sxs-lookup"><span data-stu-id="bab2c-104">breakp - ps</span></span>

<span data-ttu-id="bab2c-105">Unterbrechen Sie die aktuelle Schleife bedingt bei den nächstgelegenen [ENDLOOP-PS](endloop---ps.md) oder [ENDREP-PS](endrep---ps.md).</span><span class="sxs-lookup"><span data-stu-id="bab2c-105">Conditionally break out of the current loop at the nearest [endloop - ps](endloop---ps.md) or [endrep - ps](endrep---ps.md).</span></span> <span data-ttu-id="bab2c-106">Verwenden Sie eine der Komponenten des Prädikats "Register" als Bedingung, um zu bestimmen, ob die Anweisung durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bab2c-106">Use one of the components of the predicate register as a condition to determine whether or not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="bab2c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bab2c-107">Syntax</span></span>



| <span data-ttu-id="bab2c-108">Break p \[ ! \] P0. Stuben</span><span class="sxs-lookup"><span data-stu-id="bab2c-108">breakp \[!\]p0.{x\</span></span>|<span data-ttu-id="bab2c-109">Teenie</span><span class="sxs-lookup"><span data-stu-id="bab2c-109">y\</span></span>|<span data-ttu-id="bab2c-110">z</span><span class="sxs-lookup"><span data-stu-id="bab2c-110">z\</span></span>|<span data-ttu-id="bab2c-111">Löw</span><span class="sxs-lookup"><span data-stu-id="bab2c-111">w}</span></span> |
|-----------------------------|



 

<span data-ttu-id="bab2c-112">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="bab2c-112">Where:</span></span>

-   <span data-ttu-id="bab2c-113">\[!\] ist ein optionaler Negation-Modifizierer.</span><span class="sxs-lookup"><span data-stu-id="bab2c-113">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="bab2c-114">P0 ist das [Prädikat Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="bab2c-114">p0 is the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>
-   <span data-ttu-id="bab2c-115">{x \| y \| z \| w} ist das erforderliche Replizieren von Replizieren auf p0.</span><span class="sxs-lookup"><span data-stu-id="bab2c-115">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="bab2c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bab2c-116">Remarks</span></span>



| <span data-ttu-id="bab2c-117">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="bab2c-117">Pixel shader versions</span></span> | <span data-ttu-id="bab2c-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="bab2c-118">1\_1</span></span> | <span data-ttu-id="bab2c-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="bab2c-119">1\_2</span></span> | <span data-ttu-id="bab2c-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="bab2c-120">1\_3</span></span> | <span data-ttu-id="bab2c-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="bab2c-121">1\_4</span></span> | <span data-ttu-id="bab2c-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bab2c-122">2\_0</span></span> | <span data-ttu-id="bab2c-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="bab2c-123">2\_x</span></span> | <span data-ttu-id="bab2c-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bab2c-124">2\_sw</span></span> | <span data-ttu-id="bab2c-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bab2c-125">3\_0</span></span> | <span data-ttu-id="bab2c-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bab2c-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="bab2c-127">Break p</span><span class="sxs-lookup"><span data-stu-id="bab2c-127">breakp</span></span>                |      |      |      |      |      | <span data-ttu-id="bab2c-128">x</span><span class="sxs-lookup"><span data-stu-id="bab2c-128">x</span></span>    | <span data-ttu-id="bab2c-129">x</span><span class="sxs-lookup"><span data-stu-id="bab2c-129">x</span></span>     | <span data-ttu-id="bab2c-130">x</span><span class="sxs-lookup"><span data-stu-id="bab2c-130">x</span></span>    | <span data-ttu-id="bab2c-131">x</span><span class="sxs-lookup"><span data-stu-id="bab2c-131">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="bab2c-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bab2c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bab2c-133">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="bab2c-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




