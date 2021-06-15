---
description: Exclusive-Mode Streams
ms.assetid: 196cc6fe-91bf-46fa-acc9-38a7a4005875
title: Exclusive-Mode Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 677efa83d099bd32ddb0674414e25a9af219bd1a
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068586"
---
# <a name="exclusive-mode-streams"></a><span data-ttu-id="917b2-103">Exclusive-Mode Streams</span><span class="sxs-lookup"><span data-stu-id="917b2-103">Exclusive-Mode Streams</span></span>

<span data-ttu-id="917b2-104">Wie bereits erläutert, verwendet die Anwendung beim Öffnen eines Streams im exklusiven Modus ausschließlich das Audioendpunktgerät, das den Stream abgespielt oder aufzeichnet.</span><span class="sxs-lookup"><span data-stu-id="917b2-104">As explained previously, if an application opens a stream in exclusive mode, the application has exclusive use of the audio endpoint device that plays or records the stream.</span></span> <span data-ttu-id="917b2-105">Im Gegensatz dazu können mehrere Anwendungen ein Audioendpunktgerät gemeinsam nutzen, indem datenströme im freigegebenen Modus auf dem Gerät geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="917b2-105">In contrast, several applications can share an audio endpoint device by opening shared-mode streams on the device.</span></span>

<span data-ttu-id="917b2-106">Der Zugriff im exklusiven Modus auf ein Audiogerät kann wichtige Systemsounds blockieren, die Interoperabilität mit anderen Anwendungen verhindern und andernfalls die Benutzerfreundlichkeit beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="917b2-106">Exclusive-mode access to an audio device can block crucial system sounds, prevent interoperability with other applications, and otherwise degrade the user experience.</span></span> <span data-ttu-id="917b2-107">Um diese Probleme zu beheben, gibt eine Anwendung mit einem Stream im exklusiven Modus in der Regel die Kontrolle über das Audiogerät ab, wenn die Anwendung nicht der Vordergrundprozess ist oder nicht aktiv streamt.</span><span class="sxs-lookup"><span data-stu-id="917b2-107">To mitigate these problems, an application with an exclusive-mode stream typically relinquishes control of the audio device when the application is not the foreground process or is not actively streaming.</span></span>

<span data-ttu-id="917b2-108">Streamlatenz ist die Verzögerung, die dem Datenpfad inhärent ist, der den Endpunktpuffer einer Anwendung mit einem Audioendpunktgerät verbindet.</span><span class="sxs-lookup"><span data-stu-id="917b2-108">Stream latency is the delay that is inherent in the data path that connects an application's endpoint buffer with an audio endpoint device.</span></span> <span data-ttu-id="917b2-109">Bei einem Renderingstream ist die Latenz die maximale Verzögerung von der Zeit, zu der eine Anwendung eine Stichprobe in einen Endpunktpuffer schreibt, bis zu dem Zeitpunkt, zu dem das Beispiel über die Lautsprecher gehört wird.</span><span class="sxs-lookup"><span data-stu-id="917b2-109">For a rendering stream, the latency is the maximum delay from the time that an application writes a sample to an endpoint buffer to the time that the sample is heard through the speakers.</span></span> <span data-ttu-id="917b2-110">Bei einem Erfassungsdatenstrom ist die Latenz die maximale Verzögerung von der Zeit, zu der ein Sound in das Mikrofon eintritt, bis zu dem Zeitpunkt, zu dem eine Anwendung das Beispiel für diesen Sound aus dem Endpunktpuffer lesen kann.</span><span class="sxs-lookup"><span data-stu-id="917b2-110">For a capture stream, the latency is the maximum delay from the time that a sound enters the microphone to the time that an application can read the sample for that sound from the endpoint buffer.</span></span>

<span data-ttu-id="917b2-111">Anwendungen, die Streams im exklusiven Modus verwenden, tun dies häufig, da sie niedrige Latenzen in den Datenpfaden zwischen den Audioendpunktgeräten und den Anwendungsthreads erfordern, die auf die Endpunktpuffer zugreifen.</span><span class="sxs-lookup"><span data-stu-id="917b2-111">Applications that use exclusive-mode streams often do so because they require low latencies in the data paths between the audio endpoint devices and the application threads that access the endpoint buffers.</span></span> <span data-ttu-id="917b2-112">In der Regel werden diese Threads mit relativ hoher Priorität ausgeführt, und sie planen die Ausführung in regelmäßigen Intervallen, die dem periodischen Intervall entsprechen, das nachfolgende Verarbeitungsdurchläufe durch die Audiohardware trennt.</span><span class="sxs-lookup"><span data-stu-id="917b2-112">Typically, these threads run at relatively high priority and schedule themselves to run at periodic intervals that are close to or the same as the periodic interval that separates successive processing passes by the audio hardware.</span></span> <span data-ttu-id="917b2-113">Während jedes Durchlaufs verarbeitet die Audiohardware die neuen Daten in den Endpunktpuffern.</span><span class="sxs-lookup"><span data-stu-id="917b2-113">During each pass, the audio hardware processes the new data in the endpoint buffers.</span></span>

