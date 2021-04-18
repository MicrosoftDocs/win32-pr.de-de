---
title: LanguageID (Eigenschaft)
description: LanguageID (Eigenschaft)
ms.assetid: f57b0fa1-b3b8-49c8-b441-2a40e564d6ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7a10e6b16f9e35b223bada728871d253685538
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311039"
---
# <a name="languageid-property"></a><span data-ttu-id="4ae0f-103">LanguageID (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4ae0f-103">LanguageID Property</span></span>

<span data-ttu-id="4ae0f-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="4ae0f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="4ae0f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4ae0f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="4ae0f-106">Gibt die Sprachen-ID für das Zeichen zurück oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="4ae0f-106">Returns or sets the language ID for the character.</span></span>

</dd> <dt>

<span data-ttu-id="4ae0f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="4ae0f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="4ae0f-108">*Agent. \* \* \* Zeichen* \*  **("***Merkmal-ID***"). LanguageID** \[  =  *LanguageID*\]</span><span class="sxs-lookup"><span data-stu-id="4ae0f-108">*agent.\*\*\*Characters*\* **("***CharacterID***").LanguageID** \[ = *LanguageID*\]</span></span>



<span data-ttu-id="4ae0f-109">Teil</span><span class="sxs-lookup"><span data-stu-id="4ae0f-109">Part</span></span>

<span data-ttu-id="4ae0f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ae0f-110">Description</span></span>

<span data-ttu-id="4ae0f-111">LanguageID</span><span class="sxs-lookup"><span data-stu-id="4ae0f-111">LanguageID</span></span>

<span data-ttu-id="4ae0f-112">Eine lange ganze Zahl, die die Sprach-ID für das Zeichen angibt.</span><span class="sxs-lookup"><span data-stu-id="4ae0f-112">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="4ae0f-113">Die Sprach-ID (langid) für ein Zeichen ist ein 16-Bit-Wert, der von Windows definiert wird und aus einer primär Sprachen-ID und einer sekundären Sprach-ID besteht.</span><span class="sxs-lookup"><span data-stu-id="4ae0f-113">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="4ae0f-114">Die folgenden Beispiele sind Werte für Sprachen, die vom Microsoft-Agent unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="4ae0f-114">The following examples are values for languages supported by Microsoft Agent.</span></span> <span data-ttu-id="4ae0f-115">Informationen zum Bestimmen des Werts für andere Sprachen finden Sie in der *Platform SDK-Dokumentation*.</span><span class="sxs-lookup"><span data-stu-id="4ae0f-115">To determine the value for other languages, see the *Platform SDK documentation*.</span></span>

 

<span data-ttu-id="4ae0f-116">Arabisch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-116">Arabic</span></span>

<span data-ttu-id="4ae0f-117">&H0401</span><span class="sxs-lookup"><span data-stu-id="4ae0f-117">&H0401</span></span>

<span data-ttu-id="4ae0f-118">Italienisch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-118">Italian</span></span>

<span data-ttu-id="4ae0f-119">&H0410</span><span class="sxs-lookup"><span data-stu-id="4ae0f-119">&H0410</span></span>

 

<span data-ttu-id="4ae0f-120">Baskisch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-120">Basque</span></span>

<span data-ttu-id="4ae0f-121">&H042D</span><span class="sxs-lookup"><span data-stu-id="4ae0f-121">&H042D</span></span>

<span data-ttu-id="4ae0f-122">Japanisch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-122">Japanese</span></span>

<span data-ttu-id="4ae0f-123">&H0411</span><span class="sxs-lookup"><span data-stu-id="4ae0f-123">&H0411</span></span>

 

<span data-ttu-id="4ae0f-124">Chinesisch (vereinfacht)</span><span class="sxs-lookup"><span data-stu-id="4ae0f-124">Chinese (Simplified)</span></span>

<span data-ttu-id="4ae0f-125">&H0804</span><span class="sxs-lookup"><span data-stu-id="4ae0f-125">&H0804</span></span>

<span data-ttu-id="4ae0f-126">Koreanisch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-126">Korean</span></span>

<span data-ttu-id="4ae0f-127">&H0412</span><span class="sxs-lookup"><span data-stu-id="4ae0f-127">&H0412</span></span>

 

<span data-ttu-id="4ae0f-128">Chinesisch (traditionell)</span><span class="sxs-lookup"><span data-stu-id="4ae0f-128">Chinese (Traditional)</span></span>

<span data-ttu-id="4ae0f-129">&H0404</span><span class="sxs-lookup"><span data-stu-id="4ae0f-129">&H0404</span></span>

<span data-ttu-id="4ae0f-130">Norwegisch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-130">Norwegian</span></span>

<span data-ttu-id="4ae0f-131">&H0414</span><span class="sxs-lookup"><span data-stu-id="4ae0f-131">&H0414</span></span>

 

<span data-ttu-id="4ae0f-132">Kroatisch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-132">Croatian</span></span>

<span data-ttu-id="4ae0f-133">&H041A</span><span class="sxs-lookup"><span data-stu-id="4ae0f-133">&H041A</span></span>

