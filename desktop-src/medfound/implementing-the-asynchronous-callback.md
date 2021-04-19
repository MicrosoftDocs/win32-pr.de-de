---
description: Implementieren des asynchronen Rückrufs
ms.assetid: c2c9d0f7-038b-4f23-985c-b812908d71a7
title: Implementieren des asynchronen Rückrufs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24088aea4e74b39ae08625c6917a5ca56f554158
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356745"
---
# <a name="implementing-the-asynchronous-callback"></a>Implementieren des asynchronen Rückrufs

Der folgende Code zeigt das grundlegende Framework, das zum Implementieren der [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle erforderlich ist. In diesem Beispiel wird die [**Aufruf**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Methode als reine virtuelle Methode deklariert. Die Implementierung dieser Methode hängt von der asynchronen Methode ab, die Sie aufrufen. Weitere Informationen finden Sie unter [Aufrufen von asynchronen Methoden](calling-asynchronous-methods.md).


```C++
#include <shlwapi.h>

class CAsyncCallback : public IMFAsyncCallback 
{
public:
    CAsyncCallback () : m_cRef(1) { }
    virtual ~CAsyncCallback() { }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CAsyncCallback, IMFAsyncCallback),
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
        long cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }

    STDMETHODIMP Invoke(IMFAsyncResult* pAsyncResult) = 0;
    // TODO: Implement this method. 

    // Inside Invoke, IMFAsyncResult::GetStatus to get the status.
    // Then call the EndX method to complete the operation. 

private:
    long    m_cRef;
};
```



Der folgende Code zeigt eine Beispiel Implementierung einer Klasse, die von abgeleitet wird `CAsyncCallback` :


```C++
class CMyCallback : public CAsyncCallback
{
    HANDLE m_hEvent;
    IMFByteStream *m_pStream;

    HRESULT m_hrStatus;
    ULONG   m_cbRead;

public:

    CMyCallback(IMFByteStream *pStream, HRESULT *phr) 
        : m_pStream(pStream), m_hrStatus(E_PENDING), m_cbRead(0)
    {
        *phr = S_OK;

        m_pStream->AddRef();

        m_hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);

        if (m_hEvent == NULL)
        {
            *phr = HRESULT_FROM_WIN32(GetLastError());
        }
    }
    ~CMyCallback()
    {
        m_pStream->Release();
        CloseHandle(m_hEvent);
    }

    HRESULT WaitForCompletion(DWORD msec)
    {
        DWORD result = WaitForSingleObject(m_hEvent, msec);

        switch (result)
        {
        case WAIT_TIMEOUT:
            return E_PENDING;

        case WAIT_ABANDONED:
        case WAIT_OBJECT_0:
            return m_hrStatus;

        default:
            return HRESULT_FROM_WIN32(GetLastError());
        }
    }

    ULONG   GetBytesRead() const { return m_cbRead; }

    STDMETHODIMP Invoke(IMFAsyncResult* pResult)
    {
        m_hrStatus = m_pStream->EndRead(pResult, &m_cbRead);

        SetEvent(m_hEvent);

        return S_OK;
    }
};
```



In diesem Beispiel wird ein Ereignis innerhalb der [**Aufruf**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Methode signalisiert. Eine Erläuterung der verschiedenen Optionen finden Sie unter [Aufrufen von asynchronen Methoden](calling-asynchronous-methods.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Asynchrone Rückruf Methoden](asynchronous-callback-methods.md)
</dt> </dl>

 

 



