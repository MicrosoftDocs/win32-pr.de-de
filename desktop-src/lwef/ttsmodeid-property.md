---
title: Ttsmodeid (Eigenschaft)
description: Ttsmodeid (Eigenschaft)
ms.assetid: 9205c37e-e006-466a-9b33-b98408c01ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6852f203f5df716df6cfc5962f9cfa911d8fc1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207222"
---
# <a name="ttsmodeid-property"></a><span data-ttu-id="e7741-103">Ttsmodeid (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e7741-103">TTSModeID Property</span></span>

<span data-ttu-id="e7741-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="e7741-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e7741-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e7741-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e7741-106">Gibt den für das Zeichen verwendeten TTS-Engine-Modus zurück oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="e7741-106">Returns or sets the TTS engine mode used for the character.</span></span>

</dd> <dt>

<span data-ttu-id="e7741-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="e7741-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e7741-108">\*Agent ***. Zeichen ("*** Merkmal-ID \* \* *"). Ttsmodeid* \*  \[  =  *modeid*\]</span><span class="sxs-lookup"><span data-stu-id="e7741-108">*agent ***.Characters ("*** CharacterID\*\*\*").TTSModeID*\* \[ = *ModeID*\]</span></span>



| <span data-ttu-id="e7741-109">Teil</span><span class="sxs-lookup"><span data-stu-id="e7741-109">Part</span></span>     | <span data-ttu-id="e7741-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e7741-110">Description</span></span>                                                             |
|----------|-------------------------------------------------------------------------|
| <span data-ttu-id="e7741-111">*Modeid*</span><span class="sxs-lookup"><span data-stu-id="e7741-111">*ModeID*</span></span> | <span data-ttu-id="e7741-112">Ein Zeichen folgen Ausdruck, der der Mode-ID einer Sprach-Engine entspricht.</span><span class="sxs-lookup"><span data-stu-id="e7741-112">A string expression that corresponds to the mode ID of a speech engine.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7741-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7741-113">Remarks</span></span>

<span data-ttu-id="e7741-114">Diese Eigenschaft bestimmt die ID des TTS (Text-zu-Sprache-Engine) für die gesprochene Ausgabe eines Zeichens.</span><span class="sxs-lookup"><span data-stu-id="e7741-114">This property determines the TTS (text-to-speech) engine mode ID for a character's spoken output.</span></span> <span data-ttu-id="e7741-115">Die Mode-ID für eine TTS-Engine ist eine formatierte Zeichenfolge, die vom Sprachanbieter definiert wird, der den Modus der Engine eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e7741-115">The mode ID for a TTS engine is a formatted string defined by the speech vendor that uniquely identifies the engine's mode.</span></span> <span data-ttu-id="e7741-116">Weitere Informationen finden Sie unter [zugreifen auf eine Sprach-Engine in Ihrem Code](accessing-a-speech-engine-in-your-code.md).</span><span class="sxs-lookup"><span data-stu-id="e7741-116">For more information, see [Accessing a Speech Engine in Your Code](accessing-a-speech-engine-in-your-code.md).</span></span>

<span data-ttu-id="e7741-117">Das Festlegen dieser Eigenschaft überschreibt den Versuch des Servers, eine Engine basierend auf der kompilierten TTS-Einstellung des Zeichens und der aktuellen [**LanguageID**](languageid-property.md) -Einstellung des Zeichens zu laden.</span><span class="sxs-lookup"><span data-stu-id="e7741-117">Setting this property overrides the server's attempt to load an engine based on the character's compiled TTS setting and the character's current [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="e7741-118">Wenn Sie jedoch eine Modus-ID für eine Engine angeben, die nicht installiert ist, oder wenn der Benutzer die Sprachausgabe im Microsoft-agenteigenschaftenblatt (**Audiooutput. aktiviert = false**) deaktiviert hat, löst der Server einen Fehler aus.</span><span class="sxs-lookup"><span data-stu-id="e7741-118">However, if you specify a mode ID for an engine that isn't installed or if the user has disabled speech output in the Microsoft Agent property sheet (**AudioOutput.Enabled = False**), the server raises an error.</span></span>

