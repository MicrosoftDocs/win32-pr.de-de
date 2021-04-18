---
title: Beispiel eines LOGON-Auslösers (XML)
description: Der XML-Code in diesem Beispiel definiert einen Task, der den Editor startet, wenn sich ein Benutzer anmeldet.
ms.assetid: c1cce95f-7558-489e-b092-c82d55b42165
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d66766ce4cae33c3526ac9d30071ff2082ddc1f2
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/24/2020
ms.locfileid: "104389737"
---
# <a name="logon-trigger-example-xml"></a>Beispiel eines LOGON-Auslösers (XML)

Der XML-Code in diesem Beispiel definiert einen Task, der den Editor startet, wenn sich ein Benutzer anmeldet.

Zum Registrieren einer Aufgabe, die in XML definiert ist, können Sie entweder die [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) -Funktion ([**taskfolder. RegisterTask**](taskfolder-registertask.md) für die Skripterstellung) oder das Befehlszeilen Tool Schtasks.exe verwenden. Wenn Sie das Schtasks.exe Tool (das sich im Verzeichnis "C: \\ Windows System32" befindet \\ ) verwenden, können Sie den folgenden Befehl verwenden, um den Task zu registrieren: **Schtasks/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a>So definieren Sie einen Task zum Starten von Notepad beim Systemstart

Im folgenden XML-Beispiel wird gezeigt, wie Sie eine Aufgabe mit einer einzelnen Ausführungs Aktion (Starten von Editor) definieren, einem einzelnen Logon-Triggern, der die Aufgabe startet, wenn sich ein Benutzer anmeldet, und mehreren anderen Task Einstellungen, die sich darauf auswirken, wie der Task von Taskplaner behandelt wird.

> [!Note]  
> Legen Sie den Wert des **UserID** -Elements auf einen Benutzernamen auf dem Computer fest, auf dem der Task registriert ist.

 


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



## <a name="taskscheduler-schema-elements"></a>TaskScheduler-Schema Elemente

Im folgenden finden Sie einige wichtige Punkte, die Sie berücksichtigen sollten, wenn Sie dieses Beispiel verwenden:

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): enthält Registrierungsinformationen zum Task.
-   [**Trigger**](taskschedulerschema-triggers-tasktype-element.md): definiert den Trigger, der den Task startet.
-   [**Logon-**](taskschedulerschema-logontrigger-triggergroup-element.md)Auslösung: definiert den Logon-Auslösers. In diesem Fall werden drei untergeordnete Elemente verwendet: die Start-und endgrenzen, die angeben, wann der ausgelöst und deaktiviert wird, und das [**UserID**](taskschedulerschema-userid-logontriggertype-element.md) -Element, das den Benutzer Bezeichner hat. Der Task wird gestartet, wenn sich der Benutzer am Computer anmeldet.
-   [**Prinzipal**](taskschedulerschema-principal-principaltype-element.md): definiert den Sicherheitskontext, unter dem eine Aufgabe ausgeführt wird.
-   [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md): definiert die Aufgaben Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.
-   [**Aktionen**](taskschedulerschema-actions-tasktype-element.md): definiert die Aktionen, die von der Aufgabe durchführt werden. In diesem Fall wird der Editor ausgeführt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