<span data-ttu-id="917b2-114">Um die kleinsten Streamlatenzzeiten zu erzielen, benötigt eine Anwendung möglicherweise sowohl spezielle Audiohardware als auch ein Leicht geladenes Computersystem.</span><span class="sxs-lookup"><span data-stu-id="917b2-114">To achieve the smallest stream latencies, an application might require both special audio hardware, and a computer system that is lightly loaded.</span></span> <span data-ttu-id="917b2-115">Wenn die Audiohardware über die Zeitlimits hinausgeht oder das System mit konkurrierenden Aufgaben mit hoher Priorität geladen wird, kann dies zu einer Störung in einem Audiostream mit geringer Latenz führen.</span><span class="sxs-lookup"><span data-stu-id="917b2-115">Driving the audio hardware beyond its timing limits or loading the system with competing high-priority tasks might cause a glitch in a low-latency audio stream.</span></span> <span data-ttu-id="917b2-116">Bei einem Renderingstream kann beispielsweise eine Störung auftreten, wenn die Anwendung nicht in einen Endpunktpuffer schreiben kann, bevor die Audiohardware den Puffer liest, oder wenn die Hardware den Puffer nicht lesen kann, bevor die Wiedergabe des Puffers geplant ist.</span><span class="sxs-lookup"><span data-stu-id="917b2-116">For example, for a rendering stream, a glitch can occur if the application fails to write to an endpoint buffer before the audio hardware reads the buffer, or if the hardware fails to read the buffer before the time that the buffer is scheduled to play.</span></span> <span data-ttu-id="917b2-117">In der Regel sollte eine Anwendung, die auf einer Vielzahl von Audiohardware und in einer vielzahl von Systemen ausgeführt werden soll, ihre Zeitanforderungen so lockern, dass Störungen in allen Zielumgebungen vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="917b2-117">Typically, an application that is intended to run on a wide variety of audio hardware and in a broad range of systems should relax its timing requirements enough to avoid glitches in all target environments.</span></span>

<span data-ttu-id="917b2-118">Windows Vista verfügt über mehrere Features zur Unterstützung von Anwendungen, die Audiostreams mit geringer Latenz erfordern.</span><span class="sxs-lookup"><span data-stu-id="917b2-118">Windows Vista has several features to support applications that require low-latency audio streams.</span></span> <span data-ttu-id="917b2-119">Wie unter [Benutzermodus-Audiokomponenten](user-mode-audio-components.md)erläutert, können Anwendungen, die zeitkritische Vorgänge ausführen, die MMCSS-Funktionen (Multimedia Class Scheduler Service) aufrufen, um die Threadpriorität zu erhöhen, ohne CPU-Ressourcen für Anwendungen mit niedrigerer Priorität zu verweigern.</span><span class="sxs-lookup"><span data-stu-id="917b2-119">As discussed in [User-Mode Audio Components](user-mode-audio-components.md), applications that perform time-critical operations can call the Multimedia Class Scheduler Service (MMCSS) functions to increase thread priority without denying CPU resources to lower-priority applications.</span></span> <span data-ttu-id="917b2-120">Darüber hinaus unterstützt die [**IAudioClient::Initialize-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) ein AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK-Flag, mit dem der Pufferwartungsthread einer Anwendung die Ausführung planen kann, wenn ein neuer Puffer vom Audiogerät verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="917b2-120">In addition, the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method supports an AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK flag that enables an application's buffer-servicing thread to schedule its execution to occur when a new buffer becomes available from the audio device.</span></span> <span data-ttu-id="917b2-121">Durch die Verwendung dieser Features kann ein Anwendungsthread die Unklarheit darüber reduzieren, wann er ausgeführt wird, wodurch das Risiko von Störungen in einem Audiodatenstrom mit geringer Latenz verringert wird.</span><span class="sxs-lookup"><span data-stu-id="917b2-121">By using these features, an application thread can reduce uncertainty about when it will execute, thereby decreasing the risk of glitches in a low-latency audio stream.</span></span>

