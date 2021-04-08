---
title: Aktivieren von PNP für Geräte
description: Aktivieren von PNP für Geräte
ms.assetid: 510237a9-2b74-4c2e-ad45-3f45117289a6
keywords:
- Windows Media Device Manager, PNP-Geräte
- Device Manager, PNP-Geräte
- Programmier Handbuch, PNP-Geräte
- Dienstanbieter, PNP-Geräte
- Erstellen von Dienstanbietern, PnP-Geräten
- PNP-Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44c7ccdfd29453c1ab28e970c1b054d1278e620
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855891"
---
# <a name="enabling-pnp-for-devices"></a><span data-ttu-id="f0f86-109">Aktivieren von PNP für Geräte</span><span class="sxs-lookup"><span data-stu-id="f0f86-109">Enabling PnP for Devices</span></span>

<span data-ttu-id="f0f86-110">Windows Media Device Manager überwacht die Eingangs-und Entfernungs Benachrichtigungen von Geräten, die eine Portable Audioplayer-Geräteschnittstelle ankündigen.</span><span class="sxs-lookup"><span data-stu-id="f0f86-110">Windows Media Device Manager monitors arrival and removal notifications of devices that advertise a Portable Audio Player device interface.</span></span> <span data-ttu-id="f0f86-111">Beim Eintreffen eines solchen Geräts fragt Windows Media Device Manager einen Geräteparameter mit dem Namen " *wmdmspclsid* " für die Klassen-ID des Dienstanbieters ab, der für dieses Gerät zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="f0f86-111">On the arrival of such a device, Windows Media Device Manager queries a device parameter named *WMDMSPCLSID* for the class ID of the service provider responsible for this device.</span></span> <span data-ttu-id="f0f86-112">Windows Media Device Manager ruft [**IMDServiceProvider2:: anatedevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) für diesen Dienstanbieter auf, um ein Geräte Objekt zu erstellen, das für die Anwendung als [**iwmdmdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) -Objekt verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="f0f86-112">Windows Media Device Manager calls [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) on this service provider to create a device object, which is exposed to the application as an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

<span data-ttu-id="f0f86-113">Ein Dienstanbieter kann entweder PNP-Geräte oder nicht-PNP-Geräte verarbeiten. Beide Typen können nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="f0f86-113">A service provider can either handle PnP devices, or non-PnP devices; it cannot handle both types.</span></span>

<span data-ttu-id="f0f86-114">Damit ein Gerät mit dem vorangehenden Mechanismus funktioniert (und somit die Eingangs-und Entfernungs Benachrichtigungen für das Gerät unter Windows Media Device Manager-Anwendungen) aktivieren kann, müssen die folgenden Anforderungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="f0f86-114">For a device to work with the preceding mechanism (and thus enable arrival and removal notifications for the device under Windows Media Device Manager applications), the following requirements must be met:</span></span>

-   <span data-ttu-id="f0f86-115">Der Gerätetreiber dieses Geräts muss die Windows Media Device Manager portablen Audioplayer-Geräteschnittstelle ankündigen.</span><span class="sxs-lookup"><span data-stu-id="f0f86-115">The device driver of this device must advertise the Windows Media Device Manager Portable Audio Player device interface.</span></span> <span data-ttu-id="f0f86-116">Die GUID für diese Geräteschnittstelle wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="f0f86-116">The GUID for this device interface is defined as:</span></span>

    ```
    {0xf33fdc04, 0xd1ac, 0x4e8e, {0x9a, 0x30, 0x19, 0xbb, 0xd4, 0xb1, 0x8, 0xae} }
    ```

    

    > [!Note]  
    > <span data-ttu-id="f0f86-117">Ein Gerät sollte diese Schnittstelle nicht ankündigen, wenn das Gerät die Volume-Schnittstelle (als volumeclassguid oder GUID \_ devinterface- \_ Volume in winioctl. h definiert) ankündigt.</span><span class="sxs-lookup"><span data-stu-id="f0f86-117">A device should not advertise this interface if the device advertises the Volume interface (defined as VolumeClassGuid or GUID\_DEVINTERFACE\_VOLUME in winioctl.h).</span></span> <span data-ttu-id="f0f86-118">Wenn das Gerät die volumeschnittstelle ankündigt, ist es unter Windows Media Device Manager bereits PNP-fähig.</span><span class="sxs-lookup"><span data-stu-id="f0f86-118">If the device advertises the Volume Interface, it is already PnP-enabled under Windows Media Device Manager.</span></span>

     

    <span data-ttu-id="f0f86-119">-und/oder-</span><span class="sxs-lookup"><span data-stu-id="f0f86-119">-AND/OR-</span></span>

    <span data-ttu-id="f0f86-120">Ein neuer Registrierungs Unterschlüssel für den Dienstanbieter muss innerhalb des unter Schlüssels HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows Media Device Manager \\ knowndevices erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f0f86-120">A new registry subkey for the service provider must be created inside the subkey HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows Media Device Manager\\KnownDevices.</span></span> <span data-ttu-id="f0f86-121">Dieser Schlüssel sollte den Namen Ihres Dienstanbieters aufweisen und über die folgenden beiden REG SZ- \_ Wert Einträge verfügen:</span><span class="sxs-lookup"><span data-stu-id="f0f86-121">This key should have the name of your service provider and must have the following two Reg\_SZ value entries:</span></span>

    ```
    DeviceInterface         {25DBCE51-6C8F-4A72-8A6D-B54C2B4FC835}
    WMDMSPCLSID             {067B4B81-B1EC-489F-B111-940EBDC44EBE}
    ```

    

-   <span data-ttu-id="f0f86-122">Das Gerät muss über einen Geräteparameter mit dem Namen "wmdmspclsid" verfügen.</span><span class="sxs-lookup"><span data-stu-id="f0f86-122">The device must have a device parameter named WMDMSPCLSID.</span></span> <span data-ttu-id="f0f86-123">Der Wert dieses Parameters sollte als CLSID des Dienstanbieters in Form einer Zeichenfolge festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f0f86-123">The value of this parameter should be set as the CLSID of the service provider in a string form.</span></span> <span data-ttu-id="f0f86-124">Weitere Informationen zu Geräteparametern finden Sie unter [Geräteparameter](device-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f0f86-124">For more information about device parameters, see [Device Parameters](device-parameters.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="f0f86-125">Der Parameterwert muss die CLSID und nicht die ProgID des Dienstanbieters sein.</span><span class="sxs-lookup"><span data-stu-id="f0f86-125">The parameter value must be the CLSID, not the ProgID of the service provider.</span></span>

     

-   <span data-ttu-id="f0f86-126">Der Dienstanbieter für dieses Gerät muss die IMDServiceProvider2-Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="f0f86-126">The service provider for this device must implement the IMDServiceProvider2 interface.</span></span>
-   <span data-ttu-id="f0f86-127">Der Dienstanbieter Schlüssel unter HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows Media Device Manager \\ Plugins \\ SP \\ spname muss den folgenden DWORD-Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="f0f86-127">The service provider key under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows Media Device Manager\\Plugins\\SP\\SPName must contain the following DWORD value</span></span>
    ```
    PnPAware    1
    ```

    

## <a name="related-topics"></a><span data-ttu-id="f0f86-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f0f86-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0f86-129">**Erstellen eines Dienstanbieters**</span><span class="sxs-lookup"><span data-stu-id="f0f86-129">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




