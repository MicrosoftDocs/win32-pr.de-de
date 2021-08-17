---
title: Beispiel für Anmeldetrigger (XML)
description: Der XML-Code in diesem Beispiel definiert eine Aufgabe, die Editor, wenn sich ein Benutzer anmeldet.
ms.assetid: c1cce95f-7558-489e-b092-c82d55b42165
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f7e92216748a799c5cf8a3ae32393db2b33c680861b2a5d3249eb19c527474e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760057"
---
# <a name="logon-trigger-example-xml"></a>Beispiel für Anmeldetrigger (XML)

Der XML-Code in diesem Beispiel definiert eine Aufgabe, die Editor, wenn sich ein Benutzer anmeldet.

Zum Registrieren einer Aufgabe, die in XML definiert ist, können Sie entweder die [**ITaskFolder::RegisterTask-Funktion**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) für die Skripterstellung) oder das Schtasks.exe-Befehlszeilentool verwenden. Wenn Sie das Schtasks.exe-Tool (im Verzeichnis C: Windows System32) verwenden, können Sie den folgenden Befehl verwenden, um die Aufgabe zu \\ \\ registrieren: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a>So definieren Sie eine Aufgabe zum Starten Editor beim Systemstart

Das folgende XML-Beispiel zeigt, wie Sie eine Aufgabe mit einer einzelnen Ausführungsaktion (ab Editor), einem einzelnen Anmeldetrigger, der die Aufgabe startet, wenn sich ein Benutzer anmeldet, und mehreren anderen Aufgabeneinstellungen definieren, die sich darauf auswirken, wie der Task von Taskplaner.

> [!Note]  
> Legen Sie den Wert des **UserId-Elements** auf einen Benutzernamen auf dem Computer fest, auf dem der Task registriert ist.

 


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when a user logs on.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Starts Notepad when a specified user logs on.</Description>
    </RegistrationInfo>
    <Triggers>
        <LogonTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <UserId>DOMAIN_NAME\UserName</UserId>
        </LogonTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <GroupId>Builtin\Administrators</GroupId>
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
-   [**LogonTrigger:**](taskschedulerschema-logontrigger-triggergroup-element.md)Definiert den Logon-Trigger. In diesem Fall werden drei untergeordnete Elemente verwendet: die Start- und Endgrenzen, die angeben, wann der Trigger aktiviert und deaktiviert wird, und das [**UserId-Element,**](taskschedulerschema-userid-logontriggertype-element.md) das den Bezeichner des Benutzers enthält. Der Task wird gestartet, wenn sich dieser Benutzer beim Computer anmeldet.
-   [**Prinzipal:**](taskschedulerschema-principal-principaltype-element.md)Definiert den Sicherheitskontext, unter dem ein Task ausgeführt wird.
-   [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md): Definiert die Aufgabeneinstellungen, die der Taskplaner zum Ausführen der Aufgabe verwendet.
-   [**Aktionen:**](taskschedulerschema-actions-tasktype-element.md)Definiert die Aktionen, die der Task ausführt. In diesem Fall wird Editor.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




