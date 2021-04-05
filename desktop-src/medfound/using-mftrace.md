---
description: MF Trace ist ein Tool zum Erstellen von Ablauf Verfolgungs Protokollen für Microsoft Media Foundation Anwendungen.
ms.assetid: f93060dc-cb64-4623-847d-5d78bca59d50
title: Verwenden von MF Trace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022f888ba8b202e4b77a3a571a25874032ec233e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755248"
---
# <a name="using-mftrace"></a>Verwenden von MF Trace

MF Trace ist ein Tool zum Erstellen von Ablauf Verfolgungs Protokollen für Microsoft Media Foundation Anwendungen.

Mftrace verwendet die Umleitungen-Bibliothek, um Media Foundation API-Aufrufe zu verbinden und Ablauf Verfolgungs Protokolle zu generieren. Mftrace kann auch Ablauf Verfolgungen von allen Komponenten aufzeichnen, die die Ereignis Ablauf Verfolgung für Windows (ETW) oder den Software Trace Präprozessor (WPP) zum Generieren von Ablauf Verfolgungen verwenden. Ablauf Verfolgungs Protokolle können generiert werden, indem ein neuer Prozess von mftrace gestartet wird, oder indem mftrace an einen vorhandenen Prozess angefügt wird.

## <a name="usage"></a>Verbrauch

**MF-Ablauf Verfolgung** \[ **-a** *Process* \] \[ **-c** *ConfigurationFile* \] \[ **-DC** \] \[ **-es** \] \[ **-k** *Keywords* \] \[ **-l** *Level* \] \[ **-o** *OutputFile* \] \[ **-v** \] \[ **-** ? \] \[ {*Befehl* \| *ETL_FILE*}\]



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Befehlszeilenargumente</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="-a_Process_ID_or_Process_Name"></span><span id="-a_process_id_or_process_name"></span><span id="-A_PROCESS_ID_OR_PROCESS_NAME"></span><strong>-a</strong> <strong></strong> <em>Prozess-ID oder Prozess Name</em><br/></td>
<td>An einen laufenden Prozess anfügen.<br/></td>
</tr>
<tr class="even">
<td><span id="-c_Configuration_File"></span><span id="-c_configuration_file"></span><span id="-C_CONFIGURATION_FILE"></span><strong>-c</strong> <strong></strong> <em>Konfigurationsdatei</em><br/></td>
<td>Liest Einstellungen aus der angegebenen Konfigurationsdatei. Weitere Informationen finden Sie unter <a href="mftrace-configuration-file.md">MF-Konfigurationsdatei</a>.<br/></td>
</tr>
<tr class="odd">
<td><span id="-dc"></span><span id="-DC"></span><strong>-DC</strong><br/></td>
<td>Deaktivieren Sie die Ablauf Verfolgung für untergeordnete Prozesse. Standardmäßig ist die Ablauf Verfolgung für untergeordnete Prozesse aktiviert.<br/></td>
</tr>
<tr class="even">
<td><span id="-es"></span><span id="-ES"></span><strong>-Es</strong><br/></td>
<td>Aktivieren Sie öffentliche Symbole.<br/></td>
</tr>
<tr class="odd">
<td><span id="-k_Keywords"></span><span id="-k_keywords"></span><span id="-K_KEYWORDS"></span><strong>-k</strong> <strong></strong> <em>Schlüsselwörter</em><br/></td>
<td>Eine durch Trennzeichen getrennte Liste von Schlüsselwörtern. Siehe <a href="mftrace-keywords.md">MF Trace-Schlüsselwörter</a>.<br/></td>
</tr>
<tr class="even">
<td><span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span><strong>-l</strong> <strong></strong> <em>Ebene</em><br/></td>
<td>Die Ablaufverfolgungsebene.<br/>
<ul>
<li>0: Keine</li>
<li>1: kritisch</li>
<li>2: Fehler</li>
<li>3: Warnung</li>
<li>4: informativ</li>
<li>5: ausführlich</li>
<li>16: Debuggen</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="-o_Output_File"></span><span id="-o_output_file"></span><span id="-O_OUTPUT_FILE"></span><strong>-o</strong> <strong></strong> <em>Ausgabedatei</em><br/></td>
<td>Schreibt die Ausgabe der Ablauf Verfolgung in die angegebene Datei. Standardmäßig wird die Ausgabe an <strong>stdout</strong>ausgegeben.<br/> Wenn eine Ausgabedatei angegeben wird, muss die Dateinamenerweiterung eine der folgenden sein:<br/>
<ul>
<li>ETL: Ereignis Ablauf Verfolgungs Protokoll-Datei (ETL).</li>
<li>. log oder. txt: Textdatei.</li>
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
<td><span id="COMMAND"></span><span id="command"></span><em>S</em><br/></td>
<td>Befehlszeilenargumente, um einen neuen Prozess zu erstellen.<br/></td>
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

