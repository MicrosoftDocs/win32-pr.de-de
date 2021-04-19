---
description: Die Unicode-Teilmenge Bitfeldern (USA) werden in der fontSignature-und der LOCALESIGNATURE-Struktur verwendet.
ms.assetid: f897dfc7-3e78-48dc-8d3d-6929e2f4ec4d
title: Unicode-Teilmenge Bitfields
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fced251b1bf8e04dd4c0d7d7cb0dca15c8bdfa6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364070"
---
# <a name="unicode-subset-bitfields"></a><span data-ttu-id="f8856-103">Unicode-Teilmenge Bitfields</span><span class="sxs-lookup"><span data-stu-id="f8856-103">Unicode Subset Bitfields</span></span>

<span data-ttu-id="f8856-104">Die Unicode-Teilmenge Bitfeldern (USA) werden in der [**fontSignature**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) -und der [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature) -Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8856-104">The Unicode subset bitfields (USBs) are used in the [**FONTSIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) and [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature) structures.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="f8856-105">bit</span><span class="sxs-lookup"><span data-stu-id="f8856-105">Bit</span></span></th>
<th><span data-ttu-id="f8856-106">Unicode-Unterbereich</span><span class="sxs-lookup"><span data-stu-id="f8856-106">Unicode subrange</span></span></th>
<th><span data-ttu-id="f8856-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8856-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f8856-108">0</span><span class="sxs-lookup"><span data-stu-id="f8856-108">0</span></span></td>
<td><span data-ttu-id="f8856-109">0000 - 007F</span><span class="sxs-lookup"><span data-stu-id="f8856-109">0000 - 007F</span></span></td>
<td><span data-ttu-id="f8856-110">Basis-lateinisch</span><span class="sxs-lookup"><span data-stu-id="f8856-110">Basic Latin</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-111">1</span><span class="sxs-lookup"><span data-stu-id="f8856-111">1</span></span></td>
<td><span data-ttu-id="f8856-112">0080 - 00FF</span><span class="sxs-lookup"><span data-stu-id="f8856-112">0080 - 00FF</span></span></td>
<td><span data-ttu-id="f8856-113">Lateinisch-1 Ergänzung</span><span class="sxs-lookup"><span data-stu-id="f8856-113">Latin-1 Supplement</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-114">2</span><span class="sxs-lookup"><span data-stu-id="f8856-114">2</span></span></td>
<td><span data-ttu-id="f8856-115">0100 - 017F</span><span class="sxs-lookup"><span data-stu-id="f8856-115">0100 - 017F</span></span></td>
<td><span data-ttu-id="f8856-116">Lateinisch, erweitert-A</span><span class="sxs-lookup"><span data-stu-id="f8856-116">Latin Extended-A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-117">3</span><span class="sxs-lookup"><span data-stu-id="f8856-117">3</span></span></td>
<td><span data-ttu-id="f8856-118">0180 - 024F</span><span class="sxs-lookup"><span data-stu-id="f8856-118">0180 - 024F</span></span></td>
<td><span data-ttu-id="f8856-119">Lateinisch, erweitert-B</span><span class="sxs-lookup"><span data-stu-id="f8856-119">Latin Extended-B</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="f8856-120">4 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-120">4${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-121">0250 - 02AF</span><span class="sxs-lookup"><span data-stu-id="f8856-121">0250 - 02AF</span></span></td>
<td><span data-ttu-id="f8856-122">IPA-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="f8856-122">IPA Extensions</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-123">1D00 - 1D7F</span><span class="sxs-lookup"><span data-stu-id="f8856-123">1D00 - 1D7F</span></span></td>
<td><span data-ttu-id="f8856-124">Phonetische Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="f8856-124">Phonetic Extensions</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-125">1D80-1dbf</span><span class="sxs-lookup"><span data-stu-id="f8856-125">1D80 - 1DBF</span></span></td>
<td><span data-ttu-id="f8856-126">Ergänzung zu phonetischen Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="f8856-126">Phonetic Extensions Supplement</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="f8856-127">5 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-127">5${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-128">02B0 - 02FF</span><span class="sxs-lookup"><span data-stu-id="f8856-128">02B0 - 02FF</span></span></td>
<td><span data-ttu-id="f8856-129">Abstands-modifiziererbuch staben</span><span class="sxs-lookup"><span data-stu-id="f8856-129">Spacing Modifier Letters</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-130">A700-A71F</span><span class="sxs-lookup"><span data-stu-id="f8856-130">A700 - A71F</span></span></td>
<td><span data-ttu-id="f8856-131">Modifizierertonbuch staben</span><span class="sxs-lookup"><span data-stu-id="f8856-131">Modifier Tone Letters</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="f8856-132">6 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-132">6${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-133">0300 - 036F</span><span class="sxs-lookup"><span data-stu-id="f8856-133">0300 - 036F</span></span></td>
<td><span data-ttu-id="f8856-134">Kombinieren von diakritischen Markierungen</span><span class="sxs-lookup"><span data-stu-id="f8856-134">Combining Diacritical Marks</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-135">1dc0-1 DFF</span><span class="sxs-lookup"><span data-stu-id="f8856-135">1DC0 - 1DFF</span></span></td>
<td><span data-ttu-id="f8856-136">Ergänzen der Ergänzung von diakritischen Markierungen</span><span class="sxs-lookup"><span data-stu-id="f8856-136">Combining Diacritical Marks Supplement</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="f8856-137">7</span><span class="sxs-lookup"><span data-stu-id="f8856-137">7</span></span></td>
<td><span data-ttu-id="f8856-138">0370 - 03FF</span><span class="sxs-lookup"><span data-stu-id="f8856-138">0370 - 03FF</span></span></td>
<td><span data-ttu-id="f8856-139">Griechisch und Koptisch</span><span class="sxs-lookup"><span data-stu-id="f8856-139">Greek and Coptic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-140">8</span><span class="sxs-lookup"><span data-stu-id="f8856-140">8</span></span></td>
<td><span data-ttu-id="f8856-141">2c80-2CFF</span><span class="sxs-lookup"><span data-stu-id="f8856-141">2C80 - 2CFF</span></span></td>
<td><span data-ttu-id="f8856-142">Koptisch</span><span class="sxs-lookup"><span data-stu-id="f8856-142">Coptic</span></span></td>
</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="f8856-143">9 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-143">9${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-144">0400 - 04FF</span><span class="sxs-lookup"><span data-stu-id="f8856-144">0400 - 04FF</span></span></td>
<td><span data-ttu-id="f8856-145">Kyrillisch</span><span class="sxs-lookup"><span data-stu-id="f8856-145">Cyrillic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-146">0500 - 052F</span><span class="sxs-lookup"><span data-stu-id="f8856-146">0500 - 052F</span></span></td>
<td><span data-ttu-id="f8856-147">Cyrillic-Ergänzung</span><span class="sxs-lookup"><span data-stu-id="f8856-147">Cyrillic Supplement</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="f8856-148">2de 0-2dff</span><span class="sxs-lookup"><span data-stu-id="f8856-148">2DE0 - 2DFF</span></span></td>
<td><span data-ttu-id="f8856-149">Kyrillisch erweitert-A</span><span class="sxs-lookup"><span data-stu-id="f8856-149">Cyrillic Extended-A</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-150">A640 - A69F</span><span class="sxs-lookup"><span data-stu-id="f8856-150">A640 - A69F</span></span></td>
<td><span data-ttu-id="f8856-151">Kyrillisch erweitert-B</span><span class="sxs-lookup"><span data-stu-id="f8856-151">Cyrillic Extended-B</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="f8856-152">10</span><span class="sxs-lookup"><span data-stu-id="f8856-152">10</span></span></td>
<td><span data-ttu-id="f8856-153">0530 - 058F</span><span class="sxs-lookup"><span data-stu-id="f8856-153">0530 - 058F</span></span></td>
<td><span data-ttu-id="f8856-154">Armenisch</span><span class="sxs-lookup"><span data-stu-id="f8856-154">Armenian</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-155">11</span><span class="sxs-lookup"><span data-stu-id="f8856-155">11</span></span></td>
<td><span data-ttu-id="f8856-156">0590 - 05FF</span><span class="sxs-lookup"><span data-stu-id="f8856-156">0590 - 05FF</span></span></td>
<td><span data-ttu-id="f8856-157">Hebräisch</span><span class="sxs-lookup"><span data-stu-id="f8856-157">Hebrew</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-158">12</span><span class="sxs-lookup"><span data-stu-id="f8856-158">12</span></span></td>
<td><span data-ttu-id="f8856-159">A500-A63F</span><span class="sxs-lookup"><span data-stu-id="f8856-159">A500 - A63F</span></span></td>
<td><span data-ttu-id="f8856-160">Vai</span><span class="sxs-lookup"><span data-stu-id="f8856-160">Vai</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="f8856-161">13 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-161">13${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-162">0600 - 06FF</span><span class="sxs-lookup"><span data-stu-id="f8856-162">0600 - 06FF</span></span></td>
<td><span data-ttu-id="f8856-163">Arabisch</span><span class="sxs-lookup"><span data-stu-id="f8856-163">Arabic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-164">0750-077f</span><span class="sxs-lookup"><span data-stu-id="f8856-164">0750 - 077F</span></span></td>
<td><span data-ttu-id="f8856-165">Arabische Ergänzung</span><span class="sxs-lookup"><span data-stu-id="f8856-165">Arabic Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-166">14</span><span class="sxs-lookup"><span data-stu-id="f8856-166">14</span></span></td>
<td><span data-ttu-id="f8856-167">07c0-07FF</span><span class="sxs-lookup"><span data-stu-id="f8856-167">07C0 - 07FF</span></span></td>
<td><span data-ttu-id="f8856-168">Nko</span><span class="sxs-lookup"><span data-stu-id="f8856-168">NKo</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-169">15</span><span class="sxs-lookup"><span data-stu-id="f8856-169">15</span></span></td>
<td><span data-ttu-id="f8856-170">0900 - 097F</span><span class="sxs-lookup"><span data-stu-id="f8856-170">0900 - 097F</span></span></td>
<td><span data-ttu-id="f8856-171">Devanagari</span><span class="sxs-lookup"><span data-stu-id="f8856-171">Devanagari</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-172">16</span><span class="sxs-lookup"><span data-stu-id="f8856-172">16</span></span></td>
<td><span data-ttu-id="f8856-173">0980 - 09FF</span><span class="sxs-lookup"><span data-stu-id="f8856-173">0980 - 09FF</span></span></td>
<td><span data-ttu-id="f8856-174">Bengalisch</span><span class="sxs-lookup"><span data-stu-id="f8856-174">Bangla</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-175">17</span><span class="sxs-lookup"><span data-stu-id="f8856-175">17</span></span></td>
<td><span data-ttu-id="f8856-176">0A00 - 0A7F</span><span class="sxs-lookup"><span data-stu-id="f8856-176">0A00 - 0A7F</span></span></td>
<td><span data-ttu-id="f8856-177">Gurmukhi</span><span class="sxs-lookup"><span data-stu-id="f8856-177">Gurmukhi</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-178">18</span><span class="sxs-lookup"><span data-stu-id="f8856-178">18</span></span></td>
<td><span data-ttu-id="f8856-179">0A80 - 0AFF</span><span class="sxs-lookup"><span data-stu-id="f8856-179">0A80 - 0AFF</span></span></td>
<td><span data-ttu-id="f8856-180">Gujarati</span><span class="sxs-lookup"><span data-stu-id="f8856-180">Gujarati</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-181">19</span><span class="sxs-lookup"><span data-stu-id="f8856-181">19</span></span></td>
<td><span data-ttu-id="f8856-182">0B00 - 0B7F</span><span class="sxs-lookup"><span data-stu-id="f8856-182">0B00 - 0B7F</span></span></td>
<td><span data-ttu-id="f8856-183">Odia</span><span class="sxs-lookup"><span data-stu-id="f8856-183">Odia</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-184">20</span><span class="sxs-lookup"><span data-stu-id="f8856-184">20</span></span></td>
<td><span data-ttu-id="f8856-185">0B80 - 0BFF</span><span class="sxs-lookup"><span data-stu-id="f8856-185">0B80 - 0BFF</span></span></td>
<td><span data-ttu-id="f8856-186">Tamilisch</span><span class="sxs-lookup"><span data-stu-id="f8856-186">Tamil</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-187">21</span><span class="sxs-lookup"><span data-stu-id="f8856-187">21</span></span></td>
<td><span data-ttu-id="f8856-188">0C00 - 0C7F</span><span class="sxs-lookup"><span data-stu-id="f8856-188">0C00 - 0C7F</span></span></td>
<td><span data-ttu-id="f8856-189">Telugu</span><span class="sxs-lookup"><span data-stu-id="f8856-189">Telugu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-190">22</span><span class="sxs-lookup"><span data-stu-id="f8856-190">22</span></span></td>
<td><span data-ttu-id="f8856-191">0C80 - 0CFF</span><span class="sxs-lookup"><span data-stu-id="f8856-191">0C80 - 0CFF</span></span></td>
<td><span data-ttu-id="f8856-192">Kannada</span><span class="sxs-lookup"><span data-stu-id="f8856-192">Kannada</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-193">23</span><span class="sxs-lookup"><span data-stu-id="f8856-193">23</span></span></td>
<td><span data-ttu-id="f8856-194">0D00 - 0D7F</span><span class="sxs-lookup"><span data-stu-id="f8856-194">0D00 - 0D7F</span></span></td>
<td><span data-ttu-id="f8856-195">Malayalam</span><span class="sxs-lookup"><span data-stu-id="f8856-195">Malayalam</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-196">24</span><span class="sxs-lookup"><span data-stu-id="f8856-196">24</span></span></td>
<td><span data-ttu-id="f8856-197">0E00 - 0E7F</span><span class="sxs-lookup"><span data-stu-id="f8856-197">0E00 - 0E7F</span></span></td>
<td><span data-ttu-id="f8856-198">Thailändisch</span><span class="sxs-lookup"><span data-stu-id="f8856-198">Thai</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-199">25</span><span class="sxs-lookup"><span data-stu-id="f8856-199">25</span></span></td>
<td><span data-ttu-id="f8856-200">0E80 - 0EFF</span><span class="sxs-lookup"><span data-stu-id="f8856-200">0E80 - 0EFF</span></span></td>
<td><span data-ttu-id="f8856-201">Laotisch</span><span class="sxs-lookup"><span data-stu-id="f8856-201">Lao</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="f8856-202">26 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-202">26${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-203">10A0 - 10FF</span><span class="sxs-lookup"><span data-stu-id="f8856-203">10A0 - 10FF</span></span></td>
<td><span data-ttu-id="f8856-204">Georgisch</span><span class="sxs-lookup"><span data-stu-id="f8856-204">Georgian</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-205">2d00-2d2f</span><span class="sxs-lookup"><span data-stu-id="f8856-205">2D00 - 2D2F</span></span></td>
<td><span data-ttu-id="f8856-206">Georgische Ergänzung</span><span class="sxs-lookup"><span data-stu-id="f8856-206">Georgian Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-207">27</span><span class="sxs-lookup"><span data-stu-id="f8856-207">27</span></span></td>
<td><span data-ttu-id="f8856-208">1b00-1b7f</span><span class="sxs-lookup"><span data-stu-id="f8856-208">1B00 - 1B7F</span></span></td>
<td><span data-ttu-id="f8856-209">Balinesisch</span><span class="sxs-lookup"><span data-stu-id="f8856-209">Balinese</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-210">28</span><span class="sxs-lookup"><span data-stu-id="f8856-210">28</span></span></td>
<td><span data-ttu-id="f8856-211">1100 - 11FF</span><span class="sxs-lookup"><span data-stu-id="f8856-211">1100 - 11FF</span></span></td>
<td><span data-ttu-id="f8856-212">Hangul Jamo</span><span class="sxs-lookup"><span data-stu-id="f8856-212">Hangul Jamo</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="f8856-213">29 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-213">29${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-214">1E00 - 1EFF</span><span class="sxs-lookup"><span data-stu-id="f8856-214">1E00 - 1EFF</span></span></td>
<td><span data-ttu-id="f8856-215">Lateinisch erweitert zusätzlich</span><span class="sxs-lookup"><span data-stu-id="f8856-215">Latin Extended Additional</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-216">2c60-2c7f</span><span class="sxs-lookup"><span data-stu-id="f8856-216">2C60 - 2C7F</span></span></td>
<td><span data-ttu-id="f8856-217">Lateinisch erweitert-C</span><span class="sxs-lookup"><span data-stu-id="f8856-217">Latin Extended-C</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-218">A720 - A7FF</span><span class="sxs-lookup"><span data-stu-id="f8856-218">A720 - A7FF</span></span></td>
<td><span data-ttu-id="f8856-219">Lateinisch, erweitert-D</span><span class="sxs-lookup"><span data-stu-id="f8856-219">Latin Extended-D</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="f8856-220">30</span><span class="sxs-lookup"><span data-stu-id="f8856-220">30</span></span></td>
<td><span data-ttu-id="f8856-221">1F00 - 1FFF</span><span class="sxs-lookup"><span data-stu-id="f8856-221">1F00 - 1FFF</span></span></td>
<td><span data-ttu-id="f8856-222">Griechisch (erweitert)</span><span class="sxs-lookup"><span data-stu-id="f8856-222">Greek Extended</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="f8856-223">31 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-223">31${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-224">2000 - 206F</span><span class="sxs-lookup"><span data-stu-id="f8856-224">2000 - 206F</span></span></td>
<td><span data-ttu-id="f8856-225">Allgemeine Interpunktions Zeichen</span><span class="sxs-lookup"><span data-stu-id="f8856-225">General Punctuation</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-226">2e00-2e7f</span><span class="sxs-lookup"><span data-stu-id="f8856-226">2E00 - 2E7F</span></span></td>
<td><span data-ttu-id="f8856-227">Zusätzliches Interpunktions Zeichen</span><span class="sxs-lookup"><span data-stu-id="f8856-227">Supplemental Punctuation</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-228">32</span><span class="sxs-lookup"><span data-stu-id="f8856-228">32</span></span></td>
<td><span data-ttu-id="f8856-229">2070 - 209F</span><span class="sxs-lookup"><span data-stu-id="f8856-229">2070 - 209F</span></span></td>
<td><span data-ttu-id="f8856-230">Hoch-und tief gestellte Skripts</span><span class="sxs-lookup"><span data-stu-id="f8856-230">Superscripts And Subscripts</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-231">33</span><span class="sxs-lookup"><span data-stu-id="f8856-231">33</span></span></td>
<td><span data-ttu-id="f8856-232">20A0 - 20CF</span><span class="sxs-lookup"><span data-stu-id="f8856-232">20A0 - 20CF</span></span></td>
<td><span data-ttu-id="f8856-233">Währungssymbole</span><span class="sxs-lookup"><span data-stu-id="f8856-233">Currency Symbols</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-234">34</span><span class="sxs-lookup"><span data-stu-id="f8856-234">34</span></span></td>
<td><span data-ttu-id="f8856-235">20D0 - 20FF</span><span class="sxs-lookup"><span data-stu-id="f8856-235">20D0 - 20FF</span></span></td>
<td><span data-ttu-id="f8856-236">Kombinieren von diakritischen Markierungen für Symbole</span><span class="sxs-lookup"><span data-stu-id="f8856-236">Combining Diacritical Marks For Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-237">35</span><span class="sxs-lookup"><span data-stu-id="f8856-237">35</span></span></td>
<td><span data-ttu-id="f8856-238">2100 - 214F</span><span class="sxs-lookup"><span data-stu-id="f8856-238">2100 - 214F</span></span></td>
<td><span data-ttu-id="f8856-239">Letterlike-Symbole</span><span class="sxs-lookup"><span data-stu-id="f8856-239">Letterlike Symbols</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-240">36</span><span class="sxs-lookup"><span data-stu-id="f8856-240">36</span></span></td>
<td><span data-ttu-id="f8856-241">2150 - 218F</span><span class="sxs-lookup"><span data-stu-id="f8856-241">2150 - 218F</span></span></td>
<td><span data-ttu-id="f8856-242">Zahlen Formulare</span><span class="sxs-lookup"><span data-stu-id="f8856-242">Number Forms</span></span></td>
</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="f8856-243">37 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-243">37${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-244">2190 - 21FF</span><span class="sxs-lookup"><span data-stu-id="f8856-244">2190 - 21FF</span></span></td>
<td><span data-ttu-id="f8856-245">Pfeile</span><span class="sxs-lookup"><span data-stu-id="f8856-245">Arrows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-246">27F0 - 27FF</span><span class="sxs-lookup"><span data-stu-id="f8856-246">27F0 - 27FF</span></span></td>
<td><span data-ttu-id="f8856-247">Ergänzende Pfeile-A</span><span class="sxs-lookup"><span data-stu-id="f8856-247">Supplemental Arrows-A</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="f8856-248">2900 - 297F</span><span class="sxs-lookup"><span data-stu-id="f8856-248">2900 - 297F</span></span></td>
<td><span data-ttu-id="f8856-249">Ergänzende Pfeile-B</span><span class="sxs-lookup"><span data-stu-id="f8856-249">Supplemental Arrows-B</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-250">2B00 - 2BFF</span><span class="sxs-lookup"><span data-stu-id="f8856-250">2B00 - 2BFF</span></span></td>
<td><span data-ttu-id="f8856-251">Verschiedene Symbole und Pfeile</span><span class="sxs-lookup"><span data-stu-id="f8856-251">Miscellaneous Symbols and Arrows</span></span></td>

