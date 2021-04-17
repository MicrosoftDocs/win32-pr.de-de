---
title: Beispiel für einen Start Auslösers (XML)
description: Der XML-Code in diesem Beispiel definiert einen Task, der den Editor startet, wenn das System gestartet wird.
ms.assetid: 6dd7155c-6163-4408-9cef-c313134beeb0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8f9f5ea10f92979b0798b12a6225f8ba74a38ee
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/24/2020
ms.locfileid: "104314058"
---
# <a name="boot-trigger-example-xml"></a>Beispiel für einen Start Auslösers (XML)

Der XML-Code in diesem Beispiel definiert einen Task, der den Editor startet, wenn das System gestartet wird.

Zum Registrieren einer Aufgabe, die in XML definiert ist, können Sie entweder die [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) -Funktion ([**taskfolder. RegisterTask**](taskfolder-registertask.md) für die Skripterstellung) oder das Befehlszeilen Tool Schtasks.exe verwenden. Wenn Sie das Schtasks.exe Tool (das sich im Verzeichnis "C: \\ Windows System32" befindet \\ ) verwenden, können Sie den folgenden Befehl verwenden, um den Task zu registrieren: **Schtasks/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a>So definieren Sie einen Task zum Starten von Notepad beim Systemstart

Das folgende XML-Beispiel zeigt, wie Sie eine Aufgabe mit einer einzelnen Ausführungs Aktion (Starten von Editor), einem einzelnen Start-Triggern, der die Aufgabe startet, wenn das System gestartet wird, und mehreren anderen Task Einstellungen definieren, die sich darauf auswirken, wie die Aufgabe vom Taskplaner behandelt wird.


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when
the system is booted.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Starts Notepad on system boot.</Description>
    </RegistrationInfo>
    <Triggers>
        <BootTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <ExecutionTimeLimit>PT5M</ExecutionTimeLimit>
        </BootTrigger>
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

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): enthält Registrierungsinformationen zum Task.
-   [**Trigger**](taskschedulerschema-triggers-tasktype-element.md): definiert den Trigger, der den Task startet.
-   [**Boottrigger**](taskschedulerschema-boottrigger-triggergroup-element.md): definiert den Start--Debugger. In diesem Fall werden nur zwei untergeordnete Elemente verwendet: die Start-und endgrenzen, die angeben, wann der Auslöse Zeitpunkt aktiviert und deaktiviert wird.
-   [**Prinzipal**](taskschedulerschema-principal-principaltype-element.md): definiert den Sicherheitskontext, unter dem eine Aufgabe ausgeführt wird.
-   [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md): definiert die Aufgaben Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.
-   [**Aktionen**](taskschedulerschema-actions-tasktype-element.md): definiert die Aktionen, die von der Aufgabe durchführt werden. In diesem Fall wird der Editor ausgeführt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




