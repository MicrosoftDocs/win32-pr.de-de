---
title: Neues in Wer
description: Auf dieser Seite werden die neuen Features von Windows-Fehlerberichterstattung (wer) für die einzelnen Releases zusammengefasst.
ms.assetid: 6cdd6c64-ba67-40dc-9942-0371320f1881
keywords:
- Windows-Fehlerberichterstattung Windows-Fehlerberichterstattung, Neuerungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526776de3c5f88400e7cfae7ed9b9717318c223d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314648"
---
# <a name="whats-new-in-wer"></a>Neues in Wer

Auf dieser Seite werden die neuen Features von Windows-Fehlerberichterstattung (wer) für die einzelnen Releases zusammengefasst.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 und Windows Server 2008 R2

In der folgenden Liste werden die neuen wer-Features für Windows 7 und Windows Server 2008 R2 zusammengefasst.

-   Fügt die Möglichkeit hinzu, eine Ausnahme zu auslösen, die alle Ausnahmehandler umgeht, wodurch die Anwendung sofort beendet und Windows-Fehlerberichterstattung aufgerufen wird. Weitere Informationen finden Sie unter der [**raisegfailfastexception**](/previous-versions/dd408166(v=vs.85)) -Funktion.
-   Fügt die Möglichkeit hinzu, einen Out-of-Process-Ausnahmehandler zu registrieren, den wer beim Auftreten eines Absturzes aufruft, um den Ereignis Namen, die Berichts Parameter und die Optionen zum Debuggen zu erfassen. Weitere Informationen finden Sie unter der Funktion " [**werregisterruntimeexceptionmodule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule) ".

Hinzugefügte Funktionen:

-   [**Outo-processexceptioneventcallback**](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event)
-   [**Outo-processexceptioneventsignaturecallback**](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event_signature)
-   [**OutOfProcessExceptionEventDebuggerLaunchCallback**](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_debugger_launch)
-   [**Raian failfastexception**](/previous-versions/dd408166(v=vs.85))
-   [**Werregisterruntimeexceptionmodule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule)
-   [**Werunregisterruntimeexceptionmodule**](/windows/desktop/api/Werapi/nf-werapi-werunregisterruntimeexceptionmodule)

Hinzugefügte Strukturen:

-   [**\_Informationen zur Lauf Zeit \_ Ausnahme \_**](/windows/desktop/api/Werapi/ns-werapi-wer_runtime_exception_information)

## <a name="windows-server-2008-and-windows-vista-sp1"></a>Windows Server 2008 und Windows Vista SP1

In der folgenden Liste sind die neuen Features von wer für Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) zusammengefasst.

-   Wer kann so konfiguriert werden, dass vollständige benutzermodusdumps gesammelt und lokal gespeichert werden, nachdem eine Anwendung im Benutzermodus abstürzt (Anwendungen, die eigene benutzerdefinierte Absturzberichte ausführen, einschließlich .NET-Anwendungen, werden nicht unterstützt). Weitere Informationen finden Sie unter [Sammeln von User-Mode Dumps](collecting-user-mode-dumps.md).

## <a name="windows-vista"></a>Windows Vista

In der folgenden Liste werden die neuen Features von Windows-Fehlerberichterstattung (wer) für Windows Vista zusammengefasst:

-   Wer wurde über das Überwachen von Abstürzen und nicht reagierenden Prozessen hinaus erweitert. Wer bietet Unterstützung für viele neue Typen nicht kritischer Ereignisse, z. b. Leistungsprobleme. Dies ermöglicht es Entwicklern, mehr über die Erfahrungen zu erfahren, die Ihre Kunden mit den Anwendungen haben, die Sie entwickelt haben.
-   Neue Funktionen bieten Entwicklern die Flexibilität, Problemberichte zu erstellen, anzupassen und zu übermitteln. Weitere Informationen finden Sie unter [wer Functions](wer-functions.md).
-   Die verbesserten [Online Dienste für Windows-Qualität](https://www.microsoft.com/?ref=go) bieten Entwicklern Zugang zu den Problem Informationen, die Kunden für Ihre Anwendungen einreichen, sowie einen Mechanismus zum Bereitstellen von Lösungen für diese Kunden.
-   Mit den Funktionen, die von [Anwendungs Wiederherstellung und Neustart](/windows/desktop/Recovery/application-recovery-and-restart-portal) und [Neustart-Manager](/windows/desktop/RstMgr/restart-manager-portal) eingeführt werden, können Anwendungen automatisch Informationen wiederherstellen und im Falle eines schwerwiegenden Fehlers neu starten. Entwickler können diese Features in Ihren Anwendungen verwenden, um die Benutzer Leistung erheblich zu verbessern.
-   **Problem Berichte und-Lösungen unter Windows Vista oder das Aktions Center auf Windows 7** sind der zentrale Ort, an dem Benutzer mit wer interagieren können. Benutzer können nach neuen Lösungen suchen, ihren Berichts Verlauf verwalten, die Details eines Problem Berichts anzeigen und die Bericht Erstellungs Einstellungen verwalten. Dies schließt auch das Aktivieren von Wer ein, um automatisch nach Lösungen zu suchen, ohne den Benutzer zu unterbrechen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Fehlerberichterstattung](windows-error-reporting.md)
</dt> </dl>

 

 