---
description: In diesem Thema wird beschrieben, wie eine asynchrone Methode in Microsoft Media Foundation implementiert wird.
ms.assetid: cd94280d-7267-4d35-8333-aa4a5bd81b73
title: Schreiben einer asynchronen Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2efc9b38212f729dc840dde1ad1976a1b523103312710a0f316369637f3b66d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237013"
---
# <a name="writing-an-asynchronous-method"></a>Schreiben einer asynchronen Methode

In diesem Thema wird beschrieben, wie eine asynchrone Methode in Microsoft Media Foundation implementiert wird.

Asynchrone Methoden sind in der Media Foundation Pipeline ubiquitlich. Asynchrone Methoden erleichtern die Verteilung der Arbeit auf mehrere Threads. Es ist besonders wichtig, E/A asynchron auszuführen, damit das Lesen aus einer Datei oder einem Netzwerk den Rest der Pipeline nicht blockiert.

Wenn Sie eine Medienquelle oder Mediensenke schreiben, ist es wichtig, asynchrone Vorgänge ordnungsgemäß zu verarbeiten, da sich die Leistung Ihrer Komponente auf die gesamte Pipeline auswirkt.

> [!Note]  
> Media Foundation Transformationen (MFTs) verwenden standardmäßig synchrone Methoden.

 

### <a name="work-queues-for-asynchronous-operations"></a>Arbeitswarteschlangen für asynchrone Vorgänge

In Media Foundation besteht eine enge Beziehung zwischen [asynchronen Rückrufmethoden](asynchronous-callback-methods.md) und [Arbeitswarteschlangen.](work-queues.md) Eine Arbeitswarteschlange ist eine Abstraktion zum Verschieben von Arbeit aus dem Thread des Aufrufers in einen Arbeitsthread. Führen Sie die folgenden Schritte aus, um Aufgaben an einer Arbeitswarteschlange auszuführen:

