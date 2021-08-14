---
description: Aufrufen von Dienstmethoden
ms.assetid: 3a2796c8-1a39-49eb-98e1-c9e06c61f397
title: Aufrufen von Dienstmethoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0553e1490a6f8d0903756767397c30c2e1137a16a80609ed3a22da69188f799e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843107"
---
# <a name="invoking-service-methods"></a>Aufrufen von Dienstmethoden

Die WpdServicesApiSample-Anwendung enthält Code, der veranschaulicht, wie eine Anwendung die von einem angegebenen Contacts-Dienst unterstützten Methoden synchron aufrufen kann. In diesem Beispiel werden die folgenden Schnittstellen verwendet:



| Schnittstelle    | BESCHREIBUNG    |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | Wird zum Abrufen der **IPortableDeviceServiceMethods-Schnittstelle** zum Aufrufen von Methoden für einen bestimmten Dienst verwendet.                                                                  |
| [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods) | Wird zum Aufrufen einer Dienstmethode verwendet.                                                                                                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                 | Wird verwendet, um die ausgehenden Methodenparameter und die Ergebnisse der eingehenden Methode zu enthalten. Dies kann **NULL sein,** wenn die Methode keine Parameter erfordert oder Ergebnisse zurückgibt. |



 

Wenn der Benutzer die Option "9" in der Befehlszeile auswählt, ruft die Anwendung die **InvokeMethods-Methode** auf, die sich im Modul ServiceMethods.cpp befindet. Beachten Sie, dass die Beispielanwendung vor dem Aufrufen der Methoden einen Kontaktdienst auf einem verbundenen Gerät öffnet.

Dienstmethoden kapseln Funktionen, die von jedem Dienst definiert und implementiert werden. Sie sind für jeden Diensttyp eindeutig und werden durch eine GUID dargestellt. Der Contacts-Dienst definiert beispielsweise eine **BeginSync-Methode,** die Anwendungen aufrufen, um das Gerät für die Synchronisierung von Contact-Objekten vorzubereiten, und eine **EndSync-Methode,** um das Gerät über den Abschluss der Synchronisierung zu benachrichtigen. Anwendungen führen eine Methode aus, indem [**sie IPortableDeviceServiceMethods::Invoke aufrufen.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke)

Dienstmethoden sollten nicht mit WPD-Befehlen verwechselt werden. WPD-Befehle sind Teil der standardmäßigen WPD Device Driver Interface (DDI) und stellen den Mechanismus für die Kommunikation zwischen einer WPD-Anwendung und dem Treiber dar. Befehle sind vordefinierte, nach Kategorien geordnet, z. B. **WPD \_ CATEGORY \_ COMMON,** und werden durch eine **PROPERTYKEY-Struktur** dargestellt. Eine Anwendung sendet Befehle an den Gerätetreiber, indem sie [**IPortableDeviceService::SendCommand aufruft.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) Weitere Informationen finden Sie im Thema Befehle.

Die **InvokeMethods-Methode** ruft die [**IPortableDeviceService::Methods-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) auf, um eine [**IPortableDeviceServiceMethods-Schnittstelle**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) abzurufen. Über diese Schnittstelle werden die **Methoden BeginSync** und **EndSync** aufgerufen, indem die [**IPortableDeviceServiceMethods::Invoke-Methode aufgerufen**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) wird. Bei jedem Aufruf **von Invoke** stellt die Anwendung die REFGUID für die aufgerufene Methode zur Anwendung.

Im folgenden Code wird die **InvokeMethods-Methode** verwendet.


```C++
// Invoke methods on the Contacts Service.
// BeginSync and EndSync are methods defined by the FullEnumerationSync Device Service.
void InvokeMethods(IPortableDeviceService* pService)
{
    HRESULT hr = S_OK;
    CComPtr<IPortableDeviceServiceMethods> pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceMethods interface from the IPortableDeviceService interface to
    // invoke methods.
    hr = pService->Methods(&pMethods);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceMethods from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Invoke() the BeginSync method
    if (SUCCEEDED(hr))
    {
        // This method does not take any parameters or results, so we pass in NULL
        hr = pMethods->Invoke(METHOD_FullEnumSyncSvc_BeginSync, NULL, NULL);
        if (SUCCEEDED(hr))
        {
            printf("%ws called, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
        else
        {
            printf("! Failed to invoke %ws, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
    }

    // Invoke the EndSync method asynchronously
    if (SUCCEEDED(hr))
    {
        // This method does not take any parameters or results, so we pass in NULL
        hr = pMethods->Invoke(METHOD_FullEnumSyncSvc_EndSync, NULL, NULL);
        if (SUCCEEDED(hr))
        {
            printf("%ws called, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        }
        else
        {
            printf("! Failed to invoke %ws, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        } 
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



