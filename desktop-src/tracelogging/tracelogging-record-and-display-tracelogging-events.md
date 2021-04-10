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
# <a name="record-and-view-tracelogging-events"></a>Aufzeichnen und Anzeigen von tracelogging-Ereignissen

Aufzeichnen von tracelogging-Ereignissen mit Windows Performance Recorder (WPR) und Anzeigen dieser Ereignisse mit Windows Performance Analyzer (WPA).

## <a name="prerequisites"></a>Voraussetzungen

-   Windows 10
-   Die Windows 10-Version von Windows Performance Recorder (WPR) und die Windows 10-Version von Windows Performance Analyzer (WPA), die Bestandteil des Windows® Assessment and Deployment Kit (Windows ADK) ist.

> [!IMPORTANT]
> Mit tracelogging erfasste Ablauf Verfolgungen müssen mit der Windows 10-Version von Windows Performance Recorder aufgezeichnet und mit der Windows 10-Version von Windows Performance Analyzer angezeigt werden. Wenn Sie Ihre Ereignisse nicht erfassen oder decodieren können, vergewissern Sie sich, dass Sie die Windows 10-Version der Tools verwenden.

 

### <a name="1-capture-trace-data-with-wpr"></a>1. Erfassen von Ablauf Verfolgungs Daten mit WPR

Informationen zum Aufzeichnen einer Ablauf Verfolgung auf Windows Phone finden Sie unten unter Erfassen von tracelogging-Ereignissen auf Windows phone.

Erstellen Sie ein Windows Performance Recorder-Profil (. wprp), damit Sie die tracelogging-Ereignisse mithilfe von WPR erfassen können.

**Erstellen Sie eine. Wprp-Datei**

1.  Verwenden Sie das folgende wprp-Beispiel mit dem systemeigenen Codebeispiel in der [tracelogging-C/C++-Schnellstart](tracelogging-native-quick-start.md) oder dem verwalteten Beispiel im [verwalteten Schnellstart tracelogging](tracelogging-managed-quick-start.md). Wenn Sie Ereignisse von Ihrem eigenen Anbieter protokollieren, ersetzen Sie die `TODO` Abschnitte durch die entsprechenden Werte für Ihren Anbieter.

    > \[! Wichtig\]  

     

    Wenn Sie den Schnellstart tracelogging C/C++ verwenden, geben Sie die Anbieter-GUID im- `Name` Attribut des- `<EventProvider>` Elements an. Beispiel: `<EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833" />`. Wenn Sie den Schnellstart Managed tracelogging verwenden, geben Sie im-Attribut des-Elements den Anbieter Namen an, dem "" vorangestellt ist \* `Name` `<EventProvider />` . Beispiel: `<EventProvider Name="*SimpleTraceLoggingProvider" />`.

    Wprp-Beispieldatei.

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

    

2.  Speichern Sie die Datei mit einem. Wprp-Dateinamenerweiterung.
3.  Starten Sie die Erfassung mithilfe von WPR von einem Eingabe Aufforderungs Fenster mit erhöhten Rechten (als Administrator ausführen).

    **<path to wpr>\\wpr.exe-Start generalprofile-Start traceloggingprovider. wprp**

    > \[! PP\]  
    > Für allgemeine profilerstellungszwecke können Sie auch **– Start generalprofile** zur wpr.exe Befehlszeile hinzufügen, um Systemereignisse zusammen mit den Ereignissen des Anbieters zu erfassen. Wenn Sie nur Ihre Ereignisse erfassen möchten, lassen Sie das **-Start-generalprofile** aus.

     

4.  Führen Sie die Anwendung aus, die Ihre Ereignisse enthält.
5.  Stoppt die Erfassung der Ablauf Verfolgung.

    **<path to wpr>\\wpr.exe-Beschreibung der tracecapturefile. ETL-Beschreibung**

    > \[! PP\]  
    > Wenn Sie " **– Start generalprofile** " zum Erfassen von System Ereignissen hinzugefügt haben, fügen Sie " **generalprofile** " in der obigen **wpr.exe** Befehlszeile hinzu.

     

