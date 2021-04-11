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
# <a name="delegating-the-defining-of-permissions-in-script"></a><span data-ttu-id="3b4aa-103">Delegieren der Definition von Berechtigungen im Skript</span><span class="sxs-lookup"><span data-stu-id="3b4aa-103">Delegating the Defining of Permissions in Script</span></span>

<span data-ttu-id="3b4aa-104">Sie können die Verwaltung von Autorisierungs Richtlinien speichern delegieren, die in Active Directory gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3b4aa-104">You can delegate the administration of authorization policy stores that are stored in Active Directory.</span></span> <span data-ttu-id="3b4aa-105">Die Verwaltung kann an Benutzer und Gruppen auf Geschäfts-, Anwendungs-oder Bereichs Ebene delegiert werden.</span><span class="sxs-lookup"><span data-stu-id="3b4aa-105">Administration can be delegated to users and groups at the store, application, or scope level.</span></span>

<span data-ttu-id="3b4aa-106">Auf jeder Ebene ist eine Liste von Administratoren und Lesern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3b4aa-106">At each level, there is a list of administrators and readers.</span></span> <span data-ttu-id="3b4aa-107">Administratoren eines Stores, einer Anwendung oder eines Bereichs können den Richtlinien Speicher auf der Delegierten Ebene lesen und ändern.</span><span class="sxs-lookup"><span data-stu-id="3b4aa-107">Administrators of a store, application, or scope can read and modify the policy store at the delegated level.</span></span> <span data-ttu-id="3b4aa-108">Leser können den Richtlinien Speicher auf der Delegierten Ebene lesen, den Speicher jedoch nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="3b4aa-108">Readers can read the policy store at the delegated level but cannot modify the store.</span></span>

<span data-ttu-id="3b4aa-109">Ein Benutzer oder eine Gruppe, der entweder als Administrator oder als Leser einer Anwendung dient, muss auch als Delegierter Benutzer des Richtlinien Speicher hinzugefügt werden, der diese Anwendung enthält.</span><span class="sxs-lookup"><span data-stu-id="3b4aa-109">A user or group that is either an administrator or a reader of an application must also be added as a delegated user of the policy store that contains that application.</span></span> <span data-ttu-id="3b4aa-110">Ebenso muss ein Benutzer oder eine Gruppe, der ein Administrator oder ein Leser eines Bereichs ist, als Delegierter Benutzer der Anwendung hinzugefügt werden, die diesen Bereich enthält.</span><span class="sxs-lookup"><span data-stu-id="3b4aa-110">Similarly, a user or group that is an administrator or a reader of a scope must be added as a delegated user of the application that contains that scope.</span></span>

<span data-ttu-id="3b4aa-111">**So delegieren Sie die Verwaltung eines Bereichs**</span><span class="sxs-lookup"><span data-stu-id="3b4aa-111">**To delegate administration of a scope**</span></span>

1.  <span data-ttu-id="3b4aa-112">Fügen Sie den Benutzer oder die Gruppe der Liste der Delegierten Benutzer des Stores mit dem Bereich hinzu, indem Sie die [**adddelegatedpolicyuser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) -Methode des [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) -Objekts aufrufen, das den Bereich enthält.</span><span class="sxs-lookup"><span data-stu-id="3b4aa-112">Add the user or group to the list of delegated users of the store that contains the scope by calling the [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) method of the [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that contains the scope.</span></span>
2.  <span data-ttu-id="3b4aa-113">Fügen Sie den Benutzer oder die Gruppe der Liste der Delegierten Benutzer der Anwendung hinzu, die den Bereich enthält, indem Sie die [**adddelegatedpolicyuser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) -Methode des [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) -Objekts aufrufen, das den Bereich enthält.</span><span class="sxs-lookup"><span data-stu-id="3b4aa-113">Add the user or group to the list of delegated users of the application that contains the scope by calling the [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) method of the [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object that contains the scope.</span></span>
3.  <span data-ttu-id="3b4aa-114">Fügen Sie den Benutzer oder die Gruppe der Liste der Administratoren des Bereichs hinzu, indem Sie die [**addpolicyadministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) -Methode des [**iazscope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) -Objekts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3b4aa-114">Add the user or group to the list of administrators of the scope by calling the [**AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) method of the [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) object.</span></span>

> [!Note]  
> <span data-ttu-id="3b4aa-115">XML-basierte Richtlinien Speicher unterstützen nicht die Delegierung auf einer beliebigen Ebene.</span><span class="sxs-lookup"><span data-stu-id="3b4aa-115">XML-based policy stores do not support delegation at any level.</span></span>

 

<span data-ttu-id="3b4aa-116">Wenn ein Bereich in einem Autorisierungs Speicher, der in Active Directory gespeichert ist, Task Definitionen enthält, die Autorisierungs Regeln oder Rollen Definitionen enthalten, die Autorisierungs Regeln enthalten, kann der Bereich nicht delegiert werden.</span><span class="sxs-lookup"><span data-stu-id="3b4aa-116">If a scope within an authorization store that is stored in Active Directory contains task definitions that include authorization rules or role definitions that include authorization rules, the scope cannot be delegated.</span></span>

<span data-ttu-id="3b4aa-117">Im folgenden Beispiel wird gezeigt, wie die Verwaltung einer Anwendung delegiert wird.</span><span class="sxs-lookup"><span data-stu-id="3b4aa-117">The following example shows how to delegate administration of an application.</span></span> <span data-ttu-id="3b4aa-118">Im Beispiel wird davon ausgegangen, dass am angegebenen Speicherort ein Active Directory Autorisierungs Richtlinien Speicher vorhanden ist, dass dieser Richtlinien Speicher eine Anwendung mit dem Namen "Kosten" enthält und dass diese Anwendung keine Aufgaben mit Geschäftsregel Skripts enthält.</span><span class="sxs-lookup"><span data-stu-id="3b4aa-118">The example assumes that there is an existing Active Directory authorization policy store at the specified location, that this policy store contains an application named Expense, and that this application contains no tasks with business rule scripts.</span></span>


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



 

 