<span data-ttu-id="4ae0f-134">Polnisch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-134">Polish</span></span>

<span data-ttu-id="4ae0f-135">&H0415</span><span class="sxs-lookup"><span data-stu-id="4ae0f-135">&H0415</span></span>

 

<span data-ttu-id="4ae0f-136">Tschechisch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-136">Czech</span></span>

<span data-ttu-id="4ae0f-137">&H0405</span><span class="sxs-lookup"><span data-stu-id="4ae0f-137">&H0405</span></span>

<span data-ttu-id="4ae0f-138">Portugiesisch (Portugal)</span><span class="sxs-lookup"><span data-stu-id="4ae0f-138">Portuguese (Portugal)</span></span>

<span data-ttu-id="4ae0f-139">&H0816</span><span class="sxs-lookup"><span data-stu-id="4ae0f-139">&H0816</span></span>

 

<span data-ttu-id="4ae0f-140">Dänisch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-140">Danish</span></span>

<span data-ttu-id="4ae0f-141">&H0406</span><span class="sxs-lookup"><span data-stu-id="4ae0f-141">&H0406</span></span>

<span data-ttu-id="4ae0f-142">Portugiesisch (Brasilien)</span><span class="sxs-lookup"><span data-stu-id="4ae0f-142">Portuguese (Brazil)</span></span>

<span data-ttu-id="4ae0f-143">&H0416</span><span class="sxs-lookup"><span data-stu-id="4ae0f-143">&H0416</span></span>

 

<span data-ttu-id="4ae0f-144">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-144">Dutch</span></span>

<span data-ttu-id="4ae0f-145">&H0413</span><span class="sxs-lookup"><span data-stu-id="4ae0f-145">&H0413</span></span>

<span data-ttu-id="4ae0f-146">Rumänisch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-146">Romanian</span></span>

<span data-ttu-id="4ae0f-147">&H0418</span><span class="sxs-lookup"><span data-stu-id="4ae0f-147">&H0418</span></span>

 

<span data-ttu-id="4ae0f-148">Englisch (Großbritannien)</span><span class="sxs-lookup"><span data-stu-id="4ae0f-148">English (British)</span></span>

<span data-ttu-id="4ae0f-149">&H0809</span><span class="sxs-lookup"><span data-stu-id="4ae0f-149">&H0809</span></span>

<span data-ttu-id="4ae0f-150">Russisch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-150">Russian</span></span>

<span data-ttu-id="4ae0f-151">&H0419</span><span class="sxs-lookup"><span data-stu-id="4ae0f-151">&H0419</span></span>

 

<span data-ttu-id="4ae0f-152">Englisch (USA)</span><span class="sxs-lookup"><span data-stu-id="4ae0f-152">English (US)</span></span>

<span data-ttu-id="4ae0f-153">&H0409</span><span class="sxs-lookup"><span data-stu-id="4ae0f-153">&H0409</span></span>

<span data-ttu-id="4ae0f-154">Slowakisch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-154">Slovakian</span></span>

<span data-ttu-id="4ae0f-155">&H041B</span><span class="sxs-lookup"><span data-stu-id="4ae0f-155">&H041B</span></span>

 

<span data-ttu-id="4ae0f-156">Finnisch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-156">Finnish</span></span>

<span data-ttu-id="4ae0f-157">&H040B</span><span class="sxs-lookup"><span data-stu-id="4ae0f-157">&H040B</span></span>

<span data-ttu-id="4ae0f-158">Slowenisch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-158">Slovenian</span></span>

<span data-ttu-id="4ae0f-159">&H0424</span><span class="sxs-lookup"><span data-stu-id="4ae0f-159">&H0424</span></span>

 

<span data-ttu-id="4ae0f-160">Französisch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-160">French</span></span>

<span data-ttu-id="4ae0f-161">&H040C</span><span class="sxs-lookup"><span data-stu-id="4ae0f-161">&H040C</span></span>

<span data-ttu-id="4ae0f-162">Spanisch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-162">Spanish</span></span>

<span data-ttu-id="4ae0f-163">&H0C0A</span><span class="sxs-lookup"><span data-stu-id="4ae0f-163">&H0C0A</span></span>

 

<span data-ttu-id="4ae0f-164">Deutsch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-164">German</span></span>

<span data-ttu-id="4ae0f-165">&H0407</span><span class="sxs-lookup"><span data-stu-id="4ae0f-165">&H0407</span></span>

<span data-ttu-id="4ae0f-166">Schwedisch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-166">Swedish</span></span>

<span data-ttu-id="4ae0f-167">&H041D</span><span class="sxs-lookup"><span data-stu-id="4ae0f-167">&H041D</span></span>

 

<span data-ttu-id="4ae0f-168">Griechisch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-168">Greek</span></span>

<span data-ttu-id="4ae0f-169">&H0408</span><span class="sxs-lookup"><span data-stu-id="4ae0f-169">&H0408</span></span>

<span data-ttu-id="4ae0f-170">Thailändisch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-170">Thai</span></span>

