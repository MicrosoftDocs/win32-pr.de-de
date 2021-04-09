---
description: Exclusive-Mode Streams
ms.assetid: 196cc6fe-91bf-46fa-acc9-38a7a4005875
title: Exclusive-Mode Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7722dd3463346e976f30a77949f56026a2425624
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958386"
---
# <a name="exclusive-mode-streams"></a><span data-ttu-id="0f2ad-103">Exclusive-Mode Streams</span><span class="sxs-lookup"><span data-stu-id="0f2ad-103">Exclusive-Mode Streams</span></span>

<span data-ttu-id="0f2ad-104">Wie bereits erläutert, hat die Anwendung, wenn eine Anwendung einen Stream im exklusiven Modus öffnet, die ausschließliche Verwendung des audioendpunktgeräts, das den Stream wieder gibt oder aufzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-104">As explained previously, if an application opens a stream in exclusive mode, the application has exclusive use of the audio endpoint device that plays or records the stream.</span></span> <span data-ttu-id="0f2ad-105">Im Gegensatz dazu können mehrere Anwendungen ein audioendpunktgerät gemeinsam nutzen, indem Datenströme im freigegebenen Modus auf dem Gerät geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-105">In contrast, several applications can share an audio endpoint device by opening shared-mode streams on the device.</span></span>

<span data-ttu-id="0f2ad-106">Der Zugriff auf ein Audiogerät im exklusiven Modus kann wichtige Systemsounds blockieren, die Interoperabilität mit anderen Anwendungen verhindern und die Benutzer Leistung anderweitig beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-106">Exclusive-mode access to an audio device can block crucial system sounds, prevent interoperability with other applications, and otherwise degrade the user experience.</span></span> <span data-ttu-id="0f2ad-107">Um diese Probleme zu beheben, gibt eine Anwendung mit einem Stream im exklusiven Modus normalerweise die Kontrolle über das Audiogerät aus, wenn die Anwendung nicht der Vordergrund Prozess ist oder kein aktives Streaming durchführt.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-107">To mitigate these problems, an application with an exclusive-mode stream typically relinquishes control of the audio device when the application is not the foreground process or is not actively streaming.</span></span>

<span data-ttu-id="0f2ad-108">Die Datenstrom Latenz ist die Verzögerung, die dem Dateipfad zugrunde liegt, der den Endpunkt Puffer einer Anwendung mit einem audioendpunktgerät verbindet.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-108">Stream latency is the delay that is inherent in the data path that connects an application's endpoint buffer with an audio endpoint device.</span></span> <span data-ttu-id="0f2ad-109">Bei einem renderingstream ist die Latenz die maximale Verzögerung ab dem Zeitpunkt, an dem eine Anwendung ein Beispiel in einen Endpunkt Puffer schreibt, bis zu dem Zeitpunkt, an dem das Beispiel durch die Referenten gehört.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-109">For a rendering stream, the latency is the maximum delay from the time that an application writes a sample to an endpoint buffer to the time that the sample is heard through the speakers.</span></span> <span data-ttu-id="0f2ad-110">Bei einem Aufzeichnungsdaten Strom ist die Latenz die maximale Verzögerung ab dem Zeitpunkt, an dem ein Sound das Mikrofon in den Zeitraum eingibt, in dem eine Anwendung das Beispiel für diesen Sound aus dem Endpunkt Puffer lesen kann.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-110">For a capture stream, the latency is the maximum delay from the time that a sound enters the microphone to the time that an application can read the sample for that sound from the endpoint buffer.</span></span>

<span data-ttu-id="0f2ad-111">Anwendungen, die streamingstreamstreams verwenden, werden häufig verwendet, da Sie niedrige Latenzzeiten in den Daten Pfaden zwischen den audioendpunktgeräten und den Anwendungsthreads erfordern, die auf die Endpunkt Puffer zugreifen.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-111">Applications that use exclusive-mode streams often do so because they require low latencies in the data paths between the audio endpoint devices and the application threads that access the endpoint buffers.</span></span> <span data-ttu-id="0f2ad-112">Diese Threads werden in der Regel mit einer relativ hohen Priorität ausgeführt und planen die Ausführung in regelmäßigen Abständen, die sich in der Nähe oder demselben Intervall befinden, in dem aufeinander folgende Verarbeitungs Durchgänge von der Audiohardware getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-112">Typically, these threads run at relatively high priority and schedule themselves to run at periodic intervals that are close to or the same as the periodic interval that separates successive processing passes by the audio hardware.</span></span> <span data-ttu-id="0f2ad-113">Bei jedem Durchlauf verarbeitet die Audiohardware die neuen Daten in den Endpunkt Puffern.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-113">During each pass, the audio hardware processes the new data in the endpoint buffers.</span></span>

