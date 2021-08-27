---
description: Die IFilter-Testsammlung überprüft Ihre Filterhandler.
ms.assetid: 5ee02af1-1dc9-4d21-868f-4c439970b1ba
title: Testen von Filterhandlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf58f14f0f8de4458dd887bf52b32fb68f869d64
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122621946"
---
# <a name="testing-filter-handlers"></a>Testen von Filterhandlern

Die [**IFilter-Testsammlung**](/windows/win32/api/filter/nn-filter-ifilter) überprüft Ihre Filterhandler. Dazu ruft die Testsammlung [**IFilter-Methoden**](/windows/win32/api/filter/nn-filter-ifilter) auf und überprüft die zurückgegebenen Werte auf Konformität mit der **IFilter-Schnittstellenspezifikation.** und überprüfen, ob Blockbezeichner eindeutig und zunehmend sind, dass sich die **IFilter-Schnittstelle** nach der erneuten Initialisierung konsistent verhält und dass alle **IFilter-Methodenaufrufe** mit ungültigen Parametern erwartete Fehlercodes zurückgeben. Die Testsammlungsprogramme speichern auch die Ausgabe einer Datei, die von einem Filterhandler gefiltert wird, und überprüfen die **IFilter-Registrierungsinformationen** in der Registrierung.

Dieses Thema ist wie folgt organisiert:

