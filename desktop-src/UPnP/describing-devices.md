---
title: Beschreiben von Geräten
description: Es gibt zwei Möglichkeiten zum Abrufen von Geräte Objekten.
ms.assetid: a83fbf21-586e-4b92-9875-476d820c377d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5abc84f15f6b52328585e05abfd95503087124b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856644"
---
# <a name="describing-devices"></a><span data-ttu-id="f8f00-103">Beschreiben von Geräten</span><span class="sxs-lookup"><span data-stu-id="f8f00-103">Describing Devices</span></span>

<span data-ttu-id="f8f00-104">Es gibt zwei Möglichkeiten zum Abrufen von Geräte Objekten:</span><span class="sxs-lookup"><span data-stu-id="f8f00-104">There are two ways to obtain device objects:</span></span>

-   <span data-ttu-id="f8f00-105">Verwenden der [**iupnpdescriptiondocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f8f00-105">Using the [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) interface.</span></span> <span data-ttu-id="f8f00-106">Die **iupnpdescriptiondocument** -Schnittstelle ist die einzige Schnittstelle, die für die Skripterstellung sicher ist.</span><span class="sxs-lookup"><span data-stu-id="f8f00-106">The **IUPnPDescriptionDocument** interface is the only interface that is safe for scripting.</span></span>
-   <span data-ttu-id="f8f00-107">Verwenden der [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) -Schnittstelle zum Abrufen einer [**iupnpdevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f8f00-107">Using the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface to obtain an [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface.</span></span>

<span data-ttu-id="f8f00-108">Beide Methoden geben Geräte Auflistungen zurück.</span><span class="sxs-lookup"><span data-stu-id="f8f00-108">Both methods return Devices collections.</span></span> <span data-ttu-id="f8f00-109">Anwendungen werden dann mithilfe der Geräte Methoden zum Abrufen von Eigenschaften von Geräten verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8f00-109">Applications then use the Device methods to retrieve properties about devices.</span></span>

<span data-ttu-id="f8f00-110">Anwendungen können die folgenden Informationstypen abrufen:</span><span class="sxs-lookup"><span data-stu-id="f8f00-110">Applications are able to retrieve the following types of information:</span></span>

-   <span data-ttu-id="f8f00-111">Informationen zur Geräte Hierarchie, einschließlich der Stamm Geräte, übergeordneter und untergeordneter Geräte.</span><span class="sxs-lookup"><span data-stu-id="f8f00-111">Device hierarchy information, including root devices, parent devices, and child devices.</span></span>
-   <span data-ttu-id="f8f00-112">Geräteeigenschaften, einschließlich udns, Uniform Resource Identifiern (URIs) und Benutzer lesbaren Namen.</span><span class="sxs-lookup"><span data-stu-id="f8f00-112">Device properties, including UDNs, uniform resource identifiers (URIs), and user-readable names.</span></span>
-   <span data-ttu-id="f8f00-113">Hersteller Informationen, einschließlich Namen und zugehöriger Webseiten.</span><span class="sxs-lookup"><span data-stu-id="f8f00-113">Manufacturer information, including names and related Web pages.</span></span>
-   <span data-ttu-id="f8f00-114">Modellinformationen, einschließlich Name, Zahl, UPC, Seriennummern und Geräte Beschreibungen.</span><span class="sxs-lookup"><span data-stu-id="f8f00-114">Model information, including the name, number, UPC, serial numbers and device descriptions.</span></span>
-   <span data-ttu-id="f8f00-115">Anzeigen von Informationen, einschließlich der URL zum Steuern des Geräts und URLs, von denen Symbole heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="f8f00-115">Display information, including the URL to control the device, and URLs from which icons are downloaded.</span></span>
-   <span data-ttu-id="f8f00-116">Dienste, die von einem bestimmten Gerät bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f8f00-116">Services provided by a particular device.</span></span>

<span data-ttu-id="f8f00-117">Anwendungen rufen auch die URL des Geräte Beschreibungs Dokuments mithilfe der [**iupnpdevicedocumentaccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="f8f00-117">Applications also obtain the URL of the device description document using the [**IUPnPDeviceDocumentAccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess) interface.</span></span> <span data-ttu-id="f8f00-118">Die Anwendung lädt dann das Beschreibungs Dokument und arbeitet mit den Geräte-und Dienst Eigenschaften, die nicht von der [**iupnpdevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) -Schnittstelle verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="f8f00-118">The application then load the description document and work with device and service properties that are not exposed by the [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) interface.</span></span> <span data-ttu-id="f8f00-119">Diese Schnittstelle kann nicht in der Skripterstellung verwendet werden, da Sie nicht die Standardschnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="f8f00-119">This interface cannot be used in scripting, because it is not the default interface.</span></span>

## <a name="visual-basic-example"></a><span data-ttu-id="f8f00-120">Visual Basic Beispiel</span><span class="sxs-lookup"><span data-stu-id="f8f00-120">Visual Basic Example</span></span>

<span data-ttu-id="f8f00-121">Der folgende Beispielcode zeigt die Verwendung von [**iupnpdevicedocumentaccess:: getdocumenturl**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span><span class="sxs-lookup"><span data-stu-id="f8f00-121">The following sample code shows the usage of [**IUPnPDeviceDocumentAccess::GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span></span>


```VB
Sub GetDocumentURL()
Dim pDescDoc As IUPnPDeviceDocumentAccess
Dim strDescDocURL As String

'currentDevice is UPnPDevice object containing the current UPnP Device 
'We are trying to get IUPnPDeviceDocumentAccess interface in the UPnP Device object
Set pDescDoc = currentDevice

If Not (pDescDoc is Nothing) Then
  'Description Document URL is got from device
  strDescDocURL = pDescDoc.GetDocumentURL 
End If
```



## <a name="c-example"></a><span data-ttu-id="f8f00-122">C++-Beispiel</span><span class="sxs-lookup"><span data-stu-id="f8f00-122">C++ Example</span></span>

<span data-ttu-id="f8f00-123">Der folgende Beispielcode zeigt die Verwendung von [**iupnpdevicedocumentaccess:: getdocumenturl**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span><span class="sxs-lookup"><span data-stu-id="f8f00-123">The following sample code shows the usage of [**IUPnPDeviceDocumentAccess::GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span></span>


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "oleaut32.lib")

int GetDeviceDocumentUrl () 
{
  HRESULT hr = S_OK;
  // List of interfaces needed
  IUPnPDeviceFinder *pDevFinder=NULL;
  IUPnPDevice *pDevice =NULL;
  IUPnPDeviceDocumentAccess* pDeviceDocument=NULL;
  BSTR bstrDeviceUDN =NULL;
  BSTR bstrDeviceDocumentURL = NULL; 

  bstrDeviceUDN = SysAllocString(L"uuid:234324234324");
  if(bstrDeviceUDN == NULL){
    printf("ERROR: Could not allocate memory\n");
    return -1;
  }  

  //CoInitialize the program so that we can create COM objects
  CoInitializeEx(NULL, COINIT_MULTITHREADED);

  //now try to instantiate the DeviceFinder object
  hr = CoCreateInstance(  CLSID_UPnPDeviceFinder, 
              NULL,
              CLSCTX_INPROC_SERVER,
              IID_IUPnPDeviceFinder,
              (LPVOID *) &pDevFinder); 

  if(!SUCCEEDED(hr)){
    printf("\nERROR: CoCreateInstance on IUPnPDeviceFinder returned HRESULT %x",hr);
    goto cleanup;
  }

  printf("\nGot a pointer to the IUPnPDeviceFinder Interface");

  printf("\n Finding the device of given UDN\n");
  hr =pDevFinder->FindByUDN(bstrDeviceUDN, &pDevice);
  if(hr!=S_OK)
  {
    printf("\nERROR: FindByUDN for %S returned HRESULT %x", bstrDeviceUDN, hr);
    goto cleanup;
  }

  printf("\n\tFindByUDN for device of UDN %S succeeded", bstrDeviceUDN);
  //Now query pDevice for IUPnPDeviceDocumentAccess
  hr = pDevice->QueryInterface(IID_IUPnPDeviceDocumentAccess, (VOID **)&pDeviceDocument);
  if(SUCCEEDED(hr)){
    // We have got a pointer to the IUPnPDeviceDocumentAccess interface.
    // GetDocumentURL is available only in Windows XP. 
    hr = pDeviceDocument->GetDocumentURL(&bstrDeviceDocumentURL);
    if(SUCCEEDED(hr))
      printf("\nThe Device Document URL is %S \n", bstrDeviceDocumentURL);
  }
    
cleanup:
  //release references to all interfaces 
  if(pDevFinder)
    pDevFinder->Release();
  if(pDevice)
    pDevice->Release();
  if(pDeviceDocument)
    pDeviceDocument->Release();
  
  // Free the bstr strings
  if(bstrDeviceDocumentURL)
    SysFreeString(bstrDeviceDocumentURL);
  if(bstrDeviceUDN)
    SysFreeString(bstrDeviceUDN);
  CoUninitialize();
  return 0;
}
```



 

 




