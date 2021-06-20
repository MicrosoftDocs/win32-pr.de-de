---
title: Relative Adressierung (HLSL PS-Referenz)
description: Bei Pixel-Shadern kann die Syntax \\ nur in Registertypen verwendet werden, die in bestimmten Shadermodellen relativ adressiert werden können.
ms.assetid: 37e2bab9-f6fe-438a-8a2d-c963634ef8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8bdafe23696c460da75d87cf1f6d5a968c89ed28
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405483"
---
# <a name="relative-addressing-hlsl-ps-reference"></a><span data-ttu-id="d6a74-103">Relative Adressierung (HLSL PS-Referenz)</span><span class="sxs-lookup"><span data-stu-id="d6a74-103">Relative addressing (HLSL PS reference)</span></span>

<span data-ttu-id="d6a74-104">Die \[ \] Syntax kann nur in Registertypen verwendet werden, die in bestimmten Shadermodellen relativ adressiert werden können.</span><span class="sxs-lookup"><span data-stu-id="d6a74-104">The \[ \] syntax can be used only in register types that can be relatively addressed in certain shader models.</span></span> <span data-ttu-id="d6a74-105">Die unterstützten \[ \] Syntaxformen sind wie folgt aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="d6a74-105">The supported forms of \[ \] syntax are listed as follows:</span></span>

<span data-ttu-id="d6a74-106">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="d6a74-106">Where:</span></span>

-   <span data-ttu-id="d6a74-107">"R" bezeichnet jeden Registertyp, der relativ adressiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d6a74-107">"R" denotes any register type that can be relatively addressed.</span></span>
-   <span data-ttu-id="d6a74-108">"A" bezeichnet jedes Register, das als Index verwendet werden kann, um andere Register relativ zu adressieren.</span><span class="sxs-lookup"><span data-stu-id="d6a74-108">"A" denotes any register that can be used as an index to relatively address other registers.</span></span>
-   <span data-ttu-id="d6a74-109">n0 - ni, m0 - mj und k sind ganze Zahlen >= 0.</span><span class="sxs-lookup"><span data-stu-id="d6a74-109">n0 - ni, m0 - mj, and k are integers >= 0.</span></span>



