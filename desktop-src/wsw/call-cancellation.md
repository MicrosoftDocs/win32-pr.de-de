---
title: Abbruch Abbrechen
description: Die Aufruf Abbruch Benachrichtigung bricht den Betrieb der serverseitigen Dienst Vorgänge und Dienstmodell Rückrufe ab.
ms.assetid: dc371921-869f-4775-98d3-80a1006358ba
keywords:
- Aufrufe von Abbruch-Webdiensten für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5107f9ece421a3130f99c78b3b33788ee6c7e9f0
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "106337693"
---
# <a name="call-cancellation"></a><span data-ttu-id="72097-106">Abbruch Abbrechen</span><span class="sxs-lookup"><span data-stu-id="72097-106">Call cancellation</span></span>

<span data-ttu-id="72097-107">Die Aufruf Abbruch Benachrichtigung bricht den Betrieb der [serverseitigen Dienst Vorgänge](server-side-service-operations.md) und Dienstmodell Rückrufe ab.</span><span class="sxs-lookup"><span data-stu-id="72097-107">Call cancellation notification cancels the operation of [server side service operations](server-side-service-operations.md) and service-model callbacks.</span></span> <span data-ttu-id="72097-108">Ein solcher Abbruch kann aus zwei Gründen erfolgen:</span><span class="sxs-lookup"><span data-stu-id="72097-108">Such cancellation can be for one of two reasons:</span></span>

-   <span data-ttu-id="72097-109">Der Dienst Host hat Vorgänge aufgrund eines Aufrufes der [**wsabortservicehost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost) -Funktion beendet.</span><span class="sxs-lookup"><span data-stu-id="72097-109">The service host has stopped operations because of a call to the [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost) function.</span></span>
-   <span data-ttu-id="72097-110">Der zugrunde liegende Kanal hat einen Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="72097-110">The underlying channel has raised a fault.</span></span>


<span data-ttu-id="72097-111">Um eine Abbruch Benachrichtigung zu erhalten, muss der Dienst Vorgang oder der Dienstmodell Rückruf einen [**WS- \_ Vorgangs \_ Abbruch- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) Rückruf registrieren, indem die [**wsregisteroperationforcancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="72097-111">To receive a cancellation notification, the service operation or service-model callback must register a [**WS\_OPERATION\_CANCEL\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) callback by calling the [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) function.</span></span>

<span data-ttu-id="72097-112">Optional kann der Dienst Vorgang oder der Dienstmodell Rückruf im Rahmen der Registrierung für eine Abbruch Benachrichtigung auch anwendungsspezifische Zustandsdaten und den Rückruf Rückruf für den [**WS \_ - \_ Vorgangs \_ freien \_ Status**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) registrieren.</span><span class="sxs-lookup"><span data-stu-id="72097-112">Optionally, as part of the registering for cancellation notification, the service operation or service-model callback can also register application-specific state data and the [**WS\_OPERATION\_FREE\_STATE\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) callback.</span></span>

<span data-ttu-id="72097-113">Die Zustandsdaten werden für den WS- [**\_ Vorgang zum \_ Abbrechen des \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) Rückrufs verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="72097-113">The state data is made available to the [**WS\_OPERATION\_CANCEL\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) callback.</span></span> <span data-ttu-id="72097-114">Bei der Beendigung des Aufrufs wird der Rückruf Rückruf Rückruf für den WS-Vorgang aufgerufen, um der Anwendung die Möglichkeit zu geben, die Zustandsdaten freizugeben. [**\_ \_ \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback)</span><span class="sxs-lookup"><span data-stu-id="72097-114">On call completion, the [**WS\_OPERATION\_FREE\_STATE\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) callback is called to give the application an opportunity to free the state data.</span></span>

<span data-ttu-id="72097-115">Ein Codebeispiel finden Sie unter [blockingserviceexample](blockingserviceexample.md).</span><span class="sxs-lookup"><span data-stu-id="72097-115">For a code example, see [BlockingServiceExample](blockingserviceexample.md).</span></span>

<span data-ttu-id="72097-116">Der Abbruch Rückruf wird nur einmal für die Lebensdauer der [serverseitigen Dienst Vorgänge](server-side-service-operations.md) oder Rückruffunktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="72097-116">The cancellation callback is called only once for the lifetime of the [server side service operations](server-side-service-operations.md) or callback function.</span></span>

<span data-ttu-id="72097-117">Der Aufruf Abbruch ist in für alle Dienst Host Rückrufe verfügbar, die den [WS- \_ Vorgangs \_ Kontext](ws-operation-context.md) als Parameter annehmen.</span><span class="sxs-lookup"><span data-stu-id="72097-117">Call cancellation is available in for all service host callbacks that take [WS\_OPERATION\_CONTEXT](ws-operation-context.md) as a parameter.</span></span>

<span data-ttu-id="72097-118">Die folgenden API-Elemente beziehen sich auf den Abbruch von anrufen.</span><span class="sxs-lookup"><span data-stu-id="72097-118">The following API elements relate to call cancellation.</span></span>

| <span data-ttu-id="72097-119">Rückruf</span><span class="sxs-lookup"><span data-stu-id="72097-119">Callback</span></span>                                                                         | <span data-ttu-id="72097-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72097-120">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72097-121">**WS- \_ Vorgang \_ Abbruch \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="72097-121">**WS\_OPERATION\_CANCEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)          | <span data-ttu-id="72097-122">Wird vom Dienstmodell aufgerufen, um einen Abbruch eines asynchronen Dienst Vorgangs aufgrund eines abgebrochenen herunter Fahrens des Dienst Hosts zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="72097-122">Invoked by service model to notify a cancellation of an asynchronous service operation as a result of an aborted shutdown of service host.</span></span> |
| [<span data-ttu-id="72097-123">**WS- \_ Vorgang, \_ freier \_ Zustands \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="72097-123">**WS\_OPERATION\_FREE\_STATE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) | <span data-ttu-id="72097-124">Wird vom Dienstmodell aufgerufen, um einer Anwendung das Bereinigen von Zustandsdaten zu ermöglichen, die beim Abbruch Rückruf registriert wurden.</span><span class="sxs-lookup"><span data-stu-id="72097-124">Invoked by service model to allow an application to clean up state data that was registered with the cancellation callback.</span></span>                |



 



| <span data-ttu-id="72097-125">Funktion</span><span class="sxs-lookup"><span data-stu-id="72097-125">Function</span></span>                                                             | <span data-ttu-id="72097-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72097-126">Description</span></span>                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72097-127">**Wsregisteroperationforcancel**</span><span class="sxs-lookup"><span data-stu-id="72097-127">**WsRegisterOperationForCancel**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) | <span data-ttu-id="72097-128">Ermöglicht, dass ein Dienst Vorgang oder ein Dienstmodell Rückruf für eine Abbruch Benachrichtigung registriert wird.</span><span class="sxs-lookup"><span data-stu-id="72097-128">Allows a service operation or service-model callback to register for a cancellation notification.</span></span> |



 

 

 




