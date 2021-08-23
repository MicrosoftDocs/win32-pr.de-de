---
description: Die InkAnalysis-APIs bieten Tablet PC-Entwicklern leistungsstarke Tools zum programmgesteuerten Untersuchen von Freihandeingaben. Die API klassifiziert Ink in aussagekräftige Kategorien wie Wörter, Zeilen, Absätze und Zeichnungen.
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

Die InkAnalysis-APIs bieten Tablet PC-Entwicklern leistungsstarke Tools zum programmgesteuerten Untersuchen von Freihandeingaben. Die API klassifiziert Ink in aussagekräftige Kategorien wie Wörter, Zeilen, Absätze und Zeichnungen.

Sie können jede Klassifizierung auf verschiedene Weise verwenden, einschließlich der Verbesserung der Erkennungsergebnisse für handschriftliche Schreibung.

## <a name="ink-analysis-basics"></a>Grundlagen der Ink-Analyse

In diesem Abschnitt wird die Technologie für die Tablet PC Platform-Inkanalyse vorgestellt, und es wird erläutert, wann und wie Sie sie verwenden.

Die InkAnalysis-APIs kombinieren effektiv zwei unterschiedliche, aber ergänzende Technologien: Handschrifterkennung und Layoutklassifizierung. Die Kombination dieser beiden Technologien liefert definitiv bessere Ergebnisse als die Teile, die allein genommen werden.

Bei der Handschrifterkennung handelt es sich um die Berechnungsanalyse von handschriftlichem freihandgeschriebener Freihandhand, um zeichenbasierte Interpretationen in einer bestimmten Sprache zurückzugeben. Das heißt, die Handschrifterkennung ist, wie der Computer die Handschrift einer Person "liest".

Die Ink-Analyse kann weiter in Diekklassifizierung und Layoutanalyse unterteilt werden. Die Ink-Klassifizierung ist die berechnungsbasierte Aufteilung von Ink in semantisch aussagekräftige Einheiten wie Absätze, Zeilen, Wörter und Zeichnungen. Die Layoutanalyse ist die berechnungsbezogene Untersuchung der Ink-Eingabe, um die Position der Ink auf der Belagsoberfläche zu bestimmen und zu bestimmen, wie die Striche räumlich und sogar semantisch miteinander in Beziehung stehen. Die Layoutanalyse kann Ihnen beispielsweise mitteilen, dass es sich bei einem bestimmten Freihandelement um eine Anmerkung oder einen Aufruf handelt.

### <a name="recognition"></a>Erkennung

Ein Beispiel dafür, wie die Kombination aus Erkennung und Ink-Analyse in der InkAnalysis-API dem Entwickler hilft, ist die Verbesserung der Erkennungsergebnisse. Die Handschrifterkennungs-Engines für Tablet PC wurden in erster Linie entwickelt, um eine einzelne horizontale Freihandzeile zu erkennen. Personen schreiben jedoch in der Regel mehrere Zeilen, wenn sie Notizen machen, und diese Zeilen sind in Bezug auf die Seite nicht garantiert horizontal. Mit der InkAnalysis-API wird Ink vom Ink-Analyseprogramm vorverarbeitet, bevor sie an die Erkennung gesendet wird. Die analysierte Ink-Datei wird vor der Erkennung in horizontal transformiert, wodurch die Erkennungsergebnisse verbessert werden.

Andere Vorteile der Erkennung ergeben sich, indem das Ink-Analyseprogramm falsche Informationen zur Strichreihenfolge korrigiert, bevor die Ink an die Erkennung gesendet wird. Darüber hinaus sind Erkennungsergebnisse jetzt selektiv verfügbar. Das heißt, der Entwickler kann die Erkennungsergebnisse für ein einzelnes Wort, eine Zeile oder einen Absatz in einem Aufruf schnell abrufen.

### <a name="ink-classification"></a>Klassifizierung von Ink

