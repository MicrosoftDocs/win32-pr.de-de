---
description: In diesem Thema wird beschrieben, wie eine asynchrone Methode in Microsoft Media Foundation implementiert wird.
ms.assetid: cd94280d-7267-4d35-8333-aa4a5bd81b73
title: Schreiben einer asynchronen Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d8360d0c15fe25661b8cd0f0f5adc9768db8ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348238"
---
# <a name="writing-an-asynchronous-method"></a>Schreiben einer asynchronen Methode

In diesem Thema wird beschrieben, wie eine asynchrone Methode in Microsoft Media Foundation implementiert wird.

Asynchrone Methoden sind in der Media Foundation Pipeline allgegenwärtig. Asynchrone Methoden vereinfachen die Verteilung von Arbeit auf mehrere Threads. Es ist besonders wichtig, e/a-Vorgänge asynchron auszuführen, damit das Lesen aus einer Datei oder einem Netzwerk den Rest der Pipeline nicht blockiert.

Wenn Sie eine Medienquelle oder eine Medien Senke schreiben, ist es von entscheidender Bedeutung, asynchrone Vorgänge ordnungsgemäß zu verarbeiten, da sich die Leistung der Komponente auf die gesamte Pipeline auswirkt.

> [!Note]  
> Media Foundation Transformationen (MFTs) verwenden synchrone Methoden standardmäßig.

 

### <a name="work-queues-for-asynchronous-operations"></a>Arbeits Warteschlangen für asynchrone Vorgänge

In Media Foundation gibt es eine enge Beziehung zwischen [asynchronen Rückruf Methoden](asynchronous-callback-methods.md) und [Arbeits Warteschlangen](work-queues.md). Eine Arbeits Warteschlange ist eine Abstraktion zum Verschieben von Arbeit aus dem Thread des Aufrufers in einen Arbeits Thread. Gehen Sie folgendermaßen vor, um Arbeit an einer Arbeits Warteschlange auszuführen:

1.  Implementieren Sie die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle.
2.  Rufen Sie [**mfkreateasynkresult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) auf, um ein *Ergebnis* Objekt zu erstellen. Das Ergebnis Objekt macht [**imfasynkresult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)verfügbar. Das Ergebnis Objekt enthält drei Zeiger:

    -   Ein Zeiger auf die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle des Aufrufers.
    -   Ein optionaler Zeiger auf ein Zustands Objekt. Wenn angegeben, muss das Zustands Objekt **IUnknown** implementieren.
    -   Ein optionaler Zeiger auf ein privates Objekt. Wenn angegeben, muss dieses Objekt auch **IUnknown** implementieren.

    Die letzten beiden Zeiger können **null** sein. Verwenden Sie diese andernfalls zum Speichern von Informationen über den asynchronen Vorgang.

