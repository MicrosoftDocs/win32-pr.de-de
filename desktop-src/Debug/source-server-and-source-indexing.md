---
description: Der Quell Server ermöglicht einem Client das Abrufen der exakten Version der Quelldateien, die zum Erstellen einer Anwendung verwendet wurden.
ms.assetid: c7bf51ce-7fb4-49aa-ad33-e551b2c8362b
title: Quellserver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3d8d76c70b67c176126d8e424bd5b55b616697
ms.sourcegitcommit: bfb5d94f754d017307b4cc9d914a2716701331d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355083"
---
# <a name="source-server"></a>Quellserver

Der Quell Server ermöglicht einem Client das Abrufen der exakten Version der Quelldateien, die zum Erstellen einer Anwendung verwendet wurden. Da sich der Quellcode für ein Modul Zwischenversionen und im Laufe der Jahre ändern kann, ist es wichtig, sich den Quellcode anzusehen, wie er vorhanden war, als die Version des fraglichen Moduls erstellt wurde.

Der Quell Server Ruft die entsprechenden Dateien aus der Quell Code Verwaltung ab. Um den Quell Server verwenden zu können, muss die Anwendung als Quell Indizierung verwendet werden.

## <a name="source-indexing"></a>Quell Indizierung

Das Quell Indizierungs System ist eine Sammlung von ausführbaren Dateien und Perl-Skripts. Die Perl-Skripts erfordern perl 5,6 oder höher.

Im Allgemeinen sind Binärdateien während des Buildprozesses Quell indiziert, nachdem die Anwendung erstellt wurde. Die vom Quell Server benötigten Informationen werden in den PDB-Dateien gespeichert.

Der Quell Server ist zurzeit mit Skripts ausgeliefert, die mit den folgenden Quell Code Verwaltungssystemen funktionieren.

-   Team Foundation Server
-   Perforce
-   Visual SourceSafe
-   CVS
-   Subversion

Sie können auch ein benutzerdefiniertes Skript erstellen, um den Code für ein anderes Quell Code Verwaltungssystem zu indizieren.

In der folgenden Tabelle sind die Quell Server Tools aufgeführt.



| Tool        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Srcsrv.ini  | Diese Datei ist die Masterliste aller Quell Code Verwaltungs Server. Jeder Eintrag weist das folgende Format auf:*myserver* = *Server Info*<br/> Bei der Verwendung von Perforce bestehen die Server Informationen aus dem vollständigen Netzwerkpfad zum Server, gefolgt von einem Doppelpunkt und der verwendeten Portnummer. Beispiel:<br/> MyServer = Machine. Corp. Company. com: 1666<br/> Diese Datei kann auf dem Computer installiert werden, auf dem der Debugger ausgeführt wird. Wenn der Quell Server gestartet wird, wird Srcsrv.ini nach Werten untersucht. Diese Werte überschreiben die Informationen, die in der PDB-Datei enthalten sind. Dadurch können Benutzer einen Debugger so konfigurieren, dass zur Debugzeit ein alternativer Quell Code Verwaltungs Server verwendet wird.<br/> Weitere Informationen finden Sie im Beispiel Srcsrv.ini, das mit den Quell Server Tools installiert wurde.<br/> |
| SSINDEX. cmd | Mit diesem Skript wird die Liste der in die Quell Code Verwaltung eingecheckten Dateien zusammen mit den Versionsinformationen der einzelnen Dateien erstellt. Sie speichert eine Teilmenge dieser Informationen in den PDB-Dateien, die beim Erstellen der Anwendung generiert wurden. Das Skript verwendet eines der folgenden Perl-Module, um eine Schnittstelle mit der Quell Code Verwaltung zu erstellen: P4.pm (Perforce) oder VSS.pm (Visual Source Safe). Um weitere Informationen zu erhalten, führen Sie das Skript mit dem-? aus. oder-?? (Ausführliche Hilfe) oder untersuchen Sie das Skript.<br/>                                                                                                                                                                                                                                                                                                             |
| Srctool.exe | Dieses Hilfsprogramm listet alle Dateien auf, die in einer PDB-Datei indiziert werden. Für jede Datei werden der vollständige Pfad, der Quell Code Verwaltungs Server und die Versionsnummer der Datei aufgelistet. Sie können diese Informationen verwenden, um Dateien abzurufen, ohne den Quell Server zu verwenden. Um weitere Informationen zu erhalten, führen Sie das Hilfsprogramm mit dem/? (Neuen Branch erstellen und Pull Request starten).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Pdbstr.exe  | Dieses Hilfsprogramm wird von den Indizierungs Skripts verwendet, um die Versions Kontrollinformationen in den alternativen Stream "SRCSRV" der PDB-Ziel Datei einzufügen. Außerdem kann jeder Stream aus einer PDB-Datei gelesen werden. Sie können diese Informationen verwenden, um zu überprüfen, ob die Indizierungs Skripts ordnungsgemäß funktionieren. Um weitere Informationen zu erhalten, führen Sie das Hilfsprogramm mit dem/? (Neuen Branch erstellen und Pull Request starten).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="retrieving-the-source-file"></a>Abrufen der Quelldatei

