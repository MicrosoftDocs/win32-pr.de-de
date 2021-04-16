---
description: Erfahren Sie, wie Sie Speicher Verluste in Windows-Anwendungen für Windows 7-und Windows Server 2008 R2-Plattformen vermeiden.
ms.assetid: c5dedcab-3e6f-433f-95de-d741321c683e
title: Verhindern von Speicher Verlusten in Windows-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e973da19d075ac94824df340d1741fd9cefb3486
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "104567224"
---
# <a name="preventing-memory-leaks-in-windows-applications"></a>Verhindern von Speicher Verlusten in Windows-Anwendungen

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** -Windows 7  
**Server** -Windows Server 2008 R2  

## <a name="description"></a>BESCHREIBUNG

Speicher Verluste sind eine Klasse von Fehlern, bei denen die Anwendung keinen Arbeitsspeicher mehr freigeben kann, wenn Sie nicht mehr benötigt wird. Im Laufe der Zeit wirken sich Speicher Verluste sowohl auf die Leistung der jeweiligen Anwendung als auch auf das Betriebssystem aus. Ein großer Ausfall kann zu unzulässigen Antwortzeiten aufgrund von übermäßigem Paging führen. Letztendlich treten bei der Anwendung und anderen Teilen des Betriebssystems Fehler auf.

Windows gibt den gesamten Arbeitsspeicher frei, der von der Anwendung bei Beendigung des Prozesses belegt wird, sodass sich Anwendungen mit kurzer Laufzeit nicht erheblich auf die Gesamtleistung des Systems auswirken. Verluste in Prozessen mit langer Ausführungszeit, wie Dienste oder sogar Explorer-Plug-ins, können sich jedoch erheblich auf die Zuverlässigkeit des Systems auswirken und erzwingen möglicherweise, dass der Benutzer Windows neu startet, damit das System wiederverwendbar ist.

Anwendungen können Arbeitsspeicher in Ihrem Auftrag auf mehrfache Weise zuweisen. Jeder Zuordnungstyp kann zu einem Leck führen, wenn er nach der Verwendung nicht freigegeben wird. Im folgenden finden Sie einige Beispiele für allgemeine Zuordnungs Muster:

-   Heap Speicher über die [**heapbelegc**](/windows/win32/api/heapapi/nf-heapapi-heapalloc) -Funktion oder deren C/C++-Lauf Zeit Entsprechungen **malloc** oder **New**
-   Direkte Zuweisungen vom Betriebssystem über die [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) -Funktion.
-   Kernel Handles, die über kernel32-APIs erstellt werden, wie z. b. " [**kreatefile**](/windows/win32/api/fileapi/nf-fileapi-createfilea)", " [**forateevent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)" oder " [**foratethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)"
-   GDI-und Benutzer Handles, die über User32-und gdi32-APIs erstellt wurden (Standardmäßig verfügt jeder Prozess über ein Kontingent von 10.000 Handles)

## <a name="best-practices"></a>Bewährte Methoden

Das Überwachen des Ressourcenverbrauchs Ihrer Anwendung im Zeitverlauf ist der erste Schritt bei der Erkennung und Diagnose von Speicher Verlusten. Verwenden Sie den Windows Task-Manager, und fügen Sie die folgenden Spalten hinzu: "commitsize", "Handles", "User Objects" und "GDI Objects". Auf diese Weise können Sie eine Baseline für Ihre Anwendung einrichten und die Ressourcennutzung über einen bestimmten Zeitraum überwachen.

![Screenshot, der die Seite "Prozesse" im Windows Task-Manager anzeigt.](images/preventingmemoryleaks-windowstaskmanager.gif)

Die folgenden Microsoft-Tools bieten ausführlichere Informationen und können Ihnen helfen, Verluste für die verschiedenen Zuordnungs Typen in Ihrer Anwendung zu erkennen und zu diagnostizieren:

-   System Monitor und Ressourcenmonitor sind Teil von Windows 7 und können die Ressourcenverwendung über einen bestimmten Zeitraum überwachen und überwachen.
-   Die neueste Version von Application Verifier kann Heap Lecks unter Windows 7 diagnostizieren.
-   Mit dem in den Debuggingtools für Windows vorhandenen Umschlag werden die Heap Speicher Belegungen für einen bestimmten Prozess analysiert, und es können Verluste und andere ungewöhnliche Verwendungs Muster gefunden werden.
-   XPerf ist ein anspruchsvolles Leistungsanalyse Tool mit Unterstützung für Heap Zuordnungs Ablauf Verfolgungen.
-   CRT-Debugheap verfolgt Heap Zuordnungen und kann helfen, eigene Heap-Debugging-Features zu erstellen

Bestimmte Codierungs-und Entwurfsverfahren können die Anzahl der Lecks in Ihrem Code einschränken.

