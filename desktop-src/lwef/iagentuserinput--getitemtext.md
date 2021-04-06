---
title: Iagentuserinput GetItemText
description: Iagentuserinput GetItemText
ms.assetid: 69653806-c001-4015-bd05-3c261a312ede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7010172147f86282903641c46aa5137ce69c80be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036224"
---
# <a name="iagentuserinputgetitemtext"></a><span data-ttu-id="bbe3e-103">Iagentuserinput:: GetItemText</span><span class="sxs-lookup"><span data-stu-id="bbe3e-103">IAgentUserInput::GetItemText</span></span>

<span data-ttu-id="bbe3e-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="bbe3e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetItemText(
   Long dwItemIndex,  // index of Command alternative
   BSTR * pbszText    // address of voice text for Command 
);
```

<span data-ttu-id="bbe3e-105">Ruft den sprach Text für eine [**Befehls**](command-event.md) Alternative ab, die an den [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="bbe3e-105">Retrieves the voice text for a [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="bbe3e-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="bbe3e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="bbe3e-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwitemindex*</span><span class="sxs-lookup"><span data-stu-id="bbe3e-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span></span>
</dt> <dd>

<span data-ttu-id="bbe3e-108">Der Index einer [**Befehls**](command-event.md) Alternative, die an den [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="bbe3e-108">The index of a [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="bbe3e-109"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbsztext*</span><span class="sxs-lookup"><span data-stu-id="bbe3e-109"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*</span></span>
</dt> <dd>

<span data-ttu-id="bbe3e-110">Die Adresse eines BSTR-Werts, der den Wert des sprach Texts für den [**Befehl**](command-event.md)empfängt.</span><span class="sxs-lookup"><span data-stu-id="bbe3e-110">Address of a BSTR that receives the value of the voice text for the [**Command**](command-event.md).</span></span>

</dd> </dl>

<span data-ttu-id="bbe3e-111">Wenn die Spracheingabe nicht die Quelle für den Befehl war, z. b. wenn der Benutzer den Befehl aus dem Popupmenü des Zeichens ausgewählt hat, gibt der Server für den sprach Text des [**Befehls**](command-event.md) **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="bbe3e-111">If voice input was not the source for the command, for example, if the user selected the command from the character's pop-up menu, the server returns **NULL** for the [**Command**](command-event.md)'s voice text.</span></span>

## <a name="see-also"></a><span data-ttu-id="bbe3e-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bbe3e-112">See Also</span></span>

<span data-ttu-id="bbe3e-113">[**Iagentuserinput:: getitemconfidence**](iagentuserinput--getitemconfidence.md), [**iagentuserinput:: getItemID**](iagentuserinput--getitemid.md), [**iagentuserinput:: getallitemdata**](iagentuserinput--getallitemdata.md)</span><span class="sxs-lookup"><span data-stu-id="bbe3e-113">[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput::GetAllItemData**](iagentuserinput--getallitemdata.md)</span></span>


 

 




