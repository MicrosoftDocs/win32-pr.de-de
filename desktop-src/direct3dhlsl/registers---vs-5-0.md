---
title: Register-vs_5_0
description: Die folgenden Eingabe-und Ausgabe Register sind in der Vertex-Shader-Version 5 \_ 0 implementiert.
ms.assetid: 475753C7-C055-4DB7-9DC3-6C734413A92B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1dc211f5f3dd8819577c796849dcb86012cc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104976136"
---
# <a name="registers---vs_5_0"></a><span data-ttu-id="74233-103">Register-vs \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="74233-103">Registers - vs\_5\_0</span></span>

<span data-ttu-id="74233-104">Die folgenden Eingabe-und Ausgabe Register sind in der Vertex-Shader-Version 5 \_ 0 implementiert.</span><span class="sxs-lookup"><span data-stu-id="74233-104">The following input and output registers are implemented in the vertex shader version 5\_0.</span></span>

## <a name="input-registers"></a><span data-ttu-id="74233-105">Eingabe Register</span><span class="sxs-lookup"><span data-stu-id="74233-105">Input Registers</span></span>



| <span data-ttu-id="74233-106">Registriungstyp</span><span class="sxs-lookup"><span data-stu-id="74233-106">Register Type</span></span>                                      | <span data-ttu-id="74233-107">Anzahl</span><span class="sxs-lookup"><span data-stu-id="74233-107">Count</span></span>              | <span data-ttu-id="74233-108">R/W</span><span class="sxs-lookup"><span data-stu-id="74233-108">R/W</span></span> | <span data-ttu-id="74233-109">Dimension</span><span class="sxs-lookup"><span data-stu-id="74233-109">Dimension</span></span> | <span data-ttu-id="74233-110">Indizierbar durch r\#</span><span class="sxs-lookup"><span data-stu-id="74233-110">Indexable by r\#</span></span> | <span data-ttu-id="74233-111">der Arbeitszeittabelle</span><span class="sxs-lookup"><span data-stu-id="74233-111">Defaults</span></span> | <span data-ttu-id="74233-112">Erfordert DCL</span><span class="sxs-lookup"><span data-stu-id="74233-112">Requires DCL</span></span> |
|----------------------------------------------------|--------------------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="74233-113">32-Bit-Temp (r \# )</span><span class="sxs-lookup"><span data-stu-id="74233-113">32-bit Temp (r\#)</span></span>                                  | <span data-ttu-id="74233-114">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="74233-114">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="74233-115">R/W</span><span class="sxs-lookup"><span data-stu-id="74233-115">R/W</span></span> | <span data-ttu-id="74233-116">4</span><span class="sxs-lookup"><span data-stu-id="74233-116">4</span></span>         | <span data-ttu-id="74233-117">Nein</span><span class="sxs-lookup"><span data-stu-id="74233-117">No</span></span>               | <span data-ttu-id="74233-118">Keine</span><span class="sxs-lookup"><span data-stu-id="74233-118">None</span></span>     | <span data-ttu-id="74233-119">Ja</span><span class="sxs-lookup"><span data-stu-id="74233-119">Yes</span></span>          |
| <span data-ttu-id="74233-120">32-Bit indizierbares temporäres Array (x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="74233-120">32-bit indexable Temp Array (x\#\[n\])</span></span>             | <span data-ttu-id="74233-121">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="74233-121">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="74233-122">R/W</span><span class="sxs-lookup"><span data-stu-id="74233-122">R/W</span></span> | <span data-ttu-id="74233-123">4</span><span class="sxs-lookup"><span data-stu-id="74233-123">4</span></span>         | <span data-ttu-id="74233-124">Ja</span><span class="sxs-lookup"><span data-stu-id="74233-124">Yes</span></span>              | <span data-ttu-id="74233-125">Keine</span><span class="sxs-lookup"><span data-stu-id="74233-125">None</span></span>     | <span data-ttu-id="74233-126">Ja</span><span class="sxs-lookup"><span data-stu-id="74233-126">Yes</span></span>          |
| <span data-ttu-id="74233-127">32-Bit-Eingabe (v \# )</span><span class="sxs-lookup"><span data-stu-id="74233-127">32-bit input (v\#)</span></span>                                 | <span data-ttu-id="74233-128">32</span><span class="sxs-lookup"><span data-stu-id="74233-128">32</span></span>                 | <span data-ttu-id="74233-129">R</span><span class="sxs-lookup"><span data-stu-id="74233-129">R</span></span>   | <span data-ttu-id="74233-130">4</span><span class="sxs-lookup"><span data-stu-id="74233-130">4</span></span>         | <span data-ttu-id="74233-131">Ja</span><span class="sxs-lookup"><span data-stu-id="74233-131">Yes</span></span>              | <span data-ttu-id="74233-132">Keine</span><span class="sxs-lookup"><span data-stu-id="74233-132">None</span></span>     | <span data-ttu-id="74233-133">Ja</span><span class="sxs-lookup"><span data-stu-id="74233-133">Yes</span></span>          |
| <span data-ttu-id="74233-134">-Element in einer Eingabe Ressource (t \# )</span><span class="sxs-lookup"><span data-stu-id="74233-134">Element in an input resource (t\#)</span></span>                 | <span data-ttu-id="74233-135">128</span><span class="sxs-lookup"><span data-stu-id="74233-135">128</span></span>                | <span data-ttu-id="74233-136">R</span><span class="sxs-lookup"><span data-stu-id="74233-136">R</span></span>   | <span data-ttu-id="74233-137">1</span><span class="sxs-lookup"><span data-stu-id="74233-137">1</span></span>         | <span data-ttu-id="74233-138">Nein</span><span class="sxs-lookup"><span data-stu-id="74233-138">No</span></span>               | <span data-ttu-id="74233-139">Keine</span><span class="sxs-lookup"><span data-stu-id="74233-139">None</span></span>     | <span data-ttu-id="74233-140">Ja</span><span class="sxs-lookup"><span data-stu-id="74233-140">Yes</span></span>          |
| <span data-ttu-id="74233-141">Sampler (e \# )</span><span class="sxs-lookup"><span data-stu-id="74233-141">Sampler (s\#)</span></span>                                      | <span data-ttu-id="74233-142">16</span><span class="sxs-lookup"><span data-stu-id="74233-142">16</span></span>                 | <span data-ttu-id="74233-143">R</span><span class="sxs-lookup"><span data-stu-id="74233-143">R</span></span>   | <span data-ttu-id="74233-144">1</span><span class="sxs-lookup"><span data-stu-id="74233-144">1</span></span>         | <span data-ttu-id="74233-145">Nein</span><span class="sxs-lookup"><span data-stu-id="74233-145">No</span></span>               | <span data-ttu-id="74233-146">Keine</span><span class="sxs-lookup"><span data-stu-id="74233-146">None</span></span>     | <span data-ttu-id="74233-147">Ja</span><span class="sxs-lookup"><span data-stu-id="74233-147">Yes</span></span>          |
| <span data-ttu-id="74233-148">Constantbuffer-Verweis (CB- \# \[ Index \] )</span><span class="sxs-lookup"><span data-stu-id="74233-148">ConstantBuffer reference (cb\#\[index\])</span></span>           | <span data-ttu-id="74233-149">15</span><span class="sxs-lookup"><span data-stu-id="74233-149">15</span></span>                 | <span data-ttu-id="74233-150">R</span><span class="sxs-lookup"><span data-stu-id="74233-150">R</span></span>   | <span data-ttu-id="74233-151">4</span><span class="sxs-lookup"><span data-stu-id="74233-151">4</span></span>         | <span data-ttu-id="74233-152">Ja (Inhalt)</span><span class="sxs-lookup"><span data-stu-id="74233-152">Yes(contents)</span></span>    | <span data-ttu-id="74233-153">Keine</span><span class="sxs-lookup"><span data-stu-id="74233-153">None</span></span>     | <span data-ttu-id="74233-154">Ja</span><span class="sxs-lookup"><span data-stu-id="74233-154">Yes</span></span>          |
| <span data-ttu-id="74233-155">iimmediate constantbuffer-Referenz (ICB- \[ Index \] )</span><span class="sxs-lookup"><span data-stu-id="74233-155">iImmediate ConstantBuffer reference (icb\[index\])</span></span> | <span data-ttu-id="74233-156">1</span><span class="sxs-lookup"><span data-stu-id="74233-156">1</span></span>                  | <span data-ttu-id="74233-157">R</span><span class="sxs-lookup"><span data-stu-id="74233-157">R</span></span>   | <span data-ttu-id="74233-158">4</span><span class="sxs-lookup"><span data-stu-id="74233-158">4</span></span>         | <span data-ttu-id="74233-159">Ja (Inhalt)</span><span class="sxs-lookup"><span data-stu-id="74233-159">Yes(contents)</span></span>    | <span data-ttu-id="74233-160">Keine</span><span class="sxs-lookup"><span data-stu-id="74233-160">None</span></span>     | <span data-ttu-id="74233-161">Ja</span><span class="sxs-lookup"><span data-stu-id="74233-161">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="74233-162">Ausgabe Register</span><span class="sxs-lookup"><span data-stu-id="74233-162">Output Registers</span></span>



| <span data-ttu-id="74233-163">Registriungstyp</span><span class="sxs-lookup"><span data-stu-id="74233-163">Register Type</span></span>                                                      | <span data-ttu-id="74233-164">Anzahl</span><span class="sxs-lookup"><span data-stu-id="74233-164">Count</span></span> | <span data-ttu-id="74233-165">R/W</span><span class="sxs-lookup"><span data-stu-id="74233-165">R/W</span></span> | <span data-ttu-id="74233-166">Dimension</span><span class="sxs-lookup"><span data-stu-id="74233-166">Dimension</span></span> | <span data-ttu-id="74233-167">Indizierbar durch r\#</span><span class="sxs-lookup"><span data-stu-id="74233-167">Indexable by r\#</span></span> | <span data-ttu-id="74233-168">der Arbeitszeittabelle</span><span class="sxs-lookup"><span data-stu-id="74233-168">Defaults</span></span> | <span data-ttu-id="74233-169">Erfordert DCL</span><span class="sxs-lookup"><span data-stu-id="74233-169">Requires DCL</span></span> |
|--------------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="74233-170">NULL (Ergebnis verwerfen, nützlich für Vorgänge mit mehreren Ergebnissen)</span><span class="sxs-lookup"><span data-stu-id="74233-170">NULL (discard result, useful for operations with multiple results)</span></span> | <span data-ttu-id="74233-171">–</span><span class="sxs-lookup"><span data-stu-id="74233-171">N/A</span></span>   | <span data-ttu-id="74233-172">W</span><span class="sxs-lookup"><span data-stu-id="74233-172">W</span></span>   | <span data-ttu-id="74233-173">–</span><span class="sxs-lookup"><span data-stu-id="74233-173">N/A</span></span>       | <span data-ttu-id="74233-174">–</span><span class="sxs-lookup"><span data-stu-id="74233-174">N/A</span></span>              | <span data-ttu-id="74233-175">–</span><span class="sxs-lookup"><span data-stu-id="74233-175">N/A</span></span>      | <span data-ttu-id="74233-176">Nein</span><span class="sxs-lookup"><span data-stu-id="74233-176">No</span></span>           |
| <span data-ttu-id="74233-177">32-Bit-Ausgabe-Vertex-Daten Element (o \# )</span><span class="sxs-lookup"><span data-stu-id="74233-177">32-bit output Vertex Data Element (o\#)</span></span>                            | <span data-ttu-id="74233-178">32</span><span class="sxs-lookup"><span data-stu-id="74233-178">32</span></span>    | <span data-ttu-id="74233-179">W</span><span class="sxs-lookup"><span data-stu-id="74233-179">W</span></span>   | <span data-ttu-id="74233-180">4</span><span class="sxs-lookup"><span data-stu-id="74233-180">4</span></span>         | <span data-ttu-id="74233-181">–</span><span class="sxs-lookup"><span data-stu-id="74233-181">N/A</span></span>              | <span data-ttu-id="74233-182">–</span><span class="sxs-lookup"><span data-stu-id="74233-182">N/A</span></span>      | <span data-ttu-id="74233-183">Ja</span><span class="sxs-lookup"><span data-stu-id="74233-183">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="74233-184">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="74233-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74233-185">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="74233-185">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




