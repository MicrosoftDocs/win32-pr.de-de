---
title: Anzeigen von Tasknamen und -zuzuständen (Skripterstellung)
description: Dieses Skriptbeispiel zeigt, wie Sie Aufgaben in einem Aufgabenordner aufzählen und Eigenschaftswerte aus jedem Task anzeigen.
ms.assetid: 2a84a752-fbf3-4041-8b0a-304f89a49354
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6f3ec036b1d9d61c387495b48874bf742a9479ae0608f0e5c728a029df24709
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002488"
---
# <a name="displaying-task-names-and-states-scripting"></a>Anzeigen von Tasknamen und -zuzuständen (Skripterstellung)

Dieses Skriptbeispiel zeigt, wie Sie Aufgaben in einem Aufgabenordner aufzählen und Eigenschaftswerte aus jedem Task anzeigen.

Im folgenden Verfahren wird beschrieben, wie Aufgabennamen und -zustände für alle Aufgaben in einem Aufgabenordner angezeigt werden.

**So zeigen Sie Aufgabennamen und -status für alle Aufgaben in einem Aufgabenordner an**

1.  Erstellen Sie das [**TaskService-Objekt.**](taskservice.md)

    Mit diesem Objekt können Sie eine Verbindung mit dem Taskplaner herstellen und auf einen bestimmten Aufgabenordner zugreifen.

2.  Get a task folder that holds the tasks you want information about.

    Verwenden Sie [**die TaskService.GetFolder-Methode,**](taskservice-getfolder.md) um den Ordner zu erhalten.

3.  Sie können die Auflistung der Aufgaben aus dem Ordner erhalten.

    Verwenden Sie [**die TaskFolder.GetTasks-Methode,**](taskfolder-gettasks.md) um die Aufgabensammlung [**(RegisteredTaskCollection) zu erhalten.**](registeredtaskcollection.md)

4.  Sie können die Anzahl der Aufgaben in der Auflistung erhalten und die einzelnen Aufgaben in der Auflistung aufzählen.

    Verwenden Sie [**die RegisteredTaskCollection-Auflistung**](registeredtaskcollection.md) von -Objekten, um eine [**RegisteredTask-Objektinstanz**](registeredtask.md) zu erhalten. Jede Instanz enthält eine Aufgabe in der Auflistung. Anschließend können Sie die Informationen (Eigenschaftswerte) jeder registrierten Aufgabe anzeigen.

Das folgende VBScript-Beispiel zeigt, wie Sie eine Auflistung registrierter Aufgaben im Stammaufgabenordner aufzählen und den Namen und Status für jede Aufgabe anzeigen.


```VB
'---------------------------------------------------------
' This sample enumerates through the tasks on the local computer and
' displays their name and state.
'---------------------------------------------------------


' Create the TaskService object.
Set service = CreateObject("Schedule.Service")
call service.Connect()

' Get the task folder that contains the tasks. 
Dim rootFolder
Set rootFolder = service.GetFolder("\")
 
Dim taskCollection
Set taskCollection = rootFolder.GetTasks(0)

Dim numberOfTasks
numberOfTasks = taskCollection.Count

If numberOfTasks = 0 Then 
    Wscript.Echo "No tasks are registered."
Else
    WScript.Echo "Number of tasks registered: " & numberOfTasks
    
    Dim registeredTask
    For Each registeredTask In taskCollection
        WScript.Echo "Task Name: " & registeredTask.Name
    
        Dim taskState 
        Select Case registeredTask.State 
            Case "0"
                taskState = "Unknown"
            Case "1"
                taskState = "Disabled"
            Case "2"
                taskState = "Queued"
            Case "3"
                taskState = "Ready"
            Case "4"
                taskState = "Running"
        End Select

        WScript.Echo "    Task State: " & taskState
    Next
End If

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




