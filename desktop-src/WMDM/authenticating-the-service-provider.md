---
title: Authentifizieren des Dienstanbieters
description: Authentifizieren des Dienstanbieters
ms.assetid: e48a8a7c-0277-4f0c-bad2-5bc9d0286da8
keywords:
- Windows Media-Device Manager, Authentifizierung
- Device Manager, Authentifizierung
- Programmier Handbuch, Authentifizierung
- Dienstanbieter, Authentifizierung
- Erstellen von Dienstanbietern, Authentifizierung
- authentication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 271bf5594e4adaede01bb8e3795780f8f5c5177a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340441"
---
# <a name="authenticating-the-service-provider"></a>Authentifizieren des Dienstanbieters

Um von Windows Media Device Manager zugänglich zu sein, muss ein Dienstanbieter die [**icomponentauthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) -Schnittstelle erben und implementieren.

Ein Dienstanbieter führt die folgenden Schritte aus, um sich selbst zu authentifizieren:

1.  Bei der Instanziierung wird ein neues globales [csecurechannelserver](csecurechannelserver-class.md) -Objekt erstellt und das Zertifikat und die Schlüsselwerte aus seiner Schlüsseldatei festgelegt.
2.  Es implementiert die [**icomponentauthenticate:: sacauth**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacauth) -und die [**icomponentauthenticate:: sacgetprotokolls**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacgetprotocols) -Methode, indem die Parameter einfach an das globale csecurechannelserver-Element übergeben werden.
3.  Vor der Behandlung implementierter Windows Media Device Manager-Methoden muss der Dienstanbieter die Authentifizierung des Aufrufers durch Aufrufen von csecurechannelserver:: fisauthenticated überprüfen und einen Fehler auftreten, wenn der Aufrufer nicht authentifiziert ist.

Diese Schritte sind in den folgenden C++ Beispielen aufgeführt.

**Erstellen des csecurechannelserver-Objekts**


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



**Implementieren der icomponentauthenticate-Methoden**


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

Das folgende Codebeispiel zeigt, wie ein Dienstanbieter die Authentifizierung des Aufrufers im Rahmen der Implementierung der **imdserviceprovider** -Schnittstelle prüft.


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

 

 




