---
title: Iagentnotifysinkex listeningstate
description: Iagentnotifysinkex listeningstate
ms.assetid: e303b299-0dd0-419a-87a9-1490fe6cf54a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fee8f931030cbd68cd148fc57360d8b0ccf7624
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515830"
---
# <a name="iagentnotifysinkexlisteningstate"></a><span data-ttu-id="115f2-103">Iagentnotifysinkex:: listeningstate</span><span class="sxs-lookup"><span data-stu-id="115f2-103">IAgentNotifySinkEx::ListeningState</span></span>

<span data-ttu-id="115f2-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="115f2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ListeningState(
   long dwCharacterID,  // character ID
   long bListening,     // listening mode state
   long dwCause         // cause  
);
```

<span data-ttu-id="115f2-105">Benachrichtigt eine Client Anwendung, wenn der überwachungmodus geändert wird.</span><span class="sxs-lookup"><span data-stu-id="115f2-105">Notifies a client application when the Listening mode changes.</span></span>

-   <span data-ttu-id="115f2-106">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="115f2-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="115f2-107"><span id="dwCharacterID"></span><span id="dwcharacterid"></span><span id="DWCHARACTERID"></span>*dwcharakteriid*</span><span class="sxs-lookup"><span data-stu-id="115f2-107"><span id="dwCharacterID"></span><span id="dwcharacterid"></span><span id="DWCHARACTERID"></span>*dwCharacterID*</span></span>
</dt> <dd>

<span data-ttu-id="115f2-108">Das Zeichen, für das sich der Überwachungszustand geändert hat.</span><span class="sxs-lookup"><span data-stu-id="115f2-108">The character for which the listening state changed.</span></span>

</dd> <dt>

<span data-ttu-id="115f2-109"><span id="bListening"></span><span id="blistening"></span><span id="BLISTENING"></span>*blistening*</span><span class="sxs-lookup"><span data-stu-id="115f2-109"><span id="bListening"></span><span id="blistening"></span><span id="BLISTENING"></span>*bListening*</span></span>
</dt> <dd>

<span data-ttu-id="115f2-110">Der Status des Überwachungsmodus.</span><span class="sxs-lookup"><span data-stu-id="115f2-110">The Listening mode state.</span></span> <span data-ttu-id="115f2-111">**True** gibt an, dass der Empfangsmodus gestartet wurde. **False** gibt an, dass der Empfangsmodus beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="115f2-111">**True** indicates that Listening mode has started; **False**, that Listening mode has ended.</span></span>

</dd> <dt>

<span data-ttu-id="115f2-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwcause*</span><span class="sxs-lookup"><span data-stu-id="115f2-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="115f2-113">Die Ursache für das Ereignis, bei der es sich möglicherweise um einen der folgenden Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="115f2-113">The cause for the event, which may be one of the following values.</span></span>



| <span data-ttu-id="115f2-114">Wert</span><span class="sxs-lookup"><span data-stu-id="115f2-114">Value</span></span>                                                                             | <span data-ttu-id="115f2-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="115f2-115">Description</span></span>                                                                    |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="115f2-116">die Konstante " **Ganzzahl ohne Vorzeichen long** **lscomplete" \_ verursacht \_ Programm deaktiviert = 1;**</span><span class="sxs-lookup"><span data-stu-id="115f2-116">**const unsigned long** **LSCOMPLETE\_CAUSE\_PROGRAMDISABLED = 1;**</span></span><br/>    | <span data-ttu-id="115f2-117">Der Empfangsmodus wurde durch Programmcode ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="115f2-117">Listening mode was turned off by program code.</span></span>                                 |
| <span data-ttu-id="115f2-118">die Konstante " **Ganzzahl ohne Vorzeichen long** **lscomplete" \_ bewirkt \_ , dass Program TimedOut = 2;**</span><span class="sxs-lookup"><span data-stu-id="115f2-118">**const unsigned long** **LSCOMPLETE\_CAUSE\_PROGRAMTIMEDOUT = 2;**</span></span><br/>    | <span data-ttu-id="115f2-119">Timeout beim lauschen-Modus (durch Programmcode aktiviert).</span><span class="sxs-lookup"><span data-stu-id="115f2-119">Listening mode (turned on by program code) timed out.</span></span>                          |
| <span data-ttu-id="115f2-120">Konstante **Länge ohne** Vorzeichen **lscomplete \_ bewirkt \_ usertimedout = 3;**</span><span class="sxs-lookup"><span data-stu-id="115f2-120">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERTIMEDOUT = 3;**</span></span><br/>       | <span data-ttu-id="115f2-121">Timeout beim überwachenden Modus (aktiviert durch den abhörenden Schlüssel).</span><span class="sxs-lookup"><span data-stu-id="115f2-121">Listening mode (turned on by the Listening key) timed out.</span></span>                     |
| <span data-ttu-id="115f2-122">Konstante **Länge ohne** Vorzeichen **lscomplete \_ bewirkt \_ userreleasedkey = 4;**</span><span class="sxs-lookup"><span data-stu-id="115f2-122">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERRELEASEDKEY = 4;**</span></span><br/>    | <span data-ttu-id="115f2-123">Der Empfangsmodus wurde deaktiviert, da der Benutzer die Abhör Taste losgelassen hat.</span><span class="sxs-lookup"><span data-stu-id="115f2-123">Listening mode was turned off because the user released the Listening key.</span></span>     |
| <span data-ttu-id="115f2-124">Konstante **Länge ohne** Vorzeichen **lscomplete \_ bewirkt, dass \_ userutterancebeendeten = 5;**</span><span class="sxs-lookup"><span data-stu-id="115f2-124">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERUTTERANCEENDED = 5;**</span></span><br/> | <span data-ttu-id="115f2-125">Der Empfangsmodus wurde deaktiviert, da der Benutzer die sprachbearbeitung beendet hat.</span><span class="sxs-lookup"><span data-stu-id="115f2-125">Listening mode was turned off because the user finished speaking.</span></span>              |
| <span data-ttu-id="115f2-126">Konstante " **Ganzzahl ohne Vorzeichen long** **lscomplete \_ " \_ CLIENTDEACTIVATED = 6;**</span><span class="sxs-lookup"><span data-stu-id="115f2-126">**const unsigned long** **LSCOMPLETE\_CAUSE\_CLIENTDEACTIVATED = 6;**</span></span><br/>  | <span data-ttu-id="115f2-127">Der Abhör Modus wurde deaktiviert, da der aktive Client für die Eingabe deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="115f2-127">Listening mode was turned off because the input active client was deactivated.</span></span> |
| <span data-ttu-id="115f2-128">Konstante " **Ganzzahl ohne Vorzeichen long** **lscomplete": \_ \_ defaultcharchange = 7**</span><span class="sxs-lookup"><span data-stu-id="115f2-128">**const unsigned long** **LSCOMPLETE\_CAUSE\_DEFAULTCHARCHANGE = 7**</span></span><br/>   | <span data-ttu-id="115f2-129">Der Abhör Modus wurde deaktiviert, da das Standard Zeichen geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="115f2-129">Listening mode was turned off because the default character was changed.</span></span>       |
| <span data-ttu-id="115f2-130">Konstante " **Ganzzahl ohne Vorzeichen long** **lscomplete": \_ \_ userdeaktiviert = 8**</span><span class="sxs-lookup"><span data-stu-id="115f2-130">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERDISABLED = 8**</span></span><br/>        | <span data-ttu-id="115f2-131">Der Abhör Modus wurde deaktiviert, da der Benutzer die Spracheingabe deaktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="115f2-131">Listening mode was turned off because the user disabled speech input.</span></span>          |



 

</dd> </dl>

<span data-ttu-id="115f2-132">Dieses Ereignis wird an alle Clients gesendet, wenn der Empfangsmodus beginnt, nachdem der Benutzer die Abhör Taste gedrückt hat oder wenn das Timeout abgelaufen ist, oder wenn der Eingabe aktive Client die Methode [**iagentcharakteriex::**](iagentcharacterex--listen.md) Listening mit **true** oder **false** aufruft.</span><span class="sxs-lookup"><span data-stu-id="115f2-132">This event is sent to all clients when the Listening mode begins after the user presses the Listening key or when its time-out ends, or when the input-active client calls the [**IAgentCharacterEx::Listen**](iagentcharacterex--listen.md) method with **True** or **False**.</span></span>

<span data-ttu-id="115f2-133">Das Ereignis gibt Werte an die Clients zurück, für die dieses Zeichen zurzeit geladen ist.</span><span class="sxs-lookup"><span data-stu-id="115f2-133">The event returns values to the clients that currently have this character loaded.</span></span> <span data-ttu-id="115f2-134">Alle anderen Clients erhalten ein NULL-Zeichen (leere Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="115f2-134">All other clients receive a null character (empty string).</span></span>

## <a name="see-also"></a><span data-ttu-id="115f2-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="115f2-135">See Also</span></span>

[<span data-ttu-id="115f2-136">**Iagentcharakteriex:: lauschen**</span><span class="sxs-lookup"><span data-stu-id="115f2-136">**IAgentCharacterEx::Listen**</span></span>](iagentcharacterex--listen.md)


 

 





