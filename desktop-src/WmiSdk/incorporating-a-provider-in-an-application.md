---
description: Beschreibt, wie der WMI-com-Anbieter als Komponente in einer Anwendung statt in den Prozess in WMI eingeschlossen wird. Dies wird als entkoppelter Anbieter bezeichnet und ist der empfohlene Typ des WMI-com-Anbieters, der für Windows 2000 und spätere Betriebssysteme erstellt werden soll.
ms.assetid: a502f0dd-9add-4ebd-bc25-743a55eb78ac
ms.tgt_platform: multiple
title: Einbinden eines Anbieters in eine Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb544cd3b04cc75cef026bb2e4d2e579b8dbf135
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104555651"
---
# <a name="incorporating-a-provider-in-an-application"></a><span data-ttu-id="f35d8-104">Einbinden eines Anbieters in eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="f35d8-104">Incorporating a Provider in an Application</span></span>

<span data-ttu-id="f35d8-105">Beim Erstellen einer Anwendung, die instrumentiert werden soll, besteht die bewährte Vorgehensweise darin, den Anbieter als Komponente in die Anwendung selbst einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="f35d8-105">When creating an application that is to be instrumented, the best practice is to include the provider as a component within the application itself.</span></span> <span data-ttu-id="f35d8-106">Mit dieser Vorgehensweise können Windows-Verwaltungsinstrumentation (WMI) direkt anstelle von indirekt über die Programm-API mit dem Dienstanbieter interagieren.</span><span class="sxs-lookup"><span data-stu-id="f35d8-106">This practice permits Windows Management Instrumentation (WMI) to interact with the service provider directly instead of indirectly through the program API.</span></span> <span data-ttu-id="f35d8-107">Wenn der Anbieter von WMI entkoppelt wird, wird die Anwendung auch von der Lebensdauer des Anbieters anstatt von WMI gesteuert.</span><span class="sxs-lookup"><span data-stu-id="f35d8-107">Decoupling the provider from WMI also puts the application in control of the provider lifespan, instead of WMI.</span></span> <span data-ttu-id="f35d8-108">Weitere Informationen zum Schreiben eines Anbieters, der im WMI-Prozess ausgeführt wird, finden [Sie unter Bereitstellen von Daten für WMI durch Schreiben eines Anbieters](supplying-data-to-wmi-by-writing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f35d8-108">For more information about writing a provider that runs in the WMI process, see [Supplying Data to WMI by Writing a Provider](supplying-data-to-wmi-by-writing-a-provider.md).</span></span> <span data-ttu-id="f35d8-109">Weitere Informationen zum Hostingmodell und den Sicherheitseinstellungen für den Anbieter finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="f35d8-109">For more information about hosting model and security settings for the provider, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

<span data-ttu-id="f35d8-110">Das folgende Diagramm veranschaulicht die Beziehung zwischen WMI, einem entkoppelten Anbieter und einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="f35d8-110">The following diagram illustrates the relationship between WMI, a decoupled provider, and an application.</span></span>

![Beziehung zwischen WMI, entkoppelten Anbieter und Anwendung](images/decoupledprov.png)

<span data-ttu-id="f35d8-112">Weitere Informationen über entkoppelte Anbieter Methoden finden Sie unter [**iwbementkopppledregistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar) und [**iwbementkopppledbasiceventprovider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider).</span><span class="sxs-lookup"><span data-stu-id="f35d8-112">For more information about decoupled provider methods, see [**IWbemDecoupledRegistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar) and [**IWbemDecoupledBasicEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider).</span></span>

> [!Note]  
> <span data-ttu-id="f35d8-113">Der entkoppelte Anbieter unterstützt Instanz, Methode, Ereignis Anbieter und Ereignisconsumer.</span><span class="sxs-lookup"><span data-stu-id="f35d8-113">The decoupled provider supports instance, method, event providers, and event consumers.</span></span> <span data-ttu-id="f35d8-114">Klassen-und Eigenschaften Anbieter werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f35d8-114">It does not support class and property providers.</span></span> <span data-ttu-id="f35d8-115">Weitere Informationen finden Sie unter [Schreiben eines Klassen Anbieters](writing-a-class-provider.md) und [Schreiben eines Eigenschafts Anbieters](writing-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f35d8-115">For more information, see [Writing a Class Provider](writing-a-class-provider.md) and [Writing a Property Provider](writing-a-property-provider.md).</span></span>

 

<span data-ttu-id="f35d8-116">Die Codebeispiele in diesem Thema erfordern die folgenden Verweise und \# include-Anweisungen, um ordnungsgemäß zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="f35d8-116">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="f35d8-117">Im folgenden Verfahren werden C++-Codebeispiele verwendet, um zu beschreiben, wie ein entkoppelter Anbieter in Ihre Anwendung integriert wird.</span><span class="sxs-lookup"><span data-stu-id="f35d8-117">The following procedure uses C++ code examples to describe how to incorporate a decoupled provider in your application.</span></span> <span data-ttu-id="f35d8-118">Die Initialisierungs Methode der Anwendung führt die folgenden Schritte aus, damit WMI nur mit einem registrierten entkoppelten Anbieter interagiert.</span><span class="sxs-lookup"><span data-stu-id="f35d8-118">The initialization method of the application performs the following steps so that WMI only interacts with a registered decoupled provider.</span></span>

<span data-ttu-id="f35d8-119">**So implementieren Sie einen entkoppelten Anbieter in einer C++-Anwendung**</span><span class="sxs-lookup"><span data-stu-id="f35d8-119">**To implement a decoupled provider in a C++ application**</span></span>

1.  <span data-ttu-id="f35d8-120">Initialisieren Sie die com-Bibliothek für die Verwendung durch den aufrufenden Thread.</span><span class="sxs-lookup"><span data-stu-id="f35d8-120">Initialize the COM library for use by the calling thread.</span></span>

    <span data-ttu-id="f35d8-121">Im folgenden Codebeispiel wird gezeigt, wie die com-Bibliothek initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="f35d8-121">The following code example shows how to initialize the COM library.</span></span>

    ```C++
    HRESULT hr = S_OK ;
    hr = CoInitializeEx (0, COINIT_MULTITHREADED );
    ```

    

2.  <span data-ttu-id="f35d8-122">Legen Sie die standardmäßige Prozess Sicherheitsstufe fest.</span><span class="sxs-lookup"><span data-stu-id="f35d8-122">Set the default process security level.</span></span>

    <span data-ttu-id="f35d8-123">Auf dieser Ebene wird die Sicherheitsstufe festgelegt, die von anderen Prozessen zum Zugreifen auf die Informationen des Client Prozesses erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f35d8-123">This level establishes the security level required of other processes to access the client process' information.</span></span> <span data-ttu-id="f35d8-124">Die Authentifizierungs Ebene sollte standardmäßig auf RPC- \_ C- \_ authn- \_ Ebene eingestellt sein \_ .</span><span class="sxs-lookup"><span data-stu-id="f35d8-124">The authentication level should be RPC\_C\_AUTHN\_LEVEL\_DEFAULT.</span></span> <span data-ttu-id="f35d8-125">Weitere Informationen finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="f35d8-125">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

    <span data-ttu-id="f35d8-126">Im folgenden Codebeispiel wird gezeigt, wie die Standard Sicherheitsstufe festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f35d8-126">The following code example shows how to set the default security level.</span></span>

    ```C++
    hr = CoInitializeSecurity (NULL, 
        -1, 
        NULL, 
        NULL,
        RPC_C_AUTHN_LEVEL_DEFAULT,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL, 
        EOAC_DYNAMIC_CLOAKING, 
        NULL);

    if (FAILED(hr))
    {
      CoUninitialize();
      cout << "Failed to initialize security. Error code = 0x"
           << hex << hr << endl;
      return;
    }
    ```

    

3.  <span data-ttu-id="f35d8-127">Registrieren Sie die entkoppelte Anbieter-Registrierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="f35d8-127">Register the decoupled provider registrar.</span></span>

    <span data-ttu-id="f35d8-128">Im folgenden Codebeispiel wird gezeigt, wie die entkoppelte Anbieter Registrierungsstelle registriert wird.</span><span class="sxs-lookup"><span data-stu-id="f35d8-128">The following code example shows how to register the decoupled provider registrar.</span></span>

    ```C++
    CLSID CLSID_WbemDecoupledRegistrar;
    IID IID_IWbemDecoupledRegistrar;
    IWbemDecoupledRegistrar *myRegistrar = NULL;

    hr = CoCreateInstance(CLSID_WbemDecoupledRegistrar,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IWbemDecoupledRegistrar,
                          (void**)&myRegistrar);
    if (SUCCEEDED(hr))
    {
        IUnknown *pIUnknown = NULL;
        // CMyProv is the class added for WMI instance / event provider
        HRESULT hr = CMyProv::CreateInstance(NULL,&pIUnknown);
        if ( SUCCEEDED(hr))
        {
            hr = myRegistrar->Register(0,
                NULL,
                NULL,
                NULL,
                L"root\\cimv2",
                L"DecoupledInstanceProvider",
                pIUnknown);

                pIUnknown->Release();
        }
    }

    if (FAILED (hr))
    {
        if ( myRegistrar )
        {
            myRegistrar->Release () ;
        }
    }
    ```

    

4.  <span data-ttu-id="f35d8-129">Registrieren Sie den entkoppelten Ereignis Anbieter.</span><span class="sxs-lookup"><span data-stu-id="f35d8-129">Register the decoupled event provider.</span></span>

    <span data-ttu-id="f35d8-130">Im folgenden Codebeispiel wird gezeigt, wie der entkoppelte Ereignis Anbieter registriert wird.</span><span class="sxs-lookup"><span data-stu-id="f35d8-130">The following code example shows how to register the decoupled event provider.</span></span>

    ```C++
    IWbemDecoupledBasicEventProvider *myEvtRegistrar;

    // -- Create an instance of IWbemDecoupledEventProvider
    hr = CoCreateInstance(CLSID_WbemDecoupledBasicEventProvider,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IWbemDecoupledBasicEventProvider,
                          (void**)&myEvtRegistrar);

    if (SUCCEEDED(hr))
    {
       // -- Register the DecoupledEventProvider
       hr = myEvtRegistrar->Register(0,
                                     NULL,
                                     NULL,
                                     L"root\\cimv2",
                                     L"DecoupledEventProvider",
                                     NULL, NULL);
       if (SUCCEEDED(hr))
       {
          IWbemServices *pService = NULL;
          hr = myEvtRegistrar->GetService (0, NULL, &pService);
          if (SUCCEEDED(hr))
          {
             IWbemObjectSink *pSink = NULL;
             hr = myEvtRegistrar->GetSink ( 0, NULL, &pSink );
             if (SUCCEEDED(hr))
             {
                // Provide events
             }
          }
       } 
    }
    ```

    

5.  <span data-ttu-id="f35d8-131">Führen [Sie die Aufrufe von WMI](making-calls-to-wmi.md) durch die Funktionalität des Anbieters aus.</span><span class="sxs-lookup"><span data-stu-id="f35d8-131">Make the [calls to WMI](making-calls-to-wmi.md) required by the provider's functionality.</span></span> <span data-ttu-id="f35d8-132">Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="f35d8-132">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span> <span data-ttu-id="f35d8-133">Weitere Informationen, wenn der Anbieter eine Anforderung für Daten von einem Skript oder einer Anwendung verarbeitet, finden Sie unter Annehmen der Identität [eines Clients](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="f35d8-133">For more information if the provider services a request for data from a script or application, see [Impersonating a Client](impersonating-a-client.md).</span></span>

<span data-ttu-id="f35d8-134">Unmittelbar vor dem beenden muss die Anwendung nach selbst bereinigt werden.</span><span class="sxs-lookup"><span data-stu-id="f35d8-134">Just prior to terminating, the application must clean up after itself.</span></span> <span data-ttu-id="f35d8-135">Im folgenden Verfahren wird beschrieben, wie die Registrierung des entkoppelten Anbieters aufgehoben wird, damit von WMI keine Informationen abgefragt werden können.</span><span class="sxs-lookup"><span data-stu-id="f35d8-135">The following procedure describes how to unregister the decoupled provider so that WMI does not attempt to query it for information.</span></span>

<span data-ttu-id="f35d8-136">Im folgenden Verfahren wird beschrieben, wie die Registrierung des entkoppelten Anbieters aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="f35d8-136">The following procedure describes how to unregister the decoupled provider.</span></span>

<span data-ttu-id="f35d8-137">**So heben Sie die Registrierung des entkoppelten Anbieters auf**</span><span class="sxs-lookup"><span data-stu-id="f35d8-137">**To unregister the decoupled provider**</span></span>

1.  <span data-ttu-id="f35d8-138">Aufheben der Registrierung und Freigeben der Registrierungsstelle</span><span class="sxs-lookup"><span data-stu-id="f35d8-138">Unregister and release the registrar.</span></span>

    <span data-ttu-id="f35d8-139">Im folgenden Codebeispiel wird gezeigt, wie die Registrierung aufgehoben und die Registrierungsstelle freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f35d8-139">The following code example shows how to unregister and release the registrar.</span></span>

    ```C++
    myRegistrar->UnRegister();
    myRegistrar->Release();
    ```

    

2.  <span data-ttu-id="f35d8-140">Aufheben der Registrierung und Freigeben des Ereignis Anbieters.</span><span class="sxs-lookup"><span data-stu-id="f35d8-140">Unregister and release the event provider.</span></span>

    <span data-ttu-id="f35d8-141">Im folgenden Codebeispiel wird gezeigt, wie die Registrierung aufgehoben und der Ereignis Anbieter freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f35d8-141">The following code example shows how to unregister and release the event provider.</span></span>

    ```C++
    myEvtRegistrar->UnRegister();
    myEvtRegistrar->Release();
    ```

    

3.  <span data-ttu-id="f35d8-142">Bereinigen Sie den com-Server.</span><span class="sxs-lookup"><span data-stu-id="f35d8-142">Clean up the COM server.</span></span>

    <span data-ttu-id="f35d8-143">Im folgenden Codebeispiel wird gezeigt, wie die Initialisierung der com-Bibliothek initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="f35d8-143">The following code example shows how to uninitialize the COM library.</span></span>

    ```C++
    CoUninitialize();
    ```

    

## <a name="related-topics"></a><span data-ttu-id="f35d8-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f35d8-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f35d8-145">Festlegen von namepace-Sicherheits Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="f35d8-145">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="f35d8-146">Sichern Ihres Anbieters</span><span class="sxs-lookup"><span data-stu-id="f35d8-146">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> <dt>

[<span data-ttu-id="f35d8-147">Entwickeln eines WMI-Anbieters</span><span class="sxs-lookup"><span data-stu-id="f35d8-147">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> </dl>

 

 



