---
description: Aufrufen asynchroner Methoden
ms.assetid: 1d8688a5-d476-457d-a0ad-e4f106ac3484
title: Aufrufen asynchroner Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a53f5f0a3062ad6af955fbbfdd8cd05c82b30271cf680d6434bc652d567325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959200"
---
# <a name="calling-asynchronous-methods"></a>Aufrufen asynchroner Methoden

In Media Foundation werden viele Vorgänge asynchron ausgeführt. Asynchrone Vorgänge können die Leistung verbessern, da sie den aufrufenden Thread nicht blockieren. Ein asynchroner Vorgang in Media Foundation wird durch ein Methodenpaar mit der Namenskonvention **Begin...** und **End... definiert.** Zusammen definieren diese beiden Methoden einen asynchronen Lesevorgang für den Stream.

Um einen asynchronen Vorgang zu starten, rufen Sie die **Begin-Methode** auf. Die **Begin-Methode** enthält immer mindestens zwei Parameter:

-   Ein Zeiger auf [**dieASYNCCallback-Schnittstelle.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) Die Anwendung muss diese Schnittstelle implementieren.
-   Ein Zeiger auf ein optionales Zustandsobjekt.

[**DieASYNCAsyncCallback-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) benachrichtigt die Anwendung, wenn der Vorgang abgeschlossen ist. Ein Beispiel für die Implementierung dieser Schnittstelle finden Sie unter [Implementieren des asynchronen Rückrufs.](implementing-the-asynchronous-callback.md) Das Zustandsobjekt ist optional. Wenn angegeben, muss die **IUnknown-Schnittstelle implementiert** werden. Sie können das Zustandsobjekt verwenden, um alle Zustandsinformationen zu speichern, die von Ihrem Rückruf benötigt werden. Wenn Sie keine Zustandsinformationen benötigen, können Sie diesen Parameter auf **NULL festlegen.** Die **Begin-Methode** kann zusätzliche Parameter enthalten, die für diese Methode spezifisch sind.

Wenn die **Begin-Methode** einen Fehlercode zurückgibt, bedeutet dies, dass der Vorgang sofort fehlgeschlagen ist und der Rückruf nicht aufgerufen wird. Wenn die **Begin-Methode** erfolgreich ist, bedeutet dies, dass der Vorgang aussteht, und der Rückruf wird aufgerufen, wenn der Vorgang abgeschlossen ist.

Beispielsweise startet die [**METHODE ASYNCHRONOUSByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) einen asynchronen Lesevorgang für einen Bytestream:


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



Die Rückrufmethode ist [**"ASYNCAsyncCallback::Invoke".**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Es verfügt über einen einzelnen Parameter, *pAsyncResult,* der ein Zeiger auf [**dieASYNCAsyncResult-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) ist. Rufen Sie zum Abschließen des asynchronen Vorgangs die **End-Methode** auf, die der asynchronen **Begin-Methode** entspricht. Die **End-Methode** verwendet immer **einenASYNCAsyncResult-Zeiger.** Übergeben Sie immer denselben Zeiger, den Sie in der **Invoke-Methode erhalten** haben. Der asynchrone Vorgang ist erst abgeschlossen, wenn Sie die **End-Methode** aufrufen. Sie können die **End-Methode** innerhalb der **Invoke-Methode** aufrufen, oder Sie können sie aus einem anderen Thread aufrufen.

Rufen Sie z. B. ZUM Vervollständigen [**des NSBByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) für einen Bytestream [**DEN AUFRUF VON DURCHBYTESTREAM::EndRead auf:**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread)


```C++
    STDMETHODIMP Invoke(IMFAsyncResult* pResult)
    {
        m_hrStatus = m_pStream->EndRead(pResult, &m_cbRead);

        SetEvent(m_hEvent);

        return S_OK;
    }
```



Der Rückgabewert der **End-Methode** gibt den Status des asynchronen Vorgangs an. In den meisten Fällen führt Ihre Anwendung einige Aufgaben aus, nachdem der asynchrone Vorgang abgeschlossen wurde, unabhängig davon, ob er erfolgreich abgeschlossen wurde oder nicht. Sie haben mehrere Möglichkeiten:

-   Nehmen Sie die Arbeit innerhalb der [**Invoke-Methode**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) vor. Dieser Ansatz ist akzeptabel, solange Ihre Anwendung nie den aufrufenden Thread blockiert oder auf etwas innerhalb der **Invoke-Methode** wartet. Wenn Sie den aufrufenden Thread blockieren, können Sie die Streamingpipeline blockieren. Beispielsweise können Sie einige Zustandsvariablen aktualisieren, aber keinen synchronen Lesevorgang ausführen oder auf ein Mutex-Objekt warten.
-   Legen Sie in [**der Invoke-Methode**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) ein Ereignis fest, und geben Sie sofort zurück. Der aufrufende Thread der Anwendung wartet auf das Ereignis und führt die Arbeit aus, wenn das Ereignis signalisiert wird.
-   Posten Sie [**in der Invoke-Methode**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) eine Private Window-Nachricht in Ihr Anwendungsfenster, und kehren Sie sofort zurück. Die Anwendung führt die Arbeit an ihrer Nachrichtenschleife aus. (Stellen Sie sicher, dass Sie die Nachricht veröffentlichen, indem Sie **PostMessage** aufrufen, nicht **SendMessage,** da **SendMessage** den Rückrufthread blockieren kann.)

Beachten Sie, dass [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) von einem anderen Thread aufgerufen wird. Ihre Anwendung ist dafür verantwortlich, sicherzustellen, dass alle innerhalb von **Invoke** ausgeführten Aufgaben threadsicher sind.

Standardmäßig macht der Thread, der [**Invoke aufruft,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) keine Annahmen über das Verhalten Ihres Rückrufobjekts. Optional können Sie die [**METHODEASYNCCallback::GetParameters**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters) implementieren, um Informationen zu Ihrer Rückrufimplementierung zurück zu geben. Andernfalls kann diese Methode **E \_ NOTIMPL zurückgeben:**


```C++
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
```



Wenn Sie ein Zustandsobjekt in der **Begin-Methode** angegeben haben, können Sie es aus der Rückrufmethode abrufen, indem Sie [**DEN WERTASYNCResult::GetState aufrufen.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Asynchrone Rückrufmethoden](asynchronous-callback-methods.md)
</dt> </dl>

 

 



