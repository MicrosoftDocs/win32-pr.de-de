---
description: Gerätetopologien
ms.assetid: 5ac421e5-74a4-40e8-af6f-a99a05ebc3e0
title: Gerätetopologien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31e0af267bb4a0fa924ee23d36a2a615ac5ae7fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524256"
---
# <a name="device-topologies"></a><span data-ttu-id="3529c-103">Gerätetopologien</span><span class="sxs-lookup"><span data-stu-id="3529c-103">Device Topologies</span></span>

<span data-ttu-id="3529c-104">Die [devicetopology-API](devicetopology-api.md) ermöglicht Clients die Kontrolle über eine Vielzahl von internen Funktionen von audioadaptern, auf die Sie über die [mmdevice-API](mmdevice-api.md), die [WASAPI](wasapi.md)oder die [endpointvolume-API](endpointvolume-api.md)nicht zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="3529c-104">The [DeviceTopology API](devicetopology-api.md) gives clients control over a variety of internal functions of audio adapters that they cannot access through the [MMDevice API](mmdevice-api.md), [WASAPI](wasapi.md), or the [EndpointVolume API](endpointvolume-api.md).</span></span>

<span data-ttu-id="3529c-105">Wie bereits erläutert, stellen die [mmdevice-API](mmdevice-api.md), [WASAPI](wasapi.md)und die [endpointvolume-API](endpointvolume-api.md) an Clients als [audioendpunktgeräte](audio-endpoint-devices.md)Mikrofon, Referenten, Kopfhörer und andere Audioeingabe-und-Ausgabegeräte zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="3529c-105">As explained previously, the [MMDevice API](mmdevice-api.md), [WASAPI](wasapi.md), and the [EndpointVolume API](endpointvolume-api.md) present microphones, speakers, headphones, and other audio input and output devices to clients as [audio endpoint devices](audio-endpoint-devices.md).</span></span> <span data-ttu-id="3529c-106">Das Endpunkt Gerätemodell ermöglicht Clients den bequemen Zugriff auf die Volume-und stumm Steuerelemente in Audiogeräten.</span><span class="sxs-lookup"><span data-stu-id="3529c-106">The endpoint device model provides clients with convenient access to volume and mute controls in audio devices.</span></span> <span data-ttu-id="3529c-107">Clients, die nur diese einfachen Steuerelemente benötigen, können vermeiden, dass die internen Topologien von Hardware Geräten in audioadaptern durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="3529c-107">Clients that require only these simple controls can avoid traversing the internal topologies of hardware devices in audio adapters.</span></span>