Legen Sie diese Umgebungsvariable auf fest, um den Pfad zu den TMF-Dateien (Trace Message Format) für die Komponente anzugeben, um die Komponenten zu verfolgen, die den Windows-Ablaufverfolgungs-Präprozessor (WPP) verwenden.

</dd> <dt>

<span id="_NT_SYMBOL_PATH"></span><span id="_nt_symbol_path"></span>_NT_SYMBOL_PATH
</dt> <dd>

Wenn Symbol Suche aktiviert ist (**-es**), legen Sie diese Umgebungsvariable fest, um den Symbol Pfad anzugeben.

</dd> </dl>

## <a name="examples"></a>Beispiele

Erstellen Sie einen neuen Prozess, und verfolgen Sie diesen Prozess:

``` syntax
mftrace.exe wmplayer.exe Wildlife.wmv
```

Mftrace an einen vorhandenen Prozess anfügen:

``` syntax
mftrace.exe -a wmplayer.exe
mftrace.exe -a 9132
```

Ablauf Verfolgungs Ausgabe an eine Textdatei senden:

``` syntax
mftrace.exe -a wmplayer.exe -o trace.txt
```

Etw-oder WPP-Ablauf Verfolgungs Ereignisse:

``` syntax
mftrace.exe -c config.xml -o trace.txt
mftrace.exe -c config.xml -o trace.etl
```

> [!Note]  
> Im ersten Beispiel wird eine Textdatei generiert. Im zweiten Beispiel wird eine ETL-Datei generiert.

 

Eine ETL-Datei in eine Textdatei konvertieren:

``` syntax
mftrace.exe -o trace.txt trace.etl
```

## <a name="remarks"></a>Bemerkungen

Standardmäßig generiert MF Trace nur Umleitungen-Ablauf Verfolgungen. Zum Generieren von etw-oder WPP-Ablauf Verfolgungen müssen Sie eine Konfigurationsdatei bereitstellen. Die Konfigurationsdatei gibt die Namen der Ablauf Verfolgungs Anbieter an. Weitere Informationen finden Sie unter [MF-Konfigurationsdatei](mftrace-configuration-file.md).

Mftrace kann die Ausgabe an die folgenden Ziele senden:

-   **stdout** (Standard).
-   Eine Textdatei.
-   Eine binäre ETL-Datei.

Wenn Sie etw/WPP-Ablauf Verfolgungen protokollieren, ist eine ETL-Datei die effizienteste Option, da die Ablauf Verfolgungs Daten als binäre BLOB gespeichert werden. Nachdem die Ablauf Verfolgungs Sitzung vollständig ist, können Sie mftrace verwenden, um die ETL-Datei in eine Textdatei zu konvertieren.

> [!Note]  
> Bei der Ablauf Verfolgung für Umleitungen ist die Textausgabe genauso effizient wie eine ETL-Datei. Wenn Sie also nur Umleitungen-Ablauf Verfolgungen protokollieren (ohne etw/WPP-Ablauf Verfolgungen), wird die Textausgabe empfohlen.

 

Bei der Ablauf Verfolgung für Umleitungen müssen Sie mftrace an einen laufenden Prozess (**-a**) anfügen oder mftrace verwenden, um einen neuen Prozess zu erstellen. Bei etw/WPP-Ablauf Verfolgungen lauscht mftrace an jeden Ereignis Anbieter, der in der Konfigurationsdatei aufgelistet ist.

Sie können die Ablauf Verfolgungs Ergebnisse filtern, indem Sie Ablauf Verfolgungs Schlüsselwörter angeben, entweder über die Befehlszeilenoption " **-k** " oder in der Konfigurationsdatei. Die typische Verwendung besteht jedoch darin, alle Ablauf Verfolgungen zu protokollieren und dann mithilfe eines Skripts oder einer **grep** nach bestimmten Zeichen folgen Mustern zu suchen.

