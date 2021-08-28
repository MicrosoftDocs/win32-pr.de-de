---
title: Abrufen von Dienstobjekten
description: Geräteobjekte machen eine Eigenschaft namens Dienste verfügbar, die eine Sammlung von Dienstobjekten zurückgibt, die ein Dienstobjekt für jeden vom Gerät exportierten Dienst enthält.
ms.assetid: 8ef12b6e-cb9b-4406-95be-002117b8fc3f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b7fca24bfc79a9458cfb964af28edba813a90ef17924a68fd0d1689e047884c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999570"
---
# <a name="obtaining-service-objects"></a>Abrufen von Dienstobjekten

Geräteobjekte machen eine Eigenschaft namens [**Dienste verfügbar,**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) die eine Sammlung von Dienstobjekten zurückgibt, die ein Dienstobjekt für jeden vom Gerät exportierten Dienst enthält. Anwendungen können diese Sammlung sequenziell durchlaufen oder einen bestimmten Dienst mithilfe der Dienst-ID anfordern.

## <a name="vbscript-example"></a>VBScript-Beispiel

Das folgende Beispiel ist VBScript-Code, der Dienstobjekte für zwei der dienste extrahiert, die von einem Gerät exportiert werden.


```VB
' Get the service objects
services = device.Services
    
Set appService = services( "urn:upnp-org:serviceId:DVDVideo" )
Set xportService = services( "urn:upnp-org:serviceId:AVTransport" )
```



In der ersten Zeile wird die Dienstsammlung aus dem Device-Objekt extrahiert, indem die Eigenschaft [**Services (Dienste) abfragen**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) wird. Die nächsten beiden Zeilen erhalten die beiden gewünschten Dienstobjekte aus der Auflistung, indem sie ihre Dienst-IDs angeben. Die Dienstsammlung kann auch sequenziell durchlaufen werden, indem für **jede ... next-Schleife.**

## <a name="c-example"></a>C++-Beispiel

Das folgende Beispiel zeigt den C++-Code, der zum Abrufen von Dienstobjekten von einem Gerät erforderlich ist. Zunächst fragt der Beispielcode die [**IUPnPDevice::Services-Eigenschaft**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) auf der Schnittstelle ab, die an die Funktion übergeben wurde. Dadurch wird eine Dienstsammlung mithilfe der [**IUPnPServices-Schnittstelle**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) zurückgegeben. Um einzelne Dienstobjekte zu erhalten, verwenden Sie die [**Item-Methode,**](/windows/win32/api/upnp/nf-upnp-iupnpservices-get_item) und geben Sie die angeforderten Dienst-IDs an. Um die Auflistung sequenziell zu durchlaufen, verwenden Sie die [**Methoden IEnumVARIANT::Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset), [**IEnumVARIANT::Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next)und [**IEnumVARIANT::Skip.**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-skip) Dieses Beispiel ähnelt dem Beispiel zum Durchlaufen der [**IUPnPDevices-Sammlung.**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices)


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



 

 