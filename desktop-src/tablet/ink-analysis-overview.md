---
description: Die InkAnalysis-APIs bieten Tablet PC-Entwicklern leistungsstarke Tools für die programmgesteuerte Untersuchung von frei Hand Eingaben. Die API klassifiziert Freihand Eingaben in sinnvolle Kategorien, wie z. b. Wörter, Zeilen, Absätze und Zeichnungen.
ms.assetid: d9521a8c-f61a-40ea-8603-e8afbba75a4e
title: Übersicht über die Link Analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e383d16c01cd9475d4c54587b4b5fb4c09791a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525310"
---
# <a name="ink-analysis-overview"></a>Übersicht über die Link Analyse

Die InkAnalysis-APIs bieten Tablet PC-Entwicklern leistungsstarke Tools für die programmgesteuerte Untersuchung von frei Hand Eingaben. Die API klassifiziert Freihand Eingaben in sinnvolle Kategorien, wie z. b. Wörter, Zeilen, Absätze und Zeichnungen.

Sie können jede Klassifizierung auf verschiedene Weise verwenden, einschließlich der Verbesserung der Erkennungsergebnisse für Handschrift.

## <a name="ink-analysis-basics"></a>Grundlagen der Grundlagen

In diesem Abschnitt wird die Tablet PC Platform Ink Analysis-Technologie vorgestellt und erläutert, wann und wie Sie verwendet werden.

Die InkAnalysis-APIs kombinieren effektiv zwei unterschiedliche, aber kostenlose Technologien: Handschrifterkennung und layoutklassifizierung. Die Kombination dieser beiden Technologien ergibt definitiv größere Ergebnisse als die eigenständigen Teile.

Die Handschrifterkennung ist die Berechnungs Analyse von Hand schriftlichem digitalen Ink, um zeichenbasierte Interpretation in einer bestimmten Sprache zurückzugeben. Das heißt, die Handschrifterkennung gibt an, wie der Computer die Handschrift einer Person liest.

Die frei Hand Analyse kann weiter in die frei Hand Klassifizierung und Layoutanalyse aufgeteilt werden. Die frei Hand Klassifizierung ist die Berechnungs Abteilung von frei Hand Eingaben in semantisch sinnvolle Einheiten, wie z. b. Absätze, Linien, Wörter und Zeichnungen. Bei der Layoutanalyse handelt es sich um die Berechnungs Prüfung von frei Hand Eingaben, um die Position der frei Hand Eingaben auf der Erstellungs Oberfläche und die Beziehung zwischen den Strichen räumlich und sogar semantisch zu bestimmen. Beispielsweise können Sie mit der Layoutanalyse feststellen, dass ein bestimmtes frei Hand Element eine Anmerkung oder ein aufrufungs Element ist.

### <a name="recognition"></a>Erkennung

Ein Beispiel dafür, wie die Kombination aus Erkennung und frei Hand Analyse in der InkAnalysis-API dem Entwickler die Verbesserung der Erkennungsergebnisse erleichtert. Die Tablet PC-Handschrifterkennungs-Engines wurden in erster Linie so entworfen, dass Sie eine einzelne horizontale Handschrift erkennen Allerdings neigen Benutzer dazu, bei der Aufnahme von Notizen mehrere Zeilen zu schreiben, und diese Zeilen sind nicht unbedingt horizontal in Bezug auf die Seite. Mit der InkAnalysis-API wird Ink vor dem Senden an die Erkennung vom Ink Analyzer vorverarbeitet. Die analysierte frei Hand Eingaben werden vor dem erkennen in den horizontalen transformiert und verbessern die Erkennungsergebnisse.

Andere Vorteile für die Erkennung werden dadurch abgeleitet, dass der Ink-Analyzer falsche Informationen zur hubreihenfolge korrigiert, bevor die frei Hand Eingaben an die Erkennung gesendet werden. Außerdem sind Erkennungsergebnisse jetzt auf selektive Weise verfügbar. Das heißt, der Entwickler kann die Erkennungsergebnisse für ein einzelnes Wort, eine Zeile oder einen Absatz innerhalb eines Aufrufes schnell abrufen.

### <a name="ink-classification"></a>Ink-Klassifizierung

