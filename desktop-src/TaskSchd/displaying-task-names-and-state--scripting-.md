---
title: Anzeigen von Aufgaben Namen und-Zuständen (Skripterstellung)
description: In diesem Skript Beispiel wird gezeigt, wie Aufgaben in einem Aufgaben Ordner aufgelistet und Eigenschaftswerte aus den einzelnen Tasks angezeigt werden.
ms.assetid: 2a84a752-fbf3-4041-8b0a-304f89a49354
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e7a8f22977f8cfd2d40b3c37a1cc8d7bcb5259e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388466"
---
# <a name="displaying-task-names-and-states-scripting"></a>Anzeigen von Aufgaben Namen und-Zuständen (Skripterstellung)

In diesem Skript Beispiel wird gezeigt, wie Aufgaben in einem Aufgaben Ordner aufgelistet und Eigenschaftswerte aus den einzelnen Tasks angezeigt werden.

Im folgenden Verfahren wird beschrieben, wie Aufgaben Namen und Zustände für alle Aufgaben in einem Aufgaben Ordner angezeigt werden.

**So zeigen Sie Aufgaben Namen und den Status für alle Aufgaben in einem Aufgaben Ordner an**

1.  Erstellen Sie das [**Task Service**](taskservice.md) -Objekt.

    Mit diesem Objekt können Sie eine Verbindung mit dem Taskplaner-Dienst herstellen und auf einen bestimmten Aufgaben Ordner zugreifen.

2.  Sie erhalten einen Aufgaben Ordner, der die Aufgaben enthält, über die Sie Informationen erhalten möchten.

    Verwenden Sie die [**TaskService. GetFolder**](taskservice-getfolder.md) -Methode, um den Ordner zu erhalten.

3.  Die Auflistung von Tasks aus dem Ordner erhalten.

    Verwenden Sie die [**Task Folder. GetTasks**](taskfolder-gettasks.md) -Methode, um die Sammlung von Aufgaben ([**registeredtaskcollection**](registeredtaskcollection.md)) zu erhalten.

4.  Gibt die Anzahl der Aufgaben in der Auflistung an und listet die einzelnen Aufgaben in der Sammlung auf.

    Verwenden Sie die [**registeredtaskcollection**](registeredtaskcollection.md) -Auflistung von-Objekten, um eine [**registeredtask**](registeredtask.md) -Objektinstanz zu erhalten. Jede Instanz enthält eine Aufgabe in der Auflistung. Anschließend können Sie die Informationen (Eigenschaftswerte) für jede registrierte Aufgabe anzeigen.

Im folgenden VBScript-Beispiel wird gezeigt, wie Sie eine Auflistung registrierter Tasks im Stamm Aufgaben Ordner auflisten und den Namen und den Status für die einzelnen Aufgaben anzeigen.


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

[Verwenden des Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




