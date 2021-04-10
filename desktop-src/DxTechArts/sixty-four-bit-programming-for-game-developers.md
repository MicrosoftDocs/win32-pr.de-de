---
title: 64-Bit-Programmierung für Spieleentwickler
description: In diesem Artikel werden Kompatibilitäts-und Portierungsprobleme behandelt und Entwickler bei der Umstellung auf 64-Bit-Plattformen unterstützt.
ms.assetid: 23a7ed41-6637-0607-327e-983b622e9104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12e57ea1b3cc3272ca40465df31a04244d99e68
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039311"
---
# <a name="64-bit-programming-for-game-developers"></a>64-Bit-Programmierung für Spieleentwickler

Prozessor Hersteller liefern ausschließlich 64-Bit-Prozessoren auf Ihren Desktop Computern, und auch die Chip Sätze der meisten Laptop Computer unterstützen x64-Technologien. Es ist wichtig für Spieleentwickler, von den Verbesserungen zu profitieren, die 64-Bit-Prozessoren mit ihren neuen Anwendungen bieten, und um sicherzustellen, dass Ihre früheren Anwendungen ordnungsgemäß auf den neuen Prozessoren und in den 64-Bit-Editionen von Windows Vista und Windows 7 ausgeführt werden. In diesem Artikel werden Kompatibilitäts-und Portierungsprobleme behandelt und Entwickler bei der Umstellung auf 64-Bit-Plattformen unterstützt.

Microsoft verfügt derzeit über die folgenden 64-Bit-Betriebssysteme:

-   Windows Server 2003 Service Pack 1
-   Windows XP Professional x64 Edition (verfügbar für OEMs und Entwickler über MSDN)
-   Windows Vista
-   Windows Server 2008
-   Windows 7
-   Windows Server 2008 R2

> [!Note]  
> Windows Server 2008 R2 ist nur als 64-Bit-Edition verfügbar.

 

