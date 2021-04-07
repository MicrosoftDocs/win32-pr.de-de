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
# <a name="daily-trigger-example-xml"></a>Beispiel für das tägliche Beispiel (XML)

Der XML-Code in diesem Beispiel definiert einen Task, der den Notepad täglich um 8:00 Uhr startet. Das Beispiel zeigt auch, wie Sie ein Wiederholungsmuster für den-Vorgang festlegen, um die Aufgabe zu wiederholen.

Zum Registrieren einer Aufgabe, die in XML definiert ist, können Sie entweder die [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) -Funktion ([**taskfolder. RegisterTask**](taskfolder-registertask.md) für die Skripterstellung) oder das Befehlszeilen Tool Schtasks.exe verwenden. Wenn Sie das Schtasks.exe Tool (das sich im Verzeichnis "C: \\ Windows System32" befindet \\ ) verwenden, können Sie den folgenden Befehl verwenden, um den Task zu registrieren: **Schtasks/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-every-day-at-800-am"></a>So definieren Sie einen Task zum Starten von Notepad täglich um 8:00 Uhr

Das folgende XML-Beispiel zeigt, wie Sie eine Aufgabe mit einer einzelnen Ausführungs Aktion (Starten von Editor), einem einzelnen Kalender-Triggern (startet die Aufgabe täglich um 8:00 Uhr) und mehreren anderen Aufgaben Einstellungen definieren, die beeinflussen, wie die Aufgabe von Taskplaner behandelt wird.


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



## <a name="taskscheduler-schema-elements"></a>TaskScheduler-Schema Elemente

Im folgenden finden Sie einige wichtige Elemente, die Sie beachten sollten, wenn Sie dieses Beispiel verwenden.

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md)

    Enthält Registrierungsinformationen über den Task.

-   [**Trigger**](taskschedulerschema-triggers-tasktype-element.md)

    Definiert den-Typ, der den Task startet.

-   [**Calendarausgelöst**](taskschedulerschema-calendartrigger-triggergroup-element.md)

    Definiert den täglichen Kalender-Auslösers. In diesem Fall werden vier untergeordnete Elemente verwendet: die Start-und endgrenzen, die angeben, wann der-Auslösers aktiviert und deaktiviert wird, den täglichen Zeitplan und das Wiederholungsmuster für den Task. Das [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) -Element ist ein erforderliches Element für Kalender Trigger.

-   [**Schedulebyday**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)

    Definiert den täglichen Zeitplan. In diesem Fall wird das Intervall so festgelegt, dass die Aufgabe jeden Tag durchgeführt wird.

-   [**Prinzipal**](taskschedulerschema-principal-principaltype-element.md): definiert den Sicherheitskontext, unter dem eine Aufgabe ausgeführt wird.
-   [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md)

    Definiert die Aufgaben Einstellungen, die Taskplaner verwendet, um die Aufgabe auszuführen.

-   [**Aktionen**](taskschedulerschema-actions-tasktype-element.md)

    Definiert die Aktionen, die vom Task ausgeführt werden (in diesem Fall wird Notepad ausgeführt).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




