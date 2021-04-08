---
description: In diesem Thema werden zwei Hilfsprogramme zum Erstellen von MUI-Anwendungen beschrieben.
ms.assetid: 8ba94001-fc46-41e0-a071-0dc500a20753
title: Ressourcen Hilfsprogramme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550cf283779a57bc5ca35f88d336646b061c3f1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960354"
---
# <a name="resource-utilities"></a>Ressourcen Hilfsprogramme

In diesem Thema werden zwei Hilfsprogramme zum Erstellen von MUI-Anwendungen beschrieben. Obwohl MUI ein MUI-spezifisches Tool ist, nutzt MUI auch das standardmäßige Windows RC-Compilerdienstprogramm. Anweisungen zum Verwenden dieser Hilfsprogramme finden Sie unter [Lokalisieren von Ressourcen und entwickeln der Anwendung](localizing-resources-and-building-the-application.md).

## <a name="muirct-utility"></a>Muject-Hilfsprogramm

Muunct (Muirct.exe) ist ein Befehlszeilenprogramm zum Aufteilen einer standardmäßigen ausführbaren Datei in eine ln-Datei und sprachspezifische (lokalisierbare) Ressourcen Dateien. Jede der resultierenden Dateien enthält Ressourcen Konfigurationsdaten für die Datei Zuordnung. Muunct ist im Microsoft Windows SDK für Windows Vista enthalten.

> [!Note]  
> Ab Windows Vista wird das Win32-Ressourcen Lade Modul aktualisiert, um Ressourcen aus sprachspezifischen Dateien und aus LN-Dateien zu laden.

 

### <a name="muirct-usages"></a>Mumuct-Verwendungen

1.  Binäre Binärdatei und MUI-Datei auf Grundlage der RC- \_ Konfigurationsdatei aufteilen.

    `Muirct -q rc_config [-c checksum_file [-b LangID]] [-x LangID] [-g LangId]     [-f] [-m] [-v level] source_file [output_LN_file] [output_MUI_file]`

2.  Extrahieren Sie Prüfsumme aus der Prüfsummen \_ Datei, und fügen Sie Sie in die Ausgabe \_ Datei ein.

    `Muirct -c checksum_file [-b LangID] -e output_file`

3.  Berechnen Sie die Prüfsumme basierend auf der Prüfsummen \_ Datei, und fügen Sie Sie in die Ausgabe \_ Datei ein.

    `Muirct  -c checksum_file [-b LangID] -q rc_config  -z output_file`

4.  Speichern Sie den Inhalt der Ressourcen Konfigurationsdaten aus der Eingabe \_ Datei.

    `Muirct -d input_file`

### <a name="muirct-syntax"></a>Mumuct-Syntax

Mumuct kann die Richtung von Befehls zeilenschaltern und/oder aus einer Ressourcen Konfigurationsdatei annehmen, die mithilfe des Schalters "-q" angegeben wird.


```C++
muirct [-h|-?] [ -c checksum_file] [-b langid]  ]
     [-g langid] [-q resource configuration file<RCF>] [-v level] [-x langid]
     [-e output_file]  [-z output_file] [-f] [-d MUI'ized file] [-m file_version]

source_filename [language_neutral_filename] [mui_filename]
```



