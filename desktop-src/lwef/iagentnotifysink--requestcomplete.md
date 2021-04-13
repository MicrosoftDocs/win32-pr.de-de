---
title: Iagentnotifysink requestcomplete
description: Iagentnotifysink requestcomplete
ms.assetid: 995bc961-f175-4429-94a4-91962161298b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0265a7111369dec687fd74b9c66c27275a40e164
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311040"
---
# <a name="iagentnotifysinkrequestcomplete"></a><span data-ttu-id="b613e-103">Iagentnotifysink:: requestcomplete</span><span class="sxs-lookup"><span data-stu-id="b613e-103">IAgentNotifySink::RequestComplete</span></span>

<span data-ttu-id="b613e-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="b613e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT RequestComplete(
   long dwRequestID,  // request ID
   long hrStatus      // status code
);                          
```

<span data-ttu-id="b613e-105">Benachrichtigt eine Client Anwendung, wenn eine Anforderung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="b613e-105">Notifies a client application when a request completes.</span></span>

-   <span data-ttu-id="b613e-106">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="b613e-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="b613e-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwrequestid*</span><span class="sxs-lookup"><span data-stu-id="b613e-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*</span></span>
</dt> <dd>

<span data-ttu-id="b613e-108">Der Bezeichner der Anforderung, die gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="b613e-108">Identifier of the request that started.</span></span>

</dd> <dt>

<span data-ttu-id="b613e-109"><span id="hrStatus"></span><span id="hrstatus"></span><span id="HRSTATUS"></span>*hrStatus*</span><span class="sxs-lookup"><span data-stu-id="b613e-109"><span id="hrStatus"></span><span id="hrstatus"></span><span id="HRSTATUS"></span>*hrStatus*</span></span>
</dt> <dd>

<span data-ttu-id="b613e-110">Statuscode.</span><span class="sxs-lookup"><span data-stu-id="b613e-110">Status code.</span></span> <span data-ttu-id="b613e-111">Dieser Parameter gibt den Statuscode für die Anforderung zurück.</span><span class="sxs-lookup"><span data-stu-id="b613e-111">This parameter returns the status code for the request.</span></span>

</dd> </dl>

<span data-ttu-id="b613e-112">Mithilfe dieses Ereignisses können Sie nachverfolgen, wann eine in der Warteschlange stehende Methode mithilfe ihrer Anforderungs-ID abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="b613e-112">This event enables you to track when a queued method completes using its request ID.</span></span>

## <a name="see-also"></a><span data-ttu-id="b613e-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b613e-113">See Also</span></span>

<span data-ttu-id="b613e-114">[**Iagentnotifysink:: requeststart**](iagentnotifysink--requeststart.md), [**iagent:: Load**](iagent--load.md), [**iagentcharacter:: gestureat**](iagentcharacter--gestureat.md), [**iagentcharacter:: Hide**](iagentcharacter--hide.md), [**iagentcharacter:: Interrupt**](iagentcharacter--interrupt.md), [**iagentcharacter:: muveto**](iagentcharacter--moveto.md), [**iagentcharacter::P repare**](iagentcharacter--prepare.md), [**iagentcharacter::P Lay**](iagentcharacter--play.md), [**iagentcharacter:: Show**](iagentcharacter--show.md), [**iagentcharacter:: Speak**](iagentcharacter--speak.md), [**iagentcharacter:: Wait**](iagentcharacter--wait.md)</span><span class="sxs-lookup"><span data-stu-id="b613e-114">[**IAgentNotifySink::RequestStart**](iagentnotifysink--requeststart.md), [**IAgent::Load**](iagent--load.md), [**IAgentCharacter::GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter::Hide**](iagentcharacter--hide.md), [**IAgentCharacter::Interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter::MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter::Prepare**](iagentcharacter--prepare.md), [**IAgentCharacter::Play**](iagentcharacter--play.md), [**IAgentCharacter::Show**](iagentcharacter--show.md), [**IAgentCharacter::Speak**](iagentcharacter--speak.md), [**IAgentCharacter::Wait**](iagentcharacter--wait.md)</span></span>


 

 




