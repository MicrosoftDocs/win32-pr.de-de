---
description: Die InkAnalysis-APIs bieten Tablet PC-Entwicklern leistungsstarke Tools zum programmgesteuerten Untersuchen von Freieingaben. Die API klassifiziert Ink in aussagekräftige Kategorien wie Wörter, Linien, Absätze und Zeichnungen.
ms.assetid: d9521a8c-f61a-40ea-8603-e8afbba75a4e
title: Übersicht über die Ink-Analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3056a5e5fbff8be82f6df2de2a34fadd9761e50f451ee2d48c112589d1aff397
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718915"
---
# <a name="ink-analysis-overview"></a>Übersicht über die Ink-Analyse

Die InkAnalysis-APIs bieten Tablet PC-Entwicklern leistungsstarke Tools zum programmgesteuerten Untersuchen von Freieingaben. Die API klassifiziert Ink in aussagekräftige Kategorien wie Wörter, Linien, Absätze und Zeichnungen.

Sie können jede Klassifizierung auf verschiedene Arten verwenden, einschließlich der Verbesserung der Erkennungsergebnisse für die Handschrift.

## <a name="ink-analysis-basics"></a>Grundlagen der Ink-Analyse

In diesem Abschnitt wird die Technologie für die Ink-Analyse der Tablet PC-Plattform erläutert und erläutert, wann und wie sie verwendet wird.

Die InkAnalysis-APIs kombinieren effektiv zwei unterschiedliche, aber ergänzende Technologien: Handschrifterkennung und Layoutklassifizierung. Die Kombination dieser beiden Technologien führt definitiv zu größeren Ergebnissen als die Teile, die allein genommen werden.

Handschrifterkennung ist die Berechnungsanalyse von handschriftlichen digitalen Ink-Zeichen, um zeichenbasierte Interpretationen in einer bestimmten Sprache zurück zu geben. Die Handschrifterkennung bedeutet, dass der Computer die Handschrift einer Person "liest".

Die Ink-Analyse kann weiter in Diekklassifizierung und Layoutanalyse aufgeschlüsselt werden. Die Ink-Klassifizierung ist die berechnungsbasierte Division von Ink in semantisch sinnvolle Einheiten wie Absätze, Linien, Wörter und Zeichnungen. Bei der Layoutanalyse handelt es sich um die berechnungsbezogene Untersuchung von Ink-Eingaben, um die Position der Ink auf der Ink-Oberfläche zu bestimmen und zu bestimmen, wie die Striche räumlich und sogar semantisch miteinander in Beziehung stehen. Die Layoutanalyse kann Ihnen z. B. mitteilen, dass es sich bei einem bestimmten Ink-Teil um eine Anmerkung oder einen Aufruf handelt.

### <a name="recognition"></a>Erkennung

Ein Beispiel dafür, wie die Kombination aus Erkennung und Ink-Analyse in der InkAnalysis-API dem Entwickler hilft, ist die Verbesserung der Erkennungsergebnisse. Die Handschrifterkennungs-Engines des Tablet-PCs wurden in erster Linie für die Erkennung einer einzelnen horizontalen Linie von Ink entwickelt. Benutzer schreiben jedoch tendenziell mehrere Zeilen, wenn sie Notizen machen, und diese Zeilen sind in Bezug auf die Seite nicht garantiert horizontal. Mit der InkAnalysis-API wird die InkAnalysis-API vom Ink-Analyzer vorverarbeitet, bevor sie an die Recognizer-Funktion gesendet wird. Die analysierte Freiheit wird vor der Erkennung in horizontal transformiert, um die Erkennungsergebnisse zu verbessern.

Andere Vorteile der Erkennung werden abgeleitet, indem das Ink Analyzer falsche Strich reihenfolgeninformationen korrigiert, bevor die Ink-Klasse an die Erkennung sendet. Darüber hinaus sind Erkennungsergebnisse jetzt selektiv verfügbar. Das heißt, der Entwickler kann die Erkennungsergebnisse für ein einzelnes Wort, eine Zeile oder einen Absatz in einem Aufruf schnell abrufen.

### <a name="ink-classification"></a>Ink-Klassifizierung

