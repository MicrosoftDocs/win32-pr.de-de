---
title: Asynchrones Modell
description: Die meisten Vorgänge in der Windows-Webdienste-API können synchron oder asynchron ausgeführt werden.
ms.assetid: d0b3f154-2219-4085-a652-e9aeb126598c
keywords:
- Asynchrone modellweb Dienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c5e38dfbc0bc2ed397949da86f9a572a5b1ed5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341659"
---
# <a name="asynchronous-model"></a>Asynchrones Modell

Die meisten Vorgänge in der Windows-Webdienste-API können synchron oder asynchron ausgeführt werden. Um eine Funktion synchron aufzurufen, übergeben Sie einen NULL-Wert für die asynchrone [**WS- \_ \_ Kontext**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) Struktur. Um anzugeben, dass eine Funktion asynchron ausgeführt werden kann, übergeben Sie einen nicht-NULL- **WS- \_ Async- \_ Kontext** an die Funktion.

Wenn eine Funktion asynchron aufgerufen wird, kann Sie dennoch synchron oder asynchron ausgeführt werden. Wenn die Funktion synchron abgeschlossen wird, gibt Sie einen Wert zurück, der den endgültigen Erfolg oder Fehler angibt, und dieser Wert ist immer etwas anderes als **WS \_ S \_ Async** (siehe [Rückgabewerte für Windows-Webdienste](windows-web-services-return-values.md)). Der Rückgabewert von **WS \_ S \_ Async** gibt jedoch an, dass die Funktion asynchron vollständig ausgeführt wird. Wenn die Funktion asynchron abgeschlossen wird, wird ein Rückruf aufgerufen, um den Abschluss des Vorgangs zu signalisieren. Dieser Rückruf gibt den endgültigen Erfolg oder Fehlerwert an. Der Rückruf wird nicht aufgerufen, wenn der Vorgang synchron abgeschlossen wird.

Um einen asynchronen Kontext zu erstellen, initialisieren Sie die Felder **Callback** und **callbackstate** der [**Kontext Struktur WS \_ Async \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) . Das Feld **callbackstate** wird verwendet, um einen Zeiger auf benutzerdefinierte Daten anzugeben, die an die [**WS \_ Async- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) Funktion übermittelt werden.

Das folgende Beispiel zeigt, wie Sie eine Funktion asynchron aufrufen, indem Sie einen Zeiger an eine asynchrone [**WS- \_ \_ Kontext**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) Struktur übergeben, die den Rückruf und einen Zeiger auf die Zustandsdaten enthält.

``` syntax
HRESULT ExampleAsyncFunction(WS_ASYNC_CONTEXT* asyncContext);
void ExampleAsyncFunction()
{
    // Set up the WS_ASYNC_CONTEXT structure.
    MyState* myState = ...;  \\ Declare a pointer to user-defined data.
    WS_ASYNC_CONTEXT asyncContext;
    asyncContext.callback = MyCallback;  \\ Set the callback.
    asyncContext.callbackState = myState; \\ Set the pointer to the user-defined data.

    // Start the asynchronous operation
    HRESULT hr = SomeFunction(&asyncContext);

    if (hr == WS_S_ASYNC)
    {
        // The operation is completing asynchronously.  The callback is called 
        // when the operation is complete.
    }
    else
    {
        // The operation completed synchronously.  The callback is not called.
    }
}
void CALLBACK MyCallback(HRESULT hr, WS_CALLBACK_MODEL callbackModel, void* callbackState)
{
    MyState* myState = (MyState*)callbackState;

    // The operation completed asynchronously.
}
```

Die asynchrone [**WS- \_ \_ Kontext**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) Struktur wird von der asynchronen Funktion nur für die Dauer des Funktions Aufrufes verwendet (nicht für die Dauer des asynchronen Vorgangs), sodass Sie Sie sicher auf dem Stapel deklarieren können.

