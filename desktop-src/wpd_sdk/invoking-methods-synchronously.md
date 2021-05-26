---
description: Aufrufen von Dienstmethoden
ms.assetid: 3a2796c8-1a39-49eb-98e1-c9e06c61f397
title: Aufrufen von Dienstmethoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15b9540cf7378e13d56af2611d6216897c6750f6
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424200"
---
# <a name="invoking-service-methods"></a>Aufrufen von Dienstmethoden

Die WpdServicesApiSample-Anwendung enthält Code, der veranschaulicht, wie eine Anwendung die von einem bestimmten Contacts-Dienst unterstützten Methoden synchron aufrufen kann. In diesem Beispiel werden die folgenden Schnittstellen verwendet:



| Schnittstelle    | BESCHREIBUNG    |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | Wird verwendet, um die **IPortableDeviceServiceMethods-Schnittstelle** abzurufen, um Methoden für einen bestimmten Dienst aufzurufen.                                                                  |
| [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods) | Wird zum Aufrufen einer Dienstmethode verwendet.                                                                                                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                 | Wird verwendet, um die ausgehenden Methodenparameter und die eingehenden Methodenergebnisse zu speichern. Dies kann **NULL** sein, wenn die Methode keine Parameter erfordert oder Ergebnisse zurückgibt. |



 

Wenn der Benutzer die Option "9" in der Befehlszeile auswählt, ruft die Anwendung die **InvokeMethods-Methode** auf, die sich im ServiceMethods.cpp-Modul befindet. Beachten Sie, dass die Beispielanwendung vor dem Aufrufen der Methoden einen Contacts-Dienst auf einem verbundenen Gerät öffnet.

Dienstmethoden kapseln Funktionen, die jeder Dienst definiert und implementiert. Sie sind für jeden Diensttyp eindeutig und werden durch eine GUID dargestellt. Beispielsweise definiert der Contacts-Dienst eine **BeginSync-Methode,** die Anwendungen aufrufen, um das Gerät für die Synchronisierung von Contact-Objekten vorzubereiten, und eine **EndSync-Methode,** um das Gerät über den Abschluss der Synchronisierung zu informieren. Anwendungen führen eine Methode aus, indem [**sie IPortableDeviceServiceMethods::Invoke aufrufen.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke)

Dienstmethoden dürfen nicht mit WPD-Befehlen verwechselt werden. WPD-Befehle sind Teil der standardmäßigen WPD-Gerätetreiberschnittstelle (DDI) und der Mechanismus für die Kommunikation zwischen einer WPD-Anwendung und dem Treiber. Befehle sind vordefiniert, nach Kategorien gruppiert, z. B. **WPD \_ CATEGORY \_ COMMON**, und werden durch eine **PROPERTYKEY-Struktur** dargestellt. Eine Anwendung sendet Befehle an den Gerätetreiber, indem [**sie IPortableDeviceService::SendCommand aufruft.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) Weitere Informationen finden Sie im Thema Befehle.

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

 

 



