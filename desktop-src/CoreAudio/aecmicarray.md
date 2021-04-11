---
description: In diesem Beispiel werden die Kern-audioapis verwendet, um einen hochwertigen voicewaystream zu erfassen. Das Beispiel unterstützt die Verwendung von AEC (Akustik Echo Abbruch) und die Verarbeitung von mikrofonarrays mithilfe des AEC-DMO, auch als sprach Erfassungs-DSP bezeichnet von Microsoft.
ms.assetid: 932d3442-1beb-4938-9382-031c61cd9b05
title: Aecmicarray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe72351b9f8f61d939a9f73eaf85022d7f487bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127677"
---
# <a name="aecmicarray"></a><span data-ttu-id="75719-104">Aecmicarray</span><span class="sxs-lookup"><span data-stu-id="75719-104">AECMicArray</span></span>

<span data-ttu-id="75719-105">In diesem Beispiel werden die Kern-audioapis verwendet, um einen hochwertigen voicewaystream zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="75719-105">This sample uses the Core Audio APIs to capture a high-quality voice stream.</span></span> <span data-ttu-id="75719-106">Das Beispiel unterstützt die Verwendung von AEC (Akustik Echo Abbruch) und die Verarbeitung von mikrofonarrays mithilfe des AEC-DMO, auch als sprach Erfassungs-DSP bezeichnet von Microsoft.</span><span class="sxs-lookup"><span data-stu-id="75719-106">The sample supports acoustic echo cancellation (AEC) and microphone array processing by using the AEC DMO, also called the Voice capture DSP, provided by Microsoft .</span></span>

<span data-ttu-id="75719-107">In diesem Thema werden die folgenden Abschnitte behandelt.</span><span class="sxs-lookup"><span data-stu-id="75719-107">This topic containes the following sections.</span></span>

