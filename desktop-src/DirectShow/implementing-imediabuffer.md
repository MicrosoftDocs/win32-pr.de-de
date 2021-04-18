---
description: Implementieren von imediabuffer
ms.assetid: bde7cef8-f43e-4a11-8b77-fed5585d390a
title: Implementieren von imediabuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3425b3f612667a0b6577de385d59362bd8dafd0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354910"
---
# <a name="implementing-imediabuffer"></a><span data-ttu-id="5fc65-103">Implementieren von imediabuffer</span><span class="sxs-lookup"><span data-stu-id="5fc65-103">Implementing IMediaBuffer</span></span>

<span data-ttu-id="5fc65-104">Im DMO-Standard Streamingmodell werden Puffer über die [**imediabuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) -Schnittstelle verwaltet.</span><span class="sxs-lookup"><span data-stu-id="5fc65-104">In the default DMO streaming model, buffers are managed through the [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) interface.</span></span> <span data-ttu-id="5fc65-105">Der DMO-Client ist für die Implementierung eines Objekts verantwortlich, das diese Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="5fc65-105">The client of the DMO is responsible for implementing an object that exposes this interface.</span></span> <span data-ttu-id="5fc65-106">Die **imediabuffer** -Schnittstelle verfügt über drei Methoden:</span><span class="sxs-lookup"><span data-stu-id="5fc65-106">The **IMediaBuffer** interface has three methods:</span></span>

-   <span data-ttu-id="5fc65-107">**Getbufferandlength** gibt die Adresse des Puffers (d. h. den tatsächlichen Speicherblock, der die Daten enthält) und die Größe der gültigen Daten im Puffer zurück.</span><span class="sxs-lookup"><span data-stu-id="5fc65-107">**GetBufferAndLength** returns the address of the buffer (that is, the actual block of memory that holds the data) and the size of any valid data in the buffer.</span></span>
-   <span data-ttu-id="5fc65-108">**Getmaxlength** gibt die Größe des Puffers zurück.</span><span class="sxs-lookup"><span data-stu-id="5fc65-108">**GetMaxLength** returns the size of the buffer.</span></span>
-   <span data-ttu-id="5fc65-109">**SetLength** gibt die Länge der gültigen Daten im Puffer an.</span><span class="sxs-lookup"><span data-stu-id="5fc65-109">**SetLength** specifies the length of the valid data in the buffer.</span></span>

<span data-ttu-id="5fc65-110">Für die direkte Verarbeitung ist die **imediabuffer** -Schnittstelle nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5fc65-110">In-place processing does not require the **IMediaBuffer** interface.</span></span> <span data-ttu-id="5fc65-111">Der folgende Code zeigt eine minimale Implementierung von **imediabuffer**:</span><span class="sxs-lookup"><span data-stu-id="5fc65-111">The following code shows a minimal implementation of **IMediaBuffer**:</span></span>


```C++
//  CMediaBuffer class.
#include <dmo.h>
class CMediaBuffer : public IMediaBuffer
{
private:
    DWORD        m_cbLength;
    const DWORD  m_cbMaxLength;
    LONG         m_nRefCount;  // Reference count
    BYTE         *m_pbData;


    CMediaBuffer(DWORD cbMaxLength, HRESULT& hr) :
        m_nRefCount(1),
        m_cbMaxLength(cbMaxLength),
        m_cbLength(0),
        m_pbData(NULL)
    {
        m_pbData = new BYTE[cbMaxLength];
        if (!m_pbData) 
        {
            hr = E_OUTOFMEMORY;
        }
    }

    ~CMediaBuffer()
    {
        if (m_pbData) 
        {
            delete [] m_pbData;
        }
    }

public:

    // Function to create a new IMediaBuffer object and return 
    // an AddRef'd interface pointer.
    static HRESULT Create(long cbMaxLen, IMediaBuffer **ppBuffer)
    {
        HRESULT hr = S_OK;
        CMediaBuffer *pBuffer = NULL;

        if (ppBuffer == NULL)
        {
            return E_POINTER;
        }

        pBuffer = new CMediaBuffer(cbMaxLen, hr);

        if (pBuffer == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        if (SUCCEEDED(hr))
        {
           *ppBuffer = pBuffer;
           (*ppBuffer)->AddRef();
        }

        if (pBuffer)
        {
            pBuffer->Release();
        }
        return hr;
    }

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        if (ppv == NULL) 
        {
            return E_POINTER;
        }
        else if (riid == IID_IMediaBuffer || riid == IID_IUnknown) 
        {
            *ppv = static_cast<IMediaBuffer *>(this);
            AddRef();
            return S_OK;
        }
        else
        {
            *ppv = NULL;
            return E_NOINTERFACE;
        }
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_nRefCount);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG lRef = InterlockedDecrement(&m_nRefCount);
        if (lRef == 0) 
        {
            delete this;
            // m_cRef is no longer valid! Return lRef.
        }
        return lRef;  
    }

    // IMediaBuffer methods.
    STDMETHODIMP SetLength(DWORD cbLength)
    {
        if (cbLength > m_cbMaxLength) 
        {
            return E_INVALIDARG;
        }
        m_cbLength = cbLength;
        return S_OK;
    }

    STDMETHODIMP GetMaxLength(DWORD *pcbMaxLength)
    {
        if (pcbMaxLength == NULL) 
        {
            return E_POINTER;
        }
        *pcbMaxLength = m_cbMaxLength;
        return S_OK;
    }

    STDMETHODIMP GetBufferAndLength(BYTE **ppbBuffer, DWORD *pcbLength)
    {
        // Either parameter can be NULL, but not both.
        if (ppbBuffer == NULL && pcbLength == NULL) 
        {
            return E_POINTER;
        }
        if (ppbBuffer) 
        {
            *ppbBuffer = m_pbData;
        }
        if (pcbLength) 
        {
            *pcbLength = m_cbLength;
        }
        return S_OK;
    }
};

```



## <a name="related-topics"></a><span data-ttu-id="5fc65-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5fc65-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fc65-113">Direktes Hosting eines DMO</span><span class="sxs-lookup"><span data-stu-id="5fc65-113">Directly Hosting a DMO</span></span>](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



