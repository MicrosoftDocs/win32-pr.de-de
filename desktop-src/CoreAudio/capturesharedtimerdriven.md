---
description: Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten von einem vom Benutzer angegebenen Eingabegerät aufzuzeichnen und in eine eindeutig benannte WAV-Datei im aktuellen Verzeichnis zu schreiben. In diesem Beispiel wird die Zeit Geber gesteuerte Pufferung veranschaulicht.
ms.assetid: 06124b99-89b3-4dfa-b989-a54746ecd697
title: Capturesharedtimer-gesteuert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b635462767f22d3e31fe6deaa79b5c00911b378b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041444"
---
# <a name="capturesharedtimerdriven"></a><span data-ttu-id="aec6b-104">Capturesharedtimer-gesteuert</span><span class="sxs-lookup"><span data-stu-id="aec6b-104">CaptureSharedTimerDriven</span></span>

<span data-ttu-id="aec6b-105">Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten von einem vom Benutzer angegebenen Eingabegerät aufzuzeichnen und in eine eindeutig benannte WAV-Datei im aktuellen Verzeichnis zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="aec6b-105">This sample application uses the Core Audio APIs to capture audio data from an input device specified by the user and writes it to a uniquely named .wav file in the current directory.</span></span> <span data-ttu-id="aec6b-106">In diesem Beispiel wird die Zeit Geber gesteuerte Pufferung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="aec6b-106">This sample demonstrates timer-driven buffering.</span></span>

