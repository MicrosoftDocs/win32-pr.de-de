---
description: Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu Rendering. In diesem Beispiel wird die Zeit Geber gesteuerte Pufferung für einen renderingclient im exklusiven Modus veranschaulicht.
ms.assetid: 9dcfccd2-a709-4b4e-bbb3-4c68a15cce03
title: Renderexclusivetimer-gesteuert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6145f65de3de9425f7ba2f023a669ec0b57a3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483483"
---
# <a name="renderexclusivetimerdriven"></a><span data-ttu-id="55ed8-104">Renderexclusivetimer-gesteuert</span><span class="sxs-lookup"><span data-stu-id="55ed8-104">RenderExclusiveTimerDriven</span></span>

<span data-ttu-id="55ed8-105">Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="55ed8-105">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="55ed8-106">In diesem Beispiel wird die Zeit Geber gesteuerte Pufferung für einen renderingclient im exklusiven Modus veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="55ed8-106">This sample demonstrates timer-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="55ed8-107">Für einen Stream im exklusiven Modus gibt der Client den Endpunkt Puffer mit dem Audiogerät frei.</span><span class="sxs-lookup"><span data-stu-id="55ed8-107">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span>

<span data-ttu-id="55ed8-108">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="55ed8-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="55ed8-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="55ed8-109">Description</span></span>](#description)
-   [<span data-ttu-id="55ed8-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55ed8-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="55ed8-111">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="55ed8-111">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="55ed8-112">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="55ed8-112">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="55ed8-113">Anzeigen der Beispieldateien</span><span class="sxs-lookup"><span data-stu-id="55ed8-113">View the Sample Files</span></span>](#view-the-sample-files)
-   [<span data-ttu-id="55ed8-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="55ed8-114">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="55ed8-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55ed8-115">Description</span></span>

<span data-ttu-id="55ed8-116">In diesem Beispiel werden die folgenden Funktionen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="55ed8-116">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="55ed8-117">[Mmdevice-API](mmdevice-api.md) für die Enumeration und Auswahl von Multimedia-Geräten.</span><span class="sxs-lookup"><span data-stu-id="55ed8-117">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="55ed8-118">WASAPI für Stream-Verwaltungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="55ed8-118">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="55ed8-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55ed8-119">Requirements</span></span>



| <span data-ttu-id="55ed8-120">Produkt</span><span class="sxs-lookup"><span data-stu-id="55ed8-120">Product</span></span>                                                        | <span data-ttu-id="55ed8-121">Version</span><span class="sxs-lookup"><span data-stu-id="55ed8-121">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="55ed8-122">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="55ed8-122">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="55ed8-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="55ed8-123">Windows 7</span></span> |
| <span data-ttu-id="55ed8-124">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="55ed8-124">Visual Studio</span></span>                                                  | <span data-ttu-id="55ed8-125">2008</span><span class="sxs-lookup"><span data-stu-id="55ed8-125">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="55ed8-126">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="55ed8-126">Downloading the Sample</span></span>

<span data-ttu-id="55ed8-127">Dieses Beispiel ist in den folgenden Speicherorten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="55ed8-127">This sample is available in the following locations.</span></span>



| <span data-ttu-id="55ed8-128">Standort</span><span class="sxs-lookup"><span data-stu-id="55ed8-128">Location</span></span>    | <span data-ttu-id="55ed8-129">Pfad/URL</span><span class="sxs-lookup"><span data-stu-id="55ed8-129">Path/URL</span></span>                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55ed8-130">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="55ed8-130">Windows SDK</span></span> | <span data-ttu-id="55ed8-131">\\Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ \\ multimedioneaudiodatei \\ renderexclusivetimer-gesteuert \\ ...</span><span class="sxs-lookup"><span data-stu-id="55ed8-131">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderExclusiveTimerDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="55ed8-132">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="55ed8-132">Building the Sample</span></span>

<span data-ttu-id="55ed8-133">Führen Sie die folgenden Schritte aus, um das renderexclusivetimergesteuert-Beispiel zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="55ed8-133">To build the RenderExclusiveTimerDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="55ed8-134">Öffnen Sie die CMD-Shell für die Windows SDK, und wechseln Sie zum Verzeichnis "renderexclusivetimergesteudirectory".</span><span class="sxs-lookup"><span data-stu-id="55ed8-134">Open the CMD shell for the Windows SDK and change to the RenderExclusiveTimerDriven sample directory.</span></span>
2.  <span data-ttu-id="55ed8-135">Führen Sie den Befehl `start WASAPIRenderExclusiveTimerDriven.sln` im Verzeichnis "renderexclusivetimercommand" aus, um das Projekt "wasapirienderexclusivetimer-gesteuert" im Visual Studio-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="55ed8-135">Run the command `start WASAPIRenderExclusiveTimerDriven.sln` in the RenderExclusiveTimerDriven directory to open the WASAPIRenderExclusiveTimerDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="55ed8-136">Wählen Sie im Fenster die **Debug** -oder **releaseprojektmappenkonfiguration** aus, wählen Sie das Menü **Erstellen** in der Menüleiste aus, und wählen Sie die Option **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="55ed8-136">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="55ed8-137">Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, hat Visual Studio keinen Zugriff auf die SDK-Buildumgebung.</span><span class="sxs-lookup"><span data-stu-id="55ed8-137">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="55ed8-138">In diesem Fall wird das Beispiel nicht erstellt, es sei denn, Sie legen die Umgebungsvariable "Mssdk", die in der Projektdatei verwendet wird, "wasapirienderexclusivetimercontroller. vcproj" explizit fest.</span><span class="sxs-lookup"><span data-stu-id="55ed8-138">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderExclusiveTimerDriven.vcproj.</span></span>

## <a name="view-the-sample-files"></a><span data-ttu-id="55ed8-139">Anzeigen der Beispieldateien</span><span class="sxs-lookup"><span data-stu-id="55ed8-139">View the Sample Files</span></span>

<span data-ttu-id="55ed8-140">Wenn Sie die Demoanwendung erfolgreich erstellen, wird eine ausführbare Datei (WASAPIRenderExclusiveTimerDriven.exe) generiert.</span><span class="sxs-lookup"><span data-stu-id="55ed8-140">If you build the demo application successfully, an executable file, WASAPIRenderExclusiveTimerDriven.exe, is generated.</span></span> <span data-ttu-id="55ed8-141">Um es auszuführen, geben Sie `WASAPIRenderExclusiveTimerDriven` ein Befehlsfenster ein, gefolgt von den erforderlichen oder optionalen Argumenten.</span><span class="sxs-lookup"><span data-stu-id="55ed8-141">To run it, type `WASAPIRenderExclusiveTimerDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="55ed8-142">Im folgenden Beispiel wird gezeigt, wie das Beispiel mit einem angegeben wird, indem die Wiedergabedauer auf dem Standard Konsolen Gerät angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="55ed8-142">The following example shows how to run the sample by a specifying playback duration on the default console device.</span></span>

`WASAPIRenderExclusiveTimerDriven.exe -d 20 -console`

<span data-ttu-id="55ed8-143">In der folgenden Tabelle werden die Argumente angezeigt.</span><span class="sxs-lookup"><span data-stu-id="55ed8-143">The following table shows the arguments.</span></span>

| <span data-ttu-id="55ed8-144">Argument</span><span class="sxs-lookup"><span data-stu-id="55ed8-144">Argument</span></span>        | <span data-ttu-id="55ed8-145">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55ed8-145">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="55ed8-146">-?</span><span class="sxs-lookup"><span data-stu-id="55ed8-146">-?</span></span>              | <span data-ttu-id="55ed8-147">Zeigt die Hilfe an.</span><span class="sxs-lookup"><span data-stu-id="55ed8-147">Shows help.</span></span>                                                |
| <span data-ttu-id="55ed8-148">-h</span><span class="sxs-lookup"><span data-stu-id="55ed8-148">-h</span></span>              | <span data-ttu-id="55ed8-149">Zeigt die Hilfe an.</span><span class="sxs-lookup"><span data-stu-id="55ed8-149">Shows help.</span></span>                                                |
| <span data-ttu-id="55ed8-150">-f</span><span class="sxs-lookup"><span data-stu-id="55ed8-150">-f</span></span>              | <span data-ttu-id="55ed8-151">Sinuswellen Frequenz in Hz.</span><span class="sxs-lookup"><span data-stu-id="55ed8-151">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="55ed8-152">-l</span><span class="sxs-lookup"><span data-stu-id="55ed8-152">-l</span></span>              | <span data-ttu-id="55ed8-153">Wartezeit für audiorendering in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="55ed8-153">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="55ed8-154">-d</span><span class="sxs-lookup"><span data-stu-id="55ed8-154">-d</span></span>              | <span data-ttu-id="55ed8-155">Sinuswellen Dauer in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="55ed8-155">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="55ed8-156">-M</span><span class="sxs-lookup"><span data-stu-id="55ed8-156">-m</span></span>              | <span data-ttu-id="55ed8-157">Deaktiviert die Verwendung von MMCSS.</span><span class="sxs-lookup"><span data-stu-id="55ed8-157">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="55ed8-158">-Konsole</span><span class="sxs-lookup"><span data-stu-id="55ed8-158">-console</span></span>        | <span data-ttu-id="55ed8-159">Verwenden Sie das Standard Konsolen Gerät.</span><span class="sxs-lookup"><span data-stu-id="55ed8-159">Use the default console device.</span></span>                            |
| <span data-ttu-id="55ed8-160">-Kommunikation</span><span class="sxs-lookup"><span data-stu-id="55ed8-160">-communications</span></span> | <span data-ttu-id="55ed8-161">Verwenden Sie das Standard Kommunikationsgerät.</span><span class="sxs-lookup"><span data-stu-id="55ed8-161">Use the default communication device.</span></span>                      |
| <span data-ttu-id="55ed8-162">-Multimedia</span><span class="sxs-lookup"><span data-stu-id="55ed8-162">-multimedia</span></span>     | <span data-ttu-id="55ed8-163">Verwenden Sie das standardmäßige Multimedia-Gerät.</span><span class="sxs-lookup"><span data-stu-id="55ed8-163">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="55ed8-164">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="55ed8-164">-endpoint</span></span>       | <span data-ttu-id="55ed8-165">Verwenden Sie den Endpunkt Bezeichner, der im Switch-Wert angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="55ed8-165">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="55ed8-166">Wenn die Anwendung ohne Argumente ausgeführt wird, listet Sie die verfügbaren Geräte auf und fordert den Benutzer auf, ein Gerät für die renderingsitzung auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="55ed8-166">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="55ed8-167">Nachdem der Benutzer ein Gerät angegeben hat, rendert die Anwendung eine Sinuswelle bei 440 Hz für 10 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="55ed8-167">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="55ed8-168">Diese Werte können durch Angabe von "-f" und "-d"-Schalter Werte geändert werden.</span><span class="sxs-lookup"><span data-stu-id="55ed8-168">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="55ed8-169">Renderexclusivetimer-gesteuert zeigt eine Zeit Geber gesteuerte Pufferung.</span><span class="sxs-lookup"><span data-stu-id="55ed8-169">RenderExclusiveTimerDriven demonstrates timer-driven buffering.</span></span> <span data-ttu-id="55ed8-170">In diesem Modus muss der Client einen bestimmten Zeitraum (die Hälfte der Latenzzeit, die durch den Schalter-d angegeben wird, in Millisekunden) warten.</span><span class="sxs-lookup"><span data-stu-id="55ed8-170">In this mode, the client must wait for a period of time (half the latency, specified by the -d switch value, in milliseconds).</span></span> <span data-ttu-id="55ed8-171">Wenn der Client im Laufe der Zeit auf die gleiche Weise reaktiviert wird, ruft er den nächsten Satz von Beispielen aus der Engine ab.</span><span class="sxs-lookup"><span data-stu-id="55ed8-171">When the client wakes up, half way through the processing period, it pulls the next set of samples from the engine.</span></span> <span data-ttu-id="55ed8-172">Vor jeder Verarbeitung in der Puffer Schleife muss der Client die Menge der zu rendernden Daten ermitteln, damit die Daten den Puffer nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="55ed8-172">Before each processing pass in the buffering loop, the client must find out the amount of data to render so that the data does not overrun the buffer.</span></span>

<span data-ttu-id="55ed8-173">Audiodaten, die auf dem angegebenen Gerät abgespielt werden sollen, können durch Aktivieren der ereignisgesteuerten Pufferung verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="55ed8-173">Audio data to be played on the specified device can be processed by enabling event-driven buffering.</span></span> <span data-ttu-id="55ed8-174">Dieser Modus wird im renderexclusivetimergesteuert-Beispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="55ed8-174">This mode is demonstrated in the RenderExclusiveTimerDriven sample.</span></span>

<span data-ttu-id="55ed8-175">Weitere Informationen zum Rendern eines Streams finden Sie unter [Rendern eines Streams](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="55ed8-175">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="55ed8-176">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="55ed8-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55ed8-177">SDK-Beispiele für die Verwendung der kernaudioapis</span><span class="sxs-lookup"><span data-stu-id="55ed8-177">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



