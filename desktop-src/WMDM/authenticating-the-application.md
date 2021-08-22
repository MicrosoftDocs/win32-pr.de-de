---
title: Authentifizieren der Anwendung
description: Authentifizieren der Anwendung
ms.assetid: 011815fa-d55c-4abc-9ec8-55d754827342
keywords:
- Windows Medien Geräte-Manager,Authentifizierung
- Geräte-Manager,Authentifizierung
- Programmierhandbuch,Authentifizierung
- Desktopanwendungen,Authentifizierung
- Erstellen Windows Media Geräte-Manager Anwendungen,Authentifizierung
- authentication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b67ad7c603bbfd3a56667bfcfe8742775c8ae5683888d72661e0a0974aa5358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586735"
---
# <a name="authenticating-the-application"></a>Authentifizieren der Anwendung

Der erste Schritt, den Ihre Anwendung ausführen muss, ist die Authentifizierung. Die Authentifizierung überprüft die Identität der Anwendung, um Windows Medien Geräte-Manager. Nachdem Sie Ihre Anwendung authentifiziert haben, können Sie **QueryInterface** aufrufen, um die [**Stammschnittstelle IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) abzurufen, die nach anderen erforderlichen Schnittstellen abgefragt werden kann, die selbst für alle anderen Schnittstellen abgefragt werden können. Die Authentifizierung muss beim Start nur einmal stattfinden.

Führen Sie die folgenden Schritte aus, um Ihre Anwendung zu authentifizieren:

1.  Erstellen Sie das **MediaDevMgr-Objekt** (Klassen-ID MediaDevMgr), und fordern Sie eine [**IComponentAuthenticate-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) an.
2.  Erstellen Sie ein [CSecureChannelClient-Objekt,](csecurechannelclient-class.md) um die Authentifizierung zu verarbeiten.
3.  Übergeben Sie Ihren Anwendungsschlüssel, und übertragen Sie das Zertifikat an das Objekt des sicheren Kanals. Sie können den Im folgenden Beispielcode gezeigten Dummyschlüssel bzw. das Dummyzertifikat verwenden, um grundlegende Funktionen von SDK-Funktionen zu erhalten. Um jedoch die vollständige Funktionalität (wichtig für die Übergabe von Dateien an und vom Gerät) zu erhalten, müssen Sie einen Schlüssel und ein Zertifikat von Microsoft anfordern, wie unter [Tools für die Entwicklung beschrieben.](tools-for-development.md)
4.  Übergeben Sie **die IComponentAuthenticate-Schnittstelle,** die Sie in Schritt 1 erstellt haben, an das Objekt des sicheren Kanals.
5.  Rufen [**Sie CSecureChannelClient::Authenticate auf,**](/previous-versions/ms983906(v=msdn.10)) um Ihre Anwendung zu authentifizieren.
6.  Fragen **Sie IComponentAuthenticate** für die **IWMDeviceManager-Schnittstelle** ab.

Diese Schritte werden im folgenden C++-Code gezeigt.


```C++
HRESULT CWMDMController::Authenticate()
{
    // Use a dummy key/certificate pair to allow basic functionality.
    // An authentic keypair is required for full SDK functionality.
    BYTE abPVK[] = {0x00};
    BYTE abCert[] = {0x00};
    HRESULT hr;
    CComPtr<IComponentAuthenticate> pAuth;

    // Create the WMDM object and acquire 
    // its authentication interface.
    hr = CoCreateInstance(
        __uuidof(MediaDevMgr),
        NULL,
        CLSCTX_INPROC_SERVER,
        __uuidof(IComponentAuthenticate),
        (void**)&pAuth);

    if (FAILED(hr)) return hr;

    // Create the secure channel client class needed to authenticate the application.
    // We'll use a global member variable to hold the secure channel client
    // in case we need to handle encryption, decryption, or MAC verification
    // during this session.
    m_pSAC = new CSecureChannelClient;
    if (m_pSAC == NULL) return E_FAIL;

    // Send the application's transfer certificate and the associated 
    // private key to the secure channel client.
    hr = m_pSAC->SetCertificate(
        SAC_CERT_V1,
        (BYTE *)abCert, sizeof(abCert),
        (BYTE *)abPVK,  sizeof(abPVK));
    if (FAILED(hr)) return hr;
            
    // Send the authentication interface we created to the secure channel 
    // client and authenticate the application with the V1 protocol.
    // (This is the only protocol currently supported.)
    m_pSAC->SetInterface(pAuth);
    hr = m_pSAC->Authenticate(SAC_PROTOCOL_V1);
    if (FAILED(hr)) return hr;

    // Authentication succeeded, so we can use WMDM.
    // Query for the root WMDM interface.
    hr = pAuth->QueryInterface( __uuidof(IWMDeviceManager), (void**)&m_IWMDMDeviceMgr);

    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen einer Windows Media Geräte-Manager Anwendung**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 