<span data-ttu-id="917b2-122">Die Treiber für ältere Audioadapter verwenden wahrscheinlich die WaveCyclic- oder WavePci-Gerätetreiberschnittstelle (Device Driver Interface, DDI), während die Treiber für neuere Audioadapter die WaveRT-DDI eher unterstützen.</span><span class="sxs-lookup"><span data-stu-id="917b2-122">The drivers for older audio adapters are likely to use the WaveCyclic or WavePci device driver interface (DDI), whereas the drivers for newer audio adapters are more likely to support the WaveRT DDI.</span></span> <span data-ttu-id="917b2-123">Bei Anwendungen im exklusiven Modus können WaveRT-Treiber eine bessere Leistung bieten als WaveCyclic- oder WavePci-Treiber, aber WaveRT-Treiber erfordern zusätzliche Hardwarefunktionen.</span><span class="sxs-lookup"><span data-stu-id="917b2-123">For exclusive-mode applications, WaveRT drivers can provide better performance than WaveCyclic or WavePci drivers, but WaveRT drivers require additional hardware capabilities.</span></span> <span data-ttu-id="917b2-124">Zu diesen Funktionen gehört die Möglichkeit, Hardwarepuffer direkt für Anwendungen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="917b2-124">These capabilities include the ability to share hardware buffers directly with applications.</span></span> <span data-ttu-id="917b2-125">Bei direkter Freigabe ist kein Systemeingriff erforderlich, um Daten zwischen einer Anwendung im exklusiven Modus und der Audiohardware zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="917b2-125">With direct sharing, no system intervention is required to transfer data between an exclusive-mode application and the audio hardware.</span></span> <span data-ttu-id="917b2-126">Im Gegensatz dazu eignen sich WaveCyclic- und WavePci-Treiber für ältere, weniger leistungsfähige Audioadapter.</span><span class="sxs-lookup"><span data-stu-id="917b2-126">In contrast, WaveCyclic and WavePci drivers are suitable for older, less capable audio adapters.</span></span> <span data-ttu-id="917b2-127">Diese Adapter verwenden Systemsoftware, um Datenblöcke (angefügt an System-E/A-Anforderungspakete oder IRPs) zwischen Anwendungspuffern und Hardwarepuffern zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="917b2-127">These adapters rely on system software to transport blocks of data (attached to system I/O request packets, or IRPs) between application buffers and hardware buffers.</span></span> <span data-ttu-id="917b2-128">Darüber hinaus verwenden USB-Audiogeräte Systemsoftware, um Daten zwischen Anwendungspuffern und Hardwarepuffern zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="917b2-128">In addition, USB audio devices rely on system software to transport data between application buffers and hardware buffers.</span></span> <span data-ttu-id="917b2-129">Um die Leistung von Anwendungen im exklusiven Modus zu verbessern, die eine Verbindung mit Audiogeräten herstellen, die das System für den Datentransport verwenden, erhöht WASAPI automatisch die Priorität der Systemthreads, die Daten zwischen den Anwendungen und der Hardware übertragen.</span><span class="sxs-lookup"><span data-stu-id="917b2-129">To improve the performance of exclusive-mode applications that connect to audio devices that rely on the system for data transport, WASAPI automatically increases the priority of the system threads that transfer data between the applications and the hardware.</span></span> <span data-ttu-id="917b2-130">WASAPI verwendet MMCSS, um die Threadpriorität zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="917b2-130">WASAPI uses MMCSS to increase the thread priority.</span></span> <span data-ttu-id="917b2-131">Wenn ein Systemthread in Windows Vista den Datentransport für einen Audiowiedergabestream im exklusiven Modus mit einem PCM-Format und einem Gerätezeitraum von weniger als 10 Millisekunden verwaltet, weist WASAPI dem Thread den MMCSS-Aufgabennamen "Pro Audio" zu.</span><span class="sxs-lookup"><span data-stu-id="917b2-131">In Windows Vista, if a system thread manages data transport for an exclusive-mode audio playback stream with a PCM format and a device period of less than 10 milliseconds, WASAPI assigns the MMCSS task name "Pro Audio" to the thread.</span></span> <span data-ttu-id="917b2-132">Wenn der Gerätezeitraum des Streams größer oder gleich 10 Millisekunden ist, weist WASAPI dem Thread den MMCSS-Aufgabennamen "Audio" zu.</span><span class="sxs-lookup"><span data-stu-id="917b2-132">If the device period of the stream is greater than or equal to 10 milliseconds, WASAPI assigns the MMCSS task name "Audio" to the thread.</span></span> <span data-ttu-id="917b2-133">Weitere Informationen zu den WaveCyclic-, WavePci- und WaveRT-DDIs finden Sie in der Windows DDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="917b2-133">For more information about the WaveCyclic, WavePci, and WaveRT DDIs, see the Windows DDK documentation.</span></span> <span data-ttu-id="917b2-134">Informationen zum Auswählen eines geeigneten Gerätezeitraums finden Sie unter [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod).</span><span class="sxs-lookup"><span data-stu-id="917b2-134">For information about selecting an appropriate device period, see [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod).</span></span>

