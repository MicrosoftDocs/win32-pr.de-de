---
description: Im Autorisierungs-Manager stellt eine Rolle eine Kategorie von Benutzern und die Aufgaben dar, die diese Benutzer für die Ausführung autorisiert haben.
ms.assetid: a4981774-0f5c-4032-8a7d-d9ef44c76abe
title: Gruppieren von Aufgaben in Rollen in Skripts
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c84ec45bba8da9d76e2a4fe0b31324429374a74b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960538"
---
# <a name="grouping-tasks-into-roles-in-script"></a><span data-ttu-id="9d096-103">Gruppieren von Aufgaben in Rollen in Skripts</span><span class="sxs-lookup"><span data-stu-id="9d096-103">Grouping Tasks into Roles in Script</span></span>

<span data-ttu-id="9d096-104">Im Autorisierungs-Manager stellt eine Rolle eine Kategorie von Benutzern und die Aufgaben dar, die diese Benutzer für die Ausführung autorisiert haben.</span><span class="sxs-lookup"><span data-stu-id="9d096-104">In Authorization Manager, a role represents a category of users and the tasks those users are authorized to perform.</span></span> <span data-ttu-id="9d096-105">Tasks werden gruppiert und einer Rollendefinition zugewiesen, die durch ein [**iaztask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) -Objekt dargestellt wird, dessen [**isroledefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) -Eigenschaft auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9d096-105">Tasks are grouped together and assigned to a role definition, which is represented by an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object with its [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) property set to **True**.</span></span> <span data-ttu-id="9d096-106">Die Rollendefinition kann dann einem [**iazrole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) -Objekt zugewiesen werden, und Benutzer oder Benutzergruppen werden dann diesem Objekt zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="9d096-106">The role definition can then be assigned to an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object, and users or groups of users are then assigned to that object.</span></span> <span data-ttu-id="9d096-107">Weitere Informationen zu Aufgaben und Rollen finden Sie unter [Rollen](roles.md).</span><span class="sxs-lookup"><span data-stu-id="9d096-107">For more information about tasks and roles, see [Roles](roles.md).</span></span>

<span data-ttu-id="9d096-108">Im folgenden Beispiel wird gezeigt, wie Aufgaben einer Rollendefinition zugewiesen werden, ein Rollen Objekt erstellt und die Rollendefinition dem Rollen Objekt zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9d096-108">The following example shows how to assign tasks to a role definition, create a role object, and assign the role definition to the role object.</span></span> <span data-ttu-id="9d096-109">In diesem Beispiel wird davon ausgegangen, dass ein vorhandener XML-Richtlinien Speicher namens MyStore.xml im Stammverzeichnis des Laufwerks C vorhanden ist, dass dieser Speicher eine Anwendung mit dem Namen "Kosten" enthält und dass diese Anwendung Tasks mit dem Namen "Kosten übermitteln" und "Genehmigungskosten</span><span class="sxs-lookup"><span data-stu-id="9d096-109">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that this application contains tasks named Submit Expense and Approve Expense.</span></span>


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



 

 



