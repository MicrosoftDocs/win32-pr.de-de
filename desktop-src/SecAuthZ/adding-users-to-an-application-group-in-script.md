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
# <a name="adding-users-to-an-application-group-in-script"></a>Hinzufügen von Benutzern zu einer Anwendungs Gruppe im Skript

Im Autorisierungs-Manager ist eine Anwendungs Gruppe eine Gruppe von Benutzern und Benutzergruppen. Eine Anwendungs Gruppe kann andere Anwendungs Gruppen enthalten, sodass Gruppen von Benutzern gruppiert werden können. Eine Anwendungs Gruppe wird durch ein [**iazapplicationgroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) -Objekt dargestellt.

**So gestatten Sie Mitgliedern einer Anwendungs Gruppe das Ausführen einer Aufgabe oder eines Satzes von Tasks**

-   Weisen Sie diese Anwendungs Gruppe einer Rolle zu, in der diese Tasks enthalten sind.

    Rollen werden durch [**iazrole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) -Objekte dargestellt.

Im folgenden Beispiel wird gezeigt, wie Sie eine Anwendungs Gruppe erstellen, einen Benutzer als Mitglied der Anwendungs Gruppe hinzufügen und die Anwendungs Gruppe einer vorhandenen Rolle zuweisen. Im Beispiel wird davon ausgegangen, dass ein vorhandener XML-Richtlinien Speicher namens MyStore.xml im Stammverzeichnis des Laufwerks C vorhanden ist, dass dieser Speicher eine Anwendung mit dem Namen "Kosten" enthält und dass diese Anwendung eine Rolle mit dem Namen "Kosten Administrator" enthält.


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



 

 



