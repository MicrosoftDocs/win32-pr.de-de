---
description: Herstellen einer Verbindung
ms.assetid: 16286da5-5979-413b-a4db-ca157b10a571
title: Herstellen einer Verbindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ea922b3cd44430dc7c213a513c44fa8ef2ab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050578"
---
# <a name="establishing-a-connection"></a>Herstellen einer Verbindung

Sobald der Benutzer ein Gerät auswählt, ruft die choosedevice-Funktion wiederum die [**iportabledevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) -Methode auf, um eine Verbindung zwischen der Anwendung und dem Gerät herzustellen. Die iportabledevice:: Open-Methode benötigt zwei Argumente:

-   Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Plug & Play Namen des Geräts angibt. (Diese Zeichenfolge wird durch Aufrufen der [**iportabledevicemanager:: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) -Methode abgerufen.)
-   Ein Zeiger auf eine [**iportabledevicevalues-Schnittstelle**](iportabledevicevalues.md) , die Client Informationen für die Anwendung angibt.


```C++
// CoCreate the IPortableDevice interface and call Open() with
// the chosen PnPDeviceID string.
hr = CoCreateInstance(CLSID_PortableDeviceFTM,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(ppDevice));
if (SUCCEEDED(hr))
{
    hr = (*ppDevice)->Open(pPnpDeviceIDs[uiCurrentDevice], pClientInformation);
    if (FAILED(hr))
    {
        if (hr == E_ACCESSDENIED)
        {
            printf("Failed to Open the device for Read Write access, will open it for Read-only access instead\n");
            pClientInformation->SetUnsignedIntegerValue(WPD_CLIENT_DESIRED_ACCESS, GENERIC_READ);
            hr = (*ppDevice)->Open(pPnpDeviceIDs[uiCurrentDevice], pClientInformation);
            if (FAILED(hr))
            {
                printf("! Failed to Open the device, hr = 0x%lx\n",hr);
                // Release the IPortableDevice interface, because we cannot proceed
                // with an unopen device.
                (*ppDevice)->Release();
                *ppDevice = NULL;
            }
        }
        else
        {
            printf("! Failed to Open the device, hr = 0x%lx\n",hr);
            // Release the IPortableDevice interface, because we cannot proceed
            // with an unopen device.
            (*ppDevice)->Release();
            *ppDevice = NULL;
        }
    }
}
else
{
    printf("! Failed to CoCreateInstance CLSID_PortableDeviceFTM, hr = 0x%lx\n",hr);
}
```



Für Windows 7 unterstützt [**iportabledevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice) zwei CLSIDs für **cokreatabstance**. **CLSID \_ Portabledevice** gibt einen **iportabledevice** -Zeiger zurück, der den Freethread-Mars Haller nicht aggregiert. **CLSID \_ Portabledeviceftm** ist eine neue CLSID, die einen **iportabledevice** -Zeiger zurückgibt, der den frei Thread-Mars Haller aggregiert. Beide Zeiger unterstützen andernfalls dieselbe Funktionalität.

Anwendungen, die in Single Thread-Apartments Leben, sollten **CLSID \_ portabledeviceftm** verwenden, da dadurch der Aufwand für das Marshalling von Schnittstellen Zeigern entfällt. **CLSID \_ Portabledevice** wird weiterhin für ältere Anwendungen unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Auswählen eines Geräts**](selecting-a-device.md)
</dt> </dl>

 

 



