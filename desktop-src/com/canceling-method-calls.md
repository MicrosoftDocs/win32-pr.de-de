---
title: Abbrechen von Methoden aufrufen
description: Mit der Einführung verteilter und webbasierter Anwendungen können einige Methodenaufrufe für die Rückgabe sehr viel Zeit in Anspruch nehmen.
ms.assetid: 18228ff1-8c1c-430a-ae5f-0e9a56b0fe3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a78f042e528036135df4865e8a454cd687da
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106337263"
---
# <a name="canceling-method-calls"></a><span data-ttu-id="24eb3-103">Abbrechen von Methoden aufrufen</span><span class="sxs-lookup"><span data-stu-id="24eb3-103">Canceling Method Calls</span></span>

<span data-ttu-id="24eb3-104">Mit der Einführung verteilter und webbasierter Anwendungen können einige Methodenaufrufe für die Rückgabe sehr viel Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="24eb3-104">With the introduction of distributed and Web-based applications, some method calls can take an unacceptably long time to return.</span></span> <span data-ttu-id="24eb3-105">Die Latenz der Netzwerkverbindung kann hoch sein, der Server Computer kann viele Clients betreuen, oder die Serverkomponente übergibt möglicherweise eine große Datenmenge, z. b. eine Multimedia-Datei.</span><span class="sxs-lookup"><span data-stu-id="24eb3-105">The latency of the network connection may be high, the server machine may be serving many clients, or the server component may be passing a large amount of data, such as a multimedia file.</span></span> <span data-ttu-id="24eb3-106">Benutzer sollten in der Lage sein, eine Anforderung abzubrechen, die zu lange dauert, und die Anwendung sollte in der Lage sein, Abbruch Anforderungen zu verarbeiten und mit der anderen Arbeit fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="24eb3-106">Users should be able to cancel a request that is taking too long, and the application should be able to handle cancellation requests and continue with its other work.</span></span> <span data-ttu-id="24eb3-107">In com können Sie die [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) -Schnittstelle verwenden, um einen ausstehenden Anruf abzubrechen, der aus einem Single Thread-Apartment stammt.</span><span class="sxs-lookup"><span data-stu-id="24eb3-107">In COM, you can use the [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) interface to cancel a pending call that originates from a single-threaded apartment.</span></span>