<span data-ttu-id="0f2ad-114">Um die kleinsten streamlatenzen zu erzielen, benötigt eine Anwendung möglicherweise sowohl spezielle Audiohardware als auch ein Computersystem, das leicht ausgelastet ist.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-114">To achieve the smallest stream latencies, an application might require both special audio hardware, and a computer system that is lightly loaded.</span></span> <span data-ttu-id="0f2ad-115">Wenn Sie die Audiohardware über die Zeitlimits hinaus setzen oder das System mit konkurrierenden Aufgaben mit hoher Priorität laden, kann dies zu einem Fehler in einem Audiostream mit niedriger Latenz führen.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-115">Driving the audio hardware beyond its timing limits or loading the system with competing high-priority tasks might cause a glitch in a low-latency audio stream.</span></span> <span data-ttu-id="0f2ad-116">Beispielsweise kann bei einem renderingstream ein Fehler auftreten, wenn die Anwendung nicht in einen Endpunkt Puffer schreiben kann, bevor die Audiohardware den Puffer liest, oder wenn die Hardware den Puffer vor dem Zeitpunkt der Wiedergabe des Puffers nicht lesen kann.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-116">For example, for a rendering stream, a glitch can occur if the application fails to write to an endpoint buffer before the audio hardware reads the buffer, or if the hardware fails to read the buffer before the time that the buffer is scheduled to play.</span></span> <span data-ttu-id="0f2ad-117">In der Regel sollte eine Anwendung, die auf einer großen Bandbreite von Audiohardware und in einer Vielzahl von Systemen ausgeführt werden soll, die Zeit Steuerungsanforderungen so lockern, dass Sie in allen Ziel Umgebungen einen Fehler vermeiden.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-117">Typically, an application that is intended to run on a wide variety of audio hardware and in a broad range of systems should relax its timing requirements enough to avoid glitches in all target environments.</span></span>

