---
title: Neues in Taskplaner
description: Liste der neuen Funktionen, die von verschiedenen Versionen von Taskplaner eingeführt wurden.
ms.assetid: 43fbbbd2-6e97-4ba5-9474-23c5e2b33612
keywords:
- Taskplaner Taskplaner, Neuerungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5245ab4e681af937924cfbd217095009d80d6a11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342620"
---
# <a name="whats-new-in-task-scheduler"></a>Neues in Taskplaner

Die folgenden Änderungen fassen zusammen, welche Neuerungen in verschiedenen Versionen von Taskplaner sind.

## <a name="windows-10-and-windows-server-2016"></a>Windows 10 (und Windows Server 2016)

Die folgenden Taskplaner Änderungen werden in Windows 10 eingeführt.

-   Wenn Akku Schoner eingeschaltet ist, werden Windows Taskplaner-Tasks nur ausgelöst, wenn die Aufgabe wie folgt lautet:

    -   Nicht so festgelegt, dass **der Task nur gestartet wird, wenn sich der Computer im Leerlauf befindet...** (der Task verwendet nicht [**idlesettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings))
    -   Nicht für die automatische Wartung festgelegt (der Task verwendet keine [**maintenancesettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings))
    -   Ist so festgelegt, dass Sie **nur ausgeführt wird, wenn der Benutzer angemeldet ist** (Task [**logontype**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) ist **\_ interaktive Aufgaben Anmeldung \_ \_** oder **Task \_ Anmelde \_ Gruppe**)

    Alle anderen Trigger werden verzögert, bis Akku Schoner ausgeschaltet ist. Weitere Informationen zum Zugreifen auf den Akku Schoner Status in Ihrer Anwendung finden Sie unter [**System \_ Energie \_ Status**](/windows/desktop/api/winbase/ns-winbase-system_power_status). Allgemeine Informationen zum Akku Schoner finden Sie unter [Batterie Schoner (in den Richtlinien für die Hardwarekomponente)](/windows-hardware/design/component-guidelines/battery-saver).

-   Aus Sicherheitsgründen kann ein Benutzer ohne Administratorrechte keine Windows Taskplaner-Aufgabe anzeigen und verwalten, die von einem anderen Benutzer erstellt wurde.

## <a name="windows-8"></a>Windows 8

Die folgenden Taskplaner 2,0-Änderungen werden in Windows 8 eingeführt:

-   PowerShell-Unterstützung: Benutzer können verwalten (erstellen, löschen, ändern, explizit starten, abbrechen usw.) Windows Taskplaner Tasks mithilfe des PowerShell-Moduls scheduledtasks.
-   Verwaltete Kenn Wörter: Administratoren können die Active Directory verwalteten Kenn Wort Konten als Aufgaben Prinzipale verwenden. Diese Aufgaben erfordern keine erzwungene Richtlinie zum Zurücksetzen von Kenn Wörtern mehr.
-   API-Änderungen: in wurden zwei neue Aufgaben Einstellungen mit der [**ITaskSettings3**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3) -Schnittstelle eingeführt.
    -   [**Maintenancesettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings): Tasks, die diese Einstellungen verwenden, werden als neuer Typ geplanter Aufgaben behandelt, die während der automatischen Wartungszeit des Betriebssystems entsprechend der angegebenen Periodizität und Frist aufgerufen werden.
    -   [**Flüchtig**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile): Tasks, die als flüchtig festgelegt sind, werden bei einem Betriebssystem Start immer deaktiviert und müssen bei Bedarf explizit wieder aktiviert werden. Flüchtige Tasks werden von den Failoverclustern verwendet, um sicherzustellen, dass jeweils nur eine Task Instanz in einem Cluster geplant wird.
-   Die vereinheitlichte Planungs-Engine unterstützt jetzt die folgenden Features:
    -   S4U Logon Type, über das [**logontype**](taskschedulerschema-logontype-principaltype-element.md) -Element.
    -   XPath-Abfrage Werte für Ereignis Trigger durch das [**valuequeries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) -Element.
    -   Erlauben Sie die Beendigung der Aufgabe nicht durch das Element " [**Zustellungs**](taskschedulerschema-allowhardterminate-settingstype-element.md) Element".
