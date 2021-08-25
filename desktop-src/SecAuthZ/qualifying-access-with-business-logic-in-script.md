---
description: Verwenden von Geschäftsregelskripts in Skripts, um Laufzeitlogik für die Überprüfung des Zugriffs bereitzustellen.
ms.assetid: 10c28ecb-3f36-45a8-b037-7038e8927b6b
title: Qualifizieren des Zugriffs mit Geschäftslogik in Skripts
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b77ff1d6d520780d30efab5619c3e9bc3c896ad88315fba56e3a19e05d3ae97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907550"
---
# <a name="qualifying-access-with-business-logic-in-script"></a>Qualifizieren des Zugriffs mit Geschäftslogik in Skripts

Verwenden Sie Geschäftsregelskripts, um Laufzeitlogik zum Überprüfen des Zugriffs bereitzustellen. Weitere Informationen zu Geschäftsregeln finden Sie unter [Business Rules](business-rules.md).

Um einer Aufgabe eine Geschäftsregel zuzuweisen, legen Sie zunächst die [**BizRuleLanguage-Eigenschaft**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) des [**IAzTask-Objekts**](/windows/desktop/api/Azroles/nn-azroles-iaztask) fest, das die Aufgabe darstellt. Das Skript muss mit der Programmiersprache Visual Basic Scripting Edition (VBScript) oder JScript Entwicklungssoftware geschrieben werden. Nachdem Sie die Skriptsprache angegeben haben, legen Sie die [**BizRule-Eigenschaft**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) des **IAzTask-Objekts** mit einer Zeichenfolgendarstellung des Skripts fest.

Beim Überprüfen des Zugriffs auf einen Vorgang, der in einer Aufgabe enthalten ist, der eine Geschäftsregel zugeordnet ist, muss die Anwendung zwei Arrays derselben Größe erstellen, die als *varParameterNames-* und *varParameterValues-Parameter* der [**AccessCheck-Methode**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) eines [**IAzClientContext-Objekts**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) übergeben werden. Informationen zum Erstellen eines Clientkontexts finden Sie unter [Einrichten eines Clientkontexts in Skript](establishing-a-client-context-in-script.md).

Die [**AccessCheck-Methode**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) erstellt ein [**AzBizRuleContext-Objekt,**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) das an das Geschäftsregelskript übergeben wird. Das Skript legt dann die [**BusinessRuleResult-Eigenschaft**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) des **AzBizRuleContext-Objekts** fest. Der Wert **True** gibt an, dass der Zugriff gewährt wird, und der Wert **False** gibt an, dass der Zugriff verweigert wird.

Ein Geschäftsregelskript kann keinem [**IAzTask-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iaztask) zugewiesen werden, das in einem delegierten [**IAzScope-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iazscope) enthalten ist.

Das folgende Beispiel zeigt die Verwendung eines Geschäftsregelskripts, um den Zugriff eines Clients auf einen Vorgang zu überprüfen. Im Beispiel wird davon ausgegangen, dass im Stammverzeichnis von Laufwerk C ein vorhandener XML-Richtlinienspeicher mit dem Namen MyStore.xml vorhanden ist und dass dieser Speicher eine Anwendung mit dem Namen Expense, eine Aufgabe namens Submit Expense und einen Vorgang namens UseFormControl enthält.


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



 

 



