---
title: 64-Bit-Programmierung für Spieleentwickler
description: Dieser Artikel behandelt Kompatibilitäts- und Portierungsprobleme und hilft Entwicklern, den Übergang zu 64-Bit-Plattformen zu vereinfachen.
ms.assetid: 23a7ed41-6637-0607-327e-983b622e9104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 439db3173e18206cb04875ab9c4422dbcedc7230508c8e98cf09b7fe27bfb9f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042430"
---
# <a name="64-bit-programming-for-game-developers"></a>64-Bit-Programmierung für Spieleentwickler

Prozessorhersteller ausgeliefert ausschließlich 64-Bit-Prozessoren auf ihren Desktopcomputern, und selbst die Sätze der meisten Laptopcomputer unterstützen x64-Technologie. Es ist wichtig, dass Spieleentwickler von den Verbesserungen profitieren, die 64-Bit-Prozessoren mit ihren neuen Anwendungen bieten, und sicherzustellen, dass ihre früheren Anwendungen ordnungsgemäß auf den neuen Prozessoren und den 64-Bit-Editionen von Windows Vista und Windows 7 ausgeführt werden. Dieser Artikel behandelt Kompatibilitäts- und Portierungsprobleme und hilft Entwicklern, den Übergang zu 64-Bit-Plattformen zu vereinfachen.

Microsoft verfügt derzeit über die folgenden 64-Bit-Betriebssysteme:

-   Windows Server 2003 Service Pack 1
-   Windows XP Professional x64 Edition (verfügbar für OEMs und Entwickler über MSDN)
-   Windows Vista
-   Windows Server 2008
-   Windows 7
-   Windows Server 2008 R2

> [!Note]  
> Windows Server 2008 R2 ist nur als 64-Bit-Edition verfügbar.

 

