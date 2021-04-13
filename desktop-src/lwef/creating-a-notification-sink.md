---
title: Erstellen einer Benachrichtigungs Senke
description: Erstellen einer Benachrichtigungs Senke
ms.assetid: 6a3cc771-1fef-4b79-baa1-c8d050e36d92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 481cdd754e545ef87e3c0dc44324d46e48baf044
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388722"
---
# <a name="creating-a-notification-sink"></a><span data-ttu-id="9c2de-103">Erstellen einer Benachrichtigungs Senke</span><span class="sxs-lookup"><span data-stu-id="9c2de-103">Creating a Notification Sink</span></span>

<span data-ttu-id="9c2de-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="9c2de-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="9c2de-105">Um über Ereignisse vom Microsoft-Agent benachrichtigt zu werden, müssen Sie entweder die [**iagentnotifysink**](events.md)-oder die [**iagentnotifysinkex**](iagentnotifysinkex.md) -Schnittstelle implementieren und ein Objekt dieses Typs nach com-Konventionen erstellen und registrieren:</span><span class="sxs-lookup"><span data-stu-id="9c2de-105">To be notified of events by Microsoft Agent, you must implement either the [**IAgentNotifySink**](events.md)or the [**IAgentNotifySinkEx**](iagentnotifysinkex.md) interface, and create and register an object of that type following COM conventions:</span></span>


```
// Create a notification sink

pSinkEx = new AgentNotifySinkEx;

pSinkEx->AddRef();

// And register it with Microsoft Agent

hRes = pAgentEx->Register((IUnknown *)pSinkEx, &lNotifySinkID);
```



<span data-ttu-id="9c2de-106">Denken Sie daran, die Registrierung Ihrer Benachrichtigungs Senke aufzuheben, wenn Ihre Anwendung heruntergefahren wird und die Schnittstellen des Microsoft-Agents veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="9c2de-106">Remember to unregister your notification sink when your application shuts down and releases Microsoft Agent's interfaces.</span></span>

 

 