Es gibt natürlich eine Reihe von Szenarios, in denen Sie die frei Hand Daten intakt halten können, anstatt Sie direkt in Text umzuwandeln. Die frei Hand Analyse bietet auch hier Vorteile. Die InkAnalysis-APIs bieten die Möglichkeit, frei Hand Eingaben abhängig davon aufzuteilen, ob Sie geschrieben werden. Hand Striche, die als Schreibvorgänge klassifiziert werden, sind diejenigen, die ein Wort oder Zeichen bilden. Alle anderen Striche sind Zeichnungen. Dadurch erhalten Sie eine neue Möglichkeit, auf frei Hand Daten zuzugreifen und neue Benutzer Szenarien zu ermöglichen. Beispielsweise können Sie die Auswahl so implementieren, dass Sie je nach Art des Strichs, auf den der Benutzer tippt, unterschiedlich ist. Wenn ein Benutzer auf einen schreibstrich tippt, wählt die Anwendung den gesamten Satz von Strichen aus, die das Wort bilden. wenn der Benutzer auf einen Zeichnungs-Stoke tippt, wählt die Anwendung nur diesen Strich aus.

### <a name="layout-analysis"></a>Layoutanalyse

Die nützliche Layoutanalyse geht weit über die relativ einfache Aufteilung von frei Hand Eingaben in das Schreiben und Zeichnen von Komponenten hinaus.

Die frei Hand Analyse umfasst auch eine umfangreichere Aufschlüsselung der Schreib-und Zeichnungs Striche. Nehmen Sie als einfaches Beispiel ein BLOB frei, wie in der folgenden Abbildung dargestellt.

![zwei einfache Handschrift Zeilen](images/12e7a221-59c1-4d69-b7aa-67f2caebe375.jpg)

Nachdem die Plattform diese Striche analysiert hat, gibt Sie eine Struktur Darstellung dieser Striche zurück, wie in der folgenden Abbildung dargestellt. In diesem einfachen Fall enthält die Struktur nur Absatz-, Zeilen-und Wort Informationen, die Komplexität dieser Struktur nimmt jedoch zu, wenn sich die Komplexität des frei Hand Dokuments erhöht.

![Struktur Darstellung von Stamm, Absatz, Zeilen und Wörtern](images/be5a7635-0abc-45ad-bcb5-98fddee5e148.jpg)

Da diese Informationen jetzt in verwaltbare Einheiten voneinander getrennt sind, können Sie jetzt leistungsfähigere Funktionen erstellen. Die Anwendung kann z. b. die Funktion erweitern, auf die der Benutzer tippt, um ein Wort in eine Funktion auszuwählen, auf die der Benutzer einmal tippt, um das Wort auszuwählen, zweimal tippt, um die gesamte Zeile auszuwählen, und dreimal tippt, um den gesamten Absatz auszuwählen. Durch die Nutzung der Struktur, die vom Analyse Vorgang zurückgegeben wird, kann die Anwendung den gezapften Bereich wieder mit einem Strich in der Struktur verknüpfen. Nachdem die Anwendung einen Strich gefunden hat, kann Sie die Struktur durchlaufen, um zu bestimmen, wie und welche benachbarten Striche ausgewählt werden sollen.

Die Auswahl einer ganzen Zeile ist ein vereinfachtes Beispiel für die Vorteile der frei Hand Analyse, aber die Möglichkeiten sind hervorragend, wenn Sie die verschiedenen Arten von hierarchischen Strukturen berücksichtigen, die der Ink Analyzer erkennen kann:

-   Geordnete und ungeordnete Listen
-   Formen
-   Anmerkungen, die Inline in den Text geschrieben wurden

Die Funktionstypen unterscheiden sich von der Anwendung bis zur Anwendung und basieren auf den Anforderungen und den verfügbaren Freihand-Analyse-und Erkennungs Modulen.

### <a name="key-ink-analysis-features"></a>Features der keyink-Analyse

Die wichtigsten Funktionen der InkAnalysis-API sind die folgenden Features:

-   Krementelle Analyse
-   Persistenz
-   Daten Proxy
-   Ö
-   Erweiterungen

### <a name="incremental-analysis"></a>Krementelle Analyse

Wenn Endbenutzer mit Freihand arbeiten, behandeln Sie Sie in der Regel wie Handschrift. Die frei Hand Eingaben unterliegen kontinuierlichen Bearbeitungsvorgängen, wie z. b. das Hinzufügen neuer Freihand, das Löschen vorhandener frei Hand Eingaben und das Ändern von frei handeigenschaften. alle werden auf die gleiche Weise ausgeführt wie die Handschrift. Diese Bearbeitungsvorgänge wirken sich auf die Analyseergebnisse aus. Wenn Änderungen auftreten, können Sie normalerweise zu bestimmten Zeitpunkten in den Abschnitten des Dokuments isoliert werden. Nehmen Sie beispielsweise an, dass ein Benutzer fünf Zeilen freigibt. Die standardmäßige Art und Weise, in der Anwendungen frei Hand Eingaben analysieren, besteht darin, zu warten, bis der Benutzer alle fünf Zeilen mit Freihand schreibt – beispielsweise einen Absatz – und anschließend die Ergebnisse entweder synchron oder asynchron zu analysieren.