**Switches und Argumente**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>-h |-?</td>
<td>Zeigt den Hilfe Bildschirm an.</td>
</tr>
<tr class="even">
<td>-c</td>
<td>Gibt die Eingabe checksum_file an, aus der die Ressourcen Prüfsumme extrahiert oder berechnet werden soll. Checksum_file muss eine Win32-Binärdatei sein, die lokalisierbare Ressourcen enthält. Wenn checksum_file Ressourcen für mehr als eine Sprache enthält, muss der Schalter-b verwendet werden, um anzugeben, welche dieser verwendet werden soll, andernfalls tritt ein Fehler auf. <br/></td>
</tr>
<tr class="odd">
<td>-b</td>
<td>Gibt die Sprache an, die verwendet werden soll, wenn die mit-c angegebene checksum_file Ressourcen in mehreren Sprachen enthält. Dieser Switch kann nur in Verbindung mit dem Schalter-c verwendet werden. Der sprach Bezeichner kann im Dezimal-oder Hexadezimal Format vorliegen. Muunct schlägt fehl, wenn die checksum_file Ressourcen in mehreren Sprachen enthält und-b nicht angegeben ist oder wenn die durch den Schalter-b angegebene Sprache im checksum_file nicht gefunden werden kann. <br/></td>
</tr>
<tr class="even">
<td>-g</td>
<td>Gibt die Sprach-ID an, die als ultimative Fall Back Sprache im Abschnitt mit den Ressourcen Konfigurationsdaten der LN-Datei enthalten sein soll. Wenn das Ressourcen Lade Modul eine angeforderte MUI-Datei nicht von den bevorzugten Benutzeroberflächen Sprachen des Threads lädt, wird als letzter Versuch die endgültige Fall Back Sprache verwendet. Der langid-Wert kann im Dezimal-oder Hexadezimal Format angegeben werden. Beispielsweise kann Englisch (USA) durch-g 0x409 oder-g 1033 angegeben werden. <br/></td>
</tr>
<tr class="odd">
<td>-q</td>
<td>Gibt an, dass die source_file in den output_LN_file und die output_MUI_file entsprechend dem Layout der rc_config Datei aufgeteilt werden soll. Bei der rc_config-Datei handelt es sich um eine XML-formatierte Datei, die angibt, welche Ressourcen in die MUI-Datei extrahiert werden und in der LN-Datei verbleiben. Der rc_config kann die Verteilung von Ressourcentypen und einzelnen benannten Elementen zwischen dem output_LN_file und output_MUI_file angeben. Der source_file muss eine Win32-Binärdatei sein, die Ressourcen in einer einzelnen Sprache enthält, andernfalls tritt ein Fehler auf. Muunct teilt die Datei nicht, wenn Sie sprachneutral ist. Dies wird durch den Sprach-ID-Wert 0 in der Datei angegeben. Bei den output_LN_file und output_mui_file handelt es sich um die Namen der sprach neutralen Datei und der MUI-Datei, in die der source_file aufgeteilt ist. Diese Dateinamen sind optional. Wenn Sie nicht angegeben werden, fügt muunct die Erweiterungen. ln und. MUI an source_file an. Normalerweise sollten Sie die &quot; Erweiterung ". ln" entfernen, &quot; bevor Sie die Datei bereitstellen. Muunct verknüpft die output_LN_file und output_MUI_file, indem eine Prüfsumme basierend auf dem source_file Namen und der Dateiversion berechnet und das Ergebnis in den Ressourcen Konfigurations Abschnitt jeder Ausgabedatei eingefügt wird. Bei Verwendung in Verbindung mit dem Schalter-c hat der Schalter-q Vorrang. Wenn die mit dem Schalter-q bereitgestellte rc_config Datei eine Prüfsumme enthält, ignoriert den Schalter-c und fügt den Prüfsummen Wert aus dem Wert rc_config Datei in die LN-und MUI-Dateien ein. Wenn im rc_config kein Prüfsummen Wert gefunden wird, berechnet muunct die Ressourcen Prüfsumme basierend auf dem Verhalten des Schalters-c. <br/></td>
</tr>
<tr class="even">
<td>-v</td>
<td>Gibt die Ebene der Ausführlichkeit für die Protokollierung an. Geben Sie 1 an, um alle grundlegenden Fehlermeldungen und Vorgangs Ergebnisse zu drucken. Geben Sie 2 an, um auch die in der MUI-Datei und der LN-Datei enthaltenen Ressourcen Informationen (Typ, Name, sprach Bezeichner) einzubeziehen. Der Standardwert ist-v 1. <br/></td>
</tr>
<tr class="odd">
<td>-X</td>
<td>Gibt die Sprachen-ID an, mit der muunct alle Ressourcentypen markiert, die dem Ressourcenabschnitt der MUI-Datei hinzugefügt wurden. Der langid-Wert kann im Dezimal-oder Hexadezimal Format angegeben werden. Beispielsweise kann Englisch (USA) durch-x 0x409 oder-x 1033 angegeben werden. <br/></td>
</tr>
<tr class="even">
<td>-E</td>
<td>Extrahiert die Ressourcen Prüf Summe aus dem-checksum_file, die mit dem Schalter "-c" bereitgestellt wird, und fügt Sie in die angegebene output_file ein. Wenn-e angegeben ist, ignoriert muunct alle Switches außer dem Schalter-c. In diesem Fall muss die checksum_file eine Win32-Binärdatei sein, die einen Ressourcen Konfigurationsdaten Abschnitt mit einem Prüfsummen Wert enthält. Der output_file muss eine vorhandene LN-Datei oder MUI-Datei sein. <br/></td>
</tr>
<tr class="odd">
<td>-Z</td>
<td>Berechnet und fügt Ressourcen Prüfsummen Daten in die angegebene Ausgabedatei ein. Mumuct-Prüfsummenberechnung für die Eingabe, die mit dem Schalter "-c" bereitgestellt wird, und optional-b-Schalter. Wenn Sie eine Ausgabedatei für den nicht vorhandenen-z-Schalter angeben, wird muunct mit einem Fehler beendet.<br/> Beispiel: berechnet die Prüfsumme auf der Grundlage Lokalisier barer Ressourcen in Notepad.exe und fügt die Prüfsumme in die Ausgabedatei Notepad2.exe ein.<br/> <code>muirct -c notepad.exe -q myprog.rcconfig -z notepad2.exe</code><br/></td>
</tr>
<tr class="even">
<td>-f</td>
<td>Ermöglicht das Erstellen einer MUI-Datei, wobei die Versions Ressource die einzige lokalisierbare Ressource ist. Standardmäßig ist dies nicht zulässig.<br/></td>
</tr>
<tr class="odd">
<td>-d</td>
<td>Hiermit werden eingebettete Ressourcen Konfigurationsdaten in der Quelldatei angezeigt und angezeigt. Wenn Sie diesen Schalter angeben, ignoriert muunct alle anderen Befehlszeilenoptionen.<br/></td>
</tr>
<tr class="even">
<td>-M</td>
<td>Gibt die Versionsnummer an, die beim Berechnen der Prüfsumme zum Zuordnen der output_LN_file und output_MUI_file verwendet werden soll. <br/></td>
</tr>
<tr class="odd">
<td>source_filename</td>
<td>Der Name der lokalisierten binären Quelldatei. Platzhalter können nicht verwendet werden. Diese Datei kann nur Ressourcen in einer Sprache enthalten. Wenn sich in der Datei Ressourcen in mehreren Sprachen befinden, schlägt muunct fehl, es sei denn, der Schalter "-b" wird verwendet. Wenn die Datei Ressourcen mit sprach Bezeichnern enthält, die nur den Wert 0 haben, teilt muunct die Datei nicht, da eine Sprach-ID von 0 eine neutrale Sprache angibt.<br/> Für den Schalter "-d" ist source_filename entweder eine ln-Datei oder eine sprachspezifische Ressourcen Datei, für die die Daten der Ressourcen Konfiguration angezeigt werden. <br/></td>
</tr>
<tr class="even">
<td>language_neutral_filename</td>
<td>Dies ist optional. Name der LN-Datei. Wenn Sie den Namen dieser Datei nicht angeben, fügt muunct eine zweite Erweiterung &quot; . ln &quot; an den Quell Dateinamen an, der als sprach neutraler Dateiname verwendet werden soll. Normalerweise sollten Sie die &quot; Erweiterung ". ln" entfernen, &quot; bevor Sie die Datei bereitstellen.
<blockquote>
[!Note]<br />
Die LN-Datei darf keine Zeichen folgen oder Menüs enthalten. Sie sollten Sie manuell entfernen.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>mui_filename</td>
<td>Dies ist optional. Name der sprachspezifischen Ressourcen Datei. Wenn Sie keinen Namen angeben, fügt muunct eine zweite Erweiterung &quot; . MUI &quot; an den Quell Dateinamen an, der als Dateiname verwendet werden soll. Normalerweise erstellt muunct eine sprachspezifische Ressourcen Datei. Es wird jedoch keine Ressourcen Datei erstellt, wenn eine der folgenden Bedingungen zutrifft:<br/>
<ul>
<li>In der ursprünglichen Binärdatei befinden sich keine lokalisierbaren Ressourcen.</li>
<li>Die einzige in der ursprünglichen Binärdatei gefundene Ressourcen Sprache ist die neutrale Sprache.</li>
<li>Die ursprüngliche Binärdatei enthält Ressourcen für mehr als eine Sprache, ohne die neutrale Sprache zu zählen. Wenn die Binärdatei Ressourcen für zwei Sprachen enthält und eine von Ihnen die neutrale Sprache ist, wird die Datei vom Hilfsprogramm als monolingual betrachtet und eine sprachspezifische Ressourcen Datei erstellt, wenn lokalisierbare Ressourcen vorhanden sind.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="muirct-language-output"></a>Muout-Sprachausgabe

