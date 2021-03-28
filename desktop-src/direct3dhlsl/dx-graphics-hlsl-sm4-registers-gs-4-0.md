---
title: Register-gs_4_0
description: Dieser Abschnitt enthält Referenzinformationen zu den Eingabe-und Ausgabe Registern, die von Geometry-Shader Version 4 0 implementiert werden \_ .
ms.assetid: 1f3ebd71-19de-4e26-87f0-4fb5c8e2a343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c5db86ffb797434af4badd6496b71a4ad684583
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515812"
---
# <a name="registers---gs_4_0"></a><span data-ttu-id="1e40f-103">Register-GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1e40f-103">Registers - gs\_4\_0</span></span>

<span data-ttu-id="1e40f-104">Dieser Abschnitt enthält Referenzinformationen zu den Eingabe-und Ausgabe Registern, die von Geometry-Shader Version 4 0 implementiert werden \_ .</span><span class="sxs-lookup"><span data-stu-id="1e40f-104">This section contains reference information for the input and output registers implemented by geometry shader version 4\_0.</span></span>

## <a name="input-registers"></a><span data-ttu-id="1e40f-105">Eingabe Register</span><span class="sxs-lookup"><span data-stu-id="1e40f-105">Input Registers</span></span>



| <span data-ttu-id="1e40f-106">Register</span><span class="sxs-lookup"><span data-stu-id="1e40f-106">Register</span></span>                 | <span data-ttu-id="1e40f-107">Name</span><span class="sxs-lookup"><span data-stu-id="1e40f-107">Name</span></span> | <span data-ttu-id="1e40f-108">Anzahl</span><span class="sxs-lookup"><span data-stu-id="1e40f-108">Count</span></span>              | <span data-ttu-id="1e40f-109">R/W</span><span class="sxs-lookup"><span data-stu-id="1e40f-109">R/W</span></span> | <span data-ttu-id="1e40f-110">Dimension</span><span class="sxs-lookup"><span data-stu-id="1e40f-110">Dimension</span></span>        | <span data-ttu-id="1e40f-111">Indizierbar durch r\#</span><span class="sxs-lookup"><span data-stu-id="1e40f-111">Indexable by r\#</span></span> | <span data-ttu-id="1e40f-112">der Arbeitszeittabelle</span><span class="sxs-lookup"><span data-stu-id="1e40f-112">Defaults</span></span> | <span data-ttu-id="1e40f-113">Erfordert DCL</span><span class="sxs-lookup"><span data-stu-id="1e40f-113">Requires DCL</span></span> |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| <span data-ttu-id="1e40f-114">r\#</span><span class="sxs-lookup"><span data-stu-id="1e40f-114">r\#</span></span>                      |      | <span data-ttu-id="1e40f-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="1e40f-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="1e40f-116">R/W</span><span class="sxs-lookup"><span data-stu-id="1e40f-116">R/W</span></span> | <span data-ttu-id="1e40f-117">4</span><span class="sxs-lookup"><span data-stu-id="1e40f-117">4</span></span>                | <span data-ttu-id="1e40f-118">Nein</span><span class="sxs-lookup"><span data-stu-id="1e40f-118">No</span></span>               | <span data-ttu-id="1e40f-119">Keine</span><span class="sxs-lookup"><span data-stu-id="1e40f-119">None</span></span>     | <span data-ttu-id="1e40f-120">Ja</span><span class="sxs-lookup"><span data-stu-id="1e40f-120">Yes</span></span>          |
| <span data-ttu-id="1e40f-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="1e40f-121">x\#\[n\]</span></span>                 |      | <span data-ttu-id="1e40f-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="1e40f-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="1e40f-123">R/W</span><span class="sxs-lookup"><span data-stu-id="1e40f-123">R/W</span></span> | <span data-ttu-id="1e40f-124">4</span><span class="sxs-lookup"><span data-stu-id="1e40f-124">4</span></span>                | <span data-ttu-id="1e40f-125">Ja</span><span class="sxs-lookup"><span data-stu-id="1e40f-125">Yes</span></span>              | <span data-ttu-id="1e40f-126">Keine</span><span class="sxs-lookup"><span data-stu-id="1e40f-126">None</span></span>     | <span data-ttu-id="1e40f-127">Ja</span><span class="sxs-lookup"><span data-stu-id="1e40f-127">Yes</span></span>          |
| <span data-ttu-id="1e40f-128">v- \# \[ Vertex- \] \[ Element\]</span><span class="sxs-lookup"><span data-stu-id="1e40f-128">v\#\[vertex\]\[element\]</span></span> |      | <span data-ttu-id="1e40f-129">32</span><span class="sxs-lookup"><span data-stu-id="1e40f-129">32</span></span>                 | <span data-ttu-id="1e40f-130">R</span><span class="sxs-lookup"><span data-stu-id="1e40f-130">R</span></span>   | <span data-ttu-id="1e40f-131">4 (Comp) \* 6 (Vert)</span><span class="sxs-lookup"><span data-stu-id="1e40f-131">4(comp)\*6(vert)</span></span> | <span data-ttu-id="1e40f-132">Ja</span><span class="sxs-lookup"><span data-stu-id="1e40f-132">Yes</span></span>              | <span data-ttu-id="1e40f-133">Keine</span><span class="sxs-lookup"><span data-stu-id="1e40f-133">None</span></span>     | <span data-ttu-id="1e40f-134">Ja</span><span class="sxs-lookup"><span data-stu-id="1e40f-134">Yes</span></span>          |
| <span data-ttu-id="1e40f-135">vprim</span><span class="sxs-lookup"><span data-stu-id="1e40f-135">vprim</span></span>                    |      | <span data-ttu-id="1e40f-136">1</span><span class="sxs-lookup"><span data-stu-id="1e40f-136">1</span></span>                  | <span data-ttu-id="1e40f-137">R</span><span class="sxs-lookup"><span data-stu-id="1e40f-137">R</span></span>   | <span data-ttu-id="1e40f-138">1</span><span class="sxs-lookup"><span data-stu-id="1e40f-138">1</span></span>                | <span data-ttu-id="1e40f-139">Nein</span><span class="sxs-lookup"><span data-stu-id="1e40f-139">No</span></span>               | <span data-ttu-id="1e40f-140">Keine</span><span class="sxs-lookup"><span data-stu-id="1e40f-140">None</span></span>     | <span data-ttu-id="1e40f-141">Ja</span><span class="sxs-lookup"><span data-stu-id="1e40f-141">Yes</span></span>          |
| <span data-ttu-id="1e40f-142">t\#</span><span class="sxs-lookup"><span data-stu-id="1e40f-142">t\#</span></span>                      |      | <span data-ttu-id="1e40f-143">128</span><span class="sxs-lookup"><span data-stu-id="1e40f-143">128</span></span>                | <span data-ttu-id="1e40f-144">R</span><span class="sxs-lookup"><span data-stu-id="1e40f-144">R</span></span>   | <span data-ttu-id="1e40f-145">1</span><span class="sxs-lookup"><span data-stu-id="1e40f-145">1</span></span>                | <span data-ttu-id="1e40f-146">Nein</span><span class="sxs-lookup"><span data-stu-id="1e40f-146">No</span></span>               | <span data-ttu-id="1e40f-147">Keine</span><span class="sxs-lookup"><span data-stu-id="1e40f-147">None</span></span>     | <span data-ttu-id="1e40f-148">Ja</span><span class="sxs-lookup"><span data-stu-id="1e40f-148">Yes</span></span>          |
| <span data-ttu-id="1e40f-149">s\#</span><span class="sxs-lookup"><span data-stu-id="1e40f-149">s\#</span></span>                      |      | <span data-ttu-id="1e40f-150">16</span><span class="sxs-lookup"><span data-stu-id="1e40f-150">16</span></span>                 | <span data-ttu-id="1e40f-151">R</span><span class="sxs-lookup"><span data-stu-id="1e40f-151">R</span></span>   | <span data-ttu-id="1e40f-152">1</span><span class="sxs-lookup"><span data-stu-id="1e40f-152">1</span></span>                | <span data-ttu-id="1e40f-153">Nein</span><span class="sxs-lookup"><span data-stu-id="1e40f-153">No</span></span>               | <span data-ttu-id="1e40f-154">Keine</span><span class="sxs-lookup"><span data-stu-id="1e40f-154">None</span></span>     | <span data-ttu-id="1e40f-155">Ja</span><span class="sxs-lookup"><span data-stu-id="1e40f-155">Yes</span></span>          |
| <span data-ttu-id="1e40f-156">CB- \# \[ Index\]</span><span class="sxs-lookup"><span data-stu-id="1e40f-156">cb\#\[index\]</span></span>            |      | <span data-ttu-id="1e40f-157">15</span><span class="sxs-lookup"><span data-stu-id="1e40f-157">15</span></span>                 | <span data-ttu-id="1e40f-158">R</span><span class="sxs-lookup"><span data-stu-id="1e40f-158">R</span></span>   | <span data-ttu-id="1e40f-159">4</span><span class="sxs-lookup"><span data-stu-id="1e40f-159">4</span></span>                | <span data-ttu-id="1e40f-160">Ja (Inhalt)</span><span class="sxs-lookup"><span data-stu-id="1e40f-160">Yes(Contents)</span></span>    | <span data-ttu-id="1e40f-161">Keine</span><span class="sxs-lookup"><span data-stu-id="1e40f-161">None</span></span>     | <span data-ttu-id="1e40f-162">Ja</span><span class="sxs-lookup"><span data-stu-id="1e40f-162">Yes</span></span>          |
| <span data-ttu-id="1e40f-163">ICB- \[ Index\]</span><span class="sxs-lookup"><span data-stu-id="1e40f-163">icb\[index\]</span></span>             |      | <span data-ttu-id="1e40f-164">1</span><span class="sxs-lookup"><span data-stu-id="1e40f-164">1</span></span>                  | <span data-ttu-id="1e40f-165">R</span><span class="sxs-lookup"><span data-stu-id="1e40f-165">R</span></span>   | <span data-ttu-id="1e40f-166">4</span><span class="sxs-lookup"><span data-stu-id="1e40f-166">4</span></span>                | <span data-ttu-id="1e40f-167">Ja (Inhalt)</span><span class="sxs-lookup"><span data-stu-id="1e40f-167">Yes(Contents)</span></span>    | <span data-ttu-id="1e40f-168">Keine</span><span class="sxs-lookup"><span data-stu-id="1e40f-168">None</span></span>     | <span data-ttu-id="1e40f-169">Ja</span><span class="sxs-lookup"><span data-stu-id="1e40f-169">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="1e40f-170">Ausgabe Register</span><span class="sxs-lookup"><span data-stu-id="1e40f-170">Output Registers</span></span>