Es gibt natürlich eine Vielzahl von Szenarien, in denen Sie die Ink-Daten intakt halten können, anstatt sie sofort in Text zu konvertieren. Die Ink-Analyse bietet auch hier Vorteile. Insbesondere bieten die InkAnalysis-APIs die Möglichkeit, Ink-Striche je nach Schreib- oder Zeichnungsform aufzuteilen. Ink-Striche, die als Schreiben klassifiziert sind, sind solche, aus denen ein Wort oder Zeichen bestehen. Alle anderen Striche sind Zeichnungen. Dadurch erhalten Sie eine neue Möglichkeit, auf Freihanddaten zuzugreifen und neue Benutzerszenarien zu ermöglichen. Beispielsweise können Sie die Auswahl implementieren, sodass sie sich je nach Typ des Strichs unterscheidet, auf den der Benutzer tippt. Wenn ein Benutzer auf einen Schreibstrich tippt, wählt die Anwendung die gesamte Gruppe von Strichen aus, aus denen das Wort besteht. Wenn der Benutzer auf einen Zeichnungsstrich tippt, wählt die Anwendung nur diesen Strich aus.

### <a name="layout-analysis"></a>Layoutanalyse

Die nützliche Layoutanalyse geht tatsächlich weit über die relativ einfache Aufschlüsselung von Ink in Schreib- und Zeichnungskomponenten hinaus.

Die Ink-Analyse umfasst auch eine umfangreichere Aufschlüsselung der Schreib- und Zeichnungsstriche. Nehmen Sie als sehr einfaches Beispiel ein Blob mit Ink, wie in der folgenden Abbildung dargestellt.

![zwei einfache Handschriftzeilen](images/12e7a221-59c1-4d69-b7aa-67f2caebe375.jpg)

Nachdem die Plattform diese Striche analysiert hat, gibt sie eine Strukturdarstellung dieser Striche zurück, wie in der folgenden Abbildung dargestellt. In diesem einfachen Fall enthält die Struktur nur Absatz-, Zeilen- und Wortinformationen, aber der Umfang dieser Struktur nimmt mit zunehmender Komplexität des Ink-Dokuments zu.

![Strukturdarstellung von Stamm, Absatz, Zeilen und Wörtern](images/be5a7635-0abc-45ad-bcb5-98fddee5e148.jpg)

Da diese Informationen jetzt in verwaltbare Einheiten unterteilt sind, können Sie jetzt leistungsfähigere Features erstellen. Beispielsweise kann die Anwendung das Feature erweitern, in dem der Benutzer tippt, um ein Wort in ein Feature auszuwählen, in dem der Benutzer einmal tippt, um das Wort auszuwählen, zweimal tippt, um die gesamte Zeile auszuwählen, und dreimal tippt, um den gesamten Absatz auszuwählen. Indem die vom Analysevorgang zurückgegebene Struktur genutzt wird, kann die Anwendung den angetippten Bereich mit einem Strich in der Struktur verknüpfen. Nachdem die Anwendung einen Strich gefunden hat, kann sie die Struktur nach oben durchgehen, um zu bestimmen, wie und welche benachbarten Striche ausgewählt werden sollen.

Die Auswahl einer ganzen Zeile ist ein einfaches Beispiel für die Vorteile der Freihandanalyse, aber die Möglichkeiten werden hervorragend, wenn die verschiedenen Typen hierarchischer Strukturen berücksichtigt werden, die das Freihandanalyse-Analyseprogramm erkennen kann:

-   Sortierte und unsortierte Listen
-   Formen
-   Anmerkungen zu Kommentaren, die inline mit dem Text geschrieben wurden

Die Arten von Features variieren von Anwendung zu Anwendung und basieren auf den Anforderungen und den verfügbaren Freihandanalyse- und Erkennungs-Engines.

### <a name="key-ink-analysis-features"></a>Wichtige Funktionen für die Ink-Analyse

