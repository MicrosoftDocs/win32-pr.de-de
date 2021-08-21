---
description: Sprachressourcen bestehen aus Wörterschaltern und Wortstammlern, die die Index- und Abfragefunktionen auf neue Sprachen und Lokale erweitern.
ms.assetid: 7963805e-e279-42cf-ba95-f81a7de8e68e
title: Grundlegendes zu Sprachressourcenkomponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8feb10d14edbf4aba59b912ae1945d5e87ec32ef684f0b1f5530f1770ba70053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462382"
---
# <a name="understanding-language-resource-components"></a>Grundlegendes zu Sprachressourcenkomponenten

Sprachressourcen bestehen aus Wörterschaltern und Wortstammlern, die die Index- und Abfragefunktionen auf neue Sprachen und Lokale erweitern. Wörterschalter werden sowohl bei der Indexerstellung als auch bei Abfragen verwendet. Stemmers werden nur für Abfragen verwendet. Windows Bei der Suche werden Sprachressourcen-DLLs verwendet, um eine Bindung an [**IWordBreaker-**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) und [**IStinnen-Implementierungen**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) für ein bestimmtes Sprachdirigenz zu gewährleisten.

Dieses Thema ist wie folgt organisiert:

-   [Informationen zu Sprachressourcen](#about-language-resources)
-   [Wortbruch](#word-breaking)
-   [Wortstammerkennung](#stemming)
-   [Normalisierung](#normalization)
-   [Rauschwörter](#noise-words)
-   [Zugehörige Themen](#related-topics)

## <a name="about-language-resources"></a>Informationen zu Sprachressourcen

Windows Die Suche verwendet einen Filter (eine Implementierung der [**IFilter-Schnittstelle)**](/windows/win32/api/filter/nn-filter-ifilter) und [**ILoadFilter,**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) um auf ein Dokument im nativen Format zu zugreifen. Die [**IFilter-Komponente**](/windows/win32/api/filter/nn-filter-ifilter) extrahiert Textinhalt, Eigenschaften und Formatierungen aus dem Dokument. Der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) identifiziert das Locale des Dokuments, das gefiltert wird. Die Indizierungskomponente ruft die entsprechende Wörterpause für dieses Locale auf. Wenn keines verfügbar ist, ruft die Indizierungskomponente die neutrale Wörterpause auf. Die Wörterpause empfängt von einem [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)einen Eingabedatenstrom von Unicode-Zeichen, den die Wörterbrechen analysiert, um einzelne Wörter und Ausdrücke zu erzeugen. Die Wörterpause normalisiert auch Datums- und Uhrzeitformate. Der Indexer normalisiert die von der Wörter wörterbrechenden Wörter, indem er die Wörter in alle Großbuchstaben konvertiert. Der Indexer speichert die Großbuchstaben im Volltextindex, mit Ausnahme von Rauschwörtern, die für dieses Locale identifiziert werden.

In der folgenden Tabelle sind die Aktionen und die entsprechenden Ergebnisse für den Satz "Abbildung 1 veranschaulicht die Rolle von Sprachressourcen für die Windows Search während des Indexerstellungsprozesses" aufgeführt.



| Aktion                  | Resultierender Text                                                                                                               |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Ursprünglicher Text           | Abbildung 1 veranschaulicht die Rolle von Sprachressourcen für die Windows Während der Indexerstellung.                    |
| Filterung               | Abbildung 1 veranschaulicht die Rolle von Sprachressourcen für die Windows Während der Indexerstellung.                    |
| Wörtertrennung           | Abbildung 1 veranschaulicht, die, Rolle, von, Sprache, Ressourcen, für, Windows, Suchen, während, der, Index, Erstellung, Prozess, EOS |
| Normalisierung           | ABBILDUNG, 1, VERANSCHAULICHT, THE, ROLE, OF, LANGUAGE, RESOURCES, WINDOWS, SEARCH, DURING, THE, INDEX, CREATION, PROCESS           |
| Entfernen von Rauschworten      | ABBILDUNG, VERANSCHAULICHT, ROLLE, SPRACHE, RESSOURCEN, WINDOWS, SUCHE, WÄHREND, INDEX, ERSTELLUNG, PROZESS                            |
| Speichern im Volltextindex | ABBILDUNG, VERANSCHAULICHT, ROLLE, SPRACHE, RESSOURCEN, WINDOWS, SUCHE, WÄHREND, INDEX, ERSTELLUNG, PROZESS                            |



 

Wörter wörter- und wortstammende Wörter werden verwendet, um [FREETEXT-Abfragen](-search-sql-freetext.md) zur Abfragezeit zu erweitern. Das Locale der Abfrage ist das Standard-Locale, es sei denn, ein Sprachcodebezeichner (LCID) wird als Abfrageparameter übergeben. Die Abfragekomponente ruft die entsprechende Wörterpause für die Abfragebegriffe auf, die in der [WHERE-Klausel](-search-sql-where.md) der Abfrage aufgeführt sind. Wenn die WHERE-Klausel der Abfrage beispielsweise "FREETEXT (Apples, Orangen und Birnen)" enthält, empfängt die Wörterpause den Text "Apples, Orangen und Birnen". Wenn die WHERE-Klausel der Abfrage das CONTAINS-Volltext-Prädikat verwendet, wird die Textausgabe aus der Wörterpause normalisiert. [](-search-sql-contains.md) Andernfalls übergibt die Abfragekomponente jedes von der Wörterpause identifizierte Wort an den entsprechenden Wortstamm für diese Sprache und dieses Locale. Der Wortstamm generiert eine Liste alternativer bzw. inflected-Formen für dieses Wort. Die Abfragekomponente normalisiert die erweiterte Liste der Abfragebegriffe und entfernt Rauschwörter.

In der folgenden Tabelle sind die Aktionen und die entsprechenden Ergebnisse für die Abfrage "Äpfel, Orangen und Birnen" aufgeführt.



| Aktion                       | Resultierender Text                                            |
|------------------------------|-----------------------------------------------------------|
| Ursprünglicher Text                | Äpfel, Orangen und Birnen                                |
| Wörtertrennung                | Apples, Orangen und, Pears, EOS                          |
| Wortstammerkennung                     | apple, apples, orange, orangey, oranges, and, pear, pears |
| Normalisierung                | APPLE, APPLES, ORANGE, ORANGEY, ORANGES, AND, PEAR, PEARS |
| Entfernen von Rauschworten           | APPLE, APPLES, ORANGE, ORANGEY, ORANGES, PEAR, PEARS      |
| Erweiterte Liste der Abfragebegriffe | APPLE, APPLES, ORANGE, ORANGEY, ORANGES, PEAR, PEARS      |



 

Die erweiterten Abfragebegriffe erhöhen die Wahrscheinlichkeit, dass die Abfrage Dokumente findet, die der Absicht der ursprünglichen Abfrage entsprechen. Text, der von der Wörterbrechen- oder Wortstammzeile zur Abfragezeit generiert wird, wird nicht auf dem Datenträger gespeichert.

## <a name="word-breaking"></a>Worttrennung

Wörtertrennung ist die Trennung von Text in einzelne Texttoken oder Wörter. Viele Sprachen, insbesondere sprachen mit lateinischen Alphabeten, verfügen über ein Array von Worttrennzeichen (z. B. Leerzeichen) und Satzzeichen, die verwendet werden, um Wörter, Ausdrücke und Sätze zu erkennen. Wörterbrechen müssen auf genauen Sprachhuristiken basieren, um zuverlässige und genaue Ergebnisse zu liefern. Wortbruch ist bei zeichenbasierten Systemen des Schreibens oder skriptbasierten Alphabeten komplexer, bei denen die Bedeutung einzelner Zeichen vom Kontext bestimmt wird. Weitere Informationen zu linguistischen Überlegungen, die sich möglicherweise auf die Implementierung der Wörterumbruch-Datei auswirken, finden Sie unter [Linguistische und Unicode-Überlegungen.](linguistic-and-unicode-considerations.md)

## <a name="stemming"></a>Wortstammerkennung

Windows Die Suche wendet Stemmer ausschließlich zur Abfragezeit an, um zusätzliche Wortformen für Begriffe in [FREETEXT-](-search-sql-freetext.md) und Eigenschaftsabfragen zu generieren. Wortstammmer führen eine grammatische Analyse durch und wenden grammatikalische Regeln an, um eine Liste alternativer bzw. inflected-Formen für Wörter zu generieren. Alternative Formulare haben häufig denselben Stamm oder dieselbe Basisform. Durch das Generieren der geformten Formulare für ein Wort gibt der Indizierungsdienst Abfrageergebnisse zurück, die statistisch relevanter für eine Abfrage sind. Beispielsweise stimmt eine Volltextabfrage für "Meet"-Meeting mit Dokumenten ab, die "Beim Badieren, Beim Badieren, Beim Baden", "2" oder "Treffen, Besprechungen" und Kombinationen dieser Begriffe enthalten.

Für einige Sprachen ist es erforderlich, dass Inflected-Begriffe sowohl zur Indexzeit als auch zur Abfragezeit für Standard- und Variantenintellektionen generiert werden. In diesem Fall erfolgt die Wortstammung in der Wörterbrechenkomponente mit minimaler Wortstammarbeit. Beispielsweise führt die japanische Wörterpause wortstammende Daten sowohl während der Indexerstellung als auch bei Abfragen aus, um einer Abfrage zu ermöglichen, unterschiedliche Formen der Suchbegriffe zu finden.

## <a name="normalization"></a>Normalisierung

Dokumente aller Sprachen werden in einem einzelnen Index gespeichert. Obwohl Wörter und linguistische Regeln sich erheblich unterscheiden, gibt es einige Überlegungen, z. B. Zahlen, Datumsangaben und Zeiten, die über alle Wörterbrechen hinweg konsistent behandelt werden. Weitere Informationen zu Normalisierungsüberlegungen, die sich auf die Implementierung der Wörterumbruch-Funktion auswirken können, finden Sie unter [Surface Form Normalization](surface-form-normalization.md).

## <a name="noise-words"></a>Rauschwörter

Rauschwörter, auch als Stoppwörter bezeichnet, sind Wörter, die keine signifikanten Indikatoren für Inhalt sind. Der Indizierungsdienst entfernt Rauschwörter aus Abfragebegriffen und inhalten, die im Volltextindex enthalten sind. Ein *Offset* ist das Vorkommen eines Worts in einem Dokument oder in einer Liste von Abfrageausdrucken. Der Offset von Rauschwörtern in einem Dokument oder einer Abfrage wird als leer aufgezeichnet. Das Entfernen von Rauschwörtern verbessert die Abfrageleistung, indem unnötiges Indexwachstum vermieden wird. Außerdem wird die Relevanz von Abfrageergebnissen verbessert. Sie können die Windows für die Verwendung von Rauschwortlisten für bestimmte Sprachen konfigurieren. Diese Listen werden verwendet, wenn eine Wörterbrechen für diese Sprache aufgerufen wird. Beispielsweise tritt "the" in der englischen Sprache so häufig auf, dass es wenig Wert als eindeutigen Schlüssel hat. "The" befindet sich in der Rauschwortliste, wird nicht in den Inhaltsindex geschrieben und gibt bei Der Abfrage keine Ergebnisse zurück.

Rauschwörter fungieren als Platzhalter in Ausdrucksabfragen. Ein Dokument, das den Text "wag the dog" enthält, wird im Index mit "wag" bei Vorkommen 1 und "dog" bei Vorkommen 3 gespeichert. Die Ausdrucksabfrage "wag dog" stimmt nicht überein, die Ausdrucksabfrage "wag a dog" jedoch, da die Informationen zum Vorkommen übereinstimmen. Der Ausdruck "wag purple dog" findet keine Übereinstimmung, da "violett" im Index bei Vorkommen 2 nicht gefunden wird. Eine Abfrage für "wag the dog" gibt jedoch Dokumente zurück, die "wag purple dog" enthalten, da es keine Möglichkeit gibt, effizient zu bestimmen, ob das Dokument ein Rauschwort zwischen "wag" und "dog" hatte.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweitern von Sprachressourcen](extending-language-resources-in-windows-search.md)
</dt> <dt>

[Implementieren einer Wörterbruch- und Wortstammnotung](implementing-a-word-breaker-and-stemmer.md)
</dt> <dt>

[Linguistische und Unicode-Überlegungen](linguistic-and-unicode-considerations.md)
</dt> <dt>

[Problembehandlung für Sprachressourcen und bewährte Methoden](troubleshooting-language-resources.md)
</dt> </dl>

 

 
