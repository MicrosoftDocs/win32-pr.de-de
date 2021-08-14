---
description: Sobald Sie über eine funktionsfähige Microsoft Direct3D-Anwendung verfügen und ihre Leistung verbessern möchten, verwenden Sie in der Regel ein standardfertiges Profilerstellungstool oder eine benutzerdefinierte Messtechnik, um die Zeit zu messen, die zum Ausführen eines oder mehrere API-Aufrufe (Application Programming Interface) benötigt wird. Wenn Sie dies getan haben, aber Zeitsteuerungsergebnisse erhalten, die von einer Rendersequenz zur nächsten variieren, oder Sie Hypothesen erstellen, die die tatsächlichen Experimentergebnisse nicht unterstützen, können Ihnen die folgenden Informationen helfen, die Gründe zu verstehen.
ms.assetid: f969be42-d541-4e8d-aec4-eb9508bcc7cf
title: Exakte Profilerstellung für Direct3D-API-Aufrufe (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6457e47da58a3614270f89eefa1cfa33fbf30cf26544c1013d010696a68e4602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118097492"
---
# <a name="accurately-profiling-direct3d-api-calls-direct3d-9"></a>Exakte Profilerstellung für Direct3D-API-Aufrufe (Direct3D 9)

-   [Genaue Profilerstellung für Direct3D ist schwierig](#accurately-profiling-direct3d-is-difficult)
-   [Präzises Profil einer Direct3D-Rendersequenz](#how-to-accurately-profile-a-direct3d-render-sequence)
-   [Profilerstellung für Direct3D-Statusänderungen](#profiling-direct3d-state-changes)
-   [Zusammenfassung](#summary)
-   [Anhang](#appendix)

Sobald Sie über eine funktionsfähige Microsoft Direct3D-Anwendung verfügen und ihre Leistung verbessern möchten, verwenden Sie in der Regel ein standardfertiges Profilerstellungstool oder eine benutzerdefinierte Messtechnik, um die Zeit zu messen, die zum Ausführen eines oder mehrere API-Aufrufe (Application Programming Interface) benötigt wird. Wenn Sie dies getan haben, aber Zeitsteuerungsergebnisse erhalten, die von einer Rendersequenz zur nächsten variieren, oder Sie Hypothesen erstellen, die die tatsächlichen Experimentergebnisse nicht unterstützen, können Ihnen die folgenden Informationen helfen, die Gründe zu verstehen.

Die hier bereitgestellten Informationen basieren auf der Annahme, dass Sie über Kenntnisse und Erfahrung mit Folgenden verfügen:

-   C/C++-Programmierung
-   Direct3D-API-Programmierung
-   Messen der API-Zeitsteuerung
-   Die Grafikkarte und deren Softwaretreiber
-   Mögliche unerklärliche Ergebnisse der vorherigen Profilerstellungserfahrung

## <a name="accurately-profiling-direct3d-is-difficult"></a>Genaue Profilerstellung für Direct3D ist schwierig

Ein Profiler meldet die Zeit, die in jedem API-Aufruf verbracht wird. Dies wird zur Verbesserung der Leistung durch Suchen und Optimieren von Hotspots durchgeführt. Es gibt verschiedene Arten von Profilern und Profilerstellungstechniken.

-   Ein Sampling-Profiler befindet sich einen großen Teil der Zeit im Leerlauf und wird in bestimmten Intervallen zur Stichprobenentnahme (oder Aufzeichnung) der ausgeführten Funktionen angezeigt. Sie gibt den Prozentsatz der Zeit zurück, die in jedem Aufruf verbracht wurde. Im Allgemeinen ist ein Sampling-Profiler für die Anwendung nicht sehr invasiv und hat nur minimale Auswirkungen auf den Mehraufwand für die Anwendung.
-   Ein Instrumentierungsprofiler misst die tatsächliche Zeit, die für die Rückgabe eines Aufrufs benötigt wird. Sie erfordert das Kompilieren von Start- und Stopptrennzeichen in eine Anwendung. Ein Instrumentierungsprofiler ist eine Anwendung im Vergleich zu einem Sampling-Profiler im Vergleich zu einem Sampling-Profiler im Vergleich zu einer Anwendung.
-   Es ist auch möglich, ein benutzerdefiniertes Profilerstellungsverfahren mit einem hochleistungsbasierten Timer zu verwenden. Dies führt zu Ergebnissen, die einem Instrumentierungsprofiler sehr ähnlich sind.

Die Art der verwendeten Profiler- oder Profilerstellungstechnik ist nur ein Teil der Herausforderung, genaue Messungen zu generieren.

Die Profilerstellung bietet Ihnen Antworten, die Ihnen beim Budgetieren der Leistung helfen. Angenommen, Sie wissen, dass ein API-Aufruf durchschnittlich 1.000 auszuführende Taktzyklen zurückträgt. Sie können einige Schlussfolgerungen zur Leistung ziehen, z. B.:

-   Eine 2-GHz-CPU (die 50 Prozent ihres Zeitrenderings verbringt) ist auf den 1-Millionen-Aufruf dieser API pro Sekunde beschränkt.
-   Um 30 Frames pro Sekunde zu erreichen, können Sie diese API nicht mehr als 33.000 Mal pro Frame aufrufen.
-   Sie können nur 3,3.3.000 Objekte pro Frame rendern (vorausgesetzt, 10 dieser API-Aufrufe für die Rendersequenz jedes Objekts).

Anders ausgedrückt: Wenn Sie pro API-Aufruf genügend Zeit hatten, können Sie eine Budgetierungsfrage beantworten, z. B. die Anzahl von Primitiven, die interaktiv gerendert werden können. Die von einem Instrumentierungsprofiler zurückgegebenen Rohzahlen beantworten die Budgetierungsfragen jedoch nicht genau. Dies liegt daran, dass die Grafikpipeline komplexe Entwurfsprobleme hat, z. B. die Anzahl der Komponenten, die arbeiten müssen, die Anzahl der Prozessoren, die steuern, wie die Arbeit zwischen Komponenten fließt, und Optimierungsstrategien, die in der Laufzeit und in einem Treiber implementiert sind, die die Pipeline effizienter gestalten.

### <a name="each-api-call-goes-through-several-components"></a>Jeder API-Aufruf durchläuft mehrere Komponenten.

Jeder Aufruf wird von mehreren Komponenten auf dem Weg von der Anwendung zur Grafikkarte verarbeitet. Betrachten Sie beispielsweise die folgende Rendersequenz, die zwei Aufrufe zum Zeichnen eines einzelnen Dreiecks enthält:


```
SetTexture(...);
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);
```



Das folgende konzeptionelle Diagramm zeigt die verschiedenen Komponenten, durch die die Aufrufe übergeben werden müssen.

![Diagramm der Grafikkomponenten, die API-Aufrufe durchgehen](images/microbenchmarkinstructionflow2.png)

Die Anwendung ruft Direct3D auf, das die Szene steuert, Benutzerinteraktionen verarbeitet und bestimmt, wie das Rendering erfolgt. All diese Arbeit wird in der Rendersequenz angegeben, die mithilfe von Direct3D-API-Aufrufen an die Laufzeit gesendet wird. Die Rendersequenz ist virtuell hardwareunabhängig (d. h., die API-Aufrufe sind hardwareunabhängig, aber eine Anwendung hat Kenntnis darüber, welche Funktionen von einer Grafikkarte unterstützt werden).

Die Runtime konvertiert diese Aufrufe in ein geräteunabhängiges Format. Die Runtime verarbeitet die gesamte Kommunikation zwischen der Anwendung und dem Treiber, sodass eine Anwendung auf mehr als einem kompatiblen Hardwareteil ausgeführt wird (abhängig von den erforderlichen Features). Beim Messen eines Funktionsaufrufs misst ein Instrumentierungsprofiler die Zeit, die er in einer Funktion verbracht hat, sowie die Zeit für die Rückgabe der Funktion. Eine Einschränkung eines Instrumentierungsprofilers ist, dass er weder die Zeit, die ein Treiber zum Senden der resultierenden Arbeit an die Grafikkarte benötigt, noch die Zeit für die Verarbeitung der Arbeit durch die Grafikkarte einbeinhaltet. Anders ausgedrückt: Ein Standardinstrumentierungsprofiler kann nicht die ganze Arbeit zuordnen, die jedem Funktionsaufruf zugeordnet ist.

Der Softwaretreiber verwendet hardwarespezifisches Wissen über die Grafikkarte, um die geräteunabhängigen Befehle in eine Sequenz von Grafikkartenbefehlen zu konvertieren. Treiber können auch die Reihenfolge der Befehle optimieren, die an die Grafikkarte gesendet werden, damit das Rendern auf der Grafikkarte effizient erfolgt. Diese Optimierungen können zu Problemen bei der Profilerstellung führen, da die Menge der ausgeführten Arbeit anscheinend nicht so ist (Sie müssen möglicherweise die Optimierungen verstehen, um sie zu berücksichtigen). Der Treiber gibt die Steuerung in der Regel an die Laufzeit zurück, bevor die Verarbeitung aller Befehle durch die Grafikkarte abgeschlossen ist.

Die Grafikkarte führt den Großteil des Renderings aus, indem Daten aus den Scheitelpunkt- und Indexpuffern, Texturen, Renderzustandsinformationen und den Grafikbefehlen kombiniert werden. Wenn das Rendern der Grafikkarte abgeschlossen ist, ist die arbeit, die aus der Rendersequenz erstellt wurde, abgeschlossen.

Jeder Direct3D-API-Aufruf muss von jeder Komponente (Laufzeit, Treiber und Grafikkarte) verarbeitet werden, um etwas zu rendern.

### <a name="there-is-more-than-one-processor-controlling-the-components"></a>Es gibt mehrere Prozessoren, die die Komponenten steuern.

Die Beziehung zwischen diesen Komponenten ist noch komplexer, da die Anwendung, die Runtime und der Treiber von einem Prozessor gesteuert werden und die Grafikkarte von einem separaten Prozessor gesteuert wird. Das folgende Diagramm zeigt zwei Arten von Prozessoren: eine zentrale Verarbeitungseinheit (CPU) und eine Grafikprozessor (GRAPHICS Processing Unit, GPU).

![Diagramm einer CPU und einer GPU und ihrer Komponenten](images/microbenchmarkprocessors.png)

PC-Systeme verfügen über mindestens eine CPU und eine GPU, können aber über mehrere oder beides verfügen. Die CPUs befinden sich auf der Hauptplatine, und die GPUs befinden sich entweder auf der Hauptplatine oder auf der Grafikkarte. Die Geschwindigkeit der CPU wird durch einen Uhrchip auf der Hauptplatine bestimmt, und die Geschwindigkeit der GPU wird durch einen separaten Uhrchip bestimmt. Die CPU-Uhr steuert die Geschwindigkeit der Arbeit, die von der Anwendung, der Runtime und dem Treiber ausgeführt wird. Die Anwendung sendet Arbeit über die Runtime und den Treiber an die GPU.

CPU und GPU werden in der Regel unabhängig voneinander mit unterschiedlichen Geschwindigkeiten ausgeführt. Die GPU kann auf die Arbeit reagieren, sobald die Arbeit verfügbar ist (vorausgesetzt, die GPU hat die Verarbeitung der vorherigen Arbeit abgeschlossen). Die GPU-Arbeit erfolgt parallel zur CPU-Arbeit, wie durch die gekrümmte Linie in der obigen Abbildung hervorgehoben. Ein Profiler misst im Allgemeinen die Leistung der CPU, nicht der GPU. Dies macht die Profilerstellung schwierig, da die von einem Instrumentierungsprofiler durchgeführten Messungen die CPU-Zeit, aber möglicherweise nicht die GPU-Zeit enthalten.

Der Zweck der GPU besteht in der Auslastung der Verarbeitung von der CPU zu einem Prozessor, der speziell für Grafikarbeiten entwickelt wurde. Auf modernen Grafikkarten ersetzt die GPU einen Großen Teil der Transformations- und Beleuchtungsarbeiten in der Pipeline von der CPU zur GPU. Dadurch wird die CPU-Workload erheblich reduziert, und es stehen mehr CPU-Zyklen für andere Verarbeitungen zur Verfügung. Um eine grafische Anwendung auf Spitzenleistung zu optimieren, müssen Sie die Leistung sowohl der CPU als auch der GPU messen und die Arbeit zwischen den beiden Prozessortypen ausgleichen.

In diesem Dokument werden keine Themen behandelt, die sich auf das Messen der Leistung der GPU oder das Ausgleichen der Arbeit zwischen CPU und GPU bezieht. Wenn Sie die Leistung einer GPU (oder einer bestimmten Grafikkarte) besser verstehen möchten, besuchen Sie die Website des Anbieters, um weitere Informationen zur GPU-Leistung zu erhalten. Stattdessen konzentriert sich dieses Dokument auf die Arbeit der Runtime und des Treibers, indem die GPU-Arbeit auf einen vernachlässigbaren Betrag reduziert wird. Dies basiert zum Teil auf der Erfahrung, dass Anwendungen, bei denen Leistungsprobleme auftreten, in der Regel CPU-eingeschränkt sind.

### <a name="runtime-and-driver-optimizations-can-mask-api-measurements"></a>Laufzeit- und Treiberoptimierungen können API-Messungen maskieren

Die Laufzeit verfügt über eine integrierte Leistungsoptimierung, die die Messung eines einzelnen Aufrufs überlasten kann. Hier ist ein Beispielszenario, das dieses Problem veranschaulicht. Betrachten Sie die folgende Rendersequenz:


```
  BeginScene();
    ...
    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);
    ...
  EndScene();
  Present();
```



Beispiel 1: Einfache Rendersequenz

Wenn sie sich die Ergebnisse für die beiden Aufrufe in der Rendersequenz anzeigen, könnte ein Instrumentierungsprofiler Ähnliches zurückgeben:


```
Number of cycles for SetTexture       : 100
Number of cycles for DrawPrimitive    : 950,500
```



Der Profiler gibt die Anzahl der CPU-Zyklen zurück, die zum Verarbeiten der mit jedem Aufruf verbundenen Arbeit erforderlich sind (denken Sie daran, dass die GPU in diesen Zahlen nicht enthalten ist, da die GPU noch nicht mit der Arbeit an diesen Befehlen begonnen hat). Da [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) fast eine Million Zyklen verarbeiten musste, könnten Sie daraus schließen, dass es nicht sehr effizient ist. Sie werden jedoch bald sehen, warum diese Schlussfolgerung falsch ist und wie Sie Ergebnisse generieren können, die für die Budgetierung verwendet werden können.

### <a name="measuring-state-changes-requires-careful-render-sequences"></a>Zum Messen von Zustandsänderungen sind sorgfältige Rendersequenzen erforderlich.

Alle Aufrufe mit Ausnahme von [**IDirect3DDevice9::D rawPrimitive,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)oder [**Clear**](/windows/desktop/api) (z. B. [**SetTexture,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) [**SetVertexDeclaration**](/windows/desktop/api)und [**SetRenderState)**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)erzeugen eine Zustandsänderung. Jede Zustandsänderung legt den Pipelinezustand fest, der steuert, wie das Rendering erfolgt.

Optimierungen in der Laufzeit und/oder im Treiber wurden entwickelt, um das Rendering zu beschleunigen, indem die erforderliche Arbeitsmenge reduziert wird. Im Folgenden finden Sie einige Optimierungen der Zustandsänderung, die möglicherweise zu Profildurchschnitten führen:

-   Ein Treiber (oder die Runtime) könnte eine Zustandsänderung als lokalen Zustand speichern. Da der Treiber in einem "verzögerten" Algorithmus arbeiten könnte (arbeitsverzögerungsversetzt, bis es absolut notwendig ist), kann sich die Arbeit im Zusammenhang mit einigen Zustandsänderungen verzögern.
-   Die Runtime (oder ein Treiber) kann Zustandsänderungen durch Optimierung entfernen. Ein Beispiel hierfür ist das Entfernen einer redundanten Zustandsänderung, die die Beleuchtung deaktiviert, da die Beleuchtung zuvor deaktiviert wurde.

Es gibt keine versäumte Möglichkeit, eine Rendersequenz zu betrachten und zu schließen, welche Zustandsänderungen ein dirty bit festlegen und die Arbeit zurückschlagen oder einfach durch Optimierung entfernt werden. Selbst wenn Sie optimierte Zustandsänderungen in der heutigen Laufzeit oder im Treiber identifizieren könnten, wird die Runtime oder der Treiber von morgen wahrscheinlich aktualisiert. Sie wissen auch nicht sofort, was der vorherige Zustand war. Daher ist es schwierig, redundante Zustandsänderungen zu identifizieren. Die einzige Möglichkeit, die Kosten einer Zustandsänderung zu überprüfen, besteht darin, die Rendersequenz zu messen, die die Zustandsänderungen enthält.

Wie Sie sehen können, erschweren die Schwierigkeiten, die durch mehrere Prozessoren verursacht werden, befehle, die von mehr als einer Komponente verarbeitet werden, und die in die Komponenten integrierten Optimierungen die Profilerstellung schwierig vorherzusagen. Im nächsten Abschnitt werden diese Profilerstellungs-Herausforderungen behandelt. Es werden Direct3D-Beispielrenderingsequenzen mit den zugehörigen Messtechniken gezeigt. Mit diesem Wissen können Sie genaue, wiederholbare Messungen für einzelne Aufrufe generieren.

## <a name="how-to-accurately-profile-a-direct3d-render-sequence"></a>Genaues Profilieren einer Direct3D-Rendersequenz

Nachdem einige der Herausforderungen bei der Profilerstellung hervorgehoben wurden, werden in diesem Abschnitt Techniken gezeigt, mit denen Sie Profilmessungen generieren können, die für die Budgetierung verwendet werden können. Genaue, wiederholbare Profilerstellungsmessungen sind möglich, wenn Sie die Beziehung zwischen den von der CPU gesteuerten Komponenten verstehen und wie Leistungsoptimierungen vermieden werden, die von der Laufzeit und dem Treiber implementiert werden.

Zunächst müssen Sie in der Lage sein, die Ausführungszeit eines einzelnen API-Aufrufs genau zu messen.

### <a name="pick-an-accurate-measurement-tool-like-queryperformancecounter"></a>Auswählen eines genauen Messungstools wie QueryPerformanceCounter

Das Microsoft Windows-Betriebssystem enthält einen Zeitgeber mit hoher Auflösung, der verwendet werden kann, um verstrichene Zeiten mit hoher Auflösung zu messen. Der aktuelle Wert eines solchen Timers kann mit [**queryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)zurückgegeben werden. Nach dem Aufrufen von **QueryPerformanceCounter** zum Zurückgeben von Start- und Beendigungswerten kann der Unterschied zwischen den beiden Werten mit **queryPerformanceCounter** in die tatsächlich verstrichene Zeit (in Sekunden) konvertiert werden.

Die Verwendung von [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) hat den Vorteil, dass es in Windows verfügbar und einfach zu verwenden ist. Umschlossen Sie die Aufrufe einfach mit einem **QueryPerformanceCounter-Aufruf,** und speichern Sie die Start- und Stoppwerte. Daher wird in diesem Dokument veranschaulicht, wie **Sie QueryPerformanceCounter** verwenden, um Die Ausführungszeiten zu profilieren, ähnlich wie ein Instrumentierungsprofiler dies messen würde. Hier sehen Sie ein Beispiel, das zeigt, wie **Sie QueryPerformanceCounter** in Ihren Quellcode einbetten:


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



Beispiel 2: Benutzerdefinierte Profilerstellungsimplementierung mit QPC

start und stop sind zwei große ganze Zahlen, die die start- und stop-Werte enthalten, die vom Hochleistungstimer zurückgegeben werden. Beachten Sie, dass QueryPerformanceCounter(&start) direkt vor [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) und QueryPerformanceCounter(&stop) direkt nach [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)aufgerufen wird. Nach dem Abrufen des Stoppwerts wird QueryPerformanceFrequency aufgerufen, um freq zurückzugeben. Dies ist die Häufigkeit des Zeitgebers mit hoher Auflösung. Angenommen, Sie erhalten in diesem hypothetischen Beispiel die folgenden Ergebnisse für start, stop und freq:



| Lokale Variable | Anzahl von Ticks |
|----------------|-----------------|
| start          | 1792998845094   |
| stop           | 1792998845102   |
| Freq           | 3579545         |



 

Sie können diese Werte wie folgt in die Anzahl der Zyklen konvertieren, die zum Ausführen der API-Aufrufe benötigt werden:


```
# ticks = (stop - start) = 1792998845102 - 1792998845094 = 8 ticks

# cycles = CPU speed * number of ticks / QPF
# 4568   = 2 GHz      * 8              / 3,579,545
```



Anders ausgedrückt: Die Verarbeitung von [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) und [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) auf diesem Computer mit 2 GHz dauert etwa 4568 Taktzyklen. Sie können diese Werte in die tatsächliche Zeit konvertieren, die zum Ausführen aller Aufrufe wie folgt gedauert hat:


```
(stop - start)/ freq = elapsed time
8 ticks / 3,579,545 = 2.2E-6 seconds or between 2 and 3 microseconds.
```



Die Verwendung von QueryPerformanceCounter erfordert, dass Sie Ihrer Rendersequenz Start- und Stoppmessungen hinzufügen und QueryPerformanceFrequency verwenden, um die Differenz (Anzahl von Ticks) in die Anzahl der CPU-Zyklen oder in die tatsächliche Zeit zu konvertieren. Die Identifizierung der Messtechnik ist ein guter Ausgangspunkt für die Entwicklung einer benutzerdefinierten Profilerstellungsimplementierung. Aber bevor Sie beginnen, Messungen vorzunehmen, müssen Sie wissen, wie Sie mit der Grafikkarte umgehen müssen.

### <a name="focus-on-cpu-measurements"></a>Fokus auf CPU-Messungen

Wie bereits erwähnt, funktionieren die CPU und die GPU parallel, um die von den API-Aufrufen generierten Arbeiten zu verarbeiten. Eine reale Anwendung erfordert die Profilerstellung für beide Arten von Prozessoren, um herauszufinden, ob Ihre Anwendung cpu- oder GPU-eingeschränkt ist. Da die GPU-Leistung herstellerspezifisch ist, wäre es sehr schwierig, in diesem Dokument Ergebnisse zu erzeugen, die die Vielzahl der verfügbaren Grafikkarten abdecken.

Stattdessen konzentriert sich dieses Dokument nur auf die Profilerstellung der von der CPU ausgeführten Arbeit mithilfe eines benutzerdefinierten Verfahrens zum Messen der Laufzeit- und Treiberarbeit. Die GPU-Arbeit wird auf einen nicht signifikanten Betrag reduziert, sodass die CPU-Ergebnisse sichtbarer sind. Ein Vorteil dieses Ansatzes besteht darin, dass diese Technik Ergebnisse im Anhang liefert, die Sie mit Ihren Messungen korrelieren können sollten. Um die für die Grafikkarte erforderliche Arbeit auf eine unwichtige Ebene zu reduzieren, reduzieren Sie die Renderingarbeit einfach so gering wie möglich. Dies kann erreicht werden, indem Zeichnen-Aufrufe zum Rendern eines einzelnen Dreiecks eingeschränkt werden, und kann weiter eingeschränkt werden, sodass jedes Dreieck nur ein Pixel enthält.

Die Maßeinheit, die in diesem Dokument zum Messen der CPU-Arbeit verwendet wird, ist die Anzahl der CPU-Taktzyklen und nicht die tatsächliche Zeit. CPU-Taktzyklen haben den Vorteil, dass sie portierbarer (für ANWENDUNGEN mit CPU-Begrenzung) als die tatsächlich verstrichene Zeit auf Computern mit unterschiedlichen CPU-Geschwindigkeiten ist. Dies kann bei Bedarf problemlos in die tatsächliche Zeit konvertiert werden.

Dieses Dokument behandelt keine Themen im Zusammenhang mit dem Lastenausgleich zwischen CPU und GPU. Beachten Sie, dass das Ziel dieses Whitepapers nicht darin besteht, die Gesamtleistung einer Anwendung zu messen, sondern ihnen zu zeigen, wie Sie die Zeit, die die Laufzeit und der Treiber zum Verarbeiten von API-Aufrufen benötigt, genau messen können. Mit diesen genauen Messungen können Sie die Budgetierung der CPU übernehmen, um bestimmte Leistungsszenarien zu verstehen.

### <a name="controlling-runtime-and-driver-optimizations"></a>Steuern von Laufzeit- und Treiberoptimierungen

Mit einer identifizierten Messtechnik und einer Strategie zum Reduzieren der GPU-Arbeit besteht der nächste Schritt darin, die Laufzeit- und Treiberoptimierungen zu verstehen, die bei der Profilerstellung im Weg stehen.

Die CPU-Arbeit kann in drei Buckets unterteilt werden: die Anwendungsarbeit, die Laufzeitarbeit und die Treiberarbeit. Ignorieren Sie die Anwendungsarbeit, da diese vom Programmierer gesteuert wird. Aus Sicht der Anwendung sind die Runtime und der Treiber wie Blackboxen, da die Anwendung keine Kontrolle darüber hat, was in ihnen implementiert ist. Der Schlüssel besteht darin, die Optimierungstechniken zu verstehen, die in der Laufzeit und im Treiber implementiert werden können. Wenn Sie diese Optimierungen nicht verstehen, ist es sehr einfach, auf der Grundlage der Profilmessungen zu der falschen Schlussfolgerung über den Arbeitsaufwand der CPU zu springen. Insbesondere gibt es zwei Themen, die sich auf etwas beziehen, das als Befehlspuffer bezeichnet wird, und was es tun kann, um die Profilerstellung zu verschleiern. Diese Themen sind:

-   Laufzeitoptimierung mit dem Befehlspuffer. Der Befehlspuffer ist eine Laufzeitoptimierung, die die Auswirkungen eines Modusübergangs reduziert. Informationen zum Steuern der zeitlichen Steuerung des Modusübergangs finden Sie unter [Steuern des Befehlspuffers.](#controlling-the-command-buffer)
-   Negieren der Zeitsteuerungseffekte des Befehlspuffers. Die verstrichene Zeit eines Modusübergangs kann große Auswirkungen auf Profilerstellungsmessungen haben. Die Strategie hierfür besteht darin, [die Rendersequenz im Vergleich zum Modusübergang groß zu machen.](#make-the-render-sequence-large-compared-to-the-mode-transition)

### <a name="controlling-the-command-buffer"></a>Steuern des Befehlspuffers

Wenn eine Anwendung einen API-Aufruf vornimmt, konvertiert die Runtime den API-Aufruf in ein geräteunabhängiges Format (das wir einen Befehl aufrufen) und speichert ihn im Befehlspuffer. Der Befehlspuffer wird dem folgenden Diagramm hinzugefügt.

![Diagramm der CPU-Komponenten, einschließlich eines Befehlspuffers](images/microbenchmarkcommandbuffer2.png)

Jedes Mal, wenn die Anwendung einen weiteren API-Aufruf vornimmt, wiederholt die Laufzeit diese Sequenz und fügt dem Befehlspuffer einen weiteren Befehl hinzu. Zu einem bestimmten Zeitpunkt leert die Laufzeit den Puffer (die Befehle werden an den Treiber gesendet). In Windows XP führt das Leeren des Befehlspuffers zu einem Modusübergang, während das Betriebssystem von der Laufzeit (im Benutzermodus ausgeführt) zum Treiber (im Kernelmodus ausgeführt) wechselt, wie im folgenden Diagramm dargestellt.

-   Benutzermodus: Der nicht privilegierte Prozessormodus, der Anwendungscode ausführt. Anwendungen im Benutzermodus können nur über Systemdienste auf Systemdaten zugreifen.
-   Kernelmodus: Der privilegierte Prozessormodus, in dem Windows-basierter Executive-Code ausgeführt wird. Ein Treiber oder Thread, der im Kernelmodus ausgeführt wird, hat Zugriff auf den gesamten Systemspeicher, direkten Zugriff auf Hardware und die CPU-Anweisungen zum Ausführen von E/A-Läufen mit der Hardware.

![Diagramm der Übergänge zwischen Benutzermodus und Kernelmodus](images/microbenchmarkcommandbuffer3.png)

Der Übergang erfolgt jedes Mal, wenn die CPU vom Benutzer in den Kernelmodus wechselt (und umgekehrt), und die Anzahl der benötigten Zyklen ist im Vergleich zu einem einzelnen API-Aufruf groß. Wenn die Laufzeit jeden API-Aufruf an den Treiber gesendet hat, als er aufgerufen wurde, würde jeder API-Aufruf die Kosten eines Modusübergangs verursachen.

Stattdessen ist der Befehlspuffer eine Laufzeitoptimierung, die entwickelt wurde, um die effektiven Kosten des Modusübergangs zu reduzieren. Der Befehl puffert viele Treiberbefehle in die Warteschlange, um einen Übergang im Einzelmodus vorzubereiten. Wenn die Laufzeit dem Befehlspuffer einen Befehl hinzufügt, wird die Steuerung an die Anwendung zurückgegeben. Ein Profiler kann nicht wissen, dass die Treiberbefehle wahrscheinlich noch nicht einmal an den Treiber gesendet wurden. Daher sind die zahlen, die von einem standardbasierten Instrumentierungsprofiler zurückgegeben werden, irreführend, da er die Laufzeitarbeit, aber nicht die zugehörige Treiberarbeit misst.

### <a name="profile-results-without-a-mode-transition"></a>Profilergebnisse ohne Modusübergang

Mithilfe der Rendersequenz aus Beispiel 2 finden Sie hier einige typische Zeitmessungsmessungen, die die Größe eines Modusübergangs veranschaulichen. Unter der Annahme, dass [**SetTexture-**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) und [**DrawPrimitive-Aufrufe**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) keinen Modusübergang verursachen, könnte ein standardbasierter Instrumentierungsprofiler Ergebnisse ähnlich den folgenden zurückgeben:


```
Number of cycles for SetTexture           : 100
Number of cycles for DrawPrimitive        : 900
```



Jede dieser Zahlen ist die Zeitspanne, die die Laufzeit benötigt, um diese Aufrufe dem Befehlspuffer hinzuzufügen. Da es keinen Modusübergang gibt, hat der Treiber noch keine Arbeit ausgeführt. Die Profilerergebnisse sind genau, messen jedoch nicht die gesamte Arbeit, die die Rendersequenz letztendlich dazu führt, dass die CPU ausgeführt wird.

### <a name="profile-results-with-a-mode-transition"></a>Profilergebnisse mit einem Modusübergang

Sehen Sie sich nun an, was für das gleiche Beispiel geschieht, wenn ein Modusübergang auftritt. Dieses Mal wird davon ausgegangen, dass [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) und [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) einen Modusübergang verursachen. Auch hier könnte ein Standardinstrumentierungsprofiler Ergebnisse ähnlich den folgenden zurückgeben:


```
Number of cycles for SetTexture           : 98 
Number of cycles for DrawPrimitive        : 946,900
```



Die für [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) gemessene Zeit ist in etwa gleich, aber der drastische Anstieg der Zeit in [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) ist auf den Modusübergang zurückzuführen. Dies geschieht:

1.  Angenommen, der Befehlspuffer verfügt über Platz für einen Befehl, bevor die Rendersequenz gestartet wird.
2.  [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) wird in ein geräteunabhängiges Format konvertiert und dem Befehlspuffer hinzugefügt. In diesem Szenario füllt dieser Aufruf den Befehlspuffer aus.
3.  Die Runtime versucht, [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) zum Befehlspuffer hinzuzufügen, kann dies jedoch nicht, da sie voll ist. Stattdessen leert die Laufzeit den Befehlspuffer. Dies führt zum Übergang des Kernelmodus. Angenommen, der Übergang dauert etwa 5.000 Zyklen. Diese Zeit trägt zur Zeit bei, die in **DrawPrimitive** aufgewendet wird.
4.  Der Treiber verarbeitet dann die Arbeit, die allen Befehlen zugeordnet ist, die aus dem Befehlspuffer geleert wurden. Angenommen, die Treiberzeit zum Verarbeiten der Befehle, die den Befehlspuffer fast gefüllt haben, beträgt etwa 935.000 Zyklen. Angenommen, die mit [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) verknüpfte Treiberarbeit beträgt etwa 2750 Zyklen. Diese Zeit trägt zur Zeit bei, die in [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)aufgewendet wird.
5.  Wenn der Treiber seine Arbeit beendet, gibt der Benutzermodusübergang die Steuerung an die Laufzeit zurück. Der Befehlspuffer ist jetzt leer. Angenommen, der Übergang dauert etwa 5.000 Zyklen.
6.  Die Rendersequenz wird abgeschlossen, indem [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) konvertiert und dem Befehlspuffer hinzugefügt wird. Angenommen, dies dauert etwa 900 Zyklen. Diese Zeit trägt zur Zeit bei, die in **DrawPrimitive** aufgewendet wird.

Wenn Sie die Ergebnisse zusammenfassen, sehen Sie Folgendes:


```
DrawPrimitive = kernel-transition + driver work    + user-transition + runtime work
DrawPrimitive = 5000              + 935,000 + 2750 + 5000            + 900
DrawPrimitive = 947,950  
```



Genau wie die Messung für [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) ohne Modusübergang (900 Zyklen) ist die Messung für **DrawPrimitive** mit dem Modusübergang (947.950 Zyklen) genau, aber im Hinblick auf die Budgetierung der CPU-Arbeit unbrauchbar. Das Ergebnis enthält die richtige Laufzeitarbeit, der Treiber funktioniert für [**SetTexture,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)der Treiber funktioniert für alle Befehle, die **SetTexture** vorangestellt sind, und zwei Modusübergänge. Der Messung fehlt jedoch die **DrawPrimitive-Treiberarbeit.**

Ein Modusübergang kann als Reaktion auf jeden Aufruf erfolgen. Dies hängt davon ab, was sich zuvor im Befehlspuffer befand. Sie müssen den Modusübergang steuern, um zu verstehen, wie viel CPU-Arbeit (Laufzeit und Treiber) jedem Aufruf zugeordnet ist. Dazu benötigen Sie einen Mechanismus zum Steuern des Befehlspuffers und des Zeitlichen Ablaufs des Modusübergangs.

### <a name="the-query-mechanism"></a>Der Abfragemechanismus

Der Abfragemechanismus in Microsoft Direct3D 9 wurde so konzipiert, dass die Runtime die GPU nach Fortschritt abfragen und bestimmte Daten von der GPU zurückgeben kann. Wenn die GPU-Arbeit während der Profilerstellung minimiert wird, sodass sie eine vernachlässigbare Auswirkung auf die Leistung hat, können Sie den Status von der GPU zurückgeben, um die Leistung des Treibers zu messen. Schließlich ist die Treiberarbeit abgeschlossen, wenn die GPU die Treiberbefehle gesehen hat. Darüber hinaus kann der Abfragemechanismus in zwei Für die Profilerstellung wichtige Befehlspuffermerkmale gesteuert werden: wenn der Befehlspuffer geleert wird und wie viel Arbeit im Puffer erfolgt.

Dies ist die gleiche Rendersequenz mithilfe des Abfragemechanismus:


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



Beispiel 3: Verwenden einer Abfrage zum Steuern des Befehlspuffers

Im Folgenden finden Sie eine ausführlichere Erläuterung der einzelnen Codezeilen:

1.  Erstellen Sie eine Ereignisabfrage, indem Sie ein Abfrageobjekt mit D3DQUERYTYPE \_ EVENT erstellen.
2.  Fügen Sie dem Befehlspuffer einen Abfrageereignismarker hinzu, indem Sie [**Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)aufrufen ([**D3DISSUE \_ END**](d3dissue-end.md)). Dieser Marker weist den Treiber an, nachzuverfolgen, wann die GPU die Ausführung der Befehle vor dem Marker abgeschlossen hat.
3.  Der erste Aufruf leert den Befehlspuffer, da der Aufruf von [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) mit [**D3DGETDATA \_ FLUSH**](d3dgetdata-flush.md) erzwingt, dass der Befehlspuffer geleert wird. Bei jedem nachfolgenden Aufruf wird die GPU überprüft, um festzustellen, wann die Verarbeitung der gesamten Befehlspufferarbeit abgeschlossen ist. Diese Schleife gibt S OK erst zurück, \_ wenn sich die GPU im Leerlauf befindet.
4.  Beispiel für die Startzeit.
5.  Rufen Sie die API-Aufrufe auf, für die ein Profil erstellt wird.
6.  Fügen Sie dem Befehlspuffer einen zweiten Abfrageereignismarker hinzu. Dieser Marker wird verwendet, um den Abschluss der Aufrufe nachzuverfolgen.
7.  Der erste Aufruf leert den Befehlspuffer, da der Aufruf von [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) mit [**D3DGETDATA \_ FLUSH**](d3dgetdata-flush.md) erzwingt, dass der Befehlspuffer geleert wird. Wenn die GPU die Verarbeitung der gesamten Befehlspufferarbeit abgeschlossen hat, gibt **GetData** S \_ OK zurück, und die Schleife wird beendet, da sich die GPU im Leerlauf befindet.
8.  Probieren Sie die Beendigungszeit aus.

Dies sind die Ergebnisse, die mit QueryPerformanceCounter und QueryPerformanceFrequency gemessen werden:



| Lokale Variable | Anzahl von Ticks |
|----------------|-----------------|
| start          | 1792998845060   |
| stop           | 1792998845090   |
| Freq           | 3579545         |



 

Erneutes Konvertieren von Ticks in Zyklen (auf einem Computer mit 2 GHz):


```
# ticks  = (stop - start) = 1792998845090 - 1792998845060 = 30 ticks
# cycles = CPU speed * number of ticks / QPF
# 16,450 = 2 GHz      * 30             / 3,579,545
```



Hier ist die Aufschlüsselung der Anzahl von Zyklen pro Aufruf:


```
Number of cycles for SetTexture           : 100
Number of cycles for DrawPrimitive        : 900
Number of cycles for Issue                : 200
Number of cycles for GetData              : 16,450
```



Der Abfragemechanismus hat es uns ermöglicht, die Laufzeit und die zu messende Treiberarbeit zu steuern. Um diese Zahlen zu verstehen, geschieht folgendermaßen die Reaktion auf die einzelnen API-Aufrufe sowie die geschätzten Zeitangaben:

1.  Beim ersten Aufruf wird der Befehlspuffer geleert, indem [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) mit [**D3DGETDATA \_ FLUSH**](d3dgetdata-flush.md)aufgerufen wird. Wenn die GPU die Verarbeitung der gesamten Befehlspufferarbeit abgeschlossen hat, gibt **GetData** S \_ OK zurück, und die Schleife wird beendet, da sich die GPU im Leerlauf befindet.
2.  Die Rendersequenz beginnt, indem [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) in ein geräteunabhängiges Format konvertiert und dem Befehlspuffer hinzugefügt wird. Angenommen, dies dauert etwa 100 Zyklen.
3.  [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) wird konvertiert und dem Befehlspuffer hinzugefügt. Angenommen, dies dauert etwa 900 Zyklen.
4.  [**Problem**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) fügt dem Befehlspuffer einen Abfragemarker hinzu. Angenommen, dies dauert etwa 200 Zyklen.
5.  [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) bewirkt, dass der Befehlspuffer geleert wird, wodurch der Übergang des Kernelmodus erzwingt wird. Angenommen, dies dauert etwa 5.000 Zyklen.
6.  Der Treiber verarbeitet dann die Arbeit, die allen vier Aufrufen zugeordnet ist. Angenommen, die Treiberzeit für die Verarbeitung von [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) beträgt etwa 2964 Zyklen, [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) ca. 3.600 Zyklen, [**Problem**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) ca. 200 Zyklen. Die Gesamte Treiberzeit für alle vier Befehle beträgt also etwa 6450 Zyklen.
    > [!Note]  
    > Der Treiber benötigt auch etwas Zeit, um den Status der GPU zu sehen. Da die GPU-Arbeit trivial ist, sollte die GPU bereits ausgeführt werden. [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) gibt S \_ OK basierend auf der Wahrscheinlichkeit zurück, dass die GPU abgeschlossen ist.

     

7.  Wenn der Treiber seine Arbeit beendet, gibt der Benutzermodusübergang die Steuerung an die Laufzeit zurück. Der Befehlspuffer ist jetzt leer. Angenommen, dies dauert etwa 5.000 Zyklen.

Die Zahlen für [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) umfassen Folgendes:


```
GetData = kernel-transition + driver work + user-transition
GetData = 5000              + 6450        + 5000           
GetData = 16,450  

driver work = SetTexture + DrawPrimitive + Issue = 
driver work = 2964       + 3600          + 200   = 6450 cycles 
```



Der in Kombination mit QueryPerformanceCounter verwendete Abfragemechanismus misst die gesamte CPU-Arbeit. Dies erfolgt mit einer Kombination aus Abfragemarkern und Abfragestatusvergleichen. Abfragemarker zum Starten und Beenden, die dem Befehlspuffer hinzugefügt werden, werden verwendet, um zu steuern, wie viel Arbeit im Puffer erfolgt. Indem gewartet wird, bis der richtige Rückgabecode zurückgegeben wird, wird die Startmessung direkt vor dem Start einer sauberen Rendersequenz durchgeführt, und die Beendigungsmessung erfolgt unmittelbar nach Abschluss der Arbeit, die dem Inhalt des Befehlspuffers zugeordnet ist. Dies erfasst effektiv die CPU-Arbeit, die sowohl von der Laufzeit als auch vom Treiber ausgeführt wird.

Nachdem Sie nun über den Befehlspuffer und seine Auswirkungen auf die Profilerstellung informiert sind, sollten Sie wissen, dass es einige andere Bedingungen gibt, die dazu führen können, dass die Laufzeit den Befehlspuffer leert. Sie müssen auf diese in Ihren Rendersequenzen achten. Einige dieser Bedingungen sind als Reaktion auf API-Aufrufe, andere als Reaktion auf Ressourcenänderungen in der Runtime. Eine der folgenden Bedingungen führt zu einem Modusübergang:

-   Wenn eine der Sperrmethoden ([**Sperren**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock)) für einen Scheitelpunktpuffer, Indexpuffer oder eine Textur aufgerufen wird (unter bestimmten Bedingungen mit bestimmten Flags).
-   Wenn ein Geräte- oder Scheitelpunktpuffer, ein Indexpuffer oder eine Textur erstellt wird.
-   Wenn ein Geräte- oder Scheitelpunktpuffer, Indexpuffer oder eine Textur durch das letzte Release zerstört wird.
-   Wenn [**ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) aufgerufen wird.
-   Wenn [**Vorhanden**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) aufgerufen wird.
-   Wenn der Befehlspuffer voll ist.
-   Wenn [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) mit D3DGETDATA FLUSH aufgerufen \_ wird.

Achten Sie darauf, dass Sie in Ihren Rendersequenzen auf diese Bedingungen achten. Jedes Mal, wenn ein Modusübergang hinzugefügt wird, werden Ihren Profilerstellungsmessungen 10.000 Arbeitszyklen des Treibers hinzugefügt. Darüber hinaus ist der Befehlspuffer nicht statisch dimensioniert. Die Laufzeit kann die Größe des Puffers als Reaktion auf den Arbeitsaufwand ändern, der von der Anwendung generiert wird. Dies ist eine weitere Optimierung, die von einer Rendersequenz abhängig ist.

Achten Sie daher darauf, die Übergänge im Modus während der Profilerstellung zu steuern. Der Abfragemechanismus bietet eine stabile Methode zum Leeren des Befehlspuffers, sodass Sie die Zeitliche Steuerung des Modusübergangs sowie die Menge an Arbeit, die der Puffer enthält, steuern können. Allerdings kann auch diese Technik verbessert werden, indem die Modusübergangszeit reduziert wird, um sie in Bezug auf das gemessene Ergebnis unwichtig zu machen.

### <a name="make-the-render-sequence-large-compared-to-the-mode-transition"></a>Rendersequenz im Vergleich zum Modusübergang groß machen

Im vorherigen Beispiel verbrauchen der Kernelmodusschalter und der Benutzermodusschalter etwa 10.000 Zyklen, die nichts mit der Laufzeit- und Treiberarbeit zu tun haben. Da der Modusübergang in das Betriebssystem integriert ist, kann er nicht auf 0 (null) reduziert werden. Damit der Modusübergang nicht signifikant ist, muss die Rendersequenz so angepasst werden, dass der Treiber und die Laufzeitarbeit um eine Größenordnung größer sind als die Moduswechsel. Sie könnten versuchen, eine Subtraktion zu unternehmen, um die Übergänge zu entfernen, aber die Amortisierung der Kosten für eine viel höhere Kosten für die Rendersequenz ist zuverlässiger.

Die Strategie zum Reduzieren des Modusübergangs, bis er unwichtig wird, besteht im Hinzufügen einer Schleife zur Rendersequenz. Sehen wir uns beispielsweise die Profilerstellungsergebnisse an, wenn eine Schleife hinzugefügt wird, die die Rendersequenz 1500 Mal wiederholt:


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



Beispiel 4: Hinzufügen einer Schleife zur Rendersequenz

Dies sind die Ergebnisse, die mit QueryPerformanceCounter und QueryPerformanceFrequency gemessen werden:



| Lokale Variable | Anzahl der Tics |
|----------------|----------------|
| start          | 1792998845000  |
| stop           | 1792998847084  |
| Freq           | 3579545        |



 

Die Verwendung von QueryPerformanceCounter misst jetzt 2.840 Ticks. Das Konvertieren von Ticks in Zyklen ist identisch mit dem, was wir bereits gezeigt haben:


```
# ticks  = (stop - start) = 1792998847084 - 1792998845000 = 2840 ticks
# cycles    = machine speed * number of ticks / QPF
# 6,900,000 = 2 GHz          * 2840           / 3,579,545
```



Anders ausgedrückt: Auf diesem 2-GHz-Computer dauert es etwa 6,9 Millionen Zyklen, um die 1.500 Aufrufe in der Renderschleife zu verarbeiten. Von den 6,9 Millionen Zyklen beträgt die Zeit in den Modusübergängen ungefähr 10.000, sodass die Profilergebnisse jetzt fast vollständig die Arbeit messen, die [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) und [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)zugeordnet ist.

Beachten Sie, dass das Codebeispiel ein Array von zwei Texturen erfordert. Um eine Laufzeitoptimierung zu vermeiden, die [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) entfernen würde, wenn bei jedem Aufgerufenen derselbe Texturzeiger festgelegt wird, verwenden Sie einfach ein Array aus zwei Texturen. Auf diese Weise ändert sich bei jedem Durchlauf der Schleife der Texturzeiger, und die gesamte Arbeit, die **SetTexture** zugeordnet ist, wird ausgeführt. Stellen Sie sicher, dass beide Texturen die gleiche Größe und das gleiche Format aufweisen, damit sich kein anderer Zustand ändert, wenn die Textur dies tut.

Sie verfügen nun über ein Verfahren für die Profilerstellung für Direct3D. Es basiert auf dem Leistungsindikator (QueryPerformanceCounter), um die Anzahl der Ticks zu erfassen, die die CPU zum Verarbeiten der Arbeit benötigt. Die Arbeit wird sorgfältig so gesteuert, dass sie die Laufzeit- und Treiberarbeit ist, die API-Aufrufen mithilfe des Abfragemechanismus zugeordnet ist. Eine Abfrage bietet zwei Steuerungshilfen: erstens, um den Befehlspuffer zu leeren, bevor die Rendersequenz gestartet wird, und zweitens, um nach Abschluss der GPU-Arbeit zurückzukehren.

Bisher hat dieses Dokument gezeigt, wie sie ein Profil für eine Rendersequenz erstellen. Jede Rendersequenz war recht einfach und enthält einen einzelnen [**DrawPrimitive-Aufruf**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) und einen [**SetTexture-Aufruf.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) Dies wurde durchgeführt, um sich auf den Befehlspuffer und die Verwendung des Abfragemechanismus zu konzentrieren, um ihn zu steuern. Hier ist eine kurze Zusammenfassung des Profils für eine beliebige Rendersequenz:

-   Verwenden Sie einen Leistungsindikator wie QueryPerformanceCounter, um die Zeit zu messen, die zum Verarbeiten der einzelnen API-Aufrufe benötigt wird. Verwenden Sie QueryPerformanceFrequency und die CPU-Taktrate, um dies in die Anzahl der CPU-Zyklen pro API-Aufruf zu konvertieren.
-   Minimieren Sie die GPU-Arbeit, indem Sie Dreieckslisten rendern, wobei jedes Dreieck ein Pixel enthält.
-   Verwenden Sie den Abfragemechanismus, um den Befehlspuffer vor der Rendersequenz zu leeren. Dadurch wird sichergestellt, dass die Profilerstellung die richtige Menge an Laufzeit- und Treiberarbeit erfasst, die der Rendersequenz zugeordnet ist.
-   Steuern Sie die Menge an Arbeit, die dem Befehlspuffer mit Abfrageereignismarkern hinzugefügt wird. Dieselbe Abfrage erkennt, wann die GPU ihre Arbeit abgeschlossen hat. Da die GPU-Arbeit trivial ist, entspricht dies praktisch dem Messen, wann die Arbeit des Treibers abgeschlossen ist.

Alle diese Techniken werden zum Profilieren von Statusänderungen verwendet. Angenommen, Sie haben gelesen und verstanden, wie sie den Befehlspuffer steuern können, und haben die Baselinemessungen für [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)erfolgreich abgeschlossen. Nun können Sie Ihren Rendersequenzen Zustandsänderungen hinzufügen. Beim Hinzufügen von Zustandsänderungen zu einer Rendersequenz gibt es einige zusätzliche Herausforderungen bei der Profilerstellung. Wenn Sie ihren Rendersequenzen Zustandsänderungen hinzufügen möchten, fahren Sie mit dem nächsten Abschnitt fort.

## <a name="profiling-direct3d-state-changes"></a>Profilerstellung für Direct3D-Statusänderungen

Direct3D verwendet viele Renderzustände, um fast jeden Aspekt der Pipeline zu steuern. Zu den APIs, die Zustandsänderungen verursachen, gehören alle Funktionen oder Methoden, die keine Primitive \* zeichnen-Aufrufe sind.

Zustandsänderungen sind schwierig, da Sie die Kosten einer Zustandsänderung ohne Rendering möglicherweise nicht sehen können. Dies ist das Ergebnis des verzögerten Algorithmus, den der Treiber und die GPU verwenden, um die Arbeit so lange zu verzögert, bis sie unbedingt durchgeführt werden muss. Im Allgemeinen sollten Sie die folgenden Schritte ausführen, um eine einzelne Zustandsänderung zu messen:

1.  Erstellen [**Sie zuerst ein Profil für DrawPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)
2.  Fügen Sie der Rendersequenz eine Zustandsänderung hinzu, und erstellen Sie ein Profil für die neue Sequenz.
3.  Subtrahieren Sie die Differenz zwischen den beiden Sequenzen, um die Kosten für die Zustandsänderung zu erhalten.

Natürlich gilt alles, was Sie über die Verwendung des Abfragemechanismus und das Hinzufügen der Rendersequenz in eine Schleife gelernt haben, um die Kosten für den Modusübergang zu negieren.

### <a name="profiling-a-simple-state-change"></a>Profilerstellung für eine einfache Zustandsänderung

Beginnend mit einer Rendersequenz, die [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)enthält, ist hier die Codesequenz zum Messen der Kosten für das Hinzufügen von [**SetTexture:**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)


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



Beispiel 5: Messen eines API-Aufrufs für eine Zustandsänderung

Beachten Sie, dass die Schleife zwei Aufrufe enthält: [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) und [**DrawPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) Die Rendersequenz schleift 1500-mal und generiert ähnliche Ergebnisse wie die folgenden:



| Lokale Variable | Anzahl der Tics |
|----------------|----------------|
| start          | 1792998860000  |
| stop           | 1792998870260  |
| Freq           | 3579545        |



 

Das Konvertieren von Ticks in Zyklen führt erneut zu:


```
# ticks  = (stop - start) = 1792998870260 - 1792998860000 = 10,260 ticks
# cycles    = machine speed * number of ticks / QPF
5,775,000   = 2 GHz          * 10,260         / 3,579,545
```



Die Division durch die Anzahl der Iterationen in der Schleife ergibt:


```
5,775,000 cycles / 1500 iterations = 3850 cycles for one iteration
```



Jede Iteration der Schleife enthält eine Zustandsänderung und einen Zeichnen-Aufruf. Subtrahieren des Ergebnisses der [**DrawPrimitive-Rendersequenz**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) verlässt:


```
3850 - 1100 = 2750 cycles for SetTexture
```



Dies ist die durchschnittliche Anzahl von Zyklen, die [**dieser Rendersequenz SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) hinzugefügt werden soll. Dieses Verfahren kann auch auf andere Zustandsänderungen angewendet werden.

Warum wird [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) als einfache Zustandsänderung bezeichnet? Da der zustandsbeschränkt ist, der festgelegt wird, sodass die Pipeline bei jeder Zustandsänderung die gleiche Arbeitsmenge übernimmt. Wenn Sie beide Texturen auf die gleiche Größe und das gleiche Format beschränken, wird für jeden **SetTexture-Aufruf** die gleiche Menge an Arbeit sichergestellt.

### <a name="profiling-a-state-change-that-needs-to-be-toggled"></a>Profilerstellung für eine Zustandsänderung, die umschaltet werden muss

Es gibt andere Zustandsänderungen, die dazu führen, dass sich die Von der Grafikpipeline ausgeführte Arbeitsmenge für jede Iteration der Renderschleife ändert. Wenn z-Testing beispielsweise aktiviert ist, aktualisiert jede Pixelfarbe ein Renderziel erst, nachdem der z-Wert des neuen Pixels mit dem Z-Wert für das vorhandene Pixel getestet wurde. Wenn z-testing deaktiviert ist, wird dieser Pro-Pixel-Test nicht durchgeführt, und die Ausgabe wird viel schneller geschrieben. Durch das Aktivieren oder Deaktivieren des Z-Test-Zustands wird die Menge an Arbeit (von der CPU und der GPU) während des Renderings erheblich geändert.

[**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) erfordert einen bestimmten Renderzustand und einen Zustandswert, um Z-Tests zu aktivieren oder zu deaktivieren. Der bestimmte Zustandswert wird zur Laufzeit ausgewertet, um zu bestimmen, wie viel Arbeit erforderlich ist. Es ist schwierig, diese Zustandsänderung in einer Renderschleife zu messen und trotzdem den Pipelinezustand vorkonditioniert, sodass er wechselt. Die einzige Lösung besteht im Umschalten der Zustandsänderung während der Rendersequenz.

Beispielsweise muss die Profilerstellungsmethode wie folgt zweimal wiederholt werden:

1.  Erstellen Sie zunächst eine Profilerstellung [**für die DrawPrimitive-Rendersequenz.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) Nennen Sie dies die Baseline.
2.  Erstellen Sie ein Profil für eine zweite Rendersequenz, die die Zustandsänderung umschaltet. Die Rendersequenzschleife enthält:
    -   Eine Zustandsänderung, um den Zustand in eine "false"-Bedingung zu setzen.
    -   [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) genau wie die ursprüngliche Sequenz.
    -   Eine Zustandsänderung, um den Zustand in eine "true"-Bedingung zu setzen.
    -   Eine zweite [**DrawPrimitive,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) um zu erzwingen, dass die zweite Zustandsänderung realisiert wird.
3.  Suchen Sie den Unterschied zwischen den beiden Rendersequenzen. Dies wird wie folgt erreicht:
    -   Multiplizieren Sie die [**DrawPrimitive-Baselinesequenz**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) mit 2, da es zwei **DrawPrimitive-Aufrufe** in der neuen Sequenz gibt.
    -   Subtrahieren Sie das Ergebnis der neuen Sequenz von der ursprünglichen Sequenz.
    -   Dividieren Sie das Ergebnis durch 2, um die durchschnittlichen Kosten für die Statusänderung "false" und "true" zu erhalten.

Bei der in der Rendersequenz verwendeten Schleifentechnik müssen die Kosten für das Ändern des Pipelinezustands gemessen werden, indem der Zustand für jede Iteration in der Rendersequenz von einer "true"-Bedingung in eine "false"-Bedingung und umgekehrt umgekniffen wird. Die Bedeutung von "true" und "false" ist hier nicht literal. Dies bedeutet lediglich, dass der Zustand in gegensätzliche Bedingungen festgelegt werden muss. Dies bewirkt, dass beide Zustandsänderungen während der Profilerstellung gemessen werden. Natürlich gilt weiterhin alles, was Sie über die Verwendung des Abfragemechanismus gelernt haben und die Rendersequenz in eine Schleife setzen, um die Kosten für den Modusübergang zu negieren.

Hier sehen Sie beispielsweise die Codesequenz zum Messen der Kosten für das Ein- oder Ausschalten von Z-Tests:


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



Beispiel 5: Messen einer Änderung des Umbruchzustands

Die -Schleife umschaltet den Zustand, indem zwei [**SetRenderState-Aufrufe ausgeführt**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) werden. Der erste **SetRenderState-Aufruf** deaktiviert z-testing, und der zweite **SetRenderState** aktiviert z-testing. Auf **jeden SetRenderState** folgt [**DrawPrimitive,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) sodass die der Zustandsänderung zugeordnete Arbeit vom Treiber verarbeitet wird, anstatt nur ein dirty bit im Treiber zu setzen.

Diese Zahlen sind für diese Rendersequenz sinnvoll:



| Lokale Variable | Anzahl der Ticks |
|----------------|-----------------|
| start          | 1792998845000   |
| stop           | 1792998861740   |
| Freq           | 3579545         |



 

Das Konvertieren von Ticks in Zyklen führt erneut zu:


```
# ticks  = (stop - start) = 1792998861740 - 1792998845000 = 15,120 ticks
# cycles    = machine speed * number of ticks / QPF
 9,300,000  = 2 GHz          * 16,740         / 3,579,545
```



Die Division durch die Anzahl der Iterationen in der Schleife ergibt:


```
9,300,000 cycles / 1500 iterations = 6200 cycles for one iteration
```



Jede Iteration der Schleife enthält zwei Zustandsänderungen und zwei Zeichnen-Aufrufe. Das Subtrahieren der Zeichnen-Aufrufe (bei 1100 Zyklen) verlässt:


```
6200 - 1100 - 1100 = 4000 cycles for both state changes
```



Dies ist die durchschnittliche Anzahl von Zyklen für beide Zustandsänderungen, sodass die durchschnittliche Zeit für jede Zustandsänderung ist:


```
4000 / 2  = 2000 cycles for each state change
```



Daher beträgt die durchschnittliche Anzahl von Zyklen zum Aktivieren oder Deaktivieren von Z-Tests 2.000 Zyklen. Es ist zu sehen, dass QueryPerformanceCounter z-enable in der Hälfte der Zeit und z-disable die Hälfte der Zeit misst. Diese Technik misst tatsächlich den Durchschnitt beider Zustandsänderungen. Anders ausgedrückt: Sie messen die Zeit zum Umschalten eines Zustands. Mit dieser Technik können Sie nicht wissen, ob die Aktivierungs- und Deaktivierungszeiten gleichwertig sind, da Sie den Durchschnitt beider Werte gemessen haben. Trotzdem ist dies eine sinnvolle Zahl, die beim Budgetieren eines Umbruchzustands als Anwendung verwendet werden muss, die diese Zustandsänderung verursacht. Dies kann nur durch Umbruch dieses Zustands möglich sein.

Nun können Sie diese Techniken anwenden und ein Profil für alle von Ihnen erstellten Zustandsänderungen erstellen, richtig? Das trifft nicht vollständig zu. Sie müssen bei Optimierungen, die darauf ausgelegt sind, die Menge der zu erledigenden Arbeit zu reduzieren, weiterhin vorsichtig sein. Es gibt zwei Arten von Optimierungen, die Sie beim Entwerfen ihrer Rendersequenzen beachten sollten.

### <a name="watch-out-for-state-change-optimizations"></a>Achten Sie auf Zustandsänderungsoptimierungen.

Im vorherigen Abschnitt wird gezeigt, wie Sie ein Profil für beide Arten von Zustandsänderungen erstellen: eine einfache Zustandsänderung, die darauf beschränkt ist, die gleiche Menge an Arbeit für jede Iteration zu generieren, und eine Änderung des Umbruchzustands, die die Menge der durchgeführten Arbeit erheblich ändert. Was geschieht, wenn Sie die vorherige Rendersequenz übernehmen und ihr eine weitere Zustandsänderung hinzufügen? In diesem Beispiel wird beispielsweise die Rendersequenz z> enable verwendet und ihr ein Z-Func-Vergleich hinzufügt:


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



Der Z-Func-Zustand legt die Vergleichsebene beim Schreiben in den Z-Puffer fest (zwischen dem Z-Wert eines aktuellen Pixels mit dem Z-Wert eines Pixels im Tiefenpuffer). D3DCMP \_ deaktiviert nie den Z-Test-Vergleich, während D3DCMP ALWAYS den Vergleich so anschaltet, dass er bei jedem \_ Z-Test erfolgt.

Die Profilerstellung einer dieser Zustandsänderungen in einer Rendersequenz mit [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) generiert ähnliche Ergebnisse wie die folgenden:



| Änderung des Einzelzustands | Durchschnittliche Anzahl von Zyklen |
|---------------------|--------------------------|
| Nur D3DRS \_ ZENABLE | 2000                     |



 

oder



| Änderung des Einzelzustands | Durchschnittliche Anzahl von Zyklen |
|---------------------|--------------------------|
| Nur D3DRS- \_ ODER -DEC-10000000000000   | 600                      |



 

Wenn Sie jedoch sowohl für D3DRS ZENABLE als auch \_ für D3DRSUNKUNC ein Profil in der gleichen Rendersequenz erstellen, können Ergebnisse wie \_ die folgenden angezeigt werden:



| Beide Statusänderungen            | Durchschnittliche Anzahl von Zyklen |
|-------------------------------|--------------------------|
| D3DRS \_ ZENABLE + D3DRSUNKUNC \_ | 2000                     |



 

Sie können davon ausgehen, dass das Ergebnis die Summe von 2000- und 600-Zyklen (oder 2600) ist, da der Treiber alle Mitarbeit im Zusammenhang mit dem Festlegen beider Renderzustände verarbeite. Stattdessen beträgt der Durchschnitt 2.000 Zyklen.

Dieses Ergebnis spiegelt eine Zustandsänderungsoptimierung wider, die in der Runtime, im Treiber oder in der GPU implementiert ist. In diesem Fall könnte der Treiber den ersten [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) sehen und einen dirty-Zustand festlegen, der die Arbeit auf einen späteren Zeitpunkt verschieben würde. Wenn der Treiber den zweiten **SetRenderState** sieht, kann der gleiche dirty-Zustand redundant festgelegt werden, und die gleiche Arbeit würde erneut verschoben werden. Wenn [**DrawPrimitive aufgerufen**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) wird, wird die arbeit, die dem dirty-Zustand zugeordnet ist, schließlich verarbeitet. Der Treiber führt die Arbeit einmal aus, was bedeutet, dass die ersten beiden Zustandsänderungen vom Treiber effektiv konsolidiert werden. Ebenso werden die dritten und vierten Zustandsänderungen vom Treiber effektiv in einer einzelnen Zustandsänderung konsolidiert, wenn die zweite **DrawPrimitive** aufgerufen wird. Das Ergebnis ist, dass der Treiber und die GPU eine einzelne Zustandsänderung für jeden Zeichnen-Aufruf verarbeiten.

Dies ist ein gutes Beispiel für eine sequenzabhängige Treiberoptimierung. Der Treiber hat die Arbeit zweimal verschoben, indem er einen dirty-Zustand eingestellt hat, und dann die Arbeit einmal ausgeführt, um den dirty-Zustand zu löschen. Dies ist ein gutes Beispiel für die Art der Effizienzverbesserung, die stattfinden kann, wenn Arbeit auf absolut erforderliche Zeit verschoben wird.

Woher wissen Sie, welche Zustandsänderungen intern einen geänderten Zustand festlegen und daher die Arbeit auf einen späteren Zeitpunkt verschieben? Nur durch Testen von Rendersequenzen (oder Sprechen mit Treiberschreibern). Treiber werden regelmäßig aktualisiert und verbessert, damit die Liste der Optimierungen nicht statisch ist. Es gibt nur eine Möglichkeit, absolut zu wissen, was eine Zustandsänderung in einer bestimmten Rendersequenz auf einem bestimmten Hardwaresatz kostet. und das heißt, sie zu messen.

### <a name="watch-out-for-drawprimitive-optimizations"></a>Achten Sie auf DrawPrimitive-Optimierungen.

Zusätzlich zu Zustandsänderungsoptimierungen versucht die Runtime, die Anzahl der Zeichnen-Aufrufe zu optimieren, die der Treiber verarbeiten muss. Betrachten Sie z. B. die folgenden Zurück-zeichnen-Aufrufe:


```
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 3); // Draw 3 primitives, vertices 0 - 8
DrawPrimitive(D3DPT_TRIANGLELIST, 9, 4); // Draw 4 primitives, vertices 9 - 20
```



Beispiel 5a: Zwei Zeichnen-Aufrufe

Diese Sequenz enthält zwei Draw-Aufrufe, die die Laufzeit in einem einzigen Aufruf konsolidiert, der den folgenden entspricht:


```
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 7); // Draw 7 primitives, vertices 0 - 20
```



Beispiel 5b: Ein einzelner verketteter Draw-Aufruf

Die Runtime verkettet beide dieser speziellen Zeichnen-Aufrufe in einem einzigen Aufruf, wodurch die Treiberarbeit um 50 Prozent reduziert wird, da der Treiber jetzt nur einen Zeichnen-Aufruf verarbeiten muss.

Im Allgemeinen verkettet die Runtime zwei oder mehr [](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) Back-to-Back-DrawPrimitive-Aufrufe, wenn:

1.  Der primitive Typ ist eine Dreiecksliste (D3DPT \_ TRIANGLELIST).
2.  Jeder nachfolgende [**DrawPrimitive-Aufruf**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) muss auf aufeinander folgende Scheitelpunkte innerhalb des Scheitelpunktpuffers verweisen.

Entsprechend sind die richtigen Bedingungen für die Verkettung von zwei oder mehr [**Back-to-Back-DrawIndexedPrimitive-Aufrufen:**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)

1.  Der primitive Typ ist eine Dreiecksliste (D3DPT \_ TRIANGLELIST).
2.  Jeder nachfolgende [**DrawIndexedPrimitive-Aufruf**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) muss sequenziell auf aufeinander folgende Indizes innerhalb des Indexpuffers verweisen.
3.  Jeder nachfolgende [**DrawIndexedPrimitive-Aufruf**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) muss denselben Wert für BaseVertexIndex verwenden.

Um eine Verkettung während der Profilerstellung zu verhindern, ändern Sie die Rendersequenz so, dass der primitive Typ keine Dreiecksliste ist, oder ändern Sie die Rendersequenz so, dass es keine Back-to-Back-Zeichnen-Aufrufe gibt, die aufeinander folgende Scheitelzeichen (oder Indizes) verwenden. Genauer gesagt verkettet die Runtime auch Zeichnen-Aufrufe, die die beiden folgenden Bedingungen erfüllen:

-   Wenn der vorherige Aufruf [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)ist, , wenn der nächste Zeichnen-Aufruf:
    -   verwendet eine Dreiecksliste, AND
    -   gibt StartVertex = vorheriges StartVertex + vorheriges PrimitiveCount \* 3 an
-   Bei Verwendung [**von DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive), wenn der nächste Zeichnen-Aufruf:
    -   verwendet eine Dreiecksliste, AND
    -   gibt startIndex = previous StartIndex + previous PrimitiveCount \* 3, AND an
    -   gibt BaseVertexIndex = previous BaseVertexIndex an

Im Folgenden finden Sie ein feineres Beispiel für die Verkettung von Zeichnen-Aufrufen, die bei der Profilerstellung leicht übersehen werden kann. Angenommen, die Rendersequenz sieht wie die folgenden aus:


```
  for(int i = 0; i < 1500; i++)
  {
    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
  }
```



Beispiel 5c: Eine Zustandsänderung und ein Draw-Aufruf

Die Schleife durch iteriert 1.500 Dreiecke, setzt eine Textur und zeichnen jedes Dreieck. Diese Renderschleife benötigt etwa 2750 Zyklen für [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) und 1100 Zyklen für [**DrawPrimitive,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) wie in den vorherigen Abschnitten gezeigt. Sie können intuitiv erwarten, dass das Verschieben von **SetTexture** außerhalb der Renderschleife die Arbeitsmenge des Treibers um 1500 \* 2750 Zyklen reduzieren sollte. Dies entspricht der Arbeitsmenge, die mit dem Aufruf von **SetTexture** um das 1500-fache verbunden ist. Der Codeausschnitt sieht wie folgt aus:


```
  SetTexture(...); // Set the state outside the loop
  for(int i = 0; i < 1500; i++)
  {
//    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
  }
```



Beispiel 5d: Beispiel 5c mit der Zustandsänderung außerhalb der Schleife

Das Verschieben von [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) außerhalb der Renderschleife reduziert die Menge an Arbeit, die **SetTexture** zugeordnet ist, da sie einmal statt 1500 Mal aufgerufen wird. Ein weniger offensichtlicher sekundärer Effekt ist, dass die Arbeit für [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) ebenfalls von 1.500 aufrufen auf 1 Aufruf reduziert wird, da alle Bedingungen für die Verkettung von Draw-Aufrufen erfüllt sind. Wenn die Rendersequenz verarbeitet wird, verarbeitet die Runtime 1.500 Aufrufe in einem einzelnen Treiberaufruf. Durch das Verschieben dieser einen Codezeile wurde die Arbeitsmenge des Treibers erheblich reduziert:


```
total work done = runtime + driver work

Example 5c: with SetTexture in the loop:
runtime work = 1500 SetTextures + 1500 DrawPrimitives 
driver  work = 1500 SetTextures + 1500 DrawPrimitives 

Example 5d: with SetTexture outside of the loop:
runtime work = 1 SetTexture + 1 DrawPrimitive + 1499 Concatenated DrawPrimitives 
driver  work = 1 SetTexture + 1 DrawPrimitive 
```



Diese Ergebnisse sind vollständig richtig, aber im Kontext der ursprünglichen Frage sehr irreführend. Die Optimierung des Zeichnen-Aufrufs hat dazu geführt, dass die Menge der Treiberarbeit erheblich reduziert wurde. Dies ist ein häufiges Problem bei der benutzerdefinierten Profilerstellung. Achten Sie beim Entfernen von Aufrufen aus einer Rendersequenz darauf, dass Sie die Verkettung von Zeichnen-Aufrufen vermeiden. Tatsächlich ist dieses Szenario ein leistungsfähiges Beispiel für die durch diese Laufzeitoptimierung mögliche Verbesserung der Treiberleistung.

Sie wissen nun, wie Zustandsänderungen gemessen werden. Beginnen Sie mit der Profilerstellung für [**DrawPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) Fügen Sie dann jede zusätzliche Zustandsänderung der Sequenz hinzu (in einigen Fällen fügen Sie einen Aufruf hinzu, und fügen Sie in anderen Fällen zwei Aufrufe hinzu), und messen Sie den Unterschied zwischen den beiden Sequenzen. Sie können die Ergebnisse in Ticks, Zyklen oder Zeit konvertieren. Genau wie das Messen von Rendersequenzen mit QueryPerformanceCounter hängt das Messen einzelner Zustandsänderungen vom Abfragemechanismus ab, um den Befehlspuffer zu steuern und die Zustandsänderungen in eine Schleife zu versetzen, um die Auswirkungen der Modusübergänge zu minimieren. Dieses Verfahren misst die Kosten für das Umschalten eines Zustands, da der Profiler den Durchschnitt der Aktivierung und Deaktivierung des Zustands zurückgibt.

Mit dieser Funktion können Sie mit dem Generieren beliebiger Renderingsequenzen beginnen und die zugehörige Laufzeit- und Treiberarbeit genau messen. Die Zahlen können dann verwendet werden, um Budgetfragen wie "wie viele weitere dieser Aufrufe" in der Rendersequenz zu beantworten, während weiterhin eine angemessene Framerate beibehalten wird, vorausgesetzt, dass die CPU-Auslastung begrenzt ist.

## <a name="summary"></a>Zusammenfassung

In diesem Artikel wird veranschaulicht, wie Sie den Befehlspuffer steuern, sodass für einzelne Aufrufe ein genaues Profil erstellt werden kann. Die Profilerstellungsnummern können in Ticks, Zyklen oder absoluter Zeit generiert werden. Sie stellen den Umfang der Laufzeit- und Treiberarbeit dar, die jedem API-Aufruf zugeordnet ist.

Beginnen Sie mit der Profilerstellung für einen Draw \* Primitive-Aufruf in einer Rendersequenz. Beachten Sie Folgendes:

1.  Verwenden Sie QueryPerformanceCounter, um die Anzahl der Ticks pro API-Aufruf zu messen. Verwenden Sie QueryPerformanceFrequency, um die Ergebnisse bei Bedarf in Zyklen oder Zeit zu konvertieren.
2.  Verwenden Sie den Abfragemechanismus, um den Befehlspuffer vor dem Start zu leeren.
3.  Schließen Sie die Rendersequenz in eine Schleife ein, um die Auswirkungen des Modusübergangs zu minimieren.
4.  Verwenden Sie den Abfragemechanismus, um zu messen, wann die GPU ihre Arbeit abgeschlossen hat.
5.  Achten Sie auf die Laufzeitverkettung, die einen erheblichen Einfluss auf den Arbeitsaufwand hat.

Dadurch erhalten Sie eine Baselineleistung für [**DrawPrimitive,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) die zum Erstellen verwendet werden kann. Befolgen Sie die folgenden zusätzlichen Tipps, um ein Profil für eine Zustandsänderung zu erstellen:

1.  Fügen Sie die Zustandsänderung einem bekannten Rendersequenzprofil der neuen Sequenz hinzu. Da die Tests in einer Schleife durchgeführt werden, muss der Zustand zweimal auf entgegengesetzte Werte festgelegt werden (z. B. aktivieren und deaktivieren).
2.  Vergleichen Sie den Unterschied in den Zykluszeiten zwischen den beiden Sequenzen.
3.  Bei Zustandsänderungen, die die Pipeline erheblich ändern (z. B. [**SetTexture),**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)subtrahieren Sie den Unterschied zwischen den beiden Sequenzen, um die Zeit für die Zustandsänderung zu erhalten.
4.  Subtrahieren Sie bei Zustandsänderungen, die die Pipeline erheblich ändern (und daher ein Umschalten von Zuständen wie [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)erfordern), den Unterschied zwischen den Rendersequenzen, und dividieren Sie durch 2. Dadurch wird die durchschnittliche Anzahl von Zyklen für jede Zustandsänderung generiert.

Achten Sie jedoch auf Optimierungen, die unerwartete Ergebnisse bei der Profilerstellung verursachen. Zustandsänderungsoptimierungen können geänderte Zustände festlegen, wodurch Die Arbeit verzögert wird. Dies kann zu Profilergebnissen führen, die nicht so intuitiv wie erwartet sind. Verkettete Zeichnen-Aufrufe reduzieren die Arbeit des Treibers erheblich, was zu irreführenden Schlussfolgerungen führen kann. Sorgfältig geplante Rendersequenzen werden verwendet, um Zustandsänderungen und Zeichnen von Aufrufverkettungen zu verhindern. Der Trick besteht darin, zu verhindern, dass die Optimierungen während der Profilerstellung stattfinden, sodass es sich bei den generierten Zahlen um sinnvolle Budgetnummern handelt.

> [!Note]  
> Das Duplizieren dieser Profilerstellungsstrategie in einer Anwendung ohne den Abfragemechanismus ist schwieriger. Vor Direct3D 9 besteht die einzige vorhersagbare Möglichkeit zum Leeren des Befehlspuffers darin, eine aktive Oberfläche (z. B. ein Renderziel) zu sperren, um zu warten, bis sich die GPU im Leerlauf befindet. Dies liegt daran, dass das Sperren einer Oberfläche die Laufzeit zwingt, den Befehlspuffer zu leeren, falls der Puffer Renderingbefehle aufweist, die die Oberfläche aktualisieren sollten, bevor sie gesperrt wird, und auf den Abschluss der GPU warten müssen. Diese Technik ist funktionsfähig, obwohl sie die Verwendung des abfragemechanismus, der in Direct3D 9 eingeführt wurde, eher obtrusiv ist.

 

## <a name="appendix"></a>Anhang

Die Zahlen in dieser Tabelle sind ein Bereich von Näherungen für die Menge der Laufzeit- und Treiberarbeit, die jeder dieser Zustandsänderungen zugeordnet ist. Die Näherungswerte basieren auf tatsächlichen Messungen an Treibern mithilfe der im Dokument gezeigten Techniken. Diese Zahlen wurden mithilfe der Direct3D 9-Runtime generiert und sind treiberabhängig.

Die Verfahren in diesem Artikel dienen zur Messung der Laufzeit- und Treiberarbeit. Im Allgemeinen ist es unpraktisch, Ergebnisse bereitzustellen, die der Leistung der CPU und gpu in jeder Anwendung entsprechen, da dies ein umfassendes Array von Rendersequenzen erfordern würde. Darüber hinaus ist es besonders schwierig, die Leistung der GPU zu messen, da sie stark von der Einrichtung des Zustands in der Pipeline vor der Rendersequenz abhängig ist. Beispielsweise wirkt sich die Aktivierung von Alphablending nur wenig auf die erforderliche CPU-Arbeitsauslastung aus, kann aber einen großen Einfluss auf die Menge an Arbeit haben, die von der GPU ausgeführt wird. Daher schränken die Verfahren in diesem Artikel die GPU-Arbeit auf die geringstmögliche Menge ein, indem sie die Menge der zu rendernden Daten begrenzen. Dies bedeutet, dass die Zahlen in der Tabelle am besten mit den Ergebnissen von Anwendungen übereinstimmen, die cpu-begrenzt sind (im Gegensatz zu einer Anwendung, die durch die GPU beschränkt ist).

Es wird empfohlen, die vorgestellten Techniken zu verwenden, um die Szenarien und Konfigurationen abzudecken, die für Sie am wichtigsten sind. Die Werte in der Tabelle können zum Vergleichen mit den generierten Zahlen verwendet werden. Da jeder Treiber variiert, besteht die einzige Möglichkeit, die tatsächlich angezeigten Zahlen zu generieren, darin, Profilerstellungsergebnisse mit Ihren Szenarien zu generieren.



| API-Aufruf                             | Durchschnittliche Anzahl von Zyklen |
|--------------------------------------|--------------------------|
| SetVertexDeclaration                 | 6500 - 11250             |
| SetFVF                               | 6400 - 11200             |
| SetVertexShader                      | 3000 - 12100             |
| SetPixelShader                       | 6300 - 7000              |
| SPECULARENABLE                       | 1900 - 11200             |
| SetRenderTarget                      | 6000 - 6250              |
| SetPixelShaderConstant (1 Konstante)  | 1500 - 9000              |
| NORMALIZENORMALS                     | 2200 - 8100              |
| LightEnable                          | 1300 - 9000              |
| SetStreamSource                      | 3700 - 5800              |
| Beleuchtung                             | 1700 - 7500              |
| DIFFUSEMATERIALSOURCE                | 900 - 8300               |
| AMBIENTMATERIALSOURCE                | 900 - 8200               |
| COLORVERTEX                          | 800 - 7800               |
| SetLight                             | 2200 - 5100              |
| SetTransform                         | 3200 - 3750              |
| SetIndices                           | 900 - 5600               |
| Ambient                              | 1150 - 4800              |
| SetTexture                           | 2500 - 3100              |
| SPECULARMATERIALSOURCE               | 900 - 4600               |
| ICH BINDEDEMATERIALSOURCE               | 900 - 4500               |
| SetMaterial                          | 1000 - 3700              |
| ZENABLE                              | 700 - 3900               |
| WRAP0                                | 1600 - 2700              |
| MINFILTER                            | 1700 - 2500              |
| MAGFILTER                            | 1700 - 2400              |
| SetVertexShaderConstant (1 Konstante) | 1000 - 2700              |
| COLOROP                              | 1500 - 2100              |
| COLORARG2                            | 1300 - 2000              |
| COLORARG1                            | 1300 - 1980              |
| CULLMODE                             | 500 - 2570               |
| Clipping                             | 500 - 2550               |
| DrawIndexedPrimitive                 | 1200 - 1400              |
| ADDRESSV                             | 1090 - 1500              |
| ADDRESSU                             | 1070 - 1500              |
| DrawPrimitive                        | 1050 - 1150              |
| SRGBTEXTURE                          | 150 - 1500               |
| STENCILMASK                          | 570 - 700                |
| STENCILZFAIL                         | 500 - 800                |
| STENCILREF                           | 550 - 700                |
| ALPHABLENDENABLE                     | 550 - 700                |
| STENCILFUNC                          | 560 - 680                |
| STENCILWRITEMASK                     | 520 - 700                |
| STENCILFAIL                          | 500 - 750                |
| BESENUNC                                | 510 - 700                |
| ZWRITEENABLE                         | 520 - 680                |
| SCHABLONIERBAR                        | 540 - 650                |
| STENCILPASS                          | 560 - 630                |
| SRCBLEND                             | 500 - 685                |
| \_ \_ Zweiseitiger Schablonenmodus              | 450 - 590                |
| ALPHATESTENABLE                      | 470 - 525                |
| ALPHAREF                             | 460 - 530                |
| ALPHAFUNC                            | 450 - 540                |
| DESTBLEND                            | 475 - 510                |
| COLORWRITEENABLE                     | 465 - 515                |
| CCW \_ STENCILFAIL                     | 340 - 560                |
| CCW \_ STENCILPASS                     | 340 - 545                |
| CCW \_ STENCILZFAIL                    | 330 - 495                |
| SCISSORTESTENABLE                    | 375 - 440                |
| CCW \_ STENCILFUNC                     | 250 - 480                |
| SetScissorRect                       | 150 - 340                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterte Themen](advanced-topics.md)
</dt> </dl>

 

 
