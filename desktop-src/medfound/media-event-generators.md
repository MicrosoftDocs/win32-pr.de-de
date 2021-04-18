---
description: Medienereignis Generatoren
ms.assetid: 2e003ad4-9fcb-4834-a335-e4969ffd3a00
title: Medienereignis Generatoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 125bf165740b0260f9131e0df8af420c8a669d97
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354912"
---
# <a name="media-event-generators"></a>Medienereignis Generatoren

Media Foundation bietet eine konsistente Methode zum Senden von Ereignissen durch-Objekte. Ein Objekt kann Ereignisse verwenden, um den Abschluss einer asynchronen Methode zu signalisieren oder um die Anwendung über eine Änderung des Objekt Zustands zu benachrichtigen.

Wenn ein Objekt Ereignisse sendet, wird die [**IMF mediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle verfügbar gemacht. Wenn das-Objekt ein neues Ereignis sendet, wird das-Ereignis in eine Warteschlange eingefügt. Die Anwendung kann das nächste Ereignis aus der Warteschlange anfordern, indem Sie eine der folgenden Methoden aufrufen:

-   [**IMF mediaeventgenerator:: GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent)

-   [**IMF mediaeventgenerator:: begingetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)

Die [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) -Methode ist synchron. Wenn ein Ereignis bereits in der Warteschlange vorhanden ist, wird die Methode sofort zurückgegeben. Wenn in der Warteschlange kein Ereignis vorhanden ist, schlägt die Methode entweder sofort fehl oder blockiert, bis das nächste Ereignis in die Warteschlange eingereiht wird, je nachdem, welches Flag Sie an **GetEvent** übergeben.

Die [**begingetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) -Methode ist asynchron, sodass Sie niemals blockiert wird. Diese Methode nimmt einen Zeiger auf die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle an, die von der Anwendung implementiert werden muss. Wenn der Rückruf aufgerufen wird, ruft die Anwendung [**imfmediaeventgenerator:: endgetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) auf, um das Ereignis aus der Warteschlange zu erhalten. Weitere Informationen zu **imfasynccallback** finden Sie unter [asynchrone Rückruf Methoden](asynchronous-callback-methods.md).

Ereignisse werden durch die [**IMF Media Event**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) -Schnittstelle dargestellt. Diese Schnittstelle verfügt über die folgenden Methoden:

-   [**GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype): Ruft den Ereignistyp ab. Der Ereignistyp gibt an, was geschehen ist, um das Ereignis auslöst.

-   [**GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus): Ruft einen **HRESULT** -Wert ab, der angibt, ob der Vorgang, der das Ereignis ausgelöst hat, erfolgreich war. Wenn ein Vorgang asynchron fehlschlägt, gibt **GetStatus** einen Fehlercode zurück.

-   [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue): Ruft eine **PROPVARIANT** ab, die Ereignisdaten enthält. Die Ereignisdaten hängen vom Ereignistyp ab. Für einige Ereignisse sind keine Daten vorhanden.

-   [**Getextendedtype**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype): Ruft eine **GUID** ab. Diese Methode gilt für das [meextendedtype-Ereignis](meextendedtype.md)und bietet eine Möglichkeit, benutzerdefinierte Ereignisse zu definieren.

Außerdem erbt die [**imbomediaevent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) -Schnittstelle die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle. Einige Ereignisse enthalten zusätzliche Informationen als Attribute.

Eine Liste der Ereignis Typen und der zugehörigen Daten und Attribute finden Sie unter [Media Foundation-Ereignisse](media-foundation-events.md).

## <a name="implementing-imfmediaeventgenerator"></a>Implementieren von IMF mediaeventgenerator

Wenn Sie eine Plug-in-Komponente für Media Foundation schreiben, z. b. eine benutzerdefinierte Medienquelle oder eine Medien Senke, müssen Sie möglicherweise [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)implementieren. Um dies zu vereinfachen, stellt Media Foundation ein Hilfsobjekt bereit, das eine Ereignis Warteschlange implementiert. Erstellen Sie die Ereignis Warteschlange, indem Sie die [**mfcreateeventqueue**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue) -Funktion aufrufen. Die Ereignis Warteschlange macht die [**IMF mediaeventqueue**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue) -Schnittstelle verfügbar. In der Implementierung der **imfmediaeventgenerator** -Methoden des-Objekts können Sie die entsprechende-Methode für die Ereignis Warteschlange aufzurufen.

Das Ereignis Warteschlangen Objekt ist Thread sicher. Behalten Sie beim Aufrufen von [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-getevent) und [**queueevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent)niemals dasselbe kritische Abschnitts Objekt bei, da **GetEvent** ggf. unbegrenzt auf [**queueevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent)wartet. Wenn Sie für beide Methoden denselben kritischen Abschnitt aufbewahren, wird ein Deadlock verursacht.

Bevor Sie die Ereignis Warteschlange freigeben, wenden Sie [**imfmediaeventqueue:: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) an, um die Ressourcen freizugeben, die das Objekt enthält.

Wenn das Objekt ein Ereignis abrufen muss, rufen Sie eine der folgenden Methoden für die Ereignis Warteschlange auf:

-   [**IMF mediaeventqueue:: queueevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent)

-   [**IMF mediaeventqueue:: queueeventparamvar**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamvar)

-   [**IMF mediaeventqueue:: queueeventparamunk**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamunk)

Diese Methoden platzieren ein neues Ereignis in der Warteschlange und signalisieren allen Aufrufern, die auf das nächste Ereignis warten.

Der folgende Code zeigt eine Klasse, die [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) mithilfe dieses Hilfsobjekts implementiert. Diese Klasse definiert eine öffentliche **Shutdown** -Methode, die die Ereignis Warteschlange herunterfährt und den Ereignis Warteschlangen Zeiger freigibt. Dieses Verhalten ist typisch für Medienquellen und Medien senken, die immer über eine **Shutdown** -Methode verfügen.


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

 

 



