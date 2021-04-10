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
# <a name="establishing-a-client-context-in-script"></a><span data-ttu-id="3928b-103">Einrichten eines Client Kontexts im Skript</span><span class="sxs-lookup"><span data-stu-id="3928b-103">Establishing a Client Context in Script</span></span>

<span data-ttu-id="3928b-104">Im Autorisierungs-Manager bestimmt eine Anwendung, ob ein Client Zugriff auf einen Vorgang erhält, indem die [**Access Check**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) -Methode eines [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) -Objekts aufgerufen wird, das einen Client Kontext darstellt.</span><span class="sxs-lookup"><span data-stu-id="3928b-104">In Authorization Manager, an application determines whether a client is given access to an operation by calling the [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method of an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object, which represents a client context.</span></span>

<span data-ttu-id="3928b-105">Eine Anwendung kann einen Client Kontext mit einem Handle für ein Token, einen Domänen-und Benutzernamen oder eine Zeichen folgen Darstellung der [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -ID (SID) des Clients erstellen.</span><span class="sxs-lookup"><span data-stu-id="3928b-105">An application can create a client context with a handle to a token, a domain and user name, or a string representation of the [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) of the client.</span></span>

<span data-ttu-id="3928b-106">Verwenden Sie die Methoden [**InitializeClientContextFromToken**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken), [**InitializeClientContextFromName**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname)und [**InitializeClientContextFromStringSID**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid) eines [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) -Objekts, um einen Client Kontext zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3928b-106">Use the [**InitializeClientContextFromToken**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken), [**InitializeClientContextFromName**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname), and [**InitializeClientContextFromStringSid**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid) methods of an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object to create a client context.</span></span>

<span data-ttu-id="3928b-107">Im folgenden Beispiel wird gezeigt, wie ein [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) -Objekt anhand eines Client namens erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3928b-107">The following example shows how to create an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object from a client name.</span></span> <span data-ttu-id="3928b-108">Im Beispiel wird davon ausgegangen, dass ein vorhandener XML-Richtlinien Speicher namens MyStore.xml im Stammverzeichnis des Laufwerks C vorhanden ist und dass dieser Speicher eine Anwendung mit dem Namen "Aufwendungen" enthält.</span><span class="sxs-lookup"><span data-stu-id="3928b-108">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, and that this store contains an application named Expense.</span></span>


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



 

 
