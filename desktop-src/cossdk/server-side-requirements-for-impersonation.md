---
description: Server-Side Anforderungen für den Identitätswechsel
ms.assetid: f6128688-dfd8-40ff-83ec-99d740b9152c
title: Server-Side Anforderungen für den Identitätswechsel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30edbebd37035ab7a7f4ca09e1cff73c2afbabe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342763"
---
# <a name="server-side-requirements-for-impersonation"></a>Server-Side Anforderungen für den Identitätswechsel

Der Server führt den Identitätswechsel Programm gesteuert aus. Die Sicherheits Anmelde Informationen des Clients werden mithilfe von " [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)" explizit angenommen. Wenn der Client die ausreichende Berechtigung für den Server erteilt hat, besteht die Auswirkung, dass die Sicherheits Anmelde Informationen des Clients anstelle des Prozess Tokens durch das Thread Token des Servers ersetzt werden.

Wenn dies der Fall ist, kann der Server z. b. das Client Token für den Zugriff auf Ressourcen verwenden, die mit einer Sicherheits Beschreibung geschützt werden. Oder es können Aufrufe unter der Client Identität durchführen, wenn das Cloaking aktiviert ist.

Der Server kann das Cloaking Programm gesteuert explizit festlegen, oder er kann sich auf eine administrative Einstellung verlassen. Standardmäßig sind com+-Anwendungen für die Verwendung von dynamischem Cloaking konfiguriert. Weitere Details finden Sie unter [Cloaking](cloaking.md).

Wenn der Server die Delegierung im Namen des Clients implementiert – unter Verwendung der Client Identität über das Netzwerk – muss die Server Prozess Identität im Active Directory Dienst als "vertrauenswürdig für die Delegierung" gekennzeichnet werden. Andernfalls tritt bei der Delegierung ein Fehler auf.

Wenn die Client Identität nicht mehr verwendet wird, kann der Server mithilfe von [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)auf das eigene Prozess Token zurückgreifen.

Ausführliche Informationen zum Implementieren des Identitäts Wechsels und der Delegierung finden Sie unter [Delegierung und](/windows/desktop/com/delegation-and-impersonation)Identitätswechsel.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Client Identitätswechsel und Delegierung](client-impersonation-and-delegation.md)
</dt> <dt>

[Client seitige Anforderungen für Identitätswechsel](client-side-requirements-for-impersonation.md)
</dt> <dt>

[Cloaking](cloaking.md)
</dt> </dl>

 

 
