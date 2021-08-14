---
description: MFTrace ist ein Tool zum Generieren von Ablaufverfolgungsprotokollen für Microsoft Media Foundation Anwendungen.
ms.assetid: f93060dc-cb64-4623-847d-5d78bca59d50
title: Verwenden von MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03cb19f17978236b3e4edd8415f524913c90d99d7a7caf4183dd885d340cfbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737323"
---
# <a name="using-mftrace"></a>Verwenden von MFTrace

MFTrace ist ein Tool zum Generieren von Ablaufverfolgungsprotokollen für Microsoft Media Foundation Anwendungen.

MFTrace verwendet die Detours-Bibliothek, um Media Foundation API-Aufrufe zu verknüpfen und Ablaufverfolgungsprotokolle zu generieren. MFTrace kann auch Ablaufverfolgungen von jeder Komponente aufzeichnen, die die Ereignisablaufverfolgung für Windows (ETW) oder den Software trace preprocessor (WPP) zum Generieren von Ablaufverfolgungen verwendet. Ablaufverfolgungsprotokolle können durch Starten eines neuen Prozesses aus MFTrace oder durch Anfügen von MFTrace an einen vorhandenen Prozess generiert werden.

## <a name="usage"></a>Verbrauch

**mftrace** \[ **-a** *Process* \] \[ **-c** *ConfigurationFile* \] \[ **-dc** \] \[ **-es** \] \[ **-k** *KeyWords* \] \[ **-l** *Level* \] \[ **-o** *OutputFile* \] \[ **-v** \] \[ **-?** \] \[ {*COMMAND* \| *ETL_FILE*}\]



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Befehlszeilenargumente</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="-a_Process_ID_or_Process_Name"></span><span id="-a_process_id_or_process_name"></span><span id="-A_PROCESS_ID_OR_PROCESS_NAME"></span><strong>-a</strong> <strong></strong> <em>Prozess-ID oder Prozessname</em><br/></td>
<td>Anfügen an einen laufenden Prozess.<br/></td>
</tr>
<tr class="even">
<td><span id="-c_Configuration_File"></span><span id="-c_configuration_file"></span><span id="-C_CONFIGURATION_FILE"></span><strong>-c</strong> <strong></strong> <em>Konfigurationsdatei</em><br/></td>
<td>Liest Einstellungen aus der angegebenen Konfigurationsdatei. Siehe <a href="mftrace-configuration-file.md">MFTrace-Konfigurationsdatei.</a><br/></td>
</tr>
<tr class="odd">
<td><span id="-dc"></span><span id="-DC"></span><strong>-dc</strong><br/></td>
<td>Deaktivieren Sie die Ablaufverfolgung für untergeordnete Prozesse. Standardmäßig ist die Ablaufverfolgung für untergeordnete Prozesse aktiviert.<br/></td>
</tr>
<tr class="even">
<td><span id="-es"></span><span id="-ES"></span><strong>-es</strong><br/></td>
<td>Aktivieren Sie öffentliche Symbole.<br/></td>
</tr>
<tr class="odd">
<td><span id="-k_Keywords"></span><span id="-k_keywords"></span><span id="-K_KEYWORDS"></span><strong>-k</strong> <strong></strong> <em>Schlüsselwörter</em><br/></td>
<td>Eine durch Kommas getrennte Liste von Schlüsselwörtern. Siehe <a href="mftrace-keywords.md">MFTrace-Schlüsselwörter.</a><br/></td>
</tr>
<tr class="even">
<td><span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span><strong>-l</strong> <strong></strong> <em>Ebene</em><br/></td>
<td>Die Ablaufverfolgungsebene.<br/>
<ul>
<li>0: Keine</li>
<li>1: Kritisch</li>
<li>2: Fehler</li>
<li>3: Warnung</li>
<li>4: Informativ</li>
<li>5: Ausführlich</li>
<li>16: Debuggen</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="-o_Output_File"></span><span id="-o_output_file"></span><span id="-O_OUTPUT_FILE"></span><strong>-o</strong> <strong></strong> <em>Ausgabedatei</em><br/></td>
<td>Schreiben Sie die Ablaufverfolgungsausgabe in die angegebene Datei. Standardmäßig wird die Ausgabe an <strong>stdout</strong>ausgegeben.<br/> Wenn eine Ausgabedatei angegeben wird, muss die Dateinamenerweiterung eine der folgenden Sein:<br/>
<ul>
<li>.etl: ETL-Datei (Ereignisablaufverfolgungsprotokoll).</li>
<li>.log oder .txt: Textdatei.</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="-v"></span><span id="-V"></span><strong>-v</strong><br/></td>
<td>Aktivieren Sie den ausführlichen Modus.<br/></td>
</tr>
<tr class="odd">
<td><span id="-_"></span><strong>-?</strong><br/></td>
<td>Zeigt Nutzungsinformationen an.<br/></td>
</tr>
<tr class="even">
<td><span id="COMMAND"></span><span id="command"></span><em>Befehl</em><br/></td>
<td>Befehlszeilenargumente zum Erstellen eines neuen Prozesses.<br/></td>
</tr>
<tr class="odd">
<td><span id="ETL_FILE"></span><span id="etl_file"></span><em>ETL_FILE</em><br/></td>
<td>Der Name einer vorhandenen ETL-Datei. Wenn dieses Argument angegeben wird, wird die ETL-Datei in die Textausgabe konvertiert.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="environment-variables"></a>Umgebungsvariablen

