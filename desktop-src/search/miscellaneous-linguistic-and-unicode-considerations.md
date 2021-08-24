---
description: In diesem Thema werden Überlegungen zur Berücksichtigung von Agglutinativen Sprachen und Unicode-Ersatzzeichenpaaren sowie zur Verwendung von Ersatzzeichenpaaren beschrieben, um den Unicode-Zeichensatz auf verschiedene Zeichensätze zu erweitern.
ms.assetid: 7104b2da-2ece-46ce-b4ca-6c24dc4d6677
title: Verschiedene linguistische und Unicode-Überlegungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24372194fb17498e1e0ce19be1bbbac3f1dccb27a63d840cedf95de38f735026
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594480"
---
# <a name="miscellaneous-linguistic-and-unicode-considerations"></a>Verschiedene linguistische und Unicode-Überlegungen

In diesem Thema werden Überlegungen zur Berücksichtigung von Agglutinativen Sprachen und Unicode-Ersatzzeichenpaaren sowie zur Verwendung von Ersatzzeichenpaaren beschrieben, um den Unicode-Zeichensatz auf verschiedene Zeichensätze zu erweitern. In diesem Thema wird auch beschrieben, wie Wörterbrechen Ausdrücke in Text identifizieren und leerzeichenfreie Leerzeichen behandeln, wie Wörterbrechen und Wortstammwörter Zahlen und Datumsangaben, zusammengesetzte Wörter, Zusammengesetzte Ausdrücke, Sonderwörter und Zeichen, Akronyme und Abkürzungen sowie Groß- und Groß- und Endungen behandeln.

Dieses Thema ist wie folgt organisiert:

