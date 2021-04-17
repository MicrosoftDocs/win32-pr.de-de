---
title: Register-ps_4_0
description: Dieser Abschnitt enthält Referenzinformationen zu den von Pixel Shader Version 4 0 implementierten Eingabe-und Ausgabe Registern \_ .
ms.assetid: 8b83667f-f599-4105-b68c-0d6aa7c528ab
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3dea9606419f32a168c08cc1efbebb5e285d3815
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388364"
---
# <a name="registers---ps_4_0"></a><span data-ttu-id="ad249-103">Register-PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ad249-103">Registers - ps\_4\_0</span></span>

<span data-ttu-id="ad249-104">Dieser Abschnitt enthält Referenzinformationen zu den von Pixel Shader Version 4 0 implementierten Eingabe-und Ausgabe Registern \_ .</span><span class="sxs-lookup"><span data-stu-id="ad249-104">This section contains reference information for the input and output registers implemented by pixel shader version 4\_0.</span></span>

## <a name="input-registers"></a><span data-ttu-id="ad249-105">Eingabe Register</span><span class="sxs-lookup"><span data-stu-id="ad249-105">Input Registers</span></span>



| <span data-ttu-id="ad249-106">Register</span><span class="sxs-lookup"><span data-stu-id="ad249-106">Register</span></span>      | <span data-ttu-id="ad249-107">Name</span><span class="sxs-lookup"><span data-stu-id="ad249-107">Name</span></span> | <span data-ttu-id="ad249-108">Anzahl</span><span class="sxs-lookup"><span data-stu-id="ad249-108">Count</span></span>              | <span data-ttu-id="ad249-109">R/W</span><span class="sxs-lookup"><span data-stu-id="ad249-109">R/W</span></span> | <span data-ttu-id="ad249-110">Dimension</span><span class="sxs-lookup"><span data-stu-id="ad249-110">Dimension</span></span> | <span data-ttu-id="ad249-111">Indizierbar durch r\#</span><span class="sxs-lookup"><span data-stu-id="ad249-111">Indexable by r\#</span></span> | <span data-ttu-id="ad249-112">der Arbeitszeittabelle</span><span class="sxs-lookup"><span data-stu-id="ad249-112">Defaults</span></span> | <span data-ttu-id="ad249-113">Erfordert DCL</span><span class="sxs-lookup"><span data-stu-id="ad249-113">Requires DCL</span></span> |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="ad249-114">r\#</span><span class="sxs-lookup"><span data-stu-id="ad249-114">r\#</span></span>           |      | <span data-ttu-id="ad249-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="ad249-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="ad249-116">R/W</span><span class="sxs-lookup"><span data-stu-id="ad249-116">R/W</span></span> | <span data-ttu-id="ad249-117">4</span><span class="sxs-lookup"><span data-stu-id="ad249-117">4</span></span>         | <span data-ttu-id="ad249-118">Nein</span><span class="sxs-lookup"><span data-stu-id="ad249-118">No</span></span>               | <span data-ttu-id="ad249-119">Keine</span><span class="sxs-lookup"><span data-stu-id="ad249-119">None</span></span>     | <span data-ttu-id="ad249-120">Ja</span><span class="sxs-lookup"><span data-stu-id="ad249-120">Yes</span></span>          |
| <span data-ttu-id="ad249-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="ad249-121">x\#\[n\]</span></span>      |      | <span data-ttu-id="ad249-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="ad249-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="ad249-123">R/W</span><span class="sxs-lookup"><span data-stu-id="ad249-123">R/W</span></span> | <span data-ttu-id="ad249-124">4</span><span class="sxs-lookup"><span data-stu-id="ad249-124">4</span></span>         | <span data-ttu-id="ad249-125">Ja</span><span class="sxs-lookup"><span data-stu-id="ad249-125">Yes</span></span>              | <span data-ttu-id="ad249-126">Keine</span><span class="sxs-lookup"><span data-stu-id="ad249-126">None</span></span>     | <span data-ttu-id="ad249-127">Ja</span><span class="sxs-lookup"><span data-stu-id="ad249-127">Yes</span></span>          |
| <span data-ttu-id="ad249-128">Ramelow\#</span><span class="sxs-lookup"><span data-stu-id="ad249-128">v\#</span></span>           |      | <span data-ttu-id="ad249-129">32</span><span class="sxs-lookup"><span data-stu-id="ad249-129">32</span></span>                 | <span data-ttu-id="ad249-130">R</span><span class="sxs-lookup"><span data-stu-id="ad249-130">R</span></span>   | <span data-ttu-id="ad249-131">4</span><span class="sxs-lookup"><span data-stu-id="ad249-131">4</span></span>         | <span data-ttu-id="ad249-132">Ja</span><span class="sxs-lookup"><span data-stu-id="ad249-132">Yes</span></span>              | <span data-ttu-id="ad249-133">Keine</span><span class="sxs-lookup"><span data-stu-id="ad249-133">None</span></span>     | <span data-ttu-id="ad249-134">Ja</span><span class="sxs-lookup"><span data-stu-id="ad249-134">Yes</span></span>          |
| <span data-ttu-id="ad249-135">t\#</span><span class="sxs-lookup"><span data-stu-id="ad249-135">t\#</span></span>           |      | <span data-ttu-id="ad249-136">128</span><span class="sxs-lookup"><span data-stu-id="ad249-136">128</span></span>                | <span data-ttu-id="ad249-137">R</span><span class="sxs-lookup"><span data-stu-id="ad249-137">R</span></span>   | <span data-ttu-id="ad249-138">1</span><span class="sxs-lookup"><span data-stu-id="ad249-138">1</span></span>         | <span data-ttu-id="ad249-139">Nein</span><span class="sxs-lookup"><span data-stu-id="ad249-139">No</span></span>               | <span data-ttu-id="ad249-140">Keine</span><span class="sxs-lookup"><span data-stu-id="ad249-140">None</span></span>     | <span data-ttu-id="ad249-141">Ja</span><span class="sxs-lookup"><span data-stu-id="ad249-141">Yes</span></span>          |
| <span data-ttu-id="ad249-142">s\#</span><span class="sxs-lookup"><span data-stu-id="ad249-142">s\#</span></span>           |      | <span data-ttu-id="ad249-143">16</span><span class="sxs-lookup"><span data-stu-id="ad249-143">16</span></span>                 | <span data-ttu-id="ad249-144">R</span><span class="sxs-lookup"><span data-stu-id="ad249-144">R</span></span>   | <span data-ttu-id="ad249-145">1</span><span class="sxs-lookup"><span data-stu-id="ad249-145">1</span></span>         | <span data-ttu-id="ad249-146">Nein</span><span class="sxs-lookup"><span data-stu-id="ad249-146">No</span></span>               | <span data-ttu-id="ad249-147">Keine</span><span class="sxs-lookup"><span data-stu-id="ad249-147">None</span></span>     | <span data-ttu-id="ad249-148">Ja</span><span class="sxs-lookup"><span data-stu-id="ad249-148">Yes</span></span>          |
| <span data-ttu-id="ad249-149">CB- \# \[ Index\]</span><span class="sxs-lookup"><span data-stu-id="ad249-149">cb\#\[index\]</span></span> |      | <span data-ttu-id="ad249-150">15</span><span class="sxs-lookup"><span data-stu-id="ad249-150">15</span></span>                 | <span data-ttu-id="ad249-151">R</span><span class="sxs-lookup"><span data-stu-id="ad249-151">R</span></span>   | <span data-ttu-id="ad249-152">4</span><span class="sxs-lookup"><span data-stu-id="ad249-152">4</span></span>         | <span data-ttu-id="ad249-153">Ja (Inhalt)</span><span class="sxs-lookup"><span data-stu-id="ad249-153">Yes(Contents)</span></span>    | <span data-ttu-id="ad249-154">Keine</span><span class="sxs-lookup"><span data-stu-id="ad249-154">None</span></span>     | <span data-ttu-id="ad249-155">Ja</span><span class="sxs-lookup"><span data-stu-id="ad249-155">Yes</span></span>          |
| <span data-ttu-id="ad249-156">ICB- \[ Index\]</span><span class="sxs-lookup"><span data-stu-id="ad249-156">icb\[index\]</span></span>  |      | <span data-ttu-id="ad249-157">1</span><span class="sxs-lookup"><span data-stu-id="ad249-157">1</span></span>                  | <span data-ttu-id="ad249-158">R</span><span class="sxs-lookup"><span data-stu-id="ad249-158">R</span></span>   | <span data-ttu-id="ad249-159">4</span><span class="sxs-lookup"><span data-stu-id="ad249-159">4</span></span>         | <span data-ttu-id="ad249-160">Ja (Inhalt)</span><span class="sxs-lookup"><span data-stu-id="ad249-160">Yes(Contents)</span></span>    | <span data-ttu-id="ad249-161">Keine</span><span class="sxs-lookup"><span data-stu-id="ad249-161">None</span></span>     | <span data-ttu-id="ad249-162">Ja</span><span class="sxs-lookup"><span data-stu-id="ad249-162">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="ad249-163">Ausgabe Register</span><span class="sxs-lookup"><span data-stu-id="ad249-163">Output Registers</span></span>



