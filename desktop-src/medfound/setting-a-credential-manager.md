---
description: Festlegen eines Credential-Managers
ms.assetid: a20c2e6c-e9d9-438f-a57a-e3080587c11c
title: Festlegen eines Credential-Managers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c98d9d9572438a63f93f916a0084f8a33a7bca5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345196"
---
# <a name="setting-a-credential-manager"></a>Festlegen eines Credential-Managers

Eine Anwendung, die Anmelde Informationen für die Netzwerkquelle bereitstellt, muss folgende Aktionen ausführen:

1.  Implementieren Sie ein Anmelde Informationen Manager-Objekt, das die [**IMF netkredentialmanager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) -Schnittstelle verfügbar macht.
2.  Erstellen Sie vor dem Erstellen der Netzwerkquelle einen neuen Eigenschaften Speicher.
3.  Legen Sie die Eigenschaft "MF-Anmelde Informations [**\_ \_ Verwaltung**](mfnetsource-credential-manager-property.md) " für den Eigenschaften Speicher fest. Der Wert der-Eigenschaft ist ein Zeiger auf die [**imfnetkredentialmanager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) -Schnittstelle.
4.  Übergeben Sie einen Zeiger zum Eigenschaften Speicher an den Quell Konflikt Löser, wie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md)beschrieben.

Die Netzwerk Quellen verwenden den Anmelde Informations-Manager, um Benutzer Anmelde Informationen zu erhalten. Wenn die Netzwerkquelle Anmelde Informationen für den Zugriff auf eine Netzwerkressource erfordert, ruft Sie die [**imfnetkredentialmanager:: begingetanmeldeinformationen**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) -Methode der Anwendung auf. Dieser-Befehl startet eine asynchrone Anforderung, um die Anmelde Informationen des Benutzers abzurufen. Die **begingetcredensmethode** kann die Anmelde Informationen entweder aus dem Anmelde Informations Cache oder vom Benutzer erhalten. Anmelde Informationen werden in einem *Anmelde Informationen-Objekt* gespeichert. Wenn der Vorgang beendet ist, ruft die Anwendung die Rückruf Schnittstelle auf, um die Netzwerkquelle zu benachrichtigen. Die Netzwerkquelle ruft [**imfnetkredentialmanager:: endgetanmelde**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) Informationen auf, um den asynchronen Vorgang abzuschließen.

Da dies ein asynchroner Vorgang ist, muss die Anwendung den Rückruf am Ende des Vorgangs senden. Schritt-für-Schritt-Anleitungen zum Schreiben einer asynchronen Methode finden Sie unter [Schreiben einer asynchronen Methode](writing-an-asynchronous-method.md).

Im folgenden Beispiel wird gezeigt, wie die Eigenschaft " [**mfnetsource \_ Credential \_ Manager**](mfnetsource-credential-manager-property.md) " in der Netzwerkquelle festgelegt wird.


```C++
// Creates a media source from a URL.
//
// Demonstrates how to set a credential manager on the network source.

HRESULT CreateMediaSourceWithCredentialManager(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    CCredentialManager *pCredentials = new (std::nothrow) CCredentialManager();

    if (pCredentials == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_CREDENTIAL_MANAGER;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        pCredentials->QueryInterface(IID_PPV_ARGS(&var.punkVal));

        hr = pConfig->SetValue(key, var);

        PropVariantClear(&var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    SafeRelease(&pCredentials);

    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Netzwerk Quellen Authentifizierung](network-source-authentication.md)
</dt> </dl>

 

 



