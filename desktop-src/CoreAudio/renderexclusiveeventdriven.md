---
description: Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu Rendering.
ms.assetid: 3a2e3fa6-2d6a-4ab0-a531-d1c968458e96
title: Renderexclusiveeventdriver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3b94fa423cd4d4e7dc7121e927696529bfadf9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041454"
---
# <a name="renderexclusiveeventdriven"></a><span data-ttu-id="d43d7-103">Renderexclusiveeventdriver</span><span class="sxs-lookup"><span data-stu-id="d43d7-103">RenderExclusiveEventDriven</span></span>

<span data-ttu-id="d43d7-104">Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="d43d7-104">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="d43d7-105">In diesem Beispiel wird die ereignisgesteuerte Pufferung für einen renderingclient im exklusiven Modus veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d43d7-105">This sample demonstrates event-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="d43d7-106">Für einen Stream im exklusiven Modus gibt der Client den Endpunkt Puffer mit dem Audiogerät frei.</span><span class="sxs-lookup"><span data-stu-id="d43d7-106">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span>

<span data-ttu-id="d43d7-107">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="d43d7-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d43d7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d43d7-108">Description</span></span>](#description)
-   [<span data-ttu-id="d43d7-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d43d7-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="d43d7-110">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d43d7-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="d43d7-111">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="d43d7-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="d43d7-112">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d43d7-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="d43d7-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d43d7-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="d43d7-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d43d7-114">Description</span></span>

<span data-ttu-id="d43d7-115">In diesem Beispiel werden die folgenden Funktionen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d43d7-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="d43d7-116">[Mmdevice-API](mmdevice-api.md) für die Enumeration und Auswahl von Multimedia-Geräten.</span><span class="sxs-lookup"><span data-stu-id="d43d7-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="d43d7-117">WASAPI für Stream-Verwaltungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="d43d7-117">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="d43d7-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d43d7-118">Requirements</span></span>



| <span data-ttu-id="d43d7-119">Produkt</span><span class="sxs-lookup"><span data-stu-id="d43d7-119">Product</span></span>                                                        | <span data-ttu-id="d43d7-120">Version</span><span class="sxs-lookup"><span data-stu-id="d43d7-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="d43d7-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="d43d7-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="d43d7-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d43d7-122">Windows 7</span></span> |
| <span data-ttu-id="d43d7-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d43d7-123">Visual Studio</span></span>                                                  | <span data-ttu-id="d43d7-124">2008</span><span class="sxs-lookup"><span data-stu-id="d43d7-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="d43d7-125">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d43d7-125">Downloading the Sample</span></span>

<span data-ttu-id="d43d7-126">Dieses Beispiel ist in den folgenden Speicherorten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d43d7-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="d43d7-127">Standort</span><span class="sxs-lookup"><span data-stu-id="d43d7-127">Location</span></span>    | <span data-ttu-id="d43d7-128">Pfad/URL</span><span class="sxs-lookup"><span data-stu-id="d43d7-128">Path/URL</span></span>                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d43d7-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="d43d7-129">Windows SDK</span></span> | <span data-ttu-id="d43d7-130">\\Programme \\ Microsoft sdgs \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ \\ audiorenderexclusiveeventguide \\ ...</span><span class="sxs-lookup"><span data-stu-id="d43d7-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderExclusiveEventDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="d43d7-131">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d43d7-131">Building the Sample</span></span>

<span data-ttu-id="d43d7-132">Um das renderexclusiveeventpress-Beispiel zu erstellen, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="d43d7-132">To build the RenderExclusiveEventDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="d43d7-133">Öffnen Sie die CMD-Shell für die Windows SDK, und wechseln Sie zum Verzeichnis "renderexclusiveeventdriver Sample".</span><span class="sxs-lookup"><span data-stu-id="d43d7-133">Open the CMD shell for the Windows SDK and change to the RenderExclusiveEventDriven sample directory.</span></span>
2.  <span data-ttu-id="d43d7-134">Führen Sie den Befehl `start WASAPIRenderExclusiveEventDriven.sln` im Verzeichnis "renderexclusiveeventrun" aus, um das Projekt "wasapirienderexclusiveeventrun" im Visual Studio-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d43d7-134">Run the command `start WASAPIRenderExclusiveEventDriven.sln` in the RenderExclusiveEventDriven directory to open the WASAPIRenderExclusiveEventDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="d43d7-135">Wählen Sie im Fenster die **Debug** -oder **releaseprojektmappenkonfiguration** aus, wählen Sie das Menü **Erstellen** in der Menüleiste aus, und wählen Sie die Option **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="d43d7-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="d43d7-136">Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, hat Visual Studio keinen Zugriff auf die SDK-Buildumgebung.</span><span class="sxs-lookup"><span data-stu-id="d43d7-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="d43d7-137">In diesem Fall wird das Beispiel nicht erstellt, es sei denn, Sie legen die Umgebungsvariable "Mssdk", die in der Projektdatei "wasapirienderexclusiveeventcontroller. vcproj" verwendet wird, explizit fest.</span><span class="sxs-lookup"><span data-stu-id="d43d7-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderExclusiveEventDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="d43d7-138">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d43d7-138">Running the Sample</span></span>

<span data-ttu-id="d43d7-139">Wenn Sie die Demoanwendung erfolgreich erstellen, wird eine ausführbare Datei (WASAPIRenderExclusiveEventDriven.exe) generiert.</span><span class="sxs-lookup"><span data-stu-id="d43d7-139">If you build the demo application successfully, an executable file, WASAPIRenderExclusiveEventDriven.exe, is generated.</span></span> <span data-ttu-id="d43d7-140">Um es auszuführen, geben Sie `WASAPIRenderExclusiveEventDriven` ein Befehlsfenster ein, gefolgt von den erforderlichen oder optionalen Argumenten.</span><span class="sxs-lookup"><span data-stu-id="d43d7-140">To run it, type `WASAPIRenderExclusiveEventDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="d43d7-141">Im folgenden Beispiel wird gezeigt, wie Sie das Beispiel ausführen, indem Sie die Wiedergabedauer für das standardmäßige Multimedia-Gerät angeben.</span><span class="sxs-lookup"><span data-stu-id="d43d7-141">The following example shows how to run the sample by specifying playback duration on the default multimedia device.</span></span>

`WASAPIRenderExclusiveEventDriven.exe -d 20 -multimedia`

<span data-ttu-id="d43d7-142">In der folgenden Tabelle werden die Argumente angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d43d7-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="d43d7-143">Argument</span><span class="sxs-lookup"><span data-stu-id="d43d7-143">Argument</span></span>        | <span data-ttu-id="d43d7-144">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d43d7-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="d43d7-145">-?</span><span class="sxs-lookup"><span data-stu-id="d43d7-145">-?</span></span>              | <span data-ttu-id="d43d7-146">Zeigt die Hilfe an.</span><span class="sxs-lookup"><span data-stu-id="d43d7-146">Shows help.</span></span>                                                |
| <span data-ttu-id="d43d7-147">-h</span><span class="sxs-lookup"><span data-stu-id="d43d7-147">-h</span></span>              | <span data-ttu-id="d43d7-148">Zeigt die Hilfe an.</span><span class="sxs-lookup"><span data-stu-id="d43d7-148">Shows help.</span></span>                                                |
| <span data-ttu-id="d43d7-149">-f</span><span class="sxs-lookup"><span data-stu-id="d43d7-149">-f</span></span>              | <span data-ttu-id="d43d7-150">Sinuswellen Frequenz in Hz.</span><span class="sxs-lookup"><span data-stu-id="d43d7-150">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="d43d7-151">-l</span><span class="sxs-lookup"><span data-stu-id="d43d7-151">-l</span></span>              | <span data-ttu-id="d43d7-152">Wartezeit für audiorendering in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="d43d7-152">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="d43d7-153">-d</span><span class="sxs-lookup"><span data-stu-id="d43d7-153">-d</span></span>              | <span data-ttu-id="d43d7-154">Sinuswellen Dauer in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="d43d7-154">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="d43d7-155">-M</span><span class="sxs-lookup"><span data-stu-id="d43d7-155">-m</span></span>              | <span data-ttu-id="d43d7-156">Deaktiviert die Verwendung von MMCSS.</span><span class="sxs-lookup"><span data-stu-id="d43d7-156">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="d43d7-157">-Konsole</span><span class="sxs-lookup"><span data-stu-id="d43d7-157">-console</span></span>        | <span data-ttu-id="d43d7-158">Verwenden Sie das Standard Konsolen Gerät.</span><span class="sxs-lookup"><span data-stu-id="d43d7-158">Use the default console device.</span></span>                            |
| <span data-ttu-id="d43d7-159">-Kommunikation</span><span class="sxs-lookup"><span data-stu-id="d43d7-159">-communications</span></span> | <span data-ttu-id="d43d7-160">Verwenden Sie das Standard Kommunikationsgerät.</span><span class="sxs-lookup"><span data-stu-id="d43d7-160">Use the default communication device.</span></span>                      |
| <span data-ttu-id="d43d7-161">-Multimedia</span><span class="sxs-lookup"><span data-stu-id="d43d7-161">-multimedia</span></span>     | <span data-ttu-id="d43d7-162">Verwenden Sie das standardmäßige Multimedia-Gerät.</span><span class="sxs-lookup"><span data-stu-id="d43d7-162">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="d43d7-163">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="d43d7-163">-endpoint</span></span>       | <span data-ttu-id="d43d7-164">Verwenden Sie den Endpunkt Bezeichner, der im Switch-Wert angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d43d7-164">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="d43d7-165">Wenn die Anwendung ohne Argumente ausgeführt wird, listet Sie die verfügbaren Geräte auf und fordert den Benutzer auf, ein Gerät für die renderingsitzung auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="d43d7-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="d43d7-166">Nachdem der Benutzer ein Gerät angegeben hat, rendert die Anwendung eine Sinuswelle bei 440 Hz für 10 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="d43d7-166">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="d43d7-167">Diese Werte können durch Angabe von "-f" und "-d"-Schalter Werte geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d43d7-167">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="d43d7-168">Das renderexclusiveeventgesteuerte-Beispiel veranschaulicht die ereignisgesteuerte Pufferung.</span><span class="sxs-lookup"><span data-stu-id="d43d7-168">The RenderExclusiveEventDriven sample demonstrates event-driven buffering.</span></span> <span data-ttu-id="d43d7-169">Das Beispiel zeigt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d43d7-169">The sample shows how to:</span></span>

-   <span data-ttu-id="d43d7-170">Instanziieren Sie einen AudioClient, konfigurieren Sie ihn so, dass er im exklusiven Modus ausgeführt wird, und aktivieren Sie die ereignisgesteuerte Pufferung, indem Sie im Aufrufen von [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)das Flag " **audclnt \_ StreamFlags \_ EventCallback** " festlegen.</span><span class="sxs-lookup"><span data-stu-id="d43d7-170">Instantiate an audio client, configure it to run in exclusive mode, and enable event-driven buffering by setting the **AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK** flag in the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span>
-   <span data-ttu-id="d43d7-171">Ordnen Sie den Client die Beispiele zu, die gerendert werden können, indem Sie ein Ereignis Handle für das System bereitstellen, indem Sie die [**iaudioclient:: setteventhandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d43d7-171">Associate the client with the samples that are ready to be rendered by providing an event handle to the system by calling the [**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) method.</span></span>
-   <span data-ttu-id="d43d7-172">Erstellen Sie einen Renderthread, um Beispiele aus der Audioengine zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="d43d7-172">Create a render thread to process samples from the audio engine.</span></span>
-   <span data-ttu-id="d43d7-173">Richten Sie die Puffer ordnungsgemäß an eine 128-Byte-Grenze aus, bevor Sie Sie an das Gerät senden.</span><span class="sxs-lookup"><span data-stu-id="d43d7-173">Align the buffers properly on a 128-byte boundary before sending them to the device.</span></span> <span data-ttu-id="d43d7-174">Dies erfolgt durch die Anpassung der Periodizität der Engine.</span><span class="sxs-lookup"><span data-stu-id="d43d7-174">This is done by adjusting the periodicity of the engine.</span></span>
-   <span data-ttu-id="d43d7-175">Überprüfen Sie das Mischungs Format des Geräte Endpunkts, um zu bestimmen, ob die Beispiele gerendert werden können</span><span class="sxs-lookup"><span data-stu-id="d43d7-175">Check the mix format of the device endpoint to determine whether the samples can be rendered.</span></span> <span data-ttu-id="d43d7-176">Wenn das Gerät das Mischungs Format nicht unterstützt, werden die Daten in PCM konvertiert.</span><span class="sxs-lookup"><span data-stu-id="d43d7-176">If the device does not support the mix format, the data is converted to PCM.</span></span>
-   <span data-ttu-id="d43d7-177">Handle des streamwechsels.</span><span class="sxs-lookup"><span data-stu-id="d43d7-177">Handle stream switching.</span></span>

<span data-ttu-id="d43d7-178">Nachdem die renderingsitzung beginnt und der Stream gestartet wurde, signalisiert die Audioengine dem bereitgestellten Ereignis handle, dass der Client jedes Mal benachrichtigt wird, wenn ein Puffer für die Verarbeitung durch den Client bereit ist.</span><span class="sxs-lookup"><span data-stu-id="d43d7-178">After the rendering session begins and the stream starts, the audio engine signals the supplied event handle to notify the client each time a buffer becomes ready for the client to process.</span></span> <span data-ttu-id="d43d7-179">Die Audiodaten können auch in einer Zeit Geber gesteuerten Schleife verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="d43d7-179">The audio data can also be processed in a timer-driven loop.</span></span> <span data-ttu-id="d43d7-180">Dieser Modus wird im [renderexclusivetimergesteuert](renderexclusivetimerdriven.md) -Beispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d43d7-180">This mode is demonstrated in the [RenderExclusiveTimerDriven](renderexclusivetimerdriven.md) sample.</span></span>

<span data-ttu-id="d43d7-181">Weitere Informationen zum Rendern eines Streams finden Sie unter [Rendern eines Streams](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="d43d7-181">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d43d7-182">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d43d7-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d43d7-183">SDK-Beispiele für die Verwendung der kernaudioapis</span><span class="sxs-lookup"><span data-stu-id="d43d7-183">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



