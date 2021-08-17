---
title: Beispiel für Registrierungstrigger (XML)
description: Der XML-Code in diesem Beispiel definiert eine Aufgabe, die Editor, wenn der Task registriert wird.
ms.assetid: 976b9767-635f-42a6-84f5-7e0203478594
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b111f5c8c0801bb404e12cee20faf19208d7372d1a3980f7368c6efd2bcbfd35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759581"
---
# <a name="registration-trigger-example-xml"></a>Beispiel für Registrierungstrigger (XML)

Der XML-Code in diesem Beispiel definiert eine Aufgabe, die Editor, wenn der Task registriert wird.

Zum Registrieren einer Aufgabe, die in XML definiert ist, können Sie entweder die [**ITaskFolder::RegisterTask-Funktion**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) für Skripterstellung) oder das Schtasks.exe-Befehlszeilentool verwenden. Wenn Sie das Schtasks.exe-Tool (im Verzeichnis C: Windows System32) verwenden, können Sie den folgenden Befehl verwenden, um die Aufgabe zu \\ \\ registrieren: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>* .

> [!Note]  
> Wenn eine Aufgabe mit einem Registrierungstrigger aktualisiert wird, wird die Aufgabe nach dem Update ausgeführt.

 

## <a name="to-define-a-task-to-start-notepad-on-registration"></a>So definieren Sie eine Aufgabe, die bei Editor gestartet werden soll

Das folgende XML-Beispiel zeigt, wie sie eine Aufgabe mit einer einzelnen Ausführungsaktion (ab Editor), einem einzelnen Registrierungstrigger, der die Aufgabe startet, wenn sie registriert wird, und mehreren anderen Aufgabeneinstellungen definiert, die sich darauf auswirken, wie der Task vom -Taskplaner.

> [!Note]  
> Wenn eine Aufgabe mit einem Registrierungstrigger aktualisiert wird, wird die Aufgabe nach dem Update ausgeführt.

 


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when
the task is registered.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Task starts after registration.</Description>
    </RegistrationInfo>
    <Triggers>
        <RegistrationTrigger>
        </RegistrationTrigger>
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

-   [**RegistrationInfo:**](taskschedulerschema-registrationinfo-tasktype-element.md)Enthält Registrierungsinformationen zum Task.
-   [**Trigger:**](taskschedulerschema-triggers-tasktype-element.md)Definiert den Trigger, der die Aufgabe startet.
-   [**RegistrationTrigger:**](taskschedulerschema-registrationtrigger-triggergroup-element.md)Definiert den Registrierungstrigger. In diesem Fall werden nur zwei untergeordnete Elemente verwendet: die Start- und Endgrenzen, die angeben, wann der Trigger aktiviert und deaktiviert wird.
-   [**Prinzipal:**](taskschedulerschema-principal-principaltype-element.md)Definiert den Sicherheitskontext, unter dem ein Task ausgeführt wird.
-   [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md): Definiert die Aufgabeneinstellungen, die der Taskplaner zum Ausführen der Aufgabe verwendet.
-   [**Aktionen:**](taskschedulerschema-actions-tasktype-element.md)Definiert die Aktionen, die der Task ausführt. In diesem Fall wird Editor.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




