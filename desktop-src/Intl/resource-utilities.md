---
description: In diesem Thema werden zwei Hilfsprogramme beschrieben, die zum Erstellen vonBEREICH-Anwendungen verwendet werden.
ms.assetid: 8ba94001-fc46-41e0-a071-0dc500a20753
title: Ressourcen-Hilfsprogramme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9bb8a8608c97b700beebb53ce95fdf4b85c4d5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481506"
---
# <a name="resource-utilities"></a>Ressourcen-Hilfsprogramme

In diesem Thema werden zwei Hilfsprogramme beschrieben, die zum Erstellen vonBEREICH-Anwendungen verwendet werden. OBWOHL ESTCT ein PROGRAMMGESTEUERTEs Tool ist, verwendet AUCH DIE STANDARD-Windows RC Compiler-Hilfsprogramm. Anweisungen zur Verwendung dieser Hilfsprogramme finden Sie unter [Lokalisieren von Ressourcen und Erstellen der Anwendung.](localizing-resources-and-building-the-application.md)

## <a name="muirct-utility"></a>CT-Hilfsprogramm

DIERCT (Muirct.exe) ist ein Befehlszeilenprogramm zum Aufteilen einer ausführbaren Standarddatei in eine LN-Datei und sprachspezifische (d. h. lokalisierbare) Ressourcendateien. Jede der resultierenden Dateien enthält Ressourcenkonfigurationsdaten für die Dateizuordnung. CT ist im Microsoft Windows SDK für Windows Vista enthalten.

> [!Note]  
> Ab Windows Vista wird das Win32-Ressourcenlader aktualisiert, um Ressourcen aus sprachspezifischen Dateien sowie aus LN-Dateien zu laden.

 

### <a name="muirct-usages"></a>SYNTAXRCT-Verwendungen

1.  Teilen Sie die Binärdatei basierend auf der RC-Konfigurationsdatei in die Binärdatei \_ und die Datei "binary" auf.

    `Muirct -q rc_config [-c checksum_file [-b LangID]] [-x LangID] [-g LangId]     [-f] [-m] [-v level] source_file [output_LN_file] [output_MUI_file]`

2.  Extrahieren Sie Prüfsummen aus der \_ Prüfsummendatei, und fügen Sie sie in die Ausgabedatei \_ ein.

    `Muirct -c checksum_file [-b LangID] -e output_file`

3.  Berechnen Sie die Prüfsumme basierend auf der \_ Prüfsummendatei, und fügen Sie sie in die Ausgabedatei \_ ein.

    `Muirct  -c checksum_file [-b LangID] -q rc_config  -z output_file`

4.  Speichern Sie den Inhalt der Ressourcenkonfigurationsdaten aus der \_ Eingabedatei.

    `Muirct -d input_file`

### <a name="muirct-syntax"></a>SYNTAX VONCT

BEITCT kann die Richtung von Befehlszeilenschaltern und/oder aus einer Ressourcenkonfigurationsdatei verwendet werden, die mithilfe des Schalters -q angegeben wird.


```C++
muirct [-h|-?] [ -c checksum_file] [-b langid]  ]
     [-g langid] [-q resource configuration file<RCF>] [-v level] [-x langid]
     [-e output_file]  [-z output_file] [-f] [-d MUI'ized file] [-m file_version]

source_filename [language_neutral_filename] [mui_filename]
```



**Switches und Argumente**




