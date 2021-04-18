---
description: Aufrufen von asynchronen Methoden
ms.assetid: 1d8688a5-d476-457d-a0ad-e4f106ac3484
title: Aufrufen von asynchronen Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bdd6e272aeb3203706f0c621b4634cf3e6c0562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524643"
---
# <a name="calling-asynchronous-methods"></a>Aufrufen von asynchronen Methoden

In Media Foundation werden viele Vorgänge asynchron ausgeführt. Asynchrone Vorgänge können die Leistung verbessern, da Sie den aufrufenden Thread nicht blockieren. Ein asynchroner Vorgang in Media Foundation wird durch ein paar von Methoden definiert, wobei die Benennungs Konvention **BEGIN...** und **End....** Zusammen definieren diese beiden Methoden einen asynchronen Lesevorgang für den Datenstrom.

Um einen asynchronen Vorgang zu starten, müssen Sie die **Begin** -Methode aufzurufen. Die **Begin** -Methode enthält immer mindestens zwei Parameter:

-   Ein Zeiger auf die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle. Die Anwendung muss diese Schnittstelle implementieren.
-   Ein Zeiger auf ein optionales Zustands Objekt.

Die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle benachrichtigt die Anwendung, wenn der Vorgang abgeschlossen ist. Ein Beispiel für die Implementierung dieser Schnittstelle finden Sie unter [Implementieren des asynchronen Rückrufs](implementing-the-asynchronous-callback.md). Das Zustands Objekt ist optional. Wenn angegeben, muss die **IUnknown** -Schnittstelle implementiert werden. Sie können das State-Objekt verwenden, um alle Zustandsinformationen zu speichern, die von Ihrem Rückruf benötigt werden. Wenn Sie keine Zustandsinformationen benötigen, können Sie diesen Parameter auf **null** festlegen. Die **Begin** -Methode kann zusätzliche Parameter enthalten, die für diese Methode spezifisch sind.

Wenn die **Begin** -Methode einen Fehlercode zurückgibt, bedeutet dies, dass der Vorgang sofort fehlgeschlagen ist und der Rückruf nicht aufgerufen wird. Wenn die **Begin** -Methode erfolgreich ist, bedeutet dies, dass der Vorgang aussteht und der Rückruf aufgerufen wird, wenn der Vorgang abgeschlossen ist.

Die [**IMF Bytestream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) -Methode startet z. b. einen asynchronen Lesevorgang für einen Bytestream:


```C++
    BYTE data[DATA_SIZE];
    ULONG cbRead = 0;

    CMyCallback *pCB = new (std::nothrow) CMyCallback(pStream, &hr);

    if (pCB == NULL)
    {
        hr = E_OUTOFMEMORY;
    }

    // Start an asynchronous request to read data.
    if (SUCCEEDED(hr))
    {
        hr = pStream->BeginRead(data, DATA_SIZE, pCB, NULL);
    }
```



Die Rückruf Methode ist [**imfasynccallback:: Aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke). Er verfügt über einen einzelnen Parameter, *pasynkresult*, der ein Zeiger auf die [**imfasynkresult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) -Schnittstelle ist. Um den asynchronen Vorgang abzuschließen, nennen Sie die **End** -Methode, die mit der asynchronen **Begin** -Methode übereinstimmt. Die **End** -Methode nimmt immer einen **imfasynkresult** -Zeiger an. Übergeben Sie immer denselben Zeiger, den Sie in der **Aufruf** Methode erhalten haben. Der asynchrone Vorgang ist erst abgeschlossen, wenn Sie die **End** -Methode aufgerufen haben. Sie können die **End** **-Methode innerhalb der Aufruf** Methode aufrufen, oder Sie können Sie von einem anderen Thread aus aufrufen.

Um z. b. [**imfbytestream:: BeginRead für einen Bytestream**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) abzuschließen, nennen Sie [**imfbytestream:: EndRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread):


```C++
    STDMETHODIMP Invoke(IMFAsyncResult* pResult)
    {
        m_hrStatus = m_pStream->EndRead(pResult, &m_cbRead);

        SetEvent(m_hEvent);

        return S_OK;
    }
```



Der Rückgabewert der **End** -Methode gibt den Status des asynchronen Vorgangs an. In den meisten Fällen führt die Anwendung nach Abschluss des asynchronen Vorgangs einige Aufgaben aus, ob Sie erfolgreich abgeschlossen wurde oder nicht. Sie haben mehrere Möglichkeiten:

-   Führen Sie die Arbeit innerhalb der [**Aufruf**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Methode aus. Diese Vorgehensweise ist akzeptabel, wenn Ihre Anwendung den aufrufenden Thread niemals blockiert oder auf etwas in der **Aufruf** Methode wartet. Wenn Sie den aufrufenden Thread blockieren, kann die streamingpipeline blockiert werden. Beispielsweise können Sie einige Zustandsvariablen aktualisieren, aber keinen synchronen Lesevorgang ausführen oder auf ein Mutex-Objekt warten.
-   Legen Sie in der [**Aufruf**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Methode ein Ereignis fest, und geben Sie sofort zurück. Der Aufruf Thread der Anwendung wartet auf das Ereignis und führt die Arbeit aus, wenn das Ereignis signalisiert wird.
-   Stellen Sie in der [**Aufruf**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Methode eine private Fenster Meldung in Ihrem Anwendungsfenster bereit, und geben Sie sofort zurück. Die Anwendung führt die Verarbeitung in der Nachrichten Schleife durch. (Stellen Sie sicher, dass Sie die Nachricht senden, indem Sie **PostMessage** und nicht **SendMessage** aufrufen, da **SendMessage** den Rückruf Thread blockieren kann.)

Beachten Sie, dass [**aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) von einem anderen Thread aufgerufen wird. Ihre Anwendung ist dafür verantwortlich, sicherzustellen, dass jede im **Aufruf** ausgeführte Arbeit Thread sicher ist.

Der Thread, der " [**aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) " aufruft, trifft standardmäßig keine Annahmen über das Verhalten Ihres Rückruf Objekts. Optional können Sie die [**imfasynccallback:: GetParameters**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters) -Methode implementieren, um Informationen zu ihrer Rückruf Implementierung zurückzugeben. Andernfalls kann diese Methode **E \_ notimpl** zurückgeben:


```C++
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
```



Wenn Sie in der **Begin** -Methode ein Zustands Objekt angegeben haben, können Sie es aus der Rückruf Methode abrufen, indem Sie [**imfasyncresult:: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate)aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Asynchrone Rückruf Methoden](asynchronous-callback-methods.md)
</dt> </dl>

 

 