Sie können die Gesamtzeit für das Analysieren dieser fünf Zeilen optimieren, indem Sie die Bereiche isolieren, die beim Schreiben analysiert werden, und dann nur die Teile der geänderten Ergebnisse erneut analysieren. Nachdem die erste Zeile analysiert wurde, wird Sie nie wiedererkannt, es sei denn, Sie wird vom Endbenutzer geändert. Das Erkennen der zweiten Zeile wird als unabhängiger Erkennungs Vorgang behandelt.

Dieser inkrementelle Ansatz funktioniert auf der Zeilenebene für die Erkennungs Vorgänge, aber er muss auf einer höheren Ebene für den Ink-Analyse Vorgang funktionieren. Da der Ink Analyzer verschiedene Klassifizierungen höherer Ebene für diese fünf Zeilen von frei Hand Eingaben erkennen kann (z. b. ein Standard Absatz oder fünf Elemente in einer Liste), besteht der inkrementelle Ansatz für die frei Hand Analyse darin, dass diese höheren Strukturen analysiert werden müssen. Das heißt, nachdem die frei Hand Analyse die erste Zeile frei Hand Eingaben als Linie klassifiziert hat, überprüft Sie, ob Sie immer noch eine Linie ist, wenn die zweite Zeile klassifiziert wird. Der Ink Analyzer isoliert diese doppelte Prüfung jedoch auf den Absatz und ignoriert den ersten Absatz, wenn ein zweiter Absatz analysiert wird, wobei der zweite Absatz als unabhängiger Ink Analyzer-Vorgang behandelt wird. Diese inkrementelle Vorgehensweise bei der Analyse spart die Verarbeitungszeit erheblich, wenn in der Anwendung bereits große Mengen freigegeben wurden.

### <a name="persistence"></a>Persistenz

Die inkrementelle Analyse funktioniert gut innerhalb einer bestimmten Sitzung oder Instanz eines [**InkAnalyzer**](inkanalyzer.md) -Objekts. Die APIs der Tablet PC-Plattform der ersten Generation können jedoch keine inkrementelle Analyse durchführen Die InkAnalysis-API ermöglicht das Speichern von frei Hand Eingaben auf einem Datenträger zusammen mit einer permanenten Form der Analyseergebnisse. Die Analyseergebnisse können geladen werden, wenn die frei Hand Eingaben geladen werden und in eine neue Instanz eines **inkanalyzers** eingefügt werden können. Eine neue Instanz des **InkAnalyzer** -Objekts hat dann denselben Ergebnis Zustand wie zuvor, und kann nun Änderungen als inkrementelle Änderungen am vorhandenen Zustand akzeptieren, anstatt alles erneut zu analysieren.

### <a name="data-proxy"></a>Daten Proxy

Viele Anwendungen verfügen bereits über eine Art vorhandener Dokumentstruktur in Ihren Anwendungen. beispielsweise ein Diagramm oder eine Datenbank. Der [**InkAnalyzer**](inkanalyzer.md) zeigt auch Ergebnisse in einer strukturierten Form in einer Struktur von [**ContextNode**](icontextnode.md) -Objekten an. Die **InkAnalyzer** -Struktur und die vorhandene Struktur der Anwendung müssen in zwei Richtungen interagiert werden: Ergebnisse werden aus dem **InkAnalyzer** in die Anwendung abgerufen, und der Zustand wird von der Anwendung in den **InkAnalyzer** übertragen.

Wenn die Ergebnisse aus dem [**InkAnalyzer**](inkanalyzer.md) -Element in die Struktur der Anwendung übertragen wurden, wäre es relativ einfach. Anwendungen durchlaufen die Ergebnis Struktur und kopieren (integrieren) alle Teile der Ergebnisse, die Sie benötigen, in Ihre vorhandene Datenstruktur. Da viele horizontale Anwendungen jedoch eine inkrementelle Analyse und Persistenz auf dem Datenträger erfordern, wird das Problem zweifach direktional. State (vergangene Ergebnisse) muss aus der Struktur der Anwendung abgerufen und in den **InkAnalyzer** übertragen werden.

Um diese Anforderung zu erfüllen, enthält der [**InkAnalyzer**](inkanalyzer.md) eine Reihe von Ereignissen, die er zur entsprechenden Zeit während eines Analyse Vorgangs auslöst, damit Anwendungen die Anforderung von Daten an die vorhandenen Strukturen zurückgeben können. Diese Ereignisse werden nur für die [**ContextNode**](icontextnode.md) -Objekte ausgelöst, die für den inkrementellen Vorgang erforderlich sind.