| <span data-ttu-id="d6a74-110">\[\]Syntax</span><span class="sxs-lookup"><span data-stu-id="d6a74-110">\[ \] syntax</span></span>                              | <span data-ttu-id="d6a74-111">Effektiver Index</span><span class="sxs-lookup"><span data-stu-id="d6a74-111">Effective index</span></span>                       | <span data-ttu-id="d6a74-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6a74-112">Examples</span></span>                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| <span data-ttu-id="d6a74-113">R \[ A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="d6a74-113">R\[ A + m0 + ... + mj \]</span></span>                  | <span data-ttu-id="d6a74-114">A + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="d6a74-114">A + m0 + ... + mj</span></span>                     | <span data-ttu-id="d6a74-115">c \[ a0.x + 3 + 7 \]</span><span class="sxs-lookup"><span data-stu-id="d6a74-115">c\[ a0.x + 3 + 7 \]</span></span>              |
| <span data-ttu-id="d6a74-116">R \[ k ( = \] Rk )</span><span class="sxs-lookup"><span data-stu-id="d6a74-116">R\[ k \] ( = Rk )</span></span>                         | <span data-ttu-id="d6a74-117">k</span><span class="sxs-lookup"><span data-stu-id="d6a74-117">k</span></span>                                     | <span data-ttu-id="d6a74-118">c \[ 10 \] ( = c10 )</span><span class="sxs-lookup"><span data-stu-id="d6a74-118">c\[ 10 \] ( = c10 )</span></span>              |
| <span data-ttu-id="d6a74-119">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="d6a74-119">R\[ A \]</span></span>                                  | <span data-ttu-id="d6a74-120">Ein</span><span class="sxs-lookup"><span data-stu-id="d6a74-120">A</span></span>                                     | <span data-ttu-id="d6a74-121">c \[ a0.y \]</span><span class="sxs-lookup"><span data-stu-id="d6a74-121">c\[ a0.y \]</span></span>                      |
| <span data-ttu-id="d6a74-122">Rk \[ n0 + ... + ni + A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="d6a74-122">Rk\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span> | <span data-ttu-id="d6a74-123">A + k + n0 + ... + ni + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="d6a74-123">A + k + n0 + ... + ni + m0 + ... + mj</span></span> | <span data-ttu-id="d6a74-124">c8 \[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span><span class="sxs-lookup"><span data-stu-id="d6a74-124">c8\[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span></span> |
| <span data-ttu-id="d6a74-125">R \[ n0 + ... + ni + A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="d6a74-125">R\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span>  | <span data-ttu-id="d6a74-126">A + n0 + ... + ni + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="d6a74-126">A + n0 + ... + ni + m0 + ... + mj</span></span>     | <span data-ttu-id="d6a74-127">c \[ 2 + 1 + aL + 3 + 4 + 5 \]</span><span class="sxs-lookup"><span data-stu-id="d6a74-127">c\[ 2 + 1 + aL + 3 + 4 + 5 \]</span></span>    |
| <span data-ttu-id="d6a74-128">Rk \[ A \]</span><span class="sxs-lookup"><span data-stu-id="d6a74-128">Rk\[ A \]</span></span>                                 | <span data-ttu-id="d6a74-129">A + k</span><span class="sxs-lookup"><span data-stu-id="d6a74-129">A + k</span></span>                                 | <span data-ttu-id="d6a74-130">c12 \[ aL \] , c0 \[ a0.z \]</span><span class="sxs-lookup"><span data-stu-id="d6a74-130">c12\[ aL \], c0\[ a0.z \]</span></span>        |
| <span data-ttu-id="d6a74-131">Rk \[ A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="d6a74-131">Rk\[ A + m0 + ... + mj \]</span></span>                 | <span data-ttu-id="d6a74-132">A + k + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="d6a74-132">A + k + m0 + ... + mj</span></span>                 | <span data-ttu-id="d6a74-133">v1 \[ aL + 4 + 8 \]</span><span class="sxs-lookup"><span data-stu-id="d6a74-133">v1\[ aL + 4 + 8 \]</span></span>               |
| <span data-ttu-id="d6a74-134">R \[ n0 + ... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="d6a74-134">R\[ n0 + ... + ni + A \]</span></span>                  | <span data-ttu-id="d6a74-135">A + n0 + ... + ni</span><span class="sxs-lookup"><span data-stu-id="d6a74-135">A + n0 + ... + ni</span></span>                     | <span data-ttu-id="d6a74-136">o \[ 3 + 1 + aL \]</span><span class="sxs-lookup"><span data-stu-id="d6a74-136">o\[ 3 + 1 + aL \]</span></span>                |
| <span data-ttu-id="d6a74-137">Rk \[ n0 + ... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="d6a74-137">Rk\[ n0 + ... + ni + A \]</span></span>                 | <span data-ttu-id="d6a74-138">A + k + n0 + ... + ni</span><span class="sxs-lookup"><span data-stu-id="d6a74-138">A + k + n0 + ... + ni</span></span>                 | <span data-ttu-id="d6a74-139">o1 \[ 2 + 1 + 3 + aL \]</span><span class="sxs-lookup"><span data-stu-id="d6a74-139">o1\[ 2 + 1 + 3 + aL \]</span></span>           |



 

<span data-ttu-id="d6a74-140">Die Register sind in den folgenden Versionen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="d6a74-140">The registers are available in the following versions:</span></span>



| <span data-ttu-id="d6a74-141">Registertyp</span><span class="sxs-lookup"><span data-stu-id="d6a74-141">Register type</span></span>                                                                                   | <span data-ttu-id="d6a74-142">Pixel-Shaderversionen</span><span class="sxs-lookup"><span data-stu-id="d6a74-142">Pixel Shader Versions</span></span> |
|-------------------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="d6a74-143">[Schleifenzähler:](dx9-graphics-reference-asm-ps-registers-loop-counter.md)aL für Eingaberegister</span><span class="sxs-lookup"><span data-stu-id="d6a74-143">[loop counter](dx9-graphics-reference-asm-ps-registers-loop-counter.md): aL on input registers</span></span> | <span data-ttu-id="d6a74-144">ps \_ 3 \_ 0 und höher</span><span class="sxs-lookup"><span data-stu-id="d6a74-144">ps\_3\_0 and higher</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="d6a74-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d6a74-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6a74-146">Register</span><span class="sxs-lookup"><span data-stu-id="d6a74-146">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




