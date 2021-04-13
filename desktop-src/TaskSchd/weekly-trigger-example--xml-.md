---
title: Beispiel für einen wöchentlichen Beispiel (XML)
description: Der XML-Code in diesem Beispiel definiert einen Task, der den Editor wöchentlich startet.
ms.assetid: 1911e8b1-2583-440c-a6ed-d71080b60987
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf8c2683311aecc427e9570a0452c746375eca01
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/24/2020
ms.locfileid: "104389731"
---
# <a name="weekly-trigger-example-xml"></a><span data-ttu-id="8dc54-103">Beispiel für einen wöchentlichen Beispiel (XML)</span><span class="sxs-lookup"><span data-stu-id="8dc54-103">Weekly Trigger Example (XML)</span></span>

<span data-ttu-id="8dc54-104">Der XML-Code in diesem Beispiel definiert einen Task, der den Editor wöchentlich startet.</span><span class="sxs-lookup"><span data-stu-id="8dc54-104">The XML in this example defines a task that starts Notepad on a bi-weekly basis.</span></span>

<span data-ttu-id="8dc54-105">Zum Registrieren einer Aufgabe, die in XML definiert ist, können Sie entweder die [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) -Funktion ([**taskfolder. RegisterTask**](taskfolder-registertask.md) für die Skripterstellung) oder das Befehlszeilen Tool Schtasks.exe verwenden.</span><span class="sxs-lookup"><span data-stu-id="8dc54-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="8dc54-106">Wenn Sie das Schtasks.exe Tool (das sich im Verzeichnis "C: \\ Windows System32" befindet \\ ) verwenden, können Sie den folgenden Befehl verwenden, um den Task zu registrieren: **Schtasks/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="8dc54-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-every-other-week-on-monday-at-800-am"></a><span data-ttu-id="8dc54-107">So definieren Sie einen Task zum Starten von Notepad alle anderen Wochen am Montag um 8:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="8dc54-107">To define a task to start Notepad every other week on Monday at 8:00 AM</span></span>

<span data-ttu-id="8dc54-108">Im folgenden XML-Beispiel wird gezeigt, wie eine Aufgabe mit einer einzelnen Ausführungs Aktion (Starten von Editor), einem einzelnen Kalender-Triggern, gestartet wird (startet die Aufgabe alle anderen Wochen am Montag um 8:00 Uhr) und verschiedene andere Task Einstellungen, die beeinflussen, wie die Aufgabe von Taskplaner behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="8dc54-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single calendar trigger (starts the task every other week on Monday at 8:00 AM), and several other task settings that affect how the task is handled by Task Scheduler.</span></span>


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start on a bi-weekly basis.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-05-01T09:00:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Notepad starts every other week on Monday at 8:00am.</Description>
    </RegistrationInfo>
    <Triggers>
        <CalendarTrigger>
            <StartBoundary>2005-05-02T08:00:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00</EndBoundary>
            <ScheduleByWeek>
                <WeeksInterval>2</WeeksInterval>
                <DaysOfWeek>
                    <Monday/>
                </DaysOfWeek>
            </ScheduleByWeek>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="8dc54-109">TaskScheduler-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="8dc54-109">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="8dc54-110">Im folgenden finden Sie einige wichtige Elemente, die Sie beachten sollten, wenn Sie dieses Beispiel verwenden.</span><span class="sxs-lookup"><span data-stu-id="8dc54-110">Here are some important elements to keep in mind when using this example.</span></span>

-   [<span data-ttu-id="8dc54-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="8dc54-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md)

    <span data-ttu-id="8dc54-112">Enthält Registrierungsinformationen über den Task.</span><span class="sxs-lookup"><span data-stu-id="8dc54-112">Contains registration information about the task.</span></span>

-   [<span data-ttu-id="8dc54-113">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="8dc54-113">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)

    <span data-ttu-id="8dc54-114">Definiert den-Typ, der den Task startet.</span><span class="sxs-lookup"><span data-stu-id="8dc54-114">Defines the trigger that starts the task.</span></span>

-   [<span data-ttu-id="8dc54-115">**Calendarausgelöst**</span><span class="sxs-lookup"><span data-stu-id="8dc54-115">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)

    <span data-ttu-id="8dc54-116">Definiert den wöchentlichen Kalender-Auslösers.</span><span class="sxs-lookup"><span data-stu-id="8dc54-116">Defines the weekly calendar trigger.</span></span> <span data-ttu-id="8dc54-117">In diesem Fall werden nur vier untergeordnete Elemente verwendet: die Start-und endgrenzen, die angeben, wann der Auslöse Zeitpunkt aktiviert und deaktiviert wird, den wöchentlichen Zeitplan und die Wochentage, an denen der Task ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8dc54-117">In this case, only four child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, the weekly schedule, and the days of the week that the task will run on.</span></span> <span data-ttu-id="8dc54-118">Das [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) -Element ist ein erforderliches Element für Kalender Trigger.</span><span class="sxs-lookup"><span data-stu-id="8dc54-118">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for calendar triggers.</span></span>

-   [<span data-ttu-id="8dc54-119">**Schedulebyweek**</span><span class="sxs-lookup"><span data-stu-id="8dc54-119">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)

    <span data-ttu-id="8dc54-120">Definiert den wöchentlichen Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="8dc54-120">Defines the weekly schedule.</span></span> <span data-ttu-id="8dc54-121">In diesem Fall wird das Intervall so festgelegt, dass die Aufgabe an einem Montag alle anderen Wochen durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8dc54-121">In this case, the interval is set to perform the task every other week on a Monday.</span></span>

-   [<span data-ttu-id="8dc54-122">**Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="8dc54-122">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md)

    <span data-ttu-id="8dc54-123">Definiert den Sicherheitskontext, unter dem eine Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8dc54-123">Defines the security context that a task runs under.</span></span>

-   [<span data-ttu-id="8dc54-124">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="8dc54-124">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)

    <span data-ttu-id="8dc54-125">Definiert die Aufgaben Einstellungen, die Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8dc54-125">Defines the task settings that Task Scheduler uses to perform the task.</span></span>

-   [<span data-ttu-id="8dc54-126">**Aktionen**</span><span class="sxs-lookup"><span data-stu-id="8dc54-126">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)

    <span data-ttu-id="8dc54-127">Definiert die Aktionen, die vom Task ausgeführt werden (in diesem Fall wird Notepad ausgeführt).</span><span class="sxs-lookup"><span data-stu-id="8dc54-127">Defines the actions the task performs (in this case, running Notepad).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8dc54-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8dc54-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8dc54-129">Verwenden des Taskplaner</span><span class="sxs-lookup"><span data-stu-id="8dc54-129">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




