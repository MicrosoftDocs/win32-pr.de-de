---
title: Iagentcharakteriex getlanguageid
description: Iagentcharakteriex getlanguageid
ms.assetid: 4e4e5342-edf9-480b-a9c3-e2626fd89e76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9679538f93d779acc6272dccada824585c4449f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037319"
---
# <a name="iagentcharacterexgetlanguageid"></a><span data-ttu-id="afda8-103">Iagentcharakteriex:: getlanguageid</span><span class="sxs-lookup"><span data-stu-id="afda8-103">IAgentCharacterEx::GetLanguageID</span></span>

<span data-ttu-id="afda8-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="afda8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetLanguageID(
   long * plangID  // address of language ID setting
);
```

<span data-ttu-id="afda8-105">Ruft die Sprachen-ID ab, die für das Zeichen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="afda8-105">Retrieves the language ID set for the character.</span></span>

-   <span data-ttu-id="afda8-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="afda8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="afda8-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangid*</span><span class="sxs-lookup"><span data-stu-id="afda8-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span></span>
</dt> <dd>

<span data-ttu-id="afda8-108">Adresse einer Variablen, die die Sprach-ID-Einstellung für das Zeichen empfängt.</span><span class="sxs-lookup"><span data-stu-id="afda8-108">Address of a variable that receives the language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="afda8-109">Eine lange ganze Zahl, die die Sprach-ID für das Zeichen angibt.</span><span class="sxs-lookup"><span data-stu-id="afda8-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="afda8-110">Die Sprach-ID (langid) für ein Zeichen ist ein 16-Bit-Wert, der von Windows definiert wird und aus einer primär Sprachen-ID und einer sekundären Sprach-ID besteht.</span><span class="sxs-lookup"><span data-stu-id="afda8-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="afda8-111">Die folgenden Beispiele sind Werte für einige Sprachen.</span><span class="sxs-lookup"><span data-stu-id="afda8-111">The following examples are values for some languages.</span></span> <span data-ttu-id="afda8-112">Informationen zum Bestimmen der Werte anderer Sprachen finden Sie in der Platform SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="afda8-112">To determine the values other languages, see the Platform SDK documentation.</span></span>



|                       |        |                       |        |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="afda8-113">Arabisch (Saudi)</span><span class="sxs-lookup"><span data-stu-id="afda8-113">Arabic (Saudi)</span></span>        | <span data-ttu-id="afda8-114">0x0401</span><span class="sxs-lookup"><span data-stu-id="afda8-114">0x0401</span></span> | <span data-ttu-id="afda8-115">Italienisch</span><span class="sxs-lookup"><span data-stu-id="afda8-115">Italian</span></span>               | <span data-ttu-id="afda8-116">0x0410</span><span class="sxs-lookup"><span data-stu-id="afda8-116">0x0410</span></span> |
| <span data-ttu-id="afda8-117">Baskisch</span><span class="sxs-lookup"><span data-stu-id="afda8-117">Basque</span></span>                | <span data-ttu-id="afda8-118">0x042d</span><span class="sxs-lookup"><span data-stu-id="afda8-118">0x042d</span></span> | <span data-ttu-id="afda8-119">Japanisch</span><span class="sxs-lookup"><span data-stu-id="afda8-119">Japanese</span></span>              | <span data-ttu-id="afda8-120">0x0411</span><span class="sxs-lookup"><span data-stu-id="afda8-120">0x0411</span></span> |
| <span data-ttu-id="afda8-121">Chinesisch (vereinfacht)</span><span class="sxs-lookup"><span data-stu-id="afda8-121">Chinese (Simplified)</span></span>  | <span data-ttu-id="afda8-122">0x0804</span><span class="sxs-lookup"><span data-stu-id="afda8-122">0x0804</span></span> | <span data-ttu-id="afda8-123">Koreanisch</span><span class="sxs-lookup"><span data-stu-id="afda8-123">Korean</span></span>                | <span data-ttu-id="afda8-124">0x0412</span><span class="sxs-lookup"><span data-stu-id="afda8-124">0x0412</span></span> |
| <span data-ttu-id="afda8-125">Chinesisch (traditionell)</span><span class="sxs-lookup"><span data-stu-id="afda8-125">Chinese (Traditional)</span></span> | <span data-ttu-id="afda8-126">0x0404</span><span class="sxs-lookup"><span data-stu-id="afda8-126">0x0404</span></span> | <span data-ttu-id="afda8-127">Norwegisch</span><span class="sxs-lookup"><span data-stu-id="afda8-127">Norwegian</span></span>             | <span data-ttu-id="afda8-128">0x0414</span><span class="sxs-lookup"><span data-stu-id="afda8-128">0x0414</span></span> |
| <span data-ttu-id="afda8-129">Kroatisch</span><span class="sxs-lookup"><span data-stu-id="afda8-129">Croatian</span></span>              | <span data-ttu-id="afda8-130">0x041a</span><span class="sxs-lookup"><span data-stu-id="afda8-130">0x041A</span></span> | <span data-ttu-id="afda8-131">Polnisch</span><span class="sxs-lookup"><span data-stu-id="afda8-131">Polish</span></span>                | <span data-ttu-id="afda8-132">0x0415</span><span class="sxs-lookup"><span data-stu-id="afda8-132">0x0415</span></span> |
| <span data-ttu-id="afda8-133">Tschechisch</span><span class="sxs-lookup"><span data-stu-id="afda8-133">Czech</span></span>                 | <span data-ttu-id="afda8-134">0x0405</span><span class="sxs-lookup"><span data-stu-id="afda8-134">0x0405</span></span> | <span data-ttu-id="afda8-135">Portugiesisch (Portugal)</span><span class="sxs-lookup"><span data-stu-id="afda8-135">Portuguese (Portugal)</span></span> | <span data-ttu-id="afda8-136">0x0816</span><span class="sxs-lookup"><span data-stu-id="afda8-136">0x0816</span></span> |
| <span data-ttu-id="afda8-137">Dänisch</span><span class="sxs-lookup"><span data-stu-id="afda8-137">Danish</span></span>                | <span data-ttu-id="afda8-138">0x0406</span><span class="sxs-lookup"><span data-stu-id="afda8-138">0x0406</span></span> | <span data-ttu-id="afda8-139">Portugiesisch (Brasilien)</span><span class="sxs-lookup"><span data-stu-id="afda8-139">Portuguese (Brazil)</span></span>   | <span data-ttu-id="afda8-140">0x0416</span><span class="sxs-lookup"><span data-stu-id="afda8-140">0x0416</span></span> |
| <span data-ttu-id="afda8-141">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="afda8-141">Dutch</span></span>                 | <span data-ttu-id="afda8-142">0x0413</span><span class="sxs-lookup"><span data-stu-id="afda8-142">0x0413</span></span> | <span data-ttu-id="afda8-143">Rumänisch</span><span class="sxs-lookup"><span data-stu-id="afda8-143">Romanian</span></span>              | <span data-ttu-id="afda8-144">0x0418</span><span class="sxs-lookup"><span data-stu-id="afda8-144">0x0418</span></span> |
| <span data-ttu-id="afda8-145">Englisch (Großbritannien)</span><span class="sxs-lookup"><span data-stu-id="afda8-145">English (British)</span></span>     | <span data-ttu-id="afda8-146">0x0809</span><span class="sxs-lookup"><span data-stu-id="afda8-146">0x0809</span></span> | <span data-ttu-id="afda8-147">Russisch</span><span class="sxs-lookup"><span data-stu-id="afda8-147">Russian</span></span>               | <span data-ttu-id="afda8-148">0x0419</span><span class="sxs-lookup"><span data-stu-id="afda8-148">0x0419</span></span> |
| <span data-ttu-id="afda8-149">Englisch (USA)</span><span class="sxs-lookup"><span data-stu-id="afda8-149">English (US)</span></span>          | <span data-ttu-id="afda8-150">0x0409</span><span class="sxs-lookup"><span data-stu-id="afda8-150">0x0409</span></span> | <span data-ttu-id="afda8-151">Slowakisch</span><span class="sxs-lookup"><span data-stu-id="afda8-151">Slovakian</span></span>             | <span data-ttu-id="afda8-152">0x041b</span><span class="sxs-lookup"><span data-stu-id="afda8-152">0x041B</span></span> |
| <span data-ttu-id="afda8-153">Finnisch</span><span class="sxs-lookup"><span data-stu-id="afda8-153">Finnish</span></span>               | <span data-ttu-id="afda8-154">0x040b</span><span class="sxs-lookup"><span data-stu-id="afda8-154">0x040B</span></span> | <span data-ttu-id="afda8-155">Slowenisch</span><span class="sxs-lookup"><span data-stu-id="afda8-155">Slovenian</span></span>             | <span data-ttu-id="afda8-156">0x0424</span><span class="sxs-lookup"><span data-stu-id="afda8-156">0x0424</span></span> |
| <span data-ttu-id="afda8-157">Französisch</span><span class="sxs-lookup"><span data-stu-id="afda8-157">French</span></span>                | <span data-ttu-id="afda8-158">0x040c</span><span class="sxs-lookup"><span data-stu-id="afda8-158">0x040C</span></span> | <span data-ttu-id="afda8-159">Spanisch</span><span class="sxs-lookup"><span data-stu-id="afda8-159">Spanish</span></span>               | <span data-ttu-id="afda8-160">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="afda8-160">0x0C0A</span></span> |
| <span data-ttu-id="afda8-161">Deutsch</span><span class="sxs-lookup"><span data-stu-id="afda8-161">German</span></span>                | <span data-ttu-id="afda8-162">0x0407</span><span class="sxs-lookup"><span data-stu-id="afda8-162">0x0407</span></span> | <span data-ttu-id="afda8-163">Schwedisch</span><span class="sxs-lookup"><span data-stu-id="afda8-163">Swedish</span></span>               | <span data-ttu-id="afda8-164">0x041d</span><span class="sxs-lookup"><span data-stu-id="afda8-164">0x041D</span></span> |
| <span data-ttu-id="afda8-165">Griechisch</span><span class="sxs-lookup"><span data-stu-id="afda8-165">Greek</span></span>                 | <span data-ttu-id="afda8-166">0x0408</span><span class="sxs-lookup"><span data-stu-id="afda8-166">0x0408</span></span> | <span data-ttu-id="afda8-167">Thailändisch</span><span class="sxs-lookup"><span data-stu-id="afda8-167">Thai</span></span>                  | <span data-ttu-id="afda8-168">0x041E</span><span class="sxs-lookup"><span data-stu-id="afda8-168">0x041E</span></span> |
| <span data-ttu-id="afda8-169">Hebräisch</span><span class="sxs-lookup"><span data-stu-id="afda8-169">Hebrew</span></span>                | <span data-ttu-id="afda8-170">0x040d</span><span class="sxs-lookup"><span data-stu-id="afda8-170">0x040D</span></span> | <span data-ttu-id="afda8-171">Türkisch</span><span class="sxs-lookup"><span data-stu-id="afda8-171">Turkish</span></span>               | <span data-ttu-id="afda8-172">0x041f</span><span class="sxs-lookup"><span data-stu-id="afda8-172">0x041F</span></span> |
| <span data-ttu-id="afda8-173">Ungarisch</span><span class="sxs-lookup"><span data-stu-id="afda8-173">Hungarian</span></span>             | <span data-ttu-id="afda8-174">0x040e</span><span class="sxs-lookup"><span data-stu-id="afda8-174">0x040E</span></span> |                       |        |



 

<span data-ttu-id="afda8-175">Wenn Sie diese Sprach-ID nicht für das Zeichen festlegen, wird die Sprach-ID des Zeichens als aktuelle Systemsprachen-ID verwendet.</span><span class="sxs-lookup"><span data-stu-id="afda8-175">If you do not set this language ID for the character, the character's language ID will be the current system language ID.</span></span>

<span data-ttu-id="afda8-176">Diese Einstellung bestimmt auch die Sprache für die TTS-Ausgabe, den Word-Sprechblasen Text, die Befehle im Popupmenü des Zeichens und die Spracherkennungs-Engine.</span><span class="sxs-lookup"><span data-stu-id="afda8-176">This setting also determines the language for TTS output, word balloon text, the commands in the character's pop-up menu, and speech recognition engine.</span></span> <span data-ttu-id="afda8-177">Verwenden Sie [**iagentcharakteriex:: getsrmodeid**](iagentcharacterex--getsrmodeid.md) oder [**iagentcharakteriex:: getttsmodeid**](iagentcharacterex--getttsmodeid.md), um zu bestimmen, ob eine kompatible sprach Erkennungs-Engine für die Sprache des Zeichens verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="afda8-177">To determine if there is a compatible speech recognition engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="afda8-178">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="afda8-178">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="afda8-179">Wenn die Sprach-ID auf eine Sprache festgelegt ist, die bidirektionalen Text (z. b. Arabisch oder Hebräisch) unterstützt, aber das System, auf dem Ihre Anwendung ausgeführt wird, nicht über eine bidirektionale Unterstützung verfügt, wird Text in der Wort Sprechblase in logischer und nicht in</span><span class="sxs-lookup"><span data-stu-id="afda8-179">If the language ID is set to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="afda8-180">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="afda8-180">See Also</span></span>

<span data-ttu-id="afda8-181">[**Iagentcharakteriex: setlanguageid**](iagentcharacterex--setlanguageid.md), [**iagentcharakteriex:: gezrmodeid**](iagentcharacterex--getsrmodeid.md), [**iagentcharakteriex:: getttmodeid**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="afda8-181">[**IAgentCharacterEx:SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