Die dbghelp-API ermöglicht den Zugriff auf die Quell Serverfunktionen über die [**symgetsourcefile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) -Funktion. Um den Namen der abzurufenden Quelldatei abzurufen, rufen Sie die [**symenum SourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles) -oder [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) -Funktion auf.

## <a name="using-source-server-with-a-debugger"></a>Verwenden des Quell Servers mit einem Debugger

Um den Quell Server mit WinDbg, KD, NZD oder cdb zu verwenden, stellen Sie sicher, dass Sie eine aktuelle Version der Debugtools für Windows-Paket (Version 6,3 oder höher) installiert haben. Fügen Sie dann SRV \* wie folgt in den SRCPATH-Befehl ein:

**\. SRCPATH SRV \* ;** _c: \\ meinquelle_

Beachten Sie, dass dieses Beispiel auch einen herkömmlichen Quellpfad enthält. Wenn der Debugger die Datei nicht vom Quell Server abrufen kann, wird der angegebene Pfad durchsucht.

Wenn eine Quelldatei vom Quell Server abgerufen wird, bleibt Sie nach der Debugsitzung auf der Festplatte. Quelldateien werden lokal im Unterverzeichnis src des Installationsverzeichnisses Debugtools für Windows gespeichert.

## <a name="source-server-data-blocks"></a>Quell Server-Datenblöcke

Der Quell Server basiert auf zwei Datenblöcken in der PDB-Datei.

-   Liste der Quelldateien. Beim Erstellen eines Moduls wird automatisch eine Liste der voll qualifizierten Pfade zu den Quelldateien erstellt, die zum Erstellen des Moduls verwendet werden.
-   Datenblock. Wenn Sie die Quelle wie zuvor beschrieben indizieren, wird der PDB-Datei mit dem Namen "SRCSRV" ein alternativer Datenstrom hinzugefügt. Das Skript, das diese Daten einfügt, hängt vom jeweiligen Buildprozess und dem verwendeten Quell Code Verwaltungssystem ab.

In der Sprachspezifikation Version 1 ist der Datenblock in drei Abschnitte unterteilt: ini, Variablen und Quelldateien. Sie weist die folgende Syntax auf.

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

Der gesamte Text wird buchstäblich interpretiert, mit Ausnahme von Text, der in Prozentzeichen (%) eingeschlossen ist. Text, der in Prozentzeichen eingeschlossen ist, wird als Variablenname behandelt, der rekursiv aufgelöst werden soll, es sei denn, er ist eine der folgenden Funktionen:

<dl> <dt>

<span id="_fnvar___"></span><span id="_FNVAR___"></span>% fnvar%()
</dt> <dd>

Der Parameter Text muss in Prozentzeichen eingeschlossen und als zu erweiternde Variable behandelt werden.

</dd> <dt>

