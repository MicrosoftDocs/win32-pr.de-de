---
description: Entsperren des Windows Media-Format-SDKs
ms.assetid: 7ede8bda-3b26-452d-8ce9-cd2410ffd9f4
title: Entsperren des Windows Media-Format-SDKs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9807794dc7e42c563f2f7d45dcb0b1b684aad1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106353629"
---
# <a name="unlocking-the-windows-media-format-sdk"></a><span data-ttu-id="6bfb0-103">Entsperren des Windows Media-Format-SDKs</span><span class="sxs-lookup"><span data-stu-id="6bfb0-103">Unlocking the Windows Media Format SDK</span></span>

<span data-ttu-id="6bfb0-104">Für den Zugriff auf Version 7 oder 7,1 des Windows Media Format SDK muss eine Anwendung zur Laufzeit ein Software Zertifikat bereitstellen, das auch als Schlüssel bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="6bfb0-104">To access version 7 or 7.1 of the Windows Media Format SDK, an application must provide a software certificate, also called a key, at run time.</span></span> <span data-ttu-id="6bfb0-105">Dieser Schlüssel ist in einer statischen Bibliothek namens wmstub. lib enthalten, auf die die Anwendung zur Buildzeit verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="6bfb0-105">This key is contained in a static library called wmstub.lib to which the application links at build time.</span></span> <span data-ttu-id="6bfb0-106">Ein individualisierter Schlüssel ist nur zum Erstellen oder Lesen von DRM-geschützten Dateien erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6bfb0-106">An individualized key is only required for creating or reading DRM-protected files.</span></span> <span data-ttu-id="6bfb0-107">Nicht-DRM-Dateien können mithilfe der statischen Bibliothek erstellt werden, die mit dem Windows Media-Format SDK bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6bfb0-107">Non-DRM files can be created using the static library provided with the Windows Media Format SDK.</span></span> <span data-ttu-id="6bfb0-108">Ausführliche Informationen zum Abrufen des DRM-Schlüssels finden Sie im Windows Media-Format-SDK.</span><span class="sxs-lookup"><span data-stu-id="6bfb0-108">For details on obtaining the DRM key, see the Windows Media Format SDK.</span></span> <span data-ttu-id="6bfb0-109">Eine DirectShow-Anwendung stellt das Zertifikat für den WM-ASF-Writer bereit, wenn es dem Filter Diagramm hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="6bfb0-109">A DirectShow application provides its certificate to the WM ASF Writer when it is added to the filter graph.</span></span> <span data-ttu-id="6bfb0-110">Die Anwendung muss als Schlüssel Anbieter mithilfe der Schnittstellen com **IServiceProvider** und **IObjectWithSite** registriert werden.</span><span class="sxs-lookup"><span data-stu-id="6bfb0-110">The application must register as a key provider using the COM **IServiceProvider** and **IObjectWithSite** interfaces.</span></span> <span data-ttu-id="6bfb0-111">Mit dieser Technik implementiert die Anwendung eine von **IServiceProvider** abgeleitete Schlüssel Anbieter Klasse.</span><span class="sxs-lookup"><span data-stu-id="6bfb0-111">Using this technique, the application implements a key provider class derived from **IServiceProvider**.</span></span> <span data-ttu-id="6bfb0-112">Diese Klasse implementiert die drei com-Standardmethoden –**adressf**, **QueryInterface** und **Release**– zusammen mit einer zusätzlichen Methode ( **QueryService**), die vom Filter Graph-Manager aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6bfb0-112">This class implements the three standard COM methods—**AddRef**, **QueryInterface**, and **Release**—along with one additional method, **QueryService**, which is called by the filter graph manager.</span></span> <span data-ttu-id="6bfb0-113">**QueryService** Ruft die Windows Media-Format-SDK-Methode [**wmkreatecertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) auf und kehrt zum Filter Graph-Manager zurück, um einen Zeiger auf das Zertifikat zu erstellen, das erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6bfb0-113">**QueryService** calls the Windows Media Format SDK method [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) and returns to the filter graph manager a pointer to the certificate that was created.</span></span> <span data-ttu-id="6bfb0-114">Wenn das Zertifikat gültig ist, ermöglicht der Filter Diagramm-Manager das Fortsetzen des Diagramms.</span><span class="sxs-lookup"><span data-stu-id="6bfb0-114">If the certificate is valid, the filter graph manager allows the graph-building process to proceed.</span></span>

> [!Note]  
> <span data-ttu-id="6bfb0-115">Um eine Anwendung zu erstellen, schließen Sie wmsdkidl. h für den Prototyp für [**wmkreatecertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85))ein, und verknüpfen Sie Sie mit der wmstub. lib-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="6bfb0-115">To build an application, include Wmsdkidl.h for the prototype for [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)), and link to the Wmstub.lib library.</span></span>

 

<span data-ttu-id="6bfb0-116">Im folgenden Codebeispiel werden die grundlegenden Schritte in diesem Prozess veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="6bfb0-116">The following code example illustrates the basic steps in this process:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6bfb0-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6bfb0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bfb0-118">Erstellen von ASF-Dateien in DirectShow</span><span class="sxs-lookup"><span data-stu-id="6bfb0-118">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
