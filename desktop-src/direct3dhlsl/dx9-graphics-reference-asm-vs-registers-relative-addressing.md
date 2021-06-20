---
title: Relative Adressierung (HLSL VS-Referenz)
description: Bei Vertex-Shadern kann die Syntax \\ nur in Registertypen verwendet werden, die in bestimmten Shadermodellen relativ adressiert werden können.
ms.assetid: 9f9d2499-73a5-4c9d-9dce-94c914933334
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2bbba694878ba84ac3c2fa9c4e8058bb0d91830e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406693"
---
# <a name="relative-addressing-hlsl-vs-reference"></a><span data-ttu-id="e15e6-103">Relative Adressierung (HLSL VS-Referenz)</span><span class="sxs-lookup"><span data-stu-id="e15e6-103">Relative Addressing (HLSL VS reference)</span></span>

<span data-ttu-id="e15e6-104">Die \[ \] Syntax kann nur in Registertypen verwendet werden, die in bestimmten Shadermodellen relativ adressiert werden können.</span><span class="sxs-lookup"><span data-stu-id="e15e6-104">The \[ \] syntax can be used only in register types that can be relatively addressed in certain shader models.</span></span> <span data-ttu-id="e15e6-105">Die unterstützten \[ \] Syntaxformen sind wie folgt aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="e15e6-105">The supported forms of \[ \] syntax are listed as follows:</span></span>

<span data-ttu-id="e15e6-106">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="e15e6-106">Where:</span></span>

-   <span data-ttu-id="e15e6-107">"R" gibt jeden Registertyp an, der relativ adressiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e15e6-107">"R" denotes any register type that can be relatively addressed.</span></span>
-   <span data-ttu-id="e15e6-108">"A" gibt jedes Register an, das als Index verwendet werden kann, um relativ andere Register zu adressieren.</span><span class="sxs-lookup"><span data-stu-id="e15e6-108">"A" denotes any register that can be used as an index to relatively address other registers.</span></span>
-   <span data-ttu-id="e15e6-109">n0 - ni, m0 - mj und k sind ganze Zahlen >= 0.</span><span class="sxs-lookup"><span data-stu-id="e15e6-109">n0 - ni, m0 - mj, and k are integers >= 0.</span></span>



