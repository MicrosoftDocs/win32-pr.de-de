---
title: Server seitige Dienst Vorgänge
description: In diesem Abschnitt werden Dienst seitige Dienst Vorgänge beschrieben.
ms.assetid: d209cf2f-47f5-4025-8af4-1626c867a66a
keywords:
- Server seitige Service Operations-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c7ad5a327c1cb79278aa562bfaa1753f008a542
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104391234"
---
# <a name="server-side-service-operations"></a>Server seitige Dienst Vorgänge

In diesem Abschnitt werden Dienst seitige Dienst Vorgänge beschrieben.


Im folgenden finden Sie das Layout eines serverseitigen Dienst Vorgangs.

-   [ \_ \_ Kontext](ws-operation-context.md) Kontext Kontext des Konstanten WS-Vorgangs \* : der Vorgangs [Kontext](context.md).
-   Dienst Vorgangs Parameter: Parameter für den Dienst Vorgang.
-   konstanter [**WS- \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) \* asynchroner Kontext AsyncContext: asynchroner Kontext für die asynchrone Ausführung der Dienst Vorgänge.
-   [WS \_ Fehler](ws-error.md) \* Fehler: Rich Error-Objekt.

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

## <a name="fault-and-error-handling"></a>Fehler-und Fehlerbehandlung

Die Serverseite sollte Fehler verwenden, um Fehlerbedingungen an den Client zu übermitteln. Dies ist möglich, indem ein fehlerhaftes HRESULT zurückgegeben und der Fehler in das Fehler Objekt eingebettet wird.

Wenn der Fehler nicht für das Fehler Objekt festgelegt ist und ein HRESULT-Fehler zurückgegeben wird, versucht die Infrastruktur, einen Fehler an den Client zurückzusenden. Die Ebene der Details, die für den Client in einem solchen Fall offengelegt wird, wird von der [**WS- \_ Dienst \_ Eigenschaft \_ Fault \_ Disclosure**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) Service-Eigenschaft auf dem [Dienst Host](service-host.md)gesteuert.

## <a name="call-completion"></a>Rückruf Abschluss

Ein-Rückruf für einen synchronen serverseitigen Dienst Vorgang wird als "Complete" bezeichnet, wenn die Steuerung zurück an den Dienst Host zurückgegeben wurde. Bei einem asynchronen Dienst Vorgang wird ein-Rückruf als beendet betrachtet, sobald die Rückruf Benachrichtigung von der Dienst Vorgangs Implementierung ausgegeben wird.

## <a name="call-lifetime"></a>Lebensdauer von Anrufen

Beim Implementieren eines serverseitigen Dienst Vorgangs über seine Lebensdauer muss besonders darauf geachtet werden. Die Lebensdauer eines Aufrufes kann sich stark darauf auswirken, wie lange der Dienst Host heruntergefahren wird.

Wenn erwartet wird, dass ein serverseitiger Dienst Vorgang aufgrund eines e/a-gebundenen Vorgangs blockiert wird, wird empfohlen, einen Abbruch Rückruf so zu registrieren, dass er benachrichtigt wird, wenn der Dienst Host abgebrochen wird oder wenn die zugrunde liegende Verbindung vom Client geschlossen wird.

## <a name="server-side-service-operations-and-memory-consideration"></a>Server seitige Dienst Vorgänge und Arbeitsspeicher Überlegungen

Wenn ein Dienst Vorgang Arbeitsspeicher für die ausgehenden Parameter zuweisen muss, sollte er das [WS- \_ Heap](ws-heap.md) Objekt verwenden, das über den [WS- \_ Vorgangs \_ Kontext](ws-operation-context.md)verfügbar ist.

Beispiel: Dienst Vorgang und WS- \_ Heap

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

-   WS \_ S Async: der-Vorgang wird asynchron \_ abgeschlossen.
-   WS \_ S- \_ Ende: der-Vorgang wurde erfolgreich abgeschlossen, der Server erwartet außerhalb dieses Aufrufes keine [WS- \_ Nachricht](ws-message.md) vom Client. Wenn eine andere WS-Nachricht empfangen wird, \_ sollte der Server den Kanal abbrechen.
-   NoError/alle anderen Erfolgs-HRESULTs: der Rückruf wurde erfolgreich abgeschlossen. Beachten Sie, dass die Anwendung für einen erfolgreichen Abschluss des Dienst Vorgangs kein anderes HRESULT-Ergebnis als noError zurückgeben sollte.
-   Alles mit einem Fehler HRESULT: ein Fehler wird an den Client zurückgesendet, wenn ein Fehler in WS- \_ Fehler vorliegt. Andernfalls wird ein generischer Fehler zurück an den Client gesendet. Siehe Fehler Diskussion weiter oben.

Siehe, [Abbruch des Aufrufes](call-cancellation.md).

 

 




