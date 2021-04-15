---
title: Iagentuserinput getallitemdata
description: Iagentuserinput getallitemdata
ms.assetid: d1857b28-c745-4ed2-b49e-774f247e7348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced6a618d4fbbc093bf54c19fc393b7e195f2069
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470741"
---
# <a name="iagentuserinputgetallitemdata"></a><span data-ttu-id="9bb0f-103">Iagentuserinput:: getallitemdata</span><span class="sxs-lookup"><span data-stu-id="9bb0f-103">IAgentUserInput::GetAllItemData</span></span>

<span data-ttu-id="9bb0f-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="9bb0f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetAllItemData(
   VARIANT * pdwItemIndices,  // address of variable for alternative IDs
   VARIANT * plConfidences,   // address of variable for confidence scores
   VARIANT * pbszText         // address of variable for voice text
);
```

<span data-ttu-id="9bb0f-105">Ruft die Daten für alle [**Befehls**](command-event.md) Alternativen ab, die an einen [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="9bb0f-105">Retrieves the data for all [**Command**](command-event.md) alternatives passed to an [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="9bb0f-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="9bb0f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="9bb0f-107"><span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*pdwitemindices*</span><span class="sxs-lookup"><span data-stu-id="9bb0f-107"><span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*pdwItemIndices*</span></span>
</dt> <dd>

<span data-ttu-id="9bb0f-108">Adresse einer Variablen, die die IDs der [**Befehle**](command-event.md) empfängt, die an den [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="9bb0f-108">Address of a variable that receives the IDs of [**Commands**](command-event.md) passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="9bb0f-109"><span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*plconfidential*</span><span class="sxs-lookup"><span data-stu-id="9bb0f-109"><span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*plConfidences*</span></span>
</dt> <dd>

<span data-ttu-id="9bb0f-110">Adresse einer Variablen, die die Vertrauens Ergebnisse für [**Befehls**](command-event.md) Alternativen empfängt, die an den [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="9bb0f-110">Address of a variable that receives the confidence scores for [**Command**](command-event.md) alternatives passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="9bb0f-111"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbsztext*</span><span class="sxs-lookup"><span data-stu-id="9bb0f-111"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*</span></span>
</dt> <dd>

<span data-ttu-id="9bb0f-112">Adresse einer Variablen, die den sprach Text für [**Befehls**](command-event.md) Alternativen empfängt, die an den [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="9bb0f-112">Address of a variable that receives the voice text for [**Command**](command-event.md) alternatives passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> </dl>

<span data-ttu-id="9bb0f-113">Wenn die Spracheingabe [**iagentnotifysink:: Command**](iagentnotifysink--command.md)auslöst, gibt der Server die beste Entsprechung zurück, die zweitbeste Entsprechung und die beste Entsprechung, wenn diese von der Sprach-Engine bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9bb0f-113">If speech input triggers [**IAgentNotifySink::Command**](iagentnotifysink--command.md), the server returns the best match, the second-best match, and the third-best match, if these are provided by the speech engine.</span></span> <span data-ttu-id="9bb0f-114">Sie stellt die relativen Vertrauens Ergebnisse im Bereich von-100 bis 100 und den tatsächlichen Text "Heard" der Sprach-Engine bereit.</span><span class="sxs-lookup"><span data-stu-id="9bb0f-114">It provides the relative confidence scores, in the range of -100 to 100, and actual text "heard" by the speech engine.</span></span> <span data-ttu-id="9bb0f-115">Wenn die beste Entsprechung ein vom Server bereitgestellter Befehl war, sendet der Server eine NULL-ID, sendet jedoch dennoch eine Vertrauenswürdigkeit und den [**Stimm**](voice-property.md) Text.</span><span class="sxs-lookup"><span data-stu-id="9bb0f-115">If the best match was a server-supplied command, the server sends a NULL ID, but still sends a confidence score and the [**Voice**](voice-property.md) text.</span></span>

<span data-ttu-id="9bb0f-116">, Wenn die Spracheingabe nicht die Quelle für das Ereignis war. Wenn der Benutzer z. b. den Befehl aus dem Popupmenü des Zeichens ausgewählt hat, gibt der Microsoft-Agent-Server die ID des ausgewählten [**Befehls**](command-event.md) mit einem Vertrauens Ergebnis von 100 und einem sprach Text als NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="9bb0f-116">If speech input was not the source for the event; for example, if the user selected the command from the character's pop-up menu, the Microsoft Agent server returns the ID of the [**Command**](command-event.md) selected, with a confidence score of 100 and voice text as NULL.</span></span> <span data-ttu-id="9bb0f-117">Die anderen Alternativen geben als NULL zurück, wenn die Vertrauenswürdigkeit NULL (0) und der sprach Text NULL ist.</span><span class="sxs-lookup"><span data-stu-id="9bb0f-117">The other alternatives return as NULL with confidence scores of zero (0) and voice text as NULL.</span></span>

> [!Note]  
> <span data-ttu-id="9bb0f-118">Nicht alle Spracherkennungs-Engines geben möglicherweise alle Werte für alle Parameter dieses Ereignisses zurück.</span><span class="sxs-lookup"><span data-stu-id="9bb0f-118">Not all speech recognition engines may return all the values for all the parameters of this event.</span></span> <span data-ttu-id="9bb0f-119">Wenden Sie sich an den Hersteller Ihrer Hersteller, um zu ermitteln, ob die Engine die Microsoft Speech API-Schnittstelle für das Zurückgeben von Alternativen und Vertrauens Bewertungen</span><span class="sxs-lookup"><span data-stu-id="9bb0f-119">Check with your engine vendor to determine whether the engine supports the Microsoft Speech API interface for returning alternatives and confidence scores.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="9bb0f-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9bb0f-120">See Also</span></span>

<span data-ttu-id="9bb0f-121">[**Iagentuserinput:: getitemconfidence**](iagentuserinput--getitemconfidence.md), [**iagentuserinput:: GetItemText**](iagentuserinput--getitemtext.md), [**iagentuserinput:: getItemID**](iagentuserinput--getitemid.md)</span><span class="sxs-lookup"><span data-stu-id="9bb0f-121">[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md)</span></span>


 

 




