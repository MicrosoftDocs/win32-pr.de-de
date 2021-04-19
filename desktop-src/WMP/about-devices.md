---
title: Informationen zu Geräten
description: Informationen zu Geräten
ms.assetid: 9e68c5eb-5fcb-4d7d-8dbb-7e951f253df8
keywords:
- Windows Media Player, Synchronisieren von Geräten
- Windows Media Player-Objektmodell, Synchronisieren von Geräten
- Objektmodell, Synchronisieren von Geräten
- Windows Media Player ActiveX-Steuerelement, Synchronisieren von Geräten
- ActiveX-Steuerelement, Synchronisieren von Geräten
- Windows Media Player Mobile ActiveX-Steuerelement, Synchronisieren von Geräten
- Windows Media Player Mobile, Synchronisieren von Geräten
- Synchronisieren von Geräten, Informationen zu
- Geräte Synchronisierung, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e89a074e4edb5bdbc7d90391398d5e0e4133505a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106339867"
---
# <a name="about-devices"></a><span data-ttu-id="d5223-112">Informationen zu Geräten</span><span class="sxs-lookup"><span data-stu-id="d5223-112">About Devices</span></span>

<span data-ttu-id="d5223-113">Portable Geräte sind Hardware Geräte, die Benutzer zum Nutzen digitaler Medieninhalte nutzen, wenn Sie nicht mehr von Ihrem Computer entfernt sind.</span><span class="sxs-lookup"><span data-stu-id="d5223-113">Portable devices are hardware devices that users carry to enjoy digital media content when they are away from their computer.</span></span> <span data-ttu-id="d5223-114">In der Regel sind tragbare Geräte Akku Betrieb.</span><span class="sxs-lookup"><span data-stu-id="d5223-114">Typically, portable devices are battery operated.</span></span> <span data-ttu-id="d5223-115">Einige Geräte können nur Musik abspielen.</span><span class="sxs-lookup"><span data-stu-id="d5223-115">Some devices can play music only.</span></span> <span data-ttu-id="d5223-116">Andere Geräte können Videos und Musik abspielen.</span><span class="sxs-lookup"><span data-stu-id="d5223-116">Other devices can play video and music.</span></span>

<span data-ttu-id="d5223-117">Einige Geräte unterstützen die automatische Synchronisierung digitaler Medieninhalte mit Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d5223-117">Some devices support automatic synchronization of digital media content with Windows Media Player.</span></span> <span data-ttu-id="d5223-118">Andere Geräte unterstützen nur die manuelle Übertragung.</span><span class="sxs-lookup"><span data-stu-id="d5223-118">Other devices support only manual transfer.</span></span> <span data-ttu-id="d5223-119">Sie können bestimmen, ob ein bestimmtes Gerät die automatische Synchronisierung unterstützt, indem Sie [iwmpsyncdevice:: get- \_ Status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) aufrufen und dann den abgerufenen [wmpdevicestatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) -Wert überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d5223-119">You can determine whether a particular device supports automatic synchronization by calling [IWMPSyncDevice::get\_status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) and then inspecting the [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) value retrieved.</span></span> <span data-ttu-id="d5223-120">Wenn der abgerufene Wert **wmpdsmanualdevice** lautet, unterstützt das Gerät keine automatische Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="d5223-120">If the retrieved value is **wmpdsManualDevice**, the device does not support automatic synchronization.</span></span>

<span data-ttu-id="d5223-121">Die Geräte, die mit dem Computer des Benutzers verbunden sind, können aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="d5223-121">You can enumerate the devices connected to the user's computer.</span></span> <span data-ttu-id="d5223-122">Verwenden Sie zu diesem Zweck zuerst [iwmpsyncservices:: get \_ devicecount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-get_devicecount) , um die Anzahl der Geräte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d5223-122">To do this, first use [IWMPSyncServices::get\_deviceCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-get_devicecount) to retrieve the count of devices.</span></span> <span data-ttu-id="d5223-123">Nennen Sie dann in einer-Schleife [iwmpsyncservices:: getdevice](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-getdevice), und übergeben Sie jedes Mal den entsprechenden Indexwert.</span><span class="sxs-lookup"><span data-stu-id="d5223-123">Then, in a loop, call [IWMPSyncServices::getDevice](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-getdevice), passing the appropriate index value each time.</span></span> <span data-ttu-id="d5223-124">Mit [iwmpsyncdevice:: get- \_ Verbindung](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected) können Sie auswerten, ob ein bestimmtes Gerät zurzeit verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="d5223-124">You can use [IWMPSyncDevice::get\_connected](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected) to evaluate whether a particular device is currently connected.</span></span>

<span data-ttu-id="d5223-125">Wenn Sie wissen möchten, wenn Geräte eine Verbindung herstellen oder trennen, können Sie die Ereignisse **deviceconnetct** und **devicedisconnect** empfangen.</span><span class="sxs-lookup"><span data-stu-id="d5223-125">To know when devices connect or disconnect, you can receive the **DeviceConnect** and **DeviceDisconnect** events.</span></span> <span data-ttu-id="d5223-126">Diese Ereignisse werden über die **IWMPEvents2** -Schnittstelle empfangen.</span><span class="sxs-lookup"><span data-stu-id="d5223-126">These events are received through the **IWMPEvents2** interface.</span></span>

<span data-ttu-id="d5223-127">Die **iwmpsyncdevice** -Schnittstelle stellt zusätzliche Methoden bereit, mit denen Sie Informationen zu einem Gerät erhalten oder festlegen können.</span><span class="sxs-lookup"><span data-stu-id="d5223-127">The **IWMPSyncDevice** interface provides additional methods to enable you to get or set information about a device.</span></span> <span data-ttu-id="d5223-128">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d5223-128">For example:</span></span>

-   <span data-ttu-id="d5223-129">Mit den Methoden **get \_ FriendlyName** und **Put \_ FriendlyName** können Sie den Namen des benutzerdefinierten Geräts abrufen und angeben.</span><span class="sxs-lookup"><span data-stu-id="d5223-129">The **get\_FriendlyName** and **put\_FriendlyName** methods enable you to retrieve and specify the user-defined device name.</span></span>
-   <span data-ttu-id="d5223-130">Mit der Methode " **get \_ DeviceName** " können Sie den Gerätenamen abrufen, den Benutzer in der Windows XP-Shell sehen.</span><span class="sxs-lookup"><span data-stu-id="d5223-130">The **get\_deviceName** method enables you to retrieve the device name that users see in the Windows XP shell.</span></span>
-   <span data-ttu-id="d5223-131">Die **getiteminfo** -Methode ermöglicht das Abrufen von Metadaten von Geräten.</span><span class="sxs-lookup"><span data-stu-id="d5223-131">The **getItemInfo** method enables you to retrieve metadata from devices.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5223-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d5223-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5223-133">**Informationen zur Geräte Synchronisierung**</span><span class="sxs-lookup"><span data-stu-id="d5223-133">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="d5223-134">**IWMPEvents2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="d5223-134">**IWMPEvents2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[<span data-ttu-id="d5223-135">**Iwmpsyncdevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="d5223-135">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[<span data-ttu-id="d5223-136">**Arbeiten mit tragbaren Geräten**</span><span class="sxs-lookup"><span data-stu-id="d5223-136">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




