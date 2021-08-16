---
description: Die Hilfsfunktionen der Versions-API werden verwendet, um die Version des derzeit ausgeführten Betriebssystems zu bestimmen. Weitere Informationen finden Sie unter Abrufen der Systemversion.
ms.assetid: 1a70b1d9-ed66-4201-9921-4e26e4001020
title: Version des Betriebssystems
ms.topic: article
ms.date: 09/15/2020
ms.openlocfilehash: ae90f4eac5546fccd7513d781234896fbbbda93ff3723a9ac1db438321ecf214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763952"
---
# <a name="operating-system-version"></a>Version des Betriebssystems

Die Hilfsfunktionen der [Versions-API](version-helper-apis.md) werden verwendet, um die Version des derzeit ausgeführten Betriebssystems zu bestimmen. Weitere Informationen finden Sie unter [Abrufen der Systemversion](getting-the-system-version.md).

In der folgenden Tabelle sind die neuesten Betriebssystemversionsnummern zusammengefasst.

| Betriebssystem | Versionsnummer |
|------------------|----------------|
| Windows 10       | 10.0\*         |
| Windows Server 2019 | 10.0\*      |
| Windows Server 2016 | 10.0\*      |
| Windows 8.1      | 6.3\*          |
| Windows Server 2012 R2 | 6.3\*    |
| Windows 8        | 6.2            |
| Windows Server 2012 | 6.2         |
| Windows 7        | 6.1            |
| Windows Server 2008 R2 | 6.1      |
| Windows Server 2008 | 6.0         |
| Windows Vista    | 6.0            |
| Windows Server 2003 R2 | 5,2      |
| Windows Server 2003 | 5,2         |
| Windows XP 64-Bit Edition | 5,2   |
| Windows XP | 5,1                  |
| Windows 2000     | 5.0            |

**\*** Für Anwendungen, die für Windows 8.1 oder Windows 10 manifestiert wurden. Anwendungen, die nicht für Windows 8.1 oder Windows 10 manifestiert sind, geben den Windows 8 Betriebssystemversionswert (6.2) zurück. Informationen zum Manifestieren Ihrer Anwendungen für Windows 8.1 oder Windows 10 finden Sie unter [Targeting your application for Windows (Zielgruppenadressieren Ihrer Anwendung für Windows](targeting-your-application-at-windows-8-1.md)).<br/>

Die Identifizierung des aktuellen Betriebssystems ist in der Regel nicht die beste Methode, um zu bestimmen, ob ein bestimmtes Betriebssystemfeature vorhanden ist. Dies liegt daran, dass dem Betriebssystem möglicherweise neue Features in einer verteilbaren DLL hinzugefügt wurden. Anstatt die Funktionen des [Versions-API-Hilfssystems](version-helper-apis.md) zu verwenden, um die Betriebssystemplattform oder Versionsnummer zu bestimmen, testen Sie, ob das Feature selbst vorhanden ist.

Informationen zum Ermitteln der besten Testart für ein Feature finden Sie in der Dokumentation zu den für Sie interessanten Features. In der folgenden Liste werden einige gängige Techniken für die Featureerkennung erläutert:

- Sie können testen, ob die funktionen vorhanden sind, die einem Feature zugeordnet sind. Um zu testen, dass eine Funktion in einer System-DLL vorhanden ist, rufen Sie die [**LoadLibrary-Funktion**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) auf, um die DLL zu laden. Rufen Sie dann die [**GetProcAddress-Funktion**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) auf, um zu bestimmen, ob die interessierende Funktion in der DLL vorhanden ist. Verwenden Sie den von **GetProcAddress** zurückgegebenen Zeiger, um die Funktion aufzurufen. Beachten Sie, dass es sich auch dann, wenn die Funktion vorhanden ist, um einen Stub handelt, der nur einen Fehlercode wie ERROR \_ CALL NOT IMPLEMENTED zurückgibt. \_ \_
- Sie können das Vorhandensein einiger Features mithilfe der [**GetSystemMetrics-Funktion**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) ermitteln. Sie können beispielsweise mehrere Anzeigemonitore erkennen, indem **Sie GetSystemMetrics**(SM \_ CMONITORS) aufrufen.
- Es gibt mehrere Versionen der verteilbaren DLLs, die Shell- und allgemeine Steuerungsfunktionen implementieren. Informationen dazu, welche Versionen auf dem System vorhanden sind, auf dem Ihre Anwendung ausgeführt wird, finden Sie im Thema [Shell and Common Controls Versions (Shell- und Common Controls-Versionen).](/previous-versions/windows/desktop/legacy/bb776779(v=vs.85))

Wenn Sie ein bestimmtes Betriebssystem benötigen müssen, sollten Sie es als unterstützte Mindestversion verwenden, anstatt den Test für das eine Betriebssystem zu entwerfen. Auf diese Weise funktioniert Ihr Erkennungscode weiterhin an zukünftigen Versionen von Windows.

Beachten Sie, dass eine 32-Bit-Anwendung erkennen kann, ob sie unter WOW64 ausgeführt wird, indem sie die [**IsWow64Process-Funktion**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process) aufruft. Sie kann zusätzliche Prozessorinformationen abrufen, indem sie die [**GetNativeSystemInfo-Funktion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo) aufruft.

Weitere Informationen finden Sie unter [Windows 10 Releaseinformationen](/windows/release-information/) und [Windows Lifecycle Fact Sheet](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet).

