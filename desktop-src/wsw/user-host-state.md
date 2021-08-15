---
title: Benutzerstatus des Diensthosts
description: Der Diensthost ermöglicht einer Anwendung das Zuordnen von Zustandsdaten, die auf Diensthostebene zugeordnet sind.
ms.assetid: e18c6c0c-3205-4f88-9a9b-2515a7cfc462
keywords:
- Webdienste für den Benutzerhostzustand für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04530b74ef1ab0125b31e56751cdd6cec8109711f603c909f3afeb66970f081a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192430"
---
# <a name="service-host-user-state"></a>Benutzerstatus des Diensthosts

Der [Diensthost](service-host.md) ermöglicht einer Anwendung das Zuordnen von Zustandsdaten, die auf Diensthostebene zugeordnet sind. Dieser Zustand wird durch eine [**WS \_ SERVICE \_ PROPERTY-Struktur**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) angegeben, die an die [**WsCreateServiceHost-Funktion**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) übergeben wird, wenn die Anwendung einen [Diensthost](service-host.md)erstellt, wie im folgenden Beispiel veranschaulicht.

``` syntax
void* quotePtr = (void*) quotes;
WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_HOST_USER_STATE;
serviceProperties[0].value = &quotePtr; // assume this is some state that you want to associate with the service host
serviceProperties[0].valueSize = sizeof(quotePtr);
```


Die Zustandsdaten sind für alle Diensthostrückrufe und [Dienstvorgänge](service-operation.md)verfügbar. Rückrufe und Dienstvorgänge rufen die Informationen ab, indem sie die [**WsGetOperationContextProperty-Funktion**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) aufrufen und den Kontext angeben, auf den von der [WS \_ OPERATION \_ CONTEXT-Struktur](ws-operation-context.md) verwiesen wird, sowie die Kontexteigenschaft als einen der Werte der [**WS \_ OPERATION CONTEXT PROPERTY HOST USER \_ \_ \_ \_ STATE-Eunumeration, \_**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id) wie im folgenden Beispiel veranschaulicht.

``` syntax
QuoteTable* table = NULL;
HRESULT hr = NOERROR;
if (FAILED (WsGetOperationContextProperty (context, WS_OPERATION_CONTEXT_PROPERTY_HOST_USER_STATE, &table, sizeof(table), NULL, error)))
    return hr;
```

 

 