<span data-ttu-id="0f2ad-118">Windows Vista verfügt über mehrere Features zur Unterstützung von Anwendungen, die Audiostreams mit niedriger Latenz benötigen.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-118">Windows Vista has several features to support applications that require low-latency audio streams.</span></span> <span data-ttu-id="0f2ad-119">Wie unter [benutzermodusaudiokomponenten](user-mode-audio-components.md)erläutert, können Anwendungen, die zeitkritische Vorgänge ausführen, die MMCSS-Funktionen (Multimedia Class Scheduler Service) zum Erhöhen der Thread Priorität aufruft, ohne dass CPU-Ressourcen Anwendungen mit niedrigerer Priorität verweigert werden.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-119">As discussed in [User-Mode Audio Components](user-mode-audio-components.md), applications that perform time-critical operations can call the Multimedia Class Scheduler Service (MMCSS) functions to increase thread priority without denying CPU resources to lower-priority applications.</span></span> <span data-ttu-id="0f2ad-120">Darüber hinaus unterstützt die [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Methode ein \_ \_ Ereignis Rückruf-Flag von audclnt StreamFlags, das es dem Puffer Wartungs Thread einer Anwendung ermöglicht, die Ausführung zu planen, wenn ein neuer Puffer vom Audiogerät verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-120">In addition, the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method supports an AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK flag that enables an application's buffer-servicing thread to schedule its execution to occur when a new buffer becomes available from the audio device.</span></span> <span data-ttu-id="0f2ad-121">Durch die Verwendung dieser Features kann ein Anwendungs Thread die Sicherheits Anfälligkeit verringern, wenn er ausgeführt wird. Dadurch wird das Risiko eines Fehlers bei einem Audiostream mit niedriger Latenz verringert.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-121">By using these features, an application thread can reduce uncertainty about when it will execute, thereby decreasing the risk of glitches in a low-latency audio stream.</span></span>

<span data-ttu-id="0f2ad-122">Die Treiber für ältere Audioadapter verwenden wahrscheinlich die Gerätetreiber Schnittstelle (DDI) wavecyclic oder wavepci, wohingegen die Treiber für neuere Audioadapter wahrscheinlich den WaveRT-DDI unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-122">The drivers for older audio adapters are likely to use the WaveCyclic or WavePci device driver interface (DDI), whereas the drivers for newer audio adapters are more likely to support the WaveRT DDI.</span></span> <span data-ttu-id="0f2ad-123">Für Anwendungen im exklusiven Modus können WaveRT-Treiber eine bessere Leistung als wavecyclic-oder wavepci-Treiber bereitstellen, aber WaveRT-Treiber erfordern zusätzliche Hardwarefunktionen.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-123">For exclusive-mode applications, WaveRT drivers can provide better performance than WaveCyclic or WavePci drivers, but WaveRT drivers require additional hardware capabilities.</span></span> <span data-ttu-id="0f2ad-124">Zu diesen Funktionen gehört die Möglichkeit, Hardware Puffer direkt für Anwendungen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-124">These capabilities include the ability to share hardware buffers directly with applications.</span></span> <span data-ttu-id="0f2ad-125">Bei direkter Freigabe ist kein System Eingriff erforderlich, um Daten zwischen einer Anwendung im exklusiven Modus und der Audiohardware zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-125">With direct sharing, no system intervention is required to transfer data between an exclusive-mode application and the audio hardware.</span></span> <span data-ttu-id="0f2ad-126">Im Gegensatz dazu eignen sich wavecyclic-und wavepci-Treiber für ältere, weniger leistungsfähige Audioadapter.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-126">In contrast, WaveCyclic and WavePci drivers are suitable for older, less capable audio adapters.</span></span> <span data-ttu-id="0f2ad-127">Diese Adapter basieren auf Systemsoftware zum Transportieren von Datenblöcken (die an System-e/a-Anforderungs Pakete oder-nach Richt Paketen angefügt sind) zwischen Anwendungs Puffern und Hardware Puffern.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-127">These adapters rely on system software to transport blocks of data (attached to system I/O request packets, or IRPs) between application buffers and hardware buffers.</span></span> <span data-ttu-id="0f2ad-128">Außerdem basieren USB-Audiogeräte auf Systemsoftware, um Daten zwischen Anwendungs Puffern und Hardware Puffern zu transportieren.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-128">In addition, USB audio devices rely on system software to transport data between application buffers and hardware buffers.</span></span> <span data-ttu-id="0f2ad-129">Um die Leistung von Anwendungen im exklusiven Modus zu verbessern, die eine Verbindung mit Audiogeräten herstellen, die auf dem System für den Datentransport basieren, erhöht WASAPI automatisch die Priorität der Systemthreads, die Daten zwischen den Anwendungen und der Hardware übertragen.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-129">To improve the performance of exclusive-mode applications that connect to audio devices that rely on the system for data transport, WASAPI automatically increases the priority of the system threads that transfer data between the applications and the hardware.</span></span> <span data-ttu-id="0f2ad-130">WASAPI verwendet MMCSS, um die Thread Priorität zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-130">WASAPI uses MMCSS to increase the thread priority.</span></span> <span data-ttu-id="0f2ad-131">Wenn ein System Thread in Windows Vista den Datentransport für einen Audiowiedergabe-Stream im exklusiven Modus mit einem PCM-Format und einem Geräte Zeitraum von weniger als 10 Millisekunden verwaltet, weist WASAPI dem Thread den MMCSS-Aufgaben Namen "pro-Audiodatei" zu.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-131">In Windows Vista, if a system thread manages data transport for an exclusive-mode audio playback stream with a PCM format and a device period of less than 10 milliseconds, WASAPI assigns the MMCSS task name "Pro Audio" to the thread.</span></span> <span data-ttu-id="0f2ad-132">Wenn der Geräte Zeitraum des Streams größer oder gleich 10 Millisekunden ist, weist WASAPI dem Thread den MMCSS-Aufgaben Namen "Audiodatei" zu.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-132">If the device period of the stream is greater than or equal to 10 milliseconds, WASAPI assigns the MMCSS task name "Audio" to the thread.</span></span> <span data-ttu-id="0f2ad-133">Weitere Informationen zu wavecyclic, wavepci und WaveRT DDIs finden Sie in der Windows-DDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-133">For more information about the WaveCyclic, WavePci, and WaveRT DDIs, see the Windows DDK documentation.</span></span> <span data-ttu-id="0f2ad-134">Weitere Informationen zum Auswählen eines geeigneten Geräte Zeitraums finden Sie unter [**iaudioclient:: getdeviceperiod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod).</span><span class="sxs-lookup"><span data-stu-id="0f2ad-134">For information about selecting an appropriate device period, see [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod).</span></span>

<span data-ttu-id="0f2ad-135">Wie unter [Sitzungs Volume](session-volume-controls.md)-Steuerelemente beschrieben, bietet [WASAPI](wasapi.md) die Schnittstellen [**isimpleaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**ichannelaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)und [**iaudiostreamvolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) zum Steuern der volumeebenen von Audiodatenströmen im freigegebenen Modus.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-135">As described in [Session Volume Controls](session-volume-controls.md), [WASAPI](wasapi.md) provides the [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), and [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) interfaces for controlling the volume levels of shared-mode audio streams.</span></span> <span data-ttu-id="0f2ad-136">Die Steuerelemente in diesen Schnittstellen wirken sich jedoch nicht auf Datenströme im exklusiven Modus aus.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-136">However, the controls in these interfaces have no effect on exclusive-mode streams.</span></span> <span data-ttu-id="0f2ad-137">Anwendungen, die Stream im exklusiven Modus verwalten, verwenden stattdessen in der Regel die Schnittstelle [**iaudioendpointvolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) in der [endpointvolume-API](endpointvolume-api.md) , um die volumeebenen dieser Streams zu steuern.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-137">Instead, applications that manage exclusive-mode streams typically use the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface in the [EndpointVolume API](endpointvolume-api.md) to control the volume levels of those streams.</span></span> <span data-ttu-id="0f2ad-138">Weitere Informationen zu dieser Schnittstelle finden Sie unter [EndPoint Volume](endpoint-volume-controls.md)-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-138">For information about this interface, see [Endpoint Volume Controls](endpoint-volume-controls.md).</span></span>

<span data-ttu-id="0f2ad-139">Der Benutzer kann für jedes Wiedergabe Gerät und Erfassungsgerät im System steuern, ob das Gerät im exklusiven Modus verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-139">For each playback device and capture device in the system, the user can control whether the device can be used in exclusive mode.</span></span> <span data-ttu-id="0f2ad-140">Wenn der Benutzer die Verwendung des Geräts im exklusiven Modus deaktiviert, kann das Gerät verwendet werden, um nur Datenströme im freigegebenen Modus wiederzugeben oder aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-140">If the user disables exclusive-mode use of the device, the device can be used to play or record only shared-mode streams.</span></span>

<span data-ttu-id="0f2ad-141">Wenn der Benutzer die Verwendung des Geräts im exklusiven Modus ermöglicht, kann der Benutzer auch steuern, ob eine Anforderung von einer Anwendung, das Gerät im exklusiven Modus zu verwenden, der Verwendung des Geräts durch Anwendungen vorangestellt wird, die möglicherweise gerade wiedergeben oder die Datenströme im freigegebenen Modus über das Gerät aufzeichnen.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-141">If the user enables exclusive-mode use of the device, the user can also control whether a request by an application to use the device in exclusive mode will preempt the use of the device by applications that might currently be playing or recording shared-mode streams through the device.</span></span> <span data-ttu-id="0f2ad-142">Wenn die vorab Entfernung aktiviert ist, wird eine Anforderung von einer Anwendung, die exklusive Kontrolle über das Gerät zu nehmen, erfolgreich ausgeführt, wenn das Gerät derzeit nicht verwendet wird, oder wenn das Gerät im Modus für gemeinsame Nutzung verwendet wird, aber die Anforderung schlägt fehl, wenn eine andere Anwendung bereits über eine exklusive Kontrolle über das Gerät verfügt.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-142">If preemption is enabled, a request by an application to take exclusive control of the device succeeds if the device is currently not in use, or if the device is being used in shared mode, but the request fails if another application already has exclusive control of the device.</span></span> <span data-ttu-id="0f2ad-143">Wenn die vorab Entfernung deaktiviert ist, wird eine Anforderung von einer Anwendung, die exklusive Kontrolle über das Gerät zu nehmen, erfolgreich ausgeführt, wenn das Gerät derzeit nicht verwendet wird, aber die Anforderung schlägt fehl, wenn das Gerät bereits im freigegebenen Modus oder im exklusiven Modus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-143">If preemption is disabled, a request by an application to take exclusive control of the device succeeds if the device is not currently in use, but the request fails if the device is already being used either in shared mode or in exclusive mode.</span></span>

<span data-ttu-id="0f2ad-144">In Windows Vista lauten die Standardeinstellungen für ein audioendpunktgerät wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0f2ad-144">In Windows Vista, the default settings for an audio endpoint device are the following:</span></span>

-   <span data-ttu-id="0f2ad-145">Das Gerät kann verwendet werden, um Streams im exklusiven Modus wiederzugeben oder aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-145">The device can be used to play or record exclusive-mode streams.</span></span>
-   <span data-ttu-id="0f2ad-146">Eine Anforderung zur Verwendung eines Geräts zum Wiedergeben oder Aufzeichnen eines Streams im exklusiven Modus weist jeden Datenstrom im freigegebenen Modus an, der gerade wiedergegeben oder über das Gerät aufgezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-146">A request to use a device to play or record an exclusive-mode stream preempts any shared-mode stream that is currently being played or recorded through the device.</span></span>

<span data-ttu-id="0f2ad-147">**So ändern Sie die Einstellungen für den exklusiven Modus eines Wiedergabe-oder Aufzeichnungs Geräts**</span><span class="sxs-lookup"><span data-stu-id="0f2ad-147">**To change the exclusive-mode settings of a playback or recording device**</span></span>

1.  <span data-ttu-id="0f2ad-148">Klicken Sie mit der rechten Maustaste auf das Redner Symbol im Benachrichtigungsbereich, das sich auf der rechten Seite der Taskleiste befindet, und wählen Sie **Geräte wieder** geben oder **Geräte aufzeichnen** aus.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-148">Right-click the speaker icon in the notification area, which is located on the right side of the taskbar, and select **Playback Devices** or **Recording Devices**.</span></span> <span data-ttu-id="0f2ad-149">(Alternativ können Sie die Windows-Multimedia-Systemsteuerung Mmsys.cpl in einem Eingabe Aufforderungs Fenster ausführen.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-149">(As an alternative, run the Windows multimedia control panel, Mmsys.cpl, from a Command Prompt window.</span></span> <span data-ttu-id="0f2ad-150">Weitere Informationen finden Sie unter Hinweise in [Geräte \_ Status \_ xxx-Konstanten](device-state-xxx-constants.md).)</span><span class="sxs-lookup"><span data-stu-id="0f2ad-150">For more information, see Remarks in [DEVICE\_STATE\_XXX Constants](device-state-xxx-constants.md).)</span></span>
2.  <span data-ttu-id="0f2ad-151">Nachdem das **Sound** Fenster angezeigt wird, wählen Sie **Wiedergabe** oder **Aufzeichnung** aus.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-151">After the **Sound** window appears, select **Playback** or **Recording**.</span></span> <span data-ttu-id="0f2ad-152">Wählen Sie als nächstes einen Eintrag in der Liste der Gerätenamen aus, und klicken Sie auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-152">Next, select an entry in the list of device names, and click **Properties**.</span></span>
3.  <span data-ttu-id="0f2ad-153">Nachdem das Fenster **Eigenschaften** angezeigt wird, klicken Sie auf **erweitert**.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-153">After the **Properties** window appears, click **Advanced**.</span></span>
4.  <span data-ttu-id="0f2ad-154">Aktivieren Sie das Kontrollkästchen **Anwendungen das ausschließliche Steuern dieses Geräts gestatten**, damit Anwendungen das Gerät im exklusiven Modus verwenden können.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-154">To enable applications to use the device in exclusive mode, check the box labeled **Allow applications to take exclusive control of this device**.</span></span> <span data-ttu-id="0f2ad-155">Deaktivieren Sie das Kontrollkästchen, um die Verwendung des Geräts im exklusiven Modus zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-155">To disable exclusive-mode use of the device, clear the check box.</span></span>
5.  <span data-ttu-id="0f2ad-156">Wenn die Verwendung des Geräts im exklusiven Modus aktiviert ist, können Sie angeben, ob eine Anforderung für die exklusive Kontrolle des Geräts erfolgreich ist, wenn das Gerät gerade wieder verwendet wird oder Datenströme im freigegebenen Modus aufzeichnen.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-156">If exclusive-mode use of the device is enabled, you can specify whether a request for exclusive control of the device will succeed if the device is currently playing or recording shared-mode streams.</span></span> <span data-ttu-id="0f2ad-157">Wenn Sie Anwendungen im exklusiven Modus Vorrang vor Anwendungen im freigegebenen Modus einräumen möchten, aktivieren Sie das Kontrollkästchen mit der Bezeichnung **Anwendungs Priorität im exklusiven Modus vergeben**.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-157">To give exclusive-mode applications priority over shared-mode applications, check the box labeled **Give exclusive mode applications priority**.</span></span> <span data-ttu-id="0f2ad-158">Deaktivieren Sie das Kontrollkästchen, um Anwendungen im exklusiven Modus Vorrang vor Anwendungen im Modus für freigegebene Anwendungen zu verweigern.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-158">To deny exclusive-mode applications priority over shared-mode applications, clear the check box.</span></span>