| | | -h|-? | Zeigt den Hilfebildschirm an. | | -c | Gibt den Eingabeparameter an checksum_file aus dem die Ressourcen-Prüfsumme extrahiert oder berechnet werden soll. Checksum_file muss eine Win32-Binärdatei sein, die lokalisierbare Ressourcen enthält. Wenn checksum_file Ressourcen für mehr als eine Sprache enthält, muss der Schalter -b verwendet werden, um anzugeben, welche dieser Sprachen verwendet werden soll, andernfalls schlägt DERCT fehl. <br /> | | -b | Gibt die Sprache an, die verwendet werden soll, wenn checksum_file mit -c angegebene Datei Ressourcen in mehreren Sprachen enthält. Dieser Schalter kann nur in Verbindung mit dem Schalter -c verwendet werden. Der Sprachbezeichner kann im Dezimal- oder Hexadezimalformat vorliegen. FEHLER BEI DER VERWENDUNG SCHLÄGT FEHL, wenn die checksum_file Ressourcen in mehreren Sprachen enthält und -b nicht angegeben ist oder wenn die durch den Schalter -b angegebene Sprache im -b-Parameter nicht gefunden checksum_file. <br /> | | -g | Gibt die Sprach-ID an, die als endgültige Fallbacksprache in den Ressourcenkonfigurationsdatenabschnitt der LN-Datei aufgenommen werden soll. Wenn das Ressourcenladeprogramm keine angeforderte DATEI vom Thread aus den bevorzugten Sprachen der Benutzeroberfläche laden kann, verwendet es die endgültige Fallbacksprache als letzten Versuch. Der LangID-Wert kann im Dezimal- oder Hexadezimalformat angegeben werden. Beispielsweise kann Englisch (USA) durch -g 0x409 oder -g 1033 angegeben werden. <br /> | | -q | Gibt an, dass die source_file entsprechend dem output_LN_file und dem output_MUI_file in rc_config aufgeteilt werden soll. Die rc_config datei ist eine XML-formatierte Datei, die angibt, welche Ressourcen in die DATEI .sollen extrahiert werden und welche in der LN-Datei bleiben. Der rc_config kann die Verteilung von Ressourcentypen und einzelnen benannten Elementen zwischen der output_LN_file und output_MUI_file. Die source_file muss eine Win32-Binärdatei sein, die Ressourcen in einer einzelnen Sprache enthält, andernfalls schlägt DIERCT fehl. DIE DATEI wird nicht aufgeteilt, wenn sie sprachneutral ist. Dies wird durch den Sprach-ID-Wert 0 in der Datei angegeben. Die output_LN_file und output_mui_file sind die Namen der sprachneutralen Datei und DER DATEI, in die die source_file aufgeteilt wird. Diese Dateinamen sind optional. Wenn sie nicht angegeben sind, fügt DIECT die Erweiterungen .ln und .extensions an source_file. In der Regel sollten Sie die Erweiterung ".ln" entfernen, bevor Sie die Datei bereitstellen. ÜBERTT ordnet die output_LN_file und output_MUI_file zu, indem eine Prüfsumme basierend auf dem source_file-Namen und der Dateiversion berechnet und das Ergebnis in den Ressourcenkonfigurationsabschnitt jeder Ausgabedatei eingefügt wird. Bei Verwendung in Verbindung mit dem Schalter -c hat der Schalter -q Vorrang. Wenn die rc_config-Datei, die mit dem Schalter -q bereitgestellt wird, eine Prüfsumme enthält, ignoriert DIE PRÜFSUMME DEN Schalter -c und fügt den Prüfsummenwert aus dem Wert rc_config-Datei in die LN- und .files ein. Wenn kein Prüfsummenwert in der rc_config gefunden wird, berechnet DIECT die Ressourcen-Prüfsumme basierend auf dem Verhalten des Schalters -c. <br /> | | -v | Gibt den Ausführlichkeitsgrad für die Protokollierung an. Geben Sie 1 an, um alle grundlegenden Fehlermeldungen und Vorgangsergebnisse aus drucken. Geben Sie 2 an, um auch die Ressourceninformationen (Typ, Name, Sprachbezeichner) in die DATEI UND die LN-Datei ein include zu geben. Der Standardwert ist -v1. <br /> | | -x | Gibt die Sprach-ID an, mit der DURCHKNT alle Ressourcentypen markiert, die dem Ressourcenabschnitt der DATEI .dateityp hinzugefügt wurden. Der LangID-Wert kann im Dezimal- oder Hexadezimalformat angegeben werden. Beispielsweise kann Englisch (USA) durch -x 0x409 oder -x 1033 angegeben werden. <br /> | | -e | Extrahiert die ressourcenbasierte Prüfsumme, die in der checksum_file -c-Schalter bereitgestellt wird, und fügt sie in die angegebene output_file. Wenn -e angegeben wird, ignoriert DIECT alle Schalter außer dem Schalter -c. In diesem Fall checksum_file eine Win32-Binärdatei sein, die einen Ressourcenkonfigurationsdatenabschnitt mit einem Prüfsummenwert enthält. Der output_file muss eine vorhandene LN-Datei oder EINE DATEI sein. <br /> | | -z | Berechnet und fügt Ressourcen-Prüfsummendaten in die angegebene Ausgabedatei ein. BEI DER PRÜFSUMMEnberechnung wird die Eingabe mit dem Schalter -c und dem optionalen Schalter -b verwendet. Wenn Sie eine Ausgabedatei für den Schalter "-z" angeben, der nicht vorhanden ist, wird DIE OPTIONRCT mit einem Fehler beendet.<br /> Beispiel: Berechnet die Prüfsumme basierend auf lokalisierbaren Ressourcen in Notepad.exe und fügt die Prüfsumme in die Ausgabedatei Notepad2.exe.<br /><code>muirct -c notepad.exe -q myprog.rcconfig -z notepad2.exe</code><br /> | | -f | Ermöglicht das Erstellen einer DATEI VOMO, bei der die Versionsressource die einzige lokalisierbare Ressource ist. Standardmäßig ist dies von DERCT-Datei nicht zulässig.<br /> | | -d | Sucht eingebettete Ressourcenkonfigurationsdaten in der Quelldatei und zeigt sie an. Wenn Sie diesen Schalter angeben, ignoriertCT alle anderen Befehlszeilenoptionen.<br /> | | -m | Gibt die Versionsnummer an, die verwendet werden soll, wenn die Prüfsumme für die Zuordnung der Output_LN_file und output_MUI_file. <br /> | | source_filename | Name der lokalisierten binären Quelldatei; Platzhalter können nicht verwendet werden. Diese Datei darf nur Ressourcen in einer Sprache enthalten. Wenn die Datei Ressourcen in mehreren Sprachen enthält, schlägt DIE VERWENDUNG FEHL, es sei denn, der Schalter -b wird verwendet. Wenn die Datei Ressourcen mit Sprachbezeichnern enthält, die nur den Wert 0 haben, teilt DERTT die Datei nicht auf, da der Sprachbezeichner 0 eine neutrale Sprache angibt.<br /> Für den Schalter -d ist source_filename entweder eine LN-Datei oder eine sprachspezifische Ressourcendatei, für die MITTT Ressourcenkonfigurationsdaten anzeigen soll. <br /> | | language_neutral_filename | Optional. Name der LN-Datei. Wenn Sie den Namen dieser Datei nicht angeben, fügt DIECT eine zweite Erweiterung ".ln" an den Namen der Quelldatei an, die als sprachneutraler Dateiname verwendet werden soll. In der Regel sollten Sie die Erweiterung ".ln" entfernen, bevor Sie die Datei bereitstellen.<blockquote>[!Note]<br />Die LN-Datei darf keine Zeichenfolgen oder Menüs enthalten. Sie sollten sie manuell entfernen.</blockquote><br /> | | mui_filename | Optional. Name der sprachspezifischen Ressourcendatei. Wenn Sie keinen Namen angeben, fügt der NAME der Quelldatei, der als Dateiname verwendet werden soll, die zweite Erweiterung ".dateityp" an. Normalerweise erstellt DIECT-Datei eine sprachspezifische Ressourcendatei. Es wird jedoch keine Ressourcendatei erstellt, wenn eine der folgenden Bedingungen erfüllt ist:<br /><ul><li>Die ursprüngliche Binärdatei enthält keine lokalisierbaren Ressourcen.</li><li>Die einzige Ressourcensprache in der ursprünglichen Binärdatei ist die neutrale Sprache.</li><li>Die ursprüngliche Binärdatei enthält Ressourcen für mehr als eine Sprache, ohne die neutrale Sprache zu zählen. Wenn die Binärdatei Ressourcen für zwei Sprachen enthält und eine davon die neutrale Sprache ist, betrachtet das Hilfsprogramm die Datei als einsprachig und erstellt eine sprachspezifische Ressourcendatei, wenn lokalisierbare Ressourcen verfügbar sind.</li></ul> | 




 

