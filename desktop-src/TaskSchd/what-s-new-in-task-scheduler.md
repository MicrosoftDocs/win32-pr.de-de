---
title: Neuerungen in Taskplaner
description: Liste der neuen Funktionen, die von verschiedenen Versionen von Taskplaner eingeführt wurden.
ms.assetid: 43fbbbd2-6e97-4ba5-9474-23c5e2b33612
keywords:
- Taskplaner Taskplaner , Neuerungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3592cc5efd08afe4737e9af429d52fa41216b6c756a64faeaa45f6cc5c0774b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354782"
---
# <a name="whats-new-in-task-scheduler"></a>Neuerungen in Taskplaner

Die folgenden Änderungen fassen die Neuerungen in verschiedenen Versionen von Taskplaner zusammen.

## <a name="windows-10-and-windows-server-2016"></a>Windows 10 (und Windows Server 2016)

Die folgenden Taskplaner Änderungen werden in Windows 10 eingeführt.

-   Wenn Stromsparmodus aktiviert ist, werden Windows Taskplaner Tasks nur ausgelöst, wenn die Aufgabe wie die folgende lautet:

    -   Nicht auf **Task nur starten festgelegt, wenn sich der Computer im Leerlauf befindet...** (Task verwendet [**idleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings)nicht)
    -   Nicht auf die Ausführung während der automatischen Wartung festgelegt (Task verwendet [**maintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings)nicht)
    -   Ist **auf Nur ausführen festgelegt, wenn der Benutzer angemeldet ist** (Task [**LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) ist **TASK \_ LOGON INTERACTIVE \_ \_ TOKEN** oder **TASK \_ LOGON \_ GROUP**).

    Alle anderen Trigger werden verzögert, bis Stromsparmodus deaktiviert ist. Weitere Informationen zum Zugreifen auf Stromsparmodus Status in Ihrer Anwendung finden Sie unter [**SYSTEM \_ POWER \_ STATUS**](/windows/desktop/api/winbase/ns-winbase-system_power_status). Allgemeine Informationen zu Stromsparmodus finden Sie unter [Stromsparmodus (in den Richtlinien für Hardwarekomponenten).](/windows-hardware/design/component-guidelines/battery-saver)

-   Aus Sicherheitsgründen kann ein Benutzer ohne Administratorrechte eine Windows Taskplaner Aufgabe, die von einem anderen Benutzer erstellt wurde, weder anzeigen noch verwalten.

## <a name="windows-8"></a>Windows 8

Die folgenden Taskplaner 2.0-Änderungen werden in Windows 8 eingeführt:

-   PowerShell-Unterstützung: Benutzer können verwalten (erstellen, löschen, ändern, explizit starten, beenden usw.). Windows Taskplaner Aufgaben mithilfe des PowerShell-Moduls ScheduledTasks.
-   Verwaltete Kennwörter: Administratoren können die verwalteten Active Directory-Kennwortkonten als Aufgabenprinzipale verwenden. Für diese Aufgaben ist keine erzwungene Kennwortrücksetzungsrichtlinie mehr erforderlich.
-   API-Änderungen: Mit der [**ITaskSettings3-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3) wurden zwei neue Taskeinstellungen eingeführt.
    -   [**MaintenanceSettings:**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings)Tasks, die diese Einstellungen verwenden, werden als neue Art geplanter Tasks behandelt, die während der automatischen Wartung des Betriebssystems gemäß der angegebenen Periodizität und dem angegebenen Stichtag aufgerufen werden.
    -   [**Volatile:**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile)Tasks, die als flüchtig festgelegt sind, sind bei einem Betriebssystemstart immer deaktiviert und müssen bei Bedarf explizit wieder aktiviert werden. Flüchtige Tasks werden von den Failoverclustern verwendet, um sicherzustellen, dass jeweils nur eine Taskinstanz in einem Cluster geplant ist.
-   Die einheitliche Zeitplanungs-Engine unterstützt jetzt die folgenden Features:
    -   S4U-Anmeldetyp über das [**LogonType-Element.**](taskschedulerschema-logontype-principaltype-element.md)
    -   XPath-Abfragewerte für Ereignistrigger über das [**ValueQueries-Element.**](taskschedulerschema-valuequeries-eventtriggertype-element.md)
    -   Lassen Sie das harte Beenden von Tasks nicht über das [**AllowHardTerminate-Element**](taskschedulerschema-allowhardterminate-settingstype-element.md) zu.
