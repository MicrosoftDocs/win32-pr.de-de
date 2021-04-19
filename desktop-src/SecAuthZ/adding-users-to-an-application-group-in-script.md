---
description: Eine Anwendungs Gruppe ist eine Gruppe von Benutzern und Benutzergruppen. Eine Anwendungs Gruppe kann andere Anwendungs Gruppen enthalten, sodass Gruppen von Benutzern gruppiert werden können. Eine Anwendungs Gruppe wird durch ein iazapplicationgroup-Objekt dargestellt.
ms.assetid: 9ec5b55e-3d66-44f6-9b59-a5e66192d8ac
title: Hinzufügen von Benutzern zu einer Anwendungs Gruppe im Skript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6fd92a69a236e6b4d04d5bb0a1a8b961c699d434
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363281"
---
# <a name="adding-users-to-an-application-group-in-script"></a><span data-ttu-id="b7270-105">Hinzufügen von Benutzern zu einer Anwendungs Gruppe im Skript</span><span class="sxs-lookup"><span data-stu-id="b7270-105">Adding Users to an Application Group in Script</span></span>

<span data-ttu-id="b7270-106">Im Autorisierungs-Manager ist eine Anwendungs Gruppe eine Gruppe von Benutzern und Benutzergruppen.</span><span class="sxs-lookup"><span data-stu-id="b7270-106">In Authorization Manager, an application group is a group of users and user groups.</span></span> <span data-ttu-id="b7270-107">Eine Anwendungs Gruppe kann andere Anwendungs Gruppen enthalten, sodass Gruppen von Benutzern gruppiert werden können.</span><span class="sxs-lookup"><span data-stu-id="b7270-107">An application group can contain other application groups, so groups of users can be nested.</span></span> <span data-ttu-id="b7270-108">Eine Anwendungs Gruppe wird durch ein [**iazapplicationgroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) -Objekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b7270-108">An application group is represented by an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object.</span></span>

<span data-ttu-id="b7270-109">**So gestatten Sie Mitgliedern einer Anwendungs Gruppe das Ausführen einer Aufgabe oder eines Satzes von Tasks**</span><span class="sxs-lookup"><span data-stu-id="b7270-109">**To allow members of an application group to perform a task or set of tasks**</span></span>

-   <span data-ttu-id="b7270-110">Weisen Sie diese Anwendungs Gruppe einer Rolle zu, in der diese Tasks enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b7270-110">Assign that application group to a role that contains those tasks.</span></span>

    <span data-ttu-id="b7270-111">Rollen werden durch [**iazrole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) -Objekte dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b7270-111">Roles are represented by [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) objects.</span></span>

<span data-ttu-id="b7270-112">Im folgenden Beispiel wird gezeigt, wie Sie eine Anwendungs Gruppe erstellen, einen Benutzer als Mitglied der Anwendungs Gruppe hinzufügen und die Anwendungs Gruppe einer vorhandenen Rolle zuweisen.</span><span class="sxs-lookup"><span data-stu-id="b7270-112">The following example shows how to create an application group, add a user as a member of the application group, and assign the application group to an existing role.</span></span> <span data-ttu-id="b7270-113">Im Beispiel wird davon ausgegangen, dass ein vorhandener XML-Richtlinien Speicher namens MyStore.xml im Stammverzeichnis des Laufwerks C vorhanden ist, dass dieser Speicher eine Anwendung mit dem Namen "Kosten" enthält und dass diese Anwendung eine Rolle mit dem Namen "Kosten Administrator" enthält.</span><span class="sxs-lookup"><span data-stu-id="b7270-113">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that this application contains a role named Expense Administrator.</span></span>


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("Approvers")

'  Add a member to the group.
'  Replace with valid domain and user name.
appGroup.AddMemberName("domain\\username")

'  Save information to the store.
appGroup.Submit

'  Open a role object.
Dim adminRole
Set adminRole = expenseApp.OpenRole("Expense Administrator")

'  Add the group to the role.
adminRole.AddAppMember("Approvers")

'  Save the information to the store.
adminRole.Submit
```



 

 