-   [Unterschiede im adressierbaren Arbeitsspeicher](#differences-in-addressable-memory)
-   [Angeben von großen Adressen beim Erstellen](#specifying-large-address-aware-when-building)
-   [Kompatibilität von 32-Bit-Anwendungen auf 64-Bit-Plattformen](#compatibility-of-32-bit-applications-on-64-bit-platforms)
    -   [Potenzielle Kompatibilitätsprobleme](#potential-compatibility-pitfalls)
-   [Portieren von Anwendungen auf 64-Bit-Plattformen](#porting-applications-to-64-bit-platforms)
-   [Profilerstellung und Optimierung von portierten Anwendungen](#profiling-and-optimization-of-ported-applications)
-   [Verwalteter Code unter einem 64-Bit-Betriebssystem](#managed-code-on-a-64-bit-operating-system)
-   [Auswirkungen der Ausführung eines 64-Bit-Betriebssystems auf die Leistung](#performance-implications-of-running-a-64-bit-operating-system)
-   [Zusammenfassung](#summary)

## <a name="differences-in-addressable-memory"></a>Unterschiede im adressierbaren Arbeitsspeicher

Das erste, was die meisten Entwickler bemerken, ist, dass 64-Bit-Prozessoren einen großen Sprung in der Menge an physischem und virtuellem Arbeitsspeicher bieten, der behoben werden kann.

-   32-Bit-Anwendungen auf 32-Bit-Plattformen können bis zu 2 GB adressiert werden.
-   32-Bit-Anwendungen, die mit dem /LARGEADDRESSAWARE:YES-Linkerflag auf 32-Bit-Windows XP oder Windows Server 2003 mit der speziellen Startoption /3gb erstellt wurden, können bis zu 3 GB adressiert werden. Dadurch wird der Kernel auf nur 1 GB beschränkt, was dazu führen kann, dass einige Treiber und/oder Dienste ausfallen.
-   32-Bit-Anwendungen, die mit dem /LARGEADDRESSAWARE:YES-Linkerflag in den 32-Bit-Editionen von Windows Vista, Windows Server 2008 und Windows 7 erstellt wurden, können den Arbeitsspeicher bis zu der Anzahl adressieren, die durch das Startkonfigurationsdatenelement IncreaseUserVa angegeben wird. "IncreaseUserVa" kann einen Wert zwischen 2048 (Standard) und 3072 (entspricht der Arbeitsspeichermenge, die von der Startoption "/3gb" auf Windows XP konfiguriert wurde) aufweisen. Der Rest von 4 GB wird dem Kernel zugeordnet und kann zu fehlerhaften Treiber- und Dienstkonfigurationen führen.

    Weitere Informationen zu BCD finden Sie unter [Startkonfigurationsdaten](https://msdn.microsoft.com/library/aa362692.aspx) auf MSDN.

-   32-Bit-Anwendungen auf 64-Bit-Plattformen können bis zu 2 GB oder bis zu 4 GB mit dem Linkerflag /LARGEADDRESSAWARE:YES adressiert werden.
-   64-Bit-Anwendungen verwenden 43 Bits für die Adressierung, wodurch 8 TB virtuelle Adressen für Anwendungen und 8 TB für den Kernel reserviert sind.

Neben dem Arbeitsspeicher profitieren 64-Bit-Anwendungen, die speicherzuordnungsbasierte Datei-E/A verwenden, erheblich vom erhöhten virtuellen Adressraum. Die 64-Bit-Architektur bietet auch eine verbesserte Gleitkommaleistung und eine schnellere Übergabe von Parametern. 64-Bit-Prozessoren verfügen über die doppelte Anzahl von Registern, sowohl von allgemeinen als auch streamingbasierten SIMD-Erweiterungstypen (SSE) sowie über Unterstützung für SSE- und SSE2-Anweisungssätze. viele 64-Bit-Prozessoren unterstützen sogar SSE3-Anweisungssätze.

## <a name="specifying-large-address-aware-when-building"></a>Angeben von großen Adressen beim Erstellen

Es empfiehlt sich, beim Erstellen von 32-Bit-Anwendungen große Adressfunktionen anzugeben, indem Sie das Linkerflag /LARGEADDRESSAWARE verwenden, auch wenn die Anwendung aufgrund der Vorteile, die ohne Kosten erzielt werden, nicht für eine 64-Bit-Plattform vorgesehen ist. Wie bereits erläutert, ermöglicht das Aktivieren dieses Flags für einen Build einem 32-Bit-Programm den Zugriff auf mehr Arbeitsspeicher mit speziellen Startoptionen auf einem 32-Bit-Betriebssystem oder einem 64-Bit-Betriebssystem. Entwickler müssen jedoch darauf achten, dass keine Zeigerannahmen getroffen werden, z. B. wenn angenommen wird, dass das High-Bit nie in einem 32-Bit-Zeiger festgelegt wird. Im Allgemeinen ist das Aktivieren des /LARGEADDRESSAWARE-Flags eine bewährte Methode.

30-Zwei-Bit-Anwendungen, die große Adressen erkennen, können zur Laufzeit ermitteln, wie viel virtueller Adressraum für sie mit der aktuellen Betriebssystemkonfiguration verfügbar ist, indem [**GlobalMemoryStatusEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex)aufgerufen wird. Das ullTotalVirtual-Ergebnis reicht von 2147352576 Bytes (2 GB) bis zu 4294836224 Bytes (4 GB). Werte, die größer als 3221094400 (3 GB) sind, können nur in 64-Bit-Editionen von Windows abgerufen werden. Wenn IncreaseUserVa beispielsweise den Wert 2560 auf hat, ist das Ergebnis ullTotalVirtual mit einem Wert von 2684223488 Bytes.

## <a name="compatibility-of-32-bit-applications-on-64-bit-platforms"></a>Kompatibilität von 32-Bit-Anwendungen auf 64-Bit-Plattformen

64-Bit-Windows-Betriebssysteme sind binär kompatibel mit der IA32-Architektur, und die meisten APIs, die von 32-Bit-Anwendungen verwendet werden, sind über die Windows 32-Bit auf Windows 64-Bit-Emulator WOW64 verfügbar. MIT WOW64 können Sie sicherstellen, dass diese APIs wie vorgesehen funktionieren.

WOW64 verfügt über eine Ausführungsebene, die das Marshalling von 32-Bit-Daten verarbeitet. WOW64 leitet DLL-Dateianforderungen um, leitet einige Registrierungsbranches für 32-Bit-Anwendungen um und spiegelt einige Registrierungsbranches für 32- und 64-Bit-Anwendungen wider.

Weitere Informationen zu WOW64 finden Sie unter [WOW64-Implementierungsdetails](/windows/desktop/WinProg64/wow64-implementation-details) auf MSDN. Bewährte Methoden zum Erstellen von Anwendungen, die unter WOW64 ausgeführt werden, finden Sie unter [Best Practices für WOW64](https://www.microsoft.com/whdc/system/platform/64bit/WoW64_bestprac.mspx) auf Windows Hardware Developer Central.

### <a name="potential-compatibility-pitfalls"></a>Potenzielle Kompatibilitätsprobleme

Die meisten Anwendungen, die für eine 32-Bit-Plattform entwickelt wurden, werden problemlos auf einer 64-Bit-Plattform ausgeführt. Einige Anwendungen können Probleme haben, z. B.:

-   Alle Treiber für von 64-Bit-Editionen von Windows Betriebssystemen müssen 64-Bit-Versionen sein. Die Anforderung neuer 64-Bit-Treiber hat Auswirkungen auf Kopierschutzschemas, die auf alten Treibern basieren. Beachten Sie, dass Kernelmodustreiber authenticodesigniert sein müssen, um von 64-Bit-Editionen von Windows geladen zu werden.
-   64-Bit-Prozesse können keine 32-Bit-DLLs laden, und 32-Bit-Prozesse können keine 64-Bit-DLLs laden. Entwickler müssen sicherstellen, dass 64-Bit-Versionen von Drittanbieter-DLLs verfügbar sind, bevor sie mit der Entwicklung fortfahren. Wenn Sie eine 32-Bit-DLL in einem 64-Bit-Prozess verwenden müssen, kann Windows Prozessübergreifende Kommunikation (Inter-Process Communication, IPC) verwendet werden. COM-Komponenten können auch Out-of-Process-Server und Marshalling für die Kommunikation zwischen Grenzen verwenden, aber dies kann zu Leistungseinbußen führen.
-   Viele x64-Prozessoren sind auch Mehrkernprozessoren, und Entwickler müssen testen, wie sich dies auf ihre Legacyanwendungen auswirkt. Weitere Informationen zu Mehrkernprozessoren und den Auswirkungen auf Spieleanwendungen finden Sie unter [Game Timing und Multicore-Prozessoren.](/windows/desktop/DxTechArts/game-timing-and-multicore-processors)
-   Anwendungen sollten auch [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) aufrufen, um Dateipfade zu ermitteln, da sich einige Ordnernamen in bestimmten Fällen geändert haben. Beispielsweise würde CSIDL \_ PROGRAM \_ FILES "C: \\ Programme(x86)" für eine 32-Bit-Anwendung zurückgeben, die auf einer 64-Bit-Plattform statt "C: Programme" ausgeführt \\ wird. Entwickler müssen bedenken, wie die Umleitungs- und Reflektionsfunktionen des WOW64-Emulators funktionieren.

Darüber hinaus müssen Entwickler vor 16-Bit-Programmen, die sie möglicherweise noch verwenden, vorsichtig sein. WOW64 kann keine 16-Bit-Anwendungen verarbeiten. Dies schließt alte Installationsprogramme und alle MS-DOS-Programme ein.

> [!Note]  
> Die häufigsten Kompatibilitätsprobleme sind Installationsprogramme, die 16-Bit-Code ausführen und keine 64-Bit-Treiber für Kopierschutzschemas haben.

 

Im nächsten Abschnitt werden Probleme im Zusammenhang mit dem Portieren von Code auf 64-Bit native für Entwickler erläutert, die sicherstellen möchten, dass ihre Legacyprogramme auf 64-Bit-Plattformen funktionieren. Es ist auch für Entwickler vorgesehen, die mit der 64-Bit-Programmierung nicht vertraut sind.

## <a name="porting-applications-to-64-bit-platforms"></a>Portieren von Anwendungen auf 64-Bit-Plattformen

Die richtigen Tools und Bibliotheken erleichtern den Übergang von der 32-Bit- zur 64-Bit-Entwicklung. Das DirectX 9 SDK verfügt über Bibliotheken zur Unterstützung von x86- und x64-basierten Projekten. Microsoft Visual Studio 2005 und Visual Studio 2008 unterstützen die Codegenerierung sowohl für x86 als auch für x64. Sie enthält Bibliotheken, die für die Generierung von x64-Code optimiert sind. Es ist jedoch auch erforderlich, dass Entwickler die Visual C-Runtimes mit ihren Anwendungen verteilen. Beachten Sie, dass die Express Editionen von Visual Studio 2005 und Visual Studio 2008 nicht den x64-Compiler enthalten, aber die Standard-, Professional- und Team System-Editionen alle.

Entwickler, die 32-Bit-Plattformen als Ziel verwenden, können sich auf die 64-Bit-Entwicklung vorbereiten, um den Übergang später zu vereinfachen. Beim Kompilieren von 32-Bit-Projekten sollten Entwickler das /Wp64-Flag verwenden, das die Generierung von Warnungen zu Problemen verursacht, die sich auf die Portabilität auswirken. Der Wechsel zu 64-Bit-Tools und -Bibliotheken führt anfangs wahrscheinlich zu vielen neuen Buildfehlern. Daher ist es ratsam, vor dem Wechsel zu einem 64-Bit-Build bitneutrale Tools und Bibliotheken zu wechseln und alle Warnungen zu korrigieren.

Das Ändern von Tools, das Ändern von Bibliotheken und die Verwendung bestimmter Compilerflags reicht jedoch nicht aus. Annahmen in Codierungsstandards müssen neu ausgewertet werden, um sicherzustellen, dass die aktuellen Codierungsstandards keine Portabilitätsprobleme zulassen. Portabilitätsprobleme können das Abschneiden von Zeigern, die Größe und Ausrichtung von Datentypen, die Abhängigkeit von 32-Bit-DLLs, die Verwendung von Legacy-APIs, Assemblycode und alte Binärdateien umfassen.

> [!Note]  
> Visual C++ 2010 enthält die Header stdint.h und cstdint C99, die die Standardportabilitätstypen int32 \_ t, uint32 \_ t, int64 \_ t, uint64 \_ t, intptr \_ t und uintptr \_ t definieren. Die Verwendung dieser Datentypen zusammen mit den Datentypen ptrdiff \_ t und size t kann den unten \_ verwendeten Windows Portabilitätstypen vorzuziehen sein, um die Portabilität von Code zu verbessern.

 

Zu den wichtigsten Portierungsproblemen gehören:

<dl> <dt>

<span id="Pointer_Truncation"></span><span id="pointer_truncation"></span><span id="POINTER_TRUNCATION"></span>**Zeigerkürzung**
</dt> <dd>

Zeiger sind 64-Bit-Zeiger auf einem 64-Bit-Betriebssystem, sodass das Umwandeln von Zeigern auf andere Datentypen zu Kürzungen führen kann und die Zeigerarithmetik zu Beschädigungen führen kann. Die Verwendung des /Wp64-Flags stellt in der Regel eine Warnung zu dieser Art von Problem bereit, aber die Verwendung polymorpher Typen (INT \_ PTR, DWORD \_ PTR, SIZE \_ T, UINT \_ PTR usw.) beim Umwandeln von Zeigertypen ist eine bewährte Methode, um dieses Problem vollständig zu vermeiden. Da Zeiger auf neuen Plattformen 64-Bit-Zeiger sind, sollten Entwickler die Reihenfolge von Zeigern und datentypen in Klassen und Strukturen überprüfen, um die Auffüllung zu reduzieren oder zu entfernen.

</dd> <dt>

<span id="Data_Types_and_Binary_Files"></span><span id="data_types_and_binary_files"></span><span id="DATA_TYPES_AND_BINARY_FILES"></span>**Datentypen und Binärdateien**
</dt> <dd>

Zeiger werden auf einer 64-Bit-Plattform von 32 Bits auf 64 erhöht, andere Datentypen hingegen nicht. Datentypen mit fester Genauigkeit (DWORD32, DWORD64, INT32, INT64, LONG32, LONG64, UINT32, UINT64) können an Stellen verwendet werden, an denen die Größe des Datentyps bekannt sein muss. beispielsweise in einer Binärdateistruktur. Die Änderungen an zeigergröße und Datenausrichtung erfordern eine besondere Behandlung, um die Kompatibilität zwischen 32 Bit und 64 Bit sicherzustellen. Weitere Informationen finden Sie unter [Getting Ready for 64-bit Windows: The New Data Types (Vorbereiten auf 64-Bit-Windows: Die neuen Datentypen](/windows/desktop/WinProg64/the-new-data-types)).

</dd> <dt>

<span id="Older_Win32_APIs_and_Data_Alignment"></span><span id="older_win32_apis_and_data_alignment"></span><span id="OLDER_WIN32_APIS_AND_DATA_ALIGNMENT"></span>**Ältere Win32-APIs und Datenausrichtung**
</dt> <dd>

Einige Win32-APIs sind veraltet und wurden durch neutralere API-Aufrufe wie SetWindowLongPtr anstelle von SetWindowLong ersetzt.

Die Leistungseinbußen für nicht ausgerichtete Zugriffe sind auf x64-Plattformen größer als bei x86-Plattformen. Die TYPE \_ ALIGNMENT(t)- und FIELD \_ OFFSET(t, member)-Makros können verwendet werden, um Ausrichtungsinformationen zu bestimmen, die direkt vom Code verwendet werden können. Durch die richtige Verwendung dieser oben genannten Makros sollten potenzielle nicht ausgerichtete Zugriffsverstoße beseitigt werden.

Weitere Informationen zum TYPE ALIGNMENT-Makro, zum FIELD OFFSET-Makro und allgemeine 64-Bit-Programmierinformationen finden Sie unter \_ \_ [64-Bit-Windows Programming: Migration Tipps: Additional Considerations](/windows/desktop/WinProg64/additional-considerations) and Getting Ready for [64-Bit Windows: Rules for Using Pointers](/windows/desktop/WinProg64/rules-for-using-pointers).

</dd> <dt>

<span id="Assembly_Code"></span><span id="assembly_code"></span><span id="ASSEMBLY_CODE"></span>**Assemblycode**
</dt> <dd>

Inline-Assemblycode wird auf 64-Bit-Plattformen nicht unterstützt und muss ersetzt werden. Änderungen an der Architektur haben möglicherweise Anwendungsengpässe geändert, und C/C++ oder systeminterne Anwendungen können ähnliche Ergebnisse mit code erzielen, der leichter zu lesen ist. Die empfehlenswerteste Methode ist das Umschalten des assembly-Codes auf C oder C++. Systeminterne Eigenschaften können statt Assemblycode verwendet werden, sollten jedoch nur nach der vollständigen Profilerstellung und Analyse verwendet werden.

x87, MMX und 3DNow! -Anweisungssätze sind in 64-Bit-Modi veraltet. Die Anweisungssätze sind aus Gründen der Abwärtskompatibilität für den 32-Bit-Modus weiterhin vorhanden. Um Kompatibilitätsprobleme in Zukunft zu vermeiden, wird jedoch davon abgeraten, sie in aktuellen und zukünftigen Projekten zu verwenden.

</dd> <dt>

<span id="Deprecated_APIs"></span><span id="deprecated_apis"></span><span id="DEPRECATED_APIS"></span>**Veraltete APIs**
</dt> <dd>

Einige ältere DirectX-APIs wurden für native 64-Bit-Anwendungen gelöscht: DirectPlay 4 und früher, DirectDraw 6 und früher, Direct3D 8 und früher sowie DirectInput 7 und früher. Darüber hinaus ist die Kern-API von DirectPerformance für native 64-Bit-Anwendungen verfügbar, aber die Leistungsebene und DirectPerformance Producer sind veraltet.

Visual Studio werden Warnungen zu veralteten Versionen angezeigt, und diese Änderungen sind kein Problem für Entwickler, die die neuesten APIs verwenden.

</dd> </dl>

## <a name="profiling-and-optimization-of-ported-applications"></a>Profilerstellung und Optimierung von portierten Anwendungen

Alle Entwickler müssen ein profiliertes Profil für alle Anwendungen erstellen, die auf neue Architekturen portiert werden. Viele Anwendungen, die auf 64-Bit-Plattformen portiert werden, verfügen über andere Leistungsprofile als ihre 32-Bit-Versionen. Entwickler müssen 64-Bit-Leistungstests ausführen, bevor sie bewerten, was optimiert werden muss. Die gute Nachricht ist, dass viele herkömmliche Optimierungen auf 64-Bit-Plattformen funktionieren. Darüber hinaus können 64-Bit-Compiler auch viele Optimierungen mit der richtigen Verwendung von Compilerflags und Codierungshinweisen ausführen.

Einige Strukturen können ihre internen Datentypen neu anordnen, um Speicherplatz zu sparen und die Zwischenspeicherung zu verbessern. Arrayindizes können in einigen Fällen anstelle eines vollständigen 64-Bit-Zeigers verwendet werden. Das Flag /fp:fast kann die Gleitkommaoptimierung und Vektorisierung verbessern. Die \_ \_ Verwendung von restrict, declspec(restrict) und declspec(noalias) kann dem Compiler helfen, Aliasing aufzulösen und die Verwendung der Registerdatei zu verbessern.

Weitere Informationen zu /fp:fast finden Sie unter [/fp (Floating-Point Verhalten angeben).](/cpp/build/reference/fp-specify-floating-point-behavior)

Weitere Informationen zum \_ \_ Einschränken finden Sie unter [Microsoft-spezifische Modifizierer.](/cpp/cpp/microsoft-specific-modifiers)

Weitere Informationen zu declspec(restrict) finden Sie unter [Bewährte Methoden für die Optimierung.](/cpp/build/optimization-best-practices)

Weitere Informationen zu declspec(noalias) finden Sie unter [ \_ \_ declspec(noalias).](https://msdn.microsoft.com/library/k649tyc7(VS.80).aspx)

## <a name="managed-code-on-a-64-bit-operating-system"></a>Verwalteter Code unter einem 64-Bit-Betriebssystem

Verwalteter Code wird von vielen Spieleentwicklern in der Toolkette verwendet, sodass ein Verständnis des Verhaltens unter einem 64-Bit-Betriebssystem hilfreich sein kann. Verwalteter Code ist anweisungsunabhängig. Wenn Sie also eine verwaltete Anwendung unter einem 64-Bit-Betriebssystem ausführen, kann die Common Language Runtime (CLR) sie entweder als 32-Bit- oder 64-Bit-Prozess ausführen. Standardmäßig führt die CLR verwaltete Anwendungen als 64-Bit aus und sollte problemlos funktionieren. Wenn Ihre Anwendung jedoch von einer nativ 32-Bit-DLL abhängig ist, ist die Anwendung nicht in der 32-Bit-Datei, wenn sie versucht, diese DLL auf aufruft. Ein 64-Bit-Prozess benötigt vollständig 64-Bit-Code, und eine 32-Bit-DLL kann nicht von einem 64-Bit-Prozess aufgerufen werden. Die beste langfristige Lösung besteht in der Kompilierung Ihres nativen Codes als 64-Bit-Version. Eine sehr sinnvolle kurzfristige Lösung besteht jedoch in der einfachen Kennzeichnung Ihrer verwalteten Anwendung als x86-Anwendung, indem Sie das /platform:x86-Buildflag verwenden.

## <a name="performance-implications-of-running-a-64-bit-operating-system"></a>Auswirkungen der Ausführung eines 64-Bit-Betriebssystems auf die Leistung

Da Prozessoren mit AMD64- und Intel 64-Architektur 32-Bit-Anweisungen nativ ausführen können, können sie 32-Bit-Anwendungen mit voller Geschwindigkeit ausführen, auch unter einem 64-Bit-Betriebssystem. Beim Aufrufen von Betriebssystemfunktionen fallen geringfügige Kosten für die Konvertierung von Parametern zwischen 32-Bit und 64-Bit an, aber diese Kosten sind im Allgemeinen vernachlässigbar. Dies bedeutet, dass beim Ausführen von 32-Bit-Anwendungen unter einem 64-Bit-Betriebssystem keine Verlangsamung zu sehen ist.

Wenn Sie Anwendungen als 64-Bit kompilieren, werden die Berechnungen komplizierter. Ein 64-Bit-Programm verwendet 64-Bit-Zeiger, und seine Anweisungen sind etwas größer, sodass der Arbeitsspeicherbedarf leicht erhöht wird. Dies kann zu einem geringfügigen Leistungsabfall führen. Andererseits ist die Doppelt so viele Register und die Möglichkeit, 64-Bit-Ganzzahlberechnungen in einer einzelnen Anweisung durchführen zu können, häufig mehr als kompensieren. Das Ergebnis ist, dass eine 64-Bit-Anwendung möglicherweise etwas langsamer ausgeführt wird als dieselbe Anwendung, die als 32-Bit kompiliert wurde, aber häufig etwas schneller ausgeführt wird.

## <a name="summary"></a>Zusammenfassung

64-Bit-Architekturen ermöglichen Es Entwicklern, die Einschränkungen hinsichtlich der Wiedergabe, des Aussehens, des Sounds und der Wiedergabe von Spielen zu pushen. Der Übergang von der 32-Bit-Programmierung zur 64-Bit-Programmierung ist jedoch nicht trivial. Wenn Sie die Unterschiede zwischen den beiden Verstehen und die neuesten Tools verwenden, kann der Übergang zu 64-Bit-Plattformen einfacher und schneller sein.

Weitere Informationen zur 64-Bit-Programmierung finden Sie im [Visual C++ Developer Center: 64-Bit-Programmierung](https://msdn.microsoft.com/vstudio//aa336463.aspx).

 

 