-   In dieser Version veraltete Features
    -   Aktion: [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (Sie können [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) mit dem [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)-Cmdlet "[Send-Mail Message](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) " als Problem Umgehung verwenden).
    -   Action: [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md).
    -   AT.exe cmdline-Hilfsprogramm

## <a name="windows-7"></a>Windows 7

Die folgenden Taskplaner 2,0-Änderungen werden in Windows 7 eingeführt:

-   Verwenden der vereinheitlichten Planungs-Engine, die vom zugrunde liegenden Betriebssystem bereitgestellt wird.
-   Möglichkeit zum ablehnen von Start Tasks in lokalen Anwendungen, die lokal (Schiene) integriert sind.
-   Task Sicherheitshärtung (für Tasks, die nur als "Netzwerkdienst" oder "lokaler Dienst" ausgeführt werden):

    -   Möglichkeit zum Zuweisen eines Sicherheitstokentyps für die Prozess Token (z. b. "uneingeschränkt" oder "keine") zu einer Aufgabe.
    -   Erlauben Sie Aufgaben Entwicklern, den exakten Satz von Berechtigungen anzufordern, die ihre Aufgabe benötigt.

-   API-Änderungen:

    -   Unterstützung der Unterstützung der Sicherheit: das neue Feature zur Sicherheitshärtung wird mit der neuen IPrincipal2-Schnittstelle eingeführt
    -   In wurden zwei neue Aufgaben Einstellungen mit der neuen ITaskSettings2-Schnittstelle eingeführt.

        -   Disallowstartonremoteappsession: die neue disallowstartonremoteappsession-Einstellung kann einen Task Start ablehnen, wenn Sie in [lokal (in der lokalen Sitzung) integrierten Remote Anwendungen](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546) ausgelöst wird.
        -   Useunifiedschedulingengine: mithilfe der Einstellung useunifiedschedulingengine wird ein zusammenhängendes Verhalten für Windows-Tasks und-Dienste bereitstellt, da es auf einheitliche Weise durch eine gängige systemweite Planungs-Engine verwaltet wird. Obwohl die Verwendung eines vereinheitlichten Moduls empfohlen wird, werden einige der Taskplaner Features nicht unterstützt. Wenn die Kombination der Eigenschaften das Ausführen der Aufgabe unter einem vereinheitlichten Modul nicht zulässt, wird die Registrierung dieser solchen abgelehnt.
        -   Zu den Aufgaben Features, die von der Unified Scheduling-Engine nicht unterstützt werden, gehören:

            -   Anmelde Typen:

                -   [\_ \_ interaktives \_ Token \_ oder \_ Kennwort für die Task Anmeldung](./taskschedulerschema-logontype-principaltype-element.md)

            -   Richtlinie für mehrere Instanzen:

                -   [**Task \_ Instanzen \_ beendet \_ vorhandene**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)

            -   Aktionen:

                -   [Senden von E-Mails](./taskschedulerschema-sendemail-actiongroup-element.md)
                -   [Meldung anzeigen](./taskschedulerschema-showmessage-actiongroup-element.md)

            -   Einstellungen:

                -   [Task Netzwerkeinstellungen](./taskschedulerschema-networksettings-settingstype-element.md)
                -   [Aufgabe nicht schwer beenden](./taskschedulerschema-allowhardterminate-settingstype-element.md)

            -   Trigger:

                -   [Zeitlimit für die Triggerausführung](./taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
                -   [Wiederholungsmuster für Kalender Trigger]( ./taskschedulerschema-repetition-triggerbasetype-element.md)
                -   [XPath-Abfrage Werte für Ereignis Trigger]( ./taskschedulerschema-valuequeries-eventtriggertype-element.md)
                -   [Monatliche](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md) und [monatliche Day-of-week](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) -Auslösertypen

## <a name="windows-vista"></a>Windows Vista

Die Taskplaner 2,0-API sollte zum Entwickeln von Anwendungen verwendet werden, die den Taskplaner-Dienst unter Windows Vista verwenden. Weitere Informationen finden Sie unter [Taskplaner Referenz](task-scheduler-reference.md) und [Verwenden der Taskplaner](using-the-task-scheduler.md).

## <a name="windows-2000-windows-xp-and-windows-server-2003"></a>Windows 2000, Windows XP und Windows Server 2003

Die Taskplaner 2,0-API ist nicht verfügbar. Verwenden Sie Taskplaner 1,0.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[Informationen zum Taskplaner](about-the-task-scheduler.md)
</dt> </dl>

 

 