| <span data-ttu-id="ad249-164">Register</span><span class="sxs-lookup"><span data-stu-id="ad249-164">Register</span></span> | <span data-ttu-id="ad249-165">Name</span><span class="sxs-lookup"><span data-stu-id="ad249-165">Name</span></span>            | <span data-ttu-id="ad249-166">Anzahl</span><span class="sxs-lookup"><span data-stu-id="ad249-166">Count</span></span> | <span data-ttu-id="ad249-167">R/W</span><span class="sxs-lookup"><span data-stu-id="ad249-167">R/W</span></span> | <span data-ttu-id="ad249-168">Dimension</span><span class="sxs-lookup"><span data-stu-id="ad249-168">Dimension</span></span> | <span data-ttu-id="ad249-169">Indizierbar durch r\#</span><span class="sxs-lookup"><span data-stu-id="ad249-169">Indexable by r\#</span></span> | <span data-ttu-id="ad249-170">der Arbeitszeittabelle</span><span class="sxs-lookup"><span data-stu-id="ad249-170">Defaults</span></span> | <span data-ttu-id="ad249-171">Erfordert DCL</span><span class="sxs-lookup"><span data-stu-id="ad249-171">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="ad249-172">NULL</span><span class="sxs-lookup"><span data-stu-id="ad249-172">NULL</span></span>     | <span data-ttu-id="ad249-173">Ergebnis verwerfen</span><span class="sxs-lookup"><span data-stu-id="ad249-173">Discard Result</span></span>  | <span data-ttu-id="ad249-174">–</span><span class="sxs-lookup"><span data-stu-id="ad249-174">N/A</span></span>   | <span data-ttu-id="ad249-175">W</span><span class="sxs-lookup"><span data-stu-id="ad249-175">W</span></span>   | <span data-ttu-id="ad249-176">–</span><span class="sxs-lookup"><span data-stu-id="ad249-176">N/A</span></span>       | <span data-ttu-id="ad249-177">–</span><span class="sxs-lookup"><span data-stu-id="ad249-177">N/A</span></span>              | <span data-ttu-id="ad249-178">–</span><span class="sxs-lookup"><span data-stu-id="ad249-178">N/A</span></span>      | <span data-ttu-id="ad249-179">Nein</span><span class="sxs-lookup"><span data-stu-id="ad249-179">No</span></span>           |
| <span data-ttu-id="ad249-180">o\#</span><span class="sxs-lookup"><span data-stu-id="ad249-180">o\#</span></span>      | <span data-ttu-id="ad249-181">Ausgabe Register</span><span class="sxs-lookup"><span data-stu-id="ad249-181">Output Register</span></span> | <span data-ttu-id="ad249-182">8</span><span class="sxs-lookup"><span data-stu-id="ad249-182">8</span></span>     | <span data-ttu-id="ad249-183">W</span><span class="sxs-lookup"><span data-stu-id="ad249-183">W</span></span>   | <span data-ttu-id="ad249-184">–</span><span class="sxs-lookup"><span data-stu-id="ad249-184">N/A</span></span>       | <span data-ttu-id="ad249-185">N/V</span><span class="sxs-lookup"><span data-stu-id="ad249-185">N/A</span></span>              | <span data-ttu-id="ad249-186">4</span><span class="sxs-lookup"><span data-stu-id="ad249-186">4</span></span>        | <span data-ttu-id="ad249-187">Nein</span><span class="sxs-lookup"><span data-stu-id="ad249-187">No</span></span>           |
| <span data-ttu-id="ad249-188">otiefe</span><span class="sxs-lookup"><span data-stu-id="ad249-188">oDepth</span></span>   | <span data-ttu-id="ad249-189">Ausgabe Tiefe</span><span class="sxs-lookup"><span data-stu-id="ad249-189">Output Depth</span></span>    | <span data-ttu-id="ad249-190">1</span><span class="sxs-lookup"><span data-stu-id="ad249-190">1</span></span>     | <span data-ttu-id="ad249-191">W</span><span class="sxs-lookup"><span data-stu-id="ad249-191">W</span></span>   | <span data-ttu-id="ad249-192">–</span><span class="sxs-lookup"><span data-stu-id="ad249-192">N/A</span></span>       | <span data-ttu-id="ad249-193">–</span><span class="sxs-lookup"><span data-stu-id="ad249-193">N/A</span></span>              | <span data-ttu-id="ad249-194">1</span><span class="sxs-lookup"><span data-stu-id="ad249-194">1</span></span>        | <span data-ttu-id="ad249-195">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="ad249-195">N/A</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="ad249-196">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ad249-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad249-197">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="ad249-197">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




