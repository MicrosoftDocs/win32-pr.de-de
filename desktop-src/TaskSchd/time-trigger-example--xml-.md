---
title: Beispiel für Zeit Auslösung (XML)
description: Der XML-Code in diesem Beispiel definiert einen Task, der den Editor zu einem bestimmten Zeitpunkt startet.
ms.assetid: dde3627b-e268-45ef-9c26-08877bfe484f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c683c831aa3a07eeb3a41db9cd2768caeb6307a
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/24/2020
ms.locfileid: "104314051"
---
# <a name="time-trigger-example-xml"></a><span data-ttu-id="ca53a-103">Beispiel für Zeit Auslösung (XML)</span><span class="sxs-lookup"><span data-stu-id="ca53a-103">Time Trigger Example (XML)</span></span>

<span data-ttu-id="ca53a-104">Der XML-Code in diesem Beispiel definiert einen Task, der den Editor zu einem bestimmten Zeitpunkt startet.</span><span class="sxs-lookup"><span data-stu-id="ca53a-104">The XML in this example defines a task that starts Notepad at a specific time.</span></span>

<span data-ttu-id="ca53a-105">Zum Registrieren einer Aufgabe, die in XML definiert ist, können Sie entweder die [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) -Funktion ([**taskfolder. RegisterTask**](taskfolder-registertask.md) für die Skripterstellung) oder das Befehlszeilen Tool Schtasks.exe verwenden.</span><span class="sxs-lookup"><span data-stu-id="ca53a-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="ca53a-106">Wenn Sie das Schtasks.exe Tool (das sich im Verzeichnis "C: \\ Windows System32" befindet \\ ) verwenden, können Sie den folgenden Befehl verwenden, um den Task zu registrieren: **Schtasks/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="ca53a-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-at-a-specific-time"></a><span data-ttu-id="ca53a-107">So definieren Sie einen Task zum Starten von Notepad zu einem bestimmten Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="ca53a-107">To define a task to start Notepad at a specific time</span></span>

<span data-ttu-id="ca53a-108">Im folgenden XML-Beispiel wird gezeigt, wie eine Aufgabe mit einer einzelnen Ausführungs Aktion (Starten von Editor), einem einmaligen Triggertyp, der die Aufgabe zu einem bestimmten Zeitpunkt startet, und mehreren anderen Aufgaben Einstellungen definiert wird, die sich auf die Behandlung der Aufgabe durch die Taskplaner auswirken.</span><span class="sxs-lookup"><span data-stu-id="ca53a-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single time trigger that starts the task at a specified time, and several other task settings that affect how the task is handled by the Task Scheduler.</span></span>


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe at a specific time.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Task starts after at a specified time.</Description>
    </RegistrationInfo>
    <Triggers>
        <TimeTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <ExecutionTimeLimit>PT5M</ExecutionTimeLimit>
        </TimeTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <UserId>Administrator</UserId>
            <LogonType>InteractiveToken</LogonType>
        </Principal>
    </Principals>
    <Settings>
        <Enabled>true</Enabled>
        <AllowStartOnDemand>true</AllowStartOnDemand>
        <AllowHardTerminate>true</AllowHardTerminate>
    </Settings>
    <Actions>
        <Exec>
            <Command>notepad.exe</Command>
        </Exec>
    </Actions>
</Task>
```



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="ca53a-109">TaskScheduler-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="ca53a-109">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="ca53a-110">Im folgenden finden Sie einige wichtige Punkte, die Sie berücksichtigen sollten, wenn Sie dieses Beispiel verwenden:</span><span class="sxs-lookup"><span data-stu-id="ca53a-110">The following are some important elements to keep in mind when using this example:</span></span>

-   <span data-ttu-id="ca53a-111">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): enthält Registrierungsinformationen zum Task.</span><span class="sxs-lookup"><span data-stu-id="ca53a-111">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="ca53a-112">[**Trigger**](taskschedulerschema-triggers-tasktype-element.md): definiert den Trigger, der den Task startet.</span><span class="sxs-lookup"><span data-stu-id="ca53a-112">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="ca53a-113">[**Timetimeout**](taskschedulerschema-timetrigger-triggergroup-element.md): definiert den Zeit--Auslösers.</span><span class="sxs-lookup"><span data-stu-id="ca53a-113">[**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md): Defines the time trigger.</span></span> <span data-ttu-id="ca53a-114">In diesem Fall werden drei untergeordnete Elemente verwendet: die Start-und endgrenzen, die angeben, wann der-Triggervorgang aktiviert und deaktiviert wird, und das Ausführungszeit Limit, das die maximale Zeitspanne angibt, in der die Aufgabe vom-Triggern gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ca53a-114">In this case, three child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, and the execution time limit that specifies the maximum amount of time in which the task can be started by the trigger.</span></span> <span data-ttu-id="ca53a-115">Das [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) -Element ist ein erforderliches Element für Zeit Trigger.</span><span class="sxs-lookup"><span data-stu-id="ca53a-115">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time triggers.</span></span>
-   <span data-ttu-id="ca53a-116">[**Prinzipal**](taskschedulerschema-principal-principaltype-element.md): definiert den Sicherheitskontext, unter dem eine Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca53a-116">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="ca53a-117">[**Einstellungen**](taskschedulerschema-settings-tasktype-element.md): definiert die Aufgaben Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ca53a-117">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="ca53a-118">[**Aktionen**](taskschedulerschema-actions-tasktype-element.md): definiert die Aktionen, die der Task ausführt (in diesem Fall das Ausführen von Notepad).</span><span class="sxs-lookup"><span data-stu-id="ca53a-118">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions that the task performs (in this case, running Notepad).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca53a-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ca53a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca53a-120">Verwenden des Taskplaner</span><span class="sxs-lookup"><span data-stu-id="ca53a-120">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