<span data-ttu-id="4ae0f-171">&H041E</span><span class="sxs-lookup"><span data-stu-id="4ae0f-171">&H041E</span></span>

 

<span data-ttu-id="4ae0f-172">Hebräisch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-172">Hebrew</span></span>

<span data-ttu-id="4ae0f-173">&H040D</span><span class="sxs-lookup"><span data-stu-id="4ae0f-173">&H040D</span></span>

<span data-ttu-id="4ae0f-174">Türkisch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-174">Turkish</span></span>

<span data-ttu-id="4ae0f-175">&H041F</span><span class="sxs-lookup"><span data-stu-id="4ae0f-175">&H041F</span></span>

 

<span data-ttu-id="4ae0f-176">Ungarisch</span><span class="sxs-lookup"><span data-stu-id="4ae0f-176">Hungarian</span></span>

<span data-ttu-id="4ae0f-177">&H040E</span><span class="sxs-lookup"><span data-stu-id="4ae0f-177">&H040E</span></span>

 

 



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ae0f-178">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ae0f-178">Remarks</span></span>

<span data-ttu-id="4ae0f-179">Wenn Sie die **LanguageID** nicht für das Zeichen festlegen, wird die Sprach-ID der aktuellen Systemsprachen-ID angezeigt, wenn die entsprechende dll der Agent-Sprache installiert ist. andernfalls ist die Sprache des Zeichens Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="4ae0f-179">If you do not set the **LanguageID** for the character, its language ID will be the current system language ID if the corresponding Agent language DLL is installed, otherwise, the character's language will be English (US).</span></span>

<span data-ttu-id="4ae0f-180">Diese Eigenschaft bestimmt auch die Sprache für Word-Sprechblasen Text, die Befehle im Popupmenü des Zeichens und die Spracherkennungs-Engine.</span><span class="sxs-lookup"><span data-stu-id="4ae0f-180">This property also determines the language for word balloon text, the commands in the character's pop-up menu, and the speech recognition engine.</span></span> <span data-ttu-id="4ae0f-181">Außerdem wird die Standardsprache für die TTS-Ausgabe bestimmt.</span><span class="sxs-lookup"><span data-stu-id="4ae0f-181">It also determines the default language for TTS output.</span></span>

<span data-ttu-id="4ae0f-182">Wenn Sie versuchen, die **LanguageID** für ein Zeichen festzulegen, und die Agent-sprach-dll für diese Sprache nicht installiert ist oder eine Anzeige Schriftart für die Sprach-ID nicht verfügbar ist, löst der-Agent einen Fehler aus, und **LanguageID** bleibt bei der letzten Einstellung.</span><span class="sxs-lookup"><span data-stu-id="4ae0f-182">If you try to set the **LanguageID** for a character and the Agent language DLL for that language is not installed or a display font for the language ID is not available, Agent raises an error and **LanguageID** remains at its last setting.</span></span>

<span data-ttu-id="4ae0f-183">Wenn Sie diese Eigenschaft festlegen, wird kein Fehler ausgegeben, wenn keine übereinstimmenden Sprach-Engines für die Sprache vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="4ae0f-183">Setting this property does not raise an error if there are no matching speech engines for the language.</span></span> <span data-ttu-id="4ae0f-184">Wenn Sie feststellen möchten, ob eine kompatible Sprach-Engine für **LanguageID** verfügbar ist, überprüfen Sie [**srmodeid**](srmodeid-property.md) oder [**ttsmodeid**](ttsmodeid-property.md).</span><span class="sxs-lookup"><span data-stu-id="4ae0f-184">To determine if there is a compatible speech engine available for the **LanguageID**, check [**SRModeID**](srmodeid-property.md) or [**TTSModeID**](ttsmodeid-property.md).</span></span> <span data-ttu-id="4ae0f-185">Wenn Sie **LanguageID** nicht festlegen, wird Sie auf die Einstellung Benutzer-ID der Standardsprache festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4ae0f-185">If you do not set **LanguageID**, it will be set to the user default language ID setting.</span></span>

<span data-ttu-id="4ae0f-186">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="4ae0f-186">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="4ae0f-187">Wenn Sie **LanguageID** auf eine Sprache festlegen, die bidirektionalen Text (z. b. Arabisch oder Hebräisch) unterstützt, aber das System, auf dem Ihre Anwendung ausgeführt wird, nicht über eine bidirektionale Unterstützung verfügt, wird der Text in der Wort Sprechblase in logischer und nicht in Anzeige</span><span class="sxs-lookup"><span data-stu-id="4ae0f-187">If you set **LanguageID** to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text in the word balloon will appear in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="4ae0f-188">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4ae0f-188">See Also</span></span>

<span data-ttu-id="4ae0f-189">[**Srmodeid-Eigenschaft**](srmodeid-property.md), [ **ttsmodeid-Eigenschaft**](ttsmodeid-property.md)</span><span class="sxs-lookup"><span data-stu-id="4ae0f-189">[**SRModeID property**](srmodeid-property.md), [**TTSModeID property**](ttsmodeid-property.md)</span></span>


 

 