<span data-ttu-id="e7741-119">Wenn Sie nicht (oder nicht erfolgreich) eine TTS-Modus-ID für das Zeichen festgelegt haben, prüft der Server, ob die kompilierte TTS-Moduseinstellung des Zeichens mit der [**LanguageID**](languageid-property.md) -Einstellung des Zeichens übereinstimmt und ob die zugehörige TTS-Engine installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e7741-119">If you do not (or have not successfully) set a TTS mode ID for the character, the server checks to see if the character's compiled TTS mode setting matches the character's [**LanguageID**](languageid-property.md) setting, and that the associated TTS engine is installed.</span></span> <span data-ttu-id="e7741-120">Wenn dies der Fall ist, wird der "TTS"-Modus, der vom Zeichen für die gesprochene Ausgabe verwendet wird, und diese Eigenschaft gibt die</span><span class="sxs-lookup"><span data-stu-id="e7741-120">If so, the TTS mode used by the character for spoken output and this property returns that mode ID.</span></span> <span data-ttu-id="e7741-121">Wenn dies nicht der Grund ist, fordert der Server eine kompatible SAPI-Sprach-Engine an, die der **LanguageID** des Zeichens entspricht, sowie das Geschlecht und das Alter, die für die ID des kompilierten Modus des Zeichens festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="e7741-121">If not, the server requests a compatible SAPI speech engine that matches the **LanguageID** of the character, as well as the gender and age set for the character's compiled mode ID.</span></span> <span data-ttu-id="e7741-122">Wenn Sie die **LanguageID** des Zeichens nicht festgelegt haben, ist die **LanguageID** die aktuelle Benutzersprache.</span><span class="sxs-lookup"><span data-stu-id="e7741-122">If you have not set the character's **LanguageID**, its **LanguageID** is the current user language.</span></span> <span data-ttu-id="e7741-123">Wenn keine übereinstimmende Engine gefunden werden kann, gibt die Abfrage für diese Eigenschaft eine leere Zeichenfolge für die Modus-ID der Engine zurück.</span><span class="sxs-lookup"><span data-stu-id="e7741-123">If no matching engine can be found, querying for this property returns an empty string for the engine's mode ID.</span></span> <span data-ttu-id="e7741-124">Wenn Sie diese Eigenschaft Abfragen, wenn der Benutzer die Sprachausgabe im Microsoft-Agent-Eigenschaften Blatt (**Audiooutput. aktivierte = false**) deaktiviert hat, ist der Wert eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e7741-124">Similarly, if you query this property when the user has disabled speech output in the Microsoft Agent property sheet (**AudioOutput.Enabled = False**), the value will be an empty string.</span></span>

<span data-ttu-id="e7741-125">Durch Abfragen oder Festlegen dieser Eigenschaft wird die zugeordnete Engine geladen (sofern Sie nicht bereits geladen wurde).</span><span class="sxs-lookup"><span data-stu-id="e7741-125">Querying or setting this property will load the associated engine (if it is not already loaded).</span></span> <span data-ttu-id="e7741-126">Wenn jedoch die Engine, die in der kompilierten TTS-Einstellung des Zeichens angegeben ist, installiert ist und mit der Sprach-ID-Einstellung des Zeichens übereinstimmt, wird die Engine geladen, wenn das Zeichen geladen wird.</span><span class="sxs-lookup"><span data-stu-id="e7741-126">However, if the engine specified in the character's compiled TTS setting is installed and matches the character's language ID setting, the engine will be loaded when the character loads.</span></span>

<span data-ttu-id="e7741-127">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="e7741-127">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="e7741-128">Die Sprach-Engine-Anforderungen von Microsoft Agent basieren auf der Microsoft Speech-API.</span><span class="sxs-lookup"><span data-stu-id="e7741-128">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="e7741-129">Module, die die SAPI-Anforderungen von Microsoft Agent unterstützen, können installiert und mit dem-Agent verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e7741-129">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

> [!Note]  
> <span data-ttu-id="e7741-130">Diese Eigenschaft gibt auch die leere Zeichenfolge zurück, wenn auf dem System keine kompatible Soundunterstützung installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e7741-130">This property also returns the empty string if you have no compatible sound support installed on your system.</span></span>

 

> [!Note]  
> <span data-ttu-id="e7741-131">Das Festlegen der **ttsmodeid** kann fehlschlagen, wenn Speech.dll nicht installiert ist und die angegebene Engine nicht mit der kompilierten TTS-Moduseinstellung des Zeichens identisch ist.</span><span class="sxs-lookup"><span data-stu-id="e7741-131">Setting the **TTSModeID** can fail if Speech.dll is not installed and the engine you specify does not match the character's compiled TTS mode setting.</span></span>

 

> [!Note]  
> <span data-ttu-id="e7741-132">Das Abfragen dieser Eigenschaft gibt in der Regel keinen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="e7741-132">Querying this property does not typically return an error.</span></span> <span data-ttu-id="e7741-133">Wenn die Sprach-Engine jedoch eine ungewöhnlich lange Ladezeit benötigt, erhalten Sie möglicherweise eine Fehlermeldung, die angibt, dass die Abfrage abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="e7741-133">However, if the speech engine takes an abnormally long time to load, you may get an error indicating that the query timed out.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="e7741-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e7741-134">See Also</span></span>

[<span data-ttu-id="e7741-135">**LanguageID (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="e7741-135">**LanguageID property**</span></span>](languageid-property.md)


 

 




