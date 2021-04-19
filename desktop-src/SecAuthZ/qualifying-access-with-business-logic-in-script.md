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
# <a name="qualifying-access-with-business-logic-in-script"></a>Qualifizieren des Zugriffs mit Geschäftslogik in Skripts

Verwenden Sie Geschäftsregel Skripts, um Lauf Zeit Logik zum Überprüfen des Zugriffs bereitzustellen. Weitere Informationen zu Geschäftsregeln finden Sie unter [Geschäftsregeln](business-rules.md).

Um einer Aufgabe eine Geschäftsregel zuzuweisen, legen Sie zunächst die Eigenschaft [**BizRuleLanguage**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) des [**iaztask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) -Objekts fest, das die Aufgabe darstellt. Das Skript muss mithilfe der Visual Basic Scripting Edition Programmiersprache (VBScript) oder der JScript-Entwicklungssoftware geschrieben werden. Nachdem Sie die Skriptsprache angegeben haben, legen Sie die Eigenschaft [**BizRule**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) des **iaztask** -Objekts auf eine Zeichen folgen Darstellung des Skripts fest.

Beim Überprüfen des Zugriffs für einen Vorgang, der in einem Task enthalten ist, dem eine Geschäftsregel zugeordnet ist, muss die Anwendung zwei Arrays derselben Größe erstellen, die als Parameter des Typs " *varParameterNames* " und " *varParameterValues* " der [**Access Check**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) -Methode eines [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) -Objekts übermittelt werden. Weitere Informationen zum Erstellen eines Client Kontexts finden Sie unter [Einrichten eines Client Kontexts in einem Skript](establishing-a-client-context-in-script.md).

Die [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) -Methode erstellt ein [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) -Objekt, das an das Geschäftsregel Skript übergeben wird. Das Skript legt dann die Eigenschaft [**BusinessRuleResult**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) des **AzBizRuleContext** -Objekts fest. Der Wert **true** gibt an, dass der Zugriff gewährt wird, und der Wert **false** gibt an, dass der Zugriff verweigert wird.

Einem [**iaztask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) -Objekt, das in einem Delegierten [**iazscope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) -Objekt enthalten ist, kann kein Geschäftsregel Skript zugewiesen werden.

Im folgenden Beispiel wird gezeigt, wie ein Geschäftsregel Skript verwendet wird, um den Zugriff eines Clients auf einen Vorgang zu überprüfen. Im Beispiel wird davon ausgegangen, dass ein vorhandener XML-Richtlinien Speicher namens MyStore.xml im Stammverzeichnis des Laufwerks C vorhanden ist und dass dieser Speicher eine Anwendung mit dem Namen "Kosten", eine Aufgabe mit dem Namen "Kosten übermitteln" und einen Vorgang mit dem Namen "useformcontrol


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



 

 



