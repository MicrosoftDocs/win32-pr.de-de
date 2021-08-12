---
description: Testen, ob ein Grafiktreiber COPP unterstützt
ms.assetid: e3e1c795-5cfa-4e4b-86aa-948dd2bf91a4
title: Testen, ob ein Grafiktreiber COPP unterstützt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22280f880ba01a8e51acda74a2a46dff595d5569f885ce1da3a3631bacd8db06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651830"
---
# <a name="testing-whether-a-graphics-driver-supports-copp"></a>Testen, ob ein Grafiktreiber COPP unterstützt

Certified Output Protection Protocol (COPP) ermöglicht es einer Anwendung, Videoinhalte zu schützen, während sie von der Grafikkarte zum Anzeigegerät übertragen werden. Wenn ein Grafiktreiber COPP unterstützt, enthält der Treiber eine Von Microsoft signierte Zertifikatkette, die den Treiber authentifiziert. Wiedergabeanwendungen, die COPP zum Erzwingen des Inhaltsschutzes verwenden, müssen die Zertifikatkette überprüfen, um sicherzustellen, dass der Treiber nicht manipuliert wurde.

Möglicherweise möchten Sie jedoch überprüfen, ob ein Grafiktreiber COPP unterstützt, ohne das Zertifikat zu überprüfen. Wenn beispielsweise ein Anbieter digitaler Medien eine DRM-Lizenz (Digital Rights Management) aushing, kann er überprüfen, ob der Benutzer über einen COPP-fähigen Grafiktreiber verfügt. Der Anbieter muss COPP zum Zeitpunkt der Lizenzerzwingung nicht erzwingen. Er muss nur testen, ob der Treiber COPP unterstützt.

Der folgende Code zeigt, wie Sie testen, ob ein Treiber COPP unterstützt. Die Anwendung muss den Namen einer Videodatei übergeben, die zum Testen des Treibers verwendet wird. Dies ist erforderlich, da der Filter Video Mixing Renderer in Microsoft® DirectShow® eine COPP-Sitzung erst initialisiert, wenn der Filter verbunden ist. Diese Funktion kann in einer Clientanwendung enthalten sein, um zu überprüfen, ob der Treiber COPP ausführen kann.

> [!Note]  
> Wenn der Computer des Benutzers über zwei Grafikkarten verfügt, testet diese Funktion den Treiber auf die primäre Grafikkarte, aber nicht auf die sekundäre Grafikkarte.

 


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Certified Output Protection-Protokolls](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