<span data-ttu-id="917b2-135">Wie unter [Sitzungsvolumesteuerelemente](session-volume-controls.md)beschrieben, stellt [WASAPI](wasapi.md) die Schnittstellen [**ISimpleAudioVolume,**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)und [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) zum Steuern der Lautstärkeebenen von Audiostreams im freigegebenen Modus bereit.</span><span class="sxs-lookup"><span data-stu-id="917b2-135">As described in [Session Volume Controls](session-volume-controls.md), [WASAPI](wasapi.md) provides the [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), and [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) interfaces for controlling the volume levels of shared-mode audio streams.</span></span> <span data-ttu-id="917b2-136">Die Steuerelemente in diesen Schnittstellen haben jedoch keine Auswirkungen auf Streams im exklusiven Modus.</span><span class="sxs-lookup"><span data-stu-id="917b2-136">However, the controls in these interfaces have no effect on exclusive-mode streams.</span></span> <span data-ttu-id="917b2-137">Stattdessen verwenden Anwendungen, die Streams im exklusiven Modus verwalten, in der Regel die [**IAudioEndpointVolume-Schnittstelle**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) in der [EndpointVolume-API,](endpointvolume-api.md) um die Volumeebenen dieser Streams zu steuern.</span><span class="sxs-lookup"><span data-stu-id="917b2-137">Instead, applications that manage exclusive-mode streams typically use the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface in the [EndpointVolume API](endpointvolume-api.md) to control the volume levels of those streams.</span></span> <span data-ttu-id="917b2-138">Informationen zu dieser Schnittstelle finden Sie unter [Endpunktvolumesteuerelemente.](endpoint-volume-controls.md)</span><span class="sxs-lookup"><span data-stu-id="917b2-138">For information about this interface, see [Endpoint Volume Controls](endpoint-volume-controls.md).</span></span>

<span data-ttu-id="917b2-139">Für jedes Wiedergabegerät und Erfassungsgerät im System kann der Benutzer steuern, ob das Gerät im exklusiven Modus verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="917b2-139">For each playback device and capture device in the system, the user can control whether the device can be used in exclusive mode.</span></span> <span data-ttu-id="917b2-140">Wenn der Benutzer die Verwendung des Geräts im exklusiven Modus deaktiviert, kann das Gerät verwendet werden, um nur Streams im freigegebenen Modus wiederzugeben oder aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="917b2-140">If the user disables exclusive-mode use of the device, the device can be used to play or record only shared-mode streams.</span></span>

<span data-ttu-id="917b2-141">Wenn der Benutzer die Verwendung des Geräts im exklusiven Modus aktiviert, kann der Benutzer auch steuern, ob eine Anforderung einer Anwendung, das Gerät im exklusiven Modus zu verwenden, der Verwendung des Geräts durch Anwendungen vorkommt, die derzeit Streams im freigegebenen Modus über das Gerät wiedergeben oder aufzeichnen.</span><span class="sxs-lookup"><span data-stu-id="917b2-141">If the user enables exclusive-mode use of the device, the user can also control whether a request by an application to use the device in exclusive mode will preempt the use of the device by applications that might currently be playing or recording shared-mode streams through the device.</span></span> <span data-ttu-id="917b2-142">Wenn die Vorzeitigemption aktiviert ist, ist eine Anforderung einer Anwendung, die exklusive Kontrolle über das Gerät zu übernehmen, erfolgreich, wenn das Gerät derzeit nicht verwendet wird oder wenn das Gerät im freigegebenen Modus verwendet wird. Die Anforderung schlägt jedoch fehl, wenn eine andere Anwendung bereits über die exklusive Kontrolle über das Gerät verfügt.</span><span class="sxs-lookup"><span data-stu-id="917b2-142">If preemption is enabled, a request by an application to take exclusive control of the device succeeds if the device is currently not in use, or if the device is being used in shared mode, but the request fails if another application already has exclusive control of the device.</span></span> <span data-ttu-id="917b2-143">Wenn die Vorzeitigemption deaktiviert ist, ist eine Anforderung einer Anwendung, die exklusive Kontrolle über das Gerät zu übernehmen, erfolgreich, wenn das Gerät derzeit nicht verwendet wird. Die Anforderung schlägt jedoch fehl, wenn das Gerät bereits im freigegebenen modus oder im exklusiven Modus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="917b2-143">If preemption is disabled, a request by an application to take exclusive control of the device succeeds if the device is not currently in use, but the request fails if the device is already being used either in shared mode or in exclusive mode.</span></span>

<span data-ttu-id="917b2-144">In Windows Vista sind die Standardeinstellungen für ein Audioendpunktgerät die folgenden:</span><span class="sxs-lookup"><span data-stu-id="917b2-144">In Windows Vista, the default settings for an audio endpoint device are the following:</span></span>