Es gibt natürlich eine Vielzahl von Szenarien, in denen Sie die Ink-Daten intakt halten können, anstatt sie sofort in Text zu konvertieren. Die Ink-Analyse bietet hier auch Vorteile. Insbesondere bieten die InkAnalysis-APIs die Möglichkeit, Ink-Striche je nach Schreib- oder Zeichnungsform zu teilen. Als Schreiben klassifizierte Ink-Striche sind Striche, aus denen ein Wort oder Zeichen bestehen. Alle anderen Striche sind Zeichnungen. Dadurch erhalten Sie eine neue Möglichkeit für den Zugriff auf Ink-Daten und ermöglichen so neue Benutzerszenarien. Beispielsweise können Sie die Auswahl implementieren, sodass sie sich je nach Art des Strichs, auf den der Benutzer tippt, unterscheiden kann. Wenn ein Benutzer auf einen Schreibstrich tippt, wählt die Anwendung den gesamten Satz von Strichen aus, aus denen das Wort erstellt wird. Wenn der Benutzer auf eine Zeichnungszeichnung tippt, wählt die Anwendung nur diesen Strich aus.

### <a name="layout-analysis"></a>Layoutanalyse

Die nützliche Layoutanalyse geht tatsächlich weit über die relativ einfache Aufschlüsselung von Ink in Schreib- und Zeichnungskomponenten hinaus.

Die Ink-Analyse enthält auch eine detailliertere Aufschlüsselung der Schreib- und Zeichnungsstriche. Nehmen Sie als einfaches Beispiel ein Blob mit Ink, wie in der folgenden Abbildung dargestellt.

![zwei einfache Handschriftzeilen](images/12e7a221-59c1-4d69-b7aa-67f2caebe375.jpg)

Nachdem die Plattform diese Striche analysiert hat, gibt sie eine Strukturdarstellung dieser Striche zurück, wie in der folgenden Abbildung dargestellt. In diesem einfachen Fall enthält die Struktur nur Absatz-, Zeilen- und Wortinformationen, aber der Umfang dieser Struktur nimmt zu, wenn die Komplexität des Ink-Dokuments zunimmt.

![Strukturdarstellung von Stamm, Absatz, Zeilen und Wörtern](images/be5a7635-0abc-45ad-bcb5-98fddee5e148.jpg)

Da diese Informationen jetzt in verwaltbare Einheiten getrennt sind, können Sie jetzt leistungsfähigere Features erstellen. Beispielsweise kann die Anwendung das Feature erweitern, in dem der Benutzer tippt, um ein Wort in ein Feature auszuwählen, in dem der Benutzer einmal tippt, um das Wort auszuwählen, zweimal tippt, um die gesamte Zeile auszuwählen, und dreimal tippt, um den gesamten Absatz auszuwählen. Durch die Nutzung der vom Analysevorgang zurückgegebenen Struktur kann die Anwendung den angeknippten Bereich mit einem Strich in der Struktur in Beziehung stellen. Nachdem die Anwendung einen Strich gefunden hat, kann sie die Struktur nach oben gehen, um zu bestimmen, wie und welche benachbarten Striche ausgewählt werden müssen.

Das Auswählen einer gesamten Zeile ist ein einfaches Beispiel für die Vorteile der Ink-Analyse, aber die Möglichkeiten werden sehr gut, wenn die verschiedenen Arten von hierarchischen Strukturen berücksichtigt werden, die das Ink-Analyseprogramm erkennen kann:

-   Sortierte und ungeordnete Listen
-   Formen
-   Anmerkungskommentare, die inline mit dem Text geschrieben werden

Die Arten von Features variieren von Anwendung zu Anwendung und basieren auf den Anforderungen und den verfügbaren Freikanalyse- und Erkennungs-Engines.

### <a name="key-ink-analysis-features"></a>Wichtige Funktionen für die Ink-Analyse

Die wichtigsten Funktionen der InkAnalysis-API umfassen die folgenden Features:

-   Inkrementelle Analyse
-   Persistenz
-   Datenproxy
-   Versöhnung
-   Erweiterungen

### <a name="incremental-analysis"></a>Inkrementelle Analyse

Wenn Endbenutzer mit Ink arbeiten, behandeln sie sie in der Regel wie Handschrift. Die Freihandschrift unterliegt kontinuierlich Bearbeitungsvorgängen, z. B. dem Additionsvorgang für neue Freihandschrift, dem Löschen vorhandener Freihandschrift und der Änderung von Freihandeigenschaften, die alle auf die gleiche Weise durchgeführt werden, wie die Handschrift fortlaufend bearbeitet wird. Diese Bearbeitungsvorgänge wirken sich auf die Analyseergebnisse aus. Wenn Bearbeitungen erfolgen, können sie in der Regel zu bestimmten Zeitpunkten in Abschnitte des Dokuments isoliert werden. Angenommen, ein Benutzer schreibt fünf Zeilen Ink. Die Standardverfahren, mit denen Anwendungen Ink analysieren, sind das Warten, bis der Benutzer alle fünf Zeilen mit Ink (z. B. ein Absatz) geschrieben hat, und dann die Ergebnisse synchron oder asynchron zu analysieren.

