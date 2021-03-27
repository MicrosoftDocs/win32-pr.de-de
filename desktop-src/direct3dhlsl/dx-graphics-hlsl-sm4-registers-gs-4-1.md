---
title: Register-gs_4_1
description: Dieser Abschnitt enthält Referenzinformationen zu den Eingabe-und Ausgabe Registern, die von den Geometry-Shader-Versionen 4 \_ 0 und 4 1 implementiert werden \_ .
ms.assetid: 0312707D-11D0-45D0-9E8C-8BD2BC65352C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a01f200bd4183843b1cfd2892fde5da442ca8d36
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206945"
---
# <a name="registers---gs_4_1"></a><span data-ttu-id="60a06-103">Register-GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="60a06-103">Registers - gs\_4\_1</span></span>

<span data-ttu-id="60a06-104">Dieser Abschnitt enthält Referenzinformationen zu den Eingabe-und Ausgabe Registern, die von den Geometry-Shader-Versionen 4 \_ 0 und 4 1 implementiert werden \_ .</span><span class="sxs-lookup"><span data-stu-id="60a06-104">This section contains reference information for the input and output registers implemented by geometry shader versions 4\_0 and 4\_1.</span></span>

## <a name="input-registers"></a><span data-ttu-id="60a06-105">Eingabe Register</span><span class="sxs-lookup"><span data-stu-id="60a06-105">Input Registers</span></span>



