---
title: Windows Media Device Manager-Geräte Erweiterungen für die metadatenübertragung
description: Windows Media Device Manager-Geräte Erweiterungen für die metadatenübertragung
ms.assetid: c1d84225-b5b1-4f9e-8694-a229653e53de
keywords:
- Windows Media Player, Geräte Erweiterungen
- Windows-Media Player, Erweiterungen
- Windows-Media Player, Metadaten
- Windows Media Player, beschleunigte metadatenübertragung
- Windows Media Player, beschleunigte metadatenübertragung
- Metadaten, Geräte Erweiterungen
- Metadaten, Erweiterungen
- Geräte Erweiterungen, metadatenübertragung
- Erweiterungen, metadatenübertragung
- beschleunigte metadatenübertragung
- Metadaten, beschleunigte Übertragung
- Geräte Erweiterungen, beschleunigte metadatenübertragung
- Erweiterungen, beschleunigte metadatenübertragung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d85ff7026e3395338fdf048c54b8ff7401c9ee7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471437"
---
# <a name="windows-media-device-manager-device-extensions-for-metadata-transfer"></a><span data-ttu-id="196cf-116">Windows Media Device Manager-Geräte Erweiterungen für die metadatenübertragung</span><span class="sxs-lookup"><span data-stu-id="196cf-116">Windows Media Device Manager Device Extensions for Metadata Transfer</span></span>

<span data-ttu-id="196cf-117">Zum Aktivieren der beschleunigten metadatenübertragung müssen Hersteller von Geräten, die MTP nicht unterstützen, im Quellcode folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="196cf-117">To enable accelerated metadata transfer, manufacturers of devices that do not support MTP must do the following in source code:</span></span>

-   <span data-ttu-id="196cf-118">Definieren der **WMP- \_ WMDM- \_ Geräte \_ Unterstützung**.</span><span class="sxs-lookup"><span data-stu-id="196cf-118">Define **WMP\_WMDM\_DEVICE\_SUPPORT**.</span></span>
-   <span data-ttu-id="196cf-119">Fügen Sie wmpdevices. h ein, das als Teil des Windows Media Player SDK installiert wird.</span><span class="sxs-lookup"><span data-stu-id="196cf-119">Include wmpdevices.h, which is installed as part of the Windows Media Player SDK.</span></span>

<span data-ttu-id="196cf-120">Wmpdevices. h definiert die folgenden Strukturen.</span><span class="sxs-lookup"><span data-stu-id="196cf-120">Wmpdevices.h defines the following structures.</span></span>



| <span data-ttu-id="196cf-121">Struktur</span><span class="sxs-lookup"><span data-stu-id="196cf-121">Structure</span></span>                                                                                 | <span data-ttu-id="196cf-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="196cf-122">Description</span></span>                                                                                                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="196cf-123">WMP \_ WMDM \_ - \_ \_ metadatenroundtrip \_ PC2DEVICE</span><span class="sxs-lookup"><span data-stu-id="196cf-123">WMP\_WMDM\_METADATA\_ROUND\_TRIP\_PC2DEVICE</span></span>](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_pc2device) | <span data-ttu-id="196cf-124">Struktur, die von Windows-Media Player verwendet wird, um beschleunigte Metadaten-Synchronisierungs Informationen von tragbaren Geräten anzufordern, die MTP nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="196cf-124">Structure used by Windows Media Player to request accelerated metadata synchronization information from portable devices that do not support MTP.</span></span> |
| [<span data-ttu-id="196cf-125">WMP \_ WMDM \_ - \_ \_ metadatenroundtrip \_ DEVICE2PC</span><span class="sxs-lookup"><span data-stu-id="196cf-125">WMP\_WMDM\_METADATA\_ROUND\_TRIP\_DEVICE2PC</span></span>](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_device2pc) | <span data-ttu-id="196cf-126">Struktur, die von Windows Media Player verwendet wird, um beschleunigte Metadaten-Synchronisierungs Informationen von tragbaren Geräten zu empfangen, die MTP nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="196cf-126">Structure used by Windows Media Player to receive accelerated metadata synchronization information from portable devices that do not support MTP.</span></span> |



 

<span data-ttu-id="196cf-127">Um Informationen von dem Gerät über geänderte Metadaten anzufordern, ruft Windows Media Player 10 oder höher die Windows Media Device Manager-Methode **IWMDMDevice3::D eviceiocontrol** auf.</span><span class="sxs-lookup"><span data-stu-id="196cf-127">To request information from the device about metadata that has changed, Windows Media Player 10 or later calls the Windows Media Device Manager method **IWMDMDevice3::DeviceIoControl**.</span></span> <span data-ttu-id="196cf-128">Wenn Sie diesen Befehl ausführen, befolgt der Player bestimmte Schritte wie folgt:</span><span class="sxs-lookup"><span data-stu-id="196cf-128">When making this call, the Player follows specific steps, as follows:</span></span>

-   <span data-ttu-id="196cf-129">Der erste Parameter, *dwIoControlCode*, enthält die Konstante **IOCTL \_ WMP \_ Metadata \_ \_ Roundtrip**.</span><span class="sxs-lookup"><span data-stu-id="196cf-129">The first parameter, *dwIoControlCode*, contains the constant **IOCTL\_WMP\_METADATA\_ROUND\_TRIP**.</span></span> <span data-ttu-id="196cf-130">Diese Konstante ist in wmpdevices. h definiert.</span><span class="sxs-lookup"><span data-stu-id="196cf-130">This constant is defined in wmpdevices.h.</span></span>
-   <span data-ttu-id="196cf-131">Der zweite Parameter, *lpinbuffer*, verweist auf eine **WMP- \_ WMDM- \_ \_ metadatenroundtrip \_ \_ PC2DEVICE** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="196cf-131">The second parameter, *lpInBuffer*, points to a **WMP\_WMDM\_METADATA\_ROUND\_TRIP\_PC2DEVICE** structure.</span></span>
-   <span data-ttu-id="196cf-132">Der dritte Parameter *nInBufferSize* enthält die Größe des Eingabe Puffers.</span><span class="sxs-lookup"><span data-stu-id="196cf-132">The third parameter, *nInBufferSize*, contains the size of the input buffer.</span></span>
-   <span data-ttu-id="196cf-133">Der vierte Parameter, *lpoutbuffer*, verweist auf eine **WMP- \_ WMDM- \_ \_ metadatenroundtrip \_ \_ DEVICE2PC** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="196cf-133">The fourth parameter, *lpOutBuffer*, points to a **WMP\_WMDM\_METADATA\_ROUND\_TRIP\_DEVICE2PC** structure.</span></span> <span data-ttu-id="196cf-134">Das Gerät muss diese Struktur mit Informationen zu Änderungen ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="196cf-134">The device must fill in this structure with information about changes.</span></span>
-   <span data-ttu-id="196cf-135">Der fünfte Parameter, *pnoutbuffersize*, empfängt die Größe des Ausgabepuffers.</span><span class="sxs-lookup"><span data-stu-id="196cf-135">The fifth parameter, *pnOutBufferSize*, receives the size of the output buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="196cf-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="196cf-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="196cf-137">**Geräte Erweiterungen für die beschleunigte metadatenübertragung**</span><span class="sxs-lookup"><span data-stu-id="196cf-137">**Device Extensions for Accelerated Metadata Transfer**</span></span>](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




