---
description: Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten von einem vom Benutzer angegebenen Eingabegerät aufzuzeichnen und in eine eindeutig benannte WAV-Datei im aktuellen Verzeichnis zu schreiben. In diesem Beispiel wird die ereignisgesteuerte Pufferung veranschaulicht.
ms.assetid: 6ff3bc23-550e-41b7-b37c-35d552b29e20
title: Capturesharedebug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 339bd02fcb94f65be558c2dce767747ebf4fab98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126905"
---
# <a name="capturesharedeventdriven"></a><span data-ttu-id="6de9d-104">Capturesharedebug</span><span class="sxs-lookup"><span data-stu-id="6de9d-104">CaptureSharedEventDriven</span></span>

<span data-ttu-id="6de9d-105">Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten von einem vom Benutzer angegebenen Eingabegerät aufzuzeichnen und in eine eindeutig benannte WAV-Datei im aktuellen Verzeichnis zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="6de9d-105">This sample application uses the Core Audio APIs to capture audio data from an input device specified by the user and writes it to a uniquely named .wav file in the current directory.</span></span> <span data-ttu-id="6de9d-106">In diesem Beispiel wird die ereignisgesteuerte Pufferung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="6de9d-106">This sample demonstrates event-driven buffering.</span></span>

<span data-ttu-id="6de9d-107">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="6de9d-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6de9d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6de9d-108">Description</span></span>](#description)
-   [<span data-ttu-id="6de9d-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6de9d-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="6de9d-110">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="6de9d-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="6de9d-111">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="6de9d-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="6de9d-112">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="6de9d-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="6de9d-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6de9d-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="6de9d-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6de9d-114">Description</span></span>

<span data-ttu-id="6de9d-115">In diesem Beispiel werden die folgenden Funktionen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="6de9d-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="6de9d-116">[Mmdevice-API](mmdevice-api.md) für die Enumeration und Auswahl von Multimedia-Geräten.</span><span class="sxs-lookup"><span data-stu-id="6de9d-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="6de9d-117">[WASAPI](wasapi.md) für Stream-Verwaltungsvorgänge, z. b. das Starten und Beenden des Streams und der Datenstrom Wechsel.</span><span class="sxs-lookup"><span data-stu-id="6de9d-117">[WASAPI](wasapi.md) for stream management operations such as starting and stopping the stream, and stream switching.</span></span>

## <a name="requirements"></a><span data-ttu-id="6de9d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6de9d-118">Requirements</span></span>



| <span data-ttu-id="6de9d-119">Produkt</span><span class="sxs-lookup"><span data-stu-id="6de9d-119">Product</span></span>                                                        | <span data-ttu-id="6de9d-120">Version</span><span class="sxs-lookup"><span data-stu-id="6de9d-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="6de9d-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="6de9d-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="6de9d-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6de9d-122">Windows 7</span></span> |
| <span data-ttu-id="6de9d-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6de9d-123">Visual Studio</span></span>                                                  | <span data-ttu-id="6de9d-124">2008</span><span class="sxs-lookup"><span data-stu-id="6de9d-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="6de9d-125">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="6de9d-125">Downloading the Sample</span></span>

<span data-ttu-id="6de9d-126">Dieses Beispiel ist in den folgenden Speicherorten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6de9d-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="6de9d-127">Standort</span><span class="sxs-lookup"><span data-stu-id="6de9d-127">Location</span></span>    | <span data-ttu-id="6de9d-128">Pfad/URL</span><span class="sxs-lookup"><span data-stu-id="6de9d-128">Path/URL</span></span>                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6de9d-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="6de9d-129">Windows SDK</span></span> | <span data-ttu-id="6de9d-130">\\Programmdateien \\ Microsoft sdgs \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ \\ audiocapturesharedeventgesteu. \\ ..</span><span class="sxs-lookup"><span data-stu-id="6de9d-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\CaptureSharedEventDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="6de9d-131">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="6de9d-131">Building the Sample</span></span>

<span data-ttu-id="6de9d-132">Führen Sie die folgenden Schritte aus, um das capturesharedeventgesteuerte-Beispiel zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="6de9d-132">To build the CaptureSharedEventDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="6de9d-133">Öffnen Sie die CMD-Shell für die Windows SDK, und wechseln Sie zum Beispiel Verzeichnis "capturesharedeventgesteuerte".</span><span class="sxs-lookup"><span data-stu-id="6de9d-133">Open the CMD shell for the Windows SDK and change to the CaptureSharedEventDriven sample directory.</span></span>
2.  <span data-ttu-id="6de9d-134">Führen Sie den Befehl `start WASAPICaptureSharedEventDriven.sln` im Verzeichnis capturesharedeventgesteuaus, um das Projekt wasapicapturesharedeventgesteuim Visual Studio-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6de9d-134">Run the command `start WASAPICaptureSharedEventDriven.sln` in the CaptureSharedEventDriven directory to open the WASAPICaptureSharedEventDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="6de9d-135">Wählen Sie im Fenster die **Debug** -oder **releaseprojektmappenkonfiguration** aus, wählen Sie das Menü **Erstellen** in der Menüleiste aus, und wählen Sie die Option **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="6de9d-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="6de9d-136">Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, hat Visual Studio keinen Zugriff auf die SDK-Buildumgebung.</span><span class="sxs-lookup"><span data-stu-id="6de9d-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="6de9d-137">In diesem Fall wird das Beispiel nur dann erstellt, wenn Sie die Umgebungsvariable "Mssdk" explizit festlegen, die in der Projektdatei "wasapicapturesharedeventcontroller. vcproj" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6de9d-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPICaptureSharedEventDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="6de9d-138">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="6de9d-138">Running the Sample</span></span>

<span data-ttu-id="6de9d-139">Wenn Sie die Demoanwendung erfolgreich erstellen, wird eine ausführbare Datei (WASAPICaptureSharedEventDriven.exe) generiert.</span><span class="sxs-lookup"><span data-stu-id="6de9d-139">If you build the demo application successfully, an executable file, WASAPICaptureSharedEventDriven.exe, is generated.</span></span> <span data-ttu-id="6de9d-140">Um es auszuführen, geben Sie `WASAPICaptureSharedEventDriven` ein Befehlsfenster ein, gefolgt von den erforderlichen oder optionalen Argumenten.</span><span class="sxs-lookup"><span data-stu-id="6de9d-140">To run it, type `WASAPICaptureSharedEventDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="6de9d-141">Im folgenden Beispiel wird gezeigt, wie Sie das Beispiel ausführen, indem Sie die Erfassungs Dauer für das standardmäßige Multimedia-Gerät angeben.</span><span class="sxs-lookup"><span data-stu-id="6de9d-141">The following example shows how to run the sample by specifying capture duration on the default multimedia device.</span></span>

`WASAPICaptureSharedEventDriven.exe -d 20 -multimedia`

<span data-ttu-id="6de9d-142">In der folgenden Tabelle werden die Argumente angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6de9d-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="6de9d-143">Argument</span><span class="sxs-lookup"><span data-stu-id="6de9d-143">Argument</span></span>        | <span data-ttu-id="6de9d-144">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6de9d-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="6de9d-145">-?</span><span class="sxs-lookup"><span data-stu-id="6de9d-145">-?</span></span>              | <span data-ttu-id="6de9d-146">Zeigt die Hilfe an.</span><span class="sxs-lookup"><span data-stu-id="6de9d-146">Shows help.</span></span>                                                |
| <span data-ttu-id="6de9d-147">-h</span><span class="sxs-lookup"><span data-stu-id="6de9d-147">-h</span></span>              | <span data-ttu-id="6de9d-148">Zeigt die Hilfe an.</span><span class="sxs-lookup"><span data-stu-id="6de9d-148">Shows help.</span></span>                                                |
| <span data-ttu-id="6de9d-149">-l</span><span class="sxs-lookup"><span data-stu-id="6de9d-149">-l</span></span>              | <span data-ttu-id="6de9d-150">Wartezeit bei der Audioerfassung in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="6de9d-150">Audio capture latency in milliseconds.</span></span>                     |
| <span data-ttu-id="6de9d-151">-d</span><span class="sxs-lookup"><span data-stu-id="6de9d-151">-d</span></span>              | <span data-ttu-id="6de9d-152">Dauer der Audioerfassung in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="6de9d-152">Audio capture duration in seconds.</span></span>                         |
| <span data-ttu-id="6de9d-153">-M</span><span class="sxs-lookup"><span data-stu-id="6de9d-153">-m</span></span>              | <span data-ttu-id="6de9d-154">Deaktiviert die Verwendung von MMCSS.</span><span class="sxs-lookup"><span data-stu-id="6de9d-154">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="6de9d-155">-Konsole</span><span class="sxs-lookup"><span data-stu-id="6de9d-155">-console</span></span>        | <span data-ttu-id="6de9d-156">Verwenden Sie das Standard Konsolen Gerät.</span><span class="sxs-lookup"><span data-stu-id="6de9d-156">Use the default console device.</span></span>                            |
| <span data-ttu-id="6de9d-157">-Kommunikation</span><span class="sxs-lookup"><span data-stu-id="6de9d-157">-communications</span></span> | <span data-ttu-id="6de9d-158">Verwenden Sie das Standard Kommunikationsgerät.</span><span class="sxs-lookup"><span data-stu-id="6de9d-158">Use the default communication device.</span></span>                      |
| <span data-ttu-id="6de9d-159">-Multimedia</span><span class="sxs-lookup"><span data-stu-id="6de9d-159">-multimedia</span></span>     | <span data-ttu-id="6de9d-160">Verwenden Sie das standardmäßige Multimedia-Gerät.</span><span class="sxs-lookup"><span data-stu-id="6de9d-160">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="6de9d-161">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="6de9d-161">-endpoint</span></span>       | <span data-ttu-id="6de9d-162">Verwenden Sie den Endpunkt Bezeichner, der im Switch-Wert angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="6de9d-162">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="6de9d-163">Wenn die Anwendung ohne Argumente ausgeführt wird, listet Sie die verfügbaren Geräte auf und fordert den Benutzer auf, ein Gerät für die Erfassungs Sitzung auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="6de9d-163">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the capture session.</span></span> <span data-ttu-id="6de9d-164">Die Standard Konsole, die Kommunikations-und multimediaregeräte sind aufgeführt, gefolgt von den Geräten und den Endpunkt bezeichern.</span><span class="sxs-lookup"><span data-stu-id="6de9d-164">The default console, communication, and multimedia devices are listed followed by devices and the endpoint identifiers.</span></span> <span data-ttu-id="6de9d-165">Wenn keine Dauer angegeben ist, wird der Audiostream vom angegebenen Gerät 10 Sekunden lang aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6de9d-165">If no duration is specified, the audio stream from the specified device is captured for 10 seconds.</span></span> <span data-ttu-id="6de9d-166">Die erfassten Daten werden von der Anwendung in eine eindeutig benannte WAV-Datei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="6de9d-166">The application writes the captured data to a uniquely named .wav file.</span></span>

<span data-ttu-id="6de9d-167">Capturesharetoventgesteuerte zeigt die ereignisgesteuerte Pufferung.</span><span class="sxs-lookup"><span data-stu-id="6de9d-167">CaptureSharedEventDriven demonstrates event-driven buffering.</span></span> <span data-ttu-id="6de9d-168">Der für dieses Beispiel instanziierte AudioClient ist so konfiguriert, dass er im freigegebenen Modus ausgeführt wird, und die Verarbeitung des Audiopuffers durch den Client wird durch Festlegen des " **audclnt \_ StreamFlags \_ EventCallback** "-Flags im Aufrufen von " [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)" gesteuert.</span><span class="sxs-lookup"><span data-stu-id="6de9d-168">The audio client instantiated for this sample is configured to run in shared mode and the client's processing of the audio buffer is made event driven by setting the **AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK** flag in the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span> <span data-ttu-id="6de9d-169">Das Beispiel zeigt, wie der Client ein Ereignis Handle für das System bereitstellen muss, indem er die [**iaudioclient:: setteventhandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6de9d-169">The sample shows how the client must provide an event handle to the system by calling the [**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) method.</span></span> <span data-ttu-id="6de9d-170">Nachdem die Aufzeichnungs Sitzung beginnt und der Stream gestartet wurde, signalisiert die Audioengine dem bereitgestellten Ereignis handle, dass der Client jedes Mal benachrichtigt wird, wenn ein Puffer für die Verarbeitung durch den Client bereit ist.</span><span class="sxs-lookup"><span data-stu-id="6de9d-170">After the capture session begins and the stream starts, the audio engine signals the supplied event handle to notify the client each time a buffer becomes ready for the client to process.</span></span> <span data-ttu-id="6de9d-171">Die Audiodaten können auch in einer Zeit Geber gesteuerten Schleife verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="6de9d-171">The audio data can also be processed in a timer-driven loop.</span></span> <span data-ttu-id="6de9d-172">Dieser Modus wird im [capturesharedtimergesteuerter](capturesharedtimerdriven.md) Beispiel herabgestuft.</span><span class="sxs-lookup"><span data-stu-id="6de9d-172">This mode is demostrated in the [CaptureSharedTimerDriven](capturesharedtimerdriven.md) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6de9d-173">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6de9d-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6de9d-174">SDK-Beispiele für die Verwendung der kernaudioapis</span><span class="sxs-lookup"><span data-stu-id="6de9d-174">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



