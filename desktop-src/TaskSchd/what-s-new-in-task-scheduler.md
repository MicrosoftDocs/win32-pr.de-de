---
title: Neues in Taskplaner
description: Liste der neuen Funktionen, die durch verschiedene Versionen von Taskplaner.
ms.assetid: 43fbbbd2-6e97-4ba5-9474-23c5e2b33612
keywords:
- Taskplaner Taskplaner , neues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3592cc5efd08afe4737e9af429d52fa41216b6c756a64faeaa45f6cc5c0774b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354782"
---
# <a name="whats-new-in-task-scheduler"></a>Neues in Taskplaner

Die folgenden Änderungen fassen die Neuerungen in verschiedenen Versionen von Taskplaner.

## <a name="windows-10-and-windows-server-2016"></a>Windows 10 (und Windows Server 2016)

Die folgenden Taskplaner werden in Windows 10.

-   Wenn Stromsparmodus ist, Windows Taskplaner Aufgaben nur ausgelöst, wenn die Aufgabe wie die folgenden ist:

    -   Nicht auf **Task starten nur festgelegt, wenn sich der Computer** im Leerlauf befindet... (task doesn't use [**IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings))
    -   Während der automatischen Wartung nicht für die Ausführung festgelegt (task doesn't [**use MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings))
    -   Ist auf **Nur ausführen festgelegt, wenn** der Benutzer angemeldet ist (Task [**LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) ist **TASK \_ LOGON INTERACTIVE \_ \_ TOKEN** oder **TASK \_ LOGON \_ GROUP**).

    Alle anderen Trigger werden verzögert, bis Stromsparmodus deaktiviert ist. Weitere Informationen zum Zugreifen auf Stromsparmodus Status in Ihrer Anwendung finden Sie unter [**SYSTEM \_ POWER \_ STATUS**](/windows/desktop/api/winbase/ns-winbase-system_power_status). Allgemeine Informationen zu Stromsparmodus finden Sie unter Stromsparmodus [(in den Richtlinien für Hardwarekomponenten).](/windows-hardware/design/component-guidelines/battery-saver)

-   Aus Sicherheitsgründen kann ein Benutzer ohne Administratorrechte einen von einem anderen Benutzer erstellten Windows Taskplaner nicht anzeigen oder verwalten.

## <a name="windows-8"></a>Windows 8

Die folgenden Taskplaner 2.0-Änderungen werden in Windows 8:

-   PowerShell-Unterstützung: Benutzer können verwalten (Erstellen, Löschen, Ändern, explizites Starten, Beenden usw.). Windows Taskplaner aufgaben mithilfe des ScheduledTasks-PowerShell-Moduls.
-   Verwaltete Kennwörter: Administratoren können die verwalteten Active Directory-Kennwortkonten als Aufgabenprinzipale verwenden. Diese Aufgaben erfordern keine erzwungene Kennwortzurücksetzungsrichtlinie mehr.
-   API-Änderungen: Es wurden zwei neue Aufgabeneinstellungen mit der [**ITaskSettings3-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3) eingeführt.
    -   [**MaintenanceSettings:**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings)Tasks, die diese Einstellungen verwenden, werden als neue Art geplanter Aufgaben behandelt, die während der automatischen Wartung des Betriebssystems gemäß der angegebenen Periodizität und dem angegebenen Stichtag aufgerufen werden.
    -   [**Volatile:**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile)Aufgaben, die als flüchtig festgelegt sind, werden bei einem Betriebssystemstart immer deaktiviert und müssen bei Bedarf explizit wieder aktiviert werden. Flüchtige Tasks werden von den Failoverclustern verwendet, um sicherzustellen, dass nur eine Taskinstanz gleichzeitig in einem Cluster geplant wird.
-   Die einheitliche Zeitplanungs-Engine unterstützt jetzt die folgenden Features:
    -   S4U Logon-Typ über das [**LogonType-Element.**](taskschedulerschema-logontype-principaltype-element.md)
    -   XPath-Abfragewerte für Ereignistrigger über das [**ValueQueries-Element.**](taskschedulerschema-valuequeries-eventtriggertype-element.md)
    -   Lassen Sie keine harte Taskbeendung über das [**AllowHardTerminate-Element**](taskschedulerschema-allowhardterminate-settingstype-element.md) zu.
-   In dieser Version veraltete Features
    -   Aktion: [**sendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (Sie können [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) mit dem Cmdlet [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)[Send-MailMessage](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) als Problemumgehung verwenden).
    -   Aktion: [**showMessage**](taskschedulerschema-showmessage-actiongroup-element.md).
    -   AT.exe cmdline-Hilfsprogramm

## <a name="windows-7"></a>Windows 7

Die folgenden Taskplaner 2.0-Änderungen werden in Windows 7 eingeführt:

-   Verwenden der einheitlichen Zeitplanungs-Engine, die vom zugrunde liegenden Betriebssystem bereitgestellt wird.
-   Möglichkeit zum Ablehnen von Startaufgaben in RAIL-Sitzungen (Remote Applications Integrated Locally).
-   Sicherheitsmaßnahmen für Tasks (nur für Aufgaben, die als "NETWORK SERVICE" oder "LOCAL SERVICE" ausgeführt werden):

    -   Möglichkeit, einem Task einen Prozesstoken-Sicherheitsbezeichnertyp (z. B. uneingeschränkt oder keine) zu zuweisen.
    -   Ermöglichen Sie Es Taskentwicklern, den genauen Satz von Berechtigungen anfordern, den ihre Aufgabe erfordert.

-   API-Änderungen:

    -   Unterstützung der Tasksicherheitshärteung: Die neue Funktion zur Sicherheit von Aufgaben wird mit der neuen IPrincipal2-Schnittstelle eingeführt.
    -   Es wurden zwei neue Aufgabeneinstellungen mit der neuen ITaskSettings2-Schnittstelle eingeführt.

        -   DisallowStartOnRemoteAppSession: Die neue DisallowStartOnRemoteAppSession-Einstellung kann einen Taskstart ablehnen, wenn er in RAIL-Sitzungen [(Remote Applications Integrated Locally)](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546) ausgelöst wird.
        -   UseUnifiedSchedulingEngine: Die Verwendung der UseUnifiedSchedulingEngine-Einstellung bietet ein kohäsives Verhalten für Windows Tasks und Dienste, da sie auf einheitliche Weise von einer gemeinsamen systemweiten Planungs-Engine verwaltet wird. Obwohl die Verwendung einer einheitlichen Engine empfohlen wird, unterstützt sie einige der Taskplaner Features nicht. Wenn die Kombination von Eigenschaften die Ausführung der Aufgabe unter einer einheitlichen Engine nicht zu ermöglicht, wird die Registrierung einer solchen abgelehnt.
        -   Zu den Aufgabenfunktionen, die von der einheitlichen Zeitplanungs-Engine nicht unterstützt werden, gehören:

            -   Anmeldetypen:

                -   [INTERAKTIVES \_ TOKEN ODER KENNWORT FÜR DIE \_ \_ \_ \_ TASKANMELDUNG](./taskschedulerschema-logontype-principaltype-element.md)

            -   Richtlinie für mehrere Instanzen:

                -   [**\_TASKINSTANZEN \_ BEENDEN \_ VORHANDEN**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)

            -   Aktionen:

                -   [Senden von E-Mails](./taskschedulerschema-sendemail-actiongroup-element.md)
                -   [Meldung anzeigen](./taskschedulerschema-showmessage-actiongroup-element.md)

            -   Einstellungen:

                -   [Netzwerkeinstellungen für Aufgaben](./taskschedulerschema-networksettings-settingstype-element.md)
                -   [Task nicht hart beenden lassen](./taskschedulerschema-allowhardterminate-settingstype-element.md)

            -   Trigger:

                -   [Triggerausführungszeitlimit](./taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
                -   [Wiederholungsmuster für Kalendertrigger]( ./taskschedulerschema-repetition-triggerbasetype-element.md)
                -   [XPath-Abfragewerte für Ereignistrigger]( ./taskschedulerschema-valuequeries-eventtriggertype-element.md)
                -   [Triggertypen](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md) für monatliche und monatliche [Wochentage](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md)

## <a name="windows-vista"></a>Windows Vista

Die Taskplaner 2.0-API sollte bei der Entwicklung von Anwendungen verwendet werden, die den Taskplaner-Dienst auf Windows Vista verwenden. Weitere Informationen finden Sie unter [Taskplaner Referenz und](task-scheduler-reference.md) [Verwenden der Taskplaner](using-the-task-scheduler.md).

## <a name="windows-2000-windows-xp-and-windows-server-2003"></a>Windows 2000, Windows XP und Windows Server 2003

Die Taskplaner 2.0-API ist nicht verfügbar. Verwenden Taskplaner 1.0.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[Informationen zum Taskplaner](about-the-task-scheduler.md)
</dt> </dl>

 

 
