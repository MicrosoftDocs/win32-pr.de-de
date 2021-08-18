---
title: Grundlagen der Anwendung
description: Grundlagen der Anwendung
ms.assetid: 5593d27e-e97d-4f03-99ff-aee856abec8e
keywords:
- Windows Media Format SDK, GRUNDLAGEN DER DRM-Anwendung
- Digitale Rechteverwaltung (Digital Rights Management, DRM), Anwendungsgrundlage
- DRM (Digital Rights Management), Anwendungsgrundlage
- Digital Rights Management (DRM), WMDRMStartup-Funktion
- DRM (Digital Rights Management), WMDRMStartup-Funktion
- WMDRMStartup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8356160565754764ac71cb152799a0fd9d1530e6e6969dc7a56e203b7504645d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086206"
---
# <a name="application-basics"></a>Grundlagen der Anwendung

Es gibt einige zusätzliche Verarbeitungsvorgänge, die Sie für jede Anwendung ausführen müssen, die die erweiterten APIs Windows Media DRM-Client verwendet. In diesem Thema werden die Anforderungen für eine einfache Anwendung beschrieben.

Zunächst müssen Sie die erweiterten APIs Windows Media DRM-Clients initialisieren, indem Sie die [**WMDRMStartup-Funktion**](wmdrmstartup.md) aufrufen. Die Objekte des SDK sind COM-Objekte, aber Sie müssen **CoIntialize** nicht aufrufen, da die **WMDRMStatup-Funktion** COM für Sie initialisiert.

> [!Note]  
> Das Windows Media Format SDK verwendet nur eine Teilmenge von COM. Wenn Sie also andere COM-Objekte als die in der erweiterten API des Windows Media DRM-Clients verwenden, müssen Sie weiterhin **CoInitialize aufrufen.**

 

Alle Objekte der erweiterten APIs des Windows Media DRM-Clients werden mit Hilfsfunktionen und -methoden erstellt. Sie müssen nicht **CoCreateInstance aufrufen, um** ein Objekt zu erstellen. Die erste Schnittstelle zum Instanziieren für jede Anwendung, die das SDK verwendet, ist [**IWMDRMProvider,**](iwmdrmprovider.md)mit dem Sie alle anderen Basisschnittstellen instanziieren können. Um eine Instanz von **IWMDRMProvider zu erhalten,** müssen Sie [**entweder WMDRMCreateProvider**](wmdrmcreateprovider.md) oder [**WMDRMCreateProtectedProvider aufrufen.**](wmdrmcreateprotectedprovider.md) Der Unterschied zwischen diesen Funktionen ist, dass **WMDRMCreateProvider** ein Objekt erstellt, das wiederum nur Objekte erstellen kann, die keine Methoden unterstützen, die die Stubbibliothek erfordern.

Nachdem Sie über eine Instanz von **IWMDRMProvider** verfügen, können Sie die anderen benötigten Objekte erstellen, indem Sie [**IWMDRMProvider::CreateObject aufrufen.**](iwmdrmprovider-createobject.md)

Wenn Sie bereit sind, Ihre Anwendung zu beenden, müssen Sie die DRM-Subsystemressourcen durch Aufrufen der [**WMDRMShutdown-Funktion**](wmdrmshutdown.md) frei geben. Diese Funktion fährt auch COM für Sie herunter.

Im folgenden Codebeispiel wird veranschaulicht, wie eine Anwendung initialisiert und beendet wird, die die erweiterten APIs Windows Media DRM-Client verwendet.


```C++
#include <wmdrmsdk.h>
// TODO: Include other headers here as needed.

// This example demonstrates the code required in a single, simple
// main function. You will most likely break this code up into appropriate
// functions.
void main(void)
{
    HRESULT hr = S_OK;

    IWMDRMProvider*     pProvider     = NULL;
    // For the sake of example, this code will instantiate the
    //  IWMDRMLicenseQuery interface. The process is the same for the
    //  other base interfaces.
    IWMDRMLicenseQuery* pLicenseQuery = NULL;

    // Initialize the DRM subsystem.
    hr = WMDRMStartup();

    // Create a provider object, that can be used to create the other
    //  objects.
    if (SUCCEEDED(hr))
    {
        hr = WMDRMCreateProvider(&pProvider);
    }

    if(SUCCEEDED(hr))
    {
        hr = pProvider->CreateObject(
            IID_IWMDRMLicenseQuery, 
            (void**)&pLicenseQuery);
    }

    // TODO: Use the methods of IWMDRMLicenseQuery as required.

    // Cleanup and shutdown.
    SAFE_RELEASE(pLicenseQuery);
    SAFE_RELEASE(pProvider);

    hr = WMDRMShutdown();
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erste Schritte**](drm-getting-started.md)
</dt> </dl>

 

 




