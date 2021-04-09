---
title: Varfileingefo-Block Anweisung
description: Beschreibt die Form des Variablen Informations Blocks.
ms.assetid: 81c7f5df-78fa-4571-9dad-a6c3e932471e
keywords:
- Menüs der varfilanfo-Block Anweisung und weitere Ressourcen
topic_type:
- apiref
api_name:
- VarFileInfo BLOCK
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09645801618de130439bdf1998b92183e4791783
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038136"
---
# <a name="varfileinfo-block-statement"></a><span data-ttu-id="44867-104">Varfileingefo-Block Anweisung</span><span class="sxs-lookup"><span data-stu-id="44867-104">VarFileInfo BLOCK statement</span></span>

<span data-ttu-id="44867-105">Definiert einen Variablen Informationsblock.</span><span class="sxs-lookup"><span data-stu-id="44867-105">Defines a variable information block.</span></span>

``` syntax
BLOCK "VarFileInfo" { VALUE "Translation", langID, charsetID . . . }
```

## <a name="parameters"></a><span data-ttu-id="44867-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="44867-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44867-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span><span class="sxs-lookup"><span data-stu-id="44867-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="44867-108">Einer der sprach Bezeichner, der im Abschnitt "Hinweise" angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="44867-108">One of the language identifiers specified in the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="44867-109"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charder TID*</span><span class="sxs-lookup"><span data-stu-id="44867-109"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*</span></span>
</dt> <dd>

<span data-ttu-id="44867-110">Einer der Zeichensatz Bezeichner, der im Abschnitt "Hinweise" angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="44867-110">One of the character-set identifiers specified in the Remarks section.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44867-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44867-111">Remarks</span></span>

<span data-ttu-id="44867-112">Es können mehr als ein Bezeichnerpaar angegeben werden, aber jedes Paar muss durch ein Komma vom vorangehenden paar getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="44867-112">More than one identifier pair can be given, but each pair must be separated from the preceding pair with a comma.</span></span>

<span data-ttu-id="44867-113">Der *LangID* -Parameter gibt einen der folgenden Sprachcodes an.</span><span class="sxs-lookup"><span data-stu-id="44867-113">The *langID* parameter specifies one of the following language codes.</span></span>