Die wichtigsten Funktionen der InkAnalysis-API umfassen die folgenden Features:

-   Inkrementelle Analyse
-   Persistenz
-   Datenproxy
-   Versöhnung
-   Erweiterungen

### <a name="incremental-analysis"></a>Inkrementelle Analyse

Wenn Endbenutzer mit Freihandhand arbeiten, behandeln sie dies in der Regel wie Handschrift. Die Freihandeingabe unterliegt kontinuierlich Bearbeitungsvorgängen, z. B. dem Hinzufügen neuer Freihandeingaben, dem Löschen vorhandener Freihandeingaben und der Änderung von Freihandeigenschaften, die alle auf die gleiche Weise ausgeführt werden, wie die Handschrift kontinuierlich bearbeitet wird. Diese Bearbeitungsvorgänge wirken sich auf die Analyseergebnisse aus. Wenn Änderungen vorgenommen werden, können sie in der Regel zu bestimmten Zeitpunkten in Abschnitten des Dokuments isoliert werden. Angenommen, ein Benutzer schreibt fünf Zeilen Ink. Die Standardform, mit der Anwendungen Freihanddaten analysieren, besteht darin, zu warten, bis der Benutzer alle fünf Freihandzeilen ( z. B. einen Absatz) geschrieben hat, und dann die Ergebnisse entweder synchron oder asynchron zu analysieren.

Sie können die gesamte Zeit für die Analyse dieser fünf Zeilen optimieren, indem Sie die Bereiche isolieren, die beim Schreiben analysiert werden, und dann nur die Teile der Ergebnisse neu analysieren, die sich geändert haben. Nachdem die erste Zeile analysiert wurde, wird sie nie wieder erkannt, es sei denn, sie wird vom Endbenutzer geändert. Die Erkennung der zweiten Zeile wird als unabhängiger Erkennungsvorgang behandelt.

Dieser inkrementelle Ansatz funktioniert gut auf Zeilenebene für die Erkennungsvorgänge, muss aber auf einer höheren Ebene für den Ink-Analysevorgang funktionieren. Da das Ink-Analyseprogramm verschiedene Klassifizierungen auf höherer Ebene für diese fünf Ink-Zeilen erkennen kann (z. B. ein Standard absatz oder fünf Elemente in einer Liste), besteht der inkrementelle Ansatz für das Ink-Analyseprogramm darin, dass es diese höheren Strukturen analysieren muss. Das heißt, nachdem das Ink-Analyseprogramm die erste Zeile der Ink als Zeile klassifiziert hat, überprüft es doppelt, ob es sich noch um eine Zeile handelt, wenn es die zweite Zeile klassifiziert. Das Freihandanalyseprogramm isoliert diese doppelte Überprüfung jedoch auf den Absatz und ignoriert den ersten Absatz bei der Analyse eines zweiten Absatzes und behandelt den zweiten Absatz als unabhängigen Freihandanalysevorgang. Dieser inkrementelle Analyseansatz spart erheblich Verarbeitungszeit, wenn in der Anwendung bereits große Mengen an Ink vorhanden sind.

### <a name="persistence"></a>Persistenz

Die inkrementelle Analyse funktioniert gut innerhalb einer bestimmten Sitzung oder Instanz eines [**InkAnalyzer-Objekts.**](inkanalyzer.md) Die TABLET PC Platform-APIs der ersten Generation können jedoch keine inkrementelle Analyse durchführen, nachdem die Freihand auf dem Datenträger beibehalten wurde. Die InkAnalysis-API ermöglicht das Speichern von Freihanddaten auf dem Datenträger zusammen mit einer persistenten Form der Analyseergebnisse. Die Analyseergebnisse können geladen werden, wenn die Ink geladen wird, und sie können in eine neue Instanz eines **InkAnalyzer** eingefügt werden. Eine neue Instanz des **InkAnalyzer-Objekts** hat dann den gleichen Ergebniszustand wie zuvor und kann nun alle Änderungen als inkrementelle Änderungen am vorhandenen Zustand akzeptieren, anstatt alles erneut zu analysieren.

