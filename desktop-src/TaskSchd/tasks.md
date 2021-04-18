---
title: Aufgaben
description: Eine Aufgabe ist die geplante Arbeit, die der Taskplaner-Dienst ausführt.
ms.assetid: 24c43834-5731-4b14-9409-7d7cf20b1a71
keywords:
- Aufgaben Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbb4ef41915ec70c98b59c9a7ba74c00f283ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337390"
---
# <a name="tasks"></a><span data-ttu-id="cbd09-104">Aufgaben</span><span class="sxs-lookup"><span data-stu-id="cbd09-104">Tasks</span></span>

<span data-ttu-id="cbd09-105">Eine Aufgabe ist die geplante Arbeit, die der Taskplaner-Dienst ausführt.</span><span class="sxs-lookup"><span data-stu-id="cbd09-105">A task is the scheduled work that the Task Scheduler service performs.</span></span> <span data-ttu-id="cbd09-106">Eine Aufgabe besteht aus verschiedenen Komponenten, aber eine Aufgabe muss einen-Triggern enthalten, den der Taskplaner verwendet, um die Aufgabe zu starten, und eine Aktion, die beschreibt, welche Arbeit der Taskplaner ausführt.</span><span class="sxs-lookup"><span data-stu-id="cbd09-106">A task is composed of different components, but a task must contain a trigger that the Task Scheduler uses to start the task and an action that describes what work the Task Scheduler will perform.</span></span>

<span data-ttu-id="cbd09-107">Wenn eine Aufgabe erstellt wird, wird Sie in einem Aufgaben Ordner gespeichert.</span><span class="sxs-lookup"><span data-stu-id="cbd09-107">When a task is created, it is stored in a task folder.</span></span> <span data-ttu-id="cbd09-108">Auf Aufgaben Ordner kann über die [**ITaskFolder**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder) -Schnittstelle ([**taskfolder**](taskfolder.md) für die Skripterstellung) zugegriffen werden, und auf Aufgaben kann über die [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) -Schnittstelle ([**registeredtask**](registeredtask.md) für die Skripterstellung) zugegriffen werden, wenn Sie erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="cbd09-108">Task folders can be accessed through the [**ITaskFolder**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder) interface ([**TaskFolder**](taskfolder.md) for scripting), and tasks can be accessed through the [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) interface ([**RegisteredTask**](registeredtask.md) for scripting) when they are created.</span></span> <span data-ttu-id="cbd09-109">Sie können Zugriffs Steuerungs Listen (Access Control Lists, ACLs) für Aufgaben und Aufgaben Ordner ändern, um bestimmten Benutzern und Gruppen den Zugriff auf einen Task-oder Aufgaben Ordner zu gewähren oder zu verweigern.</span><span class="sxs-lookup"><span data-stu-id="cbd09-109">You can change access control lists (ACLs) for tasks and task folders in order to grant or deny certain users and groups access to a task or task folder.</span></span> <span data-ttu-id="cbd09-110">Dies kann mithilfe der [**IRegisteredTask:: SETSECURITYDESCRIPTOR**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor) -Methode, der [**ITaskFolder:: SETSECURITYDESCRIPTOR**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor) -Methode oder durch Angeben einer Sicherheits Beschreibung erfolgen, wenn eine Aufgabe mithilfe der [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) -Methode oder der [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) -Methode registriert wird.</span><span class="sxs-lookup"><span data-stu-id="cbd09-110">This can be done by using the [**IRegisteredTask::SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor) method, the [**ITaskFolder::SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor) method, or by specifying a security descriptor when a task is registered by using the [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) or [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) method.</span></span>

> [!Note]  
> <span data-ttu-id="cbd09-111">Wenn dem lokalen System Konto der Zugriff auf eine Aufgaben Datei oder einen Aufgaben Ordner verweigert wird, kann der Taskplaner Dienst unerwartete Ergebnisse liefern.</span><span class="sxs-lookup"><span data-stu-id="cbd09-111">If the Local System account is denied access to a task file or task folder, then the Task Scheduler service can produce unexpected results.</span></span>

 

## <a name="components-of-a-task"></a><span data-ttu-id="cbd09-112">Komponenten einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="cbd09-112">Components of a Task</span></span>

<span data-ttu-id="cbd09-113">In der folgenden Abbildung sind die Aufgaben Komponenten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="cbd09-113">The following illustration shows the task components.</span></span>

![Task Komponenten](images/taskcomponents.png)

