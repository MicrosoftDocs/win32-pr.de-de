---
title: Registrierungs auslöserbeispiel (XML)
description: Der XML-Code in diesem Beispiel definiert einen Task, der den Editor startet, wenn der Task registriert wird.
ms.assetid: 976b9767-635f-42a6-84f5-7e0203478594
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 09b9193f3b63f21464811609e8f5f19017539ecd
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/24/2020
ms.locfileid: "106338238"
---
# <a name="registration-trigger-example-xml"></a><span data-ttu-id="54588-103">Registrierungs auslöserbeispiel (XML)</span><span class="sxs-lookup"><span data-stu-id="54588-103">Registration Trigger Example (XML)</span></span>

<span data-ttu-id="54588-104">Der XML-Code in diesem Beispiel definiert einen Task, der den Editor startet, wenn der Task registriert wird.</span><span class="sxs-lookup"><span data-stu-id="54588-104">The XML in this example defines a task that starts Notepad when the task is registered.</span></span>

<span data-ttu-id="54588-105">Zum Registrieren einer Aufgabe, die in XML definiert ist, können Sie entweder die [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) -Funktion ([**taskfolder. RegisterTask**](taskfolder-registertask.md) für die Skripterstellung) oder das Befehlszeilen Tool Schtasks.exe verwenden.</span><span class="sxs-lookup"><span data-stu-id="54588-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="54588-106">Wenn Sie das Schtasks.exe Tool (das sich im Verzeichnis "C: \\ Windows System32" befindet \\ ) verwenden, können Sie den folgenden Befehl verwenden, um den Task zu registrieren: **Schtasks/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="54588-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

> [!Note]  
> <span data-ttu-id="54588-107">Wenn eine Aufgabe mit einem Registrierungs-ausgelöst wird, wird die Aufgabe ausgeführt, nachdem das Update ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="54588-107">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 

## <a name="to-define-a-task-to-start-notepad-on-registration"></a><span data-ttu-id="54588-108">So definieren Sie einen Task zum Starten von Notepad bei der Registrierung</span><span class="sxs-lookup"><span data-stu-id="54588-108">To define a task to start Notepad on registration</span></span>

<span data-ttu-id="54588-109">Im folgenden XML-Beispiel wird gezeigt, wie Sie eine Aufgabe mit einer einzelnen Ausführungs Aktion (Starten von Editor) definieren, einem einzelnen Registrierungsfehler, der die Aufgabe beim Registrieren startet, und mehreren anderen Task Einstellungen, die beeinflussen, wie die Aufgabe vom Taskplaner behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="54588-109">The following XML example shows how to define a task with a single execution action (starting Notepad), a single registration trigger that starts the task when it is registered, and several other task settings that affect how the task is handled by the Task Scheduler.</span></span>

> [!Note]  
> <span data-ttu-id="54588-110">Wenn eine Aufgabe mit einem Registrierungs-ausgelöst wird, wird die Aufgabe ausgeführt, nachdem das Update ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="54588-110">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when
the task is registered.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Task starts after registration.</Description>
    </RegistrationInfo>
    <Triggers>
        <RegistrationTrigger>
        </RegistrationTrigger>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="54588-111">TaskScheduler-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="54588-111">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="54588-112">Im folgenden finden Sie einige wichtige Elemente, die Sie beachten sollten, wenn Sie dieses Beispiel verwenden.</span><span class="sxs-lookup"><span data-stu-id="54588-112">Here are some important elements to keep in mind when using this example.</span></span>

-   <span data-ttu-id="54588-113">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): enthält Registrierungsinformationen zum Task.</span><span class="sxs-lookup"><span data-stu-id="54588-113">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="54588-114">[**Trigger**](taskschedulerschema-triggers-tasktype-element.md): definiert den Trigger, der den Task startet.</span><span class="sxs-lookup"><span data-stu-id="54588-114">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="54588-115">[**Registration-Auslösers**](taskschedulerschema-registrationtrigger-triggergroup-element.md): definiert den Registrierungs--Timeout.</span><span class="sxs-lookup"><span data-stu-id="54588-115">[**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md): Defines the registration trigger.</span></span> <span data-ttu-id="54588-116">In diesem Fall werden nur zwei untergeordnete Elemente verwendet: die Start-und endgrenzen, die angeben, wann der Auslöse Zeitpunkt aktiviert und deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="54588-116">In this case, only two child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated.</span></span>
-   <span data-ttu-id="54588-117">[**Prinzipal**](taskschedulerschema-principal-principaltype-element.md): definiert den Sicherheitskontext, unter dem eine Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54588-117">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="54588-118">[**Einstellungen**](taskschedulerschema-settings-tasktype-element.md): definiert die Aufgaben Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="54588-118">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="54588-119">[**Aktionen**](taskschedulerschema-actions-tasktype-element.md): definiert die Aktionen, die von der Aufgabe durchführt werden.</span><span class="sxs-lookup"><span data-stu-id="54588-119">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions the task performs.</span></span> <span data-ttu-id="54588-120">In diesem Fall wird der Editor ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54588-120">In this case, running Notepad.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54588-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="54588-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54588-122">Verwenden des Taskplaner</span><span class="sxs-lookup"><span data-stu-id="54588-122">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




