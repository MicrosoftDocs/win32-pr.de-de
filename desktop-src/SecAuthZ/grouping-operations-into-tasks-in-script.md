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
# <a name="grouping-operations-into-tasks-in-script"></a>Gruppieren von Vorgängen in Aufgaben in Skripts

Im Autorisierungs-Manager ist eine Aufgabe eine allgemeine Aktion, die Benutzer einer Anwendung ausführen müssen. Aufgaben bestehen aus Vorgängen, bei denen es sich um Low-Level-Funktionen und-Methoden der Anwendung handelt. Anschließend wird eine Aufgabe den Rollen zugewiesen, die diese Aufgabe ausführen müssen. Eine Aufgabe wird durch ein [**iaztask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) -Objekt dargestellt. Weitere Informationen zu Vorgängen und Aufgaben finden Sie unter [Vorgänge und Aufgaben](operations-and-tasks.md).

Im folgenden Beispiel wird gezeigt, wie Sie Vorgänge gruppieren, um eine Aufgabe zu erstellen. Im Beispiel wird davon ausgegangen, dass ein vorhandener XML-Richtlinien Speicher namens MyStore.xml im Stammverzeichnis des Laufwerks C vorhanden ist, dass dieser Speicher eine Anwendung mit dem Namen "Kosten" enthält und dass diese Anwendung Vorgänge enthält, die im Thema [Definieren von Vorgängen im Skript](defining-operations-in-script.md)definiert sind.


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



 

 