-   Verwenden Sie intelligente Zeiger in C++-Code sowohl für Heap Zuweisungen als auch für Win32-Ressourcen wie Kernel **handle** s. Die C++-Standard Bibliothek stellt die **automatische \_ ptr** -Klasse für Heap Zuweisungen bereit. Bei anderen Zuordnungs Typen müssen Sie eigene Klassen schreiben. Die ATL-Bibliothek stellt einen umfangreichen Satz von Klassen für die automatische Ressourcenverwaltung für Heap Objekte und Kernel Handles bereit.
-   Verwenden Sie systeminterne Compilerfunktionen wie **\_ com \_ ptr \_ t** , um Ihre COM-Schnittstellen Zeiger in "intelligente Zeiger" zu kapseln und die Verweis Zählung zu unterstützen. Es gibt ähnliche Klassen für andere com-Datentypen: **\_ BSTR \_ t** und **\_ Variant \_ t** .
-   Überwachen Sie die ungewöhnliche Speicherauslastung von .NET-Code. Verwalteter Code ist nicht gegen Speicher Verluste anfällig. Informationen zum Auffinden von GC-Verlusten finden [Sie unter "Nachverfolgen von verwalteten Speicher Verlusten"](/archive/blogs/ricom/) .
-   Beachten Sie die Muster für den Client seitigen Webcode. Zirkuläre Verweise zwischen COM-Objekten und Skript-Engines wie JScript können große Verluste in Webanwendungen verursachen. ["Verstehen und lösen von Internet Explorer-Verlust Mustern"](/previous-versions/ms976398(v=msdn.10)) enthält weitere Informationen zu diesen Arten von Verlusten. Sie können das JavaScript-Speicher Verlust-Erkennungs Modul verwenden, um Speicher Verluste in Ihrem Code zu debuggen. Obwohl Windows Internet Explorer 8, das mit Windows 7 ausgeliefert wird, die meisten dieser Probleme verringert, sind ältere Browser weiterhin anfällig für diese Fehler.
-   Vermeiden Sie die Verwendung mehrerer Beendigungs Pfade aus einer Funktion. Zuordnungen, die Variablen im Funktionsbereich zugewiesen werden, sollten am Ende der Funktion in einem bestimmten Block freigegeben werden.
-   Verwenden Sie keine Ausnahmen in Ihrem Code, ohne alle lokalen Variablen in Funktionen freizugeben. Wenn Sie systemeigene Ausnahmen verwenden, geben Sie alle Zuordnungen im Block "endlich" frei \_ \_ . Wenn Sie C++-Ausnahmen verwenden, müssen alle Heap-und Handle-Zuordnungen in intelligente Zeiger umschließt werden.
-   Ein [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Objekt nicht verwerfen oder erneut initialisieren, ohne die [**propvariantclear**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear) -Funktion Aufrufs

## <a name="links-to-resources"></a>Links zu Ressourcen

*Allgemeine Zuordnungs Muster:*

-   [**Heap Zuordnungs Funktion**](/windows/win32/api/heapapi/nf-heapapi-heapalloc)
-   [**Speicher Belegungs Funktion**](https://msdn.microsoft.com/library/6ewkz86d(v=VS.71).aspx)
-   [**New-Operator (C++)**](https://msdn.microsoft.com/library/kewsb8ba(v=VS.71).aspx)
-   [**Virtuelle Zuordnungs Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
-   [Kernel Objekte](../sysinfo/kernel-objects.md)
-   [GDI-Objekt Handles](../sysinfo/gdi-objects.md)
-   [Objekt Handles für die Benutzeroberfläche](../sysinfo/user-objects.md)

*Microsoft-Tools:*

-   [Application Verifier](application-verifier.md)
-   [Debuggingtools für Windows](/windows-hardware/drivers/debugger/)
-   [Dumpheap im Benutzermodus](/windows-hardware/drivers/debugger/umdh)
-   [Ablaufverfolgungs-, Verarbeitungs-und Analyse Tool](https://msdn.microsoft.com/performance/cc825801.aspx)
-   [CRT-Debugheap](/visualstudio/debugger/crt-debug-heap-details?view=vs-2015)

*Weitere Links:*

-   [**Auto \_ ptr-Klasse**](https://msdn.microsoft.com/library/ew3fk483(v=VS.71).aspx)
-   [Active Template Library (ATL)-Speicher Klassen](https://msdn.microsoft.com/library/44yh1z4f(v=VS.71).aspx)
-   [**\_com \_ ptr \_ t-Objekt**](https://msdn.microsoft.com/library/417w8b3b(v=VS.71).aspx)
-   [**\_BSTR \_ t-Klasse**](https://msdn.microsoft.com/library/zthfhkd6(v=VS.71).aspx)
-   [**\_Variant \_ YT-Klasse**](https://msdn.microsoft.com/library/x295h94e(v=VS.71).aspx)
-   ["Nachverfolgung von verwalteten Speicher Verlusten"](/archive/blogs/ricom/)
-   ["Verstehen und lösen von Internet Explorer-entwurfmustern"](/previous-versions/ms976398(v=msdn.10))
-   ["JavaScript-Speicherlecks-Erkennung"](/archive/blogs/gpde/new-javascript-memory-leak-detector-from-our-team)
-   [Minderung von zirkulären Speicherlecks (in Browsern):](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/dd361842(v=vs.85))
-   [**try-finally-Anweisung**](https://msdn.microsoft.com/library/yb3kz605(v=VS.71).aspx)
-   [**PROPVARIANT-Struktur**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)
-   [**Propvariantclear-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)

 

 
