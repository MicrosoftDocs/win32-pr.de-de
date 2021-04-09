---
description: Die exitwindows-Funktion meldet den aktuellen Benutzer ab. Sie können auch die ExitWindowsEx-Funktion mit dem Flag für die EXW-Abmeldung aufzurufen \_ .
ms.assetid: 906d92f1-7cbe-454e-9c71-34b4383aebab
title: Abmelden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0571c0522c494acd763d57dcae8d200125cd53d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869232"
---
# <a name="logging-off"></a>Abmelden

Die [**exitwindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) -Funktion meldet den aktuellen Benutzer ab. Sie können auch die [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) -Funktion mit dem Flag für die EXW-Abmeldung aufzurufen \_ .

Wenn eine Anwendung [**exitwindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) oder [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) verwendet, um sich abzumelden, sendet das System standardmäßig die [**WM-Abfrage " \_ queryendsession**](wm-queryendsession.md) " an jedes Fenster. Anwendungen Stimmen zu beenden, indem Sie " **true** " zurückgeben, wenn diese Nachricht empfangen wird. Wenn eine Anwendung bei der Verarbeitung dieser Nachricht **false** zurückgibt, wird der Abmeldevorgang abgebrochen. Wenn Ihre Anwendung die **WM- \_ queryendsession** -Nachricht behandelt, können Sie zulassen, dass der Benutzer den Abmeldevorgang abbrechen kann, auch wenn eine andere Anwendung oder das System die Anforderung der Endsitzung verursacht hat. Ein Beispiel finden Sie unter [Abmelden des aktuellen Benutzers](how-to-log-off-the-current-user.md).

Wenn eine Anwendung **true** für [**WM \_ queryendsession**](wm-queryendsession.md)zurückgibt, empfängt Sie die [**WM- \_ endsitzungs**](wm-endsession.md) Nachricht und wird beendet, unabhängig davon, wie die anderen Anwendungen auf die **WM- \_ queryendsession** -Nachricht reagieren.

Um das Beenden aller Anwendungen zu erzwingen, verwenden Sie [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex), und geben Sie das EXW \_ Force-Flag an. Dadurch wird verhindert, dass das System [**WM- \_ queryendsession**](wm-queryendsession.md) -Nachrichten sendet.

Das System sendet \_ \_ während eines Abmelde Vorgangs auch das STRG-Abmelde Ereignis-Steuerungs Signal an jeden Prozess. Eine Konsolenanwendung kann eine [**Handlerroutine**](/windows/console/handlerroutine) registrieren, um diese Nachrichten zu verarbeiten.

Wenn der Prozess, der [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) aufgerufen hat, in der Anmelde Sitzung des interaktiven Benutzers ausgeführt wird, werden alle Prozesse in der Anmelde Sitzung beendet. Wenn sich der Prozess, der **ExitWindowsEx** aufgerufen hat, in einer anderen Anmelde Sitzung befindet, werden nur die Benachrichtigungen durchgeführt. keine Prozesse werden beendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abmelden des aktuellen Benutzers](how-to-log-off-the-current-user.md)
</dt> </dl>

 

 
