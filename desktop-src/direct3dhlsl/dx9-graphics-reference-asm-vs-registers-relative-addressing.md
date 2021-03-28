---
title: Relative Adressierung (HLSL vs-Referenz)
description: Die Syntax \ \ kann nur in Registrierungs Typen verwendet werden, die in bestimmten shadermodellen relativ adressiert werden können.
ms.assetid: 9f9d2499-73a5-4c9d-9dce-94c914933334
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c11d6f6c4b448e1dee5f4237696c110519bc0dd0
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104313787"
---
# <a name="relative-addressing-hlsl-vs-reference"></a><span data-ttu-id="2c090-103">Relative Adressierung (HLSL vs-Referenz)</span><span class="sxs-lookup"><span data-stu-id="2c090-103">Relative Addressing (HLSL VS reference)</span></span>

<span data-ttu-id="2c090-104">Die \[ \] Syntax kann nur in Registrierungs Typen verwendet werden, die in bestimmten shadermodellen relativ adressiert werden können.</span><span class="sxs-lookup"><span data-stu-id="2c090-104">The \[ \] syntax can be used only in register types that can be relatively addressed in certain shader models.</span></span> <span data-ttu-id="2c090-105">Die unterstützten \[ \] Syntax Formen werden wie folgt aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="2c090-105">The supported forms of \[ \] syntax are listed as follows:</span></span>

<span data-ttu-id="2c090-106">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="2c090-106">Where:</span></span>

-   <span data-ttu-id="2c090-107">"R" bezeichnet jeden registriungstyp, der relativ adressiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="2c090-107">"R" denotes any register type that can be relatively addressed.</span></span>
-   <span data-ttu-id="2c090-108">"A" bezeichnet jedes Register, das als Index verwendet werden kann, um andere Register relativ zu adressieren.</span><span class="sxs-lookup"><span data-stu-id="2c090-108">"A" denotes any register that can be used as an index to relatively address other registers.</span></span>
-   <span data-ttu-id="2c090-109">N0-NI, M0-MJ und k sind ganze Zahlen >= 0.</span><span class="sxs-lookup"><span data-stu-id="2c090-109">n0 - ni, m0 - mj, and k are integers >= 0.</span></span>



