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
# <a name="context-windows-web-services"></a>Kontext (Windows-Webdienste)

Ein Kontext wird in Dienstmodell [Dienst-Vorgängen](service-operation.md) und-Rückrufen verwendet, um relevante Zustandsdaten an den Dienst Vorgang oder den Rückruf zu übergeben, wenn dieser aufgerufen wird. Auf einen Kontext wird durch eine [WS- \_ Vorgangs \_ Kontext](ws-operation-context.md) Struktur verwiesen. Die Eigenschaften eines Kontexts können mit der [**wsgetoperationcontextproperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) -Funktion abgerufen werden, wie im folgenden Code veranschaulicht.

``` syntax
WS_MESSAGE* requestMessage = NULL;
HRESULT hr = WsGetOperationContextProperty (
                context, 
                WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE, 
                &requestMessage, 
                sizeof(requestMessage),
                error);
```

Nicht alle Kontexteigenschaften sind zu einem bestimmten Zeitpunkt verfügbar. Weitere Informationen zur Verfügbarkeit einer bestimmten Eigenschaft in einem Rückruf-oder [Dienst Vorgang](service-operation.md)finden Sie in der Dokumentation zur Kontext Eigenschaft.

Weitere Informationen zum Verwalten der Lebensdauer des Vorgangs Kontexts und des Threading finden Sie im Thema [Vorgangs Kontext Lebensdauer und Threading](operation-context-lifetime-and-threading.md) .

Die folgende Enumeration ist Teil des Kontexts:

-   [**WS- \_ Vorgangs \_ Kontext-Eigenschaften- \_ \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id)

Die folgende Funktion ist Teil des Kontexts:

-   [**Wsgetoperationcontextproperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty)

Das folgende Handle ist Teil des Kontexts:

-   [WS- \_ Vorgangs \_ Kontext](ws-operation-context.md)

 

 




