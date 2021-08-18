---
description: Eine Anwendungsgruppe ist eine Gruppe von Benutzern und Benutzergruppen. Eine Anwendungsgruppe kann andere Anwendungsgruppen enthalten, sodass Benutzergruppen geschachtelt werden können. Eine Anwendungsgruppe wird durch ein IAzApplicationGroup-Objekt dargestellt.
ms.assetid: 9ec5b55e-3d66-44f6-9b59-a5e66192d8ac
title: Hinzufügen von Benutzern zu einer Anwendungsgruppe im Skript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 18c990e3140dcfc6a4cbc2d57379431075387f43af8fbb0b22f344ffd0b9a30b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784932"
---
# <a name="adding-users-to-an-application-group-in-script"></a>Hinzufügen von Benutzern zu einer Anwendungsgruppe im Skript

Im Autorisierungs-Manager ist eine Anwendungsgruppe eine Gruppe von Benutzern und Benutzergruppen. Eine Anwendungsgruppe kann andere Anwendungsgruppen enthalten, sodass Benutzergruppen geschachtelt werden können. Eine Anwendungsgruppe wird durch ein [**IAzApplicationGroup-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) dargestellt.

**So erlauben Sie Mitgliedern einer Anwendungsgruppe das Ausführen einer Aufgabe oder einer Gruppe von Aufgaben**

-   Weisen Sie diese Anwendungsgruppe einer Rolle zu, die diese Aufgaben enthält.

    Rollen werden durch [**IAzRole-Objekte**](/windows/desktop/api/Azroles/nn-azroles-iazrole) dargestellt.

Das folgende Beispiel zeigt, wie Sie eine Anwendungsgruppe erstellen, einen Benutzer als Mitglied der Anwendungsgruppe hinzufügen und die Anwendungsgruppe einer vorhandenen Rolle zuweisen. Im Beispiel wird davon ausgegangen, dass im Stammverzeichnis von Laufwerk C ein vorhandener XML-Richtlinienspeicher namens MyStore.xml vorhanden ist, dass dieser Speicher eine Anwendung mit dem Namen Expense enthält und dass diese Anwendung eine Rolle namens Expense Administrator enthält.


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



 

 