<span data-ttu-id="0f2ad-159">Im folgenden Codebeispiel wird gezeigt, wie Sie einen Audiostream mit niedriger Latenz auf einem audiorenderinggerät wiedergeben, das für die Verwendung im exklusiven Modus konfiguriert ist:</span><span class="sxs-lookup"><span data-stu-id="0f2ad-159">The following code example shows how to play a low-latency audio stream on an audio-rendering device that is configured for use in exclusive mode:</span></span>


```C++
//-----------------------------------------------------------
// Play an exclusive-mode stream on the default audio
// rendering device. The PlayExclusiveStream function uses
// event-driven buffering and MMCSS to play the stream at
// the minimum latency supported by the device.
//-----------------------------------------------------------

// REFERENCE_TIME time units per second and per millisecond
#define REFTIMES_PER_SEC  10000000
#define REFTIMES_PER_MILLISEC  10000

#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
const IID IID_IAudioClient = __uuidof(IAudioClient);
const IID IID_IAudioRenderClient = __uuidof(IAudioRenderClient);

HRESULT PlayExclusiveStream(MyAudioSource *pMySource)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = 0;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioRenderClient *pRenderClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    HANDLE hEvent = NULL;
    HANDLE hTask = NULL;
    UINT32 bufferFrameCount;
    BYTE *pData;
    DWORD flags = 0;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(
                        eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(
                    IID_IAudioClient, CLSCTX_ALL,
                    NULL, (void**)&pAudioClient);
    EXIT_ON_ERROR(hr)

    // Call a helper function to negotiate with the audio
    // device for an exclusive-mode stream format.
    hr = GetStreamFormat(pAudioClient, &pwfx);
    EXIT_ON_ERROR(hr)

    // Initialize the stream to play at the minimum latency.
    hr = pAudioClient->GetDevicePeriod(NULL, &hnsRequestedDuration);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->Initialize(
                         AUDCLNT_SHAREMODE_EXCLUSIVE,
                         AUDCLNT_STREAMFLAGS_EVENTCALLBACK,
                         hnsRequestedDuration,
                         hnsRequestedDuration,
                         pwfx,
                         NULL);
    EXIT_ON_ERROR(hr)

    // Tell the audio source which format to use.
    hr = pMySource->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Create an event handle and register it for
    // buffer-event notifications.
    hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (hEvent == NULL)
    {
        hr = E_FAIL;
        goto Exit;
    }

    hr = pAudioClient->SetEventHandle(hEvent);
    EXIT_ON_ERROR(hr);

    // Get the actual size of the two allocated buffers.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioRenderClient,
                         (void**)&pRenderClient);
    EXIT_ON_ERROR(hr)

    // To reduce latency, load the first buffer with data
    // from the audio source before starting the stream.
    hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
    EXIT_ON_ERROR(hr)

    hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
    EXIT_ON_ERROR(hr)

    hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
    EXIT_ON_ERROR(hr)

    // Ask MMCSS to temporarily boost the thread priority
    // to reduce glitches while the low-latency stream plays.
    DWORD taskIndex = 0;
    hTask = AvSetMmThreadCharacteristics(TEXT("Pro Audio"), &taskIndex);
    if (hTask == NULL)
    {
        hr = E_FAIL;
        EXIT_ON_ERROR(hr)
    }

    hr = pAudioClient->Start();  // Start playing.
    EXIT_ON_ERROR(hr)

    // Each loop fills one of the two buffers.
    while (flags != AUDCLNT_BUFFERFLAGS_SILENT)
    {
        // Wait for next buffer event to be signaled.
        DWORD retval = WaitForSingleObject(hEvent, 2000);
        if (retval != WAIT_OBJECT_0)
        {
            // Event handle timed out after a 2-second wait.
            pAudioClient->Stop();
            hr = ERROR_TIMEOUT;
            goto Exit;
        }

        // Grab the next empty buffer from the audio device.
        hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
        EXIT_ON_ERROR(hr)

        // Load the buffer with data from the audio source.
        hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
        EXIT_ON_ERROR(hr)

        hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
        EXIT_ON_ERROR(hr)
    }

    // Wait for the last buffer to play before stopping.
    Sleep((DWORD)(hnsRequestedDuration/REFTIMES_PER_MILLISEC));

    hr = pAudioClient->Stop();  // Stop playing.
    EXIT_ON_ERROR(hr)

Exit:
    if (hEvent != NULL)
    {
        CloseHandle(hEvent);
    }
    if (hTask != NULL)
    {
        AvRevertMmThreadCharacteristics(hTask);
    }
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pRenderClient)

    return hr;
}
```