Muunct wählt den Wert des Attributs "ultimatefallbacklanguage" aus, der auf der Grundlage der folgenden Reihenfolge in die Konfigurationsdaten der LN-Datei Ressource eingefügt werden soll, von der höchsten Priorität bis zum niedrigsten:

1.  "Ultimatefallbacklanguage"-Attribut in der Quell Ressourcen-Konfigurationsdatei, wenn eine Eingabe als Eingabe übergeben wird.
2.  Die mit dem Schalter "-g" angegebene Sprache.
3.  Sprache der Eingabedatei.

Muzict wählt den "language"-Attribut Wert aus, der auf der Grundlage der folgenden Reihenfolge in die MUI-Datei Ressourcen-Konfigurationsdaten eingefügt werden soll:

1.  "language"-Attribut in der Quell Ressourcen-Konfigurationsdatei, wenn eine Eingabe als Eingabe erfolgt.
2.  Die durch den Schalter-x angegebene Sprache (Force Language).
3.  Sprache der Eingabedatei.

### <a name="muirct-checksum-handling"></a>Verarbeitung von Mudo-Prüfsummen

Das Betriebssystem berechnet die Prüfsumme normalerweise über die sprachspezifischen Ressourcen in einer Datei, es sei denn, Sie geben die Prüfsumme über eine Ressourcen Konfigurationsdatei an. Solange die Prüfsumme für die LN-Datei und alle zugeordneten sprachspezifischen Ressourcen Dateien und das Language-Attribut in der Ressourcen Konfiguration in den LN und der sprach abhängigen Übereinstimmung identisch ist, kann das Ressourcen Lade Modul Ressourcen erfolgreich laden.

