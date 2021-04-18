---
title: Srmodeid (Eigenschaft)
description: Srmodeid (Eigenschaft)
ms.assetid: 4c784fc5-d2c2-4e5b-ba5f-f59b4507f40f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898f90a70c29d409eaa12df3d3fde845e35bd5ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341684"
---
# <a name="srmodeid-property"></a><span data-ttu-id="68bab-103">Srmodeid (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="68bab-103">SRModeID Property</span></span>

<span data-ttu-id="68bab-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="68bab-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="68bab-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="68bab-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="68bab-106">Gibt die sprach Erkennungs-Engine zurück, die das Zeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="68bab-106">Returns or sets the speech recognition engine the character uses.</span></span>

</dd> <dt>

<span data-ttu-id="68bab-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="68bab-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="68bab-108">\*Agent ***. Zeichen ("*** Merkmal-ID \* \* *"). Srmodeid* \*  \[  =  *modeid*\]</span><span class="sxs-lookup"><span data-stu-id="68bab-108">*agent ***.Characters("*** CharacterID\*\*\*").SRModeID*\* \[ = *ModeID*\]</span></span>



| <span data-ttu-id="68bab-109">Teil</span><span class="sxs-lookup"><span data-stu-id="68bab-109">Part</span></span>     | <span data-ttu-id="68bab-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="68bab-110">Description</span></span>                                                             |
|----------|-------------------------------------------------------------------------|
| <span data-ttu-id="68bab-111">*Modeid*</span><span class="sxs-lookup"><span data-stu-id="68bab-111">*ModeID*</span></span> | <span data-ttu-id="68bab-112">Ein Zeichen folgen Ausdruck, der der Mode-ID einer Sprach-Engine entspricht.</span><span class="sxs-lookup"><span data-stu-id="68bab-112">A string expression that corresponds to the mode ID of a speech engine.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68bab-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68bab-113">Remarks</span></span>

<span data-ttu-id="68bab-114">Die-Eigenschaft bestimmt die sprach Erkennungs-Engine, die vom Zeichen für die Spracheingabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="68bab-114">The property determines the speech recognition engine used by the character for speech input.</span></span> <span data-ttu-id="68bab-115">Die Mode-ID für eine Spracherkennungs-Engine ist eine formatierte Zeichenfolge, die vom Sprachanbieter definiert wird, der die Engine eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="68bab-115">The mode ID for a speech recognition engine is a formatted string defined by the speech vendor that uniquely identifies the engine.</span></span> <span data-ttu-id="68bab-116">Weitere Informationen finden Sie unter [zugreifen auf eine Sprach-Engine in Ihrem Code](accessing-a-speech-engine-in-your-code.md).</span><span class="sxs-lookup"><span data-stu-id="68bab-116">For more information, see [Accessing a Speech Engine In Your Code](accessing-a-speech-engine-in-your-code.md).</span></span>

<span data-ttu-id="68bab-117">Wenn Sie eine Modus-ID für eine Sprach-Engine angeben, die nicht installiert ist, wenn der Benutzer die Spracherkennung deaktiviert hat (auf dem Eigenschaften Blatt des Microsoft-Agents) oder wenn die Sprache der angegebenen Sprach-Engine nicht mit der [**LanguageID**](languageid-property.md) -Einstellung des Zeichens identisch ist, löst der Server einen Fehler aus.</span><span class="sxs-lookup"><span data-stu-id="68bab-117">If you specify a mode ID for a speech engine that isn't installed, if the user has disabled speech recognition (in the Microsoft Agent property sheet), or if the language of the specified speech engine doesn't match the character's [**LanguageID**](languageid-property.md) setting, the server raises an error.</span></span>