### <a name="muirct-language-output"></a>AUSGABE DERCT-Sprache

MITTT wählt den Attributwert "UltimateFallbackLanguage" aus, der in die Konfigurationsdaten der LN-Dateiressourcen basierend auf der folgenden Reihenfolge eingefügt werden soll, von der höchsten Priorität zur niedrigsten:

1.  Das Attribut "UltimateFallbackLanguage" in der Quellressourcenkonfigurationsdatei, wenn eines als Eingabe übergeben wird.
2.  Die mit dem Schalter -g angegebene Sprache.
3.  Eingabedateisprache.

MITTT wählt den Wert des Attributs "language" aus, der in die Ressourcenkonfigurationsdaten der .attribute-Datei eingefügt werden soll, basierend auf der folgenden Reihenfolge:

1.  Das Attribut "language" in der Quellressourcenkonfigurationsdatei, wenn eines als Eingabe übergeben wird.
2.  Die durch den Schalter -x angegebene Sprache (Force Language).
3.  Eingabedateisprache.

### <a name="muirct-checksum-handling"></a>CHECKSRCT-Prüfsummenbehandlung

Das Betriebssystem berechnet normalerweise die Prüfsumme für die sprachspezifischen Ressourcen in einer Datei, es sei denn, Sie geben die Prüfsumme über eine Ressourcenkonfigurationsdatei an. Solange die Prüfsumme für die LN-Datei und alle zugeordneten sprachspezifischen Ressourcendateien und das Sprachattribut in der Ressourcenkonfiguration in der LN- und sprachabhängigen Übereinstimmung identisch ist, kann das Ressourcenlader Ressourcen erfolgreich laden.

