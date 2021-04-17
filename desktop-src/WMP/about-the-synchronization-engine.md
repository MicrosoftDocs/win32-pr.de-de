---
title: Informationen zur Synchronisierungs-Engine
description: Informationen zur Synchronisierungs-Engine
ms.assetid: bb57ffb0-3833-463b-b66c-c23224fa2ba7
keywords:
- Windows Media Player, Synchronisierungs Modul
- Windows Media Player-Objektmodell, Synchronisierungs Modul
- Objektmodell, Synchronisierungs Modul
- Windows Media Player ActiveX-Steuerelement, Synchronisierungs Modul
- ActiveX-Steuerelement, Synchronisierungs Modul
- Windows Media Player Mobile ActiveX-Steuerelement, Synchronisierungs Modul
- Windows Media Player Mobile, Synchronisierungs Modul
- Synchronisieren von Geräten, Synchronisierungs Modul
- Geräte Synchronisierung, Synchronisierungs Modul
- Synchronisierungs Modul
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe0768c4805b074fdaf628a25daf47b9ced97ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389898"
---
# <a name="about-the-synchronization-engine"></a><span data-ttu-id="97b63-113">Informationen zur Synchronisierungs-Engine</span><span class="sxs-lookup"><span data-stu-id="97b63-113">About the Synchronization Engine</span></span>

<span data-ttu-id="97b63-114">Das Synchronisierungs Modul ist die Komponente von Windows Media Player, die das Kopieren von Inhalten digitaler Medien auf tragbare Geräte verwaltet.</span><span class="sxs-lookup"><span data-stu-id="97b63-114">The synchronization engine is the component of Windows Media Player that manages copying digital media content to portable devices.</span></span> <span data-ttu-id="97b63-115">Windows Media Player unterstützt eine einzelne Instanz der Synchronisierungs-Engine für jedes Gerät.</span><span class="sxs-lookup"><span data-stu-id="97b63-115">Windows Media Player supports a single instance of the synchronization engine for each device.</span></span> <span data-ttu-id="97b63-116">Sie müssen eine Remote Instanz des Windows Media Player-Steuer Elements verwenden, um Synchronisierungs Tasks Programm gesteuert auszuführen.</span><span class="sxs-lookup"><span data-stu-id="97b63-116">You must use a remoted instance of the Windows Media Player control to perform synchronization tasks programmatically.</span></span> <span data-ttu-id="97b63-117">Tatsächlich werden die Synchronisierungs-Engine-Instanzen von Ihrem Programm mit Windows Media Player und allen anderen Programmen gemeinsam genutzt, die die Player-Schnittstellen für die Geräte Synchronisierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="97b63-117">In effect, your program shares the synchronization engine instances with Windows Media Player and all other programs that use the Player interfaces for device synchronization.</span></span>

<span data-ttu-id="97b63-118">Sie können [iwmpsyncdevice:: Start](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start) und [iwmpsyncdevice::](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop) End verwenden, um zu steuern, wann das Synchronisierungs Modul funktioniert.</span><span class="sxs-lookup"><span data-stu-id="97b63-118">You can use [IWMPSyncDevice::start](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start) and [IWMPSyncDevice::stop](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop) to control when the synchronization engine does its work.</span></span> <span data-ttu-id="97b63-119">In den meisten Fällen sollten Sie diese Methoden nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="97b63-119">In most cases, you should not use these methods.</span></span> <span data-ttu-id="97b63-120">Stattdessen sollten Sie zulassen, dass das Synchronisierungs Modul seine Arbeit automatisch plant.</span><span class="sxs-lookup"><span data-stu-id="97b63-120">Instead, you should let the synchronization engine schedule its work automatically.</span></span> <span data-ttu-id="97b63-121">Die Methoden zum **starten** und **Abbrechen** sind vorhanden, damit Sie Sie verwenden können, wenn das Programm die Windows Media Player-Benutzeroberfläche ersetzen soll.</span><span class="sxs-lookup"><span data-stu-id="97b63-121">The **start** and **stop** methods exist so that you can use them if your program is designed to replace the Windows Media Player user interface.</span></span> <span data-ttu-id="97b63-122">In diesem Fall empfiehlt es sich, eine Schaltfläche zum Starten und Abbrechen ähnlich der eines Windows-Media Player bereitzustellen, die auf der Registerkarte **Geräte** bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="97b63-122">In this case, you might want to provide a start/stop button similar to the one Windows Media Player provides in the **Devices** tab.</span></span>

<span data-ttu-id="97b63-123">Sie können den Synchronisierungs Fortschritt für ein Gerät überwachen, indem Sie [iwmpsyncdevice:: get \_ Progress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress)abrufen.</span><span class="sxs-lookup"><span data-stu-id="97b63-123">You can monitor the synchronization progress for a device by polling [IWMPSyncDevice::get\_progress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress).</span></span> <span data-ttu-id="97b63-124">Diese Methode ruft einen Fortschritts Wert für den gesamten Synchronisierungs Prozess mit einem bestimmten Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="97b63-124">This method retrieves a progress value for the entire synchronization process with a particular device.</span></span> <span data-ttu-id="97b63-125">Der abgerufene Wert ist eine Zahl, die den Prozentsatz der abgeschlossenen Synchronisierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="97b63-125">The value retrieved is a number that represents the percentage of synchronization complete.</span></span> <span data-ttu-id="97b63-126">Es gibt zwei Ereignisse, die Sie im Zusammenhang mit der Synchronisierung erhalten können.</span><span class="sxs-lookup"><span data-stu-id="97b63-126">There are two events you can receive that are related to synchronization.</span></span> <span data-ttu-id="97b63-127">Wenn ein Problem auftritt, werden Sie durch das Ereignis " **entvicesyncerror** " benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="97b63-127">The **DeviceSyncError** event notifies you when a problem occurs.</span></span> <span data-ttu-id="97b63-128">Das **devicesyncstatechange** -Ereignis warnt Sie, wenn das Synchronisierungs Modul den Status für das aktuelle Gerät geändert hat.</span><span class="sxs-lookup"><span data-stu-id="97b63-128">The **DeviceSyncStateChange** event alerts you when the synchronization engine has changed state for the current device.</span></span>

<span data-ttu-id="97b63-129">Sie können die Menge an Gerätespeicher einschränken, die Windows Media Player für die Synchronisierung verwendet, indem Sie [IWMPSyncDevice2:: abtiteminfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo) mit dem Attribut " **prozentuspacereserved** " aufrufen.</span><span class="sxs-lookup"><span data-stu-id="97b63-129">You can limit the amount of device storage that Windows Media Player uses for synchronization by calling [IWMPSyncDevice2::setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo) with the **PercentSpaceReserved** attribute.</span></span> <span data-ttu-id="97b63-130">Die Verwendung dieser Schnittstelle erfordert Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="97b63-130">Using this interface requires Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97b63-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="97b63-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97b63-132">**Informationen zur Geräte Synchronisierung**</span><span class="sxs-lookup"><span data-stu-id="97b63-132">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="97b63-133">**IWMPEvents2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="97b63-133">**IWMPEvents2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[<span data-ttu-id="97b63-134">**Anzeigen des Synchronisierungs Status**</span><span class="sxs-lookup"><span data-stu-id="97b63-134">**Showing Synchronization Progress**</span></span>](showing-synchronization-progress.md)
</dt> </dl>

 

 




