---
title: Beispiel eines LOGON-Auslösers (XML)
description: Der XML-Code in diesem Beispiel definiert einen Task, der den Editor startet, wenn sich ein Benutzer anmeldet.
ms.assetid: c1cce95f-7558-489e-b092-c82d55b42165
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d66766ce4cae33c3526ac9d30071ff2082ddc1f2
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/24/2020
ms.locfileid: "104389737"
---
# <a name="logon-trigger-example-xml"></a><span data-ttu-id="8fbca-103">Beispiel eines LOGON-Auslösers (XML)</span><span class="sxs-lookup"><span data-stu-id="8fbca-103">Logon Trigger Example (XML)</span></span>

<span data-ttu-id="8fbca-104">Der XML-Code in diesem Beispiel definiert einen Task, der den Editor startet, wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="8fbca-104">The XML in this example defines a task that starts Notepad when a user logs on.</span></span>

<span data-ttu-id="8fbca-105">Zum Registrieren einer Aufgabe, die in XML definiert ist, können Sie entweder die [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) -Funktion ([**taskfolder. RegisterTask**](taskfolder-registertask.md) für die Skripterstellung) oder das Befehlszeilen Tool Schtasks.exe verwenden.</span><span class="sxs-lookup"><span data-stu-id="8fbca-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="8fbca-106">Wenn Sie das Schtasks.exe Tool (das sich im Verzeichnis "C: \\ Windows System32" befindet \\ ) verwenden, können Sie den folgenden Befehl verwenden, um den Task zu registrieren: **Schtasks/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="8fbca-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a><span data-ttu-id="8fbca-107">So definieren Sie einen Task zum Starten von Notepad beim Systemstart</span><span class="sxs-lookup"><span data-stu-id="8fbca-107">To define a task to start Notepad on system boot</span></span>

<span data-ttu-id="8fbca-108">Im folgenden XML-Beispiel wird gezeigt, wie Sie eine Aufgabe mit einer einzelnen Ausführungs Aktion (Starten von Editor) definieren, einem einzelnen Logon-Triggern, der die Aufgabe startet, wenn sich ein Benutzer anmeldet, und mehreren anderen Task Einstellungen, die sich darauf auswirken, wie der Task von Taskplaner behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="8fbca-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single logon trigger that starts the task when a user logs on, and several other task settings that affect how the task is handled by Task Scheduler.</span></span>

> [!Note]  
> <span data-ttu-id="8fbca-109">Legen Sie den Wert des **UserID** -Elements auf einen Benutzernamen auf dem Computer fest, auf dem der Task registriert ist.</span><span class="sxs-lookup"><span data-stu-id="8fbca-109">Set the value of the **UserId** element to a user name on the computer on which the task is registered.</span></span>

 


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when a user logs on.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Starts Notepad when a specified user logs on.</Description>
    </RegistrationInfo>
    <Triggers>
        <LogonTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <UserId>DOMAIN_NAME\UserName</UserId>
        </LogonTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <GroupId>Builtin\Administrators</GroupId>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="8fbca-110">TaskScheduler-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="8fbca-110">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="8fbca-111">Im folgenden finden Sie einige wichtige Punkte, die Sie berücksichtigen sollten, wenn Sie dieses Beispiel verwenden:</span><span class="sxs-lookup"><span data-stu-id="8fbca-111">The following are some important elements to keep in mind when using this example:</span></span>

-   <span data-ttu-id="8fbca-112">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): enthält Registrierungsinformationen zum Task.</span><span class="sxs-lookup"><span data-stu-id="8fbca-112">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="8fbca-113">[**Trigger**](taskschedulerschema-triggers-tasktype-element.md): definiert den Trigger, der den Task startet.</span><span class="sxs-lookup"><span data-stu-id="8fbca-113">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="8fbca-114">[**Logon-**](taskschedulerschema-logontrigger-triggergroup-element.md)Auslösung: definiert den Logon-Auslösers.</span><span class="sxs-lookup"><span data-stu-id="8fbca-114">[**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md): Defines the logon trigger.</span></span> <span data-ttu-id="8fbca-115">In diesem Fall werden drei untergeordnete Elemente verwendet: die Start-und endgrenzen, die angeben, wann der ausgelöst und deaktiviert wird, und das [**UserID**](taskschedulerschema-userid-logontriggertype-element.md) -Element, das den Benutzer Bezeichner hat.</span><span class="sxs-lookup"><span data-stu-id="8fbca-115">In this case, three child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, and the [**UserId**](taskschedulerschema-userid-logontriggertype-element.md) element that identifier of the user.</span></span> <span data-ttu-id="8fbca-116">Der Task wird gestartet, wenn sich der Benutzer am Computer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="8fbca-116">The task is started when this user logs on to the computer..</span></span>
-   <span data-ttu-id="8fbca-117">[**Prinzipal**](taskschedulerschema-principal-principaltype-element.md): definiert den Sicherheitskontext, unter dem eine Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8fbca-117">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="8fbca-118">[**Einstellungen**](taskschedulerschema-settings-tasktype-element.md): definiert die Aufgaben Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8fbca-118">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="8fbca-119">[**Aktionen**](taskschedulerschema-actions-tasktype-element.md): definiert die Aktionen, die von der Aufgabe durchführt werden.</span><span class="sxs-lookup"><span data-stu-id="8fbca-119">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions the task performs.</span></span> <span data-ttu-id="8fbca-120">In diesem Fall wird der Editor ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8fbca-120">In this case, running Notepad.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fbca-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8fbca-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fbca-122">Verwenden des Taskplaner</span><span class="sxs-lookup"><span data-stu-id="8fbca-122">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




