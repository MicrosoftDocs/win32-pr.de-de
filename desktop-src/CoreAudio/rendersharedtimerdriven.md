---
description: Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu Rendering.
ms.assetid: eae7d896-77ef-4340-bd77-1f3333166987
title: Rendersharedtimer-gesteuert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de4ce441a12d65b8bebb843c7b9a168443b34592
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748537"
---
# <a name="rendersharedtimerdriven"></a><span data-ttu-id="76858-103">Rendersharedtimer-gesteuert</span><span class="sxs-lookup"><span data-stu-id="76858-103">RenderSharedTimerDriven</span></span>

<span data-ttu-id="76858-104">Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="76858-104">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="76858-105">Dieses Beispiel veranschaulicht die Zeit Geber gesteuerte Pufferung für einen renderingclient im freigegebenen Modus.</span><span class="sxs-lookup"><span data-stu-id="76858-105">This sample demonstrates timer-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="76858-106">Bei einem Stream im freigegebenen Modus verwendet der Client den Endpunkt Puffer mit der Audioengine.</span><span class="sxs-lookup"><span data-stu-id="76858-106">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span>

<span data-ttu-id="76858-107">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="76858-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="76858-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76858-108">Description</span></span>](#description)
-   [<span data-ttu-id="76858-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76858-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="76858-110">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="76858-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="76858-111">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="76858-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="76858-112">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="76858-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="76858-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="76858-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="76858-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76858-114">Description</span></span>

<span data-ttu-id="76858-115">In diesem Beispiel werden die folgenden Funktionen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="76858-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="76858-116">[Mmdevice-API](mmdevice-api.md) für die Enumeration und Auswahl von Multimedia-Geräten.</span><span class="sxs-lookup"><span data-stu-id="76858-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="76858-117">WASAPI für Stream-Verwaltungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="76858-117">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="76858-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76858-118">Requirements</span></span>



| <span data-ttu-id="76858-119">Produkt</span><span class="sxs-lookup"><span data-stu-id="76858-119">Product</span></span>                                                        | <span data-ttu-id="76858-120">Version</span><span class="sxs-lookup"><span data-stu-id="76858-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="76858-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="76858-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="76858-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="76858-122">Windows 7</span></span> |
| <span data-ttu-id="76858-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="76858-123">Visual Studio</span></span>                                                  | <span data-ttu-id="76858-124">2008</span><span class="sxs-lookup"><span data-stu-id="76858-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="76858-125">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="76858-125">Downloading the Sample</span></span>

<span data-ttu-id="76858-126">Dieses Beispiel ist in den folgenden Speicherorten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="76858-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="76858-127">Standort</span><span class="sxs-lookup"><span data-stu-id="76858-127">Location</span></span>    | <span data-ttu-id="76858-128">Pfad/URL</span><span class="sxs-lookup"><span data-stu-id="76858-128">Path/URL</span></span>                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76858-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="76858-129">Windows SDK</span></span> | <span data-ttu-id="76858-130">\\Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ \\ audiorendersharedtimer-gesteuert \\ ...</span><span class="sxs-lookup"><span data-stu-id="76858-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderSharedTimerDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="76858-131">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="76858-131">Building the Sample</span></span>

<span data-ttu-id="76858-132">Führen Sie die folgenden Schritte aus, um das rendersharedtimergesteuerte-Beispiel zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="76858-132">To build the RenderSharedTimerDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="76858-133">Öffnen Sie die CMD-Shell für die Windows SDK, und wechseln Sie in das Verzeichnis "rendersharedtimer. Sample".</span><span class="sxs-lookup"><span data-stu-id="76858-133">Open the CMD shell for the Windows SDK and change to the RenderSharedTimerDriven sample directory.</span></span>
2.  <span data-ttu-id="76858-134">Führen Sie den Befehl `start WASAPIRenderSharedTimerDriven.sln` im Verzeichnis rendersharedtimercommand aus, um das Projekt wasapiriendersharedtimer-gesteuert im Visual Studio-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="76858-134">Run the command `start WASAPIRenderSharedTimerDriven.sln` in the RenderSharedTimerDriven directory to open the WASAPIRenderSharedTimerDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="76858-135">Wählen Sie im Fenster die **Debug** -oder **releaseprojektmappenkonfiguration** aus, wählen Sie das Menü **Erstellen** in der Menüleiste aus, und wählen Sie die Option **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="76858-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="76858-136">Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, hat Visual Studio keinen Zugriff auf die SDK-Buildumgebung.</span><span class="sxs-lookup"><span data-stu-id="76858-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="76858-137">In diesem Fall wird das Beispiel nicht erstellt, es sei denn, Sie legen die Umgebungsvariable "Mssdk", die in der Projektdatei verwendet wird, "wasapiriendersharedtimercontroller. vcproj" explizit fest.</span><span class="sxs-lookup"><span data-stu-id="76858-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderSharedTimerDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="76858-138">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="76858-138">Running the Sample</span></span>

<span data-ttu-id="76858-139">Wenn Sie die Demoanwendung erfolgreich erstellen, wird eine ausführbare Datei (WASAPIRenderSharedTimerDriven.exe) generiert.</span><span class="sxs-lookup"><span data-stu-id="76858-139">If you build the demo application successfully, an executable file, WASAPIRenderSharedTimerDriven.exe, is generated.</span></span> <span data-ttu-id="76858-140">Um es auszuführen, geben Sie `WASAPIRenderSharedTimerDriven` ein Befehlsfenster ein, gefolgt von den erforderlichen oder optionalen Argumenten.</span><span class="sxs-lookup"><span data-stu-id="76858-140">To run it, type `WASAPIRenderSharedTimerDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="76858-141">Im folgenden Beispiel wird gezeigt, wie Sie das Beispiel ausführen, indem Sie die Wiedergabedauer für das standardmäßige Multimedia-Gerät angeben.</span><span class="sxs-lookup"><span data-stu-id="76858-141">The following example shows how to run the sample by specifying playback duration on the default multimedia device.</span></span>

`WASAPIRenderSharedTimerDriven.exe -d 20 -multimedia`

<span data-ttu-id="76858-142">In der folgenden Tabelle werden die Argumente angezeigt.</span><span class="sxs-lookup"><span data-stu-id="76858-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="76858-143">Argument</span><span class="sxs-lookup"><span data-stu-id="76858-143">Argument</span></span>        | <span data-ttu-id="76858-144">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76858-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="76858-145">-?</span><span class="sxs-lookup"><span data-stu-id="76858-145">-?</span></span>              | <span data-ttu-id="76858-146">Zeigt die Hilfe an.</span><span class="sxs-lookup"><span data-stu-id="76858-146">Shows help.</span></span>                                                |
| <span data-ttu-id="76858-147">-h</span><span class="sxs-lookup"><span data-stu-id="76858-147">-h</span></span>              | <span data-ttu-id="76858-148">Zeigt die Hilfe an.</span><span class="sxs-lookup"><span data-stu-id="76858-148">Shows help.</span></span>                                                |
| <span data-ttu-id="76858-149">-f</span><span class="sxs-lookup"><span data-stu-id="76858-149">-f</span></span>              | <span data-ttu-id="76858-150">Sinuswellen Frequenz in Hz.</span><span class="sxs-lookup"><span data-stu-id="76858-150">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="76858-151">-l</span><span class="sxs-lookup"><span data-stu-id="76858-151">-l</span></span>              | <span data-ttu-id="76858-152">Wartezeit für audiorendering in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="76858-152">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="76858-153">-d</span><span class="sxs-lookup"><span data-stu-id="76858-153">-d</span></span>              | <span data-ttu-id="76858-154">Sinuswellen Dauer in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="76858-154">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="76858-155">-M</span><span class="sxs-lookup"><span data-stu-id="76858-155">-m</span></span>              | <span data-ttu-id="76858-156">Deaktiviert die Verwendung von MMCSS.</span><span class="sxs-lookup"><span data-stu-id="76858-156">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="76858-157">-Konsole</span><span class="sxs-lookup"><span data-stu-id="76858-157">-console</span></span>        | <span data-ttu-id="76858-158">Verwenden Sie das Standard Konsolen Gerät.</span><span class="sxs-lookup"><span data-stu-id="76858-158">Use the default console device.</span></span>                            |
| <span data-ttu-id="76858-159">-Kommunikation</span><span class="sxs-lookup"><span data-stu-id="76858-159">-communications</span></span> | <span data-ttu-id="76858-160">Verwenden Sie das Standard Kommunikationsgerät.</span><span class="sxs-lookup"><span data-stu-id="76858-160">Use the default communication device.</span></span>                      |
| <span data-ttu-id="76858-161">-Multimedia</span><span class="sxs-lookup"><span data-stu-id="76858-161">-multimedia</span></span>     | <span data-ttu-id="76858-162">Verwenden Sie das standardmäßige Multimedia-Gerät.</span><span class="sxs-lookup"><span data-stu-id="76858-162">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="76858-163">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="76858-163">-endpoint</span></span>       | <span data-ttu-id="76858-164">Verwenden Sie den Endpunkt Bezeichner, der im Switch-Wert angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="76858-164">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="76858-165">Wenn die Anwendung ohne Argumente ausgeführt wird, listet Sie die verfügbaren Geräte auf und fordert den Benutzer auf, ein Gerät für die renderingsitzung auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="76858-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="76858-166">Nachdem der Benutzer ein Gerät angegeben hat, rendert die Anwendung eine Sinuswelle bei 440 Hz für 10 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="76858-166">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="76858-167">Diese Werte können durch Angabe von "-f" und "-d"-Schalter Werte geändert werden.</span><span class="sxs-lookup"><span data-stu-id="76858-167">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="76858-168">Rendersharedtimer-gesteuert zeigt eine Zeit Geber gesteuerte Pufferung.</span><span class="sxs-lookup"><span data-stu-id="76858-168">RenderSharedTimerDriven demonstrates timer-driven buffering.</span></span> <span data-ttu-id="76858-169">In diesem Modus muss der Client einen bestimmten Zeitraum (die Hälfte der Latenzzeit, die durch den Schalter-d angegeben wird, in Millisekunden) warten.</span><span class="sxs-lookup"><span data-stu-id="76858-169">In this mode, the client must wait for a period of time (half the latency, specified by the -d switch value, in milliseconds).</span></span> <span data-ttu-id="76858-170">Wenn der Client im Laufe der Zeit auf die gleiche Weise reaktiviert wird, ruft er den nächsten Satz von Beispielen aus der Engine ab.</span><span class="sxs-lookup"><span data-stu-id="76858-170">When the client wakes up, half way through the processing period, it pulls the next set of samples from the engine.</span></span> <span data-ttu-id="76858-171">Vor jeder Verarbeitung in der Puffer Schleife muss der Client die Menge der zu rendernden Daten ermitteln, damit die Daten den Puffer nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="76858-171">Before each processing pass in the buffering loop, the client must find out the amount of data to render so that the data does not overrun the buffer.</span></span>

<span data-ttu-id="76858-172">Audiodaten, die auf dem angegebenen Gerät abgespielt werden sollen, können durch Aktivieren der ereignisgesteuerten Pufferung verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="76858-172">Audio data to be played on the specified device can be processed by enabling event-driven buffering.</span></span> <span data-ttu-id="76858-173">Dieser Modus wird im [rendersharedeventgesteu-](rendersharedeventdriven.md) Beispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="76858-173">This mode is demonstrated in the [RenderSharedEventDriven](rendersharedeventdriven.md) sample.</span></span>

<span data-ttu-id="76858-174">Weitere Informationen zum Rendern eines Streams finden Sie unter [Rendern eines Streams](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="76858-174">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="76858-175">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="76858-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76858-176">SDK-Beispiele für die Verwendung der kernaudioapis</span><span class="sxs-lookup"><span data-stu-id="76858-176">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



