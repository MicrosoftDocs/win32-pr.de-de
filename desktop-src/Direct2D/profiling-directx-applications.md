---
title: Profilerstellung für DirectX-Apps
description: Zeigt, wie Sie einige der wichtigsten Leistungszeitmessungen für eine DirectX-App mithilfe der XPerf- und GPUView-Tools messen, die im Rahmen des Windows Performance Toolkits enthalten sind.
ms.assetid: 4B2F7273-C9B0-4DD3-B559-6220CDE62129
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c923f2917dbb8695bcd624f4d998043e7218cf2f976b19b24ab4cff2bc65f398
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118665430"
---
# <a name="profiling-directx-apps"></a>Profilerstellung für DirectX-Apps

Hier erfahren Sie, wie Sie einige der wichtigsten Leistungszeitmessungen für eine [DirectX-App](/previous-versions/windows/apps/jj262109(v=win.10)) mit den **XPerf-** und **GPUView-Tools** messen, die im Rahmen des Windows Performance Toolkits enthalten sind. Dies ist kein umfassender Leitfaden zum Verständnis der Tools, sondern ihre spezifische Anwendbarkeit für die Analyse der Leistung von DirectX-Apps. Obwohl die meisten der hier beschriebenen Techniken für alle DirectX-Apps relevant sind, ist sie am relevantesten für Apps, die Austauschketten verwenden, und nicht für DirectX-Anwendungen, die auf XAML basieren und SIS/VSIS- und XAML-Animationen verwenden. Wir führen Sie durch die wichtigsten Leistungszeitmessungen, wie Sie die Tools abrufen und installieren, und führen Leistungsmessungsablaufverfolgungen durch und analysieren sie dann, um App-Engpässe zu verstehen.

## <a name="about-the-tools"></a>Informationen zu den Tools

### <a name="xperf"></a>**Xperf**

**XPerf** ist eine Reihe von Leistungsanalysetools, die auf der Ereignisablaufverfolgung für Windows (ETW) aufbauen und für die Messung und Analyse detaillierter System- und App-Leistung und Ressourcennutzung entwickelt wurden. Ab Windows 8 verfügt dieses Befehlszeilentool über eine grafische Benutzeroberfläche und wird als Windows Performance Recorder (WPR) und Windows Leistungsanalyse (WPA) bezeichnet. Weitere Informationen zu diesen Tools finden Sie auf der Webseite für [Windows Performance Toolkit](/previous-versions/windows/it-pro/windows-8.1-and-8/hh162945(v=win.10)) (WPT): Windows Performance [Toolkit](/previous-versions/windows/it-pro/windows-8.1-and-8/hh162945(v=win.10)).

Ein ETW sammelt angeforderte Kernelereignisse und speichert sie in einer Datei, die als Ereignisablaufverfolgungsprotokolldatei (Event Trace Log, ETL) bezeichnet wird. Diese Kernelereignisse bieten umfassende Informationen über eine App und Systemmerkmale beim Ausführen der App. Die Daten werden gesammelt, indem die Ablaufverfolgungserfassung aktiviert wird, das gewünschte App-Szenario ausgeführt wird, das analysiert werden muss, und die Erfassung beendet wird, die die Daten in einer ETL-Datei speichert. Anschließend können Sie die Datei auf demselben oder einem anderen Computer analysieren, indem Sie entweder das Befehlszeilentool **xperf.exe** oder das Analysetool für die visuelle Ablaufverfolgung **xperfview.exe** verwenden.

### <a name="gpuview"></a>GPUView

**GPUView** ist ein Entwicklungstool zum Bestimmen der Leistung der Grafikverarbeitungseinheit (GPU) und der CPU. Er untersucht die Leistung in Bezug auf die Pufferverarbeitung des direkten Speicherzugriffs (Direct Memory Access, DMA) und die gesamte andere Videoverarbeitung auf der Videohardware.

