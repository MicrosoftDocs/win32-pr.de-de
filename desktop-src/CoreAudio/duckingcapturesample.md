---
description: Diese Beispielanwendung veranschaulicht das Öffnen und Schließen von Kommunikationsstreams und bewirkt, dass Ducking-Ereignisse auftreten, die eine Anwendung zum Implementieren der Datenstrom Dämpfung erhalten kann.
ms.assetid: 9a2131b2-ec4a-492a-a277-bd26ec8d67e5
title: Duckingcapturesample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 636fe39e8fa27beee14ab17548f5929d1d937b20
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861691"
---
# <a name="duckingcapturesample"></a><span data-ttu-id="501d1-103">Duckingcapturesample</span><span class="sxs-lookup"><span data-stu-id="501d1-103">DuckingCaptureSample</span></span>

<span data-ttu-id="501d1-104">Diese Beispielanwendung veranschaulicht das Öffnen und Schließen von Kommunikationsstreams und bewirkt, dass Ducking-Ereignisse auftreten, die eine Anwendung zum Implementieren der Datenstrom Dämpfung erhalten kann.</span><span class="sxs-lookup"><span data-stu-id="501d1-104">This sample application demonstrates opening and closing communication streams and causing ducking events that an application can get to implement stream attenuation.</span></span> <span data-ttu-id="501d1-105">Diese Anwendung implementiert einen Chat Client, der kernaudioapis verwendet, um Audiodaten von einem Kommunikationsgerät zu lesen und auf dem Ausgabegerät wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="501d1-105">This application implements a chat client that uses Core Audio APIs to read audio data from a communication device and to play it on the output device.</span></span>

