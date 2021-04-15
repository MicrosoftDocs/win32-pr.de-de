---
title: Profilerstellung für DirectX-Apps
description: Zeigt, wie Sie einige der wichtigsten Leistungszeit Messungen für eine DirectX-App mithilfe der XPerf-und gpuview-Tools Messen, die als Teil des Windows Performance Toolkit ausgeliefert werden.
ms.assetid: 4B2F7273-C9B0-4DD3-B559-6220CDE62129
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0280389d4f8f2161e5e07f8906df7ea0484ad458
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104554415"
---
# <a name="profiling-directx-apps"></a>Profilerstellung für DirectX-Apps

Dadurch wird gezeigt, wie Sie einige der wichtigsten Leistungszeit Messungen für eine [DirectX](/previous-versions/windows/apps/jj262109(v=win.10)) -App mithilfe der **XPerf** -und **gpuview** -Tools Messen, die als Teil des Windows Performance Toolkit ausgeliefert werden. Dabei handelt es sich nicht um eine umfassende Anleitung zum Verständnis der Tools, sondern um die spezifische Anwendbarkeit zum Analysieren der DirectX-App-Leistung. Obwohl die meisten der hier beschriebenen Techniken für alle DirectX-apps relevant sind, sind Sie für apps, die Swapketten verwenden, und nicht für in XAML basierende DirectX-Anwendungen, die SIS/VSIs und XAML-Animationen verwenden, am relevantesten. Wir führen Sie durch die wichtigsten Leistungszeit Messungen, die Art und Weise, wie Sie die Tools erwerben und installieren, und nehmen dann die Leistungs Messungs Ablauf Verfolgungen vor

## <a name="about-the-tools"></a>Informationen zu den Tools

### <a name="xperf"></a>**XPerf**

**XPerf** ist ein Satz von Leistungsanalyse Tools, die auf der Ereignis Ablauf Verfolgung für Windows (Event Tracing for Windows, etw) basiert, die für die Messung und Analyse der detaillierten System-und App-Leistung und Ressourcennutzung Ab Windows 8 verfügt dieses Befehlszeilen Tool über eine grafische Benutzeroberfläche, die als Windows Performance Recorder (WPR) und Windows Performance Analyzer (WPA) bezeichnet wird. Weitere Informationen zu diesen Tools finden Sie auf der Webseite für [Windows Performance Toolkit](/previous-versions/windows/it-pro/windows-8.1-and-8/hh162945(v=win.10)) (WPT): [Windows Performance Toolkit](/previous-versions/windows/it-pro/windows-8.1-and-8/hh162945(v=win.10)).

Ein etw sammelt angeforderte Kernel Ereignisse und speichert Sie in einer Datei, die als ETL-Datei (Event Trace Log) bezeichnet wird. Diese Kernel Ereignisse bieten umfassende Informationen zu einer APP und zu System Merkmalen, wenn die app ausgeführt wird. Daten werden gesammelt, indem die Ablauf Verfolgungs Erfassung aktiviert, das gewünschte App-Szenario durchgeführt wird, das analysiert werden muss, und die Erfassung, die die Daten in einer ETL-Datei speichert. Anschließend können Sie die Datei auf demselben oder einem anderen Computer analysieren, indem Sie entweder das Befehlszeilen Tool **xperf.exe** oder das Tool für die visuelle Ablauf Verfolgungs Analyse **xperfview.exe**.

### <a name="gpuview"></a>GPUView

**Gpuview** ist ein Entwicklungs Tool zum Bestimmen der Leistung von GPU (Graphics Processing Unit) und CPU. Sie untersucht die Leistung hinsichtlich der DMA-Puffer Verarbeitung (Direct Memory Access) und sämtlicher anderer Videoverarbeitung auf der Video Hardware.

Bei [DirectX](/previous-versions/windows/apps/jj262109(v=win.10)) -apps, die sich stark auf die GPU stützen, ist **gpuview** ein leistungsfähiges Tool zum Verständnis der Beziehung zwischen der Arbeit auf der CPU und der GPU. Weitere Informationen zu **gpuview** finden [Sie unter Verwenden von gpuview](/windows-hardware/drivers/display/using-gpuview).

