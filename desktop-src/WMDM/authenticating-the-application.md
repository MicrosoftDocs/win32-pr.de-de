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
# <a name="authenticating-the-application"></a><span data-ttu-id="38527-109">Authentifizieren der Anwendung</span><span class="sxs-lookup"><span data-stu-id="38527-109">Authenticating the Application</span></span>

<span data-ttu-id="38527-110">Der erste Schritt, den Ihre Anwendung ausführen muss, ist die-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="38527-110">The first step your application must perform is authentication.</span></span> <span data-ttu-id="38527-111">Bei der Authentifizierung wird die Identität der Anwendung für Windows Media Device Manager überprüft.</span><span class="sxs-lookup"><span data-stu-id="38527-111">Authentication verifies the application's identity to Windows Media Device Manager.</span></span> <span data-ttu-id="38527-112">Nachdem Sie die Anwendung authentifiziert haben, können Sie **QueryInterface** zum Abrufen der Stamm- [**iwmdevicemanager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) -Schnittstelle abrufen, die für andere erforderliche Schnittstellen abgefragt werden kann, die selbst für alle anderen Schnittstellen abgefragt werden können.</span><span class="sxs-lookup"><span data-stu-id="38527-112">Once you authenticate your application, you can call **QueryInterface** to get the root [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) interface, which can be queried for other required interfaces, which can themselves be queried for all other interfaces.</span></span> <span data-ttu-id="38527-113">Die Authentifizierung muss beim Start nur einmal erfolgen.</span><span class="sxs-lookup"><span data-stu-id="38527-113">Authentication need only take place once, on startup.</span></span>

<span data-ttu-id="38527-114">Führen Sie die folgenden Schritte aus, um Ihre Anwendung zu authentifizieren:</span><span class="sxs-lookup"><span data-stu-id="38527-114">To authenticate your application, perform these steps:</span></span>

1.  <span data-ttu-id="38527-115">CoCreate the **mediadevmgr** Object (Class ID mediadevmgr) und Request an eine [**icomponentauthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="38527-115">CoCreate the **MediaDevMgr** object (class ID MediaDevMgr), and request an [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface.</span></span>
2.  <span data-ttu-id="38527-116">Erstellen Sie ein [csecurechannelclient](csecurechannelclient-class.md) -Objekt, um die Authentifizierung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="38527-116">Create a [CSecureChannelClient](csecurechannelclient-class.md) object to handle the authentication.</span></span>
3.  <span data-ttu-id="38527-117">Übergeben Sie den Anwendungs Schlüssel, und übertragen Sie das Zertifikat an das sichere Kanal Objekt.</span><span class="sxs-lookup"><span data-stu-id="38527-117">Pass your application key and transfer certificate to the secure channel object.</span></span> <span data-ttu-id="38527-118">Sie können den im folgenden Beispielcode gezeigten Dummy-Schlüssel/-Zertifikat verwenden, um grundlegende Funktionen von SDK-Funktionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="38527-118">You can use the dummy key/certificate shown in the following example code to get basic functionality from SDK functions.</span></span> <span data-ttu-id="38527-119">Um jedoch eine vollständige Funktionalität zu erhalten (wichtig für das Übergeben von Dateien an und vom Gerät), müssen Sie einen Schlüssel und ein Zertifikat von Microsoft anfordern, wie unter [Tools for Development (Tools für die Entwicklung](tools-for-development.md)) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="38527-119">However, to get full functionality (important for passing files to and from the device), you must request a key and certificate from Microsoft as described in [Tools for Development](tools-for-development.md).</span></span>
4.  <span data-ttu-id="38527-120">Übergeben Sie die **icomponentauthenticate** -Schnittstelle, die Sie in Schritt 1 erstellt haben, an das sichere Channel-Objekt.</span><span class="sxs-lookup"><span data-stu-id="38527-120">Pass the **IComponentAuthenticate** interface you created in step 1 to the secure channel object.</span></span>
5.  <span data-ttu-id="38527-121">Wenden Sie [**csecurechannelclient:: authentifizieren**](/previous-versions/ms983906(v=msdn.10)) an, um Ihre Anwendung zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="38527-121">Call [**CSecureChannelClient::Authenticate**](/previous-versions/ms983906(v=msdn.10)) to authenticate your application.</span></span>
6.  <span data-ttu-id="38527-122">Fragen Sie **icomponentauthenticate** für die **iwmtovicemanager** -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="38527-122">Query **IComponentAuthenticate** for the **IWMDeviceManager** interface.</span></span>

<span data-ttu-id="38527-123">Diese Schritte sind im folgenden C++-Code dargestellt.</span><span class="sxs-lookup"><span data-stu-id="38527-123">These steps are shown in the following C++ code.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="38527-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="38527-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38527-125">**Erstellen einer Windows Media Device Manager-Anwendung**</span><span class="sxs-lookup"><span data-stu-id="38527-125">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 