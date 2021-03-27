---
title: Register-vs_4_1
description: Dieser Abschnitt enthält Referenzinformationen zu den Eingabe-und Ausgabe Registern, die von Vertex Shader Version 4 1 implementiert werden \_ .
ms.assetid: ea449195-d012-4a14-9760-b738a8623343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df2254c111303129327d255f94727a5e42ac1c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206944"
---
# <a name="registers---vs_4_1"></a><span data-ttu-id="bcdca-103">Register-vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="bcdca-103">Registers - vs\_4\_1</span></span>

<span data-ttu-id="bcdca-104">Dieser Abschnitt enthält Referenzinformationen zu den Eingabe-und Ausgabe Registern, die von Vertex Shader Version 4 1 implementiert werden \_ .</span><span class="sxs-lookup"><span data-stu-id="bcdca-104">This section contains reference information for the input and output registers implemented by vertex shader version 4\_1.</span></span>

## <a name="input-registers"></a><span data-ttu-id="bcdca-105">Eingabe Register</span><span class="sxs-lookup"><span data-stu-id="bcdca-105">Input Registers</span></span>



| <span data-ttu-id="bcdca-106">Register</span><span class="sxs-lookup"><span data-stu-id="bcdca-106">Register</span></span>      | <span data-ttu-id="bcdca-107">Name</span><span class="sxs-lookup"><span data-stu-id="bcdca-107">Name</span></span> | <span data-ttu-id="bcdca-108">Anzahl</span><span class="sxs-lookup"><span data-stu-id="bcdca-108">Count</span></span>              | <span data-ttu-id="bcdca-109">R/W</span><span class="sxs-lookup"><span data-stu-id="bcdca-109">R/W</span></span> | <span data-ttu-id="bcdca-110">Dimension</span><span class="sxs-lookup"><span data-stu-id="bcdca-110">Dimension</span></span> | <span data-ttu-id="bcdca-111">Indizierbar durch r\#</span><span class="sxs-lookup"><span data-stu-id="bcdca-111">Indexable by r\#</span></span> | <span data-ttu-id="bcdca-112">der Arbeitszeittabelle</span><span class="sxs-lookup"><span data-stu-id="bcdca-112">Defaults</span></span> | <span data-ttu-id="bcdca-113">Erfordert DCL</span><span class="sxs-lookup"><span data-stu-id="bcdca-113">Requires DCL</span></span> |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="bcdca-114">r\#</span><span class="sxs-lookup"><span data-stu-id="bcdca-114">r\#</span></span>           |      | <span data-ttu-id="bcdca-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="bcdca-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="bcdca-116">R/W</span><span class="sxs-lookup"><span data-stu-id="bcdca-116">R/W</span></span> | <span data-ttu-id="bcdca-117">4</span><span class="sxs-lookup"><span data-stu-id="bcdca-117">4</span></span>         | <span data-ttu-id="bcdca-118">Nein</span><span class="sxs-lookup"><span data-stu-id="bcdca-118">No</span></span>               | <span data-ttu-id="bcdca-119">Keine</span><span class="sxs-lookup"><span data-stu-id="bcdca-119">None</span></span>     | <span data-ttu-id="bcdca-120">Ja</span><span class="sxs-lookup"><span data-stu-id="bcdca-120">Yes</span></span>          |
| <span data-ttu-id="bcdca-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bcdca-121">x\#\[n\]</span></span>      |      | <span data-ttu-id="bcdca-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="bcdca-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="bcdca-123">R/W</span><span class="sxs-lookup"><span data-stu-id="bcdca-123">R/W</span></span> | <span data-ttu-id="bcdca-124">4</span><span class="sxs-lookup"><span data-stu-id="bcdca-124">4</span></span>         | <span data-ttu-id="bcdca-125">Ja</span><span class="sxs-lookup"><span data-stu-id="bcdca-125">Yes</span></span>              | <span data-ttu-id="bcdca-126">Keine</span><span class="sxs-lookup"><span data-stu-id="bcdca-126">None</span></span>     | <span data-ttu-id="bcdca-127">Ja</span><span class="sxs-lookup"><span data-stu-id="bcdca-127">Yes</span></span>          |
| <span data-ttu-id="bcdca-128">Ramelow\#</span><span class="sxs-lookup"><span data-stu-id="bcdca-128">v\#</span></span>           |      | <span data-ttu-id="bcdca-129">32</span><span class="sxs-lookup"><span data-stu-id="bcdca-129">32</span></span>                 | <span data-ttu-id="bcdca-130">R</span><span class="sxs-lookup"><span data-stu-id="bcdca-130">R</span></span>   | <span data-ttu-id="bcdca-131">4</span><span class="sxs-lookup"><span data-stu-id="bcdca-131">4</span></span>         | <span data-ttu-id="bcdca-132">Ja</span><span class="sxs-lookup"><span data-stu-id="bcdca-132">Yes</span></span>              | <span data-ttu-id="bcdca-133">Keine</span><span class="sxs-lookup"><span data-stu-id="bcdca-133">None</span></span>     | <span data-ttu-id="bcdca-134">Ja</span><span class="sxs-lookup"><span data-stu-id="bcdca-134">Yes</span></span>          |
| <span data-ttu-id="bcdca-135">t\#</span><span class="sxs-lookup"><span data-stu-id="bcdca-135">t\#</span></span>           |      | <span data-ttu-id="bcdca-136">128</span><span class="sxs-lookup"><span data-stu-id="bcdca-136">128</span></span>                | <span data-ttu-id="bcdca-137">R</span><span class="sxs-lookup"><span data-stu-id="bcdca-137">R</span></span>   | <span data-ttu-id="bcdca-138">1</span><span class="sxs-lookup"><span data-stu-id="bcdca-138">1</span></span>         | <span data-ttu-id="bcdca-139">Nein</span><span class="sxs-lookup"><span data-stu-id="bcdca-139">No</span></span>               | <span data-ttu-id="bcdca-140">Keine</span><span class="sxs-lookup"><span data-stu-id="bcdca-140">None</span></span>     | <span data-ttu-id="bcdca-141">Ja</span><span class="sxs-lookup"><span data-stu-id="bcdca-141">Yes</span></span>          |
| <span data-ttu-id="bcdca-142">s\#</span><span class="sxs-lookup"><span data-stu-id="bcdca-142">s\#</span></span>           |      | <span data-ttu-id="bcdca-143">16</span><span class="sxs-lookup"><span data-stu-id="bcdca-143">16</span></span>                 | <span data-ttu-id="bcdca-144">R</span><span class="sxs-lookup"><span data-stu-id="bcdca-144">R</span></span>   | <span data-ttu-id="bcdca-145">1</span><span class="sxs-lookup"><span data-stu-id="bcdca-145">1</span></span>         | <span data-ttu-id="bcdca-146">Nein</span><span class="sxs-lookup"><span data-stu-id="bcdca-146">No</span></span>               | <span data-ttu-id="bcdca-147">Keine</span><span class="sxs-lookup"><span data-stu-id="bcdca-147">None</span></span>     | <span data-ttu-id="bcdca-148">Ja</span><span class="sxs-lookup"><span data-stu-id="bcdca-148">Yes</span></span>          |
| <span data-ttu-id="bcdca-149">CB- \# \[ Index\]</span><span class="sxs-lookup"><span data-stu-id="bcdca-149">cb\#\[index\]</span></span> |      | <span data-ttu-id="bcdca-150">15</span><span class="sxs-lookup"><span data-stu-id="bcdca-150">15</span></span>                 | <span data-ttu-id="bcdca-151">R</span><span class="sxs-lookup"><span data-stu-id="bcdca-151">R</span></span>   | <span data-ttu-id="bcdca-152">4</span><span class="sxs-lookup"><span data-stu-id="bcdca-152">4</span></span>         | <span data-ttu-id="bcdca-153">Ja (Inhalt)</span><span class="sxs-lookup"><span data-stu-id="bcdca-153">Yes(Contents)</span></span>    | <span data-ttu-id="bcdca-154">Keine</span><span class="sxs-lookup"><span data-stu-id="bcdca-154">None</span></span>     | <span data-ttu-id="bcdca-155">Ja</span><span class="sxs-lookup"><span data-stu-id="bcdca-155">Yes</span></span>          |
| <span data-ttu-id="bcdca-156">ICB- \[ Index\]</span><span class="sxs-lookup"><span data-stu-id="bcdca-156">icb\[index\]</span></span>  |      | <span data-ttu-id="bcdca-157">1</span><span class="sxs-lookup"><span data-stu-id="bcdca-157">1</span></span>                  | <span data-ttu-id="bcdca-158">R</span><span class="sxs-lookup"><span data-stu-id="bcdca-158">R</span></span>   | <span data-ttu-id="bcdca-159">4</span><span class="sxs-lookup"><span data-stu-id="bcdca-159">4</span></span>         | <span data-ttu-id="bcdca-160">Ja (Inhalt)</span><span class="sxs-lookup"><span data-stu-id="bcdca-160">Yes(Contents)</span></span>    | <span data-ttu-id="bcdca-161">Keine</span><span class="sxs-lookup"><span data-stu-id="bcdca-161">None</span></span>     | <span data-ttu-id="bcdca-162">Ja</span><span class="sxs-lookup"><span data-stu-id="bcdca-162">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="bcdca-163">Ausgabe Register</span><span class="sxs-lookup"><span data-stu-id="bcdca-163">Output Registers</span></span>



