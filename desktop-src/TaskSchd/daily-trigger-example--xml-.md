---
title: Beispiel für das tägliche Beispiel (XML)
description: Der XML-Code in diesem Beispiel definiert einen Task, der den Notepad täglich um 8 00 Uhr startet.
ms.assetid: b7818071-12b6-41df-85b9-282c08cf6e31
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fe673a764e6e7e4e3ae5089022da2232821d9184
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/24/2020
ms.locfileid: "103719985"
---
# <a name="daily-trigger-example-xml"></a><span data-ttu-id="8b36a-103">Beispiel für das tägliche Beispiel (XML)</span><span class="sxs-lookup"><span data-stu-id="8b36a-103">Daily Trigger Example (XML)</span></span>

<span data-ttu-id="8b36a-104">Der XML-Code in diesem Beispiel definiert einen Task, der den Notepad täglich um 8:00 Uhr startet.</span><span class="sxs-lookup"><span data-stu-id="8b36a-104">The XML in this example defines a task that starts Notepad at 8:00 AM every day.</span></span> <span data-ttu-id="8b36a-105">Das Beispiel zeigt auch, wie Sie ein Wiederholungsmuster für den-Vorgang festlegen, um die Aufgabe zu wiederholen.</span><span class="sxs-lookup"><span data-stu-id="8b36a-105">The example also shows how to set a repetition pattern for the trigger to repeat the task.</span></span>

<span data-ttu-id="8b36a-106">Zum Registrieren einer Aufgabe, die in XML definiert ist, können Sie entweder die [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) -Funktion ([**taskfolder. RegisterTask**](taskfolder-registertask.md) für die Skripterstellung) oder das Befehlszeilen Tool Schtasks.exe verwenden.</span><span class="sxs-lookup"><span data-stu-id="8b36a-106">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="8b36a-107">Wenn Sie das Schtasks.exe Tool (das sich im Verzeichnis "C: \\ Windows System32" befindet \\ ) verwenden, können Sie den folgenden Befehl verwenden, um den Task zu registrieren: **Schtasks/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="8b36a-107">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-every-day-at-800-am"></a><span data-ttu-id="8b36a-108">So definieren Sie einen Task zum Starten von Notepad täglich um 8:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="8b36a-108">To define a task to start Notepad every day at 8:00 AM</span></span>

<span data-ttu-id="8b36a-109">Das folgende XML-Beispiel zeigt, wie Sie eine Aufgabe mit einer einzelnen Ausführungs Aktion (Starten von Editor), einem einzelnen Kalender-Triggern (startet die Aufgabe täglich um 8:00 Uhr) und mehreren anderen Aufgaben Einstellungen definieren, die beeinflussen, wie die Aufgabe von Taskplaner behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="8b36a-109">The following XML example shows how to define a task with a single execution action (starting Notepad), a single calendar trigger (starts the task every day at 8:00 AM), and several other task settings that affect how the task is handled by Task Scheduler.</span></span>


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start on a daily basis.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Notepad starts every day.</Description>
    </RegistrationInfo>
    <Triggers>
        <CalendarTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Repetition>
                <Interval>PT1M</Interval>
                <Duration>PT4M</Duration>
            </Repetition>
            <ScheduleByDay>
                <DaysInterval>1</DaysInterval>
            </ScheduleByDay>
        </CalendarTrigger>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="8b36a-110">TaskScheduler-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="8b36a-110">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="8b36a-111">Im folgenden finden Sie einige wichtige Elemente, die Sie beachten sollten, wenn Sie dieses Beispiel verwenden.</span><span class="sxs-lookup"><span data-stu-id="8b36a-111">Here are some important elements to keep in mind when using this example.</span></span>

-   [<span data-ttu-id="8b36a-112">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="8b36a-112">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md)

    <span data-ttu-id="8b36a-113">Enthält Registrierungsinformationen über den Task.</span><span class="sxs-lookup"><span data-stu-id="8b36a-113">Contains registration information about the task.</span></span>

-   [<span data-ttu-id="8b36a-114">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="8b36a-114">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)

    <span data-ttu-id="8b36a-115">Definiert den-Typ, der den Task startet.</span><span class="sxs-lookup"><span data-stu-id="8b36a-115">Defines the trigger that starts the task.</span></span>

-   [<span data-ttu-id="8b36a-116">**Calendarausgelöst**</span><span class="sxs-lookup"><span data-stu-id="8b36a-116">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)

    <span data-ttu-id="8b36a-117">Definiert den täglichen Kalender-Auslösers.</span><span class="sxs-lookup"><span data-stu-id="8b36a-117">Defines the daily calendar trigger.</span></span> <span data-ttu-id="8b36a-118">In diesem Fall werden vier untergeordnete Elemente verwendet: die Start-und endgrenzen, die angeben, wann der-Auslösers aktiviert und deaktiviert wird, den täglichen Zeitplan und das Wiederholungsmuster für den Task.</span><span class="sxs-lookup"><span data-stu-id="8b36a-118">In this case, four child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, the daily schedule, and the repetition pattern for the task.</span></span> <span data-ttu-id="8b36a-119">Das [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) -Element ist ein erforderliches Element für Kalender Trigger.</span><span class="sxs-lookup"><span data-stu-id="8b36a-119">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for calendar triggers.</span></span>

-   [<span data-ttu-id="8b36a-120">**Schedulebyday**</span><span class="sxs-lookup"><span data-stu-id="8b36a-120">**ScheduleByDay**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md)

    <span data-ttu-id="8b36a-121">Definiert den täglichen Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="8b36a-121">Defines the daily schedule.</span></span> <span data-ttu-id="8b36a-122">In diesem Fall wird das Intervall so festgelegt, dass die Aufgabe jeden Tag durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b36a-122">In this case, the interval is set to perform the task every day.</span></span>

-   <span data-ttu-id="8b36a-123">[**Prinzipal**](taskschedulerschema-principal-principaltype-element.md): definiert den Sicherheitskontext, unter dem eine Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b36a-123">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   [<span data-ttu-id="8b36a-124">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="8b36a-124">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)

    <span data-ttu-id="8b36a-125">Definiert die Aufgaben Einstellungen, die Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8b36a-125">Defines the task settings that Task Scheduler uses to perform the task.</span></span>

-   [<span data-ttu-id="8b36a-126">**Aktionen**</span><span class="sxs-lookup"><span data-stu-id="8b36a-126">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)

    <span data-ttu-id="8b36a-127">Definiert die Aktionen, die vom Task ausgeführt werden (in diesem Fall wird Notepad ausgeführt).</span><span class="sxs-lookup"><span data-stu-id="8b36a-127">Defines the actions the task performs (in this case, running Notepad).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b36a-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8b36a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b36a-129">Verwenden des Taskplaner</span><span class="sxs-lookup"><span data-stu-id="8b36a-129">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