<dl> <dt>

<span id="TRACE_FORMAT_SEARCH_PATH"></span><span id="trace_format_search_path"></span>TRACE_FORMAT_SEARCH_PATH
</dt> <dd>

Um Komponenten zu verfolgen, die den Windows Software Trace Preprocessor (WPP) verwenden, legen Sie diese Umgebungsvariable auf fest, um den Pfad zu den TMF-Dateien (Trace Message Format) für die Komponente anzugeben.

</dd> <dt>

<span id="_NT_SYMBOL_PATH"></span><span id="_nt_symbol_path"></span>_nt_symbol_path
</dt> <dd>

Wenn die Symbolsuche aktiviert ist (**-es**), legen Sie diese Umgebungsvariable fest, um den Symbolpfad anzugeben.

</dd> </dl>

## <a name="examples"></a>Beispiele

Erstellen Sie einen neuen Prozess, und verfolgen Sie diesen Prozess:

``` syntax
mftrace.exe wmplayer.exe Wildlife.wmv
```

Fügen Sie MFTrace an einen vorhandenen Prozess an:

``` syntax
mftrace.exe -a wmplayer.exe
mftrace.exe -a 9132
```

Senden der Ablaufverfolgungsausgabe an eine Textdatei:

``` syntax
mftrace.exe -a wmplayer.exe -o trace.txt
```

Verfolgen Sie ETW- oder WPP-Ereignisse:

``` syntax
mftrace.exe -c config.xml -o trace.txt
mftrace.exe -c config.xml -o trace.etl
```

> [!Note]  
> Im ersten Beispiel wird eine Textdatei generiert. Im zweiten Beispiel wird eine ETL-Datei generiert.

 

Konvertieren einer ETL-Datei in eine Textdatei:

``` syntax
mftrace.exe -o trace.txt trace.etl
```

## <a name="remarks"></a>Hinweise

MfTrace generiert standardmäßig nur Ablaufverfolgungen für Umleitungen. Um ETW- oder WPP-Ablaufverfolgungen zu generieren, müssen Sie eine Konfigurationsdatei bereitstellen. Die Konfigurationsdatei gibt die Namen der Ablaufverfolgungsanbieter an. Weitere Informationen finden Sie unter [MFTrace-Konfigurationsdatei.](mftrace-configuration-file.md)

MFTrace kann die Ausgabe an die folgenden Ziele senden:

-   **stdout** (Standardeinstellung).
-   Eine Textdatei.
-   Eine binäre ETL-Datei.

Wenn Sie ETW-/WPP-Ablaufverfolgungen protokollieren, ist eine ETL-Datei die effizienteste Option, da die Ablaufverfolgungsdaten als binäre Blobs gespeichert werden. Nach Abschluss der Ablaufverfolgungssitzung können Sie mftrace verwenden, um die ETL-Datei in eine Textdatei zu konvertieren.

> [!Note]  
> Bei der Ablaufverfolgung von Umleitungen ist die Textausgabe genauso effizient wie eine ETL-Datei. Wenn Sie daher nur Ablaufverfolgungen für Umleitungen protokollieren (ohne ETW-/WPP-Ablaufverfolgungen), wird die Textausgabe empfohlen.

 

Für die Ablaufverfolgung von Umleitungen müssen Sie MFTrace an einen laufenden Prozess (**-a**) anfügen oder MFTrace verwenden, um einen neuen Prozess zu erstellen. Bei ETW-/WPP-Ablaufverfolgungen lauscht MFTrace an jedem Ereignisanbieter, der in der Konfigurationsdatei aufgeführt ist.