Ähnlich wie **XPerf** wird zunächst eine ETW-Ablauf Verfolgung durchgeführt, indem der Ablauf Verfolgungs Dienst gestartet wird. dabei wird das Szenario ausgeführt, bei dem für die APP eine Analyse erforderlich ist, und der Dienst wird beendet und die Informationen in einer ETL-Datei gespeichert. In **gpuview** werden die in der ETL-Datei vorhandenen Daten in einem grafischen Format dargestellt.

Nach der Installation des **gpuview** -Tools empfiehlt es sich, das Thema "**gpuview** es Main Display" im Menü "**gpuview** Help" zu lesen. Sie enthält nützliche Informationen zum Interpretieren der **gpuview** -Benutzeroberfläche.

## <a name="installing-the-tools"></a>Installieren der Tools

Sowohl **XPerf** als auch **gpuview** sind im Windows Performance Toolkit (WPT) enthalten.

**XPerf** wird als Teil des Windows Software Development Kit (SDK) für Windows ausgeliefert. [Laden Sie die Windows SDK herunter](https://dev.windows.com/downloads).

**Gpuview** ist im Windows Assessment and Deployment Kit (Windows ADK) verfügbar. [Laden Sie das Windows ADK herunter](/windows-hardware/get-started/adk-install).

Nach der Installation müssen Sie die Verzeichnisse, die **XPerf** und **gpuview** enthalten, zur System-"Path"-Variablen hinzufügen.

Klicken Sie auf die Schaltfläche Start, und geben Sie System Variablen ein. Das System Eigenschaftenfenster wird geöffnet. Klicken Sie auf "System Umgebungsvariablen bearbeiten". Wählen Sie im Dialogfeld "System Eigenschaften" die Option "Umgebungsvariablen" aus. Die Variable "Path" befindet sich unter "System Variablen". Fügen Sie das Verzeichnis mit **xperf.exe** und **GPUView.exe** an den Pfad an. Diese ausführbaren Dateien befinden sich im Verzeichnis "Windows Performance Toolkit" innerhalb der Windows-Kits. Der Standard Speicherort ist: **C: \\ Program Files (x86) \\ Windows Kits \\ 10 \\ Windows Performance Toolkit**.

## <a name="performance-time-measurements"></a>Leistungszeit Messungen

Die meisten apps erwarten einen reibungslosen Betrieb und können auf Benutzereingaben reaktionsfähig sein. Abhängig von dem Szenario, das Sie möchten, ist ein Aspekt der Leistung jedoch möglicherweise wichtiger als ein anderer. Beispielsweise ist für eine Newsreader-APP, die auf einem Touchscreen-Tablet-PC ausgeführt wird, der wichtigste Aspekt, einen einzelnen Artikel gleichzeitig anzuzeigen und den gleichen oder einen anderen Artikel zu schwenken/zu zoomen/zu scrollen. In diesem Szenario ist die Möglichkeit, den gesamten Inhalt jedes Frames zu erzeugen, nicht erforderlich. Allerdings ist die Möglichkeit, durch den Artikel reibungslos nach einer touchbewegung zu scrollen, äußerst wichtig.

In einer anderen-Instanz wird ein Spiel oder eine Video Rendering-APP, die viele Animationen verwendet, bei der Löschung von Frames abruft. In diesem Fall ist es äußerst wichtig, Inhalte auf dem Bildschirm zu präsentieren, ohne die Benutzereingaben zu überarbeiten.

Um zu verstehen, welcher Teil der APP problematisch ist, besteht der erste Schritt darin, die wichtigsten Szenarien zu entscheiden. Nachdem Sie die wichtigsten Aspekte der APP verstanden haben und wissen, wie Sie ausgeführt werden, wird die Suche nach Problemen mithilfe der Tools einfacher.

Einige der gängigsten leistungszeitmetriken lauten wie folgt:

### <a name="startup-time"></a>Start Zeit

Die Zeit, die vom Prozessstart zum ersten Anzeigen des Bildschirms gemessen wird. Diese Messung ist nützlicher, wenn das System warm ist, d. h., dass die Messung nach einiger Zeit gestartet wird.

### <a name="cpu-time-per-frame"></a>CPU-Zeit pro Frame

Der Zeitpunkt, zu dem die CPU aktiv die APP-Arbeitsauslastung für einen Frame verarbeitet. Wenn die APP reibungslos ausgeführt wird, erfolgt die gesamte für einen Frame erforderliche Verarbeitung innerhalb eines v-Synchronisierungs Intervalls. Bei der Monitor Aktualisierungsrate von 60Hz ergibt dies 16 MS Pro Frame. Wenn die CPU-Zeit/der Rahmen größer als 16 ms ist, sind möglicherweise CPU-Optimierungen erforderlich, um eine reibungslose App-Auslastung zu erzielen.

### <a name="gpu-time-per-frame"></a>GPU-Zeit pro Frame

Die Zeit, die GPU aktiv die APP-Arbeitsauslastung für einen Frame verarbeitet. Eine APP ist GPU-gebunden, wenn die Zeit, die zum Verarbeiten eines Frame-Daten Wertes benötigt wird, mehr als 16 ms beträgt.

Wenn Sie erkennen können, ob eine APP CPU-oder GPU-gebunden ist, wird der problematische Teil des Codes eingrenzen.

## <a name="taking-performance-time-measurement-trace"></a>Ablauf Verfolgung für die Leistungszeit Messung

Führen Sie diese Schritte aus, um eine Ablauf Verfolgung vorzunehmen:

1.  Öffnen Sie ein Befehlsfenster als Administrator.
2.  Schließen Sie die APP, wenn Sie bereits ausgeführt wird.
3.  Wechseln Sie in das Verzeichnis " *gpuview* " im Windows Performance Toolkit-Ordner.
4.  Geben Sie "Log. cmd" ein, um die Ereignis Ablauf Verfolgung zu starten. Mit dieser Option werden die interessantesten Ereignisse protokolliert. Bei anderen verfügbaren Optionen wird ein anderer Bereich der Ereignisse protokolliert. Im Modus "v" oder "ausführliche Log" werden alle Ereignisse erfasst, die **gpuview** kennt.
5.  Starten Sie das Beispiel, und führen Sie das Beispiel auf eine Weise aus, die den Leistungs Pfad abdeckt, den Sie analysieren müssen.
6.  Wechseln Sie zurück zu den Befehls Fenstern, und geben Sie "Log. cmd" erneut ein, um die Protokollierung zu verhindern.
7.  Dadurch wird eine Datei mit dem Namen "gemergt. ETL" im Ordner " *gpuview* " ausgegeben. Sie können diese Datei an einem anderen Speicherort speichern, und Sie können Sie auf demselben oder einem anderen Computer analysieren. Um Stapel Erfassungs Details anzuzeigen, speichern Sie die der APP zugeordnete Symbol Datei (PDB-Datei).

## <a name="measurements"></a>Messungen


> [!Note]  
> Das Beispiel für die Messung der Geometrie der Geometrie erfolgt auf einem Vierkern-Computer mit integrierter DirectX11-Grafikkarte. Die Messungen variieren je nach Computerkonfiguration.

 

In diesem Abschnitt wird veranschaulicht, wie Sie die Messwerte für die Startzeit, die CPU-und GPU-Zeit pro Frame messen. Sie können eine Leistungs Ablauf Verfolgung für das gleiche Beispiel auf Ihrem Computer erfassen und die Unterschiede in den verschiedenen Messungen sehen.

Um die Ablauf Verfolgung in " **gpuview**" zu analysieren, öffnen Sie die Datei "gemergt. ELT" mit **GPUView.exe**.

### <a name="startup-time"></a>Start Zeit

Die Startzeit wird von der gesamten Zeit bis zum Start der APP gemessen, bis der Inhalt zuerst auf dem Bildschirm angezeigt wird.

Die Start Zeitmessung wird am besten durchgeführt, indem Sie die im vorherigen Abschnitt aufgeführten Schritte mit den folgenden Variationen durchführt:

-   Wenn Sie die Start Messungen zum ersten Mal starten, wenn Sie die app starten, wird Sie als Kaltstart bezeichnet. Dies kann von Messungen abweichen, die nach dem Starten der APP mehrmals in einem kurzen Zeitraum durchgeführt werden. Dies wird als Warmstart bezeichnet. Je nachdem, wie viele Ressourcen eine APP beim Start erstellt, kann es einen großen Unterschied zwischen den beiden Startzeiten geben. Abhängig von den App-Zielen könnte das Messen eines oder das andere wünschenswert sein.
-   Wenn Sie Leistungsinformationen protokollieren, beenden Sie die APP, sobald der erste Frame auf dem Bildschirm angezeigt wird.

### <a name="calculating-start-up-time-using-gpuview"></a>Berechnen der Startzeit mithilfe von **gpuview**

1.  Scrollen Sie in **gpuview** nach unten zum relevanten Prozess, in diesem Fall GeometryRealization.exe.

    ![Screenshot, der ein Beispiel für Prozesse in "gpuview" anzeigt.](images/profile1.png)

2.  Die Kontext-CPU-Warteschlange stellt die Grafik Auslastung der Hardware in der Warteschlange dar, wird jedoch nicht notwendigerweise von der Hardware verarbeitet. Wenn die Ablauf Verfolgungs Datei geöffnet wird, werden alle Ereignisse angezeigt, die zwischen dem Zeitpunkt der Ablauf Verfolgung protokolliert wurden. Wählen Sie zum Berechnen der Startzeit die gewünschte Region aus, und vergrößern Sie den anfänglichen Teil der ersten Kontext-CPU-Warteschlange (Dies ist die Aktivität, die Aktivität anzeigt) mithilfe von STRG + Z. Weitere Informationen zu **gpuview** -Steuerelementen finden Sie im Abschnitt "Zusammenfassung der **gpuview** -Steuerelemente" im Abschnitt zur **gpuview** -Hilfedatei. Die folgende Abbildung zeigt nur den GeometryRealization.exe Prozess, der zum ersten Teil der Kontext-CPU-Warteschlange vergrößert wurde. Die Farbe der Kontext-CPU-Warteschlange wird durch das Rechteck rechts unterhalb der Warteschlange und die gleichen Farb Datenpakete in der Warteschlange gekennzeichnet, die auf der Hardware in die Warteschlange eingereiht werden. Das schraffurpaketpaket in der Kontext Warteschlange zeigt das aktuelle Paket an, was bedeutet, dass die APP die Hardware auf dem Bildschirm anzeigen möchte.

    ![Screenshot, der Beispiele für "context C P U Queue" anzeigt.](images/profile2.png)

3.  Die Startzeit ist die Zeit, zu der die APP zum ersten Mal gestartet wird (in diesem Fall SHCORE.dll des UI-Thread-Einstiegs Punkts), bis zu dem Zeitpunkt, zu dem der Kontext zuerst angezeigt wird (gekennzeichnet durch ein schraffurpaket In der Abbildung wird der relevante Bereich hervorgehoben.

    > [!Note]  
    > Die tatsächlich vorhandenen Informationen werden in der Flip-Warteschlange dargestellt. Folglich wird die Zeit bis zum Abschluss des aktuellen Pakets in der Flip-Warteschlange erweitert.

     

    Die gesamte Statusleiste wird in der folgenden Abbildung nicht angezeigt. Außerdem wird die verstrichene Zeit zwischen den hervorgehobenen Teilen angezeigt. Dies ist die Startzeit der app. In diesem Fall wurde für den oben erwähnten Computer ein Wert von ungefähr 240 MS angezeigt.

    ![Screenshot, der relevante Bereiche hinsichtlich der Startzeit in der "Kontext-C-U-Warteschlange" anzeigt.](images/profile3.png)

### <a name="cpu-and-gpu-time-per-frame"></a>CPU-und GPU-Zeit pro Frame

Beim Messen der CPU-Zeit sind einige Punkte zu berücksichtigen. Suchen Sie nach den Bereichen in der Ablauf Verfolgung, in der Sie das zu analysierende Szenario ausgeführt haben. Beispielsweise ist im Geometry-Realisierungs Beispiel eines der analysierten Szenarios der Übergang zwischen den primitiven 2048-und 8192-primitiven, die alle nicht realisiert wurden (wie in, Geometry wird nicht jedes Frame-Objekt). Die Ablauf Verfolgung zeigt den Unterschied in der CPU-und GPU-Aktivität vor und nach dem Übergang in der Anzahl der primitiven eindeutig an.

Zwei Szenarien werden analysiert, um die CPU-und GPU-Zeit pro Frame zu berechnen. Dabei handelt es sich um die folgenden.

-   Übergang von rendering2048 nicht erkannten primitiven zu 8192 nicht erkannten primitiven.
-   Der Übergang von Rendering 8192 erkannte primitive zu nicht erkannten primitiven in 8192.

In beiden Fällen wurde festgestellt, dass die Framerate drastisch abfiel. Beim Messen der CPU-und GPU-Zeit kann die Beziehung zwischen den beiden und einigen anderen Mustern in der Ablauf Verfolgung nützliche Informationen zu problematischen Bereichen in der APP erhalten.

### <a name="calculating-cpu-and-gpu-time-when-2048-primitives-are-being-rendered-unrealized"></a>Berechnen der CPU-und GPU-Zeit, wenn 2048 primitive gerendert werden

1.  Öffnen Sie die Ablauf Verfolgungs Datei mit **GPUView.exe**.
2.  Scrollen Sie nach unten zum GeometryRealization.exe Prozess.
3.  Wählen Sie einen Bereich zum Berechnen der CPU-Zeit aus, und vergrößern Sie ihn mit STRG + Z.

    ![Screenshot, der einen Bereich anzeigt, der zum Berechnen der C P U-Zeit in der "Kontext-CPU-Warteschlange" ausgewählt ist](images/profile4.png)

4.  Zeigen Sie die v-Sync-Informationen an, indem Sie zwischen F8 wechseln. Wenn Sie den Zoom Vorgang so schnell wie möglich sehen, ist es einfach, einen VSYNC-Wert für Daten zu sehen. In den blauen Zeilen werden die v-Synchronisierungs Zeiten angezeigt. Normalerweise erfolgen diese einmal alle 16 ms (60 fps), aber wenn bei DWM ein Leistungsproblem auftritt, wird Sie langsamer ausgeführt, sodass Sie alle 32 MS (30 fps) auftreten. Um einen Eindruck von der Zeit zu erhalten, wählen Sie einen blauen Balken zum nächsten aus, und sehen Sie sich dann die Anzahl der in der unteren rechten Ecke des **gpuview** -Fensters gemeldeten MS an.

    ![Screenshot, der ein Beispiel für die v-Synchronisierungs Zeiten anzeigt](images/profile5.png)

5.  Zum Messen der CPU-Zeit pro Frame Messen Sie die Zeit, die von allen an Rendering beteiligten Threads benötigt wird. Es kann sinnvoll sein, den Thread einzugrenzen, der aus Leistungs Sicht am relevantesten ist. Beispielsweise wird im Beispiel für die Geometry-Realisierung der Inhalt animiert und muss auf dem Bildschirm gerendert werden, sodass jeder Frame den UI-Thread als wichtig darstellt. Nachdem Sie festgelegt haben, welcher Thread gesucht werden soll, Messen Sie die Länge der Balken in diesem Thread. Bei einigen dieser Ergebnisse ergibt sich eine CPU-Zeit pro Frame. Die folgende Abbildung zeigt die Zeit, die im UI-Thread benötigt wird. Es zeigt auch, dass diese Zeit sich zwischen zwei aufeinander folgenden v-syncs gut eignet, was bedeutet, dass Sie 60 fps erreichen.

    ![Screenshot, der die Zeit anzeigt, die für den U I-Thread benötigt wird.](images/profile6.png)

    Sie können auch überprüfen, ob Sie die Flip-Warteschlange für den entsprechenden Zeitrahmen betrachten, der anzeigt, dass die DWM jeden Frame darstellen kann.

    ![Screenshot, der ein Beispiel für die "Flip Queue" anzeigt.](images/profile7.png)

6.  Die GPU-Zeit kann auf die gleiche Weise gemessen werden wie die CPU-Zeit. Vergrößern Sie den relevanten Bereich wie bei der Messung der CPU-Zeit. Messen Sie die Länge der Balken in der GPU-Hardware Warteschlange mit der Farbe der Kontext-CPU-Warteschlange. Solange die Balken in aufeinander folgende v-syncs passen, wird die APP mit 60fps reibungslos ausgeführt.

    ![Screenshot mit einem Beispiel für die GPU-Hardware Warteschlange, in der Informationen angezeigt werden, dass eine APP mit 60 F P S ausgeführt wird.](images/profile8.png)

### <a name="calculating-cpu-and-gpu-time-when-8192-primitives-are-being-rendered-unrealized"></a>Berechnen der CPU-und GPU-Zeit, wenn 8192 primitive gerendert werden

1.  Wenn Sie dieselben Schritte erneut ausführen, zeigt die Ablauf Verfolgung, dass die gesamte CPU-Arbeit für einen Frame nicht zwischen einer v-und der nächsten passt. Dies bedeutet, dass die APP CPU-gebunden ist. Der UI-Thread sätttet die CPU.

    ![Screenshot, der ein Beispiel für den UI-Thread zeigt, der die C P-U enthält.](images/profile9.png)

    Wenn Sie sich die Flip-Warteschlange ansehen, ist auch klar, dass DWM nicht jeden Frame darstellen kann.

    ![Screenshot, der ein Beispiel für das D W M zeigt, das nicht jeden Frame darstellen kann.](images/profile10.png)

2.  Um zu analysieren, wo die Zeit aufgewendet wird, öffnen Sie die Ablauf Verfolgung in **XPerf**. Zum Analysieren der Startzeit in **XPerf** suchen Sie zuerst das Zeitintervall in **gpuview**. Bewegen Sie den Mauszeiger über der linken Seite des Intervalls und der rechten Maustaste, und notieren Sie sich die absolute Zeit, die im unteren Bereich des **gpuview** -Fensters angezeigt wird. Öffnen Sie dann die gleiche ETL-Datei in **XPerf** , Scrollen Sie nach unten zum Diagramm "CPU-Stichproben nach CPU", klicken Sie mit der rechten Maustaste, und wählen Sie "Intervall auswählen..." aus. Dies ermöglicht die Eingabe des relevanten Intervalls, das durch die Betrachtung der GPU-Ablauf Verfolgung ermittelt wurde.

    ![Screenshot, der "C p u Sampling by C p u" in "Windows Performance Analysis" anzeigt.](images/profile11.png)

3.  Wechseln Sie zum Menü "Ablauf Verfolgung", und stellen Sie sicher, dass "Symbole laden" aktiviert ist. Wechseln Sie außerdem zu Trace-> konfigurieren Sie Symbol Pfade, und geben Sie den App-Symbol Pfad ein. Eine Symbol Datei enthält Debuginformationen zu einer kompilierten ausführbaren Datei in einer separaten Datenbank (PDB-Datei). Diese Datei wird im Allgemeinen als PDB bezeichnet. Weitere Informationen zu Symbol Dateien finden Sie hier: [Symbol Dateien](/windows/desktop/Debug/symbol-files). Diese Datei befindet sich im Ordner "Debug" des App-Verzeichnisses.

4.  Klicken Sie mit der rechten Maustaste auf das im vorherigen Schritt ausgewählte Intervall, und klicken Sie auf Zusammenfassungs Tabelle, um die Aufschlüsselung der Zeitspanne für die APP zu erhalten. Um einen Überblick darüber zu erhalten, wie viel Zeit in jeder dll aufgewendet wird, deaktivieren Sie im Menü "Spalten" die Option "Stapel". Beachten Sie, dass in der Spalte "count" die Anzahl der Stichproben innerhalb der angegebenen DLL/Funktion angezeigt wird. Da ungefähr eine Stichprobe pro MS durchgeführt wird, kann diese Zahl als beste Schätzung dafür verwendet werden, wie viel Zeit in jeder DLL/Funktion aufgewendet wird. Wenn Sie das Menü "Stapel" über das Menü "Spalten" aktivieren, erhalten Sie die inklusive Zeit, die für jede Funktion im Aufruf Diagramm aufgewendet wird Dies hilft Ihnen, die Problempunkte weiter zu unterbrechen.

5.  Die Stapel Überwachungsinformationen für nicht erkannte 2048-Elemente zeigen, dass 30% der CPU-Zeit für den Geometry-Erkenntnisprozess aufgewendet werden. Dabei werden ungefähr 36% der Zeit in Geometrie Mosaik und-Spitzen aufgewendet.

6.  Die Stapel Überwachungsinformationen für 8192 nicht erkannte primitive zeigen, dass ungefähr 60% der CPU-Zeit (4 Kerne) für die Geometrie Realisierung aufgewendet werden.

    ![Screenshot, der Stapel Überwachungsinformationen für die C P U-Zeit anzeigt](images/profile12.png)

### <a name="calculating-cpu-time-when-8192-primitives-are-being-rendered-realized"></a>Berechnen der CPU-Zeit, wenn 8192 primitive gerendert werden

In den Profilen, die die APP CPU-gebunden ist, ist es klar. Um die von der CPU aufgewendeten Zeit zu verkürzen, können Geometrien einmalig erstellt und zwischengespeichert werden. Der zwischengespeicherte Inhalt kann jeden Frame gerendert werden, ohne die Geometrie-Mosaik Kosten pro Frame zu verursachen. Wenn Sie die Ablauf Verfolgung in **gpuview** für den erkannten Teil der APP betrachten, ist klar, dass DWM jeden Frame darstellen kann und die CPU-Zeit drastisch reduziert wurde.

![Screenshot, der ein Beispiel für eine Ablauf Verfolgung in gpuview anzeigt, die zeigt, dass D W M jeden Frame darstellen kann.](images/profile13.png)

Der erste Teil des Diagramms zeigt erkannte 8192-primitive. Die entsprechende CPU-Zeit pro Frame kann innerhalb von zwei aufeinander folgenden v-syncs angepasst werden. Im späteren Teil des Diagramms ist dies nicht der Fall.

Bei der Suche in **XPerf** befindet sich die CPU-Auslastung für die längste Zeit im Leerlauf, wobei nur ungefähr 25% der CPU-Zeit für die Geometrie-und Geometrie-App aufgewendet werden.

![gpuview-Bildschirmfoto](images/profile14.png)

## <a name="summary"></a>Zusammenfassung

Sowohl **gpuview** als auch **XPerf** und leistungsstarke Tools zum Analysieren der Leistung von [DirectX](/previous-versions/windows/apps/jj262109(v=win.10)) -apps. Dieser Artikel ist eine Einführung in die Verwendung dieser Tools und das Verständnis grundlegender Leistungsmessungen und App-Merkmale. Abgesehen von der Verwendung von Tools ist es zuerst wichtig, die zu analysierende APP zu verstehen. Beginnen Sie mit dem Auffinden von Antworten auf Fragen wie das, was die APP erreichen soll? Welche Threads im System sind am wichtigsten? Welche Kompromisse sollten Sie treffen? Bei der Analyse von Leistungs Ablauf Verfolgungen sollten Sie zunächst offensichtliche problematische Orte betrachten. Ist die APP-CPU oder GPU gebunden? Kann die APP jeden Frame präsentieren? Tools und ein Verständnis der App können sehr nützliche Informationen zum verstehen, ermitteln und Beheben von Leistungsproblemen zur Verfügung stellen.

 

 