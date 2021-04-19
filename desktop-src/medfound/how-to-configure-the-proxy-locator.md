---
description: Konfigurieren des proxylocators
ms.assetid: ddc28add-ebf5-4a68-bdf4-dc5f33ab74da
title: Konfigurieren des proxylocators
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6b383dda9ac78b2c62aa8481a09cc5c0d7b3ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355550"
---
# <a name="how-to-configure-the-proxy-locator"></a><span data-ttu-id="f2d05-103">Konfigurieren des proxylocators</span><span class="sxs-lookup"><span data-stu-id="f2d05-103">How to Configure the Proxy Locator</span></span>

<span data-ttu-id="f2d05-104">Die Anwendung kann die Standardkonfiguration des proxylocators ändern, indem die Eigenschaft [mfnetsource \_ proxylocatorfactory](mfnetsource-proxylocatorfactory-property.md) auf das von der Anwendung implementierte objektlocatorfactory-Objekt festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f2d05-104">The application can change the default configuration of the proxy locator by setting the [MFNETSOURCE\_PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) property to the proxy locator factory object that is implemented by the application.</span></span> <span data-ttu-id="f2d05-105">Wenn die Anwendung quellresolver-Methoden zum Erstellen der Netzwerkquelle aufruft, wird Media Foundation die proxylocatorfactory aufruft.</span><span class="sxs-lookup"><span data-stu-id="f2d05-105">When the application calls source resolver methods to create the network source, Media Foundation calls the proxy locator factory.</span></span> <span data-ttu-id="f2d05-106">Mit diesem Objekt wird der proxylocator mit benutzerdefinierter Konfiguration erstellt.</span><span class="sxs-lookup"><span data-stu-id="f2d05-106">This object creates the proxy locator with custom configuration.</span></span>

## <a name="to-change-the-default-configuration-setting-of-the-proxy-locator"></a><span data-ttu-id="f2d05-107">So ändern Sie die Standard Konfigurationseinstellung des proxylocators</span><span class="sxs-lookup"><span data-stu-id="f2d05-107">To change the default configuration setting of the proxy locator</span></span>