Muunct unterstützt mehrere Methoden zum Platzieren geeigneter Prüfsummen in den Ressourcen Konfigurationsdaten:

1.  Erstellen Sie eine ausführbare Datei für jede Sprache, die sowohl Code als auch Ressourcen enthält. Verwenden Sie anschließend muunct, um jede dieser Dateien in eine ln-Datei und eine sprachspezifische Ressourcen Datei aufzuteilen. Muunct wird mehrmals ausgeführt, um eine Ressourcen Datei für jede Sprache zu generieren. Sie können den Build wie folgt ausführen:
    1.  Verwenden Sie den Schalter-q, um einen Prüfsummen Wert in der Ressourcen Konfigurationsdatei anzugeben. Diese Werte werden in alle LN-Dateien und sprachspezifischen Ressourcen Dateien eingefügt, die erstellt werden. Sie müssen eine Strategie zum Auswählen dieses Werts anwenden, wie weiter unten in diesem Thema beschrieben.
    2.  Verwenden Sie den Schalter-c (und optional auch den Schalter-b), um eine einzelne Sprache mit Ressourcen auszuwählen, von denen muunct die Prüfsumme extrahiert.
    3.  Verwenden Sie den Schalter-z, um eine einzelne Sprache mit Ressourcen auszuwählen, von denen die Prüfsumme immer extrahiert wird. Wenden Sie diese Prüfsumme an, nachdem die Dateien mit anderen Methoden erstellt wurden.
2.  Erstellen Sie eine ausführbare Datei, die sowohl Code als auch Ressourcen für eine einzelne Sprache enthält. Verwenden Sie danach muunct, um die Ressourcen zwischen der LN-Datei und der sprachspezifischen Ressourcen Datei aufzuteilen. Verwenden Sie abschließend ein binäres Lokalisierungs Tool, um die sich ergebende Ressourcen Datei für jede Sprache zu ändern.

Die häufigste Konvention für die Prüfsummen Behandlung besteht darin, die Prüfsumme auf den englischen Ressourcen (USA) zu basieren. Sie können eine andere Konvention anwenden, solange Sie für jede LN-Datei konsistent ist. Beispielsweise ist es für ein Unternehmen der Softwareentwicklung durchaus akzeptabel, dass die Prüfsummen in der Software basieren, die auf französischen Ressourcen (Frankreich) statt auf englischen (USA) Ressourcen aufbaut, solange alle Anwendungen über französische Ressourcen (Frankreich) verfügen, auf denen die Prüfsummen basieren. Es ist auch zulässig, die Ressourcen Konfigurationsdatei zu verwenden, um einen beliebigen hexadezimalen Wert von bis zu 16 hexadezimal Ziffern als Prüfsumme zuzuweisen. Diese letzte Strategie verhindert die effektive Verwendung der Schalter "-z", "-c" und "-b" von muunct. Hierfür ist es erforderlich, eine Methode zu verwenden, die entweder [**GUIDGEN**](/previous-versions/windows/embedded/ms924300(v=msdn.10)) oder ein anderes Tool verwendet, um Prüfsummen Werte zu generieren. Diese Strategie erfordert auch, dass Sie eine Richtlinie einrichten, um zu bestimmen, wann der Wert beim Hinzufügen neuer Lokalisier barer Ressourcen geändert werden muss.

