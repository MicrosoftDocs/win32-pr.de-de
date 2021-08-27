---
description: Entsperren des Windows Media Format SDK
ms.assetid: 7ede8bda-3b26-452d-8ce9-cd2410ffd9f4
title: Entsperren des Windows Media Format SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1f332711e9fd12c9b0ff1f789438d051487b81711f157ae1024a8e47973386
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078660"
---
# <a name="unlocking-the-windows-media-format-sdk"></a>Entsperren des Windows Media Format SDK

Für den Zugriff auf Version 7 oder 7.1 des Windows Media Format SDK muss eine Anwendung zur Laufzeit ein Softwarezertifikat bereitstellen, das auch als Schlüssel bezeichnet wird. Dieser Schlüssel ist in einer statischen Bibliothek namens wmstub.lib enthalten, mit der die Anwendung zur Buildzeit verknüpft ist. Ein individualisierter Schlüssel ist nur zum Erstellen oder Lesen von DRM-geschützten Dateien erforderlich. Nicht-DRM-Dateien können mithilfe der statischen Bibliothek erstellt werden, die mit dem Windows Media Format SDK bereitgestellt wird. Weitere Informationen zum Abrufen des DRM-Schlüssels finden Sie im Windows Media Format SDK. Eine DirectShow-Anwendung stellt ihr Zertifikat für den WM ASF Writer zur Anwendung, wenn sie dem Filterdiagramm hinzugefügt wird. Die Anwendung muss sich mithilfe der COM-Schnittstellen **IServiceProvider** und **IObjectWithSite als Schlüsselanbieter** registrieren. Mit dieser Technik implementiert die Anwendung eine von IServiceProvider abgeleitete **Schlüsselanbieterklasse.** Diese Klasse implementiert die drei COM-Standardmethoden **AddRef,** **QueryInterface** und **Release** sowie eine zusätzliche Methode, **QueryService,** die vom Filterdiagramm-Manager aufgerufen wird. **QueryService** ruft die Windows Media Format SDK-Methode [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) auf und kehrt zum Filterdiagramm-Manager einen Zeiger auf das erstellte Zertifikat zurück. Wenn das Zertifikat gültig ist, ermöglicht der Filterdiagramm-Manager, dass der Graphenprozess fortgesetzt wird.

> [!Note]  
> Um eine Anwendung zu erstellen, schließen Sie Wmsdkidl.h für den Prototyp für [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85))ein, und verknüpfen Sie die Bibliothek Wmstub.lib.

 

Das folgende Codebeispiel veranschaulicht die grundlegenden Schritte in diesem Prozess:


```C++
// Declare and implement a key provider class derived from IServiceProvider.

class CKeyProvider : public IServiceProvider {
public:
    // IUnknown interface
    STDMETHODIMP QueryInterface(REFIID riid, void ** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    CKeyProvider();

    // IServiceProvider
    STDMETHODIMP QueryService(REFIID siid, REFIID riid, void **ppv);
    
private:
    ULONG m_cRef;
};

CKeyProvider::CKeyProvider() : m_cRef(0)
{
}

// IUnknown methods
ULONG CKeyProvider::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

ULONG CKeyProvider::Release()
{
    ASSERT(m_cRef > 0);

    ULONG lCount = InterlockedDecrement(&m_cRef);
    if (m_cRef == 0) 
    {
        delete this;
        return (ULONG)0;
    }
    return (ULONG)lCount;
}

// We only support IUnknown and IServiceProvider.
HRESULT CKeyProvider::QueryInterface(REFIID riid, void ** ppv)
{
    if (!ppv) return E_POINTER;

    if (riid == IID_IUnknown) 
    {
        *ppv = (void *) static_cast<IUnknown *>(this);
        AddRef();
        return S_OK;
    }
    if (riid == IID_IServiceProvider) 
    {
        *ppv = (void *) static_cast<IServiceProvider *>(this);
        AddRef();
        return S_OK;
    }

    return E_NOINTERFACE;
}

STDMETHODIMP CKeyProvider::QueryService(REFIID siid, REFIID riid, void **ppv)
{
    if (!ppv) return E_POINTER;

    if (siid == __uuidof(IWMReader) && riid == IID_IUnknown) 
    {
        IUnknown *punkCert;
        HRESULT hr = WMCreateCertificate(&punkCert);
        if (SUCCEEDED(hr)) 
        {
            *ppv = (void *) punkCert;
        }
        return hr;
    }
    return E_NOINTERFACE;
}

////////////////////////////////////////////////////////////////////
//
// These examples illustrate the sequence of method calls
// in your application. Error checking is omitted for brevity.
//
///////////////////////////////////////////////////////////////////

// Create the filter graph manager, but don't add any filters.
IGraphBuilder *pGraph;
hr = CreateFilterGraph(&pGraph);

...

// Instantiate the key provider class, and AddRef it
// so that COM doesn't try to free our static object.

CKeyProvider prov;
prov.AddRef();  // Don't let COM try to free our static object.

// Give the graph an IObjectWithSite pointer for callbacks and QueryService.
IObjectWithSite* pObjectWithSite = NULL;

hr = pGraph->QueryInterface(IID_IObjectWithSite, (void**)&pObjectWithSite);
if (SUCCEEDED(hr))
{
    // Use the IObjectWithSite pointer to specify our key provider object.
    // The filter graph manager will use this pointer to call
    // QueryService to do the unlocking.
    // If the unlocking succeeds, then we can build our graph.

    pObjectWithSite->SetSite((IUnknown *) (IServiceProvider *) &prov);
    pObjectWithSite->Release();
}

// Now build the graph.
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von ASF-Dateien in DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