Sie können die Gesamtzeit für die Analyse dieser fünf Zeilen optimieren, indem Sie die Bereiche isolieren, die analysiert werden, während sie geschrieben werden, und dann nur die Teile der Ergebnisse neu analysieren, die sich geändert haben. Nachdem die erste Zeile analysiert wurde, wird sie nie wieder erkannt, es sei denn, sie wird vom Endbenutzer geändert. Die Erkennung der zweiten Zeile wird als unabhängiger Erkennungsvorgang behandelt.

Dieser inkrementelle Ansatz funktioniert gut auf Zeilenebene für die Erkennungsvorgänge, muss jedoch auf einer höheren Ebene für den Ink-Analysevorgang funktionieren. Da die Ink-Analyse verschiedene Klassifizierungen auf höherer Ebene für diese fünf Ink-Zeilen erkennen kann (z. B. ein Standard-Absatz oder fünf Elemente in einer Liste), besteht der inkrementelle Ansatz für das Ink Analyzer in der Analyse dieser höheren Strukturen. Das heißt, nachdem das Ink-Analyseprogramm die erste Zeile der Ink-Klasse als Zeile klassifiziert hat, überprüft es, ob es sich immer noch um eine Zeile handelt, wenn die zweite Zeile klassifiziert wird. Das Freik-Analyseprogramm isoliert diese doppelte Überprüfung jedoch auf den Absatz und ignoriert den ersten Absatz bei der Analyse eines zweiten Absatzes und behandelt den zweiten Absatz als unabhängigen Freikanalysevorgang. Dieser inkrementelle Analyseansatz spart erheblich Verarbeitungszeit, wenn bereits große Mengen an Ink in der Anwendung vorhanden sind.

### <a name="persistence"></a>Persistenz

Die inkrementelle Analyse funktioniert gut innerhalb einer bestimmten Sitzung oder Instanz eines [**InkAnalyzer-Objekts.**](inkanalyzer.md) Die ApIs der ersten Generation der Tablet PC-Plattform können jedoch keine inkrementellen Analysen durchführen, nachdem die Freiform auf dem Datenträger beibehalten wurde. Die InkAnalysis-API ermöglicht das Speichern von Freiform auf dem Datenträger zusammen mit einer persistenten Form der Analyseergebnisse. Die Analyseergebnisse können geladen werden, wenn die Ink-Datei geladen wird, und in eine neue Instanz eines **InkAnalyzer** eingefügt werden. Eine neue Instanz des **InkAnalyzer-Objekts** hat dann denselben Ergebniszustand wie zuvor und kann jetzt alle Änderungen als inkrementelle Änderungen am vorhandenen Zustand akzeptieren, anstatt alles erneut zu analysieren.

### <a name="data-proxy"></a>Datenproxy

Viele Anwendungen verfügen bereits über eine art vorhandene Dokumentstruktur in ihren Anwendungen. z. B. ein Diagramm oder eine Datenbank. [**InkAnalyzer stellt**](inkanalyzer.md) ergebnisse auch in einer strukturierten Form in einer Struktur von [**ContextNode-Objekten**](icontextnode.md) dar. Die **InkAnalyzer-Struktur** und die vorhandene -Struktur der Anwendung müssen in zwei Richtungen zusammenarbeiten: Ergebnisse werden aus **dem InkAnalyzer in** die Anwendung gezogen, und der Zustand wird von der Anwendung in in den **InkAnalyzer** pusht.

Wenn nur das Pullen der Ergebnisse aus [**dem InkAnalyzer**](inkanalyzer.md) in die Struktur der Anwendung erforderlich wäre, wäre dies relativ einfach. Anwendungen würden die Ergebnisstruktur durch iterieren und alle benötigten Teile der Ergebnisse in ihre vorhandene Datenstruktur kopieren (integrieren). Da viele horizontale Anwendungen jedoch eine inkrementelle Analyse und Persistenz auf dem Datenträger erfordern, wird das Problem zweidirektional. Der Zustand (frühere Ergebnisse) muss aus der -Struktur der Anwendung gezogen und in **den InkAnalyzer**-Wert pusht werden.

Um diese Anforderung zu erfüllen, enthält [**der InkAnalyzer**](inkanalyzer.md) eine Reihe von Ereignissen, die er während eines Analysevorgang zum richtigen Zeitpunkt auswirft, damit Anwendungen die Anforderung von Daten an ihre vorhandenen Strukturen als Proxy senden können. Diese Ereignisse werden nur für die [**ContextNode-Objekte**](icontextnode.md) ausgelöst, die für den inkrementellen Vorgang erforderlich sind.