### <a name="data-proxy"></a>Datenproxy

Viele Anwendungen verfügen bereits über eine art vorhandene Dokumentstruktur in ihren Anwendungen. z. B. ein Diagramm oder eine Datenbank. [**InkAnalyzer**](inkanalyzer.md) stellt ergebnisse auch in einer strukturierten Form in einer Struktur von [**ContextNode-Objekten**](icontextnode.md) dar. Die **InkAnalyzer-Struktur** und die vorhandene -Struktur der Anwendung müssen in zwei Richtungen zusammenarbeiten: Ergebnisse werden aus dem **InkAnalyzer** in die Anwendung gepusht, und der Zustand wird von der Anwendung in **den InkAnalyzer** gepusht.

Wenn das Abrufen der Ergebnisse aus [**InkAnalyzer**](inkanalyzer.md) in die Struktur der Anwendung erforderlich wäre, wäre dies relativ einfach. Anwendungen durchlaufen die Ergebnisstruktur und kopieren (integrieren) alle benötigten Ergebnisse in ihre vorhandene Datenstruktur. Da viele horizontale Anwendungen jedoch eine inkrementelle Analyse und Persistenz auf dem Datenträger erfordern, wird das Problem zweidirektional. Der Zustand (frühere Ergebnisse) muss aus der Struktur der Anwendung abgerufen und in **den InkAnalyzer gepusht** werden.

Um diese Anforderung zu erfüllen, enthält [**inkAnalyzer**](inkanalyzer.md) eine Reihe von Ereignissen, die während eines Analysevorgangs zum entsprechenden Zeitpunkt auslöst werden, damit Anwendungen die Anforderung für Daten an ihre vorhandenen Strukturen zurücksproxyn können. Diese Ereignisse werden nur für die [**ContextNode-Objekte**](icontextnode.md) ausgelöst, die für den inkrementellen Vorgang erforderlich sind.

### <a name="reconciliation"></a>Versöhnung

Die meisten Anwendungen möchten die Ink im Hintergrund analysieren, um Unterbrechungen der Benutzeroberfläche auf ein Minimum zu beschränken. Die Analyse von Ink im Hintergrund verursacht jedoch Probleme, wenn der Benutzer die zu analysierende Ink (oder benachbarte Ink) ändert. Wenn der Benutzer z. B. die Freihand während des Hintergrundvorgangs löscht, spiegelt die resultierende Struktur den Zustand des Dokuments wider, als der Hintergrundvorgang gestartet wurde, anstatt zu dem Zeitpunkt, zu dem er abgeschlossen wurde.

Zur Unterstützung von Anwendungen stimmen [**InkAnalyzer**](inkanalyzer.md) die Unterschiede im Dokumentzustand zwischen Dem Anfang und Ende des Analysevorgangs ab. Änderungen, die vom Benutzer oder der Anwendung vorgenommen werden, während die Analyse im Hintergrund ausgeführt wird, setzen immer die im Hintergrund berechneten Ergebnisse außer Kraft. Nach dem Abgleich werden nur die Teile der Ergebnisstruktur gemeldet, die nicht mit Dokumentänderungen in Konflikt stehen, und die in Konflikt stehenden Striche werden für die zukünftige Analyse gekennzeichnet. Wenn der Hintergrundanalysevorgang das nächste Mal ausgeführt wird, werden die Ergebnisse basierend auf dem neuen Zustand neu berechnet.

Das folgende Diagramm zeigt diesen Prozess. Die Zeit wird im Diagramm linear von oben nach unten ausgedrückt.

![Prozess zum Abgleichen von Dokumentzustandsänderungen während des Analysevorgangs](images/6323e0b5-b6b3-4adc-8c73-da3fad5b4bc2.jpg)

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

 

 