CHECKSRCT unterstützt mehrere Methoden zum Platzieren geeigneter Prüfsummen in den Ressourcenkonfigurationsdaten:

1.  Erstellen Sie eine ausführbare Datei für jede Sprache, die sowohl Code als auch Ressourcen enthält. Verwenden Sie anschließendCT, um jede dieser Dateien in eine LN-Datei und eine sprachspezifische Ressourcendatei zu unterteilen. DERCT wird mehrmals ausgeführt, einmal, um eine Ressourcendatei für jede Sprache zu generieren. Sie können den Build wie folgt ausführen:
    1.  Verwenden Sie den Schalter -q, um einen Prüfsummenwert in der Ressourcenkonfigurationsdatei anzugeben. BEI DERCT-Datei wird dieser Wert in allen erstellten LN-Dateien und sprachspezifischen Ressourcendateien platziert. Sie müssen eine Strategie für die Auswahl dieses Werts übernehmen, wie weiter unten in diesem Thema beschrieben.
    2.  Verwenden Sie den Schalter -c (und optional auch den Schalter -b), um eine einzelne Sprache mit Ressourcen zu wählen, aus denen die PRÜFsumme extrahiert wird.
    3.  Verwenden Sie den Schalter "-z", um eine einzelne Sprache mit Ressourcen zu wählen, aus der DIE PRÜFSUMME immer extrahiert wird. Wenden Sie diese Prüfsumme an, nachdem die Dateien mit anderen Methoden erstellt wurden.
2.  Erstellen Sie eine ausführbare Datei, die sowohl Code als auch Ressourcen für eine einzelne Sprache enthält. Verwenden Sie anschließendCT, um die Ressourcen zwischen der LN-Datei und der sprachspezifischen Ressourcendatei zu teilen. Verwenden Sie abschließend ein binäres Lokalisierungstool, um die resultierende Ressourcendatei für jede Sprache zu ändern.

