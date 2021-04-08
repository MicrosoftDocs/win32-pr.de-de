---
title: Iagentcharakteriex setlanguageid
description: Iagentcharakteriex setlanguageid
ms.assetid: 064f4c3c-1871-4372-9796-5b53f05c6d9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec8a396c174fd251b1cc7ac8d7e9696c9b9f2d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708879"
---
# <a name="iagentcharacterexsetlanguageid"></a><span data-ttu-id="0d26e-103">Iagentcharakteriex:: setlanguageid</span><span class="sxs-lookup"><span data-stu-id="0d26e-103">IAgentCharacterEx::SetLanguageID</span></span>

<span data-ttu-id="0d26e-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="0d26e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetLanguageID(
   long langID  // language ID setting of character
); 
```

<span data-ttu-id="0d26e-105">Legt die für das Zeichen festgelegte Sprach-ID fest.</span><span class="sxs-lookup"><span data-stu-id="0d26e-105">Sets the language ID set for the character.</span></span>

-   <span data-ttu-id="0d26e-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="0d26e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0d26e-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span><span class="sxs-lookup"><span data-stu-id="0d26e-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="0d26e-108">Die Sprach-ID-Einstellung für das Zeichen.</span><span class="sxs-lookup"><span data-stu-id="0d26e-108">The language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="0d26e-109">Eine lange ganze Zahl, die die Sprach-ID für das Zeichen angibt.</span><span class="sxs-lookup"><span data-stu-id="0d26e-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="0d26e-110">Die Sprach-ID (langid) für ein Zeichen ist ein 16-Bit-Wert, der von Windows definiert wird und aus einer primär Sprachen-ID und einer sekundären Sprach-ID besteht.</span><span class="sxs-lookup"><span data-stu-id="0d26e-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="0d26e-111">Die folgenden Werte können für die angegebenen Sprachen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d26e-111">You can use the following values for the specified languages.</span></span> <span data-ttu-id="0d26e-112">Weitere Informationen finden Sie in der Platform SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="0d26e-112">For more information, see the Platform SDK documentation.</span></span>



|                       |        |                       |        |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="0d26e-113">Arabisch (Saudi)</span><span class="sxs-lookup"><span data-stu-id="0d26e-113">Arabic (Saudi)</span></span>        | <span data-ttu-id="0d26e-114">0x0401</span><span class="sxs-lookup"><span data-stu-id="0d26e-114">0x0401</span></span> | <span data-ttu-id="0d26e-115">Italienisch</span><span class="sxs-lookup"><span data-stu-id="0d26e-115">Italian</span></span>               | <span data-ttu-id="0d26e-116">0x0410</span><span class="sxs-lookup"><span data-stu-id="0d26e-116">0x0410</span></span> |
| <span data-ttu-id="0d26e-117">Baskisch</span><span class="sxs-lookup"><span data-stu-id="0d26e-117">Basque</span></span>                | <span data-ttu-id="0d26e-118">0x042d</span><span class="sxs-lookup"><span data-stu-id="0d26e-118">0x042d</span></span> | <span data-ttu-id="0d26e-119">Japanisch</span><span class="sxs-lookup"><span data-stu-id="0d26e-119">Japanese</span></span>              | <span data-ttu-id="0d26e-120">0x0411</span><span class="sxs-lookup"><span data-stu-id="0d26e-120">0x0411</span></span> |
| <span data-ttu-id="0d26e-121">Chinesisch (vereinfacht)</span><span class="sxs-lookup"><span data-stu-id="0d26e-121">Chinese (Simplified)</span></span>  | <span data-ttu-id="0d26e-122">0x0804</span><span class="sxs-lookup"><span data-stu-id="0d26e-122">0x0804</span></span> | <span data-ttu-id="0d26e-123">Koreanisch</span><span class="sxs-lookup"><span data-stu-id="0d26e-123">Korean</span></span>                | <span data-ttu-id="0d26e-124">0x0412</span><span class="sxs-lookup"><span data-stu-id="0d26e-124">0x0412</span></span> |
| <span data-ttu-id="0d26e-125">Chinesisch (traditionell)</span><span class="sxs-lookup"><span data-stu-id="0d26e-125">Chinese (Traditional)</span></span> | <span data-ttu-id="0d26e-126">0x0404</span><span class="sxs-lookup"><span data-stu-id="0d26e-126">0x0404</span></span> | <span data-ttu-id="0d26e-127">Norwegisch</span><span class="sxs-lookup"><span data-stu-id="0d26e-127">Norwegian</span></span>             | <span data-ttu-id="0d26e-128">0x0414</span><span class="sxs-lookup"><span data-stu-id="0d26e-128">0x0414</span></span> |
| <span data-ttu-id="0d26e-129">Kroatisch</span><span class="sxs-lookup"><span data-stu-id="0d26e-129">Croatian</span></span>              | <span data-ttu-id="0d26e-130">0x041a</span><span class="sxs-lookup"><span data-stu-id="0d26e-130">0x041A</span></span> | <span data-ttu-id="0d26e-131">Polnisch</span><span class="sxs-lookup"><span data-stu-id="0d26e-131">Polish</span></span>                | <span data-ttu-id="0d26e-132">0x0415</span><span class="sxs-lookup"><span data-stu-id="0d26e-132">0x0415</span></span> |
| <span data-ttu-id="0d26e-133">Tschechisch</span><span class="sxs-lookup"><span data-stu-id="0d26e-133">Czech</span></span>                 | <span data-ttu-id="0d26e-134">0x0405</span><span class="sxs-lookup"><span data-stu-id="0d26e-134">0x0405</span></span> | <span data-ttu-id="0d26e-135">Portugiesisch (Portugal)</span><span class="sxs-lookup"><span data-stu-id="0d26e-135">Portuguese (Portugal)</span></span> | <span data-ttu-id="0d26e-136">0x0816</span><span class="sxs-lookup"><span data-stu-id="0d26e-136">0x0816</span></span> |
| <span data-ttu-id="0d26e-137">Dänisch</span><span class="sxs-lookup"><span data-stu-id="0d26e-137">Danish</span></span>                | <span data-ttu-id="0d26e-138">0x0406</span><span class="sxs-lookup"><span data-stu-id="0d26e-138">0x0406</span></span> | <span data-ttu-id="0d26e-139">Portugiesisch (Brasilien)</span><span class="sxs-lookup"><span data-stu-id="0d26e-139">Portuguese (Brazil)</span></span>   | <span data-ttu-id="0d26e-140">0x0416</span><span class="sxs-lookup"><span data-stu-id="0d26e-140">0x0416</span></span> |
| <span data-ttu-id="0d26e-141">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="0d26e-141">Dutch</span></span>                 | <span data-ttu-id="0d26e-142">0x0413</span><span class="sxs-lookup"><span data-stu-id="0d26e-142">0x0413</span></span> | <span data-ttu-id="0d26e-143">Rumänisch</span><span class="sxs-lookup"><span data-stu-id="0d26e-143">Romanian</span></span>              | <span data-ttu-id="0d26e-144">0x0418</span><span class="sxs-lookup"><span data-stu-id="0d26e-144">0x0418</span></span> |
| <span data-ttu-id="0d26e-145">Englisch (Großbritannien)</span><span class="sxs-lookup"><span data-stu-id="0d26e-145">English (British)</span></span>     | <span data-ttu-id="0d26e-146">0x0809</span><span class="sxs-lookup"><span data-stu-id="0d26e-146">0x0809</span></span> | <span data-ttu-id="0d26e-147">Russisch</span><span class="sxs-lookup"><span data-stu-id="0d26e-147">Russian</span></span>               | <span data-ttu-id="0d26e-148">0x0419</span><span class="sxs-lookup"><span data-stu-id="0d26e-148">0x0419</span></span> |
| <span data-ttu-id="0d26e-149">Englisch (USA)</span><span class="sxs-lookup"><span data-stu-id="0d26e-149">English (US)</span></span>          | <span data-ttu-id="0d26e-150">0x0409</span><span class="sxs-lookup"><span data-stu-id="0d26e-150">0x0409</span></span> | <span data-ttu-id="0d26e-151">Slowakisch</span><span class="sxs-lookup"><span data-stu-id="0d26e-151">Slovakian</span></span>             | <span data-ttu-id="0d26e-152">0x041b</span><span class="sxs-lookup"><span data-stu-id="0d26e-152">0x041B</span></span> |
| <span data-ttu-id="0d26e-153">Finnisch</span><span class="sxs-lookup"><span data-stu-id="0d26e-153">Finnish</span></span>               | <span data-ttu-id="0d26e-154">0x040b</span><span class="sxs-lookup"><span data-stu-id="0d26e-154">0x040B</span></span> | <span data-ttu-id="0d26e-155">Slowenisch</span><span class="sxs-lookup"><span data-stu-id="0d26e-155">Slovenian</span></span>             | <span data-ttu-id="0d26e-156">0x0424</span><span class="sxs-lookup"><span data-stu-id="0d26e-156">0x0424</span></span> |
| <span data-ttu-id="0d26e-157">Französisch</span><span class="sxs-lookup"><span data-stu-id="0d26e-157">French</span></span>                | <span data-ttu-id="0d26e-158">0x040c</span><span class="sxs-lookup"><span data-stu-id="0d26e-158">0x040C</span></span> | <span data-ttu-id="0d26e-159">Spanisch</span><span class="sxs-lookup"><span data-stu-id="0d26e-159">Spanish</span></span>               | <span data-ttu-id="0d26e-160">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="0d26e-160">0x0C0A</span></span> |
| <span data-ttu-id="0d26e-161">Deutsch</span><span class="sxs-lookup"><span data-stu-id="0d26e-161">German</span></span>                | <span data-ttu-id="0d26e-162">0x0407</span><span class="sxs-lookup"><span data-stu-id="0d26e-162">0x0407</span></span> | <span data-ttu-id="0d26e-163">Schwedisch</span><span class="sxs-lookup"><span data-stu-id="0d26e-163">Swedish</span></span>               | <span data-ttu-id="0d26e-164">0x041d</span><span class="sxs-lookup"><span data-stu-id="0d26e-164">0x041D</span></span> |
| <span data-ttu-id="0d26e-165">Griechisch</span><span class="sxs-lookup"><span data-stu-id="0d26e-165">Greek</span></span>                 | <span data-ttu-id="0d26e-166">0x0408</span><span class="sxs-lookup"><span data-stu-id="0d26e-166">0x0408</span></span> | <span data-ttu-id="0d26e-167">Thailändisch</span><span class="sxs-lookup"><span data-stu-id="0d26e-167">Thai</span></span>                  | <span data-ttu-id="0d26e-168">0x041E</span><span class="sxs-lookup"><span data-stu-id="0d26e-168">0x041E</span></span> |
| <span data-ttu-id="0d26e-169">Hebräisch</span><span class="sxs-lookup"><span data-stu-id="0d26e-169">Hebrew</span></span>                | <span data-ttu-id="0d26e-170">0x040d</span><span class="sxs-lookup"><span data-stu-id="0d26e-170">0x040D</span></span> | <span data-ttu-id="0d26e-171">Türkisch</span><span class="sxs-lookup"><span data-stu-id="0d26e-171">Turkish</span></span>               | <span data-ttu-id="0d26e-172">0x041f</span><span class="sxs-lookup"><span data-stu-id="0d26e-172">0x041F</span></span> |
| <span data-ttu-id="0d26e-173">Ungarisch</span><span class="sxs-lookup"><span data-stu-id="0d26e-173">Hungarian</span></span>             | <span data-ttu-id="0d26e-174">0x040e</span><span class="sxs-lookup"><span data-stu-id="0d26e-174">0x040E</span></span> |                       |        |



 

<span data-ttu-id="0d26e-175">Wenn Sie die Sprach-ID für das Zeichen nicht festlegen, wird die Sprach-ID der aktuellen Systemsprachen-ID angezeigt, wenn die entsprechende dll der Agent-Sprache installiert ist. Andernfalls ist die Sprache des Zeichens Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="0d26e-175">If you do not set the language ID for the character, its language ID will be the current system language ID if the corresponding Agent language DLL is installed; otherwise, the character's language will be English (US).</span></span>

<span data-ttu-id="0d26e-176">Diese Eigenschaft bestimmt auch die Sprache für den Word-Sprechblasen Text, die Befehle im Popupmenü des Zeichens und die Spracherkennungs-Engine.</span><span class="sxs-lookup"><span data-stu-id="0d26e-176">This property also determines the language for the word balloon text, the commands in the character's pop-up menu, and the speech recognition engine.</span></span> <span data-ttu-id="0d26e-177">Außerdem wird die Standardsprache für die TTS-Ausgabe bestimmt.</span><span class="sxs-lookup"><span data-stu-id="0d26e-177">It also determines the default language for TTS output.</span></span> <span data-ttu-id="0d26e-178">Wenn Sie feststellen möchten, ob eine kompatible Sprach-Engine für die Sprache des Zeichens verfügbar ist, verwenden Sie [**iagentcharakteriex:: gezrmodeid**](iagentcharacterex--getsrmodeid.md) oder [**iagentcharakteriex:: getttmodeid**](iagentcharacterex--getttsmodeid.md).</span><span class="sxs-lookup"><span data-stu-id="0d26e-178">To determine if there is a compatible speech engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="0d26e-179">Wenn Sie versuchen, die Sprach-ID für ein Zeichen und die Agent-Sprachressourcen festzulegen, ist die Codepage oder eine Anzeige Schriftart für die Sprach-ID nicht verfügbar. der-Agent gibt einen Fehler zurück, und die Sprach-ID des Zeichens bleibt bei der letzten Einstellung.</span><span class="sxs-lookup"><span data-stu-id="0d26e-179">If you try to set the language ID for a character and the Agent language resources, the code page, or a display font for the language ID is not available, Agent returns an error and the character's language ID remains at its last setting.</span></span> <span data-ttu-id="0d26e-180">Das Festlegen dieser Eigenschaft gibt keinen Fehler zurück, wenn keine übereinstimmenden Sprach-Engines für die Sprache vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="0d26e-180">Setting this property does not return an error if there are no matching speech engines for the language.</span></span>

<span data-ttu-id="0d26e-181">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="0d26e-181">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="0d26e-182">Wenn Sie die Sprach-ID des Zeichens auf eine Sprache festlegen, die bidirektionalen Text (z. b. Arabisch oder Hebräisch) unterstützt, aber das System, auf dem Ihre Anwendung ausgeführt wird, nicht über eine bidirektionale Unterstützung verfügt, wird Text in der Wort Sprechblase anstelle der Anzeigereihenfolge</span><span class="sxs-lookup"><span data-stu-id="0d26e-182">If you set the character's language ID to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="0d26e-183">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0d26e-183">See Also</span></span>

<span data-ttu-id="0d26e-184">[**Iagentcharakteriex: getlanguageid**](iagentcharacterex--getlanguageid.md), [**iagentcharakteriex:: gezrmodeid**](iagentcharacterex--getsrmodeid.md), [**iagentcharakteriex:: getttmodeid**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="0d26e-184">[**IAgentCharacterEx:GetLanguageID**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




