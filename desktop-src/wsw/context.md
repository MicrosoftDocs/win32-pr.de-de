---
title: Kontext (Windows Webdienste)
description: Ein Kontext wird in Dienstvorgängen und Rückrufen des Dienstmodells verwendet, um relevante Zustandsdaten an den Dienstvorgang oder Rückruf zu übergeben, wenn er aufgerufen wird.
ms.assetid: 44283854-96df-4e6b-8464-3df685896f07
keywords:
- Context Web Services for Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd7863f22193dd1496134afff991ff54efbee5026f2a11e52359b2b016c878c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026628"
---
# <a name="context-windows-web-services"></a>Kontext (Windows Webdienste)

Ein Kontext wird in [](service-operation.md) Dienstvorgängen und Rückrufen des Dienstmodells verwendet, um relevante Zustandsdaten an den Dienstvorgang oder Rückruf zu übergeben, wenn er aufgerufen wird. Auf einen Kontext wird von einer [WS \_ OPERATION \_ CONTEXT-Struktur](ws-operation-context.md) verwiesen. Die Eigenschaften eines Kontexts können wie im folgenden Code veranschaulicht mit der [**WsGetOperationContextProperty-Funktion**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) abgerufen werden.

``` syntax
WS_MESSAGE* requestMessage = NULL;
HRESULT hr = WsGetOperationContextProperty (
                context, 
                WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE, 
                &requestMessage, 
                sizeof(requestMessage),
                error);
```

Nicht alle Kontexteigenschaften sind zu einem bestimmten Zeitpunkt verfügbar. Informationen zur Verfügbarkeit einer bestimmten Eigenschaft in einem Rückruf oder dienstvorgang finden Sie in der Dokumentation zur [Kontexteigenschaft.](service-operation.md)

Weitere Informationen zum Verwalten der Lebensdauer des Vorgangskontexts und des Threadings finden Sie im Thema Lebensdauer und [Threading](operation-context-lifetime-and-threading.md) des Vorgangskontexts.

Die folgende Enumeration ist Teil des Kontexts:

-   [**\_ \_ \_ WS-VORGANGSKONTEXT-EIGENSCHAFTEN-ID \_**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id)

Die folgende Funktion ist Teil des Kontexts:

-   [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty)

Das folgende Handle ist Teil des Kontexts:

-   [\_WS-VORGANGSKONTEXT \_](ws-operation-context.md)

 

 