| <span data-ttu-id="60a06-106">Register</span><span class="sxs-lookup"><span data-stu-id="60a06-106">Register</span></span>                 | <span data-ttu-id="60a06-107">Name</span><span class="sxs-lookup"><span data-stu-id="60a06-107">Name</span></span> | <span data-ttu-id="60a06-108">Anzahl</span><span class="sxs-lookup"><span data-stu-id="60a06-108">Count</span></span>              | <span data-ttu-id="60a06-109">R/W</span><span class="sxs-lookup"><span data-stu-id="60a06-109">R/W</span></span> | <span data-ttu-id="60a06-110">Dimension</span><span class="sxs-lookup"><span data-stu-id="60a06-110">Dimension</span></span>        | <span data-ttu-id="60a06-111">Indizierbar durch r\#</span><span class="sxs-lookup"><span data-stu-id="60a06-111">Indexable by r\#</span></span> | <span data-ttu-id="60a06-112">der Arbeitszeittabelle</span><span class="sxs-lookup"><span data-stu-id="60a06-112">Defaults</span></span> | <span data-ttu-id="60a06-113">Erfordert DCL</span><span class="sxs-lookup"><span data-stu-id="60a06-113">Requires DCL</span></span> |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| <span data-ttu-id="60a06-114">r\#</span><span class="sxs-lookup"><span data-stu-id="60a06-114">r\#</span></span>                      |      | <span data-ttu-id="60a06-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="60a06-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="60a06-116">R/W</span><span class="sxs-lookup"><span data-stu-id="60a06-116">R/W</span></span> | <span data-ttu-id="60a06-117">4</span><span class="sxs-lookup"><span data-stu-id="60a06-117">4</span></span>                | <span data-ttu-id="60a06-118">Nein</span><span class="sxs-lookup"><span data-stu-id="60a06-118">No</span></span>               | <span data-ttu-id="60a06-119">Keine</span><span class="sxs-lookup"><span data-stu-id="60a06-119">None</span></span>     | <span data-ttu-id="60a06-120">Ja</span><span class="sxs-lookup"><span data-stu-id="60a06-120">Yes</span></span>          |
| <span data-ttu-id="60a06-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="60a06-121">x\#\[n\]</span></span>                 |      | <span data-ttu-id="60a06-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="60a06-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="60a06-123">R/W</span><span class="sxs-lookup"><span data-stu-id="60a06-123">R/W</span></span> | <span data-ttu-id="60a06-124">4</span><span class="sxs-lookup"><span data-stu-id="60a06-124">4</span></span>                | <span data-ttu-id="60a06-125">Ja</span><span class="sxs-lookup"><span data-stu-id="60a06-125">Yes</span></span>              | <span data-ttu-id="60a06-126">Keine</span><span class="sxs-lookup"><span data-stu-id="60a06-126">None</span></span>     | <span data-ttu-id="60a06-127">Ja</span><span class="sxs-lookup"><span data-stu-id="60a06-127">Yes</span></span>          |
| <span data-ttu-id="60a06-128">v- \# \[ Vertex- \] \[ Element\]</span><span class="sxs-lookup"><span data-stu-id="60a06-128">v\#\[vertex\]\[element\]</span></span> |      | <span data-ttu-id="60a06-129">32</span><span class="sxs-lookup"><span data-stu-id="60a06-129">32</span></span>                 | <span data-ttu-id="60a06-130">R</span><span class="sxs-lookup"><span data-stu-id="60a06-130">R</span></span>   | <span data-ttu-id="60a06-131">4 (Comp) \* 6 (Vert)</span><span class="sxs-lookup"><span data-stu-id="60a06-131">4(comp)\*6(vert)</span></span> | <span data-ttu-id="60a06-132">Ja</span><span class="sxs-lookup"><span data-stu-id="60a06-132">Yes</span></span>              | <span data-ttu-id="60a06-133">Keine</span><span class="sxs-lookup"><span data-stu-id="60a06-133">None</span></span>     | <span data-ttu-id="60a06-134">Ja</span><span class="sxs-lookup"><span data-stu-id="60a06-134">Yes</span></span>          |
| <span data-ttu-id="60a06-135">vprim</span><span class="sxs-lookup"><span data-stu-id="60a06-135">vprim</span></span>                    |      | <span data-ttu-id="60a06-136">1</span><span class="sxs-lookup"><span data-stu-id="60a06-136">1</span></span>                  | <span data-ttu-id="60a06-137">R</span><span class="sxs-lookup"><span data-stu-id="60a06-137">R</span></span>   | <span data-ttu-id="60a06-138">1</span><span class="sxs-lookup"><span data-stu-id="60a06-138">1</span></span>                | <span data-ttu-id="60a06-139">Nein</span><span class="sxs-lookup"><span data-stu-id="60a06-139">No</span></span>               | <span data-ttu-id="60a06-140">Keine</span><span class="sxs-lookup"><span data-stu-id="60a06-140">None</span></span>     | <span data-ttu-id="60a06-141">Ja</span><span class="sxs-lookup"><span data-stu-id="60a06-141">Yes</span></span>          |
| <span data-ttu-id="60a06-142">t\#</span><span class="sxs-lookup"><span data-stu-id="60a06-142">t\#</span></span>                      |      | <span data-ttu-id="60a06-143">128</span><span class="sxs-lookup"><span data-stu-id="60a06-143">128</span></span>                | <span data-ttu-id="60a06-144">R</span><span class="sxs-lookup"><span data-stu-id="60a06-144">R</span></span>   | <span data-ttu-id="60a06-145">1</span><span class="sxs-lookup"><span data-stu-id="60a06-145">1</span></span>                | <span data-ttu-id="60a06-146">Nein</span><span class="sxs-lookup"><span data-stu-id="60a06-146">No</span></span>               | <span data-ttu-id="60a06-147">Keine</span><span class="sxs-lookup"><span data-stu-id="60a06-147">None</span></span>     | <span data-ttu-id="60a06-148">Ja</span><span class="sxs-lookup"><span data-stu-id="60a06-148">Yes</span></span>          |
| <span data-ttu-id="60a06-149">s\#</span><span class="sxs-lookup"><span data-stu-id="60a06-149">s\#</span></span>                      |      | <span data-ttu-id="60a06-150">16</span><span class="sxs-lookup"><span data-stu-id="60a06-150">16</span></span>                 | <span data-ttu-id="60a06-151">R</span><span class="sxs-lookup"><span data-stu-id="60a06-151">R</span></span>   | <span data-ttu-id="60a06-152">1</span><span class="sxs-lookup"><span data-stu-id="60a06-152">1</span></span>                | <span data-ttu-id="60a06-153">Nein</span><span class="sxs-lookup"><span data-stu-id="60a06-153">No</span></span>               | <span data-ttu-id="60a06-154">Keine</span><span class="sxs-lookup"><span data-stu-id="60a06-154">None</span></span>     | <span data-ttu-id="60a06-155">Ja</span><span class="sxs-lookup"><span data-stu-id="60a06-155">Yes</span></span>          |
| <span data-ttu-id="60a06-156">CB- \# \[ Index\]</span><span class="sxs-lookup"><span data-stu-id="60a06-156">cb\#\[index\]</span></span>            |      | <span data-ttu-id="60a06-157">15</span><span class="sxs-lookup"><span data-stu-id="60a06-157">15</span></span>                 | <span data-ttu-id="60a06-158">R</span><span class="sxs-lookup"><span data-stu-id="60a06-158">R</span></span>   | <span data-ttu-id="60a06-159">4</span><span class="sxs-lookup"><span data-stu-id="60a06-159">4</span></span>                | <span data-ttu-id="60a06-160">Ja (Inhalt)</span><span class="sxs-lookup"><span data-stu-id="60a06-160">Yes(Contents)</span></span>    | <span data-ttu-id="60a06-161">Keine</span><span class="sxs-lookup"><span data-stu-id="60a06-161">None</span></span>     | <span data-ttu-id="60a06-162">Ja</span><span class="sxs-lookup"><span data-stu-id="60a06-162">Yes</span></span>          |
| <span data-ttu-id="60a06-163">ICB- \[ Index\]</span><span class="sxs-lookup"><span data-stu-id="60a06-163">icb\[index\]</span></span>             |      | <span data-ttu-id="60a06-164">1</span><span class="sxs-lookup"><span data-stu-id="60a06-164">1</span></span>                  | <span data-ttu-id="60a06-165">R</span><span class="sxs-lookup"><span data-stu-id="60a06-165">R</span></span>   | <span data-ttu-id="60a06-166">4</span><span class="sxs-lookup"><span data-stu-id="60a06-166">4</span></span>                | <span data-ttu-id="60a06-167">Ja (Inhalt)</span><span class="sxs-lookup"><span data-stu-id="60a06-167">Yes(Contents)</span></span>    | <span data-ttu-id="60a06-168">Keine</span><span class="sxs-lookup"><span data-stu-id="60a06-168">None</span></span>     | <span data-ttu-id="60a06-169">Ja</span><span class="sxs-lookup"><span data-stu-id="60a06-169">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="60a06-170">Ausgabe Register</span><span class="sxs-lookup"><span data-stu-id="60a06-170">Output Registers</span></span>