-   <span data-ttu-id="917b2-145">Das Gerät kann verwendet werden, um Streams im exklusiven Modus wiederzugeben oder aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="917b2-145">The device can be used to play or record exclusive-mode streams.</span></span>
-   <span data-ttu-id="917b2-146">Eine Anforderung, ein Gerät zum Wiedergeben oder Aufzeichnen eines Streams im exklusiven Modus zu verwenden, setzt alle Datenströme im freigegebenen Modus voraus, die derzeit über das Gerät wiedergegeben oder aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="917b2-146">A request to use a device to play or record an exclusive-mode stream preempts any shared-mode stream that is currently being played or recorded through the device.</span></span>

<span data-ttu-id="917b2-147">**So ändern Sie die Einstellungen im exklusiven Modus eines Wiedergabe- oder Aufzeichnungsgeräts**</span><span class="sxs-lookup"><span data-stu-id="917b2-147">**To change the exclusive-mode settings of a playback or recording device**</span></span>

1.  <span data-ttu-id="917b2-148">Klicken Sie mit der rechten Maustaste auf das Lautsprechersymbol im Infobereich auf der rechten Seite der Taskleiste, und wählen Sie **Wiedergabegeräte** oder **Aufzeichnungsgeräte** aus.</span><span class="sxs-lookup"><span data-stu-id="917b2-148">Right-click the speaker icon in the notification area, which is located on the right side of the taskbar, and select **Playback Devices** or **Recording Devices**.</span></span> <span data-ttu-id="917b2-149">(Alternativ können Sie die Windows-Multimedia-Systemsteuerung Mmsys.cpl über ein Eingabeaufforderungsfenster ausführen.</span><span class="sxs-lookup"><span data-stu-id="917b2-149">(As an alternative, run the Windows multimedia control panel, Mmsys.cpl, from a Command Prompt window.</span></span> <span data-ttu-id="917b2-150">Weitere Informationen finden Sie unter Hinweise in [DEVICE \_ STATE \_ XXX-Konstanten](device-state-xxx-constants.md).)</span><span class="sxs-lookup"><span data-stu-id="917b2-150">For more information, see Remarks in [DEVICE\_STATE\_XXX Constants](device-state-xxx-constants.md).)</span></span>
2.  <span data-ttu-id="917b2-151">Nachdem das Fenster **Sound** angezeigt wird, wählen Sie **Wiedergabe** oder **Aufzeichnung** aus.</span><span class="sxs-lookup"><span data-stu-id="917b2-151">After the **Sound** window appears, select **Playback** or **Recording**.</span></span> <span data-ttu-id="917b2-152">Wählen Sie als Nächstes einen Eintrag in der Liste der Gerätenamen aus, und klicken Sie auf **Eigenschaften.**</span><span class="sxs-lookup"><span data-stu-id="917b2-152">Next, select an entry in the list of device names, and click **Properties**.</span></span>
3.  <span data-ttu-id="917b2-153">Nachdem das Fenster **Eigenschaften** angezeigt wird, klicken Sie auf **Erweitert.**</span><span class="sxs-lookup"><span data-stu-id="917b2-153">After the **Properties** window appears, click **Advanced**.</span></span>
4.  <span data-ttu-id="917b2-154">Um Anwendungen die Verwendung des Geräts im exklusiven Modus zu ermöglichen, aktivieren Sie das Kontrollkästchen Zulassen, dass **Anwendungen die exklusive Kontrolle über dieses Gerät übernehmen.**</span><span class="sxs-lookup"><span data-stu-id="917b2-154">To enable applications to use the device in exclusive mode, check the box labeled **Allow applications to take exclusive control of this device**.</span></span> <span data-ttu-id="917b2-155">Deaktivieren Sie das Kontrollkästchen, um die Verwendung des Geräts im exklusiven Modus zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="917b2-155">To disable exclusive-mode use of the device, clear the check box.</span></span>
5.  <span data-ttu-id="917b2-156">Wenn die Verwendung des Geräts im exklusiven Modus aktiviert ist, können Sie angeben, ob eine Anforderung zur exklusiven Steuerung des Geräts erfolgreich ist, wenn das Gerät derzeit Streams im freigegebenen Modus abspielt oder aufzeichnet.</span><span class="sxs-lookup"><span data-stu-id="917b2-156">If exclusive-mode use of the device is enabled, you can specify whether a request for exclusive control of the device will succeed if the device is currently playing or recording shared-mode streams.</span></span> <span data-ttu-id="917b2-157">Aktivieren Sie das Kontrollkästchen Anwendungen im exklusiven Modus Priorität geben, um Anwendungen im **exklusiven Modus** Vorrang vor Anwendungen im gemeinsam genutzten Modus zu geben.</span><span class="sxs-lookup"><span data-stu-id="917b2-157">To give exclusive-mode applications priority over shared-mode applications, check the box labeled **Give exclusive mode applications priority**.</span></span> <span data-ttu-id="917b2-158">Deaktivieren Sie das Kontrollkästchen, um die Priorität von Anwendungen im exklusiven Modus gegenüber Anwendungen im freigegebenen Modus zu verweigern.</span><span class="sxs-lookup"><span data-stu-id="917b2-158">To deny exclusive-mode applications priority over shared-mode applications, clear the check box.</span></span>

