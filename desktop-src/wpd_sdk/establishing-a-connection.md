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
# <a name="establishing-a-connection"></a><span data-ttu-id="58975-103">Herstellen einer Verbindung</span><span class="sxs-lookup"><span data-stu-id="58975-103">Establishing a Connection</span></span>

<span data-ttu-id="58975-104">Sobald der Benutzer ein Gerät auswählt, ruft die choosedevice-Funktion wiederum die [**iportabledevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) -Methode auf, um eine Verbindung zwischen der Anwendung und dem Gerät herzustellen.</span><span class="sxs-lookup"><span data-stu-id="58975-104">Once the user selects a device, the ChooseDevice function, in turn, calls the [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) method to establish a connection between the application and the device.</span></span> <span data-ttu-id="58975-105">Die iportabledevice:: Open-Methode benötigt zwei Argumente:</span><span class="sxs-lookup"><span data-stu-id="58975-105">The IPortableDevice::Open method takes two arguments:</span></span>

-   <span data-ttu-id="58975-106">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Plug & Play Namen des Geräts angibt.</span><span class="sxs-lookup"><span data-stu-id="58975-106">A pointer to a null-terminated string that specifies the Plug and Play name of the device.</span></span> <span data-ttu-id="58975-107">(Diese Zeichenfolge wird durch Aufrufen der [**iportabledevicemanager:: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) -Methode abgerufen.)</span><span class="sxs-lookup"><span data-stu-id="58975-107">(This string is retrieved by calling the [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) method.)</span></span>
-   <span data-ttu-id="58975-108">Ein Zeiger auf eine [**iportabledevicevalues-Schnittstelle**](iportabledevicevalues.md) , die Client Informationen für die Anwendung angibt.</span><span class="sxs-lookup"><span data-stu-id="58975-108">A pointer to an [**IPortableDeviceValues interface**](iportabledevicevalues.md) that specifies client information for the application.</span></span>


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



<span data-ttu-id="58975-109">Für Windows 7 unterstützt [**iportabledevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice) zwei CLSIDs für **cokreatabstance**.</span><span class="sxs-lookup"><span data-stu-id="58975-109">For Windows 7, [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice) supports two CLSIDs for **CoCreateInstance**.</span></span> <span data-ttu-id="58975-110">**CLSID \_ Portabledevice** gibt einen **iportabledevice** -Zeiger zurück, der den Freethread-Mars Haller nicht aggregiert. **CLSID \_ Portabledeviceftm** ist eine neue CLSID, die einen **iportabledevice** -Zeiger zurückgibt, der den frei Thread-Mars Haller aggregiert.</span><span class="sxs-lookup"><span data-stu-id="58975-110">**CLSID\_PortableDevice** returns an **IPortableDevice** pointer that does not aggregate the free-threaded marshaler; **CLSID\_PortableDeviceFTM** is a new CLSID that returns an **IPortableDevice** pointer that aggregates the free-threaded marshaler.</span></span> <span data-ttu-id="58975-111">Beide Zeiger unterstützen andernfalls dieselbe Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="58975-111">Both pointers support the same functionality otherwise.</span></span>

<span data-ttu-id="58975-112">Anwendungen, die in Single Thread-Apartments Leben, sollten **CLSID \_ portabledeviceftm** verwenden, da dadurch der Aufwand für das Marshalling von Schnittstellen Zeigern entfällt.</span><span class="sxs-lookup"><span data-stu-id="58975-112">Applications that live in Single Threaded Apartments should use **CLSID\_PortableDeviceFTM** as this eliminates the overhead of interface pointer marshaling.</span></span> <span data-ttu-id="58975-113">**CLSID \_ Portabledevice** wird weiterhin für ältere Anwendungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="58975-113">**CLSID\_PortableDevice** is still supported for legacy applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58975-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="58975-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58975-115">**Auswählen eines Geräts**</span><span class="sxs-lookup"><span data-stu-id="58975-115">**Selecting a Device**</span></span>](selecting-a-device.md)
</dt> </dl>

 

 



