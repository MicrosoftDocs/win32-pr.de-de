---
title: Verwenden des Protokolls "Windows Media DRM 10 for Network Devices"
description: Verwenden des Protokolls "Windows Media DRM 10 for Network Devices"
ms.assetid: dec88d72-718c-42ab-8d48-eddf906051ef
keywords:
- Windows Media-Format-SDK, Windows Media DRM 10 für Netzwerkgeräte
- Windows Media-Format-SDK, DRM 10 für Netzwerkgeräte
- Advanced Systems Format (ASF), Windows Media DRM 10 für Netzwerkgeräte
- ASF (Advanced Systems Format), Windows Media DRM 10 für Netzwerkgeräte
- Advanced Systems Format (ASF), DRM 10 für Netzwerkgeräte
- ASF (Advanced Systems Format), DRM 10 für Netzwerkgeräte
- Digital Rights Management (DRM), Windows Media DRM 10 für Netzwerkgeräte
- DRM (Digital Rights Management), Windows Media DRM 10 für Netzwerkgeräte
- Digital Rights Management (DRM), DRM 10 für Netzwerkgeräte
- DRM (Digital Rights Management), DRM 10 für Netzwerkgeräte
- Windows Media DRM 10 für Netzwerkgeräte, Protokolle
- DRM 10 für Netzwerkgeräte, Protokolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73908c66dbffe7f50f4f28beb520861611d59962
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309887"
---
# <a name="using-the-windows-media-drm-10-for-network-devices-protocol"></a><span data-ttu-id="09760-115">Verwenden des Protokolls "Windows Media DRM 10 for Network Devices"</span><span class="sxs-lookup"><span data-stu-id="09760-115">Using the Windows Media DRM 10 for Network Devices Protocol</span></span>

<span data-ttu-id="09760-116">Das Windows Media-Format SDK bietet einige Features zur Unterstützung des sicheren Netzwerkgeräte Protokolls, Windows Media DRM 10 für Netzwerkgeräte.</span><span class="sxs-lookup"><span data-stu-id="09760-116">The Windows Media Format SDK provides some features to support the secure network device protocol, Windows Media DRM 10 for Network Devices.</span></span> <span data-ttu-id="09760-117">Dieses Protokoll definiert die Nachrichten, die zwischen einem digitalen Medienwiedergabe Gerät (z. b. einem Top-Video Player) und dem Computer, der Daten für das Gerät bedient, gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="09760-117">This protocol defines the messages sent between a digital media playback device, such as a set-top video player, and the computer that serves data to the device.</span></span> <span data-ttu-id="09760-118">Die zwischen dem Server und dem Gerät gesendeten Mediendaten werden verschlüsselt, um Sie vor dem abfangen zu schützen.</span><span class="sxs-lookup"><span data-stu-id="09760-118">The media data sent between server and device is encrypted to protect it from interception.</span></span>

<span data-ttu-id="09760-119">Die Kommunikation zwischen Ihrer Anwendung und Geräten, die Windows Media DRM 10 für Netzwerkgeräte unterstützen, kann alle von Ihnen bevorzugten Netzwerkprotokolle verwenden.</span><span class="sxs-lookup"><span data-stu-id="09760-119">The communication between your application and devices that support Windows Media DRM 10 for Network Devices can use whatever networking protocols you prefer.</span></span> <span data-ttu-id="09760-120">Das Windows Media-Format-SDK stellt keine Objekte bereit, die die Netzwerkkommunikation für Sie ausführen.</span><span class="sxs-lookup"><span data-stu-id="09760-120">The Windows Media Format SDK does not provide any objects that perform the network communications for you.</span></span> <span data-ttu-id="09760-121">Stattdessen verarbeiten die Objekte dieses SDK einige Windows Media DRM 10 für Netzwerkgeräte Nachrichten, nachdem Sie von Ihrer Anwendung empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="09760-121">Instead, the objects of this SDK process some Windows Media DRM 10 for Network Devices messages after your application has received them.</span></span>

<span data-ttu-id="09760-122">Zu den Features, die Windows Media DRM 10 für Netzwerkgeräte unterstützen, gehören die Geräteregistrierung, die Near-Erkennung und die Typumwandlung von DRM-geschützten Dateien</span><span class="sxs-lookup"><span data-stu-id="09760-122">The features that support Windows Media DRM 10 for Network Devices are device registration, proximity detection, and converting DRM-protected files.</span></span> <span data-ttu-id="09760-123">Diese Features werden in den folgenden Abschnitten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="09760-123">These features are described in the following sections.</span></span>



| <span data-ttu-id="09760-124">`Section`</span><span class="sxs-lookup"><span data-stu-id="09760-124">Section</span></span>                                                                                                                                                                          | <span data-ttu-id="09760-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="09760-125">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09760-126">Geräteregistrierung</span><span class="sxs-lookup"><span data-stu-id="09760-126">Device Registration</span></span>](device-registration.md)                                                                                                                                   | <span data-ttu-id="09760-127">Beschreibt, wie Registrierungs Anforderungs Nachrichten von Geräten verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="09760-127">Describes how to process registration request messages from devices.</span></span>                                                                       |
| [<span data-ttu-id="09760-128">Ausführen der Near-Erkennung</span><span class="sxs-lookup"><span data-stu-id="09760-128">Performing Proximity Detection</span></span>](performing-proximity-detection.md)                                                                                                             | <span data-ttu-id="09760-129">Beschreibt den Prozess der Near-Erkennung.</span><span class="sxs-lookup"><span data-stu-id="09760-129">Describes the proximity detection process.</span></span>                                                                                                 |
| [<span data-ttu-id="09760-130">Wandeln Sie eine DRM-Protected Datei in eine Windows Media DRM 10 for Network Devices Stream-Datei um.</span><span class="sxs-lookup"><span data-stu-id="09760-130">Converting a DRM-Protected File to a Windows Media DRM 10 for Network Devices Stream</span></span>](converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream.md) | <span data-ttu-id="09760-131">Beschreibt, wie eine DRM-geschützte Datei in einen Stream konvertiert wird, der an ein Gerät gesendet werden kann, das Windows Media DRM 10 für Netzwerkgeräte verwendet.</span><span class="sxs-lookup"><span data-stu-id="09760-131">Describes how to convert a DRM-protected file to a stream that can be sent to a device that uses Windows Media DRM 10 for Network Devices.</span></span> |



 

> [!Note]  
> <span data-ttu-id="09760-132">DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="09760-132">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="09760-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="09760-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09760-134">**Aktivieren DRM-Unterstützung**</span><span class="sxs-lookup"><span data-stu-id="09760-134">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




