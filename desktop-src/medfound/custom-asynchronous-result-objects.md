---
description: Benutzerdefinierte asynchrone Ergebnisobjekte
ms.assetid: 78cef367-b007-46d5-bb7f-2b3f7eed9926
title: Benutzerdefinierte asynchrone Ergebnisobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7212152de737a0af8e290b2c837b40cd4ad68840a49df79db148b4691068678b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742926"
---
# <a name="custom-asynchronous-result-objects"></a>Benutzerdefinierte asynchrone Ergebnisobjekte

In diesem Thema wird beschrieben, wie [**dieASYNCAsyncResult-Schnittstelle implementiert**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) wird.

Es ist selten, dass Sie eine benutzerdefinierte Implementierung [**derASYNCAsyncResult-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) schreiben müssen. In fast allen Fällen ist die Standardimplementierung Media Foundation ausreichend. (Diese Implementierung wird von der [**MFCreateAsyncResult-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) zurückgegeben.) Wenn Sie jedoch eine benutzerdefinierte Implementierung schreiben, müssen Sie einige Probleme beachten.

Zunächst muss Ihre Implementierung die [**MFASYNCRESULT-Struktur**](/windows/win32/api/mfapi/ns-mfapi-mfasyncresult) erben. Die Media Foundation Arbeitswarteschlangen verwenden diese Struktur intern, um den Vorgang zu senden. Initialisieren Sie alle Strukturmitglieder mit Ausnahme des **pCallback-Members,** der einen Zeiger auf die Rückrufschnittstelle des Aufrufers enthält, auf 0 (null).

Zweitens sollte Ihr Objekt [**MFLockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mflockplatform) in seinem Konstruktor aufrufen, um die Media Foundation sperren. Rufen [**Sie MFUnlockPlatform auf,**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform) um die Plattform zu entsperren. Diese Funktionen verhindern, dass die Plattform heruntergefahren wird, bevor das Objekt zerstört wird. Weitere Informationen finden Sie unter [Arbeitswarteschlangen](work-queues.md).

Der folgende Code zeigt eine grundlegende Implementierung [**derASYNCAsyncResult-Schnittstelle.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) Wie gezeigt, bietet dieser Code keine zusätzlichen Features, die über die Standardimplementierung Media Foundation hinausgehen.


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

[Arbeitswarteschlangen](work-queues.md)
</dt> <dt>

[Asynchrone Rückrufmethoden](asynchronous-callback-methods.md)
</dt> </dl>

 

 



