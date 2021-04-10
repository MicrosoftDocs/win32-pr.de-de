---
description: Benutzerdefinierte asynchrone Ergebnis Objekte
ms.assetid: 78cef367-b007-46d5-bb7f-2b3f7eed9926
title: Benutzerdefinierte asynchrone Ergebnis Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de5a0109b47255bc14fcccafbbb09c419848b5a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214329"
---
# <a name="custom-asynchronous-result-objects"></a>Benutzerdefinierte asynchrone Ergebnis Objekte

In diesem Thema wird beschrieben, wie die [**imfasynkresult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) -Schnittstelle implementiert wird.

Es ist selten, dass Sie eine benutzerdefinierte Implementierung der [**imfasynkresult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) -Schnittstelle schreiben müssen. In fast allen Fällen ist die Standard Media Foundation Implementierung ausreichend. (Diese Implementierung wird von der MF-Funktion " [**MF**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) -Funktion" zurückgegeben.) Wenn Sie jedoch eine benutzerdefinierte Implementierung schreiben, müssen Sie einige Punkte beachten.

Zuerst muss Ihre Implementierung die [**mfasynkresult**](/windows/win32/api/mfapi/ns-mfapi-mfasyncresult) -Struktur erben. Die Media Foundation Arbeits Warteschlangen verwenden diese Struktur intern, um den Vorgang zu verteilen. Initialisieren Sie alle Strukturmember mit Ausnahme des **pCallback** -Members, der einen Zeiger auf die Rückruf Schnittstelle des Aufrufers enthält.

Zweitens sollte Ihr Objekt [**mflockplatform**](/windows/desktop/api/mfapi/nf-mfapi-mflockplatform) in seinem Konstruktor anrufen, um die Media Foundation Plattform zu sperren. Zum Entsperren der Plattform muss [**mfunlockplatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform) aufgerufen werden. Diese Funktionen tragen dazu bei, das Herunterfahren der Plattform zu verhindern, bevor das Objekt zerstört wird. Weitere Informationen finden Sie unter [Arbeits Warteschlangen](work-queues.md).

Der folgende Code zeigt eine grundlegende Implementierung der [**imfasynkresult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) -Schnittstelle. Wie gezeigt, stellt dieser Code keine weiteren Funktionen bereit, die über die Standard Media Foundation Implementierung hinausgehen.


```C++
///////////////////////////////////////////////////////////////////////////////
//  CMyAsyncResult
//
//  Custom implementation of IMFAsyncResult. All implementations of this 
//  interface must inherit the MFASYNCRESULT structure.
// 
///////////////////////////////////////////////////////////////////////////////

class CMyAsyncResult : public MFASYNCRESULT
{
protected:
    LONG        m_cRef;             // Reference count.
    BOOL        m_bLockPlatform;    // Locked the Media Foundation platform?
    IUnknown*   m_pState;           // Caller's state object. 
    IUnknown*   m_pObject;  // Optional object. See IMFAsyncResult::GetObject.

    // Constructor. 
    CMyAsyncResult(IMFAsyncCallback *pCallback, IUnknown *pState, HRESULT *phr) :
        m_cRef(1),
        m_bLockPlatform(FALSE),
        m_pObject(NULL),
        m_pState(pState)
    {
        *phr = MFLockPlatform();

        m_bLockPlatform = TRUE;

        // Initialize the MFASYNCRESULT members.
        ZeroMemory(&this->overlapped, sizeof(OVERLAPPED));
        hrStatusResult = S_OK;
        dwBytesTransferred = 0;
        hEvent = NULL;

        this->pCallback = pCallback;
        if (pCallback)
        {
            this->pCallback->AddRef();
        }

        if (m_pState)
        {
            m_pState->AddRef();
        }
    }

    virtual ~CMyAsyncResult()
    {
        SafeRelease(&pCallback);
        SafeRelease(&m_pState);
        SafeRelease(&m_pObject);

        if (m_bLockPlatform)
        {
            MFUnlockPlatform();
        }
    }

public:
    // Static method to create an instance of this object.
    static HRESULT CreateInstance(
        IMFAsyncCallback *pCallback,    // Callback to invoke.
        IUnknown *pState,               // Optional state object.
        CMyAsyncResult **ppResult       // Receives a pointer to the object.
        )
    {
        HRESULT hr = S_OK;

        *ppResult = NULL;

        CMyAsyncResult *pResult = 
            new (std::nothrow) CMyAsyncResult(pCallback, pState, &hr);

        if (pResult == NULL)
        {
            return E_OUTOFMEMORY;
        }
        if (FAILED(hr))
        {
            delete pResult;
            return hr;
        }

        // If the callback is NULL, create an event that will be signaled.
        if (pCallback == NULL)
        {
            pResult->hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
            if (pResult->hEvent == NULL)
            {
                hr = HRESULT_FROM_WIN32(GetLastError());
            }
        }

        if (SUCCEEDED(hr))
        {
            *ppResult = pResult;  // Return the pointer to the caller.
        }
        else
        {
            pResult->Release();
        }
        return hr;
    }

    // SetObject: Sets the optional result object. 
    // (This method is not part of the interface.)
    HRESULT SetObject(IUnknown *pObject)
    {
        SafeRelease(&m_pObject);
        m_pObject = pObject;
        if (pObject)
        {
            m_pObject->AddRef();
        }
        return S_OK;
    }

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CMyAsyncResult, IMFAsyncResult),
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
    
    // IMFAsyncResult methods.
    STDMETHODIMP GetState(IUnknown** ppunkState)
    {
        if (ppunkState == NULL)
        {
            return E_POINTER;
        }

        *ppunkState = m_pState;
        if (m_pState)
        {
            (*ppunkState)->AddRef();
        }

        return S_OK;
    }

    STDMETHODIMP GetStatus( void)
    {
        return hrStatusResult;
    }

    STDMETHODIMP STDMETHODCALLTYPE SetStatus(HRESULT hrStatus)
    {
        hrStatusResult = hrStatus;
        return S_OK;
    }

    STDMETHODIMP GetObject(IUnknown **ppObject)
    {
        if (ppObject == NULL)
        {
            return E_POINTER;
        }

        *ppObject = m_pObject;
        if (m_pObject)
        {
            (*ppObject)->AddRef();
        }
        return S_OK;
    }

    IUnknown* STDMETHODCALLTYPE GetStateNoAddRef()
    {
        return m_pState;  // Warning! Can be NULL. 
    }
};
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeits Warteschlangen](work-queues.md)
</dt> <dt>

[Asynchrone Rückruf Methoden](asynchronous-callback-methods.md)
</dt> </dl>

 

 



