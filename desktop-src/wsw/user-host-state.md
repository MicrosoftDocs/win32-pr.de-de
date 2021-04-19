---
title: Benutzer Zustand des Dienst Hosts
description: Der Dienst Host ermöglicht einer Anwendung das Zuordnen von Zustandsdaten, deren Gültigkeitsbereich auf Dienst-Host Ebene liegt.
ms.assetid: e18c6c0c-3205-4f88-9a9b-2515a7cfc462
keywords:
- Benutzerhoststatus-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56f43942f7743d28534e0286a45203dc01e0e7b6
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "106341755"
---
# <a name="service-host-user-state"></a><span data-ttu-id="ed1b5-106">Benutzer Zustand des Dienst Hosts</span><span class="sxs-lookup"><span data-stu-id="ed1b5-106">Service Host User State</span></span>

<span data-ttu-id="ed1b5-107">Der [Dienst Host](service-host.md) ermöglicht einer Anwendung das Zuordnen von Zustandsdaten, deren Gültigkeitsbereich auf Dienst-Host Ebene liegt.</span><span class="sxs-lookup"><span data-stu-id="ed1b5-107">The [service host](service-host.md) enables an application to associate state data that is scoped at the service-host level.</span></span> <span data-ttu-id="ed1b5-108">Dieser Status wird durch eine WS- [**\_ Dienst \_ Eigenschafts**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) Struktur angegeben, die an die [**wscreateservicehost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) -Funktion übergeben wird, wenn die Anwendung einen [Dienst Host](service-host.md)erstellt, wie im folgenden Beispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="ed1b5-108">This state is is specified by a [**WS\_SERVICE\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) structure that is passed to the [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) function when the application creates a [service host](service-host.md), as illustrated in the following example.</span></span>

``` syntax
void* quotePtr = (void*) quotes;
WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_HOST_USER_STATE;
serviceProperties[0].value = &quotePtr; // assume this is some state that you want to associate with the service host
serviceProperties[0].valueSize = sizeof(quotePtr);
```


<span data-ttu-id="ed1b5-109">Die Zustandsdaten sind für alle Dienst Host Rückrufe und [Dienst Vorgänge](service-operation.md)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ed1b5-109">The state data is available to all service host callbacks and [service operations](service-operation.md).</span></span> <span data-ttu-id="ed1b5-110">Rückrufe und Dienst Vorgänge rufen die Informationen ab, indem Sie die [**wsgetoperationcontextproperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) -Funktion aufrufen und den Kontext, auf den von der [WS- \_ Vorgangs \_ Kontext](ws-operation-context.md) Struktur verwiesen wird, und die Context-Eigenschaft als einen der Werte der [**WS- \_ Vorgangs \_ Kontext \_ Eigenschaft \_ Host \_ User \_ State**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id) eunumeration, wie im folgenden Beispiel gezeigt, angeben.</span><span class="sxs-lookup"><span data-stu-id="ed1b5-110">Callbacks and service operations retrieve the information by calling the [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) function and specifying the context, referenced by the [WS\_OPERATION\_CONTEXT](ws-operation-context.md) structure, and the context property, as one of the values of the [**WS\_OPERATION\_CONTEXT\_PROPERTY\_HOST\_USER\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id) eunumeration, as illustrated in the following example.</span></span>

``` syntax
QuoteTable* table = NULL;
HRESULT hr = NOERROR;
if (FAILED (WsGetOperationContextProperty (context, WS_OPERATION_CONTEXT_PROPERTY_HOST_USER_STATE, &table, sizeof(table), NULL, error)))
    return hr;
```

 

 