<span id="_fnbksl___"></span><span id="_FNBKSL___"></span>%%() KSL
</dt> <dd>

Alle Schrägstriche (/) im Parameter Text sollten durch rückwärts Schrägstriche () ersetzt werden \\ .

</dd> <dt>

<span id="_fnfile___"></span><span id="_FNFILE___"></span>% fnfile%()
</dt> <dd>

Alle Pfadinformationen im Parameter Text sollten entfernt werden, sodass nur der Dateiname erhalten bleibt.

</dd> </dl>

Der ini-Abschnitt enthält Variablen, die die Anforderungen beschreiben. Das Indizierungs Skript kann diesem Abschnitt beliebig viele Variablen hinzufügen. Hier finden Sie einige Beispiele:

<dl> <dt>

<span id="VERSION"></span><span id="version"></span>Version
</dt> <dd>

Die Version der Sprachspezifikation. Diese Variable ist erforderlich.

</dd> <dt>

<span id="VERCTL"></span><span id="verctl"></span>Verctl
</dt> <dd>

Eine Zeichenfolge, die das Produkt der Quell Code Verwaltung beschreibt. Diese Variable ist optional.

</dd> <dt>

<span id="DATETIME"></span><span id="datetime"></span>DateTime
</dt> <dd>

Eine Zeichenfolge, die das Datum und die Uhrzeit der Verarbeitung der PDB-Datei angibt. Diese Variable ist optional.

</dd> </dl>

Der Abschnitt Variablen enthält Variablen, die beschreiben, wie eine Datei aus der Quell Code Verwaltung extrahiert werden soll. Sie kann auch verwendet werden, um häufig verwendeten Text als Variablen zu definieren, um die Größe des Datenblocks zu reduzieren.

<dl> <dt>

<span id="SRCSRVTRG"></span><span id="srcsrvtrg"></span>Srcsrvtrg
</dt> <dd>

Beschreibt, wie der Zielpfad für die extrahierte Datei erstellt wird. Dies ist eine erforderliche Variable.

</dd> <dt>

<span id="SRCSRVCMD"></span><span id="srcsrvcmd"></span>Srcsrvcmd
</dt> <dd>

Beschreibt, wie der Befehl zum Extrahieren der Datei aus der Quell Code Verwaltung erstellt wird. Dies schließt den Namen der ausführbaren Datei und der Befehlszeilenparameter ein. Dies ist eine erforderliche Variable.

</dd> <dt>

<span id="SRCSRVENV"></span><span id="srcsrvenv"></span>Srcsrvenv
</dt> <dd>

Eine Zeichenfolge, die Umgebungsvariablen auflistet, die während der Dateiextraktion erstellt werden sollen. Trennen Sie mehrere Einträge durch ein Rückraum Zeichen ( \\ b). Dies ist eine optionale Variable.

</dd> </dl>

Der Abschnitt Quelldateien enthält einen Eintrag für jede Quelldatei, die indiziert wurde. Die Inhalte der einzelnen Zeilen werden als Variablen mit den Namen var1, var2, var3 usw. bis VAR10 interpretiert. Die Variablen werden durch Sternchen getrennt. Var1 muss den voll qualifizierten Pfad zur Quelldatei angeben, der an anderer Stelle in der PDB-Datei aufgelistet ist. Beispielsweise die folgende Zeile:

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

In diesem Beispiel ist VAR4 eine Versionsnummer. Die meisten Quell Code Verwaltungssysteme unterstützen jedoch das bezeichnen von Dateien so, dass der Quell Zustand für einen bestimmten Build wieder hergestellt werden kann. Daher können Sie alternativ die Bezeichnung für den Build verwenden. Der Beispiel Datenblock kann so geändert werden, dass er eine Variable wie die folgende enthält:

``` syntax
LABEL=BUILD47
```

Wenn Sie dann das Quell Code Verwaltungssystem verwenden, um eine Bezeichnung anzugeben, können Sie die srcsrvcmd-Variable wie folgt ändern:

**sd.exe-p% fnvar%(% var2%) Print-o% srcsrvtrg%-q% Depot%/%var3% @% Bezeichnung%**

## <a name="how-source-server-works"></a>Funktionsweise des Quell Servers

Der Quell Server Client wird in Symsrv.dll implementiert. Der Client extrahiert keine Informationen direkt aus der PDB-Datei. Er verwendet einen Symbol Handler, z. b. den, der in Dbghelp.dll implementiert ist. Es handelt sich im Wesentlichen um eine rekursive Variablen Ersetzungs-Engine, die eine Befehlszeile erstellt, mit der die richtige Quelldatei aus dem Quell Code Verwaltungssystem extrahiert werden kann. Der Code sollte Symsrv.dll nicht direkt aufzurufen. Verwenden Sie die [**symgetsourcefile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) -Funktion, um ihre Funktionalität in Ihre Anwendung zu integrieren.

Die erste Version des Quell Servers funktioniert wie folgt. Dieses Verhalten kann sich in zukünftigen Versionen ändern.

-   Der Client ruft die **srcsrvinit** -Funktion mit dem Zielpfad auf, der als Basis für alle Quelldatei Extraktionen verwendet werden soll. Dieser Pfad wird in der Targ-Variablen gespeichert.
-   Der Client extrahiert den SRCSRV-Datenstrom aus der PDB-Datei, wenn das PDB-Modul geladen wird, und ruft die **srcsrvloadmodule** -Funktion auf, um den Datenblock an den Quell Server zu übergeben.
-   Wenn dbghelp eine Quelldatei abruft, ruft der Client die **srcsrvgetfile** -Funktion auf, um die Quelldateien aus der Quell Code Verwaltung abzurufen.
-   Der Quell Server durchsucht die Quelldatei Einträge im Datenblock nach einem Eintrag, der mit der angeforderten Datei übereinstimmt. Es füllt var1 mit dem Inhalt des Quelldatei Eintrags in var *n* auf. Anschließend wird die srcsrvtrg-Variable mithilfe von var1 auf var *n* erweitert. Wenn sich die Datei bereits an diesem Speicherort befindet, wird der Speicherort an den Aufrufer zurückgegeben. Andernfalls wird die srcsrvcmd-Variable erweitert, um den Befehl zu erstellen, der erforderlich ist, um die Datei aus der Quell Code Verwaltung abzurufen und an den Ziel Speicherort zu kopieren. Schließlich führt Sie diesen Befehl aus.

## <a name="creating-a-source-control-provider-module"></a>Erstellen eines Quellcodeverwaltungs-Anbieter Moduls

Der Quell Server umfasst Anbieter Module für Perforce (P4.pm) und Visual Source Safe (VSS.pm). Um ein eigenes Anbieter Modul zu erstellen, müssen Sie die folgenden Schnittstellen implementieren.

<dl> <dt>

<span id="_module__SimpleUsage__"></span><span id="_module__simpleusage__"></span><span id="_MODULE__SIMPLEUSAGE__"></span>**$Module:: simpleusage ()**
</dt> <dd>

Zweck: zeigt die Informationen zu einfachen Modul Verwendungs Informationen für "stdout" an.

Parameter: keine

Rückgabewert: None

</dd> <dt>

<span id="_module__VerboseUsage__"></span><span id="_module__verboseusage__"></span><span id="_MODULE__VERBOSEUSAGE__"></span>**$Module:: verbosusage ()**
</dt> <dd>

Zweck: zeigt ausführliche Informationen zur Modul Verwendung an stdout an.

Parameter: keine

Rückgabewert: None

</dd> <dt>

<span id="_objref____module__new__CommandArguments_"></span><span id="_objref____module__new__commandarguments_"></span><span id="_OBJREF____MODULE__NEW__COMMANDARGUMENTS_"></span>**$ObjRef = $Module:: New ( \@ commandarguments)**
</dt> <dd>

Zweck: Initialisiert eine Instanz des Anbieter Moduls.

Parameter: alle @ARGV Argumente, die von "SSINDEX. cmd" nicht als allgemeine Argumente erkannt wurden.