<span data-ttu-id="0f2ad-160">Im vorangehenden Codebeispiel wird die playexclusivestream-Funktion im Anwendungs Thread ausgeführt, der die Endpunkt Puffer beim Abspielen eines renderingstreams Dienste ausführt.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-160">In the preceding code example, the PlayExclusiveStream function runs in the application thread that services the endpoint buffers while a rendering stream is playing.</span></span> <span data-ttu-id="0f2ad-161">Die Funktion nimmt den einzelnen Parameter pmysource an, der ein Zeiger auf ein Objekt ist, das zu einer Client definierten Klasse myaudiosource gehört.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-161">The function takes a single parameter, pMySource, which is a pointer to an object that belongs to a client-defined class, MyAudioSource.</span></span> <span data-ttu-id="0f2ad-162">Diese Klasse verfügt über zwei Member-Funktionen, LoadData und SetFormat, die im Codebeispiel aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-162">This class has two member functions, LoadData and SetFormat, that are called in the code example.</span></span> <span data-ttu-id="0f2ad-163">Myaudiosource wird unter [Rendern eines Streams](rendering-a-stream.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-163">MyAudioSource is described in [Rendering a Stream](rendering-a-stream.md).</span></span>

<span data-ttu-id="0f2ad-164">Die playexclusivestream-Funktion Ruft die Hilfsfunktion getstreamformat auf, die mit dem standardmäßigen renderinggerät aushandiert, um zu bestimmen, ob das Gerät ein Streamformat im exklusiven Modus unterstützt, das für die Verwendung durch die Anwendung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-164">The PlayExclusiveStream function calls a helper function, GetStreamFormat, that negotiates with the default rendering device to determine whether the device supports an exclusive-mode stream format that is suitable for use by the application.</span></span> <span data-ttu-id="0f2ad-165">Der Code für die getstreamformat-Funktion wird nicht im Codebeispiel angezeigt. Dies liegt daran, dass die Details der Implementierung vollständig von den Anforderungen der Anwendung abhängen.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-165">The code for the GetStreamFormat function does not appear in the code example; that is because the details of its implementation depend entirely on the requirements of the application.</span></span> <span data-ttu-id="0f2ad-166">Der Vorgang der getstreamformat-Funktion kann jedoch einfach beschrieben werden – Sie ruft die [**iaudioclient:: isformatsupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) -Methode einmal oder mehrmals auf, um zu bestimmen, ob das Gerät ein geeignetes Format unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-166">However, the operation of the GetStreamFormat function can be described simply—it calls the [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) method one or more times to determine whether the device supports a suitable format.</span></span> <span data-ttu-id="0f2ad-167">Die Anforderungen der Anwendung legen fest, welche Formate getstreamformat für die **isformatsupported** -Methode und die Reihenfolge darstellt, in der Sie präsentiert werden.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-167">The requirements of the application dictate which formats GetStreamFormat presents to the **IsFormatSupported** method and the order in which it presents them.</span></span> <span data-ttu-id="0f2ad-168">Weitere Informationen zu **isformatsupported** finden Sie unter [Geräte Formate](device-formats.md).</span><span class="sxs-lookup"><span data-stu-id="0f2ad-168">For more information about **IsFormatSupported**, see [Device Formats](device-formats.md).</span></span>

