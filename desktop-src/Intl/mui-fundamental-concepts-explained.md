---
description: Grundlegende Konzepte von CONCEPTS explained
ms.assetid: 9ab19a56-4d31-471d-949e-a539751b62e3
title: Grundlegende Konzepte von CONCEPTS explained
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88bd677d7a6b07bc4db78d733d81fc36624ddd06f9ad3014588b8e5fd0882aa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390890"
---
# <a name="mui-fundamental-concepts-explained"></a>Grundlegende Konzepte von CONCEPTS explained

-   [Voraussetzungen für DIE VORAUSSETZUNGEN](#prerequisite-for-mui)
-   [Trennung von Quellcode und sprachspezifischen Ressourcen](#separation-of-source-code-from-language-specific-resources)
    -   [Die Anfangszeit: Code und Ressourcen leben zusammen](#the-early-days-code-and-resources-live-together)
    -   [Logisches Trennen von Code und lokalisierbaren Ressourcen](#logically-separating-code-and-localizable-resources)
    -   [Physisches Trennen von Code und Ressourcen](#physically-separating-code-and-resources)
-   [Dynamisches Laden sprachspezifischer Ressourcen](#dynamically-loading-language-specific-resources)
-   [Erstellen von MUI-Anwendungen](#building-mui-applications)

## <a name="prerequisite-for-mui"></a>Voraussetzungen für DIE VORAUSSETZUNGEN

Die grundlegende Voraussetzung für die Erstellung einer MIT DEM-Konformen Anwendung für Windows Vista und darüber hinaus besteht darin, die Anwendung in Übereinstimmung mit Windows [Globalisierungsrichtlinien](https://msdn.microsoft.com/goglobal/bb688110.aspx)zu entwerfen.

## <a name="separation-of-source-code-from-language-specific-resources"></a>Trennung von Quellcode und sprachspezifischen Ressourcen

Eine der grundlegenden Voraussetzungen der TECHNOLOGY IST die Trennung von Anwendungsquellcode und sprachspezifischen Ressourcen, um mehrsprachige Szenarien in Anwendungen effizienter zu ermöglichen. Die Trennung von Code und Ressourcen wurde über verschiedene Mechanismen und in unterschiedlichem Grad im Laufe der Zeit erreicht, wie in den folgenden Abschnitten beschrieben. Jede Methode bot unterschiedliche Flexibilität beim Erstellen, Bereitstellen und Warten der Anwendung.

Die empfohlene Lösung für MIT DEM SYSTEM kompatible Anwendungen ist die letzte hier beschriebene Methode, nämlich die physische Trennung von Anwendungsquellcode und Ressourcen, wobei die Ressourcen selbst weiter in eine Datei pro unterstützter Sprache unterteilt sind, um maximale Flexibilität beim Erstellen, Bereitstellen und Warten zu erreichen.

### <a name="the-early-days-code-and-resources-live-together"></a>Die Anfangszeit: Code und Ressourcen leben zusammen

Zu Beginn wurden lokalisierte Anwendungen erstellt, indem der Quellcode bearbeitet und die Ressourcen (normalerweise Zeichenfolgen) im Code selbst geändert und die Anwendungen neu kompiliert wurden. Dies bedeutete, dass zum Erstellen einer lokalisierten Version der ursprüngliche Quellcode kopiert, die Textelemente (Ressourcen) innerhalb des Quellcodes übersetzt und der Code neu kompiliert werden musste. Die folgende Abbildung zeigt Anwendungscode mit Text, der lokalisiert werden muss.

![Konzeptionelles Diagramm mit einer Anwendung, die Einheiten eingebetteter Textressourcen enthält](images/mui-fundamental-concepts-explained-fig3.gif)

Dieser Ansatz ermöglicht zwar die Erstellung lokalisierter Anwendungen, hat aber auch erhebliche Nachteile:

-   Es sind mehrere Versionen des Quellcodes erforderlich, mindestens eine für die Quellsprache und eine für jede Zielsprache. Dies führt zu erheblichen Problemen beim Synchronisieren der verschiedenen Sprachversionen der Anwendung. Insbesondere wenn ein Fehler im Code behoben werden muss, muss der Fehler in jeder Kopie des Quellcodes behoben werden (einer pro Sprache).
-   Es ist auch äußerst fehleranfällig, da Lokalisierer , die keine Entwickler sind, Änderungen am Quellcode vornehmen mussten, wodurch ein erhebliches Risiko in Bezug auf die Codeintegrität entsteht.

Die Kombination dieser Nachteile macht dies zu einem äußerst ineffizienten Angebot, und es wurde ein besseres Modell benötigt.

### <a name="logically-separating-code-and-localizable-resources"></a>Logisches Trennen von Code und lokalisierbaren Ressourcen

Eine erhebliche Verbesserung gegenüber dem vorherigen Modell ist die logische Trennung von Code und lokalisierbaren Ressourcen für eine Anwendung. Dadurch wird der Code von den Ressourcen isoliert und sichergestellt, dass der Code unverändert bleibt, wenn Ressourcen durch Lokalisierung geändert werden. Aus Implementierungssicht werden Zeichenfolgen und andere Benutzeroberflächenelemente in Ressourcendateien gespeichert, die relativ einfach zu übersetzen sind und logisch von den Codeabschnitten getrennt sind.

Im Idealfall kann das Hinzufügen von Unterstützung für eine beliebige Sprache so einfach sein wie die Übersetzung der lokalisierbaren Ressourcen in diese neue Sprache und die Verwendung dieser übersetzten Ressourcen, um eine neue lokalisierte Version der Anwendung zu erstellen – ohne dass Codeänderungen erforderlich sind. Die folgende Abbildung veranschaulicht, wie Code und lokalisierbare Ressourcen innerhalb einer Anwendung logisch getrennt werden sollten.

![Konzeptionelles Diagramm, das eine Anwendung zeigt, die lokalisierbare Ressourcen enthält, die vom Code getrennt sind](images/mui-fundamental-concepts-explained-fig4.gif)

Dieses Modell ermöglicht eine einfachere Erstellung lokalisierter Versionen einer Anwendung und stellt eine erhebliche Verbesserung gegenüber dem vorherigen Modell dar. Dieses Modell, das durch die Verwendung von Ressourcenverwaltungstools implementiert wurde, war im Laufe der Jahre sehr erfolgreich und wird noch heute häufig von vielen Anwendungen verwendet. Dies hat jedoch erhebliche Nachteile:

-   Code und lokalisierte Ressourcen sind zwar logisch getrennt, aber dennoch physisch in einer ausführbaren Datei verknüpft. Insbesondere ist die Dienstbarkeit weiterhin problematisch, da der gleiche Codefehler (identisch in allen Sprachversionen) einen Patch pro Sprache erfordert. Wenn die Anwendung in 20 Sprachen ausgeliefert wird, muss daher ein Dienstpatch 20 Mal (einer für jede Sprache) ausgegeben werden, obwohl der Code nur einmal korrigiert wird.
-   Die Verteilung und Verwendung mehrsprachiger Anwendungen wird von diesem Modell nicht ausreichend unterstützt. Dies kann ein erhebliches Problem in OEM- und Unternehmensszenarien sein. Wenn beispielsweise ein Computer von zwei Benutzern mit verschiedenen Sprachen gemeinsam genutzt werden soll, müssen Anwendungen mit diesem Modell zweimal installiert werden, und dann muss ein Mechanismus aktiviert werden, um zwischen den beiden Installationen zu wechseln. Dabei wird davon ausgegangen, dass es keine zusätzlichen Abhängigkeiten gibt, die verhindern, dass auch dieses Szenario implementiert wird. Die folgende Abbildung zeigt ein Beispiel für einen einzelnen Codefehler, der zwei Patches erfordert.

![Konzeptionelles Diagramm, das zwei lokalisierte Anwendungen mit dem gleichen Codefehler zeigt](images/mui-fundamental-concepts-explained-fig5.gif)

Es ist klar, dass dieses Modell zwar in einigen Szenarien gut funktioniert, seine Einschränkungen für mehrsprachige Anwendungen und ihre Bereitstellungen jedoch sehr problematisch sein können.

Eine Variante dieses Modells, die einige probleme mit mehrsprachigen Anwendungen entschärft, ist das Modell, bei dem die lokalisierbaren Ressourcen eine Reihe unterschiedlicher Sprachressourcen enthalten. Dieses Modell verfügt über eine gemeinsame Codebasis und mehrere Ressourcen für verschiedene Sprachen in derselben Anwendung. Beispielsweise kann eine Anwendung mit Englisch, Deutsch, Französisch, Spanisch, Niederländisch und Italienisch im selben Paket versendet werden. Die folgende Abbildung zeigt eine Anwendung, die mehrere Sprachressourcen enthält.

![Konzeptionelles Diagramm, das eine Anwendung mit Code zeigt, der von zwei gebietsschemaspezifischen Ressourcen getrennt ist](images/mui-fundamental-concepts-explained-fig6.gif)

Dieses Modell erleichtert die Bedienung der Anwendung, wenn ein Codefehler behoben werden muss – was eine Verbesserung darstellt –, verbessert sich jedoch nicht gegenüber vorherigen Modellen, wenn es um die Unterstützung zusätzlicher Sprachen geht. In diesem Fall muss noch eine neue Version der Anwendung veröffentlicht werden (und diese Version ist möglicherweise durch die Notwendigkeit kompliziert, sicherzustellen, dass alle Sprachressourcen innerhalb derselben Verteilung synchronisiert werden).

### <a name="physically-separating-code-and-resources"></a>Physisches Trennen von Code und Ressourcen

Der nächste Schritt besteht darin, Code und Ressourcen physisch zu trennen. In diesem Modell werden die Ressourcen vom Code abstrahiert und physisch in verschiedenen Implementierungsdateien getrennt. Dies bedeutet insbesondere, dass der Code wirklich sprachunabhängig werden kann. derselbe physische Code wird tatsächlich für alle lokalisierten Versionen einer Anwendung ausgeliefert. Die folgende Abbildung veranschaulicht, dass Code und lokalisierbare Ressourcen physisch getrennt werden müssen.

![Konzeptionelles Diagramm, das eine Anwendung zeigt, die von ihren lokalisierbaren Ressourcen getrennt ist](images/mui-fundamental-concepts-explained-fig7.gif)

Dieser Ansatz hat gegenüber den vorherigen Ansätzen mehrere Vorteile:

-   Die Bereitstellung mehrsprachiger Lösungen wird erheblich vereinfacht. Das Hinzufügen von Unterstützung für eine bestimmte Sprache erfordert nur den Versand und die Installation eines neuen Satzes von Sprachressourcen für diese bestimmte Sprache. Dies ist besonders wichtig, wenn nicht alle Sprachressourcen gleichzeitig verfügbar sind. Mit diesem Modell kann eine Anwendung in einer Reihe von Kernsprachen bereitgestellt und die Anzahl der unterstützten Sprachen im Laufe der Zeit erhöht werden, ohne den tatsächlichen Code ändern oder erneut bereitstellen zu müssen. Dieser Vorteil wird durch einen Fallbackmechanismus erweitert, der eine partielle Lokalisierung von Anwendungen und Systemkomponenten in einer bestimmten Sprache ermöglicht, indem sichergestellt wird, dass Ressourcen, die in dieser bevorzugten Sprache nicht gefunden werden, auf eine andere Sprache zurückgreifen, die die Benutzer ebenfalls verstehen. Insgesamt trägt dieses Modell dazu bei, den erheblichen Aufwand zu verringern, den globale Unternehmen bei der Bereitstellung von Anwendungen in mehreren Sprachen bewältigen müssen, da es die Bereitstellung einzelner Images auf viel effektivere Weise ermöglicht.
-   Die Dienstbarkeit wurde verbessert. Ein Codefehler muss nur einmal behoben und bereitgestellt werden, da der Code vollständig lokalisierungsunabhängig ist. Bei diesem Modell ist das Ausstellen einer Korrektur für einen Codefehler, sofern die Änderung nicht auf die Benutzeroberfläche bezogen ist, wesentlich einfacher und kostengünstiger als in einem der vorherigen Modelle.

## <a name="dynamically-loading-language-specific-resources"></a>Dynamisches Laden sprachspezifischer Ressourcen

Mit den grundlegenden KONZEPTEN der [physischen Trennung von Quellcode von sprachspezifischen Ressourcen](#physically-separating-code-and-resources)und dem Erstellen einer sprachneutralen Kernbinärdatei für eine Anwendung wird im Wesentlichen eine Architektur eingerichtet, die für die Implementierung des dynamischen Ladens sprachspezifischer Ressourcen auf der Grundlage von Benutzer- und Systemspracheinstellungen schädlich ist.

Anwendungsquellcode, der in der sprachneutralen Kernbinärdatei gebündelt ist, kann DIE GLOSSAR-APIs auf der Windows-Plattform verwenden, um die Auswahl der entsprechenden Anzeigesprache für die Benutzeroberfläche für einen bestimmten Kontext zu abstrahieren. DIES wird von DER UNTERSTÜTZT:

-   Erstellen einer priorisierten Liste von Anzeigesprachen für die Benutzeroberfläche basierend auf Einstellungen auf System-, Benutzer- und Anwendungsebene, Benutzerebene und Systemebene.
-   Implementieren eines Fallbackmechanismus, mit dem basierend auf der Verfügbarkeit lokalisierter Ressourcen ein geeigneter Kandidat aus dieser priorisierten Liste von Sprachen ausgewählt wird.

Die Vorteile des dynamischen Ladens von Benutzeroberflächenressourcen mit priorisiertem Fallback sind:

-   Sie ermöglicht die partielle Lokalisierung von Anwendungen und Systemkomponenten in einer bestimmten Sprache, da Ressourcen, die in dieser bevorzugten Sprache nicht gefunden werden, automatisch auf die nächste Sprache in der priorisierten Liste zurückfallen.
-   Dies ermöglicht Szenarien wie den dynamischen Wechsel von einer Sprache in eine andere.
-   Sie ermöglicht die Erstellung regionaler oder weltweiter Images für einzelne Bereitstellungen, die eine Reihe von Sprachen für OEMs und Unternehmen abdecken.

## <a name="building-mui-applications"></a>Erstellen von MUI-Anwendungen

In den vorherigen Abschnitten wurden die Optionen zum Trennen von Quellcode von sprachspezifischen Ressourcen und der daraus resultierende Vorteil beschrieben, dass kernbasierte Windows Plattform-APIs genutzt werden können, um lokalisierte Ressourcen dynamisch zu laden. Obwohl es sich hierbei um Richtlinien handelt, sollte auch darauf hingewiesen werden, dass es keine spezifische, vorschreibende Möglichkeit gibt, eine JAVASCRIPT-Anwendung für die Windows-Plattform zu entwickeln.

Anwendungsentwickler haben die volle Wahl, wie sie verschiedene Spracheinstellungen der Benutzeroberfläche, Optionen zum Erstellen von Ressourcen und Methoden zum Laden von Ressourcen behandeln. Entwickler können die in diesem Dokument bereitgestellten Richtlinien auswerten und eine Kombination auswählen, die ihren Anforderungen und ihrer Entwicklungsumgebung entspricht.

In der folgenden Tabelle sind die verschiedenen Entwurfsoptionen zusammengefasst, die Anwendungsentwicklern zur Verfügung stehen, die eine CAB-Anwendung für die Windows-Plattform erstellen möchten.



<table>
<thead>
<tr class="header">
<th>Spracheinstellungen für die Benutzeroberfläche</th>
<th>Ressourcenerstellung</th>
<th>Laden von Ressourcen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2">Befolgen Sie die Einstellungen für die Benutzeroberflächensprache im Betriebssystem${REMOVE}$<br />
</td>
<td>Einzelne Sprache in einer Binärdatei für geteilte Ressourcen (GLOSSAR-Ressourcentechnologie)<br/> Oder<br/> Mehrere Sprachen in einer nicht geteilten Ressourcenbinärdatei<br/></td>
<td>Die Anwendung ruft Standardfunktionen zum Laden von Ressourcen auf. Ressourcen werden in den Sprachen zurückgegeben, die den Betriebssystemeinstellungen entsprechen.<br/></td>
</tr>
<tr class="even">
<td>Anwendungsspezifischer Ressourcenmechanismus<br/></td>
<td>Die Anwendung ruft die API FÜR DIE BENUTZEROBERFLÄCHE auf, um die vom Thread bevorzugten Benutzeroberflächensprachen oder die von der Verarbeitung bevorzugten Benutzeroberflächensprachen aus dem Betriebssystem abzurufen und diese Einstellungen zum Laden eigener Ressourcen zu verwenden.<br/></td>

</tr>
<tr class="odd">
<td rowspan="2">Anwendungsspezifische Benutzeroberflächenspracheinstellungen${REMOVE}$<br />
</td>
<td>Einzelne Sprache in einer geteilten Ressourcenbinärdatei<br/> Oder<br/> Mehrere Sprachen in einer nicht geteilten Ressourcenbin binär<br/></td>
<td>Die Anwendung ruft die COD-API auf, um anwendungsspezifische Benutzeroberflächensprachen oder prozessspezifische Benutzeroberflächensprachen zu festlegen, und ruft dann Standardfunktionen zum Laden von Ressourcen auf. Ressourcen werden in den Sprachen zurückgegeben, die von der Anwendung oder den Systemsprachen festgelegt werden.<br/> Oder<br/> Die Anwendung prüft Ressourcen in einer bestimmten Sprache und verarbeitet ihre eigene Ressourcenextraktion aus den abgerufenen Binärdaten.<br/></td>
</tr>
<tr class="even">
<td>Anwendungsspezifischer Ressourcenmechanismus<br/></td>
<td>Die Anwendung verwaltet das Laden eigener Ressourcen.<br/></td>

</tr>
</tbody>
</table>



 

 

 