<span data-ttu-id="917b2-159">Das folgende Codebeispiel zeigt, wie Sie einen Audiostream mit geringer Latenz auf einem Audiorenderinggerät wiedergeben, das für die Verwendung im exklusiven Modus konfiguriert ist:</span><span class="sxs-lookup"><span data-stu-id="917b2-159">The following code example shows how to play a low-latency audio stream on an audio-rendering device that is configured for use in exclusive mode:</span></span>


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
    DWORD taskIndex = 0;
    
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
    if (hr == AUDCLNT_E_BUFFER_SIZE_NOT_ALIGNED) {
        // Align the buffer if needed, see IAudioClient::Initialize() documentation
        UINT32 nFrames = 0;
        hr = pAudioClient->GetBufferSize(&nFrames);
        EXIT_ON_ERROR(hr)
        hnsRequestedDuration = (REFERENCE_TIME)((double)REFTIMES_PER_SEC / pwfx->nSamplesPerSec * nFrames + 0.5);
        hr = pAudioClient->Initialize(
            AUDCLNT_SHAREMODE_EXCLUSIVE,
            AUDCLNT_STREAMFLAGS_EVENTCALLBACK,
            hnsRequestedDuration,
            hnsRequestedDuration,
            pwfx,
            NULL);
    }
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



