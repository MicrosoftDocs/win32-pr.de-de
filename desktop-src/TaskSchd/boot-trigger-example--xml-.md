---
title: Beispiel für einen Start Auslösers (XML)
description: Der XML-Code in diesem Beispiel definiert einen Task, der den Editor startet, wenn das System gestartet wird.
ms.assetid: 6dd7155c-6163-4408-9cef-c313134beeb0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8f9f5ea10f92979b0798b12a6225f8ba74a38ee
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/24/2020
ms.locfileid: "104314058"
---
# <a name="boot-trigger-example-xml"></a><span data-ttu-id="2517e-103">Beispiel für einen Start Auslösers (XML)</span><span class="sxs-lookup"><span data-stu-id="2517e-103">Boot Trigger Example (XML)</span></span>

<span data-ttu-id="2517e-104">Der XML-Code in diesem Beispiel definiert einen Task, der den Editor startet, wenn das System gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="2517e-104">The XML in this example defines a task that starts Notepad when the system is booted.</span></span>

<span data-ttu-id="2517e-105">Zum Registrieren einer Aufgabe, die in XML definiert ist, können Sie entweder die [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) -Funktion ([**taskfolder. RegisterTask**](taskfolder-registertask.md) für die Skripterstellung) oder das Befehlszeilen Tool Schtasks.exe verwenden.</span><span class="sxs-lookup"><span data-stu-id="2517e-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="2517e-106">Wenn Sie das Schtasks.exe Tool (das sich im Verzeichnis "C: \\ Windows System32" befindet \\ ) verwenden, können Sie den folgenden Befehl verwenden, um den Task zu registrieren: **Schtasks/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="2517e-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a><span data-ttu-id="2517e-107">So definieren Sie einen Task zum Starten von Notepad beim Systemstart</span><span class="sxs-lookup"><span data-stu-id="2517e-107">To define a task to start Notepad on system boot</span></span>

<span data-ttu-id="2517e-108">Das folgende XML-Beispiel zeigt, wie Sie eine Aufgabe mit einer einzelnen Ausführungs Aktion (Starten von Editor), einem einzelnen Start-Triggern, der die Aufgabe startet, wenn das System gestartet wird, und mehreren anderen Task Einstellungen definieren, die sich darauf auswirken, wie die Aufgabe vom Taskplaner behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="2517e-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single boot trigger that starts the task when the system is booted, and several other task settings that affect how the task is handled by the Task Scheduler.</span></span>


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when
the system is booted.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Starts Notepad on system boot.</Description>
    </RegistrationInfo>
    <Triggers>
        <BootTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <ExecutionTimeLimit>PT5M</ExecutionTimeLimit>
        </BootTrigger>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="2517e-109">TaskScheduler-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="2517e-109">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="2517e-110">Im folgenden finden Sie einige wichtige Elemente, die Sie beachten sollten, wenn Sie dieses Beispiel verwenden.</span><span class="sxs-lookup"><span data-stu-id="2517e-110">Here are some important elements to keep in mind when using this example.</span></span>

-   <span data-ttu-id="2517e-111">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): enthält Registrierungsinformationen zum Task.</span><span class="sxs-lookup"><span data-stu-id="2517e-111">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="2517e-112">[**Trigger**](taskschedulerschema-triggers-tasktype-element.md): definiert den Trigger, der den Task startet.</span><span class="sxs-lookup"><span data-stu-id="2517e-112">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="2517e-113">[**Boottrigger**](taskschedulerschema-boottrigger-triggergroup-element.md): definiert den Start--Debugger.</span><span class="sxs-lookup"><span data-stu-id="2517e-113">[**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md): Defines the boot trigger.</span></span> <span data-ttu-id="2517e-114">In diesem Fall werden nur zwei untergeordnete Elemente verwendet: die Start-und endgrenzen, die angeben, wann der Auslöse Zeitpunkt aktiviert und deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="2517e-114">In this case only two child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated.</span></span>
-   <span data-ttu-id="2517e-115">[**Prinzipal**](taskschedulerschema-principal-principaltype-element.md): definiert den Sicherheitskontext, unter dem eine Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2517e-115">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="2517e-116">[**Einstellungen**](taskschedulerschema-settings-tasktype-element.md): definiert die Aufgaben Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2517e-116">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="2517e-117">[**Aktionen**](taskschedulerschema-actions-tasktype-element.md): definiert die Aktionen, die von der Aufgabe durchführt werden.</span><span class="sxs-lookup"><span data-stu-id="2517e-117">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions the task performs.</span></span> <span data-ttu-id="2517e-118">In diesem Fall wird der Editor ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2517e-118">In this case, running Notepad.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2517e-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2517e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2517e-120">Verwenden des Taskplaner</span><span class="sxs-lookup"><span data-stu-id="2517e-120">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