-   [Ausdrucksidentifikation](#phrase-identification)
-   [Agglutinative Sprachen](#agglutinative-languages)
-   [Zahlen, Zeiten und Datumsangaben](#numbers-times-and-dates)
-   [Zusammengesetzte Wörter](#compound-words)
-   [Zusammengesetzte Ausdrücke](#compound-phrases)
-   [Sonderzeichen und Wörter](#special-characters-and-words)
-   [Akronyme und Abkürzungen](#acronyms-and-abbreviations)
-   [Großbuchstaben](#capitalization)
-   [Leerzeichen ohne Bruch](#nonbreaking-spaces)
-   [Ersatzzeichenpaare](#surrogate-pairs)

## <a name="phrase-identification"></a>Ausdrucksidentifikation

Ausdrücke sind ein Wort oder eine Gruppe von Wörtern, die von mindestens einem anderen Wort geändert werden. Ausdrücke sind schwer konsistent zu identifizieren, da derselbe Modifizierer in mehr als einem Ausdruck mit demselben Nomen verwendet werden kann. Beispiel: "Neues Haus", "House of House", "new House of House of House".

Windows Bei der Suche werden Ausdrücke am häufigsten zur Abfragezeit verwendet. Ausdrücke im Abfragetext erhalten eine höhere Gewichtung als einzelne Wörter. Aus dem vorherigen Beispiel wird ein Dokument, das "House of House" enthält, höher eingestuft als ein Dokument, das "House" und "House" an verschiedenen Punkten im Dokument enthält. Es wird empfohlen, dass Wörterbrechen zur Abfragezeit einen Ausdruck generieren, wenn der Ausdruck wahrscheinlich mit mindestens einem Dokument übereinstimmen wird.

## <a name="agglutinative-languages"></a>Agglutinative Sprachen

Agglutinative Sprachen bilden Wörter durch die Kombination kleinerer Morpheme, um zusammengesetzte Ideen auszudrücken. Jedes dieser Morpheme hat im Allgemeinen eine Bedeutung oder Funktion und behält während des Kombinationsprozesses seine ursprüngliche Form und Bedeutung bei. Für Sprachen mit agglutinativer Kante, z. B. Türkisch, Türkisch, Türkisch, Türkisch oder Koreanisch, ist es möglich, Tausende von Formularen für ein bestimmtes Stammwort zu erzeugen.

In der folgenden Tabelle ist eine Liste der gestrichenen Formen für das Wort "talo" (Haus) für Das Wort "wort" (Haus) aufgeführt.



| Word      | Sprachübersetzung   |
|-----------|---------------|
| Talo      | Haus         |
| Taloni    | Mein Haus      |
| Talossa   | Im Haus  |
| Talossani | In meinem Haus   |
| Taloja    | Häuser        |
| Taloisse  | In den Hausen |



 

Geformte Sprachen wie Englisch, Französisch und Lateinisch verfügen über eine sehr kleine Anzahl möglicher Wortformen für ein Stammwort. In gemittelten Sprachen beeinflussen sich Morpheme bei der Bindung. Die meisten Änderungen in der Inflection sind im Wortstamm oder am Wortende vorhanden. Im Gegensatz zu agglutinativen Sprachen verfügen Gespiegelte Sprachen in der Regel über unterschiedliche Funktionen für ein einzelnes Morphem. Beispielsweise kann ein Morphem sowohl die Zahl als auch den Fall bestimmen.

Stemmer für agglutinative Sprachen müssen den Abwägen zwischen Leistung und Genauigkeit abwägen, um nur eine Teilmenge der Anzahl möglicher Wortformen zu generieren.

## <a name="numbers-times-and-dates"></a>Zahlen, Zeiten und Datumsangaben

Wörterschalter müssen ein allgemeines Format zum Darstellen von Zahlen, Zeiten und Datumsangaben verwenden, um konsistente Abfragen zu ermöglichen.

Wenn Sie eine Wörterpause erstellen, wird empfohlen, dass die Wörterpause Zahlen mithilfe des Musters "NN *dd* D *cc"* in eine kanonische Darstellung normalisiert, wobei NN die Literalsequenz "NN" ist, *dd* der ganzzahlige Teil der Zahl, D das Literal "D" und *cc* der Bruchteil der Zahl ist. Wörterschalter schränken die Anzahl der Ziffern weder für die ganze Zahl noch für den Bruchteil der Zahl ein. Es wird empfohlen, dass Wörtertrennzeichen numerische Muster erkennen, die sowohl durch Zeiträume (.) als auch durch Kommas (,) getrennt sind. Beispielsweise stellt Windows Search sowohl "1.000.2" als auch "1.000,2" als "NN1000D2" dar.

Wählen Sie ein Format sowohl für wörterbrechende als auch für wortstammige Wörter aus. Einzelne arabische Zahlen mit einem Byte werden so normalisiert, dass eine Abfrage, die eines dieser Formulare enthält, Mit dokumenten mit den anderen Formularen entspricht.

Wenn Sie eine Wörterpause erstellen, wird empfohlen, dass die Wörterpause alle Zeiten als 24-Stunden-Darstellung mit dem Muster "TT *hhmmss"* präsentiert wird, wobei TT das Literalpräfix "TT", *hh* die Stunden, *mm* die Minuten und *ss* die Sekunden sind. Windows Die Suche passt nicht zu zusätzlichen Zeiteinheiten, z. B. Millisekunden. Parsing A.M. und Nachmittag -Muster sind optional.

Wenn Sie eine Wörter wörterbrechend erstellen, wird empfohlen, dass die Wörterpause Datumsangaben im kanonischen Format "DD *yyyymmdd"* generiert, wobei DD das Literal "DD", *yyyy die* Jahre, *mm* die Monate und *dd* die Tage ist. Es wird auch empfohlen, dass Wörter wörterbrechende Jahre in beiden Formaten des 19. und 21. Jh. gespeichert werden. Wörterbrechen stellen beispielsweise "2.2.99" als "DD19990202" und "DD20990202" dar. Zur Abfragezeit leitet die Windows-Suche das Datum mithilfe von Windows-APIs (Application Programming Interfaces) ab, um das Crossoverdatum für den Server zu bestimmen, um das richtige Format (19 *XX* oder 20 *XX)* anzuzeigen.

## <a name="compound-words"></a>Zusammengesetzte Wörter

In einigen Sprachen, z. B. Deutsch, werden Nomen aus einfacheren Nomen zusammengesetzt. Diese zusammengesetzten Nomen sind zu spezifisch in der Bedeutung für eine sinnvolle Abfragerückrufung. Ohne Zerlegung ist z. B. eine Abfrage für "Insurance" nicht mit "Lebens insurance salesman" (Lebens-Versicherungs-Vertriebsmitarbeiter) überein. In solchen Fällen wird empfohlen, diese zusammengesetzten Wörter sowohl während der Indexerstellung als auch während der Abfragezeit in Basiskomponenten zu unterteilen. Die deutsche Wörterumbrüche unterbricht "Lebens wies" in die Komponentenwörter "Leben", "Früher" und "Gesellschaft" auf. Sie wendet die gleiche Zerlegung zur Abfragezeit zusammen mit der optionalen Stammstammstammauslegung für jeden der resultierenden Begriffe an.

## <a name="compound-phrases"></a>Zusammengesetzte Ausdrücke

Einige Sprachen, z. B. Koreanisch, enthalten komplexe Ausdrücke, die auf verschiedene Weise unterbrochen werden können. Ein koreanischer Ausdruck besteht *aus* Inhaltswörtern wie Nomen, Pronomen, Verben und Adjektiven, gefolgt von *funktionalen Wörtern*. Funktionale Wörter befinden sich in Postpositionen und Enden. Postpositionen geben die funktionale Rolle des Nomens oder Pronomens in einem Satz an. -Endungen geben die funktionale Rolle des Verbs oder Adjektivs an.

Ein Ausdruck kann mehrere Analysen enthalten, und jede Analyse kann aus mehreren Inhaltswörtern bestehen. Die Wörterheuristik muss sprachspezifische Heuristiken verwenden, um aus dem Kontext zu bestimmen, wie viel Gewichtung verschiedenen Analysen zu geben ist. Die Wörterpause bestimmt möglicherweise anhand der Anzahl der resultierenden Komponentenwörter, welche Zerlegung verwendet werden soll. Einige Wörterumbrüche bevorzugen möglicherweise kurze Sequenzen mit längeren Begriffen, während andere Wörterumbrüche lange Sequenzen von kleineren Wörtern bevorzugen.

Ein weiterer Aspekt ist, dass nomens und pronouns in Koreanisch das im Index gespeicherte ohne die entsprechenden funktionalen Wörter sein können. Koreanisch ist eine agglutinative Sprache und kombiniert zahlreiche Wortenden mit Verben und Adjektiven, um unzählige Inflected Forms zu bilden. Verben und Adjektive, die in Ausdrücken identifiziert werden, werden mit ihren Enden im Index gespeichert, aber die Wörterpause generiert keine neuen Formulare.

## <a name="special-characters-and-words"></a>Sonderzeichen und Wörter

Sonderzeichen sind Zeichen wie "," "©" und "™". Diese Zeichen werden selten in Abfragen verwendet. Wörterschalter sollten Sonderzeichen während der Indexerstellung und zur Abfragezeit entfernt werden.

Es wird empfohlen, dass Wörterschalter spezielle Wörter wie "C++", \# "C", ".NET", Noten und Notation erkennen. Wörterschalter können eine Sprachhuristik verwenden, um ein Muster für spezielle Wörter zu identifizieren. Wörterschalter können auch ein benutzerdefiniertes Wörterbuch verwenden, das erkannte spezielle Wörter enthält.

## <a name="acronyms-and-abbreviations"></a>Akronyme und Abkürzungen

Akronyme und Abkürzungen müssen berücksichtigt werden, wenn Sie eine Wörterpause implementieren. In vielen Sprachen werden einzelne Buchstaben von Akronymen durch Zeiträume getrennt. Gelegentlich werden Wörter, die nicht als Akronyme oder Abkürzungen erkannt werden, abgekürzt. Beispielsweise kann "USA Of America" als "USA" oder "USA" abgekürzt werden. In der Suche enthaltene Wörter Windows in der Regel wörter mit nur einem Buchstaben als Rauschwörter und behandeln diese Wörter während der Abfragezeit als Platzhalter. Während der Abfragezeit konvertiert eine Wörter wörterbrechend, die keine gängigen Akronyme kennt oder keine Abkürzungen erkennt, die Abkürzung "USA". in "U", "S" und "A". Diese Zerlegung bietet nicht genügend Informationen, um Wörter im Volltextindex zu entsprechen, da alle Abfragebegriffe Rauschwörter sind. Wenn Sie eine Wörtertrennschalter-Datei erstellen, wird empfohlen, dass die Wörtertrennschalter die Zeiträume entfernen, die die Buchstaben von Akronymen trennen. Im Beispiel "U.S.A." wird als "USA" und ein Abfragebegriff gespeichert, der "USA" enthält. tatsächlich Abfragen für "USA". Wenn eine Wörter wörterbrechend eine Abkürzung verarbeitet, wird der Zeitraum in dieser Abkürzung nicht als BREAK-Break behandelt. Aus diesem Grund kann es sein, dass eine Wörterpause einen BREAK-Break nicht ordnungsgemäß identifiziert, wenn sich die Abkürzung am Ende des Satzes befindet.

## <a name="capitalization"></a>Großbuchstaben

Windows Bei der Suche wird die Groß-/Groß-/Großbuchtierung derzeit nicht beibehalten, wenn Wörter im Volltextindex speichert werden. Wörterbrechen und Wortstammwörter sollten die Case für Wörter nicht ändern.

## <a name="nonbreaking-spaces"></a>Leerzeichen ohne Bruch

Wenn Sie eine Wörtertrennung erstellen, sollten Sie sicherstellen, dass die Wörtertrennung leerzeichenfreie Leerzeichen als Worttrennzeichen behandelt. Es wird auch empfohlen, dass die Wörterpause alternative Formen des Worts mit und ohne Leerzeichen generiert. Einige Zeichen, z. B. Unterstriche, sind Sonderzeichen, die aufgrund der Quellen des Texts, in dem sie gefunden werden, als nicht bruchstückliche Zeichen behandelt werden. Quellcode- oder Dateinamen können z. B. Unterstriche als zeichenfreie Zeichen enthalten.

## <a name="surrogate-pairs"></a>Ersatzzeichenpaare

Ersatzzeichenpaare sind Zeichendarstellungen im Quellcode, die ein einzelnes Zeichen darstellen, das aus einer Sequenz von zwei Unicode-Werten besteht. In einem codierten Paar ist der erste Wert ein hohes Ersatzzeichen und das zweite ein niedriges Ersatzzeichen. Ein hohes Ersatzzeichen ist ein Zeichen im Bereich U+D800 bis U+DBFF. Ein niedriges Ersatzzeichen ist ein Zeichen im Bereich U+DC00 bis U+DFFF. Ersatzzeichenpaare erweitern den Zeichensatz über das Unicode-Zeichen hinaus. Es wird empfohlen, dass eine Wörterumbruch-Klasse bei der Behandlung von Ersatzzeichenpaaren die folgenden Regeln verwendet:

-   Ein hohes Ersatzzeichen muss einem niedrigen Ersatzzeichen voraus sein.
-   Ein niedriges Ersatzzeichen muss einem hohen Ersatzzeichen folgen.
-   Ein hohes oder niedriges Ersatzzeichen ohne entsprechenden Wert für die andere Hälfte hat keine Bedeutung.

Wörterbrechen müssen alle Paare berücksichtigen und die Paare als solche im Index generieren. Weitere Informationen finden Sie unter [Ersatzzeichen und ergänzende Zeichen.](/windows/desktop/Intl/surrogates-and-supplementary-characters)

 

 
