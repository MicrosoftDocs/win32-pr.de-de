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
# <a name="testing-whether-a-graphics-driver-supports-copp"></a>Testen, ob ein Grafiktreiber COPP unterstützt

Mit dem Certified Output Protection Protocol (COPP) kann eine Anwendung Videoinhalte während der Übertragung von der Grafikkarte zum Anzeigegerät schützen. Wenn ein Grafiktreiber COPP unterstützt, enthält der Treiber eine von Microsoft signierte Zertifikatskette, die den Treiber authentifiziert. Wiedergabe Anwendungen, die COPP zum Erzwingen von Inhalts Schutz verwenden, müssen die Zertifikat Kette validieren, um sicherzustellen, dass der Treiber nicht manipuliert wurde.

Möglicherweise möchten Sie jedoch überprüfen, ob ein Grafiktreiber COPP unterstützt, ohne das Zertifikat zu validieren. Wenn ein digitaler Medienanbieter z. b. eine Digital Rights Management-Lizenz (DRM) ausgibt, möchte er möglicherweise überprüfen, ob der Benutzer über einen COPP-fähigen Grafiktreiber verfügt. Der Anbieter muss COPP nicht durchsetzen, wenn er die Lizenz ausgibt. Es muss nur getestet werden, ob der Treiber COPP unterstützt.

Der folgende Code zeigt, wie Sie testen können, ob ein Treiber COPP unterstützt. Die Anwendung muss den Namen einer Videodatei übergeben, die verwendet wird, um den Treiber zu testen. Dies ist erforderlich, da der Filter für den Video Mischungs Renderer in Microsoft® DirectShow® eine COPP-Sitzung erst initialisiert, wenn der Filter verbunden ist. Diese Funktion kann in einer Client Anwendung enthalten sein, um zu überprüfen, ob der Treiber COPP ausführen kann.

> [!Note]  
> Wenn der Computer des Benutzers über zwei Grafikkarten verfügt, testet diese Funktion den Treiber auf die primäre Grafikkarte, jedoch nicht auf die sekundäre Grafikkarte.

 


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

[Verwenden des zertifizierten Ausgabe Schutz Protokolls](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



