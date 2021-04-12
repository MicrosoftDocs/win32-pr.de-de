---
title: Ausführen der Near-Erkennung
description: Ausführen der Near-Erkennung
ms.assetid: 73207c4c-2d8d-4ec3-b3d0-78f55ee0a754
keywords:
- Windows Media-Format-SDK, Ausführen der Near-Erkennung
- Windows Media-Format-SDK, Näherungs Erkennung
- Advanced Systems Format (ASF), durchführen der Near-Erkennung
- ASF (Advanced Systems Format), durchführen der Near-Erkennung
- Advanced Systems Format (ASF), near-Erkennung
- ASF (Advanced Systems Format), near-Erkennung
- Digital Rights Management (DRM), durchführen der Near-Erkennung
- DRM (Digital Rights Management), durchführen der Near-Erkennung
- Digital Rights Management (DRM), Näherungs Erkennung
- DRM (Digital Rights Management), Näherungs Erkennung
- Near-Erkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9628a6c33832b56858e5c457f15fd0935c2c436
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389830"
---
# <a name="performing-proximity-detection"></a><span data-ttu-id="b6d8d-114">Ausführen der Near-Erkennung</span><span class="sxs-lookup"><span data-stu-id="b6d8d-114">Performing Proximity Detection</span></span>

<span data-ttu-id="b6d8d-115">Bevor Sie verschlüsselte Daten auf ein registriertes Gerät im Windows Media DRM 10 for Network Devices-Protokoll streamen können, müssen Sie einen Prozess namens near-Erkennung (auch als Validierung bezeichnet) ausführen.</span><span class="sxs-lookup"><span data-stu-id="b6d8d-115">Before you can stream encrypted data to a registered device in the Windows Media DRM 10 for Network Devices protocol, you must perform a process called proximity detection (also called validation).</span></span> <span data-ttu-id="b6d8d-116">Dieser Prozess umfasst das Senden von Nachrichten an das Gerät und das Empfangen von Antworten.</span><span class="sxs-lookup"><span data-stu-id="b6d8d-116">This process involves sending messages to the device and receiving responses.</span></span> <span data-ttu-id="b6d8d-117">Die Zeit, die zum Empfangen einer Antwort benötigt wird, wird verwendet, um zu bestimmen, ob das Gerät für den Computer im Netzwerk "nah" genug ist, um sichere Daten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b6d8d-117">The time it takes to receive a response is used to determine whether the device is "near" enough to the computer on the network to receive secure data.</span></span> <span data-ttu-id="b6d8d-118">Wenn Sie bestätigen, dass sich das Gerät physisch in der Nähe des Client Computers im Netzwerk befindet, hilft es, Spoofing und anderen nicht autorisierten Zugriff zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="b6d8d-118">Confirming that the device is physically close to the client computer on the network helps to prevent spoofing and other unauthorized access.</span></span>

<span data-ttu-id="b6d8d-119">Wenn die Near-Erkennung erfolgreich abgeschlossen wurde, wird das Gerät als gültig bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b6d8d-119">When proximity detection is successfully completed, the device is said to be valid.</span></span> <span data-ttu-id="b6d8d-120">Sie können überprüfen, ob ein Gerät gültig ist, indem Sie die [**iwmregistereddevice:: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b6d8d-120">You can check whether a device is valid by calling the [**IWMRegisteredDevice::IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) method.</span></span> <span data-ttu-id="b6d8d-121">Geräte müssen alle 48 Stunden überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="b6d8d-121">Devices must be validated every 48 hours.</span></span> <span data-ttu-id="b6d8d-122">Ein Gerät, das mehr als 48 Stunden vor der Programmausführung überprüft wurde, muss erneut überprüft werden, indem der Near-Erkennungsprozess erneut ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b6d8d-122">A device that was validated more than 48 hours before your program runs must be revalidated by performing the proximity detection process again.</span></span>

