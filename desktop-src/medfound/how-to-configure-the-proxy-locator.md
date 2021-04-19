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
# <a name="how-to-configure-the-proxy-locator"></a>Konfigurieren des proxylocators

Die Anwendung kann die Standardkonfiguration des proxylocators ändern, indem die Eigenschaft [mfnetsource \_ proxylocatorfactory](mfnetsource-proxylocatorfactory-property.md) auf das von der Anwendung implementierte objektlocatorfactory-Objekt festgelegt wird. Wenn die Anwendung quellresolver-Methoden zum Erstellen der Netzwerkquelle aufruft, wird Media Foundation die proxylocatorfactory aufruft. Mit diesem Objekt wird der proxylocator mit benutzerdefinierter Konfiguration erstellt.

## <a name="to-change-the-default-configuration-setting-of-the-proxy-locator"></a>So ändern Sie die Standard Konfigurationseinstellung des proxylocators

1.  Implementieren Sie die [**IMF netproxyloerfactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) -Schnittstelle.
2.  Führen Sie in der [**IMF netproxylocatorfactory:: forateproxylocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) -Methode die folgenden Schritte aus:
    1.  Erstellen Sie einen Eigenschaften Speicher.
    2.  Legen Sie die Konfigurationseinstellungen für den proxylocator fest. Weitere Informationen zu diesen Einstellungen finden Sie unter [Proxy Locator-Konfigurationseinstellungen](proxy-locator-configuration-settings.md).
    3.  Aufrufen der Funktion " [**mfkreateproxylocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) ". Übergeben Sie den Eigenschaften Speicher und das Protokoll. Das Protokoll wird im *pszprotocol* -Parameter von " [**kreateproxylocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator)" angegeben.
3.  Erstellen Sie eine Instanz Ihrer proxylocator-Factoryklasse, und rufen Sie einen Zeiger auf Ihre [**imfnetproxylocatorfactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) -Schnittstelle ab.
4.  Erstellen Sie einen weiteren Eigenschafts Speicher, und legen Sie den Wert der Eigenschaft [**mfnetsource \_ proxyloerfactory**](mfnetsource-proxylocatorfactory-property.md) auf den [**imfnetproxylo}**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) -Zeiger aus Schritt 3 fest.
5.  Wenn Sie die Netzwerkquelle erstellen, übergeben Sie den Eigenschafts Speicher im *prequicparameter* der Quell Konflikt Löser-Methoden, z. b. [**IMF sourceresolver:: beginkreateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).

## <a name="example"></a>Beispiel

Im folgenden Codebeispiel wird die [**IMF netproxyloerfactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) -Schnittstelle implementiert. Die [**imfnetproxylocatorfactory:: forateproxylocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) -Methode erstellt eine Instanz des standardproxylocators und konfiguriert diese für den Betrieb im Modus für die automatische Erkennung.


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



Im nächsten Beispiel wird gezeigt, wie der [**imfnetproxyloskiorfactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) -Zeiger an die Netzwerkquelle übergeben wird.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Proxy Unterstützung für Netzwerk Quellen](proxy-support-for-network-sources.md)
</dt> </dl>

 

 