1.  <span data-ttu-id="f2d05-108">Implementieren Sie die [**IMF netproxyloerfactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f2d05-108">Implement the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) interface.</span></span>
2.  <span data-ttu-id="f2d05-109">Führen Sie in der [**IMF netproxylocatorfactory:: forateproxylocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) -Methode die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="f2d05-109">In the [**IMFNetProxyLocatorFactory::CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) method, do the following:</span></span>
    1.  <span data-ttu-id="f2d05-110">Erstellen Sie einen Eigenschaften Speicher.</span><span class="sxs-lookup"><span data-stu-id="f2d05-110">Create a property store.</span></span>
    2.  <span data-ttu-id="f2d05-111">Legen Sie die Konfigurationseinstellungen für den proxylocator fest.</span><span class="sxs-lookup"><span data-stu-id="f2d05-111">Set the configuration settings for the proxy locator.</span></span> <span data-ttu-id="f2d05-112">Weitere Informationen zu diesen Einstellungen finden Sie unter [Proxy Locator-Konfigurationseinstellungen](proxy-locator-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="f2d05-112">For information about these settings, see [Proxy Locator Configuration Settings](proxy-locator-configuration-settings.md).</span></span>
    3.  <span data-ttu-id="f2d05-113">Aufrufen der Funktion " [**mfkreateproxylocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) ".</span><span class="sxs-lookup"><span data-stu-id="f2d05-113">Call the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="f2d05-114">Übergeben Sie den Eigenschaften Speicher und das Protokoll.</span><span class="sxs-lookup"><span data-stu-id="f2d05-114">Pass in the property store and the protocol.</span></span> <span data-ttu-id="f2d05-115">Das Protokoll wird im *pszprotocol* -Parameter von " [**kreateproxylocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator)" angegeben.</span><span class="sxs-lookup"><span data-stu-id="f2d05-115">The protocol is specified in the *pszProtocol* parameter of [**CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator).</span></span>
3.  <span data-ttu-id="f2d05-116">Erstellen Sie eine Instanz Ihrer proxylocator-Factoryklasse, und rufen Sie einen Zeiger auf Ihre [**imfnetproxylocatorfactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="f2d05-116">Create an instance of your proxy locator factory class and get a pointer to its [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) interface.</span></span>
4.  <span data-ttu-id="f2d05-117">Erstellen Sie einen weiteren Eigenschafts Speicher, und legen Sie den Wert der Eigenschaft [**mfnetsource \_ proxyloerfactory**](mfnetsource-proxylocatorfactory-property.md) auf den [**imfnetproxylo}**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) -Zeiger aus Schritt 3 fest.</span><span class="sxs-lookup"><span data-stu-id="f2d05-117">Create another property store and set the value of the [**MFNETSOURCE\_PROXYLOCATORFACTORY**](mfnetsource-proxylocatorfactory-property.md) property equal to the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) pointer from step 3.</span></span>
5.  <span data-ttu-id="f2d05-118">Wenn Sie die Netzwerkquelle erstellen, übergeben Sie den Eigenschafts Speicher im *prequicparameter* der Quell Konflikt Löser-Methoden, z. b. [**IMF sourceresolver:: beginkreateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span><span class="sxs-lookup"><span data-stu-id="f2d05-118">When you create the network source, pass the property store in the *pProps* parameter of the source resolver methods such as [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span></span>

## <a name="example"></a><span data-ttu-id="f2d05-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f2d05-119">Example</span></span>

<span data-ttu-id="f2d05-120">Im folgenden Codebeispiel wird die [**IMF netproxyloerfactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="f2d05-120">The following code example implements the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) interface.</span></span> <span data-ttu-id="f2d05-121">Die [**imfnetproxylocatorfactory:: forateproxylocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) -Methode erstellt eine Instanz des standardproxylocators und konfiguriert diese für den Betrieb im Modus für die automatische Erkennung.</span><span class="sxs-lookup"><span data-stu-id="f2d05-121">The [**IMFNetProxyLocatorFactory::CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) method creates an instance of the default proxy locator, and configures it to operate in auto-detect mode.</span></span>


```C++
class CProxyLocatorFactory : public IMFNetProxyLocatorFactory 
{
    LONG m_cRef;

public:

    CProxyLocatorFactory() : m_cRef(1)
    {
    }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CProxyLocatorFactory, IMFNetProxyLocatorFactory),
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

    STDMETHODIMP CreateProxyLocator(
        LPCWSTR pszProtocol, 
        IMFNetProxyLocator **ppProxyLocator
        )
    {
        *ppProxyLocator = NULL;

        //Create the property store object
        IPropertyStore *pProp = NULL;

        HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pProp));

        if(SUCCEEDED(hr))
        {
            // Property key for proxy settings.
            PROPERTYKEY key;
            key.fmtid = MFNETSOURCE_PROXYSETTINGS;        
            key.pid = 0;

            // Proxy settings
            PROPVARIANT var;
            var.vt = VT_I4;
            var.lVal = MFNET_PROXYSETTING_AUTO;

            hr = pProp->SetValue(key, var);
        }

        //Create the default proxy locator.

        if(SUCCEEDED(hr))
        {
            hr = MFCreateProxyLocator(pszProtocol, pProp, ppProxyLocator);
        }

        SafeRelease(&pProp);
        return hr;
    }
};
```



<span data-ttu-id="f2d05-122">Im nächsten Beispiel wird gezeigt, wie der [**imfnetproxyloskiorfactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) -Zeiger an die Netzwerkquelle übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f2d05-122">The next example shows how to pass the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) pointer to the network source.</span></span>


```C++
// Creates a media source from a URL.
//
// This example demonstrates how to set a proxy locator on the network source.

HRESULT CreateMediaSourceWithProxyLocator(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    IMFNetProxyLocatorFactory *pFactory = new (std::nothrow) CProxyLocatorFactory();

    if (pFactory == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_PROXYLOCATORFACTORY;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        var.punkVal = pFactory;

        hr = pConfig->SetValue(key, var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="f2d05-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f2d05-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2d05-124">Proxy Unterstützung für Netzwerk Quellen</span><span class="sxs-lookup"><span data-stu-id="f2d05-124">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 