### <a name="reconciliation"></a>Versöhnung

Die meisten Anwendungen sollten die Ink im Hintergrund analysieren, um Unterbrechungen der Benutzeroberfläche auf ein Minimum zu beschränken. Die Analyse von Ink im Hintergrund führt jedoch zu Problemen, wenn der Benutzer die zu analysierende Ink(oder benachbarte Ink) ändert. Wenn der Benutzer z. B. die Freiform während des Hintergrundvorgang löscht, spiegelt die resultierende Struktur den Zustand des Dokuments wider, als der Hintergrundvorgang gestartet wurde, anstatt den Abschluss des Vorgangs.

Zur Unterstützung von Anwendungen gleicht [**InkAnalyzer**](inkanalyzer.md) die Unterschiede im Dokumentzustand zwischen Dem Anfang und Ende des Analysevorgang ab. Änderungen, die vom Benutzer oder der Anwendung vorgenommen werden, während die Analyse im Hintergrund ausgeführt wird, überschreiben immer die im Hintergrund berechneten Ergebnisse. Nach der Abstimmung werden nur die Teile der Ergebnisstruktur gemeldet, die nicht mit Dokumentänderungen in Konflikt stehen, und die in Konflikt stehenden Striche werden für die zukünftige Analyse markiert. Wenn der Hintergrundanalysevorgang das nächste Mal ausgeführt wird, werden die Ergebnisse basierend auf dem neuen Zustand neu berechnet.

Das folgende Diagramm zeigt diesen Prozess. Die Zeit wird linear von oben nach unten im Diagramm ausgedrückt.

![Prozess zum Abgleich von Dokumentzustandsänderungen während des Analysevorgangs](images/6323e0b5-b6b3-4adc-8c73-da3fad5b4bc2.jpg)

1.  Zum Zeitpunkt 1 (t1) erfasst die Anwendung Denkdaten vom Endbenutzer, einschließlich aller Arten von Ink-Änderungen, z. B. Hinzufügen, Entfernen oder Ändern.
2.  Bei t2 ruft die Anwendung den Hintergrundanalysevorgang auf. [**InkAnalyzer**](inkanalyzer.md) bestimmt, welche Ink-Ink keine Ergebnisse hat und welche Ink überprüft werden muss. Die erforderlichen Freihanddaten werden kopiert, damit der Hintergrundthread unabhängig ausgeführt werden kann.
3.  Bei t3 gibt [**InkAnalyzer**](inkanalyzer.md) die Threadausführung der Benutzeroberfläche an die Anwendung zurück. **InkAnalyzer** erstellt einen zweiten Thread, den Hintergrundanalysethread, und die Ink-Analyse- und Erkennungs-Engines analysieren die kopierten Ink-Daten.
4.  Während der Analysevorgang im zweiten Hintergrundthread ausgeführt wird, bearbeitet der Endbenutzer weiterhin das Dokument und fügt Strichdaten bei t4 und t5 hinzu und entfernt sie. Diese Bearbeitungen können einen Konflikt mit der Arbeit verursachen, die im Hintergrund verarbeitet wird.
5.  Bei t6 hat der Hintergrundthread den Analysevorgang abgeschlossen, und die Ergebnisse sind bereit. Bevor [**InkAnalyzer**](inkanalyzer.md) die Ergebnisse an die Anwendung übermittelt, führt er einen Abstimmungsalgorithmus aus, um zu bestimmen, ob die Änderungen des Benutzers, die während der Berechnung des Analysevorgangs vorgenommen wurden (t4 und t5), mit den Ergebnissen in Konflikt stehen. Wenn Konflikte erkannt werden, werden die kollidierenden Striche zur erneuten Analyse gekennzeichnet. Dies geschieht, wenn die Anwendung das nächste Mal den Hintergrundanalysevorgang aufruft.
6.  Bei t7 und bei allen erkannten Kollisionen stellt [**InkAnalyzer**](inkanalyzer.md) die Ergebnisse der Anwendung vor.

### <a name="extensibility"></a>Erweiterungen

Die InkAnalysis-APIs ermöglichen die Verwendung neuer Typen von Analyse-Engines durch Anwendungen, um zu verhindern, dass die Anwendung alle Vorteile der InkAnalysis-API neu schreiben muss, einschließlich Abstimmung, Datenproxy, Persistenz und inkrementelle Analyse.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Microsoft.Ink](/previous-versions/dotnet/netframework-3.5/ms581553(v=vs.90))
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 
