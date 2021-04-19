---
description: Testen, ob ein Grafiktreiber COPP unterstützt
ms.assetid: e3e1c795-5cfa-4e4b-86aa-948dd2bf91a4
title: Testen, ob ein Grafiktreiber COPP unterstützt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f98a5bfc3f577d1acb45969ec5d10503ae87b27a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360739"
---
# <a name="testing-whether-a-graphics-driver-supports-copp"></a><span data-ttu-id="a9d68-103">Testen, ob ein Grafiktreiber COPP unterstützt</span><span class="sxs-lookup"><span data-stu-id="a9d68-103">Testing Whether a Graphics Driver Supports COPP</span></span>

<span data-ttu-id="a9d68-104">Mit dem Certified Output Protection Protocol (COPP) kann eine Anwendung Videoinhalte während der Übertragung von der Grafikkarte zum Anzeigegerät schützen.</span><span class="sxs-lookup"><span data-stu-id="a9d68-104">Certified Output Protection Protocol (COPP) enables an application to protect video content as it travels from the video card to the display device.</span></span> <span data-ttu-id="a9d68-105">Wenn ein Grafiktreiber COPP unterstützt, enthält der Treiber eine von Microsoft signierte Zertifikatskette, die den Treiber authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="a9d68-105">If a graphics driver supports COPP, the driver holds a certificate chain, signed by Microsoft, authenticating the driver.</span></span> <span data-ttu-id="a9d68-106">Wiedergabe Anwendungen, die COPP zum Erzwingen von Inhalts Schutz verwenden, müssen die Zertifikat Kette validieren, um sicherzustellen, dass der Treiber nicht manipuliert wurde.</span><span class="sxs-lookup"><span data-stu-id="a9d68-106">Playback applications that use COPP to enforce content protection must validate the certificate chain to ensure that the driver has not been tampered with.</span></span>

<span data-ttu-id="a9d68-107">Möglicherweise möchten Sie jedoch überprüfen, ob ein Grafiktreiber COPP unterstützt, ohne das Zertifikat zu validieren.</span><span class="sxs-lookup"><span data-stu-id="a9d68-107">However, you might want to check whether a graphics driver supports COPP, without validating the certificate.</span></span> <span data-ttu-id="a9d68-108">Wenn ein digitaler Medienanbieter z. b. eine Digital Rights Management-Lizenz (DRM) ausgibt, möchte er möglicherweise überprüfen, ob der Benutzer über einen COPP-fähigen Grafiktreiber verfügt.</span><span class="sxs-lookup"><span data-stu-id="a9d68-108">For example, when a digital media provider issues a digital rights management (DRM) license, it might want to check whether the user has a COPP-enabled graphics driver.</span></span> <span data-ttu-id="a9d68-109">Der Anbieter muss COPP nicht durchsetzen, wenn er die Lizenz ausgibt. Es muss nur getestet werden, ob der Treiber COPP unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a9d68-109">The provider does not need to enforce COPP at the time it issues the license; it only needs to test whether the driver supports COPP.</span></span>

<span data-ttu-id="a9d68-110">Der folgende Code zeigt, wie Sie testen können, ob ein Treiber COPP unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a9d68-110">The following code shows how to test whether a driver supports COPP.</span></span> <span data-ttu-id="a9d68-111">Die Anwendung muss den Namen einer Videodatei übergeben, die verwendet wird, um den Treiber zu testen.</span><span class="sxs-lookup"><span data-stu-id="a9d68-111">The application must pass in the name of a video file that will be used to test the driver.</span></span> <span data-ttu-id="a9d68-112">Dies ist erforderlich, da der Filter für den Video Mischungs Renderer in Microsoft® DirectShow® eine COPP-Sitzung erst initialisiert, wenn der Filter verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="a9d68-112">This is required because the Video Mixing Renderer filter in Microsoft® DirectShow® does not initialize a COPP session until the filter is connected.</span></span> <span data-ttu-id="a9d68-113">Diese Funktion kann in einer Client Anwendung enthalten sein, um zu überprüfen, ob der Treiber COPP ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="a9d68-113">This function can be included in a client application to check if the driver is capable of running COPP.</span></span>

