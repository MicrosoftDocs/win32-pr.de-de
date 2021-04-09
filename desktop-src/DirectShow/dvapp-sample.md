---
description: Dvapp-Beispiel
ms.assetid: 80375170-d0d6-4371-abe3-078703e158b1
title: Dvapp-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86653781d08921bf638e7798fb34f3a86e8d34a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124826"
---
# <a name="dvapp-sample"></a><span data-ttu-id="44e33-103">Dvapp-Beispiel</span><span class="sxs-lookup"><span data-stu-id="44e33-103">DVApp Sample</span></span>

## <a name="description"></a><span data-ttu-id="44e33-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44e33-104">Description</span></span>

<span data-ttu-id="44e33-105">Digital Video (DV) Capture-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="44e33-105">Digital Video (DV) capture application.</span></span>

<span data-ttu-id="44e33-106">In diesem Beispiel wird veranschaulicht, wie verschiedene Arten von Filter Diagrammen zum Steuern von DV-Camcordern erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="44e33-106">This sample demonstrates how to build various types of filter graphs for controlling DV camcorders.</span></span> <span data-ttu-id="44e33-107">Außerdem wird gezeigt, wie Sie mit einem DV-Camcorder die Erfassung, Vorschau, Übertragung und Gerätesteuerung durchführen.</span><span class="sxs-lookup"><span data-stu-id="44e33-107">It also shows how to perform capture, preview, transmit, and device control with a DV camcorder.</span></span>

### <a name="usage"></a><span data-ttu-id="44e33-108">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="44e33-108">Usage</span></span>

<span data-ttu-id="44e33-109">Die dvapp-Anwendung unterstützt die folgenden Modi:</span><span class="sxs-lookup"><span data-stu-id="44e33-109">The DVApp application supports the following modes:</span></span>

-   <span data-ttu-id="44e33-110">Vorschau: rendert DV vom Camcorder in ein Videofenster.</span><span class="sxs-lookup"><span data-stu-id="44e33-110">Preview: Renders DV from the camcorder to a video window.</span></span>
-   <span data-ttu-id="44e33-111">DV-zu-1-Datei: Hiermit werden DV-Daten vom Camcorder in eine Type-1-DV-Datei erfasst.</span><span class="sxs-lookup"><span data-stu-id="44e33-111">DV to type-1 file: Captures DV data from the camcorder to a type-1 DV file.</span></span>
-   <span data-ttu-id="44e33-112">Type-1 Datei in DV: überträgt Daten aus einer DV-Datei vom Typ 1 an den Camcorder.</span><span class="sxs-lookup"><span data-stu-id="44e33-112">Type-1 file to DV: Transmits data from a type-1 DV file to the camcorder.</span></span>
-   <span data-ttu-id="44e33-113">DV in Type-2 file: zeichnet DV-Daten vom Camcorder bis zu einer Type-2-DV-Datei auf.</span><span class="sxs-lookup"><span data-stu-id="44e33-113">DV to type-2 file: Captures DV data from the camcorder to a type-2 DV file.</span></span>
-   <span data-ttu-id="44e33-114">Type-2 Datei in DV: überträgt Daten aus einer DV-Datei vom Typ 2 an den Camcorder.</span><span class="sxs-lookup"><span data-stu-id="44e33-114">Type-2 file to DV: Transmits data from a type-2 DV file to the camcorder.</span></span>

<span data-ttu-id="44e33-115">Die Aufzeichnungs-und Übertragungsmodi führen ebenfalls eine Vorschau aus.</span><span class="sxs-lookup"><span data-stu-id="44e33-115">The capture and transmit modes also perform preview.</span></span> <span data-ttu-id="44e33-116">Jeder dieser Modi verfügt ebenfalls über eine **Vorschau** Option, mit der die Vorschau deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="44e33-116">Each of those modes has a **No Preview** option as well, which disables preview.</span></span> <span data-ttu-id="44e33-117">Die Erfassung ohne Vorschau ist effizienter und kann die Anzahl der gelöschten Frames verringern.</span><span class="sxs-lookup"><span data-stu-id="44e33-117">Capturing without preview is more efficient and can reduce the number of dropped frames.</span></span>

