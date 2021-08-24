---
description: Mit dem Quellserver kann ein Client die genaue Version der Quelldateien abrufen, die zum Erstellen einer Anwendung verwendet wurden.
ms.assetid: c7bf51ce-7fb4-49aa-ad33-e551b2c8362b
title: Quellserver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1938a617cd6c8f613df2a1113288a27f6593336f819cde2f5380a8420c329d45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815510"
---
# <a name="source-server"></a>Quellserver

Mit dem Quellserver kann ein Client die genaue Version der Quelldateien abrufen, die zum Erstellen einer Anwendung verwendet wurden. Da sich der Quellcode für ein Modul zwischen Versionen und im Laufe der Jahre ändern kann, ist es wichtig, den Quellcode so zu betrachten, wie er vorhanden war, als die Version des betreffenden Moduls erstellt wurde.

Der Quellserver ruft die entsprechenden Dateien aus der Quellcodeverwaltung ab. Um den Quellserver verwenden zu können, muss die Anwendung quellindiziert worden sein.

## <a name="source-indexing"></a>Quellindizierung

Das Quellindizierungssystem ist eine Sammlung ausführbarer Dateien und Perl-Skripts. Die Perl-Skripts erfordern Perl 5.6 oder höher.

Im Allgemeinen werden Binärdateien während des Buildprozesses nach der Erstellung der Anwendung als Quelle indiziert. Die vom Quellserver benötigten Informationen werden in den PDB-Dateien gespeichert.

Der Quellserver enthält derzeit Skripts, die mit den folgenden Quellcodeverwaltungssystemen funktionieren sollten.

-   Team Foundation Server
-   Perforce
-   Visual SourceSafe
-   CVS
-   Subversion

Sie können auch ein benutzerdefiniertes Skript erstellen, um Ihren Code für ein anderes Quellcodeverwaltungssystem zu indizieren.

In der folgenden Tabelle sind die Quellservertools aufgeführt.



| Tool        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Srcsrv.ini  | Diese Datei ist die Masterliste aller Quellcodeverwaltungsserver. Jeder Eintrag hat das folgende Format:*MYSERVER* = *serverinfo*<br/> Bei Verwendung von Perforce bestehen die Serverinformationen aus dem vollständigen Netzwerkpfad zum Server, gefolgt von einem Doppelpunkt und der verwendeten Portnummer. Beispiel:<br/> MYSERVER=machine.corp.company.com:1666<br/> Diese Datei kann auf dem Computer installiert werden, auf dem der Debugger ausgeführt wird. Wenn der Quellserver gestartet wird, werden Srcsrv.ini nach Werten gesucht. diese Werte überschreiben die in der PDB-Datei enthaltenen Informationen. Dadurch können Benutzer einen Debugger so konfigurieren, dass zur Debugzeit ein alternativer Quellcodeverwaltungsserver verwendet wird.<br/> Weitere Informationen finden Sie im Beispiel Srcsrv.ini installiert mit den Quellservertools.<br/> |
| Ssindex.cmd | Dieses Skript erstellt die Liste der Dateien, die in die Quellcodeverwaltung eingecheckt werden, zusammen mit den Versionsinformationen jeder Datei. Eine Teilmenge dieser Informationen wird in den PDB-Dateien gespeichert, die beim Erstellen der Anwendung generiert wurden. Das Skript verwendet eines der folgenden Perl-Module für die Schnittstelle zur Quellcodeverwaltung: P4.pm (Perforce) oder Vss.pm (Visual Source Tresor). Führen Sie das Skript mit dem -? aus, um weitere Informationen zu finden. oder -?? (ausführliche Hilfe)-Option, oder untersuchen Sie das Skript.<br/>                                                                                                                                                                                                                                                                                                             |
| Srctool.exe | Dieses Hilfsprogramm listet alle Dateien auf, die in einer PDB-Datei indiziert sind. Für jede Datei werden der vollständige Pfad, der Quellcodeverwaltungsserver und die Versionsnummer der Datei aufgelistet. Sie können diese Informationen verwenden, um Dateien abzurufen, ohne den Quellserver zu verwenden. Führen Sie das Hilfsprogramm mit /? aus, um weitere Informationen zu finden. (Neuen Branch erstellen und Pull Request starten).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Pdbstr.exe  | Dieses Hilfsprogramm wird von den Indizierungsskripts verwendet, um die Versionskontrollinformationen in den alternativen Datenstrom "srcsrv" der PDB-Zieldatei einzufügen. Sie kann auch einen beliebigen Stream aus einer PDB-Datei lesen. Anhand dieser Informationen können Sie überprüfen, ob die Indizierungsskripts ordnungsgemäß funktionieren. Führen Sie das Hilfsprogramm mit /? aus, um weitere Informationen zu finden. (Neuen Branch erstellen und Pull Request starten).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="retrieving-the-source-file"></a>Abrufen der Quelldatei