> [!Note]  
> <span data-ttu-id="a9d68-114">Wenn der Computer des Benutzers über zwei Grafikkarten verfügt, testet diese Funktion den Treiber auf die primäre Grafikkarte, jedoch nicht auf die sekundäre Grafikkarte.</span><span class="sxs-lookup"><span data-stu-id="a9d68-114">If the user's computer has two graphics cards, this function tests the driver for the primary graphics card, but not the secondary graphics card.</span></span>

 


```C++
#include <dshow.h>
// Link to strmiids.lib

#define SAFE_RELEASE(p) if (NULL != (p)) { (p)->Release(); (p) = NULL; }
#define CHECK_HR(hr) if (FAILED(hr)) { goto done; }

enum COPPSupport 
{
    SUPPORTS_COPP,
    DOES_NOT_SUPPORT_COPP,
    CANNOT_DETERMINE_COPP_SUPPORT
};

//------------------------------------------------------------------------
// Name:        IsDriverCoppEnabled
// Description: Test whether the user's graphics driver supports
//              COPP.
// wszTestFile: Name of a video file to use for testing.
//
// If this method returns the value SUPPORTS_COPP, it does *not* guarantee 
// that the driver is a valid COPP-enabled driver. If you want to use COPP 
// to enforce video output protection, the application *must* validate 
// the certificate returned by the KeyExchange method. 
// 
// The purpose of this function is only to test whether the driver 
// claims to support COPP. 
//------------------------------------------------------------------------

COPPSupport IsDriverCoppEnabled(const WCHAR *wszTestFile)
{
    COPPSupport SupportResult = CANNOT_DETERMINE_COPP_SUPPORT; 

    IGraphBuilder *pGB = NULL;
    IBaseFilter *pRenderer = NULL;
    IAMCertifiedOutputProtection  *pCOPPDevice = NULL;
    BYTE *pbCertificate = NULL;
    GUID  RandomValue = GUID_NULL;
    ULONG cbCertificateLength = NULL;
    
    HRESULT hr = S_OK;

    CHECK_HR(hr = CoInitializeEx(NULL, COINIT_MULTITHREADED));
   
    // Create the Filter Graph Manager.
    CHECK_HR(hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void**)&pGB));

    // Create the VMR-9. 
    hr = CoCreateInstance(CLSID_VideoMixingRenderer9,
        NULL, CLSCTX_INPROC_SERVER, IID_IBaseFilter, 
        (void**)&pRenderer
        ));

    if (FAILED(hr))
    {
        // Try the VMR-7 instead.
        CHECK_HR(hr = CoCreateInstance(CLSID_VideoMixingRenderer,
                NULL, CLSCTX_INPROC, IID_IBaseFilter, 
                (void**)&pRenderer
                ));
    }

    // Add the VMR to the filter graph.
    CHECK_HR(hr = pGB->AddFilter(pRenderer, L"Video Renderer"));

    // Build a default playback graph.
    CHECK_HR(hr = pGB->RenderFile(wszTestFile, NULL));

    // Query for IAMCertifiedOutputProtection.
    CHECK_HR(hr = pRenderer->QueryInterface(IID_IAMCertifiedOutputProtection,
            (void**)&pCOPPDevice));

    // Get the driver's COPP certificate.
    hr = pCOPPDevice->KeyExchange(&RandomValue, &pbCertificate,
        &cbCertificateLength);

    if (SUCCEEDED(hr))
    {
        SupportResult = SUPPORTS_COPP;
    }
    else
    {
        SupportResult = DOES_NOT_SUPPORT_COPP;
    }

done:
    // Clean up.
    CoTaskMemFree(pbCertificate);
    SAFE_RELEASE(pCOPPDevice);
    SAFE_RELEASE(pRenderer);
    SAFE_RELEASE(pGB);
    CoUninitialize();

    return SupportResult;
} 

```



## <a name="related-topics"></a><span data-ttu-id="a9d68-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a9d68-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9d68-116">Verwenden des zertifizierten Ausgabe Schutz Protokolls</span><span class="sxs-lookup"><span data-stu-id="a9d68-116">Using Certified Output Protection Protocol</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