-   [Unterschiede im adressierbaren Speicher](#differences-in-addressable-memory)
-   [Angeben von großen Adressen bei der Erstellung](#specifying-large-address-aware-when-building)
-   [Kompatibilität von 32-Bit-Anwendungen auf 64-Bit-Plattformen](#compatibility-of-32-bit-applications-on-64-bit-platforms)
    -   [Mögliche Kompatibilitäts Fehler](#potential-compatibility-pitfalls)
-   [Portieren von Anwendungen auf 64-Bit-Plattformen](#porting-applications-to-64-bit-platforms)
-   [Profilerstellung und Optimierung von portierten Anwendungen](#profiling-and-optimization-of-ported-applications)
-   [Verwalteter Code auf einem 64-Bit-Betriebs System](#managed-code-on-a-64-bit-operating-system)
-   [Auswirkungen der Ausführung eines 64-Bit-Betriebssystems auf die Leistung](#performance-implications-of-running-a-64-bit-operating-system)
-   [Zusammenfassung](#summary)

## <a name="differences-in-addressable-memory"></a>Unterschiede im adressierbaren Speicher

Die meisten Entwickler bemerken zunächst, dass 64-Bit-Prozessoren einen großen Schritt in der Menge an physischem und virtuellem Arbeitsspeicher bereitstellen, der adressiert werden kann.

-   32-Bit-Anwendungen auf 32-Bit-Plattformen können bis zu 2 GB adressieren.
-   32-Bit-Anwendungen, die mit dem/LARGEADDRESSAWARE: Yes-linkerflag auf 32-Bit Windows XP oder Windows Server 2003 mit der/3GB-Startoption erstellt wurden, können bis zu 3 GB adressieren. Dadurch wird der Kernel auf nur 1 GB beschränkt, was dazu führen kann, dass einige Treiber und/oder Dienste fehlschlagen.
-   32-Bit-Anwendungen, die mit dem/LARGEADDRESSAWARE: Yes-linkerflag in den 32-Bit-Editionen von Windows Vista, Windows Server 2008 und Windows 7 erstellt wurden, können den Arbeitsspeicher bis zu dem vom Start Konfigurationsdaten-Element (BCD) angegebenen Wert adressieuserva adressieren. Für "ereuserva" kann ein Wert zwischen 2048 (Standardwert) und 3072 (der mit der von der/3GB-Startoption unter Windows XP konfigurierten Speichermenge übereinstimmt) festgelegt werden. Der Rest von 4 GB wird dem Kernel zugewiesen und kann zu fehlerhaften Treiber-und Dienst Konfigurationen führen.

    Weitere Informationen zu BCD finden Sie unter [Startkonfigurationsdaten](https://msdn.microsoft.com/library/aa362692.aspx) auf MSDN.

-   32-Bit-Anwendungen auf 64-Bit-Plattformen können bis zu 2 GB oder bis zu 4 GB mit dem/LARGEADDRESSAWARE: Yes-linkerflag adressieren.
-   64-Bit-Anwendungen verwenden 43 Bits für die Adressierung, die eine virtuelle Adresse von 8 TB für Anwendungen und 8 TB für den Kernel reserviert.

Über den Arbeitsspeicher hinaus werden 64-Bit-Anwendungen, die Speicher Abbild Datei-e/a nutzen, stark vom erweiterten virtuellen Adressraum profitieren. Die 64-Bit-Architektur hat auch eine verbesserte Gleit Komma Leistung und ein schnelleres übergeben von Parametern. 64-Bit-Prozessoren haben die doppelte Anzahl von Registern, sowohl von "General Purpose"-als auch von Streaming SIMD Extensions (SSE)-Typen sowie von Unterstützung für SSE-und SSE2-Anweisungs Sätze. viele 64-Bit-Prozessoren unterstützen sogar SSE3-Anweisungs Sätze.

## <a name="specifying-large-address-aware-when-building"></a>Angeben von großen Adressen bei der Erstellung

Es empfiehlt sich, bei der Erstellung von 32-Bit-Anwendungen mithilfe des Linkerflags/LARGEADDRESSAWARE auch dann, wenn die Anwendung nicht für eine 64-Bit-Plattform vorgesehen ist, die Groß-und klein zulegung zu unterstützen, da die Vorteile ohne Kosten entstehen. Wie bereits erläutert, ermöglicht das Aktivieren dieses Flags für einen Build einem 32-Bit-Programm den Zugriff auf mehr Arbeitsspeicher mit speziellen Startoptionen für ein 32-Bit-Betriebssystem oder ein 64-Bit-Betriebssystem. Allerdings müssen Entwickler darauf achten, dass keine Zeiger Annahmen getroffen werden, wie z. b., wenn die High-Bit-Version niemals in einem 32-Bit-Zeiger festgelegt ist. Im Allgemeinen empfiehlt es sich, das/LARGEADDRESSAWARE-Flag zu aktivieren.

32-Bit-Anwendungen, die große Adressen unterstützen, können zur Laufzeit ermitteln, wie viel gesamter virtueller Adressraum mit der aktuellen Betriebssystem Konfiguration verfügbar ist, indem Sie [**GlobalMemoryStatus usex**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex)aufrufen. Das ulltotalvirtual-Ergebnis reicht von 2147352576 bytes (2 GB) bis 4294836224 bytes (4 GB). Werte, die größer als 3221094400 (3 GB) sind, können nur in 64-Bit-Editionen von Windows abgerufen werden. Wenn z. b. "ersetzeuserva" den Wert "2560" hat, ist das Ergebnis "ulltotalvirtual" mit einem Wert von 2684223488 bytes.

## <a name="compatibility-of-32-bit-applications-on-64-bit-platforms"></a>Kompatibilität von 32-Bit-Anwendungen auf 64-Bit-Plattformen

64-Bit-Windows-Betriebssysteme sind binär kompatibel mit der ia32-Architektur, und die meisten APIs, die von 32-Bit-Anwendungen verwendet werden, sind über das Windows 32-Bit unter Windows 64-Bit-Emulator WOW64 verfügbar. Mit WOW64 wird sichergestellt, dass diese APIs wie beabsichtigt funktionieren.

WOW64 verfügt über eine Ausführungs Ebene, die das Marshalling von 32-Bit-Daten behandelt. WOW64 umleitet dll-Datei Anforderungen, leitet einige registrierungsbranches für 32-Bit-Anwendungen um und reflektiert einige Registrierungs branches für 32-und 64-Bit-Anwendungen.

Weitere Informationen zu WOW64 finden Sie unter [WOW64-Implementierungs Details](/windows/desktop/WinProg64/wow64-implementation-details) auf MSDN. Bewährte Methoden zum Entwickeln von Anwendungen, die auf WOW64 ausgeführt werden, finden Sie unter [Best Practices for WOW64](https://www.microsoft.com/whdc/system/platform/64bit/WoW64_bestprac.mspx) on Windows Hardware Developer Central.

### <a name="potential-compatibility-pitfalls"></a>Mögliche Kompatibilitäts Fehler

Die meisten Anwendungen, die für eine 32-Bit-Plattform entwickelt wurden, können ohne Probleme auf einer 64-Bit-Plattform ausgeführt werden. Einige Anwendungen können Probleme haben, die Folgendes umfassen können:

-   Alle Treiber für die 64-Bit-Editionen von Windows-Betriebssystemen müssen 64-Bit-Versionen sein. Das verlangen neuer 64-Bit-Treiber hat Auswirkungen auf Kopierschutz Schemas, die auf alten Treibern basieren. Beachten Sie, dass Kernelmodustreiber mit Authenticode signiert werden müssen, um von den 64-Bit-Editionen von Windows geladen zu werden.
-   64-Bit-Prozesse können keine 32-Bit-DLLs laden, und 32-Bit-Prozesse können keine 64-Bit-DLLs laden. Entwickler müssen sicherstellen, dass 64-Bit-Versionen von Drittanbieter-DLLs verfügbar sind, bevor Sie mit der Entwicklung fortfahren. Wenn Sie in einem 64-Bit-Prozess eine 32-Bit-DLL verwenden müssen, können Sie die Windows-prozessübergreifende Kommunikation (Inter-Process Communication, IPC) verwenden. COM-Komponenten können auch Out-of-Process-Server verwenden und Marshalling, um zwischen Grenzen zu kommunizieren. Dies kann jedoch zu einer Leistungs Einbuße führen.
-   Viele x64-Prozessoren sind auch Multi-Core-Prozessoren, und Entwickler müssen testen, wie sich dies auf Ihre Legacy Anwendungen auswirkt. Weitere Informationen zu Multi-Core-Prozessoren und den Auswirkungen auf Spiele Anwendungen finden Sie unter [Game Timing und Multicore-Prozessoren](/windows/desktop/DxTechArts/game-timing-and-multicore-processors).
-   Anwendungen sollten auch [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) aufrufen, um Dateipfade zu ermitteln, da einige Ordnernamen in bestimmten Fällen geändert wurden. CSIDL- \_ Programm \_ Dateien würden z. b. "c: \\ Program Files (x86)" für eine 32-Bit-Anwendung, die auf einer 64-Bit-Plattform ausgeführt wird, anstelle von "c: Program Files" zurückgeben \\ . Entwickler müssen berücksichtigen, wie die Umleitungs-und reflektionserfähigkeiten des WOW64-Emulators funktionieren.

Außerdem müssen Entwickler mit 16-Bit-Programmen gewarnt werden, die Sie möglicherweise weiterhin verwenden. WOW64 kann keine 16-Bit-Anwendungen verarbeiten. Dies schließt alte Installationsprogramme und alle MS-DOS-Programme ein.

> [!Note]  
> Die häufigsten Kompatibilitätsprobleme sind Installationsprogramme, die 16-Bit-Code ausführen und nicht über 64-Bit-Treiber für Kopierschutz Schemas verfügen.

 

Im nächsten Abschnitt werden Probleme im Zusammenhang mit dem Portieren von Code auf 64-Bit-System eigen für Entwickler erläutert, die sicherstellen möchten, dass Ihre Legacy Programme auf 64-Bit-Plattformen Dies gilt auch für Entwickler, die mit der 64-Bit-Programmierung nicht vertraut sind.

## <a name="porting-applications-to-64-bit-platforms"></a>Portieren von Anwendungen auf 64-Bit-Plattformen

Wenn Sie über die richtigen Tools und Bibliotheken verfügen, wird der Übergang von der 32-Bit-zu 64-Bit-Entwicklung erleichtert. Das DirectX 9 SDK verfügt über Bibliotheken zur Unterstützung von x86-und x64-basierten Projekten. Microsoft Visual Studio 2005 und Visual Studio 2008 unterstützen die Codegenerierung für x86 und x64, und Sie verfügen über Bibliotheken, die für die Generierung von x64-Code optimiert sind. Es ist jedoch auch erforderlich, dass Entwickler die Visual C-Laufzeiten mit Ihren Anwendungen verteilen. Beachten Sie, dass die Express-Editionen von Visual Studio 2005 und Visual Studio 2008 nicht den x64-Compiler enthalten, sondern die Standard-, Professional-und Team System-Editionen.

Entwickler, die auf 32-Bit-Plattformen abzielen, können sich auf die 64-Bit-Entwicklung vorbereiten, um den Übergang später zu vereinfachen. Beim Kompilieren von 32-Bit-Projekten sollten Entwickler das/Wp64-Flag verwenden, das die Generierung von Warnungen zu Problemen verursacht, die die Portabilität beeinflussen. Wenn Sie zu 64-Bit-Tools und-Bibliotheken wechseln, werden anfänglich wahrscheinlich viele neue Buildfehler generiert. Daher empfiehlt es sich, bitneutrale Tools und Bibliotheken zu wechseln und alle Warnungen zu korrigieren, bevor Sie zu einem 64-Bit-Build wechseln.

Das Ändern von Tools, das Ändern von Bibliotheken und die Verwendung bestimmter Compilerflags reicht jedoch nicht aus. Annahmen in Codierungsstandards müssen neu ausgewertet werden, um sicherzustellen, dass die aktuellen Codierungsstandards keine Portabilitäts Probleme zulassen. Portabilitäts Probleme können das Abschneiden von Zeigern, die Größe und die Ausrichtung von Datentypen, die Abhängigkeit von 32-Bit-DLLs, die Verwendung von Legacy-APIs, Assemblycode und alte Binärdateien einschließen.

> [!Note]  
> Visual C++ 2010 enthält die "stdint. h"-und "cstdint C99"-Header, die die standardportabilitäts Typen definieren Int32 \_ t, UInt32 \_ t, Int64 \_ t, UInt64 \_ t, IntPtr \_ t und UIntPtr \_ t. Die Verwendung dieser Datentypen mit den standardmäßigen ptrdiff \_ t-und size \_ t-Datentypen ist möglicherweise für die unten verwendeten Windows-portabationstypen zum Verbessern der Portabilität von Code vorzuziehen.

 

Wichtige Probleme bei der Portierung sind u. a.:

<dl> <dt>

<span id="Pointer_Truncation"></span><span id="pointer_truncation"></span><span id="POINTER_TRUNCATION"></span>**Abschneiden von Zeigern**
</dt> <dd>

Zeiger sind 64-Bit-Werte auf einem 64-Bit-Betriebssystem, sodass das Umwandeln von Zeigern auf andere Datentypen zu einem Abschneiden führen kann und Zeigerarithmetik zu Beschädigungen führen kann. Die Verwendung des/Wp64-Flags stellt in der Regel eine Warnung zu dieser Art von Problem dar, aber die Verwendung von polymorphen Typen (int \_ ptr, DWORD \_ ptr, size \_ T, uint \_ ptr usw.) ist eine bewährte Vorgehensweise, um dieses Problem zu vermeiden. Da Zeiger auf neuen Plattformen 64-Bit sind, sollten Entwickler die Reihenfolge von Zeigern und die Datentypen in Klassen und Strukturen überprüfen, um die Auffüll Zeichen zu reduzieren oder auszuschließen.

</dd> <dt>

<span id="Data_Types_and_Binary_Files"></span><span id="data_types_and_binary_files"></span><span id="DATA_TYPES_AND_BINARY_FILES"></span>**Datentypen und Binärdateien**
</dt> <dd>

Während Zeiger auf einer 64-Bit-Plattform von 32 Bits auf 64 steigen, sind andere Datentypen nicht. Datentypen mit fester Genauigkeit (DWORD32, DWORD64, Int32, Int64, LONG32, LONG64, UInt32, UINT64) können an Stellen verwendet werden, an denen die Größe des Datentyps bekannt sein muss. beispielsweise in einer binären Dateistruktur. Die Änderungen an der Zeiger Größe und der Daten Ausrichtung erfordern eine spezielle Behandlung, um die 32-Bit-zu-64-Bit-Kompatibilität sicherzustellen. Weitere Informationen finden Sie unter [vorbereiten für 64-Bit-Windows: die neuen Datentypen](/windows/desktop/WinProg64/the-new-data-types).

</dd> <dt>

<span id="Older_Win32_APIs_and_Data_Alignment"></span><span id="older_win32_apis_and_data_alignment"></span><span id="OLDER_WIN32_APIS_AND_DATA_ALIGNMENT"></span>**Ältere Win32-APIs und Daten Ausrichtung**
</dt> <dd>

Einige Win32-APIs wurden als veraltet markiert und durch komplexere API-Aufrufe, wie z. b. setwindowlongptr anstelle von SetWindowLong, ersetzt.

Die Leistungseinbußen bei nicht ausgerichteten Zugriffen sind auf der x64-Plattform höher als auf einer x86-Plattform. Die \_ typausrichtung (t) und die Feld \_ Offset-Makros (t, Member) können verwendet werden, um Ausrichtungs Informationen zu bestimmen, die direkt im Code verwendet werden können. Die korrekte Verwendung dieser oben genannten Makros sollte mögliche nicht ausgerichtete Zugriffs Strafen vermeiden.

Weitere Informationen zum Type \_ Alignment-Makro, das Field \_ Offset-Makro und allgemeine 64-Bit-Programmierinformationen finden Sie unter [64-Bit-Windows-Programmierung: Migrations Tipps: Weitere Überlegungen](/windows/desktop/WinProg64/additional-considerations) und vorbereiten [für 64-Bit-Windows: Regeln für die Verwendung von Zeigern](/windows/desktop/WinProg64/rules-for-using-pointers).

</dd> <dt>

<span id="Assembly_Code"></span><span id="assembly_code"></span><span id="ASSEMBLY_CODE"></span>**Assemblycode**
</dt> <dd>

Inline-Assemblycode wird auf 64-Bit-Plattformen nicht unterstützt und muss ersetzt werden. Änderungen an der Architektur haben möglicherweise Anwendungs Engpässe geändert, und C/C++ oder intrinsische Funktionen können ähnliche Ergebnisse mit Code erzielen, der leichter lesbar ist. Die empfohlene Vorgehensweise besteht darin, den gesamten Assemblycode in C oder C++ zu ändern. Intrinsie können anstelle von Assemblycode verwendet werden, sollten aber nur nach der vollständigen Profilerstellung und Analyse verwendet werden.

X87, MMX und 3dnow! Anweisungs Sätze werden im 64-Bit-Modus als veraltet markiert. Die Anweisungs Sätze sind zur Abwärtskompatibilität für den 32-Bit-Modus weiterhin vorhanden. um Kompatibilitätsprobleme in Zukunft zu vermeiden, wird jedoch davon abgeraten, die Verwendung in aktuellen und zukünftigen Projekten zu vermeiden.

</dd> <dt>

<span id="Deprecated_APIs"></span><span id="deprecated_apis"></span><span id="DEPRECATED_APIS"></span>**Veraltete APIs**
</dt> <dd>

Einige ältere DirectX-APIs wurden für Native 64-Bit-Anwendungen gelöscht: DirectPlay 4 und früher, DirectDraw 6 und früher, Direct3D 8 und früher und DirectInput 7 und früher. Außerdem ist die Kern-API von DirectMusic für Native 64-Bit-Anwendungen verfügbar, aber die Leistungs Ebene und der DirectMusic-Producer sind veraltet.

Visual Studio gibt veraltete Warnungen aus, und diese Änderungen sind kein Problem für Entwickler, die die neuesten APIs verwenden.

</dd> </dl>

## <a name="profiling-and-optimization-of-ported-applications"></a>Profilerstellung und Optimierung von portierten Anwendungen

Alle Entwickler müssen Profile für alle Anwendungen neu erstellen, die in neue Architekturen portiert werden. Viele Anwendungen, die auf 64-Bit-Plattformen portiert werden, haben unterschiedliche Leistungsprofile von ihren 32-Bit-Versionen. Entwickler müssen 64-Bit-Leistungstests ausführen, bevor Sie bewerten, was optimiert werden muss. Die gute Nachricht ist, dass viele herkömmliche Optimierungen auf 64-Bit-Plattformen funktionieren. Außerdem können 64-Bit-Compiler auch viele Optimierungen mit der korrekten Verwendung von Compilerflags und Codierungs hinweisen ausführen.

Einige Strukturen können Ihre internen Datentypen neu angeordnet haben, um Speicherplatz zu sparen und das Zwischenspeichern zu verbessern. Array Indizes können in einigen Fällen anstelle eines vollständigen 64-Bit-Zeigers verwendet werden. Das Flag "/fp: fast" kann die Gleit Komma Optimierung und die Vektorisierung verbessern. Mithilfe \_ \_ von einschränken, declspec (einschränken) und declspec (noalias) kann der Compiler das Aliasing auflösen und die Verwendung der Register Datei verbessern.

Weitere Informationen zu/FP finden Sie unter [/fp (Floating-Point Verhalten angeben)](/cpp/build/reference/fp-specify-floating-point-behavior).

Weitere Informationen zur Einschränkung finden Sie \_ \_ unter [Microsoft-spezifische Modifizierer](/cpp/cpp/microsoft-specific-modifiers).

Weitere Informationen zu declspec (einschränken) finden Sie unter [bewährte Methoden](/cpp/build/optimization-best-practices)für die Optimierung.

Weitere Informationen zu declspec (noalias) finden Sie unter [ \_ \_ declspec (noalias)](https://msdn.microsoft.com/library/k649tyc7(VS.80).aspx).

## <a name="managed-code-on-a-64-bit-operating-system"></a>Verwalteter Code auf einem 64-Bit-Betriebs System

Verwalteter Code wird von vielen Spiel Entwicklern in der Toolkette verwendet. Daher kann es hilfreich sein, sich mit dem Verhalten eines 64-Bit-Betriebssystems vertraut zu machen. Verwalteter Code ist Weisungs Satz neutral. Wenn Sie also eine verwaltete Anwendung auf einem 64-Bit-Betriebssystem ausführen, kann die Common Language Runtime (CLR) Sie entweder als 32-Bit-oder 64-Bit-Prozess ausführen. Standardmäßig führt die CLR verwaltete Anwendungen als 64-Bit-Version aus, und Sie sollten problemlos problemlos funktionieren. Wenn die Anwendung jedoch von einer dll abhängig ist, die systemeigene 32-Bit-Version ist, schlägt die Anwendung fehl, wenn versucht wird, diese DLL aufzurufen. Ein 64-Bit-Prozess erfordert vollständigen 64-Bit-Code, und eine 32-Bit-DLL kann nicht von einem 64-Bit-Prozess aufgerufen werden. Die beste langfristige Lösung besteht darin, den nativen Code auch als 64-Bit-Version zu kompilieren. eine absolut sinnvolle kurzfristige Lösung besteht jedoch darin, die verwaltete Anwendung einfach nur für x86 zu markieren, indem das/Platform: x86-Buildflag verwendet wird.

## <a name="performance-implications-of-running-a-64-bit-operating-system"></a>Auswirkungen der Ausführung eines 64-Bit-Betriebssystems auf die Leistung

Da Prozessoren mit amd64-und Intel 64-Architektur die 32-Bit-Anweisungen nativ ausführen können, können Sie 32-Bit-Anwendungen mit voller Geschwindigkeit ausführen, auch bei einem 64-Bit-Betriebssystem. Beim Aufrufen von Betriebssystemfunktionen gibt es einen geringfügigen Aufwand für das Umrechnen von Parametern zwischen 32-Bit und 64-Bit. diese Kosten sind jedoch im allgemeinen unerheblich. Dies bedeutet, dass beim Ausführen von 32-Bit-Anwendungen auf einem 64-Bit-Betriebssystem keine Verlangsamung angezeigt werden sollte.

Wenn Sie Anwendungen als 64-Bit-Version kompilieren, werden die Berechnungen komplizierter. Ein 64-Bit-Programm verwendet 64-Bit-Zeiger, und die Anweisungen sind etwas größer, sodass die Arbeitsspeicher Anforderungen geringfügig zunehmen. Dies kann zu einem geringfügigen Leistungsabfall führen. Andererseits ist die Verwendung von doppelt so vielen Registern und die Möglichkeit, 64-Bit-ganz Zahl Berechnungen in einer einzigen Anweisung auszuführen, häufig länger als kompensiert. Das Ergebnis ist, dass eine 64-Bit-Anwendung möglicherweise langsamer ausgeführt wird, als die gleiche Anwendung, die als 32-Bit kompiliert wurde, aber oft schneller ausgeführt wird.

## <a name="summary"></a>Zusammenfassung

64-Bit-Architekturen ermöglichen es Entwicklern, die Einschränkungen für das Aussehen, den Sound und die Wiedergabe von spielen zu übertragen. Die Umstellung von der 32-Bit-Programmierung auf die 64-Bit-Programmierung ist jedoch nicht trivial. Wenn Sie die Unterschiede zwischen den beiden und den neuesten Tools verstehen, kann der Übergang zu 64-Bit-Plattformen einfacher und schneller sein.

Weitere Informationen zur 64-Bit-Programmierung finden Sie unter [Visual C++ Developer Center: 64-Bit-Programmierung](https://msdn.microsoft.com/vstudio//aa336463.aspx).

 

 