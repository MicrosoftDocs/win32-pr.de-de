---
description: Wenn Sie über eine funktionsfähige Microsoft Direct3D-Anwendung verfügen und die Leistung verbessern möchten, verwenden Sie im Allgemeinen ein offsetprofilerstellungs-Tool oder eine benutzerdefinierte Messtechnik, um die Zeit zu messen, die für die Ausführung eines oder mehrerer API-Aufrufe (Application Programming Interface) benötigt wird. Wenn Sie dies getan haben, aber Zeit Steuerungs Ergebnisse erhalten, die von einer Rendering-Sequenz zu der nächsten reichen, oder wenn Sie Hypothesen treffen, die nicht die tatsächlichen Experiment Ergebnisse enthalten, können Sie anhand der folgenden Informationen verstehen, warum.
ms.assetid: f969be42-d541-4e8d-aec4-eb9508bcc7cf
title: Exakte Profilerstellung für Direct3D-API-Aufrufe (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdb6d60fcc1b3ace4112dbf7028d91e2c9c8b345
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748737"
---
# <a name="accurately-profiling-direct3d-api-calls-direct3d-9"></a>Exakte Profilerstellung für Direct3D-API-Aufrufe (Direct3D 9)

-   [Die genaue Profilerstellung Direct3D ist schwierig.](#accurately-profiling-direct3d-is-difficult)
-   [Genaue Profilerstellung für eine Direct3D-Rendering-Sequenz](#how-to-accurately-profile-a-direct3d-render-sequence)
-   [Profilerstellung Direct3D Zustandsänderungen](#profiling-direct3d-state-changes)
-   [Zusammenfassung](#summary)
-   [Anhang](#appendix)

Wenn Sie über eine funktionsfähige Microsoft Direct3D-Anwendung verfügen und die Leistung verbessern möchten, verwenden Sie im Allgemeinen ein offsetprofilerstellungs-Tool oder eine benutzerdefinierte Messtechnik, um die Zeit zu messen, die für die Ausführung eines oder mehrerer API-Aufrufe (Application Programming Interface) benötigt wird. Wenn Sie dies getan haben, aber Zeit Steuerungs Ergebnisse erhalten, die von einer Rendering-Sequenz zu der nächsten reichen, oder wenn Sie Hypothesen treffen, die nicht die tatsächlichen Experiment Ergebnisse enthalten, können Sie anhand der folgenden Informationen verstehen, warum.

Die hier bereitgestellten Informationen basieren auf der Annahme, dass Sie über die folgenden Informationen verfügen:

-   C/C++-Programmierung
-   Direct3D-API-Programmierung
-   Messen der API-Zeit
-   Die Grafikkarte und deren Software Treiber
-   Mögliche nicht erklärbare Ergebnisse aus vorheriger Profilerstellung

## <a name="accurately-profiling-direct3d-is-difficult"></a>Die genaue Profilerstellung Direct3D ist schwierig.

Ein Profiler meldet die Zeitspanne, die für die einzelnen API-Aufrufe aufgewendet wurde. Dies wird erreicht, um die Leistung durch Auffinden und Optimieren von Hotspots zu verbessern. Es gibt verschiedene Arten von Profiler und Profil Erstellungs Techniken.

-   Ein Samplingprofiler befindet sich in einem gewissen Zeitraum im Leerlauf und erwachte in bestimmten Intervallen, um die ausgeführten Funktionen zu testen (oder aufzuzeichnen). Er gibt den Prozentsatz der für jeden Aufruf aufgewendeten Zeit zurück. Im Allgemeinen ist ein Samplingprofiler für die Anwendung nicht sehr invasiv und wirkt sich nur minimal auf den Aufwand für die Anwendung aus.
-   Ein instrumentierungsprofiler misst die tatsächliche Zeit, die für das Zurückgeben eines Aufrufes benötigt wird. Hierfür müssen die Trennzeichen für das Starten und beenden in eine Anwendung kompiliert werden. Ein instrumentierungsprofiler ist im Gegensatz zu einem Samplingprofiler in einer Anwendung vergleichsweise invasiver.
-   Es ist auch möglich, eine benutzerdefinierte Profil Erstellungs Methode mit einem Hochleistungs-Timer zu verwenden. Dies erzeugt Ergebnisse ähnlich wie ein instrumentierungsprofiler.

Der Typ der verwendeten Profiler-oder Profil Erstellungs Methode ist nur ein Teil der Herausforderung, genaue Messungen zu generieren.

Mit der Profilerstellung erhalten Sie Antworten, die Ihnen bei der Budget Leistung helfen Angenommen, Sie wissen, dass ein API-Befehl durchschnittlich 1000-Taktzyklen für die Ausführung durchläuft. Sie können einige Schlussfolgerungen über die Leistung bestätigen, wie z. b. Folgendes:

-   Eine CPU mit 2 GHz (die 50 Prozent des Zeit Rendering verbringt) ist auf das Aufrufen dieser API 1 Million Mal pro Sekunde beschränkt.
-   Um 30 Frames pro Sekunde zu erreichen, können Sie diese API nicht mehr als 33.000 Mal pro Frame aufzurufen.
-   Sie können nur 3.3 KB-Objekte pro Frame Rendering (bei 10 dieser API-Aufrufe für die Rendering-Sequenz der einzelnen Objekte).

Anders ausgedrückt: Wenn Sie über ausreichend Zeit pro API-Aufruf verfügen, können Sie eine Budgetfrage wie die Anzahl der primitiven, die interaktiv gerendert werden können, beantworten. Die von einem Instrumentierungs Profiler zurückgegebenen Rohdaten beantworten die Fragen zur Budgetierung jedoch nicht genau. Dies liegt daran, dass die Grafik Pipeline komplexe Entwurfs Probleme aufweist, wie z. b. die Anzahl der Komponenten, die funktionieren müssen, die Anzahl der Prozessoren, die Steuern, wie der Arbeitsablauf zwischen den Komponenten verläuft, sowie Optimierungsstrategien, die in der Laufzeit und in einem Treiber implementiert werden, der entwickelt wurde, um die Pipeline effizienter zu gestalten.

### <a name="each-api-call-goes-through-several-components"></a>Jeder API-Befehl durchläuft mehrere Komponenten.

Jeder-Rückruf wird von der Anwendung bis zur Grafikkarte von mehreren Komponenten verarbeitet. Sehen Sie sich zum Beispiel die folgende rendersequenz an, die zwei Aufrufe zum Zeichnen eines einzelnen Dreiecks enthält:


```
SetTexture(...);
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);
```



Das folgende konzeptionelle Diagramm zeigt die verschiedenen Komponenten, über die die Aufrufe bestanden werden müssen.

![Diagramm der Grafik Komponenten, die API-Aufrufe durchlaufen](images/microbenchmarkinstructionflow2.png)

Die Anwendung ruft Direct3D auf, um die Szene zu steuern, Benutzerinteraktionen zu verarbeiten und zu bestimmen, wie das Rendering erfolgt. All diese Aufgaben werden in der Rendering-Sequenz angegeben, die mithilfe von Direct3D-API-Aufrufen an die Laufzeit gesendet wird. Die Rendering-Sequenz ist praktisch Hardware unabhängig (d. h., die API-Aufrufe sind Hardware unabhängig, aber eine Anwendung hat wissen, welche Funktionen von einer Grafikkarte unterstützt werden).

Die Laufzeit konvertiert diese Aufrufe in ein Geräte unabhängiges Format. Die Laufzeit übernimmt die gesamte Kommunikation zwischen der Anwendung und dem Treiber, sodass eine Anwendung auf mehr als einem kompatiblen Hardware Server ausgeführt werden kann (abhängig von den erforderlichen Features). Beim Messen eines Funktions Aufrufes misst ein Instrumentierungs Profil die Zeit, die in einer Funktion aufgewendet wurde, sowie die Zeit, die die Funktion zurückgibt. Eine Einschränkung für einen instrumentierungsprofiler besteht darin, dass es möglicherweise nicht die Zeit beinhaltet, mit der ein Treiber die resultierende Arbeit an die Grafikkarte sendet, und nicht die Uhrzeit, zu der die Grafikkarte die Arbeit verarbeitet. Anders ausgedrückt: ein offlinerinstrumentierungsprofiler kann nicht alle Arbeit, die den einzelnen Funktions aufruten zugeordnet ist, zuordnen.

Der Software Treiber verwendet Hardware spezifische Informationen über die Grafikkarte, um die geräteunabhängigen Befehle in eine Sequenz von Grafikkarten Befehlen zu konvertieren. Treiber können auch die Abfolge der Befehle optimieren, die an die Grafikkarte gesendet werden, damit das Rendering auf der Grafikkarte effizient erfolgt. Diese Optimierungen können Profil Erstellungs Probleme verursachen, da die Menge der abgeschlossenen Arbeit nicht so aussieht, wie Sie aussieht (Sie müssen möglicherweise die Optimierungen verstehen, um Sie zu berücksichtigen). Der Treiber gibt in der Regel die Steuerung an die Laufzeit zurück, bevor die Grafikkarte die Verarbeitung aller Befehle abgeschlossen hat.

Die Grafikkarte führt den Großteil des Renderings durch Kombinieren von Daten aus dem Scheitelpunkt und Index Puffer, Texturen, renderstatusinformationen und den Grafik Befehlen aus. Wenn die Grafikkarte das Rendering abschließt, ist die aus der rendersequenz erstellte Arbeit abgeschlossen.

Jeder Direct3D-API-Rückruf muss von jeder Komponente (der Laufzeit, dem Treiber und der Grafikkarte) verarbeitet werden, um alles zu Rendering.

### <a name="there-is-more-than-one-processor-controlling-the-components"></a>Es sind mehrere Prozessoren vorhanden, die die Komponenten steuern.

Die Beziehung zwischen diesen Komponenten ist noch komplexer, da die Anwendung, die Laufzeit und der Treiber von einem Prozessor gesteuert werden und die Grafikkarte von einem separaten Prozessor gesteuert wird. Das folgende Diagramm zeigt zwei Arten von Prozessoren: eine zentrale Verarbeitungseinheit (CPU) und eine GPU (Graphics Processing Unit).

![Diagramm für eine CPU und eine GPU und deren Komponenten](images/microbenchmarkprocessors.png)

PC-Systeme verfügen über mindestens eine CPU und eine GPU, Sie können jedoch mehr als eine von beiden oder beides aufweisen. Die CPUs befinden sich auf der Hauptplatine, und die GPUs befinden sich entweder auf dem Motherboard oder auf der Grafikkarte. Die Geschwindigkeit der CPU wird durch einen Takt Chip auf der Hauptplatine festgelegt, und die Geschwindigkeit der GPU wird durch einen separaten Takt Chip bestimmt. Die CPU-Uhr steuert die Geschwindigkeit der von der Anwendung, der Laufzeit und des Treibers ausgeführten Arbeit. Die Anwendung sendet Arbeit an die GPU über die Laufzeit und den Treiber.

Die CPU und die GPU werden in der Regel unabhängig voneinander mit unterschiedlichen Geschwindigkeiten ausgeführt. Die GPU reagiert möglicherweise auf die Arbeit, sobald die Arbeit verfügbar ist (vorausgesetzt, die GPU hat die Verarbeitung vorheriger Aufgaben abgeschlossen). Die GPU-Arbeit erfolgt parallel zur CPU-Arbeit, wie von der gekrümmten Linie in der obigen Abbildung hervorgehoben. Ein Profiler misst in der Regel die Leistung der CPU, nicht die GPU. Dadurch ist die Profilerstellung schwierig, da die von einem instrumentierungsprofiler erstellten Messungen die CPU-Zeit einschließen, aber nicht die GPU-Zeit einschließen.

Der Zweck der GPU besteht darin, die Verarbeitung von der CPU auf einen Prozessor zu deaktivieren, der speziell für Grafik Arbeiten konzipiert ist. Auf modernen Videokarten ersetzt die GPU einen Großteil der Transformations-und Beleuchtungsaufgaben in der Pipeline von der CPU zur GPU. Dadurch wird die CPU-Arbeitsauslastung erheblich reduziert, sodass mehr CPU-Zyklen für die andere Verarbeitung verfügbar sind. Wenn Sie eine grafische Anwendung für die Spitzenleistung optimieren möchten, müssen Sie die Leistung der CPU und der GPU Messen und die Arbeit zwischen den beiden Arten von Prozessoren ausgleichen.

In diesem Dokument werden keine Themen behandelt, die sich auf das Messen der Leistung der GPU oder den Ausgleich der Arbeitsauslastung zwischen der CPU und der GPU beziehen. Wenn Sie die Leistung einer GPU (oder einer bestimmten Grafikkarte) besser verstehen möchten, besuchen Sie die Website des Anbieters, um nach weiteren Informationen zur GPU-Leistung zu suchen. Stattdessen konzentriert sich dieses Dokument auf die Arbeit, die von der Laufzeit und dem Treiber erledigt wird, indem die GPU-Arbeit auf einen vernachlässigbaren Betrag reduziert wird. Dies ist teilweise auf der Grundlage der Erfahrung, dass Anwendungen, die Leistungsprobleme aufweisen, in der Regel CPU-beschränkt sind.

### <a name="runtime-and-driver-optimizations-can-mask-api-measurements"></a>Lauf Zeit-und Treiber Optimierungen können API-Messungen maskieren

Die Laufzeitumgebung verfügt über eine integrierte Leistungsoptimierung, mit der die Messung eines einzelnen Aufrufes überlastet werden kann. Im folgenden finden Sie ein Beispielszenario, in dem dieses Problem veranschaulicht wird. Sehen Sie sich die folgende Rendering-Sequenz an:


```
  BeginScene();
    ...
    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);
    ...
  EndScene();
  Present();
```



Beispiel 1: einfache Rendering-Sequenz

Wenn Sie sich die Ergebnisse der beiden Aufrufe in der Rendering-Sequenz ansehen, könnte ein instrumentierungsprofiler ähnliche Ergebnisse wie die folgenden zurückgeben:


```
Number of cycles for SetTexture       : 100
Number of cycles for DrawPrimitive    : 950,500
```



Der Profiler gibt die Anzahl der CPU-Zyklen zurück, die erforderlich sind, um die mit jedem-Rückruf verknüpften Aufgaben zu verarbeiten (Beachten Sie, dass die GPU nicht in diese Zahlen eingeschlossen ist, weil die GPU noch nicht mit diesen Befehlen begonnen hat) Da [**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) fast eine Million Zyklen für die Verarbeitung erforderte, konnten Sie feststellen, dass es nicht sehr effizient ist. Sie werden jedoch bald feststellen, warum diese Schlussfolgerung falsch ist, und wie Sie Ergebnisse generieren können, die für die Budgetplanung verwendet werden können.

### <a name="measuring-state-changes-requires-careful-render-sequences"></a>Das Messen von Zustandsänderungen erfordert sorgfältige Rendering-Sequenzen.

Alle Aufrufe außer [**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), [**drawindexedprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)oder [**Clear**](/windows/desktop/api) (z. b. [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), [**setvertexdeclaration**](/windows/desktop/api)und [**setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) bewirken eine Zustandsänderung. Jede Zustandsänderung legt den Pipeline Status fest, der steuert, wie das Rendering durchgeführt wird.

Optimierungen in der Laufzeit und/oder dem Treiber sind so konzipiert, dass das Rendering beschleunigt wird, indem der erforderliche Arbeitsaufwand reduziert wird. Im folgenden finden Sie eine Reihe von Optimierungen für die Statusänderung, die Profil-Mittelwerte verschmutzen können:

-   Ein Treiber (oder die Laufzeit) kann eine Zustandsänderung als lokalen Status speichern. Da der Treiber in einem "Lazy"-Algorithmus arbeiten könnte (die Arbeit wird so lange verschoben, bis er unbedingt erforderlich ist), kann die Arbeit mit einigen Zustandsänderungen verzögert werden.
-   Die Laufzeit (oder ein Treiber) kann Zustandsänderungen durch Optimieren von entfernen. Ein Beispiel hierfür ist das Entfernen einer redundanten Zustandsänderung, die die Beleuchtung deaktiviert, da die Beleuchtung zuvor deaktiviert wurde.

Es gibt keine Möglichkeit, eine rendersequenz zu überprüfen und zu bestimmen, welche Zustandsänderungen ein geändertes Bit festlegen und die Arbeit verzögern oder einfach durch Optimierung entfernt werden. Auch wenn Sie optimierte Zustandsänderungen in der Laufzeit oder im Treiber von heute ermitteln könnten, wird die Laufzeit oder der Treiber von morgen wahrscheinlich aktualisiert. Sie wissen auch nicht, was der vorherige Status war, daher ist es schwierig, redundante Zustandsänderungen zu identifizieren. Die einzige Möglichkeit, die Kosten einer Zustandsänderung zu überprüfen, ist das Messen der Rendering-Sequenz, die die Statusänderungen einschließt.

Wie Sie sehen können, ist die Erstellung der Profilerstellung schwerwiegend, wenn Sie über mehrere Prozessoren, Befehle verfügen, die von mehr als einer Komponente verarbeitet werden, und Optimierungen, die in die Komponenten integriert wurden. Im nächsten Abschnitt wird jede dieser Herausforderungen bei der Profilerstellung behandelt. Sample Direct3D-Rendering-Sequenzen werden mit den dazugehörigen Messtechniken angezeigt. Mit diesem Wissen können Sie exakte, wiederholbare Messergebnisse für einzelne Aufrufe generieren.

## <a name="how-to-accurately-profile-a-direct3d-render-sequence"></a>Genaue Profilerstellung für eine Direct3D-Rendering-Sequenz

Nachdem nun einige der Herausforderungen bei der Profilerstellung hervorgehoben wurden, werden in diesem Abschnitt Techniken vorgestellt, mit denen Sie Profilmessungen generieren können, die für die Budgetplanung verwendet werden können. Genaue, wiederholbare Profil Erstellungs Messungen sind möglich, wenn Sie die Beziehung zwischen den von der CPU kontrollierten Komponenten verstehen und die von der Laufzeit und dem Treiber implementierten Leistungsoptimierungen vermeiden.

Zunächst müssen Sie in der Lage sein, die Ausführungszeit eines einzelnen API-Aufrufes genau zu messen.

### <a name="pick-an-accurate-measurement-tool-like-queryperformancecounter"></a>Wählen Sie ein genaues Mess Tool wie QueryPerformanceCounter aus.

Das Microsoft Windows-Betriebssystem enthält einen Zeit Geber mit hoher Auflösung, der zum Messen der verstrichenen Zeiten mit hoher Auflösung verwendet werden kann. Der aktuelle Wert eines solchen Timers kann mithilfe von " [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)" zurückgegeben werden. Nachdem Sie **QueryPerformanceCounter** aufgerufen haben, um Start-und Endwerte zurückzugeben, kann der Unterschied zwischen den beiden Werten mithilfe von **QueryPerformanceCounter** in die tatsächlich verstrichene Zeit (in Sekunden) konvertiert werden.

Die Verwendung von [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) hat den Vorteil, dass es in Windows verfügbar ist und problemlos verwendet werden kann. Umschließen Sie die Aufrufe einfach mit einem **QueryPerformanceCounter** -Aufruf, und speichern Sie die Werte für Start und Ende. Daher wird in diesem Artikel veranschaulicht, wie Sie **QueryPerformanceCounter** verwenden, um die Ausführungszeiten zu Profilen, ähnlich der Art, wie Sie von einem instrumentierungsprofiler gemessen wird. Es folgt ein Beispiel, das zeigt, wie Sie **QueryPerformanceCounter** in Ihren Quellcode einbetten:


```
  BeginScene();
    ...
    // Start profiling
    LARGE_INTEGER start, stop, freq;
    QueryPerformanceCounter(&start);

    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1); 

    QueryPerformanceCounter(&stop);
    stop.QuadPart -= start.QuadPart;
    QueryPerformanceFrequency(&freq);
    // Stop profiling
    ...
  EndScene();
  Present();
```



Beispiel 2: Implementierung benutzerdefinierter Profilerstellung mit QPC

Start und anhalten sind zwei große ganze Zahlen, die die vom Hochleistungs-Timer zurückgegebenen Werte für Start und Ende enthalten. Beachten Sie, dass QueryPerformanceCounter (&Start) unmittelbar vor dem Aufruf von [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) und QueryPerformanceCounter (&Ende) direkt nach [**drawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)aufgerufen wird. Nach dem Abrufen des Endwerts wird QueryPerformanceFrequency aufgerufen, um freq zurückzugeben. Dies ist die Häufigkeit des hochauflösenden Timers. Angenommen, Sie erhalten in diesem hypothetischen Beispiel die folgenden Ergebnisse für "Start", "Start" und "FREQ":



| Lokale Variable | Anzahl der Ticks |
|----------------|-----------------|
| start          | 1792998845094   |
| stop           | 1792998845102   |
| Freq           | 3579545         |



 

Sie können diese Werte in die Anzahl der Zyklen konvertieren, die zum Ausführen der API-Aufrufe wie folgt benötigt werden:


```
# ticks = (stop - start) = 1792998845102 - 1792998845094 = 8 ticks

# cycles = CPU speed * number of ticks / QPF
# 4568   = 2 GHz      * 8              / 3,579,545
```



Das heißt, es werden ungefähr 4568 Taktzyklen benötigt, um [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) und [**drawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) auf diesem Computer mit 2 GHz zu verarbeiten. Sie könnten diese Werte in die tatsächliche Zeit konvertieren, die zum Ausführen aller Aufrufe wie folgt benötigt wird:


```
(stop - start)/ freq = elapsed time
8 ticks / 3,579,545 = 2.2E-6 seconds or between 2 and 3 microseconds.
```



Die Verwendung von QueryPerformanceCounter erfordert, dass Sie Ihrer Rendering-Sequenz Start-und Endmessungen hinzufügen und QueryPerformanceFrequency verwenden, um die Differenz (Anzahl der Ticks) in die Anzahl der CPU-Zyklen oder die tatsächliche Zeit zu konvertieren. Das Identifizieren der Messtechnik ist ein guter Einstieg in die Entwicklung einer benutzerdefinierten Profil Erstellungs Implementierung. Bevor Sie jedoch mit der Erstellung von Messungen beginnen, müssen Sie wissen, wie Sie mit der Grafikkarte umzugehen sind.

### <a name="focus-on-cpu-measurements"></a>Fokus auf CPU-Messungen

Wie bereits erwähnt, funktionieren die CPU und die GPU parallel, um die von den API-aufrufen generierten Aufgaben zu verarbeiten. Eine reale Anwendung erfordert die Profilerstellung für beide Arten von Prozessoren, um herauszufinden, ob Ihre Anwendung CPU-eingeschränkt oder GPU-begrenzt ist. Da die GPU-Leistung Hersteller spezifisch ist, wäre es sehr schwierig, Ergebnisse in diesem Whitepaper zu liefern, die die verschiedenen verfügbaren Grafikkarten abdecken.

Stattdessen konzentriert sich dieses Whitepaper auf die Profilerstellung für die von der CPU ausgeführten Arbeit, indem eine benutzerdefinierte Technik zum Messen der Laufzeit und der Treiber Arbeit verwendet wird. Die GPU-Arbeit wird auf eine unbedeutende Menge reduziert, sodass die CPU-Ergebnisse besser sichtbar sind. Ein Vorteil dieses Ansatzes besteht darin, dass diese Technik Ergebnisse in dem Anhang liefert, dass Sie in der Lage sein sollten, mit Ihren Messungen zu korrelieren. Um die für die Grafikkarte erforderliche Arbeit auf eine unbedeutende Ebene zu reduzieren, verringern Sie einfach die renderingarbeit auf die geringstmögliche Menge. Dies kann erreicht werden, indem zeichnen-Aufrufe zum Rendern eines einzelnen Dreiecks eingeschränkt werden, und Sie können weiter eingeschränkt werden, sodass jedes Dreieck nur ein Pixel enthält.

Die Maßeinheit, die in diesem Artikel zum Messen der CPU-Arbeit verwendet wird, ist die Anzahl der CPU-Taktzyklen anstelle der tatsächlichen Zeit. CPU-Taktzyklen haben den Vorteil, dass Sie besser portierbar sind (für CPU-eingeschränkte Anwendungen) als die tatsächlich verstrichene Zeit auf Computern mit unterschiedlichen CPU-Geschwindigkeiten. Dies kann bei Bedarf problemlos in die tatsächliche Zeit konvertiert werden.

Dieses Dokument behandelt keine Themen im Zusammenhang mit dem Lastenausgleich der Arbeitsauslastung zwischen der CPU und der GPU. Beachten Sie, dass das Ziel dieses Dokuments darin besteht, die Gesamtleistung einer Anwendung nicht zu messen, sondern zu veranschaulichen, wie Sie die Zeit, die die Laufzeit und der Treiber zum Verarbeiten von API-aufrufen benötigt, exakt messen können. Mit diesen präzisen Messungen können Sie die Aufgabe der Budgetierung der CPU übernehmen, um bestimmte Leistungs Szenarios zu verstehen.

### <a name="controlling-runtime-and-driver-optimizations"></a>Steuern von Lauf Zeit-und Treiber Optimierungen

Wenn eine Maßeinheit identifiziert ist und eine Strategie zur Reduzierung der GPU-Arbeit vorliegt, besteht der nächste Schritt darin, die Lauf Zeit-und Treiber Optimierungen zu verstehen, die bei der Profilerstellung durchlaufen werden.

Die CPU-Arbeit kann in drei Bucket unterteilt werden: die Anwendung funktioniert, die Laufzeit funktioniert, und der Treiber funktioniert. Ignorieren Sie die Anwendungs Arbeit, da dies der Programmierer-Kontrolle unterliegt. Aus Sicht der Anwendung sind die Laufzeit und der Treiber wie schwarze Felder, da die Anwendung nicht steuern kann, was in Ihnen implementiert ist. Der Schlüssel ist das Verständnis der Optimierungstechniken, die in der Laufzeit und im Treiber implementiert werden können. Wenn Sie diese Optimierungen nicht verstehen, ist es sehr einfach, zur falschen Schlussfolgerung hinsichtlich der Arbeitsauslastung der CPU basierend auf den Profilmessungen zu springen. Vor allem gibt es zwei Themen, die sich auf einen als Befehls Puffer bezeichneten Artikel beziehen, und auf welche Weise die Profilerstellung verschleiert werden kann. Diese Themen sind:

-   Lauf Zeitoptimierung mit dem Befehls Puffer. Der Befehls Puffer ist eine Lauf Zeitoptimierung, die die Auswirkung eines Modus-Übergangs verringert. Informationen zum Steuern der zeitliche Steuerung des Modus-Übergangs finden Sie unter [Steuern des Befehls Puffers](#controlling-the-command-buffer).
-   Neinieren der zeitlichen Auswirkungen des Befehls Puffers. Die verstrichene Zeit eines modusübergangs kann eine große Auswirkung auf die Profil Erstellungs Messungen haben. Die Strategie hierfür besteht darin, [die rendersequenz im Vergleich zum modusübergang groß zu gestalten](#make-the-render-sequence-large-compared-to-the-mode-transition).

### <a name="controlling-the-command-buffer"></a>Steuern des Befehls Puffers

Wenn eine Anwendung einen API-Befehl ausführt, konvertiert die Laufzeit den API-Aufrufe in ein Geräte unabhängiges Format (das einen Befehl aufruft) und speichert es im Befehls Puffer. Der Befehls Puffer wird dem folgenden Diagramm hinzugefügt.

![Diagramm der CPU-Komponenten, einschließlich eines Befehls Puffers](images/microbenchmarkcommandbuffer2.png)

Jedes Mal, wenn die Anwendung einen weiteren API-Aufruf durchführt, wiederholt die Laufzeit diese Sequenz und fügt dem Befehls Puffer einen weiteren Befehl hinzu. Zu einem bestimmten Zeitpunkt leert die Laufzeit den Puffer (sendet die Befehle an den Treiber). In Windows XP führt das Leeren des Befehls Puffers zu einem modusübergang, weil das Betriebssystem von der Laufzeit (im Benutzermodus ausgeführt) zum Treiber wechselt (wird im Kernel Modus ausgeführt), wie im folgenden Diagramm dargestellt.

-   Benutzermodus: der nicht privilegierte Prozessor Modus, der Anwendungscode ausführt. Benutzermodusanwendungen können mit Ausnahme von System Diensten keinen Zugriff auf Systemdaten erlangen.
-   Kernel Modus: der privilegierte Prozessor Modus, in dem Windows-basierter Executive-Code ausgeführt wird. Ein Treiber oder Thread, der im Kernel Modus ausgeführt wird, hat Zugriff auf den gesamten System Arbeitsspeicher, den direkten Zugriff auf die Hardware und die CPU-Anweisungen, um e/a-Vorgänge mit der Hardware auszuführen.

![Diagramm der Übergänge zwischen Benutzermodus und Kernel Modus](images/microbenchmarkcommandbuffer3.png)

Der Übergang erfolgt immer dann, wenn die CPU vom Benutzer in den Kernel Modus wechselt (und umgekehrt) und die Anzahl der benötigten Zyklen im Vergleich zu einem einzelnen API-Aufruf groß ist. Wenn die Laufzeit jeden API-Aufruf an den Treiber gesendet hat, als er aufgerufen wurde, würde jeder API-Aufruf die Kosten für einen modusübergang verursachen.

Stattdessen ist der Befehls Puffer eine Lauf Zeitoptimierung, die so konzipiert ist, dass die effektiven Kosten des Modus-Übergangs gesenkt werden. Der Befehls Puffer fügt viele Treiber Befehle in die Warteschlange ein, um einen Übergang im Einzelmodus vorzubereiten. Wenn die Laufzeit dem Befehls Puffer einen Befehl hinzufügt, wird die Steuerung an die Anwendung zurückgegeben. Ein Profiler kann nicht wissen, dass die Treiber Befehle wahrscheinlich noch nicht an den Treiber gesendet wurden. Demzufolge sind die von einem Off-The-Shelf instrumentierungsprofiler zurückgegebenen Zahlen irreführend, da Sie die Lauf Zeit Arbeit messen, aber nicht die zugeordnete Treiber Arbeit.

### <a name="profile-results-without-a-mode-transition"></a>Profil Ergebnisse ohne modusübergang

Mithilfe der rendersequenz aus Beispiel 2 sind hier einige typische Zeit Steuerungs Messungen angegeben, die die Größe eines Modus-Übergangs veranschaulichen. Wenn [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) -und [**drawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) -Aufrufe keinen modusübergang verursachen, könnte ein Offsets-instrumentierungsprofiler ähnliche Ergebnisse wie die folgenden zurückgeben:


```
Number of cycles for SetTexture           : 100
Number of cycles for DrawPrimitive        : 900
```



Jede dieser Zahlen ist die Zeitspanne, die es dauert, bis die Common Language Runtime diese Aufrufe zum Befehls Puffer hinzufügt. Da es keinen modusübergang gibt, hat der Treiber noch keine Arbeit erledigt. Die Profiler-Ergebnisse sind genau, aber Sie messen nicht alle Aufgaben, die von der Rendering-Sequenz letztendlich ausgeführt werden.

### <a name="profile-results-with-a-mode-transition"></a>Profil Ergebnisse mit einem modusübergang

Sehen Sie sich nun an, was für das gleiche Beispiel geschieht, wenn ein modusübergang stattfindet. Nehmen Sie diesmal an, dass [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) und [**drawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) einen Modus-Übergang verursachen. Ein Offsets-instrumentierungsprofiler könnte wiederum ähnliche Ergebnisse wie die folgenden zurückgeben:


```
Number of cycles for SetTexture           : 98 
Number of cycles for DrawPrimitive        : 946,900
```



Die Zeit, die für [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) gemessen wird, ist ungefähr identisch, aber der drastische Anstieg der in [**drawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) verbrachten Zeit ist auf den modusübergang zurückzuführen. Folgendes geschieht:

1.  Nehmen Sie an, dass der Befehls Puffer Platz für einen Befehl hat, bevor die Rendering-Sequenz gestartet wird.
2.  [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) wird in ein Geräte unabhängiges Format konvertiert und dem Befehls Puffer hinzugefügt. In diesem Szenario füllt dieser Befehl den Befehls Puffer aus.
3.  Die Laufzeit versucht, [**drawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) dem Befehls Puffer hinzuzufügen, kann jedoch nicht, da Sie voll ist. Stattdessen leert die Laufzeit den Befehls Puffer. Dies bewirkt den Kernel Modus-Übergang. Nehmen Sie an, dass der Übergang ungefähr 5000 Zyklen erfordert. Diese Zeit trägt zum Zeitaufwand für **drawprimitiv** bei.
4.  Der Treiber verarbeitet dann die Arbeit, die mit allen Befehlen verknüpft ist, die aus dem Befehls Puffer geleert wurden. Angenommen, die Treiber Zeit zum Verarbeiten der Befehle, die den Befehls Puffer fast ausgefüllt haben, beträgt ungefähr 935.000 Zyklen. Angenommen, die mit [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) verknüpften Treiber arbeiten sind ungefähr 2750 Zyklen. Diese Zeit trägt zum Zeitaufwand für [**drawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)bei.
5.  Nachdem der Treiber seine Arbeit beendet hat, gibt der Benutzermodus-Übergang die Steuerung an die Laufzeit zurück. Der Befehls Puffer ist jetzt leer. Nehmen Sie an, dass der Übergang ungefähr 5000 Zyklen erfordert.
6.  Die Rendering-Sequenz wird beendet, indem [**drawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) umgerechnet und dem Befehls Puffer hinzugefügt wird. Angenommen, dies dauert ungefähr 900 Zyklen. Diese Zeit trägt zum Zeitaufwand für **drawprimitiv** bei.

Wenn Sie die Ergebnisse zusammenfassen, sehen Sie Folgendes:


```
DrawPrimitive = kernel-transition + driver work    + user-transition + runtime work
DrawPrimitive = 5000              + 935,000 + 2750 + 5000            + 900
DrawPrimitive = 947,950  
```



Genau wie bei der Messung für [**drawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) ohne den modusübergang (900 Zyklen) ist die Messung für **drawprimitive** mit dem modusübergang (947.950 Zyklen) präzise, aber nutzlos in Bezug auf die Arbeitsauslastung der CPU. Das Ergebnis enthält die richtige Lauf Zeitfunktion, der Treiber funktioniert für [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), der Treiber für alle Befehle, die mit " **SetTexture**" vorangestellt sind, und die zwei-Modus-Übergänge. In der Messung fehlen jedoch die Arbeit des **drawprimitive** -Treibers.

Ein modusübergang kann als Reaktion auf einen beliebigen-Rückruf auftreten. Dies hängt davon ab, was zuvor im Befehls Puffer war. Sie müssen den Modus-Übergang steuern, um zu verstehen, wie viel CPU-Arbeit (Laufzeit und Treiber) den einzelnen anrufen zugeordnet ist. Zu diesem Zweck benötigen Sie einen Mechanismus zum Steuern des Befehls Puffers und die zeitliche Steuerung des Modus-Übergangs.

### <a name="the-query-mechanism"></a>Der Abfrage Mechanismus

Der Abfrage Mechanismus in Microsoft Direct3D 9 wurde so konzipiert, dass die Common Language Runtime die GPU zum Fortschritt Abfragen und bestimmte Daten von der GPU zurückgeben kann. Wenn bei der Profilerstellung die GPU-Arbeit minimiert wird, sodass Sie eine erhebliche Auswirkung auf die Leistung hat, können Sie den Status von der GPU zurückgeben, um die Treiber Arbeit zu messen. Schließlich ist der Treiber Vorgang vollständig, wenn die GPU die Treiber Befehle gesehen hat. Außerdem kann der Abfrage Mechanismus mit der Steuerung von zwei Befehls Puffer Merkmalen verknüpft werden, die für die Profilerstellung wichtig sind: Wenn der Befehls Puffer leer ist und wie viel Arbeit im Puffer liegt.

Hier ist die gleiche Rendering-Sequenz mit dem Abfrage Mechanismus:


```
// 1. Create an event query from the current device
IDirect3DQuery9* pEvent;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEvent);

// 2. Add an end marker to the command buffer queue.
pEvent->Issue(D3DISSUE_END);

// 3. Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

// 4. Start profiling
LARGE_INTEGER start, stop;
QueryPerformanceCounter(&start);

// 5. Invoke the API calls to be profiled.
SetTexture(...);
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);

// 6. Add an end marker to the command buffer queue.
pEvent->Issue(D3DISSUE_END);

// 7. Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
    
// 8. End profiling
QueryPerformanceCounter(&stop);
```



Beispiel 3: Verwenden einer Abfrage zum Steuern des Befehls Puffers

Im folgenden finden Sie eine ausführlichere Erläuterung der einzelnen Codezeilen:

1.  Erstellen Sie eine Ereignis Abfrage, indem Sie ein Abfrageobjekt mit D3DQUERYTYPE- \_ Ereignis erstellen.
2.  Fügen Sie dem Befehls Puffer einen Abfrage Ereignis Marker hinzu, indem Sie [**Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)([**D3DISSUE \_ End**](d3dissue-end.md)) aufrufen. Dieser Marker weist den Treiber an, zu verfolgen, wann die GPU die Ausführung von Befehlen beendet, die dem Marker vorangestellt sind
3.  Der erste Aufruf leert den Befehls Puffer, da der Aufruf von [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) mit [**D3DGETDATA \_ Flush**](d3dgetdata-flush.md) das Leeren des Befehls Puffers erzwingt. Jeder nachfolgende-Rückruf überprüft die GPU, um zu sehen, wann die Verarbeitung der gesamten Befehls Puffer Arbeit abgeschlossen ist. Diese Schleife gibt S \_ OK erst zurück, wenn sich die GPU im Leerlauf befindet.
4.  Beispiel für die Startzeit.
5.  Aufrufen der API-Aufrufe, für die ein Profil erstellt wird
6.  Fügen Sie dem Befehls Puffer einen zweiten Abfrage Ereignis Marker hinzu. Dieser Marker wird verwendet, um den Abschluss der Aufrufe zu verfolgen.
7.  Der erste Aufruf leert den Befehls Puffer, da der Aufruf von [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) mit [**D3DGETDATA \_ Flush**](d3dgetdata-flush.md) das Leeren des Befehls Puffers erzwingt. Wenn die GPU die Verarbeitung der Befehls Puffer Arbeit abgeschlossen hat, gibt **GetData** S \_ OK zurück, und die Schleife wird beendet, da sich die GPU im Leerlauf befindet.
8.  Beispiel für die Endzeit.

Dies sind die Ergebnisse, die mit QueryPerformanceCounter und QueryPerformanceFrequency gemessen werden:



| Lokale Variable | Anzahl der Ticks |
|----------------|-----------------|
| start          | 1792998845060   |
| stop           | 1792998845090   |
| Freq           | 3579545         |



 

Erneutes Umrechnen von Ticks in Zyklen (auf einem Computer mit 2 GHz):


```
# ticks  = (stop - start) = 1792998845090 - 1792998845060 = 30 ticks
# cycles = CPU speed * number of ticks / QPF
# 16,450 = 2 GHz      * 30             / 3,579,545
```



Hier ist die Aufschlüsselung der Anzahl von Zyklen pro-Rückruf:


```
Number of cycles for SetTexture           : 100
Number of cycles for DrawPrimitive        : 900
Number of cycles for Issue                : 200
Number of cycles for GetData              : 16,450
```



Mit dem Abfrage Mechanismus haben wir die Steuerung der Laufzeit und der zu messenden Treiber Arbeit ermöglicht. Um diese Zahlen zu verstehen, geschieht Folgendes als Reaktion auf die einzelnen API-Aufrufe, und zwar zusammen mit den geschätzten Zeitangaben:

1.  Der erste Aufruf leert den Befehls Puffer, indem [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) mit [**D3DGETDATA \_ Flush**](d3dgetdata-flush.md)aufgerufen wird. Wenn die GPU die Verarbeitung der Befehls Puffer Arbeit abgeschlossen hat, gibt **GetData** S \_ OK zurück, und die Schleife wird beendet, da sich die GPU im Leerlauf befindet.
2.  Die rendersequenz beginnt mit dem Umrechnen von [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) in ein Geräte unabhängiges Format und dem Hinzufügen des Befehls Puffers. Angenommen, dies dauert ungefähr 100 Zyklen.
3.  [**Drawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) wird konvertiert und dem Befehls Puffer hinzugefügt. Angenommen, dies dauert ungefähr 900 Zyklen.
4.  [**Problem**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) fügt dem Befehls Puffer einen Abfrage Marker hinzu. Angenommen, dies dauert ungefähr 200 Zyklen.
5.  [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) bewirkt, dass der Befehls Puffer geleert wird, der den Kernel Modus-Übergang erzwingt. Angenommen, dies dauert ungefähr 5000 Zyklen.
6.  Der Treiber verarbeitet dann die Arbeit, die mit allen vier aufrufen verknüpft ist. Angenommen, die Treiber Zeit zum Verarbeiten von [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) beträgt ungefähr 2964 Zyklen, [**drawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) beträgt ungefähr 3600 Zyklen, das [**Problem**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) beträgt ungefähr 200 Zyklen. Die gesamte Treiber Zeit für alle vier Befehle beträgt ungefähr 6450 Zyklen.
    > [!Note]  
    > Der Treiber benötigt auch etwas Zeit, um den Status der GPU anzuzeigen. Da die GPU-Arbeit trivial ist, sollte die GPU bereits ausgeführt werden. " [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) " gibt "S OK" zurück \_ , basierend auf der Wahrscheinlichkeit, dass die GPU abgeschlossen ist.

     

7.  Nachdem der Treiber seine Arbeit beendet hat, gibt der Benutzermodus-Übergang die Steuerung an die Laufzeit zurück. Der Befehls Puffer ist jetzt leer. Angenommen, dies dauert ungefähr 5000 Zyklen.

Die Zahlen für [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) umfassen Folgendes:


```
GetData = kernel-transition + driver work + user-transition
GetData = 5000              + 6450        + 5000           
GetData = 16,450  

driver work = SetTexture + DrawPrimitive + Issue = 
driver work = 2964       + 3600          + 200   = 6450 cycles 
```



Der Abfrage Mechanismus, der in Kombination mit QueryPerformanceCounter verwendet wird, misst die gesamte CPU-Arbeit. Dies erfolgt mit einer Kombination aus Abfrage Markierungen und Abfrage Status vergleichen. Die dem Befehls Puffer hinzugefügten Abfrage Marker zum Starten und Abbrechen werden verwendet, um zu steuern, wie viel Arbeit im Puffer liegt. Wenn Sie warten, bis der richtige Rückgabecode zurückgegeben wird, wird die Start Messung unmittelbar vor dem Start einer sauberen Rendering-Sequenz durchgeführt, und die Beendigung der Messung erfolgt direkt, nachdem der Treiber die mit dem Inhalt des Befehls Puffers verknüpfte Arbeit abgeschlossen hat. Dadurch werden sowohl die CPU-Arbeit, die von der Laufzeit als auch der Treiber ausgeführt wird, erfasst.

Nachdem Sie nun über den Befehls Puffer und die Auswirkungen auf die Profilerstellung informiert sind, sollten Sie wissen, dass es einige andere Bedingungen gibt, die bewirken können, dass die Laufzeit den Befehls Puffer leert. Sie müssen in ihren Rendering-Sequenzen darauf achten. Einige dieser Bedingungen gelten als Reaktion auf API-Aufrufe, andere als Reaktion auf Ressourcen Änderungen in der Laufzeit. Eine der folgenden Bedingungen führt zu einem modusübergang:

-   Wenn eine der Sperr Methoden ([**Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock)) für einen Vertex-Puffer, einen Index Puffer oder eine Textur (unter bestimmten Bedingungen mit bestimmten Flags) aufgerufen wird.
-   Wenn ein Gerät oder Vertex-Puffer, Index Puffer oder eine Textur erstellt wird.
-   Wenn ein Gerät oder Vertex-Puffer, Index Puffer oder eine Textur durch die letzte Freigabe zerstört wird.
-   Wenn " [**ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) " aufgerufen wird.
-   Wenn [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) aufgerufen wird.
-   Wenn sich der Befehls Puffer füllt.
-   Wenn [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) mit D3DGETDATA Flush aufgerufen wird \_ .

Achten Sie darauf, diese Bedingungen in ihren Rendering-Sequenzen zu überwachen. Jedes Mal, wenn ein modusübergang hinzugefügt wird, werden den Profil Erstellungs Messungen 10.000 Zyklen der Treiber Arbeit hinzugefügt. Außerdem ist der Befehls Puffer nicht statisch formatiert. Die Laufzeit kann die Größe des Puffers in Reaktion auf die Menge der Arbeit ändern, die von der Anwendung generiert wird. Dies ist noch eine andere Optimierung, die von einer rendersequenz abhängt.

Achten Sie daher darauf, während der Profilerstellung die Übergänge im Modus zu steuern Der-Abfrage Mechanismus bietet eine robuste Methode zum Leeren des Befehls Puffers, sodass Sie die zeitliche Steuerung des modusübergangs und die Menge der im Puffer enthaltenen Arbeit steuern können. Diese Vorgehensweise kann jedoch auch durch eine Reduzierung der Übergangszeit des Modus verbessert werden, damit Sie in Bezug auf das gemessene Ergebnis nicht signifikant ist.

### <a name="make-the-render-sequence-large-compared-to-the-mode-transition"></a>Renderingsequenz im Vergleich zum modusübergang als groß festlegen

Im vorherigen Beispiel verbrauchen der kernelmodusschalter und der benutzermodusschalter ungefähr 10.000 Zyklen, die keine Lauf Zeit-und Treiber Arbeit haben. Da der modusübergang in das Betriebssystem integriert ist, kann er nicht auf 0 (null) reduziert werden. Damit der Modus nicht mehr unbedeutend ist, muss die rendersequenz so angepasst werden, dass die Treiber-und Lauf Zeit Aufgaben eine Größenordnung haben, die größer als die Modusschalter ist. Sie könnten versuchen, eine Subtraktion durchzuführen, um die Übergänge zu entfernen, aber die Amortisierungen der Kosten für eine weitaus größere Anzahl von Rendering-Sequenz Kosten ist zuverlässiger.

Die Strategie zur Reduzierung des modusübergangs, bis Sie unbedeutend wird, besteht darin, der rendersequenz eine Schleife hinzuzufügen. Betrachten Sie z. b. die Profil Erstellungs Ergebnisse, wenn eine Schleife hinzugefügt wird, die die rendersequenz 1500-mal wiederholt:


```
// Initialize the array with two textures, same size, same format
IDirect3DTexture* texArray[2];

CreateQuery(D3DQUERYTYPE_EVENT, pEvent);
pEvent->Issue(D3DISSUE_END);
while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

LARGE_INTEGER start, stop;
// Now start counting because the video card is ready
QueryPerformanceCounter(&start);

// Add a loop to the render sequence 
for(int i = 0; i < 1500; i++)
{
  SetTexture(taxArray[i%2]);
  DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
}

pEvent->Issue(D3DISSUE_END);

while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
QueryPerformanceCounter(&stop);
```



Beispiel 4: Hinzufügen einer Schleife zur rendersequenz

Dies sind die Ergebnisse, die mit QueryPerformanceCounter und QueryPerformanceFrequency gemessen werden:



| Lokale Variable | Anzahl von Tics |
|----------------|----------------|
| start          | 1792998845000  |
| stop           | 1792998847084  |
| Freq           | 3579545        |



 

Die Verwendung von QueryPerformanceCounter misst 2.840 Ticks jetzt. Das Umrechnen von Ticks in Zyklen ist das gleiche wie bereits gezeigt:


```
# ticks  = (stop - start) = 1792998847084 - 1792998845000 = 2840 ticks
# cycles    = machine speed * number of ticks / QPF
# 6,900,000 = 2 GHz          * 2840           / 3,579,545
```



Das heißt, es werden ungefähr 6,9 Millionen Zyklen auf diesem 2-GHz-Computer benötigt, um die 1500-Aufrufe in der Renderschleife zu verarbeiten. Von den 6,9 Millionen Zyklen ist die Zeitspanne im Modus von ungefähr 10K. die Profil Ergebnisse sind also fast vollständig mit der Verarbeitung von Arbeit, die mit [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) und [**drawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)verknüpft ist.

Beachten Sie, dass das Codebeispiel ein Array mit zwei Texturen erfordert. Um eine Lauf Zeitoptimierung zu vermeiden, die [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) entfernt, wenn Sie bei jedem Aufruf denselben Textur Zeiger festlegt, verwenden Sie einfach ein Array aus zwei Texturen. Auf diese Weise wird bei jedem Durchlaufen der Schleife der Textur Zeiger geändert, und die vollständige Arbeit, die mit **SetTexture** verknüpft ist, wird ausgeführt. Stellen Sie sicher, dass beide Texturen dieselbe Größe und dasselbe Format aufweisen, sodass sich bei der Textur kein anderer Zustand ändert.

Und jetzt verfügen Sie über eine Technik für die Profilerstellung Direct3D. Es basiert auf dem High Performance Counter (QueryPerformanceCounter), um die Anzahl der Ticks aufzuzeichnen, die die CPU zur Verarbeitung der Arbeit benötigt. Die Arbeit wird sorgfältig gesteuert, um die Laufzeit-und Treiber Arbeit zu verwenden, die API-aufrufen mithilfe des Abfrage Mechanismus zugeordnet ist. Eine Abfrage stellt zwei Steuerungsmöglichkeiten bereit: zuerst, um den Befehls Puffer zu leeren, bevor die Rendering-Sequenz gestartet wird, und zweitens, wenn die GPU-Arbeit abgeschlossen ist.

Bisher wurde in diesem Artikel gezeigt, wie Sie ein Profil für eine Rendering-Sequenz erstellen. Jede Rendering-Sequenz ist recht einfach, enthält einen einzelnen [**drawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) -und einen [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) -Aufruf. Dies wurde erreicht, um den Fokus auf den Befehls Puffer und die Verwendung des Abfrage Mechanismus zu steuern. Im folgenden finden Sie eine kurze Zusammenfassung zum Erstellen eines Profils für eine beliebige Rendering-Sequenz:

-   Verwenden Sie einen leistungsstarken Leistungswert wie QueryPerformanceCounter, um die Zeit zu messen, die für die Verarbeitung der einzelnen API-Aufrufe benötigt wird. Verwenden Sie QueryPerformanceFrequency und die CPU-Taktfrequenz, um dies in die Anzahl der CPU-Zyklen pro API-Aufruf zu konvertieren.
-   Minimieren Sie die GPU-Arbeitsaufwand, indem Sie Dreiecks Listen rendern, wobei jedes Dreieck ein Pixel enthält.
-   Verwenden Sie den Abfrage Mechanismus, um den Befehls Puffer vor der Rendering-Sequenz zu leeren. Dadurch wird sichergestellt, dass die Profilerstellung die richtige Menge an Lauf Zeit-und Treiber Arbeit für die Rendering-Sequenz erfasst.
-   Steuern Sie den Arbeitsaufwand, der dem Befehls Puffer mit Abfrage Ereignis Markierungen hinzugefügt wird. Dieselbe Abfrage erkennt, wenn die GPU ihre Arbeit abgeschlossen hat. Da die GPU-Arbeit trivial ist, entspricht dies praktisch dem Messen, wann die Treiber Arbeit abgeschlossen ist.

Alle diese Verfahren werden verwendet, um Statusänderungen zu Profilen. Angenommen, Sie haben gelesen und verstanden, wie der Befehls Puffer gesteuert werden kann, und Sie haben die Baseline-Messungen für [**drawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)erfolgreich abgeschlossen, können Sie den Rendering-Sequenzen Zustandsänderungen hinzufügen. Beim Hinzufügen von Zustandsänderungen zu einer Rendering-Sequenz gibt es einige zusätzliche Herausforderungen bei der Profilerstellung. Wenn Sie Ihren Rendering-Sequenzen Zustandsänderungen hinzufügen möchten, stellen Sie sicher, dass Sie mit dem nächsten Abschnitt fortfahren.

## <a name="profiling-direct3d-state-changes"></a>Profilerstellung Direct3D Zustandsänderungen

Direct3D verwendet viele Rendering-Zustände, um fast jeden Aspekt der Pipeline zu steuern. Die APIs, die Zustandsänderungen verursachen, beinhalten eine beliebige Funktion oder Methode, die keine primitiven zeichnen- \* Aufrufe ist.

Zustandsänderungen sind schwierig, da Sie möglicherweise nicht in der Lage sind, die Kosten einer Zustandsänderung ohne Rendering anzuzeigen. Dies ist das Ergebnis des Lazy-Algorithmus, den der Treiber und die GPU verwenden, um die Arbeit zu verzögern, bis Sie unbedingt abgeschlossen werden muss. Im Allgemeinen sollten Sie die folgenden Schritte ausführen, um eine einzelne Zustandsänderung zu messen:

1.  Profil für [**drawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) zuerst erstellen.
2.  Fügen Sie eine Statusänderung zur Rendering-Sequenz hinzu, und erstellen Sie ein Profil der neuen Sequenz.
3.  Subtrahieren Sie den Unterschied zwischen den beiden Sequenzen, um die Kosten für die Zustandsänderung zu erhalten.

Natürlich gilt alles, was Sie mit der Verwendung des Abfrage Mechanismus gelernt haben und die rendersequenz in eine Schleife bringen, um die Kosten des Modus-Übergangs zu negieren.

### <a name="profiling-a-simple-state-change"></a>Profilerstellung für eine einfache Zustandsänderung

Beginnend mit einer Rendering-Sequenz, die [**drawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)enthält, finden Sie hier die Code Sequenz zum Messen der Kosten für das Hinzufügen von [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture):


```
// Get the start counter value as shown in Example 4 

// Initialize a texture array as shown in Example 4
IDirect3DTexture* texArray[2];

// Render sequence loop 
for(int i = 0; i < 1500; i++)
{
  SetTexture(0, texArray[i%2];
  
  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
}

// Get the stop counter value as shown in Example 4 
```



Beispiel 5: Messen eines API-Aufrufes mit einer Statusänderung

Beachten Sie, dass die-Schleife zwei Aufrufe enthält: [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) und [**drawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive). Die Rendering-Sequenz führt 1500-fache Schleifen aus und generiert ähnliche Ergebnisse wie die folgenden:



| Lokale Variable | Anzahl von Tics |
|----------------|----------------|
| start          | 1792998860000  |
| stop           | 1792998870260  |
| Freq           | 3579545        |



 

Das Umrechnen von Ticks in Zyklen wiederum ergibt folgendes:


```
# ticks  = (stop - start) = 1792998870260 - 1792998860000 = 10,260 ticks
# cycles    = machine speed * number of ticks / QPF
5,775,000   = 2 GHz          * 10,260         / 3,579,545
```



Durch die Unterteilung durch die Anzahl der Iterationen in der Schleife ergeben sich folgende Ergebnisse:


```
5,775,000 cycles / 1500 iterations = 3850 cycles for one iteration
```



Jede Iterations Schleife enthält eine Zustandsänderung und einen zeichnen-Befehl. Wenn Sie das Ergebnis der [**drawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) -Rendering-Sequenz subtrahieren, verbleibt Folgendes:


```
3850 - 1100 = 2750 cycles for SetTexture
```



Dies ist die durchschnittliche Anzahl von Zyklen zum Hinzufügen von [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) zu dieser Rendering-Sequenz. Diese Methode kann auch auf andere Zustandsänderungen angewendet werden.

Warum wurde [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) als einfache Zustandsänderung bezeichnet? Der Zustand, der festgelegt wird, wird eingeschränkt, sodass die Pipeline bei jeder Änderung des Status die gleiche Arbeitsmenge durchführt. Durch die Beschränkung beider Texturen auf die gleiche Größe und das gleiche Format wird für jeden **SetTexture** -Befehl die gleiche Menge an Arbeit sichergestellt.

### <a name="profiling-a-state-change-that-needs-to-be-toggled"></a>Profilerstellung für eine Statusänderung, die umgeschaltet werden muss

Es gibt andere Zustandsänderungen, die bewirken, dass sich der von der Grafik Pipeline ausgeführte Arbeitsaufwand für jede Iterationen der Renderschleife ändert. Wenn z. b. z-Tests aktiviert ist, aktualisiert jede Pixelfarbe ein Renderziel nur, nachdem der z-Wert des neuen Pixels mit dem z-Wert für das vorhandene Pixel getestet wurde. Wenn z-testing deaktiviert ist, wird dieser pro-Pixel-Test nicht durchgeführt, und die Ausgabe wird wesentlich schneller geschrieben. Durch das Aktivieren oder Deaktivieren des z-Test Zustands wird der Umfang der durchgeführten Arbeit (von der CPU und der GPU) während des Renderings erheblich geändert.

" [**Strenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) " erfordert einen bestimmten renderzustand und einen Zustandswert, um z-Tests zu aktivieren bzw. zu deaktivieren. Der bestimmte Zustandswert wird zur Laufzeit ausgewertet, um zu bestimmen, wie viel Arbeit erforderlich ist. Es ist schwierig, diese Zustandsänderung in einer Renderschleife zu messen und den Pipeline Status so zu ändern, dass er wechselt. Die einzige Lösung ist das Umschalten der Zustandsänderung während der Rendering-Sequenz.

Beispielsweise muss die Profil Erstellungs Methode wie folgt zweimal wiederholt werden:

1.  Beginnen Sie mit der Profilerstellung der [**drawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) -Rendering-Sequenz. Nennen Sie dies als Baseline.
2.  Profil für eine zweite Rendering-Sequenz erstellen, die die Statusänderung schaltet. Die rendersequenzschleife enthält Folgendes:
    -   Eine Statusänderung zum Festlegen des Zustands in eine "false"-Bedingung.
    -   [**Drawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) genau wie die ursprüngliche Sequenz.
    -   Eine Statusänderung zum Festlegen des Zustands in eine "true"-Bedingung.
    -   Ein zweites [**drawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) , das die Realisierung der zweiten Zustandsänderung erzwingen soll.
3.  Suchen Sie den Unterschied zwischen den beiden Rendering-Sequenzen. Dies wird wie folgt erreicht:
    -   Multiplizieren Sie die Baseline [**drawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) -Sequenz mit 2, da in der neuen Sequenz zwei **drawprimitive** -Aufrufe vorhanden sind.
    -   Subtrahieren Sie das Ergebnis der neuen Sequenz aus der ursprünglichen Sequenz.
    -   Dividieren Sie das Ergebnis durch 2, um die durchschnittlichen Kosten der Zustandsänderung "false" und "true" zu erhalten.

Mit der in der rendersequenz verwendeten Schleifen Technik müssen die Kosten für das Ändern des Pipeline Zustands gemessen werden, indem der Status von "true" in "false" und umgekehrt für jede Iterationen in der rendersequenz geändert wird. Die Bedeutung von "true" und "false" hier ist kein Literalwert. Dies bedeutet einfach, dass der Zustand in gegen übergesetzte Bedingungen festgelegt werden muss. Dies bewirkt, dass beide Zustandsänderungen während der Profilerstellung gemessen werden. Natürlich gilt alles, was Sie mit der Verwendung des Abfrage Mechanismus gelernt haben und die Renderingsequenz in eine Schleife einfügen, um die Kosten für den modusübergang zu negieren.

Hier ist beispielsweise die Code Sequenz zum Messen der Kosten für das ein-und Ausschalten von z-Tests:


```
// Get the start counter value as shown in Example 4 

// Add a loop to the render sequence 
for(int i = 0; i < 1500; i++)
{
  // Precondition the pipeline state to the "false" condition
  SetRenderState(D3DRS_ZENABLE, FALSE);
  
  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 0)*3, 1);

  // Set the pipeline state to the "true" condition
  SetRenderState(D3DRS_ZENABLE, TRUE);

  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 1)*3, 1); 
}

// Get the stop counter value as shown in Example 4 
```



Beispiel 5: Messen der Statusänderung für das Umschalten

Die Schleife schaltet den Zustand um, indem Sie zwei " [**strenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) "-Aufrufe ausführt. Der erste **setrenderstate** -Befehl deaktiviert z-Tests, und der zweite **setrenderstate** ermöglicht z-Tests. Auf jeden " **strenderstate** " folgt " [**drawprimiprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) ", sodass die mit der Zustandsänderung verknüpfte Arbeit vom Treiber verarbeitet wird, anstatt nur ein ändertes Bit im Treiber festzulegen.

Diese Zahlen sind für diese Rendering-Sequenz angemessen:



| Lokale Variable | Anzahl der Ticks |
|----------------|-----------------|
| start          | 1792998845000   |
| stop           | 1792998861740   |
| Freq           | 3579545         |



 

Das Umrechnen von Ticks in Zyklen wiederum ergibt folgendes:


```
# ticks  = (stop - start) = 1792998861740 - 1792998845000 = 15,120 ticks
# cycles    = machine speed * number of ticks / QPF
 9,300,000  = 2 GHz          * 16,740         / 3,579,545
```



Durch die Unterteilung durch die Anzahl der Iterationen in der Schleife ergeben sich folgende Ergebnisse:


```
9,300,000 cycles / 1500 iterations = 6200 cycles for one iteration
```



Jede Iterations Schleife enthält zwei Statusänderungen und zwei Draw-Aufrufe. Das Subtrahieren der Draw-Aufrufe (ausgehend von 1100 Zyklen) verlässt Folgendes:


```
6200 - 1100 - 1100 = 4000 cycles for both state changes
```



Dies ist die durchschnittliche Anzahl von Zyklen für beide Statusänderungen, sodass die durchschnittliche Zeit für jede Zustandsänderung lautet:


```
4000 / 2  = 2000 cycles for each state change
```



Daher ist die durchschnittliche Anzahl von Zyklen zum Aktivieren oder Deaktivieren von z-Tests 2000 Zyklen. Beachten Sie, dass QueryPerformanceCounter z-enable halb und z-Deaktivierung der Hälfte der Zeit misst. Mit dieser Technik wird der Durchschnitt der beiden Zustandsänderungen gemessen. Das heißt, Sie messen die Zeit zum Umschalten eines Zustands. Mit dieser Technik können Sie nicht wissen, ob die Aktivierungs-und Deaktivierungs Zeiten gleichwertig sind, da Sie den Durchschnitt beider Elemente gemessen haben. Dies ist jedoch eine angemessene Zahl, die beim budgetieren eines umgeschaltenden Zustands als Anwendung, die diese Zustandsänderung bewirkt, nur durch Umschalten dieses Zustands verwendet werden kann.

Nun können Sie diese Techniken anwenden und Profile für alle gewünschten Zustandsänderungen erstellen. Noch nicht ganz. Sie müssen jedoch immer noch mit Optimierungen bedacht werden, die so entworfen wurden, dass Sie den Aufwand für die Arbeit reduzieren. Es gibt zwei Arten von Optimierungen, die Sie beim Entwerfen der Rendering-Sequenzen beachten sollten.

### <a name="watch-out-for-state-change-optimizations"></a>Überwachen der Optimierungen von Statusänderungen

Der vorherige Abschnitt zeigt, wie Sie ein Profil für beide Arten von Zustandsänderungen erstellen können: eine einfache Zustandsänderung, die so eingeschränkt ist, dass für jede Iterations Menge die gleiche Menge an Arbeit generiert wird, und eine umschaltbare Zustandsänderung, durch die der Umfang der Arbeit erheblich geändert wird. Was geschieht, wenn Sie die vorherige Rendering-Sequenz nehmen und eine andere Zustandsänderung hinzufügen? Beispielsweise wird in diesem Beispiel die z->-enable-Rendering-Sequenz angenommen, und es wird ein z-Func-Vergleich hinzugefügt:


```
// Add a loop to the render sequence 
for(int i = 0; i < 1500; i++)
{
  // Precondition the pipeline state to the opposite condition
  SetRenderState(D3DRS_ZFUNC, D3DCMP_NEVER);

  // Precondition the pipeline state to the opposite condition
  SetRenderState(D3DRS_ZENABLE, FALSE);
  
  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 0)*3, 1);

  // Now set the state change you want to measure
  SetRenderState(D3DRS_ZFUNC, D3DCMP_ALWAYS);

  // Now set the state change you want to measure
  SetRenderState(D3DRS_ZENABLE, TRUE);

  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 1)*3, 1); 
}
```



Mit dem z-Func-Zustand wird die Vergleichs Ebene beim Schreiben in den z-Puffer (zwischen dem z-Wert eines aktuellen Pixels mit dem z-Wert eines Pixels im tiefen Puffer) festgelegt. D3DCMP deaktiviert \_ den z-Test-Vergleich nie, während D3DCMP \_ immer den Vergleich so festlegt, dass er jedes Mal durchgeführt wird, wenn z-Tests durchgeführt werden.

Die Profilerstellung für eine dieser Statusänderungen in einer Rendering-Sequenz mit [**drawprimitiver**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) generiert ähnliche Ergebnisse wie die folgenden:



| Änderung des einzelnen Zustands | Durchschnittliche Anzahl von Zyklen |
|---------------------|--------------------------|
| \_Nur D3DRS zenable | 2000                     |



 

oder



| Änderung des einzelnen Zustands | Durchschnittliche Anzahl von Zyklen |
|---------------------|--------------------------|
| \_Nur D3DRS zfunc   | 600                      |



 

Wenn Sie jedoch ein Profil für "D3DRS \_ zenable" und "D3DRS \_ zfunc" in derselben Rendering-Sequenz erstellen, sehen Sie die Ergebnisse wie die folgenden:



| Beide Statusänderungen            | Durchschnittliche Anzahl von Zyklen |
|-------------------------------|--------------------------|
| D3DRS \_ zenable + D3DRS \_ zfunc | 2000                     |



 

Sie können davon ausgehen, dass das Ergebnis die Summe aus 2000-und 600-Zyklen (bzw. 2600) ist, da der Treiber alle Aufgaben durchführt, die mit der Festlegung beider renderzustände verknüpft sind. Stattdessen beträgt der Durchschnitt 2000 Zyklen.

Dieses Ergebnis spiegelt eine in der Laufzeit, dem Treiber oder der GPU implementierte Status Änderungs Optimierung wider. In diesem Fall könnte der Treiber den ersten [**setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) sehen und einen geänderten Zustand festlegen, der die Arbeit bis zu einem späteren Zeitpunkt verschiebt. Wenn der Treiber den zweiten **setrenderstate** sieht, könnte der gleiche geänderte Zustand redundant festgelegt werden, und die gleiche Arbeit würde erneut verschoben werden. Wenn [**drawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) aufgerufen wird, wird die dem Zustand "geändert" zugeordnete Arbeit schließlich verarbeitet. Der Treiber führt die Arbeit einmal aus, was bedeutet, dass die ersten beiden Zustandsänderungen effektiv vom Treiber konsolidiert werden. Ebenso werden die dritten und vierten Zustandsänderungen durch den Treiber in eine einzelne Zustandsänderung konsolidiert, wenn der zweite **drawprimitiv** aufgerufen wird. Das Ergebnis ist, dass der Treiber und die GPU eine einzelne Statusänderung für jeden zeichnen-Befehl verarbeiten.

Dies ist ein gutes Beispiel für eine Sequenz abhängige Treiber Optimierung. Der Treiber hat den Vorgang zweimal ausgeführt, indem er einen fehlerhaften Zustand festgelegt und die Arbeit dann einmal ausgeführt hat, um den geänderten Zustand zu löschen. Dies ist ein gutes Beispiel für die Art der Verbesserung der Effizienz, die durchgeführt werden kann, wenn die Arbeit bis zum absolut notwendig verzögert wird.

Woher wissen Sie, welche Zustandsänderungen intern einen fehlerhaften Zustand festlegen und daher die Arbeit bis zu einem späteren Zeitpunkt verschieben? Nur durch das Testen von Rendering-Sequenzen (oder das Gespräch mit Treiber-Writer). Treiber werden regelmäßig aktualisiert und verbessert, sodass die Liste der Optimierungen nicht statisch ist. Es gibt nur eine Möglichkeit, um genau zu wissen, welche Zustandsänderung in einer bestimmten Rendering-Sequenz für einen bestimmten Satz von Hardwarekosten anfallen. und das soll Sie messen.

### <a name="watch-out-for-drawprimitive-optimizations"></a>Weitere Informationen zu drawprimitiven Optimierungen

Zusätzlich zu den Optimierungen bei der Statusänderung versucht die Laufzeit, die Anzahl der Draw-Aufrufe zu optimieren, die der Treiber verarbeiten muss. Sehen Sie sich beispielsweise an, dass die Aufrufe zurück zeichnen:


```
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 3); // Draw 3 primitives, vertices 0 - 8
DrawPrimitive(D3DPT_TRIANGLELIST, 9, 4); // Draw 4 primitives, vertices 9 - 20
```



Beispiel 5A: zwei Draw-Aufrufe

Diese Sequenz enthält zwei Draw-Aufrufe, die von der Laufzeit in einem einzelnen Aufruf konsolidiert werden, der entspricht:


```
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 7); // Draw 7 primitives, vertices 0 - 20
```



Beispiel 5B: ein einzelner verketteten zeichnen-Befehl

Die Laufzeit verkettet beide zeichnen-Aufrufe in einem einzelnen Aufruf, wodurch die Treiber Arbeit um 50 Prozent reduziert wird, da der Treiber jetzt nur einen Draw-Aufruf verarbeiten muss.

Im allgemeinen verkettet die Common Language Runtime zwei oder mehr Rückrufe für [**drawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) , wenn Folgendes gilt:

1.  Der primitive Typ ist eine Dreiecks Liste (D3DPT \_ trianglelist).
2.  Jeder aufeinander folgende [**drawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) -Befehl muss auf aufeinander folgende Vertices innerhalb des Vertexpuffers verweisen.

Analog dazu sind die richtigen Bedingungen zum Verketten zweier oder mehrerer Rückrufe von [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) :

1.  Der primitive Typ ist eine Dreiecks Liste (D3DPT \_ trianglelist).
2.  Jeder aufeinanderfolgende [**drawindexedprimitiver**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) -Befehl muss aufeinander folgende Indizes im Index Puffer sequenziell referenzieren.
3.  Jeder aufeinanderfolgende [**drawindexedprimitiver**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) -Befehl muss für basevertexindex denselben Wert verwenden.

Um die Verkettung während der Profilerstellung zu verhindern, ändern Sie die rendersequenz so, dass der primitive Typ keine Dreiecks Liste ist, oder ändern Sie die rendersequenz so, dass keine Back-to-Back-Draw-Aufrufe vorhanden sind, die aufeinander folgende Vertices (oder Indizes) verwenden. Genauer gesagt werden von der Laufzeit auch Draw-Aufrufe verkettet, die die beiden folgenden Bedingungen erfüllen:

-   Wenn der vorherige-Befehl [**drawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)ist, wenn der nächste Draw-Befehl:
    -   verwendet eine Dreiecks Liste und
    -   Gibt den startVertex = Vorheriges startVertex + vorherige primitivecount 3 an. \*
-   Wenn beim nächsten zeichnen-Befehl [**drawindexedprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)verwendet wird:
    -   verwendet eine Dreiecks Liste und
    -   Gibt die Start Index = Previous startIndex + Previous primitivecount \* 3 und
    -   Gibt den basevertexindex = Previous basevertexindex an.

Im folgenden finden Sie ein feineres Beispiel für die Verkettung von zeichnen-aufrufen, die bei der Profilerstellung leicht zu übersehen ist. Angenommen, die Rendering-Sequenz sieht wie folgt aus:


```
  for(int i = 0; i < 1500; i++)
  {
    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
  }
```



Beispiel 5C: eine Zustandsänderung und ein zeichnen-Befehl

Die Schleife durchläuft 1500 Dreiecke, legt eine Textur fest und zeichnet jedes Dreieck. Diese Renderschleife dauert ungefähr 2750 Zyklen für die [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) -und 1100-Zyklen für [**drawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) , wie in den vorherigen Abschnitten gezeigt. Sie werden möglicherweise intuitiv davon ausgehen, dass das Verschieben von **SetTexture** außerhalb der Renderschleife die vom Treiber ausgeführte Menge an Arbeit um 1500 \* 2750 Zyklen verringern sollte. Dies ist der Arbeitsaufwand, der mit dem Aufrufen von **SetTexture** 1500-mal verbunden ist. Der Code Ausschnitt würde wie folgt aussehen:


```
  SetTexture(...); // Set the state outside the loop
  for(int i = 0; i < 1500; i++)
  {
//    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
  }
```



Beispiel 5D: Beispiel 5C mit der Zustandsänderung außerhalb der Schleife

Durch das Verschieben von [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) außerhalb der Renderschleife wird die Menge an Arbeit reduziert, die **SetTexture** zugeordnet ist, da Sie einmal anstelle von 1500 Mal aufgerufen wird. Ein weniger offensichtlicher sekundärer Effekt ist, dass die Arbeit für [**drawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) auch von 1500 aufrufen auf einen Aufruf reduziert wird, da alle Bedingungen zum Verketten von zeichnen-aufrufen erfüllt sind. Wenn die Rendering-Sequenz verarbeitet wird, verarbeitet die Laufzeit 1500-Aufrufe an einen einzelnen Treiber Aufruf. Wenn Sie diese eine Codezeile verschieben, wurde die Menge der Treiber Arbeit drastisch reduziert:


```
total work done = runtime + driver work

Example 5c: with SetTexture in the loop:
runtime work = 1500 SetTextures + 1500 DrawPrimitives 
driver  work = 1500 SetTextures + 1500 DrawPrimitives 

Example 5d: with SetTexture outside of the loop:
runtime work = 1 SetTexture + 1 DrawPrimitive + 1499 Concatenated DrawPrimitives 
driver  work = 1 SetTexture + 1 DrawPrimitive 
```



Diese Ergebnisse sind vollständig richtig, sind jedoch im Kontext der ursprünglichen Frage sehr irreführend. Die Optimierung des Draw-Aufrufes hat bewirkt, dass die Menge der Treiber Arbeit drastisch reduziert wurde. Dies ist ein häufiges Problem bei der benutzerdefinierten Profilerstellung. Wenn Sie Aufrufe aus einer Rendering-Sequenz entfernen, achten Sie darauf, die Verkettung von Draw-aufrufen zu vermeiden. Tatsächlich handelt es sich hierbei um ein leistungsfähiges Beispiel für den Umfang der Verbesserung der Treiber Leistung, die durch diese Lauf Zeitoptimierung möglich ist.

Nun wissen Sie, wie Zustandsänderungen gemessen werden. Starten Sie die Profilerstellung für [**drawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive). Fügen Sie dann jede weitere Zustandsänderung der Sequenz hinzu (in einigen Fällen durch Hinzufügen eines Aufrufs und in anderen Fällen durch Hinzufügen von zwei aufrufen), und Messen Sie den Unterschied zwischen den beiden Sequenzen. Sie können die Ergebnisse in Ticks oder Zyklen oder Zeit konvertieren. Ebenso wie das Messen von rendersequenzen mit QueryPerformanceCounter basiert das Messen einzelner Zustandsänderungen auf dem Abfrage Mechanismus zum Steuern des Befehls Puffers und dem Einfügen der Zustandsänderungen in einer Schleife, um die Auswirkungen der Modus-Übergänge zu minimieren. Mit dieser Technik werden die Kosten für das Umschalten eines Zustands gemessen, da der Profiler den Durchschnitt der Aktivierung und Deaktivierung des Zustands zurückgibt.

Mit dieser Funktion können Sie beginnen, beliebige renderingsequenzen zu erzeugen und die zugeordnete Lauf Zeit-und Treiber Arbeit genau zu messen. Die Zahlen können dann verwendet werden, um Budgetierungs Fragen zu beantworten, wie z. b. "wie viele dieser Aufrufe in der Rendering-Sequenz erfolgen können, während gleichzeitig eine angemessene Framerate beibehalten wird.

## <a name="summary"></a>Zusammenfassung

In diesem Artikel wird veranschaulicht, wie der Befehls Puffer gesteuert werden kann, sodass für einzelne Aufrufe eine exakte Profilerstellung durchgeführt werden kann. Die Profil Erstellungs Nummern können in Ticks, Zyklen oder absoluter Zeit generiert werden. Sie stellen die Menge der Lauf Zeit-und Treiber Arbeit dar, die den einzelnen API-Anrufen zugeordnet sind.

Beginnen Sie mit der Profilerstellung eines \* primitiven Aufrufes Aufrufes in einer-Rendering Beachten Sie Folgendes:

1.  Verwenden Sie QueryPerformanceCounter, um die Anzahl der Ticks pro API-Aufrufe zu messen. Verwenden Sie QueryPerformanceFrequency, um die Ergebnisse in Zyklen oder Zeit zu konvertieren, wenn Sie möchten.
2.  Verwenden Sie den Abfrage Mechanismus, um den Befehls Puffer vor dem Starten zu leeren.
3.  Schließen Sie die rendersequenz in eine Schleife ein, um die Auswirkung des modusübergangs zu minimieren.
4.  Verwenden Sie den Abfrage Mechanismus, um zu messen, wann die GPU ihre Arbeit abgeschlossen hat.
5.  Achten Sie auf die Lauf Zeit Verkettung, bei der der Umfang der Arbeit maßgeblich beeinträchtigt wird.

Dadurch erhalten Sie eine grundlegende Leistung für [**drawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) , die zum Erstellen von verwendet werden kann. Zum Erstellen eines Profils für eine Statusänderung folgen Sie den folgenden zusätzlichen Tipps:

1.  Fügen Sie die Zustandsänderung zu einem bekannten Rendering-Sequenz Profil der neuen Sequenz hinzu. Da die Tests in einer-Schleife durchgeführt werden, muss der Zustand zweimal in umgekehrten Werten festgelegt werden (z. b. aktivieren und deaktivieren).
2.  Vergleichen Sie den Unterschied in den Zyklen zwischen den zwei Sequenzen.
3.  Bei Zustandsänderungen, die die Pipeline erheblich ändern (z. b. [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)), subtrahieren Sie die Differenz zwischen den beiden Sequenzen, um die Zeit für die Zustandsänderung zu erhalten.
4.  Bei Zustandsänderungen, bei denen die Pipeline erheblich geändert wird (und daher ein-/Ausschalten von Zuständen wie z. b. "* Trend Name" erforderlich ist), wird der Unterschied zwischen den [**rendersequenzen**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)subtrahiert Dadurch wird die durchschnittliche Anzahl von Zyklen für jede Zustandsänderung generiert.

Seien Sie jedoch vorsichtig mit Optimierungen, die bei der Profilerstellung unerwartete Ergebnisse verursachen. Mit Status Änderungs Optimierungen können geänderte Zustände festgelegt werden, die dazu führten, dass die Arbeit verzögert wird. Dies kann zu Profil Ergebnissen führen, die nicht so intuitiv wie erwartet sind. Zeichnen-Befehle, die verkettet werden, reduzieren die Treiber Arbeit drastisch, was zu irreführenden Schlussfolgerungen führen kann. Sorgfältig geplante rendersequenzen werden verwendet, um die Verkettung von Zustandsänderungen und Draw-aufrufen zu verhindern. Der Trick besteht darin, zu verhindern, dass die Optimierungen während der Profilerstellung durchgeführt werden, sodass die von Ihnen generierten Zahlen sinnvolle Budgetzahlen sind.

> [!Note]  
> Das Duplizieren dieser Profil Erstellungs Strategie in einer Anwendung ohne den Abfrage Mechanismus ist schwieriger. Vor Direct3D 9 besteht die einzige vorhersagbare Möglichkeit zum Leeren des Befehls Puffers darin, eine aktive Oberfläche (z. b. ein Renderziel) zu sperren, um zu warten, bis die GPU im Leerlauf ist Dies liegt daran, dass das Sperren einer Oberfläche die Laufzeit zum Leeren des Befehls Puffers zwingt, wenn im Puffer renderbefehle vorhanden sind, die die Oberfläche vor dem Sperren aktualisieren sollten, zusätzlich zum warten auf den Abschluss der GPU. Diese Technik ist funktionsfähig, auch wenn Sie mit dem in Direct3D 9 eingeführten Abfrage Mechanismus besser verwahrter ist.

 

## <a name="appendix"></a>Anhang

Bei den Zahlen in dieser Tabelle handelt es sich um einen Bereich von Näherungen für die Laufzeit-und Treiber Arbeit, die mit den einzelnen Statusänderungen verknüpft ist. Die Näherungs Werte basieren auf den tatsächlichen Messungen von Treibern, die die im Dokument gezeigten Verfahren verwenden. Diese Zahlen wurden mit der Direct3D 9-Laufzeit generiert und sind Treiber abhängig.

Die Verfahren in diesem Artikel sind so konzipiert, dass die Laufzeit und die Treiber Arbeit gemessen werden. Im Allgemeinen ist es nicht praktikabel, Ergebnisse bereitzustellen, die der Leistung der CPU und der GPU in jeder Anwendung entsprechen, da dies ein umfassendes Array von Rendering-Sequenzen erfordern würde. Außerdem ist es besonders schwierig, die Leistung der GPU zu messen, da Sie stark von der Zustands Einrichtung in der Pipeline vor der Rendering-Sequenz abhängt. Beispielsweise hat das Aktivieren von Alpha Blending kaum Auswirkungen auf die erforderliche CPU-Arbeit, kann jedoch eine große Auswirkung auf die von der GPU ausgeführte Arbeitsauslastung haben. Aus diesem Grund schränken die Verfahren in diesem Artikel die GPU auf den minimal möglichen Betrag ein, indem Sie die Menge der Daten einschränken, die gerendert werden müssen. Dies bedeutet, dass die Zahlen in der Tabelle am ehesten mit den Ergebnissen übereinstimmen, die von Anwendungen erzielt werden, die CPU-beschränkt sind (im Gegensatz zu einer Anwendung, die durch die GPU eingeschränkt ist).

Es wird empfohlen, die vorgestellten Techniken zu verwenden, um die für Sie wichtigsten Szenarien und Konfigurationen abzudecken. Die Werte in der Tabelle können verwendet werden, um mit den von Ihnen generierten Zahlen zu vergleichen. Da jeder Treiber variiert, ist die einzige Möglichkeit zum Generieren der tatsächlichen Zahlen, die Sie sehen, das Generieren von Profil Erstellungs Ergebnissen mithilfe ihrer Szenarien.



| API-Aufruf                             | Durchschnittliche Anzahl von Zyklen |
|--------------------------------------|--------------------------|
| Setvertexdeclaration                 | 6500-11250             |
| Setf-VF                               | 6400-11200             |
| Setvertexshader                      | 3000-12100             |
| Setpixelshader                       | 6300-7000              |
| Specularenable                       | 1900-11200             |
| "Zielort"                      | 6000-6250              |
| Setpixelshaderconstant (1-Konstante)  | 1500-9000              |
| Normalizenormals                     | 2200-8100              |
| Lightenable                          | 1300-9000              |
| SetStreamSource                      | 3700-5800              |
| Sonder                             | 1700-7500              |
| DiffuseMaterialSource                | 900-8300               |
| AmbientMaterialSource                | 900-8200               |
| ColorVertex                          | 800-7800               |
| Setlight                             | 2200-5100              |
| SetTransform                         | 3200-3750              |
| Setindizes                           | 900-5600               |
| AMBIENT                              | 1150-4800              |
| SetTexture                           | 2500-3100              |
| SpecularMaterialSource               | 900-4600               |
| Emissivematerialsource               | 900-4500               |
| Setmaterial                          | 1000-3700              |
| Zenzierbar                              | 700-3900               |
| WRAP0                                | 1600-2700              |
| MinFilter                            | 1700-2500              |
| MagFilter                            | 1700-2400              |
| Setvertexshaderconstant (1 Konstante) | 1000-2700              |
| Colorop                              | 1500-2100              |
| COLORARG2                            | 1300-2000              |
| COLORARG1                            | 1300-1980              |
| CullMode                             | 500-2570               |
| Clipping                             | 500-2550               |
| Drawindexedprimitiv                 | 1200-1400              |
| Adressssv                             | 1090-1500              |
| Adresssu                             | 1070-1500              |
| Drawprimitiv                        | 1050-1150              |
| Srgbtexture                          | 150-1500               |
| Schablone Mask                          | 570-700                |
| Stencilzfail                         | 500-800                |
| Schablone Ref                           | 550-700                |
| AlphaBlendEnable                     | 550-700                |
| Schablone Func                          | 560-680                |
| Schablone                     | 520-700                |
| Stencilfail                          | 500-750                |
| Zfunc                                | 510-700                |
| Zbeschreib teenable                         | 520-680                |
| Schablone möglich                        | 540-650                |
| Schablone-Pass                          | 560-630                |
| Srcblend                             | 500-685                |
| Zwei \_ seitiger \_ stencilmode              | 450-590                |
| Alpha atestenable                      | 470-525                |
| Alpha Aref                             | 460-530                |
| Alphafunc                            | 450-540                |
| Destblend                            | 475-510                |
| Colorschreiteenable                     | 465-515                |
| CCW- \_ stencilfail                     | 340-560                |
| CCW- \_ stencilpass                     | 340-545                |
| CCW- \_ stencilzfail                    | 330-495                |
| Scissortestenable                    | 375-440                |
| CCW- \_ Schablone                     | 250-480                |
| "S\cissorrect"                       | 150-340                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterte Themen](advanced-topics.md)
</dt> </dl>

 

 
