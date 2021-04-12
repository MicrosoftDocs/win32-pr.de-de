---
title: Iagentuserinput getitemconfidence
description: Iagentuserinput getitemconfidence
ms.assetid: 7d1ca2f0-416c-43c3-99a8-9f287cb88de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 846e1fca9ea1245a62fc68330d68263b63fb7cfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309140"
---
# <a name="iagentuserinputgetitemconfidence"></a><span data-ttu-id="eb5b4-103">Iagentuserinput:: getitemconfidence</span><span class="sxs-lookup"><span data-stu-id="eb5b4-103">IAgentUserInput::GetItemConfidence</span></span>

<span data-ttu-id="eb5b4-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="eb5b4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetItemConfidence(
   long dwItemIndex,    // index of Command alternative
   long * plConfidence  // address of confidence value for Command 
);
```

<span data-ttu-id="eb5b4-105">Ruft den Vertrauens Wert für einen [**Befehl**](command-event.md) ab, der an einen [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="eb5b4-105">Retrieves the confidence value for a [**Command**](command-event.md) passed to an [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="eb5b4-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="eb5b4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="eb5b4-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwitemindex*</span><span class="sxs-lookup"><span data-stu-id="eb5b4-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span></span>
</dt> <dd>

<span data-ttu-id="eb5b4-108">Der Index einer [**Befehls**](command-event.md) Alternative, die an den [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="eb5b4-108">The index of a [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="eb5b4-109"><span id="plConfidence"></span><span id="plconfidence"></span><span id="PLCONFIDENCE"></span>*plconfidence*</span><span class="sxs-lookup"><span data-stu-id="eb5b4-109"><span id="plConfidence"></span><span id="plconfidence"></span><span id="PLCONFIDENCE"></span>*plConfidence*</span></span>
</dt> <dd>

<span data-ttu-id="eb5b4-110">Adresse einer Variablen, die das Vertrauens Ergebnis für eine [**Befehls**](command-event.md) Alternative empfängt, die an den [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="eb5b4-110">Address of a variable that receives the confidence score for a [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> </dl>

<span data-ttu-id="eb5b4-111">Wenn die Spracheingabe nicht die Quelle für den Befehl war, z. b. wenn der Benutzer den Befehl aus dem Popupmenü des Zeichens ausgewählt hat, gibt der Microsoft-Agent-Server den Vertrauens Wert der besten Entsprechung als 100 und die Vertrauens Werte für alle anderen Alternativen als NULL (0) zurück.</span><span class="sxs-lookup"><span data-stu-id="eb5b4-111">If voice input was not the source for the command, for example, if the user selected the command from the character's pop-up menu, the Microsoft Agent server returns the confidence value of the best match as 100 and the confidence values for all other alternatives as zero (0).</span></span>

## <a name="see-also"></a><span data-ttu-id="eb5b4-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="eb5b4-112">See Also</span></span>

<span data-ttu-id="eb5b4-113">[**Iagentuserinput:: getItemID**](iagentuserinput--getitemid.md), [**iagentuserinput:: getallitemdata**](iagentuserinput--getallitemdata.md), [**iagentuserinput:: GetItemText**](iagentuserinput--getitemtext.md)</span><span class="sxs-lookup"><span data-stu-id="eb5b4-113">[**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput::GetAllItemData**](iagentuserinput--getallitemdata.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md)</span></span>


 

 




