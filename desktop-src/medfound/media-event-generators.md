---
description: Medienereignis-Generatoren
ms.assetid: 2e003ad4-9fcb-4834-a335-e4969ffd3a00
title: Medienereignis-Generatoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24bd37b347fb06f97448b43241a1da40123195b63b9191b97581be60d7378ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724160"
---
# <a name="media-event-generators"></a>Medienereignis-Generatoren

Media Foundation stellt eine konsistente Möglichkeit für Objekte zum Senden von Ereignissen dar. Ein Objekt kann Ereignisse verwenden, um den Abschluss einer asynchronen Methode zu signalisieren oder die Anwendung über eine Änderung des Zustands des Objekts zu benachrichtigen.

Wenn ein Objekt Ereignisse sendet, macht es die [**INTERFACE FÜR DENTMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) verfügbar. Jedes Mal, wenn das -Objekt ein neues Ereignis sendet, wird das Ereignis in eine Warteschlange platziert. Die Anwendung kann das nächste Ereignis aus der Warteschlange anfordern, indem sie eine der folgenden Methoden aufruft:

-   [**BESCHRIFTUNGMediaEventGenerator::GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent)

-   [**BESCHRIFTUNGMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)

Die [**GetEvent-Methode**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) ist synchron. Wenn sich ein Ereignis bereits in der Warteschlange befindet, gibt die Methode sofort zurück. Wenn kein Ereignis in der Warteschlange vorkommt, schlägt die Methode entweder sofort fehl oder blockiert, bis das nächste Ereignis in die Warteschlange eingereiht wird. Dies hängt davon ab, welches Flag Sie an **GetEvent übergeben.**

Die [**BeginGetEvent-Methode**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) ist asynchron und wird daher nie blockiert. Diese Methode verwendet einen Zeiger auf [**dieASYNCCallback-Schnittstelle,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) die die Anwendung implementieren muss. Wenn der Rückruf aufgerufen wird, ruft die Anwendung [**DENTMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) auf, um das Ereignis aus der Warteschlange zu erhalten. Weitere Informationen zu **ASYNCHRONOUSAsyncCallback finden** Sie unter [Asynchrone Rückrufmethoden](asynchronous-callback-methods.md).

Ereignisse werden durch die [**BENUTZEROBERFLÄCHEMediaEvent-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) dargestellt. Diese Schnittstelle verfügt über die folgenden Methoden:

-   [**GetType:**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype)Ruft den Ereignistyp ab. Der Ereignistyp gibt an, was passiert ist, um das Ereignis auszulösen.

-   [**GetStatus:**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus)Ruft einen **HRESULT-Wert ab,** der angibt, ob der Vorgang, der das Ereignis ausgelöst hat, erfolgreich war. Wenn ein Vorgang asynchron fehlschlägt, **gibt GetStatus** einen Fehlercode zurück.

-   [**GetValue:**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue)Ruft eine **PROPVARIANT ab,** die Ereignisdaten enthält. Die Ereignisdaten hängen vom Ereignistyp ab. Einige Ereignisse verfügen nicht über Daten.

-   [**GetExtendedType:**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype)Ruft eine **GUID ab.** Diese Methode gilt für das [MEExtendedType-Ereignis](meextendedtype.md)und bietet eine Möglichkeit, benutzerdefinierte Ereignisse zu definieren.

