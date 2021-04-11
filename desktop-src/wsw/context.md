---
title: Kontext (Windows-Webdienste)
description: Ein Kontext wird in Dienstmodell Dienst-Vorgängen und-Rückrufen verwendet, um relevante Zustandsdaten an den Dienst Vorgang oder den Rückruf zu übergeben, wenn dieser aufgerufen wird.
ms.assetid: 44283854-96df-4e6b-8464-3df685896f07
keywords:
- Kontext-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7edd1f8c93bbf4fd4b4d5feea5b2219bc522ea
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "103948335"
---
# <a name="context-windows-web-services"></a><span data-ttu-id="44e14-106">Kontext (Windows-Webdienste)</span><span class="sxs-lookup"><span data-stu-id="44e14-106">Context (Windows Web Services)</span></span>

<span data-ttu-id="44e14-107">Ein Kontext wird in Dienstmodell [Dienst-Vorgängen](service-operation.md) und-Rückrufen verwendet, um relevante Zustandsdaten an den Dienst Vorgang oder den Rückruf zu übergeben, wenn dieser aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="44e14-107">A context is used in Service Model [service operations](service-operation.md) and callbacks to pass relevant state data to the service operation or callback when it is invoked.</span></span> <span data-ttu-id="44e14-108">Auf einen Kontext wird durch eine [WS- \_ Vorgangs \_ Kontext](ws-operation-context.md) Struktur verwiesen.</span><span class="sxs-lookup"><span data-stu-id="44e14-108">A context is referenced by a [WS\_OPERATION\_CONTEXT](ws-operation-context.md) structure.</span></span> <span data-ttu-id="44e14-109">Die Eigenschaften eines Kontexts können mit der [**wsgetoperationcontextproperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) -Funktion abgerufen werden, wie im folgenden Code veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="44e14-109">The properties of a context can be retrieved with the [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) function, as illustrated in the following code.</span></span>

``` syntax
WS_MESSAGE* requestMessage = NULL;
HRESULT hr = WsGetOperationContextProperty (
                context, 
                WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE, 
                &requestMessage, 
                sizeof(requestMessage),
                error);
```

<span data-ttu-id="44e14-110">Nicht alle Kontexteigenschaften sind zu einem bestimmten Zeitpunkt verfügbar.</span><span class="sxs-lookup"><span data-stu-id="44e14-110">Not all the context properties are available at any given time.</span></span> <span data-ttu-id="44e14-111">Weitere Informationen zur Verfügbarkeit einer bestimmten Eigenschaft in einem Rückruf-oder [Dienst Vorgang](service-operation.md)finden Sie in der Dokumentation zur Kontext Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="44e14-111">See the context property documentation regarding availability of a specific property in a callback or a [service operation](service-operation.md).</span></span>

<span data-ttu-id="44e14-112">Weitere Informationen zum Verwalten der Lebensdauer des Vorgangs Kontexts und des Threading finden Sie im Thema [Vorgangs Kontext Lebensdauer und Threading](operation-context-lifetime-and-threading.md) .</span><span class="sxs-lookup"><span data-stu-id="44e14-112">For more information on how to maintain operation context lifetime and threading, see the [Operation Context Lifetime and Threading](operation-context-lifetime-and-threading.md) topic.</span></span>

<span data-ttu-id="44e14-113">Die folgende Enumeration ist Teil des Kontexts:</span><span class="sxs-lookup"><span data-stu-id="44e14-113">The following enumeration is part of the context:</span></span>

-   [<span data-ttu-id="44e14-114">**WS- \_ Vorgangs \_ Kontext-Eigenschaften- \_ \_ ID**</span><span class="sxs-lookup"><span data-stu-id="44e14-114">**WS\_OPERATION\_CONTEXT\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id)

<span data-ttu-id="44e14-115">Die folgende Funktion ist Teil des Kontexts:</span><span class="sxs-lookup"><span data-stu-id="44e14-115">The following function is part of the context:</span></span>

-   [<span data-ttu-id="44e14-116">**Wsgetoperationcontextproperty**</span><span class="sxs-lookup"><span data-stu-id="44e14-116">**WsGetOperationContextProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty)

<span data-ttu-id="44e14-117">Das folgende Handle ist Teil des Kontexts:</span><span class="sxs-lookup"><span data-stu-id="44e14-117">The following handle is part of the context:</span></span>

-   [<span data-ttu-id="44e14-118">WS- \_ Vorgangs \_ Kontext</span><span class="sxs-lookup"><span data-stu-id="44e14-118">WS\_OPERATION\_CONTEXT</span></span>](ws-operation-context.md)

 

 