- [Befehlszeilenaufruf](#command-line-invocation)
  - [ifilttst.exe](#ifilttstexe)
  - [filtdump.exe](#filtdumpexe)
  - [filtreg.exe](#filtregexe)
  - [ifilttst.ini](#ifilttstini)
- [IFilter-Testprozedur](#ifilter-test-procedure)
  - [Validierungstest](#validation-test)
  - [Konsistenztest](#consistency-test)
  - [Ungültiger Eingabetest](#invalid-input-test)
  - [Testen verschiedener IFilter-Konfigurationen](#testing-different-ifilter-configurations)
- [Sicherstellen, dass registrierte Elemente indiziert werden](#ensuring-registered-items-get-indexed)
  - [Beispielprotokolldatei](#sample-log-file)
  - [Beispieldumpdatei](#sample-dump-file)
- [Weitere Ressourcen](#additional-resources)
- [Zugehörige Themen](#related-topics)

> [!NOTE]  
> Wenn ein neuer Filterhandler für einen Dateityp als Ersatz für eine vorhandene Filterregistrierung installiert wird, sollte das Installationsprogramm die aktuelle Registrierung speichern und wiederherstellen, wenn der neue Filterhandler deinstalliert wird. Es gibt keinen Mechanismus zum Verketten von Filtern. Daher ist der neue Filterhandler für die Replikation aller erforderlichen Funktionen des alten Filters verantwortlich.

## <a name="command-line-invocation"></a>Command-Line Aufruf

Die [**IFilter-Testsammlung**](/windows/win32/api/filter/nn-filter-ifilter) besteht aus drei Befehlszeilenanwendungen: [ifilttst.exe](#ifilttstexe), [filtdump.exe](#filtdumpexe)und [filtreg.exe](#filtregexe) sowie einer Initialisierungsdatei [ifilttst.ini](#ifilttstini).

> [!IMPORTANT]
> In Windows 7 und höher werden in verwaltetem Code geschriebene Filter explizit blockiert. Filter MÜSSEN aufgrund potenzieller CLR-Versionsprobleme (Common Language Runtime) mit dem Prozess, in dem mehrere Add-Ins ausgeführt werden, in nativem Code geschrieben werden.

### <a name="ifilttstexe"></a>ifilttst.exe

Das ifilttst.exe Programm führt mehrere Tests aus, um einen Filterhandler zu überprüfen. Im folgenden Beispiel wird veranschaulicht, wie das ifilttst.exe Programm über die Befehlszeile aufgerufen wird:


```
ifilttst /i test.htm /l /d /v 1
```

Im Beispiel werden die folgenden Aufgaben ausgeführt:

- Weist das Programm an, die Datei test.htm
- Leitet die Protokollmeldungen an test.htm.log um.
- Leitet die Dumpnachrichten an test.htm.dmp um.
- Legt die Ausführlichkeit auf 1 fest.

Damit der vorherige Befehl funktioniert, müssen sich drei Dateien im aktuellen Arbeitsverzeichnis befinden: `test.htm` , [ifilttst.exe](#ifilttstexe)und [ifilttst.ini](#ifilttstini). Befehlszeilenschalter sind in der folgenden Tabelle aufgeführt.

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Switch und mögliche Variablen</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>/i-Dateiname</strong></td>
<td>Die zu filternde Eingabedatei oder das zu filternde Verzeichnis. Der Dateiname kann die Platzhalterzeichen <code>*</code> und <code>?</code> enthalten.</td>
</tr>
<tr class="even">
<td><strong>/l</strong></td>
<td>Protokollmeldungen werden an eine Datei statt an den Bildschirm weitergeleitet. Protokollmeldungen beschreiben die einzelnen durchgeführten Tests und die Bestanden/Fehlschlagen-Ergebnisse der Tests. Der Name der Protokolldatei entspricht dem Namen der Eingabedatei, jedoch mit der Erweiterung .log.</td>
</tr>
<tr class="odd">
<td><strong>/d</strong></td>
<td>Dumpmeldungen werden an eine Datei statt an den Bildschirm weitergeleitet. Dumpmeldungen beschreiben den Inhalt der Blöcke. Die Blockstruktur wird dumped, wenn der Ausführlichkeitsgrad 3 ist. Der Name der Speicherabbilddatei entspricht dem Namen der Eingabedatei, jedoch mit der Erweiterung .dmp.</td>
</tr>
<tr class="even">
<td><strong>/-l</strong></td>
<td>Deaktivieren Sie die Protokollierung. Dieses Flag überschreibt den <code>/l</code> Schalter.</td>
</tr>
<tr class="odd">
<td><strong>/-d</strong></td>
<td>Deaktivieren Sie das Abladen. Dieses Flag überschreibt den <code>/d</code> Schalter.</td>
</tr>
<tr class="even">
<td><strong>/v integer</strong></td>
<td>Der Ausführlichkeitsgrad. Der Standardwert ist 3.
<ul>
<li>0 : Der Test protokolliert <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong></strong></a> nur Meldungen zu bestimmten IFilter-Schnittstellenfehlern. Der Test dumpt den Blockinhalt.</li>
<li>1 – Der Test protokolliert Warnmeldungen sowie warnungsmeldungen für Ebene 0.</li>
<li>2 – Der Test protokolliert Meldungen zu erfolgreichen Tests sowie zu Tests für Ebene 1.</li>
<li>3 – Der Test protokolliert Informationsmeldungen sowie meldungen für Ebene 2. Darüber hinaus gibt der Test die Struktur des Blockes ab.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>/t integer</strong></td>
<td>Die Anzahl der threads, die gestartet werden sollen. Der Standardwert ist 1.</td>
</tr>
<tr class="even">
<td><strong>/r integer</strong>]</td>
<td>Filtert Unterverzeichnisse rekursiv. Der optionale ganzzahlige Parameter gibt die Tiefe an, in die die Rekursion durchgeführt werden soll. Wenn keine ganze Zahl angegeben ist oder die ganze Zahl 0 ist, wird eine vollständige Rekursion angenommen. Standardmäßig beträgt die Rekursionstiefe 1.</td>
</tr>
<tr class="odd">
<td><strong>/c integer</strong></td>
<td>Die Anzahl der Schleifen. Wenn die ganze Zahl 0 ist, wird der Test unendlich durchlaufen. Standardmäßig wird der Test nur einmal durchlaufen.</td>
</tr>
</tbody>
</table>

> [!NOTE]  
> Sie müssen ein Leerzeichen zwischen dem Befehlszeilenschalter und dem Wert einfügen.

### <a name="filtdumpexe"></a>filtdump.exe

Das filtdump.exe Programm lädt einen Filterhandler für ein angegebenes Dokument und gibt die von der [**IFilter-DLL**](/windows/win32/api/filter/nn-filter-ifilter) erzeugte Ausgabe aus. Im folgenden Beispiel wird veranschaulicht, wie das filtdump.exe-Programm aufgerufen wird.

```
filtdump filename.ext
```
Filtdump.exe verwendet die [ILoadFilter::LoadIFilter-Methode,](/windows/desktop/api/filtereg/nf-filtereg-iloadfilter-loadifilter) um die für die angegebene Dateinamenerweiterung geeignete [**IFilter-DLL**](/windows/win32/api/filter/nn-filter-ifilter) zu laden, und gibt die Ergebnisse aus. Beispielsweise weist der folgende Befehl filtdump.exe an, den smpfilt.dll Filterhandler für die Erweiterung .smp zu laden, den gesamten Text und die Eigenschaften aus der Datei myfile.smp zu extrahieren und die Ergebnisse zu drucken.

```
filtdump myfile.smp
```

### <a name="filtregexe"></a>filtreg.exe

Das filtreg.exe-Programm überprüft [**IFilter-Installationsinformationen**](/windows/win32/api/filter/nn-filter-ifilter) in der Registrierung. Sie rufen das filtreg.exe Programm über die Befehlszeile auf, indem Sie seinen Namen eingeben, wie im folgenden Beispiel.

```
filtreg
```

Filtreg.exe listet alle Dateinamenerweiterungen auf, denen Filterhandler zugeordnet sind, indem sie die Dateinamenerweiterung und den Namen der [**IFilter-DLL**](/windows/win32/api/filter/nn-filter-ifilter) für die Erweiterung drucken. Dies ist eine einfache Möglichkeit, die richtige Installation eines **IFilter** zu überprüfen.

### <a name="ifilttstini"></a>ifilttst.ini

Eine [**IFilter-Schnittstelle**](/windows/win32/api/filter/nn-filter-ifilter) wird durch Aufrufen der [**IFilter::Init-Methode**](/windows/win32/api/filter/nf-filter-ifilter-init) initialisiert. Die **IFilter::Init-Methode** verwendet die folgenden vier Parameter:

1. *grfFlags*
2. *cAttributes*
3. *aAttributes*
4. *pdwFlags*

Der Benutzer des ifilttst.exe Programms der [**IFilter-Testsammlung**](/windows/win32/api/filter/nn-filter-ifilter) kann die Werte für diese Parameter in einer Datei namens ifilttst.ini angeben. In der folgenden Tabelle werden die Einträge in der ifilttst.ini-Datei beschrieben, die die ersten drei Parameter (die Eingabeparameter) angeben. Eine Beispieldatei finden Sie unter [Beispiel ifilttst.ini Datei](#sample-ifilttstini-file).

> [!NOTE]  
> Es gibt keinen Tabelleneintrag für den *pdwFlags-Parameter,* da es sich um einen Ausgabeparameter handelt. vor dem Aufruf der [**IFilter::Init-Methode**](/windows/win32/api/filter/nf-filter-ifilter-init) muss kein spezieller Wert vorhanden sein.

 | Eingabe         | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Flags         | Die Namen der [**IFILTER \_ INIT-Flags,**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) die vom OR-Operator verknüpft werden sollen, um den *grfFlags-Parameter* der [**IFilter::Init-Methode**](/windows/win32/api/filter/nf-filter-ifilter-init) zu bilden. Die Flagnamen müssen in Großbuchstaben und in derselben Zeile stehen.                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *cAttributes* | Eine ganze Dezimalzahl, die den Wert des *cAttributes-Parameters* darstellt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| *aAttributes* | Dieser Eintrag muss mit *aAttributes* beginnen und sich von den anderen *aAttributes-Einträgen* innerhalb des Abschnitts unterscheiden. Rechtliche Namen für den Eintrag *aAttributes* sind: *aAttributes,* *aAttributes1,* *aAttributes2* usw. Das erste Token muss eine GUID sein. Die GUID muss genau wie im `[Test3]` Abschnitt des [Beispiels ifilttst.ini Datei](#sample-ifilttstini-file)dargestellt formatiert werden. Das zweite Token kann entweder ein Eigenschaftenbezeichner (PID) sein, der aus einer Zahl in Hexadezimalschreibweise besteht, oder ein Zeiger auf eine Breitzeichenfolge (lpwstr). Ein lpwstr kann durch Einschließen der Zeichenfolge in doppelte Anführungszeichen angegeben werden, wie im `[Test6]` Abschnitt des Beispiels ifilttst.ini Datei veranschaulicht. |

Wenn die Einträge Flags und *cAttributes* nicht angegeben sind, werden sie standardmäßig auf 0 festgelegt. Wenn Sie *cAttributes* auf 2 festlegen, sollten Sie zwei *aAttributes-Namen* angeben. Im `[Test5]` Abschnitt des Beispiels ist *cAttributes* 1, aber es wurden keine *aAttributes* angegeben. Der Test ruft dann die [**IFilter::Init-Methode**](/windows/win32/api/filter/nf-filter-ifilter-init) mit *cAttributes* gleich 1 und *aAttributes* gleich **NULL** auf. Dies ist ein nützlicher Testfall, da er wahrscheinlich eine Zugriffsverletzung in der **IFilter::Init-Methode** verursacht.

Wenn ifilttst.exe keine Datei mit dem Namen ifilttst.ini im Arbeitsverzeichnis finden können, wird eine Standardkonfiguration verwendet, um das [**IFilter::Init-Objekt**](/windows/win32/api/filter/nf-filter-ifilter-init) zu initialisieren. Im folgenden Beispiel wird die Standardkonfiguration veranschaulicht.

```
[default]
            grfFlags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

```

### <a name="sample-ifilttstini-file"></a>Beispieldatei für ifilttst.ini

Die ifilttst.ini Datei ist in Abschnitten organisiert, wobei der Abschnittsname in eckige Klammern eingeschlossen ist. Im Beispiel heißen die Abschnitte `[Test1]` , `[Test2]` usw. Alle Abschnittsnamen müssen eindeutig sein. Der Test liest die Werte aus dem ersten Abschnitt und initialisiert den [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) mit diesen Werten. Anschließend werden alle Tests mit dieser **IFilter-Konfiguration** ausgeführt. Anschließend wird der **IFilter** mithilfe der oben aufgeführten Parameter freigegeben und erneut initialisiert. Der Prozess wird wiederholt, bis alle Konfigurationen getestet wurden.

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

## <a name="ifilter-test-procedure"></a>IFilter-Testprozedur

Nachdem der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) initialisiert wurde, führt das ifilttst.exe Programm eine Reihe von Tests für den **IFilter** durch. Stellen Sie neben den **IFilter-Testverfahren** sicher, dass Ihre **IFilter-Implementierung** sichere Codemethoden verwendet. Weitere Informationen finden Sie unter "Sichere Codemethoden für Windows Suche" unter [Implementieren von Filterhandlern in Windows Suche.](-search-ifilter-constructing-filters.md)

### <a name="validation-test"></a>Validierungstest

Beim Validierungstest wird das Objekt segmentiert durchlaufen, wobei jeder einzelne Block und alle Rückgabecodes überprüft werden. Der Validierungstest speichert alle zurückgegebenen [**STAT \_ CHUNK-Strukturen**](/windows/win32/api/filter/ns-filter-stat_chunk) in einer Liste.

Beim Validierungstest werden die folgenden Bedingungen überprüft:

- Der [**\_ STAT-BLOCK**](/windows/win32/api/filter/ns-filter-stat_chunk).*IdChunk-Block-IDs* müssen eindeutig sein und sich erhöhen.
- Der [**\_ STAT-BLOCK**](/windows/win32/api/filter/ns-filter-stat_chunk).*flags-Parameter* ist ein erkannter Blockzustand, z. B. [**CHUNKSTATE-,**](/windows/win32/api/filter/ne-filter-chunkstate)CHUNK \_ TEXT- oder CenabledHUNK \_ VALUE-Konstanten.
- Der [**\_ STAT-BLOCK**](/windows/win32/api/filter/ns-filter-stat_chunk).*der breakType-Parameter* ist ein erkannter Unterbrechungstyp (0, 1, 2, 3, 4).
- Wenn die IFilter-Initialisierungsattribute angeben, dass der **IFilter** nur Blöcke zurückgeben soll, die interne Werttypeigenschaften enthalten, muss *idChunkSource* gleich 0 sein. [](/windows/win32/api/filter/nn-filter-ifilter)
- Wenn der Block nicht abgeleitet wird, d. h. wenn es sich nicht um eine interne Werttypeigenschaft handelt, dann [**STAT \_ CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunkSource* muss **STAT \_ CHUNK** entsprechen.*idChunk*.
- [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) gibt S \_ OK oder einen anderen zulässigen Rückgabewert zurück, z. B. FILTER E END OF \_ \_ \_ \_ CHUNKS, FILTER \_ E LINK \_ \_ UNAVAILABLE usw.
- Wenn der Block Text enthält, gibt [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) S \_ OK, FILTER \_ S LAST TEXT oder FILTER E NO MORE \_ TEXT \_ \_ \_ \_ \_ zurück.
- Wenn [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) FILTER \_ S LAST TEXT zurückgibt, gibt der nächste Aufruf von \_ \_ **IFilter::GetText** FILTER \_ E NO MORE TEXT \_ \_ \_ zurück.
- Wenn der Block einen Wert enthält, gibt [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) S \_ OK oder FILTER E NO MORE VALUES \_ \_ \_ \_ zurück.

### <a name="consistency-test"></a>Konsistenztest

Das ifilttxt.exe Programm initialisiert die [**IFilter-Schnittstelle**](/windows/win32/api/filter/nn-filter-ifilter) erneut mit den gleichen Parametern wie im Validierungstest und führt einen Konsistenztest aus. Wenn die **IFilter-Implementierung** mit dem [**IFILTER \_ INIT**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) IFILTER \_ INIT \_ INDEXING ONLY-Flag initialisiert \_ wurde, gibt der Test die **IFilter-Schnittstelle** frei und bindet sie erneut, bevor ein weiterer Aufruf der [**IFilter::Init-Methode**](/windows/win32/api/filter/nf-filter-ifilter-init) erfolgt.

Der Konsistenztest überprüft die folgenden Bedingungen:

- Jede [**STAT \_ CHUNK-Struktur,**](/windows/win32/api/filter/ns-filter-stat_chunk) die von der [**IFilter::GetChunk-Methode**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) zurückgegeben wird, ist identisch mit der entsprechenden **STAT \_ CHUNK-Struktur,** die im Validierungstest zurückgegeben wird.
- [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) gibt S \_ OK oder einen anderen zulässigen Rückgabewert zurück, z. B. FILTER E END OF \_ \_ \_ \_ CHUNKS, FILTER \_ E LINK \_ \_ UNAVAILABLE usw.

### <a name="invalid-input-test"></a>Ungültiger Eingabetest

Das ifilttst.exe Programm initialisiert die [**IFilter-Schnittstelle**](/windows/win32/api/filter/nn-filter-ifilter) mit den gleichen Parametern erneut und führt einen ungültigen Eingabetest aus. Bei diesem Test wird das Dokument segmentweise durchlaufen, sodass Funktionsaufrufe falsch sind, z. B. das Aufrufen der [**IFilter::GetValue-Methode,**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) wenn der aktuelle Chuck Text enthält. Der Test überprüft alle Rückgabecodes auf Konformität mit der **IFilter-Spezifikation.**

Der ungültige Eingabetest überprüft die folgenden Bedingungen:

- Wenn der aktuelle Block Text enthält, gibt [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) FILTER \_ E NO VALUES \_ \_ zurück, und ein Aufruf von [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) ist erfolgreich.
- Wenn der aktuelle Block einen Wert enthält, gibt [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) FILTER \_ E NO TEXT \_ \_ zurück, und ein Aufruf von [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) ist erfolgreich.
- Wenn der vorherige Aufruf von [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) FILTER E NO MORE TEXT zurückgegeben \_ \_ \_ \_ hat, geben aufeinander folgende Aufrufe von **IFilter::GetText** FILTER \_ E NO MORE TEXT \_ \_ \_ zurück.
- Wenn der vorherige Aufruf von [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) FILTER E NO MORE VALUES zurückgegeben \_ \_ \_ \_ hat, geben aufeinander folgende Aufrufe von **IFilter::GetValue** FILTER \_ E NO MORE VALUES \_ \_ \_ zurück.
- Wenn der vorherige Aufruf von [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) FILTER \_ E END OF \_ CHUNKS zurückgegeben \_ \_ hat, geben aufeinander folgende Aufrufe von **IFilter::GetChunk** FILTER \_ E END OF \_ \_ \_ CHUNKS zurück.

> [!NOTE]  
> Der ungültige Eingabetest vergleicht die aktuellen Blockstrukturen mit denen, die im Validierungstest zurückgegeben werden, um sicherzustellen, dass sie identisch sind.

### <a name="testing-different-ifilter-configurations"></a>Testen verschiedener IFilter-Konfigurationen

Das ifilttst.exe-Programm gibt die [**IFilter-Schnittstelle**](/windows/win32/api/filter/nn-filter-ifilter) frei und stellt sie wieder her. Dieses Mal wird sie mit dem nächsten Parametersatz initialisiert. Der Test wiederholt den Zyklus: Validierungstest, Konsistenztest und ungültiger Eingabetest, bis alle in [ifilttst.ini](#ifilttstini) Datei angegebenen gewünschten **IFilter-Konfigurationen** getestet wurden.

## <a name="ensuring-registered-items-get-indexed"></a>Sicherstellen, dass registrierte Elemente indiziert werden

Der letzte Test Ihres [**IFilters**](/windows/win32/api/filter/nn-filter-ifilter) stellt sicher, dass Ihr **IFilter** ordnungsgemäß registriert ist und aufgerufen wird, um die Elemente zu indizieren, die Sie für die Verwendung registriert haben. Sie können den Katalog-Manager verwenden, um eine erneute Indizierung zu initiieren, oder die Durchforstungsbereich-Manager (CSM) verwenden, um Standardregeln einzurichten, die die URLs angeben, die der Indexer durchforsten soll. Verwenden Sie nach Abschluss der Indizierung die Windows Search-Benutzeroberfläche, um im Inhalt oder in den Eigenschaften von Elementen nach einer Zeichenfolge zu suchen. Wenn die Elemente indiziert wurden, werden sie in den Suchergebnissen angezeigt.

Weitere Informationen zur Neuindizierung finden Sie unter [Verwenden des Katalog-Managers](-search-3x-wds-mngidx-catalog-manager.md) und [Verwenden des Durchforstungsbereich-Manager](-search-3x-wds-extidx-csm.md). Im Codebeispiel ReindexMatchingUrls werden Möglichkeiten veranschaulicht, wie Sie angeben können, welche Dateien wie neu indiziert werden sollen. Im Codebeispiel CrawlScopeCommandLine wird veranschaulicht, wie Befehlszeilenoptionen für csm-Indizierungsvorgänge (Durchforstungsbereich-Manager) definiert werden. Beide Codebeispiele sind auf [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)verfügbar.

### <a name="sample-log-file"></a>Beispielprotokolldatei

Auf Anforderung kann das Ifilttst.exe-Programm ein Protokoll mit einer Beschreibung der Schritte erstellen, die während der Ausführung ausgeführt werden. Die folgenden Beispiele sind Auszüge aus einer Protokolldatei, wobei die Ausführlichkeit auf den höchsten möglichen Wert 3 festgelegt ist.

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

Die erste Zeile ist eine Informationsmeldung, die angibt, dass eine neue Konfiguration aus der ifilttst.ini-Datei geladen wurde. Zeile (3) gibt den Abschnittsnamen in der ifilttst.ini Datei an, aus der die aktuelle Konfiguration gelesen wurde. Zeilen (4) bis (7) listen die Parameter für [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init)auf. Die Zeilen, die mit `INFO` beginnen, sind Informationsmeldungen über die Bindung von [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) und den Beginn des Validierungstests. Zeilen, die mit `PASS` beginnen, sind Meldungen zu bestimmten tests, die bestanden wurden.

Die Zeile im folgenden Protokollbeispiel ist eine Warnung. Warnungen rufen die Aufmerksamkeit auf [**das IFilter-Verhalten**](/windows/win32/api/filter/nn-filter-ifilter) auf, das problematisch ist, obwohl es zulässig ist. Diese Warnung gibt an, dass die [**IFilter::GetChunk-Methode**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) einen Textabschnitt zurückgegeben hat, der keinen Text enthält.

```
WARNING-First call to GetText() returned FILTER_E_NO_MORE_TEXT.
```

Die folgende Beispielfehlermeldung gibt an, dass der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) einen Block ausgegeben hat, der nicht angefordert wurde.

```
            ERROR---The IFilter has emitted a chunk which it was not requested to emit.
            Check the initialization parameters in section Test1 of the initialization file.
            INFO----Current chunk propid : 0x5
```

Im Fall dieser Beispielfehlermeldung hat der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) einen Block mit der PID `0x5` ausgegeben. Die Überprüfung des `[Test1]` Abschnitts in ifilttst.ini zeigt, dass der **IFilter** so konfiguriert wurde, dass keine Blöcke mit dieser PID ausgegeben werden. Wenn z. B. weder IFILTER \_ INIT \_ APPLY INDEX ATTRIBUTES \_ noch \_ IFILTER \_ INIT APPLY OTHER ATTRIBUTES im \_ \_ \_ Flags-Eintrag angegeben wurden und *cAttributes* 0 wären, würde **IFilter** nur Blöcke mit einer PID von `0x13` ausgeben und dem \_ PID-STG-INHALT \_ entsprechen.

### <a name="sample-dump-file"></a>Beispieldumpdatei

Auf Anforderung kann das Ifilttst.exe Programm ein Dump erstellen, das die gefundenen Blöcke und deren Inhalt enthält. Das folgende Beispiel ist ein Auszug aus einer solchen Dumpdatei.

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

Die ersten neun Zeilen beschreiben die aktuelle Blockstruktur. Die GUID und die PID entsprechen DEM \_ PSGUID-SPEICHER-/PID-STG-INHALT. \_ \_ Dies ist ein Block, der Nur-Text enthält. Der Text befindet sich in der folgenden Blockstruktur:

```
10. This is an HTML IFilter test page
```

Der nächste Block ab Zeile 11 verfügt über eine andere GUID, die dem `HTML IFilter` entspricht, und eine andere PID, die einem HTML-HREF entspricht. Dies ist eine interne Werttypeigenschaft, die von exportiert `HTML IFilter` wird.

Der nächste Block, beginnend mit Zeile 21, hat die gleiche GUID und PID, aber sein Blockzustand ist `VALUE` anstelle von `TEXT` . Beachten Sie, dass der Text in diesen beiden letzten Blocken mit dem Text für den ersten Block identisch ist. Da der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) jedoch für drei Attribute (Nur-Text, HTML HREF als Text und HTML HREF als Wert) konzipiert ist, die auf diesen Ausdruck angewendet werden sollen, werden die Ergebnisse in drei separaten Blocken ausgegeben.

## <a name="additional-resources"></a>Weitere Ressourcen

- Das [IFilterSample-Codebeispiel,](-search-sample-ifiltersample.md) das auf GitHub verfügbar [ist,](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)veranschaulicht, wie eine IFilter-Basisklasse zum Implementieren der [**IFilter-Schnittstelle erstellt**](/windows/win32/api/filter/nn-filter-ifilter) wird.
- Eine Übersicht über den Indizierungsprozess finden Sie unter [Der Indizierungsprozess](-search-indexing-process-overview.md).
- Eine Übersicht über Dateitypen finden Sie unter [Dateitypen.](../shell/fa-file-types.md)
- Informationen zum Abfragen von Dateiassoziationsattributen für einen Dateityp finden Sie unter [PerceivedTypes, SystemFileAssociations und Application Registration.](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))

## <a name="related-topics"></a>Zugehörige Themen

[Entwickeln von Filterhandlern](-search-ifilter-conceptual.md)

[Informationen zu Filterhandlern in Windows Search](-search-ifilter-about.md)

[Bewährte Methoden zum Erstellen von Filterhandlern in Windows Suchen](-search-3x-wds-extidx-filters.md)

[Zurückgeben von Eigenschaften von einem Filterhandler](-search-ifilter-property-filtering.md)

[Filterhandler, die mit Windows](-search-ifilter-implementations.md)

[Implementieren von Filterhandlern in Windows Search](-search-ifilter-constructing-filters.md)

[Registrieren von Filterhandlern](-search-ifilter-registering-filters.md)
