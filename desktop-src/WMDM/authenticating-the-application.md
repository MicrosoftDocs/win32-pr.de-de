---
title: Authentifizieren der Anwendung
description: Authentifizieren der Anwendung
ms.assetid: 011815fa-d55c-4abc-9ec8-55d754827342
keywords:
- Windows Media-Device Manager, Authentifizierung
- Device Manager, Authentifizierung
- Programmier Handbuch, Authentifizierung
- Desktop Anwendungen, Authentifizierung
- Erstellen von Windows Media Device Manager-Anwendungen, Authentifizierung
- authentication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7779cdbb874278e6b62517cc2c1983dd2ce8fa1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339886"
---
# <a name="authenticating-the-application"></a>Authentifizieren der Anwendung

Der erste Schritt, den Ihre Anwendung ausführen muss, ist die-Authentifizierung. Bei der Authentifizierung wird die Identität der Anwendung für Windows Media Device Manager überprüft. Nachdem Sie die Anwendung authentifiziert haben, können Sie **QueryInterface** zum Abrufen der Stamm- [**iwmdevicemanager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) -Schnittstelle abrufen, die für andere erforderliche Schnittstellen abgefragt werden kann, die selbst für alle anderen Schnittstellen abgefragt werden können. Die Authentifizierung muss beim Start nur einmal erfolgen.

Führen Sie die folgenden Schritte aus, um Ihre Anwendung zu authentifizieren:

1.  CoCreate the **mediadevmgr** Object (Class ID mediadevmgr) und Request an eine [**icomponentauthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) -Schnittstelle.
2.  Erstellen Sie ein [csecurechannelclient](csecurechannelclient-class.md) -Objekt, um die Authentifizierung zu verarbeiten.
3.  Übergeben Sie den Anwendungs Schlüssel, und übertragen Sie das Zertifikat an das sichere Kanal Objekt. Sie können den im folgenden Beispielcode gezeigten Dummy-Schlüssel/-Zertifikat verwenden, um grundlegende Funktionen von SDK-Funktionen zu erhalten. Um jedoch eine vollständige Funktionalität zu erhalten (wichtig für das Übergeben von Dateien an und vom Gerät), müssen Sie einen Schlüssel und ein Zertifikat von Microsoft anfordern, wie unter [Tools for Development (Tools für die Entwicklung](tools-for-development.md)) beschrieben.
4.  Übergeben Sie die **icomponentauthenticate** -Schnittstelle, die Sie in Schritt 1 erstellt haben, an das sichere Channel-Objekt.
5.  Wenden Sie [**csecurechannelclient:: authentifizieren**](/previous-versions/ms983906(v=msdn.10)) an, um Ihre Anwendung zu authentifizieren.
6.  Fragen Sie **icomponentauthenticate** für die **iwmtovicemanager** -Schnittstelle ab.

Diese Schritte sind im folgenden C++-Code dargestellt.


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

[**Erstellen einer Windows Media Device Manager-Anwendung**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 