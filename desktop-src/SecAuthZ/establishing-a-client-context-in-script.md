---
description: Zum Einrichten eines Client Kontexts im Skript kann eine Anwendung einen Client Kontext mit einem Handle für ein Token, einen Domänen-und Benutzernamen oder eine Zeichen folgen Darstellung der Sicherheits-ID des Clients erstellen.
ms.assetid: 94fb79e4-7e9f-4fef-8ca5-b2000a92efab
title: Einrichten eines Client Kontexts im Skript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 63c0381834a42d10a03b02ee949f8fe4bf7560bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867223"
---
# <a name="establishing-a-client-context-in-script"></a>Einrichten eines Client Kontexts im Skript

Im Autorisierungs-Manager bestimmt eine Anwendung, ob ein Client Zugriff auf einen Vorgang erhält, indem die [**Access Check**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) -Methode eines [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) -Objekts aufgerufen wird, das einen Client Kontext darstellt.

Eine Anwendung kann einen Client Kontext mit einem Handle für ein Token, einen Domänen-und Benutzernamen oder eine Zeichen folgen Darstellung der [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -ID (SID) des Clients erstellen.

Verwenden Sie die Methoden [**InitializeClientContextFromToken**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken), [**InitializeClientContextFromName**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname)und [**InitializeClientContextFromStringSID**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid) eines [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) -Objekts, um einen Client Kontext zu erstellen.

Im folgenden Beispiel wird gezeigt, wie ein [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) -Objekt anhand eines Client namens erstellt wird. Im Beispiel wird davon ausgegangen, dass ein vorhandener XML-Richtlinien Speicher namens MyStore.xml im Stammverzeichnis des Laufwerks C vorhanden ist und dass dieser Speicher eine Anwendung mit dem Namen "Aufwendungen" enthält.


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

%>
```



 

 