Die gängigste Konvention für die Prüfsummenbehandlung besteht in der Basis der Prüfsumme auf den englischen Ressourcen (USA). Sie können eine andere Konvention übernehmen, solange sie für jede LN-Datei konsistent ist. Beispielsweise ist es für ein Softwareentwicklungsunternehmen durchaus akzeptabel, seine Prüfsummen in der Software zu erstellen, die auf französischen (Frankreich)-Ressourcen anstatt auf englischen (USA)-Ressourcen basiert, solange alle Anwendungen über französische (Frankreich)-Ressourcen verfügen, auf denen die Prüfsummen basiert. Es ist auch akzeptabel, die Ressourcenkonfigurationsdatei zu verwenden, um einen beliebigen Hexadezimalwert von bis zu 16 Hexadezimalziffern als Prüfsumme zu zuweisen. Diese letzte Strategie schließt die effektive Verwendung der Schalter "-z", "-c" und "-b" vonCTRCT aus. Sie erfordert die Einführung einer Methode mit [**guidGen**](/previous-versions/windows/embedded/ms924300(v=msdn.10)) oder einem anderen Tool, um Prüfsummenwerte zu generieren. Bei dieser Strategie müssen Sie auch eine Richtlinie einrichten, um zu bestimmen, wann der Wert beim Hinzufügen neuer lokalisierbarer Ressourcen geändert werden muss.

Um die Prüfsumme englisch (USA) auf alle Dateien anzuwenden, können Sie eine der oben beschriebenen Methoden zur Prüfsummenbehandlung verwenden. Sie können z. B. die LN-Datei und die sprachspezifische Ressourcendatei für Englisch (USA) generieren und dann mithilfe des SWITCHESRCT -d die resultierende Prüfsumme abrufen. Sie können diese Prüfsumme in Ihre Ressourcenkonfigurationsdatei kopieren und mit dem Schalter -q mitCTRCT die Prüfsumme auf alle anderen Dateien anwenden.

### <a name="use-of-a-resource-configuration-file-with-muirct"></a>Verwenden einer Ressourcenkonfigurationsdatei mitCT

Sie können Ressourcenkonfigurationsdaten angeben, wenn SieCT verwenden. Unabhängig davon, ob Sie explizit eine Ressourcenkonfigurationsdatei angegeben haben, verfügt jede sprachspezifische Ressourcendatei über Ressourcenkonfigurationsdaten, ebenso wie jede LN-Datei mit einer zugeordneten Ressourcendatei. Beispiel:

-   Wenn Sie den Schalter -q verwenden, um eine Ressourcenkonfigurationsdatei anzugeben, ihre Eingabequellendatei jedoch keine lokalisierbaren Ressourcen enthält, wird keine sprachspezifische Ressourcendatei generiert, und die resultierende LN-Datei enthält keine Ressourcenkonfigurationsdaten. Wenn die Eingabequellendatei über mehrsprachige Ressourcen verfügt, wird die Datei von DERTCT nicht aufgeteilt.

> [!Note]  
> Derzeit ist das Verhalten vonCT inkonsistent, wenn das neutralResources-Element der Ressourcenkonfigurationsdatei keine resourceType-Elemente enthält und das localizedResources-Element beispielsweise Zeichenfolgen und Menüs enthält. In einem solchen Fall teilt DIECT die Ressourcen wie folgt auf:
>
> -   Alle Ressourcen in der ursprünglichen Binärdatei (einschließlich Zeichenfolgen und Menüs) sowie die RESOURCES-Ressourcen werden in der LN-Datei platziert.
> -   Zeichenfolgen, Menüs und RESOURCES-Ressourcen werden in der entsprechenden sprachspezifischen Ressourcendatei platziert.

 

### <a name="examples-for-using-muirct"></a>Beispiele für die Verwendung vonCTRCT

**Beispiele für die Standardverwendung**


```C++
muirct -q mui.MMF bar.exe barnew.exe barnew.exe.mui

muirct -d myprog.exe.mui
```



**Beispiel für LN-Dateiausgabe mit dem Schalter "-d"**

Im Folgenden finden Sie ein Beispiel für die Ausgabe der Ressourcenkonfigurationsdaten aus einer LN-Datei Shell32.dll mithilfe des Schalters -d mitCT:


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



**Beispiel für Language-Specific Ressourcendateiausgabe mit dem Schalter "-d"**

Im Folgenden finden Sie ein Beispiel für die Ausgabe der Ressourcenkonfigurationsdaten aus der DATEI "Shell32.dll.dateityp" unter Verwendung des Schalters -d fürCT:


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



