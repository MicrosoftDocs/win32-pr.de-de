---
description: Die ExitWindows-Funktion meldet sich vom aktuellen Benutzer ab. Sie können auch die ExitWindowsEx-Funktion mit dem FLAG EXW \_ LOGOFF aufrufen.
ms.assetid: 906d92f1-7cbe-454e-9c71-34b4383aebab
title: Abmelden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2ab8525630673b897704cea675c5c2a1e6dc6b1df4dd875e8872a79f915204
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664400"
---
# <a name="logging-off"></a>Abmelden

Die [**ExitWindows-Funktion**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) meldet sich vom aktuellen Benutzer ab. Sie können auch die [**ExitWindowsEx-Funktion mit**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) dem FLAG EXW \_ LOGOFF aufrufen.

Wenn eine Anwendung [**exitWindows oder ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) zum Abmelden verwendet, sendet das System standardmäßig die [**WM \_ QUERYENDSESSION-Nachricht**](wm-queryendsession.md) an jedes Fenster. [](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) Anwendungen stimmen zu, zu beenden, indem **sie TRUE zurückgeben,** wenn sie diese Nachricht erhalten. Wenn eine Anwendung bei der **Verarbeitung dieser** Nachricht FALSE zurückgibt, wird der Abmeldevorgang abgebrochen. Wenn Ihre Anwendung die **WM \_ QUERYENDSESSION-Nachricht** verarbeitet, können Sie dem Benutzer erlauben, den Abmeldevorgang abzubricht, selbst wenn eine andere Anwendung oder das System die Anforderung für die Endsitzung stammt. Ein Beispiel finden Sie unter [Abmelden des aktuellen Benutzers.](how-to-log-off-the-current-user.md)

Wenn eine Anwendung **TRUE für** [**WM \_ QUERYENDSESSION**](wm-queryendsession.md)zurückgibt, empfängt sie die [**WM \_ ENDSESSION-Nachricht**](wm-endsession.md) und wird beendet, unabhängig davon, wie die anderen Anwendungen auf die **WM \_ QUERYENDSESSION-Nachricht** reagieren.

Um zu erzwingen, dass alle Anwendungen beendet werden, verwenden [**Sie ExitWindowsEx,**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)und geben Sie das EXW \_ FORCE-Flag an. Dadurch wird verhindert, dass das System [**WM \_ QUERYENDSESSION-Nachrichten**](wm-queryendsession.md) sendet.

Das System sendet auch während eines Abmeldevorgangs das STRG \_ LOGOFF EVENT-Steuerungssignal an \_ jeden Prozess. Eine Konsolenanwendung kann eine [**HandlerRoutine**](/windows/console/handlerroutine) registrieren, um diese Meldungen zu verarbeiten.

Wenn der Prozess, der [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) aufgerufen hat, in der Anmeldesitzung des interaktiven Benutzers ausgeführt wird, werden alle Prozesse in der Anmeldesitzung beendet. Wenn sich der **Prozess, der ExitWindowsEx aufruft,** in einer anderen Anmeldesitzung befindet, werden nur die Benachrichtigungen gesendet. es werden keine Prozesse beendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abmelden des aktuellen Benutzers](how-to-log-off-the-current-user.md)
</dt> </dl>

 

 
