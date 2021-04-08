---
title: Srstatus (Eigenschaft)
description: Srstatus (Eigenschaft)
ms.assetid: 67618a35-05e4-4bb3-b910-c75de6e32578
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64cb6ba16bc024a52b65efa98c22fd089ad79da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037630"
---
# <a name="srstatus-property"></a><span data-ttu-id="46f9b-103">Srstatus (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="46f9b-103">SRStatus Property</span></span>

<span data-ttu-id="46f9b-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="46f9b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="46f9b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="46f9b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="46f9b-106">Gibt zurück, ob Spracheingaben für das Zeichen gestartet werden können.</span><span class="sxs-lookup"><span data-stu-id="46f9b-106">Returns whether speech input can be started for the character.</span></span>

</dd> <dt>

<span data-ttu-id="46f9b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="46f9b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="46f9b-108">*Büros. ***Zeichen ("*** Merkmal-ID \* \* *"). Srstatus**</span><span class="sxs-lookup"><span data-stu-id="46f9b-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").SRStatus**</span></span>



| <span data-ttu-id="46f9b-109">Wert</span><span class="sxs-lookup"><span data-stu-id="46f9b-109">Value</span></span> | <span data-ttu-id="46f9b-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46f9b-110">Description</span></span>                                                                                                                                                                                                                               |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46f9b-111">0</span><span class="sxs-lookup"><span data-stu-id="46f9b-111">0</span></span>     | <span data-ttu-id="46f9b-112">Bedingungen unterstützen Spracheingaben.</span><span class="sxs-lookup"><span data-stu-id="46f9b-112">Conditions support speech input.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="46f9b-113">1</span><span class="sxs-lookup"><span data-stu-id="46f9b-113">1</span></span>     | <span data-ttu-id="46f9b-114">Auf diesem System ist kein Audioeingabegerät verfügbar.</span><span class="sxs-lookup"><span data-stu-id="46f9b-114">There is no audio input device available on this system.</span></span> <span data-ttu-id="46f9b-115">(Beachten Sie, dass hierdurch nicht erkannt wird, ob ein Mikrofon installiert ist. es kann nur erkennen, ob der Benutzer über eine ordnungsgemäß installierte Audiokarte mit einem funktionierenden Treiber verfügt.)</span><span class="sxs-lookup"><span data-stu-id="46f9b-115">(Note that this does not detect whether a microphone is installed; it can only detect whether the user has a properly installed input-enabled sound card with a working driver.)</span></span> |
| <span data-ttu-id="46f9b-116">2</span><span class="sxs-lookup"><span data-stu-id="46f9b-116">2</span></span>     | <span data-ttu-id="46f9b-117">Ein anderer Client ist der aktive Client dieses Zeichens, oder das aktuelle Zeichen ist nicht oberstes Zeichen.</span><span class="sxs-lookup"><span data-stu-id="46f9b-117">Another client is the active client of this character, or the current character is not topmost.</span></span>                                                                                                                                           |
| <span data-ttu-id="46f9b-118">3</span><span class="sxs-lookup"><span data-stu-id="46f9b-118">3</span></span>     | <span data-ttu-id="46f9b-119">Die Audioeingabe oder der Ausgabekanal ist derzeit ausgelastet, eine Anwendung verwendet Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="46f9b-119">The audio input or output channel is currently busy, an application is using audio.</span></span>                                                                                                                                                       |
| <span data-ttu-id="46f9b-120">4</span><span class="sxs-lookup"><span data-stu-id="46f9b-120">4</span></span>     | <span data-ttu-id="46f9b-121">Beim Initialisieren des sprach Erkennungs Subsystems ist ein nicht spezifizierter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="46f9b-121">An unspecified error occurred in the process of initializing the speech recognition subsystem.</span></span> <span data-ttu-id="46f9b-122">Dies schließt die Möglichkeit ein, dass keine Sprach-Engine verfügbar ist, die der Spracheinstellung des Zeichens entspricht.</span><span class="sxs-lookup"><span data-stu-id="46f9b-122">This includes the possibility that there is no speech engine available matching the character's language setting.</span></span>                          |
| <span data-ttu-id="46f9b-123">5</span><span class="sxs-lookup"><span data-stu-id="46f9b-123">5</span></span>     | <span data-ttu-id="46f9b-124">Der Benutzer hat die Spracheingabe in den erweiterten Zeichen Optionen deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="46f9b-124">The user has disabled speech input in the Advanced Character Options.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="46f9b-125">6</span><span class="sxs-lookup"><span data-stu-id="46f9b-125">6</span></span>     | <span data-ttu-id="46f9b-126">Beim Überprüfen des Audiostatus ist ein Fehler aufgetreten, aber die Ursache des Fehlers wurde vom System nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="46f9b-126">An error occurred in checking the audio status, but the cause of the error was not returned by the system.</span></span>                                                                                                                                |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46f9b-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46f9b-127">Remarks</span></span>

<span data-ttu-id="46f9b-128">Diese Eigenschaft gibt die für die Unterstützung der Spracheingabe erforderlichen Bedingungen zurück, einschließlich des Status des Audiogeräts.</span><span class="sxs-lookup"><span data-stu-id="46f9b-128">This property returns the conditions necessary to support speech input, including the status of the audio device.</span></span> <span data-ttu-id="46f9b-129">Sie können diese Eigenschaft überprüfen, bevor Sie die Abhör Methode aufzurufen, [**um deren Erfolg**](listen-method.md) besser sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="46f9b-129">You can check this property before you call the [**Listen**](listen-method.md) method to better ensure its success.</span></span>

<span data-ttu-id="46f9b-130">Wenn Spracheingaben auf der Eigenschaften Seite des-Agents aktiviert sind (erweiterte Zeichen Optionen), wird beim Abfragen dieser Eigenschaft die zugeordnete Engine geladen, wenn Sie nicht bereits geladen ist, und Sprachdienste starten.</span><span class="sxs-lookup"><span data-stu-id="46f9b-130">When speech input is enabled in the Agent property sheet (Advanced Character Options), querying this property will load the associated engine, if it is not already loaded, and start speech services.</span></span> <span data-ttu-id="46f9b-131">Das heißt, der Abhör Schlüssel ist verfügbar, und der lauschabltip ist automatisch anzeigbar.</span><span class="sxs-lookup"><span data-stu-id="46f9b-131">That is, the Listening key is available, and the Listening Tip is automatically displayable.</span></span> <span data-ttu-id="46f9b-132">(Der Abhör Schlüssel und der lauschtip sind nur aktiviert, wenn Sie auch in erweiterten Zeichen Optionen aktiviert sind.) Wenn Sie jedoch die-Eigenschaft Abfragen, wenn die Sprache deaktiviert ist, startet der Server die Sprachdienste nicht.</span><span class="sxs-lookup"><span data-stu-id="46f9b-132">(The Listening key and Listening Tip are only enabled if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="46f9b-133">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="46f9b-133">This property only applies to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="46f9b-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="46f9b-134">See Also</span></span>

[<span data-ttu-id="46f9b-135">**Abhör Methode**</span><span class="sxs-lookup"><span data-stu-id="46f9b-135">**Listen method**</span></span>](listen-method.md)


 

 