Die DbgHelp-API ermöglicht den Zugriff auf die Quellserverfunktionalität über die [**Funktion SymGetSourceFile.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) Um den Namen der abzurufenden Quelldatei abzurufen, rufen Sie die [**Funktion SymEnumSourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles) oder [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) auf.

## <a name="using-source-server-with-a-debugger"></a>Verwenden des Quellservers mit einem Debugger

Um den Quellserver mit WinDbg, KD, NTSD oder CDB zu verwenden, stellen Sie sicher, dass Sie eine aktuelle Version der Debugtools für Windows-Paket installiert haben (Version 6.3 oder höher). Schließen Sie dann srv \* wie folgt in den SRCPATH-Befehl ein:

**\. srcpath srv \* ;** _c: \\ mysource_

Beachten Sie, dass dieses Beispiel auch einen herkömmlichen Quellpfad enthält. Wenn der Debugger die Datei nicht vom Quellserver abrufen kann, durchsucht er den angegebenen Pfad.

Wenn eine Quelldatei vom Quellserver abgerufen wird, verbleibt sie auf ihrer Festplatte, nachdem die Debugsitzung beendet wurde. Quelldateien werden lokal im Unterverzeichnis src der Debugtools für Windows Installationsverzeichnis gespeichert.

## <a name="source-server-data-blocks"></a>Quellserver-Datenblöcke

Der Quellserver basiert auf zwei Datenblöcken innerhalb der PDB-Datei.

-   Quelldateiliste. Beim Erstellen eines Moduls wird automatisch eine Liste mit vollqualifizierten Pfaden zu den Quelldateien erstellt, die zum Erstellen des Moduls verwendet werden.
-   Datenblock. Durch das Indizieren der Quelle wie zuvor beschrieben wird der PDB-Datei ein alternativer Stream mit dem Namen "srcsrv" hinzugefügt. Das Skript, das diese Daten einfügt, ist vom spezifischen Buildprozess und quellcodeverwaltungssystem abhängig.

In Version 1 der Sprachspezifikation ist der Datenblock in drei Abschnitte unterteilt: ini, Variablen und Quelldateien. Sie weist die folgende Syntax auf.

``` syntax
SRCSRV: ini ------------------------------------------------ 
VERSION=1
VERCTRL=<source_control_str>
DATETIME=<date_time_str>
SRCSRV: variables ------------------------------------------ 
SRCSRVTRG=%sdtrg% 
SRCSRVCMD=%sdcmd% 
SRCSRVENV=var1=string1\bvar2=string2 
DEPOT=//depot 
SDCMD=sd.exe -p %fnvar%(%var2%) print -o %srcsrvtrg% -q %depot%/%var3%#%var4%
SDTRG=%targ%\%var2%\%fnbksl%(%var3%)\%var4%\%fnfile%(%var1%) 
WIN_SDKTOOLS= sserver.microsoft.com:4444 
SRCSRV: source files --------------------------------------- 
<path1>*<var2>*<var3>*<var4> 
<path2>*<var2>*<var3>*<var4> 
<path3>*<var2>*<var3>*<var4> 
<path4>*<var2>*<var3>*<var4> 
SRCSRV: end ------------------------------------------------
```

Der gesamte Text wird wörtlich interpretiert, mit Ausnahme von Text, der in Prozentzeichen (%) eingeschlossen ist. Text, der in Prozentzeichen eingeschlossen ist, wird als Variablenname behandelt, um rekursiv aufgelöst zu werden, es sei denn, es handelt sich um eine der folgenden Funktionen:

<dl> <dt>

<span id="_fnvar___"></span><span id="_FNVAR___"></span>%fnvar%()
</dt> <dd>

Der Parametertext sollte in Prozentzeichen eingeschlossen und als zu erweiternde Variable behandelt werden.

</dd> <dt>

<span id="_fnbksl___"></span><span id="_FNBKSL___"></span>%fnbksl%()
</dt> <dd>

Alle Schrägstriche (/) im Parametertext sollten durch umgekehrte Schrägstriche () ersetzt \\ werden.

</dd> <dt>

<span id="_fnfile___"></span><span id="_FNFILE___"></span>%fnfile%()
</dt> <dd>

Alle Pfadinformationen im Parametertext sollten entfernt werden, sodass nur der Dateiname übrig bleibt.

</dd> </dl>

Der Abschnitt ini enthält Variablen, die die Anforderungen beschreiben. Das Indizierungsskript kann diesem Abschnitt eine beliebige Anzahl von Variablen hinzufügen. Hier finden Sie einige Beispiele:

<dl> <dt>

<span id="VERSION"></span><span id="version"></span>Version
</dt> <dd>

Die Sprachspezifikationsversion. Diese Variable ist erforderlich.

</dd> <dt>

<span id="VERCTL"></span><span id="verctl"></span>VERCTL
</dt> <dd>

Eine Zeichenfolge, die das Quellcodeverwaltungsprodukt beschreibt. Diese Variable ist optional.

</dd> <dt>

<span id="DATETIME"></span><span id="datetime"></span>Datetime
</dt> <dd>

Eine Zeichenfolge, die das Datum und die Uhrzeit der Verarbeitung der PDB-Datei angibt. Diese Variable ist optional.

</dd> </dl>

Der Abschnitt variables enthält Variablen, die beschreiben, wie eine Datei aus der Quellcodeverwaltung extrahiert wird. Sie kann auch verwendet werden, um häufig verwendeten Text als Variablen zu definieren, um die Größe des Datenblocks zu reduzieren.

<dl> <dt>

<span id="SRCSRVTRG"></span><span id="srcsrvtrg"></span>SRCSRVTRG
</dt> <dd>

Beschreibt, wie der Zielpfad für die extrahierte Datei erstellt wird. Dies ist eine erforderliche Variable.

</dd> <dt>

<span id="SRCSRVCMD"></span><span id="srcsrvcmd"></span>SRCSRVCMD
</dt> <dd>

Beschreibt, wie der Befehl zum Extrahieren der Datei aus der Quellcodeverwaltung erstellt wird. Dies schließt den Namen der ausführbaren Datei und deren Befehlszeilenparameter ein. Dies ist eine erforderliche Variable.

</dd> <dt>

<span id="SRCSRVENV"></span><span id="srcsrvenv"></span>SRCSRVENV
</dt> <dd>

Eine Zeichenfolge, die Umgebungsvariablen auflistet, die während der Dateiextraktion erstellt werden sollen. Trennen Sie mehrere Einträge durch ein Rücktastenzeichen ( \\ b). Dies ist eine optionale Variable.

</dd> </dl>

Der Abschnitt "Quelldateien" enthält einen Eintrag für jede Quelldatei, die indiziert wurde. Der Inhalt jeder Zeile wird als Variablen mit den Namen VAR1, VAR2, VAR3 und so weiter bis VAR10 interpretiert. Die Variablen werden durch Sternchen getrennt. VAR1 muss den vollqualifizierten Pfad zur Quelldatei angeben, wie an anderer Stelle in der PDB-Datei aufgeführt. Beispielsweise die folgende Zeile:

``` syntax
c:\proj\src\file.cpp*TOOLS_PRJ*tools/mytool/src/file.cpp*3
```

wird wie folgt interpretiert:

``` syntax
VAR1=c:\proj\src\file.cpp
VAR2=TOOLS_PRJ
VAR3=tools/mytool/src/file.cpp
VAR4=3
```

In diesem Beispiel ist VAR4 eine Versionsnummer. Die meisten Quellcodeverwaltungssysteme unterstützen das Beschriften von Dateien jedoch so, dass der Quellzustand für einen bestimmten Build wiederhergestellt werden kann. Aus diesem Grund können Sie alternativ die Bezeichnung für den Build verwenden. Der Beispieldatenblock kann so geändert werden, dass er eine Variable wie die folgende enthält:

``` syntax
LABEL=BUILD47
```

Wenn das Quellcodeverwaltungssystem dann das At-Zeichen (@) verwendet, um eine Bezeichnung anzugeben, können Sie die SRCSRVCMD-Variable wie folgt ändern:

**sd.exe -p %fnvar%(%var2%) print -o %srcsrvtrg% -q %depot%/%var3%@%label%**

## <a name="how-source-server-works"></a>Funktionsweise des Quellservers

Der Quellserverclient wird in der Symsrv.dll. Der Client extrahiert Informationen nicht direkt aus der PDB-Datei. es verwendet einen Symbolhandler, z. B. den in der Dbghelp.dll. Es handelt sich im Wesentlichen um eine rekursive Variablenersetzungs-Engine, die eine Befehlszeile erstellt, mit der die richtige Quelldatei aus dem Quellcodeverwaltungssystem extrahiert werden kann. Ihr Code sollte nicht direkt Symsrv.dll aufrufen. Um die Funktionalität in Ihre Anwendung zu integrieren, verwenden Sie die [**SymGetSourceFile-Funktion.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile)

Die erste Version des Quellservers funktioniert wie folgt. Dieses Verhalten kann sich in zukünftigen Versionen ändern.

-   Der Client ruft die **SrcSrvInit-Funktion** mit dem Zielpfad auf, der als Basis für alle Quelldateiextraktionen verwendet werden soll. Dieser Pfad wird in der TARG-Variablen gespeichert.
-   Der Client extrahiert den Srcsrv-Stream aus der PDB, wenn die Modul-PDB geladen wird, und ruft die **SrcSrvLoadModule-Funktion** auf, um den Datenblock an den Quellserver zu übergeben.
-   Wenn Dbghelp eine Quelldatei abruft, ruft der Client die **Funktion SrcSrvGetFile** auf, um die Quelldateien aus der Quellcodeverwaltung abzurufen.
-   Der Quellserver durchsucht die Quelldateieinträge im Datenblock nach einem Eintrag, der der angeforderten Datei entspricht. Er füllt VAR1 in VAR *n mit* dem Inhalt des Quelldateieintrags auf. Als Nächstes wird die SRCSRVTRG-Variable mithilfe von VAR1 auf VAR *n erweitert.* Wenn sich die Datei bereits an diesem Speicherort befindet, wird der Speicherort an den Aufrufer zurückgegeben. Andernfalls wird die Variable SRCSRVCMD erweitert, um den Befehl zu erstellen, der zum Abrufen der Datei aus der Quellcodeverwaltung und zum Kopieren an den Zielspeicherort erforderlich ist. Abschließend wird dieser Befehl ausgeführt.

## <a name="creating-a-source-control-provider-module"></a>Erstellen eines Quellcodeverwaltungsanbietermoduls

Der Quellserver enthält Anbietermodule für Perforce (p4.pm) und Visual Source Tresor (vss.pm). Um Ein eigenes Anbietermodul zu erstellen, müssen Sie die folgenden Schnittstellen implementieren.

<dl> <dt>

<span id="_module__SimpleUsage__"></span><span id="_module__simpleusage__"></span><span id="_MODULE__SIMPLEUSAGE__"></span>**$module::SimpleUsage()**
</dt> <dd>

Zweck: Zeigt einfache Modulnutzungsinformationen für STDOUT an.

Parameter: keine

Rückgabewert: Keine

</dd> <dt>

<span id="_module__VerboseUsage__"></span><span id="_module__verboseusage__"></span><span id="_MODULE__VERBOSEUSAGE__"></span>**$module::VerboseUsage()**
</dt> <dd>

Zweck: Zeigt ausführliche Informationen zur Modulverwendung für STDOUT an.

Parameter: keine

Rückgabewert: Keine

</dd> <dt>

<span id="_objref____module__new__CommandArguments_"></span><span id="_objref____module__new__commandarguments_"></span><span id="_OBJREF____MODULE__NEW__COMMANDARGUMENTS_"></span>**$objref = $module::new( \@ CommandArguments)**
</dt> <dd>

