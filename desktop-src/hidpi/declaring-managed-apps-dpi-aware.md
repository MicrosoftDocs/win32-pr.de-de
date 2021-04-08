---
title: Entwickeln einer DPI pro Monitor-fähigen WPF-Anwendung
description: Beachten Sie, dass diese Seite die ältere WPF-Entwicklung für Windows 8.1 behandelt. Wenn Sie WPF-Anwendungen für Windows 10 entwickeln, finden Sie weitere Informationen in der neuesten Dokumentation auf GitHub..
ms.assetid: 04a36dc7-684f-4846-aeba-970117070b4c
keywords:
- Windows-Benutzeroberfläche, dpi-fähige Anwendungen
- Windows-Benutzeroberfläche, hohe dpi-
- DPI-fähige Anwendungen
- hoher dpi-
- Schreiben von dpi-fähigen Win32-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a32bfaf76271e61d0dc3791d5aaae9609be6d8c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101639"
---
# <a name="developing-a-per-monitor-dpi-aware-wpf-application"></a><span data-ttu-id="9b29c-110">Entwickeln einer DPI pro Monitor-fähigen WPF-Anwendung</span><span class="sxs-lookup"><span data-stu-id="9b29c-110">Developing a Per-Monitor DPI-Aware WPF Application</span></span>

<span data-ttu-id="9b29c-111">**Wichtige APIs**</span><span class="sxs-lookup"><span data-stu-id="9b29c-111">**Important APIs**</span></span>

-   [<span data-ttu-id="9b29c-112">**Setprocessdpiawareness**</span><span class="sxs-lookup"><span data-stu-id="9b29c-112">**SetProcessDpiAwareness**</span></span>](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)
-   [<span data-ttu-id="9b29c-113">**Getprocessdpiawareness**</span><span class="sxs-lookup"><span data-stu-id="9b29c-113">**GetProcessDpiAwareness**</span></span>](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)
-   [<span data-ttu-id="9b29c-114">**Getdpiformonitor**</span><span class="sxs-lookup"><span data-stu-id="9b29c-114">**GetDpiForMonitor**</span></span>](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)

> [!Note]  
> <span data-ttu-id="9b29c-115">**Auf dieser Seite wird die Legacy-WPF-Entwicklung für Windows 8.1 behandelt.**</span><span class="sxs-lookup"><span data-stu-id="9b29c-115">**This page covers legacy WPF development for Windows 8.1.**</span></span> <span data-ttu-id="9b29c-116">Wenn Sie WPF-Anwendungen für Windows 10 entwickeln, finden Sie weitere Informationen <a href="https://github.com/microsoft/WPF-Samples/blob/master/PerMonitorDPI/readme.md">in der neuesten Dokumentation auf GitHub.</a></span><span class="sxs-lookup"><span data-stu-id="9b29c-116">If you are developing WPF applications for Windows 10, please see the <a href="https://github.com/microsoft/WPF-Samples/blob/master/PerMonitorDPI/readme.md">latest documentation on GitHub.</a></span></span>

 

<span data-ttu-id="9b29c-117">Windows 8.1 bietet Entwicklern neue Funktionen zum Erstellen von Desktop Anwendungen mit dpi-Werten pro Monitor.</span><span class="sxs-lookup"><span data-stu-id="9b29c-117">Windows 8.1 gives developers new functionality to create desktop applications that are per-monitor DPI-aware.</span></span> <span data-ttu-id="9b29c-118">Um diese Funktionalität nutzen zu können, muss eine pro-Monitor-dpi-fähige Anwendung folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="9b29c-118">In order to take advantage of this functionality, a per monitor DPI-aware application must do the following:</span></span>

-   <span data-ttu-id="9b29c-119">Ändern der Fenster Dimensionen, um eine physische Größe beizubehalten, die auf einer beliebigen Anzeige konsistent angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="9b29c-119">Change window dimensions to maintain a physical size that appears consistent on any display</span></span>
-   <span data-ttu-id="9b29c-120">Erneutes Layout und erneutes Renren von Grafiken für die neue Fenstergröße</span><span class="sxs-lookup"><span data-stu-id="9b29c-120">Re-layout and re-render graphics for the new window size</span></span>
-   <span data-ttu-id="9b29c-121">Schriftarten auswählen, die entsprechend der dpi-Ebene skaliert werden</span><span class="sxs-lookup"><span data-stu-id="9b29c-121">Select fonts that are scaled appropriately for the DPI level</span></span>
-   <span data-ttu-id="9b29c-122">Auswählen und Laden von bitmapassets, die auf die dpi-Ebene zugeschnitten sind</span><span class="sxs-lookup"><span data-stu-id="9b29c-122">Select and load bitmap assets that are tailored for the DPI level</span></span>

<span data-ttu-id="9b29c-123">Zur Vereinfachung der Erstellung einer dpi-fähigen Anwendung mit dpi-Unterstützung bietet Windows 8.1 folgende Microsoft Win32APIs:</span><span class="sxs-lookup"><span data-stu-id="9b29c-123">To facilitate making a per-monitor DPI-aware application, Windows 8.1 provides the following Microsoft Win32APIs:</span></span>

