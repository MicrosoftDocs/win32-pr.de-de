---
description: Stream-Routing ist die Fähigkeit einer Medien Anwendung, Streams zwischen Geräten mit minimaler Unterbrechung der Wiedergabe oder der Erfassungs Sitzung zu wechseln.
ms.assetid: fc6efe89-013c-47af-870e-8705fa60c99c
title: Streamrouting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b21cd15a4467cb9b08747119aab999882ae3b5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483462"
---
# <a name="stream-routing"></a><span data-ttu-id="26440-103">Streamrouting</span><span class="sxs-lookup"><span data-stu-id="26440-103">Stream Routing</span></span>

<span data-ttu-id="26440-104">*Stream-Routing* ist die Fähigkeit einer Medien Anwendung, Streams zwischen Geräten mit minimaler Unterbrechung der Wiedergabe oder der Erfassungs Sitzung zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="26440-104">*Stream routing* is the ability of a media application to switch streams between devices with minimal interruption to the playback or the capture session.</span></span>

<span data-ttu-id="26440-105">Ein Computer kann über mehrere renderinggeräte und Erfassungsgeräte verfügen.</span><span class="sxs-lookup"><span data-stu-id="26440-105">A computer can have multiple rendering and capture devices.</span></span> <span data-ttu-id="26440-106">Das System listet diese Geräte in der Systemsteuerung **Sounds** auf.</span><span class="sxs-lookup"><span data-stu-id="26440-106">The system lists these devices on the **Sounds** control panel.</span></span> <span data-ttu-id="26440-107">In dieser Liste kann ein Benutzer ein Gerät als Standardgerät für jede Rolle festlegen: Wiedergabe, Aufzeichnung oder die vier Kommunikations Rollen (Konsolen Rendering, Konsolen Erfassung, Kommunikations-Rendering oder Kommunikations Erfassung).</span><span class="sxs-lookup"><span data-stu-id="26440-107">From this list, a user can set a device to be the default device for each role: playback, recording, or the four communications roles (console render, console capture, communication render, or communication capture).</span></span> <span data-ttu-id="26440-108">Die Liste der Geräte kann dynamisch geändert werden, da einige dieser Geräte vorübergehend verfügbar sein können, z. b. ein USB-Headset.</span><span class="sxs-lookup"><span data-stu-id="26440-108">The list of devices may be modified dynamically as some of these devices can be available temporarily, for example a USB headset.</span></span> <span data-ttu-id="26440-109">Wenn mehrere Geräte verfügbar sind, kann der Benutzer die Standardeinstellung auf ein anderes Gerät ändern.</span><span class="sxs-lookup"><span data-stu-id="26440-109">When multiple devices are available, the user can change the default to a different device.</span></span> <span data-ttu-id="26440-110">Der Benutzer kann auch das Format eines Geräts (Samplingrate, Bits pro Stichprobe usw.) auf der Registerkarte **erweitert** für die Geräteeigenschaften ändern.</span><span class="sxs-lookup"><span data-stu-id="26440-110">The user can also change the format of a device (sample rate, bits per sample, and so on) on the **Advanced** tab for the device properties.</span></span>

<span data-ttu-id="26440-111">Stellen Sie sich ein Szenario vor, in dem ein Benutzer **Referenten** als Standardgerät zum Rendern von Audiostreams auswählt.</span><span class="sxs-lookup"><span data-stu-id="26440-111">Consider a scenario in which a user selects **Speakers** as the default device for rendering audio streams.</span></span> <span data-ttu-id="26440-112">Der Benutzer stellt dann eine Verbindung mit einem USB-Headset her, wählt das Headset als neues Standardgerät aus und ändert die Samplingrate des Geräts von 44,1 kHz in 48 kHz.</span><span class="sxs-lookup"><span data-stu-id="26440-112">The user then connects a USB headset, selects the headset as the new default device, and changes the sample rate of the device from 44.1 kHz to 48 kHz.</span></span> <span data-ttu-id="26440-113">Der Benutzer möchte den Audiostream in der neuen Stichprobenrate mit minimaler Unterbrechung der Streamingsitzung auf dem Headset wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="26440-113">The user wants to play the audio stream on the headset at the new sample rate with minimal interruption to the streaming session.</span></span>

<span data-ttu-id="26440-114">In diesem Szenario gibt es zwei Fälle, die die Medien Anwendung behandeln muss:</span><span class="sxs-lookup"><span data-stu-id="26440-114">In this scenario, there are two cases that the media application must handle:</span></span>