| <span data-ttu-id="e15e6-110">\[\]Syntax</span><span class="sxs-lookup"><span data-stu-id="e15e6-110">\[ \] syntax</span></span>                              | <span data-ttu-id="e15e6-111">Effektiver Index</span><span class="sxs-lookup"><span data-stu-id="e15e6-111">Effective index</span></span>                       | <span data-ttu-id="e15e6-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e15e6-112">Examples</span></span>                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| <span data-ttu-id="e15e6-113">R \[ A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="e15e6-113">R\[ A + m0 + ... + mj \]</span></span>                  | <span data-ttu-id="e15e6-114">A + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="e15e6-114">A + m0 + ... + mj</span></span>                     | <span data-ttu-id="e15e6-115">c \[ a0.x + 3 + 7 \]</span><span class="sxs-lookup"><span data-stu-id="e15e6-115">c\[ a0.x + 3 + 7 \]</span></span>              |
| <span data-ttu-id="e15e6-116">R \[ k ( = \] Rk )</span><span class="sxs-lookup"><span data-stu-id="e15e6-116">R\[ k \] ( = Rk )</span></span>                         | <span data-ttu-id="e15e6-117">k</span><span class="sxs-lookup"><span data-stu-id="e15e6-117">k</span></span>                                     | <span data-ttu-id="e15e6-118">c \[ 10 \] ( = c10 )</span><span class="sxs-lookup"><span data-stu-id="e15e6-118">c\[ 10 \] ( = c10 )</span></span>              |
| <span data-ttu-id="e15e6-119">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="e15e6-119">R\[ A \]</span></span>                                  | <span data-ttu-id="e15e6-120">Ein</span><span class="sxs-lookup"><span data-stu-id="e15e6-120">A</span></span>                                     | <span data-ttu-id="e15e6-121">c \[ a0.y \]</span><span class="sxs-lookup"><span data-stu-id="e15e6-121">c\[ a0.y \]</span></span>                      |
| <span data-ttu-id="e15e6-122">Rk \[ n0 + ... + ni + A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="e15e6-122">Rk\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span> | <span data-ttu-id="e15e6-123">A + k + n0 + ... + ni + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="e15e6-123">A + k + n0 + ... + ni + m0 + ... + mj</span></span> | <span data-ttu-id="e15e6-124">c8 \[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span><span class="sxs-lookup"><span data-stu-id="e15e6-124">c8\[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span></span> |
| <span data-ttu-id="e15e6-125">R \[ n0 + ... + ni + A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="e15e6-125">R\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span>  | <span data-ttu-id="e15e6-126">A + n0 + ... + ni + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="e15e6-126">A + n0 + ... + ni + m0 + ... + mj</span></span>     | <span data-ttu-id="e15e6-127">c \[ 2 + 1 + aL + 3 + 4 + 5 \]</span><span class="sxs-lookup"><span data-stu-id="e15e6-127">c\[ 2 + 1 + aL + 3 + 4 + 5 \]</span></span>    |
| <span data-ttu-id="e15e6-128">Rk \[ A \]</span><span class="sxs-lookup"><span data-stu-id="e15e6-128">Rk\[ A \]</span></span>                                 | <span data-ttu-id="e15e6-129">A + k</span><span class="sxs-lookup"><span data-stu-id="e15e6-129">A + k</span></span>                                 | <span data-ttu-id="e15e6-130">c12 \[ aL \] , c0 \[ a0.z \]</span><span class="sxs-lookup"><span data-stu-id="e15e6-130">c12\[ aL \], c0\[ a0.z \]</span></span>        |
| <span data-ttu-id="e15e6-131">Rk \[ A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="e15e6-131">Rk\[ A + m0 + ... + mj \]</span></span>                 | <span data-ttu-id="e15e6-132">A + k + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="e15e6-132">A + k + m0 + ... + mj</span></span>                 | <span data-ttu-id="e15e6-133">v1 \[ aL + 4 + 8 \]</span><span class="sxs-lookup"><span data-stu-id="e15e6-133">v1\[ aL + 4 + 8 \]</span></span>               |
| <span data-ttu-id="e15e6-134">R \[ n0 + ... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="e15e6-134">R\[ n0 + ... + ni + A \]</span></span>                  | <span data-ttu-id="e15e6-135">A + n0 + ... + ni</span><span class="sxs-lookup"><span data-stu-id="e15e6-135">A + n0 + ... + ni</span></span>                     | <span data-ttu-id="e15e6-136">o \[ 3 + 1 + aL \]</span><span class="sxs-lookup"><span data-stu-id="e15e6-136">o\[ 3 + 1 + aL \]</span></span>                |
| <span data-ttu-id="e15e6-137">Rk \[ n0 + ... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="e15e6-137">Rk\[ n0 + ... + ni + A \]</span></span>                 | <span data-ttu-id="e15e6-138">A + k + n0 + ... + ni</span><span class="sxs-lookup"><span data-stu-id="e15e6-138">A + k + n0 + ... + ni</span></span>                 | <span data-ttu-id="e15e6-139">o1 \[ 2 + 1 + 3 + aL \]</span><span class="sxs-lookup"><span data-stu-id="e15e6-139">o1\[ 2 + 1 + 3 + aL \]</span></span>           |



 

<span data-ttu-id="e15e6-140">Die Register sind in den folgenden Versionen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="e15e6-140">The registers are available in the following versions:</span></span>



| <span data-ttu-id="e15e6-141">Registertyp</span><span class="sxs-lookup"><span data-stu-id="e15e6-141">Register type</span></span> | <span data-ttu-id="e15e6-142">Vertex-Shaderversionen</span><span class="sxs-lookup"><span data-stu-id="e15e6-142">Vertex Shader Versions</span></span> |
|---------------|------------------------|
| <span data-ttu-id="e15e6-143">a0</span><span class="sxs-lookup"><span data-stu-id="e15e6-143">a0</span></span>            | <span data-ttu-id="e15e6-144">Alle</span><span class="sxs-lookup"><span data-stu-id="e15e6-144">All</span></span>                    |
| <span data-ttu-id="e15e6-145">Al</span><span class="sxs-lookup"><span data-stu-id="e15e6-145">aL</span></span>            | <span data-ttu-id="e15e6-146">Im Vergleich \_ zu \_ 2 0 und höher</span><span class="sxs-lookup"><span data-stu-id="e15e6-146">vs\_2\_0 and higher</span></span>    |
| <span data-ttu-id="e15e6-147">cn</span><span class="sxs-lookup"><span data-stu-id="e15e6-147">cn</span></span>            | <span data-ttu-id="e15e6-148">Im Vergleich zu \_ \_ 1 1 und höher</span><span class="sxs-lookup"><span data-stu-id="e15e6-148">vs\_1\_1 and higher</span></span>    |
| <span data-ttu-id="e15e6-149">on</span><span class="sxs-lookup"><span data-stu-id="e15e6-149">on</span></span>            | <span data-ttu-id="e15e6-150">Vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e15e6-150">vs\_3\_0</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="e15e6-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e15e6-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e15e6-152">Vertex-Shaderregister</span><span class="sxs-lookup"><span data-stu-id="e15e6-152">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




