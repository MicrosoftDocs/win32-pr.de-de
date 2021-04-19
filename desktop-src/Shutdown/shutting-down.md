---
description: 'Es gibt drei Möglichkeiten, wie eine Anwendung lokale oder Remote Computer Herunterfahren kann: fahren Sie das System herunter, und starten Sie die Anwendung neu, und starten Sie die Anwendung neu, und starten Sie das System herunter, und starten Sie alle Anwendungen neu, die für den Neustart registriert wurden.'
ms.assetid: acadf58f-3f68-4fa1-bdcf-8f85c8479263
title: Wird heruntergefahren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e436dd9e3b115112e63b0440b4d51de4c7f9f619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362924"
---
# <a name="shutting-down"></a>Wird heruntergefahren

Es gibt drei Möglichkeiten für eine Anwendung, lokale Computer oder Remote Computer herunterzufahren:

-   Herunterfahren des Systems
-   Herunterfahren des Systems und Neustarten des Systems
-   Herunterfahren der Anwendung, Herunterfahren und Neustarten des Systems und Neustarten aller Anwendungen, die für den Neustart registriert wurden

Um das System herunterzufahren, verwenden Sie die [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) -Funktion mit dem EWX- \_ Flag zum Herunterfahren. Ein Beispiel finden Sie unter Vorgehens [Weise beim Herunterfahren des Systems](how-to-shut-down-the-system.md). Um das System herunterzufahren und neu zu starten, verwenden Sie das EWX- \_ Startflag. Um alle Anwendungen neu zu starten, die mithilfe der [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) -Funktion für den Neustart registriert wurden, verwenden Sie das EXW \_ restartapps-Flag.

Die Funktionen [**InitiateShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna), [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)und [**initiatesystemshutdownetx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) starten einen Timer und zeigen ein Dialogfeld an, in dem der Benutzer aufgefordert wird, sich abzumelden. Während dieses Dialogfeld angezeigt wird, kann die Funktion " [**abortsystemshutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna) " den Timer beenden und das Herunterfahren des Computers verhindern. Wenn der Timer abgelaufen ist, wird der Computer jedoch heruntergefahren. Diese Funktionen können den Computer auch nach dem Herunterfahren neu starten. Weitere Informationen finden Sie unter [Anzeigen des Dialog](displaying-the-shutdown-dialog-box.md)Felds "Herunterfahren".

## <a name="shutdown-notifications"></a>Benachrichtigungen zum Herunterfahren

Anwendungen mit einer Fenster-und Nachrichten Warteschlange empfangen Benachrichtigungen über die [**WM- \_ Abfrage "queryendsession**](wm-queryendsession.md) " und " [**WM \_ EndSession**](wm-endsession.md) ". Diese Anwendungen sollten **true** zurückgeben, um anzugeben, dass Sie beendet werden können. Anwendungen sollten das Herunterfahren des Systems nur blockieren, wenn dies unbedingt erforderlich ist. Anwendungen sollten alle erforderlichen Bereinigungs Vorgänge ausführen, während **WM- \_ EndSession** verarbeitet wird. Anwendungen mit nicht gespeicherten Daten könnten die Daten an einem temporären Speicherort speichern und beim nächsten Start der Anwendung wiederherstellen. Es wird empfohlen, dass Anwendungen Ihre Daten und ihren Status häufig speichern. Beispielsweise werden Daten Zwischenspeicher Vorgängen, die vom Benutzer initiiert wurden, automatisch gespeichert, um die beim Herunterfahren zu speichernde Datenmenge zu verringern.

Konsolen Anwendungen erhalten herunter Fahr Benachrichtigungen in ihren Handlerroutinen. Verwenden Sie zum Registrieren eines Konsolen Handlers die [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) -Funktion.

Dienst Anwendungen empfangen Benachrichtigungen zum Herunterfahren in ihren Handlerroutinen. Verwenden Sie die [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) -Funktion, um einen Dienst Steuerungs Handler zu registrieren.

## <a name="blocking-shutdown"></a>Blockieren des herunter Fahrens

Wenn eine Anwendung ein mögliches Herunterfahren des Systems blockieren muss, kann Sie die [**shutdownblockreasoncreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) -Funktion aufzurufen. Der Aufrufer stellt eine Grund Zeichenfolge bereit, die dem Benutzer angezeigt wird. Die Zeichenfolge sollte kurz und eindeutig sein und dem Benutzer die erforderlichen Informationen bereitstellen, um zu entscheiden, ob das System weiterhin heruntergefahren werden soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Herunterfahren des Systems](how-to-shut-down-the-system.md)
</dt> </dl>

 

 