-   <span data-ttu-id="26440-115">Der Stream muss mit minimaler Unterbrechung der Wiedergabe auf das neue Standardgerät übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="26440-115">The stream must be transferred to the new default device with minimal interruption to playback.</span></span>
-   <span data-ttu-id="26440-116">Das neue Gerät muss die Wiedergabe im neuen Format fortsetzen (d. h., der Benutzer kann die Stichprobenrate ändern).</span><span class="sxs-lookup"><span data-stu-id="26440-116">The new device must resume playback in the new format (that is, the user can change more than the sample rate).</span></span>

<span data-ttu-id="26440-117">Um dieses Szenario in Windows Vista zu unterstützen, musste die Medien Anwendung die Implementierung für das Datenstrom Routing bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="26440-117">In Windows Vista, to support this scenario, the media application had to provide the implementation for stream routing.</span></span> <span data-ttu-id="26440-118">Die Anwendung war dafür verantwortlich, vorhandene Streams zu beenden und die Streams auf dem neuen Gerät neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="26440-118">The application was responsible for terminating existing streams and restarting the streams on the new device.</span></span> <span data-ttu-id="26440-119">Wenn der Benutzer das Standardgerät geändert hat oder das zugehörige Mischungs Format geändert wurde, wurden alle zugeordneten Sitzungen geschlossen, und die Anwendung musste die Wiederherstellung durchführen.</span><span class="sxs-lookup"><span data-stu-id="26440-119">If the user changed the default device or its mix format changed, then all of the associated sessions were closed and the application had to handle the recovery.</span></span>

<span data-ttu-id="26440-120">In Windows 7 kann eine Anwendung einen Stream nahtlos von einem vorhandenen Standardgerät an einen neuen standardaudioendpunkt übertragen.</span><span class="sxs-lookup"><span data-stu-id="26440-120">In Windows 7, an application can seamlessly transfer a stream from an existing default device to a new default audio endpoint.</span></span> <span data-ttu-id="26440-121">Allgemeine Audio-API-Sätze, wie Media Foundation-, DirectSound-und Wave-APIs, implementieren das Stream-Routing Feature.</span><span class="sxs-lookup"><span data-stu-id="26440-121">High-level audio API sets such as Media Foundation, DirectSound, and WAVE APIs implement the stream routing feature.</span></span> <span data-ttu-id="26440-122">Medienanwendungen, die diese API-Sätze zum Wiedergeben oder Erfassen eines Streams vom Standardgerät verwenden, verwenden die Standard Implementierung und müssen die Anwendung nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="26440-122">Media applications that use these API sets to play or capture a stream from the default device use the default implementation and will not have to modify the application.</span></span> <span data-ttu-id="26440-123">Wenn Ihre Medien Anwendung jedoch mmdeviceapi oder WASAPI direkt verwendet, muss die Anwendung die streamweiterleitungs-Implementierung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="26440-123">However, if your media application uses MMDeviceAPI or WASAPI directly, the application needs to provide the stream routing implementation.</span></span>

> [!Note]  
> <span data-ttu-id="26440-124">Mmdeviceapi und WASAPI sind Kerncode-API-Komponenten, die eine Anwendung verwenden kann, um einen Stream auf einem Gerät zu erzeugen oder zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="26440-124">MMDeviceAPI and WASAPI are Core Audio API components that an application can use to render or capture a stream on a device.</span></span> <span data-ttu-id="26440-125">Die mmdeviceapi ermittelt das neue audioendpunktgerät, und WASAPI verwaltet den Fluss der Audiodaten zwischen einer Medien Anwendung und dem audioendpunktgerät.</span><span class="sxs-lookup"><span data-stu-id="26440-125">The MMDeviceAPI discovers the new audio endpoint device, and WASAPI manages the flow of audio data between a media application and the audio endpoint device.</span></span>

 

<span data-ttu-id="26440-126">Zum Implementieren der streamweiterleitungs Funktion muss die Anwendung die von mmdeviceapi und WASAPI gesendeten Benachrichtigungen überwachen, wenn Folgendes der Fall ist:</span><span class="sxs-lookup"><span data-stu-id="26440-126">To implement the stream routing feature, the application must listen for the notifications sent by MMDeviceAPI and WASAPI when:</span></span>