<span data-ttu-id="68bab-118">Wenn Sie diese Eigenschaft Abfragen und die Spracherkennungs-Engine nicht bereits (erfolgreich) festgelegt haben, gibt der Server die Mode-ID der Engine zurück, die SAPI basierend auf der [**LanguageID**](languageid-property.md) -Einstellung des Zeichens zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="68bab-118">If you query this property and haven't already (successfully) set the speech recognition engine, the server returns the mode ID of the engine that SAPI returns based on the character's [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="68bab-119">Wenn Sie die **LanguageID** des Zeichens nicht festgelegt haben, gibt der-Agent die Mode-ID der Engine zurück, die von SAPI basierend auf der Standardeinstellung für die Sprach-ID des Benutzers zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="68bab-119">If you haven't set the character's **LanguageID**, then Agent returns the mode ID of the engine that SAPI returns based on the user's default language ID setting.</span></span> <span data-ttu-id="68bab-120">Wenn keine übereinstimmende Engine vorhanden ist, gibt der Server eine leere Zeichenfolge ("") zurück.</span><span class="sxs-lookup"><span data-stu-id="68bab-120">If there is no matching engine, the server returns an empty string ("").</span></span> <span data-ttu-id="68bab-121">Das Abfragen dieser Eigenschaft erfordert nicht, dass " [**speechinput. aktiviert**](https://www.bing.com/search?q=**SpeechInput.Enabled**) " auf " **true**" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="68bab-121">Querying this property does not require that [**SpeechInput.Enabled**](https://www.bing.com/search?q=**SpeechInput.Enabled**) be set to **True**.</span></span> <span data-ttu-id="68bab-122">Wenn Sie jedoch die-Eigenschaft Abfragen, wenn die Spracheingabe deaktiviert ist, gibt der Server eine leere Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="68bab-122">However, if you query the property when speech input is disabled, the server returns an empty string.</span></span>

<span data-ttu-id="68bab-123">Wenn die Spracheingabe aktiviert ist (im Fenster Erweiterte Zeichen Optionen), wird durch das Abfragen oder Festlegen dieser Eigenschaft die zugeordnete Engine geladen (falls Sie nicht bereits geladen wurde), und die Sprachdienste werden gestartet.</span><span class="sxs-lookup"><span data-stu-id="68bab-123">When speech input is enabled (in the Advanced Character Options window), querying or setting this property will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="68bab-124">Das heißt, der lauschende Schlüssel ist verfügbar, und der Abhör Tipp kann angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="68bab-124">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="68bab-125">(Der Abhör Schlüssel und der lauschtip sind nur aktiviert, wenn Sie auch in erweiterten Zeichen Optionen aktiviert sind.) Wenn Sie jedoch die-Eigenschaft Abfragen, wenn die Sprache deaktiviert ist, startet der Server die Sprachdienste nicht.</span><span class="sxs-lookup"><span data-stu-id="68bab-125">(The Listening key and Listening Tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="68bab-126">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="68bab-126">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="68bab-127">Die Sprach-Engine-Anforderungen von Microsoft Agent basieren auf der Microsoft Speech-API.</span><span class="sxs-lookup"><span data-stu-id="68bab-127">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="68bab-128">Module, die die SAPI-Anforderungen von Microsoft Agent unterstützen, können installiert und mit dem-Agent verwendet werden</span><span class="sxs-lookup"><span data-stu-id="68bab-128">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

> [!Note]  
> <span data-ttu-id="68bab-129">Diese Eigenschaft gibt auch die leere Zeichenfolge zurück, wenn auf dem System keine kompatible Soundunterstützung installiert ist.</span><span class="sxs-lookup"><span data-stu-id="68bab-129">This property also returns the empty string if you have no compatible sound support installed on your system.</span></span>

 

> [!Note]  
> <span data-ttu-id="68bab-130">Das Abfragen dieser Eigenschaft gibt in der Regel keinen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="68bab-130">Querying this property does not typically return an error.</span></span> <span data-ttu-id="68bab-131">Wenn die Sprach-Engine jedoch eine ungewöhnlich lange Ladezeit benötigt, erhalten Sie möglicherweise eine Fehlermeldung, die angibt, dass die Abfrage abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="68bab-131">However, if the speech engine takes an abnormally long time to load, you may get an error indicating that the query timed out.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="68bab-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="68bab-132">See Also</span></span>

[<span data-ttu-id="68bab-133">**LanguageID (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="68bab-133">**LanguageID property**</span></span>](languageid-property.md)


 

 




