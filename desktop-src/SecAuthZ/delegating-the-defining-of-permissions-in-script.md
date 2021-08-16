---
description: Sie können die Verwaltung der in Active Directory gespeicherten Autorisierungsrichtlinienspeicher delegieren.
ms.assetid: a7b43dfe-f03e-4795-bbd3-746eb3449fd0
title: Delegieren der Definition von Berechtigungen im Skript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 69cf0793a48a572ec4b37cbf3634f65b04ff3565f3205bf0380c68914abb4530
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782064"
---
# <a name="delegating-the-defining-of-permissions-in-script"></a>Delegieren der Definition von Berechtigungen im Skript

Sie können die Verwaltung von Autorisierungsrichtlinienspeichern delegieren, die in Active Directory gespeichert sind. Die Verwaltung kann an Benutzer und Gruppen auf Store-, Anwendungs- oder Bereichsebene delegiert werden.

Auf jeder Ebene gibt es eine Liste von Administratoren und Lesern. Administratoren eines Speichers, einer Anwendung oder eines Bereichs können den Richtlinienspeicher auf delegierter Ebene lesen und ändern. Leser können den Richtlinienspeicher auf delegierter Ebene lesen, aber den Speicher nicht ändern.

Ein Benutzer oder eine Gruppe, der bzw. die entweder Ein Administrator oder Leser einer Anwendung ist, muss auch als delegierter Benutzer des Richtlinienspeichers hinzugefügt werden, der diese Anwendung enthält. Ebenso muss ein Benutzer oder eine Gruppe, der bzw. die ein Administrator oder Leser eines Bereichs ist, als delegierter Benutzer der Anwendung hinzugefügt werden, die diesen Bereich enthält.

**So delegieren Sie die Verwaltung eines Bereichs**

1.  Fügen Sie den Benutzer oder die Gruppe der Liste der delegierten Benutzer des Speichers hinzu, der den Bereich enthält, indem Sie die [**AddDelegatedPolicyUser-Methode**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) des [**AzAuthorizationStore-Objekts**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) aufrufen, das den Bereich enthält.
2.  Fügen Sie den Benutzer oder die Gruppe der Liste der delegierten Benutzer der Anwendung hinzu, die den Bereich enthält, indem Sie die [**AddDelegatedPolicyUser-Methode**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) des [**IAzApplication-Objekts**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) aufrufen, das den Bereich enthält.
3.  Fügen Sie den Benutzer oder die Gruppe der Liste der Administratoren des Bereichs hinzu, indem Sie die [**AddPolicyAdministrator-Methode**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) des [**IAzScope-Objekts**](/windows/desktop/api/Azroles/nn-azroles-iazscope) aufrufen.

> [!Note]  
> XML-basierte Richtlinienspeicher unterstützen keine Delegierung auf einer beliebigen Ebene.

 

Wenn ein Bereich in einem Autorisierungsspeicher, der in Active Directory gespeichert ist, Aufgabendefinitionen enthält, die Autorisierungsregeln oder Rollendefinitionen enthalten, die Autorisierungsregeln enthalten, kann der Bereich nicht delegiert werden.

Das folgende Beispiel zeigt, wie die Verwaltung einer Anwendung delegiert wird. Im Beispiel wird davon ausgegangen, dass am angegebenen Speicherort ein Active Directory-Autorisierungsrichtlinienspeicher vorhanden ist, dass dieser Richtlinienspeicher eine Anwendung mit dem Namen Expense enthält und dass diese Anwendung keine Aufgaben mit Geschäftsregelskripts enthält.


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



 

 