Sie können die Ablaufverfolgungsergebnisse filtern, indem Sie Ablaufverfolgungsschlüsselwörter angeben, entweder über die Befehlszeilenoption **-k** oder in der Konfigurationsdatei. Die typischere Verwendung besteht jedoch darin, alle Ablaufverfolgungen zu protokollieren und dann ein Skript oder **grep** zu verwenden, um nach bestimmten Zeichenfolgenmustern zu suchen.

## <a name="interpreting-the-trace-results"></a>Interpretieren der Ablaufverfolgungsergebnisse

Sie können MFTrace verwenden, um Fragen dazu zu beantworten, was in Ihrer Media Foundation Anwendung oder Komponente geschieht. In der folgenden Tabelle sind einige typische Fragen aufgeführt. Die zweite Spalte enthält die Suchzeichenfolge, mit der die Frage beantwortet werden kann.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Frage</th>
<th>Suchzeichenfolgen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ist ein Fehler aufgetreten?</td>
<td>&quot;0xc00d&quot;</td>
</tr>
<tr class="even">
<td>Wurde die Topologie ordnungsgemäß aufgelöst?</td>
<td>&quot;CTopologyHelpers::Trace&quot;</td>
</tr>
<tr class="odd">
<td>Wurde die Mediensitzung gestartet?</td>
<td>&quot;MESessionStarted&quot;</td>
</tr>
<tr class="even">
<td>Welche Datei wurde wiedergegeben?</td>
<td>&quot;CMFSourceResolverDetours&quot;</td>
</tr>
<tr class="odd">
<td>Was sind die Medientypen für die Quellstreams?</td>
<td>&quot;Neuer &quot; Stream, &quot; MENewStream, &quot; &quot; CMFMediaSourceDetours::TracePD&quot;</td>
</tr>
<tr class="even">
<td>Haben die Quellstreams Beispiele generiert?</td>
<td>&quot;CMFMediaStreamDetours::HandleEvent &quot; , &quot; MEMediaSample&quot;</td>
</tr>
<tr class="odd">
<td>Hat die Wiedergabe das Ende der Daten erreicht?</td>
<td>&quot;MEEndOfStream &quot; , &quot; MEEndOfPresentation&quot;</td>
</tr>
<tr class="even">
<td>Hat sich das Format geändert?</td>
<td>&quot;MEStreamFormatChanged &quot; (Medienquellen), &quot; Neues &quot; Format, &quot; MESessionStreamSinkFormatChanged &quot; (Mediensenken)</td>
</tr>
<tr class="odd">
<td>Welche Objekte wurden erstellt?</td>
<td>&quot;COle32ExportDetours::CoCreateInstance&quot;</td>
</tr>
<tr class="even">
<td>Haben die Media Foundation Transforms (MFTs) in der Pipeline Daten verarbeitet?</td>
<td>&quot;CMFTransformDetours::ProcessOutput &quot; , &quot; CMFTransformDetours::ProcessInput&quot;</td>
</tr>
<tr class="odd">
<td>Welche Zustände wurden für die MFTs festgelegt?</td>
<td>&quot;CMFTransformDetours::P rocessMessage&quot;</td>
</tr>
<tr class="even">
<td>Hat ein MFT Eingabedaten angefordert?</td>
<td>&quot;MF_E_TRANSFORM_NEED_MORE_INPUT &quot; (synchrones MFT), &quot; METransformNeedInput &quot; (asynchrones MFT).</td>
</tr>
<tr class="odd">
<td>Hat ein asynchroner MFT Ausgabedaten erzeugt?</td>
<td>&quot;ProcessOutputs verfügbar&quot;</td>
</tr>
<tr class="even">
<td>Hat eine Mediensenke Beispiele angefordert?</td>
<td>&quot;MEStreamSinkRequestSample&quot;</td>
</tr>
<tr class="odd">
<td>Hat eine Mediensenke Beispiele erhalten?</td>
<td>&quot;CMFStreamSinkDetours::P rocessSample&quot;</td>
</tr>
<tr class="even">
<td>DirectShow: Welche Beispiele wurden verarbeitet?</td>
<td>&quot;Beispiel, &quot; &quot; CMemInputPinDetours&quot;</td>
</tr>
<tr class="odd">
<td>DirectShow: Welches Filterdiagramm wurde verwendet?</td>
<td>&quot;CGraphHelpers::Trace&quot;</td>
</tr>
<tr class="even">
<td>Gab es mehrere Prozesse?</td>
<td>&quot;CreateProcess&quot;
<blockquote>
[!Note]<br />
Suchen Sie auch nach dem Prozessbezeichner, der am Anfang jeder Ablaufverfolgungszeile angezeigt wird.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mftrace](mftrace.md)
</dt> </dl>

 

 