-   <span data-ttu-id="9b29c-124">[**Setprocessdpiawareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) (oder dpi-Manifest-Eintrag) legt den Prozess auf einen angegebenen dpi-Wert fest, der dann festlegt, wie Windows die Benutzeroberfläche skaliert.</span><span class="sxs-lookup"><span data-stu-id="9b29c-124">[**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) (or DPI manifest entry) sets the process to a specified DPI awareness level, which then determines how Windows scales the UI.</span></span> <span data-ttu-id="9b29c-125">Dies ersetzt [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware).</span><span class="sxs-lookup"><span data-stu-id="9b29c-125">This supersedes [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware).</span></span>
-   <span data-ttu-id="9b29c-126">[**Getprocessdpiawareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness) gibt den dpi-Bekanntheitsgrad zurück.</span><span class="sxs-lookup"><span data-stu-id="9b29c-126">[**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness) returns the DPI awareness level.</span></span> <span data-ttu-id="9b29c-127">Hierdurch wird [**isprocessdpiaware**](/windows/desktop/api/winuser/nf-winuser-isprocessdpiaware)abgelöst.</span><span class="sxs-lookup"><span data-stu-id="9b29c-127">This supersedes [**IsProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-isprocessdpiaware).</span></span>
-   <span data-ttu-id="9b29c-128">[**Getdpiformonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor) gibt den dpi-Wert für einen Monitor zurück.</span><span class="sxs-lookup"><span data-stu-id="9b29c-128">[**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor) returns the DPI for a monitor.</span></span>
-   <span data-ttu-id="9b29c-129">Die Benachrichtigung " [**WM- \_ dpichanged**](wm-dpichanged.md) -Fenster" wird an die dpi-fähigen Anwendungen pro Monitor gesendet, wenn sich die Position eines Fensters ändert, sodass der größte Teil des Bereichs einen Monitor mit einem dpi-Wert überschneidet, der sich vom dpi-Wert unterscheidet, bevor die Position geändert wird oder wenn der Benutzer den Schieberegler verschiebt.</span><span class="sxs-lookup"><span data-stu-id="9b29c-129">The [**WM\_DPICHANGED**](wm-dpichanged.md) window notification is sent to per-monitor DPI-aware applications when a window’s position changes such that most of its area intersects a monitor with a DPI that is different from the DPI before the position change or when the user moves the display slider.</span></span> <span data-ttu-id="9b29c-130">Um eine Anwendung zu erstellen, deren Größe geändert und wieder gerendert wird, wenn ein Benutzer Sie in eine andere Anzeige verschiebt, verwenden Sie diese Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="9b29c-130">To create an application that resizes and re-renders itself when a user moves it to a different display, use this notification.</span></span>

