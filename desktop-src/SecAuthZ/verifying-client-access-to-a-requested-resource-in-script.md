---
description: Rufen Sie die IAzClientContext::AccessCheck-Methode auf, um zu überprüfen, ob der Client Zugriff auf einen oder mehrere Vorgänge hat.
ms.assetid: cf1070fe-3737-4ae6-a8ef-f0782418a1d5
title: Überprüfen des Clientzugriffs auf angeforderte Ressourcen im Skript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7393001c63f0a5b605870a8498e76231f0bf620a8c7e819a8c624eace565499a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906700"
---
# <a name="verifying-client-access-to-requested-resources-in-script"></a>Überprüfen des Clientzugriffs auf angeforderte Ressourcen im Skript

Rufen Sie die [**AccessCheck-Methode**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) eines [**IAzClientContext-Objekts**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) auf, um zu überprüfen, ob der Client Zugriff auf einen oder mehrere Vorgänge hat. Informationen zum Erstellen eines **IAzClientContext-Objekts** finden Sie unter [Einrichten eines Clientkontexts in Script](establishing-a-client-context-in-script.md).

Ein Client kann über eine Mitgliedschaft in mehr als einer Rolle verfügen, und ein Vorgang kann mehr als einer Aufgabe zugewiesen werden, sodass der Autorisierungs-Manager alle Rollen und Aufgaben überprüft. Wenn eine Rolle, zu der der Client gehört, einen Task enthält, der einen Vorgang enthält, wird Der Zugriff auf diesen Vorgang gewährt.

Um den Zugriff nur auf eine einzelne Rolle zu überprüfen, zu der der Client gehört, legen Sie die [**RoleForAccessCheck-Eigenschaft**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) des [**IAzClientContext-Objekts**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) fest.

Beim Initialisieren des Autorisierungsrichtlinienspeichers für die Zugriffsüberprüfung müssen Sie 0 (null) als Wert des *lFlags-Parameters* der [**Initialize-Methode**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) des [**AzAuthorizationStore-Objekts**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) übergeben.

Es ist auch möglich, Geschäftslogik zur Laufzeit anzuwenden, um den Zugriff zu qualifizieren. Informationen zum Qualifizieren des Zugriffs mit Geschäftslogik finden Sie unter [Qualifizieren des Zugriffs mit Geschäftslogik in Script.](qualifying-access-with-business-logic-in-script.md)

Das folgende Beispiel zeigt, wie der Zugriff eines Clients auf einen Vorgang überprüft wird. Im Beispiel wird davon ausgegangen, dass im Stammverzeichnis von Laufwerk C ein XML-Richtlinienspeicher namens MyStore.xml vorhanden ist und dass dieser Speicher eine Anwendung mit dem Namen Expense und einen Vorgang namens UseFormControl enthält.


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



 

 