### <a name="reconciliation"></a>Ö

Die meisten Anwendungen sollten die frei Hand Eingaben im Hintergrund analysieren, damit die Benutzeroberflächen Unterbrechungen minimal bleiben. Das Analysieren von frei Hand Eingaben im Hintergrund verursacht jedoch Probleme, wenn der Benutzer die zu analysierende frei Hand Eingabe (oder die benachbarte frei Hand Eingabe) ändert. Wenn der Benutzer z. b. die frei Hand Eingabe während des Hintergrund Vorgangs löscht, würde die resultierende Struktur den Status des Dokuments widerspiegeln, wenn der Hintergrund Vorgang gestartet wurde, und nicht, als er abgeschlossen wurde.

Um Anwendungen zu unterstützen, gleicht der [**InkAnalyzer**](inkanalyzer.md) die Unterschiede im Dokument Zustand zwischen dem Anfang und dem Ende des Analyse Vorgangs ab. Änderungen, die vom Benutzer oder der Anwendung vorgenommen werden, während die Analyse im Hintergrund ausgeführt wird, überschreiben immer die im Hintergrund berechneten Ergebnisse. Nach der Abstimmung werden nur die Teile der Ergebnis Struktur, die nicht mit Dokument Änderungen in Konflikt stehen, gemeldet, und die in Konflikt stehenden Striche werden für eine zukünftige Analyse gekennzeichnet. Bei der nächsten Ausführung des Hintergrundanalyse Vorgangs werden die Ergebnisse basierend auf dem neuen Status neu berechnet.

Dieses Verfahren wird im folgenden Diagramm veranschaulicht. Die Zeit wird linear von oben nach unten im Diagramm ausgedrückt.

![Prozess zum Abstimmen von Dokument Zustandsänderungen während des Analyse Vorgangs](images/6323e0b5-b6b3-4adc-8c73-da3fad5b4bc2.jpg)

1.  Zum Zeitpunkt 1 (T1) sammelt die Anwendung frei Hand Eingaben vom Endbenutzer, einschließlich aller Arten von Handschrift Änderungen, z. b. hinzufügen, entfernen oder ändern.
2.  Bei T2 Ruft die Anwendung den Hintergrundanalyse Vorgang auf. Der [**InkAnalyzer**](inkanalyzer.md) bestimmt, welche frei Hand Eingaben keine Ergebnisse aufweisen und welche frei Hand Eingaben überprüft werden müssen. Die erforderlichen frei Hand Daten werden kopiert, damit der Hintergrund Thread unabhängig ausgeführt werden kann.
3.  Bei T3 gibt der [**InkAnalyzer**](inkanalyzer.md) die Thread Ausführung der Benutzeroberfläche an die Anwendung zurück. Der **InkAnalyzer** erstellt einen zweiten Thread, den Thread für die Hintergrundanalyse, und die Freihand-und Erkennungs-Engines analysieren die kopierten frei Hand Daten.
4.  Während der Analyse Vorgang im zweiten Hintergrund Thread durchgeführt wird, wird der Endbenutzer weiterhin das Dokument bearbeiten und die Strich Daten bei T4 und T5 hinzufügen und entfernen. Diese Änderungen können mit der Arbeit in Konflikt stehen, die im Hintergrund verarbeitet wird.
5.  Bei T6 hat der Hintergrund Thread den Analyse Vorgang abgeschlossen, und die Ergebnisse sind bereit. Bevor der [**InkAnalyzer**](inkanalyzer.md) die Ergebnisse an die Anwendung übermittelt, führt er einen Versöhnungs Algorithmus aus, um zu bestimmen, ob die Benutzer Änderungen während der Berechnung des Analyse Vorgangs (T4 und T5) mit den Ergebnissen durchgeführt wurden. Wenn Konflikte erkannt werden, werden die Konflikt enden Striche für die erneute Analyse gekennzeichnet, was beim nächsten Aufrufen der Hintergrundanalyse durch die Anwendung erfolgt.
6.  Schließlich zeigt der [**InkAnalyzer**](inkanalyzer.md) bei T7 mit allen gefundenen Kollisionen die Ergebnisse der Anwendung an.

### <a name="extensibility"></a>Erweiterungen

Mithilfe der InkAnalysis-APIs können neue Arten von Analysemodulen von Anwendungen verwendet werden, um zu verhindern, dass die Anwendung alle Vorteile der InkAnalysis-API neu schreiben muss, einschließlich der Abstimmung, des Daten Proxys, der Persistenz und der inkrementellen Analyse.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Microsoft. Ink](/previous-versions/dotnet/netframework-3.5/ms581553(v=vs.90))
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 