</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="f8856-252">38 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-252">38${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-253">2200 - 22FF</span><span class="sxs-lookup"><span data-stu-id="f8856-253">2200 - 22FF</span></span></td>
<td><span data-ttu-id="f8856-254">Mathematische Operatoren</span><span class="sxs-lookup"><span data-stu-id="f8856-254">Mathematical Operators</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-255">27C0 - 27EF</span><span class="sxs-lookup"><span data-stu-id="f8856-255">27C0 - 27EF</span></span></td>
<td><span data-ttu-id="f8856-256">Verschiedene mathematische Symbole-A</span><span class="sxs-lookup"><span data-stu-id="f8856-256">Miscellaneous Mathematical Symbols-A</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="f8856-257">2980 - 29FF</span><span class="sxs-lookup"><span data-stu-id="f8856-257">2980 - 29FF</span></span></td>
<td><span data-ttu-id="f8856-258">Verschiedene mathematische Symbole-B</span><span class="sxs-lookup"><span data-stu-id="f8856-258">Miscellaneous Mathematical Symbols-B</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-259">2A00 - 2AFF</span><span class="sxs-lookup"><span data-stu-id="f8856-259">2A00 - 2AFF</span></span></td>
<td><span data-ttu-id="f8856-260">Ergänzende mathematische Operatoren</span><span class="sxs-lookup"><span data-stu-id="f8856-260">Supplemental Mathematical Operators</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="f8856-261">39</span><span class="sxs-lookup"><span data-stu-id="f8856-261">39</span></span></td>
<td><span data-ttu-id="f8856-262">2300 - 23FF</span><span class="sxs-lookup"><span data-stu-id="f8856-262">2300 - 23FF</span></span></td>
<td><span data-ttu-id="f8856-263">Sonstige technische</span><span class="sxs-lookup"><span data-stu-id="f8856-263">Miscellaneous Technical</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-264">40</span><span class="sxs-lookup"><span data-stu-id="f8856-264">40</span></span></td>
<td><span data-ttu-id="f8856-265">2400 - 243F</span><span class="sxs-lookup"><span data-stu-id="f8856-265">2400 - 243F</span></span></td>
<td><span data-ttu-id="f8856-266">Steuerelement Bilder</span><span class="sxs-lookup"><span data-stu-id="f8856-266">Control Pictures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-267">41</span><span class="sxs-lookup"><span data-stu-id="f8856-267">41</span></span></td>
<td><span data-ttu-id="f8856-268">2440 - 245F</span><span class="sxs-lookup"><span data-stu-id="f8856-268">2440 - 245F</span></span></td>
<td><span data-ttu-id="f8856-269">Optische Zeichenerkennung</span><span class="sxs-lookup"><span data-stu-id="f8856-269">Optical Character Recognition</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-270">42</span><span class="sxs-lookup"><span data-stu-id="f8856-270">42</span></span></td>
<td><span data-ttu-id="f8856-271">2460 - 24FF</span><span class="sxs-lookup"><span data-stu-id="f8856-271">2460 - 24FF</span></span></td>
<td><span data-ttu-id="f8856-272">Eingeschlossene alphanumerische Zeichen</span><span class="sxs-lookup"><span data-stu-id="f8856-272">Enclosed Alphanumerics</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-273">43</span><span class="sxs-lookup"><span data-stu-id="f8856-273">43</span></span></td>
<td><span data-ttu-id="f8856-274">2500 - 257F</span><span class="sxs-lookup"><span data-stu-id="f8856-274">2500 - 257F</span></span></td>
<td><span data-ttu-id="f8856-275">Box-Zeichnung</span><span class="sxs-lookup"><span data-stu-id="f8856-275">Box Drawing</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-276">44</span><span class="sxs-lookup"><span data-stu-id="f8856-276">44</span></span></td>
<td><span data-ttu-id="f8856-277">2580 - 259F</span><span class="sxs-lookup"><span data-stu-id="f8856-277">2580 - 259F</span></span></td>
<td><span data-ttu-id="f8856-278">Block Elemente</span><span class="sxs-lookup"><span data-stu-id="f8856-278">Block Elements</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-279">45</span><span class="sxs-lookup"><span data-stu-id="f8856-279">45</span></span></td>
<td><span data-ttu-id="f8856-280">25A0 - 25FF</span><span class="sxs-lookup"><span data-stu-id="f8856-280">25A0 - 25FF</span></span></td>
<td><span data-ttu-id="f8856-281">Geometrische Formen</span><span class="sxs-lookup"><span data-stu-id="f8856-281">Geometric Shapes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-282">46</span><span class="sxs-lookup"><span data-stu-id="f8856-282">46</span></span></td>
<td><span data-ttu-id="f8856-283">2600 - 26FF</span><span class="sxs-lookup"><span data-stu-id="f8856-283">2600 - 26FF</span></span></td>
<td><span data-ttu-id="f8856-284">Verschiedene Symbole</span><span class="sxs-lookup"><span data-stu-id="f8856-284">Miscellaneous Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-285">47</span><span class="sxs-lookup"><span data-stu-id="f8856-285">47</span></span></td>
<td><span data-ttu-id="f8856-286">2700 - 27BF</span><span class="sxs-lookup"><span data-stu-id="f8856-286">2700 - 27BF</span></span></td>
<td><span data-ttu-id="f8856-287">Dingbats</span><span class="sxs-lookup"><span data-stu-id="f8856-287">Dingbats</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-288">48</span><span class="sxs-lookup"><span data-stu-id="f8856-288">48</span></span></td>
<td><span data-ttu-id="f8856-289">3000 - 303F</span><span class="sxs-lookup"><span data-stu-id="f8856-289">3000 - 303F</span></span></td>
<td><span data-ttu-id="f8856-290">CJK-Symbole und-Interpunktions Zeichen</span><span class="sxs-lookup"><span data-stu-id="f8856-290">CJK Symbols And Punctuation</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-291">49</span><span class="sxs-lookup"><span data-stu-id="f8856-291">49</span></span></td>
<td><span data-ttu-id="f8856-292">3040 - 309F</span><span class="sxs-lookup"><span data-stu-id="f8856-292">3040 - 309F</span></span></td>
<td><span data-ttu-id="f8856-293">Hiragana</span><span class="sxs-lookup"><span data-stu-id="f8856-293">Hiragana</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="f8856-294">50 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-294">50${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-295">30A0 - 30FF</span><span class="sxs-lookup"><span data-stu-id="f8856-295">30A0 - 30FF</span></span></td>
<td><span data-ttu-id="f8856-296">Katakana</span><span class="sxs-lookup"><span data-stu-id="f8856-296">Katakana</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-297">31F0 - 31FF</span><span class="sxs-lookup"><span data-stu-id="f8856-297">31F0 - 31FF</span></span></td>
<td><span data-ttu-id="f8856-298">Katakana-phonetische Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="f8856-298">Katakana Phonetic Extensions</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="f8856-299">51 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-299">51${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-300">3100 - 312F</span><span class="sxs-lookup"><span data-stu-id="f8856-300">3100 - 312F</span></span></td>
<td><span data-ttu-id="f8856-301">Bopomofo</span><span class="sxs-lookup"><span data-stu-id="f8856-301">Bopomofo</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-302">31A0 - 31BF</span><span class="sxs-lookup"><span data-stu-id="f8856-302">31A0 - 31BF</span></span></td>
<td><span data-ttu-id="f8856-303">Bopomofo erweitert</span><span class="sxs-lookup"><span data-stu-id="f8856-303">Bopomofo Extended</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-304">52</span><span class="sxs-lookup"><span data-stu-id="f8856-304">52</span></span></td>
<td><span data-ttu-id="f8856-305">3130 - 318F</span><span class="sxs-lookup"><span data-stu-id="f8856-305">3130 - 318F</span></span></td>
<td><span data-ttu-id="f8856-306">Hangul Compatibility Jamo</span><span class="sxs-lookup"><span data-stu-id="f8856-306">Hangul Compatibility Jamo</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-307">53</span><span class="sxs-lookup"><span data-stu-id="f8856-307">53</span></span></td>
<td><span data-ttu-id="f8856-308">A840 - A87F</span><span class="sxs-lookup"><span data-stu-id="f8856-308">A840 - A87F</span></span></td>
<td><span data-ttu-id="f8856-309">Phags-pa</span><span class="sxs-lookup"><span data-stu-id="f8856-309">Phags-pa</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-310">54</span><span class="sxs-lookup"><span data-stu-id="f8856-310">54</span></span></td>
<td><span data-ttu-id="f8856-311">3200 - 32FF</span><span class="sxs-lookup"><span data-stu-id="f8856-311">3200 - 32FF</span></span></td>
<td><span data-ttu-id="f8856-312">Eingeschlossene cjk-Buchstaben und Monate</span><span class="sxs-lookup"><span data-stu-id="f8856-312">Enclosed CJK Letters And Months</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-313">55</span><span class="sxs-lookup"><span data-stu-id="f8856-313">55</span></span></td>
<td><span data-ttu-id="f8856-314">3300 - 33FF</span><span class="sxs-lookup"><span data-stu-id="f8856-314">3300 - 33FF</span></span></td>
<td><span data-ttu-id="f8856-315">CJK-Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="f8856-315">CJK Compatibility</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-316">56</span><span class="sxs-lookup"><span data-stu-id="f8856-316">56</span></span></td>
<td><span data-ttu-id="f8856-317">AC00 - D7AF</span><span class="sxs-lookup"><span data-stu-id="f8856-317">AC00 - D7AF</span></span></td>
<td><span data-ttu-id="f8856-318">Hangul-Silben</span><span class="sxs-lookup"><span data-stu-id="f8856-318">Hangul Syllables</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-319">57</span><span class="sxs-lookup"><span data-stu-id="f8856-319">57</span></span></td>
<td><span data-ttu-id="f8856-320">D800 und-DFFF</span><span class="sxs-lookup"><span data-stu-id="f8856-320">D800 - DFFF</span></span></td>
<td><span data-ttu-id="f8856-321">Nicht-Ebene 0.</span><span class="sxs-lookup"><span data-stu-id="f8856-321">Non-Plane 0.</span></span> <span data-ttu-id="f8856-322">Beachten Sie, dass das Festlegen dieses Bits impliziert, dass es mindestens einen ergänzenden Code Punkt gibt, der hinter der von dieser Schriftart unterstützten grundlegenden mehrdimensionalen Ebene (BMP) liegt.</span><span class="sxs-lookup"><span data-stu-id="f8856-322">Note that setting this bit implies that there is at least one supplementary code point beyond the Basic Multilingual Plane (BMP) that is supported by this font.</span></span> <span data-ttu-id="f8856-323">Weitere Informationen finden Sie unter <a href="surrogates-and-supplementary-characters.md">Surrogates und ergänzende Zeichen</a>.</span><span class="sxs-lookup"><span data-stu-id="f8856-323">See <a href="surrogates-and-supplementary-characters.md">Surrogates and Supplementary Characters</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-324">58</span><span class="sxs-lookup"><span data-stu-id="f8856-324">58</span></span></td>
<td><span data-ttu-id="f8856-325">10900-1091f</span><span class="sxs-lookup"><span data-stu-id="f8856-325">10900 - 1091F</span></span></td>
<td><span data-ttu-id="f8856-326">Phönizischen</span><span class="sxs-lookup"><span data-stu-id="f8856-326">Phoenician</span></span></td>
</tr>
<tr class="even">
<td rowspan="7"><span data-ttu-id="f8856-327">59 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-327">59${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-328">2E80 - 2EFF</span><span class="sxs-lookup"><span data-stu-id="f8856-328">2E80 - 2EFF</span></span></td>
<td><span data-ttu-id="f8856-329">Ergänzung zu cjk-radikalen</span><span class="sxs-lookup"><span data-stu-id="f8856-329">CJK Radicals Supplement</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-330">2F00 - 2FDF</span><span class="sxs-lookup"><span data-stu-id="f8856-330">2F00 - 2FDF</span></span></td>
<td><span data-ttu-id="f8856-331">Kangxi-radikale</span><span class="sxs-lookup"><span data-stu-id="f8856-331">Kangxi Radicals</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="f8856-332">2FF0 - 2FFF</span><span class="sxs-lookup"><span data-stu-id="f8856-332">2FF0 - 2FFF</span></span></td>
<td><span data-ttu-id="f8856-333">Ideografische Beschreibungs Zeichen</span><span class="sxs-lookup"><span data-stu-id="f8856-333">Ideographic Description Characters</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-334">3190 - 319F</span><span class="sxs-lookup"><span data-stu-id="f8856-334">3190 - 319F</span></span></td>
<td><span data-ttu-id="f8856-335">Kanbun</span><span class="sxs-lookup"><span data-stu-id="f8856-335">Kanbun</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="f8856-336">3400 - 4DBF</span><span class="sxs-lookup"><span data-stu-id="f8856-336">3400 - 4DBF</span></span></td>
<td><span data-ttu-id="f8856-337">CJK Unified Ideographs Extension A</span><span class="sxs-lookup"><span data-stu-id="f8856-337">CJK Unified Ideographs Extension A</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-338">4E00 - 9FFF</span><span class="sxs-lookup"><span data-stu-id="f8856-338">4E00 - 9FFF</span></span></td>
<td><span data-ttu-id="f8856-339">Einheitliche cjk-Ideographen</span><span class="sxs-lookup"><span data-stu-id="f8856-339">CJK Unified Ideographs</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="f8856-340">20000-2a6df</span><span class="sxs-lookup"><span data-stu-id="f8856-340">20000 - 2A6DF</span></span></td>
<td><span data-ttu-id="f8856-341">CJK Unified Ideographs Extension B</span><span class="sxs-lookup"><span data-stu-id="f8856-341">CJK Unified Ideographs Extension B</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-342">60</span><span class="sxs-lookup"><span data-stu-id="f8856-342">60</span></span></td>
<td><span data-ttu-id="f8856-343">E000 - F8FF</span><span class="sxs-lookup"><span data-stu-id="f8856-343">E000 - F8FF</span></span></td>
<td><span data-ttu-id="f8856-344">Privater Verwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="f8856-344">Private Use Area</span></span></td>
</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="f8856-345">61 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-345">61${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-346">31c0 bis 31ef</span><span class="sxs-lookup"><span data-stu-id="f8856-346">31C0 - 31EF</span></span></td>
<td><span data-ttu-id="f8856-347">CJK-Striche</span><span class="sxs-lookup"><span data-stu-id="f8856-347">CJK Strokes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-348">F900 - FAFF</span><span class="sxs-lookup"><span data-stu-id="f8856-348">F900 - FAFF</span></span></td>
<td><span data-ttu-id="f8856-349">CJK-Kompatibilitäts Ideographs</span><span class="sxs-lookup"><span data-stu-id="f8856-349">CJK Compatibility Ideographs</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="f8856-350">2F 800-2fa1f</span><span class="sxs-lookup"><span data-stu-id="f8856-350">2F800 - 2FA1F</span></span></td>
<td><span data-ttu-id="f8856-351">Ergänzung der CJK-Kompatibilitäts Ideographs</span><span class="sxs-lookup"><span data-stu-id="f8856-351">CJK Compatibility Ideographs Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-352">62</span><span class="sxs-lookup"><span data-stu-id="f8856-352">62</span></span></td>
<td><span data-ttu-id="f8856-353">FB00 - FB4F</span><span class="sxs-lookup"><span data-stu-id="f8856-353">FB00 - FB4F</span></span></td>
<td><span data-ttu-id="f8856-354">Alphabetische Präsentations Formulare</span><span class="sxs-lookup"><span data-stu-id="f8856-354">Alphabetic Presentation Forms</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-355">63</span><span class="sxs-lookup"><span data-stu-id="f8856-355">63</span></span></td>
<td><span data-ttu-id="f8856-356">FB50 - FDFF</span><span class="sxs-lookup"><span data-stu-id="f8856-356">FB50 - FDFF</span></span></td>
<td><span data-ttu-id="f8856-357">Arabische Präsentations Formulare-A</span><span class="sxs-lookup"><span data-stu-id="f8856-357">Arabic Presentation Forms-A</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-358">64</span><span class="sxs-lookup"><span data-stu-id="f8856-358">64</span></span></td>
<td><span data-ttu-id="f8856-359">FE20 - FE2F</span><span class="sxs-lookup"><span data-stu-id="f8856-359">FE20 - FE2F</span></span></td>
<td><span data-ttu-id="f8856-360">Kombinieren von halb Markierungen</span><span class="sxs-lookup"><span data-stu-id="f8856-360">Combining Half Marks</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="f8856-361">65 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-361">65${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-362">FE10 - FE1F</span><span class="sxs-lookup"><span data-stu-id="f8856-362">FE10 - FE1F</span></span></td>
<td><span data-ttu-id="f8856-363">Vertikale Formulare</span><span class="sxs-lookup"><span data-stu-id="f8856-363">Vertical Forms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-364">FE30 - FE4F</span><span class="sxs-lookup"><span data-stu-id="f8856-364">FE30 - FE4F</span></span></td>
<td><span data-ttu-id="f8856-365">CJK-Kompatibilitäts Formulare</span><span class="sxs-lookup"><span data-stu-id="f8856-365">CJK Compatibility Forms</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="f8856-366">66</span><span class="sxs-lookup"><span data-stu-id="f8856-366">66</span></span></td>
<td><span data-ttu-id="f8856-367">FE50 - FE6F</span><span class="sxs-lookup"><span data-stu-id="f8856-367">FE50 - FE6F</span></span></td>
<td><span data-ttu-id="f8856-368">Kleine Formular Varianten</span><span class="sxs-lookup"><span data-stu-id="f8856-368">Small Form Variants</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-369">67</span><span class="sxs-lookup"><span data-stu-id="f8856-369">67</span></span></td>
<td><span data-ttu-id="f8856-370">FE70 - FEFF</span><span class="sxs-lookup"><span data-stu-id="f8856-370">FE70 - FEFF</span></span></td>
<td><span data-ttu-id="f8856-371">Arabische Präsentations Formulare-B</span><span class="sxs-lookup"><span data-stu-id="f8856-371">Arabic Presentation Forms-B</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-372">68</span><span class="sxs-lookup"><span data-stu-id="f8856-372">68</span></span></td>
<td><span data-ttu-id="f8856-373">FF00 - FFEF</span><span class="sxs-lookup"><span data-stu-id="f8856-373">FF00 - FFEF</span></span></td>
<td><span data-ttu-id="f8856-374">Halfwidth-und Fullwidth-Formulare</span><span class="sxs-lookup"><span data-stu-id="f8856-374">Halfwidth And Fullwidth Forms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-375">69</span><span class="sxs-lookup"><span data-stu-id="f8856-375">69</span></span></td>
<td><span data-ttu-id="f8856-376">FFF0 - FFFF</span><span class="sxs-lookup"><span data-stu-id="f8856-376">FFF0 - FFFF</span></span></td>
<td><span data-ttu-id="f8856-377">Spezi</span><span class="sxs-lookup"><span data-stu-id="f8856-377">Specials</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-378">70</span><span class="sxs-lookup"><span data-stu-id="f8856-378">70</span></span></td>
<td><span data-ttu-id="f8856-379">0F00 - 0FFF</span><span class="sxs-lookup"><span data-stu-id="f8856-379">0F00 - 0FFF</span></span></td>
<td><span data-ttu-id="f8856-380">Tibetisch</span><span class="sxs-lookup"><span data-stu-id="f8856-380">Tibetan</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-381">71</span><span class="sxs-lookup"><span data-stu-id="f8856-381">71</span></span></td>
<td><span data-ttu-id="f8856-382">0700 - 074F</span><span class="sxs-lookup"><span data-stu-id="f8856-382">0700 - 074F</span></span></td>
<td><span data-ttu-id="f8856-383">Syrisch</span><span class="sxs-lookup"><span data-stu-id="f8856-383">Syriac</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-384">72</span><span class="sxs-lookup"><span data-stu-id="f8856-384">72</span></span></td>
<td><span data-ttu-id="f8856-385">0780 - 07BF</span><span class="sxs-lookup"><span data-stu-id="f8856-385">0780 - 07BF</span></span></td>
<td><span data-ttu-id="f8856-386">Thaana</span><span class="sxs-lookup"><span data-stu-id="f8856-386">Thaana</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-387">73</span><span class="sxs-lookup"><span data-stu-id="f8856-387">73</span></span></td>
<td><span data-ttu-id="f8856-388">0D80 - 0DFF</span><span class="sxs-lookup"><span data-stu-id="f8856-388">0D80 - 0DFF</span></span></td>
<td><span data-ttu-id="f8856-389">Singhalesisch</span><span class="sxs-lookup"><span data-stu-id="f8856-389">Sinhala</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-390">74</span><span class="sxs-lookup"><span data-stu-id="f8856-390">74</span></span></td>
<td><span data-ttu-id="f8856-391">1000 - 109F</span><span class="sxs-lookup"><span data-stu-id="f8856-391">1000 - 109F</span></span></td>
<td><span data-ttu-id="f8856-392">Myanmar</span><span class="sxs-lookup"><span data-stu-id="f8856-392">Myanmar</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="f8856-393">75 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-393">75${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-394">1200 - 137F</span><span class="sxs-lookup"><span data-stu-id="f8856-394">1200 - 137F</span></span></td>
<td><span data-ttu-id="f8856-395">Ethiopic</span><span class="sxs-lookup"><span data-stu-id="f8856-395">Ethiopic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-396">1380-139 f</span><span class="sxs-lookup"><span data-stu-id="f8856-396">1380 - 139F</span></span></td>
<td><span data-ttu-id="f8856-397">Äthiopische Ergänzung</span><span class="sxs-lookup"><span data-stu-id="f8856-397">Ethiopic Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-398">2d80-2ddf</span><span class="sxs-lookup"><span data-stu-id="f8856-398">2D80 - 2DDF</span></span></td>
<td><span data-ttu-id="f8856-399">Äthiopisch erweitert</span><span class="sxs-lookup"><span data-stu-id="f8856-399">Ethiopic Extended</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="f8856-400">76</span><span class="sxs-lookup"><span data-stu-id="f8856-400">76</span></span></td>
<td><span data-ttu-id="f8856-401">13A0 - 13FF</span><span class="sxs-lookup"><span data-stu-id="f8856-401">13A0 - 13FF</span></span></td>
<td><span data-ttu-id="f8856-402">Cherokee</span><span class="sxs-lookup"><span data-stu-id="f8856-402">Cherokee</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-403">77</span><span class="sxs-lookup"><span data-stu-id="f8856-403">77</span></span></td>
<td><span data-ttu-id="f8856-404">1400 - 167F</span><span class="sxs-lookup"><span data-stu-id="f8856-404">1400 - 167F</span></span></td>
<td><span data-ttu-id="f8856-405">Einheitliche kanadische Aborigines-Silben</span><span class="sxs-lookup"><span data-stu-id="f8856-405">Unified Canadian Aboriginal Syllabics</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-406">78</span><span class="sxs-lookup"><span data-stu-id="f8856-406">78</span></span></td>
<td><span data-ttu-id="f8856-407">1680 - 169F</span><span class="sxs-lookup"><span data-stu-id="f8856-407">1680 - 169F</span></span></td>
<td><span data-ttu-id="f8856-408">Ogam</span><span class="sxs-lookup"><span data-stu-id="f8856-408">Ogham</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-409">79</span><span class="sxs-lookup"><span data-stu-id="f8856-409">79</span></span></td>
<td><span data-ttu-id="f8856-410">16A0 - 16FF</span><span class="sxs-lookup"><span data-stu-id="f8856-410">16A0 - 16FF</span></span></td>
<td><span data-ttu-id="f8856-411">Runisch</span><span class="sxs-lookup"><span data-stu-id="f8856-411">Runic</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="f8856-412">80 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-412">80${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-413">1780 - 17FF</span><span class="sxs-lookup"><span data-stu-id="f8856-413">1780 - 17FF</span></span></td>
<td><span data-ttu-id="f8856-414">Khmer</span><span class="sxs-lookup"><span data-stu-id="f8856-414">Khmer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-415">19E0 - 19FF</span><span class="sxs-lookup"><span data-stu-id="f8856-415">19E0 - 19FF</span></span></td>
<td><span data-ttu-id="f8856-416">Khmer-Symbole</span><span class="sxs-lookup"><span data-stu-id="f8856-416">Khmer Symbols</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="f8856-417">81</span><span class="sxs-lookup"><span data-stu-id="f8856-417">81</span></span></td>
<td><span data-ttu-id="f8856-418">1800 - 18AF</span><span class="sxs-lookup"><span data-stu-id="f8856-418">1800 - 18AF</span></span></td>
<td><span data-ttu-id="f8856-419">Mongolisch</span><span class="sxs-lookup"><span data-stu-id="f8856-419">Mongolian</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-420">82</span><span class="sxs-lookup"><span data-stu-id="f8856-420">82</span></span></td>
<td><span data-ttu-id="f8856-421">2800 - 28FF</span><span class="sxs-lookup"><span data-stu-id="f8856-421">2800 - 28FF</span></span></td>
<td><span data-ttu-id="f8856-422">Braillemuster</span><span class="sxs-lookup"><span data-stu-id="f8856-422">Braille Patterns</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="f8856-423">83 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-423">83${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-424">A000 - A48F</span><span class="sxs-lookup"><span data-stu-id="f8856-424">A000 - A48F</span></span></td>
<td><span data-ttu-id="f8856-425">Yi-Silben</span><span class="sxs-lookup"><span data-stu-id="f8856-425">Yi Syllables</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-426">A490 - A4CF</span><span class="sxs-lookup"><span data-stu-id="f8856-426">A490 - A4CF</span></span></td>
<td><span data-ttu-id="f8856-427">Yi-Radikale</span><span class="sxs-lookup"><span data-stu-id="f8856-427">Yi Radicals</span></span></td>

