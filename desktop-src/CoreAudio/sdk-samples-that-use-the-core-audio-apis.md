---
description: SDK-Beispiele für die Verwendung der kernaudioapis
ms.assetid: 4460df28-a77d-4bf5-9dee-5fb69ba2ded6
title: SDK-Beispiele für die Verwendung der kernaudioapis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15eb05da5fefc22eaa0987d9996f0ddb48702158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958426"
---
# <a name="sdk-samples-that-use-the-core-audio-apis"></a><span data-ttu-id="26f9a-103">SDK-Beispiele für die Verwendung der kernaudioapis</span><span class="sxs-lookup"><span data-stu-id="26f9a-103">SDK Samples That Use the Core Audio APIs</span></span>

<span data-ttu-id="26f9a-104">Die Windows SDK enthält die folgenden Codebeispiele, die die Verwendung der kernaudioapis veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="26f9a-104">The Windows SDK includes the following code samples that demonstrate the use of the Core Audio APIs.</span></span> <span data-ttu-id="26f9a-105">Die folgenden Beispiele befinden sich im Verzeichnis% MSSDK% \\ Samples \\ Multimedia \\ Audiodatei, wobei% MSSDK% das Stammverzeichnis der Windows SDK-Installation auf Ihrem Computer ist.</span><span class="sxs-lookup"><span data-stu-id="26f9a-105">The following samples are located in the directory %MSSdk%\\samples\\multimedia\\audio, where %MSSdk% is the root directory of the Windows SDK installation on your computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26f9a-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="26f9a-106">Sample</span></span></th>
<th><span data-ttu-id="26f9a-107">Wird entschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="26f9a-107">Deascription</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26f9a-108"><a href="aecmicarray.md">Aecmicarray</a></span><span class="sxs-lookup"><span data-stu-id="26f9a-108"><a href="aecmicarray.md">AECMicArray</a></span></span></td>
<td><span data-ttu-id="26f9a-109">In diesem Beispiel werden die APIs mmdevice, WASAPI, devicetopology und endpointvolume verwendet, um einen hochwertigen sprach Datenstrom zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="26f9a-109">This sample uses the MMDevice, WASAPI, DeviceTopology, and EndpointVolume APIs to capture a high-quality voice stream.</span></span> <span data-ttu-id="26f9a-110">Das Beispiel unterstützt die Verarbeitung von Akustik Echo Abbruch (AEC) und die Verarbeitung von mikrofonarrays mithilfe des AEC-DMO, der auch als sprach Erfassungs-DSP von Microsoft bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="26f9a-110">TThe sample supports acoustic echo cancellation (AEC) and microphone array processing by using the AEC DMO also called the Voice capture DSP provided by Microsoft .</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26f9a-111"><a href="capturesharedeventdriven.md">Capturesharedebug</a></span><span class="sxs-lookup"><span data-stu-id="26f9a-111"><a href="capturesharedeventdriven.md">CaptureSharedEventDriven</a></span></span></td>
<td><span data-ttu-id="26f9a-112">Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten von einem Eingabegerät, das vom Benutzer angegeben wird, aufzuzeichnen und in einen eindeutigen Namen zu schreiben. WAV-Datei im aktuellen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="26f9a-112">This sample application uses the Core Audio APIs to capture audio data from an input device, specified by the user and writes it to a uniquely named .WAV file in the current directory.</span></span> <span data-ttu-id="26f9a-113">In diesem Beispiel wird die ereignisgesteuerte Pufferung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="26f9a-113">This sample demonstrates event-driven buffering.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26f9a-114"><a href="capturesharedtimerdriven.md">Capturesharedtimer-gesteuert</a></span><span class="sxs-lookup"><span data-stu-id="26f9a-114"><a href="capturesharedtimerdriven.md">CaptureSharedTimerDriven</a></span></span></td>
<td><span data-ttu-id="26f9a-115">Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten von einem Eingabegerät, das vom Benutzer angegeben wird, aufzuzeichnen und in einen eindeutigen Namen zu schreiben. WAV-Datei im aktuellen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="26f9a-115">This sample application uses the Core Audio APIs to capture audio data from an input device, specified by the user and writes it to a uniquely named .WAV file in the current directory.</span></span> <span data-ttu-id="26f9a-116">In diesem Beispiel wird die Zeit Geber gesteuerte Pufferung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="26f9a-116">This sample demonstrates timer-driven buffering.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26f9a-117"><a href="duckingcapturesample.md">Duckingcapturesample</a></span><span class="sxs-lookup"><span data-stu-id="26f9a-117"><a href="duckingcapturesample.md">DuckingCaptureSample</a></span></span></td>
<td><span data-ttu-id="26f9a-118">Diese Beispielanwendung veranschaulicht das Öffnen und Schließen von Kommunikationsstreams und bewirkt, dass Ducking-Ereignisse auftreten, die eine Anwendung zum Implementieren der Datenstrom Dämpfung erhalten kann.</span><span class="sxs-lookup"><span data-stu-id="26f9a-118">This sample application demonstrates opening and closing communication streams and causing ducking events that an application can get to implement stream attenuation.</span></span> <span data-ttu-id="26f9a-119">Diese Anwendung implementiert einen Chat Client, der kernaudioapis verwendet, um Audiodaten von einem Kommunikationsgerät zu lesen und auf dem Ausgabegerät wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="26f9a-119">This application implements a chat client that uses Core Audio APIs to read audio data from a communication device and to play it on the output device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26f9a-120"><a href="endpointvolume.md">Endpointvolume</a></span><span class="sxs-lookup"><span data-stu-id="26f9a-120"><a href="endpointvolume.md">EndpointVolume</a></span></span></td>
<td><span data-ttu-id="26f9a-121">Diese Beispielanwendung verwendet die kernweb-APIs, um das vom Benutzer angegebene Volume des Geräts zu ändern.</span><span class="sxs-lookup"><span data-stu-id="26f9a-121">This sample application uses the Core Audio APIs to change the volume of the device, specified by the user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26f9a-122"><a href="osd.md">OSD</a></span><span class="sxs-lookup"><span data-stu-id="26f9a-122"><a href="osd.md">OSD</a></span></span></td>
<td><span data-ttu-id="26f9a-123">Dieses Beispiel verwendet die mmdevice-und endpointvolume-APIs, um eine Bildschirm Anzeige zu implementieren, die volumeänderungen an dem Ausgabestream anzeigt, die über das standardmäßige audiorenderingendpunkt-Gerät abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="26f9a-123">This sample uses the MMDevice and EndpointVolume APIs to implement an on-screen display that shows volume changes to the output stream that plays through the default audio-rendering endpoint device.</span></span> <span data-ttu-id="26f9a-124">Die Anzeige auf dem Bildschirm wird angezeigt, wenn der Benutzer die Volumeebene im Windows-Programm zur volumesteuerung (Sndvol.exe) anpasst, und er verschwindet, wenn die Volumeebene für einen kurzen Zeitraum unverändert bleibt.</span><span class="sxs-lookup"><span data-stu-id="26f9a-124">The on-screen display appears when the user adjusts the volume level in the Windows volume-control program, Sndvol.exe, and it disappears after the volume level remains unchanged for a short period.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26f9a-125"><a href="renderexclusiveeventdriven.md">Renderexclusiveeventdriver</a></span><span class="sxs-lookup"><span data-stu-id="26f9a-125"><a href="renderexclusiveeventdriven.md">RenderExclusiveEventDriven</a></span></span></td>
<td><span data-ttu-id="26f9a-126">Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="26f9a-126">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="26f9a-127">In diesem Beispiel wird die ereignisgesteuerte Pufferung für einen renderingclient im exklusiven Modus veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="26f9a-127">This sample demonstrates event-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="26f9a-128">Für einen Stream im exklusiven Modus gibt der Client den Endpunkt Puffer mit dem Audiogerät frei.</span><span class="sxs-lookup"><span data-stu-id="26f9a-128">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26f9a-129"><a href="renderexclusivetimerdriven.md">Renderexclusivetimer-gesteuert</a></span><span class="sxs-lookup"><span data-stu-id="26f9a-129"><a href="renderexclusivetimerdriven.md">RenderExclusiveTimerDriven</a></span></span></td>
<td><span data-ttu-id="26f9a-130">Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="26f9a-130">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="26f9a-131">In diesem Beispiel wird die Zeit Geber gesteuerte Pufferung für einen renderingclient im exklusiven Modus veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="26f9a-131">This sample demonstrates timer-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="26f9a-132">Für einen Stream im exklusiven Modus gibt der Client den Endpunkt Puffer mit dem Audiogerät frei.</span><span class="sxs-lookup"><span data-stu-id="26f9a-132">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26f9a-133"><a href="rendersharedeventdriven.md">Rendersharedebug-gesteuert</a></span><span class="sxs-lookup"><span data-stu-id="26f9a-133"><a href="rendersharedeventdriven.md">RenderSharedEventDriven</a></span></span></td>
<td><span data-ttu-id="26f9a-134">Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="26f9a-134">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="26f9a-135">Dieses Beispiel veranschaulicht die ereignisgesteuerte Pufferung für einen renderingclient im freigegebenen Modus.</span><span class="sxs-lookup"><span data-stu-id="26f9a-135">This sample demonstrates event-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="26f9a-136">Bei einem Stream im freigegebenen Modus verwendet der Client den Endpunkt Puffer mit der Audioengine.</span><span class="sxs-lookup"><span data-stu-id="26f9a-136">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26f9a-137"><a href="rendersharedtimerdriven.md">Rendersharedtimer-gesteuert</a></span><span class="sxs-lookup"><span data-stu-id="26f9a-137"><a href="rendersharedtimerdriven.md">RenderSharedTimerDriven</a></span></span></td>
<td><span data-ttu-id="26f9a-138">Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="26f9a-138">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="26f9a-139">Dieses Beispiel veranschaulicht die Zeit Geber gesteuerte Pufferung für einen renderingclient im freigegebenen Modus.</span><span class="sxs-lookup"><span data-stu-id="26f9a-139">This sample demonstrates timer-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="26f9a-140">Bei einem Stream im freigegebenen Modus verwendet der Client den Endpunkt Puffer mit der Audioengine.</span><span class="sxs-lookup"><span data-stu-id="26f9a-140">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26f9a-141">Winaudiodatei</span><span class="sxs-lookup"><span data-stu-id="26f9a-141">WinAudio</span></span></td>
<td><span data-ttu-id="26f9a-142">In diesem Beispiel werden die mmdevice-API und die WASAPI verwendet, um Audiostreams wiederzugeben und zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="26f9a-142">This sample uses the MMDevice API and WASAPI to play and capture audio streams.</span></span> <span data-ttu-id="26f9a-143">Die Benutzeroberfläche dieser Beispielanwendung ermöglicht Benutzern das Auswählen von audioendpunktgeräten, das Ändern der Volumeebene der lokalen Audiositzung und das Wiedergeben von WAV-Dateien und Mikrofon Eingaben.</span><span class="sxs-lookup"><span data-stu-id="26f9a-143">The user interface of this sample application enables users to select audio endpoint devices, to change the volume level of the local audio session, and to play .wav files and microphone input.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="26f9a-144">Dieses Beispiel wurde in Windows 7 als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="26f9a-144">This sample has been deprecated in Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="26f9a-145">Sie können die Windows SDK von der [Microsoft Windows SDK Download Center](https://developer.microsoft.com/windows/downloads/sdk-archive/) -Website herunterladen.</span><span class="sxs-lookup"><span data-stu-id="26f9a-145">You can download the Windows SDK from the [Microsoft Windows SDK Download Center](https://developer.microsoft.com/windows/downloads/sdk-archive/) website.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26f9a-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="26f9a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26f9a-147">Informationen zu den Windows Core-audioapis</span><span class="sxs-lookup"><span data-stu-id="26f9a-147">About the Windows Core Audio APIs</span></span>](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




