---
title: Iagentnotifysink requeststart
description: Iagentnotifysink requeststart
ms.assetid: acac2bf8-7472-4952-a984-a29654fb8b0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ced12596114214cf712cef8dbbe81edb5af278
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713620"
---
# <a name="iagentnotifysinkrequeststart"></a><span data-ttu-id="8e6db-103">Iagentnotifysink:: requeststart</span><span class="sxs-lookup"><span data-stu-id="8e6db-103">IAgentNotifySink::RequestStart</span></span>

<span data-ttu-id="8e6db-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="8e6db-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT RequestStart(
   long dwRequestID  // request ID
);                          
```

<span data-ttu-id="8e6db-105">Benachrichtigt eine Client Anwendung, wenn eine Anforderung beginnt.</span><span class="sxs-lookup"><span data-stu-id="8e6db-105">Notifies a client application when a request begins.</span></span>

-   <span data-ttu-id="8e6db-106">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="8e6db-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="8e6db-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwrequestid*</span><span class="sxs-lookup"><span data-stu-id="8e6db-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*</span></span>
</dt> <dd>

<span data-ttu-id="8e6db-108">Der Bezeichner der Anforderung, die gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="8e6db-108">Identifier of the request that started.</span></span>

</dd> </dl>

<span data-ttu-id="8e6db-109">Mithilfe dieses Ereignisses können Sie nachverfolgen, wann eine Anforderung in der Warteschlange mit ihrer Anforderungs-ID beginnt.</span><span class="sxs-lookup"><span data-stu-id="8e6db-109">This event enables you to track when a queued request begins using its request ID.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e6db-110">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8e6db-110">See Also</span></span>

<span data-ttu-id="8e6db-111">[**Iagentnotifysink:: requestcomplete**](iagentnotifysink--requestcomplete.md), [**iagent:: Load**](iagent--load.md), [**iagentcharacter:: gestureat**](iagentcharacter--gestureat.md), [**iagentcharacter:: Hide**](iagentcharacter--hide.md), [**iagentcharacter:: Interrupt**](iagentcharacter--interrupt.md), [**iagentcharacter:: muveto**](iagentcharacter--moveto.md), [**iagentcharacter::P repare**](iagentcharacter--prepare.md), [**iagentcharacter::P Lay**](iagentcharacter--play.md), [**iagentcharacter:: Show**](iagentcharacter--show.md), [**iagentcharacter:: Speak**](iagentcharacter--speak.md), [**iagentcharacter:: Wait**](iagentcharacter--wait.md)</span><span class="sxs-lookup"><span data-stu-id="8e6db-111">[**IAgentNotifySink::RequestComplete**](iagentnotifysink--requestcomplete.md), [**IAgent::Load**](iagent--load.md), [**IAgentCharacter::GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter::Hide**](iagentcharacter--hide.md), [**IAgentCharacter::Interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter::MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter::Prepare**](iagentcharacter--prepare.md), [**IAgentCharacter::Play**](iagentcharacter--play.md), [**IAgentCharacter::Show**](iagentcharacter--show.md), [**IAgentCharacter::Speak**](iagentcharacter--speak.md), [**IAgentCharacter::Wait**](iagentcharacter--wait.md)</span></span>


 

 




