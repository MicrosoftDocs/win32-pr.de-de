---
description: Endpointvolume-API
ms.assetid: 1fe1cd57-a0a4-4e08-ab52-3b6e66d14e79
title: Endpointvolume-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b827045250336aa499e386a8dafedb6ae068b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748552"
---
# <a name="endpointvolume-api"></a><span data-ttu-id="b576b-103">Endpointvolume-API</span><span class="sxs-lookup"><span data-stu-id="b576b-103">EndpointVolume API</span></span>

<span data-ttu-id="b576b-104">Die endpointvolume-API ermöglicht spezialisierten Clients das Steuern und Überwachen der volumeebenen von [audioendpunktgeräten](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="b576b-104">The EndpointVolume API enables specialized clients to control and monitor the volume levels of [audio endpoint devices](audio-endpoint-devices.md).</span></span> <span data-ttu-id="b576b-105">Ein Client erhält Verweise auf die Schnittstellen in der endpointvolume-API, indem er die [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstelle eines audioendpunktgeräts erhält und die [**immdevice:: Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="b576b-105">A client obtains references to the interfaces in the EndpointVolume API by obtaining the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of an audio endpoint device and calling the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method.</span></span>

<span data-ttu-id="b576b-106">Die Header Datei "endpointvolume. h" definiert die Schnittstellen in der endpointvolume-API.</span><span class="sxs-lookup"><span data-stu-id="b576b-106">Header file Endpointvolume.h defines the interfaces in the EndpointVolume API.</span></span>

<span data-ttu-id="b576b-107">Audioanwendungen, die die [mmdevice-API](mmdevice-api.md) und die [WASAPI](wasapi.md) verwenden, verwenden in der Regel die [**isimpleaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) -Schnittstelle, um die volumeebenen pro Sitzung zu steuern.</span><span class="sxs-lookup"><span data-stu-id="b576b-107">Audio applications that use the [MMDevice API](mmdevice-api.md) and [WASAPI](wasapi.md) typically use the [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) interface to control volume levels on a per-session basis.</span></span> <span data-ttu-id="b576b-108">Nur zwei Arten von Audioanwendungen müssen die endpointvolume-API verwenden.</span><span class="sxs-lookup"><span data-stu-id="b576b-108">Only two types of audio applications require the use of the EndpointVolume API.</span></span> <span data-ttu-id="b576b-109">Diese Anwendungs Typen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b576b-109">These application types are:</span></span>

-   <span data-ttu-id="b576b-110">Anwendungen, die die Master Volume-Ebenen von audioendpunktgeräten verwalten, ähnlich dem Windows-Volumen Steuerungsprogramm, Sndvol.exe.</span><span class="sxs-lookup"><span data-stu-id="b576b-110">Applications that manage the master volume levels of audio endpoint devices, similar to the Windows volume-control program, Sndvol.exe.</span></span>
-   <span data-ttu-id="b576b-111">Professionelle Audioanwendungen ("pro-Audioanwendungen"), die exklusiven Modus-Zugriff auf audioendpunktgeräte benötigen.</span><span class="sxs-lookup"><span data-stu-id="b576b-111">Professional audio ("pro audio") applications that require exclusive-mode access to audio endpoint devices.</span></span>

<span data-ttu-id="b576b-112">Die ungeeignete Verwendung der endpointvolume-API kann die Windows-audiorichtlinie beeinträchtigen und die systemvolumeeinstellungen des Benutzers stören.</span><span class="sxs-lookup"><span data-stu-id="b576b-112">Inappropriate use of the EndpointVolume API can interfere with Windows audio policy and disrupt the user's system volume settings.</span></span>

<span data-ttu-id="b576b-113">Wenn ein audioendpunktgerät Hardware Volume und stumm Steuerelemente implementiert, verwendet die endpointvolume-API diese Steuerelemente, um das Geräte Volume zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="b576b-113">If an audio endpoint device implements hardware volume and mute controls, the EndpointVolume API uses those controls to manage the device volume.</span></span> <span data-ttu-id="b576b-114">Andernfalls implementiert die endpointvolume-API die Steuerelemente in Software, transparent für den Client.</span><span class="sxs-lookup"><span data-stu-id="b576b-114">Otherwise, the EndpointVolume API implements the controls in software, transparently to the client.</span></span>

<span data-ttu-id="b576b-115">Wenn ein Gerät über Hardware Volume und stumm Steuerelemente verfügt, wirken sich Änderungen am Geräte Volume und stumm Einstellungen über die endpointvolume-API auf die Volumeebene im Modus "Shared" und im exklusiven Modus aus.</span><span class="sxs-lookup"><span data-stu-id="b576b-115">If a device has hardware volume and mute controls, changes made to the device's volume and mute settings through the EndpointVolume API affect the volume level in both shared mode and exclusive mode.</span></span> <span data-ttu-id="b576b-116">Wenn ein Gerät nicht über Hardware Volume und stumm Steuerelemente verfügt, wirken sich Änderungen am Software Volume und stumm Steuerelemente über die endpointvolume-API auf die Volumeebene im freigegebenen Modus, jedoch nicht im exklusiven Modus aus.</span><span class="sxs-lookup"><span data-stu-id="b576b-116">If a device lacks hardware volume and mute controls, changes made to the software volume and mute controls through the EndpointVolume API affect the volume level in shared mode, but not in exclusive mode.</span></span> <span data-ttu-id="b576b-117">Im exklusiven Modus tauschen der Client und das Gerät Audiodaten direkt aus, wobei die Software Steuerelemente umgangen werden.</span><span class="sxs-lookup"><span data-stu-id="b576b-117">In exclusive mode, the client and the device exchange audio data directly, bypassing the software controls.</span></span>

<span data-ttu-id="b576b-118">Für Anwendungen, die das Hardware Volume und das stumm schalten von Steuerelementen verwalten müssen, bietet die endpointvolume-API zwei mögliche Vorteile gegenüber der Debug- [API](devicetopology-api.md).</span><span class="sxs-lookup"><span data-stu-id="b576b-118">For applications that must manage hardware volume and mute controls, the EndpointVolume API offers two potential advantages over the [DeviceTopology API](devicetopology-api.md).</span></span>

<span data-ttu-id="b576b-119">Erstens fehlen für eine Reihe von audioadaptergeräten Hardware Volume-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="b576b-119">First, a number of audio adapter devices lack hardware volume controls.</span></span> <span data-ttu-id="b576b-120">Wenn ein Gerät nicht über ein Hardware Volume-Steuerelement verfügt, implementiert die [**iaudioendpointvolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) -Schnittstelle in der endpointvolume-API automatisch ein Software Volume-Steuerelement auf dem Stream zu oder von diesem Gerät.</span><span class="sxs-lookup"><span data-stu-id="b576b-120">If a device lacks a hardware volume control, the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface in the EndpointVolume API automatically implements a software volume control on the stream to or from that device.</span></span> <span data-ttu-id="b576b-121">Für einen Client der endpointvolume-API ist das Ergebnis identisch, unabhängig davon, ob die volumesteuerung vom Gerät oder in der Software von der endpointvolume-API-Schnittstelle in der Hardware implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="b576b-121">For a client of the EndpointVolume API, the result is the same whether the volume control is implemented in hardware by the device or in software by the EndpointVolume API interface.</span></span>

<span data-ttu-id="b576b-122">Zweitens: auch wenn das Adapter Gerät Hardware Volume-Steuerelemente implementiert, kann eine Anwendung, die die devicetopology-API zum Implementieren eines topologietraktalgorithmus verwendet, das gesuchte Steuerelement nicht finden.</span><span class="sxs-lookup"><span data-stu-id="b576b-122">Second, even if the adapter device does implement hardware volume controls, an application that uses the DeviceTopology API to implement a topology-traversal algorithm might fail to find the control that it is looking for.</span></span> <span data-ttu-id="b576b-123">In der Regel ist eine solche Anwendung so konzipiert, dass Sie die Hardware Topologie eines bestimmten Geräts oder einer Gruppe verwandter Geräte durchläuft.</span><span class="sxs-lookup"><span data-stu-id="b576b-123">Typically, such an application is designed to traverse the hardware topology of a particular device or set of related devices.</span></span> <span data-ttu-id="b576b-124">Die Anwendungs Risiken können nicht durchlaufen werden, wenn versucht wird, die Topologie eines Geräts zu durchlaufen, mit dem Sie nicht speziell entworfen oder getestet wurde.</span><span class="sxs-lookup"><span data-stu-id="b576b-124">The application risks failing if it attempts to traverse the topology of a device that it has not been specifically designed for or tested with.</span></span>

<span data-ttu-id="b576b-125">Nur spezialisierte Anwendungen, die auf andere Hardwarefunktionen als Volume-und stumm Steuerelemente zugreifen müssen, müssen die devicetopology-API verwenden.</span><span class="sxs-lookup"><span data-stu-id="b576b-125">Only specialized applications that must access hardware functions other than volume and mute controls require the use of the DeviceTopology API.</span></span> <span data-ttu-id="b576b-126">Bei Anwendungen, für die nur die Volumeebene eines Datenstroms im exklusiven Modus gesteuert werden muss, ist die endpointvolume-API einfacher zu verwenden und funktioniert zuverlässig mit einer breiteren Palette von audiohardwaregeräten.</span><span class="sxs-lookup"><span data-stu-id="b576b-126">For applications that require control only of the volume level of an exclusive-mode stream, the EndpointVolume API is simpler to use and works reliably with a wider range of audio hardware devices.</span></span>

<span data-ttu-id="b576b-127">Codebeispiele, die die Schnittstellen in der endpointvolume-API verwenden, finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="b576b-127">For code examples that use the interfaces in the EndpointVolume API, see the following topics:</span></span>

-   [<span data-ttu-id="b576b-128">Steuerelemente für Endpunkt-</span><span class="sxs-lookup"><span data-stu-id="b576b-128">Endpoint Volume Controls</span></span>](endpoint-volume-controls.md)
-   [<span data-ttu-id="b576b-129">Spitzen Zähler</span><span class="sxs-lookup"><span data-stu-id="b576b-129">Peak Meters</span></span>](peak-meters.md)

<span data-ttu-id="b576b-130">Ein Beispiel, das die endpointvolume-API verwendet, finden Sie unter [endpointvolume](endpointvolume.md) in der Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="b576b-130">To see a sample that uses the EndpointVolume API, see [EndpointVolume](endpointvolume.md) in the Windows SDK.</span></span>

<span data-ttu-id="b576b-131">Die endpointvolume-API implementiert die folgenden Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="b576b-131">The EndpointVolume API implements the following interfaces.</span></span>



| <span data-ttu-id="b576b-132">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b576b-132">Interface</span></span>                                                | <span data-ttu-id="b576b-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b576b-133">Description</span></span>                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="b576b-134">**Iaudioendpointvolume**</span><span class="sxs-lookup"><span data-stu-id="b576b-134">**IAudioEndpointVolume**</span></span>](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)     | <span data-ttu-id="b576b-135">Stellt die volumesteuerelemente im Audiostream zu oder von einem audioendpunktgerät dar.</span><span class="sxs-lookup"><span data-stu-id="b576b-135">Represents the volume controls on the audio stream to or from an audio endpoint device.</span></span> |
| [<span data-ttu-id="b576b-136">**Iaudiometerinformation**</span><span class="sxs-lookup"><span data-stu-id="b576b-136">**IAudioMeterInformation**</span></span>](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) | <span data-ttu-id="b576b-137">Stellt einen Spitzen Zähler für den Audiostream zu oder von einem audioendpunktgerät dar.</span><span class="sxs-lookup"><span data-stu-id="b576b-137">Represents a peak meter on the audio stream to or from an audio endpoint device.</span></span>        |



 

<span data-ttu-id="b576b-138">Außerdem sollten Clients der endpointvolume-API, die eine Benachrichtigung über das Volume und Änderungen an audioendpunktgeräten erfordern, die folgende Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="b576b-138">In addition, clients of the EndpointVolume API that require notification of volume and muting changes in audio endpoint devices should implement the following interface.</span></span>



| <span data-ttu-id="b576b-139">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b576b-139">Interface</span></span>                                                            | <span data-ttu-id="b576b-140">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b576b-140">Description</span></span>                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b576b-141">**Iaudioendpointvolumecallback**</span><span class="sxs-lookup"><span data-stu-id="b576b-141">**IAudioEndpointVolumeCallback**</span></span>](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | <span data-ttu-id="b576b-142">Stellt Benachrichtigungen bereit, wenn die Volumeebene oder der stumm Schaltung-Status eines audioendpunktgeräts geändert wird.</span><span class="sxs-lookup"><span data-stu-id="b576b-142">Provides notifications when the volume level or muting state of an audio endpoint device changes.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b576b-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b576b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b576b-144">Lautstärkeregler</span><span class="sxs-lookup"><span data-stu-id="b576b-144">Volume Controls</span></span>](volume-controls.md)
</dt> <dt>

[<span data-ttu-id="b576b-145">**Immdevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b576b-145">**IMMDevice Interface**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[<span data-ttu-id="b576b-146">**Immdevice:: Aktivieren**</span><span class="sxs-lookup"><span data-stu-id="b576b-146">**IMMDevice::Activate**</span></span>](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)
</dt> <dt>

[<span data-ttu-id="b576b-147">**Isimpleaudiovolume**</span><span class="sxs-lookup"><span data-stu-id="b576b-147">**ISimpleAudioVolume**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
</dt> <dt>

[<span data-ttu-id="b576b-148">**Programmierverzeichnis**</span><span class="sxs-lookup"><span data-stu-id="b576b-148">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



