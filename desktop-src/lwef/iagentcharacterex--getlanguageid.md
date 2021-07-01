---
title: IAgentCharacterEx GetLanguageID
description: IAgentCharacterEx GetLanguageID
ms.assetid: 4e4e5342-edf9-480b-a9c3-e2626fd89e76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d847bf392709b2433b045a357a703173e2de454
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120646"
---
# <a name="iagentcharacterexgetlanguageid"></a><span data-ttu-id="f967a-103">IAgentCharacterEx::GetLanguageID</span><span class="sxs-lookup"><span data-stu-id="f967a-103">IAgentCharacterEx::GetLanguageID</span></span>

<span data-ttu-id="f967a-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="f967a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetLanguageID(
   long * plangID  // address of language ID setting
);
```

<span data-ttu-id="f967a-105">Ruft den Sprach-ID-Satz für das Zeichen ab.</span><span class="sxs-lookup"><span data-stu-id="f967a-105">Retrieves the language ID set for the character.</span></span>

-   <span data-ttu-id="f967a-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="f967a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f967a-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span><span class="sxs-lookup"><span data-stu-id="f967a-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span></span>
</dt> <dd>

<span data-ttu-id="f967a-108">Adresse einer Variablen, die die Sprach-ID-Einstellung für das Zeichen empfängt.</span><span class="sxs-lookup"><span data-stu-id="f967a-108">Address of a variable that receives the language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="f967a-109">Eine long-Ganzzahl, die die Sprach-ID für das Zeichen angibt.</span><span class="sxs-lookup"><span data-stu-id="f967a-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="f967a-110">Die Sprach-ID (LANGID) für ein Zeichen ist ein von Windows definierter 16-Bit-Wert, der aus einer primären Sprach-ID und einer sekundären Sprach-ID besteht.</span><span class="sxs-lookup"><span data-stu-id="f967a-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="f967a-111">Die folgenden Beispiele sind Werte für einige Sprachen.</span><span class="sxs-lookup"><span data-stu-id="f967a-111">The following examples are values for some languages.</span></span> <span data-ttu-id="f967a-112">Informationen zum Ermitteln der Werte in anderen Sprachen finden Sie in der Dokumentation zum Plattform-SDK.</span><span class="sxs-lookup"><span data-stu-id="f967a-112">To determine the values other languages, see the Platform SDK documentation.</span></span>



| <span data-ttu-id="f967a-113">Sprache</span><span class="sxs-lookup"><span data-stu-id="f967a-113">Language</span></span>              | <span data-ttu-id="f967a-114">id</span><span class="sxs-lookup"><span data-stu-id="f967a-114">ID</span></span>     | <span data-ttu-id="f967a-115">Sprache</span><span class="sxs-lookup"><span data-stu-id="f967a-115">Language</span></span>              | <span data-ttu-id="f967a-116">id</span><span class="sxs-lookup"><span data-stu-id="f967a-116">ID</span></span>     |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="f967a-117">Arabisch (Saudi)</span><span class="sxs-lookup"><span data-stu-id="f967a-117">Arabic (Saudi)</span></span>        | <span data-ttu-id="f967a-118">0x0401</span><span class="sxs-lookup"><span data-stu-id="f967a-118">0x0401</span></span> | <span data-ttu-id="f967a-119">Italienisch</span><span class="sxs-lookup"><span data-stu-id="f967a-119">Italian</span></span>               | <span data-ttu-id="f967a-120">0x0410</span><span class="sxs-lookup"><span data-stu-id="f967a-120">0x0410</span></span> |
| <span data-ttu-id="f967a-121">Baskisch</span><span class="sxs-lookup"><span data-stu-id="f967a-121">Basque</span></span>                | <span data-ttu-id="f967a-122">0x042d</span><span class="sxs-lookup"><span data-stu-id="f967a-122">0x042d</span></span> | <span data-ttu-id="f967a-123">Japanisch</span><span class="sxs-lookup"><span data-stu-id="f967a-123">Japanese</span></span>              | <span data-ttu-id="f967a-124">0x0411</span><span class="sxs-lookup"><span data-stu-id="f967a-124">0x0411</span></span> |
| <span data-ttu-id="f967a-125">Chinesisch (vereinfacht)</span><span class="sxs-lookup"><span data-stu-id="f967a-125">Chinese (Simplified)</span></span>  | <span data-ttu-id="f967a-126">0x0804</span><span class="sxs-lookup"><span data-stu-id="f967a-126">0x0804</span></span> | <span data-ttu-id="f967a-127">Koreanisch</span><span class="sxs-lookup"><span data-stu-id="f967a-127">Korean</span></span>                | <span data-ttu-id="f967a-128">0x0412</span><span class="sxs-lookup"><span data-stu-id="f967a-128">0x0412</span></span> |
| <span data-ttu-id="f967a-129">Chinesisch (traditionell)</span><span class="sxs-lookup"><span data-stu-id="f967a-129">Chinese (Traditional)</span></span> | <span data-ttu-id="f967a-130">0x0404</span><span class="sxs-lookup"><span data-stu-id="f967a-130">0x0404</span></span> | <span data-ttu-id="f967a-131">Norwegisch</span><span class="sxs-lookup"><span data-stu-id="f967a-131">Norwegian</span></span>             | <span data-ttu-id="f967a-132">0x0414</span><span class="sxs-lookup"><span data-stu-id="f967a-132">0x0414</span></span> |
| <span data-ttu-id="f967a-133">Kroatisch</span><span class="sxs-lookup"><span data-stu-id="f967a-133">Croatian</span></span>              | <span data-ttu-id="f967a-134">0x041A</span><span class="sxs-lookup"><span data-stu-id="f967a-134">0x041A</span></span> | <span data-ttu-id="f967a-135">Polnisch</span><span class="sxs-lookup"><span data-stu-id="f967a-135">Polish</span></span>                | <span data-ttu-id="f967a-136">0x0415</span><span class="sxs-lookup"><span data-stu-id="f967a-136">0x0415</span></span> |
| <span data-ttu-id="f967a-137">Tschechisch</span><span class="sxs-lookup"><span data-stu-id="f967a-137">Czech</span></span>                 | <span data-ttu-id="f967a-138">0x0405</span><span class="sxs-lookup"><span data-stu-id="f967a-138">0x0405</span></span> | <span data-ttu-id="f967a-139">Portugiesisch (Portugal)</span><span class="sxs-lookup"><span data-stu-id="f967a-139">Portuguese (Portugal)</span></span> | <span data-ttu-id="f967a-140">0x0816</span><span class="sxs-lookup"><span data-stu-id="f967a-140">0x0816</span></span> |
| <span data-ttu-id="f967a-141">Dänisch</span><span class="sxs-lookup"><span data-stu-id="f967a-141">Danish</span></span>                | <span data-ttu-id="f967a-142">0x0406</span><span class="sxs-lookup"><span data-stu-id="f967a-142">0x0406</span></span> | <span data-ttu-id="f967a-143">Portugiesisch (Brasilien)</span><span class="sxs-lookup"><span data-stu-id="f967a-143">Portuguese (Brazil)</span></span>   | <span data-ttu-id="f967a-144">0x0416</span><span class="sxs-lookup"><span data-stu-id="f967a-144">0x0416</span></span> |
| <span data-ttu-id="f967a-145">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="f967a-145">Dutch</span></span>                 | <span data-ttu-id="f967a-146">0x0413</span><span class="sxs-lookup"><span data-stu-id="f967a-146">0x0413</span></span> | <span data-ttu-id="f967a-147">Rumänisch</span><span class="sxs-lookup"><span data-stu-id="f967a-147">Romanian</span></span>              | <span data-ttu-id="f967a-148">0x0418</span><span class="sxs-lookup"><span data-stu-id="f967a-148">0x0418</span></span> |
| <span data-ttu-id="f967a-149">Englisch (Großbritannien)</span><span class="sxs-lookup"><span data-stu-id="f967a-149">English (British)</span></span>     | <span data-ttu-id="f967a-150">0x0809</span><span class="sxs-lookup"><span data-stu-id="f967a-150">0x0809</span></span> | <span data-ttu-id="f967a-151">Russisch</span><span class="sxs-lookup"><span data-stu-id="f967a-151">Russian</span></span>               | <span data-ttu-id="f967a-152">0x0419</span><span class="sxs-lookup"><span data-stu-id="f967a-152">0x0419</span></span> |
| <span data-ttu-id="f967a-153">Englisch (USA)</span><span class="sxs-lookup"><span data-stu-id="f967a-153">English (US)</span></span>          | <span data-ttu-id="f967a-154">0x0409</span><span class="sxs-lookup"><span data-stu-id="f967a-154">0x0409</span></span> | <span data-ttu-id="f967a-155">Slowakisch</span><span class="sxs-lookup"><span data-stu-id="f967a-155">Slovakian</span></span>             | <span data-ttu-id="f967a-156">0x041B</span><span class="sxs-lookup"><span data-stu-id="f967a-156">0x041B</span></span> |
| <span data-ttu-id="f967a-157">Finnisch</span><span class="sxs-lookup"><span data-stu-id="f967a-157">Finnish</span></span>               | <span data-ttu-id="f967a-158">0x040B</span><span class="sxs-lookup"><span data-stu-id="f967a-158">0x040B</span></span> | <span data-ttu-id="f967a-159">Slowenisch</span><span class="sxs-lookup"><span data-stu-id="f967a-159">Slovenian</span></span>             | <span data-ttu-id="f967a-160">0x0424</span><span class="sxs-lookup"><span data-stu-id="f967a-160">0x0424</span></span> |
| <span data-ttu-id="f967a-161">Französisch</span><span class="sxs-lookup"><span data-stu-id="f967a-161">French</span></span>                | <span data-ttu-id="f967a-162">0x040C</span><span class="sxs-lookup"><span data-stu-id="f967a-162">0x040C</span></span> | <span data-ttu-id="f967a-163">Spanisch</span><span class="sxs-lookup"><span data-stu-id="f967a-163">Spanish</span></span>               | <span data-ttu-id="f967a-164">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="f967a-164">0x0C0A</span></span> |
| <span data-ttu-id="f967a-165">Deutsch</span><span class="sxs-lookup"><span data-stu-id="f967a-165">German</span></span>                | <span data-ttu-id="f967a-166">0x0407</span><span class="sxs-lookup"><span data-stu-id="f967a-166">0x0407</span></span> | <span data-ttu-id="f967a-167">Schwedisch</span><span class="sxs-lookup"><span data-stu-id="f967a-167">Swedish</span></span>               | <span data-ttu-id="f967a-168">0x041D</span><span class="sxs-lookup"><span data-stu-id="f967a-168">0x041D</span></span> |
| <span data-ttu-id="f967a-169">Griechisch</span><span class="sxs-lookup"><span data-stu-id="f967a-169">Greek</span></span>                 | <span data-ttu-id="f967a-170">0x0408</span><span class="sxs-lookup"><span data-stu-id="f967a-170">0x0408</span></span> | <span data-ttu-id="f967a-171">Thai</span><span class="sxs-lookup"><span data-stu-id="f967a-171">Thai</span></span>                  | <span data-ttu-id="f967a-172">0x041E</span><span class="sxs-lookup"><span data-stu-id="f967a-172">0x041E</span></span> |
| <span data-ttu-id="f967a-173">Hebräisch</span><span class="sxs-lookup"><span data-stu-id="f967a-173">Hebrew</span></span>                | <span data-ttu-id="f967a-174">0x040D</span><span class="sxs-lookup"><span data-stu-id="f967a-174">0x040D</span></span> | <span data-ttu-id="f967a-175">Türkisch</span><span class="sxs-lookup"><span data-stu-id="f967a-175">Turkish</span></span>               | <span data-ttu-id="f967a-176">0x041F</span><span class="sxs-lookup"><span data-stu-id="f967a-176">0x041F</span></span> |
| <span data-ttu-id="f967a-177">Ungarisch</span><span class="sxs-lookup"><span data-stu-id="f967a-177">Hungarian</span></span>             | <span data-ttu-id="f967a-178">0x040E</span><span class="sxs-lookup"><span data-stu-id="f967a-178">0x040E</span></span> |                       |        |



 

<span data-ttu-id="f967a-179">Wenn Sie diese Sprach-ID für das Zeichen nicht festlegen, ist die Sprach-ID des Zeichens die aktuelle Systemsprach-ID.</span><span class="sxs-lookup"><span data-stu-id="f967a-179">If you do not set this language ID for the character, the character's language ID will be the current system language ID.</span></span>

<span data-ttu-id="f967a-180">Diese Einstellung bestimmt auch die Sprache für die TTS-Ausgabe, den Text der Sprachsprechblasen, die Befehle im Popupmenü des Zeichens und die Spracherkennungs-Engine.</span><span class="sxs-lookup"><span data-stu-id="f967a-180">This setting also determines the language for TTS output, word balloon text, the commands in the character's pop-up menu, and speech recognition engine.</span></span> <span data-ttu-id="f967a-181">Verwenden Sie [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) oder [**IAgentCharacterEx::GetTTSModeID,**](iagentcharacterex--getttsmodeid.md)um zu ermitteln, ob eine kompatible Spracherkennungs-Engine für die Sprache des Zeichens verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f967a-181">To determine if there is a compatible speech recognition engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="f967a-182">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.</span><span class="sxs-lookup"><span data-stu-id="f967a-182">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="f967a-183">Wenn die Sprach-ID auf eine Sprache festgelegt ist, die bidirektionalen Text unterstützt (z. B. Arabisch oder Hebräisch), aber auf dem System, auf dem Ihre Anwendung ausgeführt wird, keine bidirektionale Unterstützung installiert ist, wird Text im Wortsprechblasen in logischer statt in der Anzeigereihenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f967a-183">If the language ID is set to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="f967a-184">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f967a-184">See Also</span></span>

<span data-ttu-id="f967a-185">[**IAgentCharacterEx:SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="f967a-185">[**IAgentCharacterEx:SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




