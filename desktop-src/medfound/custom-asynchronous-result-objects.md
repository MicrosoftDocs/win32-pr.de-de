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
# <a name="custom-asynchronous-result-objects"></a><span data-ttu-id="dc06f-103">Benutzerdefinierte asynchrone Ergebnis Objekte</span><span class="sxs-lookup"><span data-stu-id="dc06f-103">Custom Asynchronous Result Objects</span></span>

<span data-ttu-id="dc06f-104">In diesem Thema wird beschrieben, wie die [**imfasynkresult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) -Schnittstelle implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="dc06f-104">This topic describes how to implement the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span>

<span data-ttu-id="dc06f-105">Es ist selten, dass Sie eine benutzerdefinierte Implementierung der [**imfasynkresult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) -Schnittstelle schreiben müssen.</span><span class="sxs-lookup"><span data-stu-id="dc06f-105">It is rare that you will need to write a custom implementation of the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span> <span data-ttu-id="dc06f-106">In fast allen Fällen ist die Standard Media Foundation Implementierung ausreichend.</span><span class="sxs-lookup"><span data-stu-id="dc06f-106">In almost all cases, the standard Media Foundation implementation is sufficient.</span></span> <span data-ttu-id="dc06f-107">(Diese Implementierung wird von der MF-Funktion " [**MF**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) -Funktion" zurückgegeben.) Wenn Sie jedoch eine benutzerdefinierte Implementierung schreiben, müssen Sie einige Punkte beachten.</span><span class="sxs-lookup"><span data-stu-id="dc06f-107">(This implementation is returned by the [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) function.) However, if you do write a custom implementation, there are some issues to be aware of.</span></span>

<span data-ttu-id="dc06f-108">Zuerst muss Ihre Implementierung die [**mfasynkresult**](/windows/win32/api/mfapi/ns-mfapi-mfasyncresult) -Struktur erben.</span><span class="sxs-lookup"><span data-stu-id="dc06f-108">First, your implementation must inherit the [**MFASYNCRESULT**](/windows/win32/api/mfapi/ns-mfapi-mfasyncresult) structure.</span></span> <span data-ttu-id="dc06f-109">Die Media Foundation Arbeits Warteschlangen verwenden diese Struktur intern, um den Vorgang zu verteilen.</span><span class="sxs-lookup"><span data-stu-id="dc06f-109">The Media Foundation work queues use this structure internally to dispatch the operation.</span></span> <span data-ttu-id="dc06f-110">Initialisieren Sie alle Strukturmember mit Ausnahme des **pCallback** -Members, der einen Zeiger auf die Rückruf Schnittstelle des Aufrufers enthält.</span><span class="sxs-lookup"><span data-stu-id="dc06f-110">Initialize all of the structure members to zero, except for the **pCallback** member, which contains a pointer to the caller's callback interface.</span></span>

<span data-ttu-id="dc06f-111">Zweitens sollte Ihr Objekt [**mflockplatform**](/windows/desktop/api/mfapi/nf-mfapi-mflockplatform) in seinem Konstruktor anrufen, um die Media Foundation Plattform zu sperren.</span><span class="sxs-lookup"><span data-stu-id="dc06f-111">Second, your object should call [**MFLockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mflockplatform) in its constructor, to lock the Media Foundation platform.</span></span> <span data-ttu-id="dc06f-112">Zum Entsperren der Plattform muss [**mfunlockplatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="dc06f-112">Call [**MFUnlockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform) to unlock the platform.</span></span> <span data-ttu-id="dc06f-113">Diese Funktionen tragen dazu bei, das Herunterfahren der Plattform zu verhindern, bevor das Objekt zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="dc06f-113">These functions help to prevent the platform from shutting down before the object is destroyed.</span></span> <span data-ttu-id="dc06f-114">Weitere Informationen finden Sie unter [Arbeits Warteschlangen](work-queues.md).</span><span class="sxs-lookup"><span data-stu-id="dc06f-114">For more information, see [Work Queues](work-queues.md).</span></span>

<span data-ttu-id="dc06f-115">Der folgende Code zeigt eine grundlegende Implementierung der [**imfasynkresult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="dc06f-115">The following code shows a basic implementation of the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span> <span data-ttu-id="dc06f-116">Wie gezeigt, stellt dieser Code keine weiteren Funktionen bereit, die über die Standard Media Foundation Implementierung hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="dc06f-116">As shown, this code provides no additional features beyond the standard Media Foundation implementation.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="dc06f-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dc06f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc06f-118">Arbeits Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="dc06f-118">Work Queues</span></span>](work-queues.md)
</dt> <dt>

[<span data-ttu-id="dc06f-119">Asynchrone Rückruf Methoden</span><span class="sxs-lookup"><span data-stu-id="dc06f-119">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> </dl>

 

 



