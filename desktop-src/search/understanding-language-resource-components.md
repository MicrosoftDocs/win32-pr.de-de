---
description: Sprachressourcen bestehen aus Wörter Trennungen und Wort Stamm Erkennungen, die die Index Erstellungs-und Abfragefunktionen für neue Sprachen und Gebiets Schemas erweitern.
ms.assetid: 7963805e-e279-42cf-ba95-f81a7de8e68e
title: Grundlegendes zu Sprachressourcen Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e03c9294eaf6e50de024b866372093a0359fc79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525442"
---
# <a name="understanding-language-resource-components"></a>Grundlegendes zu Sprachressourcen Komponenten

Sprachressourcen bestehen aus Wörter Trennungen und Wort Stamm Erkennungen, die die Index Erstellungs-und Abfragefunktionen für neue Sprachen und Gebiets Schemas erweitern. Die Wörter Trennungen werden während der Indexerstellung und-Abfrage verwendet. Wort Stamm Erkennungen werden nur für Abfragen verwendet. Windows Search verwendet Sprachressourcen-DLLs für die Bindung an [**iwordbreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) -und [**istemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) -Implementierungen für ein bestimmtes sprach Gebiets Schema.

Dieses Thema ist wie folgt organisiert:

-   [Informationen zu Sprachressourcen](#about-language-resources)
-   [Wörter Trennung](#word-breaking)
-   [Wortstammerkennung](#stemming)
-   [Normalisierung](#normalization)
-   [Füll Wörter](#noise-words)
-   [Zugehörige Themen](#related-topics)

## <a name="about-language-resources"></a>Informationen zu Sprachressourcen

Windows Search verwendet einen Filter (eine Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle) und [**iloadfilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) , um auf ein Dokument im nativen Format zuzugreifen. Die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Komponente extrahiert Textinhalte, Eigenschaften und Formatierungen aus dem Dokument. Der IFilter identifiziert das Gebiets Schema des zu [**filternden**](/windows/win32/api/filter/nn-filter-ifilter) Dokuments. Die Indizierungs Komponente ruft die entsprechende Wörter Trennung für dieses Gebiets Schema auf. Wenn keine verfügbar ist, ruft die Indizierungs Komponente die neutrale Wörter Trennung auf. Die Wörter Trennung empfängt, von einem [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), einen Eingabedaten Strom von Unicode-Zeichen, die die Wörter Trennung analysiert, um einzelne Wörter und Ausdrücke zu liefern. Die Wörter Trennung normalisiert auch Datums-und Uhrzeit Formate. Der Indexer normalisiert die Wörter, die von der Wörter Trennung erzeugt werden, indem die Wörter in Großbuchstaben konvertiert werden. Der Indexer speichert die Großbuchstaben in den Volltextindex, mit Ausnahme von Füll Wörtern, die für dieses Gebiets Schema identifiziert werden.

In der folgenden Tabelle sind die Aktionen und die zugehörigen Ergebnisse für den Satz "Abbildung 1: die Rolle der Sprachressourcen für Windows Search während des Index Erstellungs Prozesses" aufgeführt.



| Aktion                  | Resultierende Text                                                                                                               |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Ursprünglicher Text           | Abbildung 1 zeigt die Rolle der Sprachressourcen für die Windows-Suche während des Index Erstellungs Prozesses.                    |
| Filterung               | Abbildung 1 zeigt die Rolle der Sprachressourcen für die Windows-Suche während des Index Erstellungs Prozesses.                    |
| Wörtertrennung           | Abbildung 1, illustriert,, Role, of, Language, Resources, for, Windows, Search, during, The, Index, Creation, Process, EOS |
| Normalisierung           | Abbildung 1, illustriert,, Rolle, von, Sprache, Ressourcen, Windows, Search, während,, Index, Erstellung, Prozess           |
| Entfernen von Füll Wörtern      | Abbildung, Veranschaulichung, Rolle, Sprache, Ressourcen, Windows, Suche, während, Index, Erstellung, Prozess                            |
| In Volltextindex speichern | Abbildung, Veranschaulichung, Rolle, Sprache, Ressourcen, Windows, Suche, während, Index, Erstellung, Prozess                            |



 

Wörter Trennungen und Wort Stamm Erkennungen werden zum Erweitern von frei [Text](-search-sql-freetext.md) Abfragen zur Abfragezeit verwendet. Das Gebiets Schema der Abfrage ist das Standard Gebiets Schema, es sei denn, ein Sprachcode Bezeichner (LCID) wird als Abfrage Parameter übergeben. Die Abfrage Komponente ruft die entsprechende Wörter Trennung für die Abfrage Begriffe auf, die in der [Where](-search-sql-where.md) -Klausel der Abfrage aufgeführt sind. Wenn die WHERE-Klausel der Abfrage z. b. "fretext (Äpfel, Orangen und Birnen)" enthält, empfängt die Wörter Trennung den Text "Äpfel, Orangen und Birnen". Wenn die Abfrage, in der die-Klausel das voll Text Prädikat [enthält](-search-sql-contains.md) , verwendet wird, wird die Textausgabe der Wörter Trennung normalisiert. Andernfalls übergibt die Abfrage Komponente jedes von der Wörter Trennung identifizierte Wort an die entsprechende Wort Stamm Erkennung für diese Sprache und dieses Gebiets Schema. Die Wort Stamm Erkennung generiert eine Liste alternativer oder inflektierte Formulare für dieses Wort. Die Abfrage Komponente normalisiert die erweiterte Liste der Abfrage Begriffe und entfernt Füll Wörter.

In der folgenden Tabelle sind die Aktionen und die zugehörigen Ergebnisse für die Abfrage "Äpfel, Orangen und Birnen" aufgeführt.



| Aktion                       | Resultierende Text                                            |
|------------------------------|-----------------------------------------------------------|
| Ursprünglicher Text                | Äpfel, Orangen und Birnen                                |
| Wörtertrennung                | Äpfel, Orangen und, Birnen, EOS                          |
| Wortstammerkennung                     | Apple, Äpfel, Orange, orangey, Orangen und, Birnen, Birnen |
| Normalisierung                | Apple, Äpfel, Orange, orangey, Orangen und, Birnen, Birnen |
| Entfernen von Füll Wörtern           | Apple, Äpfel, Orange, orangey, Orangen, Birnen, Birnen      |
| Erweiterte Liste der Abfrage Begriffe | Apple, Äpfel, Orange, orangey, Orangen, Birnen, Birnen      |



 

Die erweiterten Abfrage Begriffe erhöhen die Wahrscheinlichkeit, dass die Abfrage Dokumente findet, die der Absicht der ursprünglichen Abfrage entsprechen. Der Text, den die Wörter Trennung oder die Wort Stamm Erkennung zur Abfragezeit generiert, wird nicht auf dem Datenträger gespeichert.

## <a name="word-breaking"></a>Worttrennung

Die Wörter Trennung ist die Trennung von Text in einzelne Texttoken oder Wörter. Viele Sprachen, insbesondere solche mit römischen Alphabets, verfügen über ein Array von Wort Trennzeichen (z. b. Leerraum) und Interpunktions Zeichen, die zur Unterscheidung von Wörtern, Ausdrücken und Sätzen verwendet werden. Wörter Trennungen müssen sich auf eine exakte sprach-Heuristik stützen, um zuverlässige und genaue Ergebnisse zu liefern. Die Wörter Trennung ist für zeichenbasierte Systeme zum Schreiben oder skriptbasierten Alphabets komplexer, bei denen die Bedeutung einzelner Zeichen aus dem Kontext bestimmt wird. Weitere Informationen zu linguistischen Überlegungen, die sich auf die Implementierung von Wörter Trennungen auswirken können, finden Sie unter [Überlegungen zu linguistischen](linguistic-and-unicode-considerations.md)

## <a name="stemming"></a>Wortstammerkennung

Die Windows-Suche wendet Wort Stamm Erkennungen exklusiv zur Abfragezeit an, um zusätzliche Wort Formulare für Begriffe in [Freitext](-search-sql-freetext.md) -und Eigenschafts Abfragen zu generieren. Wort Stamm Erkennungen führen eine morphologische Analyse durch und wenden grammatiktische Regeln an, um eine Liste von Alternativen oder inflektierte Formularen für Wörter zu generieren. Alternative Formulare haben oft denselben stem-oder Basis Formular. Durch das Erstellen der Flexions Formen für ein Wort gibt der Indizierungs Dienst Abfrageergebnisse zurück, die statistisch relevanter für eine Abfrage sind. Eine Volltextabfrage für "swimmeet" entspricht z. b. Dokumenten, die "Swim, swimes, swims, swims", "Swimming", "sliam", "slium", "Meeting, Meet, Meet

Für einige Sprachen ist es erforderlich, dass sowohl bei der Index Zeit als auch bei der Abfragezeit sowohl für Standard-als auch für Variant-inflektionen unveränderliche Begriffe generiert In diesem Fall erfolgt die Wort Stamm Erkennung in der Wort Trennungs Komponente mit minimaler Wort Stamm Erkennung in der eigentlichen Wort Stamm Erkennung. Die japanische Wörter Trennung führt z. b. die Wort Stamm Erkennung während der Indexerstellung und-Abfrage durch, damit eine Abfrage verschiedene inflektierte Formen der Suchbegriffe finden kann.

## <a name="normalization"></a>Normalisierung

Dokumente aller Sprachen werden in einem einzigen Index gespeichert. Obwohl sich Wörter und linguistische Regeln erheblich unterscheiden, gibt es einige Überlegungen, wie z. b. Zahlen, Datumsangaben und Uhrzeiten, die konsistent über alle Wörter Trennungen hinweg behandelt werden. Weitere Informationen zu normalisierungs Überlegungen, die sich auf die Implementierung der Wörter Trennung auswirken können, finden Sie unter [Normalisierung von Oberflächen](surface-form-normalization.md)Formularen.

## <a name="noise-words"></a>Füll Wörter

Füll Wörter, auch als Stoppwörter bezeichnet, sind Wörter, die keine signifikanten Indikatoren für Inhalte sind. Der Indizierungs Dienst entfernt Füll Wörter aus den Abfrage Begriffen und aus dem Inhalt, der im Volltextindex enthalten ist. Ein *Offset* ist das Vorkommen eines Worts in einem Dokument oder in einer Liste von Abfrage Begriffen. Der Offset von Füll Wörtern in einem Dokument oder in einer Abfrage wird als leer aufgezeichnet. Das Entfernen von Füll Wörtern verbessert die Abfrageleistung, da unnötige Index Vergrößerung vermieden wird. Außerdem wird die Relevanz der Abfrageergebnisse verbessert. Sie können Windows Search so konfigurieren, dass Füll Wortlisten für bestimmte Sprachen verwendet werden. Diese Listen werden verwendet, wenn eine Wörter Trennung für diese Sprache aufgerufen wird. Beispiel: "The" in englischer Sprache kommt so oft vor, dass es nur wenig Wert als eindeutigen Schlüssel hat. "Der" befindet sich in der Liste der Füll Wörter, wird nicht in den Inhalts Index geschrieben und gibt, wenn abgefragt wird, keine Ergebnisse zurück.

Füll Wörter dienen als Platzhalter in Ausdrucksabfragen. Ein Dokument, das den Text "Wag the Dog" enthält, wird im Index mit "WAG" bei vorkommen 1 und "Dog" am vorkommen 3 gespeichert. Die Ausdrucks Abfrage "WAG Dog" stimmt nicht überein, aber die Ausdrucks Abfrage "WAG a Dog" bewirkt, dass die Informationen zu den vorkommen übereinstimmen. Der Ausdruck "WAG lila Dog" stimmt nicht, da "Lila" nicht im Index am vorkommen 2 gefunden wurde. Eine Abfrage für "Wag the Dog" gibt jedoch Dokumente zurück, die "WAG lila Dog" enthalten, da es keine Möglichkeit gibt, effizient zu ermitteln, ob das Dokument ein nicht Rausch geschütztes Wort zwischen "WAG" und "Dog" enthielt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweitern von Sprachressourcen](extending-language-resources-in-windows-search.md)
</dt> <dt>

[Implementieren von Wörter Trennungen und Wort Stamm Erkennungen](implementing-a-word-breaker-and-stemmer.md)
</dt> <dt>

[Überlegungen zu linguistischer und Unicode](linguistic-and-unicode-considerations.md)
</dt> <dt>

[Problembehandlung bei Sprachressourcen und bewährten Methoden](troubleshooting-language-resources.md)
</dt> </dl>

 

 
