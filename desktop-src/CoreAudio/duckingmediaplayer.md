---
description: In dieser Beispielanwendung wird die Datenstrom Dämpfung durch Implementieren eines Media Player veranschaulicht, der das vom System bereitgestellte standardmäßige debugierungsverhalten anzeigt, die Verarbeitung von Ducking-Ereignissen durchführt und die benutzerdefinierte Handhabung implementiert, wenn Ducking-Ereignisse empfangen werden.
ms.assetid: 667c8751-1d17-4b59-8ced-ed5f0c333ae9
title: Duckingmediaplayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86952f1aa7b81c9a7dc711f0c4f36fc8531bd63
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106367272"
---
# <a name="duckingmediaplayer"></a><span data-ttu-id="d2343-103">Duckingmediaplayer</span><span class="sxs-lookup"><span data-stu-id="d2343-103">DuckingMediaPlayer</span></span>

<span data-ttu-id="d2343-104">In dieser Beispielanwendung wird die Datenstrom Dämpfung durch Implementieren eines Media Player veranschaulicht, der das vom System bereitgestellte standardmäßige debugierungsverhalten anzeigt, die Verarbeitung von Ducking-Ereignissen durchführt und die benutzerdefinierte Handhabung implementiert, wenn Ducking-Ereignisse empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="d2343-104">This sample application demonstrates stream attenuation by implementing a media player that shows the default attenuation behavior provided by the system, opts out of ducking events, and implements custom handling when ducking events are received.</span></span> <span data-ttu-id="d2343-105">Dieses Beispiel muss in der Konturierung mit " [duckingcapturesample](duckingcapturesample.md)" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d2343-105">This sample must be used in conjuction with [DuckingCaptureSample](duckingcapturesample.md).</span></span> <span data-ttu-id="d2343-106">Weitere Informationen über das ducken oder die streamdämpfung finden Sie unter [standardmäßige Ducking](stream-attenuation.md)-Darstellung.</span><span class="sxs-lookup"><span data-stu-id="d2343-106">For more information about ducking or stream attenuation, see [Default Ducking Experience](stream-attenuation.md).</span></span>