| <span data-ttu-id="2c090-110">\[\]Syntax</span><span class="sxs-lookup"><span data-stu-id="2c090-110">\[ \] syntax</span></span>                              | <span data-ttu-id="2c090-111">Effektiver Index</span><span class="sxs-lookup"><span data-stu-id="2c090-111">Effective index</span></span>                       | <span data-ttu-id="2c090-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c090-112">Examples</span></span>                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| <span data-ttu-id="2c090-113">R \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="2c090-113">R\[ A + m0 + ... + mj \]</span></span>                  | <span data-ttu-id="2c090-114">A + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="2c090-114">A + m0 + ... + mj</span></span>                     | <span data-ttu-id="2c090-115">c \[ a0. x + 3 + 7 \]</span><span class="sxs-lookup"><span data-stu-id="2c090-115">c\[ a0.x + 3 + 7 \]</span></span>              |
| <span data-ttu-id="2c090-116">R \[ k \] (= RK)</span><span class="sxs-lookup"><span data-stu-id="2c090-116">R\[ k \] ( = Rk )</span></span>                         | <span data-ttu-id="2c090-117">k</span><span class="sxs-lookup"><span data-stu-id="2c090-117">k</span></span>                                     | <span data-ttu-id="2c090-118">c \[ 10 \] (= C10)</span><span class="sxs-lookup"><span data-stu-id="2c090-118">c\[ 10 \] ( = c10 )</span></span>              |
| <span data-ttu-id="2c090-119">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="2c090-119">R\[ A \]</span></span>                                  | <span data-ttu-id="2c090-120">Ein</span><span class="sxs-lookup"><span data-stu-id="2c090-120">A</span></span>                                     | <span data-ttu-id="2c090-121">c \[ a0. y \]</span><span class="sxs-lookup"><span data-stu-id="2c090-121">c\[ a0.y \]</span></span>                      |
| <span data-ttu-id="2c090-122">RK \[ N0 +... + NI + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="2c090-122">Rk\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span> | <span data-ttu-id="2c090-123">A + k + N0 +... + NI + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="2c090-123">A + k + n0 + ... + ni + m0 + ... + mj</span></span> | <span data-ttu-id="2c090-124">C8 \[ 3 + 2 + a0. w + 5 + 6 + 1 \]</span><span class="sxs-lookup"><span data-stu-id="2c090-124">c8\[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span></span> |
| <span data-ttu-id="2c090-125">R \[ N0 +... + NI + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="2c090-125">R\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span>  | <span data-ttu-id="2c090-126">A + N0 +... + NI + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="2c090-126">A + n0 + ... + ni + m0 + ... + mj</span></span>     | <span data-ttu-id="2c090-127">c \[ 2 + 1 + Al + 3 + 4 + 5 \]</span><span class="sxs-lookup"><span data-stu-id="2c090-127">c\[ 2 + 1 + aL + 3 + 4 + 5 \]</span></span>    |
| <span data-ttu-id="2c090-128">RK \[ A \]</span><span class="sxs-lookup"><span data-stu-id="2c090-128">Rk\[ A \]</span></span>                                 | <span data-ttu-id="2c090-129">A + k</span><span class="sxs-lookup"><span data-stu-id="2c090-129">A + k</span></span>                                 | <span data-ttu-id="2c090-130">C12 \[ Al \] , C0 \[ a0. z \]</span><span class="sxs-lookup"><span data-stu-id="2c090-130">c12\[ aL \], c0\[ a0.z \]</span></span>        |
| <span data-ttu-id="2c090-131">RK \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="2c090-131">Rk\[ A + m0 + ... + mj \]</span></span>                 | <span data-ttu-id="2c090-132">A + k + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="2c090-132">A + k + m0 + ... + mj</span></span>                 | <span data-ttu-id="2c090-133">v1 \[ Al + 4 + 8 \]</span><span class="sxs-lookup"><span data-stu-id="2c090-133">v1\[ aL + 4 + 8 \]</span></span>               |
| <span data-ttu-id="2c090-134">R \[ N0 +... + NI + A \]</span><span class="sxs-lookup"><span data-stu-id="2c090-134">R\[ n0 + ... + ni + A \]</span></span>                  | <span data-ttu-id="2c090-135">A + N0 +... + NI</span><span class="sxs-lookup"><span data-stu-id="2c090-135">A + n0 + ... + ni</span></span>                     | <span data-ttu-id="2c090-136">o \[ 3 + 1 + Al \]</span><span class="sxs-lookup"><span data-stu-id="2c090-136">o\[ 3 + 1 + aL \]</span></span>                |
| <span data-ttu-id="2c090-137">RK \[ N0 +... + NI + A \]</span><span class="sxs-lookup"><span data-stu-id="2c090-137">Rk\[ n0 + ... + ni + A \]</span></span>                 | <span data-ttu-id="2c090-138">A + k + N0 +... + NI</span><span class="sxs-lookup"><span data-stu-id="2c090-138">A + k + n0 + ... + ni</span></span>                 | <span data-ttu-id="2c090-139">o1 \[ 2 + 1 + 3 + Al \]</span><span class="sxs-lookup"><span data-stu-id="2c090-139">o1\[ 2 + 1 + 3 + aL \]</span></span>           |



 

<span data-ttu-id="2c090-140">Die Register sind in den folgenden Versionen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="2c090-140">The registers are available in the following versions:</span></span>



| <span data-ttu-id="2c090-141">Registriungstyp</span><span class="sxs-lookup"><span data-stu-id="2c090-141">Register type</span></span> | <span data-ttu-id="2c090-142">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="2c090-142">Vertex Shader Versions</span></span> |
|---------------|------------------------|
| <span data-ttu-id="2c090-143">a0</span><span class="sxs-lookup"><span data-stu-id="2c090-143">a0</span></span>            | <span data-ttu-id="2c090-144">All</span><span class="sxs-lookup"><span data-stu-id="2c090-144">All</span></span>                    |
| <span data-ttu-id="2c090-145">irdische</span><span class="sxs-lookup"><span data-stu-id="2c090-145">aL</span></span>            | <span data-ttu-id="2c090-146">vs \_ 2 \_ 0 und höher</span><span class="sxs-lookup"><span data-stu-id="2c090-146">vs\_2\_0 and higher</span></span>    |
| <span data-ttu-id="2c090-147">cn</span><span class="sxs-lookup"><span data-stu-id="2c090-147">cn</span></span>            | <span data-ttu-id="2c090-148">vs \_ 1 \_ 1 und höher</span><span class="sxs-lookup"><span data-stu-id="2c090-148">vs\_1\_1 and higher</span></span>    |
| <span data-ttu-id="2c090-149">on</span><span class="sxs-lookup"><span data-stu-id="2c090-149">on</span></span>            | <span data-ttu-id="2c090-150">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2c090-150">vs\_3\_0</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="2c090-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2c090-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c090-152">Vertex-Shader-Register</span><span class="sxs-lookup"><span data-stu-id="2c090-152">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




