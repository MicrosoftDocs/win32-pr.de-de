---
title: Aufzeichnen und Anzeigen von TraceLogging-Ereignissen
description: Zeichnen Sie TraceLogging-Ereignisse mit dem Windows Performance Recorder (WPR) auf, und zeigen Sie sie mit dem Windows Leistungsanalyse (WPA) an.
ms.assetid: 906589FA-F48D-4105-9E56-1EC8B86542FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c77c1a1759988252f57c1ec54dca77cffaa21832878ead6ba8a827df3329fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966541"
---
# <a name="record-and-view-tracelogging-events"></a>Aufzeichnen und Anzeigen von TraceLogging-Ereignissen

Zeichnen Sie TraceLogging-Ereignisse mit dem Windows Performance Recorder (WPR) auf, und zeigen Sie sie mit dem Windows Leistungsanalyse (WPA) an.

## <a name="prerequisites"></a>Voraussetzungen

-   Windows 10
-   Die Windows 10 Version von Windows Performance Recorder (WPR) und die Windows 10-Version von Windows Leistungsanalyse (WPA), die Teil des Windows® Assessment and Deployment Kit (Windows ADK) ist.

> [!IMPORTANT]
> Mit TraceLogging erfasste Ablaufverfolgungen müssen mit der Windows 10 Version von Windows Performance Recorder erfasst und mit der Windows 10 Version von Windows Leistungsanalyse angezeigt werden. Wenn Sie Ihre Ereignisse nicht erfassen oder decodieren können, überprüfen Sie, ob Sie die Windows 10 Version der Tools verwenden.

 

### <a name="1-capture-trace-data-with-wpr"></a>1. Erfassen von Ablaufverfolgungsdaten mit WPR

Informationen zum Erfassen einer Ablaufverfolgung auf Windows Phone finden Sie unter Erfassen von TraceLogging-Ereignissen auf Windows Phone weiter unten.

Erstellen Sie ein Windows Performance Recorder-Profil (WPRP), damit Sie WPR zum Erfassen Ihrer Tracelogging-Ereignisse verwenden können.

**Erstellen Sie eine . WPRP-Datei**

1.  Verwenden Sie das folgende WPRP-Beispiel mit dem nativen Codebeispiel im [TraceLogging C/C++-Schnellstart](tracelogging-native-quick-start.md) oder dem verwalteten Beispiel im [traceLogging Managed Schnellstart](tracelogging-managed-quick-start.md). Wenn Sie Ereignisse von Ihrem eigenen Anbieter protokollieren, ersetzen Sie die `TODO` Abschnitte durch die entsprechenden Werte für Ihren Anbieter.

    > \[! Wichtig\]  

     

    Wenn Sie den TraceLogging C/C++-Schnellstart verwenden, geben Sie die Anbieter-GUID im `Name` -Attribut des `<EventProvider>` -Elements an. Beispiel: `<EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833" />`. Wenn Sie den verwalteten TraceLogging-Schnellstart verwenden, geben Sie den Anbieternamen vor " \* " im `Name` -Attribut des `<EventProvider />` -Elements an. Beispiel: `<EventProvider Name="*SimpleTraceLoggingProvider" />`.

    WPRP-Beispieldatei.

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

    

2.  Speichern Sie die Datei mit einem . WPRP-Dateinamenerweiterung.
3.  Starten Sie die Erfassung mit WPR in einem Eingabeaufforderungsfenster mit erhöhten Rechten (als Administrator ausführen).

    **<path to wpr>\\wpr.exe -start GeneralProfile -start TraceLoggingProvider.wprp**

    > \[! Tipp\]  
    > Für allgemeine Profilerstellungszwecke können Sie auch **–start GeneralProfile** zur wpr.exe Befehlszeile hinzufügen, um Systemereignisse zusammen mit den Ereignissen ihres Anbieters zu erfassen. Wenn Sie nur Ihre Ereignisse erfassen möchten, lassen Sie **-start GeneralProfile aus.**

     