| <span data-ttu-id="44867-114">Code</span><span class="sxs-lookup"><span data-stu-id="44867-114">Code</span></span>   | <span data-ttu-id="44867-115">Sprache</span><span class="sxs-lookup"><span data-stu-id="44867-115">Language</span></span>            | <span data-ttu-id="44867-116">Code</span><span class="sxs-lookup"><span data-stu-id="44867-116">Code</span></span>   | <span data-ttu-id="44867-117">Sprache</span><span class="sxs-lookup"><span data-stu-id="44867-117">Language</span></span>                  |
|--------|---------------------|--------|---------------------------|
| <span data-ttu-id="44867-118">0x0401</span><span class="sxs-lookup"><span data-stu-id="44867-118">0x0401</span></span> | <span data-ttu-id="44867-119">Arabisch</span><span class="sxs-lookup"><span data-stu-id="44867-119">Arabic</span></span>              | <span data-ttu-id="44867-120">0x0415</span><span class="sxs-lookup"><span data-stu-id="44867-120">0x0415</span></span> | <span data-ttu-id="44867-121">Polnisch</span><span class="sxs-lookup"><span data-stu-id="44867-121">Polish</span></span>                    |
| <span data-ttu-id="44867-122">0x0402</span><span class="sxs-lookup"><span data-stu-id="44867-122">0x0402</span></span> | <span data-ttu-id="44867-123">Bulgarisch</span><span class="sxs-lookup"><span data-stu-id="44867-123">Bulgarian</span></span>           | <span data-ttu-id="44867-124">0x0416</span><span class="sxs-lookup"><span data-stu-id="44867-124">0x0416</span></span> | <span data-ttu-id="44867-125">Portugiesisch (Brasilien)</span><span class="sxs-lookup"><span data-stu-id="44867-125">Portuguese (Brazil)</span></span>       |
| <span data-ttu-id="44867-126">0x0403</span><span class="sxs-lookup"><span data-stu-id="44867-126">0x0403</span></span> | <span data-ttu-id="44867-127">Katalanisch</span><span class="sxs-lookup"><span data-stu-id="44867-127">Catalan</span></span>             | <span data-ttu-id="44867-128">0x0417</span><span class="sxs-lookup"><span data-stu-id="44867-128">0x0417</span></span> | <span data-ttu-id="44867-129">Rhaeto-Romanic</span><span class="sxs-lookup"><span data-stu-id="44867-129">Rhaeto-Romanic</span></span>            |
| <span data-ttu-id="44867-130">0x0404</span><span class="sxs-lookup"><span data-stu-id="44867-130">0x0404</span></span> | <span data-ttu-id="44867-131">Chinesisch (traditionell)</span><span class="sxs-lookup"><span data-stu-id="44867-131">Traditional Chinese</span></span> | <span data-ttu-id="44867-132">0x0418</span><span class="sxs-lookup"><span data-stu-id="44867-132">0x0418</span></span> | <span data-ttu-id="44867-133">Rumänisch</span><span class="sxs-lookup"><span data-stu-id="44867-133">Romanian</span></span>                  |
| <span data-ttu-id="44867-134">0x0405</span><span class="sxs-lookup"><span data-stu-id="44867-134">0x0405</span></span> | <span data-ttu-id="44867-135">Tschechisch</span><span class="sxs-lookup"><span data-stu-id="44867-135">Czech</span></span>               | <span data-ttu-id="44867-136">0x0419</span><span class="sxs-lookup"><span data-stu-id="44867-136">0x0419</span></span> | <span data-ttu-id="44867-137">Russisch</span><span class="sxs-lookup"><span data-stu-id="44867-137">Russian</span></span>                   |
| <span data-ttu-id="44867-138">0x0406</span><span class="sxs-lookup"><span data-stu-id="44867-138">0x0406</span></span> | <span data-ttu-id="44867-139">Dänisch</span><span class="sxs-lookup"><span data-stu-id="44867-139">Danish</span></span>              | <span data-ttu-id="44867-140">0x041a</span><span class="sxs-lookup"><span data-stu-id="44867-140">0x041A</span></span> | <span data-ttu-id="44867-141">Croato-Serbian (lateinisch)</span><span class="sxs-lookup"><span data-stu-id="44867-141">Croato-Serbian (Latin)</span></span>    |
| <span data-ttu-id="44867-142">0x0407</span><span class="sxs-lookup"><span data-stu-id="44867-142">0x0407</span></span> | <span data-ttu-id="44867-143">Deutsch</span><span class="sxs-lookup"><span data-stu-id="44867-143">German</span></span>              | <span data-ttu-id="44867-144">0x041b</span><span class="sxs-lookup"><span data-stu-id="44867-144">0x041B</span></span> | <span data-ttu-id="44867-145">Slowakisch</span><span class="sxs-lookup"><span data-stu-id="44867-145">Slovak</span></span>                    |
| <span data-ttu-id="44867-146">0x0408</span><span class="sxs-lookup"><span data-stu-id="44867-146">0x0408</span></span> | <span data-ttu-id="44867-147">Griechisch</span><span class="sxs-lookup"><span data-stu-id="44867-147">Greek</span></span>               | <span data-ttu-id="44867-148">0x041c</span><span class="sxs-lookup"><span data-stu-id="44867-148">0x041C</span></span> | <span data-ttu-id="44867-149">Albanisch</span><span class="sxs-lookup"><span data-stu-id="44867-149">Albanian</span></span>                  |
| <span data-ttu-id="44867-150">0x0409</span><span class="sxs-lookup"><span data-stu-id="44867-150">0x0409</span></span> | <span data-ttu-id="44867-151">US-Englisch</span><span class="sxs-lookup"><span data-stu-id="44867-151">U.S. English</span></span>        | <span data-ttu-id="44867-152">0x041d</span><span class="sxs-lookup"><span data-stu-id="44867-152">0x041D</span></span> | <span data-ttu-id="44867-153">Schwedisch</span><span class="sxs-lookup"><span data-stu-id="44867-153">Swedish</span></span>                   |
| <span data-ttu-id="44867-154">0x040A</span><span class="sxs-lookup"><span data-stu-id="44867-154">0x040A</span></span> | <span data-ttu-id="44867-155">Castilisch Spanisch</span><span class="sxs-lookup"><span data-stu-id="44867-155">Castilian Spanish</span></span>   | <span data-ttu-id="44867-156">0x041E</span><span class="sxs-lookup"><span data-stu-id="44867-156">0x041E</span></span> | <span data-ttu-id="44867-157">Thailändisch</span><span class="sxs-lookup"><span data-stu-id="44867-157">Thai</span></span>                      |
| <span data-ttu-id="44867-158">0x040b</span><span class="sxs-lookup"><span data-stu-id="44867-158">0x040B</span></span> | <span data-ttu-id="44867-159">Finnisch</span><span class="sxs-lookup"><span data-stu-id="44867-159">Finnish</span></span>             | <span data-ttu-id="44867-160">0x041f</span><span class="sxs-lookup"><span data-stu-id="44867-160">0x041F</span></span> | <span data-ttu-id="44867-161">Türkisch</span><span class="sxs-lookup"><span data-stu-id="44867-161">Turkish</span></span>                   |
| <span data-ttu-id="44867-162">0x040c</span><span class="sxs-lookup"><span data-stu-id="44867-162">0x040C</span></span> | <span data-ttu-id="44867-163">Französisch</span><span class="sxs-lookup"><span data-stu-id="44867-163">French</span></span>              | <span data-ttu-id="44867-164">0x0420</span><span class="sxs-lookup"><span data-stu-id="44867-164">0x0420</span></span> | <span data-ttu-id="44867-165">Urdu</span><span class="sxs-lookup"><span data-stu-id="44867-165">Urdu</span></span>                      |
| <span data-ttu-id="44867-166">0x040d</span><span class="sxs-lookup"><span data-stu-id="44867-166">0x040D</span></span> | <span data-ttu-id="44867-167">Hebräisch</span><span class="sxs-lookup"><span data-stu-id="44867-167">Hebrew</span></span>              | <span data-ttu-id="44867-168">0x0421</span><span class="sxs-lookup"><span data-stu-id="44867-168">0x0421</span></span> | <span data-ttu-id="44867-169">Bahasa</span><span class="sxs-lookup"><span data-stu-id="44867-169">Bahasa</span></span>                    |
| <span data-ttu-id="44867-170">0x040e</span><span class="sxs-lookup"><span data-stu-id="44867-170">0x040E</span></span> | <span data-ttu-id="44867-171">Ungarisch</span><span class="sxs-lookup"><span data-stu-id="44867-171">Hungarian</span></span>           | <span data-ttu-id="44867-172">0x0804</span><span class="sxs-lookup"><span data-stu-id="44867-172">0x0804</span></span> | <span data-ttu-id="44867-173">Chinesisch (vereinfacht)</span><span class="sxs-lookup"><span data-stu-id="44867-173">Simplified Chinese</span></span>        |
| <span data-ttu-id="44867-174">0x040f</span><span class="sxs-lookup"><span data-stu-id="44867-174">0x040F</span></span> | <span data-ttu-id="44867-175">Isländisch</span><span class="sxs-lookup"><span data-stu-id="44867-175">Icelandic</span></span>           | <span data-ttu-id="44867-176">0x0807</span><span class="sxs-lookup"><span data-stu-id="44867-176">0x0807</span></span> | <span data-ttu-id="44867-177">Deutsch (Schweiz)</span><span class="sxs-lookup"><span data-stu-id="44867-177">Swiss German</span></span>              |
| <span data-ttu-id="44867-178">0x0410</span><span class="sxs-lookup"><span data-stu-id="44867-178">0x0410</span></span> | <span data-ttu-id="44867-179">Italienisch</span><span class="sxs-lookup"><span data-stu-id="44867-179">Italian</span></span>             | <span data-ttu-id="44867-180">0x0809</span><span class="sxs-lookup"><span data-stu-id="44867-180">0x0809</span></span> | <span data-ttu-id="44867-181">Vereinigtes Königreich:</span><span class="sxs-lookup"><span data-stu-id="44867-181">U.K.</span></span> <span data-ttu-id="44867-182">Englisch</span><span class="sxs-lookup"><span data-stu-id="44867-182">English</span></span>              |
| <span data-ttu-id="44867-183">0x0411</span><span class="sxs-lookup"><span data-stu-id="44867-183">0x0411</span></span> | <span data-ttu-id="44867-184">Japanisch</span><span class="sxs-lookup"><span data-stu-id="44867-184">Japanese</span></span>            | <span data-ttu-id="44867-185">0x080a</span><span class="sxs-lookup"><span data-stu-id="44867-185">0x080A</span></span> | <span data-ttu-id="44867-186">Spanisch (Mexiko)</span><span class="sxs-lookup"><span data-stu-id="44867-186">Spanish (Mexico)</span></span>          |
| <span data-ttu-id="44867-187">0x0412</span><span class="sxs-lookup"><span data-stu-id="44867-187">0x0412</span></span> | <span data-ttu-id="44867-188">Koreanisch</span><span class="sxs-lookup"><span data-stu-id="44867-188">Korean</span></span>              | <span data-ttu-id="44867-189">0x080c</span><span class="sxs-lookup"><span data-stu-id="44867-189">0x080C</span></span> | <span data-ttu-id="44867-190">Französisch (Belgien)</span><span class="sxs-lookup"><span data-stu-id="44867-190">Belgian French</span></span>            |
| <span data-ttu-id="44867-191">0x0413</span><span class="sxs-lookup"><span data-stu-id="44867-191">0x0413</span></span> | <span data-ttu-id="44867-192">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="44867-192">Dutch</span></span>               | <span data-ttu-id="44867-193">0x0c0c</span><span class="sxs-lookup"><span data-stu-id="44867-193">0x0C0C</span></span> | <span data-ttu-id="44867-194">Französisch (Kanada)</span><span class="sxs-lookup"><span data-stu-id="44867-194">Canadian French</span></span>           |
| <span data-ttu-id="44867-195">0x0414</span><span class="sxs-lookup"><span data-stu-id="44867-195">0x0414</span></span> | <span data-ttu-id="44867-196">Norwegisch – Bokmal</span><span class="sxs-lookup"><span data-stu-id="44867-196">Norwegian – Bokmal</span></span>  | <span data-ttu-id="44867-197">0x100c</span><span class="sxs-lookup"><span data-stu-id="44867-197">0x100C</span></span> | <span data-ttu-id="44867-198">Schweiz Französisch</span><span class="sxs-lookup"><span data-stu-id="44867-198">Swiss French</span></span>              |
| <span data-ttu-id="44867-199">0x0810</span><span class="sxs-lookup"><span data-stu-id="44867-199">0x0810</span></span> | <span data-ttu-id="44867-200">Schweizer Italienisch</span><span class="sxs-lookup"><span data-stu-id="44867-200">Swiss Italian</span></span>       | <span data-ttu-id="44867-201">0x0816</span><span class="sxs-lookup"><span data-stu-id="44867-201">0x0816</span></span> | <span data-ttu-id="44867-202">Portugiesisch (Portugal)</span><span class="sxs-lookup"><span data-stu-id="44867-202">Portuguese (Portugal)</span></span>     |
| <span data-ttu-id="44867-203">0x0813</span><span class="sxs-lookup"><span data-stu-id="44867-203">0x0813</span></span> | <span data-ttu-id="44867-204">Belgisch Niederländisch</span><span class="sxs-lookup"><span data-stu-id="44867-204">Belgian Dutch</span></span>       | <span data-ttu-id="44867-205">0x081a</span><span class="sxs-lookup"><span data-stu-id="44867-205">0x081A</span></span> | <span data-ttu-id="44867-206">Serbo-Croatian (Kyrillisch)</span><span class="sxs-lookup"><span data-stu-id="44867-206">Serbo-Croatian (Cyrillic)</span></span> |
| <span data-ttu-id="44867-207">0x0814</span><span class="sxs-lookup"><span data-stu-id="44867-207">0x0814</span></span> | <span data-ttu-id="44867-208">Norwegisch – Nynorsk</span><span class="sxs-lookup"><span data-stu-id="44867-208">Norwegian – Nynorsk</span></span> | <span data-ttu-id="44867-209">?</span><span class="sxs-lookup"><span data-stu-id="44867-209">?</span></span>      | <span data-ttu-id="44867-210">?</span><span class="sxs-lookup"><span data-stu-id="44867-210">?</span></span>                         |



 

