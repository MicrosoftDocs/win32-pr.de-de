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
# <a name="weekly-trigger-example-xml"></a>Beispiel für einen wöchentlichen Beispiel (XML)

Der XML-Code in diesem Beispiel definiert einen Task, der den Editor wöchentlich startet.

Zum Registrieren einer Aufgabe, die in XML definiert ist, können Sie entweder die [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) -Funktion ([**taskfolder. RegisterTask**](taskfolder-registertask.md) für die Skripterstellung) oder das Befehlszeilen Tool Schtasks.exe verwenden. Wenn Sie das Schtasks.exe Tool (das sich im Verzeichnis "C: \\ Windows System32" befindet \\ ) verwenden, können Sie den folgenden Befehl verwenden, um den Task zu registrieren: **Schtasks/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-every-other-week-on-monday-at-800-am"></a>So definieren Sie einen Task zum Starten von Notepad alle anderen Wochen am Montag um 8:00 Uhr

Im folgenden XML-Beispiel wird gezeigt, wie eine Aufgabe mit einer einzelnen Ausführungs Aktion (Starten von Editor), einem einzelnen Kalender-Triggern, gestartet wird (startet die Aufgabe alle anderen Wochen am Montag um 8:00 Uhr) und verschiedene andere Task Einstellungen, die beeinflussen, wie die Aufgabe von Taskplaner behandelt wird.


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



## <a name="taskscheduler-schema-elements"></a>TaskScheduler-Schema Elemente

Im folgenden finden Sie einige wichtige Elemente, die Sie beachten sollten, wenn Sie dieses Beispiel verwenden.

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md)

    Enthält Registrierungsinformationen über den Task.

-   [**Trigger**](taskschedulerschema-triggers-tasktype-element.md)

    Definiert den-Typ, der den Task startet.

-   [**Calendarausgelöst**](taskschedulerschema-calendartrigger-triggergroup-element.md)

    Definiert den wöchentlichen Kalender-Auslösers. In diesem Fall werden nur vier untergeordnete Elemente verwendet: die Start-und endgrenzen, die angeben, wann der Auslöse Zeitpunkt aktiviert und deaktiviert wird, den wöchentlichen Zeitplan und die Wochentage, an denen der Task ausgeführt wird. Das [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) -Element ist ein erforderliches Element für Kalender Trigger.

-   [**Schedulebyweek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)

    Definiert den wöchentlichen Zeitplan. In diesem Fall wird das Intervall so festgelegt, dass die Aufgabe an einem Montag alle anderen Wochen durchgeführt wird.

-   [**Prinzipal**](taskschedulerschema-principal-principaltype-element.md)

    Definiert den Sicherheitskontext, unter dem eine Aufgabe ausgeführt wird.

-   [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md)

    Definiert die Aufgaben Einstellungen, die Taskplaner verwendet, um die Aufgabe auszuführen.

-   [**Aktionen**](taskschedulerschema-actions-tasktype-element.md)

    Definiert die Aktionen, die vom Task ausgeführt werden (in diesem Fall wird Notepad ausgeführt).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




