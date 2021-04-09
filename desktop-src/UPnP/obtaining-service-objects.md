---
title: Abrufen von Dienst Objekten
description: Geräte Objekte machen eine Eigenschaft mit dem Namen Dienste verfügbar, die eine Auflistung von Dienst Objekten zurückgibt, die ein Dienst Objekt für jeden vom Gerät exportierten Dienst enthält.
ms.assetid: 8ef12b6e-cb9b-4406-95be-002117b8fc3f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf951c9c620c23c2d4919dc4a8bcf082159fa7a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858392"
---
# <a name="obtaining-service-objects"></a><span data-ttu-id="ad1ed-103">Abrufen von Dienst Objekten</span><span class="sxs-lookup"><span data-stu-id="ad1ed-103">Obtaining Service Objects</span></span>

<span data-ttu-id="ad1ed-104">Geräte Objekte machen eine Eigenschaft mit dem Namen [**Dienste**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) verfügbar, die eine Auflistung von Dienst Objekten zurückgibt, die ein Dienst Objekt für jeden vom Gerät exportierten Dienst enthält.</span><span class="sxs-lookup"><span data-stu-id="ad1ed-104">Device objects expose a property called [**Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) that returns a collection of Service objects that contains one service object for each service exported by the device.</span></span> <span data-ttu-id="ad1ed-105">Anwendungen können diese Sammlung sequenziell durchlaufen oder einen bestimmten Dienst mithilfe der Dienst-ID anfordern.</span><span class="sxs-lookup"><span data-stu-id="ad1ed-105">Applications are able to traverse this collection sequentially, or request a particular service by using its service ID.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="ad1ed-106">VBScript-Beispiel</span><span class="sxs-lookup"><span data-stu-id="ad1ed-106">VBScript Example</span></span>

<span data-ttu-id="ad1ed-107">Das folgende Beispiel zeigt VBScript-Code, der Dienst Objekte für zwei der von einem Gerät exportierten Dienste extrahiert.</span><span class="sxs-lookup"><span data-stu-id="ad1ed-107">The following example is VBScript code that extracts Service objects for two of the services exported by a device.</span></span>


```VB
' Get the service objects
services = device.Services
    
Set appService = services( "urn:upnp-org:serviceId:DVDVideo" )
Set xportService = services( "urn:upnp-org:serviceId:AVTransport" )
```



<span data-ttu-id="ad1ed-108">In der ersten Zeile wird die Dienst Auflistung aus dem Geräte Objekt extrahiert, indem die [**Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) -Eigenschaft abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="ad1ed-108">The first line extracts the services collection from the Device object by querying the [**Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) property.</span></span> <span data-ttu-id="ad1ed-109">In den nächsten beiden Zeilen werden die beiden gewünschten Dienst Objekte aus der Auflistung abgerufen, indem ihre Dienst-IDs angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ad1ed-109">The next two lines obtain the two desired Service objects from the collection by specifying their service IDs.</span></span> <span data-ttu-id="ad1ed-110">Die Dienst Auflistung kann auch sequenziell durchlaufen werden, indem eine **for each-... nächste** Schleife.</span><span class="sxs-lookup"><span data-stu-id="ad1ed-110">The services collection can also be traversed sequentially by using a **for each … next** loop.</span></span>

## <a name="c-example"></a><span data-ttu-id="ad1ed-111">C++-Beispiel</span><span class="sxs-lookup"><span data-stu-id="ad1ed-111">C++ Example</span></span>

<span data-ttu-id="ad1ed-112">Das folgende Beispiel zeigt den C++-Code, der zum Abrufen von Dienst Objekten von einem Gerät erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ad1ed-112">The following example shows the C++ code required to obtain Service objects from a device.</span></span> <span data-ttu-id="ad1ed-113">Zuerst fragt der Beispielcode die [**iupnpdevice:: Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) -Eigenschaft in der Schnittstelle ab, die an die Funktion übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ad1ed-113">First, the sample code queries the [**IUPnPDevice::Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) property on the interface that was passed to the function.</span></span> <span data-ttu-id="ad1ed-114">Dadurch wird eine Dienst Sammlung mithilfe der [**iupnpservices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) -Schnittstelle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ad1ed-114">This returns a service collection using the [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) interface.</span></span> <span data-ttu-id="ad1ed-115">Zum Abrufen einzelner Dienst Objekte verwenden Sie die [**Item**](/windows/win32/api/upnp/nf-upnp-iupnpservices-get_item) -Methode, und geben Sie die angeforderten Dienst-IDs an.</span><span class="sxs-lookup"><span data-stu-id="ad1ed-115">To obtain individual Service objects, use the [**Item**](/windows/win32/api/upnp/nf-upnp-iupnpservices-get_item) method, and specify the requested service IDs.</span></span> <span data-ttu-id="ad1ed-116">Um die Auflistung sequenziell zu durchlaufen, verwenden Sie die Methoden [**IEnumVARIANT:: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset), [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next)und [**IEnumVARIANT:: Skip**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-skip) .</span><span class="sxs-lookup"><span data-stu-id="ad1ed-116">To traverse the collection sequentially, use the [**IEnumVARIANT::Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset), [**IEnumVARIANT::Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next), and [**IEnumVARIANT::Skip**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-skip) methods.</span></span> <span data-ttu-id="ad1ed-117">Dieses Beispiel ähnelt dem Beispiel, das zum Durchlaufen der [**iupnpdevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) -Auflistung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ad1ed-117">This example is similar to the example used to traverse the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) collection.</span></span>


```C++
#include <windows.h>
#include <upnp.h>

#pragma comment(lib, "oleaut32.lib")


HRESULT ExtractServices(IUPnPDevice * pDevice)
{
    // Create a BSTR to hold the service name
    BSTR bstrServiceName = SysAllocString(L"urn:upnp-org:servicId:DVDVideo");
    if (NULL == bstrServiceName)
    {
        return E_OUTOFMEMORY;
    }
    // Get the list of services available on the device
    IUPnPServices * pServices = NULL;
    HRESULT hr = pDevice->get_Services(&pServices);
    if (SUCCEEDED(hr))
    {
        // Retrieve the service we are interested in
        IUPnPService * pAppService = NULL;
        hr = pServices->get_Item(bstrServiceName, &pAppService);
        if (SUCCEEDED(hr))
        {
            // Do something interesting with the service object
            pAppService->Release();
        }
        pServices->Release();
    }
    SysFreeString(bstrServiceName);
    return hr;
}
```



 

 