---
description: Im Autorisierungs-Manager ist eine Aufgabe eine übergeordnete Aktion, die Benutzer einer Anwendung ausführen müssen.
ms.assetid: a266dde7-86f8-4537-99a5-be7142e765c6
title: Gruppieren von Vorgängen in Tasks in Skripts
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 29c7dedb9944a208e5ba128f0341a8cbde3e787056c099d527be8f79260c6f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913574"
---
# <a name="grouping-operations-into-tasks-in-script"></a>Gruppieren von Vorgängen in Tasks in Skripts

Im Autorisierungs-Manager ist eine Aufgabe eine übergeordnete Aktion, die Benutzer einer Anwendung ausführen müssen. Aufgaben bestehen aus Vorgängen, bei denen es sich um Funktionen und Methoden auf niedriger Ebene der Anwendung handelt. Eine Aufgabe wird dann den Rollen zugewiesen, die diese Aufgabe ausführen müssen. Eine Aufgabe wird durch ein [**IAzTask-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iaztask) dargestellt. Weitere Informationen zu Vorgängen und Aufgaben finden Sie unter [Vorgänge und Aufgaben.](operations-and-tasks.md)

Das folgende Beispiel zeigt, wie Vorgänge gruppiert werden, um eine Aufgabe zu erstellen. Im Beispiel wird davon ausgegangen, dass im Stammverzeichnis von Laufwerk C ein vorhandener XML-Richtlinienspeicher mit dem Namen MyStore.xml vorhanden ist, dass dieser Speicher eine Anwendung mit dem Namen Expense enthält und dass diese Anwendung Vorgänge enthält, die im Thema [Definieren von Vorgängen in Skript](defining-operations-in-script.md)definiert sind.


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



 

 