</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="f8856-428">84 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-428">84${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-429">1700 - 171F</span><span class="sxs-lookup"><span data-stu-id="f8856-429">1700 - 171F</span></span></td>
<td><span data-ttu-id="f8856-430">Tagalog</span><span class="sxs-lookup"><span data-stu-id="f8856-430">Tagalog</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-431">1720 - 173F</span><span class="sxs-lookup"><span data-stu-id="f8856-431">1720 - 173F</span></span></td>
<td><span data-ttu-id="f8856-432">Hanunoo</span><span class="sxs-lookup"><span data-stu-id="f8856-432">Hanunoo</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="f8856-433">1740 - 175F</span><span class="sxs-lookup"><span data-stu-id="f8856-433">1740 - 175F</span></span></td>
<td><span data-ttu-id="f8856-434">Buhid</span><span class="sxs-lookup"><span data-stu-id="f8856-434">Buhid</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-435">1760 - 177F</span><span class="sxs-lookup"><span data-stu-id="f8856-435">1760 - 177F</span></span></td>
<td><span data-ttu-id="f8856-436">Tagbanwa</span><span class="sxs-lookup"><span data-stu-id="f8856-436">Tagbanwa</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="f8856-437">85</span><span class="sxs-lookup"><span data-stu-id="f8856-437">85</span></span></td>
<td><span data-ttu-id="f8856-438">10300-1032f</span><span class="sxs-lookup"><span data-stu-id="f8856-438">10300 - 1032F</span></span></td>
<td><span data-ttu-id="f8856-439">Alte kursiv Formatierung</span><span class="sxs-lookup"><span data-stu-id="f8856-439">Old Italic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-440">86</span><span class="sxs-lookup"><span data-stu-id="f8856-440">86</span></span></td>
<td><span data-ttu-id="f8856-441">10330-1034F</span><span class="sxs-lookup"><span data-stu-id="f8856-441">10330 - 1034F</span></span></td>
<td><span data-ttu-id="f8856-442">Go</span><span class="sxs-lookup"><span data-stu-id="f8856-442">Gothic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-443">87</span><span class="sxs-lookup"><span data-stu-id="f8856-443">87</span></span></td>
<td><span data-ttu-id="f8856-444">10400-1044f</span><span class="sxs-lookup"><span data-stu-id="f8856-444">10400 - 1044F</span></span></td>
<td><span data-ttu-id="f8856-445">Deseret</span><span class="sxs-lookup"><span data-stu-id="f8856-445">Deseret</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="f8856-446">88 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-446">88${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-447">1 D000-1 D0FF</span><span class="sxs-lookup"><span data-stu-id="f8856-447">1D000 - 1D0FF</span></span></td>
<td><span data-ttu-id="f8856-448">Byzantinische Musik Symbole</span><span class="sxs-lookup"><span data-stu-id="f8856-448">Byzantine Musical Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-449">1D100-1D1FF</span><span class="sxs-lookup"><span data-stu-id="f8856-449">1D100 - 1D1FF</span></span></td>
<td><span data-ttu-id="f8856-450">Musik Symbole</span><span class="sxs-lookup"><span data-stu-id="f8856-450">Musical Symbols</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-451">1d200-1d24f</span><span class="sxs-lookup"><span data-stu-id="f8856-451">1D200 - 1D24F</span></span></td>
<td><span data-ttu-id="f8856-452">Alte griechische Musik Notation</span><span class="sxs-lookup"><span data-stu-id="f8856-452">Ancient Greek Musical Notation</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="f8856-453">89</span><span class="sxs-lookup"><span data-stu-id="f8856-453">89</span></span></td>
<td><span data-ttu-id="f8856-454">1d400-1d7ff</span><span class="sxs-lookup"><span data-stu-id="f8856-454">1D400 - 1D7FF</span></span></td>
<td><span data-ttu-id="f8856-455">Mathematische alphanumerische Symbole</span><span class="sxs-lookup"><span data-stu-id="f8856-455">Mathematical Alphanumeric Symbols</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="f8856-456">90 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-456">90${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-457">FF000-ffffd</span><span class="sxs-lookup"><span data-stu-id="f8856-457">FF000 - FFFFD</span></span></td>
<td><span data-ttu-id="f8856-458">Private Verwendung (Ebene 15)</span><span class="sxs-lookup"><span data-stu-id="f8856-458">Private Use (plane 15)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-459">100000-10fffd</span><span class="sxs-lookup"><span data-stu-id="f8856-459">100000 - 10FFFD</span></span></td>
<td><span data-ttu-id="f8856-460">Private Verwendung (Ebene 16)</span><span class="sxs-lookup"><span data-stu-id="f8856-460">Private Use (plane 16)</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="f8856-461">91 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-461">91${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-462">FE00 - FE0F</span><span class="sxs-lookup"><span data-stu-id="f8856-462">FE00 - FE0F</span></span></td>
<td><span data-ttu-id="f8856-463">Variierungsselektoren</span><span class="sxs-lookup"><span data-stu-id="f8856-463">Variation Selectors</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-464">E0100 - E01EF</span><span class="sxs-lookup"><span data-stu-id="f8856-464">E0100 - E01EF</span></span></td>
<td><span data-ttu-id="f8856-465">Ergänzung der variabselectoren</span><span class="sxs-lookup"><span data-stu-id="f8856-465">Variation Selectors Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-466">92</span><span class="sxs-lookup"><span data-stu-id="f8856-466">92</span></span></td>
<td><span data-ttu-id="f8856-467">E0000 - E007F</span><span class="sxs-lookup"><span data-stu-id="f8856-467">E0000 - E007F</span></span></td>
<td><span data-ttu-id="f8856-468">`Tags`</span><span class="sxs-lookup"><span data-stu-id="f8856-468">Tags</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-469">93</span><span class="sxs-lookup"><span data-stu-id="f8856-469">93</span></span></td>
<td><span data-ttu-id="f8856-470">1900 - 194F</span><span class="sxs-lookup"><span data-stu-id="f8856-470">1900 - 194F</span></span></td>
<td><span data-ttu-id="f8856-471">Limbu</span><span class="sxs-lookup"><span data-stu-id="f8856-471">Limbu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-472">94</span><span class="sxs-lookup"><span data-stu-id="f8856-472">94</span></span></td>
<td><span data-ttu-id="f8856-473">1950 - 197F</span><span class="sxs-lookup"><span data-stu-id="f8856-473">1950 - 197F</span></span></td>
<td><span data-ttu-id="f8856-474">Tai-Le</span><span class="sxs-lookup"><span data-stu-id="f8856-474">Tai Le</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-475">95</span><span class="sxs-lookup"><span data-stu-id="f8856-475">95</span></span></td>
<td><span data-ttu-id="f8856-476">1980-19DF</span><span class="sxs-lookup"><span data-stu-id="f8856-476">1980 - 19DF</span></span></td>
<td><span data-ttu-id="f8856-477">Neue Tai-Lue</span><span class="sxs-lookup"><span data-stu-id="f8856-477">New Tai Lue</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-478">96</span><span class="sxs-lookup"><span data-stu-id="f8856-478">96</span></span></td>
<td><span data-ttu-id="f8856-479">1a00-1A1F</span><span class="sxs-lookup"><span data-stu-id="f8856-479">1A00 - 1A1F</span></span></td>
<td><span data-ttu-id="f8856-480">Buginesisch</span><span class="sxs-lookup"><span data-stu-id="f8856-480">Buginese</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-481">97</span><span class="sxs-lookup"><span data-stu-id="f8856-481">97</span></span></td>
<td><span data-ttu-id="f8856-482">2c00-2c5f</span><span class="sxs-lookup"><span data-stu-id="f8856-482">2C00 - 2C5F</span></span></td>
<td><span data-ttu-id="f8856-483">Glagolitisch</span><span class="sxs-lookup"><span data-stu-id="f8856-483">Glagolitic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-484">98</span><span class="sxs-lookup"><span data-stu-id="f8856-484">98</span></span></td>
<td><span data-ttu-id="f8856-485">2D30-2d7f</span><span class="sxs-lookup"><span data-stu-id="f8856-485">2D30 - 2D7F</span></span></td>
<td><span data-ttu-id="f8856-486">Tifinagh</span><span class="sxs-lookup"><span data-stu-id="f8856-486">Tifinagh</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-487">99</span><span class="sxs-lookup"><span data-stu-id="f8856-487">99</span></span></td>
<td><span data-ttu-id="f8856-488">4DC0 - 4DFF</span><span class="sxs-lookup"><span data-stu-id="f8856-488">4DC0 - 4DFF</span></span></td>
<td><span data-ttu-id="f8856-489">Yijing-hexrammsymbole</span><span class="sxs-lookup"><span data-stu-id="f8856-489">Yijing Hexagram Symbols</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-490">100</span><span class="sxs-lookup"><span data-stu-id="f8856-490">100</span></span></td>
<td><span data-ttu-id="f8856-491">A800 - A82F</span><span class="sxs-lookup"><span data-stu-id="f8856-491">A800 - A82F</span></span></td>
<td><span data-ttu-id="f8856-492">Syloti Nagri</span><span class="sxs-lookup"><span data-stu-id="f8856-492">Syloti Nagri</span></span></td>
</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="f8856-493">101 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-493">101${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-494">10000-1007f</span><span class="sxs-lookup"><span data-stu-id="f8856-494">10000 - 1007F</span></span></td>
<td><span data-ttu-id="f8856-495">Lineare B-Silben</span><span class="sxs-lookup"><span data-stu-id="f8856-495">Linear B Syllabary</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-496">10080-100 FF</span><span class="sxs-lookup"><span data-stu-id="f8856-496">10080 - 100FF</span></span></td>
<td><span data-ttu-id="f8856-497">Lineare B-Ideogramme</span><span class="sxs-lookup"><span data-stu-id="f8856-497">Linear B Ideograms</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="f8856-498">10100-1013f</span><span class="sxs-lookup"><span data-stu-id="f8856-498">10100 - 1013F</span></span></td>
<td><span data-ttu-id="f8856-499">Ägäis-Nummern</span><span class="sxs-lookup"><span data-stu-id="f8856-499">Aegean Numbers</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-500">102</span><span class="sxs-lookup"><span data-stu-id="f8856-500">102</span></span></td>
<td><span data-ttu-id="f8856-501">10140-1018f</span><span class="sxs-lookup"><span data-stu-id="f8856-501">10140 - 1018F</span></span></td>
<td><span data-ttu-id="f8856-502">Alte griechische Zahlen</span><span class="sxs-lookup"><span data-stu-id="f8856-502">Ancient Greek Numbers</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-503">103</span><span class="sxs-lookup"><span data-stu-id="f8856-503">103</span></span></td>
<td><span data-ttu-id="f8856-504">10380-1039f</span><span class="sxs-lookup"><span data-stu-id="f8856-504">10380 - 1039F</span></span></td>
<td><span data-ttu-id="f8856-505">Ugaritisch</span><span class="sxs-lookup"><span data-stu-id="f8856-505">Ugaritic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-506">104</span><span class="sxs-lookup"><span data-stu-id="f8856-506">104</span></span></td>
<td><span data-ttu-id="f8856-507">103 a0-103 DF</span><span class="sxs-lookup"><span data-stu-id="f8856-507">103A0 - 103DF</span></span></td>
<td><span data-ttu-id="f8856-508">Alte persische</span><span class="sxs-lookup"><span data-stu-id="f8856-508">Old Persian</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-509">105</span><span class="sxs-lookup"><span data-stu-id="f8856-509">105</span></span></td>
<td><span data-ttu-id="f8856-510">10450-1047f</span><span class="sxs-lookup"><span data-stu-id="f8856-510">10450 - 1047F</span></span></td>
<td><span data-ttu-id="f8856-511">Shavian</span><span class="sxs-lookup"><span data-stu-id="f8856-511">Shavian</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-512">106</span><span class="sxs-lookup"><span data-stu-id="f8856-512">106</span></span></td>
<td><span data-ttu-id="f8856-513">10480-104af</span><span class="sxs-lookup"><span data-stu-id="f8856-513">10480 - 104AF</span></span></td>
<td><span data-ttu-id="f8856-514">Osmanya</span><span class="sxs-lookup"><span data-stu-id="f8856-514">Osmanya</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-515">107</span><span class="sxs-lookup"><span data-stu-id="f8856-515">107</span></span></td>
<td><span data-ttu-id="f8856-516">10800-1083f</span><span class="sxs-lookup"><span data-stu-id="f8856-516">10800 - 1083F</span></span></td>
<td><span data-ttu-id="f8856-517">Zypriotische silabäre</span><span class="sxs-lookup"><span data-stu-id="f8856-517">Cypriot Syllabary</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-518">108</span><span class="sxs-lookup"><span data-stu-id="f8856-518">108</span></span></td>
<td><span data-ttu-id="f8856-519">10a00-10a5f</span><span class="sxs-lookup"><span data-stu-id="f8856-519">10A00 - 10A5F</span></span></td>
<td><span data-ttu-id="f8856-520">Kharoshthi</span><span class="sxs-lookup"><span data-stu-id="f8856-520">Kharoshthi</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-521">109</span><span class="sxs-lookup"><span data-stu-id="f8856-521">109</span></span></td>
<td><span data-ttu-id="f8856-522">1d300-1d35f</span><span class="sxs-lookup"><span data-stu-id="f8856-522">1D300 - 1D35F</span></span></td>
<td><span data-ttu-id="f8856-523">Tai Xuan Jing-Symbole</span><span class="sxs-lookup"><span data-stu-id="f8856-523">Tai Xuan Jing Symbols</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="f8856-524">110 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-524">110${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-525">12000-123FF</span><span class="sxs-lookup"><span data-stu-id="f8856-525">12000 - 123FF</span></span></td>
<td><span data-ttu-id="f8856-526">Cuneiform</span><span class="sxs-lookup"><span data-stu-id="f8856-526">Cuneiform</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-527">12400-1247f</span><span class="sxs-lookup"><span data-stu-id="f8856-527">12400 - 1247F</span></span></td>
<td><span data-ttu-id="f8856-528">Cuneiform-Zahlen und-Satzzeichen</span><span class="sxs-lookup"><span data-stu-id="f8856-528">Cuneiform Numbers and Punctuation</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-529">111</span><span class="sxs-lookup"><span data-stu-id="f8856-529">111</span></span></td>
<td><span data-ttu-id="f8856-530">1d360-1d37f</span><span class="sxs-lookup"><span data-stu-id="f8856-530">1D360 - 1D37F</span></span></td>
<td><span data-ttu-id="f8856-531">Zählen von Strich Ziffern</span><span class="sxs-lookup"><span data-stu-id="f8856-531">Counting Rod Numerals</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-532">112</span><span class="sxs-lookup"><span data-stu-id="f8856-532">112</span></span></td>
<td><span data-ttu-id="f8856-533">1b80-1bbf</span><span class="sxs-lookup"><span data-stu-id="f8856-533">1B80 - 1BBF</span></span></td>
<td><span data-ttu-id="f8856-534">Sundanesisch</span><span class="sxs-lookup"><span data-stu-id="f8856-534">Sundanese</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-535">113</span><span class="sxs-lookup"><span data-stu-id="f8856-535">113</span></span></td>
<td><span data-ttu-id="f8856-536">1c00-1c4f</span><span class="sxs-lookup"><span data-stu-id="f8856-536">1C00 - 1C4F</span></span></td>
<td><span data-ttu-id="f8856-537">Lepcha</span><span class="sxs-lookup"><span data-stu-id="f8856-537">Lepcha</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-538">114</span><span class="sxs-lookup"><span data-stu-id="f8856-538">114</span></span></td>
<td><span data-ttu-id="f8856-539">1c50-1c7f</span><span class="sxs-lookup"><span data-stu-id="f8856-539">1C50 - 1C7F</span></span></td>
<td><span data-ttu-id="f8856-540">Ol Chiki</span><span class="sxs-lookup"><span data-stu-id="f8856-540">Ol Chiki</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-541">115</span><span class="sxs-lookup"><span data-stu-id="f8856-541">115</span></span></td>
<td><span data-ttu-id="f8856-542">A880 - A8DF</span><span class="sxs-lookup"><span data-stu-id="f8856-542">A880 - A8DF</span></span></td>
<td><span data-ttu-id="f8856-543">Saurashtra</span><span class="sxs-lookup"><span data-stu-id="f8856-543">Saurashtra</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-544">116</span><span class="sxs-lookup"><span data-stu-id="f8856-544">116</span></span></td>
<td><span data-ttu-id="f8856-545">A900-A92F</span><span class="sxs-lookup"><span data-stu-id="f8856-545">A900 - A92F</span></span></td>
<td><span data-ttu-id="f8856-546">Kayah Li</span><span class="sxs-lookup"><span data-stu-id="f8856-546">Kayah Li</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-547">117</span><span class="sxs-lookup"><span data-stu-id="f8856-547">117</span></span></td>
<td><span data-ttu-id="f8856-548">A930 - A95F</span><span class="sxs-lookup"><span data-stu-id="f8856-548">A930 - A95F</span></span></td>
<td><span data-ttu-id="f8856-549">Rejang</span><span class="sxs-lookup"><span data-stu-id="f8856-549">Rejang</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-550">118</span><span class="sxs-lookup"><span data-stu-id="f8856-550">118</span></span></td>
<td><span data-ttu-id="f8856-551">AA00 - AA5F</span><span class="sxs-lookup"><span data-stu-id="f8856-551">AA00 - AA5F</span></span></td>
<td><span data-ttu-id="f8856-552">Gar</span><span class="sxs-lookup"><span data-stu-id="f8856-552">Cham</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-553">119</span><span class="sxs-lookup"><span data-stu-id="f8856-553">119</span></span></td>
<td><span data-ttu-id="f8856-554">10190-101 CF</span><span class="sxs-lookup"><span data-stu-id="f8856-554">10190 - 101CF</span></span></td>
<td><span data-ttu-id="f8856-555">Alte Symbole</span><span class="sxs-lookup"><span data-stu-id="f8856-555">Ancient Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-556">120</span><span class="sxs-lookup"><span data-stu-id="f8856-556">120</span></span></td>
<td><span data-ttu-id="f8856-557">101d0-101 ff</span><span class="sxs-lookup"><span data-stu-id="f8856-557">101D0 - 101FF</span></span></td>
<td><span data-ttu-id="f8856-558">Phaistos-CD</span><span class="sxs-lookup"><span data-stu-id="f8856-558">Phaistos Disc</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="f8856-559">121 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-559">121${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-560">10280-1029f</span><span class="sxs-lookup"><span data-stu-id="f8856-560">10280 - 1029F</span></span></td>
<td><span data-ttu-id="f8856-561">Lykisch</span><span class="sxs-lookup"><span data-stu-id="f8856-561">Lycian</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-562">102a0-102df</span><span class="sxs-lookup"><span data-stu-id="f8856-562">102A0 - 102DF</span></span></td>
<td><span data-ttu-id="f8856-563">Karisch</span><span class="sxs-lookup"><span data-stu-id="f8856-563">Carian</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-564">10920-1093f</span><span class="sxs-lookup"><span data-stu-id="f8856-564">10920 - 1093F</span></span></td>
<td><span data-ttu-id="f8856-565">Lydisch</span><span class="sxs-lookup"><span data-stu-id="f8856-565">Lydian</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="f8856-566">122 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8856-566">122${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f8856-567">1F-1F</span><span class="sxs-lookup"><span data-stu-id="f8856-567">1F000 - 1F02F</span></span></td>
<td><span data-ttu-id="f8856-568">Mahjong-Kacheln</span><span class="sxs-lookup"><span data-stu-id="f8856-568">Mahjong Tiles</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-569">1F 030-1F 09F</span><span class="sxs-lookup"><span data-stu-id="f8856-569">1F030 - 1F09F</span></span></td>
<td><span data-ttu-id="f8856-570">Domino-Kacheln</span><span class="sxs-lookup"><span data-stu-id="f8856-570">Domino Tiles</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="f8856-571">123</span><span class="sxs-lookup"><span data-stu-id="f8856-571">123</span></span></td>

