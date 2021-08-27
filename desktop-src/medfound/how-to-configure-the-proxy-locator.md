---
description: Konfigurieren des Proxylocators
ms.assetid: ddc28add-ebf5-4a68-bdf4-dc5f33ab74da
title: Konfigurieren des Proxylocators
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51dcade0909159856c4286d9c2cd5d4851d10b6d2c5e56054545bdac312e21b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061540"
---
# <a name="how-to-configure-the-proxy-locator"></a>Konfigurieren des Proxylocators

Die Anwendung kann die Standardkonfiguration des Proxylocators ändern, indem sie die [MFNETSOURCE \_ PROXYLOCATORFACTORY-Eigenschaft](mfnetsource-proxylocatorfactory-property.md) auf das Proxylocatorfactoryobjekt festlegt, das von der Anwendung implementiert wird. Wenn die Anwendung Quell resolver-Methoden aufruft, um die Netzwerkquelle zu erstellen, ruft Media Foundation die Proxylocatorfactory auf. Dieses Objekt erstellt den Proxylocator mit benutzerdefinierter Konfiguration.

## <a name="to-change-the-default-configuration-setting-of-the-proxy-locator"></a>So ändern Sie die Standardkonfigurationseinstellung des Proxylocators

1.  Implementieren Sie die [**INTERFACESNetProxyLocatorFactory-Schnittstelle.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory)
2.  Gehen Sie in der [**METHODE VONNETProxyLocatorFactory::CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) wie folgt vor:
    1.  Erstellen Sie einen Eigenschaftenspeicher.
    2.  Legen Sie die Konfigurationseinstellungen für den Proxylocator fest. Informationen zu diesen Einstellungen finden Sie unter [Proxylocatorkonfiguration Einstellungen](proxy-locator-configuration-settings.md).
    3.  Rufen Sie die [**MFCreateProxyLocator-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) auf. Übergeben Sie den Eigenschaftenspeicher und das Protokoll. Das Protokoll wird im *pszProtocol-Parameter* von [**CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator)angegeben.
3.  Erstellen Sie eine Instanz der Proxylocatorfactoryklasse, und erhalten Sie einen Zeiger auf die [**ZUGEHÖRIGE SCHNITTSTELLE VONNETProxyLocatorFactory.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory)
4.  Erstellen Sie einen anderen Eigenschaftenspeicher, und legen Sie den Wert der [**MFNETSOURCE \_ PROXYLOCATORFACTORY-Eigenschaft**](mfnetsource-proxylocatorfactory-property.md) auf den [**POINTERNetProxyLocatorFactory-Zeiger**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) aus Schritt 3 fest.
5.  Wenn Sie die Netzwerkquelle erstellen, übergeben Sie den Eigenschaftenspeicher im *pProps-Parameter* der Quellresolvermethoden wie [**Z.B. SFCSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).

## <a name="example"></a>Beispiel

Im folgenden Codebeispiel wird die [**INTERFACESNetProxyLocatorFactory-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) implementiert. Mit der [**METHODE LOCATORNetProxyLocatorFactory::CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) wird eine Instanz des Standardproxylocators erstellt und für den Betrieb im Automatischerkennungsmodus konfiguriert.


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



Im nächsten Beispiel wird gezeigt, wie der [**POINTERNetProxyLocatorFactory-Zeiger**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) an die Netzwerkquelle übergeben wird.


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

[Proxyunterstützung für Netzwerkquellen](proxy-support-for-network-sources.md)
</dt> </dl>

 

 



