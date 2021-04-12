---
title: Informationen zu Partnerschaften
description: Informationen zu Partnerschaften
ms.assetid: d21813ed-efe0-48a2-a1bf-f10f4b7ac3e6
keywords:
- Windows Media Player, Partnerschaften
- Windows Media Player-Objektmodell, Partnerschaften
- Objektmodell, Partnerschaften
- Windows Media Player ActiveX-Steuerelement, Partnerschaften
- ActiveX-Steuerelement, Partnerschaften
- Windows Media Player Mobile ActiveX-Steuerelement, Partnerschaften
- Windows Media Player Mobile, Partnerschaften
- Synchronisieren von Geräten, Partnerschaften
- Geräte Synchronisierung, Partnerschaften
- Partnerschaften zwischen Geräten und Windows-Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cfc3fa20e1e8a4b6a4c7993ea7dcc5842719f2a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104472244"
---
# <a name="about-partnerships"></a><span data-ttu-id="9dbe1-113">Informationen zu Partnerschaften</span><span class="sxs-lookup"><span data-stu-id="9dbe1-113">About Partnerships</span></span>

<span data-ttu-id="9dbe1-114">Eine Partnerschaft ist eine besondere Beziehung zwischen einem tragbaren Gerät und Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9dbe1-114">A partnership is a special relationship between a portable device and Windows Media Player.</span></span> <span data-ttu-id="9dbe1-115">Benutzer können mithilfe der Windows Media Player-Benutzeroberfläche eine Partnerschaft für ein bestimmtes Gerät einrichten.</span><span class="sxs-lookup"><span data-stu-id="9dbe1-115">Users can establish a partnership for a particular device by using the Windows Media Player user interface.</span></span> <span data-ttu-id="9dbe1-116">Partnerschaften können mithilfe von [iwmpsyncdevice:: createpartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) und [iwmpsyncdevice::d eletepartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership)Programm gesteuert verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="9dbe1-116">You can programmatically manage partnerships by using [IWMPSyncDevice::createPartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) and [IWMPSyncDevice::deletePartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership).</span></span> <span data-ttu-id="9dbe1-117">Die **createpartnership** -Methode startet einen asynchronen Prozess, der endet, wenn das **createpartnershipcomplete** -Ereignis über die **IWMPEvents2** -Schnittstelle empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="9dbe1-117">The **createPartnership** method starts an asynchronous process that ends when the **CreatePartnershipComplete** event is received through the **IWMPEvents2** interface.</span></span>

<span data-ttu-id="9dbe1-118">Windows Media Player 10 oder höher unterstützt die Erstellung von Partnerschaften mit bis zu 16 Geräten.</span><span class="sxs-lookup"><span data-stu-id="9dbe1-118">Windows Media Player 10 or later supports creating partnerships with up to 16 devices.</span></span> <span data-ttu-id="9dbe1-119">Jede Partnerschaft verfügt über einen zugeordneten Partnerschafts Index.</span><span class="sxs-lookup"><span data-stu-id="9dbe1-119">Each partnership has an associated partnership index.</span></span> <span data-ttu-id="9dbe1-120">Sie können den Partnerschafts Index für ein bestimmtes Gerät abrufen, indem Sie [iwmpsyncdevice:: get \_ partnershipindex](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9dbe1-120">You can retrieve the partnership index for a particular device by calling [IWMPSyncDevice::get\_partnershipIndex](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex).</span></span> <span data-ttu-id="9dbe1-121">Partnerschafts Indizes sind von 1 bis 16 nummeriert.</span><span class="sxs-lookup"><span data-stu-id="9dbe1-121">Partnership indices are numbered from 1 to 16.</span></span> <span data-ttu-id="9dbe1-122">Wenn ein bestimmtes Gerät nicht über eine Partnerschaft mit Windows Media Player verfügt, gibt **getpartnershipindex** für den Index 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="9dbe1-122">When a particular device does not have a partnership with Windows Media Player, **getPartnershipIndex** returns zero for the index.</span></span>

<span data-ttu-id="9dbe1-123">Sie können den Partnerschaftsstatus eines bestimmten Geräts abrufen, indem Sie [iwmpsyncdevice:: get- \_ Status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) aufrufen und dann den abgerufenen [wmpdevicestatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) -Wert überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9dbe1-123">You can retrieve the partnership status of a particular device by calling [IWMPSyncDevice::get\_status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) and then inspecting the [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) value retrieved.</span></span> <span data-ttu-id="9dbe1-124">Windows Media Player ermöglicht eine Partnerschaft mit der Bibliothek eines Benutzers auf einem Computer für jedes Gerät.</span><span class="sxs-lookup"><span data-stu-id="9dbe1-124">Windows Media Player allows one partnership with one user's library on one computer for each device.</span></span> <span data-ttu-id="9dbe1-125">Dies bedeutet, dass das Erstellen einer neuen Partnerschaft eine vorhandene Partnerschaft zerstört, die das aktuelle Gerät möglicherweise mit einem anderen Computer hat.</span><span class="sxs-lookup"><span data-stu-id="9dbe1-125">This means that creating a new partnership destroys any existing partnership the current device might have with another computer.</span></span> <span data-ttu-id="9dbe1-126">Wenn Sie wissen möchten, wann sich der Status für ein Gerät ändert, können Sie das **devicestatuschange** -Ereignis empfangen.</span><span class="sxs-lookup"><span data-stu-id="9dbe1-126">To know when the status changes for a device, you can receive the **DeviceStatusChange** event.</span></span>

<span data-ttu-id="9dbe1-127">Windows Media Player kann keine Partnerschaft mit einem Gerät erstellen, das den Status **wmpdsmanualdevice** hat.</span><span class="sxs-lookup"><span data-stu-id="9dbe1-127">Windows Media Player cannot create a partnership with a device having the status **wmpdsManualDevice**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9dbe1-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9dbe1-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dbe1-129">**Informationen zur Geräte Synchronisierung**</span><span class="sxs-lookup"><span data-stu-id="9dbe1-129">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="9dbe1-130">**IWMPEvents2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="9dbe1-130">**IWMPEvents2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[<span data-ttu-id="9dbe1-131">**Arbeiten mit tragbaren Geräten**</span><span class="sxs-lookup"><span data-stu-id="9dbe1-131">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