Zweck: Initialisiert eine Instanz des Anbietermoduls.

Parameter: Alle @ARGV Argumente, die von SSIndex.cmd nicht als allgemeine Argumente erkannt wurden.

Rückgabewert: Ein Verweis, der in späteren Vorgängen verwendet werden kann.

</dd> <dt>

<span id="_objref-_GatherFileInformation__SourcePath___ServerHashReference_"></span><span id="_objref-_gatherfileinformation__sourcepath___serverhashreference_"></span><span id="_OBJREF-_GATHERFILEINFORMATION__SOURCEPATH___SERVERHASHREFERENCE_"></span>**$objref->GatherFileInformation($SourcePath, $ServerHashReference)**
</dt> <dd>

Zweck: Ermöglicht es dem Modul, die erforderlichen Quellindizierungsinformationen für das verzeichnis zu erfassen, das durch den $SourcePath wird. Das Modul sollte nicht davon ausgehen, dass dieser Eintrag nur einmal für jede Objektinstanz aufgerufen wird, da SSIndex.cmd ihn möglicherweise mehrmals für verschiedene Pfade aufruft.

Parameter: (1) Das lokale Verzeichnis, das die zu indizierende Quelle enthält. (2) Ein Verweis auf einen Hash, der alle Einträge aus der angegebenen Srcsrv.ini enthält.

Rückgabewert: Keine

</dd> <dt>

<span id="__VariableHashReference___FileEntry_____objref-_GetFileInfo__LocalFile_"></span><span id="__variablehashreference___fileentry_____objref-_getfileinfo__localfile_"></span><span id="__VARIABLEHASHREFERENCE___FILEENTRY_____OBJREF-_GETFILEINFO__LOCALFILE_"></span>**($VariableHashReference, $FileEntry) = $objref->GetFileInfo($LocalFile)**
</dt> <dd>

Zweck: Stellt die erforderlichen Informationen zum Extrahieren einer einzelnen, spezifischen Datei aus dem Quellcodeverwaltungssystem zur Verfügung.

Parameter: Ein vollqualifizierter Dateiname

Rückgabewert: (1) Ein Hashverweis der Variablen, die zum Interpretieren des zurückgegebenen Werts $FileEntry. SSIndex.cmd speichert diese Variablen für jede Quelldatei zwischen, die von einer einzelnen Debugdatei verwendet wird, um die Menge der in den Quellindexstream geschriebenen Informationen zu reduzieren. (2) Der Dateieintrag, der in den Quellindexstream geschrieben werden soll, damit SrcSrv.dll Datei aus der Quellcodeverwaltung extrahieren können. Das genaue Format dieser Zeile ist spezifisch für das Quellcodeverwaltungssystem.

</dd> <dt>

<span id="_TextString____objref-_LongName__"></span><span id="_textstring____objref-_longname__"></span><span id="_TEXTSTRING____OBJREF-_LONGNAME__"></span>**$TextString = $objref->LongName()**
</dt> <dd>

Zweck: Stellt eine beschreibende Zeichenfolge zum Identifizieren des Quellcodeverwaltungsanbieters für den Endbenutzer zur Verfügung.

Parameter: keine

Rückgabewert: Der beschreibende Name des Quellcodeverwaltungssystems.

</dd> <dt>

<span id="_StreamVariableLines____objref-_SourceStreamVariables__"></span><span id="_streamvariablelines____objref-_sourcestreamvariables__"></span><span id="_STREAMVARIABLELINES____OBJREF-_SOURCESTREAMVARIABLES__"></span>**@StreamVariableLines = $objref->SourceStreamVariables()**
</dt> <dd>

Zweck: Ermöglicht es dem Quellcodeverwaltungsanbieter, dem Quellstream für jede Debugdatei quellcodeverwaltungsspezifische Variablen hinzuzufügen. Die Beispielmodule verwenden diese Methode zum Schreiben der erforderlichen EXTRACT \_ CMD- und EXTRACT \_ TARGET-Variablen.

Parameter: keine

Rückgabewert: Die Liste der Einträge für die Quellstreamvariablen.

</dd> </dl>

 

 