Wenn andere Parameter Außer der asynchronen [**WS- \_ \_ Kontext**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) Struktur an eine asynchrone Funktion als Zeiger übergeben werden und die Funktion asynchron abgeschlossen wird, liegt es in der Verantwortung des Aufrufers, die Werte, auf die diese Parameter zeigen, so lange zu speichern, bis der asynchrone Rückruf aufgerufen wird.

Es gibt Einschränkungen hinsichtlich der Vorgänge, die ein Rückruf ausführen kann. Weitere Informationen zu möglichen Vorgängen finden Sie im [**WS- \_ Rückruf \_ Modell**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model).

Wenn Sie eine asynchrone Funktion implementieren, rufen Sie den Rückruf nicht für denselben Thread auf, der die asynchrone Funktion aufgerufen hat, bevor die asynchrone Funktion an den Aufrufer zurückgegeben wurde, da dadurch das asynchrone Modell gestört wird.

Wenn Sie eine Funktion implementieren, die eine Reihe von asynchronen Vorgängen ausführen muss, sollten Sie ggf. die [**wsasyncexecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) -Hilfsfunktion verwenden.

Das [Beispiel für eine asynchrone Funktion](asyncmodelexample.md) zeigt, wie Funktionen implementiert und genutzt werden, die dem asynchronen Modell folgen.

Beim Starten eines asynchronen e/a-Vorgangs werden Systemressourcen beansprucht. Wenn genügend e/a-Vorgänge gestartet werden, kann das System nicht mehr reagiert. Um dies zu verhindern, muss eine Anwendung die Anzahl der asynchronen Vorgänge, die gestartet werden, einschränken.

Das asynchrone Modell verwendet die folgenden API-Elemente.

| Rückruf                                         | BESCHREIBUNG                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**WS \_ Async- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) | Der Rückruf Funktionsparameter, der mit dem asynchronen Modell verwendet wird.                                                                     |
| [**WS \_ Async- \_ Funktion**](/windows/desktop/api/WebServices/nc-webservices-ws_async_function) | Wird zusammen mit [**wsasyncexecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) verwendet, um die nächste Funktion anzugeben, die in einer Reihe von asynchronen Vorgängen aufgerufen werden soll. |



 



| Enumeration                                      | Beschreibung                                                                                                       |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**WS- \_ Rückruf \_ Modell**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model) | Gibt das Threading Verhalten eines Rückrufs an (z. b. einen [**WS \_ Async- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)). |



 



| Funktion                                 | BESCHREIBUNG                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Wsasyncexecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) | Ruft einen benutzerdefinierten Rückruf auf, der einen asynchronen Vorgang initiieren kann und eine Funktion angibt, die aufgerufen werden soll, wenn der asynchrone Vorgang abgeschlossen wurde. |



 



| Struktur                                          | BESCHREIBUNG                                                                                                                           |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**asynchroner WS- \_ \_ Kontext**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)     | Gibt den asynchronen Rückruf und einen Zeiger auf benutzerdefinierte Daten an, die an den asynchronen Rückruf übermittelt werden.            |
| [**WS \_ Async- \_ Vorgang**](/windows/desktop/api/WebServices/ns-webservices-ws_async_operation) | Wird zusammen mit [**wsasyncexecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) verwendet, um die nächste Funktion anzugeben, die in einer Reihe von asynchronen Vorgängen aufgerufen werden soll. |
| [**WS- \_ Async- \_ Status**](/windows/desktop/api/WebServices/ns-webservices-ws_async_state)         | Wird von [**wsasyncexecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) verwendet, um den Status eines asynchronen Vorgangs zu verwalten.                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiel für eine asynchrone Funktion](asyncmodelexample.md)
</dt> <dt>

[**WS \_ Async- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
</dt> <dt>

[**asynchroner WS- \_ \_ Kontext**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)
</dt> <dt>

[**WS- \_ Rückruf \_ Modell**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model)
</dt> <dt>

[**Wsasyncexecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute)
</dt> </dl>

 

 




