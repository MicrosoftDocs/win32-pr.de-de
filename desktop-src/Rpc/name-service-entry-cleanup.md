---
title: Bereinigung der Namensdienst Einträge
description: Ein Name-Dienst Eintrag sollte Informationen enthalten, die sich nicht häufig ändern.
ms.assetid: b581bc10-e537-4714-b89a-d998fec23360
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf0ed6a21074a49a472d7505dcfea37cf182026
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037295"
---
# <a name="name-service-entry-cleanup"></a>Bereinigung der Namensdienst Einträge

Ein Name-Dienst Eintrag sollte Informationen enthalten, die sich nicht häufig ändern. Schließen Sie aus diesem Grund keine dynamischen Endpunkte in die exportierten Bindungs Handles ein, da Sie bei jedem Aufruf des Servers geändert werden und den Namen des Namens dienstantrags gruppieren. Um diese Bindungs Handles zu entfernen, verwenden Sie [**rpcbindingreset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset).

Eine angemessene Sequenz von Server Vorgängen wäre z. b. wie folgt:

Für mehr als einen Transport:

``` syntax
RpcServerUseProtseq();
RpcServerUseProtseq();
```

So platzieren Sie Bindungen in der Endpunkt Zuordnung:

``` syntax
RpcServerInqBindings(&Vector);
RpcEpRegister(Interface, Vector);
```

So entfernen Sie Endpunkte aus Bindungen:

``` syntax
for (i=0; i < Vector- > Count; + + i)
{
    RpcBindingReset(Vector->BindingH[i];
}
```

So fügen Sie Bindungen zum Namensdienst hinzu:

``` syntax
RpcNsBindingExport(RPC_C_NS_SYNTAX_DEFAULT, EntryName, Interface
                   Vector);
RpcServerListen();
```

 

 




