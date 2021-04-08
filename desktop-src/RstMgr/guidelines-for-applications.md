---
title: Richtlinien für Anwendungen
description: Anwendungen, die unter Windows Vista und Windows Server 2008 ausgeführt werden, sollten diese Richtlinien einhalten, um sicherzustellen, dass der Neustart-Manager Anwendungen bei Bedarf Herunterfahren und neu starten kann, um Updates zu installieren.
ms.assetid: 97b1df63-65a9-47b4-891b-e4a754882b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebace21e09956c68d34c90775c5ea646a8b2dd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729625"
---
# <a name="guidelines-for-applications"></a>Richtlinien für Anwendungen

Anwendungen, die unter Windows Vista und Windows Server 2008 ausgeführt werden, sollten diese Richtlinien einhalten, um sicherzustellen, dass der Neustart-Manager Anwendungen bei Bedarf Herunterfahren und neu starten kann, um Updates zu installieren. Dienste können die Richtlinien verwenden, die unter [Richtlinien für Dienste](guidelines-for-services.md)beschrieben werden.

-   Der Neustart-Manager fragt GUI-Anwendungen für das Herunterfahren ab, indem er eine [**WM- \_ queryendsession**](/windows/desktop/Shutdown/wm-queryendsession) -Benachrichtigung sendet, für die der *LPARAM* -Parameter auf **EndSession \_ CloseApp** (0x1) festgelegt Anwendungen sollten nicht heruntergefahren werden, wenn Sie eine " **WM \_ queryendsession** "-Meldung empfangen, weil eine andere Anwendung möglicherweise nicht heruntergefahren werden kann. GUI-Anwendungen sollten auf die **WM- \_ Abfrage "queryendsession** " lauschen und den Wert " **true** " zurückgeben, wenn die Anwendung für das Herunterfahren und den Neustart vorbereitet ist. Wenn keine Anwendung den Wert **false** zurückgibt, sendet der Neustart-Manager eine [**WM- \_ endsitzungs**](/windows/desktop/Shutdown/wm-endsession) Nachricht, wobei der *LPARAM* -Parameter auf **EndSession \_ CloseApp** (0x1) und der *wParam* -Parameter auf **true** festgelegt ist. Anwendungen sollten nur heruntergefahren werden, wenn Sie die **WM- \_ endsitzungs** Nachricht empfangen. Der Neustart-Manager sendet außerdem eine [**WM- \_ Schließen**](../winmsg/wm-close.md) -Nachricht für GUI-Anwendungen, die beim Empfangen von **WM \_ EndSession** nicht heruntergefahren werden. Wenn eine GUI-Anwendung auf eine **WM- \_ queryendsession** -Nachricht antwortet, indem der Wert **false** zurückgegeben wird, wird das Herunterfahren abgebrochen. Wenn das Herunterfahren jedoch erzwungen wird, wird die Anwendung unabhängig von der Anwendung beendet.
-   Wenn eine GUI-Anwendung eine [**WM- \_ endsitzungs**](/windows/desktop/Shutdown/wm-endsession) Nachricht empfängt, sollte sich die Anwendung auf das Herunterfahren innerhalb des angegebenen Timeout Zeitraums vorbereiten. Anwendungen sollten zumindest vorbereitet werden, indem alle Benutzerdaten und Zustandsinformationen, die nach einem Neustart benötigt werden, gespeichert werden. Es wird empfohlen, dass Anwendungen die Benutzerdaten und den Status regelmäßig speichern.
-   Der Neustart-Manager sendet eine **STRG \_ C- \_ Ereignis** Benachrichtigung an Konsolen Anwendungen, die heruntergefahren und neu gestartet werden müssen. Wenn eine Konsolenanwendung eine **STRG \_ C- \_ Ereignis** Benachrichtigung empfängt, sollte die Anwendung die erforderlichen Maßnahmen ergreifen, um das Herunterfahren innerhalb des angegebenen Zeitlimits vorzubereiten. Konsolen Anwendungen sollten mindestens eine [*Handlerroutine*](/windows/console/handlerroutine) -Funktion zum Verarbeiten der **STRG \_ C- \_ Ereignis** Benachrichtigung definieren und alle Benutzerdaten und Zustandsinformationen, die nach einem Neustart benötigt werden, speichern. Es wird empfohlen, dass Anwendungen die Benutzerdaten und den Status regelmäßig speichern.
-   Wenn Anwendungen nicht als Reaktion auf Herunterfahren heruntergefahren werden, können Installer die **rmforceshutdown** -Option der [**rmshutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) -Funktion verwenden, um zu erzwingen, dass die Anwendungen heruntergefahren werden. Wenn das Installationsprogramm das erzwungene Herunterfahren angibt, versucht der Neustart-Manager, die Anwendungen ordnungsgemäß herunterzufahren, indem die Nachrichten nach dem Herunterfahren gesendet werden GUI-Anwendungen und Konsolen Anwendungen können erzwungen werden, um die Installation eines wichtigen Sicherheitsupdates zu ermöglichen. Da dies zu Datenverlusten führen kann, sollten Anwendungen die Shutdown-Nachrichten verarbeiten und bei Bedarf ordnungsgemäß herunterfahren.
-   Anwendungen sollten sich für einen Neustart mithilfe der [**RegisterApplicationRestart**](/windows/desktop/api/winbase/nf-winbase-registerapplicationrestart) -Funktion registrieren. Der Neustart-Manager kann nur Anwendungen neu starten, die für den Neustart registriert wurden. Dies ist die einzige Möglichkeit, dass der Neustart-Manager den Befehlszeilen Befehl ermitteln kann, der beim Neustart der Anwendung verwendet werden soll. Wenn die Anwendung mit einem gespeicherten Zustand oder mit gespeicherten Daten erneut geöffnet werden muss, müssen diese Informationen in den Befehlszeilen Befehl eingeschlossen werden, der für die Anwendung registriert ist.
    > [!Note]  
    > Wenn die neu gestartete Anwendung im selben Verzeichnis ausgeführt werden muss, in dem Sie ausgeführt wurde, bevor Sie heruntergefahren wird, muss die Anwendung die Verzeichnisinformationen speichern und dann nach dem Neustart in das Verzeichnis wechseln.

     

    > [!Note]  
    > Anwendungen, die nicht als aktuell angemeldeter Benutzer ausgeführt werden, werden von der Funktion [**rmrestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) nicht neu gestartet. Beispielsweise werden mit der **rmrestart** -Funktion keine Anwendungen neu gestartet, die mit dem Befehl **Ausführen als** gestartet wurden, der nicht als aktuell angemeldeter Benutzer ausgeführt wird. Diese Anwendungen müssen manuell neu gestartet werden.

     

-   Wenn der Neustart-Manager feststellt, dass ein Systemneustart erforderlich ist, um ein Update zu installieren, werden keine Anwendungen und Dienste heruntergefahren. Stattdessen wird es dem Installer überlassen, zu entscheiden, wann ein Systemneustart geplant und das Update installiert werden soll. Installationsprogramme können die Unterbrechungen für Benutzer verringern, die durch Updates verursacht werden, die einen Systemneustart erfordern, indem Sie die [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) -Funktion mit dem **EWX \_ restartapps** -Flag oder die [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) -Funktion mit dem Flag zum Herunterfahren von **\_ restartapps** verwenden. Durch die Verwendung dieser Flags wird sichergestellt, dass für den Neustart registrierte Anwendungen nach einem Systemneustart neu gestartet werden, wodurch die Auswirkungen auf den Benutzer minimiert werden.

 

 