| <span data-ttu-id="bcdca-164">Register</span><span class="sxs-lookup"><span data-stu-id="bcdca-164">Register</span></span> | <span data-ttu-id="bcdca-165">Name</span><span class="sxs-lookup"><span data-stu-id="bcdca-165">Name</span></span>            | <span data-ttu-id="bcdca-166">Anzahl</span><span class="sxs-lookup"><span data-stu-id="bcdca-166">Count</span></span> | <span data-ttu-id="bcdca-167">R/W</span><span class="sxs-lookup"><span data-stu-id="bcdca-167">R/W</span></span> | <span data-ttu-id="bcdca-168">Dimension</span><span class="sxs-lookup"><span data-stu-id="bcdca-168">Dimension</span></span> | <span data-ttu-id="bcdca-169">Indizierbar durch r\#</span><span class="sxs-lookup"><span data-stu-id="bcdca-169">Indexable by r\#</span></span> | <span data-ttu-id="bcdca-170">der Arbeitszeittabelle</span><span class="sxs-lookup"><span data-stu-id="bcdca-170">Defaults</span></span> | <span data-ttu-id="bcdca-171">Erfordert DCL</span><span class="sxs-lookup"><span data-stu-id="bcdca-171">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="bcdca-172">NULL</span><span class="sxs-lookup"><span data-stu-id="bcdca-172">NULL</span></span>     | <span data-ttu-id="bcdca-173">Ergebnis verwerfen</span><span class="sxs-lookup"><span data-stu-id="bcdca-173">Discard Result</span></span>  | <span data-ttu-id="bcdca-174">–</span><span class="sxs-lookup"><span data-stu-id="bcdca-174">N/A</span></span>   | <span data-ttu-id="bcdca-175">W</span><span class="sxs-lookup"><span data-stu-id="bcdca-175">W</span></span>   | <span data-ttu-id="bcdca-176">–</span><span class="sxs-lookup"><span data-stu-id="bcdca-176">N/A</span></span>       | <span data-ttu-id="bcdca-177">–</span><span class="sxs-lookup"><span data-stu-id="bcdca-177">N/A</span></span>              | <span data-ttu-id="bcdca-178">–</span><span class="sxs-lookup"><span data-stu-id="bcdca-178">N/A</span></span>      | <span data-ttu-id="bcdca-179">Nein</span><span class="sxs-lookup"><span data-stu-id="bcdca-179">No</span></span>           |
| <span data-ttu-id="bcdca-180">o\#</span><span class="sxs-lookup"><span data-stu-id="bcdca-180">o\#</span></span>      | <span data-ttu-id="bcdca-181">Ausgabe Register</span><span class="sxs-lookup"><span data-stu-id="bcdca-181">Output Register</span></span> | <span data-ttu-id="bcdca-182">32</span><span class="sxs-lookup"><span data-stu-id="bcdca-182">32</span></span>    | <span data-ttu-id="bcdca-183">W</span><span class="sxs-lookup"><span data-stu-id="bcdca-183">W</span></span>   | <span data-ttu-id="bcdca-184">–</span><span class="sxs-lookup"><span data-stu-id="bcdca-184">N/A</span></span>       | <span data-ttu-id="bcdca-185">N/V</span><span class="sxs-lookup"><span data-stu-id="bcdca-185">N/A</span></span>              | <span data-ttu-id="bcdca-186">4</span><span class="sxs-lookup"><span data-stu-id="bcdca-186">4</span></span>        | <span data-ttu-id="bcdca-187">Ja</span><span class="sxs-lookup"><span data-stu-id="bcdca-187">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="bcdca-188">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bcdca-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bcdca-189">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="bcdca-189">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




