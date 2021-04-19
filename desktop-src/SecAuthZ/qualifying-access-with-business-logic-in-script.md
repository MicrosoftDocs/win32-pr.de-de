---
description: Verwenden von Geschäftsregel Skripts in Skripts zum Bereitstellen von Lauf Zeit Logik zum Überprüfen des Zugriffs.
ms.assetid: 10c28ecb-3f36-45a8-b037-7038e8927b6b
title: Qualifizieren des Zugriffs mit Geschäftslogik in Skripts
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 65ee69e0572c0f480cded2930ea81ac6da710b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360087"
---
# <a name="qualifying-access-with-business-logic-in-script"></a><span data-ttu-id="13c9f-103">Qualifizieren des Zugriffs mit Geschäftslogik in Skripts</span><span class="sxs-lookup"><span data-stu-id="13c9f-103">Qualifying Access with Business Logic in Script</span></span>

<span data-ttu-id="13c9f-104">Verwenden Sie Geschäftsregel Skripts, um Lauf Zeit Logik zum Überprüfen des Zugriffs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="13c9f-104">Use business rule scripts to provide run-time logic for checking access.</span></span> <span data-ttu-id="13c9f-105">Weitere Informationen zu Geschäftsregeln finden Sie unter [Geschäftsregeln](business-rules.md).</span><span class="sxs-lookup"><span data-stu-id="13c9f-105">For more information about business rules, see [Business Rules](business-rules.md).</span></span>

<span data-ttu-id="13c9f-106">Um einer Aufgabe eine Geschäftsregel zuzuweisen, legen Sie zunächst die Eigenschaft [**BizRuleLanguage**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) des [**iaztask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) -Objekts fest, das die Aufgabe darstellt.</span><span class="sxs-lookup"><span data-stu-id="13c9f-106">To assign a business rule to a task, first set the [**BizRuleLanguage**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) property of the [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object that represents the task.</span></span> <span data-ttu-id="13c9f-107">Das Skript muss mithilfe der Visual Basic Scripting Edition Programmiersprache (VBScript) oder der JScript-Entwicklungssoftware geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="13c9f-107">The script must be written using the Visual Basic Scripting Edition (VBScript) programming language or JScript development software.</span></span> <span data-ttu-id="13c9f-108">Nachdem Sie die Skriptsprache angegeben haben, legen Sie die Eigenschaft [**BizRule**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) des **iaztask** -Objekts auf eine Zeichen folgen Darstellung des Skripts fest.</span><span class="sxs-lookup"><span data-stu-id="13c9f-108">After you specify the script language, set the [**BizRule**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) property of the **IAzTask** object with a string representation of the script.</span></span>

<span data-ttu-id="13c9f-109">Beim Überprüfen des Zugriffs für einen Vorgang, der in einem Task enthalten ist, dem eine Geschäftsregel zugeordnet ist, muss die Anwendung zwei Arrays derselben Größe erstellen, die als Parameter des Typs " *varParameterNames* " und " *varParameterValues* " der [**Access Check**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) -Methode eines [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) -Objekts übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="13c9f-109">When checking access for an operation contained by a task that has an associated business rule, the application must create two arrays of the same size to be passed as the *varParameterNames* and *varParameterValues* parameters of the [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method of an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object.</span></span> <span data-ttu-id="13c9f-110">Weitere Informationen zum Erstellen eines Client Kontexts finden Sie unter [Einrichten eines Client Kontexts in einem Skript](establishing-a-client-context-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="13c9f-110">For information about creating a client context, see [Establishing a Client Context in Script](establishing-a-client-context-in-script.md).</span></span>

<span data-ttu-id="13c9f-111">Die [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) -Methode erstellt ein [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) -Objekt, das an das Geschäftsregel Skript übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="13c9f-111">The [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method creates an [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) object that is passed to the business rule script.</span></span> <span data-ttu-id="13c9f-112">Das Skript legt dann die Eigenschaft [**BusinessRuleResult**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) des **AzBizRuleContext** -Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="13c9f-112">The script then sets the [**BusinessRuleResult**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) property of the **AzBizRuleContext** object.</span></span> <span data-ttu-id="13c9f-113">Der Wert **true** gibt an, dass der Zugriff gewährt wird, und der Wert **false** gibt an, dass der Zugriff verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="13c9f-113">A value of **True** indicates that access is granted, and a value of **False** indicates that access is denied.</span></span>

<span data-ttu-id="13c9f-114">Einem [**iaztask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) -Objekt, das in einem Delegierten [**iazscope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) -Objekt enthalten ist, kann kein Geschäftsregel Skript zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="13c9f-114">A business rule script cannot be assigned to an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object contained by a delegated [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) object.</span></span>

<span data-ttu-id="13c9f-115">Im folgenden Beispiel wird gezeigt, wie ein Geschäftsregel Skript verwendet wird, um den Zugriff eines Clients auf einen Vorgang zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="13c9f-115">The following example shows how to use a business rule script to check a client's access to an operation.</span></span> <span data-ttu-id="13c9f-116">Im Beispiel wird davon ausgegangen, dass ein vorhandener XML-Richtlinien Speicher namens MyStore.xml im Stammverzeichnis des Laufwerks C vorhanden ist und dass dieser Speicher eine Anwendung mit dem Namen "Kosten", eine Aufgabe mit dem Namen "Kosten übermitteln" und einen Vorgang mit dem Namen "useformcontrol</span><span class="sxs-lookup"><span data-stu-id="13c9f-116">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, and that this store contains an application named Expense, a task named Submit Expense, and an operation named UseFormControl.</span></span>


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

'  Create a business rule for the Submit Expense task.

'  Open the Submit Expense task.
Dim submitTask
Set submitTask = expenseApp.OpenTask("Submit Expense")

'  Set the business rule language to VBScript.
submitTask.BizRuleLanguage = "VBScript"

'  Create a string with the business rule code.
Dim newline
newline = chr(13)
Dim bizRuleString
bizRuleString = "Dim Amount" + newline _
         +"AzBizRuleContext.BusinessRuleResult = FALSE" + newline _
         +"Amount = AzBizRuleContext.GetParameter(""ExpAmount"")" _
   +newline _
   +"if Amount < 500 then AzBizRuleContext.BusinessRuleResult = TRUE"

'  Assign the business rule to the Submit Expense task.
submitTask.BizRule = bizRuleString
                
'  Save the task information to the store.
submitTask.Submit

'  Open the operation to check.
Dim formOperation
Set formOperation = expenseApp.OpenOperation("UseFormControl")

'  Get the ID of the operation.
Dim operationID
operationID = formOperation.OperationID

'  Set up arrays for operations and results.
Dim Operations(1)
Operations(0) = operationID
Dim Results

'  Set up business rule parameters.
Dim bizNames(1)
Dim bizValues(1)
bizNames(0) = "ExpAmount"
bizValues(0) = 100

'  Check access.
Results = clientContext.AccessCheck _
    ("UseFormControl", Empty, Operations, bizNames, bizValues)
 
%>
```



 

 