<span data-ttu-id="44e33-118">Die Anwendung wird im Vorschaumodus gestartet.</span><span class="sxs-lookup"><span data-stu-id="44e33-118">The application starts in preview mode.</span></span> <span data-ttu-id="44e33-119">Wenn Sie einen anderen Modus auswählen möchten, wählen Sie im Menü **Diagramm Modus** einen Modus aus.</span><span class="sxs-lookup"><span data-stu-id="44e33-119">To select another mode, choose a mode from the **Graph Mode** menu.</span></span> <span data-ttu-id="44e33-120">Für jeden Modus erstellt dvapp ein Filter Diagramm, das die Funktionalität dieses Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="44e33-120">For each mode, DVApp builds a filter graph that supports the functionality of that mode.</span></span> <span data-ttu-id="44e33-121">Um das Diagramm als GraphEdit-Datei (. GRF) zu speichern, wählen Sie im Menü **Datei** die Option **Diagramm in Datei speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="44e33-121">To save the graph as a GraphEdit (.grf) file, select **Save Graph to File** from the **File** menu.</span></span> <span data-ttu-id="44e33-122">Beenden Sie dvapp, bevor Sie die Datei in GraphEdit öffnen.</span><span class="sxs-lookup"><span data-stu-id="44e33-122">Quit DVApp before opening the file in GraphEdit.</span></span>

<span data-ttu-id="44e33-123">So erfassen Sie in einer Datei:</span><span class="sxs-lookup"><span data-stu-id="44e33-123">To capture to a file:</span></span>

1.  <span data-ttu-id="44e33-124">Wählen Sie im Menü **Datei** die Option **Ausgabedatei festlegen** aus, und geben Sie einen Dateinamen ein.</span><span class="sxs-lookup"><span data-stu-id="44e33-124">From the **File** menu, choose **Set Output File** and enter a file name.</span></span>
2.  <span data-ttu-id="44e33-125">Wählen Sie im Menü **Diagramm Modus** einen *DV-zu-Datei* -Modus aus (Typ 1 oder Typ 2, mit oder ohne Vorschau).</span><span class="sxs-lookup"><span data-stu-id="44e33-125">From the **Graph Mode** menu, select a *DV to File* mode (type 1 or type 2, with or without preview).</span></span>
3.  <span data-ttu-id="44e33-126">Klicken Sie auf **Datensatz**.</span><span class="sxs-lookup"><span data-stu-id="44e33-126">Click **Record**.</span></span>
4.  <span data-ttu-id="44e33-127">Wenn sich der Camcorder im VTR-Modus befindet **, klicken Sie** auf wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="44e33-127">If the camcorder is in VTR mode, click **Play**.</span></span>
5.  <span data-ttu-id="44e33-128">Klicken Sie auf " **Abbrechen**", um die Erfassung anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="44e33-128">To stop capturing, click **Stop**.</span></span>

<span data-ttu-id="44e33-129">So übertragen Sie aus einer Datei an den Camcorder:</span><span class="sxs-lookup"><span data-stu-id="44e33-129">To transmit from a file to the camcorder:</span></span>

1.  <span data-ttu-id="44e33-130">Klicken Sie im Menü **Datei** auf **Eingabedatei festlegen** , und wählen Sie eine DV-Datei aus.</span><span class="sxs-lookup"><span data-stu-id="44e33-130">From the **File** menu, click **Set Input File** and select a DV file.</span></span> <span data-ttu-id="44e33-131">Die Datei muss mit dem ausgewählten Modus (Typ 1 oder Typ 2) identisch sein.</span><span class="sxs-lookup"><span data-stu-id="44e33-131">The file must match the selected mode (type 1 or type 2).</span></span>
2.  <span data-ttu-id="44e33-132">Wählen Sie im Menü **Diagramm Modus** eine *Datei in den DV* -Modus aus (Typ 1 oder Typ 2, mit oder ohne Vorschau).</span><span class="sxs-lookup"><span data-stu-id="44e33-132">From the **Graph Mode** menu, select a *File to DV* mode (type 1 or type 2, with or without preview).</span></span>
3.  <span data-ttu-id="44e33-133">Klicken Sie auf **Wiedergabe**.</span><span class="sxs-lookup"><span data-stu-id="44e33-133">Click **Play**.</span></span>
4.  <span data-ttu-id="44e33-134">Klicken Sie auf **Datensatz**, um die Daten auf Band aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="44e33-134">To record the data to tape, click **Record**.</span></span>
5.  <span data-ttu-id="44e33-135">Klicken Sie auf " **Abbrechen**", um die Übertragung anzuhalten</span><span class="sxs-lookup"><span data-stu-id="44e33-135">To stop transmitting, click **Stop**.</span></span>

<span data-ttu-id="44e33-136">Wenn sich der Camcorder im VTR-Modus befindet, kann der Benutzer den Transportmechanismus über die Schaltflächen im VCR-Stil der Anwendung steuern.</span><span class="sxs-lookup"><span data-stu-id="44e33-136">If the camcorder is in VTR mode, the user can control the transport mechanism through the application's VCR-style buttons.</span></span> <span data-ttu-id="44e33-137">Um das Band zu suchen, geben Sie den zieltimecode ein, und klicken Sie auf die Schaltfläche Suchen.</span><span class="sxs-lookup"><span data-stu-id="44e33-137">To seek the tape, enter the target timecode and click the seek button.</span></span>

