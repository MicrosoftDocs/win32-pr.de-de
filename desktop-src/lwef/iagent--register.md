---
title: Iagent-Register
description: Iagent-Register
ms.assetid: 3592e8ba-979e-4914-8197-17e645806f97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9dd611219fa994f4fe61f7f3e08facf02c9fb73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856240"
---
# <a name="iagentregister"></a><span data-ttu-id="5881c-103">Iagent:: Register</span><span class="sxs-lookup"><span data-stu-id="5881c-103">IAgent::Register</span></span>

<span data-ttu-id="5881c-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="5881c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Register(
   IUnknown * punkNotifySink  // IUnknown address for client notification sink
   long * pdwSinkID           // address of the notification sink ID
);
```

<span data-ttu-id="5881c-105">Registriert eine Benachrichtigungs Senke für die Client Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5881c-105">Registers a notification sink for the client application.</span></span>

-   <span data-ttu-id="5881c-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="5881c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5881c-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span><span class="sxs-lookup"><span data-stu-id="5881c-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span></span>
</dt> <dd>

<span data-ttu-id="5881c-108">Adresse von [**IUnknown**](https://www.bing.com/search?q=**IUnknown**) für Ihre Notification Sink-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5881c-108">Address of [**IUnknown**](https://www.bing.com/search?q=**IUnknown**) for your notification sink interface.</span></span>

</dd> <dt>

<span data-ttu-id="5881c-109"><span id="pdwSinkID"></span><span id="pdwsinkid"></span><span id="PDWSINKID"></span>*pdwsink ID*</span><span class="sxs-lookup"><span data-stu-id="5881c-109"><span id="pdwSinkID"></span><span id="pdwsinkid"></span><span id="PDWSINKID"></span>*pdwSinkID*</span></span>
</dt> <dd>

<span data-ttu-id="5881c-110">Adresse der Benachrichtigungs-Senke-ID (zur Aufhebung der Registrierung der Benachrichtigungs Senke).</span><span class="sxs-lookup"><span data-stu-id="5881c-110">Address of notification sink ID (used to unregister the notification sink).</span></span>

</dd> </dl>

<span data-ttu-id="5881c-111">Sie müssen ihre Benachrichtigungs Senke (auch als Benachrichtigungs Senke oder Ereignis Senke bezeichnet) registrieren, um Ereignisse vom Microsoft-Agent-Server zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="5881c-111">You need to register your notification sink (also known as a notify sink or event sink) to receive events from the Microsoft Agent server.</span></span>

## <a name="see-also"></a><span data-ttu-id="5881c-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5881c-112">See Also</span></span>

[<span data-ttu-id="5881c-113">**Iagent:: Unregister**</span><span class="sxs-lookup"><span data-stu-id="5881c-113">**IAgent::Unregister**</span></span>](iagent--unregister.md)


 

 




