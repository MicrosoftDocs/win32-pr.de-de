---
title: Debuggen mit Symbolen
description: Dieser Artikel bietet eine allgemeine Übersicht über die optimale Verwendung von Symbolen in Ihrem Debugprozess.
ms.assetid: 7ce0c9c7-485c-8d72-0353-27fd2e369a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd9935c490204736995e17e3c8013ce56f57624b
ms.sourcegitcommit: 4c71a269e3a114c72dd9eb31ccb4948a32beaa5b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/24/2021
ms.locfileid: "114662260"
---
# <a name="debugging-with-symbols"></a>Debuggen mit Symbolen

Dieser Artikel bietet eine allgemeine Übersicht über die optimale Verwendung von Symbolen in Ihrem Debugprozess. Es wird erläutert, wie Sie den Microsoft-Symbolserver verwenden und wie Sie einen eigenen privaten Symbolserver einrichten und verwenden. Diese bewährten Methoden können Dazu beitragen, Ihre Effektivität zu erhöhen und Probleme zu debuggen, selbst wenn sich nicht alle Symbole und ausführbaren Dateien, die mit einem Problem in Zusammenhang stehen, auf Ihrem Computer befinden.

-   [Symbols](#debugging-with-symbols)
-   [Verwenden von Symbolen für das Debuggen](#using-symbols-for-debugging)
-   [Abrufen der benötigten Symbole](#getting-the-symbols-you-need)
    -   [Überprüfen Sie, ob eine bestimmte DLL oder .exe Datei und PDB im selben Ordner übereinstimmen.](#check-if-a-given-dll-or-exe-file-and-pdb-in-the-same-folder-match)
    -   [Überprüfen Sie, ob alle DLLs und ausführbaren Dateien in einer Gruppe von Ordnern übereinstimmende PDBs aufweisen.](#check-if-all-the-dlls-and-executable-files-in-a-set-of-folders-have-matching-pdbs)
    -   [Funktionsweise von Symchk](#how-symchk-works)
-   [Symbolserver](#symbol-servers)
-   [Verwenden des Microsoft-Symbolservers](#using-the-microsoft-symbol-server)
-   [Manuelles Abrufen von Symbolen](#getting-symbols-manually)
-   [Einrichten eines Symbolservers](#setting-up-a-symbol-server)
-   [Hinzufügen von Symbolen zu einem Symbolserver](#adding-symbols-to-a-symbol-server)
-   [Bewährte Methoden](#best-practices)

## <a name="symbols"></a>Symbole

Für das Debuggen stehen verschiedene Symboltypen zur Verfügung. Dazu gehören CodeView-Symbole, COFF, DBG, SYM, PDB und sogar Exportsymbole, die aus einer Exporttabelle für Binärdateien generiert werden. In diesem Whitepaper werden nur VS.NET und die PDB-Formatsymbole erläutert, da es sich um das neueste bevorzugte Format handelt. Sie werden standardmäßig für Projekte generiert, die mithilfe von Visual Studio kompiliert werden.

Das Generieren von PDB-Dateien für ausführbare Releasedateien wirkt sich nicht auf Optimierungen aus oder ändert die Größe der generierten Dateien erheblich. In der Regel ist der einzige Unterschied der Pfad, und der Dateiname der PDB-Datei wird in die ausführbare Datei eingebettet. Aus diesem Grund sollten Sie immer PDB-Dateien erstellen, auch wenn Sie sie nicht mit der ausführbaren Datei versenden möchten.

PDB-Dateien werden generiert, wenn ein Projekt mithilfe des Compilerschalters **/Zi** oder **/ZI** (PdB-Informationen erzeugen) zusammen mit dem Linkerschalter **/DEBUG** (Debuginformationen generieren) erstellt wird. Die vom Compiler generierten PDB-Dateien werden kombiniert und in eine einzelne PDB-Datei geschrieben, die sich im selben Verzeichnis wie die ausführbare Datei befindet.

PdB-Dateien enthalten standardmäßig die folgenden Informationen:

-   Öffentliche Symbole (in der Regel alle Funktionen, statische und globale Variablen)
-   Eine Liste der Objektdateien, die für Codeabschnitte in der ausführbaren Datei verantwortlich sind.
-   Informationen zur Framezeigeroptimierung (Frame Pointer Optimization Information, FPO)
-   Namens- und Typinformationen für lokale Variablen und Datenstrukturen
-   Informationen zur Quelldatei und Zeilennummer

Wenn Sie Bedenken haben, dass Personen die PDB-Dateiinformationen verwenden, um sie beim Reverse Engineering Ihrer ausführbaren Datei zu unterstützen, können Sie auch entfernte PDB-Dateien generieren, indem Sie die Linkeroption **/PDBSTRIPPED:filename** verwenden. Wenn Sie über vorhandene PDB-Dateien verfügen, aus denen Sie private Informationen entfernen möchten, können Sie ein Tool namens pdbcopy verwenden, das Teil der Debugtools für Windows ist.

Standardmäßig enthalten pdb-Stripesetdateien die folgenden Informationen:

-   Öffentliche Symbole (in der Regel nur nicht statische Funktionen und globale Variablen)
-   Eine Liste der Objektdateien, die für Codeabschnitte in der ausführbaren Datei verantwortlich sind.
-   Informationen zur Framezeigeroptimierung (Frame Pointer Optimization Information, FPO)

Dies sind die Mindestinformationen, die erforderlich sind, um ein zuverlässiges Debuggen zu ermöglichen. Minimale Informationen erschweren auch das Abrufen zusätzlicher Informationen zu Ihrem ursprünglichen Quellcode. Da sowohl eine PDB-Stripesetdatei als auch eine reguläre PDB-Datei generiert werden, können Sie die entfernte Version benutzern bereitstellen, die möglicherweise eingeschränkte Debugfähigkeiten benötigen, aber die vollständigen PDB-Dateien vertraulich halten. Beachten Sie, dass **/PDBSTRIPPED** eine zweite, kleinere PDB-Datei generiert. Stellen Sie daher sicher, dass Sie die richtige PDB-Datei verwenden, wenn Sie Builds generieren, um sie umfassend zu verteilen. Bei einem typischen Projekt kann ein reguläres PDB einige Megabyte groß sein, aber eine entfernte Version der PDB kann nur einige hundert Kilobyte groß sein.

## <a name="using-symbols-for-debugging"></a>Verwenden von Symbolen für das Debuggen

Wenn Sie eine anwendung debuggen, die abgestürzt ist, versucht der Debugger, Ihnen die Funktionen auf dem Stapel anzuzeigen, die zum Absturz geführt haben. Ohne eine PDB-Datei kann der Debugger die Funktionsnamen, ihre Parameter oder lokale Variablen, die im Stapel gespeichert sind, nicht auflösen. Wenn Sie ausführbare 32-Bit-Dateien debuggen, gibt es Situationen, in denen Sie keine zuverlässigen Stapelüberwachungen ohne Symbole erhalten können. Manchmal ist es möglich, die rohen Werte im Stapel zu betrachten und herauszufinden, welche Werte Adressen zurückgeben können. Diese können jedoch leicht mit Funktionsverweisen oder Daten verwechselt werden.

Wenn Funktionen im aktuellen Stapel mithilfe der Optimierung Framezeiger auslassen (**/Oy**) kompiliert wurden und keine Symbole vorhanden sind, kann der Debugger nicht zuverlässig bestimmen, welche Funktion die aktuelle Funktion aufgerufen hat. Dies liegt daran, dass der Debugger ohne die Framezeigeroptimierungsinformationen (Frame Pointer Optimization, FPO), die PDBs enthalten, sich nicht darauf verlassen kann, dass das Framezeigerregister (EBP) auf den gespeicherten vorherigen Framezeiger und auf die Rückgabeadresse der übergeordneten Funktion zeigt. Stattdessen wird erraten. Manchmal wird es richtig. Es kommt jedoch häufig zu einem Fehler, der irreführend sein kann. Wenn wie im folgenden Beispiel eine Warnung zu fehlenden oder nicht geladenen Symbolen angezeigt wird, vertrauen Sie dem Stapel von diesem Punkt an nicht.

``` syntax
SWPerfTest.exe!TextFunction(... ...)    Line 59    C++
d3dx9d.dll!008829b5()
[Frames below may be incorrect and/or missing, no symbols loaded for d3dx9d.dll]
SWPerfTest.exe!main(int argc=, const char * * argv=)  Line 328 + 0x12 bytes     C++
SWPerfTest.exe!__mainCRTStartup() Line 716 + 0x17 bytes    C
kernel32.dll!@BaseThreadInitThunk@12() + 0x12 bytes
ntdll.dll!__RtlUserThreadStart@8() + 0x27 bytes
```

In vielen Fällen ist es möglich, das Debuggen ohne Symbole fortzusetzen, da sich das Problem an einem Speicherort mit genauen Symbolen befindet und Sie sich die Funktionen nicht weiter unten in der Aufrufliste ansehen müssen. Selbst wenn für eine Bibliothek, die sich in Ihrer Aufrufliste befindet, keine PDBs verfügbar sind, sollte der Debugger in der Lage sein, die übergeordneten Funktionen richtig zu erraten, solange sie mit Framezeigern kompiliert wurden. Ab Windows XP Service Pack 2 werden alle Windows DLL- und ausführbaren Dateien mit deaktivierter FPO kompiliert, da das Debuggen genauer wird. Durch das Deaktivieren des FPO können Samplingprofiler den Stapel auch während der Laufzeit durchlaufen, ohne dass die Leistung beeinträchtigt wird. In Versionen von Windows vor Windows XP SP2 erfordern alle Betriebssystembinärdateien übereinstimmende Symboldateien, die FPO-Informationen enthalten, um genaues Debuggen und Profilerstellung zu ermöglichen.

Wenn Sie native 64-Bit-Ausführbare Dateien debuggen, benötigen Sie keine Symboldateien, um gültige Stapelüberwachungen zu erzeugen, da x64-Betriebssysteme und -Compiler dafür ausgelegt sind, sie nicht zu erfordern. Sie benötigen jedoch weiterhin Symboldateien, um die Funktionsnamen, Aufrufparameter und lokalen Variablen abzurufen.

In einigen Fällen ist das Debuggen ohne Symbole jedoch besonders schwierig. Wenn Sie z. B. ein Programm debuggen, für das Sie eine PDB-Datei erstellt haben, und wenn Sie einen Rückruf von einer Funktion in einer DLL abstürzen, für die Sie keine Symbole haben, können Sie nicht erkennen, für welche Funktion der Rückruf verursacht wurde, da Sie den Stapel nicht decodieren können. Dies geschieht häufig in Bibliotheken von Drittanbietern, wenn PDBs nicht bereitgestellt werden, oder in alten Betriebssystemkomponenten, wenn PDBs nicht verfügbar sind. Rückrufe erfolgen häufig während der Nachrichtenübergabe, Enumeration, Speicherbelegung oder Ausnahmebehandlung. Das Debuggen dieser Funktionen ohne einen genauen Stapel kann frustrierend sein.

Zum zuverlässigen Debuggen von Minidummps, die auf einem anderen Computer generiert werden oder in Code abgestürzt sind, den Sie nicht besitzen, ist es wichtig, auf alle Symbole und Binärdateien für die ausführbaren Dateien zugreifen zu können, auf die im Minidump verwiesen wird. Wenn die Symbole und Binärdateien von einem Symbolserver verfügbar sind, werden sie automatisch vom Debugger abgerufen. Weitere Informationen zu Minidumps finden Sie im Whitepaper [Absturzabbildanalyse.](/windows/desktop/DxTechArts/crash-dump-analysis)

## <a name="getting-the-symbols-you-need"></a>Abrufen der benötigten Symbole

Visual Studio und andere Microsoft-Debugger wie WinDbg sind in der Regel so eingerichtet, dass sie nur funktionieren, wenn Sie eine Anwendung erstellen und auf Ihrem eigenen Computer debuggen. Wenn Sie Ihre ausführbare Datei einer anderen Person zur Verfügung stellen müssen, wenn Sie mehrere Versionen einer DLL oder einer .exe-Datei auf Ihrem Computer haben oder eine Anwendung, die Windows oder andere Bibliotheken wie DirectX verwendet, genau debuggen möchten, müssen Sie verstehen, wie Debugger Symbole suchen und laden. Der Debugger verwendet entweder den vom Benutzer angegebenen Symbolsuchpfad , der sich unter \\ Optionen \\ Debugsymbole in Visual Studio befindet, oder die \_ \_ Umgebungsvariable NT SYMBOL \_ PATH. In der Regel sucht der Debugger an den folgenden Speicherorten nach übereinstimmenden PDBs:

-   Der Speicherort, der in der DLL-Datei oder der ausführbaren Datei angegeben ist.

    Wenn Sie eine DLL oder eine ausführbare Datei auf Ihrem Computer erstellt haben, platziert der Linker standardmäßig den vollständigen Pfad und Dateinamen der zugeordneten PDB-Datei in der DLL oder der ausführbaren Datei. Beim Debuggen überprüft der Debugger zunächst, ob die Symboldatei an dem Speicherort vorhanden ist, der in der DLL oder der ausführbaren Datei angegeben ist. Dies ist hilfreich, da Immer Symbole für Code verfügbar sind, den Sie auf Ihrem Computer kompiliert haben.

-   PDBs, die sich möglicherweise im selben Ordner wie die DLL oder ausführbare Datei befinden.
-   Alle lokalen Symbolcache-Ordner.
-   Alle Symbolserver für lokale Netzwerkdateifreigaben.
-   Alle Internetsymbolserver, z. B. der Microsoft-Symbolserver.

Installieren Sie die Debugtools für Windows, um sicherzustellen, dass Sie über alle PDBs verfügen, die Sie für das genaue Debuggen benötigen. Die 32- und 64-Bit-Versionen finden Sie unter [Debugtools für Windows](/windows-hardware/drivers/debugger/).

Ein nützliches Tool, das mit diesem Paket installiert wird, ist symchk.exe. Es kann helfen, fehlende oder falsche Symbole zu identifizieren. Dieses Tool verfügt über eine große Anzahl potenzieller Befehlszeilenoptionen. Hier sind zwei der nützlicheren und häufig verwendeten.

### <a name="check-if-a-given-dll-or-exe-file-and-pdb-in-the-same-folder-match"></a>Überprüfen Sie, ob eine bestimmte DLL oder .exe Datei und PDB im selben Ordner übereinstimmen.

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" testing.dll /s .

SYMCHK: FAILED files = 0
SYMCHK: PASSED + IGNORED files = 1
```

Die **/s .** -Option weist **symchk** an, nur im aktuellen Ordner nach Symbolen zu suchen und nicht auf Symbolservern.

### <a name="check-if-all-the-dlls-and-executable-files-in-a-set-of-folders-have-matching-pdbs"></a>Überprüfen Sie, ob alle DLLs und ausführbaren Dateien in einer Gruppe von Ordnern übereinstimmende PDBs aufweisen.

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" *.* /r
```

Mit der Option **/r** wird **symchk** so festgelegt, dass Ordner rekursiv durchlaufen werden, um zu überprüfen, ob alle ausführbaren Dateien über übereinstimmende PDBs verfügen. Ohne die Option **/s** verwendet **symchk** den aktuellen NT SYMBOL PATH, um nach \_ \_ \_ Symbolen auf einem privaten oder lokalen Server oder auf den Microsoft-Symbolservern zu suchen. Das **Symchk-Tool** sucht nur nach Symbolen für ausführbare Dateien (.exe, .dll usw.). Sie können keine Platzhalter verwenden, um nach Symbolen für nicht ausführbare Dateien zu suchen.

### <a name="how-symchk-works"></a>Funktionsweise von Symchk

Wenn der Linker .dll, ausführbare Dateien und PDB-Dateien generiert, speichert er identische GUIDs in jeder Datei. Die GUID wird von Tools verwendet, um zu bestimmen, ob eine bestimmte PDB-Datei mit einer DLL oder einer ausführbaren Datei entspricht. Wenn Sie eine DLL oder eine ausführbare Datei ändern – mithilfe eines Ressourcen-Editors oder einer Kopierschutzcodierung oder durch Ändern der Versionsinformationen –, wird die GUID aktualisiert, und der Debugger kann die PDB-Datei nicht laden. Aus diesem Grund ist es sehr wichtig, zu vermeiden, dass die DLL oder ausführbare Datei nach dem Erstellen durch den Linker manipuliert wird.

Sie können auch das hilfsprogramm DUMPBIN verwenden, das im VS.NET enthalten ist, um die gesuchten Symbolpfade zu zeigen und um zu sehen, ob Symboldateien gefunden werden, die mit einer bestimmten DLL oder ausführbaren Datei übereinstimmen. Beispiel:

``` syntax
DUMPBIN /PDBPATH:VERBOSE filename.exe
```

## <a name="symbol-servers"></a>Symbolserver

Ein Symbolserver ist ein Repository für mehrere Versionen von ausführbaren Dateien und Symboldateien. Sie enthält entweder die Symboldateien selbst oder Zeiger auf die zugeordneten Symboldateien. Debugger verstehen, wie Symbolserver verwendet werden, und können sie verwenden, um nach fehlenden oder unbekannten Symbolen zu suchen.

DLL- und ausführbare Dateien sind auch auf dem Microsoft-Symbolserver verfügbar. Dies ermöglicht das Debuggen von Abstürzen und das Untersuchen von Code auf Betriebssystemdateien, die möglicherweise nicht auf Ihrem Computer vorhanden sind. Wenn ein Debugger auf eine ausführbare Datei oder dll trifft, die nicht auf dem System vorhanden ist, das Sie zum Debuggen verwenden, fordert er automatisch sowohl die Symbole als auch eine Kopie der Binärdatei von den Microsoft-Symbolservern an. Dies ist hilfreich, wenn Sie eine Komponente debuggen, die über viele Versionen verfügt , z. B. msvcrt.dll), und Sie den Code auf eine Version untersuchen müssen, die auf Ihrem Computer nicht vorhanden ist. Dies hilft auch beim Debuggen von Minidumps, die auf einem Betriebssystem generiert werden, das sich von dem System, das Sie für das Debuggen verwenden, unterscheiden.

Microsoft veröffentlicht alle PDB-Dateien für alle Betriebssysteme und andere weiterverteilte Komponenten, z. B. das DirectX SDK, auf dem extern zugänglichen Symbolserver. Dies erleichtert das Debuggen einer Anwendung, die diese DLL- oder ausführbaren Dateien verwendet. Sie können den Microsoft-Symbolserver verwenden, um Symbole zusammen mit allen lokalen Symbolen für Komponenten aufzulösen, die auf Ihrem Computer erstellt wurden.

Sie können Ihren Computer für die Verwendung des Microsoft-Symbolservers einrichten, der Ihnen Zugriff auf alle Microsoft-Symboldateien bietet. Sie können auch einen privaten Symbolserver für Ihr Unternehmen, Team oder Netzwerk einrichten, der verwendet werden kann, um mehrere ältere Versionen eines Projekts zu speichern, an dem Sie arbeiten, oder um einen lokalen Cache für die Symbole zur Verfügung zu stellen, die Sie vom Microsoft-Symbolserver verwenden.

Um einen Symbolserver zu verwenden, geben Sie den Suchpfad in einer Umgebungsvariablen mit dem Namen \_ NT \_ SYMBOL PATH \_ an. Debugger und moderne Tools wie WinDbg, NTSD oder Visual Studio verwenden diesen Pfad automatisch, um nach Symbolen zu suchen.

Wenn ein Debugger nach Symbolen sucht, sucht er zuerst lokal. Anschließend wird nach Symbolservern sucht. Wenn ein übereinstimmendes Symbol gefunden wird, wird die Symboldatei in Ihren lokalen Cache übertragen. Die Symbole für eine typische DLL- oder ausführbare Datei reichen von 1 bis 100 MB. Wenn Sie einen Prozess debuggen, der viele DLLs enthält, kann es daher einige Zeit dauern, alle Symbole aufzulösen und in einen lokalen Cache zu übertragen.

## <a name="using-the-microsoft-symbol-server"></a>Verwenden des Microsoft-Symbolservers

Mit dem Microsoft-Symbolserver können Sie alle aktuellen Symbole abrufen, einschließlich Symbolen für gepatchte oder aktualisierte Dateien. Der Microsoft-Symbolserver ist unter <https://msdl.microsoft.com/download/symbols> verfügbar.

Sie können auf eine der folgenden Arten auf den Symbolserver zugreifen:

-   Geben Sie die Serveradresse direkt ein. Wählen Visual Studio im Menü **Extras** die Option **Optionen** aus, und klicken Sie dann **auf Debuggen** und dann auf **Symbole.**
-   Verwenden Sie die Umgebungsvariable \_ NT \_ SYMBOL \_ PATH. Diese Methode wird empfohlen.

    Dies wird von allen Debugtools verwendet. Er wird auch von Visual Studio verwendet und gelesen und decodiert, wenn Visual Studio wird. Wenn Sie dies ändern, müssen Sie daher Visual Studio.

    Mit dieser Umgebungsvariable können Sie mehrere Symbolserver angeben, z. B. einen internen privaten Symbolserver. Außerdem können Sie ein lokales Cacheverzeichnis angeben, in dem PDBs für alle Symbole gespeichert werden, die Sie von Symbolservern suchen, sowohl intern als auch über das Internet.

Die Syntax für die \_ NT \_ SYMBOL \_ PATH-Variable ist:

``` syntax
srv*[local cache]*[private symbol server]*https://msdl.microsoft.com/download/symbols
```

Ersetzen Sie den lokalen Cache durch den Namen eines Verzeichnisses auf Ihrem Computer, in dem Sie einen Cache aller verwendeten Symbole speichern möchten, z. B. \[ \] %SYSTEMROOT%-Symbole oder \\ \\ c:-Symbole.

Der \[ private Symbolserver \] ist optional. Er kann auf einen Symbolserver in Ihrem Netzwerk oder auf einen Symbolserver verweisen, der von Ihrem Team, Ihrer Produktgruppe oder Ihrem Unternehmen gemeinsam genutzt wird.

Wenn Sie nur den Microsoft-Symbolserver zusammen mit einem lokalen Cache von Symbolen verwenden möchten, um den Zugriff über das Internet zu beschleunigen, verwenden Sie die folgende Einstellung für \_ NT \_ SYMBOL \_ PATH:

``` syntax
srv*c:\symbols*https://msdl.microsoft.com/download/symbols
```

Weitere Optionen für NT SYMBOL PATH finden Sie in der Hilfedatei, die mit den \_ Microsoft Debugging Tools for Windows installiert \_ \_ wird.

Ausführbare Dateien ohne Symbole können die Zeit zum Starten eines Debuggers erhöhen, wenn Sie einen Symbolserver verwenden. Dies liegt daran, dass der Debugger den Symbolserver jedes Mal abfragt, wenn er versucht, die ausführbare Datei zu laden. Aus diesem Grund ist es am besten, immer Symbole für alle Komponenten an fordern.

Es ist möglicherweise nicht möglich, Symbole für jede Komponente anzufordern. Beispielsweise können Videotreiber DLLs in Ihrem Prozessbereich enthalten, und die erforderlichen PDB-Dateien sind auf dem Microsoft-Symbolserver verfügbar. In diesem Fall gibt es eine kleine Verzögerung, wenn Sie eine Debugsitzung starten.

Um selbst diese kleine Verzögerung zu vermeiden, können Sie den Debugger einmal ausführen, um alle Symbole lokal vom Microsoft-Symbolserver zwischenspeichern zu können. Ändern Sie dann Den \_ NT \_ SYMBOL \_ PATH, um den Microsoft-Symbolserver zu entfernen. Wenn sich die ausführbaren Dateien nicht ändern, ist für die Überprüfung auf ausführbare Dateien, die keine Symbole enthalten, keine Abfrage über das Internet erforderlich, da Sie über lokale zwischengespeicherte Kopien aller Symbole verfügen, die Sie vom Microsoft-Symbolserver benötigen.

## <a name="getting-symbols-manually"></a>Manuelles Abrufen von Symbolen

Wenn Sie den Debugger ordnungsgemäß eingerichtet haben, werden automatisch alle benötigten Symbole aus dem lokalen Cache oder von einem Symbolserver geladen. Wenn Sie die Symbole nur für eine einzelne ausführbare Datei oder für einen Ordner mit ausführbaren Dateien erhalten möchten, können Sie **symchk verwenden.** Wenn Sie beispielsweise die Symbole für die30.dll-Datei d3dx9 im Ordner Windows System in das aktuelle Verzeichnis herunterladen möchten, können Sie den folgenden \_ Befehl verwenden:

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" c:\Windows\System32\d3dx9_30.dll /oc \.
```

Das **Symchk-Tool** hat viele andere Verwendungsmöglichkeiten. Weitere Informationen finden Sie unter **symchk /?** oder in der Dokumentation zu Microsoft Debugging Tools Windows Tools.

## <a name="setting-up-a-symbol-server"></a>Einrichten eines Symbolservers

Das Einrichten eines Symbolservers ist sehr einfach. Dies ist aus den folgenden Gründen nützlich:

-   Um Bandbreite zu sparen oder die Symbolauflösung für Ihr Unternehmen, Team oder Produkt zu beschleunigen. Ein interner Symbolserver auf einer lokalen Dateifreigabe in Ihrem Netzwerk speichert alle Verweise auf externe Symbolserver zwischen, z. B. den Microsoft-Symbolserver. Auf einen lokalen oder internen Symbolserver kann von vielen Personen gleichzeitig schnell zugegriffen werden. Aus diesem Grund spart es Bandbreite und die Latenz, die doppelte Symbolanforderungen erstellen können.
-   Zum Speichern von Symbolen für alte Builds, Versionen oder externe Releases Ihrer Anwendung. Indem Sie die Symbole für diese Builds auf einem Symbolserver speichern, auf den Sie problemlos zugreifen können, können Sie Abstürze und Probleme in diesen Builds auf jedem Computer debuggen, der über einen Debugger und eine Verbindung mit dem lokalen Symbolserver verfügt. Dies ist besonders nützlich, wenn Sie Minidumps debuggen, die von ausführbaren Dateien generiert werden, die Sie nicht selbst erstellt haben, d. &a; Builds, die von einem anderen Programmierer oder von einem Buildcomputer generiert wurden. Wenn die Symbole für diese Builds auf Dem Symbolserver gespeichert werden, verfügen Sie über zuverlässiges und genaues Debuggen.
-   So halten Sie Symbole auf dem neuesten Stand. Wenn Komponenten aktualisiert werden, z. B. Betriebssystemkomponenten, die durch Windows Update oder das DirectX SDK geändert werden, können Sie weiterhin debuggen, indem Sie alle aktuellen Symbole verwenden.

Das Einrichten eines Symbolservers in Ihrem eigenen lokalen Netzwerk ist so einfach wie das Erstellen einer Dateifreigabe auf einem Server und das Erteilen von vollständigen Berechtigungen für Benutzer zum Zugreifen auf die Freigabe sowie zum Erstellen von Dateien und Ordnern. Diese Freigabe sollte auf einem Serverbetriebssystem wie Windows Server 2003 erstellt werden, damit die Anzahl der Personen, die gleichzeitig auf die Freigabe zugreifen können, nicht begrenzt ist.

Wenn Sie beispielsweise eine Dateifreigabe für mainserver-Symbole einrichten, legen die Mitglieder Ihres Teams \\ \\ NT SYMBOL PATH \\ auf \_ \_ \_ Folgendes fest:

``` syntax
Srv*c:\symbols*\\mainserver\symbols*https://msdl.microsoft.com/download/symbols
```

Wenn Symbole abgerufen werden, werden Dateien und Ordner im freigegebenen Verzeichnis mainserver symbols sowie in einzelnen \\ \\ \\ Caches im Verzeichnis c: \\ symbols angezeigt.

Dies ist in der Regel alles, was an der Einrichtung und Verwendung ihres eigenen Symbolservers oder des Microsoft-Symbolservers beteiligt ist.

## <a name="adding-symbols-to-a-symbol-server"></a>Hinzufügen von Symbolen zu einem Symbolserver

Verwenden Sie zum Hinzufügen, Löschen oder Bearbeiten von Dateien auf einer Symbolserverfreigabe das symstore.exe Tool. Dieses Tool ist Teil des Microsoft Debugging Tools for Windows Pakets. Die vollständige Dokumentation zu Symbolservern, zum Symstore-Tool und zu Indizierungssymbolen ist im Paket Debugtools für Windows enthalten.

Möglicherweise möchten Sie Ihrem eigenen Symbolserver symbole direkt im Rahmen eines Buildprozesses hinzufügen oder Symbole für Drittanbieterbibliotheken oder -tools für Ihr gesamtes Team zur Verfügung stellen. Das Hinzufügen eines Symbols zu einer Symbolserver-Dateifreigabe wird als Indizierungssymbole bezeichnet. Es gibt zwei gängige Methoden zum Indizieren von Symbolen. Eine Symboldatei kann auf den Symbolserver kopiert werden. Oder ein Zeiger auf die Position des Symbols kann auf den Symbolserver kopiert werden. Wenn Sie über einen Archivordner verfügen, der Ihre alten Builds enthält, sollten Sie Zeiger auf die PDB-Dateien indizieren, die sich bereits auf der Freigabe befinden, anstatt Symbole zu duplizieren. Da Symbole manchmal dutzende Megabyte groß sein können, ist es eine gute Idee, im Voraus zu planen, wie viel Speicherplatz Sie benötigen, um alle Builds Ihres Projekts während der Entwicklung zu archivieren. Wenn Sie nur Zeiger auf Symbole indizieren, können Probleme auftreten, wenn Sie alte Builds entfernen oder den Namen einer Dateifreigabe ändern.

Um beispielsweise rekursiv alle Symbole in c: dxsym Extras Symbols zu indizieren, die Sie aus dem DirectX SDK vom Oktober \\ \\ \\ 2006 in einer Symbolserver-Dateifreigabe namens mainserver symbols erhalten \\ \\ haben, können Sie den folgenden Befehl \\ verwenden:

``` syntax
"c:\Program Files\Debugging Tools for Windows\symstore" add /f "C:\dxsym\Extras\Symbols\*.pdb"
/s \\mainserver\symbols /t "October 2006 DirectX SDK " /r
```

Der **Parameter /t "comment"** wird verwendet, um der Transaktion, die die Symbole hinzugefügt hat, eine Beschreibung hinzuzufügen. Dies kann beim Ausführen administrativer Aufgaben für die Symbole nützlich sein.

## <a name="best-practices"></a>Empfehlungen

-   Richten Sie Ihre eigene Symbolserver-Dateifreigabe für Ihr Team, Ihr Unternehmen oder Ihr Produkt ein.
-   Richten Sie \_ NT SYMBOL PATH ein, um auf einen lokalen Cache, auf einen privaten Symbolserver und auf den \_ \_ Microsoft-Symbolserver zu verweisen.
-   Wenn ein Debugger keine Symbole für eine Komponente laden kann, die Sie debuggen, wenden Sie sich an den Besitzer der Komponente, um Symbole anzufordern – mindestens eine entfernte PDB.
-   Richten Sie ein automatisiertes Buildsystem ein, um Symbole auf Ihrem privaten Symbolserver für jeden erstellten Build zu indizieren. Stellen Sie sicher, dass die von Ihnen verteilten Builds die Builds sind, die von diesem Prozess generiert werden. Dadurch wird sichergestellt, dass Symbole immer zum Debuggen von Problemen verfügbar sind.
-   Richten Sie einen Symbolserver ein, damit Debugger direkt über ein Visual Source-Tresor oder Perforce-basiertes Quellcodeverwaltungssystem auf den Quellcode für ein bestimmtes Modul zugreifen können. Wenn die Quelldateiinformationen und Symbole für eine veröffentlichte Version eines Spiels indiziert sind, können Entwickler, die Zugriff auf Ihren Symbolserver haben, das vollständige Debuggen gemeldeter Probleme auf Quellebene haben, ohne Buildumgebungen oder alte Versionen von Quelldateien auf ihren Entwicklungscomputern zu speichern. Informationen zum Einrichten des Symbolservers für die Indizierung von Quelldateiinformationen finden Sie in der Dokumentation zum Quellserver.

 

 