<span data-ttu-id="44e33-138">Wählen Sie im Menü **Datei** die Option **Größe erfassen** aus, um die von der Anwendung erfassten Daten einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="44e33-138">To limit how much data the application captures, choose **Capture Size** from the **File** menu.</span></span>

<span data-ttu-id="44e33-139">Wählen Sie im Menü **Optionen die Option** **Band überprüfen** aus, um das Band Format (NTSC oder PAL) zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="44e33-139">To check the tape format (NTSC or PAL), choose **Check Tape** from the **Options** menu.</span></span>

<span data-ttu-id="44e33-140">Um die Größe des Vorschaufensters zu ändern, wählen Sie im Menü Optionen die **Option** **decodiergröße ändern** aus.</span><span class="sxs-lookup"><span data-stu-id="44e33-140">To change the size of the preview window, choose **Change Decode Size** from the **Options** menu.</span></span>

### <a name="programming-notes"></a><span data-ttu-id="44e33-141">Programmier Hinweise</span><span class="sxs-lookup"><span data-stu-id="44e33-141">Programming Notes</span></span>

<span data-ttu-id="44e33-142">Der Hauptzweck dieser Anwendung besteht darin, zu zeigen, wie verschiedene DV-Erfassungs-und-Übertragungs Diagramme erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="44e33-142">The main purpose of this application is to show how to build various DV capture and transmit graphs.</span></span>

### <a name="device-arrival-and-removal"></a><span data-ttu-id="44e33-143">Geräte Ankunft und-Entfernung</span><span class="sxs-lookup"><span data-stu-id="44e33-143">Device Arrival and Removal</span></span>

<span data-ttu-id="44e33-144">Die Anwendung übernimmt das eintreffen und Entfernen von Geräten mit zwei verschiedenen Techniken.</span><span class="sxs-lookup"><span data-stu-id="44e33-144">The application handles device arrival and removal, using two different techniques.</span></span> <span data-ttu-id="44e33-145">Beim Eintreffen des Geräts antwortet die Nachrichten Schleife der Anwendung auf die "WM \_ devicechange"-Meldungen.</span><span class="sxs-lookup"><span data-stu-id="44e33-145">For device arrival, the application's message loop responds to WM\_DEVICECHANGE messages.</span></span> <span data-ttu-id="44e33-146">Zum Entfernen des Geräts antwortet die Anwendung auf Ereignisse des EC-Geräts, die vom Filter Graph-Manager [**\_ \_ verloren gehen**](ec-device-lost.md) .</span><span class="sxs-lookup"><span data-stu-id="44e33-146">For device removal, the application responds to [**EC\_DEVICE\_LOST**](ec-device-lost.md) events from the filter graph manager.</span></span> <span data-ttu-id="44e33-147">Beide Ansätze sind funktionsfähig, obwohl das Ereignis "EC- \_ Gerät \_ verloren" davon abhängt, dass das Gerät im Filter Diagramm vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="44e33-147">Either approach works, although the EC\_DEVICE\_LOST event depends on the existence of the device in the filter graph.</span></span>

<span data-ttu-id="44e33-148">Die Anwendung verarbeitet jeweils nur ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="44e33-148">The application only handles one device at a time.</span></span> <span data-ttu-id="44e33-149">Wenn das aktuelle Gerät entfernt wird, sucht die Anwendung im System nach einem anderen DV-Gerät.</span><span class="sxs-lookup"><span data-stu-id="44e33-149">If the current device is removed, the application looks for another DV device on the system.</span></span>

<span data-ttu-id="44e33-150">Bei manchen DV-Camcordern muss der Benutzer das Gerät Herunterfahren, wenn es zwischen dem Kameramodus und dem VTR-Modus wechselt, wodurch eine Meldung zum Verlust von Geräten ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="44e33-150">On some DV camcorders, the user must shut off the device when switching it between camera mode and VTR mode, which triggers a device-lost message.</span></span> <span data-ttu-id="44e33-151">Die Anwendung antwortet durch Aktivieren oder Deaktivieren der entsprechenden Menübefehle.</span><span class="sxs-lookup"><span data-stu-id="44e33-151">The application responds by enabling or disabling the appropriate menu commands.</span></span> <span data-ttu-id="44e33-152">Wenn der Benutzer jedoch schnell zwischen den Modi wechselt, generiert der Camcorder möglicherweise keine Geräte verlorene Nachricht.</span><span class="sxs-lookup"><span data-stu-id="44e33-152">However, if the user toggles rapidly between modes, the camcorder might not generate a device-lost message.</span></span> <span data-ttu-id="44e33-153">Sie können erzwingen, dass die Menüs aktualisiert werden, indem Sie im Menü **Optionen** den **Modus aktualisieren** auswählen.</span><span class="sxs-lookup"><span data-stu-id="44e33-153">You can force the menus to update by choosing **Refresh Mode** from the **Options** menu.</span></span> <span data-ttu-id="44e33-154">Einige DV-Camcorder können Modi umschalten, ohne dass Sie ausgeschaltet werden, aber eine Meldung zum Verlust von Geräten nur dann senden, wenn Sie in den VTR-Modus wechseln.</span><span class="sxs-lookup"><span data-stu-id="44e33-154">Some DV camcorders can toggle modes without shutting off, but send a device-lost message only when they switch to VTR mode.</span></span>