-   <span data-ttu-id="26440-127">Das Standardgerät wird vom Benutzer geändert.</span><span class="sxs-lookup"><span data-stu-id="26440-127">The default device is changed by the user.</span></span>
-   <span data-ttu-id="26440-128">Das vorhandene Standardgerät wird entfernt und ein neues Standardgerät hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="26440-128">The existing default device is removed and a new default device is added.</span></span>
-   <span data-ttu-id="26440-129">Das Geräte Format wird geändert.</span><span class="sxs-lookup"><span data-stu-id="26440-129">The device format is changed.</span></span>

<span data-ttu-id="26440-130">Durch die Behandlung dieser Benachrichtigungen kann eine Anwendung die erforderlichen Stream-Verwaltungsvorgänge ausführen, während der Datenstrom auf das neue Standardgerät übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="26440-130">By handling these notifications, an application can perform the necessary stream management operations while transferring the stream to the new default device.</span></span> <span data-ttu-id="26440-131">Außerdem kann die Anwendung vorhandene Streams mithilfe des neuen Formats rendern oder erfassen, das vom Benutzer angegeben wird, während eine renderingsitzung aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="26440-131">In addition, the application can render or capture existing streams by using the new format specified by the user while a rendering session is active.</span></span>

<span data-ttu-id="26440-132">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="26440-132">This section contains the following topics:</span></span>

-   [<span data-ttu-id="26440-133">Der Geräte Endpunkt für das streamrouting wird erhalten.</span><span class="sxs-lookup"><span data-stu-id="26440-133">Getting the Device Endpoint for Stream Routing</span></span>](getting-the-default-device-endpoint-for-stream-routing.md)
-   [<span data-ttu-id="26440-134">Relevante Benachrichtigungen für das Datenstrom Routing</span><span class="sxs-lookup"><span data-stu-id="26440-134">Relevant Notifications for Stream Routing</span></span>](relevant-device-notifications-for-stream-routing.md)
-   [<span data-ttu-id="26440-135">Überlegungen zur Implementierung von streamrouting</span><span class="sxs-lookup"><span data-stu-id="26440-135">Stream Routing Implementation Considerations</span></span>](stream-routing-implementation-considerations.md)

<span data-ttu-id="26440-136">Die folgenden Beispiele, die im Windows SDK enthalten sind, veranschaulichen, wie eine Anwendung Stream-Routing Benachrichtigungen verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="26440-136">The following samples, included in the Windows SDK, demonstrate how an application can handle stream routing notifications.</span></span>

-   [<span data-ttu-id="26440-137">Rendersharedtimer-gesteuert</span><span class="sxs-lookup"><span data-stu-id="26440-137">RenderSharedTimerDriven</span></span>](rendersharedtimerdriven.md)
-   [<span data-ttu-id="26440-138">Rendersharedebug-gesteuert</span><span class="sxs-lookup"><span data-stu-id="26440-138">RenderSharedEventDriven</span></span>](rendersharedeventdriven.md)
-   [<span data-ttu-id="26440-139">Renderexclusivetimer-gesteuert</span><span class="sxs-lookup"><span data-stu-id="26440-139">RenderExclusiveTimerDriven</span></span>](renderexclusivetimerdriven.md)
-   [<span data-ttu-id="26440-140">Renderexclusiveeventdriver</span><span class="sxs-lookup"><span data-stu-id="26440-140">RenderExclusiveEventDriven</span></span>](renderexclusiveeventdriven.md)
-   [<span data-ttu-id="26440-141">Capturesharedtimer-gesteuert</span><span class="sxs-lookup"><span data-stu-id="26440-141">CaptureSharedTimerDriven</span></span>](capturesharedtimerdriven.md)
-   [<span data-ttu-id="26440-142">Capturesharedebug</span><span class="sxs-lookup"><span data-stu-id="26440-142">CaptureSharedEventDriven</span></span>](capturesharedeventdriven.md)

## <a name="related-topics"></a><span data-ttu-id="26440-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="26440-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26440-144">Datenstrom Verwaltung</span><span class="sxs-lookup"><span data-stu-id="26440-144">Stream Management</span></span>](stream-management.md)
</dt> <dt>

[<span data-ttu-id="26440-145">Informationen über die mmdevice-API</span><span class="sxs-lookup"><span data-stu-id="26440-145">About MMDevice API</span></span>](mmdevice-api.md)
</dt> <dt>

[<span data-ttu-id="26440-146">Informationen zu WASAPI</span><span class="sxs-lookup"><span data-stu-id="26440-146">About WASAPI</span></span>](wasapi.md)
</dt> </dl>

 

 