<span data-ttu-id="aec6b-107">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="aec6b-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="aec6b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aec6b-108">Description</span></span>](#description)
-   [<span data-ttu-id="aec6b-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aec6b-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="aec6b-110">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="aec6b-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="aec6b-111">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="aec6b-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="aec6b-112">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="aec6b-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="aec6b-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aec6b-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="aec6b-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aec6b-114">Description</span></span>

<span data-ttu-id="aec6b-115">In diesem Beispiel werden die folgenden Funktionen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="aec6b-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="aec6b-116">[Mmdevice-API](mmdevice-api.md) für die Enumeration und Auswahl von Multimedia-Geräten.</span><span class="sxs-lookup"><span data-stu-id="aec6b-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="aec6b-117">[WASAPI](wasapi.md) für Stream-Verwaltungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="aec6b-117">[WASAPI](wasapi.md) for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="aec6b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aec6b-118">Requirements</span></span>



| <span data-ttu-id="aec6b-119">Produkt</span><span class="sxs-lookup"><span data-stu-id="aec6b-119">Product</span></span>                                                        | <span data-ttu-id="aec6b-120">Version</span><span class="sxs-lookup"><span data-stu-id="aec6b-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="aec6b-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="aec6b-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="aec6b-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="aec6b-122">Windows 7</span></span> |
| <span data-ttu-id="aec6b-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="aec6b-123">Visual Studio</span></span>                                                  | <span data-ttu-id="aec6b-124">2008</span><span class="sxs-lookup"><span data-stu-id="aec6b-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="aec6b-125">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="aec6b-125">Downloading the Sample</span></span>

<span data-ttu-id="aec6b-126">Dieses Beispiel ist in den folgenden Speicherorten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="aec6b-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="aec6b-127">Standort</span><span class="sxs-lookup"><span data-stu-id="aec6b-127">Location</span></span>    | <span data-ttu-id="aec6b-128">Pfad/URL</span><span class="sxs-lookup"><span data-stu-id="aec6b-128">Path/URL</span></span>                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aec6b-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="aec6b-129">Windows SDK</span></span> | <span data-ttu-id="aec6b-130">\\Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ \\ audiocapturesharedtimer-gesteuert \\ ...</span><span class="sxs-lookup"><span data-stu-id="aec6b-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\CaptureSharedTimerDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="aec6b-131">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="aec6b-131">Building the Sample</span></span>

<span data-ttu-id="aec6b-132">Führen Sie die folgenden Schritte aus, um das capturesharedtimergesteuert-Beispiel zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="aec6b-132">To build the CaptureSharedTimerDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="aec6b-133">Öffnen Sie die CMD-Shell für die Windows SDK, und wechseln Sie zum Verzeichnis capturesharedtimer-gesteuerte Beispiele.</span><span class="sxs-lookup"><span data-stu-id="aec6b-133">Open the CMD shell for the Windows SDK and change to the CaptureSharedTimerDriven sample directory.</span></span>
2.  <span data-ttu-id="aec6b-134">Führen Sie den Befehl `start WASAPICaptureSharedTimerDriven.sln` im Verzeichnis capturesharedtimercommand aus, um das Projekt wasapicapturesharedtimer-gesteuert im Visual Studio-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="aec6b-134">Run the command `start WASAPICaptureSharedTimerDriven.sln` in the CaptureSharedTimerDriven directory to open the WASAPICaptureSharedTimerDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="aec6b-135">Wählen Sie im Fenster die **Debug** -oder **releaseprojektmappenkonfiguration** aus, wählen Sie das Menü **Erstellen** in der Menüleiste aus, und wählen Sie die Option **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="aec6b-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="aec6b-136">Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, hat Visual Studio keinen Zugriff auf die SDK-Buildumgebung.</span><span class="sxs-lookup"><span data-stu-id="aec6b-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="aec6b-137">In diesem Fall wird das Beispiel nur dann erstellt, wenn Sie die Umgebungsvariable "Mssdk" explizit festlegen, die in der Projektdatei "wasapicapturesharedtimerused. vcproj" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aec6b-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPICaptureSharedTimerDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="aec6b-138">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="aec6b-138">Running the Sample</span></span>

<span data-ttu-id="aec6b-139">Wenn Sie die Demoanwendung erfolgreich erstellen, wird eine ausführbare Datei (WASAPICaptureSharedTimerDriven.exe) generiert.</span><span class="sxs-lookup"><span data-stu-id="aec6b-139">If you build the demo application successfully, an executable file, WASAPICaptureSharedTimerDriven.exe, is generated.</span></span> <span data-ttu-id="aec6b-140">Um es auszuführen, geben Sie `WASAPICaptureSharedTimerDriven` ein Befehlsfenster ein, gefolgt von den erforderlichen oder optionalen Argumenten.</span><span class="sxs-lookup"><span data-stu-id="aec6b-140">To run it, type `WASAPICaptureSharedTimerDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="aec6b-141">Im folgenden Beispiel wird gezeigt, wie Sie das Beispiel ausführen, indem Sie die Erfassungs Dauer für das standardmäßige Multimedia-Gerät angeben.</span><span class="sxs-lookup"><span data-stu-id="aec6b-141">The following example shows how to run the sample by specifying capture duration on the default multimedia device.</span></span>

`WASAPICaptureSharedTimerDriven.exe -d 20 -multimedia`

<span data-ttu-id="aec6b-142">In der folgenden Tabelle werden die Argumente angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aec6b-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="aec6b-143">Argument</span><span class="sxs-lookup"><span data-stu-id="aec6b-143">Argument</span></span>        | <span data-ttu-id="aec6b-144">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aec6b-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="aec6b-145">-?</span><span class="sxs-lookup"><span data-stu-id="aec6b-145">-?</span></span>              | <span data-ttu-id="aec6b-146">Zeigt die Hilfe an.</span><span class="sxs-lookup"><span data-stu-id="aec6b-146">Shows help.</span></span>                                                |
| <span data-ttu-id="aec6b-147">-h</span><span class="sxs-lookup"><span data-stu-id="aec6b-147">-h</span></span>              | <span data-ttu-id="aec6b-148">Zeigt die Hilfe an.</span><span class="sxs-lookup"><span data-stu-id="aec6b-148">Shows help.</span></span>                                                |
| <span data-ttu-id="aec6b-149">-l</span><span class="sxs-lookup"><span data-stu-id="aec6b-149">-l</span></span>              | <span data-ttu-id="aec6b-150">Wartezeit bei der Audioerfassung in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="aec6b-150">Audio capture latency in milliseconds.</span></span>                     |
| <span data-ttu-id="aec6b-151">-d</span><span class="sxs-lookup"><span data-stu-id="aec6b-151">-d</span></span>              | <span data-ttu-id="aec6b-152">Dauer der Audioerfassung in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="aec6b-152">Audio capture duration in seconds.</span></span>                         |
| <span data-ttu-id="aec6b-153">-M</span><span class="sxs-lookup"><span data-stu-id="aec6b-153">-m</span></span>              | <span data-ttu-id="aec6b-154">Deaktiviert die Verwendung von MMCSS.</span><span class="sxs-lookup"><span data-stu-id="aec6b-154">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="aec6b-155">-Konsole</span><span class="sxs-lookup"><span data-stu-id="aec6b-155">-console</span></span>        | <span data-ttu-id="aec6b-156">Verwenden Sie das Standard Konsolen Gerät.</span><span class="sxs-lookup"><span data-stu-id="aec6b-156">Use the default console device.</span></span>                            |
| <span data-ttu-id="aec6b-157">-Kommunikation</span><span class="sxs-lookup"><span data-stu-id="aec6b-157">-communications</span></span> | <span data-ttu-id="aec6b-158">Verwenden Sie das Standard Kommunikationsgerät.</span><span class="sxs-lookup"><span data-stu-id="aec6b-158">Use the default communication device.</span></span>                      |
| <span data-ttu-id="aec6b-159">-Multimedia</span><span class="sxs-lookup"><span data-stu-id="aec6b-159">-multimedia</span></span>     | <span data-ttu-id="aec6b-160">Verwenden Sie das standardmäßige Multimedia-Gerät.</span><span class="sxs-lookup"><span data-stu-id="aec6b-160">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="aec6b-161">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="aec6b-161">-endpoint</span></span>       | <span data-ttu-id="aec6b-162">Verwenden Sie den Endpunkt Bezeichner, der im Switch-Wert angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="aec6b-162">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="aec6b-163">Wenn die Anwendung ohne Argumente ausgeführt wird, listet Sie die verfügbaren Geräte auf und fordert den Benutzer auf, ein Gerät für die Erfassungs Sitzung auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="aec6b-163">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the capture session.</span></span> <span data-ttu-id="aec6b-164">Die Standard Konsole, die Kommunikations-und multimediaregeräte sind aufgeführt, gefolgt von den Geräten und den Endpunkt bezeichern.</span><span class="sxs-lookup"><span data-stu-id="aec6b-164">The default console, communication, and multimedia devices are listed followed by devices and the endpoint identifiers.</span></span> <span data-ttu-id="aec6b-165">Wenn keine Dauer angegeben ist, wird der Audiostream vom angegebenen Gerät 10 Sekunden lang aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="aec6b-165">If no duration is specified, the audio stream from the specified device is captured for 10 seconds.</span></span> <span data-ttu-id="aec6b-166">Die erfassten Daten werden von der Anwendung in eine eindeutig benannte WAV-Datei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="aec6b-166">The application writes the captured data to a uniquely named .wav file.</span></span>

<span data-ttu-id="aec6b-167">Capturesharedtimer-gesteuert zeigt eine Zeit Geber gesteuerte Pufferung.</span><span class="sxs-lookup"><span data-stu-id="aec6b-167">CaptureSharedTimerDriven demonstrates timer-driven buffering.</span></span> <span data-ttu-id="aec6b-168">In diesem Modus muss der Client einen bestimmten Zeitraum (die Hälfte der Latenzzeit, die durch den Schalter-d angegeben wird, in Millisekunden) warten.</span><span class="sxs-lookup"><span data-stu-id="aec6b-168">In this mode, the client must wait for a period of time (half the latency, specified by the -d switch value, in milliseconds).</span></span> <span data-ttu-id="aec6b-169">Wenn der Client im Laufe der Zeit auf die gleiche Weise reaktiviert wird, ruft er den nächsten Satz von Beispielen aus der Engine ab.</span><span class="sxs-lookup"><span data-stu-id="aec6b-169">When the client wakes up, half way through the processing period, it pulls the next set of samples from the engine.</span></span> <span data-ttu-id="aec6b-170">Vor jeder Verarbeitung in der Puffer Schleife muss der Client die Menge der verfügbaren Aufzeichnungsdaten ermitteln, damit die Daten den Aufzeichnungs Puffer nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="aec6b-170">Before each processing pass in the buffering loop, the client must find out the amount of capture data available so that the data does not overrun the capture buffer.</span></span> <span data-ttu-id="aec6b-171">Die Audiodaten, die vom angegebenen Gerät aufgezeichnet werden, können durch Aktivieren der ereignisgesteuerten Pufferung verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="aec6b-171">The audio data that is captured from the specified device can be processed by enabling event-driven buffering.</span></span> <span data-ttu-id="aec6b-172">Dieser Modus wird im [capturesharedeventgesteu-Beispiel veranschaulicht](capturesharedeventdriven.md) .</span><span class="sxs-lookup"><span data-stu-id="aec6b-172">This mode is demonstrated in the [CaptureSharedEventDriven](capturesharedeventdriven.md) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aec6b-173">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aec6b-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aec6b-174">SDK-Beispiele für die Verwendung der kernaudioapis</span><span class="sxs-lookup"><span data-stu-id="aec6b-174">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



