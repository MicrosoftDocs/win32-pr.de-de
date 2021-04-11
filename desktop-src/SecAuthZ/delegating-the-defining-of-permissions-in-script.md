---
description: Sie können die Verwaltung der Autorisierungs Richtlinien Speicher delegieren, die in Active Directory gespeichert werden.
ms.assetid: a7b43dfe-f03e-4795-bbd3-746eb3449fd0
title: Delegieren der Definition von Berechtigungen im Skript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a9569f82271642a610919db8246cc6389daba309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346558"
---
# <a name="delegating-the-defining-of-permissions-in-script"></a>Delegieren der Definition von Berechtigungen im Skript

Sie können die Verwaltung von Autorisierungs Richtlinien speichern delegieren, die in Active Directory gespeichert werden. Die Verwaltung kann an Benutzer und Gruppen auf Geschäfts-, Anwendungs-oder Bereichs Ebene delegiert werden.

Auf jeder Ebene ist eine Liste von Administratoren und Lesern vorhanden. Administratoren eines Stores, einer Anwendung oder eines Bereichs können den Richtlinien Speicher auf der Delegierten Ebene lesen und ändern. Leser können den Richtlinien Speicher auf der Delegierten Ebene lesen, den Speicher jedoch nicht ändern.

Ein Benutzer oder eine Gruppe, der entweder als Administrator oder als Leser einer Anwendung dient, muss auch als Delegierter Benutzer des Richtlinien Speicher hinzugefügt werden, der diese Anwendung enthält. Ebenso muss ein Benutzer oder eine Gruppe, der ein Administrator oder ein Leser eines Bereichs ist, als Delegierter Benutzer der Anwendung hinzugefügt werden, die diesen Bereich enthält.

**So delegieren Sie die Verwaltung eines Bereichs**

1.  Fügen Sie den Benutzer oder die Gruppe der Liste der Delegierten Benutzer des Stores mit dem Bereich hinzu, indem Sie die [**adddelegatedpolicyuser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) -Methode des [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) -Objekts aufrufen, das den Bereich enthält.
2.  Fügen Sie den Benutzer oder die Gruppe der Liste der Delegierten Benutzer der Anwendung hinzu, die den Bereich enthält, indem Sie die [**adddelegatedpolicyuser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) -Methode des [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) -Objekts aufrufen, das den Bereich enthält.
3.  Fügen Sie den Benutzer oder die Gruppe der Liste der Administratoren des Bereichs hinzu, indem Sie die [**addpolicyadministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) -Methode des [**iazscope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) -Objekts aufrufen.

> [!Note]  
> XML-basierte Richtlinien Speicher unterstützen nicht die Delegierung auf einer beliebigen Ebene.

 

Wenn ein Bereich in einem Autorisierungs Speicher, der in Active Directory gespeichert ist, Task Definitionen enthält, die Autorisierungs Regeln oder Rollen Definitionen enthalten, die Autorisierungs Regeln enthalten, kann der Bereich nicht delegiert werden.

Im folgenden Beispiel wird gezeigt, wie die Verwaltung einer Anwendung delegiert wird. Im Beispiel wird davon ausgegangen, dass am angegebenen Speicherort ein Active Directory Autorisierungs Richtlinien Speicher vorhanden ist, dass dieser Richtlinien Speicher eine Anwendung mit dem Namen "Kosten" enthält und dass diese Anwendung keine Aufgaben mit Geschäftsregel Skripts enthält.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, _
    "msldap://CN=MyStore,CN=Program Data,DC=authmanager,DC=com"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Add a delegated policy user to the store.
AzManStore.AddDelegatedPolicyUserName("ExampleDomain\\UserName")

'  Add the user as an administrator of the application.
expenseApp.AddPolicyAdministratorName("ExampleDomain\\UserName")

'  Save changes to the store.
AzManStore.Submit
```



 

 