## <a name="rc-compiler-utility"></a>RC-Compiler-Hilfsprogramm

RC Compiler (Rc.exe) ist ein Befehlszeilenprogramm zum Kompilieren einer Ressourcendefinitionsskriptdatei (ERWEITERUNG RC) in Ressourcendateien (Erweiterung RES). Der RC-Compiler ist im Windows SDK enthalten. In diesem Dokument wird nur die Verwendung des RC-Compilers mit DEN IMT-bezogenen Funktionen des Ressourcenladeers erläutert. Vollständige Informationen zum Compiler finden Sie unter [Informationen zu Ressourcendateien.](../menurc/about-resource-files.md)

Mit dem RC-Compiler können Sie aus einer einzelnen Gruppe von Quellen eine LN-Datei und eine separate sprachspezifische Ressourcendatei erstellen. Wie bei DERCT werden die Dateien den Ressourcenkonfigurationsdaten zugeordnet.

### <a name="rc-compiler-syntax-as-used-for-mui-resources"></a>RC-Compilersyntax, wie sie für DIE RESOURCES-Ressourcen verwendet wird

RC-Compilerschalter werden unter Verwenden von [RC ausführlich definiert.](../menurc/using-rc-the-rc-command-line-.md) In diesem Abschnitt werden nur die Switches definiert, die zum Erstellen vonBAU-Ressourcen verwendet werden. Beachten Sie, dass bei jedem Schalter die Groß-/Kleinschreibung nicht beachtet wird. Sofern nicht anders angegeben, wird davon ausgegangen, dass Ressourcentypen sprachneutral sind.


```C++
rc [-h|-?] -fm mui_res_name [-q rc_config_file_name] [-g langid] [-g1 ] [-g2 version]
```



**Switches und Argumente**




| | | -h|-? | Zeigt den Hilfebildschirm an. | | -fm | Verwendet die angegebene Ressourcendatei für sprachspezifische Ressourcen. Normalerweise erstellt der Ressourcencompiler eine sprachspezifische Ressourcendatei. Die Datei wird jedoch nicht erstellt, wenn eine der folgenden Bedingungen vorhanden ist:<br /><ul><li>Die RC-Datei enthält keine lokalisierbaren Ressourcen.</li><li>Die einzige Ressourcensprache in der RC-Datei ist die neutrale Sprache.</li><li>Die RC-Datei enthält Ressourcen für mehr als eine Sprache, ohne die neutrale Sprache zu zählen. Wenn die RC-Datei Ressourcen für zwei Sprachen enthält und eine davon die neutrale Sprache ist, betrachtet der Compiler die Datei als einsprachig. Wenn lokalisierbare Ressourcen verfügbar sind, erstellt der Compiler eine sprachspezifische Ressourcendatei.</li></ul> | | -q | Verwendet die angegebene Ressourcenkonfigurationsdatei, um die Ressourcentypen zu erhalten, die in der sprachspezifischen Ressourcendatei und der LN-Datei gespeichert werden. Weitere Informationen finden Sie unter <a href="preparing-a-resource-configuration-file.md">Vorbereiten einer Ressourcenkonfigurationsdatei.</a> Als Alternative zu diesem Schalter können Sie die Schalter -j und -k verwenden, es wird jedoch bevorzugt, eine Ressourcenkonfigurationsdatei zu verwenden. <br /> Mithilfe des Schalters -q mit einer Ressourcenkonfigurationsdatei können Sie eine elementbasierte Aufteilung implementieren und Attribute bereitstellen, die die binäre Ressourcenkonfiguration in der LN und sprachspezifischen Ressourcendatei erhalten. Diese Aufteilung ist mit den Schaltern -j und -k nicht möglich.<blockquote>[!Note]<br />Der RC Compiler Split-Prozess funktioniert nicht ordnungsgemäß, wenn Sie Ressourcen und Versionsinformationen in verschiedenen Ressourcenkonfigurationsdateien speichern. In diesem Fall teilt der RC-Compiler die Versionsinformationen nicht auf. Daher tritt beim Verknüpfen der sprachspezifischen Ressourcendatei ein Linkerfehler auf, da die Datei keine Versionsressourcen enthält.</blockquote><br /><br /> | | -g | Gibt den endgültigen <a href="language-identifiers.md">Fallbacksprachbezeichner</a> im Hexadezimalwert an.<br /> | | -g1 | Erstellt selbst dann eine RES-Datei vom Computer , wenn es sich bei der VERSION-Ressource um den einzigen lokalisierbaren Inhalt handelt. Standardmäßig erzeugt der RC-Compiler keine RES-Datei, wenn VERSION die einzige lokalisierbare Ressource ist.<br /> | | -g2 | Gibt die benutzerdefinierte Versionsnummer an, die beim Berechnen der Prüfsumme verwendet werden soll.<br /> | | mui_res_name | Ressourcendatei für sprachspezifische Ressourcen.<br /> | | rc_config_file_name | Ressourcenkonfigurationsdatei.<br /> | | langid | Sprachbezeichner.<br /> | | Version | Benutzerdefinierte Versionsnummer in einem Format wie "6.2.0.0".<br /> | 




 

