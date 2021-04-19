---
title: Iagentnotifysinkex activeclientchange
description: Iagentnotifysinkex activeclientchange
ms.assetid: e953e803-c898-4c07-adc0-8b895b5e8473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96988f80d8a1799bf46f12bd38906e9357453f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341861"
---
# <a name="iagentnotifysinkexactiveclientchange"></a><span data-ttu-id="d5aff-103">Iagentnotifysinkex:: activeclientchange</span><span class="sxs-lookup"><span data-stu-id="d5aff-103">IAgentNotifySinkEx::ActiveClientChange</span></span>

<span data-ttu-id="d5aff-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="d5aff-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ActiveClientChange(
...long dwCharID,  // character ID
   long lStatus    // active state flag
);
```

<span data-ttu-id="d5aff-105">Benachrichtigt eine Client Anwendung, wenn der aktive Client nicht mehr der aktive Client eines Zeichens ist.</span><span class="sxs-lookup"><span data-stu-id="d5aff-105">Notifies a client application if its active client is no longer the active client of a character.</span></span>

-   <span data-ttu-id="d5aff-106">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="d5aff-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="d5aff-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwcharid*</span><span class="sxs-lookup"><span data-stu-id="d5aff-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="d5aff-108">Der Bezeichner des Zeichens, für das der Status des aktiven Clients geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="d5aff-108">Identifier of the character for which active client status changed.</span></span>

</dd> <dt>

<span data-ttu-id="d5aff-109"><span id="lStatus"></span><span id="lstatus"></span><span id="LSTATUS"></span>*lstatus*</span><span class="sxs-lookup"><span data-stu-id="d5aff-109"><span id="lStatus"></span><span id="lstatus"></span><span id="LSTATUS"></span>*lStatus*</span></span>
</dt> <dd>

<span data-ttu-id="d5aff-110">Aktive Zustandsänderung des Clients, bei der es sich um eine Kombination aus einem der folgenden Werte handeln kann:</span><span class="sxs-lookup"><span data-stu-id="d5aff-110">Active state change of the client, which can be a combination of any of the following values:</span></span>



| <span data-ttu-id="d5aff-111">Wert</span><span class="sxs-lookup"><span data-stu-id="d5aff-111">Value</span></span>                                                              | <span data-ttu-id="d5aff-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5aff-112">Description</span></span>                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="d5aff-113">Konstante " **Ganzzahl ohne Vorzeichen Short** " Aktivieren von " **\_ notactive" = 0;**</span><span class="sxs-lookup"><span data-stu-id="d5aff-113">**const unsigned short** **ACTIVATE\_NOTACTIVE = 0;**</span></span><br/>   | <span data-ttu-id="d5aff-114">Der Client ist nicht der aktive Client des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="d5aff-114">Your client is not the active client of the character.</span></span>                |
| <span data-ttu-id="d5aff-115">Konstante " **Ganzzahl ohne Vorzeichen Short** **" \_ aktiviert = 1;**</span><span class="sxs-lookup"><span data-stu-id="d5aff-115">**const unsigned short** **ACTIVATE\_ACTIVE = 1;**</span></span><br/>      | <span data-ttu-id="d5aff-116">Der Client ist der aktive Client des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="d5aff-116">Your client is the active client of the character.</span></span>                    |
| <span data-ttu-id="d5aff-117">Konstante " **Ganzzahl ohne Vorzeichen Short** **" \_ inputactive = 2;**</span><span class="sxs-lookup"><span data-stu-id="d5aff-117">**const unsigned short** **ACTIVATE\_INPUTACTIVE = 2;**</span></span><br/> | <span data-ttu-id="d5aff-118">Der Client ist Eingabe aktiv (aktiver Client des obersten Zeichens).</span><span class="sxs-lookup"><span data-stu-id="d5aff-118">Your client is input-active (active client of the topmost character).</span></span> |



 

</dd> </dl>

<span data-ttu-id="d5aff-119">Wenn mehrere Client Anwendungen dasselbe Zeichen gemeinsam verwenden, empfängt der aktive Client des Zeichens Maus Eingaben (z. b. Click-oder Drag-Ereignisse der Microsoft-agentsteuerung).</span><span class="sxs-lookup"><span data-stu-id="d5aff-119">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="d5aff-120">Wenn mehrere Zeichen angezeigt werden, empfängt der aktive Client des obersten Zeichens (auch als Input-Active Client bezeichnet) [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="d5aff-120">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives [**IAgentNotifySink::Command**](iagentnotifysink--command.md) events.</span></span>

<span data-ttu-id="d5aff-121">Wenn sich der aktive Client eines Zeichens ändert, übergibt dieses Ereignis die ID dieses Zeichens und **true** , wenn die Anwendung zum aktiven Client des Zeichens geworden ist, oder **false** , wenn es nicht mehr der aktive Client des Zeichens ist.</span><span class="sxs-lookup"><span data-stu-id="d5aff-121">When the active client of a character changes, this event passes back the ID of that character and **True** if your application has become the active client of the character or **False** if it is no longer the active client of the character.</span></span>

<span data-ttu-id="d5aff-122">Eine Client Anwendung empfängt dieses Ereignis möglicherweise, wenn der Benutzer im Popupmenü des Zeichens oder über den Sprachbefehl den Eintrag einer anderen Client Anwendung auswählt, die Client Anwendung seinen aktiven Status ändert oder eine andere Client Anwendung die Verbindung mit dem Microsoft-Agent beendet.</span><span class="sxs-lookup"><span data-stu-id="d5aff-122">A client application may receive this event when the user selects another client application's entry in character's pop-up menu or by voice command, the client application changes its active status, or another client application quits its connection to Microsoft Agent.</span></span> <span data-ttu-id="d5aff-123">Der-Agent sendet dieses Ereignis nur an die Client Anwendungen, die direkt betroffen sind. diese Ereignisse werden entweder zum aktiven Client, oder der aktive Client wird beendet.</span><span class="sxs-lookup"><span data-stu-id="d5aff-123">Agent sends this event only to the client applications that are directly affected-those that either become the active client or stop being the active client.</span></span>

<span data-ttu-id="d5aff-124">Mit der Methode " [**aktivieren**](iagentcharacter--activate.md) " können Sie festlegen, ob Ihre Anwendung der aktive Client des Zeichens ist, oder ob Sie die Anwendung als Eingabe-aktiv-Client festlegen möchten (wodurch das Zeichen auch am höchsten ist).</span><span class="sxs-lookup"><span data-stu-id="d5aff-124">You can use the [**Activate**](iagentcharacter--activate.md) method to set whether your application is the active client of the character or to make your application the input-active client (which also makes the character topmost).</span></span>

## <a name="see-also"></a><span data-ttu-id="d5aff-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d5aff-125">See Also</span></span>

<span data-ttu-id="d5aff-126">[**Iagentcharacter:: Aktivierung**](iagentcharacter--activate.md), [**iagentcharakteriex:: getactive**](iagentcharacterex--getactive.md), [**iagentnotifysink:: activateinputstate**](iagentnotifysink--activateinputstate.md)</span><span class="sxs-lookup"><span data-stu-id="d5aff-126">[**IAgentCharacter::Activate**](iagentcharacter--activate.md), [**IAgentCharacterEx::GetActive**](iagentcharacterex--getactive.md), [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md)</span></span>


 

 





