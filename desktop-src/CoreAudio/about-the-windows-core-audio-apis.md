---
description: Informationen zu den Windows Core-audioapis
ms.assetid: 657cf75f-3d72-4a5f-ae29-299e826b2b86
title: Informationen zu den Windows Core-audioapis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30763d70bae4340436145a303763c0aad57171f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861695"
---
# <a name="about-the-windows-core-audio-apis"></a><span data-ttu-id="bce25-103">Informationen zu den Windows Core-audioapis</span><span class="sxs-lookup"><span data-stu-id="bce25-103">About the Windows Core Audio APIs</span></span>

<span data-ttu-id="bce25-104">Diese Dokumentation enthält Informationen zu den Kerncode-APIs für die Microsoft Windows-Betriebssystem Familie.</span><span class="sxs-lookup"><span data-stu-id="bce25-104">This documentation provides information about Core Audio APIs for the Microsoft Windows family of operating systems.</span></span>

<span data-ttu-id="bce25-105">Die Kern-audioapis wurden in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="bce25-105">The Core Audio APIs were introduced in Windows Vista.</span></span> <span data-ttu-id="bce25-106">Dies ist ein neuer Satz von Audiokomponenten im Benutzermodus, der Client Anwendungen verbesserte Audiofunktionen bietet.</span><span class="sxs-lookup"><span data-stu-id="bce25-106">This is a new set of user-mode audio components provides client applications with improved audio capabilities.</span></span> <span data-ttu-id="bce25-107">Diese Funktionen umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="bce25-107">These capabilities include the following:</span></span>

-   <span data-ttu-id="bce25-108">Geringe Latenz, gleitrobustes Audiostreaming.</span><span class="sxs-lookup"><span data-stu-id="bce25-108">Low-latency, glitch-resilient audio streaming.</span></span>
-   <span data-ttu-id="bce25-109">Verbesserte Zuverlässigkeit (viele Audiofunktionen wurden vom Kernel Modus in den Benutzermodus verschoben).</span><span class="sxs-lookup"><span data-stu-id="bce25-109">Improved reliability (many audio functions have moved from kernel mode to user mode).</span></span>
-   <span data-ttu-id="bce25-110">Verbesserte Sicherheit (die Verarbeitung geschützter Audioinhalte findet in einem sicheren Prozess mit niedrigerer Berechtigung statt).</span><span class="sxs-lookup"><span data-stu-id="bce25-110">Improved security (processing of protected audio content takes place in a secure, lower-privilege process).</span></span>
-   <span data-ttu-id="bce25-111">Zuweisung von bestimmten systemweiten Rollen (Konsole, Multimedia und Kommunikation) zu einzelnen Audiogeräten.</span><span class="sxs-lookup"><span data-stu-id="bce25-111">Assignment of particular system-wide roles (console, multimedia, and communications) to individual audio devices.</span></span>
-   <span data-ttu-id="bce25-112">Software Abstraktion der audioendpunktgeräte (z. b. Sprecher, Kopfhörer und Mikrofone), die der Benutzer direkt bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="bce25-112">Software abstraction of the audio endpoint devices (for example, speakers, headphones, and microphones) that the user manipulates directly.</span></span>