Für [DirectX-Apps,](/previous-versions/windows/apps/jj262109(v=win.10)) die stark von der GPU abhängig sind, ist **GPUView** ein leistungsstarkes Tool zum Verständnis der Beziehung zwischen der Arbeit an der CPU und der GPU. Weitere Informationen zu **GPUView** finden Sie unter [Verwenden von GPUView.](/windows-hardware/drivers/display/using-gpuview)

Ähnlich wie **bei XPerf** wird zunächst eine ETW-Ablaufverfolgung durchgeführt, indem der Ablaufverfolgungsdienst gestartet wird, das Szenario, das für die zu berücksichtigende App analysiert werden muss, beendet und die Informationen in einer ETL-Datei gespeichert werden. **GPUView** stellt die in der ETL-Datei vorhandenen Daten in einem grafischen Format dar.

Nach der Installation des **GPUView-Tools** empfiehlt es sich, das Thema **"Hauptanzeige von GPUView"** im Menü **"GPUView-Hilfe"** zu lesen. Sie enthält nützliche Informationen zum Interpretieren der **GPUView-Benutzeroberfläche.**

## <a name="installing-the-tools"></a>Installieren der Tools

Sowohl **XPerf** als auch **GPUView** sind im Windows Performance Toolkit (WPT) enthalten.

