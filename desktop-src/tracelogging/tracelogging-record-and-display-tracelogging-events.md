---
title: Aufzeichnen und Anzeigen von tracelogging-Ereignissen
description: Aufzeichnen von tracelogging-Ereignissen mit Windows Performance Recorder (WPR) und Anzeigen dieser Ereignisse mit Windows Performance Analyzer (WPA).
ms.assetid: 906589FA-F48D-4105-9E56-1EC8B86542FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09be054d274fc2c2c62635cc7bf12e8cf8acdef3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858450"
---
# <a name="record-and-view-tracelogging-events"></a><span data-ttu-id="2c590-103">Aufzeichnen und Anzeigen von tracelogging-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="2c590-103">Record and View TraceLogging Events</span></span>

<span data-ttu-id="2c590-104">Aufzeichnen von tracelogging-Ereignissen mit Windows Performance Recorder (WPR) und Anzeigen dieser Ereignisse mit Windows Performance Analyzer (WPA).</span><span class="sxs-lookup"><span data-stu-id="2c590-104">Record TraceLogging events with the Windows Performance Recorder (WPR) and view them with the Windows Performance Analyzer (WPA).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2c590-105">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="2c590-105">Prerequisites</span></span>

-   <span data-ttu-id="2c590-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="2c590-106">Windows 10</span></span>
-   <span data-ttu-id="2c590-107">Die Windows 10-Version von Windows Performance Recorder (WPR) und die Windows 10-Version von Windows Performance Analyzer (WPA), die Bestandteil des Windows® Assessment and Deployment Kit (Windows ADK) ist.</span><span class="sxs-lookup"><span data-stu-id="2c590-107">The Windows 10 version of Windows Performance Recorder (WPR), and the Windows 10 version of Windows Performance Analyzer (WPA) which is part of the Windows® Assessment and Deployment Kit (Windows ADK).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2c590-108">Mit tracelogging erfasste Ablauf Verfolgungen müssen mit der Windows 10-Version von Windows Performance Recorder aufgezeichnet und mit der Windows 10-Version von Windows Performance Analyzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2c590-108">Traces captured with TraceLogging must be captured with the Windows 10 version of Windows Performance Recorder and viewed with the Windows 10 version of Windows Performance Analyzer.</span></span> <span data-ttu-id="2c590-109">Wenn Sie Ihre Ereignisse nicht erfassen oder decodieren können, vergewissern Sie sich, dass Sie die Windows 10-Version der Tools verwenden.</span><span class="sxs-lookup"><span data-stu-id="2c590-109">If you are unable to capture or decode your events, verify that you are using the Windows 10 version of the tools.</span></span>

 

### <a name="1-capture-trace-data-with-wpr"></a><span data-ttu-id="2c590-110">1. Erfassen von Ablauf Verfolgungs Daten mit WPR</span><span class="sxs-lookup"><span data-stu-id="2c590-110">1. Capture trace data with WPR</span></span>

<span data-ttu-id="2c590-111">Informationen zum Aufzeichnen einer Ablauf Verfolgung auf Windows Phone finden Sie unten unter Erfassen von tracelogging-Ereignissen auf Windows phone.</span><span class="sxs-lookup"><span data-stu-id="2c590-111">To capture a trace on Windows Phone, see Capture TraceLogging events on Windows Phone below.</span></span>

<span data-ttu-id="2c590-112">Erstellen Sie ein Windows Performance Recorder-Profil (. wprp), damit Sie die tracelogging-Ereignisse mithilfe von WPR erfassen können.</span><span class="sxs-lookup"><span data-stu-id="2c590-112">Create a Windows Performance Recorder profile (.wprp) so that you can use WPR to capture your Tracelogging events.</span></span>

<span data-ttu-id="2c590-113">**Erstellen Sie eine. Wprp-Datei**</span><span class="sxs-lookup"><span data-stu-id="2c590-113">**Create a .WPRP file**</span></span>