<span data-ttu-id="0f2ad-169">Nach dem Aufruf getstreamformat Ruft die playexclusivestream-Funktion die [**iaudioclient:: getdeviceperiod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod) -Methode auf, um den minimalen von der Audiohardware unterstützten Geräte Zeitraum zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-169">After the GetStreamFormat call, the PlayExclusiveStream function calls the [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod) method to obtain the minimum device period supported by the audio hardware.</span></span> <span data-ttu-id="0f2ad-170">Als nächstes Ruft die-Funktion die [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Methode auf, um eine Puffer Dauer anzufordern, die dem minimalen Zeitraum entspricht.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-170">Next, the function calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method to request a buffer duration equal to the minimum period.</span></span> <span data-ttu-id="0f2ad-171">Wenn der-Vorgang erfolgreich ausgeführt wird, ordnet die **Initialize** -Methode zwei Endpunkt Puffer zu, von denen jeder gleich dem Mindestzeitraum ist.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-171">If the call succeeds, the **Initialize** method allocates two endpoint buffers, each of which is equal in duration to the minimum period.</span></span> <span data-ttu-id="0f2ad-172">Wenn der Audiostream zu einem späteren Zeitpunkt ausgeführt wird, werden die beiden Puffer von der Anwendungs-und Audiohardware in der "Ping-Pong"-Weise gemeinsam genutzt – das heißt, während die Anwendung in einen Puffer schreibt, liest die Hardware aus dem anderen Puffer.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-172">Later, when the audio stream begins running, the application and audio hardware will share the two buffers in "ping-pong" fashion—that is, while the application writes to one buffer, the hardware reads from the other buffer.</span></span>

