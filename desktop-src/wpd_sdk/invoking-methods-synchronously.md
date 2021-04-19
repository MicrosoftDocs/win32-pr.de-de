---
description: Aufrufen von Dienstmethoden
ms.assetid: 3a2796c8-1a39-49eb-98e1-c9e06c61f397
title: Aufrufen von Dienstmethoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b568ea169d0f3c6465d9879eb9eb01c0b46b526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359418"
---
# <a name="invoking-service-methods"></a>Aufrufen von Dienstmethoden

Die Anwendung wpdservicesapisample enthält Code, der veranschaulicht, wie eine Anwendung die Methoden aufrufen kann, die von einem bestimmten Kontakt Dienst unterstützt werden. In diesem Beispiel werden die folgenden Schnittstellen verwendet.



|                                                                        |                                                                                                                                                                         |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstelle                                                              | BESCHREIBUNG                                                                                                                                                             |
| [**Iportablede viceservice**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | Wird zum Abrufen der **iportabledeviceservicemethods** -Schnittstelle verwendet, um Methoden für einen bestimmten Dienst aufzurufen.                                                                  |
| [**Iportabledeviceservicemethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods) | Wird verwendet, um eine Dienst Methode aufzurufen.                                                                                                                                        |
| [**Iportablede vicevalues**](iportabledevicevalues.md)                 | Wird verwendet, um die Parameter für die ausgehende Methode und die Ergebnisse der eingehenden Methode aufzunehmen. Dieser Wert kann **null** sein, wenn die Methode keine Parameter erfordert oder keine Ergebnisse zurückgibt. |



 

Wenn der Benutzer die Option "9" in der Befehlszeile auswählt, ruft die Anwendung die **invokemethods** -Methode auf, die im Modul "servicemethods. cpp" zu finden ist. Beachten Sie, dass die Beispielanwendung vor dem Aufrufen der Methoden einen Contacts-Dienst auf einem verbundenen Gerät öffnet.

Dienst Methoden Kapseln Funktionen, die von den einzelnen Diensten definiert und implementiert werden. Sie sind für jeden Diensttyp eindeutig und werden durch eine GUID dargestellt. Der Kontakt Dienst definiert z. b. eine **BeginSync** -Methode, die Anwendungen aufrufen, um das Gerät für die Synchronisierung von Kontakt Objekten vorzubereiten, und eine **EndSync** -Methode, um das Gerät zu benachrichtigen, dass die Synchronisierung abgeschlossen ist. Anwendungen führen eine Methode aus, indem Sie [**iportabledeviceservicemethods::**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke)Call aufrufen.

Dienst Methoden sollten nicht mit WPD-Befehlen verwechselt werden. WPD-Befehle sind Teil der standardmäßigen WPD-Gerätetreiber Schnittstelle (DDI) und stellen den Mechanismus für die Kommunikation zwischen einer WPD-Anwendung und dem Treiber dar. Befehle sind vordefiniert, gruppiert nach Kategorien, z. b. die **WPD- \_ Kategorie \_ Common**, und werden durch eine **PropertyKey** -Struktur dargestellt. Eine Anwendung sendet durch Aufrufen von [**iportabledeviceservice:: Send Command**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)Befehle an den Gerätetreiber. Weitere Informationen finden Sie im Thema "Befehle".

Die **invokemethods** -Methode ruft die [**iportabledeviceservice:: Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) -Methode auf, um eine [**iportabledeviceservicemethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) -Schnittstelle abzurufen. Mithilfe dieser Schnittstelle ruft Sie die **BeginSync** -Methode und die **EndSync** -Methode auf, indem Sie die [**iportabledeviceservicemethods::**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) Call-Methode aufruft. Jedes **Mal, wenn der Aufruf aufgerufen** wird, gibt die Anwendung die refguid für die aufgerufene Methode an.

Im folgenden Code wird die **invokemethods** -Methode verwendet.


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

[**Iportablede viceservice**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**Iportabledeviceservicemethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[Wpdservicesapisample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