Die [**INTERFACESMediaEvent-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) erbt auch die [**SCHNITTSTELLE ATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Einige Ereignisse enthalten zusätzliche Informationen als Attribute.

Eine Liste der Ereignistypen und der zugehörigen Daten und Attribute finden Sie unter [Media Foundation Ereignisse.](media-foundation-events.md)

## <a name="implementing-imfmediaeventgenerator"></a>Implementieren von ZUNTMediaEventGenerator

Wenn Sie eine Plug-In-Komponente für eine Media Foundation schreiben, z. B. eine benutzerdefinierte Medienquelle oder Mediensenke, müssen Sie [**möglicherweise DENTMEDIAEventGenerator implementieren.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) Um dies zu vereinfachen, Media Foundation ein Hilfsobjekt, das eine Ereigniswarteschlange implementiert. Erstellen Sie die Ereigniswarteschlange, indem Sie die [**MFCreateEventQueue-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue) aufrufen. Die Ereigniswarteschlange macht die [**BENUTZEROBERFLÄCHEMediaEventQueue-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue) verfügbar. Rufen Sie in der Implementierung der **METHODEN DESTMEDIAEventGenerator-Objekts** die entsprechende Methode in der Ereigniswarteschlange auf.

Das Ereigniswarteschlangenobjekt ist threadsicher. Halten Sie nie dasselbe kritische Abschnittsobjekt beim Aufrufen [**von GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-getevent) und [**QueueEvent,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent)da **GetEvent** das warten auf QueueEvent möglicherweise unbegrenzt [**blockiert.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent) Wenn Sie denselben kritischen Abschnitt für beide Methoden verwenden, verursacht dies einen Deadlock.

Rufen Sie vor dem Freigeben der Ereigniswarteschlange [**DIE WarteschlangeNMEDIAEventQueue::Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) auf, um die Ressourcen frei zu geben, die das Objekt enthält.

Wenn Ihr Objekt ein Ereignis ausrufen muss, rufen Sie eine der folgenden Methoden für die Ereigniswarteschlange auf:

-   [**DURCHSCHN.MediaEventQueue::QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent)

-   [**BEREINIGENMediaEventQueue::QueueEventParamVar**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamvar)

-   [**BEREINIGENMediaEventQueue::QueueEventParamUnk**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamunk)

Diese Methoden setzen ein neues Ereignis in die Warteschlange und signalisieren jedem Aufrufer, der auf das nächste Ereignis wartet.

Der folgende Code zeigt eine Klasse, die MITHILFE dieses Hilfsobjekts [**DENTMEDIAEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) implementiert. Diese Klasse definiert eine öffentliche **Shutdown-Methode,** die die Ereigniswarteschlange heruntergefahren und den Ereigniswarteschlangenzeiger freilässt. Dieses Verhalten ist typisch für Medienquellen und Mediensenken, die immer über eine **Shutdown-Methode** verfügen.


```C++
class MyObject : public IMFMediaEventGenerator
{
private:
    long                m_nRefCount;    // Reference count.
    CRITICAL_SECTION    m_critSec;      // Critical section.
    IMFMediaEventQueue *m_pQueue;       // Event queue.
    BOOL                m_bShutdown;    // Is the object shut down?

    // CheckShutdown: Returns MF_E_SHUTDOWN if the object was shut down.
    HRESULT CheckShutdown() const 
    {
        return (m_bShutdown? MF_E_SHUTDOWN : S_OK);
    }

public:
    MyObject(HRESULT &hr) : m_nRefCount(0), m_pQueue(NULL), m_bShutdown(FALSE)
    {
        InitializeCriticalSection(&m_critSec);
        
        // Create the event queue.
        hr = MFCreateEventQueue(&m_pQueue);
    }

    // Shutdown: Shuts down this object.
    HRESULT Shutdown()
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            // Shut down the event queue.
            if (m_pQueue)
            {
                hr = m_pQueue->Shutdown();
            }

            // Release the event queue.
            SAFE_RELEASE(m_pQueue);
            // Release any other objects owned by the class (not shown).

            // Set the shutdown flag.
            m_bShutdown = TRUE;
        }

        LeaveCriticalSection(&m_critSec);
        return hr;
    }

    // TODO: Implement IUnknown (not shown).
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);

    // IMFMediaEventGenerator::BeginGetEvent
    STDMETHODIMP BeginGetEvent(IMFAsyncCallback* pCallback, IUnknown* pState)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->BeginGetEvent(pCallback, pState);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;    
    }

    // IMFMediaEventGenerator::EndGetEvent
    STDMETHODIMP EndGetEvent(IMFAsyncResult* pResult, IMFMediaEvent** ppEvent)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->EndGetEvent(pResult, ppEvent);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;    
    }

    // IMFMediaEventGenerator::GetEvent
    STDMETHODIMP GetEvent(DWORD dwFlags, IMFMediaEvent** ppEvent)
    {
        // Because GetEvent can block indefinitely, it requires
        // a slightly different locking strategy.
        IMFMediaEventQueue *pQueue = NULL;

        // Hold lock.
        EnterCriticalSection(&m_critSec);

        // Check shutdown
        HRESULT hr = CheckShutdown();

        // Store the pointer in a local variable, so that another thread
        // does not release it after we leave the critical section.
        if (SUCCEEDED(hr))
        {
            pQueue = m_pQueue;
            pQueue->AddRef();
        }

        // Release the lock.
        LeaveCriticalSection(&m_critSec);

        if (SUCCEEDED(hr))
        {
            hr = pQueue->GetEvent(dwFlags, ppEvent);
        }

        SAFE_RELEASE(pQueue);
        return hr;
    }

    // IMFMediaEventGenerator::QueueEvent
    STDMETHODIMP QueueEvent(
        MediaEventType met, REFGUID extendedType, 
        HRESULT hrStatus, const PROPVARIANT* pvValue)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->QueueEventParamVar(
                met, extendedType, hrStatus, pvValue);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;
    }

private:

    // The destructor is private. The caller must call Release.
    virtual ~MyObject()
    {
        assert(m_bShutdown);
        assert(m_nRefCount == 0);
    }
};
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Plattform-APIs](media-foundation-platform-apis.md)
</dt> </dl>

 

 



