---
title: HTML-Schriftart-Fall Back-Verhalten
description: HTML-Schriftart-Fall Back-Verhalten
ms.assetid: 5BDFBD58-0B34-4A58-BFAF-B8BB1DD569DB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc7da95c46190fd348dda72edc8283ee6438b00
ms.sourcegitcommit: 80bac5863880f1bd4c1c3e06db27c5d8fb5232b4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "106338501"
---
# <a name="html-font-fallback-behavior"></a><span data-ttu-id="9bd6a-103">HTML-Schriftart-Fall Back-Verhalten</span><span class="sxs-lookup"><span data-stu-id="9bd6a-103">HTML font fallback behavior</span></span>

## <a name="platform"></a><span data-ttu-id="9bd6a-104">Plattform</span><span class="sxs-lookup"><span data-stu-id="9bd6a-104">Platform</span></span>

<span data-ttu-id="9bd6a-105">Clients-\* \* Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9bd6a-105">Clients -\*\* Windows 8.1</span></span>  
<span data-ttu-id="9bd6a-106">**Server:** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9bd6a-106">**Servers -** Windows Server 2012 R2</span></span>  


## <a name="description"></a><span data-ttu-id="9bd6a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9bd6a-107">Description</span></span>

<span data-ttu-id="9bd6a-108">Microsoft aktualisiert die Logik für UI-Schriftarten für verschiedene Sprachen in Windows Store-Apps mit HTML.</span><span class="sxs-lookup"><span data-stu-id="9bd6a-108">Microsoft is updating the logic for UI fonts for several languages in Windows Store apps using HTML.</span></span> <span data-ttu-id="9bd6a-109">Anstatt eine einzelne Schriftart für alle Sprachen zu verwenden, wird die Benutzeroberflächen Schriftart nun pro Sprache bestimmt.</span><span class="sxs-lookup"><span data-stu-id="9bd6a-109">Rather than using a single font for all languages, the UI font will now be determined on a per language basis.</span></span> <span data-ttu-id="9bd6a-110">Beispielsweise werden UI-Schriftarten für Japanisch nun in apps, die HTML verwenden, in der Benutzeroberfläche "meiryo" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9bd6a-110">For example, UI fonts for Japanese will now be Meiryo UI in apps that use HTML.</span></span>

## <a name="manifestation"></a><span data-ttu-id="9bd6a-111">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="9bd6a-111">Manifestation</span></span>

<span data-ttu-id="9bd6a-112">Apps, die von einer alten Schriftart abhängen, können anders aussehen. während Ihre APP-Darstellung aufgrund lesbarer Schriftarten insgesamt verbessert wird, kann es ein Problem mit Layouts geben, die von Pixel-perfekten Inhalts Größen abhängen.</span><span class="sxs-lookup"><span data-stu-id="9bd6a-112">Apps that depended on an old font may look different; while your app appearance will be improved overall thanks to more readable fonts, there could be an issue with layouts that depend on pixel-perfect content sizes.</span></span> <span data-ttu-id="9bd6a-113">Beispielsweise sind einige Inhalts Zeilen möglicherweise größer als zuvor, was unerwartete Zeilenumbrüche und/oder die Größe von Container Elementen verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="9bd6a-113">For example, some lines of content may be bigger than they were previously, causing unexpected line breaks and/or resizing of container elements.</span></span> <span data-ttu-id="9bd6a-114">In der Praxis wurden jedoch keine Probleme mit vorhandenen apps festgestellt.</span><span class="sxs-lookup"><span data-stu-id="9bd6a-114">However, in practice we haven’t noticed any issues with any existing apps.</span></span>

## <a name="solution"></a><span data-ttu-id="9bd6a-115">Lösung</span><span class="sxs-lookup"><span data-stu-id="9bd6a-115">Solution</span></span>

<span data-ttu-id="9bd6a-116">Betroffene Apps können dieses Verhalten mindern, indem Sie eine bestimmte Schriftart über CSS angeben (z. b. "Font-Family: meiryo UI"), anstatt sich auf die alten Standard Schriftarten zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="9bd6a-116">Affected apps can mitigate this behavior by specifying a given font via CSS (for example, “font-family: Meiryo UI”) instead of relying on the old default fonts.</span></span> <span data-ttu-id="9bd6a-117">In der folgenden Tabelle ist die Benutzeroberflächen Schriftart für jeden der Skriptnamen enthalten.</span><span class="sxs-lookup"><span data-stu-id="9bd6a-117">The following table provides the UI font for each of the script names.</span></span>



