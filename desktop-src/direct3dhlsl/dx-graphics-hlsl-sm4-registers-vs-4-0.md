---
title: Register-vs_4_0
description: Dieser Abschnitt enthält Referenzinformationen zu den Eingabe-und Ausgabe Registern, die von Vertex Shader Version 4 0 implementiert werden \_ .
ms.assetid: f471df6a-06f6-4783-ba8f-cf0a3b43727f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 425fc4174b1c4a103fc7db15b5f05ae2b6dd95e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992783"
---
# <a name="registers---vs_4_0"></a><span data-ttu-id="0f5a5-103">Register-vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0f5a5-103">Registers - vs\_4\_0</span></span>

<span data-ttu-id="0f5a5-104">Dieser Abschnitt enthält Referenzinformationen zu den Eingabe-und Ausgabe Registern, die von Vertex Shader Version 4 0 implementiert werden \_ .</span><span class="sxs-lookup"><span data-stu-id="0f5a5-104">This section contains reference information for the input and output registers implemented by vertex shader version 4\_0.</span></span>

## <a name="input-registers"></a><span data-ttu-id="0f5a5-105">Eingabe Register</span><span class="sxs-lookup"><span data-stu-id="0f5a5-105">Input Registers</span></span>



| <span data-ttu-id="0f5a5-106">Register</span><span class="sxs-lookup"><span data-stu-id="0f5a5-106">Register</span></span>      | <span data-ttu-id="0f5a5-107">Name</span><span class="sxs-lookup"><span data-stu-id="0f5a5-107">Name</span></span> | <span data-ttu-id="0f5a5-108">Anzahl</span><span class="sxs-lookup"><span data-stu-id="0f5a5-108">Count</span></span>              | <span data-ttu-id="0f5a5-109">R/W</span><span class="sxs-lookup"><span data-stu-id="0f5a5-109">R/W</span></span> | <span data-ttu-id="0f5a5-110">Dimension</span><span class="sxs-lookup"><span data-stu-id="0f5a5-110">Dimension</span></span> | <span data-ttu-id="0f5a5-111">Indizierbar durch r\#</span><span class="sxs-lookup"><span data-stu-id="0f5a5-111">Indexable by r\#</span></span> | <span data-ttu-id="0f5a5-112">der Arbeitszeittabelle</span><span class="sxs-lookup"><span data-stu-id="0f5a5-112">Defaults</span></span> | <span data-ttu-id="0f5a5-113">Erfordert DCL</span><span class="sxs-lookup"><span data-stu-id="0f5a5-113">Requires DCL</span></span> |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="0f5a5-114">r\#</span><span class="sxs-lookup"><span data-stu-id="0f5a5-114">r\#</span></span>           |      | <span data-ttu-id="0f5a5-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="0f5a5-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="0f5a5-116">R/W</span><span class="sxs-lookup"><span data-stu-id="0f5a5-116">R/W</span></span> | <span data-ttu-id="0f5a5-117">4</span><span class="sxs-lookup"><span data-stu-id="0f5a5-117">4</span></span>         | <span data-ttu-id="0f5a5-118">Nein</span><span class="sxs-lookup"><span data-stu-id="0f5a5-118">No</span></span>               | <span data-ttu-id="0f5a5-119">Keine</span><span class="sxs-lookup"><span data-stu-id="0f5a5-119">None</span></span>     | <span data-ttu-id="0f5a5-120">Ja</span><span class="sxs-lookup"><span data-stu-id="0f5a5-120">Yes</span></span>          |
| <span data-ttu-id="0f5a5-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="0f5a5-121">x\#\[n\]</span></span>      |      | <span data-ttu-id="0f5a5-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="0f5a5-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="0f5a5-123">R/W</span><span class="sxs-lookup"><span data-stu-id="0f5a5-123">R/W</span></span> | <span data-ttu-id="0f5a5-124">4</span><span class="sxs-lookup"><span data-stu-id="0f5a5-124">4</span></span>         | <span data-ttu-id="0f5a5-125">Ja</span><span class="sxs-lookup"><span data-stu-id="0f5a5-125">Yes</span></span>              | <span data-ttu-id="0f5a5-126">Keine</span><span class="sxs-lookup"><span data-stu-id="0f5a5-126">None</span></span>     | <span data-ttu-id="0f5a5-127">Ja</span><span class="sxs-lookup"><span data-stu-id="0f5a5-127">Yes</span></span>          |
| <span data-ttu-id="0f5a5-128">Ramelow\#</span><span class="sxs-lookup"><span data-stu-id="0f5a5-128">v\#</span></span>           |      | <span data-ttu-id="0f5a5-129">16</span><span class="sxs-lookup"><span data-stu-id="0f5a5-129">16</span></span>                 | <span data-ttu-id="0f5a5-130">R</span><span class="sxs-lookup"><span data-stu-id="0f5a5-130">R</span></span>   | <span data-ttu-id="0f5a5-131">4</span><span class="sxs-lookup"><span data-stu-id="0f5a5-131">4</span></span>         | <span data-ttu-id="0f5a5-132">Ja</span><span class="sxs-lookup"><span data-stu-id="0f5a5-132">Yes</span></span>              | <span data-ttu-id="0f5a5-133">Keine</span><span class="sxs-lookup"><span data-stu-id="0f5a5-133">None</span></span>     | <span data-ttu-id="0f5a5-134">Ja</span><span class="sxs-lookup"><span data-stu-id="0f5a5-134">Yes</span></span>          |
| <span data-ttu-id="0f5a5-135">t\#</span><span class="sxs-lookup"><span data-stu-id="0f5a5-135">t\#</span></span>           |      | <span data-ttu-id="0f5a5-136">128</span><span class="sxs-lookup"><span data-stu-id="0f5a5-136">128</span></span>                | <span data-ttu-id="0f5a5-137">R</span><span class="sxs-lookup"><span data-stu-id="0f5a5-137">R</span></span>   | <span data-ttu-id="0f5a5-138">1</span><span class="sxs-lookup"><span data-stu-id="0f5a5-138">1</span></span>         | <span data-ttu-id="0f5a5-139">Nein</span><span class="sxs-lookup"><span data-stu-id="0f5a5-139">No</span></span>               | <span data-ttu-id="0f5a5-140">Keine</span><span class="sxs-lookup"><span data-stu-id="0f5a5-140">None</span></span>     | <span data-ttu-id="0f5a5-141">Ja</span><span class="sxs-lookup"><span data-stu-id="0f5a5-141">Yes</span></span>          |
| <span data-ttu-id="0f5a5-142">s\#</span><span class="sxs-lookup"><span data-stu-id="0f5a5-142">s\#</span></span>           |      | <span data-ttu-id="0f5a5-143">16</span><span class="sxs-lookup"><span data-stu-id="0f5a5-143">16</span></span>                 | <span data-ttu-id="0f5a5-144">R</span><span class="sxs-lookup"><span data-stu-id="0f5a5-144">R</span></span>   | <span data-ttu-id="0f5a5-145">1</span><span class="sxs-lookup"><span data-stu-id="0f5a5-145">1</span></span>         | <span data-ttu-id="0f5a5-146">Nein</span><span class="sxs-lookup"><span data-stu-id="0f5a5-146">No</span></span>               | <span data-ttu-id="0f5a5-147">Keine</span><span class="sxs-lookup"><span data-stu-id="0f5a5-147">None</span></span>     | <span data-ttu-id="0f5a5-148">Ja</span><span class="sxs-lookup"><span data-stu-id="0f5a5-148">Yes</span></span>          |
| <span data-ttu-id="0f5a5-149">CB- \# \[ Index\]</span><span class="sxs-lookup"><span data-stu-id="0f5a5-149">cb\#\[index\]</span></span> |      | <span data-ttu-id="0f5a5-150">15</span><span class="sxs-lookup"><span data-stu-id="0f5a5-150">15</span></span>                 | <span data-ttu-id="0f5a5-151">R</span><span class="sxs-lookup"><span data-stu-id="0f5a5-151">R</span></span>   | <span data-ttu-id="0f5a5-152">4</span><span class="sxs-lookup"><span data-stu-id="0f5a5-152">4</span></span>         | <span data-ttu-id="0f5a5-153">Ja (Inhalt)</span><span class="sxs-lookup"><span data-stu-id="0f5a5-153">Yes(Contents)</span></span>    | <span data-ttu-id="0f5a5-154">Keine</span><span class="sxs-lookup"><span data-stu-id="0f5a5-154">None</span></span>     | <span data-ttu-id="0f5a5-155">Ja</span><span class="sxs-lookup"><span data-stu-id="0f5a5-155">Yes</span></span>          |
| <span data-ttu-id="0f5a5-156">ICB- \[ Index\]</span><span class="sxs-lookup"><span data-stu-id="0f5a5-156">icb\[index\]</span></span>  |      | <span data-ttu-id="0f5a5-157">1</span><span class="sxs-lookup"><span data-stu-id="0f5a5-157">1</span></span>                  | <span data-ttu-id="0f5a5-158">R</span><span class="sxs-lookup"><span data-stu-id="0f5a5-158">R</span></span>   | <span data-ttu-id="0f5a5-159">4</span><span class="sxs-lookup"><span data-stu-id="0f5a5-159">4</span></span>         | <span data-ttu-id="0f5a5-160">Ja (Inhalt)</span><span class="sxs-lookup"><span data-stu-id="0f5a5-160">Yes(Contents)</span></span>    | <span data-ttu-id="0f5a5-161">Keine</span><span class="sxs-lookup"><span data-stu-id="0f5a5-161">None</span></span>     | <span data-ttu-id="0f5a5-162">Ja</span><span class="sxs-lookup"><span data-stu-id="0f5a5-162">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="0f5a5-163">Ausgabe Register</span><span class="sxs-lookup"><span data-stu-id="0f5a5-163">Output Registers</span></span>



