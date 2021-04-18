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
# <a name="application-basics"></a><span data-ttu-id="fc8ec-109">Grundlagen der Anwendung</span><span class="sxs-lookup"><span data-stu-id="fc8ec-109">Application Basics</span></span>

<span data-ttu-id="fc8ec-110">Für jede Anwendung, die die erweiterten APIs des Windows Media DRM-Clients verwendet, müssen zusätzliche Verarbeitungsschritte durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fc8ec-110">There is some extra processing that you must perform for any application that uses the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="fc8ec-111">In diesem Thema werden die Anforderungen für eine einfache Anwendung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fc8ec-111">This topic describes the requirements for a simple application.</span></span>

<span data-ttu-id="fc8ec-112">Zunächst müssen Sie die erweiterten APIs des Windows Media DRM-Clients initialisieren, indem Sie die [**wmdrmstartup**](wmdrmstartup.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fc8ec-112">First, you must initialize the Windows Media DRM Client Extended APIs by calling the [**WMDRMStartup**](wmdrmstartup.md) function.</span></span> <span data-ttu-id="fc8ec-113">Bei den Objekten des SDK handelt es sich um COM-Objekte, aber Sie müssen **CoInitialize** nicht aufrufen, da die **wmdrmstatuup** -Funktion com für Sie initialisiert.</span><span class="sxs-lookup"><span data-stu-id="fc8ec-113">The objects of the SDK are COM objects, but you do not need to call **CoIntialize**, because the **WMDRMStatup** function initializes COM for you.</span></span>

> [!Note]  
> <span data-ttu-id="fc8ec-114">Das Windows Media-Format SDK verwendet nur eine Teilmenge von com. Wenn Sie also COM-Objekte verwenden, die nicht in der erweiterten API des Windows Media DRM-Clients verwendet werden, müssen Sie immer noch **CoInitialize** aufruft.</span><span class="sxs-lookup"><span data-stu-id="fc8ec-114">The Windows Media Format SDK uses only a subset of COM, so if you use COM objects other than those in the Windows Media DRM Client Extended API, you must still call **CoInitialize**.</span></span>

 

<span data-ttu-id="fc8ec-115">Alle Objekte der erweiterten APIs des Windows Media DRM-Clients werden mithilfe von Hilfsfunktionen und-Methoden erstellt.</span><span class="sxs-lookup"><span data-stu-id="fc8ec-115">All of the objects of the Windows Media DRM Client Extended APIs are created using helper functions and methods.</span></span> <span data-ttu-id="fc8ec-116">Sie müssen niemals **cokreateinstance** aufrufen, um ein Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fc8ec-116">You never need to call **CoCreateInstance** to create an object.</span></span> <span data-ttu-id="fc8ec-117">Die erste Schnittstelle zum Instanziieren für jede Anwendung, die das SDK verwendet, ist [**iwmdrmprovider**](iwmdrmprovider.md), das Sie verwenden können, um alle anderen Basis Schnittstellen zu instanziieren.</span><span class="sxs-lookup"><span data-stu-id="fc8ec-117">The first interface to instantiate for any application that uses the SDK is [**IWMDRMProvider**](iwmdrmprovider.md), which you can use to instantiate all of the other base interfaces.</span></span> <span data-ttu-id="fc8ec-118">Um eine Instanz von **iwmdrmprovider** abzurufen, müssen Sie entweder [**wmdrmkreateprovider**](wmdrmcreateprovider.md) oder [**wmdrmkreateprotectedprovider**](wmdrmcreateprotectedprovider.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fc8ec-118">To get an instance of **IWMDRMProvider**, you must call either [**WMDRMCreateProvider**](wmdrmcreateprovider.md) or [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md).</span></span> <span data-ttu-id="fc8ec-119">Der Unterschied zwischen diesen Funktionen besteht darin, dass **wmdrmkreateprovider** ein Objekt erstellt, das wiederum nur Objekte erstellen kann, die keine Methoden unterstützen, die die stubbibliothek benötigen.</span><span class="sxs-lookup"><span data-stu-id="fc8ec-119">The difference between these functions is that **WMDRMCreateProvider** creates an object that can in turn create only objects that do not support methods that require the stub library.</span></span>

<span data-ttu-id="fc8ec-120">Nachdem Sie über eine Instanz von **iwmdrmprovider** verfügen, können Sie die anderen Objekte erstellen, die Sie benötigen, indem Sie [**iwmdrmprovider:: CreateObject**](iwmdrmprovider-createobject.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fc8ec-120">After you have an instance of **IWMDRMProvider**, you can create the other objects that you need by calling [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span>

<span data-ttu-id="fc8ec-121">Wenn Sie bereit sind, die Anwendung zu beenden, müssen Sie die DRM-Subsystem-Ressourcen freigeben, indem Sie die [**wmdrmshutdown**](wmdrmshutdown.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fc8ec-121">When you are ready to exit your application, you must release the DRM subsystem resources by calling the [**WMDRMShutdown**](wmdrmshutdown.md) function.</span></span> <span data-ttu-id="fc8ec-122">Diese Funktion wird auch com für Sie heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="fc8ec-122">This function also shuts down COM for you.</span></span>

<span data-ttu-id="fc8ec-123">Im folgenden Codebeispiel wird veranschaulicht, wie Sie eine Anwendung, die die erweiterten APIs des Windows Media DRM-Clients verwendet, initialisieren und beenden.</span><span class="sxs-lookup"><span data-stu-id="fc8ec-123">The following code example demonstrates how to initialize and conclude an application that uses the Windows Media DRM Client Extended APIs.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="fc8ec-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fc8ec-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc8ec-125">**Einstieg**</span><span class="sxs-lookup"><span data-stu-id="fc8ec-125">**Getting Started**</span></span>](drm-getting-started.md)
</dt> </dl>

 

 