1.  <span data-ttu-id="2c590-114">Verwenden Sie das folgende wprp-Beispiel mit dem systemeigenen Codebeispiel in der [tracelogging-C/C++-Schnellstart](tracelogging-native-quick-start.md) oder dem verwalteten Beispiel im [verwalteten Schnellstart tracelogging](tracelogging-managed-quick-start.md).</span><span class="sxs-lookup"><span data-stu-id="2c590-114">Use the following WPRP example with the native code example in the [TraceLogging C/C++ Quick Start](tracelogging-native-quick-start.md) or the managed example in the [TraceLogging Managed Quick Start](tracelogging-managed-quick-start.md).</span></span> <span data-ttu-id="2c590-115">Wenn Sie Ereignisse von Ihrem eigenen Anbieter protokollieren, ersetzen Sie die `TODO` Abschnitte durch die entsprechenden Werte für Ihren Anbieter.</span><span class="sxs-lookup"><span data-stu-id="2c590-115">If you are logging events from your own provider, replace the `TODO` sections with the appropriate values for your provider.</span></span>

    > <span data-ttu-id="2c590-116">\[! Wichtig\]</span><span class="sxs-lookup"><span data-stu-id="2c590-116">\[!Important\]</span></span>  

     

    <span data-ttu-id="2c590-117">Wenn Sie den Schnellstart tracelogging C/C++ verwenden, geben Sie die Anbieter-GUID im- `Name` Attribut des- `<EventProvider>` Elements an.</span><span class="sxs-lookup"><span data-stu-id="2c590-117">If you are using the TraceLogging C/C++ quick start, specify the provider GUID in the `Name` attribute of the `<EventProvider>` element.</span></span> <span data-ttu-id="2c590-118">Beispiel: `<EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833" />`.</span><span class="sxs-lookup"><span data-stu-id="2c590-118">For example: `<EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833" />`.</span></span> <span data-ttu-id="2c590-119">Wenn Sie den Schnellstart Managed tracelogging verwenden, geben Sie im-Attribut des-Elements den Anbieter Namen an, dem "" vorangestellt ist \* `Name` `<EventProvider />` .</span><span class="sxs-lookup"><span data-stu-id="2c590-119">If you are using the managed TraceLogging quick start, specify the provider name prefaced by '\*' in the `Name` attribute of the `<EventProvider />` element.</span></span> <span data-ttu-id="2c590-120">Beispiel: `<EventProvider Name="*SimpleTraceLoggingProvider" />`.</span><span class="sxs-lookup"><span data-stu-id="2c590-120">For example, `<EventProvider Name="*SimpleTraceLoggingProvider" />`.</span></span>

    <span data-ttu-id="2c590-121">Wprp-Beispieldatei.</span><span class="sxs-lookup"><span data-stu-id="2c590-121">Sample WPRP file.</span></span>

    ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <!-- TODO: 
    1. Find and replace "SimpleTraceLoggingProvider" with the name of your provider.
    2. See TODO below to update GUID for your event provider
    -->
    <WindowsPerformanceRecorder Version="1.0" Author="Microsoft Corporation" Copyright="Microsoft Corporation" Company="Microsoft Corporation">
      <Profiles>
        <EventCollector Id="EventCollector_SimpleTraceLoggingProvider" Name="SimpleTraceLoggingProvider">
          <BufferSize Value="64" />
          <Buffers Value="4" />
        </EventCollector>

        <!-- TODO: 
     1. Update Name attribute in EventProvider xml element with your provider GUID, eg: Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833". Or
        if you specify an EventSource C# provider or call TraceLoggingRegister(...) without a GUID, use star (*) before your provider
        name, eg: Name="*MyEventSourceProvider" which will enable your provider appropriately.  
     2. This sample lists one EventProvider xml element and references it in a Profile with EventProviderId xml element. 
        For your component wprp, enable the required number of providers and fix the Profile xml element appropriately
    -->
        <EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="*SimpleTraceLoggingProvider" />
        
        <Profile Id="SimpleTraceLoggingProvider.Verbose.File" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" LoggingMode="File" DetailLevel="Verbose">
          <Collectors>
            <EventCollectorId Value="EventCollector_SimpleTraceLoggingProvider">
              <EventProviders>
                <!-- TODO:
     1. Fix your EventProviderId with Value same as the Id attribute on EventProvider xml element above
    -->
                <EventProviderId Value="EventProvider_SimpleTraceLoggingProvider" />
              </EventProviders>
            </EventCollectorId>
          </Collectors>
        </Profile>

        <Profile Id="SimpleTraceLoggingProvider.Light.File" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" Base="SimpleTraceLoggingProvider.Verbose.File" LoggingMode="File" DetailLevel="Light" />
        <Profile Id="SimpleTraceLoggingProvider.Verbose.Memory" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" Base="SimpleTraceLoggingProvider.Verbose.File" LoggingMode="Memory" DetailLevel="Verbose" />
        <Profile Id="SimpleTraceLoggingProvider.Light.Memory" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" Base="SimpleTraceLoggingProvider.Verbose.File" LoggingMode="Memory" DetailLevel="Light" />

      </Profiles>
    </WindowsPerformanceRecorder>
    
    ```

    

2.  <span data-ttu-id="2c590-122">Speichern Sie die Datei mit einem. Wprp-Dateinamenerweiterung.</span><span class="sxs-lookup"><span data-stu-id="2c590-122">Save the file with a .WPRP file name extension.</span></span>
3.  <span data-ttu-id="2c590-123">Starten Sie die Erfassung mithilfe von WPR von einem Eingabe Aufforderungs Fenster mit erhöhten Rechten (als Administrator ausführen).</span><span class="sxs-lookup"><span data-stu-id="2c590-123">Start the capture using WPR from an elevated (run as Administrator) Command Prompt window.</span></span>

    <span data-ttu-id="2c590-124">**<path to wpr>\\wpr.exe-Start generalprofile-Start traceloggingprovider. wprp**</span><span class="sxs-lookup"><span data-stu-id="2c590-124">**<path to wpr>\\wpr.exe -start GeneralProfile -start TraceLoggingProvider.wprp**</span></span>

    > <span data-ttu-id="2c590-125">\[! PP\]</span><span class="sxs-lookup"><span data-stu-id="2c590-125">\[!Tip\]</span></span>  
    > <span data-ttu-id="2c590-126">Für allgemeine profilerstellungszwecke können Sie auch **– Start generalprofile** zur wpr.exe Befehlszeile hinzufügen, um Systemereignisse zusammen mit den Ereignissen des Anbieters zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="2c590-126">For general profiling purposes, you can also add **–start GeneralProfile** to the wpr.exe command line to capture system events along with the events from your provider.</span></span> <span data-ttu-id="2c590-127">Wenn Sie nur Ihre Ereignisse erfassen möchten, lassen Sie das **-Start-generalprofile** aus.</span><span class="sxs-lookup"><span data-stu-id="2c590-127">If you only want to gather your events, omit **-start GeneralProfile**.</span></span>

     

4.  <span data-ttu-id="2c590-128">Führen Sie die Anwendung aus, die Ihre Ereignisse enthält.</span><span class="sxs-lookup"><span data-stu-id="2c590-128">Run the application that contains your events.</span></span>
5.  <span data-ttu-id="2c590-129">Stoppt die Erfassung der Ablauf Verfolgung.</span><span class="sxs-lookup"><span data-stu-id="2c590-129">Stop the trace capture.</span></span>

    <span data-ttu-id="2c590-130">**<path to wpr>\\wpr.exe-Beschreibung der tracecapturefile. ETL-Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c590-130">**<path to wpr>\\wpr.exe -stop TraceCaptureFile.etl description**</span></span>

    > <span data-ttu-id="2c590-131">\[! PP\]</span><span class="sxs-lookup"><span data-stu-id="2c590-131">\[!Tip\]</span></span>  
    > <span data-ttu-id="2c590-132">Wenn Sie " **– Start generalprofile** " zum Erfassen von System Ereignissen hinzugefügt haben, fügen Sie " **generalprofile** " in der obigen **wpr.exe** Befehlszeile hinzu.</span><span class="sxs-lookup"><span data-stu-id="2c590-132">If you added **–start GeneralProfile** to gather system events, add **-stop GeneralProfile** to the **wpr.exe** command line above.</span></span>

     

### <a name="2-capture-tracelogging-events-on-windows-phone"></a><span data-ttu-id="2c590-133">2. Erfassen von tracelogging-Ereignissen auf Windows Phone</span><span class="sxs-lookup"><span data-stu-id="2c590-133">2. Capture TraceLogging events on Windows Phone</span></span>

<span id="capturephone"></span><span id="CAPTUREPHONE"></span>

1.  <span data-ttu-id="2c590-134">Starten Sie tracelog, um Ereignisse von Ihrem Anbieter zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="2c590-134">Start tracelog to capture events from your provider.</span></span>

    <span data-ttu-id="2c590-135">**cmdd tracelog-Start Test-f c: \\ Test. ETL-GUID \# ProviderGUID**</span><span class="sxs-lookup"><span data-stu-id="2c590-135">**cmdd tracelog -start test -f c:\\test.etl -guid \#providerguid**</span></span>

2.  <span data-ttu-id="2c590-136">Führen Sie das Testszenario zum Protokollieren von Ereignissen aus.</span><span class="sxs-lookup"><span data-stu-id="2c590-136">Run your test scenario to log events.</span></span>
3.  <span data-ttu-id="2c590-137">Ablauf Verfolgungs Erfassung abbrechen.</span><span class="sxs-lookup"><span data-stu-id="2c590-137">Stop trace capture.</span></span>

    <span data-ttu-id="2c590-138">**cmdd tracelog-Test abbrechen**</span><span class="sxs-lookup"><span data-stu-id="2c590-138">**cmdd tracelog -stop test**</span></span>

4.  <span data-ttu-id="2c590-139">Zusammenführen der Ergebnisse der System Ablauf Verfolgung mit den Ablauf Verfolgungs Ergebnissen.</span><span class="sxs-lookup"><span data-stu-id="2c590-139">Merge the system trace results with your trace results.</span></span>

    <span data-ttu-id="2c590-140">**cmdd XPerf-Merge c: \\ Test. ETL c: \\ testgemergt. ETL**</span><span class="sxs-lookup"><span data-stu-id="2c590-140">**cmdd xperf -merge c:\\test.etl c:\\testmerged.etl**</span></span>

5.  <span data-ttu-id="2c590-141">Rufen Sie die zusammengeführte Protokolldatei ab.</span><span class="sxs-lookup"><span data-stu-id="2c590-141">Retrieve the merged log file.</span></span>

    <span data-ttu-id="2c590-142">**getd c: \\ testgemergt. ETL**</span><span class="sxs-lookup"><span data-stu-id="2c590-142">**getd c:\\testmerged.etl**</span></span>

### <a name="3-view-tracelogging-data-using-windows-performance-analyzer"></a><span data-ttu-id="2c590-143">3. Anzeigen von Ablauf Verfolgungs Daten mithilfe von Windows Performance Analyzer.</span><span class="sxs-lookup"><span data-stu-id="2c590-143">3. View TraceLogging data using Windows Performance Analyzer.</span></span>

<span data-ttu-id="2c590-144">WPA ist zurzeit der einzige Viewer, den Sie zum Anzeigen von tracelogging-Ablauf Verfolgungs Dateien (ETL-Dateien) verwenden können.</span><span class="sxs-lookup"><span data-stu-id="2c590-144">WPA is currently the only viewer you can use to view TraceLogging trace (.etl) files.</span></span>

1.  <span data-ttu-id="2c590-145">Starten Sie WPA.</span><span class="sxs-lookup"><span data-stu-id="2c590-145">Start WPA.</span></span>

    <span data-ttu-id="2c590-146">**<path to wpr>\\wpa.exe traceloggingresults. ETL**</span><span class="sxs-lookup"><span data-stu-id="2c590-146">**<path to wpr>\\wpa.exe traceLoggingResults.etl**</span></span>

2.  <span data-ttu-id="2c590-147">Laden Sie die Ablauf Verfolgungs Datei (. ETL), die Sie im obigen wpa.exe Befehl angegeben haben, z. b. traceloggingresults. ETL.</span><span class="sxs-lookup"><span data-stu-id="2c590-147">Load the trace (.etl) file that you specified in the wpa.exe command above, e.g. traceLoggingResults.etl.</span></span>
3.  <span data-ttu-id="2c590-148">Sehen Sie sich die Anbieter Ereignisse an.</span><span class="sxs-lookup"><span data-stu-id="2c590-148">View your provider events.</span></span> <span data-ttu-id="2c590-149">Erweitern Sie im WPA Graph-Explorer die Option **System Aktivität**.</span><span class="sxs-lookup"><span data-stu-id="2c590-149">In the WPA Graph Explorer, expand **System Activity**.</span></span>
4.  <span data-ttu-id="2c590-150">Doppelklicken Sie auf den Bereich **generische Ereignisse** , um die Ereignisse im Bereich **Analyse** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2c590-150">Double-click in the **Generic Events** pane to view the events in the **Analysis** pane.</span></span>

    ![generische Ereignisse erweitern](images/expandsystemactivity.png)

5.  <span data-ttu-id="2c590-152">Suchen Sie im Analysebereich nach den Ereignissen des Anbieters, um zu überprüfen, ob tracelogging funktioniert.</span><span class="sxs-lookup"><span data-stu-id="2c590-152">In the Analysis pane, locate the events from your provider to verify that TraceLogging is working.</span></span>

    <span data-ttu-id="2c590-153">Suchen Sie in der Spalte **Anbieter Name** der Tabelle **generische Ereignisse** die Zeile mit dem Anbieter Namen, und wählen Sie Sie aus.</span><span class="sxs-lookup"><span data-stu-id="2c590-153">In the **Provider Name** column of the **Generic Events** table, find and select the row with your provider name.</span></span>

    <span data-ttu-id="2c590-154">Wenn Sie über mehrere zu sortierende Anbieter verfügen, klicken Sie auf die Spaltenüberschrift, um nach Spaltennamen zu sortieren. Dies erleichtert die Suche nach Ihrem Anbieter.</span><span class="sxs-lookup"><span data-stu-id="2c590-154">If you have multiple providers to sort through, click the column header to sort by column name which may make it easier to find your provider.</span></span>

    <span data-ttu-id="2c590-155">Wenn Sie Ihren Anbieter gefunden haben, klicken Sie mit der rechten Maustaste auf den Namen, und wählen Sie **zur Auswahl Filtern**.</span><span class="sxs-lookup"><span data-stu-id="2c590-155">When you find your provider, right click on the name and select **Filter to Selection**.</span></span>

    ![Auswahl an Anbieter Filtern](images/filtertoselection.png)

    <span data-ttu-id="2c590-157">Das-Ereignis für simpletraceloggingprovider und dessen Wert werden im unteren Bereich des Analyse Fensters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2c590-157">The event for the SimpleTraceLoggingProvider and its value will appear in the bottom pane of the Analysis window.</span></span> <span data-ttu-id="2c590-158">Erweitern Sie den Anbieter Namen, um die Ereignisse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2c590-158">Expand the provider name to see the events.</span></span>

    ![Anzeigen des Ereignisses von simpletraceloggingprovider](images/eventview.png)

    <span data-ttu-id="2c590-160">Weitere Informationen zur Verwendung von WPA finden Sie unter [Windows Performance Analyzer](/previous-versions/windows/it-pro/windows-8.1-and-8/hh448170(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="2c590-160">For more information about using WPA, see [Windows Performance Analyzer](/previous-versions/windows/it-pro/windows-8.1-and-8/hh448170(v=win.10)).</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="2c590-161">Zusammenfassung und nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="2c590-161">Summary and next steps</span></span>

<span data-ttu-id="2c590-162">Der Prozess zum Aufzeichnen und Anzeigen von ETW-Ereignissen mithilfe von WPR und WPA gilt auch für tracelogging-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="2c590-162">The process for recording and viewing ETW events using WPR and WPA apply equally well to TraceLogging events.</span></span>

<span data-ttu-id="2c590-163">Weitere Beispiele für tracelogging finden Sie unter [C/C++ tracelogging-Beispiele](tracelogging-c-cpp-tracelogging-examples.md) .</span><span class="sxs-lookup"><span data-stu-id="2c590-163">See [C/C++ Tracelogging Examples](tracelogging-c-cpp-tracelogging-examples.md) for additional TraceLogging examples.</span></span>

 

 