-   [<span data-ttu-id="75719-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75719-108">Description</span></span>](#description)
-   [<span data-ttu-id="75719-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75719-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="75719-110">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="75719-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="75719-111">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="75719-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="75719-112">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="75719-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="75719-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="75719-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="75719-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75719-114">Description</span></span>

<span data-ttu-id="75719-115">In diesem Beispiel werden die folgenden Funktionen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="75719-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="75719-116">[Mmdevice](mmdevice-api.md) für die Enumeration und Auswahl von Multimedia-Geräten.</span><span class="sxs-lookup"><span data-stu-id="75719-116">[MMDevice](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="75719-117">[WASAPI](wasapi.md) für streamverwaltungsvorgänge wie das Starten und Beenden des Streams, streamumschaltung.</span><span class="sxs-lookup"><span data-stu-id="75719-117">[WASAPI](wasapi.md) for stream management operations such as starting and stopping the stream, stream switching.</span></span>
-   <span data-ttu-id="75719-118">" [Opvicetopology](devicetopology-api.md) " zum Auflisten von audioadaptern.</span><span class="sxs-lookup"><span data-stu-id="75719-118">[DeviceTopology](devicetopology-api.md) for enumerating audio adapters.</span></span>
-   <span data-ttu-id="75719-119">[Endpointvolume](endpointvolume-api.md) steuern Sie die volumeebenen von [audiositzungen](audio-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="75719-119">[EndpointVolume](endpointvolume-api.md) control the volume levels of [audio sessions](audio-sessions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="75719-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75719-120">Requirements</span></span>



| <span data-ttu-id="75719-121">Produkt</span><span class="sxs-lookup"><span data-stu-id="75719-121">Product</span></span>                                                        | <span data-ttu-id="75719-122">Version</span><span class="sxs-lookup"><span data-stu-id="75719-122">Version</span></span>                     |
|----------------------------------------------------------------|-----------------------------|
| [<span data-ttu-id="75719-123">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="75719-123">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="75719-124">Windows Vista oder höher</span><span class="sxs-lookup"><span data-stu-id="75719-124">Windows Vista or later</span></span>      |
| <span data-ttu-id="75719-125">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="75719-125">Visual Studio</span></span>                                                  | <span data-ttu-id="75719-126">2005 (nicht-Express-Editionen)</span><span class="sxs-lookup"><span data-stu-id="75719-126">2005 (non-express editions)</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="75719-127">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="75719-127">Downloading the Sample</span></span>

<span data-ttu-id="75719-128">Dieses Beispiel ist in den folgenden Speicherorten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="75719-128">This sample is available in the following locations.</span></span>



| <span data-ttu-id="75719-129">Standort</span><span class="sxs-lookup"><span data-stu-id="75719-129">Location</span></span>    | <span data-ttu-id="75719-130">Pfad/URL</span><span class="sxs-lookup"><span data-stu-id="75719-130">Path/URL</span></span>                                                                                     |
|-------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="75719-131">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="75719-131">Windows SDK</span></span> | <span data-ttu-id="75719-132">\\Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ \\ audioaecmicarray \\ ...</span><span class="sxs-lookup"><span data-stu-id="75719-132">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\AECMicArray\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="75719-133">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="75719-133">Building the Sample</span></span>

<span data-ttu-id="75719-134">Um das aecsdkdemo-Beispiel zu erstellen, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="75719-134">To build the AecSDKDemo sample, use the following steps:</span></span>

1.  <span data-ttu-id="75719-135">Öffnen Sie ein SDK-Befehlsfenster.</span><span class="sxs-lookup"><span data-stu-id="75719-135">Open an SDK command window.</span></span>
2.  <span data-ttu-id="75719-136">Geben Sie **CD% MSSDK% \\ Setup** ein.</span><span class="sxs-lookup"><span data-stu-id="75719-136">Type **cd %MSSDK%\\Setup**.</span></span>
3.  <span data-ttu-id="75719-137">Führen Sie VCIntegrate.exe aus.</span><span class="sxs-lookup"><span data-stu-id="75719-137">Run VCIntegrate.exe.</span></span>

    <span data-ttu-id="75719-138">Ab diesem Zeitpunkt verfügen Befehlsfenster über die richtigen Umgebungseinstellungen zum Erstellen einer Anwendung, die das SDK nutzt.</span><span class="sxs-lookup"><span data-stu-id="75719-138">From this point forward, command windows will have the proper environment settings to build an application that takes advantage of the SDK.</span></span>

4.  <span data-ttu-id="75719-139">Erstellen Sie das Beispiel.</span><span class="sxs-lookup"><span data-stu-id="75719-139">Build the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="75719-140">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="75719-140">Running the Sample</span></span>

<span data-ttu-id="75719-141">Wenn Sie die Demoanwendung erfolgreich erstellen, wird eine ausführbare Datei AecSDKDemo.exe generiert.</span><span class="sxs-lookup"><span data-stu-id="75719-141">If you build the demo application successfully, an executable file, AecSDKDemo.exe is generated.</span></span> <span data-ttu-id="75719-142">Um es auszuführen, geben Sie `AecSDKDemo` in ein Befehlsfenster ein, gefolgt von den erforderlichen oder optionalen Argumenten, wie unten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="75719-142">To run it, type `AecSDKDemo` in a command window followed by required or optional arguments as described below.</span></span>

`AecSDKDemo -out mic_out.pcm -mod system_mode [-option value] `

<span data-ttu-id="75719-143">In der folgenden Tabelle werden die Argumente angezeigt.</span><span class="sxs-lookup"><span data-stu-id="75719-143">The following table shows the arguments.</span></span>

| <span data-ttu-id="75719-144">Argument</span><span class="sxs-lookup"><span data-stu-id="75719-144">Argument</span></span>  | <span data-ttu-id="75719-145">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75719-145">Description</span></span>                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75719-146">-out</span><span class="sxs-lookup"><span data-stu-id="75719-146">-out</span></span>      | <span data-ttu-id="75719-147">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="75719-147">Required.</span></span> <span data-ttu-id="75719-148">Gibt den Ausgabe Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="75719-148">Specifies output file name.</span></span>                                                                                                 |
| <span data-ttu-id="75719-149">-mod</span><span class="sxs-lookup"><span data-stu-id="75719-149">-mod</span></span>      | <span data-ttu-id="75719-150">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="75719-150">Required.</span></span> <span data-ttu-id="75719-151">Gibt den System Modus für die sprach Erfassung an.</span><span class="sxs-lookup"><span data-stu-id="75719-151">Specifies voice capture system mode.</span></span> <span data-ttu-id="75719-152">Ausführliche Informationen finden Sie im Abschnitt "Konfigurieren des sprach Erfassungs-DMO" in der Beispiel-Info.</span><span class="sxs-lookup"><span data-stu-id="75719-152">Refer to "Configuring the voice capture DMO" section in the sample readme for details.</span></span> |
| <span data-ttu-id="75719-153">-feat</span><span class="sxs-lookup"><span data-stu-id="75719-153">-feat</span></span>     | <span data-ttu-id="75719-154">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="75719-154">Optional.</span></span> <span data-ttu-id="75719-155">Aktiviert den Funktionsmodus (1) oder deaktiviert (0).</span><span class="sxs-lookup"><span data-stu-id="75719-155">Turns feature mode on (1) or off (0).</span></span>                                                                                       |
| <span data-ttu-id="75719-156">-NS</span><span class="sxs-lookup"><span data-stu-id="75719-156">-ns</span></span>       | <span data-ttu-id="75719-157">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="75719-157">Optional.</span></span> <span data-ttu-id="75719-158">Wandelt die Rauschunterdrückung um (1) oder Off (0).</span><span class="sxs-lookup"><span data-stu-id="75719-158">Turns noise suppression on (1) or off (0).</span></span> <span data-ttu-id="75719-159">Der Funktionsmodus muss auf ON festgelegt sein, um dies anzugeben.</span><span class="sxs-lookup"><span data-stu-id="75719-159">Feature mode must be on for specifying this.</span></span>                                     |
| <span data-ttu-id="75719-160">-AGC</span><span class="sxs-lookup"><span data-stu-id="75719-160">-agc</span></span>      | <span data-ttu-id="75719-161">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="75719-161">Optional.</span></span> <span data-ttu-id="75719-162">Wandelt Digital AGC um (1) oder Off (0).</span><span class="sxs-lookup"><span data-stu-id="75719-162">Turns digital AGC on (1) or off (0).</span></span> <span data-ttu-id="75719-163">Der Funktionsmodus muss auf ON festgelegt sein, um dies anzugeben.</span><span class="sxs-lookup"><span data-stu-id="75719-163">Feature mode must be on for specifying this.</span></span>                                           |
| <span data-ttu-id="75719-164">-cntrclip</span><span class="sxs-lookup"><span data-stu-id="75719-164">-cntrclip</span></span> | <span data-ttu-id="75719-165">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="75719-165">Optional.</span></span> <span data-ttu-id="75719-166">Schaltet die zentrale Clipping (1) oder Off (0) ein.</span><span class="sxs-lookup"><span data-stu-id="75719-166">Turns center clipping on (1) or off (0).</span></span> <span data-ttu-id="75719-167">Der Funktionsmodus muss auf ON festgelegt sein, um dies anzugeben.</span><span class="sxs-lookup"><span data-stu-id="75719-167">Feature mode must be on for specifying this.</span></span>                                       |
| <span data-ttu-id="75719-168">-spkdev</span><span class="sxs-lookup"><span data-stu-id="75719-168">-spkdev</span></span>   | <span data-ttu-id="75719-169">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="75719-169">Optional.</span></span> <span data-ttu-id="75719-170">Gibt den sprechergeräteindex an.</span><span class="sxs-lookup"><span data-stu-id="75719-170">Specifies speaker device index.</span></span> <span data-ttu-id="75719-171">Wenn nicht angegeben, wird der Benutzer aufgefordert, auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="75719-171">If not specified, the user will be asked to select.</span></span>                                         |
| <span data-ttu-id="75719-172">-micdev</span><span class="sxs-lookup"><span data-stu-id="75719-172">-micdev</span></span>   | <span data-ttu-id="75719-173">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="75719-173">Optional.</span></span> <span data-ttu-id="75719-174">Gibt den Mikrofon-Geräte Index an.</span><span class="sxs-lookup"><span data-stu-id="75719-174">Specifies microphone device index.</span></span> <span data-ttu-id="75719-175">Wenn nicht angegeben, wird der Benutzer aufgefordert, auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="75719-175">If not specified, the user will be asked to select.</span></span>                                      |
| <span data-ttu-id="75719-176">-Dauer</span><span class="sxs-lookup"><span data-stu-id="75719-176">-duration</span></span> | <span data-ttu-id="75719-177">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="75719-177">Optional.</span></span> <span data-ttu-id="75719-178">Gibt an, wie lange die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75719-178">Specifies how long the application runs.</span></span>                                                                                    |



 

<span data-ttu-id="75719-179">In dieser Beispielanwendung werden keine Signale abgespielt.</span><span class="sxs-lookup"><span data-stu-id="75719-179">This sample application does not play any signals.</span></span> <span data-ttu-id="75719-180">Um die Demo ordnungsgemäß für AEC-aktivierte Modi (Modus 0 und 4) auszuführen, müssen Benutzer einige Audiosignale über das für den DMO angegebene sprechende Gerät (d. h. das Gerät, das durch die Option "-spkdev" angegeben wird) abspielen, das die bidirektionale Stimme in einem bidirektionalen Chat Szenario simuliert.</span><span class="sxs-lookup"><span data-stu-id="75719-180">To run the demo properly for AEC enabled modes (mode 0 and 4), users must play some audio signals through the same speaker device specified for the DMO (that is, the device specified by the "-spkdev" option), which simulates the far-end voice in a two-way chatting scenario.</span></span> <span data-ttu-id="75719-181">Benutzer können beliebige Audiosignale mit jedem beliebigen Player abspielen.</span><span class="sxs-lookup"><span data-stu-id="75719-181">Users can use any player to play any audio signals.</span></span> <span data-ttu-id="75719-182">Wenn auf dem ausgewählten Redner Gerät kein aktiver Rendering-Stream vorhanden ist, kann der DMO nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="75719-182">If there is no active render stream on the selected speaker device, the DMO will fail to process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75719-183">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="75719-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75719-184">SDK-Beispiele für die Verwendung der kernaudioapis</span><span class="sxs-lookup"><span data-stu-id="75719-184">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