| <span data-ttu-id="9bd6a-118">Skriptname</span><span class="sxs-lookup"><span data-stu-id="9bd6a-118">Script Name</span></span>        | <span data-ttu-id="9bd6a-119">Benutzeroberflächen Schriftart</span><span class="sxs-lookup"><span data-stu-id="9bd6a-119">UI Font</span></span>               |
|--------------------|-----------------------|
| <span data-ttu-id="9bd6a-120">Arabisch</span><span class="sxs-lookup"><span data-stu-id="9bd6a-120">Arabic</span></span>             | <span data-ttu-id="9bd6a-121">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="9bd6a-121">Segoe UI</span></span>              |
| <span data-ttu-id="9bd6a-122">Armenisch</span><span class="sxs-lookup"><span data-stu-id="9bd6a-122">Armenian</span></span>           | <span data-ttu-id="9bd6a-123">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="9bd6a-123">Segoe UI</span></span>              |
| <span data-ttu-id="9bd6a-124">Bengali</span><span class="sxs-lookup"><span data-stu-id="9bd6a-124">Bengali</span></span>            | <span data-ttu-id="9bd6a-125">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="9bd6a-125">Nirmala UI</span></span>            |
| <span data-ttu-id="9bd6a-126">Bopomofo</span><span class="sxs-lookup"><span data-stu-id="9bd6a-126">Bopomofo</span></span>           | <span data-ttu-id="9bd6a-127">Microsoft JhengHei UI</span><span class="sxs-lookup"><span data-stu-id="9bd6a-127">Microsoft JhengHei UI</span></span> |
| <span data-ttu-id="9bd6a-128">Braille</span><span class="sxs-lookup"><span data-stu-id="9bd6a-128">Braille</span></span>            | <span data-ttu-id="9bd6a-129">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="9bd6a-129">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="9bd6a-130">Buginesisch</span><span class="sxs-lookup"><span data-stu-id="9bd6a-130">Buginese</span></span>           | <span data-ttu-id="9bd6a-131">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="9bd6a-131">Leelawadee UI</span></span>         |
| <span data-ttu-id="9bd6a-132">Kanadische Silben</span><span class="sxs-lookup"><span data-stu-id="9bd6a-132">Canadian Syllabics</span></span> | <span data-ttu-id="9bd6a-133">Gadugi</span><span class="sxs-lookup"><span data-stu-id="9bd6a-133">Gadugi</span></span>                |
| <span data-ttu-id="9bd6a-134">Cherokee</span><span class="sxs-lookup"><span data-stu-id="9bd6a-134">Cherokee</span></span>           | <span data-ttu-id="9bd6a-135">Gadugi</span><span class="sxs-lookup"><span data-stu-id="9bd6a-135">Gadugi</span></span>                |
| <span data-ttu-id="9bd6a-136">Koptisch</span><span class="sxs-lookup"><span data-stu-id="9bd6a-136">Coptic</span></span>             | <span data-ttu-id="9bd6a-137">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="9bd6a-137">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="9bd6a-138">Han (vereinfacht)</span><span class="sxs-lookup"><span data-stu-id="9bd6a-138">Han (Simplified)</span></span>   | <span data-ttu-id="9bd6a-139">Microsoft YaHei UI</span><span class="sxs-lookup"><span data-stu-id="9bd6a-139">Microsoft YaHei UI</span></span>    |
| <span data-ttu-id="9bd6a-140">Han (traditionell)</span><span class="sxs-lookup"><span data-stu-id="9bd6a-140">Han (Traditional)</span></span>  | <span data-ttu-id="9bd6a-141">Microsoft JhengHei UI</span><span class="sxs-lookup"><span data-stu-id="9bd6a-141">Microsoft JhengHei UI</span></span> |
| <span data-ttu-id="9bd6a-142">Kyrillisch</span><span class="sxs-lookup"><span data-stu-id="9bd6a-142">Cyrillic</span></span>           | <span data-ttu-id="9bd6a-143">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="9bd6a-143">Segoe UI</span></span>              |
| <span data-ttu-id="9bd6a-144">Devanagari</span><span class="sxs-lookup"><span data-stu-id="9bd6a-144">Devanagari</span></span>         | <span data-ttu-id="9bd6a-145">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="9bd6a-145">Nirmala UI</span></span>            |
| <span data-ttu-id="9bd6a-146">Deseret</span><span class="sxs-lookup"><span data-stu-id="9bd6a-146">Deseret</span></span>            | <span data-ttu-id="9bd6a-147">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="9bd6a-147">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="9bd6a-148">Ethiopic</span><span class="sxs-lookup"><span data-stu-id="9bd6a-148">Ethiopic</span></span>           | <span data-ttu-id="9bd6a-149">Ebrima</span><span class="sxs-lookup"><span data-stu-id="9bd6a-149">Ebrima</span></span>                |
| <span data-ttu-id="9bd6a-150">Georgisch</span><span class="sxs-lookup"><span data-stu-id="9bd6a-150">Georgian</span></span>           | <span data-ttu-id="9bd6a-151">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="9bd6a-151">Segoe UI</span></span>              |
| <span data-ttu-id="9bd6a-152">Glagolitisch</span><span class="sxs-lookup"><span data-stu-id="9bd6a-152">Glagolitic</span></span>         | <span data-ttu-id="9bd6a-153">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="9bd6a-153">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="9bd6a-154">Go</span><span class="sxs-lookup"><span data-stu-id="9bd6a-154">Gothic</span></span>             | <span data-ttu-id="9bd6a-155">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="9bd6a-155">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="9bd6a-156">Griechisch</span><span class="sxs-lookup"><span data-stu-id="9bd6a-156">Greek</span></span>              | <span data-ttu-id="9bd6a-157">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="9bd6a-157">Segoe UI</span></span>              |
| <span data-ttu-id="9bd6a-158">Gujarati</span><span class="sxs-lookup"><span data-stu-id="9bd6a-158">Gujarati</span></span>           | <span data-ttu-id="9bd6a-159">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="9bd6a-159">Nirmala UI</span></span>            |
| <span data-ttu-id="9bd6a-160">Gurmukhi</span><span class="sxs-lookup"><span data-stu-id="9bd6a-160">Gurmukhi</span></span>           | <span data-ttu-id="9bd6a-161">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="9bd6a-161">Nirmala UI</span></span>            |
| <span data-ttu-id="9bd6a-162">Hebräisch</span><span class="sxs-lookup"><span data-stu-id="9bd6a-162">Hebrew</span></span>             | <span data-ttu-id="9bd6a-163">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="9bd6a-163">Segoe UI</span></span>              |
| <span data-ttu-id="9bd6a-164">Alte kursiv Formatierung</span><span class="sxs-lookup"><span data-stu-id="9bd6a-164">Old Italic</span></span>         | <span data-ttu-id="9bd6a-165">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="9bd6a-165">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="9bd6a-166">Javanisch</span><span class="sxs-lookup"><span data-stu-id="9bd6a-166">Javanese</span></span>           | <span data-ttu-id="9bd6a-167">Javanese-Text</span><span class="sxs-lookup"><span data-stu-id="9bd6a-167">Javanese Text</span></span>         |
| <span data-ttu-id="9bd6a-168">Japanisch</span><span class="sxs-lookup"><span data-stu-id="9bd6a-168">Japanese</span></span>           | <span data-ttu-id="9bd6a-169">Meiryo-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="9bd6a-169">Meiryo UI</span></span>             |
| <span data-ttu-id="9bd6a-170">Kannada</span><span class="sxs-lookup"><span data-stu-id="9bd6a-170">Kannada</span></span>            | <span data-ttu-id="9bd6a-171">Mirmala-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="9bd6a-171">Mirmala UI</span></span>            |
| <span data-ttu-id="9bd6a-172">Khmer</span><span class="sxs-lookup"><span data-stu-id="9bd6a-172">Khmer</span></span>              | <span data-ttu-id="9bd6a-173">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="9bd6a-173">Leelawadee UI</span></span>         |
| <span data-ttu-id="9bd6a-174">Koreanisch</span><span class="sxs-lookup"><span data-stu-id="9bd6a-174">Korean</span></span>             | <span data-ttu-id="9bd6a-175">Malgun Gothic</span><span class="sxs-lookup"><span data-stu-id="9bd6a-175">Malgun Gothic</span></span>         |
| <span data-ttu-id="9bd6a-176">Laotisch</span><span class="sxs-lookup"><span data-stu-id="9bd6a-176">Lao</span></span>                | <span data-ttu-id="9bd6a-177">Leelawadee</span><span class="sxs-lookup"><span data-stu-id="9bd6a-177">Leelawadee</span></span>            |
| <span data-ttu-id="9bd6a-178">Lateinisch</span><span class="sxs-lookup"><span data-stu-id="9bd6a-178">Latin</span></span>              | <span data-ttu-id="9bd6a-179">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="9bd6a-179">Segoe UI</span></span>              |
| <span data-ttu-id="9bd6a-180">Malayalam</span><span class="sxs-lookup"><span data-stu-id="9bd6a-180">Malayalam</span></span>          | <span data-ttu-id="9bd6a-181">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="9bd6a-181">Nirmala UI</span></span>            |
| <span data-ttu-id="9bd6a-182">Mongolisch</span><span class="sxs-lookup"><span data-stu-id="9bd6a-182">Mongolian</span></span>          | <span data-ttu-id="9bd6a-183">Mongolisches Baiti</span><span class="sxs-lookup"><span data-stu-id="9bd6a-183">Mongolian Baiti</span></span>       |
| <span data-ttu-id="9bd6a-184">Myanmar</span><span class="sxs-lookup"><span data-stu-id="9bd6a-184">Myanmar</span></span>            | <span data-ttu-id="9bd6a-185">Myanmar Text</span><span class="sxs-lookup"><span data-stu-id="9bd6a-185">Myanmar Text</span></span>          |
| <span data-ttu-id="9bd6a-186">N ' Ko</span><span class="sxs-lookup"><span data-stu-id="9bd6a-186">N'Ko</span></span>               | <span data-ttu-id="9bd6a-187">Ebrima</span><span class="sxs-lookup"><span data-stu-id="9bd6a-187">Ebrima</span></span>                |
| <span data-ttu-id="9bd6a-188">Ogam</span><span class="sxs-lookup"><span data-stu-id="9bd6a-188">Ogham</span></span>              | <span data-ttu-id="9bd6a-189">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="9bd6a-189">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="9bd6a-190">Ol Chiki</span><span class="sxs-lookup"><span data-stu-id="9bd6a-190">Ol Chiki</span></span>           | <span data-ttu-id="9bd6a-191">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="9bd6a-191">Nirmala UI</span></span>            |
| <span data-ttu-id="9bd6a-192">Altes Turkisch</span><span class="sxs-lookup"><span data-stu-id="9bd6a-192">Old Turkic</span></span>         | <span data-ttu-id="9bd6a-193">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="9bd6a-193">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="9bd6a-194">Oriya</span><span class="sxs-lookup"><span data-stu-id="9bd6a-194">Oriya</span></span>              | <span data-ttu-id="9bd6a-195">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="9bd6a-195">Nirmala UI</span></span>            |
| <span data-ttu-id="9bd6a-196">Osmanya</span><span class="sxs-lookup"><span data-stu-id="9bd6a-196">Osmanya</span></span>            | <span data-ttu-id="9bd6a-197">Ebrima</span><span class="sxs-lookup"><span data-stu-id="9bd6a-197">Ebrima</span></span>                |
| <span data-ttu-id="9bd6a-198">Phags-pa</span><span class="sxs-lookup"><span data-stu-id="9bd6a-198">Phags-pa</span></span>           | <span data-ttu-id="9bd6a-199">Microsoft PhagsPa</span><span class="sxs-lookup"><span data-stu-id="9bd6a-199">Microsoft PhagsPa</span></span>     |
| <span data-ttu-id="9bd6a-200">Runisch</span><span class="sxs-lookup"><span data-stu-id="9bd6a-200">Runic</span></span>              | <span data-ttu-id="9bd6a-201">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="9bd6a-201">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="9bd6a-202">Sora sompg</span><span class="sxs-lookup"><span data-stu-id="9bd6a-202">Sora Sompeng</span></span>       | <span data-ttu-id="9bd6a-203">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="9bd6a-203">Nirmala UI</span></span>            |
| <span data-ttu-id="9bd6a-204">Singhalesisch</span><span class="sxs-lookup"><span data-stu-id="9bd6a-204">Sinhala</span></span>            | <span data-ttu-id="9bd6a-205">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="9bd6a-205">Nirmala UI</span></span>            |
| <span data-ttu-id="9bd6a-206">Syrisch</span><span class="sxs-lookup"><span data-stu-id="9bd6a-206">Syriac</span></span>             | <span data-ttu-id="9bd6a-207">Estrangelo Edessa</span><span class="sxs-lookup"><span data-stu-id="9bd6a-207">Estrangelo Edessa</span></span>     |
| <span data-ttu-id="9bd6a-208">Tai-Le</span><span class="sxs-lookup"><span data-stu-id="9bd6a-208">Tai Le</span></span>             | <span data-ttu-id="9bd6a-209">Microsoft Tai Le</span><span class="sxs-lookup"><span data-stu-id="9bd6a-209">Microsoft Tai Le</span></span>      |
| <span data-ttu-id="9bd6a-210">Neue Tai-Lue</span><span class="sxs-lookup"><span data-stu-id="9bd6a-210">New Tai Lue</span></span>        | <span data-ttu-id="9bd6a-211">Microsoft Neu-Tai-Lue</span><span class="sxs-lookup"><span data-stu-id="9bd6a-211">Microsoft New Tai Lue</span></span> |
| <span data-ttu-id="9bd6a-212">Tamilisch</span><span class="sxs-lookup"><span data-stu-id="9bd6a-212">Tamil</span></span>              | <span data-ttu-id="9bd6a-213">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="9bd6a-213">Nirmala UI</span></span>            |
| <span data-ttu-id="9bd6a-214">Telugu</span><span class="sxs-lookup"><span data-stu-id="9bd6a-214">Telugu</span></span>             | <span data-ttu-id="9bd6a-215">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="9bd6a-215">Nirmala UI</span></span>            |
| <span data-ttu-id="9bd6a-216">Tifinagh</span><span class="sxs-lookup"><span data-stu-id="9bd6a-216">Tifinagh</span></span>           | <span data-ttu-id="9bd6a-217">Ebrima</span><span class="sxs-lookup"><span data-stu-id="9bd6a-217">Ebrima</span></span>                |
| <span data-ttu-id="9bd6a-218">Thaana</span><span class="sxs-lookup"><span data-stu-id="9bd6a-218">Thaana</span></span>             | <span data-ttu-id="9bd6a-219">MV Boli</span><span class="sxs-lookup"><span data-stu-id="9bd6a-219">MV Boli</span></span>               |
| <span data-ttu-id="9bd6a-220">Thailändisch</span><span class="sxs-lookup"><span data-stu-id="9bd6a-220">Thai</span></span>               | <span data-ttu-id="9bd6a-221">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="9bd6a-221">Leelawadee UI</span></span>         |
| <span data-ttu-id="9bd6a-222">Tibetisch</span><span class="sxs-lookup"><span data-stu-id="9bd6a-222">Tibetan</span></span>            | <span data-ttu-id="9bd6a-223">Microsoft Himalaya</span><span class="sxs-lookup"><span data-stu-id="9bd6a-223">Microsoft Himalaya</span></span>    |
| <span data-ttu-id="9bd6a-224">Vai</span><span class="sxs-lookup"><span data-stu-id="9bd6a-224">Vai</span></span>                | <span data-ttu-id="9bd6a-225">Ebrima</span><span class="sxs-lookup"><span data-stu-id="9bd6a-225">Ebrima</span></span>                |
| <span data-ttu-id="9bd6a-226">Yi</span><span class="sxs-lookup"><span data-stu-id="9bd6a-226">Yi</span></span>                 | <span data-ttu-id="9bd6a-227">Microsoft Yi Baiti</span><span class="sxs-lookup"><span data-stu-id="9bd6a-227">Microsoft Yi Baiti</span></span>    |



 

 

 




