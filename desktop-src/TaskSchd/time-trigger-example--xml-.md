---
title: Beispiel für Zeittrigger (XML)
description: Der XML-Code in diesem Beispiel definiert einen Task, Editor zu einem bestimmten Zeitpunkt gestartet wird.
ms.assetid: dde3627b-e268-45ef-9c26-08877bfe484f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 25c4cffb3764f96a191b1c5ad0d2999664d536f2df9be9862fa98f0335f3fe23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990810"
---
# <a name="time-trigger-example-xml"></a>Beispiel für Zeittrigger (XML)

Der XML-Code in diesem Beispiel definiert einen Task, Editor zu einem bestimmten Zeitpunkt gestartet wird.

Zum Registrieren einer aufgabe, die in XML definiert ist, können Sie entweder die [**ITaskFolder::RegisterTask-Funktion**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) für Skripterstellung) oder das Schtasks.exe-Befehlszeilentool verwenden. Wenn Sie das Schtasks.exe-Tool (im Verzeichnis C: Windows System32) verwenden, können Sie den folgenden Befehl verwenden, um die Aufgabe zu \\ \\ registrieren: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-at-a-specific-time"></a>So definieren Sie eine Aufgabe, die Editor zu einem bestimmten Zeitpunkt gestartet werden soll

Das folgende XML-Beispiel zeigt, wie sie einen Task mit einer einzelnen Ausführungsaktion (ab Editor), einem einmaligen Trigger, der den Task zu einem bestimmten Zeitpunkt startet, und mehreren anderen Aufgabeneinstellungen definieren, die sich darauf auswirken, wie der Task vom -Taskplaner.


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



## <a name="taskscheduler-schema-elements"></a>TaskScheduler-Schemaelemente

Im Folgenden finden Sie einige wichtige Elemente, die Sie bei der Verwendung dieses Beispiels beachten sollten:

-   [**RegistrationInfo:**](taskschedulerschema-registrationinfo-tasktype-element.md)Enthält Registrierungsinformationen zum Task.
-   [**Trigger:**](taskschedulerschema-triggers-tasktype-element.md)Definiert den Trigger, der die Aufgabe startet.
-   [**TimeTrigger:**](taskschedulerschema-timetrigger-triggergroup-element.md)Definiert den Zeittrigger. In diesem Fall werden drei untergeordnete Elemente verwendet: die Start- und Endgrenzen, die angeben, wann der Trigger aktiviert und deaktiviert wird, und das Ausführungszeitlimit, das die maximale Zeitdauer angibt, in der der Task vom Trigger gestartet werden kann. Das [**StartBoundary-Element**](taskschedulerschema-startboundary-triggerbasetype-element.md) ist ein erforderliches Element für Zeittrigger.
-   [**Prinzipal:**](taskschedulerschema-principal-principaltype-element.md)Definiert den Sicherheitskontext, unter dem ein Task ausgeführt wird.
-   [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md): Definiert die Aufgabeneinstellungen, die der Taskplaner zum Ausführen der Aufgabe verwendet.
-   [**Aktionen:**](taskschedulerschema-actions-tasktype-element.md)Definiert die Aktionen, die der Task ausführt (in diesem Fall die Ausführung Editor).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




