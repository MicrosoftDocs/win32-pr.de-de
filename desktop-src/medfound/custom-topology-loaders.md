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
# <a name="custom-topology-loaders"></a>Benutzerdefinierte topologielader

Wenn eine Anwendung eine partielle Topologie in der Medien Sitzung in eine Warteschlange stellt, verwendet die Medien Sitzung einen topologielader, um die Topologie aufzulösen. Standardmäßig verwendet die Medien Sitzung die Standard Media Foundation-Implementierung des topologieladers, aber Sie können auch eine benutzerdefinierte-Implementierung bereitstellen. Dadurch erhalten Sie mehr Kontrolle über die endgültige Topologie. Ein benutzerdefiniertes topologielader muss die [**imftopoloader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) -Schnittstelle implementieren.

Gehen Sie folgendermaßen vor, um ein benutzerdefiniertes topologielader in der Medien Sitzung festzulegen:

1.  Erstellen Sie einen leeren Attribut Speicher, indem Sie [**mfcreateattribute**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes)aufrufen.
2.  Legen Sie das [**MF- \_ Sitzungs \_ topoloader**](mf-session-topoloader-attribute.md) -Attribut für den Attribut Speicher fest. Der Wert des-Attributs ist die CLSID Ihres benutzerdefinierten Lade Moduls.
3.  Rufen Sie [**mfkreatemediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) auf, um die Medien Sitzung für ungeschützten Inhalt zu erstellen, oder [**mfkreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) , um die Medien Sitzung im geschützten Medien Pfad (PMP) zu erstellen.

> [!Note]  
> Um ein benutzerdefiniertes topologielader innerhalb des PMP zu verwenden, muss das topologielader eine vertrauenswürdige Komponente sein. Weitere Informationen finden Sie unter [geschützter Medien Pfad](protected-media-path.md).

 

Der folgende Code zeigt, wie ein benutzerdefiniertes topologielader für die Medien Sitzung festgelegt wird.


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



Es ist nicht erforderlich, den gesamten topologieladealgorithmus in Ihrem topologielader zu implementieren. Als Alternative können Sie den Standard Media Foundation topologielader umschließen. Ändern Sie in der Implementierung der [**imftopoloader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) -Methode die Topologie nach Bedarf, und übergeben Sie die geänderte Topologie an den Standard-topologielader. Der Standard-topologielader schließt dann die Topologie ab. Sie können auch die vollständige Topologie ändern, bevor Sie Sie wieder an die Medien Sitzung übergeben.

Der folgende Code zeigt die allgemeine Gliederung dieses Ansatzes. Es werden keine Details der [**Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) -Methode angezeigt, da diese von den speziellen Anforderungen Ihrer Anwendung abhängen.


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

[**MF-abetopoloader**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader)
</dt> <dt>

[Erweiterte topologiebildung](advanced-topology-building.md)
</dt> </dl>

 

 



