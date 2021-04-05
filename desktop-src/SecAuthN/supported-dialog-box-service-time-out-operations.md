---
description: Winlogon implementiert zwei Timeout Vorgänge, eine für sichere Dialogfelder und die andere für die Aktivierung und Beendigung des Bildschirmschoners.
ms.assetid: b1dfd7dc-cc00-4f1a-a157-c60b5d0f0b13
title: Unterstützte Dialog Feld Dienstnutzungsdauer-out-Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274950cadd45cd4e7e3be890da0e4350a4d0c5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751665"
---
# <a name="supported-dialog-box-service-time-out-operations"></a>Unterstützte Dialog Feld Dienstnutzungsdauer-out-Vorgänge

[*Winlogon*](../secgloss/w-gly.md) implementiert zwei Timeout Vorgänge, eine für sichere Dialogfelder und die andere für die Aktivierung und Beendigung des Bildschirmschoners.

Beim Anzeigen eines sicheren Dialog Felds (z. b. Anmeldung oder Entsperren einer Arbeitsstation) kann Winlogon die Dialogfelder mit einem Timeout erreichen und einen geeigneten Ergebniscode an die Dialogfeld Prozedur zurückgeben. Winlogon stellt eine Reihe von Dialogfeld-Unterstützungsfunktionen für die [*Gina*](../secgloss/g-gly.md)bereit. Die Gina muss diese Funktionen anstelle ihrer Windows-Entsprechungen verwenden, um sicherzustellen, dass die Gina und Winlogon die entsprechende Kontrolle über die Dialogfelder behalten. Wenn Sie die Winlogon-Versionen dieser Funktionen nicht verwenden, kann dies dazu führen, dass nicht autorisierte Benutzer Zugriff auf das System erhalten.

Die Dienste für das Winlogon-Dialogfeld werden von den folgenden Unterstützungsfunktionen bereitgestellt.



| Support-Funktion                                               | BESCHREIBUNG                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Wlxmessagebox**](/windows/win32/api/winwlx/nc-winwlx-pwlx_message_box)                         | Ähnelt der [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) -Funktion von Windows.                         |
| [**Wlxdialogbox**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box)                           | Ähnelt der Windows [**Dialogbox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) -Funktion.                           |
| [**Wlxdialogboxindirekte**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect)           | Ähnelt der Windows [**dialogboxindirekte**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta) -Funktion.           |
| [**Wlxdialogboxparam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param)                 | Ähnelt der Windows [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama) -Funktion.                 |
| [**Wlxdialogboxderederederetztparam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect_param) | Ähnelt der Windows [**dialogboxderetparam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama) -Funktion. |



 

Gina-DLLs können auch wlx- \_ WM- \_ SAS-Nachrichten von Winlogon empfangen. Diese Nachrichten werden an aktive Dialogfelder gesendet, wenn eine Sicherheits [*Sequenz (Secure Attention Sequence*](../secgloss/s-gly.md) , SAS) empfangen wird. Dies ist hilfreich, wenn die Gina gerade aufgefordert wird, die passende PIN für eine [*Smartcard*](../secgloss/s-gly.md)einzugeben, und die Karte aus dem [*Smartcardleser*](../secgloss/r-gly.md)entfernt wird. Winlogon verwendet wlx \_ DLG- \_ SAS als EndDialog-Ergebniscode, wenn ein SAS-Ereignis während eines Dialogfeld Vorgangs auftritt.

Timeouts werden ebenfalls auf diese Weise übermittelt. Eine wlx- \_ WM- \_ SAS-Nachricht wird mit dem wlx- \_ SAS- \_ Typ \_ scrnsvr- \_ Timeout oder dem wlx- \_ SAS- \_ \_ typtimeout gesendet. Das Dialogfeld endet mit einem geeigneten Exitcode, damit Gina-Entwickler die Timeout Benachrichtigungen miteinander verbinden können.

Die Gina-Dialogfelder können von Winlogon mithilfe des Codes wlx DLG-Benutzer Abmeldung beendet werden \_ \_ \_ . Dies weist darauf hin, dass sich der Benutzer während der Ausführung des Dialog Felds abgemeldet hat (z. b. durch Aufrufen der [**ExitWindowsEx**](/windows/win32/api/winuser/nf-winuser-exitwindowsex) -Funktion von einem anderen Thread).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Winlogon wird initialisiert.](initializing-winlogon.md)
</dt> <dt>

[Winlogon-Zustände](winlogon-states.md)
</dt> <dt>

[Senden von Nachrichten an die Gina](sending-messages-to-the-gina.md)
</dt> <dt>

[Winlogon-Unterstützungsfunktionen](authentication-functions.md)
</dt> </dl>

 

 
