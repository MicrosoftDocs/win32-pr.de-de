---
title: Anzeigen von Serverschnittstellen
description: Die Serverseite einer Anwendung, die automatische Handles verwendet, muss die Funktion RpcNsBindingExport aufrufen, um Den Clients Bindungsinformationen über den Server zur Verfügung zu stellen.
ms.assetid: d15fd8da-3afd-4031-95d1-b76a0ad9a20d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f81ec4b494c9ce2abd18031e3bf0ed3dd25d55908238ebc7bba96bce57e88f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073600"
---
# <a name="advertising-server-interfaces"></a>Anzeigen von Serverschnittstellen

Die Serverseite einer Anwendung, die automatische Handles verwendet, muss die Funktion [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) aufrufen, um Den Clients Bindungsinformationen über den Server zur Verfügung zu stellen. Automatische Bindungshandles erfordern einen Namensdienst, der auf einem Server ausgeführt wird, auf den der Client zugreifen kann. Die Microsoft-Implementierung des Namensdiensts Microsoft Locator verwaltet automatische Handles. Serveranwendungen, die implizite und explizite Bindungshandles verwenden, können auch ihre Präsenz in der Namensdienstdatenbank ankündigen.

In der Regel ruft der Server die folgenden Laufzeitfunktionen auf:

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

Die Aufrufe der ersten beiden Funktionen in diesem Codefragment ähneln dem [Hello, World-Beispiel.](tutorial.md) Diese Funktionen machen Informationen über die Bindung für den Client verfügbar. Die Aufrufe von [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) und [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) speichern die Informationen in der Namensdienstdatenbank. Durch den Aufruf von [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) wird der Bindungsvektor mit gültigen Bindungshandles gefüllt, bevor die Handles in den Namensdienst exportiert werden. Nachdem das Serverprogramm die Handles in die Datenbank exportiert hat, kann der Client (oder Clientstubs) [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) und [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) aufrufen, um diese Informationen abzurufen. Weitere Informationen finden Sie unter [Suchen von Serverhostsystemen.](finding-server-host-systems.md)

Die Aufrufe von [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) und [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) und den zugehörigen Datenstrukturen sehen in etwa wie folgt aus:

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

Beachten Sie, dass der [**RpcServerInqBindings-Parameter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) *pBindingVector* ein Zeiger auf einen Zeiger auf [**RPC BINDING \_ \_ VECTOR**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector)ist. Denken Sie auch daran, dass jedem Aufruf von [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) ein Aufruf von [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree)folgen muss.

Um die exportierte Schnittstelle aus der Namensdienstdatenbank zu entfernen, ruft der Server [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) auf, wie gezeigt:

``` syntax
status = RpcNsBindingUnexport(
                fNameSyntaxType, 
                pszAutoEntryName,  
                auto_ServerIfHandle,
                NULL);              // unexport handles only
```

Die [**RpcNsBindingUnexport-Funktion**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) sollte nur verwendet werden, wenn der Dienst dauerhaft entfernt wird. Sie sollte nicht verwendet werden, wenn der Dienst vorübergehend deaktiviert ist, z. B. wenn der Server zur Wartung heruntergefahren wird. Ein Serverprogramm kann sich bei der Namensdienstdatenbank registrieren, ist jedoch nicht verfügbar, da der Server vorübergehend offline ist. Die Clientanwendung sollte Ausnahmebehandlungscode für eine solche Bedingung enthalten.

Weitere Informationen zum Inhalt und Format der Namensdienstdatenbank finden Sie unter [The RPC Name Service Database](the-rpc-name-service-database.md).

Anwendungen können den Active Directory-Dienst nutzen, wenn die Client- und Serverprogramme unter Windows 2000 ausgeführt werden. Die Computer, auf denen die Client- und Serverprogramme ausgeführt werden, müssen Mitglieder einer Windows 2000-Domäne sein.

Um seine Präsenz mithilfe des Active Directory-Diensts anzukündigen, sollte das Serverprogramm im Sicherheitskontext eines Domänenadministrators ausgeführt werden. Wenn sie im Kontext von Domänenbenutzern ausgeführt wird, muss ein Domänenadministrator die Zugriffssteuerungsliste (Access Control List, ACL) im RPC Services-Container ändern. Weitere Informationen finden Sie in der Active Directory-Dokumentation.

 

 