<span data-ttu-id="bce25-113">Die Kern-audioapis wurden in Windows 7 verbessert.</span><span class="sxs-lookup"><span data-stu-id="bce25-113">The Core Audio APIs have been improved in Windows 7.</span></span> <span data-ttu-id="bce25-114">Weitere Informationen zu den Verbesserungen und neuen Features finden Sie unter [What es New for Core audioapis in Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md).</span><span class="sxs-lookup"><span data-stu-id="bce25-114">For more information about the improvements and new features added, see [What's New for Core Audio APIs in Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md).</span></span>

<span data-ttu-id="bce25-115">In dieser Dokumentation werden die Kern-API-APIs beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bce25-115">This documentation describes the Core Audio APIs.</span></span> <span data-ttu-id="bce25-116">Diese APIs dienen als Grundlage für die folgenden APIs auf höherer Ebene:</span><span class="sxs-lookup"><span data-stu-id="bce25-116">These APIs serve as the foundation for the following higher-level APIs:</span></span>

-   <span data-ttu-id="bce25-117">DirectSound</span><span class="sxs-lookup"><span data-stu-id="bce25-117">DirectSound</span></span>
-   <span data-ttu-id="bce25-118">DirectMusic</span><span class="sxs-lookup"><span data-stu-id="bce25-118">DirectMusic</span></span>
-   <span data-ttu-id="bce25-119">Windows Multimedia **wavexxx** -und **mixerxxx** -Funktionen</span><span class="sxs-lookup"><span data-stu-id="bce25-119">Windows multimedia **waveXxx** and **mixerXxx** functions</span></span>
-   <span data-ttu-id="bce25-120">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bce25-120">Media Foundation</span></span>

<span data-ttu-id="bce25-121">Diese APIs auf höherer Ebene verwenden die Kerndatei-APIs, um den Zugriff auf Audiogeräte freizugeben.</span><span class="sxs-lookup"><span data-stu-id="bce25-121">These higher-level APIs use the Core Audio APIs to share access to audio devices.</span></span> <span data-ttu-id="bce25-122">Media Foundation in Windows Vista neu ist, während die Funktionen DirectSound, DirectMusic und **wavexxx** und **mixerxxx** in Windows 98, Windows Millennium Edition und Windows 2000 und höher unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="bce25-122">Media Foundation is new with Windows Vista, whereas DirectSound, DirectMusic, and the **waveXxx** and **mixerXxx** functions are supported in Windows 98, Windows Millennium Edition, and in Windows 2000 and later.</span></span>

<span data-ttu-id="bce25-123">Die meisten Audioanwendungen kommunizieren mit den APIs auf höherer Ebene, anstatt direkt mit den Kerncode-APIs zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="bce25-123">Most audio applications communicate with the higher-level APIs instead of communicating directly with the Core Audio APIs.</span></span> <span data-ttu-id="bce25-124">Einige Beispiele für Anwendungen, die APIs höherer Ebene verwenden, sind:</span><span class="sxs-lookup"><span data-stu-id="bce25-124">Some examples of applications that use higher-level APIs are:</span></span>

-   <span data-ttu-id="bce25-125">Media Player</span><span class="sxs-lookup"><span data-stu-id="bce25-125">Media players</span></span>
-   <span data-ttu-id="bce25-126">DVD-Player</span><span class="sxs-lookup"><span data-stu-id="bce25-126">DVD players</span></span>
-   <span data-ttu-id="bce25-127">Spiele</span><span class="sxs-lookup"><span data-stu-id="bce25-127">Games</span></span>
-   <span data-ttu-id="bce25-128">Geschäftsanwendungen, wie z. b. Microsoft Office PowerPoint, die Sounddateien abspielen</span><span class="sxs-lookup"><span data-stu-id="bce25-128">Business applications, such as Microsoft Office PowerPoint, that play sound files</span></span>

<span data-ttu-id="bce25-129">In der Regel kommunizieren diese Anwendungen mit den DirectSound-oder Media Foundation-APIs.</span><span class="sxs-lookup"><span data-stu-id="bce25-129">Typically, these applications communicate with the DirectSound or Media Foundation APIs.</span></span>

<span data-ttu-id="bce25-130">Die direkte Kommunikation mit den kernaudioapis eignet sich möglicherweise nicht für viele allgemeine Audioanwendungen.</span><span class="sxs-lookup"><span data-stu-id="bce25-130">Direct communication with the Core Audio APIs might not be suitable for many general-purpose audio applications.</span></span> <span data-ttu-id="bce25-131">Beispielsweise erfordern die Kern-audioapis Audiostreams, um die nativen Datenformate eines Audiogeräts zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="bce25-131">For example, the Core Audio APIs require audio streams to use an audio device's native data formats.</span></span> <span data-ttu-id="bce25-132">Softwareentwickler von Drittanbietern, die die folgenden Produkttypen entwickeln, benötigen jedoch möglicherweise die speziellen Funktionen der kernaudioapis:</span><span class="sxs-lookup"><span data-stu-id="bce25-132">However, third-party software developers who are developing the following types of products might require the special capabilities of the Core Audio APIs:</span></span>

-   <span data-ttu-id="bce25-133">Professionelle Audioanwendungen ("pro-Audiodatei")</span><span class="sxs-lookup"><span data-stu-id="bce25-133">Professional audio ("pro audio") applications</span></span>
-   <span data-ttu-id="bce25-134">Echtzeitkommunikation (RTC)-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="bce25-134">Real-time communication (RTC) applications</span></span>
-   <span data-ttu-id="bce25-135">Audioapis von Drittanbietern</span><span class="sxs-lookup"><span data-stu-id="bce25-135">Third-party audio APIs</span></span>

<span data-ttu-id="bce25-136">Eine "pro-Audiodatei" oder RTC-Anwendung benötigt möglicherweise direkten Zugriff auf die Low-Level-Funktionen der kernaudioapis, um eine minimale Latenz zu erzielen, indem exklusiver Zugriff auf Audiohardware erhalten wird.</span><span class="sxs-lookup"><span data-stu-id="bce25-136">A "pro audio" or RTC application might need direct access to the low-level features of the Core Audio APIs to achieve minimum latency by obtaining exclusive access to audio hardware.</span></span> <span data-ttu-id="bce25-137">Für eine audioapi von Drittanbietern ist möglicherweise direkter Zugriff auf die Kerndatei-APIs erforderlich, um eine Reihe von Features zu implementieren, die von einer einzelnen, in Windows bereitgestellten audioapi mit hoher Ebene möglicherweise nicht vollständig unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="bce25-137">A third-party audio API might require direct access to the Core Audio APIs to implement a set of features that might not be entirely supported by any single high-level audio API that is supplied with Windows.</span></span>

<span data-ttu-id="bce25-138">Eine Anwendung, die eine Legacy-audioapi zum Abspielen oder Aufzeichnen von Audiodaten verwendet, erfordert möglicherweise zusätzliche Funktionen, die von der Legacy-audioapi nicht unterstützt werden, aber von den kernaudioapis unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="bce25-138">An application that uses a legacy audio API to play or record audio might require additional capabilities that are not supported by the legacy audio API, but that are supported by the Core Audio APIs.</span></span> <span data-ttu-id="bce25-139">In vielen Fällen kann die Anwendung direkt über die wichtigsten audioapis auf diese Funktionen zugreifen, die in Verbindung mit der Legacy-audioapi verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="bce25-139">In many cases, the application can access these capabilities directly through the Core Audio APIs, which can be used in conjunction with the legacy audio API.</span></span>

<span data-ttu-id="bce25-140">Die Kern-audioapis lauten:</span><span class="sxs-lookup"><span data-stu-id="bce25-140">The Core Audio APIs are:</span></span>

-   <span data-ttu-id="bce25-141">[API für Multimedia-Geräte (mmdevice)](mmdevice-api.md).</span><span class="sxs-lookup"><span data-stu-id="bce25-141">[Multimedia Device (MMDevice) API](mmdevice-api.md).</span></span> <span data-ttu-id="bce25-142">Clients verwenden diese API, um die audioendpunktgeräte im System aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="bce25-142">Clients use this API to enumerate the audio endpoint devices in the system.</span></span>
-   <span data-ttu-id="bce25-143">[Windows-audiositzungs-API (WASAPI)](wasapi.md).</span><span class="sxs-lookup"><span data-stu-id="bce25-143">[Windows Audio Session API (WASAPI)](wasapi.md).</span></span> <span data-ttu-id="bce25-144">Clients verwenden diese API, um audiodatenstreams zu und von audioendpunktgeräten zu erstellen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="bce25-144">Clients use this API to create and manage audio streams to and from audio endpoint devices.</span></span>
-   <span data-ttu-id="bce25-145">Die Geräte-API (Debug- [API](devicetopology-api.md)).</span><span class="sxs-lookup"><span data-stu-id="bce25-145">[DeviceTopology API](devicetopology-api.md).</span></span> <span data-ttu-id="bce25-146">Clients verwenden diese API, um direkt auf die topologischen Features zuzugreifen (z. b. volumesteuerelemente und Multiplexer), die sich auf den Daten Pfaden innerhalb von Hardware Geräten in audioadaptern befinden.</span><span class="sxs-lookup"><span data-stu-id="bce25-146">Clients use this API to directly access the topological features (for example, volume controls and multiplexers) that lie along the data paths inside hardware devices in audio adapters.</span></span>
-   <span data-ttu-id="bce25-147">[Endpointvolume-API](endpointvolume-api.md).</span><span class="sxs-lookup"><span data-stu-id="bce25-147">[EndpointVolume API](endpointvolume-api.md).</span></span> <span data-ttu-id="bce25-148">Clients verwenden diese API, um direkt auf die volumesteuerelemente auf audioendpunktgeräten zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="bce25-148">Clients use this API to directly access the volume controls on audio endpoint devices.</span></span> <span data-ttu-id="bce25-149">Diese API wird hauptsächlich von Anwendungen verwendet, die Audiostreams im exklusiven Modus verwalten.</span><span class="sxs-lookup"><span data-stu-id="bce25-149">This API is primarily used by applications that manage exclusive-mode audio streams.</span></span>

<span data-ttu-id="bce25-150">Diese APIs unterstützen das benutzerfreundliche Konzept eines Endpunkt Geräts, das in [audioendpunktgeräten](audio-endpoint-devices.md)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="bce25-150">These APIs support the user-friendly notion of an endpoint device, which is described in [Audio Endpoint Devices](audio-endpoint-devices.md).</span></span>

<span data-ttu-id="bce25-151">Microsoft plant nicht, die hier beschriebenen kernaudioapis für die Verwendung mit früheren Versionen von Windows, einschließlich Microsoft Windows Server 2003, Windows XP, Windows Millennium Edition, Windows 2000 und Windows 98, bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="bce25-151">Microsoft does not plan to make the Core Audio APIs that are described here available for use with earlier versions of Windows, including Microsoft Windows Server 2003, Windows XP, Windows Millennium Edition, Windows 2000, and Windows 98.</span></span>

<span data-ttu-id="bce25-152">Diese Übersicht enthält die folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="bce25-152">This overview contains the following topics.</span></span>



| <span data-ttu-id="bce25-153">**Thema**</span><span class="sxs-lookup"><span data-stu-id="bce25-153">**Topic**</span></span>                                                                                      | <span data-ttu-id="bce25-154">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bce25-154">**Description**</span></span>                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bce25-155">Neuerungen bei den Kerncode-APIs in Windows 7</span><span class="sxs-lookup"><span data-stu-id="bce25-155">What's New for Core Audio APIs in Windows 7</span></span>](what-s-new-for-core-audio-apis-in-windows-7.md) | <span data-ttu-id="bce25-156">Fasst die neuen Features und die Verbesserungen der kernaudioapis zusammen</span><span class="sxs-lookup"><span data-stu-id="bce25-156">Summarizes the new features and the improvements to the Core Audio APIs</span></span>                   |
| [<span data-ttu-id="bce25-157">Header Dateien und System Komponenten</span><span class="sxs-lookup"><span data-stu-id="bce25-157">Header Files and System Components</span></span>](header-files-and-system-components.md)                   | <span data-ttu-id="bce25-158">Beschreibt die Header Dateien und Systemkomponenten für die Kerndatei-APIs.</span><span class="sxs-lookup"><span data-stu-id="bce25-158">Describes the header files and system components for the Core Audio APIs.</span></span>                 |
| [<span data-ttu-id="bce25-159">SDK-Beispiele für die Verwendung der kernaudioapis</span><span class="sxs-lookup"><span data-stu-id="bce25-159">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)       | <span data-ttu-id="bce25-160">Listet die Beispiele in den Windows SDK auf, die die Kern-audioapis verwenden.</span><span class="sxs-lookup"><span data-stu-id="bce25-160">Lists the samples in the Windows SDK that use the Core Audio APIs.</span></span>                        |




 

## <a name="related-topics"></a><span data-ttu-id="bce25-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bce25-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bce25-162">Kernaudioapis</span><span class="sxs-lookup"><span data-stu-id="bce25-162">Core Audio APIs</span></span>](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



