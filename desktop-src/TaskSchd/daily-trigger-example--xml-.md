---
title: Beispiel für einen täglichen Trigger (XML)
description: Der XML-Code in diesem Beispiel definiert einen Task, Editor täglich um 8:00 Uhr beginnt.
ms.assetid: b7818071-12b6-41df-85b9-282c08cf6e31
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cd98ada9a69f694d59262682317b7e5be91509b4862f8b896e22b7b0deac2167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139503"
---
# <a name="daily-trigger-example-xml"></a>Beispiel für einen täglichen Trigger (XML)

Der XML-Code in diesem Beispiel definiert einen Task, Editor täglich um 8:00 Uhr gestartet wird. Das Beispiel zeigt auch, wie ein Wiederholungsmuster für den Trigger festgelegt wird, um die Aufgabe zu wiederholen.

Zum Registrieren einer aufgabe, die in XML definiert ist, können Sie entweder die [**ITaskFolder::RegisterTask-Funktion**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) für Skripterstellung) oder das Schtasks.exe-Befehlszeilentool verwenden. Wenn Sie das Schtasks.exe-Tool (im Verzeichnis C: Windows System32) verwenden, können Sie den folgenden Befehl verwenden, um die Aufgabe zu \\ \\ registrieren: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-every-day-at-800-am"></a>So definieren Sie eine Aufgabe, die Editor täglich um 8:00 Uhr gestartet werden soll

Das folgende XML-Beispiel zeigt, wie Sie eine Aufgabe mit einer einzelnen Ausführungsaktion (ab Editor), einem einzelnen Kalendertrigger (startet die Aufgabe täglich um 8:00 Uhr) und mehreren anderen Aufgabeneinstellungen definieren, die beeinflussen, wie die Aufgabe von Taskplaner.


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



## <a name="taskscheduler-schema-elements"></a>TaskScheduler-Schemaelemente

Im Folgenden finden Sie einige wichtige Elemente, die Sie bei der Verwendung dieses Beispiels beachten sollten.

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md)

    Enthält Registrierungsinformationen zum Task.

-   [**Trigger**](taskschedulerschema-triggers-tasktype-element.md)

    Definiert den Trigger, der die Aufgabe startet.

-   [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)

    Definiert den täglichen Kalendertrigger. In diesem Fall werden vier untergeordnete Elemente verwendet: die Start- und Endgrenzen, die angeben, wann der Trigger aktiviert und deaktiviert wird, den täglichen Zeitplan und das Wiederholungsmuster für die Aufgabe. Das [**StartBoundary-Element**](taskschedulerschema-startboundary-triggerbasetype-element.md) ist ein erforderliches Element für Kalendertrigger.

-   [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)

    Definiert den täglichen Zeitplan. In diesem Fall wird das Intervall so festgelegt, dass die Aufgabe täglich ausgeführt wird.

-   [**Prinzipal:**](taskschedulerschema-principal-principaltype-element.md)Definiert den Sicherheitskontext, unter dem ein Task ausgeführt wird.
-   [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md)

    Definiert die Aufgabeneinstellungen, die Taskplaner zum Ausführen der Aufgabe verwendet.

-   [**Aktionen**](taskschedulerschema-actions-tasktype-element.md)

    Definiert die Aktionen, die der Task ausführt (in diesem Fall die Ausführung Editor).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




