---
description: 'Aufrufen der IAzClientContext:: AccessCheck-Methode, um zu überprüfen, ob der Client Zugriff auf einen oder mehrere Vorgänge hat.'
ms.assetid: cf1070fe-3737-4ae6-a8ef-f0782418a1d5
title: Überprüfen des Client Zugriffs auf angeforderte Ressourcen im Skript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6d5c3940e38d8a9a8befa00b85ac9c3cd406c292
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356251"
---
# <a name="verifying-client-access-to-requested-resources-in-script"></a><span data-ttu-id="49c60-103">Überprüfen des Client Zugriffs auf angeforderte Ressourcen im Skript</span><span class="sxs-lookup"><span data-stu-id="49c60-103">Verifying Client Access to Requested Resources in Script</span></span>

<span data-ttu-id="49c60-104">Ruft die [**Access Check**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) -Methode eines [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) -Objekts auf, um zu überprüfen, ob der Client Zugriff auf einen oder mehrere Vorgänge hat.</span><span class="sxs-lookup"><span data-stu-id="49c60-104">Call the [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method of an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object to check whether the client has access to one or more operations.</span></span> <span data-ttu-id="49c60-105">Weitere Informationen zum Erstellen eines **IAzClientContext** -Objekts finden Sie unter [Einrichten eines Client Kontexts im Skript](establishing-a-client-context-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="49c60-105">For information about creating an **IAzClientContext** object, see [Establishing a Client Context in Script](establishing-a-client-context-in-script.md).</span></span>

<span data-ttu-id="49c60-106">Ein Client kann möglicherweise Mitglied mehrerer Rollen sein, und ein Vorgang kann mehr als einer Aufgabe zugewiesen werden, sodass der Autorisierungs-Manager alle Rollen und Tasks prüft.</span><span class="sxs-lookup"><span data-stu-id="49c60-106">A client might have membership in more than one role, and an operation might be assigned to more than one task, so Authorization Manager checks for all roles and tasks.</span></span> <span data-ttu-id="49c60-107">Wenn eine Rolle, zu der der Client gehört, einen Task enthält, der einen Vorgang enthält, wird der Zugriff auf diesen Vorgang gewährt.</span><span class="sxs-lookup"><span data-stu-id="49c60-107">If any role to which the client belongs contains any task that contains an operation, access to that operation is granted.</span></span>

<span data-ttu-id="49c60-108">Um den Zugriff nur für eine einzige Rolle zu überprüfen, zu der der Client gehört, legen Sie die [**roleforaccesscheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) -Eigenschaft des [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) -Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="49c60-108">To check access for only a single role to which the client belongs, set the [**RoleForAccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) property of the [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object.</span></span>

<span data-ttu-id="49c60-109">Wenn Sie den Autorisierungs Richtlinien Speicher für die Zugriffs Überprüfung initialisieren, müssen Sie NULL als Wert des *lFlags* -Parameters der [**Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) -Methode des [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) -Objekts übergeben.</span><span class="sxs-lookup"><span data-stu-id="49c60-109">When initializing the authorization policy store for access check, you must pass zero as the value of the *lFlags* parameter of the [**Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) method of the [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span>

<span data-ttu-id="49c60-110">Es ist auch möglich, Geschäftslogik zur Laufzeit anzuwenden, um den Zugriff zu qualifizieren.</span><span class="sxs-lookup"><span data-stu-id="49c60-110">It is also possible to apply business logic at run time to qualify access.</span></span> <span data-ttu-id="49c60-111">Informationen zum Qualifizieren des Zugriffs mit Geschäftslogik finden Sie unter [qualifizieren des Zugriffs mit Geschäftslogik in Skripts](qualifying-access-with-business-logic-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="49c60-111">For information about qualifying access with business logic, see [Qualifying Access with Business Logic in Script](qualifying-access-with-business-logic-in-script.md).</span></span>

<span data-ttu-id="49c60-112">Im folgenden Beispiel wird gezeigt, wie der Zugriff eines Clients auf einen Vorgang überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="49c60-112">The following example shows how to check a client's access to an operation.</span></span> <span data-ttu-id="49c60-113">Im Beispiel wird davon ausgegangen, dass ein vorhandener XML-Richtlinien Speicher namens MyStore.xml im Stammverzeichnis des Laufwerks C vorhanden ist und dass dieser Speicher eine Anwendung mit dem Namen "Aufwendungen" und einen Vorgang mit dem Namen "useformcontrol" enthält.</span><span class="sxs-lookup"><span data-stu-id="49c60-113">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, and that this store contains an application named Expense and an operation named UseFormControl.</span></span>


```VB
<%@ Language=VBScript %>
<%
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 0, "msxml://C:\MyStore.xml"

'  Open the application object in the store.
Dim expenseApp
Set expenseApp = AzManStore.OpenApplication("Expense")

'  Create a client context.
Dim clientName
clientName = Request.ServerVariables("LOGON_USER")
Dim clientContext
Set clientContext = _
    expenseApp.InitializeClientContextFromName(clientName)

'  Open the operation to check.
Dim formOperation
Set formOperation = expenseApp.OpenOperation("UseFormControl")

'  Get the ID of the operation.
Dim operationID
operationID = formOperation.OperationID

'  Check access.
Dim Operations(1)
Operations(0) = operationID
Dim Results

Results = _
    clientContext.AccessCheck("UseFormControl", Empty, Operations)

%>
```



 

 



