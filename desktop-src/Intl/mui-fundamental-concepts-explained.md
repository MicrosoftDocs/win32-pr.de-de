---
description: Grundlegende Konzepte von MUI erläutert
ms.assetid: 9ab19a56-4d31-471d-949e-a539751b62e3
title: Grundlegende Konzepte von MUI erläutert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82dbeedb246944bef6c23c739eafddff86423b35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959180"
---
# <a name="mui-fundamental-concepts-explained"></a>Grundlegende Konzepte von MUI erläutert

-   [Voraussetzung für MUI](#prerequisite-for-mui)
-   [Trennung des Quellcodes von sprachspezifischen Ressourcen](#separation-of-source-code-from-language-specific-resources)
    -   [Die frühen Tage: Code und Ressourcen Live](#the-early-days-code-and-resources-live-together)
    -   [Logische Trennung von Code und lokalisierbaren Ressourcen](#logically-separating-code-and-localizable-resources)
    -   [Physisches trennen von Code und Ressourcen](#physically-separating-code-and-resources)
-   [Dynamisches Laden sprachspezifischer Ressourcen](#dynamically-loading-language-specific-resources)
-   [Entwickeln von MUI-Anwendungen](#building-mui-applications)

## <a name="prerequisite-for-mui"></a>Voraussetzung für MUI

Die grundlegende Voraussetzung für das Erstellen einer MUI-kompatiblen Anwendung für Windows Vista und darüber hinaus besteht darin, die Anwendung gemäß den Windows- [Globalisierungs Richtlinien](https://msdn.microsoft.com/goglobal/bb688110.aspx)zu entwerfen.

## <a name="separation-of-source-code-from-language-specific-resources"></a>Trennung des Quellcodes von sprachspezifischen Ressourcen

Eines der grundlegenden Standorte der MUI-Technologie ist die Trennung des Anwendungs Quellcodes von sprachspezifischen Ressourcen, um mehrsprachige Szenarios in Anwendungen effizienter zu gestalten. Die Trennung von Code und Ressourcen wurde durch unterschiedliche Mechanismen und in unterschiedlichen Graden erzielt, wie in den folgenden Abschnitten beschrieben. Jede Methode bietet unterschiedliche Flexibilität beim entwickeln, bereitstellen und warten der Anwendung.

Die empfohlene Lösung für MUI-kompatible Anwendungen ist die letzte hier beschriebene Methode, nämlich die physische Trennung von Quellcode und Ressourcen der Anwendung, wobei die Ressourcen selbst in eine Datei pro unterstützter Sprache aufgeteilt werden, um maximale Flexibilität beim Aufbau, bei der Bereitstellung und bei der Wartung zu erhalten.

### <a name="the-early-days-code-and-resources-live-together"></a>Die frühen Tage: Code und Ressourcen Live

Anfänglich wurden lokalisierte Anwendungen durch Bearbeiten des Quellcodes und Ändern der Ressourcen (normalerweise Zeichen folgen) im Code selbst und Neukompilieren der Anwendungen erstellt. Dies bedeutete, dass eine lokalisierte Version erstellt werden musste, um den ursprünglichen Quellcode zu kopieren, die Text (Resources)-Elemente innerhalb des Quellcodes zu übersetzen und den Code neu zu kompilieren. Die folgende Abbildung zeigt Anwendungscode mit Text, der lokalisiert werden muss.

![konzeptionelles Diagramm mit einer Anwendung, die Einheiten von eingebetteten Textressourcen enthält](images/mui-fundamental-concepts-explained-fig3.gif)

Obwohl dieser Ansatz das Erstellen lokalisierter Anwendungen ermöglicht, hat er auch erhebliche Nachteile:

-   Hierfür sind mehrere Versionen des Quellcodes erforderlich, mindestens eine für die Quellsprache und eine für jede der Zielsprachen. Hierdurch werden wichtige Probleme beim Synchronisieren der verschiedenen Sprachversionen der Anwendung verursacht. Insbesondere, wenn ein Fehler im Code korrigiert werden muss, muss der Fehler in jeder Kopie des Quellcodes (einer pro Sprache) korrigiert werden.
-   Dies ist auch äußerst fehleranfällig, da es lokalisierungssoren – die keine Entwickler sind –, Änderungen im Quellcode vorzunehmen, wodurch ein erhebliches Risiko in Bezug auf die Code Integrität entsteht.

Die Kombination dieser Nachteile macht dies zu einem äußerst ineffizienten Angebot, und es war ein besseres Modell erforderlich.

### <a name="logically-separating-code-and-localizable-resources"></a>Logische Trennung von Code und lokalisierbaren Ressourcen

Eine bedeutende Verbesserung gegenüber dem vorangehenden Modell ist die logische Trennung von Code und lokalisierbaren Ressourcen für eine Anwendung. Dadurch wird der Code von den Ressourcen isoliert, und es wird sichergestellt, dass der Code unverändert bleibt, wenn Ressourcen durch Lokalisierung geändert werden. Aus Implementierungs Sicht werden Zeichen folgen und andere Elemente der Benutzeroberfläche in Ressourcen Dateien gespeichert, die relativ einfach zu übersetzen sind und logisch von den Code Abschnitten getrennt sind.

Im Idealfall kann das Hinzufügen von Unterstützung für eine beliebige Sprache so einfach sein wie das Übersetzen der lokalisierbaren Ressourcen in diese neue Sprache und die Verwendung dieser übersetzten Ressourcen, um eine neue lokalisierte Version der Anwendung zu erstellen – ohne dass Codeänderungen erforderlich sind. In der folgenden Abbildung wird veranschaulicht, wie Code und lokalisierbare Ressourcen logisch in einer Anwendung getrennt werden sollten.

![konzeptionelles Diagramm, das eine Anwendung anzeigt, die lokalisierbare Ressourcen enthält, getrennt vom Code](images/mui-fundamental-concepts-explained-fig4.gif)

Dieses Modell ermöglicht eine einfachere Erstellung lokalisierter Versionen einer Anwendung und stellt eine bedeutende Verbesserung gegenüber dem vorherigen Modell dar. Dieses Modell, das durch die Verwendung von Tools zur Ressourcenverwaltung implementiert wurde, ist im Laufe der Jahre sehr erfolgreich und wird noch heute von vielen Anwendungen verwendet. Dies hat jedoch erhebliche Nachteile:

-   Während logisch getrennt, werden Code und lokalisierte Ressourcen in einer ausführbaren Datei weiterhin physisch verknüpft. Insbesondere ist die Wartbarkeit immer noch problematisch, da der gleiche Code Fehler (identisch in allen Sprachversionen) einen Patch pro Sprache erfordert. Wenn die Anwendung also in 20 Sprachen ausgeliefert wird, muss ein Dienst Patch 20-Mal ausgegeben werden (einer für jede Sprache), obwohl der Code nur einmal korrigiert wird.
-   Die Verteilung und Verwendung von mehrsprachigen Anwendungen wird von diesem Modell nicht ausreichend unterstützt. Dies kann in OEM-und Enterprise-Szenarios ein erhebliches Problem darstellen. Wenn ein Computer beispielsweise von zwei Benutzern mit unterschiedlichen Sprachen gemeinsam genutzt werden soll, müssen Anwendungen mit diesem Modell zweimal installiert werden, und dann muss ein Mechanismus zwischen den beiden Installationen abweichen. Dabei wird davon ausgegangen, dass keine zusätzlichen Abhängigkeiten vorhanden sind, die verhindern, dass auch dieses Szenario implementiert wird. Die folgende Abbildung zeigt ein Beispiel für einen einzelnen Code Fehler, der zwei Patches erfordert.

![konzeptionelles Diagramm, das zwei lokalisierte Anwendungen anzeigt, die denselben Code Fehler aufweisen](images/mui-fundamental-concepts-explained-fig5.gif)

Es ist klar, dass dieses Modell zwar in einigen Szenarien gut funktioniert, aber die Einschränkungen für mehrsprachige Anwendungen und ihre bereit Stellungen können sehr problematisch sein.

Eine Variation dieses Modells, bei der einige der mehrsprachigen Anwendungsprobleme behoben werden, ist das Modell, in dem lokalisierbare Ressourcen einen Satz unterschiedlicher Sprachressourcen enthalten. Dieses Modell verfügt über eine gemeinsame Codebasis und mehrere Ressourcen für verschiedene Sprachen in der gleichen Anwendung. Beispielsweise kann eine Anwendung mit Englisch, Deutsch, Französisch, Spanisch, Niederländisch und Italienisch im gleichen Paket ausgeliefert werden. Die folgende Abbildung zeigt eine Anwendung, die mehrere Sprachressourcen enthält.

![Konzeptionelle Darstellung einer Anwendung mit Code, der von zwei Gebiets Schema spezifischen Ressourcen getrennt ist](images/mui-fundamental-concepts-explained-fig6.gif)

Mit diesem Modell können Sie die Anwendung leichter bedienen, wenn ein Code Fehler korrigiert werden muss – was eine Verbesserung ist – aber nicht im Vergleich zu vorherigen Modellen, wenn es um die Unterstützung zusätzlicher Sprachen geht. In diesem Fall muss eine neue Version der Anwendung freigegeben werden (und das Release ist potenziell kompliziert, da sichergestellt werden muss, dass alle Sprachressourcen innerhalb derselben Verteilung synchronisiert werden).

### <a name="physically-separating-code-and-resources"></a>Physisches trennen von Code und Ressourcen

Der nächste evolutionäre Schritt besteht in der physischen Trennung von Code und Ressourcen. In diesem Modell werden die Ressourcen aus dem Code abstrahiert und physisch in verschiedenen Implementierungs Dateien getrennt. Dies bedeutet insbesondere, dass der Code wirklich sprachunabhängig werden kann. derselbe physische Code wird tatsächlich für alle lokalisierten Versionen einer Anwendung ausgeliefert. Die folgende Abbildung veranschaulicht, dass Code und lokalisierbare Ressourcen physisch getrennt werden müssen.

![konzeptionelles Diagramm, in dem eine Anwendung getrennt von den lokalisierbaren Ressourcen angezeigt wird](images/mui-fundamental-concepts-explained-fig7.gif)

Dieser Ansatz bietet mehrere Vorteile gegenüber den vorherigen Ansätzen:

-   Die Bereitstellung von mehrsprachigen Lösungen ist erheblich vereinfacht. Das Hinzufügen von Unterstützung für eine bestimmte Sprache erfordert nur das Versenden und Installieren eines neuen Satzes von Sprachressourcen für diese Sprache. Dies ist besonders wichtig, wenn Sprachressourcen nicht gleichzeitig verfügbar sind. Mit diesem Modell können Sie eine Anwendung in einer Reihe von Kern Sprachen bereitstellen und die Anzahl der unterstützten Sprachen im Laufe der Zeit erhöhen, ohne den eigentlichen Code ändern oder erneut bereitstellen zu müssen. Dieser Vorteil wird durch einen Fall Back Mechanismus erweitert, der die partielle Lokalisierung von Anwendungen und Systemkomponenten in einer bestimmten Sprache ermöglicht, indem sichergestellt wird, dass Ressourcen, die in dieser bevorzugten Sprache nicht gefunden werden, auf eine andere Sprache zurückgreifen, die die Benutzer ebenfalls verstehen. Insgesamt trägt dieses Modell dazu bei, den beträchtlichen Aufwand zu verringern, den globale Unternehmen bei der Bereitstellung von Anwendungen in mehreren Sprachen unterstützen, da die Bereitstellung mit einem einzelnen Image weitaus effektiver ermöglicht wird.
-   Die Serviceability wurde verbessert. Ein Code Fehler muss nur einmal korrigiert und bereitgestellt werden, da der Code vollständig Lokalisierungs unabhängig ist. Bei diesem Modell ist die Ausgabe einer Korrektur für einen Code Fehler, vorausgesetzt, die Änderung ist nicht auf die Benutzeroberfläche bezogen, wesentlich einfacher und kostengünstiger als in den vorherigen Modellen.

## <a name="dynamically-loading-language-specific-resources"></a>Dynamisches Laden sprachspezifischer Ressourcen

Die grundlegenden Konzepte für die [physische Trennung von Quellcode von sprachspezifischen Ressourcen](#physically-separating-code-and-resources)und das Entwickeln einer sprach neutralen Kern Binärdatei für eine Anwendung richten im Wesentlichen eine Architektur ein, die die Implementierung des dynamischen Ladens sprachspezifischer Ressourcen basierend auf Benutzer-und System Spracheinstellungen fördert.

Der in der sprach neutralen kernbinär Datei gebündelte Anwendungs Quell Code kann MUI-APIs in der Windows-Plattform verwenden, um die Auswahl der entsprechenden Benutzeroberflächen Sprache für einen bestimmten Kontext zu abstrahieren. MUI unterstützt Folgendes:

-   Erstellen einer priorisierten Liste von Benutzeroberflächen Sprachen auf der Grundlage von Einstellungen auf System-, Benutzer-und Anwendungsebene, Benutzerebene und Systemebene.
-   Implementieren eines Fall Back Mechanismus, der einen geeigneten Kandidaten aus dieser priorisierten Liste von Sprachen auswählt, basierend auf der Verfügbarkeit lokalisierter Ressourcen.

Das dynamische Laden von Ressourcen der Benutzeroberfläche mit einem priorisierten Fall Back bietet folgende Vorteile:

-   Sie ermöglicht die partielle Lokalisierung von Anwendungen und Systemkomponenten in einer bestimmten Sprache, da Ressourcen, die in dieser bevorzugten Sprache nicht gefunden werden, automatisch auf die nächste Sprache in der priorisierten Liste zurückgreifen.
-   Es ermöglicht Szenarien wie z. b. das dynamische wechseln von einer Sprache in eine andere.
-   Es ermöglicht das Erstellen regionaler oder weltweit einstellungsimages, die eine Reihe von Sprachen für OEMs und Unternehmen abdecken.

## <a name="building-mui-applications"></a>Entwickeln von MUI-Anwendungen

In den vorherigen Abschnitten wurden die Optionen zum Trennen von Quellcode von sprachspezifischen Ressourcen und der daraus resultierende Vorteil bei der Verwendung von Kern-APIs der Windows-Plattform für das dynamische Laden lokalisierter Ressourcen erläutert. Obwohl es sich hierbei um Richtlinien handelt, sollte darauf hingewiesen werden, dass es keine spezifische Methode gibt, eine MUI-Anwendung für die Windows-Plattform zu entwickeln.

Anwendungsentwickler haben die volle Wahl, wie Sie verschiedene Spracheinstellungen für Benutzeroberflächen, Ressourcen Erstellungs Optionen und Methoden zum Laden von Ressourcen verarbeiten. Entwickler können die in diesem Dokument bereitgestellten Richtlinien auswerten und eine Kombination auswählen, die Ihren Anforderungen und ihrer Entwicklungsumgebung entspricht.

In der folgenden Tabelle werden die verschiedenen Entwurfs Optionen zusammengefasst, die Anwendungsentwicklern zur Verfügung stehen, die eine MUI-Anwendung für die Windows-Plattform erstellen möchten.



<table>
<thead>
<tr class="header">
<th>Spracheinstellungen der Benutzeroberfläche</th>
<th>Ressourcenerstellung</th>
<th>Laden von Ressourcen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2">Befolgen Sie die Einstellungen der Benutzeroberflächen Sprache im Betriebssystem $ {Remove} $.<br />
</td>
<td>Einzelne Sprache in einer Split Resource Binary (MUI-Ressourcen Technologie)<br/> Oder<br/> Mehrere Sprachen in einer nicht aufgeteilten Ressourcen Binärdatei<br/></td>
<td>Die Anwendung ruft Standardfunktionen zum Laden von Ressourcen auf. Ressourcen werden in den Sprachen zurückgegeben, die mit den Betriebs Systemeinstellungen übereinstimmen.<br/></td>
</tr>
<tr class="even">
<td>Anwendungsspezifischer Ressourcenmechanismus<br/></td>
<td>Die Anwendung ruft die MUI-API auf, um die Thread bevorzugten Benutzeroberflächen Sprachen oder die Prozess bevorzugten Benutzeroberflächen Sprachen aus dem Betriebssystem abzurufen und diese Einstellungen zum Laden der eigenen Ressourcen zu verwenden.<br/></td>

</tr>
<tr class="odd">
<td rowspan="2">Anwendungsspezifische Einstellungen der Benutzeroberflächen Sprache $ {Remove} $<br />
</td>
<td>Einzelne Sprache in einer getrennten Ressourcen Binärdatei<br/> Oder<br/> Mehrere Sprachen in einer nicht aufgeteilten Ressourcen Binärdatei<br/></td>
<td>Die Anwendung ruft die MUI-API auf, um anwendungsspezifische UI-Sprachen oder Prozess bevorzugte Benutzeroberflächen Sprachen festzulegen, und ruft dann Standardfunktionen zum Laden von Ressourcen auf Ressourcen werden in den Sprachen zurückgegeben, die von der Anwendungs-oder Systemsprache festgelegt werden.<br/> Oder<br/> Die Anwendung testet Ressourcen in einer bestimmten Sprache und verarbeitet die eigene Ressourcen Extraktion aus den abgerufenen Binärdaten.<br/></td>
</tr>
<tr class="even">
<td>Anwendungsspezifischer Ressourcenmechanismus<br/></td>
<td>Die Anwendung verwaltet das eigene Laden von Ressourcen.<br/></td>

</tr>
</tbody>
</table>



 

 

 