### <a name="device-control"></a><span data-ttu-id="44e33-155">Gerätesteuerung</span><span class="sxs-lookup"><span data-stu-id="44e33-155">Device Control</span></span>

<span data-ttu-id="44e33-156">Die Funktionalität der Schaltfläche wieder **Gabe** und **Datensatz** hängt vom aktuellen Modus ab:</span><span class="sxs-lookup"><span data-stu-id="44e33-156">The functionality of the **Play** and **Record** button depends on the current mode:</span></span>

-   <span data-ttu-id="44e33-157">Vorschau: das Filter Diagramm wird automatisch ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="44e33-157">Preview: The filter graph runs automatically.</span></span> <span data-ttu-id="44e33-158">Die **Wiedergabe** Schaltfläche startet den Transport.</span><span class="sxs-lookup"><span data-stu-id="44e33-158">The **Play** button starts the transport.</span></span>
-   <span data-ttu-id="44e33-159">In Datei erfassen: die Schaltfläche **Datensatz** führt das Diagramm aus, und die **Wiedergabe** Schaltfläche startet den Transport.</span><span class="sxs-lookup"><span data-stu-id="44e33-159">Capture to file: The **Record** button runs the graph, and the **Play** button starts the transport.</span></span>
-   <span data-ttu-id="44e33-160">An Gerät übertragen: die **Wiedergabe** Schaltfläche führt das Diagramm aus, und die Schaltfläche **Datensatz** startet den Transport.</span><span class="sxs-lookup"><span data-stu-id="44e33-160">Transmit to device: The **Play** button runs the graph, and the **Record** button starts the transport.</span></span>

<span data-ttu-id="44e33-161">Die Beispielanwendung führt keine Frame genaue Erfassung aus.</span><span class="sxs-lookup"><span data-stu-id="44e33-161">The sample application does not perform frame-accurate capture.</span></span> <span data-ttu-id="44e33-162">An verschiedenen Punkten **Ruft die Anwendung** die Standbyfunktion auf, um zu warten, bis das Gerät antwortet.</span><span class="sxs-lookup"><span data-stu-id="44e33-162">At various points, the application calls the **Sleep** function to wait for the device to respond.</span></span> <span data-ttu-id="44e33-163">Neuere DV-Camcorder senden eine Benachrichtigung, wenn sich der Status des Geräts ändert.</span><span class="sxs-lookup"><span data-stu-id="44e33-163">Newer DV camcorders send a notification when the state of the device changes.</span></span> <span data-ttu-id="44e33-164">Ältere Geräte unterstützen möglicherweise keine Benachrichtigung. im Rahmen eines Beispiels ist das Aufrufen von **Sleep** eine einfachere Lösung.</span><span class="sxs-lookup"><span data-stu-id="44e33-164">Older devices might not support notification; for the purposes of a sample, calling **Sleep** is a simpler solution.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="44e33-165">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="44e33-165">Downloading the Sample</span></span>

<span data-ttu-id="44e33-166">Zum Herunterladen der DirectShow SDK-Beispiele installieren Sie die neueste Version der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="44e33-166">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="44e33-167">Dieses Beispiel wird unter folgendem Pfad installiert: *\[ SDK Root \]* \\ Samples \\ Multimedia \\ DirectShow \\ Capture \\ dvapp.</span><span class="sxs-lookup"><span data-stu-id="44e33-167">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Capture\\DVApp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44e33-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="44e33-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44e33-169">Steuern eines DV-Camcorder</span><span class="sxs-lookup"><span data-stu-id="44e33-169">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> <dt>

[<span data-ttu-id="44e33-170">Digitales Video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="44e33-170">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="44e33-171">DirectShow-Beispiele</span><span class="sxs-lookup"><span data-stu-id="44e33-171">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



