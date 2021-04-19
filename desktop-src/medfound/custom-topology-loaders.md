---
description: Benutzerdefinierte topologielader
ms.assetid: 3982b07e-3179-45c1-9f17-f2114363f53d
title: Benutzerdefinierte topologielader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a8f9e24b207d43620e7b2d09080d244b0a9e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344982"
---
# <a name="custom-topology-loaders"></a><span data-ttu-id="743fd-103">Benutzerdefinierte topologielader</span><span class="sxs-lookup"><span data-stu-id="743fd-103">Custom Topology Loaders</span></span>

<span data-ttu-id="743fd-104">Wenn eine Anwendung eine partielle Topologie in der Medien Sitzung in eine Warteschlange stellt, verwendet die Medien Sitzung einen topologielader, um die Topologie aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="743fd-104">When an application queues a partial topology on the Media Session, the Media Session uses a topology loader to resolve the topology.</span></span> <span data-ttu-id="743fd-105">Standardmäßig verwendet die Medien Sitzung die Standard Media Foundation-Implementierung des topologieladers, aber Sie können auch eine benutzerdefinierte-Implementierung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="743fd-105">By default, the Media Session uses the standard Media Foundation implementation of the topology loader, but you can also provide a custom implementation.</span></span> <span data-ttu-id="743fd-106">Dadurch erhalten Sie mehr Kontrolle über die endgültige Topologie.</span><span class="sxs-lookup"><span data-stu-id="743fd-106">This gives you more control over the final topology.</span></span> <span data-ttu-id="743fd-107">Ein benutzerdefiniertes topologielader muss die [**imftopoloader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="743fd-107">A custom topology loader must implement the [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) interface.</span></span>

<span data-ttu-id="743fd-108">Gehen Sie folgendermaßen vor, um ein benutzerdefiniertes topologielader in der Medien Sitzung festzulegen:</span><span class="sxs-lookup"><span data-stu-id="743fd-108">To set a custom topology loader on the Media Session, do the following:</span></span>

1.  <span data-ttu-id="743fd-109">Erstellen Sie einen leeren Attribut Speicher, indem Sie [**mfcreateattribute**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="743fd-109">Create an empty attribute store by calling [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>
2.  <span data-ttu-id="743fd-110">Legen Sie das [**MF- \_ Sitzungs \_ topoloader**](mf-session-topoloader-attribute.md) -Attribut für den Attribut Speicher fest.</span><span class="sxs-lookup"><span data-stu-id="743fd-110">Set the [**MF\_SESSION\_TOPOLOADER**](mf-session-topoloader-attribute.md) attribute on the attribute store.</span></span> <span data-ttu-id="743fd-111">Der Wert des-Attributs ist die CLSID Ihres benutzerdefinierten Lade Moduls.</span><span class="sxs-lookup"><span data-stu-id="743fd-111">The value of the attribute is the CLSID of your custom loader.</span></span>
3.  <span data-ttu-id="743fd-112">Rufen Sie [**mfkreatemediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) auf, um die Medien Sitzung für ungeschützten Inhalt zu erstellen, oder [**mfkreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) , um die Medien Sitzung im geschützten Medien Pfad (PMP) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="743fd-112">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create the Media Session for unprotected content, or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) to create the Media Session inside the protected media path (PMP).</span></span>

> [!Note]  
> <span data-ttu-id="743fd-113">Um ein benutzerdefiniertes topologielader innerhalb des PMP zu verwenden, muss das topologielader eine vertrauenswürdige Komponente sein.</span><span class="sxs-lookup"><span data-stu-id="743fd-113">To use a custom topology loader inside the PMP, the topology loader must be a trusted component.</span></span> <span data-ttu-id="743fd-114">Weitere Informationen finden Sie unter [geschützter Medien Pfad](protected-media-path.md).</span><span class="sxs-lookup"><span data-stu-id="743fd-114">For more information, see [Protected Media Path](protected-media-path.md).</span></span>

 

<span data-ttu-id="743fd-115">Der folgende Code zeigt, wie ein benutzerdefiniertes topologielader für die Medien Sitzung festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="743fd-115">The following code shows how to set a custom topology loader on the Media Session.</span></span>


```C++
HRESULT CreateSession_CustomTopoLoader(REFCLSID clsid, IMFMediaSession **ppSession)
{
    *ppSession = NULL;

    IMFMediaSession *pSession = NULL;
    IMFAttributes *pConfig = NULL;

    // Create an attribute store to configure the media session.
    HRESULT hr = MFCreateAttributes(&pConfig, 1);

    // Set the CLSID of the custom topology loader.
    if (SUCCEEDED(hr))
    {
        hr = pConfig->SetGUID(MF_SESSION_TOPOLOADER, clsid);
    }

    // Create the media session.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaSession(pConfig, &pSession);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppSession = pSession;
        (*ppSession)->AddRef();
    }

    SafeRelease(&pSession);
    SafeRelease(&pConfig);

    return hr;
}
```



<span data-ttu-id="743fd-116">Es ist nicht erforderlich, den gesamten topologieladealgorithmus in Ihrem topologielader zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="743fd-116">It is not necessary to implement the entire topology-loading algorithm in your topology loader.</span></span> <span data-ttu-id="743fd-117">Als Alternative können Sie den Standard Media Foundation topologielader umschließen.</span><span class="sxs-lookup"><span data-stu-id="743fd-117">As an alternative, you can wrap the standard Media Foundation topology loader.</span></span> <span data-ttu-id="743fd-118">Ändern Sie in der Implementierung der [**imftopoloader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) -Methode die Topologie nach Bedarf, und übergeben Sie die geänderte Topologie an den Standard-topologielader.</span><span class="sxs-lookup"><span data-stu-id="743fd-118">In your implementation of the [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method, modify the topology as needed and pass the modified topology to the standard topology loader.</span></span> <span data-ttu-id="743fd-119">Der Standard-topologielader schließt dann die Topologie ab.</span><span class="sxs-lookup"><span data-stu-id="743fd-119">Then the standard topology loader completes the topology.</span></span> <span data-ttu-id="743fd-120">Sie können auch die vollständige Topologie ändern, bevor Sie Sie wieder an die Medien Sitzung übergeben.</span><span class="sxs-lookup"><span data-stu-id="743fd-120">You can also modify the completed topology before passing it back to the Media Session.</span></span>

<span data-ttu-id="743fd-121">Der folgende Code zeigt die allgemeine Gliederung dieses Ansatzes.</span><span class="sxs-lookup"><span data-stu-id="743fd-121">The following code shows the general outline of this approach.</span></span> <span data-ttu-id="743fd-122">Es werden keine Details der [**Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) -Methode angezeigt, da diese von den speziellen Anforderungen Ihrer Anwendung abhängen.</span><span class="sxs-lookup"><span data-stu-id="743fd-122">It does not show any details of the [**Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method, because these will depend on the particular requirements of your application.</span></span>


```C++
class CTopoLoader : public IMFTopoLoader
{
public:

    static HRESULT CreateInstance(REFIID iid, void **ppv)
    {
        HRESULT hr = S_OK;

        CTopoLoader *pTopoLoader = new (std::nothrow) CTopoLoader(&hr);
        
        if (pTopoLoader == NULL)
        {
            return E_OUTOFMEMORY;
        }

        if (SUCCEEDED(hr))
        {
            hr = pTopoLoader->QueryInterface(iid, ppv);
        }

        SafeRelease(&pTopoLoader);
        return hr;
    }

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CTopoLoader, IMFTopoLoader),
            { 0 },
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

    // IMTopoLoader methods.
    STDMETHODIMP Load(
        IMFTopology *pInput, 
        IMFTopology **ppOutput, 
        IMFTopology *pCurrent
        )
    {
        HRESULT hr = S_OK;

        // TODO: Add custom topology-building code here.
        //       Modify pInput as needed.

        if (SUCCEEDED(hr))
        {
            hr = m_pTopoLoader->Load(pInput, ppOutput, pCurrent);
        }

        // TODO: Add custom topology-building code here.
        //       Modify ppOutput as needed.

        return hr;
    }

private:
    CTopoLoader(HRESULT *phr) : m_cRef(1), m_pTopoLoader(NULL)
    {
        *phr = MFCreateTopoLoader(&m_pTopoLoader);
    }

    virtual ~CTopoLoader()
    {
        SafeRelease(&m_pTopoLoader);
    }

private:
    long            m_cRef;          // Reference count.
    IMFTopoLoader   *m_pTopoLoader;  // Standard topoloader.
};
```



## <a name="related-topics"></a><span data-ttu-id="743fd-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="743fd-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="743fd-124">**MF-abetopoloader**</span><span class="sxs-lookup"><span data-stu-id="743fd-124">**MFCreateTopoLoader**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader)
</dt> <dt>

[<span data-ttu-id="743fd-125">Erweiterte topologiebildung</span><span class="sxs-lookup"><span data-stu-id="743fd-125">Advanced Topology Building</span></span>](advanced-topology-building.md)
</dt> </dl>

 

 



