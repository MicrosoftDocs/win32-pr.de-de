---
description: Benutzerdefinierte Topologielader
ms.assetid: 3982b07e-3179-45c1-9f17-f2114363f53d
title: Benutzerdefinierte Topologielader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02ca9cf393b83693199cea984183bf88186f74322ed816352e3c43d19a6e880b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880385"
---
# <a name="custom-topology-loaders"></a>Benutzerdefinierte Topologielader

Wenn eine Anwendung eine Teiltopologie in der Mediensitzung in die Warteschlange einreiht, verwendet die Mediensitzung ein Topologielader, um die Topologie aufzulösen. Standardmäßig verwendet die Mediensitzung die standardmäßige Media Foundation implementierung des Topologieladeers, aber Sie können auch eine benutzerdefinierte Implementierung bereitstellen. Dadurch erhalten Sie mehr Kontrolle über die endgültige Topologie. Ein benutzerdefiniertes Topologielader muss [**dieTOPOLOGYTopoLoader-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) implementieren.

Gehen Sie wie folgt vor, um ein benutzerdefiniertes Topologielader für die Mediensitzung festlegen:

1.  Erstellen Sie einen leeren Attributspeicher, indem [**Sie MFCreateAttributes aufrufen.**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes)
2.  Legen Sie das [**MF \_ SESSION \_ TOPOLOADER-Attribut**](mf-session-topoloader-attribute.md) für den Attributspeicher fest. Der Wert des -Attributs ist die CLSID Des benutzerdefinierten Ladeers.
3.  Rufen [**Sie MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) auf, um die Mediensitzung für ungeschützten Inhalt zu erstellen, oder [**MFCreatePMPMediaSession,**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) um die Mediensitzung innerhalb des geschützten Medienpfads (PMP) zu erstellen.

> [!Note]  
> Um ein benutzerdefiniertes Topologielader innerhalb des PMP zu verwenden, muss das Topologielader eine vertrauenswürdige Komponente sein. Weitere Informationen finden Sie unter [Protected Media Path](protected-media-path.md).

 

Der folgende Code zeigt, wie ein benutzerdefiniertes Topologielader für die Mediensitzung festgelegt wird.


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



Es ist nicht erforderlich, den gesamten Topologieladealgorithmus in Ihrem Topologielader zu implementieren. Alternativ können Sie das Standard-Media Foundation Topologielader umschließen. Ändern Sie in Ihrer Implementierung der [**METHODETOPOLOGYTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) die Topologie nach Bedarf, und übergeben Sie die geänderte Topologie an das Standardtopologielader. Anschließend schließt das Standardtopologielader die Topologie ab. Sie können auch die abgeschlossene Topologie ändern, bevor Sie sie an die Mediensitzung übergeben.

Der folgende Code zeigt die allgemeine Gliederung dieses Ansatzes. Es werden keine Details der [**Load-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) gezeigt, da diese von den speziellen Anforderungen Ihrer Anwendung abhängen.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**MFCreateTopoLoader**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader)
</dt> <dt>

[Advanced Topology Building](advanced-topology-building.md)
</dt> </dl>

 

 



