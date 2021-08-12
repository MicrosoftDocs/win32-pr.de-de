---
title: Authentifizieren des Dienstanbieters
description: Authentifizieren des Dienstanbieters
ms.assetid: e48a8a7c-0277-4f0c-bad2-5bc9d0286da8
keywords:
- Windows Medien Geräte-Manager,Authentifizierung
- Geräte-Manager,Authentifizierung
- Programmierhandbuch,Authentifizierung
- Dienstanbieter,Authentifizierung
- Erstellen von Dienstanbietern,Authentifizierung
- authentication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d6931acb4644d4222659d428be10877deb164a184c95609663a915c12b95d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586486"
---
# <a name="authenticating-the-service-provider"></a>Authentifizieren des Dienstanbieters

Um über Windows Media Geräte-Manager zugänglich zu sein, muss ein Dienstanbieter die [**IComponentAuthenticate-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) erben und implementieren.

Um sich selbst zu authentifizieren, führt ein Dienstanbieter die folgenden Schritte aus:

1.  Bei der Instanziierung wird ein neues globales [CSecureChannelServer-Objekt](csecurechannelserver-class.md) erstellt und die Zertifikat- und Schlüsselwerte aus der Schlüsseldatei definiert.
2.  Sie implementiert die [**Methoden IComponentAuthenticate::SACAuth**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacauth) und [**IComponentAuthenticate::SACGetProtocols,**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacgetprotocols) indem die Parameter einfach an das globale CSecureChannelServer-Member übergeben werden.
3.  Vor der Verarbeitung implementierter Windows Media Geräte-Manager-Methoden muss der Dienstanbieter die Authentifizierung des Aufrufers überprüfen, indem er CSecureChannelServer::fIsAuthenticated aufruft und einen Fehler auft, wenn der Aufrufer nicht authentifiziert ist.

Diese Schritte werden in den folgenden C++-Beispielen gezeigt.

**Erstellen des CSecureChannelServer-Objekts**


```C++
CMyServiceProvider::CMyServiceProvider()
{
    HRESULT hr = S_OK;

    // Create the persistent SAC object.
    g_pSAC = new CSecureChannelServer();

    // Set the SAC certificate.
    if (g_pSAC)
    {
        hr = g_pSAC->SetCertificate(
             SAC_CERT_V1,
            (BYTE*)abCert, sizeof(abCert), // SP's certificate.
            (BYTE*)abPVK, sizeof(abPVK)    // SP's key.
        );
    }   
    if (FAILED(hr)) return hr;

    //... Perform other class initialization here ...

    return hr;
}
```



**Implementieren der IComponentAuthenticate-Methoden**


```C++
STDMETHODIMP CMDServiceProvider::SACAuth(
    DWORD   dwProtocolID,
    DWORD   dwPass,
    BYTE   *pbDataIn,
    DWORD   dwDataInLen,
    BYTE  **ppbDataOut,
    DWORD  *pdwDataOutLen)
{
    HRESULT hr = S_OK;

    // Verify that the global CSecureChannelServer member still exists.
    if (!g_pSAC)
        return E_FAIL;

    // Just pass the call to the global SAC member.
    hr = g_pSAC->SACAuth(
        dwProtocolID,
        dwPass,
        pbDataIn, dwDataInLen,
        ppbDataOut, pdwDataOutLen
    );
    return hr;
}

STDMETHODIMP CMDServiceProvider::SACGetProtocols(
    DWORD **ppdwProtocols,
    DWORD  *pdwProtocolCount)
{
    HRESULT hr = E_FAIL;

    if (!g_pSAC)
        return hr;

    hr = g_pSAC->SACGetProtocols(
        ppdwProtocols,
        pdwProtocolCount
    );
    return hr;
}
```



**Überprüfen der Authentifizierung des Aufrufers**

Das folgende Codebeispiel zeigt einen Dienstanbieter, der die Authentifizierung des Aufrufers als Teil seiner Implementierung der **IMDServiceProvider-Schnittstelle** überprüft.


```C++
STDMETHODIMP CMyServiceProvider::GetDeviceCount(DWORD * pdwCount)
{
    HRESULT hr = S_OK;
    if (!g_pSAC)
        return E_FAIL;

    if (!(g_pSAC->fIsAuthenticated()))
        return WMDM_E_NOTCERTIFIED;

    *pdwCount = m_DeviceCount;

    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen eines Dienstanbieters**](creating-a-service-provider.md)
</dt> </dl>

 

 




