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
# <a name="whats-new-in-task-scheduler"></a><span data-ttu-id="4eee7-104">Neues in Taskplaner</span><span class="sxs-lookup"><span data-stu-id="4eee7-104">What's New in Task Scheduler</span></span>

<span data-ttu-id="4eee7-105">Die folgenden Änderungen fassen zusammen, welche Neuerungen in verschiedenen Versionen von Taskplaner sind.</span><span class="sxs-lookup"><span data-stu-id="4eee7-105">The following changes summarize what is new in different versions of Task Scheduler.</span></span>

## <a name="windows-10-and-windows-server-2016"></a><span data-ttu-id="4eee7-106">Windows 10 (und Windows Server 2016)</span><span class="sxs-lookup"><span data-stu-id="4eee7-106">Windows 10 (and Windows Server 2016)</span></span>

<span data-ttu-id="4eee7-107">Die folgenden Taskplaner Änderungen werden in Windows 10 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4eee7-107">The following Task Scheduler changes are introduced in Windows 10.</span></span>

-   <span data-ttu-id="4eee7-108">Wenn Akku Schoner eingeschaltet ist, werden Windows Taskplaner-Tasks nur ausgelöst, wenn die Aufgabe wie folgt lautet:</span><span class="sxs-lookup"><span data-stu-id="4eee7-108">When battery saver is on, Windows Task Scheduler tasks are triggered only if the task is:</span></span>

    -   <span data-ttu-id="4eee7-109">Nicht so festgelegt, dass **der Task nur gestartet wird, wenn sich der Computer im Leerlauf befindet...** (der Task verwendet nicht [**idlesettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings))</span><span class="sxs-lookup"><span data-stu-id="4eee7-109">Not set to **Start the task only if the computer is idle...** (task doesn't use [**IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings))</span></span>
    -   <span data-ttu-id="4eee7-110">Nicht für die automatische Wartung festgelegt (der Task verwendet keine [**maintenancesettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings))</span><span class="sxs-lookup"><span data-stu-id="4eee7-110">Not set to run during automatic maintenance (task doesn't use [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings))</span></span>
    -   <span data-ttu-id="4eee7-111">Ist so festgelegt, dass Sie **nur ausgeführt wird, wenn der Benutzer angemeldet ist** (Task [**logontype**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) ist **\_ interaktive Aufgaben Anmeldung \_ \_** oder **Task \_ Anmelde \_ Gruppe**)</span><span class="sxs-lookup"><span data-stu-id="4eee7-111">Is set to **Run only when user is logged on** (task [**LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) is **TASK\_LOGON\_INTERACTIVE\_TOKEN** or **TASK\_LOGON\_GROUP**)</span></span>

    <span data-ttu-id="4eee7-112">Alle anderen Trigger werden verzögert, bis Akku Schoner ausgeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="4eee7-112">All other triggers are delayed until battery saver is off.</span></span> <span data-ttu-id="4eee7-113">Weitere Informationen zum Zugreifen auf den Akku Schoner Status in Ihrer Anwendung finden Sie unter [**System \_ Energie \_ Status**](/windows/desktop/api/winbase/ns-winbase-system_power_status).</span><span class="sxs-lookup"><span data-stu-id="4eee7-113">For more information about accessing battery saver status in your application, see [**SYSTEM\_POWER\_STATUS**](/windows/desktop/api/winbase/ns-winbase-system_power_status).</span></span> <span data-ttu-id="4eee7-114">Allgemeine Informationen zum Akku Schoner finden Sie unter [Batterie Schoner (in den Richtlinien für die Hardwarekomponente)](/windows-hardware/design/component-guidelines/battery-saver).</span><span class="sxs-lookup"><span data-stu-id="4eee7-114">For general information about battery saver, see [battery saver (in the hardware component guidelines)](/windows-hardware/design/component-guidelines/battery-saver).</span></span>

-   <span data-ttu-id="4eee7-115">Aus Sicherheitsgründen kann ein Benutzer ohne Administratorrechte keine Windows Taskplaner-Aufgabe anzeigen und verwalten, die von einem anderen Benutzer erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4eee7-115">For security reasons, a non-administrator user cannot view nor manage a Windows Task Scheduler task that was created by another user.</span></span>

## <a name="windows-8"></a><span data-ttu-id="4eee7-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4eee7-116">Windows 8</span></span>

<span data-ttu-id="4eee7-117">Die folgenden Taskplaner 2,0-Änderungen werden in Windows 8 eingeführt:</span><span class="sxs-lookup"><span data-stu-id="4eee7-117">The following Task Scheduler 2.0 changes are introduced in Windows 8:</span></span>

-   <span data-ttu-id="4eee7-118">PowerShell-Unterstützung: Benutzer können verwalten (erstellen, löschen, ändern, explizit starten, abbrechen usw.) Windows Taskplaner Tasks mithilfe des PowerShell-Moduls scheduledtasks.</span><span class="sxs-lookup"><span data-stu-id="4eee7-118">Powershell support: users can manage (create, delete, modify, explicitly start, stop etc.) Windows Task Scheduler tasks using the ScheduledTasks powershell module.</span></span>
-   <span data-ttu-id="4eee7-119">Verwaltete Kenn Wörter: Administratoren können die Active Directory verwalteten Kenn Wort Konten als Aufgaben Prinzipale verwenden.</span><span class="sxs-lookup"><span data-stu-id="4eee7-119">Managed passwords: administrators can use the Active Directory managed password accounts as task principals.</span></span> <span data-ttu-id="4eee7-120">Diese Aufgaben erfordern keine erzwungene Richtlinie zum Zurücksetzen von Kenn Wörtern mehr.</span><span class="sxs-lookup"><span data-stu-id="4eee7-120">These tasks no longer require an enforced password reset policy.</span></span>
-   <span data-ttu-id="4eee7-121">API-Änderungen: in wurden zwei neue Aufgaben Einstellungen mit der [**ITaskSettings3**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3) -Schnittstelle eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4eee7-121">API changes: Introduced two new task settings with the [**ITaskSettings3**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3) interface.</span></span>
    -   <span data-ttu-id="4eee7-122">[**Maintenancesettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings): Tasks, die diese Einstellungen verwenden, werden als neuer Typ geplanter Aufgaben behandelt, die während der automatischen Wartungszeit des Betriebssystems entsprechend der angegebenen Periodizität und Frist aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4eee7-122">[**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings): tasks using these settings are treated as a new type of scheduled tasks that are invoked during OS automatic maintenance time, according to the specified periodicity and deadline.</span></span>
    -   <span data-ttu-id="4eee7-123">[**Flüchtig**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile): Tasks, die als flüchtig festgelegt sind, werden bei einem Betriebssystem Start immer deaktiviert und müssen bei Bedarf explizit wieder aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="4eee7-123">[**Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile): tasks that are set to be volatile are always disabled on an OS boot and must be explicitly re-enabled back when required.</span></span> <span data-ttu-id="4eee7-124">Flüchtige Tasks werden von den Failoverclustern verwendet, um sicherzustellen, dass jeweils nur eine Task Instanz in einem Cluster geplant wird.</span><span class="sxs-lookup"><span data-stu-id="4eee7-124">Volatile tasks are utilized by the failover clusters to ensure only one task instance is scheduled on a cluster at a time.</span></span>
-   <span data-ttu-id="4eee7-125">Die vereinheitlichte Planungs-Engine unterstützt jetzt die folgenden Features:</span><span class="sxs-lookup"><span data-stu-id="4eee7-125">The unified scheduling engine now supports the following features:</span></span>
    -   <span data-ttu-id="4eee7-126">S4U Logon Type, über das [**logontype**](taskschedulerschema-logontype-principaltype-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="4eee7-126">S4U Logon type, through the [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) element.</span></span>
    -   <span data-ttu-id="4eee7-127">XPath-Abfrage Werte für Ereignis Trigger durch das [**valuequeries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="4eee7-127">XPath query values for event triggers, through the [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) element.</span></span>
    -   <span data-ttu-id="4eee7-128">Erlauben Sie die Beendigung der Aufgabe nicht durch das Element " [**Zustellungs**](taskschedulerschema-allowhardterminate-settingstype-element.md) Element".</span><span class="sxs-lookup"><span data-stu-id="4eee7-128">Do not allow task hard terminate, through the [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md) element.</span></span>
-   <span data-ttu-id="4eee7-129">In dieser Version veraltete Features</span><span class="sxs-lookup"><span data-stu-id="4eee7-129">Features deprecated in this release</span></span>
    -   <span data-ttu-id="4eee7-130">Aktion: [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (Sie können [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) mit dem [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)-Cmdlet "[Send-Mail Message](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) " als Problem Umgehung verwenden).</span><span class="sxs-lookup"><span data-stu-id="4eee7-130">Action: [**sendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (you can use [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) with the [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)[Send-MailMessage](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) cmdlet as a workaround).</span></span>
    -   <span data-ttu-id="4eee7-131">Action: [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md).</span><span class="sxs-lookup"><span data-stu-id="4eee7-131">Action: [**showMessage**](taskschedulerschema-showmessage-actiongroup-element.md).</span></span>
    -   <span data-ttu-id="4eee7-132">AT.exe cmdline-Hilfsprogramm</span><span class="sxs-lookup"><span data-stu-id="4eee7-132">AT.exe cmdline utility</span></span>

## <a name="windows-7"></a><span data-ttu-id="4eee7-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4eee7-133">Windows 7</span></span>

<span data-ttu-id="4eee7-134">Die folgenden Taskplaner 2,0-Änderungen werden in Windows 7 eingeführt:</span><span class="sxs-lookup"><span data-stu-id="4eee7-134">The following Task Scheduler 2.0 changes are introduced in Windows 7:</span></span>

-   <span data-ttu-id="4eee7-135">Verwenden der vereinheitlichten Planungs-Engine, die vom zugrunde liegenden Betriebssystem bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4eee7-135">Using the unified scheduling engine provided by the underlying operating system.</span></span>
-   <span data-ttu-id="4eee7-136">Möglichkeit zum ablehnen von Start Tasks in lokalen Anwendungen, die lokal (Schiene) integriert sind.</span><span class="sxs-lookup"><span data-stu-id="4eee7-136">Ability to reject starting tasks in Remote Applications Integrated Locally (RAIL) sessions.</span></span>
-   <span data-ttu-id="4eee7-137">Task Sicherheitshärtung (für Tasks, die nur als "Netzwerkdienst" oder "lokaler Dienst" ausgeführt werden):</span><span class="sxs-lookup"><span data-stu-id="4eee7-137">Task security hardening (for tasks running as "NETWORK SERVICE" or "LOCAL SERVICE" only):</span></span>

    -   <span data-ttu-id="4eee7-138">Möglichkeit zum Zuweisen eines Sicherheitstokentyps für die Prozess Token (z. b. "uneingeschränkt" oder "keine") zu einer Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="4eee7-138">Ability to assign a process token security identifier (SID) type (for example, unrestricted or none) to a task.</span></span>
    -   <span data-ttu-id="4eee7-139">Erlauben Sie Aufgaben Entwicklern, den exakten Satz von Berechtigungen anzufordern, die ihre Aufgabe benötigt.</span><span class="sxs-lookup"><span data-stu-id="4eee7-139">Allow task developers to request the exact set of privileges that their task requires.</span></span>

-   <span data-ttu-id="4eee7-140">API-Änderungen:</span><span class="sxs-lookup"><span data-stu-id="4eee7-140">API changes:</span></span>

    -   <span data-ttu-id="4eee7-141">Unterstützung der Unterstützung der Sicherheit: das neue Feature zur Sicherheitshärtung wird mit der neuen IPrincipal2-Schnittstelle eingeführt</span><span class="sxs-lookup"><span data-stu-id="4eee7-141">Task security hardening support: new task security hardening feature is introduced with new IPrincipal2 interface.</span></span>
    -   <span data-ttu-id="4eee7-142">In wurden zwei neue Aufgaben Einstellungen mit der neuen ITaskSettings2-Schnittstelle eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4eee7-142">Introduced two new task settings with the new ITaskSettings2 interface.</span></span>

        -   <span data-ttu-id="4eee7-143">Disallowstartonremoteappsession: die neue disallowstartonremoteappsession-Einstellung kann einen Task Start ablehnen, wenn Sie in [lokal (in der lokalen Sitzung) integrierten Remote Anwendungen](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546) ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="4eee7-143">DisallowStartOnRemoteAppSession: The new DisallowStartOnRemoteAppSession setting can reject a task start if triggered in [Remote Applications Integrated Locally (RAIL)](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546) sessions.</span></span>
        -   <span data-ttu-id="4eee7-144">Useunifiedschedulingengine: mithilfe der Einstellung useunifiedschedulingengine wird ein zusammenhängendes Verhalten für Windows-Tasks und-Dienste bereitstellt, da es auf einheitliche Weise durch eine gängige systemweite Planungs-Engine verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="4eee7-144">UseUnifiedSchedulingEngine: Using the UseUnifiedSchedulingEngine setting provides a cohesive behavior for Windows Tasks and Services because it is being managed in a uniform manner by a common system-wide scheduling engine.</span></span> <span data-ttu-id="4eee7-145">Obwohl die Verwendung eines vereinheitlichten Moduls empfohlen wird, werden einige der Taskplaner Features nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4eee7-145">Although using a unified engine is recommended, it does not support some of the Task Scheduler features.</span></span> <span data-ttu-id="4eee7-146">Wenn die Kombination der Eigenschaften das Ausführen der Aufgabe unter einem vereinheitlichten Modul nicht zulässt, wird die Registrierung dieser solchen abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="4eee7-146">If the combination of properties will not allow running of the task under a unified engine, the registration of such will be rejected.</span></span>
        -   <span data-ttu-id="4eee7-147">Zu den Aufgaben Features, die von der Unified Scheduling-Engine nicht unterstützt werden, gehören:</span><span class="sxs-lookup"><span data-stu-id="4eee7-147">The task features that are not supported by the unified scheduling engine include:</span></span>

            -   <span data-ttu-id="4eee7-148">Anmelde Typen:</span><span class="sxs-lookup"><span data-stu-id="4eee7-148">Logon types:</span></span>

                -   [<span data-ttu-id="4eee7-149">\_ \_ interaktives \_ Token \_ oder \_ Kennwort für die Task Anmeldung</span><span class="sxs-lookup"><span data-stu-id="4eee7-149">TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD</span></span>](./taskschedulerschema-logontype-principaltype-element.md)

            -   <span data-ttu-id="4eee7-150">Richtlinie für mehrere Instanzen:</span><span class="sxs-lookup"><span data-stu-id="4eee7-150">Multiple instance policy:</span></span>

                -   [<span data-ttu-id="4eee7-151">**Task \_ Instanzen \_ beendet \_ vorhandene**</span><span class="sxs-lookup"><span data-stu-id="4eee7-151">**TASK\_INSTANCES\_STOP\_EXISTING**</span></span>](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)

            -   <span data-ttu-id="4eee7-152">Aktionen:</span><span class="sxs-lookup"><span data-stu-id="4eee7-152">Actions:</span></span>

                -   [<span data-ttu-id="4eee7-153">Senden von E-Mails</span><span class="sxs-lookup"><span data-stu-id="4eee7-153">Send email</span></span>](./taskschedulerschema-sendemail-actiongroup-element.md)
                -   [<span data-ttu-id="4eee7-154">Meldung anzeigen</span><span class="sxs-lookup"><span data-stu-id="4eee7-154">Display message</span></span>](./taskschedulerschema-showmessage-actiongroup-element.md)

            -   <span data-ttu-id="4eee7-155">Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="4eee7-155">Settings:</span></span>

                -   [<span data-ttu-id="4eee7-156">Task Netzwerkeinstellungen</span><span class="sxs-lookup"><span data-stu-id="4eee7-156">Task network settings</span></span>](./taskschedulerschema-networksettings-settingstype-element.md)
                -   [<span data-ttu-id="4eee7-157">Aufgabe nicht schwer beenden</span><span class="sxs-lookup"><span data-stu-id="4eee7-157">Do not allow task hard terminate</span></span>](./taskschedulerschema-allowhardterminate-settingstype-element.md)

            -   <span data-ttu-id="4eee7-158">Trigger:</span><span class="sxs-lookup"><span data-stu-id="4eee7-158">Triggers:</span></span>

                -   [<span data-ttu-id="4eee7-159">Zeitlimit für die Triggerausführung</span><span class="sxs-lookup"><span data-stu-id="4eee7-159">Trigger execution time limit</span></span>](./taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
                -   [<span data-ttu-id="4eee7-160">Wiederholungsmuster für Kalender Trigger</span><span class="sxs-lookup"><span data-stu-id="4eee7-160">Repetition patterns for calendar triggers</span></span>]( ./taskschedulerschema-repetition-triggerbasetype-element.md)
                -   [<span data-ttu-id="4eee7-161">XPath-Abfrage Werte für Ereignis Trigger</span><span class="sxs-lookup"><span data-stu-id="4eee7-161">XPath query values for event triggers</span></span>]( ./taskschedulerschema-valuequeries-eventtriggertype-element.md)
                -   <span data-ttu-id="4eee7-162">[Monatliche](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md) und [monatliche Day-of-week](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) -Auslösertypen</span><span class="sxs-lookup"><span data-stu-id="4eee7-162">[Monthly](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md) and [Monthly day-of-week](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) trigger types</span></span>

## <a name="windows-vista"></a><span data-ttu-id="4eee7-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4eee7-163">Windows Vista</span></span>

<span data-ttu-id="4eee7-164">Die Taskplaner 2,0-API sollte zum Entwickeln von Anwendungen verwendet werden, die den Taskplaner-Dienst unter Windows Vista verwenden.</span><span class="sxs-lookup"><span data-stu-id="4eee7-164">The Task Scheduler 2.0 API should be used in developing applications that use the Task Scheduler service on Windows Vista.</span></span> <span data-ttu-id="4eee7-165">Weitere Informationen finden Sie unter [Taskplaner Referenz](task-scheduler-reference.md) und [Verwenden der Taskplaner](using-the-task-scheduler.md).</span><span class="sxs-lookup"><span data-stu-id="4eee7-165">For more information, see [Task Scheduler Reference](task-scheduler-reference.md) and [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

## <a name="windows-2000-windows-xp-and-windows-server-2003"></a><span data-ttu-id="4eee7-166">Windows 2000, Windows XP und Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4eee7-166">Windows 2000, Windows XP, and Windows Server 2003</span></span>

<span data-ttu-id="4eee7-167">Die Taskplaner 2,0-API ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4eee7-167">The Task Scheduler 2.0 API is not available.</span></span> <span data-ttu-id="4eee7-168">Verwenden Sie Taskplaner 1,0.</span><span class="sxs-lookup"><span data-stu-id="4eee7-168">Use Task Scheduler 1.0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4eee7-169">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4eee7-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4eee7-170">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="4eee7-170">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="4eee7-171">Informationen zum Taskplaner</span><span class="sxs-lookup"><span data-stu-id="4eee7-171">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 
