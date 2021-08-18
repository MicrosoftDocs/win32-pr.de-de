---
title: Beispiel für wöchentlichen Trigger (XML)
description: Der XML-Code in diesem Beispiel definiert eine Aufgabe, Editor zwei wochenweise gestartet wird.
ms.assetid: 1911e8b1-2583-440c-a6ed-d71080b60987
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7c038c21db137ce9180d76cecf4c2885274f7cdd72720b12b919f9a39e98e575
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001809"
---
# <a name="weekly-trigger-example-xml"></a>Beispiel für wöchentlichen Trigger (XML)

Der XML-Code in diesem Beispiel definiert eine Aufgabe, Editor zwei wochenweise gestartet wird.

Zum Registrieren einer Aufgabe, die in XML definiert ist, können Sie entweder die [**ITaskFolder::RegisterTask-Funktion**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) für Skripterstellung) oder das Schtasks.exe-Befehlszeilentool verwenden. Wenn Sie das Schtasks.exe-Tool (im Verzeichnis C: Windows System32) verwenden, können Sie den folgenden Befehl verwenden, um die Aufgabe zu \\ \\ registrieren: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-every-other-week-on-monday-at-800-am"></a>So definieren Sie eine Aufgabe, die Editor zwei Wochen am Montag um 8:00 Uhr gestartet wird

Das folgende XML-Beispiel zeigt, wie Sie eine Aufgabe mit einer einzelnen Ausführungsaktion (ab Editor), einem einzelnen Kalendertrigger (startet die Aufgabe alle zwei Wochen am Montag um 8:00 Uhr) und mehreren anderen Aufgabeneinstellungen definieren, die beeinflussen, wie die Aufgabe von Taskplaner.


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



## <a name="taskscheduler-schema-elements"></a>TaskScheduler-Schemaelemente

Im Folgenden finden Sie einige wichtige Elemente, die Sie bei der Verwendung dieses Beispiels beachten sollten.

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md)

    Enthält Registrierungsinformationen zum Task.

-   [**Auslöser**](taskschedulerschema-triggers-tasktype-element.md)

    Definiert den Trigger, der die Aufgabe startet.

-   [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)

    Definiert den wöchentlichen Kalendertrigger. In diesem Fall werden nur vier untergeordnete Elemente verwendet: die Start- und Endgrenzen, die angeben, wann der Trigger aktiviert und deaktiviert wird, den wöchentlichen Zeitplan und die Wochentage, an denen die Aufgabe ausgeführt wird. Das [**StartBoundary-Element**](taskschedulerschema-startboundary-triggerbasetype-element.md) ist ein erforderliches Element für Kalendertrigger.

-   [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)

    Definiert den wöchentlichen Zeitplan. In diesem Fall wird das Intervall so festgelegt, dass die Aufgabe alle zwei Wochen an einem Montag ausgeführt wird.

-   [**Prinzipal**](taskschedulerschema-principal-principaltype-element.md)

    Definiert den Sicherheitskontext, unter dem eine Aufgabe ausgeführt wird.

-   [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md)

    Definiert die Aufgabeneinstellungen, die Taskplaner zum Ausführen der Aufgabe verwendet.

-   [**Aktionen**](taskschedulerschema-actions-tasktype-element.md)

    Definiert die Aktionen, die der Task ausführt (in diesem Fall die Ausführung Editor).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




