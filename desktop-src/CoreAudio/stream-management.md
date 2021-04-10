---
description: Datenstrom Verwaltung
ms.assetid: 936d8d69-e86c-418b-b5b0-c4fbbfa1dd49
title: Datenstrom Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07180d8b46f4d079c08f4b619cf4a7773a6104d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127049"
---
# <a name="stream-management"></a><span data-ttu-id="16e5d-103">Datenstrom Verwaltung</span><span class="sxs-lookup"><span data-stu-id="16e5d-103">Stream Management</span></span>

<span data-ttu-id="16e5d-104">Nachdem Sie die [audioendpunktgeräte](audio-endpoint-devices.md) im System aufgelistet und ein geeignetes Rendering-oder Erfassungsgerät identifiziert haben, besteht die nächste Aufgabe für eine audioclientanwendung darin, eine Verbindung mit dem Endpunkt Gerät zu öffnen und den Fluss der Audiodaten über diese Verbindung zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="16e5d-104">After enumerating the [audio endpoint devices](audio-endpoint-devices.md) in the system and identifying a suitable rendering or capture device, the next task for an audio client application is to open a connection with the endpoint device and to manage the flow of audio data over that connection.</span></span> <span data-ttu-id="16e5d-105">[WASAPI](wasapi.md) ermöglicht Clients das Erstellen und Verwalten von Audiodatenströmen.</span><span class="sxs-lookup"><span data-stu-id="16e5d-105">[WASAPI](wasapi.md) enables clients to create and manage audio streams.</span></span>

<span data-ttu-id="16e5d-106">WASAPI implementiert mehrere Schnittstellen, um streamverwaltungsdienste für audioclients bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="16e5d-106">WASAPI implements several interfaces to provide stream-management services to audio clients.</span></span> <span data-ttu-id="16e5d-107">Die primäre Schnittstelle ist [**iaudioclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient).</span><span class="sxs-lookup"><span data-stu-id="16e5d-107">The primary interface is [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient).</span></span> <span data-ttu-id="16e5d-108">Ein Client ruft die **iaudioclient** -Schnittstelle für ein audioendpunktgerät ab, indem er die [**immdevice:: Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) -Methode (mit dem Parameter *IID* ist auf **refi** IID \_ iaudioclient festgelegt) für das Endpunkt Objekt aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="16e5d-108">A client obtains the **IAudioClient** interface for an audio endpoint device by calling the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method (with parameter *iid* set to **REFIID** IID\_IAudioClient) on the endpoint object.</span></span>

<span data-ttu-id="16e5d-109">Der Client ruft die Methoden in der [**iaudioclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) -Schnittstelle auf, um Folgendes durchzuführen:</span><span class="sxs-lookup"><span data-stu-id="16e5d-109">The client calls the methods in the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface to do the following:</span></span>

-   <span data-ttu-id="16e5d-110">Ermitteln Sie, welche Audioformate das Endpunkt Gerät unterstützt.</span><span class="sxs-lookup"><span data-stu-id="16e5d-110">Discover which audio formats the endpoint device supports.</span></span>
-   <span data-ttu-id="16e5d-111">Gibt die Größe des Endpunkt Puffers an.</span><span class="sxs-lookup"><span data-stu-id="16e5d-111">Get the endpoint buffer size.</span></span>
-   <span data-ttu-id="16e5d-112">Das Streamformat und die Latenzzeit erhalten.</span><span class="sxs-lookup"><span data-stu-id="16e5d-112">Get the stream format and latency.</span></span>
-   <span data-ttu-id="16e5d-113">Starten, Abbrechen und Zurücksetzen des Streams, der über das Endpunkt Gerät fließt.</span><span class="sxs-lookup"><span data-stu-id="16e5d-113">Start, stop, and reset the stream that flows through the endpoint device.</span></span>
-   <span data-ttu-id="16e5d-114">Greifen Sie auf zusätzliche Audiodienste zu.</span><span class="sxs-lookup"><span data-stu-id="16e5d-114">Access additional audio services.</span></span>

