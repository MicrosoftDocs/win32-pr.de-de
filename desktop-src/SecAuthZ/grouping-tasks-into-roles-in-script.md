---
description: Im Autorisierungs-Manager stellt eine Rolle eine Kategorie von Benutzern und die Aufgaben dar, für die diese Benutzer autorisiert sind.
ms.assetid: a4981774-0f5c-4032-8a7d-d9ef44c76abe
title: Gruppieren von Aufgaben in Rollen in Skripts
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: db0314ad953eecb94f10c995dea28e1dc3d69b586c386a94ae4f1ed45037fdcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913584"
---
# <a name="grouping-tasks-into-roles-in-script"></a>Gruppieren von Aufgaben in Rollen in Skripts

Im Autorisierungs-Manager stellt eine Rolle eine Kategorie von Benutzern und die Aufgaben dar, für die diese Benutzer autorisiert sind. Aufgaben werden gruppiert und einer Rollendefinition zugewiesen, die durch ein [**IAzTask-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iaztask) dargestellt wird, dessen [**IsRoleDefinition-Eigenschaft**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) auf **True** festgelegt ist. Die Rollendefinition kann dann einem [**IAzRole-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iazrole) zugewiesen werden, und Benutzer oder Benutzergruppen werden dann diesem Objekt zugewiesen. Weitere Informationen zu Aufgaben und Rollen finden Sie unter [Rollen.](roles.md)

Das folgende Beispiel zeigt, wie Sie einer Rollendefinition Aufgaben zuweisen, ein Rollenobjekt erstellen und die Rollendefinition dem Rollenobjekt zuweisen. Im Beispiel wird davon ausgegangen, dass im Stammverzeichnis von Laufwerk C ein vorhandener XML-Richtlinienspeicher namens MyStore.xml vorhanden ist, dass dieser Speicher eine Anwendung mit dem Namen Expense enthält und dass diese Anwendung Aufgaben mit dem Namen Submit Expense und Approve Expense enthält.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp = AzManStore.OpenApplication("Expense")

'  Create a task object to act as a role definition.
Dim roleTask
Set roleTask = expenseApp.CreateTask("Expense Admin")

'  Set the IsRoleDefinition property of roleTask to True.
roleTask.IsRoleDefinition = True

'  Add two tasks to the role definition.
roleTask.AddTask CStr("Submit Expense")
roleTask.AddTask CStr("Approve Expense")

'  Save the role definition to the store.
roleTask.Submit

'  Create a role object.
Dim role1
Set role1 = expenseApp.CreateRole("Expense Administrator")

'  Add the role definition to the role object.
role1.AddTask(roleTask.Name)

'  Save the role object to the store.
role1.Submit
```



 

 