### <a name="example-for-using-rc-compiler-to-build-mui-resources"></a>Beispiel für die Verwendung des RC-Compilers zum Erstellen vonBAU-Ressourcen

Zur Veranschaulichung des RC-Compiler-Vorgangs mit RESOURCES-Ressourcen sehen wir uns die folgende Befehlszeile für die Ressourcendatei Myfile.rc an:


```C++
rc -fm myfile_res.res -q myfile.rcconfig myfile.rc
```



Diese Befehlszeile bewirkt, dass der RC-Compiler Folgendes bewirkt:

-   Erstellen Sie die sprachspezifische Ressourcendatei Myfile res.res und eine sprachneutrale Ressourcendatei, die standardmäßig auf Myfile.res festgelegt ist, basierend auf dem Namen der \_ RC-Datei.
-   Fügen Sie die Ressourcentypen 2 (Item 5 6 7 8 9 10 11 12), 4, 5, 6, 9, 11, 16, 23, 240, 1024 MY TYPE der sprachspezifischen RES-Datei hinzu, wenn sie sich in der \_ RC-Datei befinden.
-   Fügen Sie den Ressourcentyp 16 zusammen mit allen anderen in der Ressourcendatei beschriebenen Ressourcentypen zur sprachneutralen RES-Datei und zur sprachspezifischen RES-Datei hinzu. Beachten Sie, dass in diesem Beispiel der Ressourcentyp 16 an zwei Stellen hinzugefügt wird.
-   Wählen Sie den Attributwert "UltimateFallbackLanguage" aus, der in die Konfigurationsdaten der LN-Dateiressource eingefügt werden soll, basierend auf den folgenden Kriterien, geordnet von der höchsten Priorität zur niedrigsten:
    -   Das Attribut "UltimateFallbackLanguage" in der Ressourcenkonfigurationsdatei, wenn eines als Eingabe übergeben wird.
    -   Sprachattributwert, der in die Ressourcenkonfigurationsdaten basierend auf der RC Compiler-Sprach reihenfolge (sprachneutrale und sprachspezifische Ressourcendateisprache) eingefügt werden soll. Zu den Überlegungen gehören die Sprache in der RC-Datei, der Sprachwert des Schalters -gl und der Bezeichner 0x0409 für Englisch (USA).

## <a name="remarks"></a>Hinweise

Wenn Sie den Ressourcentyp ICON(3), DIALOG(5), STRING(6) oder VERSION(16) in das neutralResources-Element einfügen, müssen Sie diesen Eintrag im localizedResources-Element in der Ressourcenkonfigurationsdatei duplizieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[mehrsprachige Benutzeroberfläche Verweis](multilingual-user-interface-reference.md)
</dt> <dt>

[FALLS-Ressourcenverwaltung](mui-resource-management.md)
</dt> <dt>

[Lokalisieren von Ressourcen und Erstellen der Anwendung](localizing-resources-and-building-the-application.md)
</dt> </dl>

 

 
