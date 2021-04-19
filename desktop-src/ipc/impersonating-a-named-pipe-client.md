---
description: Identitätswechsel ist die Fähigkeit eines Threads, in einem anderen Sicherheitskontext als dem Prozess auszuführen, der den Thread besitzt.
ms.assetid: 1bde4d4d-958e-45f4-8cdb-0572adcaa3ac
title: Annehmen der Identität eines Named Pipe-Clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586de99ae24ba9bab8b65ba4cb1a3a91922aa9d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343031"
---
# <a name="impersonating-a-named-pipe-client"></a>Annehmen der Identität eines Named Pipe-Clients

Identitäts *Wechsel ist die* Fähigkeit eines Threads, in einem anderen Sicherheitskontext als dem Prozess auszuführen, der den Thread besitzt. Durch den Identitätswechsel kann der Server Thread Aktionen im Namen des Clients durchführen, jedoch innerhalb der Grenzen des Sicherheits Kontexts des Clients. Der Client verfügt in der Regel über weniger Zugriffsrechte. Weitere Informationen finden Sie unter Identitäts [Wechsel.](/windows/desktop/SecAuthZ/client-impersonation)

Ein Named Pipe Server Thread kann die Funktion "Identitäts- [**amedpipeclient**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) " aufrufen, um das Zugriffs Token des Benutzers anzunehmen, der mit dem Client Ende der Pipe verbunden ist. Beispielsweise kann ein Named Pipe Server Zugriff auf eine Datenbank oder ein Dateisystem bereitstellen, für die der Pipeserver über privilegierten Zugriff verfügt. Wenn ein Pipe-Client eine Anforderung an den Server sendet, nimmt der Server die Identität des Clients an und versucht, auf die geschützte Datenbank zuzugreifen. Das System gewährt oder verweigert den Server Zugriff basierend auf der Sicherheitsstufe des Clients. Wenn der Server fertiggestellt ist, wird die Funktion [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) verwendet, um das ursprüngliche Sicherheits Token wiederherzustellen.

Die Identitätswechsel [Ebene](/windows/desktop/SecAuthZ/impersonation-levels) bestimmt die Vorgänge, die der Server ausführen kann, während die Identität des Clients angenommen wird. Standardmäßig nimmt ein Server einen Identitätswechsel auf der Identitätswechsel Ebene des securityidentitäts Wechsels vor. Wenn der Client jedoch die Funktion "up- [**File**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " aufruft, um ein Handle für das Client Ende der Pipe zu öffnen, kann der Client das \_ Flag "Security sqos Present" verwenden, um die Identitätswechsel \_ Ebene des Servers zu steuern.

 

 
