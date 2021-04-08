---
title: ListenStart-Ereignis
description: ListenStart-Ereignis
ms.assetid: 59feacd6-0b9f-4bf4-b544-48de49384312
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b8cc19ad727f8e9c4606bbbfba7b2e03e7d638
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856788"
---
# <a name="listenstart-event"></a><span data-ttu-id="2e74f-103">ListenStart-Ereignis</span><span class="sxs-lookup"><span data-stu-id="2e74f-103">ListenStart Event</span></span>

<span data-ttu-id="2e74f-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="2e74f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2e74f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2e74f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2e74f-106">Tritt auf, wenn der Empfangsmodus beginnt (Spracherkennung).</span><span class="sxs-lookup"><span data-stu-id="2e74f-106">Occurs when Listening mode (speech recognition) begins.</span></span>

</dd> <dt>

<span data-ttu-id="2e74f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="2e74f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2e74f-108">**Sub** - *Agent. \* \* \* ListenStart (ByVal*- \*  *Merkmal-ID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="2e74f-108">**Sub** *agent.\*\*\*ListenStart (ByVal*\* *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="2e74f-109">Teil</span><span class="sxs-lookup"><span data-stu-id="2e74f-109">Part</span></span>          | <span data-ttu-id="2e74f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2e74f-110">Description</span></span>                                            |
|---------------|--------------------------------------------------------|
| <span data-ttu-id="2e74f-111">*Merkmal-ID*</span><span class="sxs-lookup"><span data-stu-id="2e74f-111">*CharacterID*</span></span> | <span data-ttu-id="2e74f-112">Gibt die ID des überwachungzeichens als Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="2e74f-112">Returns the ID of the listening character as a string.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="2e74f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e74f-113">Remarks</span></span>

<span data-ttu-id="2e74f-114">Dieses Ereignis wird an alle Clients gesendet, wenn der Empfangsmodus beginnt, da der Benutzer die Abhör Taste gedrückt hat oder der Eingabe aktive [**Client die Abhör Methode mit**](listen-method.md) **true** aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="2e74f-114">This event is sent to all clients when Listening mode begins because the user pressed the Listening key or the input-active client called the [**Listen**](listen-method.md) method with **True**.</span></span> <span data-ttu-id="2e74f-115">Sie können dieses Ereignis verwenden, um zu vermeiden, dass Ihr Zeichen in den Modus "on" (lauschen) wechselt.</span><span class="sxs-lookup"><span data-stu-id="2e74f-115">You can use this event to avoid having your character speak while the Listening mode is on.</span></span>

<span data-ttu-id="2e74f-116">Wenn Sie den Empfangsmodus mit der Abhör [**Methode aktivieren**](listen-method.md) und der Benutzer dann die Abhör Taste drückt, wird der Lesemodus zurückgesetzt und fortgesetzt, bis das Timeout für die Überwachung abgeschlossen ist, der Schlüssel für die Überwachung freigegeben wird oder der Benutzer die Sprache abschließt, je nachdem, welcher Wert später angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2e74f-116">If you turn on Listening mode with the [**Listen**](listen-method.md) method and then the user presses the Listening key, the Listening mode resets and continues until the Listening key time-out completes, the Listening key is released, or the user finishes speaking, whichever is later.</span></span> <span data-ttu-id="2e74f-117">Wenn der Überwachungsmodus bereits auf on on ist, wird ein zusätzliches **ListenStart** -Ereignis nicht angezeigt, wenn der Benutzer die Abhör Taste drückt.</span><span class="sxs-lookup"><span data-stu-id="2e74f-117">In this situation, when Listening mode is already on, you will not get an additional **ListenStart** event when the user presses the Listening key.</span></span>

<span data-ttu-id="2e74f-118">Das-Ereignis gibt das Zeichen an die Clients zurück, für die zurzeit dieses Zeichen geladen ist.</span><span class="sxs-lookup"><span data-stu-id="2e74f-118">The event returns the character to the clients that currently have this character loaded.</span></span> <span data-ttu-id="2e74f-119">Alle anderen Clients erhalten ein NULL-Zeichen (leere Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="2e74f-119">All other clients receive a null character (empty string).</span></span>

### <a name="see-also"></a><span data-ttu-id="2e74f-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2e74f-120">See Also</span></span>

<span data-ttu-id="2e74f-121">[**Listencomplete-Ereignis**](listencomplete-event.md), Abhör [ **Methode**](listen-method.md)</span><span class="sxs-lookup"><span data-stu-id="2e74f-121">[**ListenComplete event**](listencomplete-event.md), [**Listen method**](listen-method.md)</span></span>


 

 




