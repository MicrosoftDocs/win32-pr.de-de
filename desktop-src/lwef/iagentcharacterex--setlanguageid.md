---
title: IAgentCharacterEx SetLanguageID
description: IAgentCharacterEx SetLanguageID
ms.assetid: 064f4c3c-1871-4372-9796-5b53f05c6d9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036e1d41878adaae878a5961b45d190971d790af
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119005"
---
# <a name="iagentcharacterexsetlanguageid"></a><span data-ttu-id="f0cd2-103">IAgentCharacterEx::SetLanguageID</span><span class="sxs-lookup"><span data-stu-id="f0cd2-103">IAgentCharacterEx::SetLanguageID</span></span>

<span data-ttu-id="f0cd2-104">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="f0cd2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetLanguageID(
   long langID  // language ID setting of character
); 
```

<span data-ttu-id="f0cd2-105">Legt die Sprach-ID fest, die für das Zeichen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f0cd2-105">Sets the language ID set for the character.</span></span>

-   <span data-ttu-id="f0cd2-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="f0cd2-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f0cd2-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*Langid*</span><span class="sxs-lookup"><span data-stu-id="f0cd2-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="f0cd2-108">Die Sprach-ID-Einstellung für das Zeichen.</span><span class="sxs-lookup"><span data-stu-id="f0cd2-108">The language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="f0cd2-109">Eine lange ganze Zahl, die die Sprach-ID für das Zeichen angibt.</span><span class="sxs-lookup"><span data-stu-id="f0cd2-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="f0cd2-110">Die Sprach-ID (LANGID) für ein Zeichen ist ein von Windows definierter 16-Bit-Wert, der aus einer primären Sprach-ID und einer sekundären Sprach-ID besteht.</span><span class="sxs-lookup"><span data-stu-id="f0cd2-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="f0cd2-111">Sie können die folgenden Werte für die angegebenen Sprachen verwenden.</span><span class="sxs-lookup"><span data-stu-id="f0cd2-111">You can use the following values for the specified languages.</span></span> <span data-ttu-id="f0cd2-112">Weitere Informationen finden Sie in der Platform SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="f0cd2-112">For more information, see the Platform SDK documentation.</span></span>



| <span data-ttu-id="f0cd2-113">Sprache</span><span class="sxs-lookup"><span data-stu-id="f0cd2-113">Language</span></span>              | <span data-ttu-id="f0cd2-114">id</span><span class="sxs-lookup"><span data-stu-id="f0cd2-114">ID</span></span>     |  <span data-ttu-id="f0cd2-115">Sprache</span><span class="sxs-lookup"><span data-stu-id="f0cd2-115">Language</span></span>             | <span data-ttu-id="f0cd2-116">id</span><span class="sxs-lookup"><span data-stu-id="f0cd2-116">ID</span></span>     |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="f0cd2-117">Arabisch (Arabisch)</span><span class="sxs-lookup"><span data-stu-id="f0cd2-117">Arabic (Saudi)</span></span>        | <span data-ttu-id="f0cd2-118">0x0401</span><span class="sxs-lookup"><span data-stu-id="f0cd2-118">0x0401</span></span> | <span data-ttu-id="f0cd2-119">Italienisch</span><span class="sxs-lookup"><span data-stu-id="f0cd2-119">Italian</span></span>               | <span data-ttu-id="f0cd2-120">0x0410</span><span class="sxs-lookup"><span data-stu-id="f0cd2-120">0x0410</span></span> |
| <span data-ttu-id="f0cd2-121">Baskisch</span><span class="sxs-lookup"><span data-stu-id="f0cd2-121">Basque</span></span>                | <span data-ttu-id="f0cd2-122">0x042d</span><span class="sxs-lookup"><span data-stu-id="f0cd2-122">0x042d</span></span> | <span data-ttu-id="f0cd2-123">Japanisch</span><span class="sxs-lookup"><span data-stu-id="f0cd2-123">Japanese</span></span>              | <span data-ttu-id="f0cd2-124">0x0411</span><span class="sxs-lookup"><span data-stu-id="f0cd2-124">0x0411</span></span> |
| <span data-ttu-id="f0cd2-125">Chinesisch (vereinfacht)</span><span class="sxs-lookup"><span data-stu-id="f0cd2-125">Chinese (Simplified)</span></span>  | <span data-ttu-id="f0cd2-126">0x0804</span><span class="sxs-lookup"><span data-stu-id="f0cd2-126">0x0804</span></span> | <span data-ttu-id="f0cd2-127">Koreanisch</span><span class="sxs-lookup"><span data-stu-id="f0cd2-127">Korean</span></span>                | <span data-ttu-id="f0cd2-128">0x0412</span><span class="sxs-lookup"><span data-stu-id="f0cd2-128">0x0412</span></span> |
| <span data-ttu-id="f0cd2-129">Chinesisch (traditionell)</span><span class="sxs-lookup"><span data-stu-id="f0cd2-129">Chinese (Traditional)</span></span> | <span data-ttu-id="f0cd2-130">0x0404</span><span class="sxs-lookup"><span data-stu-id="f0cd2-130">0x0404</span></span> | <span data-ttu-id="f0cd2-131">Norwegisch</span><span class="sxs-lookup"><span data-stu-id="f0cd2-131">Norwegian</span></span>             | <span data-ttu-id="f0cd2-132">0x0414</span><span class="sxs-lookup"><span data-stu-id="f0cd2-132">0x0414</span></span> |
| <span data-ttu-id="f0cd2-133">Kroatisch</span><span class="sxs-lookup"><span data-stu-id="f0cd2-133">Croatian</span></span>              | <span data-ttu-id="f0cd2-134">0x041A</span><span class="sxs-lookup"><span data-stu-id="f0cd2-134">0x041A</span></span> | <span data-ttu-id="f0cd2-135">Polnisch</span><span class="sxs-lookup"><span data-stu-id="f0cd2-135">Polish</span></span>                | <span data-ttu-id="f0cd2-136">0x0415</span><span class="sxs-lookup"><span data-stu-id="f0cd2-136">0x0415</span></span> |
| <span data-ttu-id="f0cd2-137">Tschechisch</span><span class="sxs-lookup"><span data-stu-id="f0cd2-137">Czech</span></span>                 | <span data-ttu-id="f0cd2-138">0x0405</span><span class="sxs-lookup"><span data-stu-id="f0cd2-138">0x0405</span></span> | <span data-ttu-id="f0cd2-139">Portugiesisch (Portugal)</span><span class="sxs-lookup"><span data-stu-id="f0cd2-139">Portuguese (Portugal)</span></span> | <span data-ttu-id="f0cd2-140">0x0816</span><span class="sxs-lookup"><span data-stu-id="f0cd2-140">0x0816</span></span> |
| <span data-ttu-id="f0cd2-141">Dänisch</span><span class="sxs-lookup"><span data-stu-id="f0cd2-141">Danish</span></span>                | <span data-ttu-id="f0cd2-142">0x0406</span><span class="sxs-lookup"><span data-stu-id="f0cd2-142">0x0406</span></span> | <span data-ttu-id="f0cd2-143">Portugiesisch (Brasilien)</span><span class="sxs-lookup"><span data-stu-id="f0cd2-143">Portuguese (Brazil)</span></span>   | <span data-ttu-id="f0cd2-144">0x0416</span><span class="sxs-lookup"><span data-stu-id="f0cd2-144">0x0416</span></span> |
| <span data-ttu-id="f0cd2-145">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="f0cd2-145">Dutch</span></span>                 | <span data-ttu-id="f0cd2-146">0x0413</span><span class="sxs-lookup"><span data-stu-id="f0cd2-146">0x0413</span></span> | <span data-ttu-id="f0cd2-147">Rumänisch</span><span class="sxs-lookup"><span data-stu-id="f0cd2-147">Romanian</span></span>              | <span data-ttu-id="f0cd2-148">0x0418</span><span class="sxs-lookup"><span data-stu-id="f0cd2-148">0x0418</span></span> |
| <span data-ttu-id="f0cd2-149">Englisch (Großbritannien)</span><span class="sxs-lookup"><span data-stu-id="f0cd2-149">English (British)</span></span>     | <span data-ttu-id="f0cd2-150">0x0809</span><span class="sxs-lookup"><span data-stu-id="f0cd2-150">0x0809</span></span> | <span data-ttu-id="f0cd2-151">Russisch</span><span class="sxs-lookup"><span data-stu-id="f0cd2-151">Russian</span></span>               | <span data-ttu-id="f0cd2-152">0x0419</span><span class="sxs-lookup"><span data-stu-id="f0cd2-152">0x0419</span></span> |
| <span data-ttu-id="f0cd2-153">Englisch (USA)</span><span class="sxs-lookup"><span data-stu-id="f0cd2-153">English (US)</span></span>          | <span data-ttu-id="f0cd2-154">0x0409</span><span class="sxs-lookup"><span data-stu-id="f0cd2-154">0x0409</span></span> | <span data-ttu-id="f0cd2-155">Slowakisch</span><span class="sxs-lookup"><span data-stu-id="f0cd2-155">Slovakian</span></span>             | <span data-ttu-id="f0cd2-156">0x041B</span><span class="sxs-lookup"><span data-stu-id="f0cd2-156">0x041B</span></span> |
| <span data-ttu-id="f0cd2-157">Finnisch</span><span class="sxs-lookup"><span data-stu-id="f0cd2-157">Finnish</span></span>               | <span data-ttu-id="f0cd2-158">0x040B</span><span class="sxs-lookup"><span data-stu-id="f0cd2-158">0x040B</span></span> | <span data-ttu-id="f0cd2-159">Slowenisch</span><span class="sxs-lookup"><span data-stu-id="f0cd2-159">Slovenian</span></span>             | <span data-ttu-id="f0cd2-160">0x0424</span><span class="sxs-lookup"><span data-stu-id="f0cd2-160">0x0424</span></span> |
| <span data-ttu-id="f0cd2-161">Französisch</span><span class="sxs-lookup"><span data-stu-id="f0cd2-161">French</span></span>                | <span data-ttu-id="f0cd2-162">0x040C</span><span class="sxs-lookup"><span data-stu-id="f0cd2-162">0x040C</span></span> | <span data-ttu-id="f0cd2-163">Spanisch</span><span class="sxs-lookup"><span data-stu-id="f0cd2-163">Spanish</span></span>               | <span data-ttu-id="f0cd2-164">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="f0cd2-164">0x0C0A</span></span> |
| <span data-ttu-id="f0cd2-165">Deutsch</span><span class="sxs-lookup"><span data-stu-id="f0cd2-165">German</span></span>                | <span data-ttu-id="f0cd2-166">0x0407</span><span class="sxs-lookup"><span data-stu-id="f0cd2-166">0x0407</span></span> | <span data-ttu-id="f0cd2-167">Schwedisch</span><span class="sxs-lookup"><span data-stu-id="f0cd2-167">Swedish</span></span>               | <span data-ttu-id="f0cd2-168">0x041D</span><span class="sxs-lookup"><span data-stu-id="f0cd2-168">0x041D</span></span> |
| <span data-ttu-id="f0cd2-169">Griechisch</span><span class="sxs-lookup"><span data-stu-id="f0cd2-169">Greek</span></span>                 | <span data-ttu-id="f0cd2-170">0x0408</span><span class="sxs-lookup"><span data-stu-id="f0cd2-170">0x0408</span></span> | <span data-ttu-id="f0cd2-171">Thai</span><span class="sxs-lookup"><span data-stu-id="f0cd2-171">Thai</span></span>                  | <span data-ttu-id="f0cd2-172">0x041E</span><span class="sxs-lookup"><span data-stu-id="f0cd2-172">0x041E</span></span> |
| <span data-ttu-id="f0cd2-173">Hebräisch</span><span class="sxs-lookup"><span data-stu-id="f0cd2-173">Hebrew</span></span>                | <span data-ttu-id="f0cd2-174">0x040D</span><span class="sxs-lookup"><span data-stu-id="f0cd2-174">0x040D</span></span> | <span data-ttu-id="f0cd2-175">Türkisch</span><span class="sxs-lookup"><span data-stu-id="f0cd2-175">Turkish</span></span>               | <span data-ttu-id="f0cd2-176">0x041F</span><span class="sxs-lookup"><span data-stu-id="f0cd2-176">0x041F</span></span> |
| <span data-ttu-id="f0cd2-177">Ungarisch</span><span class="sxs-lookup"><span data-stu-id="f0cd2-177">Hungarian</span></span>             | <span data-ttu-id="f0cd2-178">0x040E</span><span class="sxs-lookup"><span data-stu-id="f0cd2-178">0x040E</span></span> |                       |        |



 

<span data-ttu-id="f0cd2-179">Wenn Sie die Sprach-ID für das Zeichen nicht festlegen, ist ihre Sprach-ID die aktuelle Systemsprach-ID, wenn die entsprechende -Agent-Sprach-DLL installiert ist. Andernfalls ist die Sprache des Zeichens Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="f0cd2-179">If you do not set the language ID for the character, its language ID will be the current system language ID if the corresponding Agent language DLL is installed; otherwise, the character's language will be English (US).</span></span>

<span data-ttu-id="f0cd2-180">Diese Eigenschaft bestimmt auch die Sprache für den Text der Wortsprechblasen, die Befehle im Popupmenü des Zeichens und die Spracherkennungs-Engine.</span><span class="sxs-lookup"><span data-stu-id="f0cd2-180">This property also determines the language for the word balloon text, the commands in the character's pop-up menu, and the speech recognition engine.</span></span> <span data-ttu-id="f0cd2-181">Außerdem wird die Standardsprache für die TTS-Ausgabe bestimmt.</span><span class="sxs-lookup"><span data-stu-id="f0cd2-181">It also determines the default language for TTS output.</span></span> <span data-ttu-id="f0cd2-182">Verwenden Sie [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) oder [**IAgentCharacterEx::GetTTSModeID,**](iagentcharacterex--getttsmodeid.md)um zu ermitteln, ob eine kompatible Sprach-Engine für die Sprache des Zeichens verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f0cd2-182">To determine if there is a compatible speech engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="f0cd2-183">Wenn Sie versuchen, die Sprach-ID für ein Zeichen und die Agent-Sprachressourcen, die Codepage oder eine Anzeigeschriftart für die Sprach-ID nicht verfügbar zu machen, gibt der -Agent einen Fehler zurück, und die Sprach-ID des Zeichens bleibt bei seiner letzten Einstellung.</span><span class="sxs-lookup"><span data-stu-id="f0cd2-183">If you try to set the language ID for a character and the Agent language resources, the code page, or a display font for the language ID is not available, Agent returns an error and the character's language ID remains at its last setting.</span></span> <span data-ttu-id="f0cd2-184">Das Festlegen dieser Eigenschaft gibt keinen Fehler zurück, wenn keine übereinstimmenden Sprach-Engines für die Sprache sind.</span><span class="sxs-lookup"><span data-stu-id="f0cd2-184">Setting this property does not return an error if there are no matching speech engines for the language.</span></span>

<span data-ttu-id="f0cd2-185">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.</span><span class="sxs-lookup"><span data-stu-id="f0cd2-185">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="f0cd2-186">Wenn Sie die Sprach-ID des Zeichens auf eine Sprache festlegen, die bidirektionalen Text unterstützt (z. B. Arabisch oder Hebräisch), aber das System, auf dem Ihre Anwendung ausgeführt wird, keine bidirektionale Unterstützung installiert ist, wird Text im Wortsprechblasen in logischer statt in der Anzeigerichtung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f0cd2-186">If you set the character's language ID to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="f0cd2-187">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f0cd2-187">See Also</span></span>

<span data-ttu-id="f0cd2-188">[**IAgentCharacterEx:GetLanguageID**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="f0cd2-188">[**IAgentCharacterEx:GetLanguageID**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




