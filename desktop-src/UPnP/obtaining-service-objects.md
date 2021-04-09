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
# <a name="obtaining-service-objects"></a>Abrufen von Dienst Objekten

Geräte Objekte machen eine Eigenschaft mit dem Namen [**Dienste**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) verfügbar, die eine Auflistung von Dienst Objekten zurückgibt, die ein Dienst Objekt für jeden vom Gerät exportierten Dienst enthält. Anwendungen können diese Sammlung sequenziell durchlaufen oder einen bestimmten Dienst mithilfe der Dienst-ID anfordern.

## <a name="vbscript-example"></a>VBScript-Beispiel

Das folgende Beispiel zeigt VBScript-Code, der Dienst Objekte für zwei der von einem Gerät exportierten Dienste extrahiert.


```VB
' Get the service objects
services = device.Services
    
Set appService = services( "urn:upnp-org:serviceId:DVDVideo" )
Set xportService = services( "urn:upnp-org:serviceId:AVTransport" )
```



In der ersten Zeile wird die Dienst Auflistung aus dem Geräte Objekt extrahiert, indem die [**Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) -Eigenschaft abgefragt wird. In den nächsten beiden Zeilen werden die beiden gewünschten Dienst Objekte aus der Auflistung abgerufen, indem ihre Dienst-IDs angegeben werden. Die Dienst Auflistung kann auch sequenziell durchlaufen werden, indem eine **for each-... nächste** Schleife.

## <a name="c-example"></a>C++-Beispiel

Das folgende Beispiel zeigt den C++-Code, der zum Abrufen von Dienst Objekten von einem Gerät erforderlich ist. Zuerst fragt der Beispielcode die [**iupnpdevice:: Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) -Eigenschaft in der Schnittstelle ab, die an die Funktion übergeben wurde. Dadurch wird eine Dienst Sammlung mithilfe der [**iupnpservices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) -Schnittstelle zurückgegeben. Zum Abrufen einzelner Dienst Objekte verwenden Sie die [**Item**](/windows/win32/api/upnp/nf-upnp-iupnpservices-get_item) -Methode, und geben Sie die angeforderten Dienst-IDs an. Um die Auflistung sequenziell zu durchlaufen, verwenden Sie die Methoden [**IEnumVARIANT:: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset), [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next)und [**IEnumVARIANT:: Skip**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-skip) . Dieses Beispiel ähnelt dem Beispiel, das zum Durchlaufen der [**iupnpdevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) -Auflistung verwendet wird.


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



 

 