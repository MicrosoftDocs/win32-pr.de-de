---
title: Iagentuserinput getItemID
description: Iagentuserinput getItemID
ms.assetid: 3afd4d9d-51bb-4086-bf7b-7c9a2ddcd807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716ae1386d87fa6051111801c5603837519eeb4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342234"
---
# <a name="iagentuserinputgetitemid"></a><span data-ttu-id="4353a-103">Iagentuserinput:: getItemID</span><span class="sxs-lookup"><span data-stu-id="4353a-103">IAgentUserInput::GetItemID</span></span>

<span data-ttu-id="4353a-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="4353a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetItemID(
   long dwItemIndex,    // index of Command alternative
   long * pdwCommandID  // address of a variable for number of alternatives 
);
```

<span data-ttu-id="4353a-105">Ruft den Bezeichner einer [**Befehls**](command-event.md) Alternative ab, die an einen [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="4353a-105">Retrieves the identifier of a [**Command**](command-event.md) alternative passed to an [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="4353a-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="4353a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4353a-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwitemindex*</span><span class="sxs-lookup"><span data-stu-id="4353a-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span></span>
</dt> <dd>

<span data-ttu-id="4353a-108">Der Index der [**Befehls**](command-event.md) Alternative, die an den [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="4353a-108">The index of the [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="4353a-109"><span id="pdwCommandID"></span><span id="pdwcommandid"></span><span id="PDWCOMMANDID"></span>*pdwcommandid*</span><span class="sxs-lookup"><span data-stu-id="4353a-109"><span id="pdwCommandID"></span><span id="pdwcommandid"></span><span id="PDWCOMMANDID"></span>*pdwCommandID*</span></span>
</dt> <dd>

<span data-ttu-id="4353a-110">Adresse einer Variablen, die die ID eines [**Befehls**](command-event.md)empfängt.</span><span class="sxs-lookup"><span data-stu-id="4353a-110">Address of a variable that receives the ID of a [**Command**](command-event.md).</span></span>

</dd> </dl>

<span data-ttu-id="4353a-111">Wenn die Spracheingabe den [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf auslöst, gibt der Server die IDs für alle übereinstimmenden [**Befehle**](command-event.md) zurück, die von der Anwendung definiert werden.</span><span class="sxs-lookup"><span data-stu-id="4353a-111">If voice input triggers the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback, the server returns the IDs for any matching [**Commands**](command-event.md) defined by your application.</span></span>

## <a name="see-also"></a><span data-ttu-id="4353a-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4353a-112">See Also</span></span>

<span data-ttu-id="4353a-113">[**Iagentuserinput:: getitemconfidence**](iagentuserinput--getitemconfidence.md), [**iagentuserinput:: GetItemText**](iagentuserinput--getitemtext.md), [**iagentuserinput:: getallitemdata**](iagentuserinput--getallitemdata.md)</span><span class="sxs-lookup"><span data-stu-id="4353a-113">[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput::GetAllItemData**](iagentuserinput--getallitemdata.md)</span></span>


 

 