-   In dieser Version veraltete Features
    -   Aktion: [**sendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (Sie können [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) mit dem [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)[Send-MailMessage-Cmdlet](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) als Problemumgehung verwenden).
    -   Aktion: [**showMessage**](taskschedulerschema-showmessage-actiongroup-element.md).
    -   AT.exe Cmdline-Hilfsprogramm

## <a name="windows-7"></a>Windows 7

Die folgenden Taskplaner 2.0-Änderungen werden in Windows 7 eingeführt:

-   Verwenden der einheitlichen Zeitplanungs-Engine, die vom zugrunde liegenden Betriebssystem bereitgestellt wird.
-   Möglichkeit zum Ablehnen von Startaufgaben in Rail-Sitzungen (Remote Applications Integrated Locally).
-   Härtung der Aufgabensicherheit (nur für Aufgaben, die als "NETZWERKDIENST" oder "LOKALER DIENST" ausgeführt werden):

    -   Möglichkeit zum Zuweisen eines SID-Typs (Process Token Security Identifier) (z. B. uneingeschränkt oder keiner) zu einer Aufgabe.
    -   Ermöglichen Sie Es Taskentwicklern, den genauen Satz von Berechtigungen anzufordern, die für ihre Aufgabe erforderlich sind.

-   API-Änderungen:

    -   Unterstützung der Tasksicherheitshärtung: Mit der neuen IPrincipal2-Schnittstelle wird ein neues Feature für die Tasksicherheitshärtung eingeführt.
    -   Es wurden zwei neue Taskeinstellungen mit der neuen ITaskSettings2-Schnittstelle eingeführt.

        -   DisallowStartOnRemoteAppSession: Die neue Einstellung DisallowStartOnRemoteAppSession kann einen Taskstart ablehnen, wenn er in [Rail-Sitzungen (Remote Applications Integrated Locally)](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546) ausgelöst wird.
        -   UseUnifiedSchedulingEngine: Die Verwendung der UseUnifiedSchedulingEngine-Einstellung bietet ein einheitliches Verhalten für Windows Tasks und Dienste, da sie von einer allgemeinen systemweiten Planungs-Engine einheitlich verwaltet wird. Obwohl die Verwendung einer einheitlichen Engine empfohlen wird, werden einige der Taskplaner Features nicht unterstützt. Wenn die Kombination von Eigenschaften die Ausführung der Aufgabe unter einer einheitlichen Engine nicht zulässt, wird die Registrierung dieser Art abgelehnt.
        -   Die Aufgabenfunktionen, die von der einheitlichen Planungs-Engine nicht unterstützt werden, umfassen Folgendes:

            -   Anmeldetypen:

                -   [\_INTERAKTIVES \_ TOKEN ODER \_ \_ \_ KENNWORT FÜR DIE TASKANMELDUNG](./taskschedulerschema-logontype-principaltype-element.md)

            -   Richtlinie für mehrere Instanzen:

                -   [**\_TASKINSTANZEN \_ BEENDEN \_ VORHANDENE**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)

            -   Aktionen:

                -   [Senden von E-Mails](./taskschedulerschema-sendemail-actiongroup-element.md)
                -   [Meldung anzeigen](./taskschedulerschema-showmessage-actiongroup-element.md)

            -   Einstellungen:

                -   [Tasknetzwerkeinstellungen](./taskschedulerschema-networksettings-settingstype-element.md)
                -   [Keine harte Beendigung der Aufgabe zulassen](./taskschedulerschema-allowhardterminate-settingstype-element.md)

            -   Trigger:

                -   [Zeitlimit für Triggerausführung](./taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
                -   [Wiederholungsmuster für Kalendertrigger]( ./taskschedulerschema-repetition-triggerbasetype-element.md)
                -   [XPath-Abfragewerte für Ereignistrigger]( ./taskschedulerschema-valuequeries-eventtriggertype-element.md)
                -   [Monatliche](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md) und monatliche Triggertypen [für Wochentage](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md)

## <a name="windows-vista"></a>Windows Vista

Die Taskplaner 2.0-API sollte bei der Entwicklung von Anwendungen verwendet werden, die den Taskplaner-Dienst auf Windows Vista verwenden. Weitere Informationen finden Sie unter [Taskplaner-Referenz](task-scheduler-reference.md) und [Verwenden des Taskplaner](using-the-task-scheduler.md).

## <a name="windows-2000-windows-xp-and-windows-server-2003"></a>Windows 2000, Windows XP und Windows Server 2003

Die Taskplaner 2.0-API ist nicht verfügbar. Verwenden Sie Taskplaner 1.0.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[Informationen zum Taskplaner](about-the-task-scheduler.md)
</dt> </dl>

 

 