4.  Führen Sie die Anwendung aus, die Ihre Ereignisse enthält.
5.  Beenden Sie die Ablaufverfolgungserfassung.

    **<path to wpr>\\wpr.exe -stop TraceCaptureFile.etl description**

    > \[! Tipp\]  
    > Wenn Sie **–start GeneralProfile** hinzugefügt haben, um Systemereignisse zu sammeln, fügen Sie der **obigenwpr.exe** Befehlszeile **-stop GeneralProfile** hinzu.

     

### <a name="2-capture-tracelogging-events-on-windows-phone"></a>2. Erfassen von TraceLogging-Ereignissen auf Windows Phone

<span id="capturephone"></span><span id="CAPTUREPHONE"></span>

1.  Starten Sie das Ablaufverfolgungsprotokoll, um Ereignisse von Ihrem Anbieter zu erfassen.

    **cmdd tracelog -start test -f c: \\ test.etl -guid \# providerguid**

2.  Führen Sie Ihr Testszenario aus, um Ereignisse zu protokollieren.
3.  Beenden Sie die Ablaufverfolgungserfassung.

    **cmdd tracelog -stop test**

4.  Führen Sie die Ergebnisse der Systemablaufverfolgung mit ihren Ablaufverfolgungsergebnissen zusammen.

    **cmdd xperf -merge c: \\ test.etl c: \\ testmerged.etl**

5.  Rufen Sie die zusammengeführte Protokolldatei ab.

    **getd c: \\ testmerged.etl**

### <a name="3-view-tracelogging-data-using-windows-performance-analyzer"></a>3. Anzeigen von TraceLogging-Daten mit Windows Leistungsanalyse.

WPA ist derzeit der einzige Viewer, den Sie zum Anzeigen von TraceLogging-Ablaufverfolgungsdateien (.etl) verwenden können.

1.  Starten Sie WPA.

    **<path to wpr>\\wpa.exe traceLoggingResults.etl**

2.  Laden Sie die Ablaufverfolgungsdatei (.etl), die Sie im obigen wpa.exe Befehl angegeben haben, z. B. traceLoggingResults.etl.
3.  Zeigen Sie Die Anbieterereignisse an. Erweitern Sie im WPA Graph Explorer die Option **Systemaktivität**.
4.  Doppelklicken Sie auf den Bereich **Generische Ereignisse,** um die Ereignisse im **Analysebereich** anzuzeigen.

    ![Generische Ereignisse erweitern](images/expandsystemactivity.png)

5.  Suchen Sie im Analysebereich nach den Ereignissen ihres Anbieters, um zu überprüfen, ob TraceLogging funktioniert.

    Suchen Sie in der Spalte **Anbietername** der Tabelle **Generische Ereignisse** die Zeile mit ihrem Anbieternamen, und wählen Sie sie aus.

    Wenn Mehrere Anbieter sortiert werden müssen, klicken Sie auf die Spaltenüberschrift, um nach Spaltenname zu sortieren, was die Suche nach Ihrem Anbieter erleichtern kann.

    Wenn Sie Ihren Anbieter finden, klicken Sie mit der rechten Maustaste auf den Namen, und wählen **Sie Nach Auswahl filtern** aus.

    ![Filterauswahl zum Anbieter](images/filtertoselection.png)

    Das Ereignis für SimpleTraceLoggingProvider und seinen Wert wird im unteren Bereich des Analysefensters angezeigt. Erweitern Sie den Anbieternamen, um die Ereignisse anzuzeigen.

    ![Anzeigen des Ereignisses aus simpletraceloggingprovider](images/eventview.png)

    Weitere Informationen zur Verwendung von WPA finden Sie unter [Windows Leistungsanalyse](/previous-versions/windows/it-pro/windows-8.1-and-8/hh448170(v=win.10)).

## <a name="summary-and-next-steps"></a>Zusammenfassung und nächste Schritte

Der Prozess zum Aufzeichnen und Anzeigen von ETW-Ereignissen mit WPR und WPA gilt ebenso gut für TraceLogging-Ereignisse.

Weitere TraceLogging-Beispiele finden Sie unter [C/C++-Beispiele](tracelogging-c-cpp-tracelogging-examples.md) für die Ablaufverfolgung.

 

 