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
# <a name="advertising-server-interfaces"></a>Ankündigen von Server Schnittstellen

Die Serverseite einer Anwendung, die automatische Handles verwendet, muss die Funktion [**rpcnsbindingexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) aufrufen, um den Clients Bindungs Informationen zum Server zur Verfügung zu stellen. Automatische Bindungs Handles erfordern einen Namensdienst, der auf einem Server ausgeführt wird, auf den der Client zugreifen kann. Die Microsoft-Implementierung des Namens Dienstanbieter, Microsoft Locator, verwaltet automatische Handles. Server Anwendungen, die implizite und explizite Bindungs Handles verwenden, können auch Ihre Anwesenheit in der Name Service-Datenbank ankündigen.

In der Regel ruft der Server die folgenden Lauf Zeitfunktionen auf:

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

Die Aufrufe der ersten beiden Funktionen in diesem Code Fragment ähneln dem [Hello, World-Beispiel](tutorial.md). Diese Funktionen machen Informationen über die Bindung für den Client verfügbar. Mit den Aufrufen von [**rpcserverinqbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) und [**rpcnsbindingexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) werden die Informationen in die Name Service-Datenbank eingefügt. Der Aufrufe von [**rpcserverinqbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) füllt den Bindungs Vektor mit gültigen Bindungs Handles aus, bevor die Handles in den Namensdienst exportiert werden. Nachdem das Serverprogramm die Handles in die-Datenbank exportiert hat, kann der Client (oder Clientstub) [**rpcnsbindingimportbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) und [**rpcnsbindingimportnext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) abrufen, um diese Informationen zu erhalten. Weitere Informationen finden Sie untersuchen von [Server Host Systemen](finding-server-host-systems.md).

Die Aufrufe von [**rpcserverinqbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) und [**rpcnsbindingexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) und deren zugeordneten Datenstrukturen sehen etwa wie folgt aus:

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

Beachten Sie, dass der [**rpcserverinqbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) -Parameter *pbindingvector* ein Zeiger auf einen Zeiger auf den [**RPC- \_ Bindungs \_ Vektor**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector)ist. Beachten Sie auch, dass auf jeden Aufrufen von [**rpcnsbindingexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) ein Aufrufen von [**rpcbindingvectorfree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree)folgen muss.

Zum Entfernen der exportierten Schnittstelle aus der Name Service-Datenbank ruft der Server [**rpcnsbindingunexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) auf, wie hier gezeigt:

``` syntax
status = RpcNsBindingUnexport(
                fNameSyntaxType, 
                pszAutoEntryName,  
                auto_ServerIfHandle,
                NULL);              // unexport handles only
```

Die [**rpcnsbindingunexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) -Funktion sollte nur verwendet werden, wenn der Dienst dauerhaft entfernt wird. Er sollte nicht verwendet werden, wenn der Dienst vorübergehend deaktiviert wird, z. b. wenn der Server zur Wartung heruntergefahren wird. Ein Serverprogramm kann sich selbst bei der Name Service-Datenbank registrieren, ist aber nicht verfügbar, da der Server vorübergehend offline ist. Die Client Anwendung sollte Ausnahme Behandlungs Code für eine solche Bedingung enthalten.

Weitere Informationen zum Inhalt und Format der Name Service-Datenbank finden Sie [unter RPC Name Service Database](the-rpc-name-service-database.md).

Anwendungen können den Active Directory-Dienst nutzen, wenn die Client-und Serverprogramme unter Windows 2000 ausgeführt werden. Die Computer, auf denen die-Client-und-Serverprogramme ausgeführt werden, müssen Mitglieder einer Windows 2000-Domäne sein.

Um seine Anwesenheit mit dem Active Directory-Dienst ankündigen zu können, sollte das Serverprogramm im Sicherheitskontext eines Domänen Administrators ausgeführt werden. Wenn Sie im Kontext von Domänen Benutzern ausgeführt wird, muss ein Domänen Administrator die Zugriffs Steuerungs Liste (ACL) für den RPC-Dienst Container ändern. Weitere Informationen finden Sie in der Active Directory-Dokumentation.

 

 