**XPerf** ist im Lieferumfang des Windows Software Development Kit (SDK) für Windows enthalten. [Laden Sie das Windows SDK herunter.](https://dev.windows.com/downloads)

**GPUView** ist im Windows Assessment and Deployment Kit (Windows ADK) verfügbar. [Laden Sie die Windows ADK herunter.](/windows-hardware/get-started/adk-install)

Nach der Installation müssen Sie der Systemvariablen "Path" die Verzeichnisse hinzufügen, die **XPerf** und **GPUView** enthalten.

Klicken Sie auf die Schaltfläche "Start", und geben Sie "Systemvariablen" ein. Das system Eigenschaftenfenster wird geöffnet. Klicken Sie auf "Systemumgebungsvariablen bearbeiten". Wählen Sie im Dialogfeld "Systemeigenschaften" die Option "Umgebungsvariablen" aus. Die Variable "Path" befindet sich unter "Systemvariablen". Fügen Sie das Verzeichnis mit **xperf.exe** und **GPUView.exe** an den Pfad an. Diese ausführbaren Dateien befinden sich im Verzeichnis "Windows Performance Toolkit" in den "Windows Kits". Der Standardspeicherort ist: **C: \\ Programme (x86) \\ Windows Kits \\ 10 \\ Windows Performance Toolkit**.

## <a name="performance-time-measurements"></a>Leistungszeitmessungen

Die meisten Apps erwarten eine reibungslose Ausführung und reagieren auf Benutzereingaben. Je nach gewünschtem Szenario kann jedoch ein Aspekt der Leistung wichtiger sein als ein anderer. Für eine Nachrichtenlese-App, die auf einem Touch-Tablet-PC ausgeführt wird, besteht der wichtigste Aspekt beispielsweise darin, einen einzelnen Artikel gleichzeitig anzuzeigen und denselben oder einen anderen Artikel zu schwenken,zu zoomen/zu scrollen. In diesem Szenario ist es nicht erforderlich, den gesamten Inhalt jedes Frames zu rendern. Die Möglichkeit, bei einer Berührungsgeste reibungslos durch den Artikel zu scrollen, ist jedoch äußerst wichtig.

In einer anderen Instanz ein Spiel oder eine Videorendering-App, die viele Animationsstörungen verwendet, wenn Frames gelöscht werden. In diesem Fall ist die Möglichkeit, Inhalte auf dem Bildschirm ohne Interuption von Benutzereingaben darzustellen, äußerst wichtig.

Um zu verstehen, welcher Teil der App problematisch ist, ist der erste Schritt die Entscheidung über die wichtigsten Szenarien. Sobald die wichtigsten Aspekte der App verstanden wurden und wie sie ausgeführt werden, wird die Suche nach Problemen mit den Tools einfacher.

Einige der gängigsten Leistungszeitmetriken sind:

### <a name="startup-time"></a>Startzeit

Zeit, die vom Prozessstart bis zur ersten Anzeige gemessen wird, die auf dem Bildschirm angezeigt wird. Diese Messung ist nützlicher, wenn das System warm ist, was bedeutet, dass die Messung nach dem mehrmaligen Start der App durchgeführt wird.

### <a name="cpu-time-per-frame"></a>CPU-Zeit pro Frame

Die Zeit, für die die CPU die App-Workload für einen Frame aktiv verarbeitet. Wenn die App reibungslos ausgeführt wird, erfolgt die gesamte Verarbeitung, die für einen Frame erforderlich ist, innerhalb eines V-Synchronisierungsintervalls. Mit der Aktualisierungsrate des Monitors von 60Hz beträgt dies 16 ms pro Frame. Wenn cpu time/frame größer als 16 ms ist, sind möglicherweise CPU-Optimierungen erforderlich, um eine störungsfreie App-Erfahrung zu erzeugen.

### <a name="gpu-time-per-frame"></a>GPU-Zeit pro Frame

Die Zeit, für die GPU die App-Workload für einen Frame aktiv verarbeitet. Eine App ist GPU-gebunden, wenn die zeitaufwändige Verarbeitung eines Framedatenwerts mehr als 16 ms beträgt.

Wenn Sie verstehen können, ob eine App CPU- oder GPU-gebunden ist, wird der problematische Teil des Codes eingeschränkt.

## <a name="taking-performance-time-measurement-trace"></a>Messen der Leistungszeit

Führen Sie die folgenden Schritte aus, um eine Ablaufverfolgung durchzuführen:

1.  Öffnen Sie ein Befehlsfenster als Administrator.
2.  Schließen Sie die App, wenn sie bereits ausgeführt wird.
3.  Wechseln Sie im Ordner Windows Performance Toolkit in das Verzeichnis *gpuview.*
4.  Geben Sie "log.cmd" ein, um die Ereignisablaufverfolgung zu starten. Diese Option protokolliert die interessantesten Ereignisse. Andere verfügbare Optionen protokollieren einen anderen Bereich der Ereignisse. Beispielsweise erfasst "v" oder der ausführliche Protokollmodus alle Ereignisse, die **gpuView** erkennt.
5.  Starten Sie das Beispiel, und nehmen Sie das Beispiel auf eine Weise vor, die den Leistungspfad abdeckt, den Sie analysieren müssen.
6.  Wechseln Sie zurück zu den Befehlsfenstern, und geben Sie erneut "log.cmd" ein, um die Protokollierung zu beenden.
7.  Dadurch wird eine Datei namens "merged.etl" im Ordner *gpuview* ausgegeben. Sie können diese Datei an einem anderen Speicherort speichern und auf demselben oder einem anderen Computer analysieren. Um Stapelerfassungsdetails anzuzeigen, speichern Sie die Symboldatei (PDB), die der App zugeordnet ist.

## <a name="measurements"></a>Messungen


> [!Note]  
> Die Messungen für das Geometrierealisierungsbeispiel werden auf einem Quad Core-Computer mit einer integrierten DirectX11-Grafikkarte durchgeführt. Die Messungen variieren je nach Computerkonfiguration.

 

In diesem Abschnitt wird veranschaulicht, wie Die Startzeit, CPU- und GPU-Zeit pro Frame gemessen werden. Sie können eine Leistungsablaufverfolgung für das gleiche Beispiel auf Ihrem Computer erfassen und die Unterschiede in den verschiedenen Messungen anzeigen.

Um die Ablaufverfolgung in **GPUView** zu analysieren, öffnen Sie die Datei "merged.elt" mit **GPUView.exe**.

### <a name="startup-time"></a>Startzeit

Die Startzeit wird anhand der Gesamtzeit gemessen, die vom App-Start bis zum ersten Erscheinen des Inhalts auf dem Bildschirm aufgewendet wird.

Die Startzeitmessung wird am besten anhand der im vorherigen Abschnitt aufgeführten Schritte mit diesen Variationen durchgeführt:

-   Wenn Sie die Startmessungen beim ersten Start der App verwenden, wird dies als Kaltstart bezeichnet. Dies kann von den Messungen abweichen, die nach dem mehrmaligen Starten der App in kurzer Zeit durchgeführt wurden. Dies wird als warmer Start bezeichnet. Je nachdem, wie viele Ressourcen eine App beim Start erstellt, kann es einen großen Unterschied zwischen den beiden Startzeiten geben. Je nach App-Zielen kann es wünschenswert sein, das eine oder das andere zu messen.
-   Wenn Sie Leistungsinformationen protokollieren, beenden Sie die App, sobald der erste Frame auf dem Bildschirm angezeigt wird.

### <a name="calculating-start-up-time-using-gpuview"></a>Berechnen der Startzeit mit **GPUView**

1.  Scrollen Sie in **GPUView** nach unten zum relevanten Prozess, in diesem Fall GeometryRealization.exe.

    ![Screenshot: Beispiel für Prozesse in GPUView](images/profile1.png)

2.  Die KONTEXT-CPU-Warteschlange stellt die Grafikworkload dar, die in der Hardware in die Warteschlange eingereiht, aber nicht unbedingt von der Hardware verarbeitet wird. Wenn die Ablaufverfolgungsdatei geöffnet wird, werden alle Ereignisse angezeigt, die zwischen der Erstellung der Ablaufverfolgung protokolliert wurden. Um die Startzeit zu berechnen, wählen Sie den gewünschten Bereich aus, zoomen Sie den Anfangsbereich der ersten Kontext-CPU-Warteschlange (dies ist die, die Aktivität anzeigt) mit STRG +Z. Weitere Informationen zu **GPUView-Steuerelementen** finden Sie im ABSCHNITT "Zusammenfassung der **GPUView-Steuerelemente"** in der **GPUView-Hilfedatei.** Die folgende Abbildung zeigt nur den GeometryRealization.exe Prozess, der auf den ersten Teil der Kontext-CPU-Warteschlange vergrößert wurde. Die Farbe der Kontext-CPU-Warteschlange wird durch das Rechteck direkt unterhalb der Warteschlange gekennzeichnet, und die gleichen Farbdatenpakete in der Warteschlange zeigen GPU-Arbeit in der Warteschlange auf der Hardware an. Das Schraffurmusterpaket in der Kontextwarteschlange zeigt das aktuelle Paket an, was bedeutet, dass die App möchte, dass die Hardware den Inhalt auf dem Bildschirm anzeigt.

    ![Screenshot mit Beispielen für die "Kontext-CP-U-Warteschlange".](images/profile2.png)

3.  Die Startzeit ist die Zeit, zu der die App zum ersten Mal gestartet wird (in diesem Fall SHCORE.dll ui thread entry point module), bis der Kontext zum ersten Mal angezeigt wird (gekennzeichnet durch ein Schraffurpaket). In der Abbildung wird der interessante Bereich hervorgehoben.

    > [!Note]  
    > Die tatsächlichen aktuellen Informationen werden in der Flip-Warteschlange dargestellt, und daher wird die Zeitspanne verlängert, bis das aktuelle Paket tatsächlich in der Flip-Warteschlange abgeschlossen ist.

     

    Die vollständige Statusleiste ist in der folgenden Abbildung nicht sichtbar, die auch die verstrichene Zeit zwischen den hervorgehobenen Teilen anzeigt. Dies ist die Startzeit der App. In diesem Fall wurde für den oben erwähnten Computer ein Ungefähres von 240 ms festgestellt.

    ![Screenshot: Interessante Bereiche in Bezug auf die Startzeit in der "Kontext-C P U-Warteschlange"](images/profile3.png)

### <a name="cpu-and-gpu-time-per-frame"></a>CPU- und GPU-Zeit pro Frame

Beim Messen der CPU-Zeit sind einige Punkte zu bedenken. Suchen Sie nach den Bereichen in der Ablaufverfolgung, in denen Sie das zu analysierende Szenario durchgeführt haben. Im Geometry-Realisierungsbeispiel ist eines der analysierten Szenarien beispielsweise der Übergang zwischen den Primitiven des Renderings von 2048 und 8192, alle nicht realisiert (wie in wird die Geometrie nicht in jedem Frame mosaikiert). Die Ablaufverfolgung zeigt eindeutig den Unterschied in der CPU- und GPU-Aktivität vor und nach dem Übergang in der Anzahl von Primitiven.

Es werden zwei Szenarien analysiert, um die CPU- und GPU-Zeit pro Frame zu berechnen. Sie sind wie folgt.

-   Übergang von unrealisierten Primitiven vom Rendering 2048 zu nicht realisierten Primitiven von 8192.
-   Der Übergang vom Rendering 8192 erkannte Primitive zu 8192 unrealisierten Primitiven.

In beiden Fällen wurde festgestellt, dass die Bildfrequenz drastisch absinkt. Das Messen der CPU- und GPU-Zeit, die Beziehung zwischen den beiden sowie einige andere Muster in der Ablaufverfolgung können nützliche Informationen zu problematischen Bereichen in der App liefern.

### <a name="calculating-cpu-and-gpu-time-when-2048-primitives-are-being-rendered-unrealized"></a>Berechnen der CPU- und GPU-Zeit, wenn 2048-Primitive nicht gerendert werden

1.  Öffnen Sie die Ablaufverfolgungsdatei mit **GPUView.exe**.
2.  Scrollen Sie nach unten zum GeometryRealization.exe Prozess.
3.  Wählen Sie einen Bereich zum Berechnen der CPU-Zeit aus, und vergrößern Sie ihn mit STRG+Z.

    ![Screenshot: Ausgewählter Bereich zum Berechnen der C P-U-Zeit in der "Kontext-CPU-Warteschlange"](images/profile4.png)

4.  Zeigen Sie V-Synchronisierungsinformationen an, indem Sie zwischen F8 umschaltungen. Vergrößern Sie die Daten, bis eine vsync-Synchronisierung deutlich zu erkennen ist. Die blauen Linien sind der Ort, an dem die V-Synchronisierung erfolgt. In der Regel treten diese alle 16 ms (60 fps) auf, aber wenn DWM auf ein Leistungsproblem stößt, wird es langsamer ausgeführt, sodass sie alle 32 ms (30 fps) auftreten. Um einen Eindruck von der Zeit zu erhalten, wählen Sie von einem blauen Balken zum nächsten aus, und sehen Sie sich dann die Anzahl der ms an, die in der unteren rechten Ecke des **GPUView-Fensters** gemeldet werden.

    ![Screenshot: Beispiel für V-Synchronisierungszeiten](images/profile5.png)

5.  Um die CPU-Zeit pro Frame zu messen, messen Sie die Zeitspanne, die von allen am Rendering beteiligten Threads benötigt wird. Es kann sinnvoll sein, den Thread einzugrenzen, der aus Leistungssicht am relevantesten ist. Im Geometrierealisierungsbeispiel wird der Inhalt beispielsweise animiert und muss auf dem Bildschirm gerendert werden, sodass jeder Frame den UI-Thread zum wichtigen Thread macht. Nachdem Sie bestimmt haben, welcher Thread untersucht werden soll, messen Sie die Länge der Balken in diesem Thread. Bei einigen dieser Daten ergibt sich eine CPU-Zeit pro Frame. Die folgende Abbildung zeigt die Zeit, die für den UI-Thread in Anspruch genommen wurde. Es zeigt auch, dass diese Zeit gut zwischen zwei aufeinander folgenden V-Synchronisierungen passt, was bedeutet, dass 60FPS erreicht wird.

    ![Screenshot, der die Zeit zeigt, die für den U I-Thread in Anspruch genommen wurde.](images/profile6.png)

    Sie können dies auch überprüfen, indem Sie sich die Flip-Warteschlange für den entsprechenden Zeitrahmen ansehen, der anzeigt, dass DWM jeden Frame darstellen kann.

    ![Screenshot, der ein Beispiel für die "Flip-Warteschlange" zeigt.](images/profile7.png)

6.  Die GPU-Zeit kann auf die gleiche Weise wie die CPU-Zeit gemessen werden. Vergrößern Sie den relevanten Bereich wie beim Messen der CPU-Zeit. Messen Sie die Länge der Balken in der GPU-Hardwarewarteschlange mit der gleichen Farbe wie die Farbe der Kontext-CPU-Warteschlange. Solange die Balken in aufeinander folgende v-Synchronisierungen passen, wird die App bei 60FPS reibungslos ausgeführt.

    ![Screenshot: Beispiel für die GPU-Hardwarewarteschlange mit Informationen, dass eine App mit 60 F P S ausgeführt wird](images/profile8.png)

### <a name="calculating-cpu-and-gpu-time-when-8192-primitives-are-being-rendered-unrealized"></a>Berechnen der CPU- und GPU-Zeit, wenn 8192-Primitive nicht gerendert werden

1.  Wenn Sie die gleichen Schritte erneut ausführen, zeigt die Ablaufverfolgung an, dass die gesamte CPU-Arbeit für einen Frame nicht zwischen einer V-Synchronisierung und dem nächsten passt. Dies bedeutet, dass die App CPU-gebunden ist. Der UI-Thread sättigt die CPU.

    ![Screenshot, der ein Beispiel für den UI-Thread zeigt, der die C P U sättigt.](images/profile9.png)

    Wenn Sie sich die Flip-Warteschlange ansehen, ist auch klar, dass DWM nicht in der Lage ist, jeden Frame darzustellen.

    ![Screenshot, der ein Beispiel zeigt, dass D W M nicht jeden Frame präsentieren kann.](images/profile10.png)

2.  Um zu analysieren, wo die Zeit aufgewendet wird, öffnen Sie die Ablaufverfolgung in **XPerf**. Um die Startzeit in **XPerf** zu analysieren, suchen Sie zunächst das Zeitintervall in **GPUView**. Zeigen Sie auf die linke Seite des Intervalls und rechts, und notieren Sie sich die absolute Zeit, die unten im **GPUView-Fenster** angezeigt wird. Öffnen Sie dann dieselbe ETL-Datei in **XPerf,** scrollen Sie nach unten zum Diagramm "CPU Sampling by CPU", klicken Sie mit der rechten Maustaste, und wählen Sie "Intervall auswählen..." aus. Dies ermöglicht die Eingabe in das Intervall von Interesse, das durch Betrachten der GPU-Ablaufverfolgung ermittelt wurde.

    ![Screenshot: "C P U Sampling by C P U" in "Windows Performance Analysis"](images/profile11.png)

3.  Wechseln Sie zum Menü Ablaufverfolgung, und stellen Sie sicher, dass "Symbole laden" aktiviert ist. Wechseln Sie außerdem zu Ablaufverfolgung > Symbolpfade konfigurieren, und geben Sie den App-Symbolpfad ein. Eine Symboldatei enthält Debuginformationen zu einer kompilierten ausführbaren Datei in einer separaten Datenbank (PDB). Diese Datei wird häufig als PDB bezeichnet. Weitere Informationen zu Symboldateien finden Sie hier: [Symboldateien](/windows/desktop/Debug/symbol-files). Diese Datei befindet sich im Ordner "Debug" des App-Verzeichnisses.

4.  Klicken Sie mit der rechten Maustaste auf das im vorherigen Schritt ausgewählte Intervall, und klicken Sie dann auf Zusammenfassungstabelle, um die Aufschlüsselung des Zeitaufwands für die App zu erhalten. Um einen Überblick darüber zu erhalten, wie viel Zeit in den einzelnen DLLs aufgewendet wird, deaktivieren Sie im Menü "Spalten" die Option "Stapel". Beachten Sie, dass die Spalte "Count" hier zeigt, wie viele Beispiele in der angegebenen DLL/Funktion enthalten sind. Da ungefähr eine Stichprobe pro Ms entnommen wird, kann diese Zahl als beste Schätzung verwendet werden, wie viel Zeit in jeder DLL/Funktion aufgewendet wird. Wenn Sie das Menü "Stapel" im Menü Spalten überprüfen, erhalten Sie die inklusive Zeit, die für jede Funktion im Aufrufdiagramm aufgewendet wird. Dies hilft, die Problempunkte weiter aufzubrechen.

5.  Stapelüberwachungsinformationen für nicht realisierte Primitive im Jahr 2048 zeigen, dass 30 % der CPU-Zeit für den Geometrierealisierungsprozess aufgewendet wird. Davon werden etwa 36 % der Zeit für die Mosaik- und Verzweigungsgeometrie aufgewendet.

6.  Stapelüberwachungsinformationen für 8192 nicht realisierte Primitive zeigen, dass etwa 60 % der CPU-Zeit (4 Kerne) für die Geometrierealisierung aufgewendet werden.

    ![Screenshot: Stapelüberwachungsinformationen für die C P U-Zeit](images/profile12.png)

### <a name="calculating-cpu-time-when-8192-primitives-are-being-rendered-realized"></a>Berechnen der CPU-Zeit, wenn 8192 Primitive gerendert werden

Aus den Profilen geht hervor, dass die App CPU-gebunden ist. Um die CPU-Zeit zu reduzieren, können Geometrien einmal erstellt und zwischengespeichert werden. Der zwischengespeicherte Inhalt kann in jedem Frame gerendert werden, ohne dass die Kosten für das Mosaik der Geometrie pro Frame anfallen. Wenn Sie sich die Ablaufverfolgung in **GPUView** für den realisierten Teil der App ansehen, ist klar, dass DWM jeden Frame darstellen kann und die CPU-Zeit drastisch reduziert wurde.

![Screenshot, der ein Beispiel für eine Ablaufverfolgung in GPUView zeigt, die zeigt, dass D W M jeden Frame darstellen kann.](images/profile13.png)

Der erste Teil des Diagramms zeigt erkannte 8192 Primitive. Die entsprechende CPU-Zeit pro Frame kann innerhalb von zwei aufeinanderfolgenden V-Synchronisierungen passen. Im späteren Teil des Diagramms ist dies nicht der Fall.

In **XPerf** befindet sich die CPU am längsten im Leerlauf, wobei nur etwa 25 % der CPU-Zeit für die Geometrierealisierungs-App aufgewendet werden.

![Screenshot der GPU-Ansicht.](images/profile14.png)

## <a name="summary"></a>Zusammenfassung

SOWOHL **GPUView** als auch **XPerf** und leistungsstarke Tools zum Analysieren der Leistung von [DirectX-Apps.](/previous-versions/windows/apps/jj262109(v=win.10)) Dieser Artikel ist eine Einführung in die Verwendung dieser Tools und zum Verstehen grundlegender Leistungsmessungen und App-Merkmale. Neben dem Verständnis der Verwendung von Tools ist es zunächst wichtig, die zu analysierende App zu verstehen. Beginnen Sie mit der Suche nach Antworten auf Fragen wie das, was die App erreichen möchte? Welche Threads im System sind am wichtigsten? Welche Vor- und Voreinschläge möchten Sie vornehmen? Sehen Sie sich beim Analysieren von Leistungsablaufverfolgungen zunächst offensichtliche problematische Stellen an. Ist die APP-CPU oder GPU gebunden? Kann die App jeden Frame präsentieren? Tools zusammen mit einem Verständnis der App können sehr nützliche Informationen zum Verstehen, Suchen und schließlich Lösen von Leistungsproblemen liefern.

 

 