<span data-ttu-id="0f2ad-173">Vor dem Starten des Streams führt die playexclusivestream-Funktion folgende Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="0f2ad-173">Before starting the stream, the PlayExclusiveStream function does the following:</span></span>

-   <span data-ttu-id="0f2ad-174">Erstellt und registriert das Ereignis handle, über das es Benachrichtigungen empfängt, wenn Puffer bereit zum Auffüllen werden.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-174">Creates and registers the event handle through which it will receive notifications when buffers become ready to fill.</span></span>
-   <span data-ttu-id="0f2ad-175">Füllt den ersten Puffer mit Daten aus der Audioquelle aus, um die Verzögerung zu verringern, wenn der Stream mit der Ausführung beginnt, wenn der ursprüngliche Sound gehört.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-175">Fills the first buffer with data from the audio source to reduce the delay from when the stream starts running to when the initial sound is heard.</span></span>
-   <span data-ttu-id="0f2ad-176">Ruft die **avsetmmthreadcharacteristics** -Funktion auf, um anzufordern, dass MMCSS die Priorität des Threads erhöht, in dem playexclusivestream ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-176">Calls the **AvSetMmThreadCharacteristics** function to request that MMCSS increase the priority of the thread in which PlayExclusiveStream executes.</span></span> <span data-ttu-id="0f2ad-177">(Wenn der Stream nicht mehr ausgeführt wird, stellt der **avrevertmmthreadcharacteristics** -Funktionsaufrufe die ursprüngliche Thread Priorität wieder her.)</span><span class="sxs-lookup"><span data-stu-id="0f2ad-177">(When the stream stops running, the **AvRevertMmThreadCharacteristics** function call restores the original thread priority.)</span></span>