## <a name="interpreting-the-trace-results"></a>Interpretieren der Ablauf Verfolgungs Ergebnisse

Sie können mftrace verwenden, um Fragen zu den Ereignissen in Ihrer Media Foundation Anwendung oder Komponente zu beantworten. In der folgenden Tabelle sind einige typische Fragen aufgeführt. Die zweite Spalte enthält die Such Zeichenfolge, mit der die Frage beantwortet werden kann.



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
<td>&quot;Ctopologyhilfsprogramme:: Trace&quot;</td>
</tr>
<tr class="odd">
<td>Wurde die Medien Sitzung gestartet?</td>
<td>&quot;Mesessionstarted&quot;</td>
</tr>
<tr class="even">
<td>Welche Datei wurde abgespielt?</td>
<td>&quot;CMF sourceresolverumleitungen&quot;</td>
</tr>
<tr class="odd">
<td>Welche Medientypen sind für die quellstreams verfügbar?</td>
<td>&quot;Neuer Stream &quot; , &quot; menewstream &quot; , &quot; cmfmediasourceumleitungen:: tracepd&quot;</td>
</tr>
<tr class="even">
<td>Werden die Quelldaten Ströme Beispiele generiert?</td>
<td>&quot;Cmfmediastreamumleitungen:: Lenker Event &quot; , &quot; memediasample&quot;</td>
</tr>
<tr class="odd">
<td>Hat die Wiedergabe das Ende der Daten erreicht?</td>
<td>&quot;Meendof Stream &quot; , &quot; meendof Presentation&quot;</td>
</tr>
<tr class="even">
<td>Hat sich das Format geändert?</td>
<td>&quot;Mestreamformatchanged &quot; (Medienquellen), &quot; Neues Format &quot; , &quot; mesessionstreamsinkformatchanged &quot; (Medien senken)</td>
</tr>
<tr class="odd">
<td>Welche Objekte wurden erstellt?</td>
<td>&quot;COle32ExportDetours:: cokreateingestance&quot;</td>
</tr>
<tr class="even">
<td>Haben die Media Foundation Transformationen (MFTs) in der Pipeline alle Daten verarbeitet?</td>
<td>&quot;CMF transformumleitungen::P rocess Output &quot; , &quot; cmbtransformumleitungen::P rocessinput&quot;</td>
</tr>
<tr class="odd">
<td>Welche Zustände wurden für die MFTs festgelegt?</td>
<td>&quot;CMF transformumleitungen::P rocess Message&quot;</td>
</tr>
<tr class="even">
<td>Hat ein MFT-Anforderungs Eingabedaten eingegeben?</td>
<td>&quot;MF_E_TRANSFORM_NEED_MORE_INPUT &quot; (synchrone MFT), &quot; metransformneedinput &quot; (Asynchronous MFT).</td>
</tr>
<tr class="odd">
<td>Hat eine asynchrone MFT Ausgabedaten erzeugt?</td>
<td>&quot;Processoutputs verfügbar&quot;</td>
</tr>
<tr class="even">
<td>Haben Sie eine Media Sink Request-Stichprobe durchgeführt?</td>
<td>&quot;Mestreamsinkrequestsample&quot;</td>
</tr>
<tr class="odd">
<td>Hat eine Medien Senke Stichproben erhalten?</td>
<td>&quot;CMF streamsink Umleitungen::P rocesssample&quot;</td>
</tr>
<tr class="even">
<td>DirectShow: welche Beispiele wurden verarbeitet?</td>
<td>&quot;Beispiel &quot; , &quot; cmeminputpindetours&quot;</td>
</tr>
<tr class="odd">
<td>DirectShow: welches Filter Diagramm wurde verwendet?</td>
<td>&quot;Cgraphhilfsprogramme:: Trace&quot;</td>
</tr>
<tr class="even">
<td>Gab es mehrere Prozesse?</td>
<td>&quot;CreateProcess&quot;
<blockquote>
[!Note]<br />
Suchen Sie auch nach der Prozess-ID, die am Anfang jeder Ablauf Verfolgungs Zeile angezeigt wird.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MF-Ablauf Verfolgung](mftrace.md)
</dt> </dl>

 

 