<span data-ttu-id="16e5d-115">Zum Erstellen eines Streams Ruft ein Client die [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="16e5d-115">To create a stream, a client calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span> <span data-ttu-id="16e5d-116">Durch diese Methode gibt der Client das Datenformat für den Stream, die Größe des Endpunkt Puffers und ob der Stream im freigegebenen oder exklusiven Modus betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="16e5d-116">Through this method, the client specifies the data format for the stream, the size of the endpoint buffer, and whether the stream operates in shared or exclusive mode.</span></span>

<span data-ttu-id="16e5d-117">Die verbleibenden Methoden in der [**iaudioclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) -Schnittstelle fallen in zwei Gruppen:</span><span class="sxs-lookup"><span data-stu-id="16e5d-117">The remaining methods in the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface fall into two groups:</span></span>

-   <span data-ttu-id="16e5d-118">Methoden, die nur aufgerufen werden können, nachdem der Stream von [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="16e5d-118">Methods that can be called only after the stream has been opened by [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span>
-   <span data-ttu-id="16e5d-119">Methoden, die zu einem beliebigen Zeitpunkt vor oder nach dem [**Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Aufruf aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="16e5d-119">Methods that can be called at any time before or after the [**Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) call.</span></span>

<span data-ttu-id="16e5d-120">Die folgenden Methoden können nur nach dem Aufruf von [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="16e5d-120">The following methods can be called only after the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize):</span></span>

-   [<span data-ttu-id="16e5d-121">**Iaudioclient:: getBufferSize**</span><span class="sxs-lookup"><span data-stu-id="16e5d-121">**IAudioClient::GetBufferSize**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize)
-   [<span data-ttu-id="16e5d-122">**Iaudioclient:: getcurrentpadding**</span><span class="sxs-lookup"><span data-stu-id="16e5d-122">**IAudioClient::GetCurrentPadding**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding)
-   [<span data-ttu-id="16e5d-123">**Iaudioclient:: GetService**</span><span class="sxs-lookup"><span data-stu-id="16e5d-123">**IAudioClient::GetService**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
-   [<span data-ttu-id="16e5d-124">**Iaudioclient:: getstreamlatency**</span><span class="sxs-lookup"><span data-stu-id="16e5d-124">**IAudioClient::GetStreamLatency**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getstreamlatency)
-   [<span data-ttu-id="16e5d-125">**Iaudioclient:: Reset**</span><span class="sxs-lookup"><span data-stu-id="16e5d-125">**IAudioClient::Reset**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-reset)
-   [<span data-ttu-id="16e5d-126">**Iaudioclient:: Start**</span><span class="sxs-lookup"><span data-stu-id="16e5d-126">**IAudioClient::Start**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start)
-   [<span data-ttu-id="16e5d-127">**Iaudioclient:: Beendigung**</span><span class="sxs-lookup"><span data-stu-id="16e5d-127">**IAudioClient::Stop**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop)

<span data-ttu-id="16e5d-128">Die folgenden Methoden können vor oder nach dem [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Aufruf aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="16e5d-128">The following methods can be called before or after the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) call:</span></span>

-   [<span data-ttu-id="16e5d-129">**Iaudioclient:: getdeviceperiod**</span><span class="sxs-lookup"><span data-stu-id="16e5d-129">**IAudioClient::GetDevicePeriod**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod)
-   [<span data-ttu-id="16e5d-130">**Iaudioclient:: getmixformat**</span><span class="sxs-lookup"><span data-stu-id="16e5d-130">**IAudioClient::GetMixFormat**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getmixformat)
-   [<span data-ttu-id="16e5d-131">**Iaudioclient:: isformatsupported**</span><span class="sxs-lookup"><span data-stu-id="16e5d-131">**IAudioClient::IsFormatSupported**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported)

<span data-ttu-id="16e5d-132">Um auf die zusätzlichen audioclientdienste zuzugreifen, ruft der Client die [**iaudioclient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="16e5d-132">To access the additional audio client services, the client calls the [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) method.</span></span> <span data-ttu-id="16e5d-133">Mit dieser Methode kann der Client Verweise auf die folgenden Schnittstellen abrufen:</span><span class="sxs-lookup"><span data-stu-id="16e5d-133">Through this method, the client can obtain references to the following interfaces:</span></span>

-   [<span data-ttu-id="16e5d-134">**Iaudiorenderclient**</span><span class="sxs-lookup"><span data-stu-id="16e5d-134">**IAudioRenderClient**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)

    <span data-ttu-id="16e5d-135">Schreibt Renderingdaten in einen Endpunkt Puffer für audiorendering.</span><span class="sxs-lookup"><span data-stu-id="16e5d-135">Writes rendering data to an audio-rendering endpoint buffer.</span></span>

-   [<span data-ttu-id="16e5d-136">**Iaudiocaptureclient**</span><span class="sxs-lookup"><span data-stu-id="16e5d-136">**IAudioCaptureClient**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)

    <span data-ttu-id="16e5d-137">Liest erfasste Daten aus einem Endpunkt Puffer der Audioerfassung.</span><span class="sxs-lookup"><span data-stu-id="16e5d-137">Reads captured data from an audio-capture endpoint buffer.</span></span>

-   [<span data-ttu-id="16e5d-138">**Iaudiosessioncontrol**</span><span class="sxs-lookup"><span data-stu-id="16e5d-138">**IAudioSessionControl**</span></span>](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)

    <span data-ttu-id="16e5d-139">Kommuniziert mit dem audiositzungsmanager, um die dem Stream zugeordnete Audiositzung zu konfigurieren und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="16e5d-139">Communicates with the audio session manager to configure and manage the audio session that is associated with the stream.</span></span>

-   [<span data-ttu-id="16e5d-140">**Isimpleaudiovolume**</span><span class="sxs-lookup"><span data-stu-id="16e5d-140">**ISimpleAudioVolume**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)

    <span data-ttu-id="16e5d-141">Steuert die Volumeebene der Audiositzung, die dem Stream zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="16e5d-141">Controls the volume level of the audio session that is associated with the stream.</span></span>

-   [<span data-ttu-id="16e5d-142">**Ichannelaudiovolume**</span><span class="sxs-lookup"><span data-stu-id="16e5d-142">**IChannelAudioVolume**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)

    <span data-ttu-id="16e5d-143">Steuert die volumeebenen der einzelnen Kanäle in der Audiositzung, die dem Stream zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="16e5d-143">Controls the volume levels of the individual channels in the audio session that is associated with the stream.</span></span>

-   [<span data-ttu-id="16e5d-144">**Iaudioclock**</span><span class="sxs-lookup"><span data-stu-id="16e5d-144">**IAudioClock**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)

    <span data-ttu-id="16e5d-145">Überwacht die streamdatenrate und die Streamposition.</span><span class="sxs-lookup"><span data-stu-id="16e5d-145">Monitors the stream data rate and stream position.</span></span>

<span data-ttu-id="16e5d-146">Außerdem sollten WASAPI-Clients, für die Benachrichtigungen über Sitzungs bezogene Ereignisse erforderlich sind, die folgende Schnittstelle implementieren:</span><span class="sxs-lookup"><span data-stu-id="16e5d-146">In addition, WASAPI clients that require notification of session-related events should implement the following interface:</span></span>

-   [<span data-ttu-id="16e5d-147">**Iaudiosessionevents**</span><span class="sxs-lookup"><span data-stu-id="16e5d-147">**IAudioSessionEvents**</span></span>](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)

    <span data-ttu-id="16e5d-148">Um Ereignis Benachrichtigungen zu empfangen, übergibt der Client einen Zeiger an seine [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstelle an die [**iaudiosessioncontrol:: registeraudiosessionnotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) -Methode als callparameter.</span><span class="sxs-lookup"><span data-stu-id="16e5d-148">To receive event notifications, the client passes a pointer to its [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface to the [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) method as a call parameter.</span></span>

<span data-ttu-id="16e5d-149">Zum Schluss verwendet ein Client möglicherweise eine API auf höherer Ebene, um einen Audiostream zu erstellen, erfordert aber auch Zugriff auf die Sitzungs Steuerelemente und volumesteuerelemente für die Sitzung, die den Stream enthält.</span><span class="sxs-lookup"><span data-stu-id="16e5d-149">Finally, a client might use a higher-level API to create an audio stream, but also require access to the session controls and volume controls for the session that contains the stream.</span></span> <span data-ttu-id="16e5d-150">Eine API höherer Ebene bietet diesen Zugriff in der Regel nicht.</span><span class="sxs-lookup"><span data-stu-id="16e5d-150">A higher-level API typically does not provide this access.</span></span> <span data-ttu-id="16e5d-151">Der Client kann die Steuerelemente für eine bestimmte Sitzung über die [**iaudiosessionmanager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) -Schnittstelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="16e5d-151">The client can obtain the controls for a particular session through the [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) interface.</span></span> <span data-ttu-id="16e5d-152">Diese Schnittstelle ermöglicht es dem Client, die [**iaudiosessioncontrol**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) -Schnittstelle und die [**isimpleaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) -Schnittstelle für eine Sitzung abzurufen, ohne dass der Client die [**iaudioclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) -Schnittstelle zum Erstellen eines Streams und zum Zuweisen des Streams zur Sitzung benötigt.</span><span class="sxs-lookup"><span data-stu-id="16e5d-152">This interface enables the client to obtain the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) and [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) interfaces for a session without requiring the client to use the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface to create a stream and to assign the stream to the session.</span></span> <span data-ttu-id="16e5d-153">Ein Client ruft die **iaudiosessionmanager** -Schnittstelle für ein audioendpunktobjekt ab, indem er die [**immdevice:: Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) -Methode (mit dem Parameter *IID* ist auf **refID** IID \_ iaudiosessionmanager festgelegt) für das Endpunkt Objekt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="16e5d-153">A client obtains the **IAudioSessionManager** interface for an audio endpoint device by calling the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method (with parameter *iid* set to **REFIID** IID\_IAudioSessionManager) on the endpoint object.</span></span>

<span data-ttu-id="16e5d-154">Die Schnittstellen [**iaudiosessioncontrol**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol), [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)und [**iaudiosessionmanager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) werden in der Header Datei audiopolicy. h definiert.</span><span class="sxs-lookup"><span data-stu-id="16e5d-154">The [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol), [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents), and [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) interfaces are defined in header file Audiopolicy.h.</span></span> <span data-ttu-id="16e5d-155">Alle anderen WASAPI-Schnittstellen sind in der Header Datei "AudioClient. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="16e5d-155">All other WASAPI interfaces are defined in header file Audioclient.h.</span></span>

<span data-ttu-id="16e5d-156">In den folgenden Abschnitten wird beschrieben, wie Sie die WASAPI verwenden, um Audiostreams zu verwalten:</span><span class="sxs-lookup"><span data-stu-id="16e5d-156">The following sections describe how to use WASAPI to manage audio streams:</span></span>

-   [<span data-ttu-id="16e5d-157">Informationen zu WASAPI</span><span class="sxs-lookup"><span data-stu-id="16e5d-157">About WASAPI</span></span>](wasapi.md)
-   [<span data-ttu-id="16e5d-158">Rendern eines Streams</span><span class="sxs-lookup"><span data-stu-id="16e5d-158">Rendering a Stream</span></span>](rendering-a-stream.md)
-   [<span data-ttu-id="16e5d-159">Erfassen eines Streams</span><span class="sxs-lookup"><span data-stu-id="16e5d-159">Capturing a Stream</span></span>](capturing-a-stream.md)
-   [<span data-ttu-id="16e5d-160">Loopback Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="16e5d-160">Loopback Recording</span></span>](loopback-recording.md)
-   [<span data-ttu-id="16e5d-161">Datenströme im exklusiven Modus</span><span class="sxs-lookup"><span data-stu-id="16e5d-161">Exclusive-Mode Streams</span></span>](exclusive-mode-streams.md)
-   [<span data-ttu-id="16e5d-162">Wiederherstellen nach einem Invalid-Device Fehler</span><span class="sxs-lookup"><span data-stu-id="16e5d-162">Recovering from an Invalid-Device Error</span></span>](recovering-from-an-invalid-device-error.md)
-   [<span data-ttu-id="16e5d-163">Verwenden eines kommunikationsgeräts</span><span class="sxs-lookup"><span data-stu-id="16e5d-163">Using a Communication Device</span></span>](using-the-communication-device.md)
-   [<span data-ttu-id="16e5d-164">Streamrouting</span><span class="sxs-lookup"><span data-stu-id="16e5d-164">Stream Routing</span></span>](stream-routing.md)

## <a name="related-topics"></a><span data-ttu-id="16e5d-165">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="16e5d-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16e5d-166">Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="16e5d-166">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 