<span data-ttu-id="b6d8d-123">Um die Near-Erkennung durchzuführen, müssen Sie die Kommunikation mit dem Gerät einrichten und dann die [**iwmaccessmityerkennungs:: starterkennungs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmproximitydetection-startdetection) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b6d8d-123">To perform proximity detection, you must establish communications with the device and then call the [**IWMProximityDetection::StartDetection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmproximitydetection-startdetection) method.</span></span> <span data-ttu-id="b6d8d-124">Der Erkennungs Vorgang wird asynchron von den internen DRM-Komponenten des Windows Media Format SDK abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b6d8d-124">The detection process is completed asynchronously by the internal DRM components of the Windows Media Format SDK.</span></span> <span data-ttu-id="b6d8d-125">Die Anwendung muss eine Implementierung der [**iwmstatus Callback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) -Schnittstelle enthalten, um Near-Erkennungs Meldungen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="b6d8d-125">Your application must include an implementation of the [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) interface to process proximity detection messages.</span></span>

<span data-ttu-id="b6d8d-126">Es gibt zwei Nachrichten, die vom Near-Erkennungsprozess gesendet werden: eine Ergebnis Meldung und eine Abschluss Meldung.</span><span class="sxs-lookup"><span data-stu-id="b6d8d-126">There are two messages that are sent by the proximity detection process: a result message and a completion message.</span></span>

<span data-ttu-id="b6d8d-127">\_Wenn der Erkennungsprozess abgeschlossen ist, wird die Ergebnis Meldung, das WMT-near- \_ Ergebnis, gesendet.</span><span class="sxs-lookup"><span data-stu-id="b6d8d-127">The result message, WMT\_PROXIMITY\_RESULT, is sent when the detection process is completed.</span></span> <span data-ttu-id="b6d8d-128">Der *HR* -Parameter der [**OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Rückruf Methode gibt an, ob das Gerät fast genug für den Client Computer ist.</span><span class="sxs-lookup"><span data-stu-id="b6d8d-128">The *hr* parameter of the [**OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method indicates whether the device was found to be near enough to the client computer.</span></span> <span data-ttu-id="b6d8d-129">Wenn der *HR* -Parameter der Ergebnis Meldung Erfolg angibt, enthält der *pValue* -Parameter ein **DWORD** , das die gemessene Latenz für das Gerät in Millisekunden angibt.</span><span class="sxs-lookup"><span data-stu-id="b6d8d-129">If the *hr* parameter of the result message indicates success, the *pValue* parameter contains a **DWORD** specifying the measured latency to the device in milliseconds.</span></span>

<span data-ttu-id="b6d8d-130">Die Abschluss Meldung, die WMT- \_ Nähe ist \_ abgeschlossen, wird gesendet, wenn die Erkennung abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="b6d8d-130">The completion message, WMT\_PROXIMITY\_COMPLETED, is sent when the detection is finalized.</span></span> <span data-ttu-id="b6d8d-131">Sie sollten die [**iwmkurzmityerkennungs**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) -Schnittstelle erst freigeben, nachdem Sie diese Nachricht empfangen haben.</span><span class="sxs-lookup"><span data-stu-id="b6d8d-131">You should release the [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) interface only after receiving this message.</span></span>

<span data-ttu-id="b6d8d-132">Wenn die Near-Erkennung für ein Gerät erfolgreich ist, wird die Geräte Registrierungsdatenbank automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b6d8d-132">When proximity detection for a device succeeds, the device registration database is automatically updated.</span></span> <span data-ttu-id="b6d8d-133">Nachfolgende Aufrufe von [**iwmregistereddevice:: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) geben " **true** " zurück, bis 48 Stunden vergangen sind und das Gerät erneut überprüft werden muss.</span><span class="sxs-lookup"><span data-stu-id="b6d8d-133">Subsequent calls to [**IWMRegisteredDevice::IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) will return **TRUE** until 48 hours have passed and the device needs to be revalidated.</span></span>

<span data-ttu-id="b6d8d-134">**Hinweis** DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b6d8d-134">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6d8d-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b6d8d-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6d8d-136">**Verwenden des Protokolls "Windows Media DRM 10 for Network Devices"**</span><span class="sxs-lookup"><span data-stu-id="b6d8d-136">**Using the Windows Media DRM 10 for Network Devices Protocol**</span></span>](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




