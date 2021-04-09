---
title: Konfigurieren der Anforderungs Warteschlange
description: Konfigurieren der Anforderungs Warteschlange
ms.assetid: ab03089c-2ef1-457d-a5f5-a4d400f3a7f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ed397ffbcb42d887d519bc4492bd167dd98c57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856128"
---
# <a name="configuring-the-request-queue"></a><span data-ttu-id="e9ada-103">Konfigurieren der Anforderungs Warteschlange</span><span class="sxs-lookup"><span data-stu-id="e9ada-103">Configuring the Request Queue</span></span>

<span data-ttu-id="e9ada-104">Wenn die Anforderungs Warteschlange geöffnet oder erstellt wird, empfängt die aufrufende Anwendung ein Handle, das zum Senden von Anforderungen oder Konfigurieren der Anforderungs Warteschlange verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e9ada-104">When the request queue is opened or created, the calling application receives a handle to it that can be used to send requests or configure the request queue.</span></span> <span data-ttu-id="e9ada-105">Wenn Sie [**httpseturlgroupproperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) mit **httpserverbindingproperty** aufrufen und das Anforderungs Warteschlangen Handle in der [**http- \_ Bindungs \_**](/windows/desktop/api/Http/ns-http-http_binding_info) Informationsstruktur bereitstellen, die im *ppropertyinformation* -Parameter angegeben ist, ordnet die URL-Gruppe der Anforderungs Warteschlange zu.</span><span class="sxs-lookup"><span data-stu-id="e9ada-105">Calling [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) with **HttpServerBindingProperty** and supplying the request queue handle in the [**HTTP\_BINDING\_INFO**](/windows/desktop/api/Http/ns-http-http_binding_info) structure, specified in the *pPropertyInformation* parameter, associates the URL group with the request queue.</span></span> <span data-ttu-id="e9ada-106">Eigenschaften der Anforderungs Warteschlange werden nur von der Anwendung festgelegt, die die Anforderungs Warteschlange erstellt.</span><span class="sxs-lookup"><span data-stu-id="e9ada-106">Request queue properties are set only by the application that creates the request queue.</span></span> <span data-ttu-id="e9ada-107">Wenn Sie z. b. die Eigenschaft Server-Warteschlangen Länge festlegen möchten, ruft die Ersteller-Anwendung [**httpsetrequestqueueproperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) auf, wobei **httpserverqueuelengthproperty** im *Property* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e9ada-107">For example, to set the server queue length property, the creator application calls [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) specifying **HttpServerQueueLengthProperty** in the *Property* parameter.</span></span>

 

 




