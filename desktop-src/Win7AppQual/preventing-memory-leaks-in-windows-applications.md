---
description: Erfahren Sie, wie Sie Speicherverlusten in Windows-Anwendungen für Windows 7- und Windows Server 2008 R2-Plattformen verhindern.
ms.assetid: c5dedcab-3e6f-433f-95de-d741321c683e
title: Verhindern von Speicherverlusten in Windows Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef336c52ff4869ae9947b898e8a42c480be58054315de0180ec6a18f8c917f51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994795"
---
# <a name="preventing-memory-leaks-in-windows-applications"></a>Verhindern von Speicherverlusten in Windows Anwendungen

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** – Windows 7  
**Server** – Windows Server 2008 R2  

## <a name="description"></a>BESCHREIBUNG

Speicherverlusten sind eine Klasse von Fehlern, bei denen die Anwendung keinen Arbeitsspeicher mehr frei gibt, wenn sie nicht mehr benötigt wird. Im Laufe der Zeit wirken sich Speicherverlusten sowohl auf die Leistung der jeweiligen Anwendung als auch des Betriebssystems aus. Ein großer Leck kann aufgrund übermäßiger Paging zu inakzeptablen Antwortzeiten führen. Schließlich kommt es bei der Anwendung und anderen Teilen des Betriebssystems zu Ausfällen.

Windows bei der Prozessbeendigung den gesamten von der Anwendung zugewiesenen Arbeitsspeicher frei, sodass anwendungen mit kurzer Ausführung keine erheblichen Auswirkungen auf die Gesamtleistung des Systems haben. Allerdings können Lecks in Prozessen mit langer Laufzeit wie Diensten oder sogar Explorer-Plug-Ins die Systemzuverlässigkeit stark beeinflussen und den Benutzer zwingen, Windows neu zu starten, um das System wieder nutzbar zu machen.

Anwendungen können Speicher in ihrem Namen auf mehrere Weisen zuordnen. Jede Art von Zuordnung kann zu einem Leck führen, wenn sie nach der Verwendung nicht wieder frei wird. Im Folgenden finden Sie einige Beispiele für allgemeine Zuordnungsmuster:

-   Heapspeicher über die [**HeapAlloc-Funktion**](/windows/win32/api/heapapi/nf-heapapi-heapalloc) oder die entsprechenden C/C++-Laufzeitentsprechungen **malloc** oder **new**
-   Direkte Zuordnungen vom Betriebssystem über die [**VirtualAlloc-Funktion.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
-   Kernelhandles, die über Kernel32-APIs wie [**CreateFile,**](/windows/win32/api/fileapi/nf-fileapi-createfilea) [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)oder [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)erstellt wurden, halten Kernelspeicher im Namen der Anwendung.
-   Über User32- und Gdi32-APIs erstellte GDI- und USER-Handles (standardmäßig verfügt jeder Prozess über ein Kontingent von 10.000 Handles).

## <a name="best-practices"></a>Empfehlungen

Die Überwachung des Ressourcenverbrauchs Ihrer Anwendung im Laufe der Zeit ist der erste Schritt bei der Erkennung und Diagnose von Speicherverlusten. Verwenden Windows Task-Manager, und fügen Sie die folgenden Spalten hinzu: "Commit Size", "Handles", "User Objects" und "GDI Objects". Auf diese Weise können Sie eine Baseline für Ihre Anwendung erstellen und die Ressourcennutzung im Laufe der Zeit überwachen.

![Screenshot: Seite "Prozesse" in Windows Task-Manager.](images/preventingmemoryleaks-windowstaskmanager.gif)

Die folgenden Microsoft-Tools bieten ausführlichere Informationen und können helfen, Lecks für die verschiedenen Zuordnungstypen in Ihrer Anwendung zu erkennen und zu diagnostizieren:

-   Leistungsmonitor und Ressourcenmonitor sind Teil von Windows 7 und können die Ressourcennutzung im Laufe der Zeit überwachen und graphen.
-   Die neueste Version von Application Verifier heap leaks on Windows 7
-   UMDH, das Teil der Debugtools für Windows ist, analysiert die Heapspeicherzuordnungen für einen bestimmten Prozess und kann dabei helfen, Lecks und andere ungewöhnliche Verwendungsmuster zu finden.
-   Xperf ist ein anspruchsvolles Leistungsanalysetool mit Unterstützung für Heapzuordnungs-Ablaufverfolgungen.
-   CRT Debug Heap verfolgt Heapzuordnungen nach und kann ihnen helfen, eigene Heapdebugfeatures zu erstellen.

Bestimmte Codierungs- und Entwurfsmethoden können die Anzahl von Lecks in Ihrem Code begrenzen.

-   Verwenden Sie intelligente Zeiger in C++-Code sowohl für Heapzuordnungen als auch für Win32-Ressourcen wie kernel **HANDLE** s. Die C++-Standardbibliothek stellt die **auto \_ ptr-Klasse** für Heapzuordnungen zur Verfügung. Für andere Zuordnungstypen müssen Sie Eigene Klassen schreiben. Die ATL-Bibliothek bietet einen großen Satz von Klassen für die automatische Ressourcenverwaltung für Heapobjekte und Kernelhandles.
-   Verwenden Sie systeminterne Compilerfeatures wie **\_ com \_ ptr \_ t,** um Ihre COM-Schnittstellenzeker in "intelligente Zeiger" zu kapseln und die Verweiszählung zu unterstützen. Es gibt ähnliche Klassen für andere COM-Datentypen: **\_ bstr \_ t** und **\_ variant \_ t**
-   Überwachen Sie die ungewöhnliche Speicherauslastung Ihres .NET-Codes. Verwalteter Code ist nicht ungnicht gegen Speicherverlusten. Informationen [zum Aufspüren von GC-Lecks](/archive/blogs/ricom/) finden Sie unter "Nachverfolgen verwalteter Speicherverlusten".
-   Beachten Sie Leak-Muster im clientseitigen Webcode. Zirkelverweise zwischen COM-Objekten und Skript-Engines wie JScript können große Lecks in Webanwendungen verursachen. ["Understanding and Solving Internet Explorer Leak Patterns"](/previous-versions/ms976398(v=msdn.10)) enthält weitere Informationen zu diesen Arten von Lecks. Sie können die JavaScript-Speicherverlusterkennung verwenden, um Speicherverlusten in Ihrem Code zu debuggen. Während Windows Internet Explorer 8, der mit Windows 7 veröffentlicht wird, die meisten dieser Probleme entschärft, sind ältere Browser weiterhin anfällig für diese Fehler.
-   Vermeiden Sie die Verwendung mehrerer Exitpfade aus einer Funktion. Zuordnungen, die Variablen im Funktionsumfang zugewiesen sind, sollten in einem bestimmten Block am Ende der Funktion frei werden.
-   Verwenden Sie keine Ausnahmen in Ihrem Code, ohne alle lokalen Variablen in Funktionen frei zu machen. Wenn Sie native Ausnahmen verwenden, geben Sie alle Ihre Zuordnungen innerhalb des \_ \_ finally-Blocks frei. Wenn Sie C++-Ausnahmen verwenden, müssen alle Ihre Heap- und Handlezuordnungen in intelligente Zeiger umschlossen werden.
-   Verwerfen oder erneut initialisieren Sie ein [**PROPVARIANT-Objekt**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) nicht, ohne die [**PropVariantClear-Funktion aufrufen zu**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear) müssen.

## <a name="links-to-resources"></a>Links zu Ressourcen

*Allgemeine Zuordnungsmuster:*

-   [**Heapzuordnungsfunktion**](/windows/win32/api/heapapi/nf-heapapi-heapalloc)
-   [**Speicherzuordnungsfunktion**](https://msdn.microsoft.com/library/6ewkz86d(v=VS.71).aspx)
-   [**New-Operator (C++)**](https://msdn.microsoft.com/library/kewsb8ba(v=VS.71).aspx)
-   [**Virtuelle Zuordnungsfunktion**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
-   [Kernelobjekte](../sysinfo/kernel-objects.md)
-   [GDI-Objekthandles](../sysinfo/gdi-objects.md)
-   [Benutzeroberfläche Objekthandles](../sysinfo/user-objects.md)

*Microsoft-Tools:*

-   [Application Verifier](application-verifier.md)
-   [Debuggingtools für Windows](/windows-hardware/drivers/debugger/)
-   [Speicherabbild-Heap im Benutzermodus](/windows-hardware/drivers/debugger/umdh)
-   [Trace Capture, Processing, and Analysis Tool](https://msdn.microsoft.com/performance/cc825801.aspx)
-   [CRT-Debug heap](/visualstudio/debugger/crt-debug-heap-details?view=vs-2015)

*Weitere Links:*

-   [**auto \_ ptr-Klasse**](https://msdn.microsoft.com/library/ew3fk483(v=VS.71).aspx)
-   [Active Template Library (ATL)-Speicherklassen](https://msdn.microsoft.com/library/44yh1z4f(v=VS.71).aspx)
-   [**\_com \_ ptr \_ t Object**](https://msdn.microsoft.com/library/417w8b3b(v=VS.71).aspx)
-   [**\_bstr \_ t-Klasse**](https://msdn.microsoft.com/library/zthfhkd6(v=VS.71).aspx)
-   [**\_variant \_ yt-Klasse**](https://msdn.microsoft.com/library/x295h94e(v=VS.71).aspx)
-   ["Nachverfolgen verwalteter Speicherverlusten"](/archive/blogs/ricom/)
-   ["Understanding and Solving Internet Explorer Leak Patterns" (Verstehen und Lösen von Internet Explorer Verlustmustern)](/previous-versions/ms976398(v=msdn.10))
-   ["JavaScript Memory Leak Detector"](/archive/blogs/gpde/new-javascript-memory-leak-detector-from-our-team)
-   [Entschärfung von Zirkelspeicherverlust (in Browsern):](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/dd361842(v=vs.85))
-   [**try-finally-Anweisung**](https://msdn.microsoft.com/library/yb3kz605(v=VS.71).aspx)
-   [**PROPVARIANT-Struktur**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)
-   [**PropVariantClear-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)

 

 