<span data-ttu-id="0f2ad-178">Weitere Informationen zu **avsetmmthreadcharacteristics** und **avrevertmmthreadcharacteristics** finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-178">For more information about **AvSetMmThreadCharacteristics** and **AvRevertMmThreadCharacteristics**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="0f2ad-179">Während der Stream ausgeführt wird, füllt jede Iterationen der **while**-Schleife im vorangehenden Codebeispiel einen Endpunkt Puffer aus.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-179">While the stream is running, each iteration of the **while**-loop in the preceding code example fills one endpoint buffer.</span></span> <span data-ttu-id="0f2ad-180">Zwischen Iterationen wartet der **WaitForSingleObject** -Funktions Aufrufpunkt darauf, dass das Ereignis Handle signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-180">Between iterations, the **WaitForSingleObject** function call waits for the event handle to be signaled.</span></span> <span data-ttu-id="0f2ad-181">Wenn das Handle signalisiert wird, führt der Schleifen Text Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="0f2ad-181">When the handle is signaled, the loop body does the following:</span></span>

1.  <span data-ttu-id="0f2ad-182">Ruft die [**iaudiorenderclient:: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) -Methode auf, um den nächsten Puffer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-182">Calls the [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) method to get the next buffer.</span></span>
2.  <span data-ttu-id="0f2ad-183">Füllt den Puffer.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-183">Fills the buffer.</span></span>
3.  <span data-ttu-id="0f2ad-184">Ruft die [**iaudiorenderclient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) -Methode auf, um den Puffer freizugeben.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-184">Calls the [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) method to release the buffer.</span></span>

<span data-ttu-id="0f2ad-185">Weitere Informationen zu **WaitForSingleObject** finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-185">For more information about **WaitForSingleObject**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="0f2ad-186">Wenn der Audioadapter von einem WaveRT-Treiber gesteuert wird, ist die Signalisierung des Ereignis Handles an die DMA-Transfer-Benachrichtigungen von der Audiohardware gebunden.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-186">If the audio adapter is controlled by a WaveRT driver, the signaling of the event handle is tied to the DMA-transfer notifications from the audio hardware.</span></span> <span data-ttu-id="0f2ad-187">Bei einem USB-Audiogerät oder bei einem Audiogerät, das von einem wavecyclic-oder wavepci-Treiber gesteuert wird, ist die Signalisierung des Ereignis Handles an die Vervollständigung der Datenpunkte gebunden, die Daten aus dem Anwendungs Puffer an den Hardware Puffer übertragen.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-187">For a USB audio device, or for an audio device that is controlled by a WaveCyclic or WavePci driver, the signaling of the event handle is tied to completions of the IRPs that transfer data from the application buffer to the hardware buffer.</span></span>

<span data-ttu-id="0f2ad-188">Im vorangehenden Codebeispiel werden die Audiohardware und das Computersystem auf ihre Leistungs Limits übertragen.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-188">The preceding code example pushes the audio hardware and the computer system to their performance limits.</span></span> <span data-ttu-id="0f2ad-189">Um die Datenstrom Latenz zu verringern, plant die Anwendung zunächst, den Puffer Wartungs Thread für die Verwendung des minimalen Geräte Zeitraums zu verwenden, der von der Audiohardware unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-189">First, to reduce the stream latency, the application schedules its buffer-servicing thread to use the minimum device period that the audio hardware will support.</span></span> <span data-ttu-id="0f2ad-190">Um sicherzustellen, dass der Thread zuverlässig innerhalb jedes Geräte Zeitraums ausgeführt wird, legt der **avsetmmthreadcharacteristics** -Funktionsname den Taskname-Parameter auf "pro-Audiodatei" (in Windows Vista) auf den Standardaufgaben Namen mit der höchsten Priorität fest.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-190">Second, to ensure that the thread reliably executes within each device period, the **AvSetMmThreadCharacteristics** function call sets the TaskName parameter to "Pro Audio", which is, in Windows Vista, the default task name with the highest priority.</span></span> <span data-ttu-id="0f2ad-191">Stellen Sie sich vor, ob die zeitlichen Anforderungen Ihrer Anwendung gelockert werden können, ohne dass deren Nützlichkeit beeinträchtigt wird.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-191">Consider whether the timing requirements of your application might be relaxed without compromising its usefulness.</span></span> <span data-ttu-id="0f2ad-192">Die Anwendung kann z. b. den Puffer Wartungs Thread so planen, dass er einen Zeitraum verwendet, der länger als der minimale Wert ist.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-192">For example, the application might schedule its buffer-servicing thread to use a period that is longer than the minimum.</span></span> <span data-ttu-id="0f2ad-193">Ein längerer Zeitraum kann die Verwendung einer niedrigeren Thread Priorität sicher erlauben.</span><span class="sxs-lookup"><span data-stu-id="0f2ad-193">A longer period might safely allow the use of a lower thread priority.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f2ad-194">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0f2ad-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f2ad-195">Datenstrom Verwaltung</span><span class="sxs-lookup"><span data-stu-id="0f2ad-195">Stream Management</span></span>](stream-management.md)
</dt> </dl>

 

 