<span data-ttu-id="24eb3-108">Wenn ein Aufruf gemarshallt wird, erstellt der Proxy ein Cancel-Objekt, das die [**icancelmethodcalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="24eb3-108">When a call is marshaled, the proxy creates a cancel object, which implements the [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) interface.</span></span> <span data-ttu-id="24eb3-109">Das Cancel-Objekt ist sowohl dem-Rückruf als auch dem Thread zugeordnet, für den der-Vorgang aussteht.</span><span class="sxs-lookup"><span data-stu-id="24eb3-109">The cancel object is associated with both the call and the thread on which the call is pending.</span></span>

<span data-ttu-id="24eb3-110">Um den ausstehenden-Befehl abzubrechen, übergibt der Client eine Abbruch Anforderung über das Cancel-Objekt, das die Details der Benachrichtigung des Server Objekts behandelt, dass der Rückruf abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="24eb3-110">To cancel the pending call, the client passes a cancellation request through the cancel object, which handles the details of notifying the server object that the call has been canceled.</span></span> <span data-ttu-id="24eb3-111">Wenn die aufgerufene Methode nicht zurückgegeben hat, bereinigt das Server Objekt beim Erkennen der Abbruch Anforderung alle Programmressourcen, die Sie zugeordnet hat, und benachrichtigt den Client, indem er einen entsprechenden **HRESULT** -Wert zurückgibt, der die Ausführung des Aufrufs abgebrochen hat.</span><span class="sxs-lookup"><span data-stu-id="24eb3-111">If the called method has not returned, the server object, on detecting the cancellation request, cleans up any program resources it has allocated and notifies its client, by returning an appropriate **HRESULT** value, that it canceled execution of the call.</span></span> <span data-ttu-id="24eb3-112">Wenn die aufgerufene Methode bereits zurückgegeben wurde, benachrichtigt das Cancel-Objekt den Client.</span><span class="sxs-lookup"><span data-stu-id="24eb3-112">If the called method has already returned, the cancel object notifies the client.</span></span> <span data-ttu-id="24eb3-113">In beiden Fällen wird die Blockierung des Client Threads aufgehoben, und die Verarbeitung kann fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="24eb3-113">In either case, the client thread is unblocked and can continue processing.</span></span>

<span data-ttu-id="24eb3-114">Wie das Server Objekt auf eine Abbruch Anforderung antwortet, liegt im Ermessen des Implementierers des Servers, aber der aufrufende Thread auf dem Client wird immer die Blockierung aufgehoben und ignoriert alle Ergebnisse, die vom Server an ihn übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="24eb3-114">How the server object responds to a cancellation request is at the discretion of the server implementer, but the calling thread on the client will always be unblocked and will ignore whatever results the server tries to pass to it.</span></span> <span data-ttu-id="24eb3-115">Mithilfe von Cancel-Objekten können Sie anfordern, dass eine derzeit laufende Methode abgebrochen wird, aber es gibt keine Garantie dafür, dass das Server Objekt die Verarbeitung des Aufrufes beendet.</span><span class="sxs-lookup"><span data-stu-id="24eb3-115">Cancel objects provide a means to request that a currently running method be canceled, but there is no guarantee that the server object will stop processing the call.</span></span> <span data-ttu-id="24eb3-116">Beispielsweise kann der-Rückruf bereits zurückgegeben worden sein, oder das Server Objekt unterstützt keine Cancel-Objekte.</span><span class="sxs-lookup"><span data-stu-id="24eb3-116">For example, the call may have already returned, or the server object may not support cancel objects.</span></span>

<span data-ttu-id="24eb3-117">COM stellt automatisch eine Standard Implementierung von Cancel-Objekten für Client Objekte und Schnittstellen bereit, die Standardmäßiges Marshalling verwenden.</span><span class="sxs-lookup"><span data-stu-id="24eb3-117">COM automatically provides a standard implementation of cancel objects for client objects and interfaces that use standard marshaling.</span></span> <span data-ttu-id="24eb3-118">Für Objekte und Schnittstellen, die benutzerdefiniertes Marshalling verwenden, müssen Sie ein eigenes Cancel-Objekt implementieren.</span><span class="sxs-lookup"><span data-stu-id="24eb3-118">For objects and interfaces that use custom marshaling, you will need to implement your own cancel object.</span></span>

<span data-ttu-id="24eb3-119">Zu diesem Zeitpunkt werden bei Cancel-Objekten nur synchrone Aufrufe behandelt.</span><span class="sxs-lookup"><span data-stu-id="24eb3-119">At this time, cancel objects handle only synchronous calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24eb3-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="24eb3-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24eb3-121">Abbrechen eines asynchronen Aufrufes</span><span class="sxs-lookup"><span data-stu-id="24eb3-121">Canceling an Asynchronous Call</span></span>](canceling-an-asynchronous-call.md)
</dt> <dt>

[<span data-ttu-id="24eb3-122">**Cogetcancelobject**</span><span class="sxs-lookup"><span data-stu-id="24eb3-122">**CoGetCancelObject**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcancelobject)
</dt> <dt>

[<span data-ttu-id="24eb3-123">**Cosetcancelobject**</span><span class="sxs-lookup"><span data-stu-id="24eb3-123">**CoSetCancelObject**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cosetcancelobject)
</dt> <dt>

[<span data-ttu-id="24eb3-124">**Cotestcancel**</span><span class="sxs-lookup"><span data-stu-id="24eb3-124">**CoTestCancel**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotestcancel)
</dt> </dl>

 

 