<span data-ttu-id="3529c-108">In Windows Vista konfiguriert die Audioengine automatisch die Topologien von Audiogeräten für die Verwendung durch Audioanwendungen.</span><span class="sxs-lookup"><span data-stu-id="3529c-108">In Windows Vista, the audio engine automatically configures the topologies of audio devices for use by audio applications.</span></span> <span data-ttu-id="3529c-109">Daher müssen Anwendungen selten, falls immer, die Debug-API-API zu diesem Zweck verwenden.</span><span class="sxs-lookup"><span data-stu-id="3529c-109">Thus, applications rarely, if ever, need to use the DeviceTopology API for this purpose.</span></span> <span data-ttu-id="3529c-110">Nehmen wir beispielsweise an, dass ein Audioadapter einen eingabemultiplexer enthält, der einen Stream aus einer Zeilen Eingabe oder einem Mikrofon erfassen kann, aber nicht gleichzeitig Datenströme von beiden Endpunkt Geräten erfassen kann.</span><span class="sxs-lookup"><span data-stu-id="3529c-110">For example, assume that an audio adapter contains an input multiplexer that can capture a stream from either a line input or a microphone, but that cannot capture streams from both endpoint devices at the same time.</span></span> <span data-ttu-id="3529c-111">Angenommen, der Benutzer hat Anwendungen im exklusiven Modus aktiviert, um die Verwendung eines audioendpunktgeräts durch Anwendungen im freigegebenen Modus vorzuführen, wie in Daten [strömen im exklusiven Modus](exclusive-mode-streams.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3529c-111">Assume that the user has enabled exclusive-mode applications to preempt the use of an audio endpoint device by shared-mode applications, as described in [Exclusive-Mode Streams](exclusive-mode-streams.md).</span></span> <span data-ttu-id="3529c-112">Wenn eine Anwendung im freigegebenen Modus einen Stream aus der Zeilen Eingabe abzeichnet, wenn eine Anwendung im exklusiven Modus beginnt, einen Stream vom Mikrofon aufzuzeichnen, schaltet die Audioengine den Multiplexer automatisch von der Zeilen Eingabe in das Mikrofon um.</span><span class="sxs-lookup"><span data-stu-id="3529c-112">If a shared-mode application is recording a stream from the line input at the time that an exclusive-mode application begins recording a stream from the microphone, the audio engine automatically switches the multiplexer from the line input to the microphone.</span></span> <span data-ttu-id="3529c-113">In früheren Versionen von Windows, einschließlich Windows XP, würde die Anwendung im exklusiven Modus in diesem Beispiel die **mixerxxx** -Funktionen in der Windows-Multimedia-API verwenden, um die Topologien der Adapter Geräte zu durchlaufen, den Multiplexer zu ermitteln und den Multiplexer so zu konfigurieren, dass die Mikrofon Eingabe ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="3529c-113">In contrast, in earlier versions of Windows, including Windows XP, the exclusive-mode application in this example would use the **mixerXxx** functions in the Windows multimedia API to traverse the topologies of the adapter devices, discover the multiplexer, and configure the multiplexer to select the microphone input.</span></span> <span data-ttu-id="3529c-114">In Windows Vista sind diese Schritte nicht mehr erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3529c-114">In Windows Vista, these steps are no longer required.</span></span>

<span data-ttu-id="3529c-115">Einige Clients benötigen jedoch möglicherweise explizite Kontrolle über die Typen von audiohardwaresteuerelementen, auf die über die mmdevice-API, die WASAPI oder die endpointvolume-API nicht zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="3529c-115">However, some clients might require explicit control over types of audio hardware controls that cannot be accessed through the MMDevice API, WASAPI, or the EndpointVolume API.</span></span> <span data-ttu-id="3529c-116">Für diese Clients bietet die devicetopology-API die Möglichkeit, die Topologien von Adapter Geräten zu durchlaufen, um die Audiosteuerelemente in den Geräten zu ermitteln und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="3529c-116">For these clients, the DeviceTopology API provides the ability to traverse the topologies of adapter devices to discover and manage the audio controls in the devices.</span></span> <span data-ttu-id="3529c-117">Anwendungen, die die devicetopology-API verwenden, müssen sorgfältig entworfen werden, um das stören der Windows-audiorichtlinie zu vermeiden und die internen Konfigurationen von Audiogeräten zu beeinträchtigen, die für andere Anwendungen freigegeben sind.</span><span class="sxs-lookup"><span data-stu-id="3529c-117">Applications that use the DeviceTopology API must be designed with care to avoid interfering with Windows audio policy and disturbing the internal configurations of audio devices that are shared with other applications.</span></span> <span data-ttu-id="3529c-118">Weitere Informationen zur Windows-audiorichtlinie finden Sie unter [benutzermodusaudiokomponenten](user-mode-audio-components.md).</span><span class="sxs-lookup"><span data-stu-id="3529c-118">For more information about Windows audio policy, see [User-Mode Audio Components](user-mode-audio-components.md).</span></span>

<span data-ttu-id="3529c-119">Die devicetopology-API stellt Schnittstellen zum Ermitteln und Verwalten der folgenden Typen von Audiosteuer Elementen in einer Geräte Topologie bereit:</span><span class="sxs-lookup"><span data-stu-id="3529c-119">The DeviceTopology API provides interfaces for discovering and managing the following types of audio controls in a device topology:</span></span>

-   <span data-ttu-id="3529c-120">Automatisches erlangen von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="3529c-120">Automatic gain control</span></span>
-   <span data-ttu-id="3529c-121">Bass-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3529c-121">Bass control</span></span>
-   <span data-ttu-id="3529c-122">Eingabeauswahl (Multiplexer)</span><span class="sxs-lookup"><span data-stu-id="3529c-122">Input selector (multiplexer)</span></span>
-   <span data-ttu-id="3529c-123">Lautheit-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3529c-123">Loudness control</span></span>
-   <span data-ttu-id="3529c-124">Midrange-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3529c-124">Midrange control</span></span>
-   <span data-ttu-id="3529c-125">Steuerelement stumm schalten</span><span class="sxs-lookup"><span data-stu-id="3529c-125">Mute control</span></span>
-   <span data-ttu-id="3529c-126">Ausgabe Auswahl (Demultiplexer)</span><span class="sxs-lookup"><span data-stu-id="3529c-126">Output selector (demultiplexer)</span></span>
-   <span data-ttu-id="3529c-127">Spitzen Meter</span><span class="sxs-lookup"><span data-stu-id="3529c-127">Peak meter</span></span>
-   <span data-ttu-id="3529c-128">Treble-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3529c-128">Treble control</span></span>
-   <span data-ttu-id="3529c-129">Volumesteuerung</span><span class="sxs-lookup"><span data-stu-id="3529c-129">Volume control</span></span>

<span data-ttu-id="3529c-130">Außerdem ermöglicht die devicetopology-API Clients, Adapter Geräte nach Informationen zu den von Ihnen unterstützten Streamingformaten abzufragen.</span><span class="sxs-lookup"><span data-stu-id="3529c-130">In addition, the DeviceTopology API enables clients to query adapter devices for information about the stream formats that they support.</span></span> <span data-ttu-id="3529c-131">In der Header Datei devicetopology. h sind die Schnittstellen in der devicetopology-API definiert.</span><span class="sxs-lookup"><span data-stu-id="3529c-131">The header file Devicetopology.h defines the interfaces in the DeviceTopology API.</span></span>

<span data-ttu-id="3529c-132">Das folgende Diagramm zeigt ein Beispiel für mehrere verbundene gerätetopologien für den Teil eines PCI-Adapters, der Audiodaten von einem Mikrofon, einer Zeilen Eingabe und einem CD-Player aufzeichnet.</span><span class="sxs-lookup"><span data-stu-id="3529c-132">The following diagram shows an example of several connected device topologies for the portion of a PCI adapter that captures audio from a microphone, line input, and CD player.</span></span>

![Beispiel für vier Topologien mit verbundenen Geräten](images/fig2.jpg)

<span data-ttu-id="3529c-134">Das obige Diagramm zeigt die Daten Pfade, die von den analogen Eingaben zum Systembus geleitet werden.</span><span class="sxs-lookup"><span data-stu-id="3529c-134">The preceding diagram shows the data paths that lead from the analog inputs to the system bus.</span></span> <span data-ttu-id="3529c-135">Jedes der folgenden Geräte wird als Geräte Topologieobjekt mit einer [**idevicetopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) -Schnittstelle dargestellt:</span><span class="sxs-lookup"><span data-stu-id="3529c-135">Each of the following devices is represented as a device-topology object with an [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) interface:</span></span>

-   <span data-ttu-id="3529c-136">Wave Capture-Gerät</span><span class="sxs-lookup"><span data-stu-id="3529c-136">Wave capture device</span></span>
-   <span data-ttu-id="3529c-137">Eingabe-Multiplexer-Gerät</span><span class="sxs-lookup"><span data-stu-id="3529c-137">Input multiplexer device</span></span>
-   <span data-ttu-id="3529c-138">Endpunkt Gerät A</span><span class="sxs-lookup"><span data-stu-id="3529c-138">Endpoint device A</span></span>
-   <span data-ttu-id="3529c-139">Endpunkt Gerät B</span><span class="sxs-lookup"><span data-stu-id="3529c-139">Endpoint device B</span></span>

<span data-ttu-id="3529c-140">Beachten Sie, dass im Topologiediagramm Adapter Geräte (die Wellen Erfassung und die Eingabe-Multiplexer-Geräte) mit Endpunkt Geräten kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="3529c-140">Note that the topology diagram combines adapter devices (the wave capture and input multiplexer devices) with endpoint devices.</span></span> <span data-ttu-id="3529c-141">Über die Verbindungen zwischen Geräten werden Audiodaten von einem Gerät an das nächste weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="3529c-141">Through the connections between devices, audio data passes from one device to the next.</span></span> <span data-ttu-id="3529c-142">Auf jeder Seite einer Verbindung befindet sich ein Connector (im Diagramm als "con" bezeichnet), über den Daten in ein Gerät eingegeben oder verlassen werden.</span><span class="sxs-lookup"><span data-stu-id="3529c-142">On each side of a connection is a connector (labeled Con in the diagram) through which data enters or leaves a device.</span></span>

<span data-ttu-id="3529c-143">Am linken Rand des Diagramms geben Signale von den Zeilen-und Mikrofon-Buben die Endpunkt Geräte ein.</span><span class="sxs-lookup"><span data-stu-id="3529c-143">On the left edge of the diagram, signals from the line-input and microphone jacks enter the endpoint devices.</span></span>

<span data-ttu-id="3529c-144">Innerhalb des Wave Capture-Geräts und des Eingabe-Multiplexer-Geräts handelt es sich um streamverarbeitungs Funktionen, die in der Terminologie der devicetopology-API als Untereinheiten bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="3529c-144">Inside the wave capture device and input multiplexer device are stream-processing functions, which, in the terminology of the DeviceTopology API, are called subunits.</span></span> <span data-ttu-id="3529c-145">Die folgenden Typen von Untereinheiten werden im vorangehenden Diagramm angezeigt:</span><span class="sxs-lookup"><span data-stu-id="3529c-145">The following types of subunits appear in the preceding diagram:</span></span>

-   <span data-ttu-id="3529c-146">Volumesteuerelement (mit der Bezeichnung Vol)</span><span class="sxs-lookup"><span data-stu-id="3529c-146">Volume control (labeled Vol)</span></span>
-   <span data-ttu-id="3529c-147">Stumm Steuerelement (mit der Bezeichnung stumm)</span><span class="sxs-lookup"><span data-stu-id="3529c-147">Mute control (labeled Mute)</span></span>
-   <span data-ttu-id="3529c-148">Multiplexer (oder Eingabeauswahl; mit Bezeichnung MUX)</span><span class="sxs-lookup"><span data-stu-id="3529c-148">Multiplexer (or input selector; labeled MUX)</span></span>
-   <span data-ttu-id="3529c-149">Analog zu Digital Converter (mit der Bezeichnung ADC)</span><span class="sxs-lookup"><span data-stu-id="3529c-149">Analog-to-digital converter (labeled ADC)</span></span>

<span data-ttu-id="3529c-150">Die Einstellungen in den Untereinheiten Volume, stumm und Multiplexer können von Clients gesteuert werden, und die devicetopology-API stellt Steuerungs Schnittstellen für Clients zur Steuerung bereit.</span><span class="sxs-lookup"><span data-stu-id="3529c-150">The settings in the volume, mute, and multiplexer subunits can be controlled by clients, and the DeviceTopology API provides control interfaces to clients for controlling them.</span></span> <span data-ttu-id="3529c-151">In diesem Beispiel hat die ADC-Untereinheit keine Steuerungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="3529c-151">In this example, the ADC subunit has no control settings.</span></span> <span data-ttu-id="3529c-152">Folglich bietet die API "de vicetopology" keine Steuerungs Schnittstelle für den ADC.</span><span class="sxs-lookup"><span data-stu-id="3529c-152">Thus, the DeviceTopology API provides no control interface for the ADC.</span></span>

<span data-ttu-id="3529c-153">In der Terminologie der Debug-API-API Gehören Connectors und Untereinheiten zur gleichen allgemeinen Kategorie – Parts.</span><span class="sxs-lookup"><span data-stu-id="3529c-153">In the terminology of the DeviceTopology API, connectors and subunits belong to the same general category—parts.</span></span> <span data-ttu-id="3529c-154">Alle Teile, unabhängig davon, ob es sich um Connectors oder Untereinheiten handelt, stellen einen gemeinsamen Satz von Funktionen bereit.</span><span class="sxs-lookup"><span data-stu-id="3529c-154">All parts, regardless of whether they are connectors or subunits, provide a common set of functions.</span></span> <span data-ttu-id="3529c-155">Die devicetopology-API implementiert eine [**ipart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) -Schnittstelle, die die generischen Funktionen darstellt, die von Connectors und Untereinheiten gemeinsam sind.</span><span class="sxs-lookup"><span data-stu-id="3529c-155">The DeviceTopology API implements an [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) interface to represent the generic functions that are common to connectors and subunits.</span></span> <span data-ttu-id="3529c-156">Die API implementiert die [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector) -und [**isubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit) -Schnittstellen, um die spezifischen Aspekte von Connectors und Untereinheiten darzustellen.</span><span class="sxs-lookup"><span data-stu-id="3529c-156">The API implements the [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector) and [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit) interfaces to represent the specific aspects of connectors and subunits.</span></span>

<span data-ttu-id="3529c-157">Die devicetopology-API erstellt die Topologien des Wave Capture-Geräts und des Eingabe-Multiplexer-Geräts aus den kernelstreamingfiltern, die der Audiotreiber für das Betriebssystem zur Darstellung dieser Geräte verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="3529c-157">The DeviceTopology API constructs the topologies of the wave capture device and input multiplexer device from the kernel-streaming (KS) filters that the audio driver exposes to the operating system to represent these devices.</span></span> <span data-ttu-id="3529c-158">(Der audioadaptertreiber implementiert **iminiportwavexxx** -und **iminiporttopology** -Schnittstellen, um die Hardware abhängigen Teile dieser Filter darzustellen. Weitere Informationen zu diesen Schnittstellen und zu KS-Filtern finden Sie in der Windows-DDK-Dokumentation.)</span><span class="sxs-lookup"><span data-stu-id="3529c-158">(The audio adapter driver implements **IMiniportWaveXxx** and **IMiniportTopology** interfaces to represent the hardware-dependent portions of these filters; for more information about these interfaces and about KS filters, see the Windows DDK documentation.)</span></span>

<span data-ttu-id="3529c-159">Die Debug-API erstellt triviale Topologien zur Darstellung der Endpunkt Geräte A und B im vorangehenden Diagramm.</span><span class="sxs-lookup"><span data-stu-id="3529c-159">The DeviceTopology API constructs trivial topologies to represent endpoint devices A and B in the preceding diagram.</span></span> <span data-ttu-id="3529c-160">Die Geräte Topologie eines Endpunkt Geräts besteht aus einem einzelnen Connector.</span><span class="sxs-lookup"><span data-stu-id="3529c-160">The device topology of an endpoint device consists of a single connector.</span></span> <span data-ttu-id="3529c-161">Bei dieser Topologie handelt es sich lediglich um einen Platzhalter für das Endpunktgerät, der keine Untereinheiten für die Verarbeitung von Audiodaten enthält.</span><span class="sxs-lookup"><span data-stu-id="3529c-161">This topology is merely a placeholder for the endpoint device and contains no subunits for processing audio data.</span></span> <span data-ttu-id="3529c-162">In der Tat enthalten Adapter Geräte alle Untereinheiten, die von Client Anwendungen zum Steuern der Audioverarbeitung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3529c-162">In fact, adapter devices contain all of the subunits that client applications use to control audio processing.</span></span> <span data-ttu-id="3529c-163">Die Geräte Topologie eines Endpunkt Geräts dient hauptsächlich als Ausgangspunkt für die Untersuchung der gerätetopologien von Adapter Geräten.</span><span class="sxs-lookup"><span data-stu-id="3529c-163">The device topology of an endpoint device serves primarily as a starting point for exploring the device topologies of adapter devices.</span></span>

<span data-ttu-id="3529c-164">Interne Verbindungen zwischen zwei Teilen in einer Geräte Topologie werden als Verknüpfungen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3529c-164">Internal connections between two parts in a device topology are called links.</span></span> <span data-ttu-id="3529c-165">Die devicetopology-API stellt Methoden zum Durchlaufen von Links von einem Teil zum nächsten in einer Geräte Topologie bereit.</span><span class="sxs-lookup"><span data-stu-id="3529c-165">The DeviceTopology API provides methods for traversing links from one part to the next in a device topology.</span></span> <span data-ttu-id="3529c-166">Die API bietet auch Methoden zum Durchlaufen der Verbindungen zwischen gerätetopologien.</span><span class="sxs-lookup"><span data-stu-id="3529c-166">The API also provides methods for traversing the connections between device topologies.</span></span>

<span data-ttu-id="3529c-167">Um mit der Untersuchung eines Satzes von Topologien verbundener Geräte zu beginnen, aktiviert eine Client Anwendung die **idevicetopology** -Schnittstelle eines audioendpunktgeräts.</span><span class="sxs-lookup"><span data-stu-id="3529c-167">To begin exploration of a set of connected device topologies, a client application activates the **IDeviceTopology** interface of an audio endpoint device.</span></span> <span data-ttu-id="3529c-168">Der Connector in einem Endpunkt Gerät stellt eine Verbindung mit einem Connector in einem Audioadapter oder einem Netzwerk her.</span><span class="sxs-lookup"><span data-stu-id="3529c-168">The connector in an endpoint device connects either to a connector in an audio adapter or to a network.</span></span> <span data-ttu-id="3529c-169">Wenn der Endpunkt eine Verbindung mit einem Gerät auf einem Audioadapter herstellt, ermöglichen die Methoden in der devicetopology-API der Anwendung, über die Verbindung zwischen dem Endpunkt und dem Adapter zu wechseln, indem Sie einen Verweis auf die **idevicetopology** -Schnittstelle des Adapter Geräts auf der anderen Seite der Verbindung erhalten.</span><span class="sxs-lookup"><span data-stu-id="3529c-169">If the endpoint connects to a device on an audio adapter, then the methods in the DeviceTopology API enable the application to step across the connection from the endpoint to the adapter by obtaining a reference to the **IDeviceTopology** interface of the adapter device on the other side of the connection.</span></span> <span data-ttu-id="3529c-170">Ein Netzwerk hat dagegen keine Geräte Topologie.</span><span class="sxs-lookup"><span data-stu-id="3529c-170">A network, on the other hand, has no device topology.</span></span> <span data-ttu-id="3529c-171">Eine Netzwerkverbindung leitet einen Audiostream an einen Client, der Remote auf das System zugreift.</span><span class="sxs-lookup"><span data-stu-id="3529c-171">A network connection pipes an audio stream to a client that is accessing the system remotely.</span></span>

<span data-ttu-id="3529c-172">Die devicetopology-API ermöglicht nur den Zugriff auf die Topologien der Hardware Geräte in einem Audioadapter.</span><span class="sxs-lookup"><span data-stu-id="3529c-172">The DeviceTopology API provides access only to the topologies of the hardware devices in an audio adapter.</span></span> <span data-ttu-id="3529c-173">Die externen Geräte am linken Rand des Diagramms und die Softwarekomponenten am rechten Rand überschreiten den Geltungsbereich der API.</span><span class="sxs-lookup"><span data-stu-id="3529c-173">The external devices on the left edge of the diagram and the software components on the right edge are beyond the scope of the API.</span></span> <span data-ttu-id="3529c-174">Die gestrichelten Linien auf beiden Seiten des Diagramms stellen die Grenzen der devicetopology-API dar.</span><span class="sxs-lookup"><span data-stu-id="3529c-174">The dashed lines on either side of the diagram represent the limits of the DeviceTopology API.</span></span> <span data-ttu-id="3529c-175">Der Client kann die API verwenden, um einen Dateipfad zu untersuchen, der vom Eingabe-Jack zum Systembus reicht, aber die API kann nicht über diese Grenzen hinweg durchdringen.</span><span class="sxs-lookup"><span data-stu-id="3529c-175">The client can use the API to explore a data path that stretches from the input jack to the system bus, but the API cannot penetrate beyond these boundaries.</span></span>

<span data-ttu-id="3529c-176">Jeder Connector im vorangehenden Diagramm verfügt über einen zugeordneten Verbindungstyp, der den Verbindungstyp angibt, der vom Connector hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3529c-176">Each connector in the preceding diagram has an associated connection type that indicates the type of connection that the connector makes.</span></span> <span data-ttu-id="3529c-177">Daher verfügen die Connectors auf den beiden Seiten einer Verbindung immer über identische Verbindungstypen.</span><span class="sxs-lookup"><span data-stu-id="3529c-177">Thus, the connectors on the two sides of a connection always have identical connection types.</span></span> <span data-ttu-id="3529c-178">Der Verbindungstyp wird durch einen [**ConnectorType**](/windows/win32/api/devicetopology/ne-devicetopology-connectortype) -Enumerationswert angegeben – physischer \_ externer, physischer interner, Software-Fixed, Software-e/a \_ \_ \_ oder Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="3529c-178">The connection type is indicated by a [**ConnectorType**](/windows/win32/api/devicetopology/ne-devicetopology-connectortype) enumeration value—Physical\_External, Physical\_Internal, Software\_Fixed, Software\_IO, or Network.</span></span> <span data-ttu-id="3529c-179">Die Verbindungen zwischen dem Eingabe-Multiplexer-Gerät und den Endpunkt Geräten A und B sind physischer \_ extern, d. h. die Verbindung stellt eine physische Verbindung mit einem externen Gerät dar (d. h. einen AudioJack, der vom Benutzer aufgerufen werden kann).</span><span class="sxs-lookup"><span data-stu-id="3529c-179">The connections between the input multiplexer device and endpoint devices A and B are of type Physical\_External, which means that the connection represents a physical connection to an external device (in other words, a user-accessible audio jack).</span></span> <span data-ttu-id="3529c-180">Die Verbindung mit dem analogen Signal vom internen CD-Player ist vom Typ Physical \_ internal, was eine physische Verbindung mit einem zusätzlichen Gerät angibt, das im System Chassis installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3529c-180">The connection to the analog signal from the internal CD player is of type Physical\_Internal, which indicates a physical connection to an auxiliary device that is installed inside the system chassis.</span></span> <span data-ttu-id="3529c-181">Die Verbindung zwischen dem Wave Capture-Gerät und dem Eingabe-Multiplexer-Gerät ist vom Typ "Software \_ Fixed", was auf eine permanente Verbindung hinweist, die fest ist und nicht unter der Software Steuerung konfiguriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="3529c-181">The connection between the wave capture device and input multiplexer device is of type Software\_Fixed, which indicates a permanent connection that is fixed and cannot be configured under software control.</span></span> <span data-ttu-id="3529c-182">Zum Schluss ist die Verbindung mit dem Systembus auf der rechten Seite des Diagramms vom Typ Software-e \_ /a, was darauf hinweist, dass die Daten-e/a für die Verbindung von einem DMA-Modul unter Software Steuerung implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="3529c-182">Finally, the connection to the system bus on the right side of the diagram is of type Software\_IO, which indicates that the data I/O for the connection is implemented by a DMA engine under software control.</span></span> <span data-ttu-id="3529c-183">(Das Diagramm enthält kein Beispiel für einen Netzwerk Verbindungstyp.)</span><span class="sxs-lookup"><span data-stu-id="3529c-183">(The diagram does not include an example of a Network connection type.)</span></span>

<span data-ttu-id="3529c-184">Der Client beginnt mit dem Durchlaufen eines Daten Pfads auf dem Endpunkt Gerät.</span><span class="sxs-lookup"><span data-stu-id="3529c-184">The client begins traversing a data path at the endpoint device.</span></span> <span data-ttu-id="3529c-185">Zuerst erhält der Client eine [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstelle, die das Endpunkt Gerät darstellt, wie in Auflisten von [Audiogeräten](enumerating-audio-devices.md)erläutert.</span><span class="sxs-lookup"><span data-stu-id="3529c-185">First, the client obtains an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface that represents the endpoint device, as explained in [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span> <span data-ttu-id="3529c-186">Um die **idevicetopology** -Schnittstelle für das Endpunkt Gerät abzurufen, ruft der Client die Methode " [**immdevice:: Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) " mit dem Parameter " *IID* " auf, der auf refi IID \_ idevicetopology festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3529c-186">To obtain the **IDeviceTopology** interface for the endpoint device, the client calls the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method with parameter *iid* set to REFIID IID\_IDeviceTopology.</span></span>

<span data-ttu-id="3529c-187">Im Beispiel im vorangehenden Diagramm enthält das Eingabe-Multiplexer-Gerät alle Hardware Steuerelemente (Volume, stumm und Multiplexer) für die Erfassungsdaten Ströme von den Zeilen-und Mikrofon-Buben.</span><span class="sxs-lookup"><span data-stu-id="3529c-187">In the example in the preceding diagram, the input multiplexer device contains all the hardware controls (volume, mute, and multiplexer) for the capture streams from the line-input and microphone jacks.</span></span> <span data-ttu-id="3529c-188">Im folgenden Codebeispiel wird veranschaulicht, wie Sie die **idevicetopology** -Schnittstelle für das Eingabe-Multiplexer-Gerät von der **immdevice** -Schnittstelle für das Endpunkt Gerät für die Zeilen Eingabe oder das Mikrofon abrufen:</span><span class="sxs-lookup"><span data-stu-id="3529c-188">The following code example shows how to obtain the **IDeviceTopology** interface for the input multiplexer device from the **IMMDevice** interface for the endpoint device for the line input or microphone:</span></span>


```C++
//-----------------------------------------------------------
// The input argument to this function is a pointer to the
// IMMDevice interface of an endpoint device. The function
// outputs a pointer (counted reference) to the
// IDeviceTopology interface of the adapter device that
// connects to the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IDeviceTopology = __uuidof(IDeviceTopology);
const IID IID_IPart = __uuidof(IPart);

HRESULT GetHardwareDeviceTopology(
            IMMDevice *pEndptDev,
            IDeviceTopology **ppDevTopo)
{
    HRESULT hr = S_OK;
    IDeviceTopology *pDevTopoEndpt = NULL;
    IConnector *pConnEndpt = NULL;
    IConnector *pConnHWDev = NULL;
    IPart *pPartConn = NULL;

    // Get the endpoint device's IDeviceTopology interface.

    hr = pEndptDev->Activate(
                      IID_IDeviceTopology, CLSCTX_ALL,
                      NULL, (void**)&pDevTopoEndpt);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).

    hr = pDevTopoEndpt->GetConnector(0, &pConnEndpt);
    EXIT_ON_ERROR(hr)

    // Use the connector in the endpoint device to get the
    // connector in the adapter device.

    hr = pConnEndpt->GetConnectedTo(&pConnHWDev);
    EXIT_ON_ERROR(hr)

    // Query the connector in the adapter device for
    // its IPart interface.

    hr = pConnHWDev->QueryInterface(
                         IID_IPart, (void**)&pPartConn);
    EXIT_ON_ERROR(hr)

    // Use the connector's IPart interface to get the
    // IDeviceTopology interface for the adapter device.

    hr = pPartConn->GetTopologyObject(ppDevTopo);

Exit:
    SAFE_RELEASE(pDevTopoEndpt)
    SAFE_RELEASE(pConnEndpt)
    SAFE_RELEASE(pConnHWDev)
    SAFE_RELEASE(pPartConn)

    return hr;
}
```



<span data-ttu-id="3529c-189">Die Funktion "gethardwaredevicetopology" im vorangehenden Codebeispiel führt die folgenden Schritte aus, um die **idevicetopology** -Schnittstelle für das Eingabe-Multiplexer-Gerät abzurufen:</span><span class="sxs-lookup"><span data-stu-id="3529c-189">The GetHardwareDeviceTopology function in the previous code example performs the following steps to obtain the **IDeviceTopology** interface for the input multiplexer device:</span></span>

1.  <span data-ttu-id="3529c-190">Wenden Sie die **immdevice:: Aktivierungs** -Methode an, um die **idevicetopology** -Schnittstelle für das Endpunkt Gerät abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3529c-190">Call the **IMMDevice::Activate** method to get the **IDeviceTopology** interface for the endpoint device.</span></span>
2.  <span data-ttu-id="3529c-191">Mit der im vorherigen Schritt erhaltenen **idevicetopology** -Schnittstelle können Sie die [**idevicetopology:: getconnector**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getconnector) -Methode aufrufen, um die **IConnector** -Schnittstelle des einzelnen Connector (Connector-Nummer 0) im Endpunkt Gerät abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3529c-191">With the **IDeviceTopology** interface obtained in the preceding step, call the [**IDeviceTopology::GetConnector**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getconnector) method to get the **IConnector** interface of the single connector (connector number 0) in the endpoint device.</span></span>
3.  <span data-ttu-id="3529c-192">Mit der **IConnector** -Schnittstelle, die Sie im vorherigen Schritt abgerufen haben, können Sie die [**IConnector:: getconnectedto**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getconnectedto) -Methode aufrufen, um die **IConnector** -Schnittstelle des Konnektors im Eingabe-Multiplexer-Gerät abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3529c-192">With the **IConnector** interface obtained in the preceding step, call the [**IConnector::GetConnectedTo**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getconnectedto) method to get the **IConnector** interface of the connector in the input multiplexer device.</span></span>
4.  <span data-ttu-id="3529c-193">Fragen Sie die **IConnector** -Schnittstelle ab, die im vorherigen Schritt für die **ipart** -Schnittstelle abgerufen wurde</span><span class="sxs-lookup"><span data-stu-id="3529c-193">Query the **IConnector** interface obtained in the preceding step for its **IPart** interface.</span></span>
5.  <span data-ttu-id="3529c-194">Mit der im vorherigen Schritt abzurufenden **ipart** -Schnittstelle können Sie die [**ipart:: gettopologyobject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) -Methode aufrufen, um die **idevicetopology** -Schnittstelle für das eingabemultiplexer-Gerät abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3529c-194">With the **IPart** interface obtained in the preceding step, call the [**IPart::GetTopologyObject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) method to get the **IDeviceTopology** interface for the input multiplexer device.</span></span>

<span data-ttu-id="3529c-195">Bevor der Benutzer aus dem Mikrofon im vorangehenden Diagramm aufzeichnen kann, muss die Client Anwendung sicherstellen, dass der Multiplexer die Mikrofon Eingabe auswählt.</span><span class="sxs-lookup"><span data-stu-id="3529c-195">Before the user can record from the microphone in the preceding diagram, the client application must make certain that the multiplexer selects the microphone input.</span></span> <span data-ttu-id="3529c-196">Im folgenden Codebeispiel wird gezeigt, wie ein Client den Dateipfad vom Mikrofon durchlaufen kann, bis der Multiplexer gefunden wird, der dann die Mikrofon Eingabe auswählen kann:</span><span class="sxs-lookup"><span data-stu-id="3529c-196">The following code example shows how a client can traverse the data path from the microphone until it finds the multiplexer, which it then programs to select the microphone input:</span></span>


```C++
//-----------------------------------------------------------
// The input argument to this function is a pointer to the
// IMMDevice interface for a capture endpoint device. The
// function traverses the data path that extends from the
// endpoint device to the system bus (for example, PCI)
// or external bus (USB). If the function discovers a MUX
// (input selector) in the path, it selects the MUX input
// that connects to the stream from the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IDeviceTopology = __uuidof(IDeviceTopology);
const IID IID_IPart = __uuidof(IPart);
const IID IID_IConnector = __uuidof(IConnector);
const IID IID_IAudioInputSelector = __uuidof(IAudioInputSelector);

HRESULT SelectCaptureDevice(IMMDevice *pEndptDev)
{
    HRESULT hr = S_OK;
    DataFlow flow;
    IDeviceTopology *pDeviceTopology = NULL;
    IConnector *pConnFrom = NULL;
    IConnector *pConnTo = NULL;
    IPart *pPartPrev = NULL;
    IPart *pPartNext = NULL;
    IAudioInputSelector *pSelector = NULL;

    if (pEndptDev == NULL)
    {
        EXIT_ON_ERROR(hr = E_POINTER)
    }

    // Get the endpoint device's IDeviceTopology interface.
    hr = pEndptDev->Activate(
                      IID_IDeviceTopology, CLSCTX_ALL, NULL,
                      (void**)&pDeviceTopology);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).
    hr = pDeviceTopology->GetConnector(0, &pConnFrom);
    SAFE_RELEASE(pDeviceTopology)
    EXIT_ON_ERROR(hr)

    // Make sure that this is a capture device.
    hr = pConnFrom->GetDataFlow(&flow);
    EXIT_ON_ERROR(hr)

    if (flow != Out)
    {
        // Error -- this is a rendering device.
        EXIT_ON_ERROR(hr = AUDCLNT_E_WRONG_ENDPOINT_TYPE)
    }

    // Outer loop: Each iteration traverses the data path
    // through a device topology starting at the input
    // connector and ending at the output connector.
    while (TRUE)
    {
        BOOL bConnected;
        hr = pConnFrom->IsConnected(&bConnected);
        EXIT_ON_ERROR(hr)

        // Does this connector connect to another device?
        if (bConnected == FALSE)
        {
            // This is the end of the data path that
            // stretches from the endpoint device to the
            // system bus or external bus. Verify that
            // the connection type is Software_IO.
            ConnectorType  connType;
            hr = pConnFrom->GetType(&connType);
            EXIT_ON_ERROR(hr)

            if (connType == Software_IO)
            {
                break;  // finished
            }
            EXIT_ON_ERROR(hr = E_FAIL)
        }

        // Get the connector in the next device topology,
        // which lies on the other side of the connection.
        hr = pConnFrom->GetConnectedTo(&pConnTo);
        EXIT_ON_ERROR(hr)
        SAFE_RELEASE(pConnFrom)

        // Get the connector's IPart interface.
        hr = pConnTo->QueryInterface(
                        IID_IPart, (void**)&pPartPrev);
        EXIT_ON_ERROR(hr)
        SAFE_RELEASE(pConnTo)

        // Inner loop: Each iteration traverses one link in a
        // device topology and looks for input multiplexers.
        while (TRUE)
        {
            PartType parttype;
            UINT localId;
            IPartsList *pParts;

            // Follow downstream link to next part.
            hr = pPartPrev->EnumPartsOutgoing(&pParts);
            EXIT_ON_ERROR(hr)

            hr = pParts->GetPart(0, &pPartNext);
            pParts->Release();
            EXIT_ON_ERROR(hr)

            hr = pPartNext->GetPartType(&parttype);
            EXIT_ON_ERROR(hr)

            if (parttype == Connector)
            {
                // We've reached the output connector that
                // lies at the end of this device topology.
                hr = pPartNext->QueryInterface(
                                  IID_IConnector,
                                  (void**)&pConnFrom);
                EXIT_ON_ERROR(hr)

                SAFE_RELEASE(pPartPrev)
                SAFE_RELEASE(pPartNext)
                break;
            }

            // Failure of the following call means only that
            // the part is not a MUX (input selector).
            hr = pPartNext->Activate(
                              CLSCTX_ALL,
                              IID_IAudioInputSelector,
                              (void**)&pSelector);
            if (hr == S_OK)
            {
                // We found a MUX (input selector), so select
                // the input from our endpoint device.
                hr = pPartPrev->GetLocalId(&localId);
                EXIT_ON_ERROR(hr)

                hr = pSelector->SetSelection(localId, NULL);
                EXIT_ON_ERROR(hr)

                SAFE_RELEASE(pSelector)
            }

            SAFE_RELEASE(pPartPrev)
            pPartPrev = pPartNext;
            pPartNext = NULL;
        }
    }

Exit:
    SAFE_RELEASE(pConnFrom)
    SAFE_RELEASE(pConnTo)
    SAFE_RELEASE(pPartPrev)
    SAFE_RELEASE(pPartNext)
    SAFE_RELEASE(pSelector)
    return hr;
}
```



<span data-ttu-id="3529c-197">Die devicetopology-API implementiert eine [**iaudioinputselector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector) -Schnittstelle, um einen Multiplexer (z. b. den im vorangehenden Diagramm) zu kapseln.</span><span class="sxs-lookup"><span data-stu-id="3529c-197">The DeviceTopology API implements an [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector) interface to encapsulate a multiplexer, such as the one in the preceding diagram.</span></span> <span data-ttu-id="3529c-198">(Eine [**iaudiooutputselector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector) -Schnittstelle kapselt einen Demultiplexer.) Im vorangehenden Codebeispiel fragt die innere Schleife der selectcapturedevice-Funktion jede gefundene Untereinheit ab, um zu ermitteln, ob die Untereinheit ein Multiplexer ist.</span><span class="sxs-lookup"><span data-stu-id="3529c-198">(An [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector) interface encapsulates a demultiplexer.) In the preceding code example, the inner loop of the SelectCaptureDevice function queries each subunit that it finds to discover whether the subunit is a multiplexer.</span></span> <span data-ttu-id="3529c-199">Wenn es sich bei der Teil Einheit um einen Multiplexer handelt, ruft die Funktion die [**iaudioinputselector:: setSelection**](/windows/desktop/api/Devicetopology/nf-devicetopology-iaudioinputselector-setselection) -Methode auf, um die Eingabe auszuwählen, die vom Endpunkt Gerät aus eine Verbindung mit dem Stream herstellt.</span><span class="sxs-lookup"><span data-stu-id="3529c-199">If the subunit is a multiplexer, then the function calls the [**IAudioInputSelector::SetSelection**](/windows/desktop/api/Devicetopology/nf-devicetopology-iaudioinputselector-setselection) method to select the input that connects to the stream from the endpoint device.</span></span>

<span data-ttu-id="3529c-200">Im vorangehenden Codebeispiel durchläuft jede Iterationen der äußeren Schleife eine Geräte Topologie.</span><span class="sxs-lookup"><span data-stu-id="3529c-200">In the preceding code example, each iteration of the outer loop traverses one device topology.</span></span> <span data-ttu-id="3529c-201">Beim Durchlaufen der gerätetopologien im vorangehenden Diagramm durchläuft die erste Iteration das Eingabe-Multiplexer-Gerät, und die zweite Iteration durchläuft das Wave Capture-Gerät.</span><span class="sxs-lookup"><span data-stu-id="3529c-201">When traversing the device topologies in the preceding diagram, the first iteration traverses the input multiplexer device and the second iteration traverses the wave capture device.</span></span> <span data-ttu-id="3529c-202">Die Funktion wird beendet, wenn Sie den Connector am rechten Rand des Diagramms erreicht.</span><span class="sxs-lookup"><span data-stu-id="3529c-202">The function will terminate when it reaches the connector at the right edge of the diagram.</span></span> <span data-ttu-id="3529c-203">Die Beendigung tritt auf, wenn die Funktion einen Connector mit einem Software- \_ IO-Verbindungstyp erkennt.</span><span class="sxs-lookup"><span data-stu-id="3529c-203">Termination occurs when the function detects a connector with a Software\_IO connection type.</span></span> <span data-ttu-id="3529c-204">Dieser Verbindungstyp gibt den Punkt an, an dem sich das Adapter Gerät mit dem Systembus verbindet.</span><span class="sxs-lookup"><span data-stu-id="3529c-204">This connection type identifies the point at which the adapter device connects to the system bus.</span></span>

<span data-ttu-id="3529c-205">Durch den Aufrufen der [**ipart:: getParser Type**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype) -Methode im vorangehenden Codebeispiel wird ein **iparser Type** -Enumerationswert abgerufen, der angibt, ob es sich bei dem aktuellen Teil um einen Connector oder eine Audioverarbeitungs-Untereinheit handelt.</span><span class="sxs-lookup"><span data-stu-id="3529c-205">The call to the [**IPart::GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype) method in the preceding code example obtains an **IPartType** enumeration value that indicates whether the current part is a connector or an audio-processing subunit.</span></span>

<span data-ttu-id="3529c-206">In der inneren-Schleife im vorangehenden Codebeispiel wird durch Aufrufen der [**ipart:: enumpartsoutgoing**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsoutgoing) -Methode die Verknüpfung zwischen einem Teil und dem nächsten Schritt überschritten.</span><span class="sxs-lookup"><span data-stu-id="3529c-206">The inner loop in the preceding code example steps across the link from one part to the next by calling the [**IPart::EnumPartsOutgoing**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsoutgoing) method.</span></span> <span data-ttu-id="3529c-207">(Es gibt auch eine [**ipart:: enumpartsincoming**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsincoming) -Methode, die in umgekehrter Richtung verläuft.) Diese Methode ruft ein [**ipartslist**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist) -Objekt ab, das eine Liste aller ausgehenden Teile enthält.</span><span class="sxs-lookup"><span data-stu-id="3529c-207">(There's also an [**IPart::EnumPartsIncoming**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsincoming) method for stepping in the opposite direction.) This method retrieves an [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist) object that contains a list of all the outgoing parts.</span></span> <span data-ttu-id="3529c-208">Alle Teile, die von der selectcapturedevice-Funktion in einem Erfassungsgerät erwartet werden, haben jedoch immer genau einen ausgehenden Teil.</span><span class="sxs-lookup"><span data-stu-id="3529c-208">However, any part that the SelectCaptureDevice function expects to encounter in a capture device will always have exactly one outgoing part.</span></span> <span data-ttu-id="3529c-209">Folglich fordert der nachfolgende Aufrufe von [**ipartslist:: GetPart**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getpart) immer den ersten Teil in der Liste an, Teil Nummer 0, da die Funktion annimmt, dass dies der einzige Teil in der Liste ist.</span><span class="sxs-lookup"><span data-stu-id="3529c-209">Thus, the subsequent call to [**IPartsList::GetPart**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getpart) always requests the first part in the list, part number 0, because the function assumes that this is the only part in the list.</span></span>

<span data-ttu-id="3529c-210">Wenn die selectcapturedevice-Funktion auf eine Topologie stößt, für die diese Annahme nicht gültig ist, kann die Funktion das Gerät möglicherweise nicht ordnungsgemäß konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="3529c-210">If the SelectCaptureDevice function encounters a topology for which that assumption is not valid, the function might fail to configure the device correctly.</span></span> <span data-ttu-id="3529c-211">Um einen solchen Fehler zu vermeiden, kann eine allgemeinere Version der-Funktion folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="3529c-211">To avoid such a failure, a more general-purpose version of the function might do the following:</span></span>

-   <span data-ttu-id="3529c-212">Aufrufen der [**ipartslist:: GetCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getcount) -Methode, um die Anzahl der ausgehenden Teile zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="3529c-212">Call the [**IPartsList::GetCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getcount) method to determine the number of outgoing parts.</span></span>
-   <span data-ttu-id="3529c-213">Für jeden ausgehenden Teil muss **ipartslist:: GetPart** aufgerufen werden, um zu beginnen, den Daten Pfad zu durchlaufen, der aus dem Teil resultiert.</span><span class="sxs-lookup"><span data-stu-id="3529c-213">For each outgoing part, call **IPartsList::GetPart** to begin to traverse the data path that leads from the part.</span></span>

<span data-ttu-id="3529c-214">Einige, aber nicht unbedingt alle Teile verfügen über zugeordnete Hardware Steuerelemente, die von Clients festgelegt oder festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="3529c-214">Some, but not necessarily all, parts have associated hardware controls that clients can set or get.</span></span> <span data-ttu-id="3529c-215">Ein bestimmter Teil kann keine, eine oder mehrere Hardware Steuerelemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="3529c-215">A particular part might have zero, one, or more hardware controls.</span></span> <span data-ttu-id="3529c-216">Ein Hardware Steuerelement wird durch das folgende Schnittstellen Paar dargestellt:</span><span class="sxs-lookup"><span data-stu-id="3529c-216">A hardware control is represented by the following pair of interfaces:</span></span>

-   <span data-ttu-id="3529c-217">Eine generische Steuerungs Schnittstelle ( [**icontrolinterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)), die über Methoden verfügt, die allen Hardware Steuerelementen gemeinsam sind.</span><span class="sxs-lookup"><span data-stu-id="3529c-217">A generic control interface, [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface), which has methods that are common to all hardware controls.</span></span>
-   <span data-ttu-id="3529c-218">Eine Funktions spezifische Schnittstelle (z. b. [**iaudiovolumelevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)), die die Steuerelement Parameter für einen bestimmten Typ von Hardware Steuerung (z. b. ein volumesteuerelement) verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="3529c-218">A function-specific interface (for example, [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)) that exposes the control parameters for a particular type of hardware control (for example, a volume control).</span></span>

<span data-ttu-id="3529c-219">Zum Auflisten der Hardware Steuerelemente für einen Teil ruft der Client zuerst die [**ipart:: getcontrolinterfacecount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterfacecount) -Methode auf, um die Anzahl der Hardware Steuerelemente zu ermitteln, die mit dem Teil verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="3529c-219">To enumerate the hardware controls for a part, the client first calls the [**IPart::GetControlInterfaceCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterfacecount) method to determine the number of hardware controls that are associated with the part.</span></span> <span data-ttu-id="3529c-220">Als Nächstes führt der Client eine Reihe von Aufrufen der [**ipart:: getcontrolinterface**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterface) -Methode aus, um die **icontrolinterface** -Schnittstelle für jedes Hardware Steuerelement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3529c-220">Next, the client makes a series of calls to the [**IPart::GetControlInterface**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterface) method to obtain the **IControlInterface** interface for each hardware control.</span></span> <span data-ttu-id="3529c-221">Schließlich ruft der Client die Funktions spezifische Schnittstelle für jedes Hardware Steuerelement ab, indem er die [**icontrolinterface:: getiid**](/windows/desktop/api/Devicetopology/nf-devicetopology-icontrolinterface-getiid) -Methode zum Abrufen der Schnittstellen-ID anfordert.</span><span class="sxs-lookup"><span data-stu-id="3529c-221">Finally, the client obtains the function-specific interface for each hardware control by calling the [**IControlInterface::GetIID**](/windows/desktop/api/Devicetopology/nf-devicetopology-icontrolinterface-getiid) method to obtain the interface ID.</span></span> <span data-ttu-id="3529c-222">Der Client ruft die [**ipart:: Aktivierungs**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-activate) -Methode mit dieser ID auf, um die Funktions spezifische Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3529c-222">The client calls the [**IPart::Activate**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-activate) method with this ID to obtain the function-specific interface.</span></span>

<span data-ttu-id="3529c-223">Ein Teil, bei dem es sich um einen Connector handelt, kann eine der folgenden Funktions spezifischen Steuerungs Schnittstellen unterstützen:</span><span class="sxs-lookup"><span data-stu-id="3529c-223">A part that is a connector might support one of the following function-specific control interfaces:</span></span>

-   [<span data-ttu-id="3529c-224">**"Iksformatsupport"**</span><span class="sxs-lookup"><span data-stu-id="3529c-224">**IKsFormatSupport**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)
-   [<span data-ttu-id="3529c-225">**"Iksjackdescription"**</span><span class="sxs-lookup"><span data-stu-id="3529c-225">**IKsJackDescription**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)

<span data-ttu-id="3529c-226">Ein Teil, bei dem es sich um eine Untereinheit handelt, kann eine oder mehrere der folgenden Funktions spezifischen Steuerungs Schnittstellen unterstützen:</span><span class="sxs-lookup"><span data-stu-id="3529c-226">A part that is a subunit might support one or more of the following function-specific control interfaces:</span></span>

-   [<span data-ttu-id="3529c-227">**Iaudioautogaincontrol**</span><span class="sxs-lookup"><span data-stu-id="3529c-227">**IAudioAutoGainControl**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)
-   [<span data-ttu-id="3529c-228">**Iaudiobass**</span><span class="sxs-lookup"><span data-stu-id="3529c-228">**IAudioBass**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)
-   [<span data-ttu-id="3529c-229">**Iaudiochannelconfig**</span><span class="sxs-lookup"><span data-stu-id="3529c-229">**IAudioChannelConfig**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)
-   [<span data-ttu-id="3529c-230">**Iaudioinputselector**</span><span class="sxs-lookup"><span data-stu-id="3529c-230">**IAudioInputSelector**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)
-   [<span data-ttu-id="3529c-231">**Iaudioloudness**</span><span class="sxs-lookup"><span data-stu-id="3529c-231">**IAudioLoudness**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)
-   [<span data-ttu-id="3529c-232">**Iaudiomidrange**</span><span class="sxs-lookup"><span data-stu-id="3529c-232">**IAudioMidrange**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)
-   [<span data-ttu-id="3529c-233">**Iaudiomute**</span><span class="sxs-lookup"><span data-stu-id="3529c-233">**IAudioMute**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)
-   [<span data-ttu-id="3529c-234">**Iaudiooutputselector**</span><span class="sxs-lookup"><span data-stu-id="3529c-234">**IAudioOutputSelector**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)
-   [<span data-ttu-id="3529c-235">**Iaudiopeakmeter**</span><span class="sxs-lookup"><span data-stu-id="3529c-235">**IAudioPeakMeter**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)
-   [<span data-ttu-id="3529c-236">**Iaudiotreble**</span><span class="sxs-lookup"><span data-stu-id="3529c-236">**IAudioTreble**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)
-   [<span data-ttu-id="3529c-237">**Iaudiovolumelevel**</span><span class="sxs-lookup"><span data-stu-id="3529c-237">**IAudioVolumeLevel**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)
-   [<span data-ttu-id="3529c-238">**Idevicespecificproperty**</span><span class="sxs-lookup"><span data-stu-id="3529c-238">**IDeviceSpecificProperty**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)

<span data-ttu-id="3529c-239">Ein Teil unterstützt die **idevicespecificproperty** -Schnittstelle nur dann, wenn das zugrunde liegende Hardware Steuerelement über einen gerätespezifischen Steuerelement Wert verfügt und das Steuerelement nicht durch eine andere Funktions spezifische Schnittstelle in der vorangehenden Liste dargestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3529c-239">A part supports the **IDeviceSpecificProperty** interface only if the underlying hardware control has a device-specific control value and the control cannot be adequately represented by any other function-specific interface in the preceding list.</span></span> <span data-ttu-id="3529c-240">In der Regel ist eine gerätespezifische Eigenschaft nur für einen Client nützlich, der die Bedeutung des Eigenschafts Werts aus Informationen wie z. b. dem Teiltyp, dem Part-Untertyp und dem Teilnamen ableiten kann.</span><span class="sxs-lookup"><span data-stu-id="3529c-240">Typically, a device-specific property is useful only to a client that can infer the meaning of the property value from information such as the part type, part subtype, and part name.</span></span> <span data-ttu-id="3529c-241">Der Client kann diese Informationen abrufen, indem er die Methoden [**ipart:: getparamettype**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype), [**ipart:: getsubtype**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype)und [**ipart:: GetName**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getname) anruft.</span><span class="sxs-lookup"><span data-stu-id="3529c-241">The client can obtain this information by calling the [**IPart::GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype), [**IPart::GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype), and [**IPart::GetName**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getname) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3529c-242">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3529c-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3529c-243">Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="3529c-243">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