| <span data-ttu-id="1e40f-171">Register</span><span class="sxs-lookup"><span data-stu-id="1e40f-171">Register</span></span> | <span data-ttu-id="1e40f-172">Name</span><span class="sxs-lookup"><span data-stu-id="1e40f-172">Name</span></span>            | <span data-ttu-id="1e40f-173">Anzahl</span><span class="sxs-lookup"><span data-stu-id="1e40f-173">Count</span></span> | <span data-ttu-id="1e40f-174">R/W</span><span class="sxs-lookup"><span data-stu-id="1e40f-174">R/W</span></span> | <span data-ttu-id="1e40f-175">Dimension</span><span class="sxs-lookup"><span data-stu-id="1e40f-175">Dimension</span></span> | <span data-ttu-id="1e40f-176">Indizierbar durch r\#</span><span class="sxs-lookup"><span data-stu-id="1e40f-176">Indexable by r\#</span></span> | <span data-ttu-id="1e40f-177">der Arbeitszeittabelle</span><span class="sxs-lookup"><span data-stu-id="1e40f-177">Defaults</span></span> | <span data-ttu-id="1e40f-178">Erfordert DCL</span><span class="sxs-lookup"><span data-stu-id="1e40f-178">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="1e40f-179">NULL</span><span class="sxs-lookup"><span data-stu-id="1e40f-179">NULL</span></span>     | <span data-ttu-id="1e40f-180">Ergebnis verwerfen</span><span class="sxs-lookup"><span data-stu-id="1e40f-180">Discard Result</span></span>  | <span data-ttu-id="1e40f-181">–</span><span class="sxs-lookup"><span data-stu-id="1e40f-181">N/A</span></span>   | <span data-ttu-id="1e40f-182">W</span><span class="sxs-lookup"><span data-stu-id="1e40f-182">W</span></span>   | <span data-ttu-id="1e40f-183">–</span><span class="sxs-lookup"><span data-stu-id="1e40f-183">N/A</span></span>       | <span data-ttu-id="1e40f-184">–</span><span class="sxs-lookup"><span data-stu-id="1e40f-184">N/A</span></span>              | <span data-ttu-id="1e40f-185">–</span><span class="sxs-lookup"><span data-stu-id="1e40f-185">N/A</span></span>      | <span data-ttu-id="1e40f-186">Nein</span><span class="sxs-lookup"><span data-stu-id="1e40f-186">No</span></span>           |
| <span data-ttu-id="1e40f-187">o\#</span><span class="sxs-lookup"><span data-stu-id="1e40f-187">o\#</span></span>      | <span data-ttu-id="1e40f-188">Ausgabe Register</span><span class="sxs-lookup"><span data-stu-id="1e40f-188">Output Register</span></span> | <span data-ttu-id="1e40f-189">32</span><span class="sxs-lookup"><span data-stu-id="1e40f-189">32</span></span>    | <span data-ttu-id="1e40f-190">W</span><span class="sxs-lookup"><span data-stu-id="1e40f-190">W</span></span>   | <span data-ttu-id="1e40f-191">–</span><span class="sxs-lookup"><span data-stu-id="1e40f-191">N/A</span></span>       | <span data-ttu-id="1e40f-192">N/V</span><span class="sxs-lookup"><span data-stu-id="1e40f-192">N/A</span></span>              | <span data-ttu-id="1e40f-193">4</span><span class="sxs-lookup"><span data-stu-id="1e40f-193">4</span></span>        | <span data-ttu-id="1e40f-194">Ja</span><span class="sxs-lookup"><span data-stu-id="1e40f-194">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="1e40f-195">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1e40f-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e40f-196">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="1e40f-196">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