<span data-ttu-id="9b29c-131">Weitere Informationen zu verschiedenen dpi-Informationen, die für Desktop Anwendungen in unterstützt werden, finden Sie unter Windows 8.1 im Thema [Schreiben von DPI-Aware Desktop-und Win32-Anwendungen](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span><span class="sxs-lookup"><span data-stu-id="9b29c-131">For more details on various DPI awareness levels supported for desktop applications in Windows 8.1 see the topic [Writing DPI-Aware Desktop and Win32 Applications](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span>

## <a name="dpi-scaling-and-wpf"></a><span data-ttu-id="9b29c-132">DPI-Skalierung und WPF</span><span class="sxs-lookup"><span data-stu-id="9b29c-132">DPI Scaling and WPF</span></span>

<span data-ttu-id="9b29c-133">Windows Presentation Foundation (WPF)-Anwendungen sind standardmäßig System-dpi-fähig.</span><span class="sxs-lookup"><span data-stu-id="9b29c-133">Windows Presentation Foundation (WPF) applications are by default system DPI-aware.</span></span> <span data-ttu-id="9b29c-134">Definitionen der verschiedenen dpi-Informationen finden Sie im Thema [schreiben DPI-Aware Desktop-und Win32-Anwendungen](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span><span class="sxs-lookup"><span data-stu-id="9b29c-134">For definitions of the different DPI awareness levels see the topic [Writing DPI-Aware Desktop and Win32 Applications](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span> <span data-ttu-id="9b29c-135">Das WPF-Grafiksystem verwendet geräteunabhängige Einheiten, um Auflösung und Geräteunabhängigkeit zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="9b29c-135">The WPF graphics system uses device-independent units to enable resolution and device independence.</span></span> <span data-ttu-id="9b29c-136">WPF skaliert jedes geräteunabhängige Pixel automatisch basierend auf dem aktuellen System-dpi-Wert.</span><span class="sxs-lookup"><span data-stu-id="9b29c-136">WPF scales each device independent pixel automatically based on current system DPI.</span></span> <span data-ttu-id="9b29c-137">Dadurch können WPF-Anwendungen automatisch skaliert werden, wenn der dpi-Wert des Monitors, auf dem sich das Fenster befindet, dasselbe System-dpi ist.</span><span class="sxs-lookup"><span data-stu-id="9b29c-137">This allows WPF applications to scale automatically when the DPI of the monitor the window is on is same system DPI.</span></span> <span data-ttu-id="9b29c-138">Da WPF-Anwendungen jedoch System dpi-fähig sind, wird die Anwendung vom Betriebssystem skaliert, wenn die Anwendung auf einen Monitor mit einem anderen dpi-Wert verschoben wird oder wenn der Schieberegler in der Systemsteuerung verwendet wird, um den dpi-Wert zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9b29c-138">However, since WPF applications are system dpi-aware, the application will be scaled by the OS when the application is moved to a monitor with a different DPI or when the slider in the control panel is used to change the DPI.</span></span> <span data-ttu-id="9b29c-139">Das Skalieren im Betriebssystem kann dazu führen, dass WPF-Anwendungen unscharf angezeigt werden, insbesondere, wenn die Skalierung nicht ganzzahlig ist.</span><span class="sxs-lookup"><span data-stu-id="9b29c-139">Scaling in the OS may result in WPF applications to appear blurry especially when the scaling is non-integral.</span></span> <span data-ttu-id="9b29c-140">Um das Skalieren von WPF-Anwendungen zu vermeiden, müssen Sie für die dpi-Unterstützung pro Monitor aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="9b29c-140">In order to avoid scaling WPF applications, they need to be updated to be per-monitor DPI-aware.</span></span>

## <a name="per-monitor-aware-wpf-sample-walkthrough"></a><span data-ttu-id="9b29c-141">Exemplarische Vorgehensweise für das WPF-Beispiel pro Monitor</span><span class="sxs-lookup"><span data-stu-id="9b29c-141">Per Monitor Aware WPF Sample Walkthrough</span></span>

<span data-ttu-id="9b29c-142">Das [WPF](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) -Beispiel "pro Monitor-fähig" ist eine WPF-Beispielanwendung, die für die dpi-Unterstützung pro Monitor aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9b29c-142">The [Per Monitor Aware WPF sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) is a sample WPF application updated to be per-monitor DPI-aware.</span></span> <span data-ttu-id="9b29c-143">Das Beispiel umfasst zwei Projekte:</span><span class="sxs-lookup"><span data-stu-id="9b29c-143">The sample consists of two projects:</span></span>

-   <span data-ttu-id="9b29c-144">Nativehelpers. vcxproj: Hierbei handelt es sich um ein System eigenes Hilfsprogramm, das die Kernfunktionen implementiert, um eine WPF-Anwendung mit dpi-Werten pro Monitor zu erstellen, indem Sie die oben genannten Win32APIs verwenden.</span><span class="sxs-lookup"><span data-stu-id="9b29c-144">NativeHelpers.vcxproj: This is a native helper project that implements the core functionality to make a WPF application as per-monitor DPI-aware utilizing the Win32APIs above.</span></span> <span data-ttu-id="9b29c-145">Das Projekt enthält zwei Klassen:</span><span class="sxs-lookup"><span data-stu-id="9b29c-145">The project contains two classes:</span></span>
    -   <span data-ttu-id="9b29c-146">Permondpihelper: eine Klasse, die Hilfsfunktionen für dpi-bezogene Vorgänge bereitstellt, z. b. das Abrufen des aktuellen dpi-Wert des aktiven Monitors, das Festlegen eines Prozesses für die dpi-Unterstützung pro Monitor usw.</span><span class="sxs-lookup"><span data-stu-id="9b29c-146">PerMonDPIHelpers: A class that provides helper functions for DPI related operations like retrieving the current DPI of the active monitor, setting a process to be per-monitor DPI-aware, etc.</span></span>
    -   <span data-ttu-id="9b29c-147">Permonitordpiwindow: eine Basisklasse, die von **System. Windows. Window** abgeleitet wird und Funktionen implementiert, mit denen ein WPF-Anwendungsfenster pro Monitor dpi-fähig ist.</span><span class="sxs-lookup"><span data-stu-id="9b29c-147">PerMonitorDPIWindow: A base class derived from **System.Windows.Window** that implements functionality to make a WPF application window to be per-monitor dpi-aware.</span></span> <span data-ttu-id="9b29c-148">Passt die Fenstergröße, Grafik Renderinggröße und Schriftgröße basierend auf der dpi des Monitors und nicht auf dem System-dpi an.</span><span class="sxs-lookup"><span data-stu-id="9b29c-148">Adjusts window size, graphics rendering size and font size based on the DPI of the monitor rather than the system DPI.</span></span>
-   <span data-ttu-id="9b29c-149">Wpfapplikation. csproj: Beispiel einer WPF-Anwendung, die das permonitordpiwindow (permonitordpiwindow) verwendet, und zeigt, wie das Anwendungsfenster und das Rendering geändert werden, wenn das Fenster auf einen Monitor mit einem anderen dpi-Wert verschoben wird, oder wenn der Schieberegler in der Anzeige Steuerung verwendet wird, um den dpi zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9b29c-149">WPFApplication.csproj: Sample WPF application that consumes the PerMonitorDPIWindow (PerMonitorDPIWindow), and showcases how the application window and rendering resizes when the window is moved to a monitor with a different DPI or when the slider in the Display control panel is used to change the DPI.</span></span>

<span data-ttu-id="9b29c-150">Führen Sie die folgenden Schritte aus, um das Beispiel auszuführen:</span><span class="sxs-lookup"><span data-stu-id="9b29c-150">To run the sample follow the steps below:</span></span>

1.  <span data-ttu-id="9b29c-151">Herunterladen und Entpacken des WPF-Beispiels " [pro Monitor](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) "</span><span class="sxs-lookup"><span data-stu-id="9b29c-151">Download and unzip the [Per Monitor Aware WPF sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)</span></span>
2.  <span data-ttu-id="9b29c-152">Starten Sie Microsoft Visual Studio, und wählen Sie **Datei > > Projekt/Projekt Mappe öffnen** .</span><span class="sxs-lookup"><span data-stu-id="9b29c-152">Start Microsoft Visual Studio and select **File > Open > Project/Solution**</span></span>
3.  <span data-ttu-id="9b29c-153">Navigieren Sie zu dem Verzeichnis, das das entzippte Beispiel enthält.</span><span class="sxs-lookup"><span data-stu-id="9b29c-153">Browse to the directory that contains the unzipped sample.</span></span> <span data-ttu-id="9b29c-154">Wechseln Sie zum Verzeichnis für das Beispiel, und doppelklicken Sie auf die Visual Studio-Projektmappendatei (. sln).</span><span class="sxs-lookup"><span data-stu-id="9b29c-154">Go to the directory named for the sample, and double-click the Visual Studio Solution (.sln) file</span></span>
4.  <span data-ttu-id="9b29c-155">Drücken Sie F7, oder verwenden Sie **Build > Build Solution** , um das Beispiel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9b29c-155">Press F7 or use **Build > Build Solution** to build the sample</span></span>
5.  <span data-ttu-id="9b29c-156">Drücken Sie STRG + F5 oder **Debuggen > starten ohne Debugging** , um das Beispiel auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9b29c-156">Press Ctrl+F5 or use **Debug > Start Without Debugging** to run the sample</span></span>

<span data-ttu-id="9b29c-157">Um die Auswirkungen der Änderung von dpi für eine WPF-Anwendung, die mit der-Basisklasse im Beispiel aktualisiert wird, auf dpi-fähig zu erkennen, verschieben Sie das Anwendungsfenster in und aus anzeigen, die über unterschiedliche DPIs verfügen.</span><span class="sxs-lookup"><span data-stu-id="9b29c-157">To see the impact of changing DPI on a WPF application that is updated to be per-monitor DPI-aware using the base class in the sample, move the application window to and from displays that have different DPIs.</span></span> <span data-ttu-id="9b29c-158">Wenn das Fenster zwischen Monitoren verschoben wird, werden die Fenstergröße und die Benutzeroberflächen Skala basierend auf dem dpi-Wert der Anzeige mithilfe des skalierbaren Grafik Systems von WPF aktualisiert, anstatt durch das Betriebssystem skaliert zu werden.</span><span class="sxs-lookup"><span data-stu-id="9b29c-158">As the window is moved between monitors, the window size and the UI scale is updated based on the DPI of the display by using WPF’s scalable graphics system, rather than being scaled by the OS.</span></span> <span data-ttu-id="9b29c-159">Die Benutzeroberfläche der Anwendung wird nativ gerendert und wird nicht verschwommen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9b29c-159">The application’s UI is rendered natively and does not appear blurry.</span></span> <span data-ttu-id="9b29c-160">Wenn Sie nicht über zwei Anzeigeelemente mit unterschiedlichem dpi verfügen, ändern Sie den dpi-Code, indem Sie den Schieberegler in der Systemsteuerung anzeigen ändern.</span><span class="sxs-lookup"><span data-stu-id="9b29c-160">If you don’t have two displays with different DPI, change the DPI by changing the slider in the Display control panel.</span></span> <span data-ttu-id="9b29c-161">Wenn Sie den Schieberegler ändern und auf **anwenden** klicken, wird die Größe des Anwendungsfensters geändert und die Benutzeroberflächen Skalierung automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9b29c-161">Changing the slider and clicking **Apply** will resize the application’s window and update the UI scale automatically.</span></span>

## <a name="updating-an-existing-wpf-application-to-be-per-monitor-dpi-aware-using-helper-project-in-the-wpf-sample"></a><span data-ttu-id="9b29c-162">Aktualisieren einer vorhandenen WPF-Anwendung für die dpi-Unterstützung per Monitor mithilfe des Hilfsprojekts im WPF-Beispiel</span><span class="sxs-lookup"><span data-stu-id="9b29c-162">Updating an existing WPF Application to be per-monitor dpi-aware using helper project in the WPF Sample</span></span>

<span data-ttu-id="9b29c-163">Wenn Sie bereits über eine WPF-Anwendung verfügen und das dpi-Hilfsobjekt aus dem Beispiel nutzen möchten, um es zu berücksichtigen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="9b29c-163">If you have an existing WPF application and wish to leverage the DPI helper project from the sample to make it DPI aware, follow these steps.</span></span>

1.  <span data-ttu-id="9b29c-164">Herunterladen und Entpacken des WPF-Beispiels "pro Monitor"</span><span class="sxs-lookup"><span data-stu-id="9b29c-164">Download and unzip the Per Monitor Aware WPF sample</span></span>
2.  <span data-ttu-id="9b29c-165">Starten Sie Visual Studio, und wählen Sie **Datei > > Projekt/Projekt Mappe öffnen** aus.</span><span class="sxs-lookup"><span data-stu-id="9b29c-165">Start Visual Studio and select **File > Open > Project/Solution**</span></span>
3.  <span data-ttu-id="9b29c-166">Navigieren Sie zu dem Verzeichnis, das eine vorhandene WPF-Anwendung enthält, und doppelklicken Sie auf die Visual Studio-Projektmappendatei (. sln).</span><span class="sxs-lookup"><span data-stu-id="9b29c-166">Browse to the directory which contains an existing WPF application and double-click the Visual Studio Solution (.sln) file</span></span>
4.  <span data-ttu-id="9b29c-167">Klicken Sie mit der rechten Maustaste auf Projekt Mappe, **> > vorhandenes Projekt hinzuzufügen**. ![](images/scrvs-image1.png)</span><span class="sxs-lookup"><span data-stu-id="9b29c-167">Right click on **Solution > Add > Existing Project**![a screenshot that illustrates the add: existing project menu selection](images/scrvs-image1.png)</span></span>
5.  <span data-ttu-id="9b29c-168">Navigieren Sie im Dialogfeld zur Dateiauswahl zu dem Verzeichnis, das das entzippte Beispiel enthält.</span><span class="sxs-lookup"><span data-stu-id="9b29c-168">In the file selection dialogue browse to the directory that contains the unzipped sample.</span></span> <span data-ttu-id="9b29c-169">Öffnen Sie für das Verzeichnis, das für das Beispiel benannt ist, navigieren Sie zum Ordner "nativehelpers", wählen Sie die Visual C++ Projektdatei "nativehelpers. vcxproj" aus, und klicken Sie auf **OK** .</span><span class="sxs-lookup"><span data-stu-id="9b29c-169">Open to the directory named for the sample, browse to the folder "NativeHelpers", select the Visual C++ project file "NativeHelpers.vcxproj” and click **OK**</span></span>
6.  <span data-ttu-id="9b29c-170">Klicken Sie mit der rechten Maustaste auf das Projekt nativehelpers, und wählen Sie **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="9b29c-170">Right click on the project NativeHelpers and select **Build**.</span></span> <span data-ttu-id="9b29c-171">Hierdurch werden NativeHelpers.dll generiert, die im nächsten Schritt als Verweis auf die WPF-Anwendung hinzugefügt werden. ![](images/scrvs-image2.png)</span><span class="sxs-lookup"><span data-stu-id="9b29c-171">This will generate NativeHelpers.dll that will be added as a reference to the WPF Application in the next step![a screen shot illustrating the build menu selection](images/scrvs-image2.png)</span></span>
7.  <span data-ttu-id="9b29c-172">Fügen Sie einen Verweis auf NativeHelpers.dll aus der WPF-Anwendung hinzu.</span><span class="sxs-lookup"><span data-stu-id="9b29c-172">Add a reference to NativeHelpers.dll from your WPF Application.</span></span> <span data-ttu-id="9b29c-173">Erweitern Sie das WPF-Anwendungsprojekt, klicken Sie mit der rechten Maustaste auf **Verweise** , und klicken Sie auf **Verweis hinzufügen.**</span><span class="sxs-lookup"><span data-stu-id="9b29c-173">Expand your WPF application project, right click on **References** and click on **Add Reference...**</span></span>
8.  <span data-ttu-id="9b29c-174">Erweitern Sie im daraufhin angezeigten Dialogfeld **den Abschnitt Projekt** Mappe.</span><span class="sxs-lookup"><span data-stu-id="9b29c-174">In the resulting dialogue, expand the **Solution** section.</span></span> <span data-ttu-id="9b29c-175">Wählen Sie unter **Projekte** die Option nativehelpers aus, und klicken Sie auf **OK** ![ einen Screenshot, der das Dialogfeld Resource Manager veranschaulicht.](images/scrvs-image3.png)</span><span class="sxs-lookup"><span data-stu-id="9b29c-175">Under **Projects**, select NativeHelpers, and click **OK**![a screen shot illustrating the resource manager dialog](images/scrvs-image3.png)</span></span>
9.  <span data-ttu-id="9b29c-176">Erweitern Sie das WPF-Anwendungsprojekt, erweitern Sie **Eigenschaften**, und öffnen Sie **AssemblyInfo. cs**.</span><span class="sxs-lookup"><span data-stu-id="9b29c-176">Expand your WPF application project, expand **Properties**, and open **AssemblyInfo.cs**.</span></span> <span data-ttu-id="9b29c-177">Nehmen Sie an AssemblyInfo. cs die folgenden Ergänzungen vor.</span><span class="sxs-lookup"><span data-stu-id="9b29c-177">Make the following additions to AssemblyInfo.cs</span></span>
    -   <span data-ttu-id="9b29c-178">Fügen Sie im Referenz Abschnitt (mithilfe von System. Windows. Media;) einen Verweis auf System. Windows. Media hinzu.</span><span class="sxs-lookup"><span data-stu-id="9b29c-178">Add reference to System.Windows.Media in the reference section (using System.Windows.Media;)</span></span>
    -   <span data-ttu-id="9b29c-179">Fügen Sie das disabledpiawareness-Attribut () hinzu. `[assembly: DisableDpiAwareness]`</span><span class="sxs-lookup"><span data-stu-id="9b29c-179">Add the DisableDpiAwareness attribute (`[assembly: DisableDpiAwareness]`)</span></span>

    ![ein Screenshot, der die zusätzlichen Eigenschaften veranschaulicht](images/scrvs-image4.png)
10. <span data-ttu-id="9b29c-181">Die Haupt-WPF-Fenster Klasse wird von der permonitordpiwindow-Basisklasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="9b29c-181">Inherit the main WPF window class from PerMonitorDPIWindow base class</span></span>
    -   <span data-ttu-id="9b29c-182">Aktualisieren Sie die CS-Datei des Hauptfensters von WPF so, dass Sie von der permonitordpiwindow-Basisklasse geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="9b29c-182">Update the .cs file of the main WPF window to inherit from the PerMonitorDPIWindow base class</span></span>
        -   <span data-ttu-id="9b29c-183">Fügen Sie im Abschnitt "Reference" einen Verweis auf nativehelpers hinzu, indem Sie die Zeile hinzufügen. `using NativeHelpers;`</span><span class="sxs-lookup"><span data-stu-id="9b29c-183">Add a reference to NativeHelpers in the reference section by adding the line `using NativeHelpers;`</span></span>
        -   <span data-ttu-id="9b29c-184">Die Hauptfenster Klasse wird von der permonitordpiwindow-Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="9b29c-184">Inherit the main window class from PerMonitorDPIWindow class</span></span>

        ![ein Screenshot, der die c++-Referenz veranschaulicht](images/scrvs-image5.png)
    -   <span data-ttu-id="9b29c-186">Aktualisieren Sie die XAML-Datei des Haupt-WPF-Fensters, um von der permonitordpiwindow-Basisklasse zu erben.</span><span class="sxs-lookup"><span data-stu-id="9b29c-186">Update the .xaml file of the main WPF window to inherit from PerMonitorDPIWindow base class</span></span>
        -   <span data-ttu-id="9b29c-187">Fügen Sie im Abschnitt "Reference" einen Verweis auf nativehelpers hinzu, indem Sie die Zeile hinzufügen. `xmlns:src="clr-namespace:NativeHelpers;assembly=NativeHelpers"`</span><span class="sxs-lookup"><span data-stu-id="9b29c-187">Add a reference to NativeHelpers in the reference section by adding the line `xmlns:src="clr-namespace:NativeHelpers;assembly=NativeHelpers"`</span></span>
        -   <span data-ttu-id="9b29c-188">Die Hauptfenster Klasse wird von der permonitordpiwindow-Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="9b29c-188">Inherit the main window class from PerMonitorDPIWindow class</span></span>

        ![Screenshot, der das Hinzufügen des XAML-Verweises veranschaulicht](images/scrvs-image6.png)
11. <span data-ttu-id="9b29c-190">Drücken Sie F7, oder verwenden Sie **Build > Build Solution** , um das Beispiel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9b29c-190">Press F7 or use **Build > Build Solution** to build the sample</span></span>
12. <span data-ttu-id="9b29c-191">Drücken Sie STRG + F5 oder **Debuggen > starten ohne Debugging** , um das Beispiel auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9b29c-191">Press Ctrl+F5 or use **Debug > Start Without Debugging** to run the sample</span></span>

<span data-ttu-id="9b29c-192">Die [Beispielanwendung "pro Monitor-fähiger WPF](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) " veranschaulicht, wie eine WPF-Anwendung aktualisiert werden kann, um dpi-fähig zu sein, indem auf die Benachrichtigung "WM- [**\_ dpichanged**](wm-dpichanged.md) -Fenster" reagiert wird.</span><span class="sxs-lookup"><span data-stu-id="9b29c-192">The [Per Monitor Aware WPF sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) application illustrates how a WPF application can be updated to be per-monitor DPI-aware by responding to the [**WM\_DPICHANGED**](wm-dpichanged.md) window notification.</span></span> <span data-ttu-id="9b29c-193">In Reaktion auf die Fenster Benachrichtigung aktualisiert das Beispiel die Skalierungs Transformation, die von WPF verwendet wird, basierend auf dem aktuellen dpi-Wert des Monitors, auf dem sich das Fenster befindet.</span><span class="sxs-lookup"><span data-stu-id="9b29c-193">In response to the window notification, the sample updates the scale transform used by WPF based on the current DPI of the monitor the window is on.</span></span> <span data-ttu-id="9b29c-194">Der *wParam* -Parameter der Fenster Benachrichtigung enthält den neuen dpi-Code in der *wParam*.</span><span class="sxs-lookup"><span data-stu-id="9b29c-194">The *wParam* of the window notification contains the new DPI in the *wParam*.</span></span> <span data-ttu-id="9b29c-195">Der *LPARAM* enthält ein Rechteck mit der Größe und Position des neuen vorgeschlagenen Fensters, das auf den neuen dpi skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="9b29c-195">The *lParam* contains a rectangle that has the size and position of the new suggested window, scaled for the new DPI.</span></span>

<span data-ttu-id="9b29c-196">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="9b29c-196">Note:</span></span>

> [!Note]  
> <span data-ttu-id="9b29c-197">Da in diesem Beispiel die Fenstergröße und die Skalierungs Transformation des Stamm Knotens des WPF-Fensters überschrieben werden, sind möglicherweise weitere Aufgaben für Anwendungsentwickler erforderlich, wenn Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="9b29c-197">Since this sample overwrites the window size and the scale transform of the root node of the WPF window, further work may be required by application developer if:</span></span>
>
> -   <span data-ttu-id="9b29c-198">Die Größe des Fensters wirkt sich auf andere Teile der Anwendung aus, wie dieses WPF-Fenster, das in einer anderen Anwendung gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="9b29c-198">The size of the window impacts other portions of the application like this WPF Window being hosted inside another application.</span></span>
> -   <span data-ttu-id="9b29c-199">Die WPF-Anwendung, die diese Klasse erweitert, legt eine andere Transformation für das visuelle Stamm Element fest. Das Beispiel kann eine andere Transformation überschreiben, die von der WPF-Anwendung selbst angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="9b29c-199">The WPF application that is extending this class is setting some other transform on the root visual; the sample may overwrite some other transform that is being applied by the WPF application itself.</span></span>

 

## <a name="overview-of-the-helper-project-in-the-wpf-sample"></a><span data-ttu-id="9b29c-200">Übersicht über das Hilfsprojekt im WPF-Beispiel</span><span class="sxs-lookup"><span data-stu-id="9b29c-200">Overview of the helper project in the WPF sample</span></span>

<span data-ttu-id="9b29c-201">Um eine vorhandene WPF-Anwendung pro Monitor dpi-fähig zu machen, bietet die nativehelpers-Bibliothek die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="9b29c-201">In order to make an existing WPF application per-monitor DPI-aware the NativeHelpers library provides following functionality:</span></span>

-   <span data-ttu-id="9b29c-202">**Markiert die WPF-Anwendung als pro-ponitor-dpi-Unterstützung:** Die WPF-Anwendung wird mit dpi-Werten pro Monitor gekennzeichnet, indem [**setprocessdpiawareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) für den aktuellen Prozess aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9b29c-202">**Marks the WPF application as per-ponitor DPI-aware:** The WPF application is marked as per-monitor DPI-aware by calling [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) for the current process.</span></span> <span data-ttu-id="9b29c-203">Wenn Sie die Anwendung mit dpi-Werten pro Monitor markieren, wird sichergestellt, dass</span><span class="sxs-lookup"><span data-stu-id="9b29c-203">Marking the application as per-monitor DPI-aware will ensure that</span></span>

    -   <span data-ttu-id="9b29c-204">Das Betriebssystem skaliert die Anwendung nicht, wenn der System-dpi nicht mit dem aktuellen dpi-Wert des Monitors identisch ist, auf dem sich das Anwendungsfenster befindet.</span><span class="sxs-lookup"><span data-stu-id="9b29c-204">The OS does not scale the application when the system DPI does not match the current DPI of the monitor the application window is on</span></span>
    -   <span data-ttu-id="9b29c-205">Die [**WM- \_ dpichanged**](wm-dpichanged.md) -Nachricht wird gesendet, wenn sich der dpi-Wert des Fensters ändert.</span><span class="sxs-lookup"><span data-stu-id="9b29c-205">The [**WM\_DPICHANGED**](wm-dpichanged.md) message is sent whenever the DPI of the window changes</span></span>

-   <span data-ttu-id="9b29c-206">**Passt die Fenster Dimension an, formatiert das Layout und renre den Grafik Inhalt erneut und wählt Schriftarten basierend auf dem anfänglichen dpi-Wert des Monitors aus, auf dem sich das Fenster befindet:** Nachdem die Anwendung mit dpi-Werten pro Monitor markiert wurde, skaliert WPF weiterhin die Fenstergröße, Grafik und Schriftgröße basierend auf dem System-dpi.</span><span class="sxs-lookup"><span data-stu-id="9b29c-206">**Adjusts the window dimension, re-layout and re-render graphics content and select fonts based on initial DPI of the monitor the window is on:** Once the application is marked as per-monitor DPI-aware, WPF will still scale the window size, graphics and font size based on the system DPI.</span></span> <span data-ttu-id="9b29c-207">Da der dpi-Wert beim APP-Start nicht garantiert identisch mit dem dpi-Wert des Monitors ist, auf dem das Fenster gestartet wird, werden diese Werte von der Bibliothek nach dem Laden des Fensters angepasst.</span><span class="sxs-lookup"><span data-stu-id="9b29c-207">Since, at app launch, the system DPI is not guaranteed to be the same as the DPI of the monitor the window is launched on, the library adjust these values once the window is loaded.</span></span> <span data-ttu-id="9b29c-208">Die Basisklasse **permonitordpiwindow** aktualisiert diese im **OnLoaded ()** -Handler.</span><span class="sxs-lookup"><span data-stu-id="9b29c-208">The base class **PerMonitorDPIWindow** updates these in the **OnLoaded()** handler.</span></span>

    <span data-ttu-id="9b29c-209">Die Fenstergröße wird aktualisiert, indem die Eigenschaften für **Breite** und **Höhe** des Fensters geändert werden.</span><span class="sxs-lookup"><span data-stu-id="9b29c-209">The Window size is updated by changing the **Width** and **Height** properties of the Window.</span></span> <span data-ttu-id="9b29c-210">Layout und Größe werden aktualisiert, indem eine entsprechende Skalierungs Transformation auf den Stamm Knoten des WPF-Fensters angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="9b29c-210">The layout and size are updated by applying an appropriate scale transform to the root node of the WPF window.</span></span>

    ```C++
    void PerMonitorDPIWindow::OnLoaded(Object^ , RoutedEventArgs^ ) 
    {   
    if (m_perMonitorEnabled)
        {
        m_source = (HwndSource^) PresentationSource::FromVisual((Visual^) this);
        HwndSourceHook^ hook = gcnew HwndSourceHook(this, &PerMonitorDPIWindow::HandleMessages);
        m_source->AddHook(hook); 
                
        //Calculate the DPI used by WPF.                    
        m_wpfDPI = 96.0 *  m_source->CompositionTarget->TransformToDevice.M11; 

        //Get the Current DPI of the monitor of the window. 
        m_currentDPI = NativeHelpers::PerMonitorDPIHelper::GetDpiForWindow(m_source->Handle);

        //Calculate the scale factor used to modify window size, graphics and text
        m_scaleFactor = m_currentDPI / m_wpfDPI; 
            
        //Update Width and Height based on the on the current DPI of the monitor
        Width = Width * m_scaleFactor;
        Height = Height * m_scaleFactor;

        //Update graphics and text based on the current DPI of the monitor
    UpdateLayoutTransform(m_scaleFactor);
        }
    }

    void PerMonitorDPIWindow::UpdateLayoutTransform(double scaleFactor)
    {
    // Adjust the rendering graphics and text size by applying the scale transform to the top         
    level visual node of the Window     

    if (m_perMonitorEnabled) 
        {       
            auto child = GetVisualChild(0);
            if (m_scaleFactor != 1.0) 
           {
            ScaleTransform^ dpiScale = gcnew ScaleTransform(scaleFactor, scaleFactor);
            child->SetValue(Window::LayoutTransformProperty, dpiScale);
            }
            else 
            {
            child->SetValue(Window::LayoutTransformProperty, nullptr);
            }           
        }
    }
    ```

    

-   <span data-ttu-id="9b29c-211">**Antwortet auf WM \_ Benachrichtigung zum dpichanged-Fenster:** aktualisieren Sie die Fenstergröße, Grafik und Schriftgröße basierend auf dem in der Fenster Benachrichtigung übergebenen dpi-Code.</span><span class="sxs-lookup"><span data-stu-id="9b29c-211">**Responds to WM\_DPICHANGED window notification:** Update the window size, graphics and font size based on the DPI passed in the window notification.</span></span> <span data-ttu-id="9b29c-212">Die Basisklasse **permonitordpiwindow** behandelt die Fenster Benachrichtigung in der Methode " **Lenker Nachrichten ()** ".</span><span class="sxs-lookup"><span data-stu-id="9b29c-212">The base class **PerMonitorDPIWindow** handles the window notification in the **HandleMessages()** method.</span></span>

    <span data-ttu-id="9b29c-213">Die Fenstergröße wird durch Aufrufen von **SetWindowPos** mithilfe der Informationen aktualisiert, die im *LPARAM* der Fenster Meldung ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9b29c-213">The Window size is updated by calling **SetWindowPos** using the information passed in the *lparam* of the window message.</span></span> <span data-ttu-id="9b29c-214">Layout und Grafik Größe werden aktualisiert, indem eine entsprechende Skalierungs Transformation auf den Stamm Knoten des WPF-Fensters angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="9b29c-214">The layout and graphics size are updated by applying an appropriate scale transform to the root node of the WPF window.</span></span> <span data-ttu-id="9b29c-215">Der Skalierungsfaktor wird mithilfe des dpi-Wert berechnet, der in der *wParam* der Fenster Meldung ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9b29c-215">The scale factor is calculated by using the DPI passed in the *wparam* of the window message.</span></span>

    ```C++
    IntPtr PerMonitorDPIWindow::HandleMessages(IntPtr hwnd, int msg, IntPtr wParam, IntPtr lParam, bool% )
    {
    double oldDpi;
    switch (msg)
        {
        case WM_DPICHANGED:
        LPRECT lprNewRect = (LPRECT)lParam.ToPointer();
        SetWindowPos(static_cast<HWND>(hwnd.ToPointer()), 0, lprNewRect->left, lprNewRect-
            >top, lprNewRect->right - lprNewRect->left, lprNewRect->bottom - lprNewRect->top, 
           SWP_NOZORDER | SWP_NOOWNERZORDER | SWP_NOACTIVATE);
        oldDpi = m_currentDPI;
        m_currentDPI = static_cast<int>(LOWORD(wParam.ToPointer()));
        if (oldDpi != m_currentDPI) 
            {
            OnDPIChanged();
            }
        break;
        }
    return IntPtr::Zero;
    }

    void PerMonitorDPIWindow::OnDPIChanged() 
    {
    m_scaleFactor = m_currentDPI / m_wpfDPI;
    UpdateLayoutTransform(m_scaleFactor);
    DPIChanged(this, EventArgs::Empty);
    }

    void PerMonitorDPIWindow::UpdateLayoutTransform(double scaleFactor)
    {
    // Adjust the rendering graphics and text size by applying the scale transform to the top         
    level visual node of the Window     

    if (m_perMonitorEnabled) 
        {       
            auto child = GetVisualChild(0);
            if (m_scaleFactor != 1.0) 
           {
            ScaleTransform^ dpiScale = gcnew ScaleTransform(scaleFactor, scaleFactor);
            child->SetValue(Window::LayoutTransformProperty, dpiScale);
            }
            else 
            {
            child->SetValue(Window::LayoutTransformProperty, nullptr);
            }           
        }
    }
    ```

    

## <a name="handling-dpi-change-for-assets-like-images"></a><span data-ttu-id="9b29c-216">Behandeln von dpi-Änderungen für Assets wie Bilder</span><span class="sxs-lookup"><span data-stu-id="9b29c-216">Handling DPI change for assets like images</span></span>

<span data-ttu-id="9b29c-217">Um Grafik Inhalte zu aktualisieren, wendet die Beispiel-WPF-Anwendung eine Skalierungs Transformation auf den Stamm Knoten der WPF-Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="9b29c-217">In order to update graphics content, the sample WPF application applies a scale transform to the root node of the WPF application.</span></span> <span data-ttu-id="9b29c-218">Dies funktioniert gut für Inhalte, die nativ von WPF (Rechteck, Text usw.) gerendert werden. Dies impliziert, dass Bitmap-Assets wie Bilder von WPF skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="9b29c-218">While this works well for content that is rendered natively by WPF (rectangle, text etc.), this implies that bitmap assets like images are scaled by WPF.</span></span>

<span data-ttu-id="9b29c-219">Um unscharfe Bitmaps zu vermeiden, die durch die Skalierung verursacht werden, kann der WPF-Anwendungsentwickler ein benutzerdefiniertes dpi-Bild Steuerelement schreiben, das basierend auf dem aktuellen dpi-Wert des Monitors, auf dem sich das Fenster befindet, ein anderes</span><span class="sxs-lookup"><span data-stu-id="9b29c-219">In order to avoid blurred bitmaps caused by scaling, the WPF application developer can write a custom DPI image control that selects a different asset based on the current DPI of the monitor the window is on.</span></span> <span data-ttu-id="9b29c-220">Das Image-Steuerelement kann sich auf das **dpichanged ()** -Ereignis stützen, das für das WPF-Fenster ausgelöst wird, das aus dem **permonitordpiwindow** verwendet wird</span><span class="sxs-lookup"><span data-stu-id="9b29c-220">The image control can rely on the **DPIChanged()** event fired for the WPF window that consumes from the **PerMonitorDPIWindow**, when the DPI changes.</span></span>

> [!Note]  
> <span data-ttu-id="9b29c-221">Das Image-Steuerelement sollte auch das Rechte Steuerelement beim Starten der APP im **geladenen** WPF-Fenster Ereignishandler auswählen.</span><span class="sxs-lookup"><span data-stu-id="9b29c-221">The image control should also select the right control during app launch in the **Loaded()** WPF window event handler.</span></span>

 

 

 