<span data-ttu-id="cbd09-115">Die folgende Liste enthält eine kurze Beschreibung der einzelnen Aufgaben Komponenten:</span><span class="sxs-lookup"><span data-stu-id="cbd09-115">The following list contains a brief description of each task component:</span></span>

-   <span data-ttu-id="cbd09-116">Trigger: Taskplaner verwendet Ereignis-oder zeitbasierte Trigger, um zu erfahren, wann eine Aufgabe gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cbd09-116">Triggers: Task Scheduler uses event or time-based triggers to know when to start a task.</span></span> <span data-ttu-id="cbd09-117">Jeder Task kann einen oder mehrere Trigger zum Starten der Aufgabe angeben.</span><span class="sxs-lookup"><span data-stu-id="cbd09-117">Every task can specify one or more triggers to start the task.</span></span>

    <span data-ttu-id="cbd09-118">Weitere Informationen zu Triggern finden Sie unter [Task Trigger](task-triggers.md).</span><span class="sxs-lookup"><span data-stu-id="cbd09-118">For more information about triggers, see [Task Triggers](task-triggers.md).</span></span>

-   <span data-ttu-id="cbd09-119">Aktionen: Dies sind die Aktionen, die von der Aufgabe durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cbd09-119">Actions: These are the actions, the actual work, that is performed by the task.</span></span> <span data-ttu-id="cbd09-120">Jeder Task kann eine oder mehrere Aktionen angeben, um seine Arbeit abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="cbd09-120">Every task can specify one or more actions to complete its work.</span></span>

    <span data-ttu-id="cbd09-121">Weitere Informationen zu Aktionen finden Sie unter [Task Actions](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="cbd09-121">For more information about actions, see [Task Actions](task-actions.md).</span></span>

-   <span data-ttu-id="cbd09-122">Prinzipale: Prinzipale definieren den Sicherheitskontext, in dem die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cbd09-122">Principals: Principals define the security context in which the task is run.</span></span> <span data-ttu-id="cbd09-123">Ein Prinzipal könnte z. b. einen bestimmten Benutzer oder eine Benutzergruppe definieren, die die Aufgabe ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="cbd09-123">For example, a principal might define a specific user or user group that can run the task.</span></span>

    <span data-ttu-id="cbd09-124">Weitere Informationen zu Prinzipale finden Sie unter [Sicherheits Kontexte für Aufgaben](security-contexts-for-running-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="cbd09-124">For more information about principals, see [Security Contexts for Tasks](security-contexts-for-running-tasks.md).</span></span>

-   <span data-ttu-id="cbd09-125">Einstellungen: Dies sind die Einstellungen, die von der Taskplaner verwendet werden, um die Aufgabe in Bezug auf Bedingungen auszuführen, die sich außerhalb der Aufgabe selbst befinden.</span><span class="sxs-lookup"><span data-stu-id="cbd09-125">Settings: These are the settings that the Task Scheduler uses to run the task with respect to conditions that are external to the task itself.</span></span> <span data-ttu-id="cbd09-126">Diese Einstellungen können z. b. die Priorität der Aufgabe in Bezug auf andere Aufgaben angeben, unabhängig davon, ob mehrere Instanzen der Aufgabe ausgeführt werden können, wie die Aufgabe behandelt wird, wenn sich der Computer in einem Leerlaufzustand befindet, und andere Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="cbd09-126">For example, these settings can specify the priority of the task with respect to other tasks, whether multiple instances of the task can be run, how the task is handled when the computer is in an idle condition, and other conditions.</span></span>

    <span data-ttu-id="cbd09-127">Weitere Informationen zu Aufgaben Einstellungen finden Sie unter [**itasksettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) ([**tasksettings**](tasksettings.md) für Skripterstellung).</span><span class="sxs-lookup"><span data-stu-id="cbd09-127">For more information about task settings, see [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) ([**TaskSettings**](tasksettings.md) for scripting).</span></span>

    > [!Note]  
    > <span data-ttu-id="cbd09-128">Standardmäßig wird eine Aufgabe 72 Stunden nach dem Start angehalten.</span><span class="sxs-lookup"><span data-stu-id="cbd09-128">By default, a task will be stopped 72 hours after it starts to run.</span></span> <span data-ttu-id="cbd09-129">Sie können dies ändern, indem Sie die Einstellung [**executiontimelimit**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit) ändern.</span><span class="sxs-lookup"><span data-stu-id="cbd09-129">You can change this by changing the [**ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit) setting.</span></span>

     

-   <span data-ttu-id="cbd09-130">Registrierungsinformationen: Hierbei handelt es sich um administrative Informationen, die gesammelt werden, wenn der Task registriert wird.</span><span class="sxs-lookup"><span data-stu-id="cbd09-130">Registration Information: This is administrative information that is gathered when the task is registered.</span></span> <span data-ttu-id="cbd09-131">Diese Informationen beschreiben beispielsweise den Autor der Aufgabe, das Datum, an dem die Aufgabe registriert wurde, eine XML-Beschreibung des Tasks und weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="cbd09-131">For example, this information describes the author of the task, the date when the task was registered, an XML description of the task, and other information.</span></span>

    <span data-ttu-id="cbd09-132">Weitere Informationen zu Aufgaben Registrierungsinformationen finden Sie unter [Aufgaben Registrierungsinformationen](task-registration-information.md).</span><span class="sxs-lookup"><span data-stu-id="cbd09-132">For more information about task registration information, see [Task Registration Information](task-registration-information.md).</span></span>

-   <span data-ttu-id="cbd09-133">Daten: Dies ist eine zusätzliche Dokumentation zu der Aufgabe, die vom Autor der Aufgabe bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cbd09-133">Data: This is additional documentation about the task that is supplied by the author of the task.</span></span> <span data-ttu-id="cbd09-134">Diese Daten können z. b. XML-Hilfe enthalten, die von Benutzern verwendet werden kann, wenn Sie die Aufgabe ausführen.</span><span class="sxs-lookup"><span data-stu-id="cbd09-134">For example, this data may contain XML Help that can be used by users when they run the task.</span></span>

## <a name="task-apis"></a><span data-ttu-id="cbd09-135">Task-APIs</span><span class="sxs-lookup"><span data-stu-id="cbd09-135">Task APIs</span></span>

<span data-ttu-id="cbd09-136">Taskplaner 2,0 stellt zwei Sätze von APIs bereit: einen Satz von Skript Objekten und Schnittstellen für Taskplaner 2,0.</span><span class="sxs-lookup"><span data-stu-id="cbd09-136">Task Scheduler 2.0 provides two sets of APIs: a set of scripting objects and interfaces for Task Scheduler 2.0.</span></span> <span data-ttu-id="cbd09-137">Weitere Informationen finden Sie unter [Taskplaner Referenz](task-scheduler-reference.md).</span><span class="sxs-lookup"><span data-stu-id="cbd09-137">For more information, see [Task Scheduler Reference](task-scheduler-reference.md).</span></span>

<span data-ttu-id="cbd09-138">Die mit der [**Compatibility**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) -Eigenschaft festgelegte Task Kompatibilität sollte nur auf Task Kompatibilität v1 festgelegt werden, \_ \_ Wenn ein Task auf einen Computer unter Windows XP, Windows Server 2003 oder Windows 2000 zugegriffen werden muss oder geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="cbd09-138">Task compatibility, which is set through the [**Compatibility**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) property, should only be set to TASK\_COMPATIBILITY\_V1 if a task must be accessed or modified from a Windows XP, Windows Server 2003, or Windows 2000 computer.</span></span> <span data-ttu-id="cbd09-139">Andernfalls empfiehlt es sich, die Kompatibilität mit Taskplaner 2,0 zu verwenden, da Sie mehr Features hat.</span><span class="sxs-lookup"><span data-stu-id="cbd09-139">Otherwise, it is recommended that you use Task Scheduler 2.0 compatibility because it has more features.</span></span>

<span data-ttu-id="cbd09-140">Ab Taskplaner 2,0 wird die [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) -Schnittstelle ([**Task Service**](taskservice.md) für die Skripterstellung) als Ausgangspunkt zum Erstellen von Aufgaben in den angegebenen Ordnern verwendet.</span><span class="sxs-lookup"><span data-stu-id="cbd09-140">Starting with Task Scheduler 2.0, the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) interface ([**TaskService**](taskservice.md) for scripting) is used as a starting point to create tasks in specified folders.</span></span> <span data-ttu-id="cbd09-141">Die [**itaskdefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) -Schnittstelle ([**Task Definition**](taskdefinition.md) für die Skripterstellung) wird verwendet, um alle Komponenten einer Aufgabe (z. b. Einstellungen, Aktionen und Trigger) zu speichern.</span><span class="sxs-lookup"><span data-stu-id="cbd09-141">The [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) interface ([**TaskDefinition**](taskdefinition.md) for scripting) is used to hold all the components of a task, such as the settings, actions, and triggers.</span></span> <span data-ttu-id="cbd09-142">Die [**itasktrigger-**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger), [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction)-und [**itasksettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) -APIs stellen Eigenschaften bereit, die dann verwendet werden, um die anderen Komponenten der Aufgabe zu definieren.</span><span class="sxs-lookup"><span data-stu-id="cbd09-142">The [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger), [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction), and [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) APIs provide properties that are then used to define the other components of the task.</span></span> <span data-ttu-id="cbd09-143">Taskplaner 1,0 stellt die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle bereit, die nur aus Gründen der Abwärtskompatibilität unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="cbd09-143">Task Scheduler 1.0 provides the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface, which is supported only for backward compatibility.</span></span>

<span data-ttu-id="cbd09-144">Bei der Skripterstellung werden die Taskplaner Schnittstellen Skript Objekten mit ähnlichen Namen, Eigenschaften und Methoden zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="cbd09-144">For scripting, the Task Scheduler interfaces map to scripting objects that have the similar names, properties, and methods.</span></span> <span data-ttu-id="cbd09-145">Das [**TaskService**](taskservice.md) -Skript Objekt hat z. b. die gleichen Eigenschaften und Methoden wie die [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cbd09-145">For example, the [**TaskService**](taskservice.md) scripting object has the same properties and methods as the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) interface.</span></span>

<span data-ttu-id="cbd09-146">Weitere Informationen und Beispiele zur Verwendung der Taskplaner Schnittstellen, Skript Objekte und XML finden [Sie unter Verwenden der Taskplaner](using-the-task-scheduler.md).</span><span class="sxs-lookup"><span data-stu-id="cbd09-146">For more information and examples about how to use the Task Scheduler interfaces, scripting objects, and XML, see [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

### <a name="task-scheduler-10-tasks"></a><span data-ttu-id="cbd09-147">Taskplaner 1,0 Tasks</span><span class="sxs-lookup"><span data-stu-id="cbd09-147">Task Scheduler 1.0 Tasks</span></span>

<span data-ttu-id="cbd09-148">Eine Taskplaner 1,0-Aufgabe ist jede Anwendung oder jeder Dateityp, die von der Taskplaner ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cbd09-148">A Task Scheduler 1.0 task is any application or file type that the Task Scheduler can execute.</span></span> <span data-ttu-id="cbd09-149">Diese können Folgendes umfassen (wie von dem Betriebssystem unterstützt, auf dem der Task ausgeführt wird): Win32-Anwendungen, Win16-Anwendungen, OS/2-Anwendungen, MS-DOS-Anwendungen, Batch Dateien ( \* bat), Befehls Dateien ( \* . cmd) oder ein beliebiger ordnungsgemäß registrierter Dateityp.</span><span class="sxs-lookup"><span data-stu-id="cbd09-149">These may include any of the following (as supported by the operating system on which the task will execute): Win32 applications, Win16 applications, OS/2 applications, MS-DOS applications, batch files (\*.bat), command files (\*.cmd), or any properly registered file type.</span></span>

<span data-ttu-id="cbd09-150">Daten, die eine Aufgabe beschreiben, werden in einer Aufgaben Datei gespeichert, die im Ordner "geplante Aufgaben" gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="cbd09-150">Data that describes a task is kept in a task file that is stored in the Scheduled Tasks folder.</span></span> <span data-ttu-id="cbd09-151">Weitere Informationen finden Sie im [*Ordner "geplante Aufgaben*](s.md)".</span><span class="sxs-lookup"><span data-stu-id="cbd09-151">For more information, see [*Scheduled Tasks folder*](s.md).</span></span> <span data-ttu-id="cbd09-152">Der Name dieser Aufgaben Dateien enthält den Namen der Aufgabe, gefolgt von der Dateinamenerweiterung. Job.</span><span class="sxs-lookup"><span data-stu-id="cbd09-152">The name of these task files include the name of the task, followed by a .job file name extension.</span></span>

<span data-ttu-id="cbd09-153">Weitere Informationen zum Hinzufügen von Taskplaner 1,0-Tasks finden Sie unter [Hinzufügen von Arbeits Elementen](adding-work-items.md).</span><span class="sxs-lookup"><span data-stu-id="cbd09-153">For more information about adding Task Scheduler 1.0 tasks, see [Adding Work Items](adding-work-items.md).</span></span>

<span data-ttu-id="cbd09-154">Weitere Informationen zum Auflisten von Taskplaner 1,0-Tasks finden Sie unter Auflisten von [Tasks](enumerating-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="cbd09-154">For more information about enumerating through Task Scheduler 1.0 tasks, see [Enumerating Tasks](enumerating-tasks.md).</span></span>

<span data-ttu-id="cbd09-155">Für einen Computer mit Windows Server 2003, Windows XP oder Windows 2000 zum Erstellen, überwachen oder Steuern von Aufgaben auf einem Computer mit Windows Vista müssen die folgenden Vorgänge auf dem Computer mit Windows Vista ausgeführt werden, und der Benutzer, der die [**itaskscheduler:: settargetcomputer**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-settargetcomputer) -Methode aufgerufen hat, muss ein Mitglied der Gruppe "Administratoren" auf dem Windows Vista-Remote Computer sein.</span><span class="sxs-lookup"><span data-stu-id="cbd09-155">For a Windows Server 2003, Windows XP, or Windows 2000 computer to create, monitor, or control tasks on a Windows Vista computer, the following operations should be completed on the Windows Vista computer, and the user who is calling the [**ITaskScheduler::SetTargetComputer**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-settargetcomputer) method must be a member of the Administrators group on the remote Windows Vista computer.</span></span>

<span data-ttu-id="cbd09-156">**So aktivieren Sie die Ausnahme "Datei und Drucker freigeben" in der Windows-Firewall**</span><span class="sxs-lookup"><span data-stu-id="cbd09-156">**To enable the "Share File and Printers" exception in Windows Firewall**</span></span>

1.  <span data-ttu-id="cbd09-157">Klicken Sie auf **Start** und dann auf **Systemsteuerung**.</span><span class="sxs-lookup"><span data-stu-id="cbd09-157">Click **Start**, and then click **Control Panel**.</span></span>
2.  <span data-ttu-id="cbd09-158">Klicken Sie in der **Systemsteuerung** auf **klassische Ansicht** , und doppelklicken Sie dann auf das Symbol **Windows-Firewall** .</span><span class="sxs-lookup"><span data-stu-id="cbd09-158">In **Control Panel**, click **Classic View** and then double-click the **Windows Firewall** icon.</span></span>
3.  <span data-ttu-id="cbd09-159">Klicken Sie im Fenster **Windows-Firewall** auf die Registerkarte **Ausnahmen** , und aktivieren Sie das Kontrollkästchen **Datei-und Druckerfreigabe Ausnahme** .</span><span class="sxs-lookup"><span data-stu-id="cbd09-159">In the **Windows Firewall** window, click the **Exceptions** tab and select **File and Printer Sharing exception** check box.</span></span>

<span data-ttu-id="cbd09-160">**So aktivieren Sie den Dienst "Remote Registrierung"**</span><span class="sxs-lookup"><span data-stu-id="cbd09-160">**To enable the "Remote Registry" service**</span></span>

-   <span data-ttu-id="cbd09-161">Öffnen Sie ein Eingabe Aufforderungs Fenster, und geben Sie den folgenden Befehl ein: **net Start "Remote Registry"**.</span><span class="sxs-lookup"><span data-stu-id="cbd09-161">Open a Command Prompt window and enter the following command: **net start "Remote Registry"**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbd09-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cbd09-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbd09-163">Informationen zum Taskplaner</span><span class="sxs-lookup"><span data-stu-id="cbd09-163">About the Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> <dt>

[<span data-ttu-id="cbd09-164">Task Trigger</span><span class="sxs-lookup"><span data-stu-id="cbd09-164">Task Triggers</span></span>](task-triggers.md)
</dt> <dt>

[<span data-ttu-id="cbd09-165">Task Aktionen</span><span class="sxs-lookup"><span data-stu-id="cbd09-165">Task Actions</span></span>](task-actions.md)
</dt> <dt>

[<span data-ttu-id="cbd09-166">**Itaskdefinition**</span><span class="sxs-lookup"><span data-stu-id="cbd09-166">**ITaskDefinition**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
</dt> <dt>

[<span data-ttu-id="cbd09-167">**Task Definition**</span><span class="sxs-lookup"><span data-stu-id="cbd09-167">**TaskDefinition**</span></span>](taskdefinition.md)
</dt> <dt>

[<span data-ttu-id="cbd09-168">**ITaskService**</span><span class="sxs-lookup"><span data-stu-id="cbd09-168">**ITaskService**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)
</dt> <dt>

[<span data-ttu-id="cbd09-169">**Task Service**</span><span class="sxs-lookup"><span data-stu-id="cbd09-169">**TaskService**</span></span>](taskservice.md)
</dt> </dl>

 

 




