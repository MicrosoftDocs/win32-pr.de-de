---
description: Die IFilter-Test Sammlung überprüft die Filter Handler.
ms.assetid: 5ee02af1-1dc9-4d21-868f-4c439970b1ba
title: Testen von Filter Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d2a2b0b6a6728051ab22590a481ad23a7197692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128564"
---
# <a name="testing-filter-handlers"></a>Testen von Filter Handlern

Die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Test Sammlung überprüft die Filter Handler. Die Test Sammlung bewirkt dies: Aufrufen von [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Methoden und Überprüfen der zurückgegebenen Werte auf Konformität mit der **IFilter** -Schnittstellen Spezifikation; und die Überprüfung, ob Block Bezeichner eindeutig sind und zunehmen, dass sich die **IFilter** -Schnittstelle nach der erneuten Initialisierung konsistent verhält, und dass alle **IFilter** -Methodenaufrufe mit ungültigen Parametern erwartete Fehlercodes zurückgeben. Die Test Sammlungs Programme sichern auch die Ausgabe einer Datei, die von einem Filter Handler gefiltert wurde, und überprüfen die **IFilter** -Registrierungsinformationen in der Registrierung.

Dieses Thema ist wie folgt organisiert:

- [Befehlszeilen Aufruf](#command-line-invocation)
  - [ifilttst.exe](#ifilttstexe)
  - [filtdump.exe](#filtdumpexe)
  - [filtreg.exe](#filtregexe)
  - [ifilttst.ini](#ifilttstini)
- [IFilter-Test Prozedur](#ifilter-test-procedure)
  - [Validierungs Test](#validation-test)
  - [Konsistenz Test](#consistency-test)
  - [Ungültiger Eingabe Test](#invalid-input-test)
  - [Testen verschiedener IFilter-Konfigurationen](#testing-different-ifilter-configurations)
- [Sicherstellen, dass registrierte Elemente indiziert werden](#ensuring-registered-items-get-indexed)
  - [Beispiel Protokolldatei](#sample-log-file)
  - [Beispiel Dumpdatei](#sample-dump-file)
- [Weitere Ressourcen](#additional-resources)
- [Zugehörige Themen](#related-topics)

> [!NOTE]  
> Wenn ein neuer Filter Handler für einen Dateityp als Ersatz für eine vorhandene Filter Registrierung installiert wird, sollte der Installer die aktuelle Registrierung speichern und wiederherstellen, wenn der neue Filter Handler deinstalliert wird. Es gibt keinen Mechanismus zum Verketten von Filtern. Daher ist der neue Filter Handler für die Replikation aller notwendigen Funktionen des alten Filters verantwortlich.

## <a name="command-line-invocation"></a>Command-Line Aufruf

Die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Test Sammlung besteht aus drei Befehlszeilen Anwendungen: [ifilttst.exe](#ifilttstexe), [filtdump.exe](#filtdumpexe)und [ #d2](#filtregexe) und einer Initialisierungsdatei, [ifilttst.ini](#ifilttstini).

> [!IMPORTANT]
> In Windows 7 und höher werden in verwaltetem Code geschriebene Filter explizit blockiert. Filter müssen in nativem Code geschrieben werden, da bei dem Prozess, in dem mehrere Add-Ins ausgeführt werden, mögliche Common Language Runtime (CLR)-Versions Probleme aufgetreten sind.

### <a name="ifilttstexe"></a>ifilttst.exe

Das ifilttst.exe Programm führt mehrere Tests aus, um einen Filter Handler zu validieren. Im folgenden Beispiel wird veranschaulicht, wie Sie das ifilttst.exe Programm über die Befehlszeile aufrufen:


```
ifilttst /i test.htm /l /d /v 1
```

Das Beispiel führt die folgenden Aufgaben aus:

- Weist das Programm an, die Datei zu filtern test.htm
- Leitet die Protokollmeldungen an test.htm. log um.
- Leitet die dumpnachrichten an test.htm. dmp um.
- Legt die Ausführlichkeit auf 1 fest.

Damit der vorherige Befehl funktioniert, müssen sich drei Dateien im aktuellen Arbeitsverzeichnis befinden: `test.htm` , [ifilttst.exe](#ifilttstexe)und [ifilttst.ini](#ifilttstini). Befehls Zeilenschalter sind in der folgenden Tabelle aufgeführt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Switch und mögliche Variablen</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>/i-Dateiname</strong></td>
<td>Die zu filternde Eingabedatei oder das Verzeichnis. Der Dateiname kann die Platzhalter Zeichen <code>*</code> und enthalten <code>?</code> .</td>
</tr>
<tr class="even">
<td><strong>/l</strong></td>
<td>Protokollmeldungen werden an eine Datei statt an den Bildschirm geleitet. Protokollmeldungen beschreiben die einzelnen Tests, die ausgeführt werden, sowie die Erfolgs-/Fehler-Ergebnisse der Tests. Der Name der Protokolldatei ist mit dem Namen der Eingabedatei, jedoch mit der Dateierweiterung ". log" identisch.</td>
</tr>
<tr class="odd">
<td><strong>/d</strong></td>
<td>Das Absichern von Nachrichten wird an eine Datei statt an den Bildschirm geleitet. Dumpmeldungen beschreiben den Inhalt der Blöcke. Die Blockstruktur wird gekippt, wenn der ausführlichkeits Grad 3 ist. Der Name der Dumpdatei ist mit dem Eingabe Dateinamen identisch, aber mit der Erweiterung DMP.</td>
</tr>
<tr class="even">
<td><strong>/-l</strong></td>
<td>Deaktiviert die Protokollierung. Dieses Flag überschreibt den <code>/l</code> Switch.</td>
</tr>
<tr class="odd">
<td><strong>/-d</strong></td>
<td>Deaktivieren Sie die Sicherung. Dieses Flag überschreibt den <code>/d</code> Switch.</td>
</tr>
<tr class="even">
<td><strong>/v-Ganzzahl</strong></td>
<td>Der Ausführlichkeitsgrad. Der Standardwert ist 3.
<ul>
<li>0-der Test protokolliert nur Meldungen zu bestimmten Fehlern der <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> -Schnittstelle. Der Test sichert den Block Inhalt.</li>
<li>1-der Test protokolliert Warnmeldungen und die für Ebene 0.</li>
<li>2: der Test protokolliert Nachrichten zu bestandenen Tests sowie zu den für Ebene 1 übergebenen Tests.</li>
<li>3-der Test protokolliert Informationsmeldungen und die für Ebene 2. Außerdem sichert der Test die Struktur des Blocks.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>/t-Ganzzahl</strong></td>
<td>Die Anzahl der zu startenden Threads. Der Standardwert ist 1.</td>
</tr>
<tr class="even">
<td><strong>/r-Ganzzahl</strong>]</td>
<td>Filtert Unterverzeichnisse rekursiv. Der optionale INTEGER-Parameter gibt die Tiefe an, in der Rekursion durchlaufen werden soll. Wenn keine Ganzzahl angegeben wird, oder wenn die Ganzzahl 0 ist, wird die vollständige Rekursion angenommen. Standardmäßig ist die Rekursions Tiefe 1.</td>
</tr>
<tr class="odd">
<td><strong>/c-Ganzzahl</strong></td>
<td>Gibt an, wie oft die Schleife durchlaufen werden soll. Wenn die Ganzzahl 0 ist, wird der Test unendlich durchlaufen. Standardmäßig wird der Test nur einmal durchlaufen.</td>
</tr>
</tbody>
</table>

> [!NOTE]  
> Sie müssen ein Leerzeichen zwischen dem Befehls Zeilenschalter und dem Wert einschließen.

### <a name="filtdumpexe"></a>filtdump.exe

Das filtdump.exe Programm lädt einen Filter Handler für ein angegebenes Dokument und druckt die Ausgabe, die von der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -dll erzeugt wird. Im folgenden Beispiel wird veranschaulicht, wie Sie das filtdump.exe Programm aufrufen.

```
filtdump filename.ext
```
Filtdump.exe verwendet die [iloadfilter:: loadifilter](/windows/desktop/api/filtereg/nf-filtereg-iloadfilter-loadifilter) -Methode, um die für die angegebene Dateinamenerweiterung geeignete [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -dll zu laden und die Ergebnisse zu drucken. Beispielsweise weist der folgende Befehl filtdump.exe an, den smpfilt.dll Filter Handler für die Erweiterung ". SMP" zu laden, den gesamten Text und die Eigenschaften aus der Datei "MyFile. SMP" zu extrahieren und die Ergebnisse zu drucken.

```
filtdump myfile.smp
```

### <a name="filtregexe"></a>filtreg.exe

Das filtreg.exe Programm überprüft die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Installationsinformationen in der Registrierung. Sie rufen das filtreg.exe Programm von der Befehlszeile aus, indem Sie seinen Namen eingeben, wie im folgenden Beispiel gezeigt.

```
filtreg
```

Filtreg.exe listet alle Dateinamen Erweiterungen auf, denen Filter Handler zugeordnet sind, indem die Dateinamenerweiterung und der Name der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -dll für die Erweiterung gedruckt werden. Dies ist eine einfache Möglichkeit, die korrekte Installation eines **IFilters** zu überprüfen.

### <a name="ifilttstini"></a>ifilttst.ini

Eine [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle wird initialisiert, indem die [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) -Methode aufgerufen wird. Die **IFilter:: init** -Methode übernimmt die folgenden vier Parameter:

1. *grfFlags*
2. *cAttributes*
3. *aattribute*
4. *pdwflags*

Der Benutzer des ifilttst.exe Programms der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Test Sammlung kann die Werte für diese Parameter in einer Datei namens ifilttst.ini angeben. In der folgenden Tabelle werden die Einträge in der ifilttst.ini-Datei beschrieben, in denen die ersten drei Parameter (die Eingabeparameter) angegeben werden. Eine Beispieldatei finden Sie unter [Sample ifilttst.ini File](#sample-ifilttstini-file).

> [!NOTE]  
> Es ist kein Tabelleneintrag für den *pdwflags* -Parameter vorhanden, da es sich um einen Output-Parameter handelt. vor dem Aufrufe der [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) -Methode muss kein spezieller Wert vorhanden sein.

 | Eingabe         | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Flags         | Die Namen der [**IFilter- \_ Init**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) -Flags, die durch den or-Operator verknüpft werden sollen, um den *grfFlags* -Parameter der [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) -Methode zu bilden. Die flagnamen müssen in Großbuchstaben und in derselben Zeile angegeben werden.                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *cAttributes* | Eine ganze Dezimalzahl, die den Wert *des Parameters* "-Parameter" darstellt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| *aattribute* | Dieser Eintrag muss mit " *aattributs* " beginnen und muss sich von den anderen " *aattribute* "-Einträgen innerhalb des Abschnitts unterscheiden. Zulässige Namen für den *aattribute* -Eintrag lauten: *aattribute*, *aAttributes1*, *aAttributes2* usw. Das erste Token muss eine GUID sein. Die GUID muss genau so formatiert sein, wie im `[Test3]` Abschnitt der [Beispiel ifilttst.ini Datei](#sample-ifilttstini-file)veranschaulicht. Das zweite Token kann entweder ein Eigenschaften Bezeichner (PID) sein, der aus einer Zahl in hexadezimal Notation besteht, oder ein Zeiger auf eine breit Zeichen Zeichenfolge (LPWSTR). Ein LPWSTR kann angegeben werden, indem die Zeichenfolge in doppelte Anführungszeichen eingeschlossen wird, wie im `[Test6]` Abschnitt der Beispiel ifilttst.ini Datei veranschaulicht. |

Wenn die *Flags und die* "}"-Einträge nicht angegeben sind, werden Sie standardmäßig auf 0 festgelegt. Wenn Sie "" auf "2 *" festlegen,* sollten Sie zwei *aattribute* -Namen angeben. Im- `[Test5]` Abschnitt des Beispiels ist "  " für "" "" "1", aber es wurden keine *aattribute* angegeben. Der Test ruft dann die [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) -Methode *mit "* " für "1" und " *aattribute* " auf, die gleich **null** sind. Dies ist ein nützlicher Testfall, da er wahrscheinlich eine Zugriffsverletzung in der **IFilter:: init** -Methode verursacht.

Wenn ifilttst.exe im Arbeitsverzeichnis eine Datei mit dem Namen ifilttst.ini nicht finden kann, wird eine Standardkonfiguration verwendet, um das [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) -Objekt zu initialisieren. Das folgende Beispiel veranschaulicht die Standardkonfiguration.

```
[default]
            grfFlags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

```

### <a name="sample-ifilttstini-file"></a>Beispiel ifilttst.ini Datei

Die ifilttst.ini-Datei ist in Abschnitten organisiert, wobei der Abschnitts Name in eckige Klammern eingeschlossen ist. Im Beispiel werden die Abschnitte, `[Test1]` `[Test2]` usw. benannt. Alle Abschnittsnamen müssen eindeutig sein. Der Test liest die Werte aus dem ersten Abschnitt und initialisiert den [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) mit diesen Werten. Anschließend werden alle Tests mit dieser **IFilter** -Konfiguration ausgeführt. Anschließend wird der **IFilter** freigegeben und mit den oben aufgeführten Parametern erneut initialisiert. Der Prozess wird wiederholt, bis alle Konfigurationen getestet wurden.

```
; Only extract text from the object
            [Test1]
            Flags =
            cAttributes = 0

            // Get all attributes (text-type and internal value-type properties.
            [Test2]
            Flags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

            // This also extracts just text from the object (the GUID is PSGUID_STORAGE, and the propid is
            // PID_STG_CONTENTS).
            [Test3]
            Flags = IFILTER_INIT_CANON_PARAGRAPHS IFILTER_INIT_HARD_LINE_BREAKS
            cAttributes = 1
            aAttributes1 = b725f130-47ef-101a-a5f1-02608c9eebac 13

            // Only extract requested attribute from the html object (the GUID corresponds to the HTML IFilter.
            [Test4]
            Flags = IFILTER_INIT_CANON_HYPHENS IFILTER_INIT_CANON_SPACES
            cAttributes = 1
            aAttributes1 = 70eb7a10-55d9-11cf-b75b-00aa0051fe20 2

            // Question: what happens if cAttributes is nonzero, but aAttributes is empty?
            [Test5]
            Flags = IFILTER_INIT_CANON_SPACES IFILTER_INIT_APPLY_INDEX_ATTRIBUTES IFILTER_INIT_APPLY_OTHER_ATTRIBUTES
            cAttributes = 1

            // Here is an attribute with a lpwstr instead of a propid (the lpwstr is enclosed in quotes).
            // The GUID corresponds to the meta tag clsid for the HTML IFilter.
            [Test6]
            Flags =
            cAttributes = 1
            aAttributes1 = D1B5D3F0-C0B3-11CF-9A92-00A0C908DBF1 "GENERATOR"
```

## <a name="ifilter-test-procedure"></a>IFilter-Test Prozedur

Nachdem der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) initialisiert wurde, führt das ifilttst.exe Programm eine Reihe von Tests für den **IFilter** aus. Zusätzlich zu den **IFilter** -Test Prozeduren müssen Sie sicherstellen, dass Ihre **IFilter** -Implementierung sichere Code Praktiken einsetzt. Weitere Informationen finden Sie unter "sichere Code Praktiken für Windows Search" in [Implementieren von Filter Handlern in Windows Search](-search-ifilter-constructing-filters.md).

### <a name="validation-test"></a>Validierungs Test

Bei der Überprüfung werden die einzelnen einzelnen Blöcke und alle Rückgabecodes schrittweise durch das Objekt überprüfen. Beim Validierungstest werden alle zurück [**gegebenen \_ stat**](/windows/win32/api/filter/ns-filter-stat_chunk) -Block Strukturen in einer Liste gespeichert.

Der Validierungstest überprüft die folgenden Bedingungen:

- Der [**stat \_**](/windows/win32/api/filter/ns-filter-stat_chunk)-Block.*idchunk* -Block-IDs müssen eindeutig sein und zunehmen.
- Der [**stat \_**](/windows/win32/api/filter/ns-filter-stat_chunk)-Block.*der Flags* -Parameter ist ein erkannter Block Zustand, wie z. b. " [**chunkstate**](/windows/win32/api/filter/ne-filter-chunkstate)", " \_ Block Text" oder "cenabledhunk"- \_ Wert Konstanten.
- Der [**stat \_**](/windows/win32/api/filter/ns-filter-stat_chunk)-Block.*der breaktype* -Parameter ist ein erkannter breaktyp (0, 1, 2, 3, 4).
- Wenn die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Initialisierungs Attribute angeben, dass der **IFilter** nur Segmente mit internen Werttyp Eigenschaften zurückgeben soll, muss *idchunksource* gleich 0 sein.
- Wenn der Block nicht abgeleitet ist, d. h., wenn es sich nicht um eine Eigenschaft des internen Werttyps handelt, dann ist [**stat \_**](/windows/win32/api/filter/ns-filter-stat_chunk)Block.*idchunksource* muss dem **stat \_**-Block entsprechen.*idblock*.
- [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) gibt S \_ OK oder einen anderen akzeptablen Rückgabewert zurück, wie \_ z \_ . b. Filter e Ende \_ von \_ Blöcken, Filter \_ \_ -e-Link nicht verfügbar usw \_ .
- Wenn der Block Text enthält, gibt [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) s \_ OK zurück, filtert den \_ \_ letzten \_ Text oder filtert \_ E \_ nicht \_ mehr \_ Text.
- Wenn [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) Filter \_ S \_ Last Text zurückgibt \_ , gibt der nächste **IFilter:: gettext** -Aufrufe Filter \_ E \_ nicht \_ mehr Text zurück \_ .
- Wenn der Block einen Wert enthält, gibt [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) S \_ OK zurück oder filtert \_ E \_ nicht \_ mehr \_ .

### <a name="consistency-test"></a>Konsistenz Test

Das ifilttxt.exe Programm initialisiert die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle erneut mit denselben Parametern wie im Validierungstest und führt einen Konsistenz Test aus. Wenn die **IFilter** -Implementierung mit dem Flag [**IFilter \_**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) init IFilter \_ Init \_ Indizierung nur initialisiert wurde \_ , gibt der Test die **IFilter** -Schnittstelle frei und bindet Sie erneut, bevor Sie einen weiteren Rückruf an die [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) -Methode durchführen.

Der Konsistenz Test überprüft die folgenden Bedingungen:

- Jede von der [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) -Methode zurückgegebene stat-Blockstruktur ist mit dem entsprechenden im Validierungstest zurückgegebenen **stat \_** -Block identisch. [**\_**](/windows/win32/api/filter/ns-filter-stat_chunk)
- [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) gibt S \_ OK oder einen anderen akzeptablen Rückgabewert zurück, wie \_ z \_ . b. Filter e Ende \_ von \_ Blöcken, Filter \_ \_ -e-Link nicht verfügbar usw \_ .

### <a name="invalid-input-test"></a>Ungültiger Eingabe Test

Das ifilttst.exe Programm initialisiert die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle mit denselben Parametern erneut und führt einen ungültigen Eingabe Test aus. Dieser Test durchläuft das Dokument einen Block zu einem Zeitpunkt, an dem Funktionsaufrufe nicht ordnungsgemäß ausgeführt werden, wie z. b. das Aufrufen der [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) -Methode, wenn der aktuelle Chuck Text enthält. Der Test überprüft alle Rückgabecodes auf Konformität mit der **IFilter** -Spezifikation.

Der ungültige Eingabe Test überprüft die folgenden Bedingungen:

- Wenn der aktuelle Block Text enthält, gibt [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) Filter \_ E \_ No \_ -Werte zurück, und ein [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) -Rückruf ist erfolgreich.
- Wenn der aktuelle Block einen Wert enthält, gibt [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) Filter \_ E \_ No Text zurück \_ , und ein [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) -Rückruf ist erfolgreich.
- Wenn beim vorherigen Aufruf von [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) der Filter \_ e \_ nicht \_ mehr \_ Text zurückgegeben wurde, wird bei aufeinander folgenden Aufrufen von **IFilter:: gettext** der Filter \_ e \_ nicht \_ mehr Text zurückgegeben \_ .
- Wenn der vorherige Aufruf von [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) den Filter \_ e \_ nicht \_ mehr zurückgegeben \_ hat, werden bei aufeinander folgenden Aufrufen von **IFilter:: GetValue** Filter \_ e \_ nicht \_ mehr Werte zurückgegeben \_ .
- Wenn der vorherige Aufruf von [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) das Ende von Segmenten filtert \_ \_ \_ \_ , werden nachfolgende Aufrufe von **IFilter:: GetChunk** das \_ \_ Ende von Blöcken am Ende Filtern \_ \_ .

> [!NOTE]  
> Der ungültige Eingabe Test vergleicht die aktuellen Block Strukturen mit den im Validierungstest zurückgegebenen, um sicherzustellen, dass Sie identisch sind.

### <a name="testing-different-ifilter-configurations"></a>Testen verschiedener IFilter-Konfigurationen

Mit dem ifilttst.exe Programm wird die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle freigegeben und die Bindung wieder hergestellt. dieses Mal wird Sie mit dem nächsten Parametersatz initialisiert. Der Test wiederholt den Zeitraum: Validierungstest, Konsistenz Test und Ungültiger Eingabe Test, bis alle gewünschten **IFilter** -Konfigurationen, die in [ifilttst.ini](#ifilttstini) Datei angegeben wurden, getestet wurden.

## <a name="ensuring-registered-items-get-indexed"></a>Sicherstellen, dass registrierte Elemente indiziert werden

Der abschließende Test Ihres [**IFilters**](/windows/win32/api/filter/nn-filter-ifilter) stellt sicher, dass Ihr **IFilter** ordnungsgemäß registriert ist und aufgerufen wird, um die Elemente zu indizieren, die Sie für die Verwendung registriert haben. Sie können den Katalog-Manager verwenden, um die erneute Indizierung zu initiieren, oder Sie verwenden den Crawl Scope Manager (CSM) zum Einrichten von Standardregeln, die die URLs angeben, die der Indexer durchforsten soll. Nachdem die Indizierung durchgeführt wurde, verwenden Sie die Windows-Such Benutzeroberfläche, um eine Zeichenfolge im Inhalt oder in den Eigenschaften von Elementen zu suchen. Wenn die Elemente indiziert wurden, werden Sie in den Suchergebnissen angezeigt.

Weitere Informationen zur erneuten Indizierung finden Sie unter [using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) und [using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md). Das Codebeispiel für das XML-matchingurls veranschaulicht, wie Sie angeben können, welche Dateien neu indiziert werden sollen und wie. Das Codebeispiel crawlscopecommandline veranschaulicht, wie Befehlszeilenoptionen für CSM-Indizierungs Vorgänge (Crawl Scope Manager) definiert werden. Beide Codebeispiele sind auf [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)verfügbar.

### <a name="sample-log-file"></a>Beispiel Protokolldatei

Bei der Anforderung kann das Ifilttst.exe Programm ein Protokoll mit einer Beschreibung der Schritte, die während der Ausführung ausgeführt werden, liefern. Die folgenden Beispiele sind Ausschnitte aus einer Protokolldatei, wobei der ausführlichkeits Grad auf den höchstmöglichen Wert 3 festgelegt ist.

```
            1. INFO----**** New configuration ****
            2.
            3. Section name : Test2
            4. grfFlags     : 63
            5. cAttributes  : 0
            6. aAttributes  : NONE
            7. pdwFlags     : 0
            8.
            9. INFO----Successfully bound filter.
            10.
            11. PASS----Init() returned a valid value for pdwFlags.
            12.
            13. INFO----Successfully initialized filter.
            14.
            15. INFO----Performing validation test. In this part of the test, the chunks structures
            16.         returned by the IFilter are checked for correctness, and the return values
            17.         of the IFilter calls are checked.
            18.
            19. PASS----GetChunk() succeeded.
            20.
            21. PASS----The current chunk has a legal value for the flags field.

```

Die erste Zeile ist eine Informations Meldung, die angibt, dass eine neue Konfiguration aus der ifilttst.ini Datei geladen wurde. Line (3) gibt den Abschnittsnamen in der ifilttst.ini Datei an, aus der die aktuelle Konfiguration gelesen wurde. In Zeilen (4) bis (7) werden die Parameter für [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init)aufgelistet. Die Zeilen, die mit beginnen, `INFO` sind Informationsmeldungen zur Bindung von [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) und zum Beginn des Validierungstests. Zeilen `PASS` , die mit beginnen, sind Meldungen in Bezug auf bestimmte Tests, die bestanden wurden.

Die Zeile im folgenden Protokoll Beispiel ist eine Warnung. Warnungen werden auf das [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Verhalten aufmerksam gemacht, das problematisch ist, auch wenn dies rechtmäßig Diese Warnung gibt an, dass die [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) -Methode einen Textabschnitt zurückgegeben hat, der keinen Text enthält.

```
WARNING-First call to GetText() returned FILTER_E_NO_MORE_TEXT.
```

Die folgende Beispiel Fehlermeldung gibt an, dass der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) einen nicht angeforderten Block ausgegeben hat.

```
            ERROR---The IFilter has emitted a chunk which it was not requested to emit.
            Check the initialization parameters in section Test1 of the initialization file.
            INFO----Current chunk propid : 0x5
```

Im Fall dieser Beispiel Fehlermeldung hat der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) einen Block mit einer PID von ausgegeben `0x5` . Die Überprüfung des Abschnitts `[Test1]` in ifilttst.ini würde zeigen, dass der **IFilter** so konfiguriert wurde, dass keine Blöcke mit dieser PID ausgegeben werden. Wenn z. b. weder die IFilter- \_ Init \_ \_ Index \_ Attribute noch die IFilter-init anwenden, werden \_ \_ \_ \_ im Flags-Eintrag andere Attribute festgelegt, und bei der Erstellung von " *jtributes* " würde " **IFilter** " nur Blöcke mit einer PID von ausgeben, `0x13` die dem PID- \_ STG- \_ Inhalt entsprechen.

### <a name="sample-dump-file"></a>Beispiel Dumpdatei

Bei der Anforderung kann das Ifilttst.exe Programm einen Dump mit den gefundenen Segmenten und deren Inhalt liefern. Das folgende Beispiel ist ein Auszug aus einer solchen Dumpdatei.

```
                1. Chunk ID: ........... 2
                2. Chunk Break Type: ... END OF SENTENCE
                3. Chunk State: ........ TEXT
                4. Chunk Locale: ....... 0x411
                5. Chunk Source ID: .... 2
                6. Chunk Start Source .. 0x0
                7. Chunk Length Source . 0x0
                8. GUID ................ b725f130-47ef-101a-a5f1-02608c9eebac
                9. Property ID ......... 0x13

                10. This is a HTML IFilter test page

                11. Chunk ID: ........... 3
                12. Chunk Break Type: ... END OF SENTENCE
                13. Chunk State: ........ TEXT
                14. Chunk Locale: ....... 0x411
                15. Chunk Source ID: .... 2
                16. Chunk Start Source .. 0x0
                17. Chunk Length Source . 0x0
                18. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                19. Property ID ......... 0x2

                20. This is a HTML IFilter test page

                21. Chunk ID: ........... 4
                22. Chunk Break Type: ... END OF SENTENCE
                23. Chunk State: ........ VALUE
                24. Chunk Locale: ....... 0x411
                25. Chunk Source ID: .... 2
                26. Chunk Start Source .. 0x0
                27. Chunk Length Source . 0x0
                28. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                29. Property ID ......... 0x2

                30. This is an HTML IFilter test page
```

In den ersten neun Zeilen wird die aktuelle Blockstruktur beschrieben. Die GUID und die PID entsprechen dem psguid \_ Storage/PID- \_ STG- \_ Inhalt. Dabei handelt es sich um einen Block, der Klartext enthält. Der Text befindet sich in der folgenden Blockstruktur:

```
10. This is an HTML IFilter test page
```

Der nächste Block, beginnend bei Zeile 11, verfügt über eine andere GUID, die der entspricht, `HTML IFilter` und eine andere PID, die einem HTML-href entspricht. Dies ist eine interne Werttyp Eigenschaft, die von exportiert wird `HTML IFilter` .

Der nächste Block, beginnend bei Zeile 21, verfügt über die gleiche GUID und PID, aber der Segment Zustand ist `VALUE` anstelle von `TEXT` . Beachten Sie, dass der Text in den letzten beiden Blöcken mit dem des ersten Blocks identisch ist. Da der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) für drei Attribute (nur-Text, HTML-href als Text und HTML href als Wert) entwickelt wurde, die auf diesen Ausdruck angewendet werden, werden die Ergebnisse in drei separaten Blöcken ausgegeben.

## <a name="additional-resources"></a>Weitere Ressourcen

- Das in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)verfügbare [ifiltersample](-search-sample-ifiltersample.md) -Codebeispiel veranschaulicht, wie eine IFilter-Basisklasse für die Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle erstellt wird.
- Eine Übersicht über den Indizierungsprozess finden Sie [im Abschnitt zur Indizierung](-search-indexing-process-overview.md).
- Eine Übersicht über die Dateitypen finden Sie unter [Dateitypen](../shell/fa-file-types.md).
- Informationen zum Abfragen von Datei Zuordnungs Attributen für einen Dateityp finden Sie unter " [wahrtentypen", "systemfileassociation" und "Anwendungs Registrierung](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))".

## <a name="related-topics"></a>Zugehörige Themen

[Entwickeln von Filter Handlern](-search-ifilter-conceptual.md)

[Informationen zu Filter Handlern in Windows Search](-search-ifilter-about.md)

[Bewährte Methoden zum Erstellen von Filter Handlern in Windows Search](-search-3x-wds-extidx-filters.md)

[Zurückgeben von Eigenschaften aus einem Filter Handler](-search-ifilter-property-filtering.md)

[Filtern von Handlern, die mit Windows ausgeliefert werden](-search-ifilter-implementations.md)

[Implementieren von Filter Handlern in Windows Search](-search-ifilter-constructing-filters.md)

[Registrieren von Filter Handlern](-search-ifilter-registering-filters.md)
