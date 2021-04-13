---
title: Listencomplete-Ereignis
description: Listencomplete-Ereignis
ms.assetid: 29e3f424-17b4-4287-b644-ed62b80e0035
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dbfe0fac272b50af3f82efdc8a422bebddbf786
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388667"
---
# <a name="listencomplete-event"></a><span data-ttu-id="c9ce5-103">Listencomplete-Ereignis</span><span class="sxs-lookup"><span data-stu-id="c9ce5-103">ListenComplete Event</span></span>

<span data-ttu-id="c9ce5-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="c9ce5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c9ce5-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c9ce5-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c9ce5-106">Tritt auf, wenn der Überwachungsmodus (Spracherkennung) beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c9ce5-106">Occurs when Listening mode (speech recognition) has ended.</span></span>

</dd> <dt>

<span data-ttu-id="c9ce5-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="c9ce5-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c9ce5-108">**Sub** *Agent. \* \* \* listencomplete (ByVal*- \*  *Kenn zeichenkennung*, **ByVal** - *Ursache \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="c9ce5-108">**Sub** *agent.\*\*\*ListenComplete (ByVal*\* *CharacterID*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="c9ce5-109">Teil</span><span class="sxs-lookup"><span data-stu-id="c9ce5-109">Part</span></span>          | <span data-ttu-id="c9ce5-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c9ce5-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9ce5-111">*Merkmal-ID*</span><span class="sxs-lookup"><span data-stu-id="c9ce5-111">*CharacterID*</span></span> | <span data-ttu-id="c9ce5-112">Gibt die ID des überwachungzeichens als Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="c9ce5-112">Returns the ID of the listening character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="c9ce5-113">*Ursache*</span><span class="sxs-lookup"><span data-stu-id="c9ce5-113">*Cause*</span></span>       | <span data-ttu-id="c9ce5-114">Gibt die Ursache für das Complete-Ereignis als Ganzzahl zurück, die eines der folgenden sein kann: 1 der Empfangsmodus wurde vom Programmcode ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="c9ce5-114">Returns the cause of the complete event as an integer that may be one of the following: 1 Listening mode was turned off by program code.</span></span><br/> <span data-ttu-id="c9ce5-115">Zeitüberschreitung bei 2 Überwachungsmodus (durch Programmcode aktiviert).</span><span class="sxs-lookup"><span data-stu-id="c9ce5-115">2 Listening mode (turned on by program code) timed out.</span></span><br/> <span data-ttu-id="c9ce5-116">beim 3-Empfangsmodus (aktiviert durch den abhörenden Schlüssel) ist ein Timeout aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c9ce5-116">3 Listening mode (turned on by the Listening key) timed out.</span></span><br/> <span data-ttu-id="c9ce5-117">4 der Empfangsmodus wurde deaktiviert, da der Benutzer die Abhör Taste losgelassen hat.</span><span class="sxs-lookup"><span data-stu-id="c9ce5-117">4 Listening mode was turned off because the user released the Listening key.</span></span><br/> <span data-ttu-id="c9ce5-118">5 der Empfangsmodus wurde beendet, da der Benutzer die Sprache beendet hat.</span><span class="sxs-lookup"><span data-stu-id="c9ce5-118">5 Listening mode ended because the user finished speaking.</span></span><br/> <span data-ttu-id="c9ce5-119">6 der Empfangsmodus wurde beendet, weil der Eingabe aktive Client deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="c9ce5-119">6 Listening mode ended because the input-active client was deactivated.</span></span><br/> <span data-ttu-id="c9ce5-120">7 der Empfangsmodus wurde beendet, da das Standard Zeichen geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="c9ce5-120">7 Listening mode ended because the default character was changed.</span></span><br/> <span data-ttu-id="c9ce5-121">8 der Empfangsmodus wurde beendet, da der Benutzer die Spracheingabe deaktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="c9ce5-121">8 Listening mode ended because the user disabled speech input.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="c9ce5-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9ce5-122">Remarks</span></span>

<span data-ttu-id="c9ce5-123">Dieses Ereignis wird an alle Clients gesendet, wenn das Timeout für den Lesemodus endet, nachdem der Benutzer den Überwachungs Schlüssel losgelassen hat, wenn der aktive [**Client der Eingabe die Abhör Methode mit**](listen-method.md) **false** aufruft oder der Benutzer die Sprache beendet hat.</span><span class="sxs-lookup"><span data-stu-id="c9ce5-123">This event is sent to all clients when the Listening mode time-out ends, after the user releases the Listening key, when the input active client calls the [**Listen**](listen-method.md) method with **False**, or the user finished speaking.</span></span> <span data-ttu-id="c9ce5-124">Sie können dieses Ereignis verwenden, um zu bestimmen, wann die Ausgabe eines Zeichens (Audioausgabe) fortgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c9ce5-124">You can use this event to determine when to resume character spoken (audio) output.</span></span>

<span data-ttu-id="c9ce5-125">Wenn Sie den Empfangsmodus mithilfe der Abhör Methode einschalten und der Benutzer dann die Abhör Taste drückt, wird der Lesemodus zurückgesetzt und fortgesetzt, bis das Timeout [**für die Abhör**](listen-method.md) Taste erreicht ist, der Schlüssel für die Überwachung freigegeben wird oder der Benutzer die Sprache abschließt, je nachdem, welcher Wert später angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c9ce5-125">If you turn on Listening mode using the [**Listen**](listen-method.md) method and then the user presses the Listening key, the Listening mode resets and continues until the Listening key time-out completes, the Listening key is released, or the user finishes speaking, whichever is later.</span></span> <span data-ttu-id="c9ce5-126">In dieser Situation wird erst dann ein **listencomplete** -Ereignis empfangen, wenn der Modus des abhörenden Schlüssels abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="c9ce5-126">In this situation, you will not receive a **ListenComplete** event until the listening key's mode completes.</span></span>

<span data-ttu-id="c9ce5-127">Das-Ereignis gibt das Zeichen an die Clients zurück, für die zurzeit dieses Zeichen geladen ist.</span><span class="sxs-lookup"><span data-stu-id="c9ce5-127">The event returns the character to the clients that currently have this character loaded.</span></span> <span data-ttu-id="c9ce5-128">Alle anderen Clients erhalten ein NULL-Zeichen (leere Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="c9ce5-128">All other clients receive a null character (empty string).</span></span>

### <a name="see-also"></a><span data-ttu-id="c9ce5-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c9ce5-129">See Also</span></span>

<span data-ttu-id="c9ce5-130">[**ListenStart-Ereignis**](listenstart-event.md), Abhör [ **Methode**](listen-method.md)</span><span class="sxs-lookup"><span data-stu-id="c9ce5-130">[**ListenStart event**](listenstart-event.md), [**Listen method**](listen-method.md)</span></span>


 

 





