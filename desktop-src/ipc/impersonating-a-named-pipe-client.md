---
description: Identitätswechsel ist die Fähigkeit eines Threads, in einem anderen Sicherheitskontext als dem prozess, der den Thread besitzt, auszuführen.
ms.assetid: 1bde4d4d-958e-45f4-8cdb-0572adcaa3ac
title: Identitätswechsel für einen Named Pipe-Client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6f0cb51acb09be9774fd67bae7a176c75156b28fb5b03f398202ee8ad9cbc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350400"
---
# <a name="impersonating-a-named-pipe-client"></a>Identitätswechsel für einen Named Pipe-Client

*Identitätswechsel ist* die Fähigkeit eines Threads, in einem anderen Sicherheitskontext als dem prozess, der den Thread besitzt, auszuführen. Der Identitätswechsel ermöglicht dem Serverthread das Ausführen von Aktionen im Namen des Clients, jedoch innerhalb der Grenzen des Sicherheitskontexts des Clients. Der Client verfügt in der Regel über weniger Zugriffsrechte. Weitere Informationen finden Sie unter [Identitätswechsel.](/windows/desktop/SecAuthZ/client-impersonation)

Ein Named Pipe-Serverthread kann die [**ImpersonateNamedPipeClient-Funktion**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) aufrufen, um das Zugriffstoken des Benutzers anzunehmen, der mit dem Clientende der Pipe verbunden ist. Beispielsweise kann ein Named Pipe-Server Zugriff auf eine Datenbank oder ein Dateisystem bereitstellen, auf die der Pipeserver privilegierten Zugriff hat. Wenn ein Pipeclient eine Anforderung an den Server sendet, wird vom Server die Identität des Clients angenommen und versucht, auf die geschützte Datenbank zu zugreifen. Das System gewährt oder verweigert dann den Zugriff des Servers basierend auf der Sicherheitsstufe des Clients. Wenn der Server fertig ist, verwendet er die [**RevertToSelf-Funktion,**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) um das ursprüngliche Sicherheitstoken wiederherzustellen.

Die [Ebene des Identitätswechsels bestimmt](/windows/desktop/SecAuthZ/impersonation-levels) die Vorgänge, die der Server beim Identitätswechsel des Clients ausführen kann. Standardmäßig wird die Identität eines Servers auf der Identitätswechselebene SecurityImpersonation angenommen. Wenn der Client jedoch die [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) aufruft, um ein Handle für das Clientende der Pipe zu öffnen, kann der Client das SECURITY SQOS PRESENT-Flag verwenden, um die Identitätswechselebene des Servers zu \_ \_ steuern.

 

 
