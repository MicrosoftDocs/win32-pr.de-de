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
# <a name="time-trigger-example-xml"></a>Beispiel für Zeit Auslösung (XML)

Der XML-Code in diesem Beispiel definiert einen Task, der den Editor zu einem bestimmten Zeitpunkt startet.

Zum Registrieren einer Aufgabe, die in XML definiert ist, können Sie entweder die [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) -Funktion ([**taskfolder. RegisterTask**](taskfolder-registertask.md) für die Skripterstellung) oder das Befehlszeilen Tool Schtasks.exe verwenden. Wenn Sie das Schtasks.exe Tool (das sich im Verzeichnis "C: \\ Windows System32" befindet \\ ) verwenden, können Sie den folgenden Befehl verwenden, um den Task zu registrieren: **Schtasks/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-at-a-specific-time"></a>So definieren Sie einen Task zum Starten von Notepad zu einem bestimmten Zeitpunkt

Im folgenden XML-Beispiel wird gezeigt, wie eine Aufgabe mit einer einzelnen Ausführungs Aktion (Starten von Editor), einem einmaligen Triggertyp, der die Aufgabe zu einem bestimmten Zeitpunkt startet, und mehreren anderen Aufgaben Einstellungen definiert wird, die sich auf die Behandlung der Aufgabe durch die Taskplaner auswirken.


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



## <a name="taskscheduler-schema-elements"></a>TaskScheduler-Schema Elemente

Im folgenden finden Sie einige wichtige Punkte, die Sie berücksichtigen sollten, wenn Sie dieses Beispiel verwenden:

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): enthält Registrierungsinformationen zum Task.
-   [**Trigger**](taskschedulerschema-triggers-tasktype-element.md): definiert den Trigger, der den Task startet.
-   [**Timetimeout**](taskschedulerschema-timetrigger-triggergroup-element.md): definiert den Zeit--Auslösers. In diesem Fall werden drei untergeordnete Elemente verwendet: die Start-und endgrenzen, die angeben, wann der-Triggervorgang aktiviert und deaktiviert wird, und das Ausführungszeit Limit, das die maximale Zeitspanne angibt, in der die Aufgabe vom-Triggern gestartet werden kann. Das [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) -Element ist ein erforderliches Element für Zeit Trigger.
-   [**Prinzipal**](taskschedulerschema-principal-principaltype-element.md): definiert den Sicherheitskontext, unter dem eine Aufgabe ausgeführt wird.
-   [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md): definiert die Aufgaben Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.
-   [**Aktionen**](taskschedulerschema-actions-tasktype-element.md): definiert die Aktionen, die der Task ausführt (in diesem Fall das Ausführen von Notepad).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




