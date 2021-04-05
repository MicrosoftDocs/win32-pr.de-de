---
title: Ankündigen von Server Schnittstellen
description: Die Serverseite einer Anwendung, die automatische Handles verwendet, muss die Funktion rpcnsbindingexport aufrufen, um den Clients Bindungs Informationen zum Server zur Verfügung zu stellen.
ms.assetid: d15fd8da-3afd-4031-95d1-b76a0ad9a20d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45955ac7228018d8ddebbc7c156031648091b6f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037009"
---
# <a name="advertising-server-interfaces"></a><span data-ttu-id="1ebfc-103">Ankündigen von Server Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1ebfc-103">Advertising Server Interfaces</span></span>

<span data-ttu-id="1ebfc-104">Die Serverseite einer Anwendung, die automatische Handles verwendet, muss die Funktion [**rpcnsbindingexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) aufrufen, um den Clients Bindungs Informationen zum Server zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="1ebfc-104">The server side of an application that uses automatic handles must call the function [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) to make binding information about the server available to clients.</span></span> <span data-ttu-id="1ebfc-105">Automatische Bindungs Handles erfordern einen Namensdienst, der auf einem Server ausgeführt wird, auf den der Client zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="1ebfc-105">Automatic binding handles require a name service running on a server that is accessible to the client.</span></span> <span data-ttu-id="1ebfc-106">Die Microsoft-Implementierung des Namens Dienstanbieter, Microsoft Locator, verwaltet automatische Handles.</span><span class="sxs-lookup"><span data-stu-id="1ebfc-106">The Microsoft implementation of the name service, Microsoft Locator, manages automatic handles.</span></span> <span data-ttu-id="1ebfc-107">Server Anwendungen, die implizite und explizite Bindungs Handles verwenden, können auch Ihre Anwesenheit in der Name Service-Datenbank ankündigen.</span><span class="sxs-lookup"><span data-stu-id="1ebfc-107">Server applications that use implicit and explicit binding handles can also advertise their presence in the name service database.</span></span>

<span data-ttu-id="1ebfc-108">In der Regel ruft der Server die folgenden Lauf Zeitfunktionen auf:</span><span class="sxs-lookup"><span data-stu-id="1ebfc-108">Typically, the server calls the following run-time functions:</span></span>

``` syntax
/* auto handle server application (fragment) */
 
//interface header file that the MIDL compiler generates
#include "auto.h" 
 
void main(void)
{
    RpcUseProtseqEp(...);
    RpcServerRegisterIf(...);
    RpcServerInqBindings(...);
    RpcNsBindingExport(...);
    ...
}
```

