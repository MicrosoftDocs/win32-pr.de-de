---
description: 'Diese Programmier Referenz für das Core-audiosdk umfasst die folgenden Eigenschaften:'
ms.assetid: db7d68c3-5642-4238-a212-88d3479ce73d
title: Kernaudioeigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41528e66977f1f3b9282cf78ba76e4bae32c5bd6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522891"
---
# <a name="core-audio-properties"></a><span data-ttu-id="01e65-103">Kernaudioeigenschaften</span><span class="sxs-lookup"><span data-stu-id="01e65-103">Core Audio Properties</span></span>

<span data-ttu-id="01e65-104">Diese Programmier Referenz für das Core-audiosdk umfasst die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="01e65-104">This programming reference for the Core Audio SDK includes the following properties.</span></span>

## <a name="audio-endpoint-properties"></a><span data-ttu-id="01e65-105">Eigenschaften des audioendpunkts</span><span class="sxs-lookup"><span data-stu-id="01e65-105">Audio Endpoint Properties</span></span>

<span data-ttu-id="01e65-106">Das Core-audiosdk umfasst mehrere Eigenschaften von [audioendpunktgeräten](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="01e65-106">Core Audio SDK includes several properties of [audio endpoint devices](audio-endpoint-devices.md).</span></span> <span data-ttu-id="01e65-107">Weitere Informationen finden Sie unter [Eigenschaften für audioendpunkte](audio-endpoint-properties.md).</span><span class="sxs-lookup"><span data-stu-id="01e65-107">For more information, see [Audio Endpoint Properties](audio-endpoint-properties.md).</span></span>

<span data-ttu-id="01e65-108">Die folgenden Eigenschaften sind in "mmdeviceapi. h" in Windows Vista und höher definiert.</span><span class="sxs-lookup"><span data-stu-id="01e65-108">The following properties are defined in Mmdeviceapi.h in Windows Vista and later.</span></span>



| <span data-ttu-id="01e65-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="01e65-109">Property</span></span>                                                                                                            | <span data-ttu-id="01e65-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01e65-110">Description</span></span>                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01e65-111">**Pkey \_ audioendpoint-Zuordnung \_**</span><span class="sxs-lookup"><span data-stu-id="01e65-111">**PKEY\_AudioEndpoint\_Association**</span></span>](pkey-audioendpoint-association.md)                                          | <span data-ttu-id="01e65-112">Ordnet einem audioendpunktgerät eine-PIN-Kategorie (Kernel Streaming) zu.</span><span class="sxs-lookup"><span data-stu-id="01e65-112">Associates a kernel-streaming (KS) pin category with an audio endpoint device.</span></span>                                                                                |
| [<span data-ttu-id="01e65-113">**Pkey \_ audioendpoint \_ controlpanelpageprovider**</span><span class="sxs-lookup"><span data-stu-id="01e65-113">**PKEY\_AudioEndpoint\_ControlPanelPageProvider**</span></span>](pkey-audioendpoint-controlpanelpageprovider.md)                | <span data-ttu-id="01e65-114">Gibt die CLSID des registrierten Anbieters der Geräteeigenschaften Erweiterung für das audioendpunkt-Gerät an.</span><span class="sxs-lookup"><span data-stu-id="01e65-114">Specifies the CLSID of the registered provider of the device-properties extension for the audio endpoint device.</span></span>                                              |
| [<span data-ttu-id="01e65-115">**Pkey \_ audioendpoint \_ Deaktivieren von \_ sysfx**</span><span class="sxs-lookup"><span data-stu-id="01e65-115">**PKEY\_AudioEndpoint\_Disable\_SysFx**</span></span>](pkey-audioendpoint-disable-sysfx.md)                                     | <span data-ttu-id="01e65-116">Gibt an, ob System Effekte im freigegebenen Modus-Stream aktiviert sind, der zum oder vom audioendpunktgerät fließt.</span><span class="sxs-lookup"><span data-stu-id="01e65-116">Indicates whether system effects are enabled in the shared-mode stream that flows to or from the audio endpoint device.</span></span>                                       |
| [<span data-ttu-id="01e65-117">**Pkey- \_ audioendpoint- \_ FormFactor**</span><span class="sxs-lookup"><span data-stu-id="01e65-117">**PKEY\_AudioEndpoint\_FormFactor**</span></span>](pkey-audioendpoint-formfactor.md)                                            | <span data-ttu-id="01e65-118">Gibt die physischen Attribute des audioendpunktgeräts an.</span><span class="sxs-lookup"><span data-stu-id="01e65-118">Indicates the physical attributes of the audio endpoint device.</span></span>                                                                                               |
| [<span data-ttu-id="01e65-119">**Pkey- \_ audioendpoint \_ fullrangespeakers**</span><span class="sxs-lookup"><span data-stu-id="01e65-119">**PKEY\_AudioEndpoint\_FullRangeSpeakers**</span></span>](pkey-audioendpoint-fullrangespeakers.md)                              | <span data-ttu-id="01e65-120">Gibt die Kanal konfigurationsmaske für die vollständig gültigen Referenten an, die mit dem audioendpunktgerät verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="01e65-120">Specifies the channel-configuration mask for the full-range speakers that are connected to the audio endpoint device.</span></span>                                         |
| [<span data-ttu-id="01e65-121">**Pkey- \_ audioendpunkt- \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="01e65-121">**PKEY\_AudioEndpoint\_GUID**</span></span>](pkey-audioendpoint-guid.md)                                                        | <span data-ttu-id="01e65-122">Gibt den DirectSound-Geräte Bezeichner an, der dem audioendpunktgerät entspricht.</span><span class="sxs-lookup"><span data-stu-id="01e65-122">Supplies the DirectSound device identifier that corresponds to the audio endpoint device.</span></span>                                                                     |
| [<span data-ttu-id="01e65-123">**Pkey \_ audioendpoint \_ physicalspeakers**</span><span class="sxs-lookup"><span data-stu-id="01e65-123">**PKEY\_AudioEndpoint\_PhysicalSpeakers**</span></span>](pkey-audioendpoint-physicalspeakers.md)                                | <span data-ttu-id="01e65-124">Definiert die physische Lautsprecher Konfiguration für das audioendpunktgerät.</span><span class="sxs-lookup"><span data-stu-id="01e65-124">Defines the physical speaker configuration for the audio endpoint device.</span></span>                                                                                     |
| [<span data-ttu-id="01e65-125">**Pkey \_ Audioengine \_ deviceformat**</span><span class="sxs-lookup"><span data-stu-id="01e65-125">**PKEY\_AudioEngine\_DeviceFormat**</span></span>](pkey-audioengine-deviceformat.md)                                            | <span data-ttu-id="01e65-126">Gibt das Geräte Format an. Hierbei handelt es sich um das Format, das die Audioengine für den Stream im freigegebenen Modus verwendet, der zum oder vom audioendpunktgerät fließt.</span><span class="sxs-lookup"><span data-stu-id="01e65-126">Specifies the device format, which is the format that the audio engine uses for the shared-mode stream that flows to or from the audio endpoint device.</span></span>       |
| [<span data-ttu-id="01e65-127">**Pkey \_ Audioengine- \_ oemformat**</span><span class="sxs-lookup"><span data-stu-id="01e65-127">**PKEY\_AudioEngine\_OEMFormat**</span></span>](pkey-audioengine-oemformat.md)<br/>                                       | <span data-ttu-id="01e65-128">Gibt das Standardformat des Geräts an, das zum Rendern oder Erfassen eines Streams verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="01e65-128">Specifies the default format of the device that is used for rendering or capturing a stream.</span></span> <span data-ttu-id="01e65-129">Die Werte werden vom OEM in einer INF-Datei aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="01e65-129">The values are populated by the OEM in an .inf file.</span></span> <br/> |
| [<span data-ttu-id="01e65-130">**Pkey \_ audioendpoint \_ unterstützt den \_ ereignisbasierten \_ Modus**</span><span class="sxs-lookup"><span data-stu-id="01e65-130">**PKEY\_AudioEndpoint\_Supports\_EventDriven\_Mode**</span></span>](pkey-audioendpoint-supports-eventdriven-mode.md)<br/> | <span data-ttu-id="01e65-131">Gibt an, ob der Endpunkt den ereignisgesteuerten Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="01e65-131">Indicates whether the endpoint supports the event-driven mode.</span></span> <span data-ttu-id="01e65-132">Die Werte werden vom OEM in einer INF-Datei aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="01e65-132">The values are populated by the OEM in an .inf file.</span></span><br/>                                |
| [<span data-ttu-id="01e65-133">**Pkey- \_ audioendpoint-" \_ jacksubtype"**</span><span class="sxs-lookup"><span data-stu-id="01e65-133">**PKEY\_AudioEndpoint\_JackSubType**</span></span>](pkey-audioendpoint-jacksubtype.md)<br/>                               | <span data-ttu-id="01e65-134">Enthält eine Ausgabe Kategorie-GUID für ein audioendpunktgerät.</span><span class="sxs-lookup"><span data-stu-id="01e65-134">Contains an output category GUID for an audio endpoint device.</span></span> <br/>                                                                                    |



 

