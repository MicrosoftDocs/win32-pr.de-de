---
title: Iagentnotifysinkex helpcomplete
description: Iagentnotifysinkex helpcomplete
ms.assetid: f8285d05-3b96-4046-a058-0e001e47b54b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3b7dbbdf272844242943d49ed86b303d220185
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038862"
---
# <a name="iagentnotifysinkexhelpcomplete"></a><span data-ttu-id="73e4b-103">Iagentnotifysinkex:: helpcomplete</span><span class="sxs-lookup"><span data-stu-id="73e4b-103">IAgentNotifySinkEx::HelpComplete</span></span>

<span data-ttu-id="73e4b-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="73e4b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT HelpComplete(
   long dwCharID,     // character ID
   long dwCommandID,  // command ID
   long dwCause       // cause 
);
```

<span data-ttu-id="73e4b-105">Benachrichtigt eine Client Anwendung, wenn der Benutzer einen Befehl oder ein Zeichen zum Vervollständigen des Hilfe Modus auswählt.</span><span class="sxs-lookup"><span data-stu-id="73e4b-105">Notifies a client application when the user selects a command or character to complete Help mode.</span></span>

-   <span data-ttu-id="73e4b-106">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="73e4b-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="73e4b-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwcharid*</span><span class="sxs-lookup"><span data-stu-id="73e4b-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="73e4b-108">Der Bezeichner des Zeichens, für das der Hilfe Modus abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="73e4b-108">Identifier of the character for which Help mode completed.</span></span>

</dd> <dt>

<span data-ttu-id="73e4b-109"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwcommandid*</span><span class="sxs-lookup"><span data-stu-id="73e4b-109"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span></span>
</dt> <dd>

<span data-ttu-id="73e4b-110">Der Bezeichner des Befehls, den der Benutzer ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="73e4b-110">Identifier of the command the user selected.</span></span>

</dd> <dt>

<span data-ttu-id="73e4b-111"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwcause*</span><span class="sxs-lookup"><span data-stu-id="73e4b-111"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="73e4b-112">Die Ursache für das Ereignis, bei der es sich um die folgenden Werte handeln kann:</span><span class="sxs-lookup"><span data-stu-id="73e4b-112">The cause for the event, which may be the following values:</span></span>



| <span data-ttu-id="73e4b-113">Wert</span><span class="sxs-lookup"><span data-stu-id="73e4b-113">Value</span></span>                                                                         | <span data-ttu-id="73e4b-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="73e4b-114">Description</span></span>                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="73e4b-115">**Ganzzahl ohne Vorzeichen Short** **cshelpcause- \_ Befehl = 1;**</span><span class="sxs-lookup"><span data-stu-id="73e4b-115">**const unsigned short** **CSHELPCAUSE\_COMMAND = 1;**</span></span><br/>             | <span data-ttu-id="73e4b-116">Der Benutzer hat einen von der Anwendung bereitgestellten Befehl ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="73e4b-116">The user selected a command supplied by your application.</span></span>                            |
| <span data-ttu-id="73e4b-117">**Ganzzahl ohne Vorzeichen Short** **cshelpcause \_ otherprogram = 2;**</span><span class="sxs-lookup"><span data-stu-id="73e4b-117">**const unsigned short** **CSHELPCAUSE\_OTHERPROGRAM = 2;**</span></span><br/>        | <span data-ttu-id="73e4b-118">Der Benutzer hat das Objekt " [**Befehle**](/windows/desktop/lwef/the-commands-collection-object) " eines anderen Clients ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="73e4b-118">The user selected the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object of another client.</span></span> |
| <span data-ttu-id="73e4b-119">" **Ganzzahl ohne Vorzeichen Short** **cshelpcause" für " \_ opencommandswindow = 3;** "</span><span class="sxs-lookup"><span data-stu-id="73e4b-119">**const unsigned short** **CSHELPCAUSE\_OPENCOMMANDSWINDOW = 3;**</span></span><br/>  | <span data-ttu-id="73e4b-120">Der Benutzer hat den Befehl "Sprachbefehle öffnen" ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="73e4b-120">The user selected the Open Voice Commands command.</span></span>                                   |
| <span data-ttu-id="73e4b-121">" **Ganzzahl ohne Vorzeichen Short** **cshelpcause" \_ , "closecommandswindow" = 4;**</span><span class="sxs-lookup"><span data-stu-id="73e4b-121">**const unsigned short** **CSHELPCAUSE\_CLOSECOMMANDSWINDOW = 4;**</span></span><br/> | <span data-ttu-id="73e4b-122">Der Benutzer hat den Befehl "Sprachbefehle schließen" ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="73e4b-122">The user selected the Close Voice Commands command.</span></span>                                  |
| <span data-ttu-id="73e4b-123">**unsigniertes kurzes** **cshelpcause- \_ showcharacter = 5;**</span><span class="sxs-lookup"><span data-stu-id="73e4b-123">**const unsigned short** **CSHELPCAUSE\_SHOWCHARACTER = 5;**</span></span><br/>       | <span data-ttu-id="73e4b-124">Der Benutzer hat den Befehl " *Merkmal Name* anzeigen" ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="73e4b-124">The user selected the Show *CharacterName* command.</span></span>                                  |
| <span data-ttu-id="73e4b-125">**Ganzzahl ohne Vorzeichen Short** **cshelpcause- \_ hidecharacter = 6;**</span><span class="sxs-lookup"><span data-stu-id="73e4b-125">**const unsigned short** **CSHELPCAUSE\_HIDECHARACTER = 6;**</span></span><br/>       | <span data-ttu-id="73e4b-126">Der Benutzer hat den Befehl " *Merkmal Name* ausblenden" ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="73e4b-126">The user selected the Hide *CharacterName* command.</span></span>                                  |
| <span data-ttu-id="73e4b-127">**Ganzzahl ohne Vorzeichen Short** **cshelpcause- \_ Zeichen = 7;**</span><span class="sxs-lookup"><span data-stu-id="73e4b-127">**const unsigned short** **CSHELPCAUSE\_CHARACTER = 7;**</span></span><br/>           | <span data-ttu-id="73e4b-128">Der Benutzer hat das Zeichen ausgewählt (geklickt).</span><span class="sxs-lookup"><span data-stu-id="73e4b-128">The user selected (clicked) the character.</span></span>                                           |



 

</dd> </dl>

<span data-ttu-id="73e4b-129">In der Regel wird der Hilfe Modus abgeschlossen, wenn der Benutzer auf das Zeichen klickt oder zieht oder einen Befehl aus dem Popupmenü des Zeichens auswählt.</span><span class="sxs-lookup"><span data-stu-id="73e4b-129">Typically Help mode completes when the user clicks or drags the character or selects a command from the character's pop-up menu.</span></span> <span data-ttu-id="73e4b-130">Durch Klicken auf ein anderes Zeichen oder an anderer Stelle auf dem Bildschirm wird der Hilfe Modus nicht abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="73e4b-130">Clicking on another character or elsewhere on the screen does not cancel Help mode.</span></span> <span data-ttu-id="73e4b-131">Der Client, der den Hilfe Modus für das Zeichen festlegt, kann den Hilfe Modus abbrechen, indem er [**iagentcharacter:: helpmudeon**](https://www.bing.com/search?q=**IAgentCharacter::HelpModeOn**) auf **false** festlegt.</span><span class="sxs-lookup"><span data-stu-id="73e4b-131">The client that set Help mode for the character can cancel Help mode by setting [**IAgentCharacter::HelpModeOn**](https://www.bing.com/search?q=**IAgentCharacter::HelpModeOn**) to **False**.</span></span> <span data-ttu-id="73e4b-132">(Hierdurch wird das Ereignis **iagentnotifysinkex:: helpcomplete** nicht auslöst.)</span><span class="sxs-lookup"><span data-stu-id="73e4b-132">(This does not trigger the **IAgentNotifySinkEx::HelpComplete** event.)</span></span>

<span data-ttu-id="73e4b-133">Wenn der Benutzer im Hilfe Modus aus dem Popupmenü des Zeichens einen Befehl auswählt, entfernt der Server das Menü, ruft die Hilfe mit der angegebenen [**HelpContextID**](helpcontextid-property.md)des Befehls auf und sendet dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="73e4b-133">When the user selects a command from the character's pop-up menu in Help mode, the server removes the menu, calls Help with the command's specified [**HelpContextID**](helpcontextid-property.md), and sends this event.</span></span> <span data-ttu-id="73e4b-134">Die kontextabhängige (auch bekannt als was ist das?) Das Hilfefenster wird an der Zeigerposition angezeigt.</span><span class="sxs-lookup"><span data-stu-id="73e4b-134">The context-sensitive (also known as What's This?) Help window is displayed at the pointer location.</span></span> <span data-ttu-id="73e4b-135">Wenn der Benutzer den Befehl per Spracheingabe auswählt, wird das Hilfefenster für das Zeichen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="73e4b-135">If the user selects the command by voice input, the Help window is displayed over the character.</span></span> <span data-ttu-id="73e4b-136">Wenn das Zeichen außerhalb des Bildschirms ist, wird das Fenster auf dem Bildschirm angezeigt, das der aktuellen Position des Zeichens am nächsten ist.</span><span class="sxs-lookup"><span data-stu-id="73e4b-136">If the character is off-screen, the window is displayed on-screen nearest to the character's current position.</span></span>

<span data-ttu-id="73e4b-137">Wenn der Server *dwcommandid* als leere Zeichenfolge ("") zurückgibt, bedeutet dies, dass der Benutzer einen vom Server bereitgestellten Befehl ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="73e4b-137">If the server returns *dwCommandID* as an empty string (""), it indicates that the user selected a server-supplied command.</span></span>

<span data-ttu-id="73e4b-138">Dieses Ereignis wird nur an die Client Anwendung gesendet, die das Zeichen in den Hilfe Modus versetzt.</span><span class="sxs-lookup"><span data-stu-id="73e4b-138">This event is sent only to the client application that places the character into Help mode.</span></span>

## <a name="see-also"></a><span data-ttu-id="73e4b-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="73e4b-139">See Also</span></span>

<span data-ttu-id="73e4b-140">[**Iagentcharakteriex::**](iagentcharacterex--sethelpmodeon.md)Setup Element-ID, [**iagentcharakteriex:: Setup Element Dateiname**](iagentcharacterex--sethelpfilename.md), [**iagentcharakteriex::**](iagentcharacterex--sethelpcontextid.md)Setup Element-ID, [**iagentcommandsex::**](iagentcommandsex--sethelpcontextid.md) ab.</span><span class="sxs-lookup"><span data-stu-id="73e4b-140">[**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md), [**IAgentCharacterEx::SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)</span></span>


 

