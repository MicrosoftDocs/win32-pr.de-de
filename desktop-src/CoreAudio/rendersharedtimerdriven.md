---
description: Diese Beispielanwendung, die die zeitgebergesteuerte Pufferung veranschaulicht, verwendet die Core Audio-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu rendern.
ms.assetid: eae7d896-77ef-4340-bd77-1f3333166987
title: RenderSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89d2814f359668f8724d3deb65a7c2a9eeff5b06
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410093"
---
# <a name="rendersharedtimerdriven"></a><span data-ttu-id="c0ff8-103">RenderSharedTimerDriven</span><span class="sxs-lookup"><span data-stu-id="c0ff8-103">RenderSharedTimerDriven</span></span>

<span data-ttu-id="c0ff8-104">Diese Beispielanwendung verwendet die Core Audio-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu rendern.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-104">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="c0ff8-105">In diesem Beispiel wird die zeitgebergesteuerte Pufferung für einen Renderingclient im freigegebenen Modus veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-105">This sample demonstrates timer-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="c0ff8-106">Für einen Stream im freigegebenen Modus teilt sich der Client den Endpunktpuffer mit der Audio-Engine.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-106">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span>

<span data-ttu-id="c0ff8-107">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="c0ff8-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c0ff8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0ff8-108">Description</span></span>](#description)
-   [<span data-ttu-id="c0ff8-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0ff8-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="c0ff8-110">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c0ff8-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="c0ff8-111">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c0ff8-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="c0ff8-112">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c0ff8-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="c0ff8-113">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c0ff8-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="c0ff8-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0ff8-114">Description</span></span>

<span data-ttu-id="c0ff8-115">In diesem Beispiel werden die folgenden Features veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="c0ff8-116">[MMDevice-API](mmdevice-api.md) für multimediale Geräteenumeration und -auswahl.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="c0ff8-117">WASAPI für Datenstromverwaltungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-117">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0ff8-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c0ff8-118">Requirements</span></span>



| <span data-ttu-id="c0ff8-119">Produkt</span><span class="sxs-lookup"><span data-stu-id="c0ff8-119">Product</span></span>                                                        | <span data-ttu-id="c0ff8-120">Version</span><span class="sxs-lookup"><span data-stu-id="c0ff8-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="c0ff8-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="c0ff8-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="c0ff8-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0ff8-122">Windows 7</span></span> |
| <span data-ttu-id="c0ff8-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c0ff8-123">Visual Studio</span></span>                                                  | <span data-ttu-id="c0ff8-124">2008</span><span class="sxs-lookup"><span data-stu-id="c0ff8-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="c0ff8-125">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c0ff8-125">Downloading the Sample</span></span>

<span data-ttu-id="c0ff8-126">Dieses Beispiel ist an den folgenden Speicherorten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="c0ff8-127">Standort</span><span class="sxs-lookup"><span data-stu-id="c0ff8-127">Location</span></span>    | <span data-ttu-id="c0ff8-128">Pfad/URL</span><span class="sxs-lookup"><span data-stu-id="c0ff8-128">Path/URL</span></span>                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0ff8-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="c0ff8-129">Windows SDK</span></span> | <span data-ttu-id="c0ff8-130">\\Programme \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Multimedia Audio \\ \\ \\ RenderSharedTimerDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="c0ff8-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderSharedTimerDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="c0ff8-131">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c0ff8-131">Building the Sample</span></span>

<span data-ttu-id="c0ff8-132">Führen Sie die folgenden Schritte aus, um das RenderSharedTimerDriven-Beispiel zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="c0ff8-132">To build the RenderSharedTimerDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="c0ff8-133">Öffnen Sie die CMD-Shell für die Windows SDK, und wechseln Sie zum Beispielverzeichnis RenderSharedTimerDriven.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-133">Open the CMD shell for the Windows SDK and change to the RenderSharedTimerDriven sample directory.</span></span>
2.  <span data-ttu-id="c0ff8-134">Führen Sie den Befehl `start WASAPIRenderSharedTimerDriven.sln` im Verzeichnis RenderSharedTimerDriven aus, um das Projekt WASAPIRenderSharedTimerDriven im fenster Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-134">Run the command `start WASAPIRenderSharedTimerDriven.sln` in the RenderSharedTimerDriven directory to open the WASAPIRenderSharedTimerDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="c0ff8-135">Wählen Sie im Fenster die Konfiguration **Debug-** oder **Releaselösung** aus, wählen Sie in der Menüleiste das Menü **Erstellen** und dann die Option **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="c0ff8-136">Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, haben Visual Studio keinen Zugriff auf die SDK-Buildumgebung.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="c0ff8-137">In diesem Fall wird das Beispiel nur erstellt, wenn Sie die Umgebungsvariable MSSdk explizit festlegen, die in der Projektdatei WASAPIRenderSharedTimerDriven.vcproj verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderSharedTimerDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="c0ff8-138">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c0ff8-138">Running the Sample</span></span>

<span data-ttu-id="c0ff8-139">Wenn Sie die Demoanwendung erfolgreich erstellen, wird eine ausführbare Datei WASAPIRenderSharedTimerDriven.exe generiert.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-139">If you build the demo application successfully, an executable file, WASAPIRenderSharedTimerDriven.exe, is generated.</span></span> <span data-ttu-id="c0ff8-140">Geben Sie zum Ausführen `WASAPIRenderSharedTimerDriven` ein Befehlsfenster gefolgt von erforderlichen oder optionalen Argumenten ein.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-140">To run it, type `WASAPIRenderSharedTimerDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="c0ff8-141">Das folgende Beispiel zeigt, wie das Beispiel ausgeführt wird, indem die Wiedergabedauer auf dem Standardmäßigen Multimediagerät angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-141">The following example shows how to run the sample by specifying playback duration on the default multimedia device.</span></span>

`WASAPIRenderSharedTimerDriven.exe -d 20 -multimedia`

<span data-ttu-id="c0ff8-142">In der folgenden Tabelle sind die Argumente aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="c0ff8-143">Argument</span><span class="sxs-lookup"><span data-stu-id="c0ff8-143">Argument</span></span>        | <span data-ttu-id="c0ff8-144">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0ff8-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="c0ff8-145">-?</span><span class="sxs-lookup"><span data-stu-id="c0ff8-145">-?</span></span>              | <span data-ttu-id="c0ff8-146">Zeigt Hilfe an.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-146">Shows help.</span></span>                                                |
| <span data-ttu-id="c0ff8-147">-H</span><span class="sxs-lookup"><span data-stu-id="c0ff8-147">-h</span></span>              | <span data-ttu-id="c0ff8-148">Zeigt Hilfe an.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-148">Shows help.</span></span>                                                |
| <span data-ttu-id="c0ff8-149">-f</span><span class="sxs-lookup"><span data-stu-id="c0ff8-149">-f</span></span>              | <span data-ttu-id="c0ff8-150">Sinusfrequenz in Hz.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-150">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="c0ff8-151">-l</span><span class="sxs-lookup"><span data-stu-id="c0ff8-151">-l</span></span>              | <span data-ttu-id="c0ff8-152">Audiorenderinglatenz in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-152">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="c0ff8-153">-d</span><span class="sxs-lookup"><span data-stu-id="c0ff8-153">-d</span></span>              | <span data-ttu-id="c0ff8-154">Sinus-Wellendauer in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-154">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="c0ff8-155">-M</span><span class="sxs-lookup"><span data-stu-id="c0ff8-155">-m</span></span>              | <span data-ttu-id="c0ff8-156">Deaktiviert die Verwendung von MMCSS.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-156">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="c0ff8-157">-console</span><span class="sxs-lookup"><span data-stu-id="c0ff8-157">-console</span></span>        | <span data-ttu-id="c0ff8-158">Verwenden Sie das Standardkonsolengerät.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-158">Use the default console device.</span></span>                            |
| <span data-ttu-id="c0ff8-159">-communications</span><span class="sxs-lookup"><span data-stu-id="c0ff8-159">-communications</span></span> | <span data-ttu-id="c0ff8-160">Verwenden Sie das Standardkommunikationsgerät.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-160">Use the default communication device.</span></span>                      |
| <span data-ttu-id="c0ff8-161">-multimedia</span><span class="sxs-lookup"><span data-stu-id="c0ff8-161">-multimedia</span></span>     | <span data-ttu-id="c0ff8-162">Verwenden Sie das Standardmäßige Multimediagerät.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-162">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="c0ff8-163">-endpoint</span><span class="sxs-lookup"><span data-stu-id="c0ff8-163">-endpoint</span></span>       | <span data-ttu-id="c0ff8-164">Verwenden Sie den Endpunktbezeichner, der im Switchwert angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-164">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="c0ff8-165">Wenn die Anwendung ohne Argumente ausgeführt wird, listet sie die verfügbaren Geräte auf und fordert den Benutzer auf, ein Gerät für die Renderingsitzung auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="c0ff8-166">Nachdem der Benutzer ein Gerät angegeben hat, rendert die Anwendung eine Sinusbewegung bei 440 Hz für 10 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-166">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="c0ff8-167">Diese Werte können durch Angeben der Schalterwerte -f und -d geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-167">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="c0ff8-168">RenderSharedTimerDriven veranschaulicht die zeitgebergesteuerte Pufferung.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-168">RenderSharedTimerDriven demonstrates timer-driven buffering.</span></span> <span data-ttu-id="c0ff8-169">In diesem Modus muss der Client einen Zeitraum warten (die Hälfte der Latenz, angegeben durch den Schalterwert -d, in Millisekunden).</span><span class="sxs-lookup"><span data-stu-id="c0ff8-169">In this mode, the client must wait for a period of time (half the latency, specified by the -d switch value, in milliseconds).</span></span> <span data-ttu-id="c0ff8-170">Wenn der Client reaktiviert wird, wird in der Mitte des Verarbeitungszeitraums die nächste Gruppe von Stichproben aus der Engine abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-170">When the client wakes up, half way through the processing period, it pulls the next set of samples from the engine.</span></span> <span data-ttu-id="c0ff8-171">Bevor jeder Verarbeitungsdurchlauf in der Pufferungsschleife erfolgt, muss der Client die zu rendernde Datenmenge ermitteln, damit die Daten den Puffer nicht überlaufen.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-171">Before each processing pass in the buffering loop, the client must find out the amount of data to render so that the data does not overrun the buffer.</span></span>

<span data-ttu-id="c0ff8-172">Audiodaten, die auf dem angegebenen Gerät wiedergegeben werden sollen, können verarbeitet werden, indem die ereignisgesteuerte Pufferung aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-172">Audio data to be played on the specified device can be processed by enabling event-driven buffering.</span></span> <span data-ttu-id="c0ff8-173">Dieser Modus wird im [RenderSharedEventDriven-Beispiel](rendersharedeventdriven.md) veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-173">This mode is demonstrated in the [RenderSharedEventDriven](rendersharedeventdriven.md) sample.</span></span>

<span data-ttu-id="c0ff8-174">Weitere Informationen zum Rendern eines Streams finden Sie unter [Rendern eines Streams.](rendering-a-stream.md)</span><span class="sxs-lookup"><span data-stu-id="c0ff8-174">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0ff8-175">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c0ff8-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0ff8-176">SDK-Beispiele, die die Kernaudio-APIs verwenden</span><span class="sxs-lookup"><span data-stu-id="c0ff8-176">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



