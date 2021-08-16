---
description: 'GRUNDLAGEN: Grundlegende Konzepte'
ms.assetid: 9ab19a56-4d31-471d-949e-a539751b62e3
title: 'GRUNDLAGEN: Grundlegende Konzepte'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88bd677d7a6b07bc4db78d733d81fc36624ddd06f9ad3014588b8e5fd0882aa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390890"
---
# <a name="mui-fundamental-concepts-explained"></a>GRUNDLAGEN: Grundlegende Konzepte

-   [Erforderliche Komponenten für DIE AN-A-Datei](#prerequisite-for-mui)
-   [Trennung von Quellcode von sprachspezifischen Ressourcen](#separation-of-source-code-from-language-specific-resources)
    -   [Die ersten Tage: Code und Ressourcen werden zusammen verwendet](#the-early-days-code-and-resources-live-together)
    -   [Logisches Trennen von Code und lokalisierbaren Ressourcen](#logically-separating-code-and-localizable-resources)
    -   [Physisches Trennen von Code und Ressourcen](#physically-separating-code-and-resources)
-   [Dynamisches Laden sprachspezifischer Ressourcen](#dynamically-loading-language-specific-resources)
-   [Erstellen vonBAU-Anwendungen](#building-mui-applications)

## <a name="prerequisite-for-mui"></a>Erforderliche Komponenten für DIE AN-A-Datei

Die grundlegende Voraussetzung für das Erstellen einer MIT-kompatiblen Anwendung für Windows Vista und darüber hinaus ist das Entwerfen der Anwendung in Übereinstimmung mit Windows [Globalisierungsrichtlinien.](https://msdn.microsoft.com/goglobal/bb688110.aspx)

## <a name="separation-of-source-code-from-language-specific-resources"></a>Trennung von Quellcode von sprachspezifischen Ressourcen

Eine der grundlegenden Voraussetzungen für DIE TECHNOLOGY ist die Trennung von Anwendungsquellencode von sprachspezifischen Ressourcen, um mehrsprachige Szenarien in Anwendungen effizienter zu ermöglichen. Die Trennung von Code und Ressourcen wurde im Laufe der Zeit über verschiedene Mechanismen und in unterschiedlichen Graden erreicht, wie in den folgenden Abschnitten beschrieben. Jede Methode bot unterschiedliche Flexibilität beim Erstellen, Bereitstellen und Warten der Anwendung.

Die empfohlene Lösung für DIE MIT-kompatiblen Anwendungen ist die letzte hier beschriebene Methode, nämlich die physische Trennung von Quellcode und Ressourcen der Anwendung, bei der die Ressourcen selbst weiter in eine Datei pro unterstützter Sprache aufgeschlüsselt sind, um maximale Flexibilität beim Erstellen, Bereitstellen und Warten zu erhalten.

### <a name="the-early-days-code-and-resources-live-together"></a>Die ersten Tage: Code und Ressourcen werden zusammen verwendet

Anfänglich wurden lokalisierte Anwendungen erstellt, indem der Quellcode bearbeitet und die Ressourcen (in der Regel Zeichenfolgen) im Code selbst geändert und die Anwendungen neu kompiliert wurden. Dies bedeutete, dass zum Erstellen einer lokalisierten Version der ursprüngliche Quellcode kopiert, die Textelemente (Ressourcen) innerhalb des Quellcodes übersetzt und der Code neu kompiliert werden musste. Die folgende Abbildung zeigt Anwendungscode mit Text, der lokalisiert werden muss.

![Konzeptionelles Diagramm, das eine Anwendung zeigt, die Einheiten eingebetteter Textressourcen enthält](images/mui-fundamental-concepts-explained-fig3.gif)

Dieser Ansatz ermöglicht zwar die Erstellung lokalisierter Anwendungen, hat aber auch erhebliche Nachteile:

-   Es sind mehrere Versionen des Quellcodes erforderlich, mindestens eine für die Quellsprache und eine für jede der Zielsprachen. Dies führt zu erheblichen Problemen beim Synchronisieren der verschiedenen Sprachversionen der Anwendung. Insbesondere wenn ein Fehler im Code behoben werden muss, muss der Fehler in jeder Kopie des Quellcodes (eine pro Sprache) behoben werden.
-   Es ist auch äußerst fehleranfällig, da lokalisierer – die keine Entwickler sind – Änderungen am Quellcode vorgenommen haben müssen, wodurch ein erhebliches Risiko in Bezug auf die Codeintegrität verursacht wird.

Die Kombination dieser Nachteile macht dies zu einem äußerst ineffizienten Angebot, und es wurde ein besseres Modell benötigt.

### <a name="logically-separating-code-and-localizable-resources"></a>Logisches Trennen von Code und lokalisierbaren Ressourcen

Eine erhebliche Verbesserung gegenüber dem vorherigen Modell ist die logische Trennung von Code und lokalisierbaren Ressourcen für eine Anwendung. Dadurch wird der Code von den Ressourcen isoliert und sichergestellt, dass code unverändert bleibt, wenn Ressourcen durch Lokalisierung geändert werden. Aus Implementierungs sicht werden Zeichenfolgen und andere Benutzeroberflächenelemente in Ressourcendateien gespeichert, die relativ einfach zu übersetzen sind und logisch von den Codeabschnitten getrennt sind.

Im Idealfall kann das Hinzufügen von Unterstützung für eine beliebige Sprache so einfach wie das Übersetzen der lokalisierbaren Ressourcen in diese neue Sprache und die Verwendung dieser übersetzten Ressourcen sein, um eine neue lokalisierte Version der Anwendung zu erstellen – ohne dass Codeänderungen erforderlich sind. Die folgende Abbildung veranschaulicht, wie Code und lokalisierbare Ressourcen innerhalb einer Anwendung logisch getrennt werden sollten.

![Konzeptionelles Diagramm, das eine Anwendung zeigt, die lokalisierbare Ressourcen getrennt von Code enthält](images/mui-fundamental-concepts-explained-fig4.gif)

Dieses Modell ermöglicht eine einfachere Erstellung lokalisierter Versionen einer Anwendung und ist eine erhebliche Verbesserung gegenüber dem vorherigen Modell. Dieses Modell, das mithilfe von Ressourcenverwaltungstools implementiert wurde, war im Laufe der Jahre sehr erfolgreich und wird auch heute noch häufig von vielen Anwendungen verwendet. Dies hat jedoch erhebliche Nachteile:

-   Während sie logisch getrennt sind, werden Code und lokalisierte Ressourcen weiterhin physisch in einer ausführbaren Datei verbunden. Insbesondere ist die Dienstbarkeit weiterhin problematisch, da derselbe Codefehler (identisch in allen Sprachversionen) einen Patch pro Sprache erfordert. Wenn die Anwendung also in 20 Sprachen versenden wird, muss ein Dienstpatch 20 Mal ausgegeben werden (einer für jede Sprache), obwohl der Code nur einmal korrigiert wird.
-   Die Verteilung und Verwendung mehrsprachiger Anwendungen wird von diesem Modell nicht angemessen unterstützt. Dies kann in OEM- und Unternehmensszenarien ein erhebliches Problem darstellen. Wenn ein Computer beispielsweise von zwei Benutzern mit verschiedenen Sprachen gemeinsam genutzt werden soll, müssen Anwendungen zweimal mit diesem Modell installiert werden, und dann muss ein Mechanismus aktiviert werden, um zwischen den beiden Installationen zu wechseln. Dabei wird davon ausgegangen, dass keine zusätzlichen Abhängigkeiten vorhanden sind, die verhindern, dass auch dieses Szenario implementiert wird. Die folgende Abbildung zeigt ein Beispiel für einen einzelnen Codefehler, der zwei Patches erfordert.

![Konzeptionelles Diagramm, das zwei lokalisierte Anwendungen zeigt, die denselben Codefehler haben](images/mui-fundamental-concepts-explained-fig5.gif)

Es ist klar, dass dieses Modell zwar in einigen Szenarien gut funktioniert, die Einschränkungen für mehrsprachige Anwendungen und deren Bereitstellungen jedoch sehr problematisch sein können.

Eine Variante dieses Modells, die einige der Probleme mit mehrsprachigen Anwendungen entschärft, ist das Modell, bei dem die lokalisierbaren Ressourcen eine Reihe verschiedener Sprachressourcen enthalten. Dieses Modell verfügt über eine gemeinsame Codebasis und mehrere Ressourcen für verschiedene Sprachen in derselben Anwendung. Eine Anwendung kann beispielsweise mit Englisch, Deutsch, Französisch, Spanisch, Niederländisch und Italienisch im selben Paket versenden. Die folgende Abbildung zeigt eine Anwendung, die mehrere Sprachressourcen enthält.

![Konzeptionelles Diagramm, das eine Anwendung mit Code zeigt, der von zwei lokalen Ressourcen getrennt ist](images/mui-fundamental-concepts-explained-fig6.gif)

Dieses Modell erleichtert die Arbeit an der Anwendung, wenn ein Codefehler behoben werden muss – was eine Verbesserung ist –, verbessert sich jedoch nicht gegenüber früheren Modellen, wenn es um die Unterstützung zusätzlicher Sprachen geht. In diesem Fall muss weiterhin eine neue Version der Anwendung veröffentlicht werden (und dieses Release ist möglicherweise kompliziert, da sichergestellt werden muss, dass alle Sprachressourcen innerhalb derselben Verteilung synchronisiert werden).

### <a name="physically-separating-code-and-resources"></a>Physisches Trennen von Code und Ressourcen

Der nächste Schritt besteht in der physischen Trennung von Code und Ressourcen. In diesem Modell werden die Ressourcen vom Code abstrahiert und physisch in verschiedenen Implementierungsdateien getrennt. Dies bedeutet insbesondere, dass der Code wirklich sprachunabhängig werden kann. Derselbe physische Code wird tatsächlich für alle lokalisierten Versionen einer Anwendung ausgeliefert. Die folgende Abbildung veranschaulicht, dass Code und lokalisierbare Ressourcen physisch getrennt werden müssen.

![Konzeptionelles Diagramm, das eine Anwendung getrennt von den lokalisierbaren Ressourcen zeigt](images/mui-fundamental-concepts-explained-fig7.gif)

Dieser Ansatz hat gegenüber den vorherigen Ansätzen mehrere Vorteile:

-   Die Bereitstellung mehrsprachiger Lösungen wird erheblich vereinfacht. Das Hinzufügen von Unterstützung für eine beliebige Sprache erfordert nur den Versand und die Installation einer neuen Gruppe von Sprachressourcen für diese bestimmte Sprache. Dies ist besonders wichtig, wenn nicht alle Sprachressourcen gleichzeitig verfügbar sind. Mit diesem Modell können Sie eine Anwendung in einer Reihe von Kernsprachen bereitstellen und die Anzahl der unterstützten Sprachen im Laufe der Zeit erhöhen, ohne den tatsächlichen Code ändern oder erneut bereitstellen zu müssen. Dieser Vorteil wird durch einen Fallbackmechanismus erweitert, der eine partielle Lokalisierung von Anwendungen und Systemkomponenten in einer bestimmten Sprache ermöglicht, indem sichergestellt wird, dass Ressourcen, die nicht in dieser bevorzugten Sprache gefunden werden, auf eine andere Sprache zurückfallen, die auch von den Benutzern verstanden wird. Insgesamt trägt dieses Modell dazu bei, die erhebliche Belastung zu verringern, mit der globale Unternehmen bei der Bereitstellung von Anwendungen in mehreren Sprachen konfrontiert sind, da es die Bereitstellung einzelner Images wesentlich effektiver ermöglicht.
-   Die Serviceability wurde verbessert. Ein Codefehler muss nur einmal behoben und bereitgestellt werden, da der Code vollständig lokalisierungsunabhängig ist. Bei diesem Modell ist das Ausstellen einer Korrektur für einen Codefehler, sofern die Änderung nicht benutzeroberflächenbezogen ist, wesentlich einfacher und kostengünstiger als in jedem der vorherigen Modelle.

## <a name="dynamically-loading-language-specific-resources"></a>Dynamisches Laden sprachspezifischer Ressourcen

Mit den grundlegenden Konzepten des THEMAs der physischen Trennung von Quellcode von sprachspezifischen Ressourcen und dem Erstellen einer sprachneutralen Kernbin binärer Daten für eine Anwendung richten Sie im Wesentlichen eine Architektur ein, die sich auf die Implementierung des dynamischen Ladens sprachspezifischer Ressourcen basierend auf Benutzer- und Systemspracheinstellungen stützt. [](#physically-separating-code-and-resources)

Anwendungsquellencode, der in der sprachneutralen Kernbin binär gebündelt ist, kann DIE-APIs in der Windows-Plattform verwenden, um die Auswahl der entsprechenden Anzeige-Benutzeroberflächensprache für einen bestimmten Kontext zu abstrahieren. DIES wird durch:

-   Erstellen einer priorisierten Liste von Anzeige-Benutzeroberflächensprachen basierend auf Einstellungen auf System-, Benutzer- und Anwendungsebene, Benutzerebene und Systemebene.
-   Implementieren eines Fallbackmechanismus, der basierend auf der Verfügbarkeit lokalisierter Ressourcen einen geeigneten Kandidaten aus dieser priorisierten Liste von Sprachen auswählt.

Die Vorteile des dynamischen Ladens von Benutzeroberflächenressourcen mit priorisiertem Fallback sind:

-   Sie ermöglicht die partielle Lokalisierung von Anwendungen und Systemkomponenten in einer bestimmten Sprache, da Ressourcen, die in dieser bevorzugten Sprache nicht gefunden werden, automatisch auf die nächste Sprache in der priorisierten Liste zurückfallen.
-   Sie ermöglicht Szenarien wie das dynamische Wechseln von einer Sprache in eine andere.
-   Sie ermöglicht das Erstellen regionaler oder weltweiter Einzelbereitstellungsabbilder, die eine Reihe von Sprachen für OEMs und Unternehmen abdecken.

## <a name="building-mui-applications"></a>Erstellen vonBAU-Anwendungen

In den vorherigen Abschnitten wurden die Optionen zum Trennen von Quellcode von sprachspezifischen Ressourcen sowie der daraus resultierende Vorteil beschrieben, dass die wichtigsten Windows-Plattform-APIs zum dynamischen Laden lokalisierter Ressourcen genutzt werden können. Obwohl es sich hierbei um Richtlinien handelt, sollte auch darauf hingewiesen werden, dass es keine bestimmte präskriptive Möglichkeit gibt, eineSTELLUNG-Anwendung für die Windows zu entwickeln.

Anwendungsentwickler haben die volle Auswahl bei der Behandlung verschiedener Spracheinstellungen für die Benutzeroberfläche, Optionen zum Erstellen von Ressourcen und Methoden zum Laden von Ressourcen. Entwickler können die in diesem Dokument bereitgestellten Richtlinien auswerten und eine Kombination auswählen, die ihren Anforderungen und ihrer Entwicklungsumgebung entspricht.

In der folgenden Tabelle sind die verschiedenen Entwurfsoptionen zusammengefasst, die Anwendungsentwicklern zur Verfügung stehen, die eine PROGRAMMANWENDUNG für die Windows erstellen möchten.



<table>
<thead>
<tr class="header">
<th>Einstellungen der Benutzeroberflächensprache</th>
<th>Ressourcenerstellung</th>
<th>Laden von Ressourcen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2">Befolgen Sie die Einstellungen der Benutzeroberflächensprache im Betriebssystem${REMOVE}$$<br />
</td>
<td>Einzelne Sprache in einer Binärdatei für geteilte Ressourcen (RESOURCE Technology)<br/> Oder<br/> Mehrere Sprachen in einer nicht geteilten Ressourcenbin binär<br/></td>
<td>Die Anwendung ruft Standardfunktionen zum Laden von Ressourcen auf. Ressourcen werden in den Sprachen zurückgegeben, die mit den Betriebssystemeinstellungen übereinstimmen.<br/></td>
</tr>
<tr class="even">
<td>Anwendungsspezifischer Ressourcenmechanismus<br/></td>
<td>Die Anwendung ruft die COD-API auf, um die von Threads bevorzugten Sprachen der Benutzeroberfläche oder die vom Prozess bevorzugten Sprachen der Benutzeroberfläche aus dem Betriebssystem abzurufen und diese Einstellungen zu verwenden, um ihre eigenen Ressourcen zu laden.<br/></td>

</tr>
<tr class="odd">
<td rowspan="2">Anwendungsspezifische Ui-Spracheinstellungen${REMOVE}$<br />
</td>
<td>Einzelne Sprache in einer Binärdatei für geteilte Ressourcen<br/> Oder<br/> Mehrere Sprachen in einer nicht geteilten Ressourcenbin binär<br/></td>
<td>Die Anwendung ruft die COD-API auf, um anwendungsspezifische Benutzeroberflächensprachen oder prozessspezifische Sprachen für die Benutzeroberfläche zu festlegen, und ruft dann Standardfunktionen zum Laden von Ressourcen auf. Ressourcen werden in den Sprachen zurückgegeben, die von der Anwendung oder den Systemsprachen festgelegt werden.<br/> Oder<br/> Die Anwendung prüft Ressourcen in einer bestimmten Sprache und verarbeitet ihre eigene Ressourcenextraktion aus den abgerufenen Binärdaten.<br/></td>
</tr>
<tr class="even">
<td>Anwendungsspezifischer Ressourcenmechanismus<br/></td>
<td>Die Anwendung verwaltet das Laden eigener Ressourcen.<br/></td>

</tr>
</tbody>
</table>



 

 

 




