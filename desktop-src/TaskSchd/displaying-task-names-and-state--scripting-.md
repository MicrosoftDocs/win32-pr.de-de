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
# <a name="displaying-task-names-and-states-scripting"></a><span data-ttu-id="39d61-103">Anzeigen von Aufgaben Namen und-Zuständen (Skripterstellung)</span><span class="sxs-lookup"><span data-stu-id="39d61-103">Displaying Task Names and States (Scripting)</span></span>

<span data-ttu-id="39d61-104">In diesem Skript Beispiel wird gezeigt, wie Aufgaben in einem Aufgaben Ordner aufgelistet und Eigenschaftswerte aus den einzelnen Tasks angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="39d61-104">This scripting example shows how to enumerate tasks in a task folder and display property values from each task.</span></span>

<span data-ttu-id="39d61-105">Im folgenden Verfahren wird beschrieben, wie Aufgaben Namen und Zustände für alle Aufgaben in einem Aufgaben Ordner angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="39d61-105">The following procedure describes how to display task names and states for all the tasks in a task folder.</span></span>

<span data-ttu-id="39d61-106">**So zeigen Sie Aufgaben Namen und den Status für alle Aufgaben in einem Aufgaben Ordner an**</span><span class="sxs-lookup"><span data-stu-id="39d61-106">**To display task names and state for all the tasks in a task folder**</span></span>

1.  <span data-ttu-id="39d61-107">Erstellen Sie das [**Task Service**](taskservice.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="39d61-107">Create the [**TaskService**](taskservice.md) object.</span></span>

    <span data-ttu-id="39d61-108">Mit diesem Objekt können Sie eine Verbindung mit dem Taskplaner-Dienst herstellen und auf einen bestimmten Aufgaben Ordner zugreifen.</span><span class="sxs-lookup"><span data-stu-id="39d61-108">This object allows you to connect to the Task Scheduler service and access a specific task folder.</span></span>

2.  <span data-ttu-id="39d61-109">Sie erhalten einen Aufgaben Ordner, der die Aufgaben enthält, über die Sie Informationen erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="39d61-109">Get a task folder that holds the tasks you want information about.</span></span>

    <span data-ttu-id="39d61-110">Verwenden Sie die [**TaskService. GetFolder**](taskservice-getfolder.md) -Methode, um den Ordner zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="39d61-110">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder.</span></span>

3.  <span data-ttu-id="39d61-111">Die Auflistung von Tasks aus dem Ordner erhalten.</span><span class="sxs-lookup"><span data-stu-id="39d61-111">Get the collection of tasks from the folder.</span></span>

    <span data-ttu-id="39d61-112">Verwenden Sie die [**Task Folder. GetTasks**](taskfolder-gettasks.md) -Methode, um die Sammlung von Aufgaben ([**registeredtaskcollection**](registeredtaskcollection.md)) zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="39d61-112">Use the [**TaskFolder.GetTasks**](taskfolder-gettasks.md) method to get the collection of tasks ([**RegisteredTaskCollection**](registeredtaskcollection.md)).</span></span>

4.  <span data-ttu-id="39d61-113">Gibt die Anzahl der Aufgaben in der Auflistung an und listet die einzelnen Aufgaben in der Sammlung auf.</span><span class="sxs-lookup"><span data-stu-id="39d61-113">Get the number of tasks in the collection and enumerate through each task in the collection.</span></span>

    <span data-ttu-id="39d61-114">Verwenden Sie die [**registeredtaskcollection**](registeredtaskcollection.md) -Auflistung von-Objekten, um eine [**registeredtask**](registeredtask.md) -Objektinstanz zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="39d61-114">Use the [**RegisteredTaskCollection**](registeredtaskcollection.md) collection of objects to get a [**RegisteredTask**](registeredtask.md) object instance.</span></span> <span data-ttu-id="39d61-115">Jede Instanz enthält eine Aufgabe in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="39d61-115">Each instance will contain a task in the collection.</span></span> <span data-ttu-id="39d61-116">Anschließend können Sie die Informationen (Eigenschaftswerte) für jede registrierte Aufgabe anzeigen.</span><span class="sxs-lookup"><span data-stu-id="39d61-116">You can then display the information (property values) from each registered task.</span></span>

<span data-ttu-id="39d61-117">Im folgenden VBScript-Beispiel wird gezeigt, wie Sie eine Auflistung registrierter Tasks im Stamm Aufgaben Ordner auflisten und den Namen und den Status für die einzelnen Aufgaben anzeigen.</span><span class="sxs-lookup"><span data-stu-id="39d61-117">The following VBScript example shows how to enumerate through a collection of registered tasks in the root task folder and display the name and state for each task.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="39d61-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="39d61-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39d61-119">Verwenden des Taskplaner</span><span class="sxs-lookup"><span data-stu-id="39d61-119">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