<span data-ttu-id="1ebfc-109">Die Aufrufe der ersten beiden Funktionen in diesem Code Fragment ähneln dem [Hello, World-Beispiel](tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="1ebfc-109">The calls to the first two functions in this code fragment are similar to the [Hello, World example](tutorial.md).</span></span> <span data-ttu-id="1ebfc-110">Diese Funktionen machen Informationen über die Bindung für den Client verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1ebfc-110">These functions make information about the binding available to the client.</span></span> <span data-ttu-id="1ebfc-111">Mit den Aufrufen von [**rpcserverinqbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) und [**rpcnsbindingexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) werden die Informationen in die Name Service-Datenbank eingefügt.</span><span class="sxs-lookup"><span data-stu-id="1ebfc-111">The calls to [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) and [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) put the information in the name service database.</span></span> <span data-ttu-id="1ebfc-112">Der Aufrufe von [**rpcserverinqbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) füllt den Bindungs Vektor mit gültigen Bindungs Handles aus, bevor die Handles in den Namensdienst exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="1ebfc-112">The call to [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) fills the binding vector with valid binding handles before the handles are exported to the name service.</span></span> <span data-ttu-id="1ebfc-113">Nachdem das Serverprogramm die Handles in die-Datenbank exportiert hat, kann der Client (oder Clientstub) [**rpcnsbindingimportbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) und [**rpcnsbindingimportnext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) abrufen, um diese Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1ebfc-113">After the server program exports the handles to the database, the client (or client stubs) can call [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) and [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) to obtain this information.</span></span> <span data-ttu-id="1ebfc-114">Weitere Informationen finden Sie untersuchen von [Server Host Systemen](finding-server-host-systems.md).</span><span class="sxs-lookup"><span data-stu-id="1ebfc-114">For details, see [Finding Server Host Systems](finding-server-host-systems.md).</span></span>

<span data-ttu-id="1ebfc-115">Die Aufrufe von [**rpcserverinqbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) und [**rpcnsbindingexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) und deren zugeordneten Datenstrukturen sehen etwa wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="1ebfc-115">The calls to [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) and [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) and their associated data structures look similar to the following:</span></span>

``` syntax
RPC_BINDING_VECTOR * pBindingVector;
RPCSTATUS status;
 
status = RpcServerInqBindings(&pBindingVector);
 
status = RpcNsBindingExport(
                fNameSyntaxType,      // name syntax type 
                pszAutoEntryName,     // nsi entry name 
                autoh_ServerIfHandle, // if server handle
                pBindingVector,       // set in previous call 
                NULL);                // UUID vector
```

<span data-ttu-id="1ebfc-116">Beachten Sie, dass der [**rpcserverinqbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) -Parameter *pbindingvector* ein Zeiger auf einen Zeiger auf den [**RPC- \_ Bindungs \_ Vektor**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector)ist.</span><span class="sxs-lookup"><span data-stu-id="1ebfc-116">Note that the [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) parameter *pBindingVector* is a pointer to a pointer to [**RPC\_BINDING\_VECTOR**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector).</span></span> <span data-ttu-id="1ebfc-117">Beachten Sie auch, dass auf jeden Aufrufen von [**rpcnsbindingexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) ein Aufrufen von [**rpcbindingvectorfree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree)folgen muss.</span><span class="sxs-lookup"><span data-stu-id="1ebfc-117">Also remember that each call to [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) must be followed by a call to [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree).</span></span>

<span data-ttu-id="1ebfc-118">Zum Entfernen der exportierten Schnittstelle aus der Name Service-Datenbank ruft der Server [**rpcnsbindingunexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) auf, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="1ebfc-118">To remove the exported interface from the name service database, the server calls [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) as shown:</span></span>

``` syntax
status = RpcNsBindingUnexport(
                fNameSyntaxType, 
                pszAutoEntryName,  
                auto_ServerIfHandle,
                NULL);              // unexport handles only
```

<span data-ttu-id="1ebfc-119">Die [**rpcnsbindingunexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) -Funktion sollte nur verwendet werden, wenn der Dienst dauerhaft entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="1ebfc-119">The [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) function should be used only when the service is being permanently removed.</span></span> <span data-ttu-id="1ebfc-120">Er sollte nicht verwendet werden, wenn der Dienst vorübergehend deaktiviert wird, z. b. wenn der Server zur Wartung heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="1ebfc-120">It should not be used when the service is temporarily disabled, such as when the server is shut down for maintenance.</span></span> <span data-ttu-id="1ebfc-121">Ein Serverprogramm kann sich selbst bei der Name Service-Datenbank registrieren, ist aber nicht verfügbar, da der Server vorübergehend offline ist.</span><span class="sxs-lookup"><span data-stu-id="1ebfc-121">A server program can register itself with the name service database, yet be unavailable because the server is temporarily offline.</span></span> <span data-ttu-id="1ebfc-122">Die Client Anwendung sollte Ausnahme Behandlungs Code für eine solche Bedingung enthalten.</span><span class="sxs-lookup"><span data-stu-id="1ebfc-122">The client application should contain exception-handling code for such a condition.</span></span>

<span data-ttu-id="1ebfc-123">Weitere Informationen zum Inhalt und Format der Name Service-Datenbank finden Sie [unter RPC Name Service Database](the-rpc-name-service-database.md).</span><span class="sxs-lookup"><span data-stu-id="1ebfc-123">For more information on the content and format of the name service database, see [The RPC Name Service Database](the-rpc-name-service-database.md).</span></span>

<span data-ttu-id="1ebfc-124">Anwendungen können den Active Directory-Dienst nutzen, wenn die Client-und Serverprogramme unter Windows 2000 ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1ebfc-124">Applications can utilize the Active Directory service if both the client and server programs are running under Windows 2000.</span></span> <span data-ttu-id="1ebfc-125">Die Computer, auf denen die-Client-und-Serverprogramme ausgeführt werden, müssen Mitglieder einer Windows 2000-Domäne sein.</span><span class="sxs-lookup"><span data-stu-id="1ebfc-125">The computers running the client and server programs must both be members of a Windows 2000 domain.</span></span>

<span data-ttu-id="1ebfc-126">Um seine Anwesenheit mit dem Active Directory-Dienst ankündigen zu können, sollte das Serverprogramm im Sicherheitskontext eines Domänen Administrators ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1ebfc-126">To advertise its presence using the Active Directory service, the server program should run in the security context of a domain administrator.</span></span> <span data-ttu-id="1ebfc-127">Wenn Sie im Kontext von Domänen Benutzern ausgeführt wird, muss ein Domänen Administrator die Zugriffs Steuerungs Liste (ACL) für den RPC-Dienst Container ändern.</span><span class="sxs-lookup"><span data-stu-id="1ebfc-127">If it is running in the context of domain users, a domain administrator must modify the access control list (ACL) on the RPC Services container.</span></span> <span data-ttu-id="1ebfc-128">Weitere Informationen finden Sie in der Active Directory-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="1ebfc-128">For more information, see the Active Directory documentation.</span></span>

 

 