<span data-ttu-id="501d1-106">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="501d1-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="501d1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="501d1-107">Description</span></span>](#description)
-   [<span data-ttu-id="501d1-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="501d1-108">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="501d1-109">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="501d1-109">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="501d1-110">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="501d1-110">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="501d1-111">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="501d1-111">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="501d1-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="501d1-112">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="501d1-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="501d1-113">Description</span></span>

<span data-ttu-id="501d1-114">In diesem Beispiel werden die folgenden Funktionen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="501d1-114">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="501d1-115">[Mmdevice-API](mmdevice-api.md) für die Enumeration und Auswahl von Multimedia-Geräten.</span><span class="sxs-lookup"><span data-stu-id="501d1-115">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="501d1-116">[WASAPI](wasapi.md) für den Zugriff auf Kommunikations Erfassungs-und Rendering-Geräte, streamverwaltungsvorgänge und Behandlung von Ducking-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="501d1-116">[WASAPI](wasapi.md) for accessing the communications capture and render device, stream management operations, and handling ducking events.</span></span>
-   <span data-ttu-id="501d1-117">[Wave-APIs](/previous-versions//ms713499(v=vs.85)) für den Zugriff auf das Kommunikationsgerät und das Erfassen von Audioeingaben.</span><span class="sxs-lookup"><span data-stu-id="501d1-117">[WAVE APIs](/previous-versions//ms713499(v=vs.85)) for accessing the communications device and capturing audio input.</span></span>

## <a name="requirements"></a><span data-ttu-id="501d1-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="501d1-118">Requirements</span></span>



| <span data-ttu-id="501d1-119">Produkt</span><span class="sxs-lookup"><span data-stu-id="501d1-119">Product</span></span>                                                        | <span data-ttu-id="501d1-120">Version</span><span class="sxs-lookup"><span data-stu-id="501d1-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="501d1-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="501d1-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="501d1-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="501d1-122">Windows 7</span></span> |
| <span data-ttu-id="501d1-123">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="501d1-123">Visual Studio 2008</span></span>                                             |           |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="501d1-124">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="501d1-124">Downloading the Sample</span></span>

<span data-ttu-id="501d1-125">Dieses Beispiel ist in den folgenden Speicherorten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="501d1-125">This sample is available in the following locations.</span></span>



| <span data-ttu-id="501d1-126">Standort</span><span class="sxs-lookup"><span data-stu-id="501d1-126">Location</span></span>    | <span data-ttu-id="501d1-127">Pfad/URL</span><span class="sxs-lookup"><span data-stu-id="501d1-127">Path/URL</span></span>                                                                                              |
|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="501d1-128">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="501d1-128">Windows SDK</span></span> | <span data-ttu-id="501d1-129">\\Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ Audiodatei \\ duckingcapturesample \\ ...</span><span class="sxs-lookup"><span data-stu-id="501d1-129">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\DuckingCaptureSample\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="501d1-130">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="501d1-130">Building the Sample</span></span>

<span data-ttu-id="501d1-131">Führen Sie die folgenden Schritte aus, um das Beispiel "duckingcapturesample" zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="501d1-131">To build the DuckingCaptureSample sample, use the following steps:</span></span>

1.  <span data-ttu-id="501d1-132">Öffnen Sie die Datei "duckingcapturesample. sln" in Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="501d1-132">Open the DuckingCaptureSample.sln in Visual Studio 2008.</span></span>
2.  <span data-ttu-id="501d1-133">Wählen Sie im Fenster die **Debug** -oder **releaseprojektmappenkonfiguration** aus, wählen Sie das Menü **Erstellen** in der Menüleiste aus, und wählen Sie die Option **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="501d1-133">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="501d1-134">Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, hat Visual Studio keinen Zugriff auf die SDK-Buildumgebung.</span><span class="sxs-lookup"><span data-stu-id="501d1-134">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="501d1-135">In diesem Fall wird das Beispiel nicht erstellt, es sei denn, Sie legen die Umgebungsvariable "Mssdk", die in der Projektdatei verwendet wird, "duckingcapturesample. vcproj" explizit fest.</span><span class="sxs-lookup"><span data-stu-id="501d1-135">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, DuckingCaptureSample.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="501d1-136">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="501d1-136">Running the Sample</span></span>

<span data-ttu-id="501d1-137">Wenn Sie die Anwendung erfolgreich erstellen, wird eine ausführbare Datei (DuckingCaptureSample.exe) generiert.</span><span class="sxs-lookup"><span data-stu-id="501d1-137">If you build the application successfully, an executable file, DuckingCaptureSample.exe, is generated.</span></span> <span data-ttu-id="501d1-138">Um es auszuführen, wählen Sie im Menü **Debuggen** die Option **Debugging starten** oder **Starten ohne Debuggen** aus, oder geben Sie `DuckingCaptureSample` ein Befehlsfenster ein</span><span class="sxs-lookup"><span data-stu-id="501d1-138">To run it, select **Start Debugging** or **Start Without Debugging** from the **Debug** menu or type `DuckingCaptureSample` in a command window.</span></span>

<span data-ttu-id="501d1-139">"Duckingcapturesample" bietet dem Benutzer zwei Implementierungen zum Erfassen von Audiodaten über das Standard Konsolen Gerät: WASAPI-und Wave-APIs.</span><span class="sxs-lookup"><span data-stu-id="501d1-139">DuckingCaptureSample provides the user with two implementations to capture audio from the default console device: WASAPI and Wave APIs.</span></span> <span data-ttu-id="501d1-140">Wählen Sie zum Starten einer Aufzeichnungs Sitzung einen Modus aus, und klicken Sie auf der Benutzeroberfläche der Anwendung auf **Start** .</span><span class="sxs-lookup"><span data-stu-id="501d1-140">To start a capture session, select a mode and click **Start** on the application's user interface.</span></span> <span data-ttu-id="501d1-141">Um die Sitzung zu beenden, klicken Sie auf **Beenden**.</span><span class="sxs-lookup"><span data-stu-id="501d1-141">To end the session, click **Stop**.</span></span> <span data-ttu-id="501d1-142">Abhängig vom Gerät, das vom Benutzer angegeben wird (Eingabe oder Ausgabe), verwendet die Anwendung die mmdevice-API, um einen Verweis auf das standardmäßige Rendering-oder Aufzeichnungs Kommunikationsgerät zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="501d1-142">Depending on the device specified by the user (input or output), the application uses MMDevice API to get a reference to the default rendering or capture communication device.</span></span> <span data-ttu-id="501d1-143">Nachdem der Benutzer eine Chatsitzung gestartet hat, führt die Anwendung die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="501d1-143">After the user starts a chat session, the application performs the following tasks:</span></span>

-   <span data-ttu-id="501d1-144">Erstellt und initialisiert einen AudioClient im ereignisgesteuerten Modus.</span><span class="sxs-lookup"><span data-stu-id="501d1-144">Creates and initializes an audio client in event-driven mode.</span></span>
-   <span data-ttu-id="501d1-145">Verknüpft den Client mit dem Ereignis handle, das signalisiert, dass die Beispiele für die Erfassung oder das Rendering bereit sind.</span><span class="sxs-lookup"><span data-stu-id="501d1-145">Associates the client with the event handle that signals that samples are ready for capture or rendering.</span></span>
-   <span data-ttu-id="501d1-146">Richtet einen Erfassungs Client und einen renderingclient für den Transport ein.</span><span class="sxs-lookup"><span data-stu-id="501d1-146">Sets up a capture client and a rendering client for the transport.</span></span>
-   <span data-ttu-id="501d1-147">Erstellt den chatthread und startet die Audioengine.</span><span class="sxs-lookup"><span data-stu-id="501d1-147">Creates the chat thread and starts the audio engine.</span></span>

<span data-ttu-id="501d1-148">Zum Erfassen von Audiodaten verwendet das Beispiel den Erfassungs Client, um die Gesamtmenge der aufgezeichneten Daten, die im Puffer verfügbar ist, zu lesen, Daten vom Standardeingabe Gerät zu lesen und das Paket freizugeben und den Puffer zum Lesen des nächsten Satzes erfasster Daten verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="501d1-148">For capturing audio data, with each processing pass, the sample uses the capture client to get the total amount of captured data that is available in the buffer, read data from the default input device, and release the packet and make the buffer available for reading the next set of captured data.</span></span>

<span data-ttu-id="501d1-149">Zum Rendern bestimmt die Anwendung die Menge der Daten, die in die Warteschlange eingereiht werden, um im Erfassungs Endpunkt Puffer wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="501d1-149">For rendering, the application determines the amount of data that is queued up to play in the capture endpoint buffer.</span></span> <span data-ttu-id="501d1-150">Entsprechend schreibt Sie in den Puffer und gibt den Puffer als Vorbereitung für den nächsten Verarbeitungs Durchlauf frei, bis alle Daten geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="501d1-150">It accordingly writes to the buffer and releases the buffer in preparation for the next processing pass until all of the data has been written.</span></span> <span data-ttu-id="501d1-151">Zum Rendern werden automatische Rahmen vorgerendert, um zu verhindern, dass die Audioengine beim Start einen Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="501d1-151">For rendering, silent frames are prerolled to prevent the audio engine from glitching on startup.</span></span> <span data-ttu-id="501d1-152">"Duckingcapturesample" zeigt auch, wie der Rendering-Stream aus dem volumemixer ausgeblendet wird.</span><span class="sxs-lookup"><span data-stu-id="501d1-152">DuckingCaptureSample also shows how to hide the render stream from the volume mixer.</span></span>

<span data-ttu-id="501d1-153">Weitere Informationen zur Datenstrom Dämpfung finden [Sie unter Verwenden eines kommunikationsgeräts](using-the-communication-device.md).</span><span class="sxs-lookup"><span data-stu-id="501d1-153">For more information about the stream attenuation feature, see [Using a Communication Device](using-the-communication-device.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="501d1-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="501d1-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="501d1-155">SDK-Beispiele für die Verwendung der kernaudioapis</span><span class="sxs-lookup"><span data-stu-id="501d1-155">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 
