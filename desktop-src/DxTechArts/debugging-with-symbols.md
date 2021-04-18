---
title: Debuggen mit Symbolen
description: Dieser Artikel bietet einen Überblick über die beste Verwendung von Symbolen im Debugprozess.
ms.assetid: 7ce0c9c7-485c-8d72-0353-27fd2e369a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff63e2404a07a2f0ab5adcb156d83dc989b42fd4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516940"
---
# <a name="debugging-with-symbols"></a>Debuggen mit Symbolen

Dieser Artikel bietet einen Überblick über die beste Verwendung von Symbolen im Debugprozess. Es wird erläutert, wie Sie den Microsoft-Symbol Server verwenden und wie Sie Ihren eigenen privaten Symbol Server einrichten und verwenden. Mit diesen bewährten Methoden können Sie die Effektivität und die Fähigkeit zum Debuggen von Problemen steigern, auch wenn sich alle Symbole und ausführbaren Dateien, die mit einem Problem zusammenhängen, nicht auf dem Computer befinden.

-   [Symbols](#debugging-with-symbols)
-   [Verwenden von Symbolen zum Debuggen](#using-symbols-for-debugging)
-   [Erhalten der benötigten Symbole](#getting-the-symbols-you-need)
    -   [Überprüfen Sie, ob eine bestimmte dll-Datei oder exe-Datei und PDB im gleichen Ordner übereinstimmen.](#check-if-a-given-dll-or-exe-file-and-pdb-in-the-same-folder-match)
    -   [Überprüfen Sie, ob alle DLLs und ausführbaren Dateien in einem Ordner Satz übereinstimmende pdsb aufweisen.](#check-if-all-the-dlls-and-executable-files-in-a-set-of-folders-have-matching-pdbs)
    -   [Funktionsweise von Symchk](#how-symchk-works)
-   [Symbol Server](#symbol-servers)
-   [Verwenden des Microsoft-Symbol Servers](#using-the-microsoft-symbol-server)
-   [Manuelles erhalten von Symbolen](#getting-symbols-manually)
-   [Einrichten eines Symbol Servers](#setting-up-a-symbol-server)
-   [Hinzufügen von Symbolen zu einem Symbol Server](#adding-symbols-to-a-symbol-server)
-   [Bewährte Methoden](#best-practices)

## <a name="symbols"></a>Symbole

Eine Reihe verschiedener Typen von Symbolen sind zum Debuggen verfügbar. Dazu zählen CodeView-Symbole, COFF, dbg, SYM, PDB und sogar Export Symbole, die aus einer Export Tabelle für binäre Dateien generiert werden. In diesem Whitepaper werden nur die Symbole vs.net und PDB-Format erläutert, da Sie das aktuellste bevorzugte Format aufweisen. Sie werden standardmäßig für Projekte generiert, die mithilfe von Visual Studio kompiliert werden.

Das Generieren von PDB-Dateien für releaseexecutables wirkt sich nicht auf Optimierungen aus oder ändert die Größe der generierten Dateien erheblich. In der Regel ist der Pfad der einzige Unterschied, und der Dateiname der PDB-Datei wird in die ausführbare Datei eingebettet. Aus diesem Grund sollten Sie immer PDB-Dateien entwickeln, auch wenn Sie Sie nicht mit der ausführbaren Datei versenden möchten.

PDB-Dateien werden generiert, wenn ein Projekt erstellt wird, indem der **/Zi** -oder **/Zi** -Compilerschalter (erzeugt PDB-Informationen) sowie der Linkerschalter **/Debug** (Debuginfo generieren) verwendet wird. Die vom Compiler generierten PDB-Dateien werden kombiniert und in eine einzelne PDB-Datei geschrieben, die sich im selben Verzeichnis wie die ausführbare Datei befindet.

Standardmäßig enthalten PDB-Dateien die folgenden Informationen:

-   Öffentliche Symbole (in der Regel alle Funktionen, statische und globale Variablen)
-   Eine Liste von Objektdateien, die für Code Abschnitte in der ausführbaren Datei verantwortlich sind.
-   Informationen zur Frame Zeiger Optimierung (FPO)
-   Name und Typinformationen für lokale Variablen und Datenstrukturen
-   Informationen zur Quelldatei und Zeilennummer

Wenn Sie sich Gedanken darüber machen, welche Personen die PDB-Dateiinformationen verwenden, um Sie bei der Umkehrung der ausführbaren Datei zu unterstützen, können Sie auch gestreifte PDB-Dateien mithilfe der Linkeroption **/PDBSTRIPPED: filename** generieren. Wenn Sie über vorhandene PDB-Dateien verfügen, von denen Sie private Informationen entfernen möchten, können Sie ein Tool namens pdbcopy verwenden, das Teil der Debugtools für Windows ist.

Standardmäßig enthalten die abgestürzten PDB-Dateien die folgenden Informationen:

-   Öffentliche Symbole (in der Regel nur nicht statische Funktionen und globale Variablen)
-   Eine Liste von Objektdateien, die für Code Abschnitte in der ausführbaren Datei verantwortlich sind.
-   Informationen zur Frame Zeiger Optimierung (FPO)

Dies sind die minimalen Informationen, die erforderlich sind, um zuverlässiges Debuggen zu ermöglichen. Die minimalen Informationen erschweren außerdem das Abrufen zusätzlicher Informationen über den ursprünglichen Quellcode. Da sowohl eine abgestreifte PDB-Datei als auch eine reguläre PDB-Datei generiert werden, können Sie Benutzern, die möglicherweise eingeschränkte Debuggingfähigkeiten benötigen, eine nicht benötigte Version bereitstellen, aber die vollständigen pdsb vertraulich aufbewahren. Beachten Sie, dass **/PDBSTRIPPED** eine zweite, kleinere PDB-Datei generiert. Stellen Sie daher sicher, dass Sie die richtige PDB-Datei verwenden, wenn Sie Builds zur allgemeinen Verteilung generieren. Bei einem typischen Projekt kann eine reguläre PDB-Datei eine Größe von wenigen Megabyte aufweisen, aber eine gestreifte Version der PDB-Datei kann nur ein paar hundert Kilobyte betragen.

## <a name="using-symbols-for-debugging"></a>Verwenden von Symbolen zum Debuggen

Wenn Sie eine Anwendung debuggen, die abgestürzt ist, versucht der Debugger, die Funktionen auf dem Stapel anzuzeigen, der zum Absturz geführt hat. Ohne eine PDB-Datei kann der Debugger die Funktionsnamen, die zugehörigen Parameter oder lokale Variablen, die auf dem Stapel gespeichert sind, nicht auflösen. Wenn Sie ausführbare 32-Bit-Dateien Debuggen, gibt es Situationen, in denen Sie nicht sogar zuverlässige Stapel Überwachungen ohne Symbole erhalten können. Manchmal ist es möglich, die Rohwerte im Stapel zu betrachten und herauszufinden, welche Werte Rückgabe Adressen sein können. Diese können jedoch problemlos mit Funktions verweisen oder Daten verwechselt werden.

Wenn Funktionen auf dem aktuellen Stapel mithilfe der **/Oy**-Optimierung (unterdrücken von Frame Zeigern) kompiliert wurden und keine Symbole vorhanden sind, kann der Debugger nicht zuverlässig bestimmen, welche Funktion die aktuelle Funktion aufgerufen hat. Dies liegt daran, dass der Debugger ohne die Informationen der Frame Zeiger Optimierung (FPO), die PDBs enthalten, nicht darauf verlassen kann, dass das Frame Zeiger Register (EBP) auf den gespeicherten vorherigen Frame Zeiger und an der Rückgabeadresse der übergeordneten Funktion verweist. Stattdessen wird es angezeigt. Manchmal wird Sie richtig angezeigt. Es ist jedoch häufig falsch, was irreführend sein kann. Wenn eine Warnung zu fehlenden Symbolen angezeigt wird oder keine Symbole geladen wurden, wie im folgenden Beispiel gezeigt, sollten Sie den Stapel von diesem Punkt nicht als vertrauenswürdig einstufen.

``` syntax
SWPerfTest.exe!TextFunction(... ...)    Line 59    C++
d3dx9d.dll!008829b5()
[Frames below may be incorrect and/or missing, no symbols loaded for d3dx9d.dll]
SWPerfTest.exe!main(int argc=, const char * * argv=)  Line 328 + 0x12 bytes     C++
SWPerfTest.exe!__mainCRTStartup() Line 716 + 0x17 bytes    C
kernel32.dll!@BaseThreadInitThunk@12() + 0x12 bytes
ntdll.dll!__RtlUserThreadStart@8() + 0x27 bytes
```

In vielen Fällen ist es möglich, das Debuggen ohne Symbole fortzusetzen, da sich das Problem an einem Speicherort mit exakten Symbolen befindet und Sie die Funktionen nicht weiter unten in der aufrufsstapel ansehen müssen. Auch wenn für eine Bibliothek, die sich in der Aufruf Stapel befindet, keine PDB-Funktionen verfügbar sind, sollte der Debugger bei der Kompilierung mit Frame Zeigern in der Lage sein, in den übergeordneten Funktionen ordnungsgemäß zu erraten. Ab Windows XP Service Pack 2 werden alle Windows-DLL-Dateien und ausführbaren Dateien mit deaktiviertem voll qualifizierte Datenschutz kompiliert, da das Debugging genauer ist. Durch die Deaktivierung der FPO können auch Samplings von Profiler während der Laufzeit den Stapel durchlaufen, mit minimalen Auswirkungen auf die Leistung. Unter Windows-Versionen vor Windows XP SP2 erfordern alle Binärdateien des Betriebssystems übereinstimmende Symbol Dateien, die FPO-Informationen enthalten, um das exakte Debuggen und die Profilerstellung zu ermöglichen.

Wenn Sie systemeigene 64-Bit-Dateien Debuggen, benötigen Sie keine Symbol Dateien, um gültige Stapel Überwachungen zu erhalten, da x64-Betriebssysteme und Compiler diese nicht benötigen. Sie benötigen jedoch weiterhin Symbol Dateien, um die Funktionsnamen, die aufrufsparameter und die lokalen Variablen abzurufen.

In einigen Fällen ist es jedoch besonders schwierig, ohne Symbole zu debuggen. Wenn Sie z. b. ein Programm debuggen, für das Sie eine PDB-Datei erstellt haben, und wenn Sie in einem Rückruf von einer Funktion in einer DLL abstürzen, für die Sie keine Symbole haben, können Sie nicht sehen, welche Funktion den Rückruf verursacht hat, da Sie den Stapel nicht decodieren können. Dies geschieht häufig in Bibliotheken von Drittanbietern, wenn keine pdsb bereitgestellt werden, oder bei alten Betriebssystemkomponenten, wenn pdsb nicht verfügbar sind. Rückrufe erfolgen häufig während der Nachrichten Übergabe, der Enumeration, der Speicher Belegung oder der Ausnahmebehandlung. Das Debuggen dieser Funktionen ohne einen exakten Stapel kann frustrierend sein.

Es ist wichtig, auf alle Symbole und Binärdateien für die ausführbaren Dateien zuzugreifen, auf die im Minidump verwiesen wird, um Mini Abbilder zuverlässig zu debuggen, die auf einem anderen Computer generiert werden oder in nicht eigenen Code abstürzen. Wenn die Symbole und Binärdateien von einem Symbol Server verfügbar sind, werden Sie automatisch vom Debugger abgerufen. Weitere Informationen zu Minidumps finden Sie im Whitepaper zur Absturz Abbild [Analyse](/windows/desktop/DxTechArts/crash-dump-analysis) .

## <a name="getting-the-symbols-you-need"></a>Erhalten der benötigten Symbole

Visual Studio und andere Microsoft-Debugger (z. b. WinDbg) werden in der Regel so eingerichtet, dass Sie funktionieren, wenn Sie eine Anwendung entwickeln und auf Ihrem eigenen Computer Debuggen. Wenn Sie die ausführbare Datei an eine andere Person übergeben müssen, wenn Sie mehrere Versionen einer DLL-oder exe-Datei auf Ihrem Computer haben oder wenn Sie eine Anwendung, die Windows oder andere Bibliotheken verwendet (z. b. DirectX), genau debuggen möchten, müssen Sie verstehen, wie Debugger Symbole suchen und laden. Der Debugger verwendet entweder den Symbol Suchpfad, der vom Benutzer angegeben wird – in Optionen zum \\ Debuggen von \\ Symbolen in Visual Studio – oder die \_ NT- \_ Symbol Pfad- \_ Umgebungsvariable. In der Regel sucht der Debugger an den folgenden Speicherorten nach passenden pdsb:

-   Der Speicherort, der in der DLL-Datei oder der ausführbaren Datei angegeben ist.

    Wenn Sie eine DLL-Datei oder eine ausführbare Datei auf dem Computer erstellt haben, platziert der Linker standardmäßig den vollständigen Pfad und den Dateinamen der zugehörigen PDB-Datei in der DLL-Datei oder der ausführbaren Datei. Beim Debuggen prüft der Debugger zunächst, ob die Symbol Datei an dem Speicherort vorhanden ist, der in der DLL-Datei oder der ausführbaren Datei angegeben ist. Dies ist hilfreich, da Sie immer über Symbole für den Code verfügen, den Sie auf dem Computer kompiliert haben.

-   Pdsb, die möglicherweise im gleichen Ordner wie die DLL-Datei oder die ausführbare Datei vorhanden sind.
-   Alle lokalen Symbolcache-Ordner.
-   Beliebige lokale Netzwerkdatei Freigabe-Symbol Server.
-   Alle Internet Symbol Server, wie z. b. der Microsoft-Symbol Server.

Installieren Sie die Debugtools für Windows, um sicherzustellen, dass Sie über alle pdsb verfügen, die Sie für das exakte Debuggen benötigen. Die Bit-Versionen 32 und 64 finden Sie unter [Debugtools für Windows](/windows-hardware/drivers/debugger/).

Ein nützliches Tool, das mit diesem Paket installiert wird, ist symchk.exe. Dadurch können fehlende oder falsche Symbole identifiziert werden. Dieses Tool verfügt über eine große Anzahl potenzieller Befehlszeilenoptionen. Hier sind zwei der nützlicheren und häufig verwendeten.

### <a name="check-if-a-given-dll-or-exe-file-and-pdb-in-the-same-folder-match"></a>Überprüfen Sie, ob eine bestimmte dll-Datei oder exe-Datei und PDB im gleichen Ordner übereinstimmen.

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" testing.dll /s

SYMCHK: FAILED files = 0
SYMCHK: PASSED + IGNORED files = 1
```

Die **/s** -Option weist **Symchk** an, nur im aktuellen Ordner nach Symbolen zu suchen und nicht in Symbol Servern zu suchen.

### <a name="check-if-all-the-dlls-and-executable-files-in-a-set-of-folders-have-matching-pdbs"></a>Überprüfen Sie, ob alle DLLs und ausführbaren Dateien in einem Ordner Satz übereinstimmende pdsb aufweisen.

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" *.* /r
```

Mit der **/r** -Option wird **Symchk** so festgelegt, dass Ordner rekursiv durchlaufen werden, um zu überprüfen, ob alle ausführbaren Dateien übereinstimmende Ohne die **/s** -Option verwendet **Symchk** den aktuellen \_ NT- \_ Symbol Pfad, \_ um auf einem beliebigen privaten oder lokalen Server oder auf den Microsoft-Symbol Servern nach Symbolen zu suchen. Das **Symchk** -Tool sucht nur nach Symbolen für ausführbare Dateien (. exe,. dll und ähnlich). Es ist nicht möglich, die Platzhalter Suche nach Symbolen für nicht ausführbare Dateien zu verwenden.

### <a name="how-symchk-works"></a>Funktionsweise von Symchk

Wenn der Linker dll-, ausführbare und PDB-Dateien generiert, speichert er identische GUIDs in jeder Datei. Der GUID wird von den-Tools verwendet, um zu bestimmen, ob eine bestimmte PDB-Datei mit einer DLL oder einer ausführbaren Datei übereinstimmt. Wenn Sie eine DLL oder eine ausführbare Datei ändern – indem Sie einen Ressourcen-Editor oder eine Codierung zum Kopieren von Schutz oder die Versionsinformationen ändern – wird die GUID aktualisiert, und der Debugger kann die PDB-Datei nicht laden. Aus diesem Grund ist es sehr wichtig, die DLL-Datei oder die ausführbare Datei zu manipulieren, nachdem Sie vom Linker erstellt wurde.

Sie können auch das Dienstprogramm DUMPBIN, das in vs.NET enthalten ist, verwenden, um die zu durchsuchenden Symbol Pfade anzuzeigen und zu überprüfen, ob Symbol Dateien gefunden werden, die einer bestimmten dll oder ausführbaren Datei entsprechen. Beispiel:

``` syntax
DUMPBIN /PDBPATH:VERBOSE filename.exe
```

## <a name="symbol-servers"></a>Symbol Server

Ein Symbol Server ist ein Repository für mehrere Versionen von ausführbaren Dateien und Symbol Dateien. Sie enthält entweder die Symbol Dateien selbst oder Zeiger auf die zugeordneten Symbol Dateien. Debugger verstehen, wie Symbol Server verwendet werden, und können Sie verwenden, um nach fehlenden oder unbekannten Symbolen zu suchen.

DLL-Dateien und ausführbare Dateien sind auch auf dem Microsoft-Symbol Server verfügbar. Dies ermöglicht das Debuggen von Abstürzen und das Untersuchen von Code für Betriebssystemdateien, die möglicherweise nicht auf Ihrem Computer vorhanden sind. Wenn ein Debugger auf eine ausführbare Datei oder eine DLL trifft, die nicht auf dem System vorhanden ist, das Sie für das Debuggen verwenden, fordert es automatisch sowohl die Symbole als auch eine Kopie der Binärdatei von den Microsoft-Symbol Servern an. Dies ist hilfreich, wenn Sie eine Komponente Debuggen, die über viele Versionen verfügt – z. b. msvcrt.dll –. Sie müssen den Code für eine Version untersuchen, die auf dem Computer nicht vorhanden ist. Dies hilft auch beim Debuggen von Mini Abbildern, die auf einem Betriebssystem generiert werden, das sich von dem System unterscheidet, das Sie für das Debuggen verwenden.

Microsoft veröffentlicht alle PDB-Dateien für alle Betriebssysteme und anderen verteilbaren Komponenten, z. b. das DirectX SDK, auf dem extern zugänglichen Symbol Server. Dies erleichtert das Debuggen einer Anwendung, die diese DLL-Dateien oder ausführbaren Dateien verwendet. Sie können den Microsoft-Symbol Server verwenden, um Symbole sowie alle lokalen Symbole für Komponenten aufzulösen, die auf Ihrem Computer erstellt wurden.

Sie können den Computer so einrichten, dass er den Microsoft-Symbol Server verwendet, der Ihnen den Zugriff auf alle Microsoft-Symbol Dateien ermöglicht. Sie können auch einen privaten Symbol Server für das Unternehmen, das Team oder das Netzwerk einrichten, der zum Speichern mehrerer älterer Versionen eines Projekts verwendet werden kann, an dem Sie arbeiten, oder um einen lokalen Cache für die Symbole bereitzustellen, die Sie auf dem Microsoft-Symbol Server verwenden.

Wenn Sie einen Symbol Server verwenden möchten, geben Sie den Suchpfad in einer Umgebungsvariablen an, die als \_ NT- \_ Symbol Pfad bezeichnet wird \_ . Zu Debuggern und modernen Tools, wie WinDBG, NTD oder Visual Studio, wird dieser Pfad automatisch verwendet, um nach Symbolen zu suchen.

Wenn ein Debugger nach Symbolen sucht, wird er zuerst lokal durchsucht. Anschließend werden Symbol Server angezeigt. Wenn ein übereinstimmendes Symbol gefunden wird, wird die Symbol Datei in Ihren lokalen Cache übertragen. Die Symbole für eine typische dll oder eine ausführbare Datei reichen von 1 bis 100 MB. Wenn Sie also einen Prozess Debuggen, der viele DLLs enthält, kann es einige Zeit dauern, bis alle Symbole aufgelöst und in einen lokalen Cache übertragen wurden.

## <a name="using-the-microsoft-symbol-server"></a>Verwenden des Microsoft-Symbol Servers

Mit dem Microsoft-Symbol Server können Sie alle aktuellen Symbole abrufen, einschließlich Symbolen für gepatchte oder aktualisierte Dateien. Den Microsoft-Symbol Server finden Sie unter <https://msdl.microsoft.com/download/symbols> .

Sie können auf den Symbol Server auf eine der folgenden Arten zugreifen:

-   Geben Sie die Server Adresse direkt ein. Wählen Sie in Visual Studio im **Menü Extras** die **Option Optionen** aus, und wählen Sie dann **Debuggen** und dann **Symbole** aus.
-   Verwenden Sie die Umgebungsvariable \_ NT- \_ Symbol \_ Pfad. Diese Methode wird empfohlen.

    Diese wird von allen Debuggingtools verwendet. Sie wird auch von Visual Studio verwendet und wird beim Öffnen von Visual Studio gelesen und decodiert. Daher müssen Sie Visual Studio neu starten, wenn Sie Sie ändern.

    Mit dieser Umgebungsvariablen können Sie mehrere Symbol Server angeben, z. –. einen internen privaten Symbol Server. Außerdem können Sie ein lokales Cache Verzeichnis angeben, in dem Sie pdsb für alle Symbole speichern können, die Sie von Symbol Servern sowohl intern als auch über das Internet suchen.

Die Syntax für die \_ NT- \_ Symbol \_ Pfad Variable lautet wie folgt:

``` syntax
srv*[local cache]*[private symbol server]*https://msdl.microsoft.com/download/symbols
```

Ersetzen \[ Sie local Cache \] durch den Namen eines Verzeichnisses auf dem Computer, in dem Sie einen Cache aller verwendeten Symbole speichern möchten, z. – .% systemroot% \\ Symbols oder c: \\ Symbols.

Der \[ private Symbol Server \] ist optional. Sie kann auf einen Symbol Server verweisen, der sich im Netzwerk befindet, oder auf einen Symbol Server, der von Ihrem Team, ihrer Produktgruppe oder Ihrem Unternehmen gemeinsam genutzt wird.

Wenn Sie nur den Microsoft-Symbol Server in Verbindung mit einem lokalen Cache von Symbolen verwenden möchten, um den Zugriff über das Internet zu beschleunigen, verwenden Sie die folgende Einstellung für den \_ NT- \_ Symbol \_ Pfad:

``` syntax
srv*c:\symbols*https://msdl.microsoft.com/download/symbols
```

Weitere Optionen für den \_ NT- \_ Symbol Pfad finden Sie \_ in der Hilfedatei, die mit dem Paket Microsoft Debugtools für Windows installiert wird.

Ausführbare Dateien ohne Symbole können den Zeitbedarf für das Starten eines Debuggers erhöhen, wenn Sie einen Symbol Server verwenden. Dies liegt daran, dass der Debugger den Symbol Server jedes Mal abfragt, wenn er versucht, die ausführbare Datei zu laden. Aus diesem Grund ist es am besten, immer Symbole für alle Komponenten anzufordern.

Es ist möglicherweise nicht möglich, Symbole für jede Komponente anzufordern, z. –., wenn Videotreiber über DLLs im Prozessbereich verfügen und die erforderlichen PDB-Dateien auf dem Microsoft-Symbol Server verfügbar sind. In diesem Fall kommt es zu einer kurzen Verzögerung, wenn Sie eine Debugsitzung starten.

Um dies zu vermeiden, können Sie den Debugger einmal ausführen, um alle Symbole lokal vom Microsoft-Symbol Server zwischenzuspeichern. Ändern Sie dann Ihren \_ NT- \_ Symbol \_ Pfad, um den Microsoft-Symbol Server zu entfernen. Wenn sich die ausführbaren Dateien nicht ändern, wird durch die Prüfung auf ausführbare Dateien ohne Symbole keine Abfrage über das Internet benötigt, da Sie über lokale zwischengespeicherte Kopien aller Symbole verfügen, die Sie auf dem Microsoft-Symbol Server benötigen.

## <a name="getting-symbols-manually"></a>Manuelles erhalten von Symbolen

Wenn Sie den Debugger ordnungsgemäß eingerichtet haben, lädt er automatisch alle erforderlichen Symbole aus dem lokalen Cache oder einem Symbol Server. Wenn Sie die Symbole für nur eine einzelne ausführbare Datei oder für einen Ordner mit ausführbaren Dateien erhalten möchten, können Sie **Symchk** verwenden. Wenn Sie z. b. die Symbole für die \_ Datei d3dx930.dll im Windows-System Ordner in das aktuelle Verzeichnis herunterladen möchten, können Sie den folgenden Befehl verwenden:

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" c:\Windows\System32\d3dx9_30.dll /oc \.
```

Das **Symchk** -Tool hat viele andere Verwendungsmöglichkeiten. Weitere Informationen finden Sie unter **Symchk/?**, oder in der Dokumentation zu Microsoft-Debuggingtools für Windows.

## <a name="setting-up-a-symbol-server"></a>Einrichten eines Symbol Servers

Das Einrichten eines Symbol Servers ist sehr einfach. Dies ist aus folgenden Gründen hilfreich:

-   Um Bandbreite zu sparen oder um die Symbol Auflösung für Ihr Unternehmen, Ihr Team oder Ihr Produkt zu beschleunigen. Ein interner Symbol Server in einer lokalen Dateifreigabe im Netzwerk speichert alle Verweise auf externe Symbol Server, wie z. b. den Microsoft-Symbol Server, zwischen. Auf einen lokalen oder internen Symbol Server kann von vielen Benutzern gleichzeitig schnell zugegriffen werden. Daher spart Sie Bandbreite und Latenzzeit, die doppelte Symbol Anforderungen erstellen können.
-   Zum Speichern von Symbolen für alte Builds, Versionen oder externe Releases Ihrer Anwendung. Durch das Speichern der Symbole für diese Builds auf einem Symbol Server, auf den Sie problemlos zugreifen können, können Sie Abstürze und Probleme in diesen Builds auf allen Computern Debuggen, die über einen Debugger und eine Verbindung mit dem lokalen Symbol Server verfügen. Dies ist besonders nützlich, wenn Sie Minidumps Debuggen, die von ausführbaren Dateien generiert werden, die Sie nicht selbst erstellt haben – d. h. Builds, die von einem anderen Programmierer oder einem Buildcomputer generiert wurden. Wenn die Symbole für diese Builds auf dem Symbol Server gespeichert sind, haben Sie zuverlässiges und genaues Debuggen.
-   , Um Symbole auf dem neuesten Stand zu halten. Wenn Komponenten aktualisiert werden, wie z. b. Betriebssystemkomponenten, die durch Windows Update oder das DirectX SDK geändert werden, können Sie weiterhin mit allen aktuellen Symbolen Debuggen.

Das Einrichten eines Symbol Servers in Ihrem eigenen lokalen Netzwerk ist so einfach wie das Erstellen einer Dateifreigabe auf einem Server und das Erteilen von vollständigen Berechtigungen für den Zugriff auf die Freigabe, um Dateien und Ordner zu erstellen. Diese Freigabe sollte auf einem Server Betriebssystem erstellt werden, z. b. Windows Server 2003, damit die Anzahl der Personen, die gleichzeitig auf die Freigabe zugreifen können, nicht eingeschränkt ist.

Wenn Sie z. b. eine Dateifreigabe auf \\ \\ Main maindatabase- \\ Symbolen einrichten, legen die Mitglieder des Teams den \_ NT- \_ Symbol \_ Pfad auf Folgendes fest:

``` syntax
Srv*c:\symbols*\\mainserver\symbols*https://msdl.microsoft.com/download/symbols
```

Beim Abrufen von Symbolen werden Dateien und Ordner im frei \\ \\ gegebenen Verzeichnis der Main maindatabase- \\ Symbole sowie in einzelnen Caches im Verzeichnis c: \\ Symbols angezeigt.

Dies ist in der Regel alles, was beim Einrichten und Verwenden Ihres eigenen Symbol Servers oder des Microsoft-Symbol Servers beteiligt ist.

## <a name="adding-symbols-to-a-symbol-server"></a>Hinzufügen von Symbolen zu einem Symbol Server

Um Dateien auf einer Symbol Server Freigabe hinzuzufügen, zu löschen oder zu bearbeiten, verwenden Sie das symstore.exe Tool. Dieses Tool ist Teil des Microsoft Debugtools für Windows-Paket. Die vollständige Dokumentation zu Symbol Servern, dem SymStore-Tool und Indizierungs Symbolen ist im Paket Debugtools für Windows enthalten.

Möglicherweise möchten Sie dem eigenen Symbol Server als Teil eines Buildprozesses Symbole direkt hinzufügen, oder Sie können dem gesamten Team Symbole für Bibliotheken oder Tools von Drittanbietern zur Verfügung stellen. Das Hinzufügen eines Symbols zu einer Symbol Server-Dateifreigabe wird als Indizierungs Symbole bezeichnet. Es gibt zwei gängige Methoden zum Indizieren von Symbolen. Eine Symbol Datei kann auf den Symbol Server kopiert werden. Oder ein Zeiger auf den Speicherort des Symbols kann auf den Symbol Server kopiert werden. Wenn Sie über einen Archivordner verfügen, der Ihre alten Builds enthält, können Sie Zeiger auf die PDB-Dateien indizieren, die sich bereits auf der Freigabe befinden, anstatt Symbole zu duplizieren. Da Symbole manchmal eine Größe von zehn Megabyte haben können, empfiehlt es sich, voraus zu planen, wie viel Speicherplatz Sie benötigen, um alle Builds Ihres Projekts während der Entwicklung zu archivieren. Wenn Sie nur Zeiger auf Symbole indizieren, treten möglicherweise Probleme auf, wenn Sie alte Builds entfernen oder den Namen einer Dateifreigabe ändern.

Um beispielsweise rekursiv alle Symbole in c: dxsym-Extras-Symbolen zu indizieren, die \\ \\ \\ Sie aus dem DirectX SDK von Oktober 2006 auf eine Symbol Server-Dateifreigabe \\ \\ mit dem Namen Main maindatabase- \\ Symbole abgerufen haben, können Sie den folgenden Befehl verwenden:

``` syntax
"c:\Program Files\Debugging Tools for Windows\symstore" add /f "C:\dxsym\Extras\Symbols\*.pdb"
/s \\mainserver\symbols /t "October 2006 DirectX SDK " /r
```

Der **/t-Parameter "comment"** wird verwendet, um der Transaktion, durch die die Symbole hinzugefügt wurden, eine Beschreibung hinzuzufügen. Dies kann beim Ausführen administrativer Aufgaben für die Symbole nützlich sein.

## <a name="best-practices"></a>Bewährte Methoden

-   Richten Sie eine eigene Symbol Server-Dateifreigabe für Ihr Team, Ihr Unternehmen oder Ihr Produkt ein.
-   Richten Sie \_ \_ den NT \_ -Symbol Pfad ein, um auf einen lokalen Cache, auf einen privaten Symbol Server und auf den Microsoft-Symbol Server zu verweisen.
-   Wenn ein Debugger keine Symbole für eine Komponente laden kann, die Sie Debuggen, wenden Sie sich an den Besitzer der Komponente, um Symbole anzufordern – zumindest eine abgestreifte pdb.
-   Richten Sie ein automatisiertes Buildsystem ein, um Symbole auf dem privaten Symbol Server für jeden erstellten Build zu indizieren. Stellen Sie sicher, dass es sich bei den von Ihnen verteilten Builds um die Builds handelt, die von diesem Prozess generiert werden. Dadurch wird sichergestellt, dass Symbole immer für Debugprobleme verfügbar sind.
-   Richten Sie einen Symbol Server ein, um den Debuggern den Zugriff auf den Quellcode für ein bestimmtes Modul direkt von einem auf der Grundlage eines visuellen Quellcodes oder einem auf einem Symbol basierenden Quell Code Verwaltungssystem zu gestatten. Wenn die Quelldatei Informationen und-Symbole für eine veröffentlichte Version eines Spiels indiziert sind, können Entwickler, die Zugriff auf Ihren Symbol Server haben, über vollständiges Debuggen von gemeldeten Problemen auf Quell Ebene verfügen, ohne dass Buildumgebungen oder alte Versionen der Quelldateien auf ihren Entwicklungs Computern aufbewahrt werden. Informationen zum Einrichten des Symbol Servers zum Zulassen der Indizierung von Quelldatei Informationen finden Sie in der Dokumentation zum Quell Server.

 

 