3.  [**Mfputworkitemex**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) wird aufgerufen, um das Arbeits Element in die Warteschlange zu stellen.
4.  Der Arbeits Warteschlangen Thread ruft die [**imfasynccallback:: Aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) -Methode auf.
5.  Führen Sie die Arbeit innerhalb der [**Aufruf**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Methode aus. Der *pasynkresult* -Parameter dieser Methode ist der [**imfasynkresult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) -Zeiger aus Schritt 2. Verwenden Sie diesen Zeiger, um das State-Objekt und das private-Objekt zu erhalten:
    -   Um das State-Objekt abzurufen, nennen Sie [**imfasynkresult:: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).
    -   Um das private Objekt abzurufen, nennen Sie [**imfasynkresult:: GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject).

Als Alternative können Sie die Schritte 2 und 3 durch Aufrufen der Funktion " [**mfputworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) " kombinieren. Intern ruft diese Funktion [**mfkreateasynkresult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) auf, um das Ergebnis Objekt zu erstellen.

Das folgende Diagramm zeigt die Beziehungen zwischen dem Aufrufer, dem Ergebnis Objekt, dem Zustands Objekt und dem privaten Objekt.

![Diagramm, das ein asynchrones Ergebnis Objekt anzeigt](images/workqueues01.png)

Das folgende Sequenzdiagramm zeigt, wie ein-Objekt eine Arbeitsaufgabe in die Warteschlange stellt. Wenn der Arbeits Warteschlangen Thread [**aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)aufruft, führt das-Objekt den asynchronen Vorgang in diesem Thread aus.

![Diagramm, das zeigt, wie ein Objekt in die Warteschlange eines Arbeits](images/workqueues02.png)

Beachten Sie, dass [**aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) von einem Thread aufgerufen wird, der sich im Besitz der Arbeits Warteschlange befindet. Die **Implementierung des** Aufrufs muss Thread sicher sein. Wenn Sie die Platform Work Queue (**mfasync \_ Callback \_ Queue \_ Standard**) verwenden, ist es außerdem wichtig, dass Sie den Thread nie blockieren, da dadurch die gesamte Media Foundation Pipeline die Verarbeitung von Daten blockieren kann. Wenn Sie einen Vorgang ausführen müssen, der blockiert wird oder lange dauert, verwenden Sie eine private Arbeits Warteschlange. Um eine private Arbeits Warteschlange zu erstellen, rufen Sie [**mfbelegcateworkqueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue)auf. Jede Pipeline Komponente, die e/a-Vorgänge ausführt, sollte aus demselben Grund verhindern, dass e/a-Aufrufe blockiert werden. Die [**IMF Bytestream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) -Schnittstelle stellt eine nützliche Abstraktion für asynchrone Datei-e/a dar.

### <a name="implementing-the-beginend-pattern"></a>Implementieren von BEGIN. ../End... Bau

Wie unter [Aufrufen von asynchronen Methoden](calling-asynchronous-methods.md)beschrieben, verwenden asynchrone Methoden in Media Foundation häufig den **Anfang...** / **Ende...** Bau. In diesem Muster verwendet ein asynchroner Vorgang zwei Methoden mit Signaturen, die den folgenden ähneln:

``` syntax
// Starts the asynchronous operation.
HRESULT BeginX(IMFAsyncCallback *pCallback, IUnknown *punkState);

// Completes the asynchronous operation. 
// Call this method from inside the caller's Invoke method.
HRESULT EndX(IMFAsyncResult *pResult);
```

Damit die Methode wirklich asynchron ist, muss die Implementierung von **BeginX** die tatsächliche Arbeit in einem anderen Thread durchführen. An dieser Stelle kommen Arbeits Warteschlangen ins Spiel. In den folgenden *Schritten ist der* Aufrufer der Code, der **BeginX** und **EndX** aufruft. Dabei kann es sich um eine Anwendung oder die Media Foundation Pipeline handeln. Bei der *Komponente* handelt es sich um den Code, der **BeginX** und **EndX** implementiert.

1.  Der Aufrufer ruft **BEGIN...** auf und übergibt einen Zeiger auf die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle des Aufrufers.
2.  Die Komponente erstellt ein neues asynchrones Ergebnis Objekt. Dieses Objekt speichert die Rückruf Schnittstelle und das Zustands Objekt des Aufrufers. In der Regel speichert Sie auch alle privaten Zustandsinformationen, die die Komponente benötigt, um den Vorgang abzuschließen. Das Ergebnis Objekt aus diesem Schritt wird im nächsten Diagramm als "Ergebnis 1" bezeichnet.
3.  Die Komponente erstellt ein zweites Ergebnis Objekt. Dieses Ergebnis Objekt speichert zwei Zeiger: das erste Ergebnis Objekt und die Rückruf Schnittstelle des aufgerufenen. Dieses Ergebnis Objekt wird im nächsten Diagramm als "Ergebnis 2" bezeichnet.
4.  Die Komponente ruft [**mfputworkitemex**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) auf, um eine neue Arbeitsaufgabe in die Warteschlange zu stellen.
5.  In der [**Aufruf**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Methode führt die Komponente die asynchrone Arbeit aus.
6.  Die Komponente ruft [**mfinvokecallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) auf, um die Rückruf Methode des Aufrufers aufzurufen.
7.  Der Aufrufer ruft die **EndX** -Methode auf.

![Diagramm, das zeigt, wie ein Objekt das Begin/End-Muster implementiert](images/workqueues03.png)

## <a name="asynchronous-method-example"></a>Beispiel für eine asynchrone Methode

Um diese Erörterung zu veranschaulichen, verwenden wir ein Beispiel mit einem Beispiel. Stellen Sie sich eine asynchrone Methode zum Berechnen einer Quadratwurzel vor:


```C++
    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);
```



Der *x* -Parameter von `BeginSquareRoot` ist der Wert, dessen Quadratwurzel berechnet wird. Die Quadratwurzel wird im *PVal* -Parameter von zurückgegeben `EndSquareRoot` .

Hier ist die Deklaration einer Klasse, die diese beiden Methoden implementiert:


```C++
class SqrRoot : public IMFAsyncCallback
{
    LONG    m_cRef;
    double  m_sqrt;

    HRESULT DoCalculateSquareRoot(AsyncOp *pOp);

public:

    SqrRoot() : m_cRef(1)
    {

    }

    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(SqrRoot, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    // IMFAsyncCallback methods.

    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;  
    }
    // Invoke is where the work is performed.
    STDMETHODIMP Invoke(IMFAsyncResult* pResult);
};
```



Die `SqrRoot` Klasse implementiert [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , sodass Sie die Quadratwurzel Operation in einer Arbeits Warteschlange platzieren kann. Die- `DoCalculateSquareRoot` Methode ist die private-Klassenmethode, die die Quadratwurzel berechnet. Diese Methode wird vom Arbeitswarteschlangen-Thread aufgerufen.

Zunächst benötigen wir eine Möglichkeit, den Wert von *x* zu speichern, damit Sie abgerufen werden kann, wenn der Arbeits Warteschlangen Thread aufruft `SqrRoot::Invoke` . Im folgenden finden Sie eine einfache Klasse, in der die Informationen gespeichert werden:


```C++
class AsyncOp : public IUnknown
{
    LONG    m_cRef;

public:

    double  m_value;

    AsyncOp(double val) : m_cRef(1), m_value(val) { }

    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(AsyncOp, IUnknown),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }
};
```



Diese Klasse implementiert **IUnknown** , damit Sie in einem Ergebnis Objekt gespeichert werden kann.

Der folgende Code implementiert die- `BeginSquareRoot` Methode:


```C++
HRESULT SqrRoot::BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState)
{
    AsyncOp *pOp = new (std::nothrow) AsyncOp(x);
    if (pOp == NULL)
    {
        return E_OUTOFMEMORY;
    }

    IMFAsyncResult *pResult = NULL;

    // Create the inner result object. This object contains pointers to:
    // 
    //   1. The caller's callback interface and state object. 
    //   2. The AsyncOp object, which contains the operation data.
    //

    HRESULT hr = MFCreateAsyncResult(pOp, pCB, pState, &pResult);

    if (SUCCEEDED(hr))
    {
        // Queue a work item. The work item contains pointers to:
        // 
        // 1. The callback interface of the SqrRoot object.
        // 2. The inner result object.

        hr = MFPutWorkItem(MFASYNC_CALLBACK_QUEUE_STANDARD, this, pResult);

        pResult->Release();
    }

    return hr;
}
```



Im Code werden folgende Schritte ausgeführt:

1.  Erstellt eine neue Instanz der- `AsyncOp` Klasse, die den Wert von *x* enthalten soll.
2.  Ruft [**mfkreateasynkresult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) auf, um ein Ergebnis Objekt zu erstellen. Dieses Objekt enthält mehrere Zeiger:
    -   Ein Zeiger auf die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle des Aufrufers.
    -   Ein Zeiger auf das Zustands Objekt des Aufrufers (*pState*).
    -   Ein Zeiger auf das `AsyncOp`-Objekt.
3.  Ruft [**mfputworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) auf, um ein neues Arbeits Element in die Warteschlange zu stellen Dieser Befehl erstellt implizit ein äußeres Ergebnis Objekt, das die folgenden Zeiger enthält:
    -   Ein Zeiger auf die `SqrRoot` [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle des Objekts.
    -   Ein Zeiger auf das innere Ergebnis Objekt aus Schritt 2.

Der folgende Code implementiert die- `SqrRoot::Invoke` Methode:


```C++
// Invoke is called by the work queue. This is where the object performs the
// asynchronous operation.

STDMETHODIMP SqrRoot::Invoke(IMFAsyncResult* pResult)
{
    HRESULT hr = S_OK;

    IUnknown *pState = NULL;
    IUnknown *pUnk = NULL;
    IMFAsyncResult *pCallerResult = NULL;

    AsyncOp *pOp = NULL; 

    // Get the asynchronous result object for the application callback. 

    hr = pResult->GetState(&pState);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pState->QueryInterface(IID_PPV_ARGS(&pCallerResult));
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the object that holds the state information for the asynchronous method.
    hr = pCallerResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    pOp = static_cast<AsyncOp*>(pUnk);

    // Do the work.

    hr = DoCalculateSquareRoot(pOp);

done:
    // Signal the application.
    if (pCallerResult)
    {
        pCallerResult->SetStatus(hr);
        MFInvokeCallback(pCallerResult);
    }

    SafeRelease(&pState);
    SafeRelease(&pUnk);
    SafeRelease(&pCallerResult);
    return S_OK;
}
```



Diese Methode ruft das innere Ergebnis Objekt und das- `AsyncOp` Objekt ab. Anschließend wird das- `AsyncOp` Objekt an das-Objekt weitergeleitet `DoCalculateSquareRoot` . Schließlich ruft Sie [**imfasynkresult:: SetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-setstatus) auf, um den Statuscode festzulegen, und [**mfinvokecallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) , um die Rückruf Methode des Aufrufers aufzurufen.

Die- `DoCalculateSquareRoot` Methode erfüllt genau das, was Sie erwarten würden:


```C++
HRESULT SqrRoot::DoCalculateSquareRoot(AsyncOp *pOp)
{
    pOp->m_value = sqrt(pOp->m_value);

    return S_OK;
}
```



Wenn die Rückruf Methode des Aufrufers aufgerufen wird, liegt es in der Verantwortung des Aufrufers, die **End...** -Methode aufzurufen – in diesem Fall `EndSquareRoot` . Der `EndSquareRoot` gibt an, wie der Aufrufer das Ergebnis des asynchronen Vorgangs abruft, der in diesem Beispiel die berechnete Quadratwurzel ist. Diese Informationen werden im Ergebnis Objekt gespeichert:


```C++
HRESULT SqrRoot::EndSquareRoot(IMFAsyncResult *pResult, double *pVal)
{
    *pVal = 0;

    IUnknown *pUnk = NULL;

    HRESULT hr = pResult->GetStatus();

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    AsyncOp *pOp = static_cast<AsyncOp*>(pUnk);

    // Get the result.
    *pVal = pOp->m_value;

done:
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="operation-queues"></a>Vorgangs Warteschlangen

Bisher wurde angenommen, dass ein asynchroner Vorgang jederzeit ausgeführt werden kann, unabhängig vom aktuellen Zustand des Objekts. Nehmen Sie beispielsweise an, was geschieht, wenn eine Anwendung aufruft, `BeginSquareRoot` während ein früherer Aufruf derselben Methode noch aussteht. Die- `SqrRoot` Klasse kann die neue Arbeitsaufgabe in die Warteschlange stellen, bevor die vorherige Arbeitsaufgabe abgeschlossen ist. Arbeits Warteschlangen werden jedoch nicht garantiert, dass Arbeitselemente serialisiert werden. Beachten Sie, dass eine Arbeits Warteschlange mehr als einen Thread zum Verteilen von Arbeits Elementen verwenden kann. In einer Multithread-Umgebung kann ein Arbeits Element aufgerufen werden, bevor das vorherige abgeschlossen ist. Arbeitselemente können sogar außerhalb der Reihenfolge aufgerufen werden, wenn ein Kontextwechsel unmittelbar vor dem Aufrufen des Rückrufs stattfindet.

Aus diesem Grund ist es für das Objekt zuständig, Vorgänge für sich selbst zu serialisieren, wenn dies erforderlich ist. Anders ausgedrückt: Wenn das-Objekt erfordert *, dass der* Vorgang *a* abgeschlossen ist, bevor der Vorgang *b* gestartet werden kann, darf das Objekt eine Arbeitsaufgabe nicht in die Warteschlange stellen, bis der Vorgang *a* abgeschlossen ist. Ein Objekt kann diese Anforderung erfüllen, indem es eine eigene Warteschlange für ausstehende Vorgänge hat. Wenn eine asynchrone Methode für das-Objekt aufgerufen wird, stellt das-Objekt die Anforderung in eine eigene Warteschlange. Wenn jeder asynchrone Vorgang abgeschlossen ist, ruft das-Objekt die nächste Anforderung aus der Warteschlange ab. Das [MPEG1Source](mpeg1source-sample.md) -Beispiel zeigt, wie eine solche Warteschlange implementiert wird.

Eine einzelne Methode kann mehrere asynchrone Vorgänge umfassen, insbesondere dann, wenn e/a-Aufrufe verwendet werden. Wenn Sie asynchrone Methoden implementieren, sollten Sie sich sorgfältig mit den Serialisierungsanforderungen beschäftigen. Ist es z. b. für das-Objekt zulässig, einen neuen Vorgang zu starten, während eine vorherige e/a-Anforderung noch aussteht? Wenn der neue Vorgang den internen Zustand des Objekts ändert, was geschieht, wenn eine vorherige e/a-Anforderung abgeschlossen ist und Daten zurückgibt, die möglicherweise veraltet sind? Ein gutes Zustandsdiagramm kann bei der Identifizierung der gültigen Zustandsübergänge helfen.

## <a name="cross-thread-and-cross-process-considerations"></a>Thread übergreifende und prozessübergreifende Überlegungen

Arbeits Warteschlangen verwenden kein COM-Marshalling zum Mars Hallen von Schnittstellen Zeigern über Thread Grenzen hinweg. Daher wird auch dann, wenn ein Objekt als Apartment Thread registriert ist oder der Anwendungs Thread ein Single Thread-Apartment (STA) eingegeben hat, [**imfasynccallback-Rückrufe**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) von einem anderen Thread aufgerufen. In jedem Fall sollten alle Media Foundation Pipeline Komponenten das "beide" Threading Modell verwenden.

Einige Schnittstellen in Media Foundation definieren Remote Versionen einiger asynchroner Methoden. Wenn eine dieser Methoden über Prozess Grenzen hinweg aufgerufen wird, ruft die Media Foundation Proxy-/Stub-DLL die Remote Version der-Methode auf, die das benutzerdefinierte Marshalling der Methoden Parameter ausführt. Im Remote Prozess übersetzt der Stub den Rückruf wieder in die lokale Methode des Objekts. Dieser Prozess ist sowohl für die Anwendung als auch für das Remote Objekt transparent. Diese benutzerdefinierten marshallingmethoden werden primär für Objekte bereitgestellt, die in den geschützten Medien Pfad (PMP) geladen werden. Weitere Informationen zum PMP finden Sie unter [geschützter Medien Pfad](protected-media-path.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Asynchrone Rückruf Methoden](asynchronous-callback-methods.md)
</dt> <dt>

[Arbeits Warteschlangen](work-queues.md)
</dt> </dl>

 

 