### <a name="2-capture-tracelogging-events-on-windows-phone"></a>2. Erfassen von tracelogging-Ereignissen auf Windows Phone

<span id="capturephone"></span><span id="CAPTUREPHONE"></span>

1.  Starten Sie tracelog, um Ereignisse von Ihrem Anbieter zu erfassen.

    **cmdd tracelog-Start Test-f c: \\ Test. ETL-GUID \# ProviderGUID**

2.  Führen Sie das Testszenario zum Protokollieren von Ereignissen aus.
3.  Ablauf Verfolgungs Erfassung abbrechen.

    **cmdd tracelog-Test abbrechen**

4.  Zusammenführen der Ergebnisse der System Ablauf Verfolgung mit den Ablauf Verfolgungs Ergebnissen.

    **cmdd XPerf-Merge c: \\ Test. ETL c: \\ testgemergt. ETL**

5.  Rufen Sie die zusammengeführte Protokolldatei ab.

    **getd c: \\ testgemergt. ETL**

### <a name="3-view-tracelogging-data-using-windows-performance-analyzer"></a>3. Anzeigen von Ablauf Verfolgungs Daten mithilfe von Windows Performance Analyzer.

WPA ist zurzeit der einzige Viewer, den Sie zum Anzeigen von tracelogging-Ablauf Verfolgungs Dateien (ETL-Dateien) verwenden können.

1.  Starten Sie WPA.

    **<path to wpr>\\wpa.exe traceloggingresults. ETL**

2.  Laden Sie die Ablauf Verfolgungs Datei (. ETL), die Sie im obigen wpa.exe Befehl angegeben haben, z. b. traceloggingresults. ETL.
3.  Sehen Sie sich die Anbieter Ereignisse an. Erweitern Sie im WPA Graph-Explorer die Option **System Aktivität**.
4.  Doppelklicken Sie auf den Bereich **generische Ereignisse** , um die Ereignisse im Bereich **Analyse** anzuzeigen.

    ![generische Ereignisse erweitern](images/expandsystemactivity.png)

5.  Suchen Sie im Analysebereich nach den Ereignissen des Anbieters, um zu überprüfen, ob tracelogging funktioniert.

    Suchen Sie in der Spalte **Anbieter Name** der Tabelle **generische Ereignisse** die Zeile mit dem Anbieter Namen, und wählen Sie Sie aus.

    Wenn Sie über mehrere zu sortierende Anbieter verfügen, klicken Sie auf die Spaltenüberschrift, um nach Spaltennamen zu sortieren. Dies erleichtert die Suche nach Ihrem Anbieter.

    Wenn Sie Ihren Anbieter gefunden haben, klicken Sie mit der rechten Maustaste auf den Namen, und wählen Sie **zur Auswahl Filtern**.

    ![Auswahl an Anbieter Filtern](images/filtertoselection.png)

    Das-Ereignis für simpletraceloggingprovider und dessen Wert werden im unteren Bereich des Analyse Fensters angezeigt. Erweitern Sie den Anbieter Namen, um die Ereignisse anzuzeigen.

    ![Anzeigen des Ereignisses von simpletraceloggingprovider](images/eventview.png)

    Weitere Informationen zur Verwendung von WPA finden Sie unter [Windows Performance Analyzer](/previous-versions/windows/it-pro/windows-8.1-and-8/hh448170(v=win.10)).

## <a name="summary-and-next-steps"></a>Zusammenfassung und nächste Schritte

Der Prozess zum Aufzeichnen und Anzeigen von ETW-Ereignissen mithilfe von WPR und WPA gilt auch für tracelogging-Ereignisse.

Weitere Beispiele für tracelogging finden Sie unter [C/C++ tracelogging-Beispiele](tracelogging-c-cpp-tracelogging-examples.md) .

 

 