<td><span data-ttu-id="f8856-572"><strong>Windows 2000 und höher:</strong> Layoutfortschritt, horizontal von rechts nach links</span><span class="sxs-lookup"><span data-stu-id="f8856-572"><strong>Windows 2000 and later:</strong> Layout progress, horizontal from right to left</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-573">124</span><span class="sxs-lookup"><span data-stu-id="f8856-573">124</span></span></td>

<td><span data-ttu-id="f8856-574"><strong>Windows 2000 und höher:</strong> Layoutfortschritt, vertikal vor horizontal</span><span class="sxs-lookup"><span data-stu-id="f8856-574"><strong>Windows 2000 and later:</strong> Layout progress, vertical before horizontal</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8856-575">125</span><span class="sxs-lookup"><span data-stu-id="f8856-575">125</span></span></td>

<td><span data-ttu-id="f8856-576"><strong>Windows 2000 und höher:</strong> Layoutfortschritt, vertikal von unten nach oben</span><span class="sxs-lookup"><span data-stu-id="f8856-576"><strong>Windows 2000 and later:</strong> Layout progress, vertical bottom to top</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8856-577">126-127</span><span class="sxs-lookup"><span data-stu-id="f8856-577">126-127</span></span></td>

<td><span data-ttu-id="f8856-578">Reserviert für Prozess interne Verwendung</span><span class="sxs-lookup"><span data-stu-id="f8856-578">Reserved for process-internal usage</span></span></td>
</tr>
</tbody>
</table>



 

 

 



