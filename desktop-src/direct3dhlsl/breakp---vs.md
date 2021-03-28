---
title: Break p-vs
description: Unterbrechen Sie die aktuelle Schleife bedingt bei den nächstgelegenen ENDLOOP-vs oder ENDREP-vs. verwenden Sie eine der Komponenten des Prädikats als Bedingung, um zu bestimmen, ob die Anweisung durchgeführt werden soll oder nicht.
ms.assetid: 940252a0-6f6a-45d8-9d2f-315cc97686ca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dbd0d5e20040bc2d353287eb4243c9e9d6d21dc8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038334"
---
# <a name="breakp---vs"></a><span data-ttu-id="52857-103">Break p-vs</span><span class="sxs-lookup"><span data-stu-id="52857-103">breakp - vs</span></span>

<span data-ttu-id="52857-104">Unterbrechen Sie die aktuelle Schleife bedingt bei den nächstgelegenen [endschleifen-vs](endloop---vs.md) oder [ENDREP-vs](endrep---vs.md). Verwenden Sie eine der Komponenten des Prädikats "Register" als Bedingung, um zu bestimmen, ob die Anweisung durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="52857-104">Conditionally break out of the current loop at the nearest [endloop - vs](endloop---vs.md) or [endrep - vs](endrep---vs.md). Use one of the components of the predicate register as a condition to determine whether or not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="52857-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="52857-105">Syntax</span></span>



| <span data-ttu-id="52857-106">Break p \[ ! \] P0. Stuben</span><span class="sxs-lookup"><span data-stu-id="52857-106">breakp \[!\]p0.{x\</span></span>|<span data-ttu-id="52857-107">Teenie</span><span class="sxs-lookup"><span data-stu-id="52857-107">y\</span></span>|<span data-ttu-id="52857-108">z</span><span class="sxs-lookup"><span data-stu-id="52857-108">z\</span></span>|<span data-ttu-id="52857-109">Löw</span><span class="sxs-lookup"><span data-stu-id="52857-109">w}</span></span> |
|-----------------------------|



 

<span data-ttu-id="52857-110">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="52857-110">Where:</span></span>

-   <span data-ttu-id="52857-111">\[!\] Optionaler boolescher Wert nicht.</span><span class="sxs-lookup"><span data-stu-id="52857-111">\[!\] optional boolean NOT.</span></span>
-   <span data-ttu-id="52857-112">P0 ist das Prädikat Register.</span><span class="sxs-lookup"><span data-stu-id="52857-112">p0 is the predicate register.</span></span> <span data-ttu-id="52857-113">Siehe [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="52857-113">See [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>
-   <span data-ttu-id="52857-114">{x \| y \| z \| w} ist das erforderliche Replizieren von Replizieren auf p0.</span><span class="sxs-lookup"><span data-stu-id="52857-114">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="52857-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52857-115">Remarks</span></span>



| <span data-ttu-id="52857-116">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="52857-116">Vertex shader versions</span></span> | <span data-ttu-id="52857-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="52857-117">1\_1</span></span> | <span data-ttu-id="52857-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="52857-118">2\_0</span></span> | <span data-ttu-id="52857-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="52857-119">2\_x</span></span> | <span data-ttu-id="52857-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="52857-120">2\_sw</span></span> | <span data-ttu-id="52857-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="52857-121">3\_0</span></span> | <span data-ttu-id="52857-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="52857-122">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="52857-123">Break p</span><span class="sxs-lookup"><span data-stu-id="52857-123">breakp</span></span>                 |      |      | <span data-ttu-id="52857-124">x</span><span class="sxs-lookup"><span data-stu-id="52857-124">x</span></span>    | <span data-ttu-id="52857-125">x</span><span class="sxs-lookup"><span data-stu-id="52857-125">x</span></span>     | <span data-ttu-id="52857-126">x</span><span class="sxs-lookup"><span data-stu-id="52857-126">x</span></span>    | <span data-ttu-id="52857-127">x</span><span class="sxs-lookup"><span data-stu-id="52857-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="52857-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="52857-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52857-129">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="52857-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