## <a name="device-properties"></a><span data-ttu-id="01e65-135">Geräteeigenschaften</span><span class="sxs-lookup"><span data-stu-id="01e65-135">Device Properties</span></span>

<span data-ttu-id="01e65-136">Das Core-audiosdk umfasst verschiedene Geräteeigenschaften von [audioendpunktgeräten](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="01e65-136">Core Audio SDK includes several device properties of [audio endpoint devices](audio-endpoint-devices.md).</span></span> <span data-ttu-id="01e65-137">Weitere Informationen finden Sie unter [Geräteeigenschaften](device-properties.md).</span><span class="sxs-lookup"><span data-stu-id="01e65-137">For more information, see [Device Properties](device-properties.md).</span></span>

<span data-ttu-id="01e65-138">Die folgenden Eigenschaften sind in functiondiscoverykeys \_ devpkey. h in Windows Vista und höher definiert.</span><span class="sxs-lookup"><span data-stu-id="01e65-138">The following properties are defined in Functiondiscoverykeys\_devpkey.h in Windows Vista and later.</span></span>



| <span data-ttu-id="01e65-139">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="01e65-139">Property</span></span>                                                                         | <span data-ttu-id="01e65-140">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01e65-140">Description</span></span>                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01e65-141">**Pkey-Geräte \_ Name (tviceinterface \_ FriendlyName)**</span><span class="sxs-lookup"><span data-stu-id="01e65-141">**PKEY\_DeviceInterface\_FriendlyName**</span></span>](pkey-deviceinterface-friendlyname.md) | <span data-ttu-id="01e65-142">Der Anzeige Name des audioadapters, an den das Endpunkt Gerät angefügt wird (z. b. "XYZ-Audioadapter").</span><span class="sxs-lookup"><span data-stu-id="01e65-142">The friendly name of the audio adapter to which the endpoint device is attached (for example, "XYZ Audio Adapter").</span></span>                                                                               |
| [<span data-ttu-id="01e65-143">**Pkey- \_ Gerät \_ devicedebug**</span><span class="sxs-lookup"><span data-stu-id="01e65-143">**PKEY\_Device\_DeviceDesc**</span></span>](pkey-device-devicedesc.md)                       | <span data-ttu-id="01e65-144">Die Geräte Beschreibung des Endpunkt Geräts (z. b. "Sprecher").</span><span class="sxs-lookup"><span data-stu-id="01e65-144">The device description of the endpoint device (for example, "Speakers").</span></span>                                                                                                                          |
| [<span data-ttu-id="01e65-145">**Pkey- \_ Gerät \_ FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="01e65-145">**PKEY\_Device\_FriendlyName**</span></span>](pkey-device-friendlyname.md)                   | <span data-ttu-id="01e65-146">Der Anzeige Name des Endpunkt Geräts (z. b. "Sprecher (XYZ-Audioadapter)").</span><span class="sxs-lookup"><span data-stu-id="01e65-146">The friendly name of the endpoint device (for example, "Speakers (XYZ Audio Adapter)").</span></span>                                                                                                           |
| <span data-ttu-id="01e65-147">**Pkey \_ \_ -Geräte-containerid**</span><span class="sxs-lookup"><span data-stu-id="01e65-147">**PKEY\_Device\_ContainerId**</span></span>                                                    | <span data-ttu-id="01e65-148">Speichert den Container Bezeichner des PNP-Geräts, das den audioendpunkt implementiert.</span><span class="sxs-lookup"><span data-stu-id="01e65-148">Stores the container identifier of the PnP device that implements the audio endpoint.</span></span> <span data-ttu-id="01e65-149">Weitere Informationen zu dieser Eigenschaft finden Sie unter "Referenz zu Geräteeigenschaften" in der Windows WDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="01e65-149">For more information about this property, see "Device Property Reference" in the Windows WDK documentation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="01e65-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="01e65-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01e65-151">Programmierverzeichnis</span><span class="sxs-lookup"><span data-stu-id="01e65-151">Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