<span data-ttu-id="d2343-107">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="d2343-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d2343-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2343-108">Description</span></span>](#description)
-   [<span data-ttu-id="d2343-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2343-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="d2343-110">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d2343-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="d2343-111">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="d2343-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="d2343-112">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d2343-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="d2343-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d2343-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="d2343-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2343-114">Description</span></span>

<span data-ttu-id="d2343-115">In diesem Beispiel werden die folgenden Funktionen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d2343-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="d2343-116">DirectShow zum Wiedergeben einer Mediendatei.</span><span class="sxs-lookup"><span data-stu-id="d2343-116">DirectShow to play a media file.</span></span>
-   <span data-ttu-id="d2343-117">[WASAPI](wasapi.md) für die streamverwaltung und Behandlung von Ducking-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="d2343-117">[WASAPI](wasapi.md) for stream management and handling ducking events.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2343-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2343-118">Requirements</span></span>



| <span data-ttu-id="d2343-119">Produkt</span><span class="sxs-lookup"><span data-stu-id="d2343-119">Product</span></span>                                                        | <span data-ttu-id="d2343-120">Version</span><span class="sxs-lookup"><span data-stu-id="d2343-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="d2343-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="d2343-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="d2343-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d2343-122">Windows 7</span></span> |
| <span data-ttu-id="d2343-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d2343-123">Visual Studio</span></span>                                                  | <span data-ttu-id="d2343-124">2008</span><span class="sxs-lookup"><span data-stu-id="d2343-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="d2343-125">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d2343-125">Downloading the Sample</span></span>

<span data-ttu-id="d2343-126">Dieses Beispiel ist in den folgenden Speicherorten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d2343-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="d2343-127">Standort</span><span class="sxs-lookup"><span data-stu-id="d2343-127">Location</span></span>    | <span data-ttu-id="d2343-128">Pfad/URL</span><span class="sxs-lookup"><span data-stu-id="d2343-128">Path/URL</span></span>                                                                                            |
|-------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2343-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="d2343-129">Windows SDK</span></span> | <span data-ttu-id="d2343-130">\\Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ \\ audiooneingmediaplayer \\ ...</span><span class="sxs-lookup"><span data-stu-id="d2343-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\DuckingMediaPlayer\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="d2343-131">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d2343-131">Building the Sample</span></span>

<span data-ttu-id="d2343-132">Führen Sie die folgenden Schritte aus, um das Beispiel "duckingmediaplayer" zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="d2343-132">To build the DuckingMediaPlayer sample, use the following steps:</span></span>

1.  <span data-ttu-id="d2343-133">Öffnen Sie die Datei "duckingmediaplayer. sln" in Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="d2343-133">Open the DuckingMediaPlayer.sln in Visual Studio 2008.</span></span>
2.  <span data-ttu-id="d2343-134">Wählen Sie im Fenster die **Debug** -oder **releaseprojektmappenkonfiguration** aus, wählen Sie das Menü **Erstellen** in der Menüleiste aus, und wählen Sie die Option **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="d2343-134">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="d2343-135">Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, hat Visual Studio keinen Zugriff auf die SDK-Buildumgebung.</span><span class="sxs-lookup"><span data-stu-id="d2343-135">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="d2343-136">In diesem Fall wird das Beispiel nicht erstellt, es sei denn, Sie legen die Umgebungsvariable "Mssdk", die in der Projektdatei verwendet wird, "duckingmediaplayer. vcproj" explizit fest.</span><span class="sxs-lookup"><span data-stu-id="d2343-136">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, DuckingMediaPlayer.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="d2343-137">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d2343-137">Running the Sample</span></span>

<span data-ttu-id="d2343-138">Wenn Sie die Anwendung erfolgreich erstellen, wird eine ausführbare Datei (DuckingMediaPlayer.exe) generiert.</span><span class="sxs-lookup"><span data-stu-id="d2343-138">If you build the application successfully, an executable file, DuckingMediaPlayer.exe, is generated.</span></span> <span data-ttu-id="d2343-139">Um es auszuführen, wählen Sie im Menü **Debuggen** die Option **Debugging starten** oder **Starten ohne Debuggen** aus, oder geben Sie `DuckingMediaPlayer` ein Befehlsfenster ein</span><span class="sxs-lookup"><span data-stu-id="d2343-139">To run it, select **Start Debugging** or **Start Without Debugging** from the **Debug** menu or type `DuckingMediaPlayer` in a command window.</span></span>

<span data-ttu-id="d2343-140">Um eine Demonstration von Ducking anzuzeigen, müssen Sie "duckingmediaplayer" und "duckingcapturesample" gleichzeitig ausführen.</span><span class="sxs-lookup"><span data-stu-id="d2343-140">To view a demonstration of ducking, you must execute DuckingMediaPlayer and DuckingCaptureSample simultaneously.</span></span> <span data-ttu-id="d2343-141">"Duckingcapturesample" öffnet einen Kommunikationsstream und signalisiert dem System, ein Ducking-Ereignis zu generieren.</span><span class="sxs-lookup"><span data-stu-id="d2343-141">DuckingCaptureSample opens a communication stream and signals the system to generate a ducking event.</span></span> <span data-ttu-id="d2343-142">Der duckingmediaplayer wird vom System benachrichtigt, wenn ein duckereignis auftritt, und der Media Player führt die vom Benutzer angeforderte Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="d2343-142">The DuckingMediaPlayer is notified by the system when a ducking event occurs, and the media player performs the action requested by the user.</span></span>

<span data-ttu-id="d2343-143">So deaktivieren Sie das Ducking-Verhalten:</span><span class="sxs-lookup"><span data-stu-id="d2343-143">To disable ducking behavior:</span></span>

1.  <span data-ttu-id="d2343-144">Wählen Sie im Fenster "duckingcapturesample" die Option **Standardeingabe Gerät verwenden** aus, und klicken Sie auf **starten** , um eine Aufzeichnungs Sitzung vom Kommunikationsgerät zu starten.</span><span class="sxs-lookup"><span data-stu-id="d2343-144">On the DuckingCaptureSample window, select **Use default input device**, and click **Start** to start a capture session from the communication device.</span></span>
2.  <span data-ttu-id="d2343-145">Wählen Sie auf dem duckingmediaplayer eine Mediendatei aus, die Sie wiedergeben möchten, und geben Sie die Option für das ducken als **Abmelde** Option an.</span><span class="sxs-lookup"><span data-stu-id="d2343-145">On the DuckingMediaPlayer, select a media file to play, and specify the ducking option as **Opt out of Ducking**.</span></span>

<span data-ttu-id="d2343-146">Beachten Sie, dass die Mediendatei ohne Unterbrechung wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d2343-146">Notice that the media file is played without any interruption.</span></span> <span data-ttu-id="d2343-147">Die vom System generierten Ereignisse beim Öffnen des Kommunikationsstreams werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d2343-147">The events generated by the system when the communication stream opened are ignored.</span></span>

<span data-ttu-id="d2343-148">Gehen Sie folgendermaßen vor, um das vom System bereitgestellte Standardverhalten zu veranschaulichen:</span><span class="sxs-lookup"><span data-stu-id="d2343-148">To demonstrate the default ducking behavior provided by the system, do the following:</span></span>

1.  <span data-ttu-id="d2343-149">Wählen Sie in der Systemsteuerung die Option **Sounds** aus.</span><span class="sxs-lookup"><span data-stu-id="d2343-149">Select the **Sounds** option from the control panel.</span></span> <span data-ttu-id="d2343-150">Wählen Sie auf der Registerkarte **Kommunikation** **die Option verringern Sie die Anzahl anderer Sounds um 80% aus**.</span><span class="sxs-lookup"><span data-stu-id="d2343-150">On the **Communications** tab, select **Reduce the volume of other sounds by 80%**.</span></span>
2.  <span data-ttu-id="d2343-151">Wählen Sie im Fenster "duckingcapturesample" die Option **Standardeingabe Gerät verwenden** aus, und klicken Sie auf **starten** , um eine Aufzeichnungs Sitzung vom Kommunikationsgerät zu starten.</span><span class="sxs-lookup"><span data-stu-id="d2343-151">On the DuckingCaptureSample window, select **Use default input device**, and click **Start** to start a capture session from the communication device.</span></span>
3.  <span data-ttu-id="d2343-152">Wählen Sie auf dem duckingmediaplayer eine Mediendatei aus, die Sie wiedergeben möchten, ohne eine der Optionen für das ducken auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="d2343-152">On the DuckingMediaPlayer, select a media file to play, without choosing any of the ducking options.</span></span>
4.  <span data-ttu-id="d2343-153">Klicken Sie im Fenster "duckingcapturesample" auf " **Abbrechen** ", um den Kommunikationsstream zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="d2343-153">On the DuckingCaptureSample window, click **Stop** to stop the communication stream.</span></span>

<span data-ttu-id="d2343-154">Beachten Sie, dass beim Öffnen des Kommunikationsstreams durch "duckingcapturesample" die von duckingmediaplayer wiedergegebene Mediendatei ohne Unterbrechung abgespielt wird, die Volumeebene jedoch verringert wird.</span><span class="sxs-lookup"><span data-stu-id="d2343-154">Notice that when DuckingCaptureSample opens the communication stream, the media file played by DuckingMediaPlayer plays without interruption, but the volume level is lowered.</span></span> <span data-ttu-id="d2343-155">Wenn die Kommunikationssitzung angehalten wird, wird das Volume auf die ursprüngliche Einstellung zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="d2343-155">When the communication session is stopped, the volume is reset to the original setting.</span></span> <span data-ttu-id="d2343-156">Dieses streamdäsierungsverhalten ist das Standardverhalten, das vom System implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="d2343-156">This stream attenuation behavior is the default ducking behavior implemented by the system.</span></span>

<span data-ttu-id="d2343-157">So zeigen Sie ein angepasstes, vom Media Player implementiertes duckverhalten an:</span><span class="sxs-lookup"><span data-stu-id="d2343-157">To view a customized ducking behavior implemented by the media player:</span></span>

1.  <span data-ttu-id="d2343-158">Wählen Sie im Fenster "duckingcapturesample" die Option **Standardeingabe Gerät verwenden** aus, und klicken Sie auf **starten** , um eine Aufzeichnungs Sitzung vom Kommunikationsgerät zu starten.</span><span class="sxs-lookup"><span data-stu-id="d2343-158">On the DuckingCaptureSample window, select **Use default input device**, and click **Start** to start a capture session from the communication device.</span></span>
2.  <span data-ttu-id="d2343-159">Wählen Sie auf dem duckingmediaplayer eine Mediendatei aus, die Sie wiedergeben möchten, und geben Sie die Option Ducking als **Pause on Duck** an.</span><span class="sxs-lookup"><span data-stu-id="d2343-159">On the DuckingMediaPlayer, select a media file to play, and specify the ducking option as **Pause on Duck**.</span></span>
3.  <span data-ttu-id="d2343-160">Klicken Sie im Fenster "duckingcapturesample" auf " **Abbrechen** ", um den Kommunikationsstream zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="d2343-160">On the DuckingCaptureSample window, click **Stop** to stop the communication stream.</span></span>

<span data-ttu-id="d2343-161">Beachten Sie, dass die von duckingmediaplayer ausgespielte Mediendatei angehalten wird, wenn "duckingcapturesample" den Kommunikationsstream öffnet.</span><span class="sxs-lookup"><span data-stu-id="d2343-161">Notice that when DuckingCaptureSample opens the communication stream, the media file played by DuckingMediaPlayer is paused.</span></span> <span data-ttu-id="d2343-162">Die Wiedergabe wird fortgesetzt, wenn die Kommunikationssitzung angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="d2343-162">The playback resumes when the communication session is stopped.</span></span> <span data-ttu-id="d2343-163">Dieses streamdäsierungsverhalten ist das vom Media Player implementierte duckverhalten.</span><span class="sxs-lookup"><span data-stu-id="d2343-163">This stream attenuation behavior is the ducking behavior implemented by the media player.</span></span>

<span data-ttu-id="d2343-164">Duckingmediaplayer zeigt außerdem, wie Sie die volumesteuerung für jede Anwendung mit dem volumemixer integrieren können.</span><span class="sxs-lookup"><span data-stu-id="d2343-164">DuckingMediaPlayer also demonstrates how to integrate volume control for each application with the volume mixer.</span></span>

<span data-ttu-id="d2343-165">Weitere Informationen zur Datenstrom Dämpfung finden Sie unter standardmäßige [Ducking](stream-attenuation.md)-Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="d2343-165">For more information about the stream attenuation feature, see [Default Ducking Experience](stream-attenuation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2343-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d2343-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2343-167">SDK-Beispiele für die Verwendung der kernaudioapis</span><span class="sxs-lookup"><span data-stu-id="d2343-167">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