Wenn Sie die englische Prüfsumme (USA) auf alle Dateien anwenden möchten, können Sie eine der oben beschriebenen Prüfsummen Behandlungsmethoden verwenden. Sie können z. b. die Datei "ln" und die sprachspezifische Ressourcen Datei für Englisch (USA) generieren und dann mit dem Schalter "muunct-d" die resultierende Prüfsumme abrufen. Sie können diese Prüfsumme in ihre Ressourcen Konfigurationsdatei kopieren und den Schalter-q mit muunct verwenden, um die Prüfsumme auf alle anderen Dateien anzuwenden.

### <a name="use-of-a-resource-configuration-file-with-muirct"></a>Verwendung einer Ressourcen Konfigurationsdatei mit muesct

Bei der Verwendung von muunct können Sie Ressourcen Konfigurationsdaten angeben. Unabhängig davon, ob Sie explizit eine Ressourcen Konfigurationsdatei angeben, enthält jede sprachspezifische Ressourcen Datei Ressourcen Konfigurationsdaten, ebenso wie jede andere Datei mit einer zugeordneten Ressourcen Datei. Beispiel:

-   Wenn Sie den Schalter-q zum Angeben einer Ressourcen Konfigurationsdatei verwenden, aber keine lokalisierbaren Ressourcen in der Eingabe Quelldatei vorhanden sind, wird keine sprachspezifische Ressourcen Datei generiert, und die resultierende LN-Datei enthält keine Ressourcen Konfigurationsdaten. Wenn die Eingabe Quelldatei über mehrsprachige Ressourcen verfügt, wird die Datei von muzct nicht geteilt.

> [!Note]  
> Das Verhalten von muunct ist derzeit nicht konsistent, wenn das neutralresources-Element der Ressourcen Konfigurationsdatei keine ResourceType-Elemente enthält und das localizedresources-Element z. b. Zeichen folgen und Menüs enthält. In einem solchen Fall teilt muunct die Ressourcen wie folgt:
>
> -   Alle Ressourcen in der ursprünglichen Binärdatei (einschließlich Zeichen folgen und Menüs) sowie die MUI-Ressourcen werden in der LN-Datei abgelegt.
> -   Zeichen folgen, Menüs und MUI-Ressourcen werden in die entsprechende sprachspezifische Ressourcen Datei eingefügt.

 

### <a name="examples-for-using-muirct"></a>Beispiele für die Verwendung von muunct

**Beispiele für die Standard Verwendung**


```C++
muirct -q mui.MMF bar.exe barnew.exe barnew.exe.mui

muirct -d myprog.exe.mui
```



**Beispiel für Ausgabe der LN-Datei mit dem Schalter "-d"**

Im folgenden finden Sie ein Beispiel für die Ausgabe der Ressourcen Konfigurationsdaten aus einer LN-Datei Shell32.dll, wobei der Schalter-d mit muunct verwendet wird:


```C++
Signature          -    fecdfecd
Length             -    148
RC Config Version  -    10000
FileType           -    11
SystemAttributes   -    100
UltimateFallback location    -  external
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    AVI FTR ORDERSTREAM TYPELIB UIFILE XML MUI
MainIDTypes        -    1 2 3 12 14 16 24
MuiNameTypes       -    MUI
MuiIDTypes         -    2 3 4 5 6 9 14 16
UltimateFallbackLanguage   -   en-US
```



**Beispiel für Language-Specific Ausgabe der Ressourcen Datei mit dem Schalter "-d"**

Im folgenden finden Sie ein Beispiel für die Ausgabe der Ressourcen Konfigurationsdaten aus einer MUI-Datei (Shell32.dll. MUI), wobei der Schalter "-d" für muunct verwendet wird:


```C++
Signature          -    fecdfecd
Length             -     c8
RC Config Version  -    10000
FileType           -    12
SystemAttributes   -    100
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    MUI
MainIDTypes        -    2 3 4 5 6 9 14 16
Language           -    en-US
```



## <a name="rc-compiler-utility"></a>RC Compiler Utility

Der RC-Compiler (Rc.exe) ist ein Befehlszeilenprogramm zum Kompilieren einer Ressourcen Definitions Skriptdatei (RC-Erweiterung) in Ressourcen Dateien (Erweiterung ". res"). Der RC-Compiler ist in der Windows SDK enthalten. In diesem Dokument wird nur die Verwendung des RC-Compilers mit MUI-bezogenen Funktionen des Ressourcen Laders erläutert. Ausführliche Informationen zum Compiler finden Sie unter Informationen [zu Ressourcen Dateien](../menurc/about-resource-files.md).

Der RC-Compiler ermöglicht das Erstellen aus einem einzelnen Satz von Quellen, einer LN-Datei und einer separaten sprachspezifischen Ressourcen Datei. Die Dateien werden in Bezug auf die Daten mithilfe von Ressourcen Konfigurationsdaten verknüpft.

### <a name="rc-compiler-syntax-as-used-for-mui-resources"></a>RC-compilersyntax wie für MUI-Ressourcen verwendet

RC-Compilerschalter werden ausführlich in [mithilfe von RC](../menurc/using-rc-the-rc-command-line-.md)definiert. In diesem Abschnitt werden nur die Schalter definiert, mit denen MUI-Ressourcen erstellt werden. Denken Sie daran, dass bei jedem Switch die Groß-/Kleinschreibung Es wird angenommen, dass Ressourcentypen sprachneutral sind, sofern nicht anders angegeben.


```C++
rc [-h|-?] -fm mui_res_name [-q rc_config_file_name] [-g langid] [-g1 ] [-g2 version]
```



**Switches und Argumente**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>-h |-?</td>
<td>Zeigt den Hilfe Bildschirm an.</td>
</tr>
<tr class="even">
<td>-FM</td>
<td>Verwendet die angegebene Ressourcen Datei für sprachspezifische Ressourcen. Normalerweise erstellt der Ressourcen Compiler eine sprachspezifische Ressourcen Datei. Die Datei wird jedoch nicht erstellt, wenn eine der folgenden Bedingungen zutrifft:<br/>
<ul>
<li>Es sind keine lokalisierbaren Ressourcen in der RC-Datei vorhanden.</li>
<li>Die einzige in der RC-Datei gefundene Ressourcen Sprache ist die neutrale Sprache.</li>
<li>Die RC-Datei enthält Ressourcen für mehr als eine Sprache, ohne die neutrale Sprache zu zählen. Wenn die RC-Datei Ressourcen für zwei Sprachen enthält und eine von Ihnen die neutrale Sprache ist, betrachtet der Compiler die Datei als monolingual. Wenn lokalisierbare Ressourcen vorhanden sind, erstellt der Compiler eine sprachspezifische Ressourcen Datei.</li>
</ul></td>
</tr>
<tr class="odd">
<td>-q</td>
<td>Verwendet die angegebene Ressourcen Konfigurationsdatei zum Abrufen der Ressourcentypen, die in der sprachspezifischen Ressourcen Datei und der LN-Datei platziert werden sollen. Weitere Informationen finden Sie unter <a href="preparing-a-resource-configuration-file.md">Vorbereiten einer Ressourcen Konfigurationsdatei</a>. Als Alternative zu diesem Switch können Sie die Schalter-j und-k verwenden, aber es wird empfohlen, eine Ressourcen Konfigurationsdatei zu verwenden. <br/> Wenn Sie den Schalter-q mit einer Ressourcen Konfigurationsdatei verwenden, können Sie eine Element basierte Teilung implementieren und Attribute bereitstellen, für die die binäre Ressourcen Konfiguration in der LN-und sprachspezifischen Ressourcen Datei enden soll. Diese Aufteilung ist mit den Switches-j und-k nicht möglich.
<blockquote>
[!Note]<br />
Der RC-compilersplit-Prozess funktioniert nicht ordnungsgemäß, wenn Sie Ressourcen und Versionsinformationen in verschiedenen Ressourcen Konfigurationsdateien speichern. In diesem Fall teilt der RC-Compiler die Versionsinformationen nicht. Daher tritt beim Verknüpfen der sprachspezifischen Ressourcen Datei ein linker-Fehler auf, da die Datei nicht über Versions Ressourcen verfügt.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>-g</td>
<td>Gibt die endgültige <a href="language-identifiers.md">Fall Back Sprachen</a> -ID im Hexadezimal Format an.<br/></td>
</tr>
<tr class="odd">
<td>-G1</td>
<td>Erstellt eine MUI. res-Datei, auch wenn die Versions Ressource der einzige lokalisierbare Inhalt ist. Standardmäßig erzeugt der RC-Compiler keine res-Datei, wenn die Version die einzige lokalisierbare Ressource ist.<br/></td>
</tr>
<tr class="even">
<td>-g2</td>
<td>Gibt die benutzerdefinierte Versionsnummer an, die beim Berechnen der Prüfsumme verwendet werden soll.<br/></td>
</tr>
<tr class="odd">
<td>mui_res_name</td>
<td>Ressourcen Datei für sprachspezifische Ressourcen.<br/></td>
</tr>
<tr class="even">
<td>rc_config_file_name</td>
<td>Ressourcen Konfigurationsdatei.<br/></td>
</tr>
<tr class="odd">
<td>langid</td>
<td>Der Sprachen Bezeichner.<br/></td>
</tr>
<tr class="even">
<td>version</td>
<td>Benutzerdefinierte Versionsnummer in einem Format wie z &quot; &quot; . b. 6.2.0.0.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="example-for-using-rc-compiler-to-build-mui-resources"></a>Beispiel für die Verwendung von RC-Compiler zum Erstellen von MUI-Ressourcen

