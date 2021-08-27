---
description: MFTrace ist ein Tool zum Generieren von Ablaufverfolgungsprotokollen für Microsoft Media Foundation Anwendungen.
ms.assetid: f93060dc-cb64-4623-847d-5d78bca59d50
title: Verwenden von MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8416fbde708dd44858fe5df580945f326944a1f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469967"
---
# <a name="using-mftrace"></a>Verwenden von MFTrace

MFTrace ist ein Tool zum Generieren von Ablaufverfolgungsprotokollen für Microsoft Media Foundation Anwendungen.

MFTrace verwendet die Detours-Bibliothek, um Media Foundation API-Aufrufe zu verknüpfen und Ablaufverfolgungsprotokolle zu generieren. MFTrace kann auch Ablaufverfolgungen von jeder Komponente aufzeichnen, die die Ereignisablaufverfolgung für Windows (ETW) oder den Software trace preprocessor (WPP) zum Generieren von Ablaufverfolgungen verwendet. Ablaufverfolgungsprotokolle können durch Starten eines neuen Prozesses aus MFTrace oder durch Anfügen von MFTrace an einen vorhandenen Prozess generiert werden.

## <a name="usage"></a>Verbrauch

**mftrace** \[ **-a** *Process* \] \[ **-c** *ConfigurationFile* \] \[ **-dc** \] \[ **-es** \] \[ **-k** *KeyWords* \] \[ **-l** *Level* \] \[ **-o** *OutputFile* \] \[ **-v** \] \[ **-?** \] \[ {*COMMAND* \| *ETL_FILE*}\]




| Befehlszeilenargumente | BESCHREIBUNG | 
|------------------------|-------------|
| <span id="-a_Process_ID_or_Process_Name"></span><span id="-a_process_id_or_process_name"></span><span id="-A_PROCESS_ID_OR_PROCESS_NAME"></span><strong>-a</strong> <strong></strong> <em>Prozess-ID oder Prozessname</em><br /> | Anfügen an einen laufenden Prozess.<br /> | 
| <span id="-c_Configuration_File"></span><span id="-c_configuration_file"></span><span id="-C_CONFIGURATION_FILE"></span><strong>-c</strong> <strong></strong> <em>Konfigurationsdatei</em><br /> | Liest Einstellungen aus der angegebenen Konfigurationsdatei. Siehe <a href="mftrace-configuration-file.md">MFTrace-Konfigurationsdatei.</a><br /> | 
| <span id="-dc"></span><span id="-DC"></span><strong>-dc</strong><br /> | Deaktivieren Sie die Ablaufverfolgung für untergeordnete Prozesse. Standardmäßig ist die Ablaufverfolgung für untergeordnete Prozesse aktiviert.<br /> | 
| <span id="-es"></span><span id="-ES"></span><strong>-es</strong><br /> | Aktivieren Sie öffentliche Symbole.<br /> | 
| <span id="-k_Keywords"></span><span id="-k_keywords"></span><span id="-K_KEYWORDS"></span><strong>-k</strong> <strong></strong> <em>Schlüsselwörter</em><br /> | Eine durch Kommas getrennte Liste von Schlüsselwörtern. Siehe <a href="mftrace-keywords.md">MFTrace-Schlüsselwörter.</a><br /> | 
| <span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span><strong>-l</strong> <strong></strong> <em>Ebene</em><br /> | Die Ablaufverfolgungsebene.<br /><ul><li>0: Keine</li><li>1: Kritisch</li><li>2: Fehler</li><li>3: Warnung</li><li>4: Informativ</li><li>5: Ausführlich</li><li>16: Debuggen</li></ul> | 
| <span id="-o_Output_File"></span><span id="-o_output_file"></span><span id="-O_OUTPUT_FILE"></span><strong>-o</strong> <strong></strong> <em>Ausgabedatei</em><br /> | Schreiben Sie die Ablaufverfolgungsausgabe in die angegebene Datei. Standardmäßig wird die Ausgabe an <strong>stdout</strong>ausgegeben.<br /> Wenn eine Ausgabedatei angegeben wird, muss die Dateinamenerweiterung eine der folgenden Sein:<br /><ul><li>.etl: ETL-Datei (Ereignisablaufverfolgungsprotokoll).</li><li>.log oder .txt: Textdatei.</li></ul> | 
| <span id="-v"></span><span id="-V"></span><strong>-v</strong><br /> | Aktivieren Sie den ausführlichen Modus.<br /> | 
| <span id="-_"></span><strong>-?</strong><br /> | Zeigt Nutzungsinformationen an.<br /> | 
| <span id="COMMAND"></span><span id="command"></span><em>BEFEHL</em><br /> | Befehlszeilenargumente zum Erstellen eines neuen Prozesses.<br /> | 
| <span id="ETL_FILE"></span><span id="etl_file"></span><em>ETL_FILE</em><br /> | Der Name einer vorhandenen ETL-Datei. Wenn dieses Argument angegeben wird, wird die ETL-Datei in die Textausgabe konvertiert.<br /> | 




 

