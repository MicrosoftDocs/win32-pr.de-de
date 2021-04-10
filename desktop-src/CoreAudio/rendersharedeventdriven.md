---
description: Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu Rendering.
ms.assetid: 92e644be-df8b-415d-ac8e-c0c30c85f844
title: Rendersharedebug-gesteuert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9901896b962717ed72fd36d022eef9510d7cb916
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861303"
---
# <a name="rendersharedeventdriven"></a><span data-ttu-id="c462c-103">Rendersharedebug-gesteuert</span><span class="sxs-lookup"><span data-stu-id="c462c-103">RenderSharedEventDriven</span></span>

<span data-ttu-id="c462c-104">Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="c462c-104">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="c462c-105">Dieses Beispiel veranschaulicht die ereignisgesteuerte Pufferung für einen renderingclient im freigegebenen Modus.</span><span class="sxs-lookup"><span data-stu-id="c462c-105">This sample demonstrates event-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="c462c-106">Bei einem Stream im freigegebenen Modus verwendet der Client den Endpunkt Puffer mit der Audioengine.</span><span class="sxs-lookup"><span data-stu-id="c462c-106">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span>

<span data-ttu-id="c462c-107">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="c462c-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c462c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c462c-108">Description</span></span>](#description)
-   [<span data-ttu-id="c462c-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c462c-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="c462c-110">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c462c-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="c462c-111">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="c462c-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="c462c-112">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c462c-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="c462c-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c462c-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="c462c-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c462c-114">Description</span></span>

<span data-ttu-id="c462c-115">In diesem Beispiel werden die folgenden Funktionen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c462c-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="c462c-116">[Mmdevice-API](mmdevice-api.md) für die Enumeration und Auswahl von Multimedia-Geräten.</span><span class="sxs-lookup"><span data-stu-id="c462c-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="c462c-117">WASAPI für Stream-Verwaltungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="c462c-117">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="c462c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c462c-118">Requirements</span></span>



| <span data-ttu-id="c462c-119">Produkt</span><span class="sxs-lookup"><span data-stu-id="c462c-119">Product</span></span>                                                        | <span data-ttu-id="c462c-120">Version</span><span class="sxs-lookup"><span data-stu-id="c462c-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="c462c-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="c462c-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="c462c-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c462c-122">Windows 7</span></span> |
| <span data-ttu-id="c462c-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c462c-123">Visual Studio</span></span>                                                  | <span data-ttu-id="c462c-124">2008</span><span class="sxs-lookup"><span data-stu-id="c462c-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="c462c-125">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c462c-125">Downloading the Sample</span></span>

<span data-ttu-id="c462c-126">Dieses Beispiel ist in den folgenden Speicherorten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c462c-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="c462c-127">Standort</span><span class="sxs-lookup"><span data-stu-id="c462c-127">Location</span></span>    | <span data-ttu-id="c462c-128">Pfad/URL</span><span class="sxs-lookup"><span data-stu-id="c462c-128">Path/URL</span></span>                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c462c-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="c462c-129">Windows SDK</span></span> | <span data-ttu-id="c462c-130">\\Programmdateien \\ Microsoft sdgs \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ \\ audiorendersharedeventgesteu. \\ ..</span><span class="sxs-lookup"><span data-stu-id="c462c-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderSharedEventDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="c462c-131">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c462c-131">Building the Sample</span></span>

<span data-ttu-id="c462c-132">Führen Sie die folgenden Schritte aus, um das rendersharedeventgesteuerte-Beispiel zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="c462c-132">To build the RenderSharedEventDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="c462c-133">Öffnen Sie die CMD-Shell für die Windows SDK, und wechseln Sie zum Verzeichnis "rendersharedeventgesteudirectory".</span><span class="sxs-lookup"><span data-stu-id="c462c-133">Open the CMD shell for the Windows SDK and change to the RenderSharedEventDriven sample directory.</span></span>
2.  <span data-ttu-id="c462c-134">Führen Sie den Befehl `start WASAPIRenderSharedEventDriven.sln` im Verzeichnis rendersharedeventlab aus, um das Projekt wasapiriendersharedeventgesteuim Visual Studio-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c462c-134">Run the command `start WASAPIRenderSharedEventDriven.sln` in the RenderSharedEventDriven directory to open the WASAPIRenderSharedEventDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="c462c-135">Wählen Sie im Fenster die **Debug** -oder **releaseprojektmappenkonfiguration** aus, wählen Sie das Menü **Erstellen** in der Menüleiste aus, und wählen Sie die Option **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="c462c-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="c462c-136">Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, hat Visual Studio keinen Zugriff auf die SDK-Buildumgebung.</span><span class="sxs-lookup"><span data-stu-id="c462c-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="c462c-137">In diesem Fall wird das Beispiel nicht erstellt, es sei denn, Sie legen die Umgebungsvariable "Mssdk", die in der Projektdatei verwendet wird, "wasapiriendersharedevent-Controller. vcproj" explizit fest.</span><span class="sxs-lookup"><span data-stu-id="c462c-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderSharedEventDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="c462c-138">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c462c-138">Running the Sample</span></span>

<span data-ttu-id="c462c-139">Wenn Sie die Demoanwendung erfolgreich erstellen, wird eine ausführbare Datei (WASAPIRenderSharedEventDriven.exe) generiert.</span><span class="sxs-lookup"><span data-stu-id="c462c-139">If you build the demo application successfully, an executable file, WASAPIRenderSharedEventDriven.exe, is generated.</span></span> <span data-ttu-id="c462c-140">Um es auszuführen, geben Sie `WASAPIRenderSharedEventDriven` ein Befehlsfenster ein, gefolgt von den erforderlichen oder optionalen Argumenten.</span><span class="sxs-lookup"><span data-stu-id="c462c-140">To run it, type `WASAPIRenderSharedEventDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="c462c-141">Im folgenden Beispiel wird gezeigt, wie Sie das Beispiel ausführen, indem Sie die Wiedergabedauer für das standardmäßige Multimedia-Gerät angeben.</span><span class="sxs-lookup"><span data-stu-id="c462c-141">The following example shows how to run the sample by specifying playback duration on the default multimedia device.</span></span>

`WASAPIRenderSharedEventDriven.exe -d 20 -multimedia`

<span data-ttu-id="c462c-142">In der folgenden Tabelle werden die Argumente angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c462c-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="c462c-143">Argument</span><span class="sxs-lookup"><span data-stu-id="c462c-143">Argument</span></span>        | <span data-ttu-id="c462c-144">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c462c-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="c462c-145">-?</span><span class="sxs-lookup"><span data-stu-id="c462c-145">-?</span></span>              | <span data-ttu-id="c462c-146">Zeigt die Hilfe an.</span><span class="sxs-lookup"><span data-stu-id="c462c-146">Shows help.</span></span>                                                |
| <span data-ttu-id="c462c-147">-h</span><span class="sxs-lookup"><span data-stu-id="c462c-147">-h</span></span>              | <span data-ttu-id="c462c-148">Zeigt die Hilfe an.</span><span class="sxs-lookup"><span data-stu-id="c462c-148">Shows help.</span></span>                                                |
| <span data-ttu-id="c462c-149">-f</span><span class="sxs-lookup"><span data-stu-id="c462c-149">-f</span></span>              | <span data-ttu-id="c462c-150">Sinuswellen Frequenz in Hz.</span><span class="sxs-lookup"><span data-stu-id="c462c-150">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="c462c-151">-l</span><span class="sxs-lookup"><span data-stu-id="c462c-151">-l</span></span>              | <span data-ttu-id="c462c-152">Wartezeit für audiorendering in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="c462c-152">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="c462c-153">-d</span><span class="sxs-lookup"><span data-stu-id="c462c-153">-d</span></span>              | <span data-ttu-id="c462c-154">Sinuswellen Dauer in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="c462c-154">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="c462c-155">-M</span><span class="sxs-lookup"><span data-stu-id="c462c-155">-m</span></span>              | <span data-ttu-id="c462c-156">Deaktiviert die Verwendung von MMCSS.</span><span class="sxs-lookup"><span data-stu-id="c462c-156">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="c462c-157">-Konsole</span><span class="sxs-lookup"><span data-stu-id="c462c-157">-console</span></span>        | <span data-ttu-id="c462c-158">Verwenden Sie das Standard Konsolen Gerät.</span><span class="sxs-lookup"><span data-stu-id="c462c-158">Use the default console device.</span></span>                            |
| <span data-ttu-id="c462c-159">-Kommunikation</span><span class="sxs-lookup"><span data-stu-id="c462c-159">-communications</span></span> | <span data-ttu-id="c462c-160">Verwenden Sie das Standard Kommunikationsgerät.</span><span class="sxs-lookup"><span data-stu-id="c462c-160">Use the default communication device.</span></span>                      |
| <span data-ttu-id="c462c-161">-Multimedia</span><span class="sxs-lookup"><span data-stu-id="c462c-161">-multimedia</span></span>     | <span data-ttu-id="c462c-162">Verwenden Sie das standardmäßige Multimedia-Gerät.</span><span class="sxs-lookup"><span data-stu-id="c462c-162">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="c462c-163">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="c462c-163">-endpoint</span></span>       | <span data-ttu-id="c462c-164">Verwenden Sie den Endpunkt Bezeichner, der im Switch-Wert angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c462c-164">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="c462c-165">Wenn die Anwendung ohne Argumente ausgeführt wird, listet Sie die verfügbaren Geräte auf und fordert den Benutzer auf, ein Gerät für die renderingsitzung auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c462c-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="c462c-166">Nachdem der Benutzer ein Gerät angegeben hat, rendert die Anwendung eine Sinuswelle bei 440 Hz für 10 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="c462c-166">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="c462c-167">Diese Werte können durch Angabe von "-f" und "-d"-Schalter Werte geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c462c-167">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="c462c-168">Rendershareentventgesteuerte zeigt die ereignisgesteuerte Pufferung.</span><span class="sxs-lookup"><span data-stu-id="c462c-168">RenderSharedEventDriven demonstrates event-driven buffering.</span></span> <span data-ttu-id="c462c-169">Das Beispiel zeigt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c462c-169">The sample shows how to:</span></span>

-   <span data-ttu-id="c462c-170">Instanziieren Sie einen AudioClient, konfigurieren Sie ihn so, dass er im exklusiven Modus ausgeführt wird, und aktivieren Sie die ereignisgesteuerte Pufferung, indem Sie im Aufrufen von [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)das Flag " **audclnt \_ StreamFlags \_ EventCallback** " festlegen.</span><span class="sxs-lookup"><span data-stu-id="c462c-170">Instantiate an audio client, configure it to run in exclusive mode, and enable event-driven buffering by setting the **AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK** flag in the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span>
-   <span data-ttu-id="c462c-171">Ordnen Sie den Client die Beispiele zu, die gerendert werden können, indem Sie ein Ereignis Handle für das System bereitstellen, indem Sie die [**iaudioclient:: setteventhandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c462c-171">Associate the client with the samples that are ready to be rendered by providing an event handle to the system by calling the [**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) method.</span></span>
-   <span data-ttu-id="c462c-172">Erstellen Sie einen Renderthread, um Beispiele aus der Audioengine zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c462c-172">Create a render thread to proces samples from the audio engine.</span></span>
-   <span data-ttu-id="c462c-173">Überprüfen Sie das Mischungs Format des Geräte Endpunkts, um zu bestimmen, ob die Beispiele gerendert werden können</span><span class="sxs-lookup"><span data-stu-id="c462c-173">Check the mix format of the device endpoint to determine whether the samples can be rendered.</span></span> <span data-ttu-id="c462c-174">Wenn das Gerät das Mischungs Format nicht unterstützt, werden die Daten in PCM konvertiert.</span><span class="sxs-lookup"><span data-stu-id="c462c-174">If the device does not support the mix format, the data is converted to PCM.</span></span>
-   <span data-ttu-id="c462c-175">Handle des streamwechsels.</span><span class="sxs-lookup"><span data-stu-id="c462c-175">Handle stream switching.</span></span>

<span data-ttu-id="c462c-176">Nachdem die renderingsitzung beginnt und der Stream gestartet wurde, signalisiert die Audioengine dem bereitgestellten Ereignis handle, dass der Client jedes Mal benachrichtigt wird, wenn ein Puffer für die Verarbeitung durch den Client bereit ist.</span><span class="sxs-lookup"><span data-stu-id="c462c-176">After the rendering session begins and the stream starts, the audio engine signals the supplied event handle to notify the client each time a buffer becomes ready for the client to process.</span></span> <span data-ttu-id="c462c-177">Die Audiodaten können auch in einer Zeit Geber gesteuerten Schleife verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="c462c-177">The audio data can also be processed in a timer-driven loop.</span></span> <span data-ttu-id="c462c-178">Dieser Modus wird im [rendersharedtimergesteuert](rendersharedtimerdriven.md) -Beispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c462c-178">This mode is demonstrated in the [RenderSharedTimerDriven](rendersharedtimerdriven.md) sample.</span></span>

<span data-ttu-id="c462c-179">Weitere Informationen zum Rendern eines Streams finden Sie unter [Rendern eines Streams](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="c462c-179">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c462c-180">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c462c-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c462c-181">SDK-Beispiele für die Verwendung der kernaudioapis</span><span class="sxs-lookup"><span data-stu-id="c462c-181">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



