---
description: In diesem Thema werden die grundlegenden Aspekte für agglutinative Sprachen und Unicode-Ersatz Zeichenpaare beschrieben, und Sie können Ersatzpaare verwenden, um den Unicode-Zeichensatz auf verschiedene Zeichensätze zu erweitern.
ms.assetid: 7104b2da-2ece-46ce-b4ca-6c24dc4d6677
title: Verschiedene linguistische und Unicode-Überlegungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8433fb212917f29acbc2347c3324668a77533dee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041622"
---
# <a name="miscellaneous-linguistic-and-unicode-considerations"></a>Verschiedene linguistische und Unicode-Überlegungen

In diesem Thema werden die grundlegenden Aspekte für agglutinative Sprachen und Unicode-Ersatz Zeichenpaare beschrieben, und Sie können Ersatzpaare verwenden, um den Unicode-Zeichensatz auf verschiedene Zeichensätze zu erweitern. In diesem Thema wird auch beschrieben, wie Wörter Trennungen Text in Text identifizieren und nicht brechende Leerzeichen verarbeiten. Außerdem wird erläutert, wie Wörter Trennungen und Wort Stamm Erkennungen Zahlen und Datumsangaben, Verbund Wörter, zusammengesetzte Ausdrücke, sonderwörter und Zeichen, Akronyme und Abkürzungen sowie die groß-

Dieses Thema ist wie folgt organisiert:

-   [Ausdrucks Identifikation](#phrase-identification)
-   [Agglutinative Sprachen](#agglutinative-languages)
-   [Zahlen, Uhrzeiten und Datumsangaben](#numbers-times-and-dates)
-   [Zusammengesetzte Wörter](#compound-words)
-   [Zusammengesetzte Ausdrücke](#compound-phrases)
-   [Sonderzeichen und Wörter](#special-characters-and-words)
-   [Akronyme und Abkürzungen](#acronyms-and-abbreviations)
-   [Großbuchstaben](#capitalization)
-   [Nicht brechende Leerzeichen](#nonbreaking-spaces)
-   [Ersatz Zeichenpaare](#surrogate-pairs)

## <a name="phrase-identification"></a>Ausdrucks Identifikation

Ausdrücke sind ein Wort oder eine Gruppe von Wörtern, die von einem oder mehreren anderen Personen geändert werden. Ausdrücke können nur schwer konsistent identifiziert werden, da derselbe Modifizierer in mehr als einem Ausdruck mit demselben Substantiv verwendet werden kann. Z. b. "New House", "House of das Parlament", "New House of Bundestag".

Windows Search verwendet Ausdrücke, die am häufigsten zur Abfragezeit verwendet werden. Ausdrücke im Abfragetext erhalten eine höhere Gewichtung als einzelne Wörter. Im vorherigen Beispiel hat ein Dokument mit dem Wort "House of das Parlament" eine höhere Rangfolge als eins, das "House" und "Bundestag" an verschiedenen Punkten im Dokument enthält. Es wird empfohlen, dass Wörter Trennungen einen Ausdruck zur Abfragezeit generieren, wenn der Ausdruck wahrscheinlich mindestens einem Dokument entspricht.

## <a name="agglutinative-languages"></a>Agglutinative Sprachen

Agglutinative Sprachen bilden Wörter durch die Kombination kleinerer Morphen, um zusammengesetzte Ideen auszudrücken. Jede dieser Morphen hat im Allgemeinen eine Bedeutung oder Funktion und behält ihre ursprüngliche Form und Bedeutung während des Kombinations Prozesses bei. Für Sprachen, die über eine agglutinative Morphologie verfügen (z. b. Türkisch, Finnisch, Ungarisch oder Koreanisch), ist es möglich, Tausende von Formularen für ein bestimmtes Stamm Wort zu schaffen.

In der folgenden Tabelle wird eine Liste der inflechten Formulare für das finnische Wort "Talo" ("House") angezeigt.



| Word      | Sprachübersetzung   |
|-----------|---------------|
| Talo      | Pfarrhaus         |
| Taloni    | Mein Haus      |
| Talosse   | Im Haus  |
| Talossani | In meinem Haus   |
| Taloja    | Enthält        |
| Taloisse  | In den Häusern |



 

Inflektierte Sprachen, wie z. b. Englisch, Französisch und lateinisch, haben eine sehr geringe Anzahl von möglichen Word-Formularen für ein Stammpfad. In den flektierten Sprachen beeinflussen Morphemen bei der Bindung einander. Die meisten Änderungen in der Wende sind im Stamm-oder Word-Ende vorhanden. Im Gegensatz zu agglutinative Sprachen haben inflektierte Sprachen in der Regel unterschiedliche Funktionen für ein einzelnes Morpheme. Beispielsweise kann ein Morpheme sowohl die Anzahl als auch die Groß-/Kleinschreibung bestimmen.

Wort Stamm Erkennungen müssen den Kompromiss zwischen Leistung und Genauigkeit abwägen, um nur eine Teilmenge der möglichen Wort Formulare zu generieren.

## <a name="numbers-times-and-dates"></a>Zahlen, Uhrzeiten und Datumsangaben

Wörter Trennungen müssen ein gängiges Format für die Darstellung von Zahlen, Uhrzeiten und Datumsangaben verwenden, um konsistente Abfragen zu ermöglichen.

Wenn Sie eine Wörter Trennung erstellen, wird empfohlen, dass die Wörter Trennung Zahlen in eine kanonische Darstellung normalisiert, indem Sie das Muster "nn *DD* D *CC*" verwendet, wobei nn die literalsequenz "nn", " *DD* " der ganzzahlige Teil der Zahl, "d" das Literale "d" und " *CC* " der Bruchteil der Zahl ist. Die Wörter Trennung schränkt nicht die Anzahl der Ziffern für den ganzzahligen oder den Bruchteil der Zahl ein. Es wird empfohlen, dass Wörter Trennungen numerische Muster erkennen, die durch Punkte (.) und Kommas (,) getrennt sind. Beispielsweise stellt Windows Search sowohl "1.000,2" als auch "1.000, 2" als "NN1000D2" dar.

Wählen Sie ein Format für die Wörter Trennung und die Wort Stamm Erkennung aus. Arabische Ziffern mit einem Byte werden normalisiert, sodass eine Abfrage, die eines dieser Formulare enthält, mit Dokumenten mit den anderen Formularen übereinstimmt.

Wenn Sie eine Wörter Trennung erstellen, wird empfohlen, dass die Wörter Trennung alle Uhrzeiten als 24-Stunden-Darstellung mit dem Muster "TT *HHMMSS*" darstellt, wobei TT das literalpräfix "TT" ist, *HH* die Stunden, *mm* die Minuten und *SS* die Sekunden. Die Windows-Suche entspricht nicht den zusätzlichen Zeiteinheiten, z. b. Millisekunden. Wird am- und Nachmittag Patterns ist optional.

Wenn Sie eine Wörter Trennung erstellen, empfiehlt es sich, dass die Wörter Trennung Datumsangaben im kanonischen Format "DD *JJJJMMTT*" generiert, wobei DD das Literale "dd", *JJJJ* die Jahre, *mm* für die Monate und *DD* für die Tage ist. Außerdem wird empfohlen, dass die Wörter Trennungen zweistellige Jahres Angaben in den Formaten 20 Jahre hundert und 21. Jahrhundert speichern. Die Wörter Trennungen stellen z. b. "2.2.99" als "DD19990202" und "DD20990202" dar. Zur Abfragezeit leitet Windows Search das Datum mithilfe von Windows-Anwendungs Programmierschnittstellen (APIs) ab, um das Übergangs Datum zu bestimmen, auf dem der Server das richtige Format (19 *xx* oder 20 *xx*) anzeigt.

## <a name="compound-words"></a>Zusammengesetzte Wörter

In einigen Sprachen, wie z. b. Deutsch, werden Nomen aus einfacheren Substantiven entfernt. Diese zusammengesetzten Nomen sind zu spezifisch für einen sinnvollen Abfrage Rückruf. Beispielsweise entspricht eine Abfrage für "Versicherung" ("Insurance") ohne Zerlegung nicht "Lebensversicherungsgesellschaft" ("Lebensversicherungs Händler"). In diesen Fällen wird empfohlen, dass Wörter Trennungen diese zusammengesetzten Wörter während der Indexerstellung und der Abfragezeit in Basiskomponenten unterteilen. Die deutsche Wörter Trennung unterbricht "Lebensversicherungsgesellschaft" in den Komponenten Wörtern "Leben", "Versicherung" und "Gesellschaft". Die gleiche Zerlegung wird zur Abfragezeit zusammen mit der optionalen Wort Stamm Erkennung für jeden der resultierenden Bedingungen angewendet.

## <a name="compound-phrases"></a>Zusammengesetzte Ausdrücke

Einige Sprachen, z. b. Koreanisch, enthalten komplexe Ausdrücke, die auf unterschiedliche Weise unterteilt werden können. Ein koreanischer Ausdruck besteht aus *Inhalts Wörtern*, wie z. b. Nomen, Pronomen, Verben und Adjektiven, gefolgt von *funktionalen Wörtern*. Funktionale Wörter werden in nach Positionen und enden gefunden. Post Positionen geben die funktionale Rolle des Substantiv oder des Pronomen in einem Satz an. Enden geben die funktionale Rolle des Verbs oder Adjektiv an.

Ein Ausdruck kann mehrere Analysen aufweisen, und jede Analyse kann aus mehreren Inhalts Wörtern bestehen. Die Wörter Trennung muss sprachspezifische Heuristik verwenden, um von Kontext zu bestimmen, wie viel Gewichtung für verschiedene Analysen verwendet werden soll. Die Wörter Trennung kann basierend auf der Anzahl der resultierenden Komponenten Wörter ermitteln, welche Zerlegung verwendet werden soll. Einige Wörter Trennungen können kurze Sequenzen von längeren Begriffen bevorzugen, während andere Wörter Trennungen lange Sequenzen kleiner Wörter bevorzugen.

Ein weiterer Aspekt ist, dass in Koreanisch, Nomen und Pronomen im Index gespeichert werden können, ohne dass entsprechende funktionale Wörter vorliegen. Koreanisch ist eine agglutinative Sprache und kombiniert zahlreiche Wort enden mit Verben und Adjektiven, um unzählige Flexions Formen zu bilden. Verben und Adjektive, die in Ausdrücken identifiziert werden, werden mit ihren Enden im Index gespeichert, aber die Wörter Trennung generiert keine neuen Formulare.

## <a name="special-characters-and-words"></a>Sonderzeichen und Wörter

Sonderzeichen sind Zeichen wie "," "©" und "™". Diese Zeichen werden selten in Abfragen verwendet. Die Wörter Trennungen sollten Sonderzeichen während der Indexerstellung und zur Abfragezeit entfernen.

Es wird empfohlen, dass Wörter Trennungen sonderwörter erkennen, wie z. b. "C++", "C", ".net", \# "Grades" und "Musical Notation". Wörter Trennungen können eine Sprache Heuristik verwenden, um ein Muster für sonderwörter zu identifizieren. Wörter Trennungen können auch ein benutzerdefiniertes Wörterbuch verwenden, das erkannte sonderwörter enthält.

## <a name="acronyms-and-abbreviations"></a>Akronyme und Abkürzungen

Akronyme und Abkürzungen müssen berücksichtigt werden, wenn Sie eine Wörter Trennung implementieren. In vielen Sprachen werden einzelne Buchstaben von Akronymen durch Punkte getrennt. Gelegentlich werden Wörter, die nicht als Akronyme oder Abkürzungen erkannt werden, abgekürzt. Beispielsweise kann "USA of America" entweder als "USA" oder "USA" abgekürzt werden. In Windows Search enthaltene Wörter Trennungen identifizieren in der Regel Wörter mit nur einem Buchstaben als Füll Wörter und behandeln diese Wörter während der Abfragezeit als Platzhalter. Während der Abfragezeit konvertiert eine Wörter Trennung, die keine allgemeinen Akronyme kennt oder Abkürzungen nicht erkennt, die Abkürzung "USA". in "U", "S" und "A". Diese Zerlegung bietet nicht genügend Informationen, um die Wörter im Volltextindex abzugleichen, da alle Abfrage Begriffe Füll Wörter sind. Wenn Sie eine Wörter Trennung erstellen, wird empfohlen, dass die Wörter Trennung die Zeiträume entfernt, in denen die Buchstaben von Akronymen getrennt werden. Im Beispiel "USA" wird als "USA" gespeichert, und ein Abfragebegriff, der "USA" enthält fragt tatsächlich nach "USA". Wenn eine Wörter Trennung eine Abkürzung verarbeitet, wird der Zeitraum in dieser Abkürzung nicht als EOS-Pause behandelt. Aus diesem Grund kann eine Wörter Trennung einen EOS-Break nicht korrekt identifizieren, wenn die Abkürzung am Ende des Satzes liegt.

## <a name="capitalization"></a>Großbuchstaben

Die Groß-/Kleinschreibung wird von Windows Search derzeit nicht beibehalten, wenn die Wörter im Volltextindex gespeichert werden. Wörter Trennungen und Wort Stamm Erkennungen sollten die Groß-/Kleinschreibung nicht ändern.

## <a name="nonbreaking-spaces"></a>Nicht brechende Leerzeichen

Wenn Sie eine Wörter Trennung erstellen, sollten Sie sicherstellen, dass die Wörter Trennung nicht unterbrechende Leerzeichen als Trennzeichen für Wörter behandelt. Außerdem wird empfohlen, dass die Wörter Trennung Alternative Formen des Worts generiert, mit und ohne unterbrechende Leerzeichen. Einige Zeichen, z. b. Unterstriche, sind Sonderzeichen, die aufgrund der Quellen des Texts, in dem Sie gefunden werden, als nicht-brechende Zeichen behandelt werden. Beispielsweise können Quell Code-oder Dateinamen Unterstriche als nicht unterbrechende Zeichen enthalten.

## <a name="surrogate-pairs"></a>Ersatzzeichenpaare

Ersatz Zeichenpaare sind Zeichen Darstellungen im Quellcode, die ein einzelnes Zeichen darstellen, das aus einer Sequenz von zwei Unicode-Werten besteht. In einem codierten Paar ist der erste Wert ein hohes Ersatz Zeichen, und der zweite Wert ist ein niedriges Ersatz Zeichen. Ein hohes Ersatz Zeichen ist ein Zeichen im Bereich von u + D800 und bis u + DBFF. Ein niedriges Ersatz Zeichen ist ein Zeichen im Bereich von u + DC00 und bis u + DFFF. Ersatz Zeichenpaare erweitern den Zeichensatz über das Unicode-Zeichen hinaus. Es wird empfohlen, dass eine Wörter Trennung bei der Behandlung von Ersatz Zeichen Paaren die folgenden Regeln verwendet:

-   Ein hohes Ersatz Zeichen muss ein niedriges Ersatz Zeichen vorangestellt sein.
-   Ein niedriges Ersatz Zeichen muss einem hohen Ersatz Zeichen folgen.
-   Ein hohes oder niedriges Ersatz Zeichen ohne entsprechenden Wert für die andere Hälfte hat keine Bedeutung.

Wörter Trennungen müssen alle Paare in Erwägung gezogen und die Paare als solche im Index generieren. Weitere Informationen finden Sie unter [Surrogates und ergänzende Zeichen](/windows/desktop/Intl/surrogates-and-supplementary-characters).

 

 