## <a name="environment-variables"></a>Umgebungsvariablen

<dl> <dt>

<span id="TRACE_FORMAT_SEARCH_PATH"></span><span id="trace_format_search_path"></span>TRACE_FORMAT_SEARCH_PATH
</dt> <dd>

Legen Sie zum Nachverfolgen von Komponenten, die den Windows Software Trace Preprocessor (WPP) verwenden, diese Umgebungsvariable auf fest, um den Pfad zu den TMF-Dateien (Trace Message Format) für die Komponente anzugeben.

</dd> <dt>

<span id="_NT_SYMBOL_PATH"></span><span id="_nt_symbol_path"></span>_NT_SYMBOL_PATH
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




| Frage | Suchzeichenfolgen | 
|----------|----------------|
| Ist ein Fehler aufgetreten? | "0xc00d" | 
| Wurde die Topologie ordnungsgemäß aufgelöst? | "CTopologyHelpers::Trace" | 
| Wurde die Mediensitzung gestartet? | "MESessionStarted" | 
| Welche Datei wurde wiedergegeben? | "CMFSourceResolverDetours" | 
| Was sind die Medientypen für die Quellstreams? | "Neuer Stream", "MENewStream", "CMFMediaSourceDetours::TracePD" | 
| Haben die Quellstreams Beispiele generiert? | "CMFMediaStreamDetours::HandleEvent", "MEMediaSample" | 
| Hat die Wiedergabe das Ende der Daten erreicht? | "MEEndOfStream", "MEEndOfPresentation" | 
| Hat sich das Format geändert? | "MEStreamFormatChanged" (Medienquellen), "Neues Format", "MESessionStreamSinkFormatChanged" (Mediensenken) | 
| Welche Objekte wurden erstellt? | "COle32ExportDetours::CoCreateInstance" | 
| Haben die Media Foundation Transforms (MFTs) in der Pipeline Daten verarbeitet? | "CMFTransformDetours::P rocessOutput", "CMFTransformDetours::P rocessInput" | 
| Welche Zustände wurden für die MFTs festgelegt? | "CMFTransformDetours::P rocessMessage" | 
| Hat ein MFT Eingabedaten angefordert? | "MF_E_TRANSFORM_NEED_MORE_INPUT" (synchrones MFT), "METransformNeedInput" (asynchrones MFT). | 
| Hat ein asynchroner MFT Ausgabedaten erzeugt? | "ProcessOutputs verfügbar" | 
| Hat eine Mediensenke Beispiele angefordert? | "MEStreamSinkRequestSample" | 
| Hat eine Mediensenke Beispiele erhalten? | "CMFStreamSinkDetours::P rocessSample" | 
| DirectShow: Welche Beispiele wurden verarbeitet? | "sample", "CMemInputPinDetours" | 
| DirectShow: Welches Filterdiagramm wurde verwendet? | "CGraphHelpers::Trace" | 
| Gab es mehrere Prozesse? | "CreateProcess"<blockquote>[!Note]<br />Suchen Sie auch nach dem Prozessbezeichner, der am Anfang jeder Ablaufverfolgungszeile angezeigt wird.</blockquote><br /><br /> | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mftrace](mftrace.md)
</dt> </dl>

 

 