Rückgabewert: ein Verweis, der in späteren Vorgängen verwendet werden kann.

</dd> <dt>

<span id="_objref-_GatherFileInformation__SourcePath___ServerHashReference_"></span><span id="_objref-_gatherfileinformation__sourcepath___serverhashreference_"></span><span id="_OBJREF-_GATHERFILEINFORMATION__SOURCEPATH___SERVERHASHREFERENCE_"></span>**$ObjRef->gatherfileinformation ($SourcePath, $ServerHashReference)**
</dt> <dd>

Zweck: ermöglicht dem Modul, die erforderlichen Quell Indizierungs Informationen für das vom $SourcePath-Parameter angegebene Verzeichnis zu erfassen. Das Modul sollte nicht davon ausgehen, dass dieser Eintrag für jede Objektinstanz nur einmal aufgerufen wird, da SSINDEX. cmd ihn möglicherweise mehrmals für verschiedene Pfade aufruft.

Parameter: (1) das lokale Verzeichnis, das die zu indizierende Quelle enthält. (2) ein Verweis auf einen Hash, der alle Einträge aus der angegebenen Srcsrv.ini Datei enthält.

Rückgabewert: None

</dd> <dt>

<span id="__VariableHashReference___FileEntry_____objref-_GetFileInfo__LocalFile_"></span><span id="__variablehashreference___fileentry_____objref-_getfileinfo__localfile_"></span><span id="__VARIABLEHASHREFERENCE___FILEENTRY_____OBJREF-_GETFILEINFO__LOCALFILE_"></span>**($VariableHashReference, $FileEntry) = $ObjRef->GetFileInfo ($LocalFile)**
</dt> <dd>

Zweck: stellt die erforderlichen Informationen bereit, um eine einzelne, bestimmte Datei aus dem Quell Code Verwaltungssystem zu extrahieren.

Parameter: ein voll qualifizierter Dateiname

Rückgabewert: (1) ein Hash Verweis auf die Variablen, die zum Interpretieren der zurückgegebenen $FileEntry erforderlich sind. SSINDEX. cmd speichert diese Variablen für jede Quelldatei, die von einer einzelnen Debugdatei verwendet wird, um die Menge der Informationen zu reduzieren, die in den quellindexstream geschrieben werden. (2) der Datei Eintrag, der in den quellindexstream geschrieben werden soll, damit SrcSrv.dll diese Datei aus der Quell Code Verwaltung extrahieren kann. Das genaue Format dieser Zeile ist spezifisch für das Quell Code Verwaltungssystem.

</dd> <dt>

<span id="_TextString____objref-_LongName__"></span><span id="_textstring____objref-_longname__"></span><span id="_TEXTSTRING____OBJREF-_LONGNAME__"></span>**$TextString = $ObjRef->longname ()**
</dt> <dd>

Zweck: stellt eine beschreibende Zeichenfolge bereit, um den Quell Code Verwaltungs Anbieter für den Endbenutzer zu identifizieren.

Parameter: keine

Rückgabewert: der beschreibende Name des Quell Code Verwaltungssystems.

</dd> <dt>

<span id="_StreamVariableLines____objref-_SourceStreamVariables__"></span><span id="_streamvariablelines____objref-_sourcestreamvariables__"></span><span id="_STREAMVARIABLELINES____OBJREF-_SOURCESTREAMVARIABLES__"></span>**@StreamVariableLines = $ObjRef->sourcestreamvariables ()**
</dt> <dd>

Zweck: ermöglicht dem Quell Code Verwaltungs Anbieter, dem Quellstream für jede Debugdatei Quell Code Verwaltungs spezifische Variablen hinzuzufügen. Die Beispiel Module verwenden diese Methode zum Schreiben der erforderlichen Extract \_ cmd-und Extract \_ target-Variablen.

Parameter: keine

Rückgabewert: die Liste der Einträge für die Quelldaten Strom Variablen.

</dd> </dl>

 

 




