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
# <a name="verifying-client-access-to-requested-resources-in-script"></a>Überprüfen des Client Zugriffs auf angeforderte Ressourcen im Skript

Ruft die [**Access Check**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) -Methode eines [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) -Objekts auf, um zu überprüfen, ob der Client Zugriff auf einen oder mehrere Vorgänge hat. Weitere Informationen zum Erstellen eines **IAzClientContext** -Objekts finden Sie unter [Einrichten eines Client Kontexts im Skript](establishing-a-client-context-in-script.md).

Ein Client kann möglicherweise Mitglied mehrerer Rollen sein, und ein Vorgang kann mehr als einer Aufgabe zugewiesen werden, sodass der Autorisierungs-Manager alle Rollen und Tasks prüft. Wenn eine Rolle, zu der der Client gehört, einen Task enthält, der einen Vorgang enthält, wird der Zugriff auf diesen Vorgang gewährt.

Um den Zugriff nur für eine einzige Rolle zu überprüfen, zu der der Client gehört, legen Sie die [**roleforaccesscheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) -Eigenschaft des [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) -Objekts fest.

Wenn Sie den Autorisierungs Richtlinien Speicher für die Zugriffs Überprüfung initialisieren, müssen Sie NULL als Wert des *lFlags* -Parameters der [**Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) -Methode des [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) -Objekts übergeben.

Es ist auch möglich, Geschäftslogik zur Laufzeit anzuwenden, um den Zugriff zu qualifizieren. Informationen zum Qualifizieren des Zugriffs mit Geschäftslogik finden Sie unter [qualifizieren des Zugriffs mit Geschäftslogik in Skripts](qualifying-access-with-business-logic-in-script.md).

Im folgenden Beispiel wird gezeigt, wie der Zugriff eines Clients auf einen Vorgang überprüft wird. Im Beispiel wird davon ausgegangen, dass ein vorhandener XML-Richtlinien Speicher namens MyStore.xml im Stammverzeichnis des Laufwerks C vorhanden ist und dass dieser Speicher eine Anwendung mit dem Namen "Aufwendungen" und einen Vorgang mit dem Namen "useformcontrol" enthält.


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



 

 