| <span data-ttu-id="0f5a5-164">Register</span><span class="sxs-lookup"><span data-stu-id="0f5a5-164">Register</span></span> | <span data-ttu-id="0f5a5-165">Name</span><span class="sxs-lookup"><span data-stu-id="0f5a5-165">Name</span></span>            | <span data-ttu-id="0f5a5-166">Anzahl</span><span class="sxs-lookup"><span data-stu-id="0f5a5-166">Count</span></span> | <span data-ttu-id="0f5a5-167">R/W</span><span class="sxs-lookup"><span data-stu-id="0f5a5-167">R/W</span></span> | <span data-ttu-id="0f5a5-168">Dimension</span><span class="sxs-lookup"><span data-stu-id="0f5a5-168">Dimension</span></span> | <span data-ttu-id="0f5a5-169">Indizierbar durch r\#</span><span class="sxs-lookup"><span data-stu-id="0f5a5-169">Indexable by r\#</span></span> | <span data-ttu-id="0f5a5-170">der Arbeitszeittabelle</span><span class="sxs-lookup"><span data-stu-id="0f5a5-170">Defaults</span></span> | <span data-ttu-id="0f5a5-171">Erfordert DCL</span><span class="sxs-lookup"><span data-stu-id="0f5a5-171">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="0f5a5-172">NULL</span><span class="sxs-lookup"><span data-stu-id="0f5a5-172">NULL</span></span>     | <span data-ttu-id="0f5a5-173">Ergebnis verwerfen</span><span class="sxs-lookup"><span data-stu-id="0f5a5-173">Discard Result</span></span>  | <span data-ttu-id="0f5a5-174">–</span><span class="sxs-lookup"><span data-stu-id="0f5a5-174">N/A</span></span>   | <span data-ttu-id="0f5a5-175">W</span><span class="sxs-lookup"><span data-stu-id="0f5a5-175">W</span></span>   | <span data-ttu-id="0f5a5-176">–</span><span class="sxs-lookup"><span data-stu-id="0f5a5-176">N/A</span></span>       | <span data-ttu-id="0f5a5-177">–</span><span class="sxs-lookup"><span data-stu-id="0f5a5-177">N/A</span></span>              | <span data-ttu-id="0f5a5-178">–</span><span class="sxs-lookup"><span data-stu-id="0f5a5-178">N/A</span></span>      | <span data-ttu-id="0f5a5-179">Nein</span><span class="sxs-lookup"><span data-stu-id="0f5a5-179">No</span></span>           |
| <span data-ttu-id="0f5a5-180">o\#</span><span class="sxs-lookup"><span data-stu-id="0f5a5-180">o\#</span></span>      | <span data-ttu-id="0f5a5-181">Ausgabe Register</span><span class="sxs-lookup"><span data-stu-id="0f5a5-181">Output Register</span></span> | <span data-ttu-id="0f5a5-182">16</span><span class="sxs-lookup"><span data-stu-id="0f5a5-182">16</span></span>    | <span data-ttu-id="0f5a5-183">W</span><span class="sxs-lookup"><span data-stu-id="0f5a5-183">W</span></span>   | <span data-ttu-id="0f5a5-184">–</span><span class="sxs-lookup"><span data-stu-id="0f5a5-184">N/A</span></span>       | <span data-ttu-id="0f5a5-185">N/V</span><span class="sxs-lookup"><span data-stu-id="0f5a5-185">N/A</span></span>              | <span data-ttu-id="0f5a5-186">4</span><span class="sxs-lookup"><span data-stu-id="0f5a5-186">4</span></span>        | <span data-ttu-id="0f5a5-187">Ja</span><span class="sxs-lookup"><span data-stu-id="0f5a5-187">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="0f5a5-188">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0f5a5-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f5a5-189">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="0f5a5-189">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




