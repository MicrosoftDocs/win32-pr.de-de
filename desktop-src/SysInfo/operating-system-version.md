---
description: Die Versions-API-Hilfsfunktionen werden verwendet, um die Version des Betriebssystems zu ermitteln, die derzeit ausgeführt wird. Weitere Informationen finden Sie unter erhalten der System Version.
ms.assetid: 1a70b1d9-ed66-4201-9921-4e26e4001020
title: Version des Betriebssystems
ms.topic: article
ms.date: 09/15/2020
ms.openlocfilehash: 73eb9a81880f29f9292713af46c5c79a7e9eb2de
ms.sourcegitcommit: 7ea69db68bca2b1592802e676ada8432a2583410
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/17/2020
ms.locfileid: "104039789"
---
# <a name="operating-system-version"></a>Version des Betriebssystems

Die [Versions-API-Hilfsfunktionen](version-helper-apis.md) werden verwendet, um die Version des Betriebssystems zu ermitteln, die derzeit ausgeführt wird. Weitere Informationen finden Sie unter [erhalten der System Version](getting-the-system-version.md).

In der folgenden Tabelle werden die aktuellen Versionsnummern des Betriebssystems zusammengefasst.

| Betriebssystem | Versionsnummer |
|------------------|----------------|
| Windows 10       | 10,0\*         |
| Windows Server 2019 | 10,0\*      |
| Windows Server 2016 | 10,0\*      |
| Windows 8.1      | 6.3\*          |
| Windows Server 2012 R2 | 6.3\*    |
| Windows 8        | 6.2            |
| Windows Server 2012 | 6.2         |
| Windows 7        | 6.1            |
| Windows Server 2008 R2 | 6.1      |
| Windows Server 2008 | 6.0         |
| Windows Vista    | 6.0            |
| Windows Server 2003 R2 | 5,2      |
| Windows Server 2003 | 5,2         |
| Windows XP 64-Bit-Edition | 5,2   |
| Windows XP | 5,1                  |
| Windows 2000     | 5.0            |

**\*** Für Anwendungen, die sich für Windows 8.1 oder Windows 10 manifestieren. Anwendungen, die nicht für Windows 8.1 oder Windows 10 angezeigt werden, geben den Wert für die Windows 8-Betriebssystemversion (6,2) zurück. Informationen zum manifestieren Ihrer Anwendungen für Windows 8.1 oder Windows 10 finden Sie unter [Zielanwendung für Windows](targeting-your-application-at-windows-8-1.md).<br/>

Die Identifizierung des aktuellen Betriebssystems ist in der Regel nicht die beste Methode, um zu bestimmen, ob ein bestimmtes Betriebssystem Feature vorhanden ist. Dies liegt daran, dass dem Betriebssystem möglicherweise neue Features in einer verteilbaren dll hinzugefügt wurden. Anstatt die Version der- [API](version-helper-apis.md) -Hilfsobjekte zum Ermitteln der Betriebssystem Plattform oder der Versionsnummer zu verwenden, testen Sie, ob das Feature selbst vorhanden ist.

Um die beste Methode zum Testen auf eine Funktion zu ermitteln, lesen Sie die Dokumentation für das relevante Feature. In der folgenden Liste werden einige gängige Techniken für die Funktionserkennung erläutert:

- Sie können überprüfen, ob die einem Feature zugeordneten Funktionen vorhanden sind. Um zu testen, ob eine Funktion in einer System-DLL vorhanden ist, müssen Sie die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion zum Laden der DLL-Datei aufzurufen. Anschließend können Sie die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen, um zu bestimmen, ob die gewünschte Funktion in der dll vorhanden ist. Verwenden Sie den von **GetProcAddress** zurückgegebenen Zeiger zum Aufrufen der Funktion. Beachten Sie, dass auch dann, wenn die Funktion vorhanden ist, ein Stub ist, der nur einen Fehlercode zurückgibt, wie z \_ \_ . b \_ . nicht implementierte Fehler Aufrufe.
- Sie können das vorhanden sein einiger Features mithilfe der [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) -Funktion bestimmen. Beispielsweise können Sie mehrere Anzeige Monitore durch Aufrufen von **GetSystemMetrics**(SM \_ cmonitors) erkennen.
- Es gibt mehrere Versionen der verteilbaren DLLs, die Shell und allgemeine Steuerungsfunktionen implementieren. Informationen zum Bestimmen der Versionen, die auf dem System vorhanden sind, auf dem Ihre Anwendung ausgeführt wird, finden Sie im Thema [Shell-und Common Controls-Versionen](/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)).

Wenn Sie ein bestimmtes Betriebssystem benötigen, achten Sie darauf, dass Sie es als unterstützte Mindestversion verwenden, anstatt den Test für das einzige Betriebssystem zu entwerfen. Auf diese Weise kann der Erkennungs Code weiterhin in zukünftigen Versionen von Windows verwendet werden.

Beachten Sie, dass eine 32-Bit-Anwendung erkennen kann, ob Sie unter WOW64 ausgeführt wird, indem Sie die [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process) -Funktion aufrufen. Sie kann zusätzliche Prozessor Informationen abrufen, indem Sie die [**GetNativeSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo) -Funktion aufrufen.

Weitere Informationen finden Sie unter [Windows 10-Releaseinformationen](/windows/release-information/) und [Windows Lifecycle-Faktenblatt](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet).