Um den RC-compilervorgang mit MUI-Ressourcen zu veranschaulichen, betrachten wir die folgende Befehlszeile für die Ressourcen Datei "MyFile. RC":


```C++
rc -fm myfile_res.res -q myfile.rcconfig myfile.rc
```



Diese Befehlszeile bewirkt, dass der RC-Compiler folgende Aktionen durchführen kann:

-   Erstellen Sie die sprachspezifische Ressourcen Datei "MyFile \_ Res. res" und eine sprachneutrale Ressourcen Datei, die standardmäßig auf "MyFile. res" basiert, basierend auf dem Namen der RC-Datei.
-   Fügen Sie die Ressourcentypen 2 (Item 5 6 7 8 9 10 11 12), 4, 5, 6, 9, 11, 16, 23, 240, 1024 \_ Type der sprachspezifischen res-Datei hinzu, wenn Sie sich in der RC-Datei befinden.
-   Fügen Sie den Ressourcentyp 16 sowie alle anderen Ressourcentypen, die in der Ressourcen Datei beschrieben werden, der sprach neutralen res-Datei und der sprachspezifischen res-Datei hinzu. Beachten Sie, dass in diesem Beispiel der Ressourcentyp 16 an zwei Stellen hinzugefügt wird.
-   Wählen Sie den Attribut Wert "ultimatefallbacklanguage" aus, der auf der Grundlage der folgenden Kriterien in die Konfigurationsdaten der LN-Datei Ressource eingefügt werden soll:
    -   Das Attribut "ultimatefallbacklanguage" in der Ressourcen Konfigurationsdatei, wenn eines als Eingabe übergeben wird.
    -   Der sprach Attribut Wert, der basierend auf der RC-compilersprachreihenfolge (sprachneutrale Sprache und sprachspezifische Ressourcen Datei Sprache) in die Ressourcen Konfigurationsdaten eingefügt werden soll. Zu den Überlegungen zählen die Sprache in der RC-Datei, der sprach Wert des Schalters-GL und der Bezeichner 0x0409 für Englisch (USA).

## <a name="remarks"></a>Bemerkungen

Wenn Sie ein beliebiges Symbol (3), einen Dialog (5), einen Zeichen folgen-(6) oder einen Versions (16) Ressourcentyp im neutralresources-Element enthalten, müssen Sie diesen Eintrag im localizedresources-Element in der Ressourcen Konfigurationsdatei duplizieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mehrsprachige Benutzeroberflächen Referenz](multilingual-user-interface-reference.md)
</dt> <dt>

[MUI-Ressourcenverwaltung](mui-resource-management.md)
</dt> <dt>

[Lokalisieren von Ressourcen und entwickeln der Anwendung](localizing-resources-and-building-the-application.md)
</dt> </dl>

 

 
