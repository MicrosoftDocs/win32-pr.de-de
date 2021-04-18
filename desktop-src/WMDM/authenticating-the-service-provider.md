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
# <a name="authenticating-the-service-provider"></a><span data-ttu-id="d9e8d-109">Authentifizieren des Dienstanbieters</span><span class="sxs-lookup"><span data-stu-id="d9e8d-109">Authenticating the Service Provider</span></span>

<span data-ttu-id="d9e8d-110">Um von Windows Media Device Manager zugänglich zu sein, muss ein Dienstanbieter die [**icomponentauthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) -Schnittstelle erben und implementieren.</span><span class="sxs-lookup"><span data-stu-id="d9e8d-110">To be accessible from Windows Media Device Manager, a service provider must inherit and implement the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface.</span></span>

<span data-ttu-id="d9e8d-111">Ein Dienstanbieter führt die folgenden Schritte aus, um sich selbst zu authentifizieren:</span><span class="sxs-lookup"><span data-stu-id="d9e8d-111">To authenticate itself, a service provider performs the following steps:</span></span>

1.  <span data-ttu-id="d9e8d-112">Bei der Instanziierung wird ein neues globales [csecurechannelserver](csecurechannelserver-class.md) -Objekt erstellt und das Zertifikat und die Schlüsselwerte aus seiner Schlüsseldatei festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d9e8d-112">On instantiation, it creates a new global [CSecureChannelServer](csecurechannelserver-class.md) object and sets the certificate and key values from its key file.</span></span>
2.  <span data-ttu-id="d9e8d-113">Es implementiert die [**icomponentauthenticate:: sacauth**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacauth) -und die [**icomponentauthenticate:: sacgetprotokolls**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacgetprotocols) -Methode, indem die Parameter einfach an das globale csecurechannelserver-Element übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="d9e8d-113">It implements the [**IComponentAuthenticate::SACAuth**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacauth) and [**IComponentAuthenticate::SACGetProtocols**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacgetprotocols) methods by simply passing the parameters into its global CSecureChannelServer member.</span></span>
3.  <span data-ttu-id="d9e8d-114">Vor der Behandlung implementierter Windows Media Device Manager-Methoden muss der Dienstanbieter die Authentifizierung des Aufrufers durch Aufrufen von csecurechannelserver:: fisauthenticated überprüfen und einen Fehler auftreten, wenn der Aufrufer nicht authentifiziert ist.</span><span class="sxs-lookup"><span data-stu-id="d9e8d-114">Before handling any implemented Windows Media Device Manager methods, the service provider must verify the caller's authentication by calling CSecureChannelServer::fIsAuthenticated, and failing if the caller is not authenticated.</span></span>

<span data-ttu-id="d9e8d-115">Diese Schritte sind in den folgenden C++ Beispielen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9e8d-115">These steps are shown in the following C++ examples.</span></span>

<span data-ttu-id="d9e8d-116">**Erstellen des csecurechannelserver-Objekts**</span><span class="sxs-lookup"><span data-stu-id="d9e8d-116">**Creating the CSecureChannelServer object**</span></span>


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



<span data-ttu-id="d9e8d-117">**Implementieren der icomponentauthenticate-Methoden**</span><span class="sxs-lookup"><span data-stu-id="d9e8d-117">**Implementing the IComponentAuthenticate methods**</span></span>


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



<span data-ttu-id="d9e8d-118">**Überprüfen der Authentifizierung des Aufrufers**</span><span class="sxs-lookup"><span data-stu-id="d9e8d-118">**Verifying the caller's authentication**</span></span>

<span data-ttu-id="d9e8d-119">Das folgende Codebeispiel zeigt, wie ein Dienstanbieter die Authentifizierung des Aufrufers im Rahmen der Implementierung der **imdserviceprovider** -Schnittstelle prüft.</span><span class="sxs-lookup"><span data-stu-id="d9e8d-119">The following code example shows a service provider checking the caller's authentication as part of its implementation of the **IMDServiceProvider** interface.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d9e8d-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d9e8d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9e8d-121">**Erstellen eines Dienstanbieters**</span><span class="sxs-lookup"><span data-stu-id="d9e8d-121">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