| <span data-ttu-id="60a06-171">Register</span><span class="sxs-lookup"><span data-stu-id="60a06-171">Register</span></span> | <span data-ttu-id="60a06-172">Name</span><span class="sxs-lookup"><span data-stu-id="60a06-172">Name</span></span>            | <span data-ttu-id="60a06-173">Anzahl</span><span class="sxs-lookup"><span data-stu-id="60a06-173">Count</span></span> | <span data-ttu-id="60a06-174">R/W</span><span class="sxs-lookup"><span data-stu-id="60a06-174">R/W</span></span> | <span data-ttu-id="60a06-175">Dimension</span><span class="sxs-lookup"><span data-stu-id="60a06-175">Dimension</span></span> | <span data-ttu-id="60a06-176">Indizierbar durch r\#</span><span class="sxs-lookup"><span data-stu-id="60a06-176">Indexable by r\#</span></span> | <span data-ttu-id="60a06-177">der Arbeitszeittabelle</span><span class="sxs-lookup"><span data-stu-id="60a06-177">Defaults</span></span> | <span data-ttu-id="60a06-178">Erfordert DCL</span><span class="sxs-lookup"><span data-stu-id="60a06-178">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="60a06-179">NULL</span><span class="sxs-lookup"><span data-stu-id="60a06-179">NULL</span></span>     | <span data-ttu-id="60a06-180">Ergebnis verwerfen</span><span class="sxs-lookup"><span data-stu-id="60a06-180">Discard Result</span></span>  | <span data-ttu-id="60a06-181">–</span><span class="sxs-lookup"><span data-stu-id="60a06-181">N/A</span></span>   | <span data-ttu-id="60a06-182">W</span><span class="sxs-lookup"><span data-stu-id="60a06-182">W</span></span>   | <span data-ttu-id="60a06-183">–</span><span class="sxs-lookup"><span data-stu-id="60a06-183">N/A</span></span>       | <span data-ttu-id="60a06-184">–</span><span class="sxs-lookup"><span data-stu-id="60a06-184">N/A</span></span>              | <span data-ttu-id="60a06-185">–</span><span class="sxs-lookup"><span data-stu-id="60a06-185">N/A</span></span>      | <span data-ttu-id="60a06-186">Nein</span><span class="sxs-lookup"><span data-stu-id="60a06-186">No</span></span>           |
| <span data-ttu-id="60a06-187">o\#</span><span class="sxs-lookup"><span data-stu-id="60a06-187">o\#</span></span>      | <span data-ttu-id="60a06-188">Ausgabe Register</span><span class="sxs-lookup"><span data-stu-id="60a06-188">Output Register</span></span> | <span data-ttu-id="60a06-189">32</span><span class="sxs-lookup"><span data-stu-id="60a06-189">32</span></span>    | <span data-ttu-id="60a06-190">W</span><span class="sxs-lookup"><span data-stu-id="60a06-190">W</span></span>   | <span data-ttu-id="60a06-191">–</span><span class="sxs-lookup"><span data-stu-id="60a06-191">N/A</span></span>       | <span data-ttu-id="60a06-192">N/V</span><span class="sxs-lookup"><span data-stu-id="60a06-192">N/A</span></span>              | <span data-ttu-id="60a06-193">4</span><span class="sxs-lookup"><span data-stu-id="60a06-193">4</span></span>        | <span data-ttu-id="60a06-194">Ja</span><span class="sxs-lookup"><span data-stu-id="60a06-194">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="60a06-195">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="60a06-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60a06-196">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="60a06-196">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




