---
description: Diese Beispielanwendung, die die ereignisgesteuerte Pufferung veranschaulicht, verwendet die Core Audio-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu rendern.
ms.assetid: 3a2e3fa6-2d6a-4ab0-a531-d1c968458e96
title: RenderExclusiveEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75553496219d0a4ddaf6685089de802e034f94cb
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405133"
---
# <a name="renderexclusiveeventdriven"></a><span data-ttu-id="dea2d-103">RenderExclusiveEventDriven</span><span class="sxs-lookup"><span data-stu-id="dea2d-103">RenderExclusiveEventDriven</span></span>

<span data-ttu-id="dea2d-104">Diese Beispielanwendung verwendet die Core Audio-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu rendern.</span><span class="sxs-lookup"><span data-stu-id="dea2d-104">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="dea2d-105">In diesem Beispiel wird die ereignisgesteuerte Pufferung für einen Renderingclient im exklusiven Modus veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="dea2d-105">This sample demonstrates event-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="dea2d-106">Für einen Stream im exklusiven Modus teilt sich der Client den Endpunktpuffer mit dem Audiogerät.</span><span class="sxs-lookup"><span data-stu-id="dea2d-106">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span>

<span data-ttu-id="dea2d-107">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="dea2d-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="dea2d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dea2d-108">Description</span></span>](#description)
-   [<span data-ttu-id="dea2d-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dea2d-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="dea2d-110">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="dea2d-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="dea2d-111">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="dea2d-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="dea2d-112">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="dea2d-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="dea2d-113">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="dea2d-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="dea2d-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dea2d-114">Description</span></span>

<span data-ttu-id="dea2d-115">In diesem Beispiel werden die folgenden Features veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="dea2d-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="dea2d-116">[MMDevice-API](mmdevice-api.md) für multimediale Geräteenumeration und -auswahl.</span><span class="sxs-lookup"><span data-stu-id="dea2d-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="dea2d-117">WASAPI für Datenstromverwaltungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="dea2d-117">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="dea2d-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="dea2d-118">Requirements</span></span>



| <span data-ttu-id="dea2d-119">Produkt</span><span class="sxs-lookup"><span data-stu-id="dea2d-119">Product</span></span>                                                        | <span data-ttu-id="dea2d-120">Version</span><span class="sxs-lookup"><span data-stu-id="dea2d-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="dea2d-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="dea2d-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="dea2d-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dea2d-122">Windows 7</span></span> |
| <span data-ttu-id="dea2d-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="dea2d-123">Visual Studio</span></span>                                                  | <span data-ttu-id="dea2d-124">2008</span><span class="sxs-lookup"><span data-stu-id="dea2d-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="dea2d-125">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="dea2d-125">Downloading the Sample</span></span>

<span data-ttu-id="dea2d-126">Dieses Beispiel ist an den folgenden Speicherorten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dea2d-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="dea2d-127">Standort</span><span class="sxs-lookup"><span data-stu-id="dea2d-127">Location</span></span>    | <span data-ttu-id="dea2d-128">Pfad/URL</span><span class="sxs-lookup"><span data-stu-id="dea2d-128">Path/URL</span></span>                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dea2d-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="dea2d-129">Windows SDK</span></span> | <span data-ttu-id="dea2d-130">\\Programme \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Multimedia Audio \\ \\ \\ RenderExclusiveEventDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="dea2d-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderExclusiveEventDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="dea2d-131">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="dea2d-131">Building the Sample</span></span>

<span data-ttu-id="dea2d-132">Führen Sie die folgenden Schritte aus, um das RenderExclusiveEventDriven-Beispiel zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="dea2d-132">To build the RenderExclusiveEventDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="dea2d-133">Öffnen Sie die CMD-Shell für die Windows SDK, und wechseln Sie in das Beispielverzeichnis RenderExclusiveEventDriven.</span><span class="sxs-lookup"><span data-stu-id="dea2d-133">Open the CMD shell for the Windows SDK and change to the RenderExclusiveEventDriven sample directory.</span></span>
2.  <span data-ttu-id="dea2d-134">Führen Sie den Befehl `start WASAPIRenderExclusiveEventDriven.sln` im Verzeichnis RenderExclusiveEventDriven aus, um das Projekt WASAPIRenderExclusiveEventDriven im fenster Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dea2d-134">Run the command `start WASAPIRenderExclusiveEventDriven.sln` in the RenderExclusiveEventDriven directory to open the WASAPIRenderExclusiveEventDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="dea2d-135">Wählen Sie im Fenster die Konfiguration **Debug-** oder **Releaselösung** aus, wählen Sie in der Menüleiste das Menü **Erstellen** und dann die Option **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="dea2d-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="dea2d-136">Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, haben Visual Studio keinen Zugriff auf die SDK-Buildumgebung.</span><span class="sxs-lookup"><span data-stu-id="dea2d-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="dea2d-137">In diesem Fall wird das Beispiel nur erstellt, wenn Sie die Umgebungsvariable MSSdk explizit festlegen, die in der Projektdatei WASAPIRenderExclusiveEventDriven.vcproj verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dea2d-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderExclusiveEventDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="dea2d-138">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="dea2d-138">Running the Sample</span></span>

<span data-ttu-id="dea2d-139">Wenn Sie die Demoanwendung erfolgreich erstellen, wird eine ausführbare Datei WASAPIRenderExclusiveEventDriven.exe generiert.</span><span class="sxs-lookup"><span data-stu-id="dea2d-139">If you build the demo application successfully, an executable file, WASAPIRenderExclusiveEventDriven.exe, is generated.</span></span> <span data-ttu-id="dea2d-140">Geben Sie zum Ausführen `WASAPIRenderExclusiveEventDriven` ein Befehlsfenster gefolgt von erforderlichen oder optionalen Argumenten ein.</span><span class="sxs-lookup"><span data-stu-id="dea2d-140">To run it, type `WASAPIRenderExclusiveEventDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="dea2d-141">Das folgende Beispiel zeigt, wie das Beispiel ausgeführt wird, indem die Wiedergabedauer auf dem Standardmäßigen Multimediagerät angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="dea2d-141">The following example shows how to run the sample by specifying playback duration on the default multimedia device.</span></span>

`WASAPIRenderExclusiveEventDriven.exe -d 20 -multimedia`

<span data-ttu-id="dea2d-142">In der folgenden Tabelle sind die Argumente aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="dea2d-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="dea2d-143">Argument</span><span class="sxs-lookup"><span data-stu-id="dea2d-143">Argument</span></span>        | <span data-ttu-id="dea2d-144">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dea2d-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="dea2d-145">-?</span><span class="sxs-lookup"><span data-stu-id="dea2d-145">-?</span></span>              | <span data-ttu-id="dea2d-146">Zeigt Hilfe an.</span><span class="sxs-lookup"><span data-stu-id="dea2d-146">Shows help.</span></span>                                                |
| <span data-ttu-id="dea2d-147">-H</span><span class="sxs-lookup"><span data-stu-id="dea2d-147">-h</span></span>              | <span data-ttu-id="dea2d-148">Zeigt Hilfe an.</span><span class="sxs-lookup"><span data-stu-id="dea2d-148">Shows help.</span></span>                                                |
| <span data-ttu-id="dea2d-149">-f</span><span class="sxs-lookup"><span data-stu-id="dea2d-149">-f</span></span>              | <span data-ttu-id="dea2d-150">Sinusfrequenz in Hz.</span><span class="sxs-lookup"><span data-stu-id="dea2d-150">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="dea2d-151">-l</span><span class="sxs-lookup"><span data-stu-id="dea2d-151">-l</span></span>              | <span data-ttu-id="dea2d-152">Audiorenderinglatenz in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="dea2d-152">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="dea2d-153">-d</span><span class="sxs-lookup"><span data-stu-id="dea2d-153">-d</span></span>              | <span data-ttu-id="dea2d-154">Sinus-Wellendauer in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="dea2d-154">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="dea2d-155">-M</span><span class="sxs-lookup"><span data-stu-id="dea2d-155">-m</span></span>              | <span data-ttu-id="dea2d-156">Deaktiviert die Verwendung von MMCSS.</span><span class="sxs-lookup"><span data-stu-id="dea2d-156">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="dea2d-157">-console</span><span class="sxs-lookup"><span data-stu-id="dea2d-157">-console</span></span>        | <span data-ttu-id="dea2d-158">Verwenden Sie das Standardkonsolengerät.</span><span class="sxs-lookup"><span data-stu-id="dea2d-158">Use the default console device.</span></span>                            |
| <span data-ttu-id="dea2d-159">-communications</span><span class="sxs-lookup"><span data-stu-id="dea2d-159">-communications</span></span> | <span data-ttu-id="dea2d-160">Verwenden Sie das Standardkommunikationsgerät.</span><span class="sxs-lookup"><span data-stu-id="dea2d-160">Use the default communication device.</span></span>                      |
| <span data-ttu-id="dea2d-161">-multimedia</span><span class="sxs-lookup"><span data-stu-id="dea2d-161">-multimedia</span></span>     | <span data-ttu-id="dea2d-162">Verwenden Sie das Standardmäßige Multimediagerät.</span><span class="sxs-lookup"><span data-stu-id="dea2d-162">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="dea2d-163">-endpoint</span><span class="sxs-lookup"><span data-stu-id="dea2d-163">-endpoint</span></span>       | <span data-ttu-id="dea2d-164">Verwenden Sie den Endpunktbezeichner, der im Switchwert angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="dea2d-164">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="dea2d-165">Wenn die Anwendung ohne Argumente ausgeführt wird, listet sie die verfügbaren Geräte auf und fordert den Benutzer auf, ein Gerät für die Renderingsitzung auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="dea2d-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="dea2d-166">Nachdem der Benutzer ein Gerät angegeben hat, rendert die Anwendung eine Sinusbewegung bei 440 Hz für 10 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="dea2d-166">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="dea2d-167">Diese Werte können durch Angeben der Schalterwerte -f und -d geändert werden.</span><span class="sxs-lookup"><span data-stu-id="dea2d-167">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="dea2d-168">Das RenderExclusiveEventDriven-Beispiel veranschaulicht die ereignisgesteuerte Pufferung.</span><span class="sxs-lookup"><span data-stu-id="dea2d-168">The RenderExclusiveEventDriven sample demonstrates event-driven buffering.</span></span> <span data-ttu-id="dea2d-169">Das Beispiel zeigt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="dea2d-169">The sample shows how to:</span></span>

-   <span data-ttu-id="dea2d-170">Instanziieren Sie einen Audioclient, konfigurieren Sie ihn für die Ausführung im exklusiven Modus, und aktivieren Sie die ereignisgesteuerte Pufferung, indem Sie das **AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK-Flag** im Aufruf von [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)festlegen.</span><span class="sxs-lookup"><span data-stu-id="dea2d-170">Instantiate an audio client, configure it to run in exclusive mode, and enable event-driven buffering by setting the **AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK** flag in the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span>
-   <span data-ttu-id="dea2d-171">Ordnen Sie den Client den Beispielen zu, die gerendert werden können, indem Sie ein Ereignishandle für das System bereitstellen, indem Sie die [**IAudioClient::SetEventHandle-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dea2d-171">Associate the client with the samples that are ready to be rendered by providing an event handle to the system by calling the [**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) method.</span></span>
-   <span data-ttu-id="dea2d-172">Erstellen Sie einen Renderthread, um Beispiele aus der Audio-Engine zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="dea2d-172">Create a render thread to process samples from the audio engine.</span></span>
-   <span data-ttu-id="dea2d-173">Richten Sie die Puffer ordnungsgemäß an einer 128-Byte-Grenze aus, bevor Sie sie an das Gerät senden.</span><span class="sxs-lookup"><span data-stu-id="dea2d-173">Align the buffers properly on a 128-byte boundary before sending them to the device.</span></span> <span data-ttu-id="dea2d-174">Dies erfolgt durch Anpassen der Periodizität der Engine.</span><span class="sxs-lookup"><span data-stu-id="dea2d-174">This is done by adjusting the periodicity of the engine.</span></span>
-   <span data-ttu-id="dea2d-175">Überprüfen Sie das Mischungsformat des Geräteendpunkts, um zu bestimmen, ob die Beispiele gerendert werden können.</span><span class="sxs-lookup"><span data-stu-id="dea2d-175">Check the mix format of the device endpoint to determine whether the samples can be rendered.</span></span> <span data-ttu-id="dea2d-176">Wenn das Gerät das Mischungsformat nicht unterstützt, werden die Daten in PCM konvertiert.</span><span class="sxs-lookup"><span data-stu-id="dea2d-176">If the device does not support the mix format, the data is converted to PCM.</span></span>
-   <span data-ttu-id="dea2d-177">Behandeln von Datenstromwechseln.</span><span class="sxs-lookup"><span data-stu-id="dea2d-177">Handle stream switching.</span></span>

<span data-ttu-id="dea2d-178">Nachdem die Renderingsitzung gestartet und der Stream gestartet wurde, signalisiert die Audio-Engine dem bereitgestellten Ereignishandle, dass der Client benachrichtigt wird, wenn ein Puffer für die Verarbeitung durch den Client bereit ist.</span><span class="sxs-lookup"><span data-stu-id="dea2d-178">After the rendering session begins and the stream starts, the audio engine signals the supplied event handle to notify the client each time a buffer becomes ready for the client to process.</span></span> <span data-ttu-id="dea2d-179">Die Audiodaten können auch in einer zeitgebergesteuerten Schleife verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="dea2d-179">The audio data can also be processed in a timer-driven loop.</span></span> <span data-ttu-id="dea2d-180">Dieser Modus wird im [RenderExclusiveTimerDriven-Beispiel](renderexclusivetimerdriven.md) veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="dea2d-180">This mode is demonstrated in the [RenderExclusiveTimerDriven](renderexclusivetimerdriven.md) sample.</span></span>

<span data-ttu-id="dea2d-181">Weitere Informationen zum Rendern eines Streams finden Sie unter [Rendern eines Streams.](rendering-a-stream.md)</span><span class="sxs-lookup"><span data-stu-id="dea2d-181">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dea2d-182">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dea2d-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dea2d-183">SDK-Beispiele, die die Kernaudio-APIs verwenden</span><span class="sxs-lookup"><span data-stu-id="dea2d-183">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



