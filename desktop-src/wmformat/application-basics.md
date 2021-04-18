---
title: Grundlagen der Anwendung
description: Grundlagen der Anwendung
ms.assetid: 5593d27e-e97d-4f03-99ff-aee856abec8e
keywords:
- Windows Media-Format-SDK, DRM-Anwendungs Grundlagen
- Digital Rights Management (DRM), Grundlagen der Anwendung
- DRM (Digital Rights Management), Grundlagen der Anwendung
- Digital Rights Management (DRM), wmdrmstartup-Funktion
- DRM (Digital Rights Management), wmdrmstartup-Funktion
- Wmdrmstartup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182a9e54e077c174c4f4cbe74ba392aa44ce5112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206310"
---
# <a name="application-basics"></a>Grundlagen der Anwendung

Für jede Anwendung, die die erweiterten APIs des Windows Media DRM-Clients verwendet, müssen zusätzliche Verarbeitungsschritte durchgeführt werden. In diesem Thema werden die Anforderungen für eine einfache Anwendung beschrieben.

Zunächst müssen Sie die erweiterten APIs des Windows Media DRM-Clients initialisieren, indem Sie die [**wmdrmstartup**](wmdrmstartup.md) -Funktion aufrufen. Bei den Objekten des SDK handelt es sich um COM-Objekte, aber Sie müssen **CoInitialize** nicht aufrufen, da die **wmdrmstatuup** -Funktion com für Sie initialisiert.

> [!Note]  
> Das Windows Media-Format SDK verwendet nur eine Teilmenge von com. Wenn Sie also COM-Objekte verwenden, die nicht in der erweiterten API des Windows Media DRM-Clients verwendet werden, müssen Sie immer noch **CoInitialize** aufruft.

 

Alle Objekte der erweiterten APIs des Windows Media DRM-Clients werden mithilfe von Hilfsfunktionen und-Methoden erstellt. Sie müssen niemals **cokreateinstance** aufrufen, um ein Objekt zu erstellen. Die erste Schnittstelle zum Instanziieren für jede Anwendung, die das SDK verwendet, ist [**iwmdrmprovider**](iwmdrmprovider.md), das Sie verwenden können, um alle anderen Basis Schnittstellen zu instanziieren. Um eine Instanz von **iwmdrmprovider** abzurufen, müssen Sie entweder [**wmdrmkreateprovider**](wmdrmcreateprovider.md) oder [**wmdrmkreateprotectedprovider**](wmdrmcreateprotectedprovider.md)aufrufen. Der Unterschied zwischen diesen Funktionen besteht darin, dass **wmdrmkreateprovider** ein Objekt erstellt, das wiederum nur Objekte erstellen kann, die keine Methoden unterstützen, die die stubbibliothek benötigen.

Nachdem Sie über eine Instanz von **iwmdrmprovider** verfügen, können Sie die anderen Objekte erstellen, die Sie benötigen, indem Sie [**iwmdrmprovider:: CreateObject**](iwmdrmprovider-createobject.md)aufrufen.

Wenn Sie bereit sind, die Anwendung zu beenden, müssen Sie die DRM-Subsystem-Ressourcen freigeben, indem Sie die [**wmdrmshutdown**](wmdrmshutdown.md) -Funktion aufrufen. Diese Funktion wird auch com für Sie heruntergefahren.

Im folgenden Codebeispiel wird veranschaulicht, wie Sie eine Anwendung, die die erweiterten APIs des Windows Media DRM-Clients verwendet, initialisieren und beenden.


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

[**Einstieg**](drm-getting-started.md)
</dt> </dl>

 

 




