---
description: Im Autorisierungs-Manager ist eine Aufgabe eine allgemeine Aktion, die Benutzer einer Anwendung ausführen müssen.
ms.assetid: a266dde7-86f8-4537-99a5-be7142e765c6
title: Gruppieren von Vorgängen in Aufgaben in Skripts
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fb7fc1d4a84cd42dc0ae48af4fcbf02412b93337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867831"
---
# <a name="grouping-operations-into-tasks-in-script"></a><span data-ttu-id="d2499-103">Gruppieren von Vorgängen in Aufgaben in Skripts</span><span class="sxs-lookup"><span data-stu-id="d2499-103">Grouping Operations into Tasks in Script</span></span>

<span data-ttu-id="d2499-104">Im Autorisierungs-Manager ist eine Aufgabe eine allgemeine Aktion, die Benutzer einer Anwendung ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="d2499-104">In Authorization Manager, a task is a high-level action that users of an application need to complete.</span></span> <span data-ttu-id="d2499-105">Aufgaben bestehen aus Vorgängen, bei denen es sich um Low-Level-Funktionen und-Methoden der Anwendung handelt.</span><span class="sxs-lookup"><span data-stu-id="d2499-105">Tasks are made up of operations, which are low-level functions and methods of the application.</span></span> <span data-ttu-id="d2499-106">Anschließend wird eine Aufgabe den Rollen zugewiesen, die diese Aufgabe ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="d2499-106">A task is then assigned to those roles that must perform that task.</span></span> <span data-ttu-id="d2499-107">Eine Aufgabe wird durch ein [**iaztask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) -Objekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d2499-107">A task is represented by an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object.</span></span> <span data-ttu-id="d2499-108">Weitere Informationen zu Vorgängen und Aufgaben finden Sie unter [Vorgänge und Aufgaben](operations-and-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="d2499-108">For more information about operations and tasks, see [Operations and Tasks](operations-and-tasks.md).</span></span>

<span data-ttu-id="d2499-109">Im folgenden Beispiel wird gezeigt, wie Sie Vorgänge gruppieren, um eine Aufgabe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d2499-109">The following example shows how to group operations to create a task.</span></span> <span data-ttu-id="d2499-110">Im Beispiel wird davon ausgegangen, dass ein vorhandener XML-Richtlinien Speicher namens MyStore.xml im Stammverzeichnis des Laufwerks C vorhanden ist, dass dieser Speicher eine Anwendung mit dem Namen "Kosten" enthält und dass diese Anwendung Vorgänge enthält, die im Thema [Definieren von Vorgängen im Skript](defining-operations-in-script.md)definiert sind.</span><span class="sxs-lookup"><span data-stu-id="d2499-110">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that this application contains operations defined in the topic [Defining Operations in Script](defining-operations-in-script.md).</span></span>


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create a task object.
Dim Task1
Set Task1 = expenseApp.CreateTask("Submit Expense")

'  Add operations to the task.
Task1.AddOperation CStr("RetrieveForm")
Task1.AddOperation CStr("EnqueRequest")
Task1.AddOperation Cstr("UseFormControl")

'  Save the task to the store.
Task1.Submit
```



 

 



