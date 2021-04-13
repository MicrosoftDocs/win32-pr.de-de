---
title: Erstellen und Binden an eine Anforderungs Warteschlange
description: Eine Anforderungs Warteschlange ist eine Dienst Warteschlange, die ausstehende Anforderungen für eine bestimmte Anwendung enthält.
ms.assetid: 93f8b230-af0a-4582-b35b-d65f6841e525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945b8451f9128357b7da0ddc64600b74deffd0d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388552"
---
# <a name="creating-and-binding-to-a-request-queue"></a><span data-ttu-id="fc767-103">Erstellen und Binden an eine Anforderungs Warteschlange</span><span class="sxs-lookup"><span data-stu-id="fc767-103">Creating and Binding to a Request Queue</span></span>

<span data-ttu-id="fc767-104">Eine Anforderungs Warteschlange ist eine Dienst Warteschlange, die ausstehende Anforderungen für eine bestimmte Anwendung enthält.</span><span class="sxs-lookup"><span data-stu-id="fc767-104">A request queue is a service queue that holds pending requests for a specific application.</span></span> <span data-ttu-id="fc767-105">Eine Anwendung erstellt die Anforderungs Warteschlange unabhängig von der URL-Gruppe oder der Server Sitzung durch Aufrufen der Funktion [**httpcreaterequestqueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) und legt die Eigenschaften der Anforderungs Warteschlange durch Aufrufen der Funktion [**httpsetrequestqueueproperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) fest.</span><span class="sxs-lookup"><span data-stu-id="fc767-105">An application creates the request queue independently of the URL group or server session by calling the [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) function, and sets the request queue properties by calling the [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) function.</span></span> <span data-ttu-id="fc767-106">Bei diesen Eigenschaften handelt es sich um die Ausführlichkeit von 503 Antworten, die maximale Länge der Warteschlange und den Aktivitäts Zustand.</span><span class="sxs-lookup"><span data-stu-id="fc767-106">These properties are the verbosity of 503 responses, the maximum length of the queue, and the activity state.</span></span>

<span data-ttu-id="fc767-107">Um zu bewirken, dass Anforderungen an die Anforderungs Warteschlange weitergeleitet werden, bindet die Anwendung die URL-Gruppe, die Sie als Teil der [Laufzeitkonfiguration](run-time-configuration.md) erstellt hat, durch Aufrufen von [**httpseturlgroupproperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) mit **httpserverbindingproperty** in den *Property* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="fc767-107">To cause requests to be routed to its request queue, the application binds the URL group it created as part of [run-time configuration](run-time-configuration.md) to the queue by calling [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) with **HttpServerBindingProperty** specified in the *Property* parameter.</span></span> <span data-ttu-id="fc767-108">Eingehende Anforderungen von den URLs in der Gruppe werden dann an die angegebene Anforderungs Warteschlange weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="fc767-108">Incoming requests from the URLs in the group are then routed to the specified request queue.</span></span>

 

 