<span data-ttu-id="917b2-160">Im vorherigen Codebeispiel wird die PlayExclusiveStream-Funktion im Anwendungsthread ausgeführt, der die Endpunktpuffer wartet, während ein Renderingstream wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="917b2-160">In the preceding code example, the PlayExclusiveStream function runs in the application thread that services the endpoint buffers while a rendering stream is playing.</span></span> <span data-ttu-id="917b2-161">Die Funktion verwendet einen einzelnen Parameter, pMySource, der ein Zeiger auf ein Objekt ist, das zu einer vom Client definierten Klasse MyAudioSource gehört.</span><span class="sxs-lookup"><span data-stu-id="917b2-161">The function takes a single parameter, pMySource, which is a pointer to an object that belongs to a client-defined class, MyAudioSource.</span></span> <span data-ttu-id="917b2-162">Diese Klasse verfügt über zwei Memberfunktionen, LoadData und SetFormat, die im Codebeispiel aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="917b2-162">This class has two member functions, LoadData and SetFormat, that are called in the code example.</span></span> <span data-ttu-id="917b2-163">MyAudioSource wird unter [Rendern eines Streams](rendering-a-stream.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="917b2-163">MyAudioSource is described in [Rendering a Stream](rendering-a-stream.md).</span></span>

<span data-ttu-id="917b2-164">Die PlayExclusiveStream-Funktion ruft die Hilfsfunktion GetStreamFormat auf, die mit dem Standardrenderinggerät aushandelt, um zu bestimmen, ob das Gerät ein Streamformat im exklusiven Modus unterstützt, das für die Verwendung durch die Anwendung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="917b2-164">The PlayExclusiveStream function calls a helper function, GetStreamFormat, that negotiates with the default rendering device to determine whether the device supports an exclusive-mode stream format that is suitable for use by the application.</span></span> <span data-ttu-id="917b2-165">Der Code für die GetStreamFormat-Funktion wird im Codebeispiel nicht angezeigt. Dies liegt daran, dass die Details der Implementierung vollständig von den Anforderungen der Anwendung abhängen.</span><span class="sxs-lookup"><span data-stu-id="917b2-165">The code for the GetStreamFormat function does not appear in the code example; that is because the details of its implementation depend entirely on the requirements of the application.</span></span> <span data-ttu-id="917b2-166">Der Vorgang der GetStreamFormat-Funktion kann jedoch einfach beschrieben werden. Sie ruft die [**IAudioClient::IsFormatSupported-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) ein oder mehrere Male auf, um zu bestimmen, ob das Gerät ein geeignetes Format unterstützt.</span><span class="sxs-lookup"><span data-stu-id="917b2-166">However, the operation of the GetStreamFormat function can be described simply—it calls the [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) method one or more times to determine whether the device supports a suitable format.</span></span> <span data-ttu-id="917b2-167">Die Anforderungen der Anwendung legen fest, welche Formate GetStreamFormat der **IsFormatSupported-Methode** und in welcher Reihenfolge sie präsentiert werden.</span><span class="sxs-lookup"><span data-stu-id="917b2-167">The requirements of the application dictate which formats GetStreamFormat presents to the **IsFormatSupported** method and the order in which it presents them.</span></span> <span data-ttu-id="917b2-168">Weitere Informationen zu **IsFormatSupported** finden Sie unter [Geräteformate.](device-formats.md)</span><span class="sxs-lookup"><span data-stu-id="917b2-168">For more information about **IsFormatSupported**, see [Device Formats](device-formats.md).</span></span>

<span data-ttu-id="917b2-169">Nach dem GetStreamFormat-Aufruf ruft die PlayExclusiveStream-Funktion die [**IAudioClient::GetDevicePeriod-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod) auf, um den minimalen Gerätezeitraum abzurufen, der von der Audiohardware unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="917b2-169">After the GetStreamFormat call, the PlayExclusiveStream function calls the [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod) method to obtain the minimum device period supported by the audio hardware.</span></span> <span data-ttu-id="917b2-170">Als Nächstes ruft die Funktion die [**IAudioClient::Initialize-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) auf, um eine Pufferdauer anzufordern, die dem Mindestzeitraum entspricht.</span><span class="sxs-lookup"><span data-stu-id="917b2-170">Next, the function calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method to request a buffer duration equal to the minimum period.</span></span> <span data-ttu-id="917b2-171">Wenn der Aufruf erfolgreich ist, ordnet die **Initialize-Methode** zwei Endpunktpuffer zu, von denen jeder der Mindestdauer entspricht.</span><span class="sxs-lookup"><span data-stu-id="917b2-171">If the call succeeds, the **Initialize** method allocates two endpoint buffers, each of which is equal in duration to the minimum period.</span></span> <span data-ttu-id="917b2-172">Wenn der Audiostream später ausgeführt wird, teilen sich die Anwendung und die Audiohardware die beiden Puffer "ping-pong", d. h., während die Anwendung in einen Puffer schreibt, liest die Hardware aus dem anderen Puffer.</span><span class="sxs-lookup"><span data-stu-id="917b2-172">Later, when the audio stream begins running, the application and audio hardware will share the two buffers in "ping-pong" fashion—that is, while the application writes to one buffer, the hardware reads from the other buffer.</span></span>

<span data-ttu-id="917b2-173">Vor dem Starten des Streams führt die PlayExclusiveStream-Funktion Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="917b2-173">Before starting the stream, the PlayExclusiveStream function does the following:</span></span>

-   <span data-ttu-id="917b2-174">Erstellt und registriert das Ereignishandle, über das Benachrichtigungen empfangen werden, wenn Puffer gefüllt werden können.</span><span class="sxs-lookup"><span data-stu-id="917b2-174">Creates and registers the event handle through which it will receive notifications when buffers become ready to fill.</span></span>
-   <span data-ttu-id="917b2-175">Füllt den ersten Puffer mit Daten aus der Audioquelle aus, um die Verzögerung von der Ausführung des Streams bis zu dem Zeitpunkt zu reduzieren, zu dem der erste Sound gehört wird.</span><span class="sxs-lookup"><span data-stu-id="917b2-175">Fills the first buffer with data from the audio source to reduce the delay from when the stream starts running to when the initial sound is heard.</span></span>
-   <span data-ttu-id="917b2-176">Ruft die **AvSetMmThreadCharacteristics-Funktion** auf, um anzufordern, dass MMCSS die Priorität des Threads erhöht, in dem PlayExclusiveStream ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="917b2-176">Calls the **AvSetMmThreadCharacteristics** function to request that MMCSS increase the priority of the thread in which PlayExclusiveStream executes.</span></span> <span data-ttu-id="917b2-177">(Wenn die Ausführung des Streams beendet wird, stellt der **AvRevertMmThreadCharacteristics-Funktionsaufruf** die ursprüngliche Threadpriorität wieder her.)</span><span class="sxs-lookup"><span data-stu-id="917b2-177">(When the stream stops running, the **AvRevertMmThreadCharacteristics** function call restores the original thread priority.)</span></span>

<span data-ttu-id="917b2-178">Weitere Informationen zu **AvSetMmThreadCharacteristics** und **AvRevertMmThreadCharacteristics** finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="917b2-178">For more information about **AvSetMmThreadCharacteristics** and **AvRevertMmThreadCharacteristics**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="917b2-179">Während der Stream ausgeführt wird, füllt jede Iteration von **while**-loop im vorherigen Codebeispiel einen Endpunktpuffer aus.</span><span class="sxs-lookup"><span data-stu-id="917b2-179">While the stream is running, each iteration of the **while**-loop in the preceding code example fills one endpoint buffer.</span></span> <span data-ttu-id="917b2-180">Zwischen Iterationen wartet der **WaitForSingleObject-Funktionsaufruf,** bis das Ereignishandle signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="917b2-180">Between iterations, the **WaitForSingleObject** function call waits for the event handle to be signaled.</span></span> <span data-ttu-id="917b2-181">Wenn das Handle signalisiert wird, führt der Schleifentext Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="917b2-181">When the handle is signaled, the loop body does the following:</span></span>

1.  <span data-ttu-id="917b2-182">Ruft die [**IAudioRenderClient::GetBuffer-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) auf, um den nächsten Puffer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="917b2-182">Calls the [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) method to get the next buffer.</span></span>
2.  <span data-ttu-id="917b2-183">Füllt den Puffer aus.</span><span class="sxs-lookup"><span data-stu-id="917b2-183">Fills the buffer.</span></span>
3.  <span data-ttu-id="917b2-184">Ruft die [**IAudioRenderClient::ReleaseBuffer-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) auf, um den Puffer freizugeben.</span><span class="sxs-lookup"><span data-stu-id="917b2-184">Calls the [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) method to release the buffer.</span></span>

<span data-ttu-id="917b2-185">Weitere Informationen zu **WaitForSingleObject** finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="917b2-185">For more information about **WaitForSingleObject**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="917b2-186">Wenn der Audioadapter von einem WaveRT-Treiber gesteuert wird, ist die Signalisierung des Ereignishandle an die DMA-Übertragungsbenachrichtigungen von der Audiohardware gebunden.</span><span class="sxs-lookup"><span data-stu-id="917b2-186">If the audio adapter is controlled by a WaveRT driver, the signaling of the event handle is tied to the DMA-transfer notifications from the audio hardware.</span></span> <span data-ttu-id="917b2-187">Für ein USB-Audiogerät oder für ein Audiogerät, das von einem WaveCyclic- oder WavePci-Treiber gesteuert wird, ist die Signalisierung des Ereignishandle an Vervollständigungen der IRPs gebunden, die Daten aus dem Anwendungspuffer in den Hardwarepuffer übertragen.</span><span class="sxs-lookup"><span data-stu-id="917b2-187">For a USB audio device, or for an audio device that is controlled by a WaveCyclic or WavePci driver, the signaling of the event handle is tied to completions of the IRPs that transfer data from the application buffer to the hardware buffer.</span></span>

<span data-ttu-id="917b2-188">Im obigen Codebeispiel werden die Audiohardware und das Computersystem an ihre Leistungsgrenzen gepusht.</span><span class="sxs-lookup"><span data-stu-id="917b2-188">The preceding code example pushes the audio hardware and the computer system to their performance limits.</span></span> <span data-ttu-id="917b2-189">Um zunächst die Streamlatenz zu reduzieren, plant die Anwendung ihren Pufferwartungsthread so, dass er den minimalen Gerätezeitraum verwendet, den die Audiohardware unterstützt.</span><span class="sxs-lookup"><span data-stu-id="917b2-189">First, to reduce the stream latency, the application schedules its buffer-servicing thread to use the minimum device period that the audio hardware will support.</span></span> <span data-ttu-id="917b2-190">Zweitens legt der **AvSetMmThreadCharacteristics-Funktionsaufruf** den TaskName-Parameter auf "Pro Audio" fest, d.h. in Windows Vista den Standardtasknamen mit der höchsten Priorität, um sicherzustellen, dass der Thread innerhalb jedes Gerätezeitraums zuverlässig ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="917b2-190">Second, to ensure that the thread reliably executes within each device period, the **AvSetMmThreadCharacteristics** function call sets the TaskName parameter to "Pro Audio", which is, in Windows Vista, the default task name with the highest priority.</span></span> <span data-ttu-id="917b2-191">Überlegen Sie, ob die Zeitlichen Anforderungen Ihrer Anwendung möglicherweise gelockert werden, ohne ihre Nützlichkeit zu beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="917b2-191">Consider whether the timing requirements of your application might be relaxed without compromising its usefulness.</span></span> <span data-ttu-id="917b2-192">Beispielsweise kann die Anwendung ihren Pufferwartungsthread so planen, dass er einen Zeitraum verwendet, der länger als der mindeste ist.</span><span class="sxs-lookup"><span data-stu-id="917b2-192">For example, the application might schedule its buffer-servicing thread to use a period that is longer than the minimum.</span></span> <span data-ttu-id="917b2-193">Ein längerer Zeitraum kann die Verwendung einer niedrigeren Threadpriorität sicher zulassen.</span><span class="sxs-lookup"><span data-stu-id="917b2-193">A longer period might safely allow the use of a lower thread priority.</span></span>

## <a name="related-topics"></a><span data-ttu-id="917b2-194">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="917b2-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="917b2-195">Streamverwaltung</span><span class="sxs-lookup"><span data-stu-id="917b2-195">Stream Management</span></span>](stream-management.md)
</dt> </dl>

 

 