1.  Implementieren Sie die [**INTERFACESAsyncCallback-Schnittstelle.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
2.  Rufen Sie [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) auf, um ein *Ergebnisobjekt* zu erstellen. Das Ergebnisobjekt macht DAS [**ASYNCRESULT verfügbar.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) Das Ergebnisobjekt enthält drei Zeiger:

    -   Ein Zeiger auf die [**POINTERAsyncCallback-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) des Aufrufers.
    -   Ein optionaler Zeiger auf ein Zustandsobjekt. Wenn angegeben, muss das Zustandsobjekt **IUnknown** implementieren.
    -   Ein optionaler Zeiger auf ein privates Objekt. Wenn angegeben, muss dieses Objekt auch **IUnknown** implementieren.

    Die letzten beiden Zeiger können **NULL** sein. Andernfalls verwenden Sie sie, um Informationen zum asynchronen Vorgang zu speichern.

3.  Rufen Sie [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) auf, um das Arbeitselement in die Warteschlange zu stellen.
4.  Der Arbeitswarteschlangenthread ruft Ihre [**METHODE VOMASYNCCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) auf.
5.  Führen Sie die Arbeit in Ihrer [**Invoke-Methode**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) aus. Der *pAsyncResult-Parameter* dieser Methode ist der [**POINTERAsyncResult-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) aus Schritt 2. Verwenden Sie diesen Zeiger, um das Zustandsobjekt und das private Objekt abzurufen:
    -   Rufen Sie ZUM Abrufen des Zustandsobjekts [**DEN AUFRUF VONASYNCResult::GetState auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate)
    -   Rufen Sie ZUM Abrufen des privaten Objekts [**DEN AUFRUF VONASYNCResult::GetObject auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject)

Alternativ können Sie die Schritte 2 und 3 kombinieren, indem Sie die [**MFPutWorkItem-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) aufrufen. Intern ruft diese Funktion [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) auf, um das Ergebnisobjekt zu erstellen.

Das folgende Diagramm zeigt die Beziehungen zwischen dem Aufrufer, dem Ergebnisobjekt, dem Zustandsobjekt und dem privaten Objekt.

![Diagramm eines asynchronen Ergebnisobjekts](images/workqueues01.png)

Das folgende Sequenzdiagramm zeigt, wie ein Objekt ein Arbeitselement in die Warteschlange einreiht. Wenn der Arbeitswarteschlangenthread [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)aufruft, führt das -Objekt den asynchronen Vorgang für diesen Thread aus.

![Diagramm, das zeigt, wie ein Objekt ein Arbeitselement in die Warteschlange einreiht](images/workqueues02.png)

Denken Sie daran, dass [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) von einem Thread aufgerufen wird, der sich im Besitz der Arbeitswarteschlange befindet. Die Implementierung von **Invoke** muss threadsicher sein. Wenn Sie außerdem die Plattformarbeitswarteschlange **(MFASYNC \_ CALLBACK \_ QUEUE \_ STANDARD)** verwenden, ist es wichtig, dass Sie den Thread nie blockieren, da dadurch die Verarbeitung von Daten für die gesamte Media Foundation Pipeline blockiert werden kann. Wenn Sie einen Vorgang ausführen müssen, der blockiert wird oder lange dauert, verwenden Sie eine private Arbeitswarteschlange. Um eine private Arbeitswarteschlange zu erstellen, rufen Sie [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue)auf. Jede Pipelinekomponente, die E/A-Vorgänge ausführt, sollte aus dem gleichen Grund verhindern, dass E/A-Aufrufe blockiert werden. Die [**INTERFACESByteStream-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) stellt eine nützliche Abstraktion für asynchrone Datei-E/A bereit.

### <a name="implementing-the-beginend-pattern"></a>Implementieren von Begin.../End... Muster

Wie unter [Aufrufen asynchroner Methoden](calling-asynchronous-methods.md)beschrieben, verwenden asynchrone Methoden in Media Foundation häufig **begin...** / **Ende...** Muster. In diesem Muster verwendet ein asynchroner Vorgang zwei Methoden mit Signaturen ähnlich der folgenden:

``` syntax
// Starts the asynchronous operation.
HRESULT BeginX(IMFAsyncCallback *pCallback, IUnknown *punkState);

// Completes the asynchronous operation. 
// Call this method from inside the caller's Invoke method.
HRESULT EndX(IMFAsyncResult *pResult);
```

Damit die Methode wirklich asynchron wird, muss die Implementierung von **BeginX** die eigentliche Arbeit an einem anderen Thread ausführen. Hier kommen Arbeitswarteschlangen ins Spiel. In den folgenden Schritten ist der *Aufrufer* der Code, der **BeginX** und **EndX** aufruft. Dies kann eine Anwendung oder die Media Foundation Pipeline sein. Die *-Komponente* ist der Code, der **BeginX** und **EndX** implementiert.

1.  Der Aufrufer ruft **Begin...** auf und übergibt einen Zeiger auf die [**POINTERAsyncCallback-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) des Aufrufers.
2.  Die Komponente erstellt ein neues asynchrones Ergebnisobjekt. Dieses Objekt speichert die Rückrufschnittstelle und das Zustandsobjekt des Aufrufers. In der Regel werden auch alle Informationen zum privaten Zustand gespeichert, die die Komponente zum Abschließen des Vorgangs benötigt. Das Ergebnisobjekt aus diesem Schritt wird im nächsten Diagramm als "Ergebnis 1" bezeichnet.
3.  Die Komponente erstellt ein zweites Ergebnisobjekt. Dieses Ergebnisobjekt speichert zwei Zeiger: das erste Ergebnisobjekt und die Rückrufschnittstelle des Aufgerufenen. Dieses Ergebnisobjekt wird im nächsten Diagramm als "Ergebnis 2" bezeichnet.
4.  Die Komponente ruft [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) auf, um ein neues Arbeitselement in die Warteschlange zu setzen.
5.  In der [**Invoke-Methode**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) führt die Komponente die asynchrone Arbeit aus.
6.  Die Komponente ruft [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) auf, um die Rückrufmethode des Aufrufers aufzurufen.
7.  Der Aufrufer ruft die **EndX-Methode** auf.

![Diagramm, das zeigt, wie ein Objekt das Begin/End-Muster implementiert](images/workqueues03.png)

## <a name="asynchronous-method-example"></a>Beispiel für eine asynchrone Methode

Zur Veranschaulichung dieser Diskussion verwenden wir ein konstruiertes Beispiel. Betrachten Sie eine asynchrone Methode zum Berechnen einer Quadratwurzel:


```C++
    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);
```



Der *x-Parameter* von `BeginSquareRoot` ist der Wert, dessen Quadratwurzel berechnet wird. Die Quadratwurzel wird im *pVal-Parameter* von `EndSquareRoot` zurückgegeben.

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



Die `SqrRoot` -Klasse implementiert [**DEN AsyncCallback-Vorgang SO,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) dass der Quadratstammvorgang in eine Arbeitswarteschlange gestellt werden kann. Die `DoCalculateSquareRoot` -Methode ist die private Klassenmethode, die die Quadratwurzel berechnet. Diese Methode wird aus dem Arbeitswarteschlangenthread aufgerufen.

Zunächst benötigen wir eine Möglichkeit, den Wert von *x* zu speichern, damit er abgerufen werden kann, wenn der Arbeitswarteschlangenthread `SqrRoot::Invoke` aufruft. Hier ist eine einfache Klasse, die die Informationen speichert:


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



Diese Klasse implementiert **IUnknown,** damit sie in einem Ergebnisobjekt gespeichert werden kann.

Der folgende Code implementiert die `BeginSquareRoot` -Methode:


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

1.  Erstellt eine neue Instanz der `AsyncOp` -Klasse, die den Wert von *x* enthalten soll.
2.  Ruft [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) auf, um ein Ergebnisobjekt zu erstellen. Dieses Objekt enthält mehrere Zeiger:
    -   Ein Zeiger auf die [**POINTERAsyncCallback-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) des Aufrufers.
    -   Ein Zeiger auf das Zustandsobjekt des Aufrufers (*pState*).
    -   Ein Zeiger auf das `AsyncOp`-Objekt.
3.  Ruft [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) auf, um ein neues Arbeitselement in die Warteschlange zu setzen. Dieser Aufruf erstellt implizit ein äußeres Ergebnisobjekt, das die folgenden Zeiger enthält:
    -   Ein Zeiger auf die `SqrRoot` [**POINTERAsyncCallback-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) des Objekts.
    -   Ein Zeiger auf das innere Ergebnisobjekt aus Schritt 2.

Der folgende Code implementiert die `SqrRoot::Invoke` -Methode:


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



Diese Methode ruft das innere Ergebnisobjekt und das `AsyncOp` -Objekt ab. Anschließend wird das `AsyncOp` -Objekt an `DoCalculateSquareRoot` übergeben. Schließlich ruft sie [**DEN STATUSCODE AUFASYNCResult::SetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-setstatus) und [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) auf, um die Rückrufmethode des Aufrufers aufzurufen.

Die `DoCalculateSquareRoot` -Methode führt genau das aus, was Sie erwarten würden:


```C++
HRESULT SqrRoot::DoCalculateSquareRoot(AsyncOp *pOp)
{
    pOp->m_value = sqrt(pOp->m_value);

    return S_OK;
}
```



Wenn die Rückrufmethode des Aufrufers aufgerufen wird, liegt es in der Verantwortung des Aufrufers, die **End...-Methode** aufzurufen, in diesem Fall `EndSquareRoot` . `EndSquareRoot`Der ruft das Ergebnis des asynchronen Vorgangs ab, bei dem es sich in diesem Beispiel um die berechnete Quadratwurzel handelt. Diese Informationen werden im Ergebnisobjekt gespeichert:


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



## <a name="operation-queues"></a>Vorgangswarteschlangen

Bisher wurde implizit davon ausgegangen, dass ein asynchroner Vorgang jederzeit ausgeführt werden kann, unabhängig vom aktuellen Zustand des Objekts. Stellen Sie sich beispielsweise vor, was geschieht, wenn eine Anwendung `BeginSquareRoot` aufruft, während ein früherer Aufruf derselben Methode noch aussteht. Die `SqrRoot` -Klasse kann das neue Arbeitselement in die Warteschlange einreihen, bevor das vorherige Arbeitselement abgeschlossen ist. Es ist jedoch nicht garantiert, dass Arbeitselemente von Arbeitswarteschlangen serialisiert werden. Denken Sie daran, dass eine Arbeitswarteschlange mehrere Threads zum Senden von Arbeitselementen verwenden kann. In einer Multithreadumgebung kann ein Arbeitselement aufgerufen werden, bevor das vorherige abgeschlossen ist. Arbeitselemente können sogar außerhalb der Reihenfolge aufgerufen werden, wenn ein Kontextwechsel erfolgt, kurz bevor der Rückruf aufgerufen wird.

Aus diesem Grund ist das Objekt für die Serialisierung von Vorgängen für sich selbst verantwortlich, falls dies erforderlich ist. Anders ausgedrückt: Wenn das Objekt erfordert, dass Vorgang *A* abgeschlossen ist, bevor Vorgang *B* gestartet werden kann, darf das Objekt ein Arbeitselement für *B* erst in die Warteschlange stellen, nachdem Vorgang *A* abgeschlossen wurde. Ein Objekt kann diese Anforderung erfüllen, indem es über eine eigene Warteschlange mit ausstehenden Vorgängen verfügt. Wenn eine asynchrone Methode für das Objekt aufgerufen wird, fügt das Objekt die Anforderung in eine eigene Warteschlange ein. Wenn jeder asynchrone Vorgang abgeschlossen ist, ruft das -Objekt die nächste Anforderung aus der Warteschlange ab. Das [MPEG1Source-Beispiel](mpeg1source-sample.md) zeigt ein Beispiel für die Implementierung einer solchen Warteschlange.

Eine einzelne Methode kann mehrere asynchrone Vorgänge umfassen, insbesondere wenn E/A-Aufrufe verwendet werden. Wenn Sie asynchrone Methoden implementieren, sollten Sie sorgfältig über serialisierungsanforderungen nachdenken. Ist es beispielsweise gültig, dass das -Objekt einen neuen Vorgang startet, während eine vorherige E/A-Anforderung noch aussteht? Wenn der neue Vorgang den internen Zustand des Objekts ändert, was geschieht, wenn eine vorherige E/A-Anforderung abgeschlossen wird und Daten zurückgibt, die möglicherweise veraltet sind? Ein gutes Zustandsdiagramm kann dabei helfen, die gültigen Zustandsübergänge zu identifizieren.

## <a name="cross-thread-and-cross-process-considerations"></a>Thread- und prozessübergreifende Überlegungen

Arbeitswarteschlangen verwenden kein COM-Marshalling, um Schnittstellenzeiger über Threadgrenzen hinweg zu marshallen. Selbst wenn ein Objekt als apartment-threaded registriert ist oder der Anwendungsthread in ein Singlethread-Apartment (STA) eingetreten ist, werden [**DAHER DIE RÜCKRUFE VONASYNCCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) von einem anderen Thread aufgerufen. In jedem Fall sollten alle Media Foundation Pipelinekomponenten das Threadingmodell "Beide" verwenden.

Einige Schnittstellen in Media Foundation definieren Remoteversionen einiger asynchroner Methoden. Wenn eine dieser Methoden über Prozessgrenzen hinweg aufgerufen wird, ruft die Media Foundation Proxy-/Stub-DLL die Remoteversion der Methode auf, die ein benutzerdefiniertes Marshalling der Methodenparameter ausführt. Im Remoteprozess übersetzt der Stub den Rückruf in die lokale Methode für das Objekt. Dieser Prozess ist sowohl für die Anwendung als auch für das Remoteobjekt transparent. Diese benutzerdefinierten Marshallingmethoden werden hauptsächlich für Objekte bereitgestellt, die im Geschützten Medienpfad (Protected Media Path, PMP) geladen werden. Weitere Informationen zum PMP finden Sie unter [Geschützter Medienpfad.](protected-media-path.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Asynchrone Rückrufmethoden](asynchronous-callback-methods.md)
</dt> <dt>

[Arbeitswarteschlangen](work-queues.md)
</dt> </dl>

 

 



