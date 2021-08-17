---
title: Serverseitige Dienstvorgänge
description: In diesem Abschnitt werden dienstseitige Dienstvorgänge beschrieben.
ms.assetid: d209cf2f-47f5-4025-8af4-1626c867a66a
keywords:
- Serverseitige Dienstvorgänge Webdienste für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f1656e56df08d00a0551946c4e52898beccd4d1a37a5bd96c63eb2066928fe1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119344630"
---
# <a name="server-side-service-operations"></a>Serverseitige Dienstvorgänge

In diesem Abschnitt werden dienstseitige Dienstvorgänge beschrieben.


Im Folgenden finden Sie das Layout eines serverseitigen Dienstvorgang.

-   const [WS \_ OPERATION \_ CONTEXT](ws-operation-context.md) \* context: Der Vorgangskontext . [](context.md)
-   Dienstbetriebsparameter: Parameter für den Dienstvorgang.
-   const [**WS \_ ASYNC \_ CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) \* asyncContext: asynchroner Kontext zum asynchronen Ausführen der Dienstvorgänge.
-   [WS \_ FEHLERfehler:](ws-error.md) \* Umfangreiches Fehlerobjekt.

``` syntax
HRESULT CALLBACK Add(const WS_OPERATION_CONTEXT* context, 
                     ULONG a, ULONG b, ULONG* result, 
                     const WS_ASYNC_CONTEXT* asyncContext, 
                     WS_ERROR* error)
{
    *result = a +b;
    return NOERROR;
}
```

## <a name="fault-and-error-handling"></a>Fehler- und Fehlerbehandlung

Die Serverseite sollte Fehler verwenden, um Fehlerbedingungen an den Client zu senden. Dazu kann ein fehlerhaftes HRESULT zurückgegeben und der Fehler in das Fehlerobjekt eingebettet werden.

Wenn der Fehler nicht für das Fehlerobjekt festgelegt ist und ein Fehler HRESULT zurückgegeben wird, versucht die Infrastruktur, einen Fehler an den Client zurück zu liefern. Die Ebene der Details, die dem Client in einem solchen Fall offengelegt werden, wird durch die [**WS \_ SERVICE PROPERTY \_ FAULT \_ \_ DISCLOSURE-Diensteigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) auf dem [Diensthost gesteuert.](service-host.md)

## <a name="call-completion"></a>Aufrufabschluss

Ein Aufruf eines synchronen serverseitigen Dienstvorgang wird als abgeschlossen bezeichnet, wenn einer der Beiden die Steuerung an den Diensthost zurückgegeben hat. Bei einem asynchronen Dienstvorgang gilt ein Aufruf als abgeschlossen, sobald die Rückrufbenachrichtigung von der Dienstvorgangimplementierung ausgegeben wird.

## <a name="call-lifetime"></a>Aufruflebensdauer

Bei der Implementierung eines serverseitigen Dienstvorgang über dessen Lebensdauer sollte besondere Vorsichtsmaßnahmen ergriffen werden. Die Lebensdauer eines Aufrufs kann sich stark darauf auswirken, wie lange das Herunterfahren des Diensthosts dauert.

Wenn erwartet wird, dass ein serverseitiger Dienstvorgang aufgrund eines E/A-gebundenen Vorgangs blockiert wird, wird empfohlen, einen Abbruchrückruf so zu registrieren, dass er benachrichtigt wird, wenn der Diensthost abgebrochen wird oder wenn die zugrunde liegende Verbindung vom Client geschlossen wird.

## <a name="server-side-service-operations-and-memory-consideration"></a>Serverseitige Dienstvorgänge und Arbeitsspeicherberücksichtigung

Wenn ein Dienstvorgang Speicher für seine ausgehenden Parameter zuordnen muss, sollte er [das \_ WS-HEAP-Objekt](ws-heap.md) verwenden, das über den [ \_ WS-VORGANGSKONTEXT verfügbar \_ ist.](ws-operation-context.md)

Beispiel: Dienstvorgang und \_ WS-HEAP

``` syntax
HRESULT CALLBACK ProcessOrder (const WS_OPERATION_CONTEXT* context, const ULONG orderNumber, OrderReceipt** orderReceipt, const WS_ASYNC_CONTEXT* asyncContext, WS_ERROR* error)
{
    WS_HEAP* heap;
    HRESULT hr = WsGetOperationContextProperty (context, WS_OPERATION_CONTEXT_PROPERTY_HEAP, &heap, sizeof(heap), NULL, error);
    if (FAILED(hr))
        return hr;
    hr = WsAlloc(heap, sizeof (OrderReceipt), orderReceipt, error);
    if (FAILED(hr))
        return hr;
    hr = FillInReceipt(*orderReceipt);
    if (FAILED(hr))
        return hr;
    return NOERROR;
} 
```

## <a name="return-values"></a>Rückgabewerte

-   WS \_ S \_ ASYNC: Der Aufruf wird asynchron abgeschlossen.
-   WS S END: Der Aufruf wurde erfolgreich abgeschlossen, der Server erwartet über diesen Aufruf hinaus keine \_ \_ [ \_ WS-NACHRICHT](ws-message.md) vom Client. Wenn eine andere \_ WS-NACHRICHT einkommt, sollte der Server den Kanal abbrechen.
-   NOERROR/Alle anderen erfolgreichen HRESULTS: Der Aufruf wurde erfolgreich abgeschlossen. Beachten Sie, dass es empfohlen wird, dass die Anwendung für den erfolgreichen Abschluss des Dienstbetriebs kein anderes HRESULT als NOERROR zurückgibt.
-   Alles mit einem Fehler-HRESULT: Ein Fehler wird an den Client zurück gesendet, wenn ein Fehler in WS ERROR verfügbar \_ ist. Andernfalls wird ein generischer Fehler zurück an den Client gesendet. Siehe Fehlerdiskussion oben.

Weitere Informationen finden Sie [unter Aufrufabbruch.](call-cancellation.md)

 

 