<span data-ttu-id="44867-211">Der *charsetid* -Parameter gibt einen der folgenden Zeichensatz Bezeichner an:</span><span class="sxs-lookup"><span data-stu-id="44867-211">The *charsetID* parameter specifies one of the following character-set identifiers:</span></span>



| <span data-ttu-id="44867-212">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="44867-212">Identifier</span></span> | <span data-ttu-id="44867-213">Zeichensatz</span><span class="sxs-lookup"><span data-stu-id="44867-213">Character Set</span></span>              |
|------------|----------------------------|
| <span data-ttu-id="44867-214">0</span><span class="sxs-lookup"><span data-stu-id="44867-214">0</span></span>          | <span data-ttu-id="44867-215">7-Bit-ASCII</span><span class="sxs-lookup"><span data-stu-id="44867-215">7-bit ASCII</span></span>                |
| <span data-ttu-id="44867-216">932</span><span class="sxs-lookup"><span data-stu-id="44867-216">932</span></span>        | <span data-ttu-id="44867-217">Japan (Shift – JIS X-0208)</span><span class="sxs-lookup"><span data-stu-id="44867-217">Japan (Shift – JIS X-0208)</span></span> |
| <span data-ttu-id="44867-218">949</span><span class="sxs-lookup"><span data-stu-id="44867-218">949</span></span>        | <span data-ttu-id="44867-219">Korea (Shift – KSC 5601)</span><span class="sxs-lookup"><span data-stu-id="44867-219">Korea (Shift – KSC 5601)</span></span>   |
| <span data-ttu-id="44867-220">950</span><span class="sxs-lookup"><span data-stu-id="44867-220">950</span></span>        | <span data-ttu-id="44867-221">Taiwan (Big5)</span><span class="sxs-lookup"><span data-stu-id="44867-221">Taiwan (Big5)</span></span>              |
| <span data-ttu-id="44867-222">1200</span><span class="sxs-lookup"><span data-stu-id="44867-222">1200</span></span>       | <span data-ttu-id="44867-223">Unicode</span><span class="sxs-lookup"><span data-stu-id="44867-223">Unicode</span></span>                    |
| <span data-ttu-id="44867-224">1250</span><span class="sxs-lookup"><span data-stu-id="44867-224">1250</span></span>       | <span data-ttu-id="44867-225">Lateinisch-2 (Osteuropäisch)</span><span class="sxs-lookup"><span data-stu-id="44867-225">Latin-2 (Eastern European)</span></span> |
| <span data-ttu-id="44867-226">1251</span><span class="sxs-lookup"><span data-stu-id="44867-226">1251</span></span>       | <span data-ttu-id="44867-227">Kyrillisch</span><span class="sxs-lookup"><span data-stu-id="44867-227">Cyrillic</span></span>                   |
| <span data-ttu-id="44867-228">1252</span><span class="sxs-lookup"><span data-stu-id="44867-228">1252</span></span>       | <span data-ttu-id="44867-229">Mehrsprachige</span><span class="sxs-lookup"><span data-stu-id="44867-229">Multilingual</span></span>               |
| <span data-ttu-id="44867-230">1253</span><span class="sxs-lookup"><span data-stu-id="44867-230">1253</span></span>       | <span data-ttu-id="44867-231">Griechisch</span><span class="sxs-lookup"><span data-stu-id="44867-231">Greek</span></span>                      |
| <span data-ttu-id="44867-232">1254</span><span class="sxs-lookup"><span data-stu-id="44867-232">1254</span></span>       | <span data-ttu-id="44867-233">Türkisch</span><span class="sxs-lookup"><span data-stu-id="44867-233">Turkish</span></span>                    |
| <span data-ttu-id="44867-234">1255</span><span class="sxs-lookup"><span data-stu-id="44867-234">1255</span></span>       | <span data-ttu-id="44867-235">Hebräisch</span><span class="sxs-lookup"><span data-stu-id="44867-235">Hebrew</span></span>                     |
| <span data-ttu-id="44867-236">1256</span><span class="sxs-lookup"><span data-stu-id="44867-236">1256</span></span>       | <span data-ttu-id="44867-237">Arabisch</span><span class="sxs-lookup"><span data-stu-id="44867-237">Arabic</span></span>                     |



 

 

 




