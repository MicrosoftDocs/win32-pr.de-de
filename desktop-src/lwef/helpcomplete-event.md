---
title: Helpcomplete-Ereignis
description: Helpcomplete-Ereignis
ms.assetid: d805f089-154f-4b39-9d78-a02b732f87ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3984f4b67eaed6bc9226685e927c35e151c11e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337220"
---
# <a name="helpcomplete-event"></a><span data-ttu-id="f2d2e-103">Helpcomplete-Ereignis</span><span class="sxs-lookup"><span data-stu-id="f2d2e-103">HelpComplete Event</span></span>

<span data-ttu-id="f2d2e-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="f2d2e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f2d2e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f2d2e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f2d2e-106">Gibt an, dass der kontextbezogene Hilfe Modus beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-106">Indicates that context-sensitive Help mode has been exited.</span></span>

</dd> <dt>

<span data-ttu-id="f2d2e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="f2d2e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f2d2e-108">**Sub** - *Agent. \* \* \* (ByVal*- \*  \*Merkmal-ID \* \* *, ByVal*- \*  \*Name \* \* *, ByVal*- \*  *Ursache \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="f2d2e-108">**Sub** *agent.\*\*\*(ByVal*\* *CharacterID\*\*\*, ByVal*\* *Name\*\*\*, ByVal*\* *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="f2d2e-109">Teil</span><span class="sxs-lookup"><span data-stu-id="f2d2e-109">Part</span></span>          | <span data-ttu-id="f2d2e-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2d2e-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2d2e-111">*Merkmal-ID*</span><span class="sxs-lookup"><span data-stu-id="f2d2e-111">*CharacterID*</span></span> | <span data-ttu-id="f2d2e-112">Gibt die ID des angeklickten Zeichens als Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-112">Returns the ID of the clicked character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="f2d2e-113">*Name*</span><span class="sxs-lookup"><span data-stu-id="f2d2e-113">*Name*</span></span>        | <span data-ttu-id="f2d2e-114">Gibt einen Zeichen folgen Wert zurück, der den Namen (ID) des Befehls identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-114">Returns a string value identifying the name (ID) of the command.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="f2d2e-115">*Ursache*</span><span class="sxs-lookup"><span data-stu-id="f2d2e-115">*Cause*</span></span>       | <span data-ttu-id="f2d2e-116">Gibt einen Wert zurück, der angibt, wodurch der Hilfe Modus beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-116">Returns a value that indicates what caused the Help mode to complete.</span></span> <span data-ttu-id="f2d2e-117">1 der Benutzer hat einen von der Anwendung bereitgestellten Befehl ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-117">1 The user selected a command supplied by your application.</span></span><br/> <span data-ttu-id="f2d2e-118">2 der Benutzer hat das Objekt " [**Befehle**](/windows/desktop/lwef/the-commands-collection-object) " eines anderen Clients ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-118">2 The user selected the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object of another client.</span></span><br/> <span data-ttu-id="f2d2e-119">3 der Benutzer hat den Befehl "Sprachbefehle öffnen" ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-119">3 The user selected the Open Voice Commands command.</span></span><br/> <span data-ttu-id="f2d2e-120">4 der Benutzer hat den Befehl "Sprachbefehle schließen" ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-120">4 The user selected the Close Voice Commands command.</span></span><br/> <span data-ttu-id="f2d2e-121">5 der Benutzer hat den Befehl " *Merkmal Name* anzeigen" ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-121">5 The user selected the Show *CharacterName* command.</span></span><br/> <span data-ttu-id="f2d2e-122">6 der Benutzer hat den Befehl " *Merkmal Name* ausblenden" ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-122">6 The user selected the Hide *CharacterName* command.</span></span><br/> <span data-ttu-id="f2d2e-123">7 der Benutzer hat das Zeichen ausgewählt (geklickt).</span><span class="sxs-lookup"><span data-stu-id="f2d2e-123">7 The user selected (clicked) the character.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="f2d2e-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2d2e-124">Remarks</span></span>

<span data-ttu-id="f2d2e-125">In der Regel wird der Hilfe Modus beendet, wenn der Benutzer auf das Zeichen klickt oder zieht oder einen Befehl aus dem Popupmenü des Zeichens auswählt.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-125">Typically, Help mode completes when the user clicks or drags the character or selects a command from the character's pop-up menu.</span></span> <span data-ttu-id="f2d2e-126">Durch Klicken auf ein anderes Zeichen oder an anderer Stelle auf dem Bildschirm wird der Hilfe Modus nicht abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-126">Clicking on another character or elsewhere on the screen does not cancel Help mode.</span></span> <span data-ttu-id="f2d2e-127">Der Client, der den Hilfe Modus für das Zeichen festlegt, kann den Hilfe Modus abbrechen, indem [**helpmudeon**](helpmodeon-property.md) auf **false** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-127">The client that set Help mode for the character can cancel Help mode by setting [**HelpModeOn**](helpmodeon-property.md) to **False**.</span></span> <span data-ttu-id="f2d2e-128">(Dies löst nicht das **helpcomplete** -Ereignis aus.)</span><span class="sxs-lookup"><span data-stu-id="f2d2e-128">(This does not trigger the **HelpComplete** event.)</span></span>

<span data-ttu-id="f2d2e-129">Wenn der Benutzer im Hilfe Modus aus dem Popupmenü des Zeichens einen Befehl auswählt, entfernt der Server das Menü, ruft die Hilfe mit der angegebenen [**HelpContextID**](helpcontextid-property.md)des Befehls auf und sendet dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-129">When the user selects a command from the character's pop-up menu in Help mode, the server removes the menu, calls Help with the command's specified [**HelpContextID**](helpcontextid-property.md), and sends this event.</span></span> <span data-ttu-id="f2d2e-130">Die kontextabhängige (auch bekannt als was ist das?) Das Hilfefenster wird an der Zeigerposition angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-130">The context-sensitive (also known as What's This?) Help window is displayed at the pointer location.</span></span> <span data-ttu-id="f2d2e-131">Wenn der Benutzer den Befehl per Spracheingabe auswählt, wird das Hilfefenster für das Zeichen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-131">If the user selects the command by voice input, the Help window is displayed over the character.</span></span> <span data-ttu-id="f2d2e-132">Wenn das Zeichen außerhalb des Bildschirms ist, wird das Fenster auf dem Bildschirm angezeigt, das der aktuellen Position des Zeichens am nächsten ist.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-132">If the character is off-screen, the window is displayed on-screen nearest to the character's current position.</span></span>

<span data-ttu-id="f2d2e-133">Wenn der Server den Namen als leere Zeichenfolge ("") zurückgibt, bedeutet dies, dass der Benutzer einen vom Server bereitgestellten Befehl ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-133">If the server returns Name as an empty string (""), it indicates that the user selected a server-supplied command.</span></span>

<span data-ttu-id="f2d2e-134">Dieses Ereignis wird nur an die Client Anwendung gesendet, die das Zeichen im Hilfe Modus platziert.</span><span class="sxs-lookup"><span data-stu-id="f2d2e-134">This event is sent only to the client application that places the character in Help mode.</span></span>

### <a name="see-also"></a><span data-ttu-id="f2d2e-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f2d2e-135">See Also</span></span>

<span data-ttu-id="f2d2e-136">[**Helpmudeon-Eigenschaft**](helpmodeon-property.md), [ **HelpContextID-Eigenschaft**](helpcontextid-property.md)</span><span class="sxs-lookup"><span data-stu-id="f2d2e-136">[**HelpModeOn property**](helpmodeon-property.md), [**HelpContextID property**](helpcontextid-property.md)</span></span>


 

